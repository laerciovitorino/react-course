# React Course
  **DISCLAIMER:** The instructions and guidelines below are all related to the React Course taught by [Andrew Mead](https://github.com/andrewjmead) on the Udemy platform. All snippets of code and instructions below were took from his course. All credits go to him.

  This README file is divided into sections to better guide anyone who would like to follow along and for people who don't have prior experience with React development. There is a general setup section and after that the sections are related for the various sub-projects in this course.

## General Setup

* If you haven't **node** installed in your machine yet, go to [node](https://nodejs.org), download it and then install it on your machine.

   To check out if everything is okay, open the terminal(*Git Bash - Windows(suggested)*), and then type in **node -v**. If the version you downloaded appears on the screen, you are good to go!

* Then, check which version of npm you have installed. To do that, just type in **npm -v**. As the same with *node -v*, a version number should appears on the screen.

## Hello React Project
This project is divided into two parts: the first one, **Initial Version**, will guide you on how to build a React App without almost any automation; the second one, **Enhanced Version**, will show you how to automate some parts in the development process using some third-party tools and libraries in order to ease the way you develop React applications

Before we get started, we need first to do some configuration in order to generate our *package.json* file. This file will keep all the information about license, author, description etc, and about the dependencies(libraries, modules etc) used to work on the project and to ease the development process.

* First off, create a directory with the name HelloReact: mkdir HelloReact (*via cli*)
* To configure our *package.json* file do the following:
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
   * After all that you can see how your *package.json* file will look like. You can hit enter and you are done!

### Create a simple web server
For the projects that we'll be working on, it's necessary to have a webserver up and running.

* First we'll install Express(Express is a standard server framework for Node.js)
   * npm install express@4 --save
   -  After the command above a folder named node_modules will be created inside the root folder with the **Express** module installed and all its dependencies

* After that, create a server.js file inside the root **HelloReact** folder. Inside it, type in the following snippet of code:
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

* To test if the server is working properly, first we need to:
  * Create the **public** folder referenced in the *server.js* file. This folder will hold all the application files that will be used to generate our web application;
  * Create an *index.html* file inside the **public** folder, and inside it, type in the following snippet of code:
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

  * After that, in the command line, inside the **HelloReact** folder, enter the following:
     * **node server.js**
     * The message: *Express server is up on port 3000* will appears and you can see in your web browser if the content of the **index.html** file is exhibited. If so, everything worked as expected and you are good to go with React development and follow along. :thumbsup:

  * Everytime you need to check if your project is working properly you can run the command just above to run the server and then see the result in the browser


### Initial Version
In this version, almost all the libraries used in the code will be imported manually, as well as the ....

* First off, inside the **index.html** file you will do the following:
  * add the three lines below inside the `<head></head>` tags:
  ```html
  <script src="https://cdnjs.cloudflare.com/ajax/libs/babel-core/5.8.23/browser.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.14.7/react.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/react/0.14.7/react-dom.js"></script>
  ```

  * Remove the `<h1></h1>` tags along with its content and add the following:
  ```html
  <div id="app"></div>

  <script type="text/babel">
    ReactDOM.render(
      <h1>Hello React!</h1>,
      document.getElementById('app')
    );
  </script>
  ```

* To see if everything is fine, run the server and check the result in the browser. If you see **Hello React!** on your screen. Congrats!
