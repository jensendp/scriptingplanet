---
templateKey: blog-post
title: "TypeScript: Is it a Frontend or Backend Language"
date: 2021-09-01T15:38:00.000Z
description: Recently I was doing some investigation into the nuances of
  TypeScript. TypeScript is continuing to gather speed and adoption in several
  areas of software development, and that is one of the reasons I'm diving
  headfirst into it. During my research, I came across a very interesting and
  valid question with regards to the language that many people ask themselves at
  one point or another. Is TypeScript a frontend or a backend language?
featuredpost: true
featuredimage: /img/frontend-or-backend.jpg
---
**TypeScript is a superset of JavaScript. TypeScript code gets transpiled into JavaScript. And since JavaScript can be used as either a frontend or backend language, so too can TypeScript be considered both a frontend AND backend language.**

With the continued growing popularity of scripting languages, such as TypeScript, it's only natural to want to know once you learn the language, where and how can you use it. Because TypeScript is just as versatile as JavaScript, if not more so, it's not only suited to traditional web-based frontend and backend development but can also be applied to other avenues as well. Below I will give you several examples of how you can use TypeScript in just about any type of application you would want to write.

The pre-cursor to just about everything we are about to go through is having a couple of tools installed. In order to get started you will need to <a href="https://nodejs.dev/download" target="_blank">download the latest version of Node.js</a>. You are mostly installing this to get access to `npm`, the Node Package Manager, and `npx`, the Node Package Runner.

## Frontend

Over the last several years, TypeScript has become a very popular frontend language to use in conjunction with many of the popular frameworks used to build web applications. This makes sense because TypeScript transpiles down to JavaScript and all of these frontend frameworks are accessible via JavaScript.

Out of the box, these frameworks typically are ready-to-go with JavaScript support. All you really need to do is either supply a command-line argument or a small configuration change to enable your project with TypeScript support.

Here are a few examples of popular frameworks that can take advantage of TypeScript as a frontend language.

### React

Currently, React has to be my favorite framework for building frontend web applications. It's easily accessible and quick to pick up even if you have never used it before. It can be used to build lightning-fast, responsive web applications, and best of all...you can use TypeScript as your frontend language of choice.

The typical way to create a React application is to use the `create-react-app` command-line utility, so why reinvent the wheel. In order to create a React application using TypeScript as the frontend language, you will use the following command:

```
npx create-react-app <your-app-name> --template typescript
```

Simply replace the `<your-app-name>` with whatever you want to call your application and you are ready to go!

### Angular

Angular is another incredibly popular framework for building web applications. Before I started working with React, I spent a few years with Angular. I really liked this framework as well. It got a little confusing for a while with a lot of versioning and naming confusion as I grew along with Angular, but it seems like most of those earlier growing pains have worked themselves out.

A really cool feature of Angular is the fact that <a href="https://www.typescriptlang.org/docs/handbook/angular.html" target="_blank">it is actually written in TypeScript</a>. So you actually get full TypeScript frontend support out of the box without any extra work or configurations.

Getting started with Angular starts off similarly to how we started with React. You will need to begin with downloading and installing the latest version of Node.js. Once that is installed, you will install the Angular CLI, command line interface, with the following command:

```
npm install -g @angular/cli
```

From there all you need to do is create a new application:

```
ng new <your-app-name>
```

Simply replace the `<your-app-name>` with whatever you want your app to be called and you are in Angular world!

### Vue

Vue is another popular JavaScript framework for building beautify web applications. Similar to Angular, TypeScript has built-in support directly in the tooling so that you get to use it right out-of-the-box with very little extra work. That is always a nice feature.

To be honest, I haven't done much work with Vue. I've done enough research to understand the fundamentals, write a couple of basic apps, and teach a few people what I've learned. My verdict is still out on how much I like it, but for now I think it is a viable option in the world of web apps.

To get started using TypeScript in a Vue application you will need to install the Vue CLI:

```
npm install -g @vue/cli
```

Now that you have the CLI installed, you can use the `vue` command line too to create a new application:

```
vue create <your-app-name>
```

This will give you the opportunity to choose your Vue configuration. At this point, select the `Manually select features` option. In the following guide, be sure to select that you want to add TypeScript support:

```
Vue CLI v4.5.13
? Please pick a preset: Manually select features
? Check the features needed for your project: Choose Vue version, Babel, TS, Linter
? Choose a version of Vue.js that you want to start the project with 3.x
? Use class-style component syntax? No
? Use Babel alongside TypeScript (required for modern mode, auto-detected polyfills, transpiling JSX)? Yes
? Pick a linter / formatter config: Basic
? Pick additional lint features: Lint on save
? Where do you prefer placing config for Babel, ESLint, etc.? In dedicated config files
? Save this as a preset for future projects? (y/N)
```

You have now successfully create a Vue application with full TypeScript support as the frontend language.

## Backend

It's true that TypeScript gets labeled as a frontend language. It's not hard to see why. It's a close relative to JavaScript and hence spends a lot of time running near the browser. But it isn't a one trick pony. You know that framework that you installed at the beginning of this article? Node.js? Because of that, TypeScript can also be used as a backed language that runs on the server.

### Node & Express

Node.js is a framework that allows you to write server-side code in JavaScript, and in our case, even TypeScript. There are a few more steps to the equation to get it up and running compared to frontend frameworks, but it's not really a big deal.

Let's start by creating a backend application directory:

```
mkdir <your-app-name>
cd <your-app-name>
```

You are now in your new application's directory. The next thing you need to do is setup your project with the following command:

```
npm init -y
```

This command will create a new `package.json` file in your application directory that will have the default configuration. Not important to worry about right now, but as you build your application you will spend a little more time in this file.

Next we need to install a dependency to get our backend app up and running. In this case we will be using Express. Express is a framework that helps us to serve web pages and create APIs for our frontend apps to use.

```
npm install express
```

Express has now been installed and added to the `package.json` file. Now we need to write a little code. Nothing crazy and we aren't going to go into great detail on this. We will save that for another day.

Create a file named `index.js` in the root of your application directory and add the following contents to that file:

```
import express from 'express';
const app = express();
const port = 1234;

app.get('/', (req, res) => {
  res.send('Welcome to the backend');
});

// start the Express server
app.listen(port, () => {
  console.log(`server started at http://localhost:${port}`);
});
```

Nothing fancy. Just a simple backend server that will listen on port 1234 and replay with "Welcome to the backend" when you navigate to `localhost:1234`.

Now you need to make sure your app nows how to use this file. So make sure you have lines similar to this in your package.json file:

```
"main": "index.js",
"scripts": {
  "start": "node .",
  "test": "echo \"Error: no test specified\" && exit 1"
},
```

Now when you go to the terminal inside your application directory and run the following command you can open a web browser and see your application in all of it's glory:

```
npm run start
```

But where is the TypeScript you say?

That part is next.

You are going to need to install a couple dependencies and add some configurations to change your application to support TypeScript as the backend language. But don't worry, it isn't too complicated.

Start by installing TypeScript into your application with the following command:

```
npm install --save-dev typescript
```

This will install TypeScript as a development dependency so all of your code files can be written in TypeScript.

Now comes some configuration. Begin by creating a file named `tsconfig.json` in the root of your application and paste the following into that file:

```
{
  "compilerOptions": {
    "module": "commonjs",
    "esModuleInterop": true,
    "target": "es6",
    "noImplicitAny": true,
    "moduleResolution": "node",
    "sourceMap": true,
    "outDir": "dist",
    "baseUrl": ".",
    "paths": {
      "*": [
        "node_modules/*"
      ]
    }
  },
  "include": [
    "*"
  ]
}
```

We aren't going to worry about this file much at this point. Just know that this is a configuration file that tells Node how to transpile your TypeScript code into JavaScript code so that it can be run successfully in your backend application.

The second group of dependencies you will need to install are the types associated with TypeScript to integrate it with Node and Express. That's the thing about TypeScript as a frontend or backend language. It needs to know about types.

```
npm install --save-dev @types/node @types/express
```

Now you are ready to convert this to a TypeScript application. Start by renaming your `index.js` file to `index.ts`.

Next, modify a few pieces of your project.json file. Change your `main` value from `index.js` to `dist/index.js`.

Under the scripts section, add a `prestart` key with a value of `tsc`.

Your updated package.json file should look like this:

```
{
  "name": "backend",
  "version": "1.0.0",
  "description": "",
  "main": "dist/index.js",
  "scripts": {
    "prestart": "tsc",
    "start": "node .",
    "test": "echo \"Error: no test specified\" && exit 1"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "dependencies": {
    "express": "^4.17.1"
  },
  "devDependencies": {
    "@types/express": "^4.17.13",
    "@types/node": "^16.7.10",
    "typescript": "^4.4.2"
  }
}
```

Finally, you need to make one more change in your source code to make this a full TypeScript application. When it comes to import modules into your application, TypeScript prefers to use the `import` syntax as opposed to the `require` syntax.

So change the first line of your `index.ts` file from

```
const express = require('express');
```

to the following updated line:

```
import express from 'express';
```

Now you can once again run your start command

```
npm run start
```

and open a browser and navigate to `localhost:1234` and you are running a TypeScript backend application!

## Mobile

The use of TypeScript in mobile applications is by far my favorite! To me, there is nothing more satisfying that writing a native mobile application in a cool scripting language like TypeScript. And if you do it right, you can actually take the app that you create in TypeScript and ultimately deploy it to both iOS _and_ Android.

But that is a topic for another day.

Let's stick with creating a basic mobile application using TypeScript. Is this considered a frontend usage of TypeScript. I'm going to say yes, because the code you are writing is going to be in front and useable directly by the user. So, to me, that sounds like a frontend language to me.

There are a few different ways to create mobile applications using TypeScript, but my favorite is through <a href="https://reactnative.dev/" target="_blank">React Native</a>.

Creating an application with these frameworks is quite easy.

We will start with installing the Expo CLI which is core to creating this application.

```
npm install -g expo-cli
```

Once expo is installed, the process is very simple to using the `init` command to create your project and choose TypeScript as your language of choice.

```
expo init <your-app-name>
```

Then Expo will ask for your input. Just select the blank (TypeScript) option from the provided menu:

```
? Choose a template: › - Use arrow-keys. Return to submit.
    ----- Managed workflow -----
    blank               a minimal app as clean as an empty canvas
❯   blank (TypeScript)  same as blank but with TypeScript configuration
    tabs (TypeScript)   several example screens and tabs using react-navigation and TypeScript
    ----- Bare workflow -----
    minimal             bare and minimal, just the essentials to get you started
```

You have now created a React Native project that uses the TypeScript language to build applications that can target both iOS and Android!

How Cool!

## TypeScript is Both Frontend and Backend

As you can see, there are many ways to use the TypeScript programming language. Each of these ways can fall either on the frontend side of development as well as the backend.

Now that is versatility!

So the next time you need to create an application and you aren't sure about which language to use based on the type of application, give TypeScript some serious consideration simply based on how incredibly versatile it is!