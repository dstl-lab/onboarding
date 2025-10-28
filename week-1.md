---
title: Week 1
layout: default
---

# Week 1: Getting Started

{: .note-title}
> Goals
>
> - Set up a modern development environment
> - Understand how to work on the command-line
> - Learn about the `uv` and `npm` package managers and why they are useful
> - Learn our pull request workflow using `git`
> - Make your first pull request (and deal with a merge conflict!)

{: .warning}
> Sam drafted these pages super quickly, so there are probably lots of details
> that he left out! Feel free to send a pull request for any page of these
> guides.


## Development Environment

This is just one recommended setup, feel free to customize as much as you'd
like.

- For Windows users: Install WSL and Ubuntu, super important! Lots of web dev
  stuff breaks on non-WSL environments.
- IDE: VSCode / Cursor
  - Github Copilot is free for students, be sure to use!
- Terminal: iTerm2 / Ghostty

macOS-specific:
- Install `brew` for CLI tools

Watch a tutorial on using VSCode productively, e.g.:
<https://youtu.be/ifTF3ags0XI?si=MDWD-K34sOrKuaVk>.

Follow this guide to set up VSCode / Cursor for Python development:
<https://medium.com/ordinaryindustries/the-ultimate-vs-code-setup-for-python-538026b34d94>


{: .important-title}
> Now, check your knowledge:
>
> 1. What is the difference between Cmd+Shift+P and Cmd+P in VSCode?
> 1. What do `brew` (macOS) or `apt-get` (WSL/Linux) do? What is different
>    about these tools vs. downloading and installing an app on your laptop?
> 1. What are pros and cons of using a GUI like VSCode over a command-line
>    editor like `nano` or `vim`?

## Working on the Command-Line

Walk through each of these lessons of the Missing Semester. Complete the
exercises.

1. <https://missing.csail.mit.edu/2020/course-shell/>
1. <https://missing.csail.mit.edu/2020/shell-tools/>
1. <https://missing.csail.mit.edu/2020/command-line/>
1. <https://missing.csail.mit.edu/2020/version-control/>
1. <https://missing.csail.mit.edu/2020/potpourri/> (No exercises for this one.)

Optional, but recommended: install and set up `fish` as your default shell
instead of `bash`.

Rationale:

- <https://jvns.ca/blog/2017/04/23/the-fish-shell-is-awesome/>
- <https://jvns.ca/blog/2024/09/12/reasons-i--still--love-fish/>


{: .important-title}
> Now, check your knowledge:
>
> 1. What do `~`, `.`, and `..` mean in paths? What is the difference
>    between an absolute path and a relative path?
> 1. What does the `$PATH` environment variable control? How would you add a
>    directory to it for just this session vs. permanently?
> 1. What is the difference between `>`, `>>`, `|`, and `2>`?
> 1. What is the difference between stopping a program with `Ctrl-C` and
>    suspending it with `Ctrl-Z`? How do you resume a suspended job in the
>    foreground and in the background?
> 1. What does the permission string `-rwxr-x---` mean? How do you make a
>    script executable and run it from the current directory?
> 1. In `git`, what is the difference between the working directory, the
>    staging area, and a commit? What is the difference between `git commit`
>    and `git push`?
> 1. How can you quickly search your command history? What does `history` do
>    and how do you trigger reverse search?

## `uv` and `npm`

- install `uv`: <https://docs.astral.sh/uv/>
- we will strongly prefer using `uv` over `pip` and `conda` where possible.
- rationale: <https://www.bitecode.dev/p/a-year-of-uv-pros-cons-and-should>


{: .important-title}
> Now, check your knowledge:
>
> 1. In one sentence, why do we prefer `uv` over `pip`?
> 1. What does a lockfile provide, and where does `uv` write it in a project?
> 1. How do you add a runtime dependency vs. a dev dependency with `uv`?
> 1. How do you run a module or script through `uv` without activating the venv?
> 1. Start a new `uv` project targeting Python `3.13`. Add `jupyterlab` and
>    `babypandas==1.0.0.dev1`. Launch JupyterLab, create a notebook, `import
>    babypandas as bpd`, build a tiny DataFrame (e.g., names and ages), sort it
>    by age, and confirm it works.

## `git` workflow: making pull requests

- We will avoid pushing to the `main` branch of our GitHub!
- rationale:
  <https://www.reddit.com/r/explainlikeimfive/comments/1kob5xw/eli5_why_is_pushing_to_a_main_branch_bad_what_is/>
- Sam will ask the PLs to prevent direct pushes to the main branch
- read the GitHub flow workflow:
  <https://docs.github.com/en/get-started/using-github/github-flow>


{: .important-title}
> Now, check your knowledge:
>
> 1. Clone our lab webpage <https://github.com/dstl-lab/dstl-lab.github.io>
> 1. Run the lab webpage locally by following the instructions in the repo
>    README.
> 1. Checkout to a new branch with your name in the branch name (e.g. Sam would
>    create a branch like `sam-add-picture`).
> 1. Add your name and picture to the lab homepage. Make sure your picture loads
>    locally.
> 1. Commit, then make a pull request to our homepage repo.
> 1. Request a code review from someone else on your team.
> 1. When the other person approves the PR, merge the PR.
> 1. Verify that the build works correctly, then see your updated picture at
>    <https://dstl.ucsd.edu/>!
