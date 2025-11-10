---
title: "Week 3: React"
layout: default
---

# Week 3: React

{: .note-title}
> Goals
>
> - Learn rationale behind React
> - Understand why we use JS bundlers
> - Create a basic React app

## React Basics

- Read <https://react.dev/>
- Read <https://react.dev/learn>

{: .important-title}
> Now, check your knowledge:
>
> 1. What is React and why would you use it over plain HTML/CSS/JavaScript?
> 1. What is JSX? How is it different from HTML?
> 1. What is the difference between props and state in React? When would you
>    use each?
> 1. What is a component in React?
> 1. Explain what the `useState` hook does. What do the two values it returns
>    represent?
> 1. How do you handle events in React (e.g., button clicks)? How is this
>    different from handling events in plain JavaScript?
> 1. Why do we need to use `key` props when rendering lists in React? What
>    happens if you don't include them?

## JS Bundlers

- Read <https://dev.to/sayanide/the-what-why-and-how-of-javascript-bundlers-4po9>
- Read <https://vite.dev/>, which is our bundler of choice when possible.
- Read <https://vite.dev/guide/> and run the commands there.
- Read <https://vite.dev/guide/philosophy>
- Read <https://vite.dev/guide/why>
- Using vite, create a new app called `dstl-onboarding-vite`.
  - Select `React` as framework
  - Select `Typescript + SWC` as the variant
  - Select `No` for "Use rolldown-vite (Experimental)?:"
  - Select `Yes` for "Install with npm and start now?"
- Vite should start a dev server. Open the page in your browser
- Test hot module reloading by clicking the button a few times, then editing
  some of the text in `App.tsx`. You should see the page update live without
  reloading your button count!

{: .important-title}
> Now, check your knowledge:
>
> 1. What is a JavaScript bundler and why do we need one? What problems do
>    bundlers solve that can't be handled with plain HTML `<script>` tags?
> 1. What is the difference between a development build and a production build?
>    Why does Vite optimize differently for each?
> 1. What is Hot Module Replacement (HMR)? How does it improve the developer
>    experience compared to traditional full-page reloads?
> 1. In your own words, explain what happens when you run `npm run dev` vs.
>    `npm run build` in a Vite project.
> 1. What is TypeScript and why might you want to use it over plain JavaScript?
> 1. What files does Vite generate when you run `npm run build`? Where do they
>    go and how would you deploy them to a web server (e.g. in Flask)?
