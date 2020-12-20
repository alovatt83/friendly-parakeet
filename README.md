# Password Generator
>  This application allows the user to select uppercase, lowercase, numbers or special characters to automatically generate a secure password.

## Table of contents
* [General info](#general-info)
* [Screenshots](#screenshot)
* [Technologies](#technologies)
* [Setup](#setup)
* [Features](#features)
* [Status](#status)
* [Contact](#contact)

## General info
Third weekly assignment due on Sunday December 20, 2020 @ 11:59 PM.
## Screenshot
![Homepage Screenshot](https://alovatt83.github.io/portfolio-alovatt/assets/images/screenshot.png)

## Technologies
* HTML
* CSS
* JavaScript


## Setup
Clone files into your own root directory, file extensions are relative and will operate normally.

## Code Examples
Show examples of usage:

HTML:

 <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Password Generator</title>
    <link rel="stylesheet" href="./assets/css/style.css" />
  </head>
  <body>
    <div class="wrapper">
      <header>
        <h1>Password Generator</h1>
      </header>
      <div class="card">
        <div class="card-header">
          <h2>Generate a Password</h2>
        </div>
        <div class="card-body">
          <textarea
            readonly
            id="password"
            placeholder="Your Secure Password"
            aria-label="Generated Password"
          ></textarea>
        </div>
        <div class="card-footer">
          <button id="generate" class="btn">Generate Password</button>
        </div>
      </div>
    </div>

CSS:
  html,
body,
.wrapper {
  height: 100%;
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
  background-color: #f9fbfd;
}

.wrapper {
  padding-top: 30px;
  padding-left: 20px;
  padding-right: 20px;
}

header {
  text-align: center;
  padding: 20px;
  padding-top: 0px;
  color: hsl(206, 17%, 28%);
}

.card {
  background-color: hsl(0, 0%, 100%);
  border-radius: 5px;
  border-width: 1px;
  box-shadow: rgba(0, 0, 0, 0.15) 0px 2px 8px 0px;
  color: hsl(206, 17%, 28%);
  font-size: 18px;
  margin: 0 auto;
  max-width: 800px;
  padding: 30px 40px;
}

.card-header::after {
  content: " ";
  display: block;
  width: 100%;
  background: #e7e9eb;
  height: 2px;
}

.card-body {
  min-height: 100px;
}

.card-footer {
  text-align: center;
}

.card-footer::before {
  content: " ";
  display: block;
  width: 100%;
  background: #e7e9eb;
  height: 2px;
}

.card-footer::after {
  content: " ";
  display: block;
  clear: both;
}

.btn {
  border: none;
  background-color: hsl(360, 91%, 36%);
  border-radius: 25px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 1px 6px 0px rgba(0, 0, 0, 0.2) 0px 1px 1px
    0px;
  color: hsl(0, 0%, 100%);
  display: inline-block;
  font-size: 22px;
  line-height: 22px;
  margin: 16px 16px 16px 20px;
  padding: 14px 34px;
  text-align: center;
  cursor: pointer;
}

button[disabled] {
  cursor: default;
  background: #c0c7cf;
}

.float-right {
  float: right;
}

#password {
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  border: none;
  display: block;
  width: 100%;
  padding-top: 15px;
  padding-left: 15px;
  padding-right: 15px;
  padding-bottom: 85px;
  font-size: 1.2rem;
  text-align: center;
  margin-top: 10px;
  margin-bottom: 10px;
  border: 2px dashed #c0c7cf;
  border-radius: 6px;
  resize: none;
  overflow: hidden;
}

JavaScript:

var lowercase = "abcdefghijklmnopqrstuvwxyz";
var uppercase = "ABCDEFGHIJKLMNOPQRSTUZWXYZ";
var numbers = "0123456789";
var special = "!#$%&'()*+,-./:;<=>?@[\]^_`{|}~";
var passwordReturn = document.querySelector ("#password");
var generator = document.querySelector ("#generate");

// Generate Function
function createPassword () {

var password = "";
var passwordSelect = "";

//Character Length Selection
var passwordLength = window.prompt ("What length would you like your password to be?");
    if (
// Character Validity Checker
    passwordLength >128 ||  passwordLength <8 ) { window.alert ("Please enter a valid number, between 8 and 128.");
    return;}
// Include Number Selection
var characterSettings0 = window.confirm ("Include numbers?");
    console.log (characterSettings0);

    if (characterSettings0) {passwordSelect += numbers;} 
    console.log (passwordSelect);
// Include Special Character Selection      
var characterSettings1 = window.confirm ("Include special characters?");
    console.log (characterSettings1);

    if (characterSettings1) {passwordSelect += special;} 
    console.log (passwordSelect);
// Include Lowercase Letters Selection      

var characterSettings2 = window.confirm ("Include lowercase letters?");
    console.log (characterSettings2);

    if (characterSettings2) {passwordSelect += lowercase;} 
    console.log (passwordSelect);
// Include Uppercase Letters Selection      
var characterSettings3 = window.confirm("Include uppercase letters??");
    console.log (characterSettings3);

    if (characterSettings3) {passwordSelect += uppercase;} 
    console.log (passwordSelect);

## Features
List of features
* Inputs for characters wanted in password.
* Limits automatically set for characters in password length.
* Character randomizer added to scramble selected inputs.

To-do list:
* Project completed

## Status
Project is: completed. Assignment ready for submission.

## Contact
Created by Allen Lovatt - allenlovatt@gmail.com
