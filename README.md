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
    Hello from the viva-LA-vue Workshop!
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

### Next, let's test that our css works, by adding id and styles:

#### Note so far in our Vue.js app, we have only needed to use **standard HTML**  You will see that we also use **stardard CSS.**
+ This is a major benefit to the Vue ecosystem.  You can just use the HTML and CSS that you already know. No special languages required.


Let’s style our div: 

A. First, add an “id” to it.
`&lt;div id="current-id">`
B. then, we can attach a background-color to that &lt;div> via our “current-id” in our &lt;style> section:

    Down the page, in your &lt;style> section, you should create the following id, and add a background-color:
```
    #current-id{


    background-color: cornflowerblue;


    }
```


































---
<a name="section-2">Section II.</a>
# Using Data in our App
---


---
<a name="section-3">Section III.</a>
# Our First Directive: v-model
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