# Part 1: Setting Up Your JavaScript Development Environment

*Time: 1 hour*

## Welcome to Real Programming

You've been writing HTML and CSS, styling beautiful web pages. But now we're crossing into a new territory: **programming**. JavaScript isn't just about making things look good—it's about making things *happen*. 

Today you'll set up the tools that will be your companions for the rest of your JavaScript journey.

## What You'll Understand By the End

- What those mysterious `npm install` commands were actually doing
- Why VS Code, Node, and npm work together as a team
- How your computer's terminal works (and why VS Code's terminal is the same thing)
- The difference between JavaScript in your browser and JavaScript on your computer

---

## The Big Picture: Your Development Ecosystem

Before we dive into installation, let's understand what we're building. Think of your development environment like a workshop:

- **VS Code** = Your workbench (where you craft your code)
- **Node.js** = JavaScript that can talk to your computer (not just browsers)
- **npm** = The massive shared toolbox where millions of developers contribute tools
- **Terminal/Shell** = Your direct line to give commands to your computer

### JavaScript's Two Homes

JavaScript originally lived only in web browsers. But now it has two homes:

1. **In the Browser**: Making web pages interactive
2. **On Your Computer (Node.js)**: Building applications, running scripts, powering servers

This is huge! It means you can use the same language for websites AND for programs that run directly on computers.

---

## Demystifying the Command Line

Remember when you ran `npm install` and `npm test`? You were using something called a **terminal** (or **command line**). Let's demystify this before we go further.

### What is a Terminal?

A terminal is simply a text-based way to give commands directly to your computer. Instead of clicking buttons and icons, you type what you want to do.

### What is a Shell?

A shell is the interpreter that understands your text commands. Common shells include:
- **bash** (common on older systems)
- **zsh** (common on newer Mac systems)
- **PowerShell** (Windows)

Don't worry about the differences—they all do basically the same thing.

### VS Code Terminal vs "Real" Terminal

Here's something that confuses many beginners: **The terminal inside VS Code is exactly the same as opening your computer's terminal application.** 

VS Code just gives you convenient access to your computer's terminal without leaving your code editor. When you press ``Ctrl + ` `` (or ``Cmd + ` `` on Mac) in VS Code, you're opening the same terminal you could access through your computer's Terminal or Command Prompt application.

### The Concept of "Where Am I?"

Your terminal is always **pointing** to some location on your computer—to specific folders (called directories). This is why sometimes commands work and sometimes they don't:

- When you open VS Code's terminal, it starts in your project folder
- When you open your computer's terminal, it might start in your home folder
- Commands like `npm install` look for files like `package.json` in the current folder (so if you open the terminal in the wrong folder, it won't find them when you run the command)

You can always see where you are by typing `pwd` (print working directory).

You will often use commands like `cd` (change directory) to navigate to the right folder. For example, `cd ~` takes you to your home folder. `cd ..` takes you up one folder. `cd foldername` takes you into a folder called `foldername`.

**Try This:** Open VS Code's terminal and type `pwd`. Then open your computer's terminal and type `pwd`. See the difference? Then type `ls` (or `dir` on Windows) in both to see the files in each location. Try navigating with `cd` from your home folder to find your project folder. These commands are important and will help you to understand where you are in your file system.

---

## Installation Guide

Even if you already have these tools installed, it's worth understanding what each one does and how to install them fresh (for future reference or new computers).

### 1. Installing VS Code

**What it is:** A free, powerful code editor made by Microsoft.

**Why we use it:** 
- Excellent JavaScript support
- Built-in terminal
- Thousands of helpful extensions
- Used by millions of developers worldwide

**To install:**
1. Go to [https://code.visualstudio.com/](https://code.visualstudio.com/)
2. Download for your operating system
3. Follow the installation instructions

**Test it:** Open VS Code and create a new file. Save it as `test.js` and type `console.log("Hello, world!");`

**Note:** VS Code is not the only free and open-source code editor, but it is a great option for beginners and experienced developers. If you have another favorite code editor and are willing to figure out how to do things in that editor, feel free to use it. Many code editors provide similar functionalities and there is no "correct" editor to use!

> **Tip:** Did you know that you could open VS Code directly from your terminal? Whatever directory your terminal is in, if you type `code .` (with a space and a dot), it will open VS Code in that directory. This is super handy for quickly jumping into your projects. Someday you may even prefer using the terminal to get around your computer instead of clicking around with a mouse! Seems crazy right now? Just wait!

### 2. Installing Node.js

**What it is:** JavaScript runtime that lets you run JavaScript on your computer (not just in browsers).

**Why we need it:**
- Run JavaScript files directly on your computer
- Comes bundled with npm (package manager)
- Powers many development tools

**To install:**
1. Go to [https://nodejs.org/](https://nodejs.org/)
2. Download the LTS (Long Term Support) version
3. Follow the installation instructions

**Test it:** 
1. Open a terminal (VS Code's terminal or your computer's)
2. Type `node --version`
3. You should see a version number like `v18.17.0`


### 3. Understanding npm (comes with Node.js)

**What it is:** Node Package Manager - a massive library where developers share code tools.

**Why it's amazing:**
- Millions of free, open-source packages
- Handles dependencies automatically
- Standard way JavaScript developers share tools

**Test it:**
1. In your terminal, type `npm --version`
2. You should see a version number

---

## Exploration Time: Understanding What You Have

Now that everything is installed, let's explore what these tools actually do.

### Activity 1: Exploring npm's Magic

Remember those `npm install` commands you've been running? Let's see what they actually did.

1. Open VS Code in a project where you previously ran `npm install`
2. Look in the file explorer - do you see a folder called `node_modules`?
3. Open that folder and explore

**What you're seeing:** All the code packages that npm downloaded for you. Each folder is a different tool or library created by developers around the world.

**Mind-blowing fact:** That `node_modules` folder might contain thousands of files and hundreds of packages, all working together to power your project.

### Activity 2: VS Code Feature Discovery

VS Code can do much more than just edit text files.

**Explore these features:**
1. **Integrated Terminal:** Press `Ctrl+`` (or `Cmd+`` on Mac)
2. **File Explorer:** The sidebar on the left
3. **Extensions:** Click the squares icon in the sidebar
4. **Command Palette:** Press `Ctrl+Shift+P` (or `Cmd+Shift+P`)

**Try installing a JavaScript extension:**
1. Go to Extensions
2. Search for "JavaScript"
3. Install "JavaScript (ES6) code snippets"

### Activity 3: Your First Node.js Program

Let's run JavaScript outside of a browser for the first time.

1. In VS Code, create a new file called `hello.js`
2. Type: `console.log("Hello from Node.js!");`
3. Save the file
4. Open VS Code's terminal
5. Type: `node hello.js`

**What just happened?** You ran JavaScript directly on your computer using Node.js. No browser needed!

---

## Understanding the Connections

By now you should be starting to see how these tools work together:

- **VS Code** gives you a powerful environment to write code
- **Node.js** lets you run that JavaScript code on your computer
- **npm** provides thousands of tools and libraries to enhance your projects
- **Terminal** is your direct line to control all of these tools

### The Development Workflow

This is the basic cycle you'll follow:

1. **Write** code in VS Code
2. **Run** code using Node.js through the terminal
3. **Install** helpful packages using npm
4. **Debug** and explore using various tools

---

## Reflection Questions

Before moving on to the next part, take a moment to think about:

1. What was the most surprising thing you learned about your development environment?
2. How does understanding the terminal change your mental model of how computers work?
3. What questions do you still have about these tools?

---

## Looking Ahead

In the next session, we'll start writing and running JavaScript programs. You now have the foundation to understand:

- Why we run `node filename.js` to execute our programs
- How npm packages can add superpowers to our code
- Why the terminal is our friend, not something to fear

Your development environment is now ready. Let's start programming!
