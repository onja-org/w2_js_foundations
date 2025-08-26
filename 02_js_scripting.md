# Part 2: Introduction to JavaScript Scripting

*Time: 1.5 hours*

## From Environment to Action

You've set up your development workspace and run your first JavaScript program. Now it's time to really dive in and start exploring what JavaScript can do. 

Today we'll move from running single commands to writing actual programs that solve problems and respond to input.

## What You'll Learn

- How to experiment and explore using the Node.js REPL
- Writing your first real JavaScript programs
- Understanding how JavaScript thinks about data and logic
- Building scripts that actually do useful things

---

## Part 1: Exploration & Discovery (30 minutes)

### Meet the REPL: Your JavaScript Playground

REPL stands for **Read-Eval-Print Loop**. It's like having a conversation with JavaScript - you type something, JavaScript responds immediately. A REPL session doesn't save your work and doesn't create a file -- it is just for quick experiments directly in the terminal. When you exit the REPL, everything you did is gone!

**Let's start exploring:**

1. Open your terminal and navigate to your scratch folder: `cd ~/development/scratch`
2. Type `node` and press Enter
3. You should see a prompt that looks like `>` - you're now inside the Node.js REPL!

### Your First REPL Experiments

Try typing one line and then pressing enter. See what happens. Do this for each line below (You can skip the comments, which start with `//`):

```javascript
// Basic math
5 + 3
10 - 4
6 * 7
15 / 3

// What about this?
10 / 3
5 + 3 * 2

// Text (we call this a "string")
"Hello, world!"
"My name is " + "Your Name"

// Questions for JavaScript
5 > 3
10 === 10
"hello" === "goodbye"

// Variables - storing information
let myName = "Your Name"
myName
let myAge = 25
myAge
myName + " is " + myAge + " years old"

// JavaScript can remember things
let x = 10
let y = 5
x + y
x * y

// Functions - teaching JavaScript new tricks
function greet(name) {
  return "Hello, " + name + "!"
}

greet("Alice")
greet("Bob")
greet(myName)
```

**Exploration Questions:**
- What happens when you type just a number vs. a number in quotes?
- Try some math with text - what happens with `"5" + "3"`?
- What if you don't use `let` before a variable name?
- Can you create your own function that does math?

**To exit the REPL:** Type `.exit` or press `Ctrl+C` twice

### Reflection Moment

What surprised you most about these experiments? What questions do you have about how JavaScript works?

---

## Part 2: Your First Real Script (30 minutes)

Now let's take what we learned and build something more substantial. We'll create a personal introduction script that gathers information and tells a story.

### Activity: Personal Introduction Generator

**Create a new file:** `introduction.js` in this lab's folder (it should be `~/development/labs/w2_js_foundations` or similar if you followed the folder scheme from the environment setup lesson)

> **Terminal Tip:** You can create and open the file in one command from your terminal. First navigate to the correct folder with `cd ~/development/labs/w2_js_foundations`, then type `code introduction.js` to open the VS Code text editor. This automatically creates an empty file named `introduction.js` and opens it.

For this exercise, you can choose whether to type it out or copy/paste it into your file. Just know that typing out code (especially when it is new to you or you don't really understand what it is doing) really makes the learning happen more concretely in your mind. This is an important skill to practice as you learn programming and find help or solutions from various sources -- the "fix" or "solution" is actually far less important than the learning that happens when you take your time to try to understand it. Typing it out is a great way to force yourself to slow down and really think about what each part does. On the other hand, sometimes it can just feel like a chore, and can be unnecessary if you are already comfortable with the concepts. Use your judgment (now and in the future)!

```javascript
// Personal Introduction Generator
// This script creates a personalized introduction

// Store information about yourself
let firstName = "Your First Name";
let lastName = "Your Last Name";
let age = 25; // Change to your actual age
let favoriteColor = "blue";
let favoriteFood = "pizza";
let hobby = "reading";

// Calculate some interesting facts
let birthYear = 2024 - age;
let nextAge = age + 1;
let doubleAge = age * 2;

// Create the introduction
console.log("=================================");
console.log("     PERSONAL INTRODUCTION");
console.log("=================================");
console.log();
console.log("Hello! My name is " + firstName + " " + lastName);
console.log("I am " + age + " years old, which means I was born in " + birthYear);
console.log("Next year I will be " + nextAge + " years old!");
console.log();
console.log("Some things I love:");
console.log("- My favorite color is " + favoriteColor);
console.log("- My favorite food is " + favoriteFood);
console.log("- I enjoy " + hobby + " in my free time");
console.log();
console.log("Fun fact: When I'm " + doubleAge + ", I'll be twice as old as I am now!");
console.log();
console.log("Nice to meet you!");
console.log("=================================");
```

**Your turn:**
1. Customize this script with your own information
2. Run it with: `node introduction.js` (Make sure you're in the right folder in your terminal! Use `cd` to navigate if needed, e.g. `cd ~/development/labs/w2_js_foundations`)
3. Experiment with changing the values and running it again

**Try These Modifications:**
- Add more favorite things (favorite book, movie, place)
- Calculate how many days old you are (age * 365)
- Add some personality to the messages
- Include information about where you're from

---

## Part 3: Building Something Interactive (30 minutes)

Let's step it up and create a script that can respond to different situations. We'll build a simple decision-making calculator.

### Activity: Smart Calculator

**Create a new file:** `smart-calculator.js`

```javascript
// Smart Calculator
// This calculator can do different operations and give helpful responses

console.log("🧮 Welcome to the Smart Calculator! 🧮");
console.log();

// Let's define some numbers to work with
let firstNumber = 15;
let secondNumber = 4;

console.log("Today we're working with " + firstNumber + " and " + secondNumber);
console.log();

// Basic operations
let sum = firstNumber + secondNumber;
let difference = firstNumber - secondNumber;
let product = firstNumber * secondNumber;
let quotient = firstNumber / secondNumber;

console.log("📊 CALCULATION RESULTS:");
console.log("Addition: " + firstNumber + " + " + secondNumber + " = " + sum);
console.log("Subtraction: " + firstNumber + " - " + secondNumber + " = " + difference);
console.log("Multiplication: " + firstNumber + " × " + secondNumber + " = " + product);
console.log("Division: " + firstNumber + " ÷ " + secondNumber + " = " + quotient);
console.log();

// Let's make it smart - give different responses based on results
console.log("🤖 SMART ANALYSIS:");

if (sum > 20) {
  console.log("Wow! The sum is greater than 20. That's a big number!");
} else {
  console.log("The sum is 20 or less. Nice and manageable!");
}

if (firstNumber > secondNumber) {
  console.log("The first number (" + firstNumber + ") is larger than the second (" + secondNumber + ")");
} else if (secondNumber > firstNumber) {
  console.log("The second number (" + secondNumber + ") is larger than the first (" + firstNumber + ")");
} else {
  console.log("Both numbers are equal!");
}

if (quotient === Math.floor(quotient)) {
  console.log("Perfect division! " + firstNumber + " divides evenly into " + secondNumber);
} else {
  console.log("Division gives us a decimal: " + quotient);
}

console.log();
console.log("🎉 Calculation complete! Thanks for using Smart Calculator!");
```

**Experiment with this script:**
1. Run it as-is: `node smart-calculator.js`
2. Change the values of `firstNumber` and `secondNumber`
3. Run it again and see how the responses change
4. Try making the numbers equal - what happens?
5. Try making secondNumber larger than firstNumber

**Challenge Extensions:**
- Add more operations (maybe calculating percentages?)
- Add more smart responses based on different conditions
- Calculate and display the average of the two numbers
- Add some ASCII art or emoji to make it more fun

---

## Understanding What You Built

Let's reflect on what you just accomplished:

### Key Programming Concepts You Used

1. **Variables**: Storing and reusing information
2. **Operations**: Making calculations and combining text
3. **Conditional Logic**: Making decisions based on data
4. **Output**: Displaying results in a formatted, user-friendly way

### The Power of Scripts

Notice how your scripts:
- **Remember information** (variables)
- **Process that information** (calculations, comparisons)
- **Respond intelligently** (different outputs based on conditions)
- **Present results clearly** (formatted output)

This is the essence of programming: taking input, processing it, and producing meaningful output.

---

## Connecting to the Real World

The scripts you just built use the same fundamental concepts that power:
- Banking apps (calculating balances, interest)
- Social media (personalizing content based on user data)
- Games (responding to player actions)
- Websites (showing different content to different users)

You're thinking like a programmer now!

---

## Practice Challenges (If Time Permits)

Try building one of these mini-scripts:

### 1. Weather Reporter
Create a script that takes a temperature and gives weather advice:
```javascript
let temperature = 75; // Change this value
// Add logic to give different advice based on temperature
```

### 2. Age Calculator
Build a script that calculates interesting facts about someone's age:
```javascript
let birthYear = 2000; // Change this
let currentYear = 2024;
// Calculate age, decades lived, years until milestones, etc.
```

### 3. Text Formatter
Create a script that takes text and formats it in different ways:
```javascript
let message = "hello world";
// Make it uppercase, count letters, reverse it, etc.
```

---

## Reflection Questions

Before moving to the next session:

1. What was most exciting about writing these scripts?
2. How does JavaScript feel different from HTML and CSS?
3. What would you like to build next?
4. Which part felt most challenging, and why?

---

## Looking Ahead

In our next session, we'll dive deeper into **data types and operators** - understanding exactly how JavaScript thinks about different kinds of information and what operations you can perform on them.

You'll understand why `"5" + "3"` gives a different result than `5 + 3`, and how to use this knowledge to build even more powerful programs.

Great work! You're officially scripting with JavaScript! 🎉
