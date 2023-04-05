# 100DAYSOFCODE
A log of all my coding tasks during the School of Code

## DAY 1
_15th March_

Arrays & Objects 

## DAY 2 
_16th March_

Functions 

## Day 3 - HACKATHON
_17th March_

Create a Rock, Paper, Scissors Game.

## Day 4
_20th March_

CODEWARS - If you can't sleep, just count sheep!! (8KYU)

Introduction to the DOM. Using event listeners, create elements and changing text content using JS.

## Day 5 
_21st March

CODEWARS - Grasshopper - Summation (8KYU)

Continuing with the DOM Model. Selecting elements in HTML, event listeners.

## Day 6
_22nd March_

CODEWARS - Gravity Flip (8KYU)

Creating a Rock, Paper, Scissors game using the DOM model

## Day 7
_23rd March_

Using the DOM to change html items while using incrementcount.
Async functions using fetch and APIs

Changing the second hand of a clock using the DOM model.

const hand = document.querySelector(".hand");
let count = 0
function incrementCount() {
    hand.style.transform = `rotate(${count}deg)`;
    return count += 6;
};
setInterval(incrementCount, 1000);

------
Using async function to grab quotes from a website and changing the H1 content of a html file.

async function getQuote() {
    const response = await fetch ("https://meowfacts.herokuapp.com/");
    const data = await response.json();
    console.log(data)
    let quoteFromData = (data.data[0])
    let h1Quote = document.querySelector("#quote");
    h1Quote.textContent = quoteFromData
    console.log(getQuote);
}
// console.log(getQuote());


## Day 8 - HACKATHON
_24th March_

Use APIs to create a trivia game.
Grabbing the questions, using the DOM model to change the HTML for each question.


## DAY 9 (HWK)
_25th & 26th March_

Task 1:- Create a function that creates an array of a celebritys' names with an extra string that said " is a legend".
Then create a new function that does the same but only returns the celebrities whose name starts with a vowel.

const celebs = [
  "David Beckham",
  "Cher",
  "Madonna",
  "Tom Petty",
  "Cristiano Ronaldo",
  "Whoopi Goldberg",
  "Samuel L Jackson",
  "Angelina Jolie",
  "Richard Osman",
  "Emma Thompson"
];

function makeLegend(name){
  return `${name} is now a legend.`
const legendaryCelebs = [];  

for (let i = 0; i < celebs.length; i++) {
  legendaryCelebs.push(makeLegend(celebs[i]));
}

const vowelCelebs = [];

for (let i = 0; i < celebs.length; i++){
  let firstLetter = celebs[i][0].toLowerCase();
  if (firstLetter === "a" || firstLetter === "e" || firstLetter === "i" || firstLetter === "o" || firstLetter === "u") {
    vowelCelebs.push(makeLegend(celebs[i]));
  } 
}

console.log(vowelCelebs)

-----
Task 2:- 
Code that starts a timer linked to a html element. Timer stops at 12 seconds.

let count = 0
let myInterval = setInterval(function() {
    document.querySelector("p").innerHTML++;
    count ++;
    if (count >= 12) {
        clearInterval(myInterval)};
}, 1000);

-----
Task 3:- 
A function that generates a cat photo taken from an API on each reolad of the page.

async function getCatPic() {
    const response = await fetch ("https://api.thecatapi.com/v1/images/search");
    const data = await response.json();
    const imageUrl = data[0].url;
    document.getElementById("cat-here").src = imageUrl
}

console.log(getCatPic());

## Day 10
_27th March_

CODEWARS - Count the number of cubes with paint on (8KYU)
         - Sentence Smash (8KYU)


CSS Flexbox & CSS Grid. Introduction to the flexbox and grid. Understanding the concepts behind them and having a play with its functionality.

## Day 11
_28th March_

CODEWARS - Remove String Spaces (8KYU)
         - Opposite number (8KYU)

Clone a page using HTML & CSS. I cloned Uber Eats home page from scratch, including adding a navigation bar, new background, new fonts with sizing and search bar.

## Day 12
_29th March_

CODEWARS - Convert a Number to a String! (8KYU)

Using figma to create wireframes. 

## Day 13 - Hackathon
_31st March_

Using our knowledge of figma and wireframes, we created a UI/UX experience for a fictional bootcamp. Reseaching our business, its competitors (The School of Music Production) to create user personas for our target audience to design our website appropriately.

See a pdf of our website here ---> [SoM.pdf](https://github.com/lastcastleofbowser/100DAYSOFCODE/files/11124026/SoM.pdf)

## Day 13 (HWK)
_1st & 2nd April_


## Day 14
_3rd April_

CODEWARS - String repeat (8KYU)

 Introduction to Node.js. In our groups we used Node to run js files without the use of a browser. We learnt how to:
 - call js files using node
 - create json files
 - install third party code for running tests
 
## Day 15 
_4th April_

CODEWARS - Keep Hydrated (8kyu)

Introduction to Jest testing. We learnt how to:
- import and export code from different js files
- use matchers to test our functions were operating as they should


## Day 16
_5th April_

CODEWARS - Convert boolean values to strings 'Yes' or 'No'. (8kyu)

Introduction to Playwright. In our groups we had a webpage to write end-to-end tests on to check that it was functioning accurately. We looked at:
- how to import global tests from Playwright
- how to select areas within a webpage
- how to use actions, locators and assertions
- how to use tests to enter text and navigate within a page to check its functionality

## Day 17 - HACKATHON
_6th April_


## Day 18 (HWK)
_7th - 9th April_

## Day 19
_11th April_


## Day 20
_12th April_


## Day 21
_13th April_


## Day 22 - HACKATHON
_14th April_


