---
title: 'Working with the NRP'
layout: default
---

# sam's notes for getting started with the NRP

following <https://nrp.ai/documentation/userdocs/start/getting-started/>:

```bash
brew install kubectl
brew install kubelogin

mkdir ~/.kube
cd ~/.kube
wget https://nrp.ai/config
cat config # should output around 26 lines of config

kubectl config get-contexts # nautilus should show up in output

# should authenticate in browser, then display a bunch of nodes
kubectl get nodes

# should either output running pods, or:
# "No resources found in dsc-10-llm namespace."
# which means that the command worked
kubectl get pods -n dsc-10-llm

# to set namespace as default
kubectl config set contexts.nautilus.namespace dsc-10-llm
```

Then, I'm following https://nrp.ai/documentation/userdocs/tutorial/basic/ to
start up a pod. Made a `pod1.yaml` file with these contents:

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: test-pod
spec:
  containers:
    - name: mypod
      image: ubuntu
      resources:
        limits:
          memory: 500Mi
          cpu: 500m
        requests:
          memory: 500Mi
          cpu: 500m
      command: ['sh', '-c', "echo 'Im a new pod' && sleep infinity"]
```

Then, ran:

```bash
kubectl create -f pod1.yaml
# pod/test-pod created

# actually, sam had to add info to the namespace before the pod creation could
# work, but that's a one-time thing per namespace so no one else should need
# to worry about that

kubectl get pods
# NAME       READY   STATUS    RESTARTS   AGE
# test-pod   1/1     Running   0          81s

kubectl logs test-pod
# Im a new pod

kubectl exec -it test-pod -- /bin/bash
# logs into a bash shell on pod, Ctrl-D to exit

kubectl delete pod test-pod
# takes a few seconds to fully shut down
```
