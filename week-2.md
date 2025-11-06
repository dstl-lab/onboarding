---
title: "Week 2: Web Development"
layout: default
---

# Week 2: Web Development

{: .note-title}
> Goals
>
> - Understand the client-server model for web development
> - Learn the basics of HTML, CSS, and JavaScript
> - Create a mini web app using Flask

## Introduction to Web Development
Please complete the following labs from DSC106. You do not need to make a video.
- <https://dsc106.com/labs/lab01/>
- <https://dsc106.com/labs/lab02/>
- <https://dsc106.com/labs/lab03/>

{: .important-title}
> Now, check your knowledge:
>
> 1. Make a pull request to the main lab website so that when someone clicks on
>    your name, they will get redirected to your personal website.
> 1. Order the following CSS selectors from most specific to least specific:
>    `*`, class, id, element.
> 1. What is the difference between padding and margin in CSS?
> 1. What is the DOM, and how does JavaScript interact with it?
> 1. What are the three ways to include CSS in an HTML document? Which method is
>    generally preferred for larger projects and why?
> 1. Explain the difference between `display: block`, `display: inline`, and
>    `display: flex`.
> 1. What is the box model in CSS? What are its four components?
> 1. What does it mean for JavaScript to be "event-driven"? Provide an example
>    of an event.

## CRUD and REST
Please read the following article:
- <https://www.codecademy.com/article/what-is-crud-explained>

{: .important-title}
> Now, check your knowledge:
>
> 1. What does CRUD stand for? Explain each operation in your own words.
> 1. What is the difference between CRUD and REST? How are they related?
> 1. What is the difference between a POST and a GET request? Can GET requests
>    have a request body?
> 1. What does it mean for an HTTP method to be "idempotent"? Which methods are
>    idempotent and which are not?
> 1. What are HTTP status codes? Give examples of common status codes in the
>    2xx, 4xx, and 5xx ranges and what they indicate.
> 1. In a RESTful API, what would a URL like `/api/users/123/posts` typically
>    represent? How about `/api/users/123/posts/456`?

## Creating a Simple App
Complete the following mini-project:
- <https://github.com/dstl-lab/flask-reddit-demo>

{: .important-title}
> Now, check your knowledge:
>
> 1. What functionality does Flask give you for the Reddit Demo over the DSC 106
>    labs?
> 1. In the flask-reddit-demo, trace through what happens when a user submits a
>    new post. What route handles it, what data is processed, and how is the
>    user redirected?
> 1. What is a route in Flask? How do you define a route that accepts both GET
>    and POST requests?
> 1. What is the purpose of HTML templates in Flask? Why not just use static
>    HTML files (like we did in the DSC 106 labs)?
> 1. How do you pass data from a Flask route to a template? How do you access
>    that data in the template?
> 1. What is the difference between `render_template()` and `redirect()` in
>    Flask? When would you use each?
> 1. How do you handle form data submitted to a Flask app? Where does Flask
>    store this data?
> 1. Why do we need to use a database (in this case, `sqlite`) for this
>    mini-project?
