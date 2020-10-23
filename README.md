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
- swhat a method is
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

In your browser, try typing over Hillary.  You can try typing in the `<input>` field, but nothing else in the page can change. **Only the `<input>` can change.**  It’s because data `value="Hillary"` is **“hard-coded”** which means it will only show the one thing that you told it to display.
+ We cannot really update this, nor share that data with the rest of the page. :(    
+ (Advanced: yes, we could send info to the server, but that is a whole new POST/GET cycle, and that’s having the server send us updated data).





---
---
---
---
---



---
<a name="section-4">Section IV.</a>
# Events
## Events and Event Driven Programming
---


---
<a name="section-5">Section V.</a>
# Programming Logic in our HTML
---


---
<a name="section-6">Section VI.</a>
# Components
## Components: Building Blocks to Assemble your Webpage
---


---
<a name="section-7">Section VII.</a>
# Props
## Props: Passing Data Between Components
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