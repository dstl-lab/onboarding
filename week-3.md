---
title: "Week 3: React"
layout: default
---

# Week 3: React

{: .note-title}
> Goals
>
> - Learn rationale behind React
> - Understand why we use JS bundlers and become familiar with `vite`, our bundler of choice
> - Learn Typescript rationale and basics
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
> 1. List all the files/folders that get changed when you run `npm install @tanstack/react-query`.
> 1. What is more appropriate, and why: `npm install prettier`? Or `npm install
>    -D prettier`?
> 1. What is the difference between a development build and a production build?
>    Why does Vite optimize differently for each?
> 1. What is Hot Module Replacement (HMR)? How does it improve the developer
>    experience compared to traditional full-page reloads?
> 1. In your own words, explain what happens when you run `npm run dev` vs.
>    `npm run build` in a Vite project.
> 1. What files does Vite generate when you run `npm run build`? Where do they
>    go and how would you deploy them to a web server (e.g. in Flask)?

## Typescript

- Watch <https://www.destroyallsoftware.com/talks/wat>, a legendary talk about
  crazy results from programming languages. The JS examples in particular are a
  key motivation for using Typescript.
- Read <https://www.typescriptlang.org/>
- Read <https://www.typescriptlang.org/docs/handbook/typescript-from-scratch.html>
- Read <https://www.typescriptlang.org/docs/handbook/typescript-in-5-minutes.html#types-by-inference>
- Read the Typescript handbook:
  - <https://www.typescriptlang.org/docs/handbook/2/basic-types.html>
  - <https://www.typescriptlang.org/docs/handbook/2/everyday-types.html>
  - <https://www.typescriptlang.org/docs/handbook/2/narrowing.html>
  - <https://www.typescriptlang.org/docs/handbook/2/functions.html>
  - <https://www.typescriptlang.org/docs/handbook/2/objects.html>
  - (skip type manipulation for now, although the Generics page is useful)
  - <https://www.typescriptlang.org/docs/handbook/2/classes.html>
  - <https://www.typescriptlang.org/docs/handbook/2/modules.html>

{: .important-title}
> Now, check your knowledge:
>
> 1. What is TypeScript and why might you want to use it over plain JavaScript?
> 1. Why does `[] + []` produce `0` in JS? What does Typescript do instead?
> 1. Why does `[] + {}` produce `"[object Object]"` in JS? What does Typescript do instead?
> 1. What does it mean when we say that Typescript is "structurally typed"? How
>    is this different from Python, for example?
> 1. What is the difference between optional parameters and parameters with default
>    values in TypeScript functions? How do you define each?
> 1. What is the difference between `interface` and `type` in TypeScript when
>    defining object shapes? When might you prefer one over the other?
> 1. What does it mean when a class `implements` an interface? How is this
>    different from `extends`?
> 1. What is the difference between default exports and named exports in
>    TypeScript modules? Can you mix both in a single file?
> 1. When you import a module, what is the difference between `import * as name`
>    and `import { thing }` syntax? When would you use each?


## React: Tic-Tac-Toe

- Follow <https://react.dev/learn/tutorial-tic-tac-toe> to build a tic-tac-toe
  app.
  - To get started, fork <https://github.com/dstl-lab/dstl-onboarding-react>
    onto your personal GitHub account, `git clone` your fork, and run `npm
    install`.
  - Now, you can start following the tic-tac-toe tutorial starting from the
    section titled "Setup for the tutorial".
- One key difference is that we are working in a Typescript file, not a plain JS
  file. This means that certain steps in the tutorial will produce Typescript
  errors. The first one you'll run into is probably in "Passing data through
  props".
  - You should edit the code so that the errors are fixed. Don't leave the
    errors alone, and don't change the file extension to `.jsx`.
- After you're done with the main tutorial, complete ALL the suggested
  improvements (#1-5) for the tic-tac-toe app.
- Make a pull request from your  to the original repo
  (<https://github.com/dstl-lab/dstl-onboarding-react>). The pull request should
  include a short screen recording showing how your app works after you
  implemented improvements #4 and #5 ("highlighting the three squares that
  caused the win" and "displaying the location for each move in the move history
  list").

{: .important-title}
> Now, check your knowledge:
>
> 1. What does it mean to "lift state up" in React? Why did we need to do this
>    in the tic-tac-toe game?
> 1. The tutorial emphasizes immutability when updating the `squares` array.
>    Explain why we use `squares.slice()` instead of modifying the array
>    directly. What benefits does immutability provide?
> 1. In the final game, how does the `Game` component calculate `xIsNext`
>    without storing it in state? Why is this approach better than storing it
>    as a separate state variable?
> 1. What is the purpose of the `key` prop in the list of moves? What would
>    happen if you used the move description as the key instead of the move
>    index?
> 1. When working with TypeScript in React, why do you need to define types for
>    component props? What errors did you encounter and how did you fix them?
> 1. Describe how you implemented improvement #4. What React concepts did you
>    need to use to complete it?
