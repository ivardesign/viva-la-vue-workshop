# Our App - Bouncy Bounce
## Our Goals

**At the end of the day you should**

- Feel comfortable in the terminal
- Have your project online
- Be comfortable in git
- Meet new friends to learn with
- Find a mentor
- Get resources to continue learning
- Have Fun! <3

**You should know**
- what a component is and how to use one
- how to start a new Vue project
- the difference between your local and remote code
- what a Frontend Framework means means
- what a method is
- what a directive is

#### Share your sites at the end of the day:
[https://gist.github.com/jendiamond/5a26b531e8e47b4aa638#file-tutorial_sharing-md](https://gist.github.com/jendiamond/5a26b531e8e47b4aa638#file-tutorial_sharing-md)

#### Kindness, Consideration and Respect.
- Be kind to yourself. You are not less than anyone else because you do not know something.
- Be considerate. Remember that all the coaches and organizers are happily volunteering their time to help you.  
- Respect others. Remember your coach is having patience with you so have patience with your student pair.

**If you have any problems with anyone please let someone know.** [Code of Conduct](https://docs.google.com/document/d/1XEnFI3R30IiGXOpC4idb0ku3pw8OoJcBpG9mg3iKiAo/edit)

---

### A Little Review to Start the Day

**Go over the commandline prompts with your coach so you can be sure you can communicate clearly and easily throught the day.**

#### Coach, your should read these aloud and have the students do them in their terminals
+ See what directory you are currently in `pwd`
+ Navigate to the Desktop directory `cd`
+ Create a new directory called rainbow `mkdir rainbow`
+ Change into the rainbow directory `cd rainbow`
+ Create a new directory in the rainbow directory called leprechaun `mkdir leprechaun`
+ Change into the leprechaun directory `cd leprechaun`
+ Create 3 files gold.md, nyancat.md & unicorn.md (in the terminal) `touch gold.md nyancat.md unicorn.md`
+ List the files in the leprechaun directory `ls`
+ Go into sublime and add a bit of text to the gold.md file `subl .`
+ Open the file in the terminal and read it `cat gold.md`
+ Delete the gold.md file from the leprechaun directory `rm gold.md`
+ Change back into the rainbow directory `cd ../`
+ Delete the rainbow directory `rm -r rainbow`
+ Find the flag to list all the hidden files `man ls` (`ls -a`)

**Hooray for The Terminal Slide Show!**

**Psst** - If you ever see a **`$`** sign in this tutorial, it is not part of the code. The **`$`** sign means that you should type the code that follows it into your terminal.

---

<a name="section-1">Section I.</a>
![birds](https://anantasite.files.wordpress.com/2015/10/page-header-blog.png)
# Let us Dive into Vue
**In the first section we are going to do a small amount of code but we will learn a lot about it.**

# First of all, What is Vue.js?
## Vue.js is a Frontend Framework. 

#### Let's break down what "frontend framework" means. 

“Frontend” means the code that you see in your browser, like Firefox, Chrome, or Safari. 
- A “framework” is like the workbench of tools and supplies that you need to build a project on the web.
- Imagine that instead of coding, you were a carpenter building a house. A carpenter has her workbench of tools. This might include a saw and hammer. But it would probably not include a (cherry-shaped) toilet plunger. The carpenter’s workbench only includes that which is needed for carpentry.
- Our “frontend framework” includes all of the tools we need to create web-pages and only includes those tools.
 
Other Frontend Frameworks that you may have heard of include React, Angular, Ember and many, many more. 
  
We choose to use Vue.js because it is one of the most modern, one of the most   popular, AND the code is **easy to read.** 
  
Vue.js is one of the frameworks you are most likely to use in the real world, and one of the quickest to learn. 


## Let’s get started!

### First, make sure the `vue` command is available in your terminal:
```js
$ npm install -g @vue/cli
```
#### now we can do vue commands, like $ `vue create our-app`

## Let’s create our first app

+ Create to a directory (aka a folder) where you want to create your new Vue app. (You may want to create it on your Desktop so you can easily find it later.)
  
### Tell Vue to create a new app 
##### How we do that? 
#### Run the following command in your terminal.  
(*However, **use your name** instead. For example: if your name is Veronica, you could write:  $ vue create veronicas-vue-app*)
```js
$ vue create my-app-name
```
#### Once you run this command, Vue will ask you to make several decisions.  
Today we are going to make these choices:
+ Use “Default, vue 3”
    
**Best Practice** Once the app is created, be sure to **read what the terminal is telling you**. This is a good thing to start doing as a developer. The terminal gives you a lot of good information.

#### The terminal is now telling you to do the next few steps which are listed below…

#### 1. Change into your app directory
```bash
$ cd my-app-name
```
#### 2. Install packages
```bash
$ npm install
```
#### 3. Start the server:
```bash
$ npm run serve
```
Once you run `$ npm run serve` this terminal is going to continue to be used by the server to run your app locally on your machine.

#### This means that you can go to your browser and SEE YOUR APP!  Woo Hoo!!
+ We do this, by typing [http://localhost:8080/](http://localhost:8080/) in your browser.
##### YES! That’s *YOUR* app!!!

It does not seem like it, but you’ve just done a lot.

1. You created your app
1. By typing `$ npm install`, you told the app to download and install all the packages you need for the app to run.
1. By typing `$ npm run serve` you started a server (locally!)
    + Which is why you can see your app in the browser.

**Coach**: Explain the difference between a local and remote server.
+ A Remote server is (a computer that “serves” webpages – usually somewhere in the cloud, like [https://www.google.com/](https://www.google.com/) or [https://icanhas.cheezburger.com/](https://icanhas.cheezburger.com/).)
+ A Local server is a server that is running ***on your laptop only***. So ***in your browser***, instead of going to www.google.com, you can **type** [http://localhost:8080/](http://localhost:8080/), and it is as if you have gone to a website on the web, only now it is **on your machine**.

---

### Let’s dive in and look at the actual code
+ Open a second terminal to run your terminal commands
+ Open your code in your text editor

Let’s look at what the command $ `vue create my-app-name` created.

Directory name |  explanation 
--- | ---
node_modules | where all our downloaded packages are saved
public | The only folder seen to the world as-is. If you put files in here, they will be served directly without any processing.
src | src stands for “source,” which are the files we are going to alter.
src/App.vue |  the primary file we will start with.
src/assets | where images, JavaScript, stylesheets (CSS) and other static files should go  
src/components | where our “components” go -- we will discuss this a lot in the rest of the tutorial.
src/main.js | our javascript entry point. Only for advanced usage.

### Edit the code
Now that we have a sense of our directory structure, let’s look at some of the files and start altering the code.
#### Strip down the default Vue app
+ Let’s clean up our `App.vue` file into its simplest form.  
We’re getting rid of everything, to show you the simplest version of a Vue.js web-application.
   
#### Open the `src/App.vue` file
+ Look at what is currrently there, then delete it.
+ Copy and paste this simplified code:

```html
<template>
  <div>
    <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
  </div>
</template>

<script>
  export default {

  }
</script>

<style>

</style>
```

#### Delete the /components folder
+ Now, take a look in your browser.
+ You should see the text you wrote: “Welcome to the Viva-LA-Vue Workshop!” in your browser.

#### Next, let's test that our css works, by adding id and styles:
+ Note so far in our Vue.js app, we have only needed to use **standard HTML.** We also use **stardard CSS.**
+ This is a major benefit to the Vue ecosystem.  You can just use the HTML and CSS that you already know. No special languages required.

#### Let’s style our `<div>`: 

A. First, add an “id” to our `<div>`.
`<div id="current-id">`

B. then, we can attach a background-color to that `<div>` via our “current-id” in our `<style>` section:

Down the page, in your `<style>` section, you should create the following id, and add a `background-color`:
```css
  <style>
    #current-id{
      background-color: cornflowerblue;
    }
  </style>
```

#### All together, your page should look like this:

```html

  <template>
    <div id="current-id">
      <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
    </div>
  </template>

  <script>
    export default {

    }
  </script>

  <style>
    #current-id{
      background-color: cornflowerblue;
    }
  </style>

```

####  Coaches discuss:

Note that the styles **automatically** update in the browser. This is not a little thing. This is one of the niceties of modern tooling. We no longer need to press refresh on the browser constantly. With Vue and other modern frontend frameworks, it makes sure to update in the browser for you as much as possible. This makes for a much smoother development workflow. (Sometimes, in some rarer cases, we still need to press refresh).

Do you have blue on your page?  Great, it worked! 

#### We see that it works. Now we can go back to the default css, because it is prettier.

```html
  <style>
    #current-id{
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
    }
  </style>
```
+ You’ll know that it worked if the text is centered, and the background is back to white.

### SPECIAL VUE USAGE Note:
+ For each `<template>` **we need a parent `<div>`** or Vue will throw an error. This is the case for all of these frontend frameworks.
+ Notice that the `<h1>` is within a `<div>` this is critical. We always need ONE parent `<div>` in each of our `.vue` files.

---

## Concept: Overview of the Browser

#### The Browser’s abilities can be broken down in 3 concepts...

+ **HTML**: Text, Organized like a Newspaper. (Hyper-Text Markup Language)
  + We think of each HTML page as a “document.” Much like a Newspaper, text can be organized into different sections like “header” “article” or “aside” (and many more). Because we are linking these pages together, we also use “links” and “buttons.”

+ **CSS**: Style. (Cascading Style Sheets)
  + Used to define the styles for your page and how they will appear. It controls the presentation of your site through position, layout, colors, size, font, et cetera. CSS allows us to style individual elements and/or all the elements at once for our entire web-application.

+ **Javascript**: Behavior.
  + Javascript is the way we create interactive behavior, to engage with the User.  For example, we can make a website that has a *Popup.*  Javascript gives us the ability to do programming in the browser.

Normally, HTML, CSS and Javascript are all written in separate files.  Vue.js makes our lives easier, by grouping related `HTML` `CSS` and `Javascript` in `.vue` files.

In every `.vue` file, there will be these 3 sections, the 1st section will be the html, between `<template>` the 2nd section, will be in the `<script>` section which contains the Javascript, the 3rd section is the `<style>` section, which contains the CSS. 

In Vue.js these abilities are all wrapped together in a nice little package, the `.vue` file. This structure allows us to use `stardard HTML and CSS` together, and sprinkle in little bits of Javascript directly into our HTML code.

#### Our App.vue file:
```html

  <template>
    <div id="current-id">
      <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
    </div>
  </template>

  <script>
    export default {

    }
  </script>

  <style>
    #current-id{
      background-color: cornflowerblue;
    }
  </style>

```

As we can see, the `.vue` file has all 3 parts of what a browser can use: the `HTML`, `CSS`, and `Javascript` (aka: the "js"). It encapsulates the 3 things a browser can understand.

+ **Term**: All together, this .vue file is called a **“component.”**

For example, in our app, **App.vue is a “vue component.”** We will talk a lot more about components later, but for now know that each `.vue` file, is known as a Vue “component” – a mini-package of HTML, CSS, and Javascript, so they can more easily work together.

---
<a name="section-2">Section II.</a>
# Using Data in our App
---

For our next step, we want to add some behavior.  We will make some changes in the Javascript section.

In Javascript, we can create logic like programming “if/else” and “loops” and can also store information as data. 

Let’s create some data which we can then use in our HTML.   We use our Javascript variables to store our data.  First, let’s focus on creating data.

#### Currently, this is our Javascript area:

+ **Note**: We will be using arrows such as these ⮕ to ***help you see new code***.  You should be typing your code.
  + Do **\*not\*** copy these arrows into your code.

*CURRENT:*
```js

  <script>
    export default {

    }
  </script>

```
Let’s create your "data" section.  This is where we will declare our Javascript variables.
+ Technically “we are creating a data method which returns a data object.”


*UPDATE:*
```js

  <script>
    export default {
⮕     data(){
⮕       return {
⮕         // ( This is where your data will go ))
⮕       }
⮕     }
    }
  </script>

```
Let's add a first "variable" in our data.  You should USE YOUR firstName.

*UPDATE AGAIN:*
```js

  <script>
    export default {
      data(){
        return {
⮕         firstName: 'Kamala'
        }
      }
    }
  </script>

```
In our example, we have now “declared a variable,” called **firstName** with a “value” of **Kamala**.

With Vue.js it is super simple to **use** these variables *within our HTML!*

#### Let’s see!

In the HTML, we use double curly brackets like this:
`{{ firstName }}` ← wherever you see this, Kamala will appear.
+ This is called the "template syntax" -- it ***displays*** the variable value.

So now in our HTML aka `<template>` section, we can add another sentence to use our variable.

```html
<div> I am a developer named {{ firstName }}. Watch me as I code in Vue.js! </div>
```

All together your HTML code should look like this:
```html
  <template>
    <div id="current-id">
      <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
      <div> I am a developer named {{ firstName }}. Watch me as I code in Vue.js! </div>
    </div>
  </template>
```

Let’s add another variable, lastName, in out data object:
+ USE YOUR lastName.

*UPDATE:*
```js

  <script>
    export default {
      data(){
        return {
          firstName: 'Kamala', // ← note this new comma.
⮕         lastName: 'Harris'
        }
      }
    }
  </script>

```

#### Note the Syntax:
**IF you get errors**, check for the following...
  1. camelCase (casing matters, begin with lowercase)
  2. comma after firstName
  + Many beginner will miss this and get error
  + errors “are not bad” they are merely guiding you that you have to fix something
  3. the values like lastName value ‘Harris’ is in quotes (single or double quotes are fine).

If you forget the comma, you may see this in your browser:

```js
  Failed to compile.
  ./src/App.vue
  Module Error (from ./node_modules/eslint-loader/index.js):
  /home/one/Desktop/viva-la-vue/src/App.vue
  13:8 error Parsing error: Unexpected token, expected ","
  4 | return {
  5 | firstName: 'Kamala'
  > 6 | lastName: ‘Harris’
  | ^
  7 | }
  8 | }
  9 | }
  ✖ 1 problem (1 error, 0 warnings)

```
#### Temporarily Break your code:
+ \*Temporarily\* remove the comma after firstName. 
  + To experiment, let's purposefully make an error by removing the comma between firstName & lastName. 
+ Look at how clear the errors are in Vue.js.
+ **Errors are a normal part of programming.** *You did not break anything.* Errors are there to help guide you back to the right direction.

Put the comma back, and let's continue.

#### Let’s add the lastName to your HTML using our curly brace, the template syntax. Try to do this yourself.

*CURRENT:*
```html
  <div>I am a developer named {{ firstName }}. Watch me as I code in Vue.js!</div>
```

*UPDATE:*
```html
  <div>I am a developer named {{ firstName }} {{ lastName }}. Watch me as I code in Vue.js!</div>
```

---
<a name="section-3">Section III.</a>
# Dynamic Data
## Updatable Data, Two-Way Binding and Our First Directive v-model.
---

Let's start using data in more interesting ways:
+ Our 1st syntax `{{ firstName }}` is only used to display data in our HTML.
+ However, data is ***meant to be updated*** and displayed.  

We will now learn a 2nd syntax, one that makes our data much more useful.  
+ As we said earlier, Javascript is all about affecting behavior.  
+ What we will learn next will allow us to use logic and make our data updatable.  This is called *dynamic data*.


#### IMPORTANT:
Notice ***where*** this new code is going to go...

**Previous Syntax** (Our "template language"):
+ We put our curly braces **between** the open/close tags of the divs. 
```html
<div> {{ CODE WAS HERE }} <div>
```

**NEW Syntax**:
+ We will be doing stuff **inside the open tag**.
```html
<div CODE NOW HERE> ... <div>
```

## Updating Data via v-model:

In our Vue.js template section, v-model will allow us to update our data in an `<input>` field in the browser.

Let’s compare using a normal HTML `<input>` versus using the Vue.js **v-model** with an `<input>`.

#### Compare Part 1: Standard HTML `<input>`

Add an `<input>` in our HTML (in a new paragraph `<p>`).

+ Basic HTML Refresh: If we want to create an `<input>` it’s like this:
```html
  <p>
    My First Name is: <input type="text">
  </p>
```

All together, our `<template>` area now looks like this:
```html
  <template>
    <div id="current-id">
      <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
      <div>I am a developer named {{ firstName }} {{ lastName }}. Watch me as I code in Vue.js!</div>
      <p>
        My First Name is: <input type="text">
      </p>
    </div>
  </template>
```  

Now, let’s  pre-populate our `<input>` with a default value, like so (this is still standard HTML):
```html
  <p>
    My First Name is: <input type="text" value="Hillary">
  </p>
```

In your browser, try typing over Hillary.  You can try typing in the `<input>` field, but nothing else in the page can change. ***Only* the `<input>` field change.**  It’s because data `value="Hillary"` is **“hard-coded”** which means it will only show the one thing that you told it to display.

This standard HTML `<input>` is limited in 2 ways:
1. We cannot update this data. :(
2. We cannot share this data with the rest of the page.

+ (Advanced: yes, we could send info to the server, but that is a whole new POST/GET cycle, and that’s having the server send us updated data).

Wouldn’t it be nice if we could use one of our variables?

+ Let’s replace our “default” attribute `value="Hillary"` with one of our variables.
+ We will use one of our **variables**, together with **new v-model syntax**.

## Let’s try using Vue’s v-model:
#### Compare Part 2: Vue.js improved `<input>` functionality.

In Vue, we can use v-model to automatically update the data.

*CURRENT* (regular HTML):
```html
  <p>
    My First Name is: <input type="text" value="Hillary">
  </p>
```

*UPDATE* (using our new Vue.js syntax):
```html
  <p>
    My First Name is: <input type="text" v-model="firstName">
  </p>
```
**NOTE**: Make sure to press refresh on your browser.  

You should see “Kamala” in the `<input>`
+ Instead of using the hard-coded `value="Hillary"` we are using a variable, “firstName” in our `<input>`.

Now you are using the “firstName” variable, in our HTML. And, it is doing ***much more***.
+ In your browser, try typing in the <input> box again.
+ WHOA! firstName is being updated EVERYWHERE our “firstName” variable is being used!

+ For fun, you can use it many times.  Try temporarily putting in your vue file:

  `<h2>{{ firstName }} {{ firstName }} {{ firstName }}</h2>`

  + Then try typing in your `<input>` field (in your Browser again). They all update!!

**Term**: We are *“binding”* the `<input>` value to the variable.

Vue.js **automatically** updates the “firstName” variable in our data() area, and then updates everywhere “firstName” 

---

## Our First Directive:
#### Giving your HTML Superpowers
`v-model` is your first taste of a Vue.js **"Directive"**. This little `v-model` line ***makes our HTML "dynamic."***

Remember:
+ Standard HTML is "static."  It merely lays the text across the page.
+ Javascript is programmatic.  It can be used to update data.  It would normally take some sophisticated Javascript to update and share data across the page.   


+ `v-model` is not HTML, or normal Javascript.
  + This is the Vue.js doing a bunch of extremely complicated stuff, giving us an incredibly concise workflow.
  + We can now use `v-model` everywhere, and our "firstName" will be updated.

#### This is the power of the Vue.js Frontend Framework. This is Vue.js!  🔥 🤯 🔥

---

### Try it again yourself.

In the same `<p>` add a lastName `<input>` on your own.
End result: `My Last Name: <input type="text" v-model="lastName">`

All together, your code should currently look like this:
```html
  <template>
    <div id="current-id">
      <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
      <div>I am a developer named {{ firstName }} {{ lastName }}. Watch me as I code in Vue.js!</div>
      <p>
        My First Name is: <input type="text" v-model="firstName">
        <br>
        My Last Name is: <input type="text" v-model="lastName">
      </p>
    </div>
  </template>

  <script>
    export default {
      data() {
        return {
          firstName: 'Kamala',
          lastName: 'Harris'
        }
      }
    }
  </script>

  <style>
    #current-id{
      font-family: 'Avenir', Helvetica, Arial, sans-serif;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      text-align: center;
      color: #2c3e50;
      margin-top: 60px;
    }
  </style>
```

## Directives
#### `v-model` is one example of a Vue.js Directive.

## Concept: Directives allow you to "program" in your HTML code. 

Like we said before, directives are what give HTML superpowers. It allows your HTML to go from dumb to smart. 
+ Standard HTML is merely a way to layout a document. 
+ With Vue.js, you are able to ***program in your HTML code.*** That’s pretty cool!

We can now pepper the HTML with our Directives, in a very clean, organized way. This becomes an incredibly powerful tool as we start to build out a more useful web-application.

*Directives* are one of the central concepts of Vue.js. They make coding in Vue a pleasure. You will see how powerful they are as we start coding.

---

### Aside:
####  Coaches, this might also be new to you...
+ Doing anything dynamic like this used to be extremely time consuming and hard.   
+ DOM manipulation was the way to do everything.
  + Finding elements in the DOM
  + Replacing elements in the DOM
    + It becomes incredibly time consuming and complex.
+ What we just did would have required a ton of work.
  + Not to mention if you wanted to update the data in multiple places, it could be an enormous amount of code.

#### Vue.js and other Frontend Frameworks give us a new way to develop in the browser, make our code more concise, and make it easier to use.

---

## Data with Directives:
#### Understanding how our data() block works together with Directives:

Our current data() block:
```js
  data() {
    return {
      firstName: 'Kamala',
      lastName: 'Harris'
    }
  }
```
Notice our “data” block is the centralized place where all data is stored for that component. 
+ This is a very powerful, uniform way to organize your data.

`v-model` is in fact so powerful, that it might be under appreciated.
+ `v-model` in particular is doing ***two*** things: 
+ This particularly important concept is called “two-way binding.”

#### `v-model` “two-way binding” explained:
1. `v-model` takes the new information you are typing in the `<input>` and ***sends*** the updated "firstName" value ***to the data block***
2. Simultaneously `v-model` instantly ***broadcasts*** that new data ***to our variables***, everywhere “firstName” is displayed.


We see the use of many other **Directives**.

To truly understand Directives, we first need to understand a critical concept called **“events.”** and the workflow around it, **event driven programming**. 

Understanding “event driven programming” is the key “to thinking” as a web-developer.  When you understand “event driven programming” you will appreciate the tools that Vue.js gives you.


---
<a name="section-4">Section IV.</a>
# Events
## Events and Event Driven Programming
---

Event Driven Programming:

1. Events
2. Responding to Events
    + (a.) Event Listeners
    + (b.) Event Handlers

---

## Concept: Overview of Browser Events:

#### 1. Events and 2. Responding to Events

Programming for the web is all about responding to **“events”** that are occurring in the browser, like “clicking,” “scrolling,” “hovering,” and many others that are going on behind the scenes.

As a developer, you ***can*** **decide** to do something if one of these events occur.  We call this **responding to events.**

Let’s think of examples of some events, and what the responses might be. The events often come from a User, and we decide on a response:

Example Events from User |  Possible response from us, the Developer
--- | ---
Click button |  “like” a photo.
Click button |  User goes to the next page.
Go to page for the first time | popup could say “welcome!”
Click “pay now” button |  Send the User’s credit card information to the server, to make a purchase.

There are also tons of events happening that the User is not aware of:
Example Event not from the User |  Possible response from us, the developer
--- | ---
Browser senses that a document changed | automatically saves the document
Timeline update timer goes off | browser asks your server for updated timeline data.
Browser collecting information on what websites you have visited | your data being shared back to the server, to collect information on you.

Hundreds of “events” are occurring every minute.  In fact, there are so many that you couldn’t possibly track all of them. As a developer, you may choose to “respond” to some of those events. 

---

## Responding to Events, in detail:
#### (a.) Event Listeners and (b.) Event Handlers

Let’s say there is an event, like a user “clicked” on a button.

(a.) First, you would want to “listen” for that event.  You are writing code that is waiting for that click to happen. This is called an **Event Listener**.  It waits to listen “did a user click?”

(b.) Then, if that Event Listener fires, you instruct the browser what it should do next. This is called the **Event Handler**.  The Event Handler is the response you probably recognize as a user, such as “seeing that someone 'liked' a photo.”

All together: If a user clicked on a "like" Button (the event), we would listen for the click (the Event Listener waiting for the click), and then we could "show a new 'like'" (the Event Handler pops up the "like" image).

---

## Doing Events in Vue.js: Using v-on

Now that we understand the concepts of Events and Event Driven Programming, let’s see our concepts in action, and learn how we write that code in Vue.js.

(Let’s get back to our code...)

First off, let’s create a new variable, a boolean, that we’ll use shortly.

In our data() section, let’s declare a boolean and set it to ‘true’.

```js
  data() {
    return {
      firstName: 'Kamala',
      lastName: 'Harris', // (note the new comma here)
⮕     myBoolean: true
    }
  }
```

Now, in our template, let’s create a new div and display our boolean in there.  While we’re at it, let’s also add a button:

*ADD*:
```html
  <div>
    <button> Toggle Me </button> This is our boolean: {{ myBoolean }}
  </div>
```

Let’s improve our code further. Inside your `<button>` tag, we will add another Vue.js directive, v-on:

*UPDATE further*:

Adding `v-on:click=“myBoolean = !myBoolean”` inside the `<button>` tag:
```html
  <div>
    <button v-on:click=“myBoolean = !myBoolean”> Toggle Me </button> This is our boolean: {{ myBoolean }}
  </div>
```

---

#### Break Down our `v-on:click=“myBoolean = !myBoolean”` into understandable steps:
Our `v-on:click=“myBoolean = !myBoolean”` directive encapsulates the 3 steps of ***Event Driven Programming*** we just learned about earlier.

First **v-on**, part 1 of 3:
+ “v-on” is basically saying, “start paying attention here” aka start to “listen” here.

Second, v-on:**click**, part 2 of 3:
+ The word “click” is telling Vue ***which event*** to listen for. In this case, we are listening for the button to be clicked.

Last, part 3 of 3, we write the code to tell it what to do. This is the Event Handler.
+ In this case, `myBoolean = !myBoolean` our event handler is saying “toggle our boolean back and forth from true to false.”


All together, your code should currently look like this:
```html
  <div>
    <button v-on:click=“myBoolean = !myBoolean”> Toggle Me </button> This is our boolean: {{ myBoolean }}
  </div>
```

In your browser, try clicking the “Toggle Me” button.
+ We are displaying True or False on the page.
+ The button should switch True/False back and forth.

---

*To recap*:
(the concept together with the Vue.js code)

**Event Listener:**

1. `v-on` ➙ add a listener.
2. `v-on:click` ➙ which type of listener, in this case, a “click”.
  
**Event Handler:**  
  
3. `v-on:click=“myBoolean = !myBoolean”` ➙ An "event handler" can do anything. In this case we are simply toggling myBoolean’s true/false.

---

#### Minor Code Improvement, for reusability.
Let’s take a moment to slightly improve both our Listener and our Handler...

---

##  Improve our Listener:
#### Shortcut: `v-on` is the same as the `@` symbol.

First off, We showed you `v-on`, but “listeners” are such a common part of our code, that there is a shortcut for it. Anywhere you want ***add a listener***, we can simply use the `@` sign instead of `v-on`.
+ **Before**: We wrote our listeners like this: v-on:click=“…”
+ **NEW**: We can write our listeners like this: @click=“…”

Let's replace this in our code:

*BEFORE*:
```html
  <div>
    <button v-on:click=“myBoolean = !myBoolean”> Toggle Me </button> This is our boolean: {{ myBoolean }}
  </div>
```

*UPDATED*:
```html
  <div>
    <button @click=“myBoolean = !myBoolean”> Toggle Me </button> This is our boolean: {{ myBoolean }}
  </div>
```

**Note**: We simple do `@click`


In your browser, test to see that it works. Make sure your boolean is still toggling in the browser.  Should work exactly the same. 
+ This `@` symbol is a minor thing, but since we use listeners everywhere, this is how you will see it in the majority of your Vue.js code.
+ Since there are a ton of events that can happen in the browser, there are a ton of  event listeners you could listen for.
  + As the developer, you can listen for the User to “click” “hover” “scroll” “mouseover” “play” “pause” “drag” “hover” “submit” and many, many more.
  + Therefore, in Vue.js, you can listen by doing `@click=“...”` `@hover =“...”` `@scroll=“...”` etc.

---

##  improve our Handler:
#### Move our handler code into a method.

Now, let’s improve our handler:

Currently, we have `@click="myBoolean = !myBoolean"`
  
In this particular case, we did something **very** simple in our handler.  All we did was toggle the boolean, which *we **could** fit in one line of code.* This is rarely the case.  Our handlers are often performing much more complex actions.

MOST of the time, we want our **handlers to do much more.**  Let’s **refactor** (reorganize our code) into a method (a block of code).

***Coaches:***  If it is not clear, review what a function/method is – but basically “a discrete block of code to accomplish a task.”

#### Let’s move our boolean toggling code into a method, so that our code is more organized.


Refactor our Event Handler into a method:  
(All we are doing here is moving our boolean toggling code into another area).

First off, let’s go back into our javascript `<script>` block, and ***add another section called "methods"***:


*BEFORE*:  
Currently, our entire `<script>` code section looks like this:

```html
  <script>
    export default {
      data() {
        return {
          firstName: 'Kamala',
          lastName: 'Harris',
          myBoolean: true
        }
      }
    }
  </script>
```

Let’s add a new section, called “methods.”
+ Note, this is the same indentation level as data()


*UPDATE*:  
After, adding methods section:

```html
  <script>
    export default {
      data() {
        return {
          firstName: 'Kamala',
          lastName: 'Harris',
          myBoolean: true
        }
      },
      methods: {
        
      }
    }
  </script>
```

We now have a place to add new methods. We will add our first method there in a moment, but first let's start writing that method.

Back above in our HTML, our `@click` handler on our button looked like this:

*BEFORE*:
```html
  <button @click="myBoolean = !myBoolean"> Toggle Me </button> This is our boolean: {{ myBoolean }}
```

We are going to ***move our logic*** `myBoolean = !myBoolean` out of this area, and put somewhere else in our code.  It will be the ***same logic*** only inside a method below.

We are moving our logic into a newly named method, called doSomething(). Then we can call the doSomething() method in our HTML.

*UPDATED*:

```html
  <button @click="doSomething()"> Toggle Me </button> This is our boolean: {{ myBoolean }}
```
(Note: Does \*not\* yet work).


Back to our Javascript “methods” section, let’s write that doSomething() method, with our same boolean logic we can reuse:

*BEFORE*:

```js
  methods: {

  }
```

*UPDATE*:

```js
methods: {
  doSomething(){
    this.myBoolean = !this.myBoolean
  }
}
```

This should result in the same action as before. It merely toggles myBoolean.  Give it a try!

#### This is the exact same logic.
+ The code has one important change.

When ***in the Javascript area*** of our code, ***we need to use `this.` to access variables*** in the data() section.

Review, before: `myBoolean = !myBoolean`

Review, after: `this.myBoolean = !this.myBoolean`

In fact, we usually just "cut & paste" the code from the HTML into your Javascript method.  Then we simply add `this.` in front of the variables.

+ ADVANCED NOTE:  
(For those familiar with vanilla Javascript):  
We are seeing a special Vue.js implementation of `this.` It will make your life much easier later on, but might not be the behavior you've come to expect from `this` in our traditional use of Javascript.   

#### One last fix: Improve our Method Name.

It was important for you to understand that methods “do something” in your code, so we gave our method a very generic doSomething() name.

However doSomething() is actually a terrible method name, because it is so undescriptive. *Method names should always be descriptive*, describing what they are doing.

As a final fix for this section, go ahead and rename your method.  Update the name to `toggleMyBoolean()`.  Let’s remember to do so in your Javascript’s method area, and in your HTML.

**Updated all together:**

in Javascript:

```js
methods: {
  toggleMyBoolean(){
    this.myBoolean = !this.myBoolean
  }
}
```

in our HTML:
```html
  <button @click="toggleMyBoolean()"> Toggle Me </button> This is our boolean: {{ myBoolean }}
```

---
<a name="section-5">Section V.</a>
# Programming Logic in our HTML
## Using another Directive, v-if
---

We have so far seen the use of 2 Vue.js directives: `v-model` and `v-on`.  

#### Let’s learn about one more directive, `v-if`:  

`v-if` is going to give us the power to do ***"if statements" in our HTML!***

Using “conditionals” like an “if” statement is something that is usually reserved for programming logic.  That means that it would only be available to you in Javascript, not in your HTML.
    
Now, watch as the `v-if` directive gives your HTML programming logic, as we use an “if” statement in our HTML.

First off, let’s setup a new div area, with an image in it.  

Below your other HTML code, add this:

```html
  <div>
    <img src="http://www.fillster.com/images/pictures/10p.jpg">
  </div>
```
We’ve just added an image from the internet. Check it out in your browser.

All together in our HTML, our `template` currently looks like this:

```html
  <template>
    <div id="current-id">
      <h1>Welcome to the Viva-LA-Vue Workshop!</h1>
      <div>I am a developer named {{ firstName }} {{ lastName }}. Watch me as I code in Vue.js!</div>
      <p>
        My First Name is: <input type="text" v-model="firstName">
        <br>
        My Last Name is: <input type="text" v-model="lastName">
      </p>
      <div>
        <button @click="toggleMyBoolean()"> Toggle Me </button> This is our boolean: {{ myBoolean }}
      </div>
      <div>
        <img src="http://www.fillster.com/images/pictures/10p.jpg">
      </div>
    </div>
  </template>
```

Let’s focus on our <img> tag:

*CURRENTLY* we have this:
```html
  <div>
    <img src="http://www.fillster.com/images/pictures/10p.jpg">
  </div>
```

If you remember, previously we had setup our `myBoolean` variable, which we could toggle from true/false, with the push of our button in the browser.

Now, let’s use the true/false value for something more useful.

We can **use a new `v-if` Directive** which allows you to put an “if statement” in your HTML.
+ We are adding an “if” to our HTML code!


*UPDATE*:
```html
  <div>
    <img v-if="myBoolean" src="http://www.fillster.com/images/pictures/10p.jpg">
  </div>
```
#### The `v-if` in our HTML is now \*reading the `myBoolean` value.\*

In our case, what this code is saying is “if” myBoolean is true, continue to show the image. “if” myBoolean is false, do not show it any more.
+ v-if true, show the image.  
– or –  
+ v-if false, do not show the image.


This seems simple, and that’s the point!
+ Adding “logic”  to your HTML is NOT normal.
+ Vue.js gives you the tools to do things like this very easily, and conveniently.
  
We have so far seen the use of 3 Directives as we've learned.  Vue.js provides you with many more, and you can even write your own.  These Directives are an incredibly powerful tool, and are a big part of how Vue.js makes it a pleasure to write your frontend code.  


---
<a name="section-6">Section VI.</a>
# Components
## Components: Building Blocks to Assemble your WebApps
---

In this tutorial so far, we’ve spent a lot of time talking about Directives, little bits of code that give your HTML superpowers, so that your HTML goes from a simple document layout methodology, to having programmatic abilities, where you can do things like have “if” statements in your HTML.

#### Components are a Fundamental Concept of Modern Frontend Frameworks.
## Concept: Components are building blocks we create to weave together our larger WebApp.

Another central concept of frontend web-development, is something called **“components.”** In fact, if there is one thing that distinguishes modern frontend frameworks from everything before it, it is the concept of components, and how you use them to assemble your web-apps (short for "web-applications", aka your website).

#### In short, `components` are small individual building blocks you use to assemble into a complete website.

We didn’t discuss it before, but when you were coding in your App.vue file, you were in fact building your first Vue.js “component.”

> You can think of components as Lego blocks. When we build web-apps, we take those blocks (the "component") and assemble them into a complete website.

For now, you can think of components as mostly the “visual parts” of your website.

#### Component Example:
A good example of a “component” that you might want to create is a Button.  But, imagine that ***your button*** had a particular look and feel that belonged to your website. 
  
Of course all websites have buttons, but let’s say that for your website you want your buttons to all have rounded corners, a double pinstripe border, and a fun balloon🎈emoji.
    
Wouldn’t it be nice to make this once, and then just reuse it everywhere in your site? That’s what components are all about.

If you created this, we would call it, your **Button Component**.

---

When you buy a box of Legos, there are different shapes that you can use any way you want. 
However, our first step is to build our own legos.

Unlike legos, we don't neccesarily get any out of the box.  We often need to craft our own individual blocks, and then assemble them into the whole of our website.

---

## Creating a new component:
We are going to create a "Bouncing Ball" component.

Notice: We ***already*** have 1 component. The code we are in App.vue is a component.  In fact, it is our main component.  
  
+ In Vue.js anything that ends with .vue is a component.
+ We will now create additional components, which can be used within our main App.vue component.
+ Note: The concept of “components” exists in all of our modern frontend frameworks. It just happens to be exceptionally clear in Vue.js, that ***Vue.js components are one simple .vue file***.

**Back to our code**:  
To create our first new component, let’s create a new directory, where we will put our new components.
+ (this isn’t strictly necessary, but good for organization).

If you look at the directories and files in your app, you should see a `src/` directory (this stands for “source”).

In the `src/` directory, create a new directory called `components/`

In your terminal, you could do:  
 $ `mkdir src/components/`

Now, let’s create a new file. A file that ends with `.vue` is our new component!  Since we are creating a bouncing ball, why don’t we call it `BouncingBall.vue`.

In your terminal, you could do:  
$ `touch src/components/BouncingBall.vue`
+ We just created a new `BouncingBall.vue` file, inside our new `components/` directory.

Open up BouncingBall.vue and add the following...
+ We are doing some coding for you.  You can just ***copy & paste this into BouncingBall.vue***.

```html

  <template>
    <div class="ball"></div>
  </template>

  <script>

    export default {

    }

  </script>

  <style scoped>

    body {
      display: flex;
      justify-content: center;
    }

    .ball {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      background-color: #FF5722;
    }

  </style>

```

What we have pasted here is simply a `<div>` with some css styles applied to it.

#### This is structured just like App.vue. 

It has the 3 sections that we discussed earlier:
1. the HTML `<template>`   
2. a Javascript `<script>` section, and  
3. an area for our CSS `<styles>`
  
  + This is **OUR** BouncingBall.vue component!
  + We just "created" this component.

Note: You will ***not yet see any changes in the browser.***
+ If you get an error, just keep going, we fix it below...

So far, we have ***"created our component,"*** but have ***not used our component, yet!***

---

Before we continue, let’s clean up our App.vue file a bit, to make room for other code.  

In our App.vue file, let’s get rid of our puppy image.


#### In App.vue.  

***REMOVE***:
```html
  <div>
    <img v-if="myBoolean" src="http://www.fillster.com/images/pictures/10p.jpg">
  </div>
```
***REPLACE WITH***:  

In its place, let’s create a `<div>` and center what is inside the `<div>`:  
(So that what we place inside here, will be in the middle of the page):

```html
  <div style="display:flex; align-items: center; justify-content: center;">

  </div>
```

---

## Using our Component:

We are now going to ***use*** our BouncingBall.vue component for the first time.  

**Note:** This is a 3 step process. You can ignore errors in your browser, until we complete step 3.

#### “import” component (Step 1 of 3):

In your javascript `<script>` area **above your `export` line** we are going to `import` the component you just built.

**In App.vue**:  
(Note: Make sure to do in `App.vue` NOT in `BouncingBall.vue`):

All together, your `<script>` area should look like this:  
(arrows show new code):

```html 

  <script>

⮕  import BouncingBall from "./components/BouncingBall.vue"

    export default {
      data() {
        return {
          firstName: 'Kamala',
          lastName: 'Harris',
          myBoolean: true
        }
      },
      methods: {
        toggleMyBoolean(){
          this.myBoolean = !this.myBoolean
        }
      }
    }
    
  </script>

```

#### Register the Component (Step 2 of 3):

Back inside your “export default” area, we are going to add a new section, called “components” at the same level as “methods” and “data”.  Then, we will “register” that component.

"Registering a component" means we are **telling App.vue** that **BouncingBall.vue exists, and *is a component***  
(but we ***have not used it yet***).  

```js

  export default {
    data() {
      return {
        firstName: 'Kamala',
        lastName: 'Harris',
        myBoolean: true
      }
    },
    methods: {
      toggleMyBoolean(){
        this.myBoolean = !this.myBoolean
      }
⮕  },   // (← notice the new comma here )
⮕  components: {
⮕    BouncingBall
⮕  }
  }

```

+ Here, we are creating a new "Components" section
+ "Registering" the `BouncingBall.vue` component means we are letting `App.vue` know about `BouncingBall.vue`
  1. Let's `App.vue` know that `BouncingBall.vue` *we just imported* **exists**.
  2. Let's `App.vue` know that `BouncingBall.vue` **is a component.**
+ However, we have not "used" the `BouncingBall.vue` component, yet.

#### Using the Component (Step 3 of 3):

We can finally use our new `BouncingBall.vue` component in our `App.vue`!
  
**In App.vue** back up top in our HTML, in the centered `<div>` we created a minute ago, we are going to do something cool.  We will **USE our BouncingBall.vue component**.

**In App.vue**:  

*CURRENTLY*:  
```html
  <div style="display:flex; align-items: center; justify-content: center;">

  </div>
```
Let’s use our `BouncingBall.vue` component in here:  
+ NOTE: For now, this is just a simple ball.  Our ball will ***not*** bounce, yet.

*UPDATED*:

```html
  <div style="display:flex; align-items: center; justify-content: center;">
⮕   <bouncing-ball></bouncing-ball>
  </div>
```

WOW! Notice what we did here? Once we created a component, we can now use it in our code ***just like other element of HTML!***  

Just like `<div>`, `<h1>`, `<img>` and `<p>` tags, we have ***created our own new version of HTML elements.***

> THIS IS the power of components!
> 🔥🔥🔥 We have created our own HTML elements!! 🔥🔥🔥

Moreso, now that we’ve created this `BouncingBall.vue` building block, we can use it over and over again.  
Try using the `<bouncing-ball>` component a few times. See how easy it is to reuse.

(just for fun, try this...)  
**UPDATE**:

```html
<div style="display:flex; align-items: center; justify-content: center;">
  <bouncing-ball></bouncing-ball>
  <bouncing-ball></bouncing-ball>
  <bouncing-ball></bouncing-ball>
</div>
```

We can see that we not only created our component, our little reusable building blocks, but it is suuuuuper easy to use those building blocks over and over again.

### Improve Our Component:

Now that we understand how easy it is to reuse or component, it is a nice time to improve on our ball, and see how the improvement propagates through all of our BouncingBall.vue components.

Right now, ***we** are going to do some coding for you.*  Let us give you an updated version of the `BouncingBall.vue` component (which you will cut and paste from below), so we can focus on a new concept: data flows between components.

(Note: This looks like a lot of code, but it is mostly just some fancy use of normal CSS.)

***UPDATE* BouncingBall.vue:**  
Copy/paste this into BouncingBall.vue:  
(You can completely overwrite what was there before.)


```html
<template>
  <div class="ball" :style="dynamicBallBackgroundColor"></div>
</template>

<script>

  export default {

    data() {
      return {
        ballcolor: '#FF5722'
      }
    },

    computed: {
      dynamicBallBackgroundColor(){
        return `background-color: ${this.ballcolor};`
      },
    },
  }

</script>

<style scoped>

  body {
    display: flex;
    justify-content: center;
  }

  .ball {
    width: 100px;
    height: 100px;
    border-radius: 50%;

    animation: bounce 0.5s;
    animation-direction: alternate;
    animation-timing-function: cubic-bezier(.5,0.05,1,.5);
    animation-iteration-count: infinite;
  }

  @keyframes bounce {
    from { transform: translate3d(0, 0, 0);     }
    to   { transform: translate3d(0, 200px, 0); }
  }

  /* Prefix Support */
  ball {
    -webkit-animation-name: bounce;
    -webkit-animation-duration: 0.5s;
    -webkit-animation-direction: alternate;
    -webkit-animation-timing-function: cubic-bezier(.5,0.05,1,.5);
    -webkit-animation-iteration-count: infinite;
  }

  @-webkit-keyframes bounce {
    from { -webkit-transform: translate3d(0, 0, 0); transform: translate3d(0, 0, 0); }
    to   { -webkit-transform: translate3d(0, 200px, 0); transform: translate3d(0, 200px, 0); }
  }
  
</style>

```

We’ve improved our `BouncingBall.vue` component. Now we should see them bounce!

Let’s play with what we’ve given you!  

In your `BouncingBall.vue` let’s focus on the data() section:

```js

  data() {
    return {
      ballcolor: '#FF5722'
    }
  },

```

Let’s take a look at your new code.  The way we’ve set it up, in our data object, we are simply using a CSS hex color to define the color of the ball.

In `BouncingBall.vue`, let play with our data() section:

Currently we have `#FF5722` which is CSS `orange`.  Go ahead and change that to any valid CSS color. It can be a hex code, or the valid CSS color names if you know them.

+ You could go here to grab any CSS color: [https://www.december.com/html/spec/color.html](https://www.december.com/html/spec/color.html) 
+ For example, try replacing `#FF5722` with any of these valid CSS colors:
  + `red`
  + `LightGreen`
  + `cornflowerblue`
  + `#FFA07A`
  + `rgb(255,215,0)`

The CSS works in the data section here because of some of the coding we did for you called “style binding” (which we will not get to today), but for now let’s continue to focus on this data section.

#### Updating the `ballcolor` data variable in the `BouncingBall.vue` updates all of our `<bouncing-ball></bouncing-ball>` instances.

As you would expect, once you’ve updated the color inside your `BouncingBall.vue` component, you’ll notice that ALL 3 times we used `<bouncing-ball>` updates to that new color. So far, that’s kind of the point of components: ***that they are all uniform.***

But, wouldn’t it be nice if they were slightly more flexible? Wouldn’t it be nice to **give them each individual colors**?

Currently, we are updating the color of **all** of the `BouncingBall.vue` components.

> Wouldn’t it be nice to keep ***most* of the components the same**, but ***give each one a different color***?  That feels like it would make our components **much more useful**.  Allowing them to share **most** of the same functionality, while making them individually unique.

Well, we can!  We can create components that give us **all the value of reusability**, while being **flexible enough to give us useful variations**.


---
<a name="section-7">Section VII.</a>
# Props
## Props: Passing Data Between Components
---

Notice that up until now, all of our data() has been isolated inside each individual component.

## Concept: "Props" allow us to send data \*into\* each component.

**Props** are like data that come from ***outside*** of the component. Specifically, it comes from a parent component.

In our case, App.vue is the “parent” component, and `BouncingBall.vue` is the “child” component.
+ This means we can pass data *from App.vue* ***into*** `BouncingBall.vue`.

Let’s set that up!  

#### Passing "prop data" from `App.vue` into `BouncingBall.vue`

Passing Props is a 2 step process:
1. In the child `BouncingBall.vue` we setup ***which data to expect*** from the parent `App.vue`.
2. Then, in `App.vue` when we will ***pass data into each `<bouncing-ball>` component.***






---
---
---
---
---













---
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

orem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

orem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

orem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


---

# Table of Contents:
  * [I. What is Vue.js?](#section-1)
  * [II. Using Data in our App](#section-2)
  * [III. Our First Directive: v-model](#section-3)
  * [IV. Events](#section-4)
  * [V. Programming Logic in our HTML](#section-5)
  * [VI. Components](#section-6)
  * [VII. Props](#section-7)