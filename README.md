# BasicBuildingBlockofReact
Hello,
Welcome to this tutorial, today I am going to teach you how to get starter with React and React Native.

What is React?
In simple terms, React is “A JavaScript library for building user interfaces”. Think about React as:
Declarative
React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes.

Component-Based
Build encapsulated components that manage their own state, and then compose them to make complex UIs. Since component logic is written in JavaScript instead of templates, you can easily pass rich data through your app and keep state out of the DOM.

Learn Once, Write Anywhere
We do not make assumptions about the rest of your technology stack, so you can develop new features in React without rewriting existing code.
React can also render on the server using Node and power mobile apps using React Native.


React Vs React Native:

While there are several similarities between Reactjs and React Native, however, there are some notable differences as well. Let’s have a look:
•	Reactjs can be described as a base derivative of React DOM, for the web platform while React Native is a base derivative in itself, which means that the syntax and workflow remain the same, but components alter.
•	Reactjs, eventually, is a JavaScript library, which enables the programmer to create an engaging and high performing UI Layer while React Native is an entire framework for building cross-platform apps, be it web, iOS or Android. 
•	In Reactjs, virtual DOM is used to render browser code in Reactjs while in React Native, native APIs are used to render components in mobile.
•	The apps developed with Reactjs renders HTML in UI while React Native uses JSX for rendering UI, which is nothing but javascript. 
•	CSS is used for creating styling in Reactjs while a stylesheet is used for styling in React Native.
•	In Reactjs, the animation is possible, using CSS, just like web development while in React Native, an animated API is used for inducing animation across different components of the React Native application.
•	If the need is to build a high performing, dynamic, and responsive UI for web interfaces, then Reactjs is the best option while if the need is to give mobile apps a truly native feeling, then React Native is the best option.
More can be read at (https://www.simform.com/reactjs-vs-reactnative/#:~:text=In%20Reactjs%2C%20virtual%20DOM%20is,which%20is%20nothing%20but%20javascript.)

How to set up?
Prerequisites:
To be able to work through this guide, you need:
•	Windows operating system 
•	4 gig of ROM memory space.
React can be run and debug on virtual and physical devices.  For the purpose of this tutorial, we are going to use the expo app available in the Google Play Store. So let us get started, enjoy your tutorial.

Setting Up Your Environment
The React Native ecosystem has evolved quite a bit since the first edition. The open source tool Expo.io, in particular, has streamlined both the project initialization and development phases, making working in React Native even more of a pleasure than it already was in version 0.36.
With the Expo workflow, you will be able to build native iOS and Android applications using only JavaScript, work in the iOS simulator and Android emulator with live reload, and effortlessly test your app on any real-world device via Expo's app. Until you need access to native code (say, to integrate with legacy native code from a separate code base), you can develop your application entirely in JavaScript without ever needing to use Xcode or Android Studio. If your project ever needs to evolve into native code support, Expo provides the ability to detach your project, which changes your app into native code for use in Xcode and Android Studio.
Installing Node.JS
Node.js is a JavaScript runtime built on Chrome's V8 JavaScript engine, and is designed to build scalable network applications. Node allows JavaScript to be executed in a Terminal, and is an indispensable tool for any web developer. For more information on what Node.js is, you can read the project's About Node.js page at https://nodejs.org/en/about/. Download and install Node.js from the project's site at https://nodejs.org/en/download/.

The hard part of the setup is done! From here on out, we can use the magic provided by Expo to easily create new apps for development. We will create our first app using Expo via the command line (CMD) using the following steps:

Get the command line tool
You will run this tool locally to package, serve, and publish your projects.

npm install expo-cli --global

Create your first project
You will be asked to create an Expo account before proceeding.

expo init myNewProject
cd myNewProject
expo start

Preview your project
Open the Expo development client on your device. Scan the QR code printed by expo start with Expo Client (Android) or Camera (iOS). You may have to wait a minute while your project bundles and loads for the first time.

For a list of all of the available commands for the Expo CLI, check out the documentation at https://docs.expo.io/versions/latest/guides/expo-cli.html.



Basic react and react native structure

my-app
├── build
├── node_modules
├── public
│   ├── favicon.ico
│   ├── index.html
│   └── manifest.json
├── src
│   ├── App.css
│   ├── App.js
│   ├── App.test.js
│   ├── index.css
│   ├── index.js
│   ├── logo.svg
│   └── serviceWorker.js
├── .gitignore
├── package.json
└── README.md
•	build is the location of your final, production-ready build. This directory won’t exist until you run npm build or yarn build. The contents of this folder should be ready-to-ship without any interaction on your part.
•	node_modules is where packages installed by NPM or Yarn will reside.
•	public is where your static files reside. If the file is not imported by your JavaScript application and must maintain its file name, put it here. Files in the public directory will maintain the same file name in production, which typically means that they will be cached by your client and never downloaded again. If your file does not have a filename that matters — such as index.html, manifest.json, or robots.txt — you should put it in src instead.
•	src is where your dynamic files reside. If the file is imported by your JavaScript application or changes contents, put it here. In order to make sure the client downloads the most up-to-date version of your file instead of relying on a cached copy, Webpack will give changed files a unique file name in the production build. This allows you to use simple, intuitive file names during development, such as banner.png instead of banner-2019-03-01-final.png. You never have to worry about your client using the outdated cached copy, because Webpack will automatically rename banner.png to banner.unique-hash.png, where the unique hash changes only when banner.png changes.

Basic building blocks:
Component:

React and react native programs are made of UI’s interconnected to one another.
Those UI’s are called components. We have two types of components:
Functional Component:
The simplest way to define a component is to write a JavaScript function:

function HelloWorld (props) {
  return <h1>Hello World</h1>;
}
This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

Class component:
You can also use an ES6 class to define a component:
class HelloWorld extends React.Component {
  render() {
    return (
      <div>
        <h1>Hello, world!</h1>
      </div>
    );
  }
}
One can convert a function component like HelloWorld to a class in four steps:
•	Create an ES6 class, with the same name, that extends React.Component.
•	Add a single empty method to it called render().
•	Move the body of the function into the render() method.
•	Delete the remaining empty function declaration

Depending on the library (react/react native) used, we can have many types of components:
For react components, more can be read at https://reactjs.org/docs/react-component.html#gatsby-focus-wrapper.
For react native components, more can be read at https://reactnative.dev/docs/components-and-apis.

Props (Properties)
Props is short for “properties.” Props let you customize React components. For example, here you pass each <Cat> a different name for Cat to render:
import React from 'react';
import { Text, View } from 'react-native';
const Cat = (props) => {
  return (
    <View>
      <Text>Hello, I am {props.name}!</Text>
    </View>
  );
}
const Cafe = () => {
  return (
    <View>
      <Cat name="Leo" />
      <Cat name="John" />
      <Cat name="Jack" />
    </View>
  );
}

export default Cafe;
r
 
Most of React and React Native’s Core Components can be customized with props, too. 


States
While you can think of props as arguments you use to configure how components render, state is like a component’s personal data storage. State is useful for handling data that changes over time or that comes from user interaction. State gives your components memory!
import React, { useState } from "react";
import { Button, Text, View } from "react-native";

const Cat = (props) => {
  const [isHungry, setIsHungry] = useState(true);

  return (
    <View>
      <Text>
        I am {props.name}, and I am {isHungry ? "hungry" : "full"}!
      </Text>
      <Button
        onPress={() => {
          setIsHungry(false);
        }}
        disabled={!isHungry}
        title={isHungry ? "Pour me some milk, please!" : "Thank you!"}
      />
    </View>
  );
}

const Cafe = () => {
  return (
    <>
      <Cat name="Munkustrap" />
      <Cat name="Spot" />
    </>
  );
}

export default Cafe;
 
First, you will want to import useState from React like so:
import React, { useState } from 'react';
Then you declare the component’s state by calling useState inside its function. In this example, useState creates an isHungry state variable:
const Cat = (props) => {
  const [isHungry, setIsHungry] = useState(true);
  // ...
};
You can use useState to track any kind of data: strings, numbers, Booleans, arrays, objects. For example, you can track the number of times a cat has been petted with const [timesPetted, setTimesPetted] = useState(0)!
Calling useState does two things:
•	it creates a “state variable” with an initial value—in this case the state variable is isHungry and its initial value is true
•	it creates a function to set that state variable’s value—setIsHungry
It doesn’t matter what names you use. But it can be handy to think of the pattern as [<getter>, <setter>] = useState(<initialValue>).
Next you add the Button Core Component and give it an onPress prop:
<Button
  onPress={() => {
    setIsHungry(false);
  }}
  //..
/>
Now, when someone presses the button, onPress will fire, calling the setIsHungry(false). This sets the state variable isHungry to false. When isHungry is false, the Button’s disabled prop is set to true and its title also changes:
<Button
  //..
  disabled={!isHungry}
  title={isHungry ? 'Pour me some milk, please!' : 'Thank you!'}
/>
You might’ve noticed that although isHungry is a const, it is seemingly reassignable! What is happening is when a state-setting function like setIsHungry is called, its component will re-render. In this case the Cat function will run again—and this time, useState will give us the next value of isHungry.
Finally, put your cats inside a Cafe component:
const Cafe = () => {
  return (
    <>
      <Cat name="Munkustrap" />
      <Cat name="Spot" />
    </>
  );
};







