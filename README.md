# React Course
  The instructions and guidelines below are all related to the React Course taught by [Andrew Mead](https://github.com/andrewjmead) on the Udemy platform. All snippets of code and instructions below were took from his course. All credits go to him.

  This README file is divided into sections to better guide anyone who would like to follow along and for people who don't have prior experience with React development. There is a general setup section and after that the sections are related for the various sub-projects in this course.

## General Setup

1. If you haven't **node** installed in your machine yet, go to [node](https://nodejs.org), download it and then install it on your machine.

    To check out if everything is okay, open the terminal(*Git Bash - Windows(suggested)*), and then type in **node -v**. If the version you downloaded appears on the screen, you are good to go!

2. Then, check which version of npm you have installed. To do that, just type in **npm -v**. As the same with *node -v*, a version number should appears on the screen.

## Hello React Project
  Before we get started, we need first to do some configuration in order to generate our *package.json* file. This file will keep all the information about license, author, description etc, and about the dependencies(libraries, modules etc) used to work on the project and ease the development process

  3. To configure our *package.json* file do the following:
  * Create a directory called HelloReact: mkdir HelloReact (*via cli*)
      * Inside the HelloReact folder, type in **npm init**
      * After that, it's necessary to do some configuration on your project:
        -  For the HelloReact project, type in the project name as *hello-react*;
        -  For the **version** you can just hit *enter* to use the default value;
        -  For **description** you can put anything(e.g. Simple react app);
        -  For **entry point** you can just hit *enter*;
        -  For **test command** you can leave that empty for this project;
        -  For **git repository** you can also leave that empty for this project;
        -  For **keywords** you can leave that empty as well;
        -  For **author** you can put your name;
        -  For **license** you can use *MIT* or any other license as you wish;
      * After all that you can see how your *package.json* file will look like.
        You can hit enter and you are done!

## Create a simple web server
  For the projects that we'll be working on, it's necessary to have a webserver up and running.

  4. First, we'll install Express(Express is a standard server framework for Node.js)
     * npm install express@4 --save

  5. After that, create a server.js file inside the root **HelloReact** folder. Inside it, type in the following snippet of code:
     ```javascript
     var express = require('express');

     // Create our app
     var app = express();

     // The public folder is where we'll put all the application files for this project.
     app.use(express.static('public'));

     app.listen(3000, function () {
       console.log('Express server is up on port 3000');
     });
     ```

6. Create the **public** folder referenced in the *server.js* file. This folder will hold all the application files that will be used to generate our web application

7. Inside the **public** folder, create an *index.html* file and inside it, type in the following snippet of code(for now):
   ```html
   <!DOCTYPE html>
   <html>
     <head>
       <meta charset="utf-8">
       <title>Hello React</title>
     </head>
     <body>
       <h1>Hello World!</h1>
     </body>
   </html>
   ```

8. After all that above, you can test if everything is working fine. In the command line, inside the **HelloReact** folder, enter the following:
   * node server.js
   The message: *Express server is up on port 3000* will appears and you can see in your web browser if the content of the **index.html** file is exhibited. If so, everything worked as expected and you are good to go with React development and follow along
