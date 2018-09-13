# edxNodejs-Lab2


This project is part of the [Microsoft's __Introduction to NodeJS__ course](https://courses.edx.org/courses/course-v1:Microsoft+DEV283x+2T2018/course/) hosted edx course platform. This project's purpose is to build a RESTful API to manage blog entries, like posts and comments. The REST API uses an in-memory store as database.

## RESTful blog API

The app is developed in NodeJS and is created with [`express-generator`](https://expressjs.com/en/starter/generator.html).
The Express application has the following REST API endpoints:

- __GET__ and __POST__ /posts
- __PUT__ and __DELETE__ /posts/:id/
- __GET__ and __POST__ /posts/:postId/comments
- __PUT__ and __DELETE__ /posts/:postId/comments/:commentId

## Installation

You can clone this repository or download it as a .zip file.
Once downloaded, you need to run `npm install` in your console to install all the npm dependencies.

## Instructions

To use the application you must use your terminal and navigate to the app's local folder and start the local server on port 3000, using `npm start` or `npm start-debug`. This will result in starting the server at `http://localhost:3000`.
In order to test the API you can use [Postman](https://www.getpostman.com/), CURL or any other HTTP agent or tester. For example, the CRUD commands are
```
//posts post data
curl -H "Content-Type: application/json" -X POST -d '{"name": "Top 10 ES6 Features", "url":"http://webapplog.com/es6", "text": ""}'  "http://localhost:3000/posts"

//updates post data at specific id
curl -H 'Content-Type: application/json' -X PUT -d '{"name": "Top 10 ES6 Features Every Developer Must Know", "url":"http://webapplog.com/es6", "text": ""}' "http://localhost:3000/posts/0"

//gets post data
curl "http://localhost:3000/posts"

//deletes post data at specific id
curl -X DELETE "http://localhost:3000/posts/0"
```
