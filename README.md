# 100DAYSOFCODE / School of Code Diary 

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

Creating a wireframe and mock up for my own personal website. I used figma to create my design and I am in the stages of using HTML, CSS and JS to code it into a fully operational website to display my work.

![Landing_Page](https://user-images.githubusercontent.com/123087687/230148452-609a635f-4315-47ab-9370-e1fce0e8c06f.png)
![Work_Page](https://user-images.githubusercontent.com/123087687/230148491-91f550d5-980c-44a1-b529-1b4ac1f57205.png)
![About_Page](https://user-images.githubusercontent.com/123087687/230148505-bf698008-235a-4a5a-8e1f-486f30b2c52d.png)
![Contact_Page](https://user-images.githubusercontent.com/123087687/230148512-aa250c64-2159-4df2-8fa8-36c28b20f0dc.png)


## Day 14
_3rd April_

CODEWARS - String repeat (8KYU)

 Introduction to Node.js. In our groups we used Node to run js files without the use of a browser. We learnt how to:
 - call js files using node
 - create json files
 - install third party code for running tests
<img src = "https://user-images.githubusercontent.com/123087687/230150744-07ff365d-1ac5-4f0c-bcf2-5948e77ac827.png" width = "1000" height = "200">

## Day 15 
_4th April_

CODEWARS - Keep Hydrated (8kyu)

Introduction to Jest testing. We learnt how to:
- import and export code from different js files
- use matchers to test our functions were operating as they should
<img src = "https://user-images.githubusercontent.com/123087687/230148956-aa40368a-bfb6-4c9e-bb27-3f51dbe261db.png" width = "830" height = "200">

## Day 16
_5th April_

CODEWARS - Convert boolean values to strings 'Yes' or 'No'. (8kyu)

Introduction to Playwright. In our groups we had a webpage to write end-to-end tests on to check that it was functioning accurately. We looked at:
- how to import global tests from Playwright
- how to select areas within a webpage
- how to use actions, locators and assertions
- how to use tests to enter text and navigate within a page to check its functionality
<img src = "https://user-images.githubusercontent.com/123087687/230148825-798e7a0d-8aa7-49ce-9b50-ff6d2117f1df.png" width = "1000" height = "200">



## Day 17 - HACKATHON
_6th April_

Playwright testing challenge


## Day 18 (HWK)
_7th - 9th April_

Playwright Hwk challenge

## Day 19
_11th April_
![Screenshot 2023-04-13 at 16 51 45](https://user-images.githubusercontent.com/123087687/232526622-64c6de8f-84ee-46f0-8d6c-e9f01e9c14f2.png)
![Screenshot 2023-04-13 at 16 52 41](https://user-images.githubusercontent.com/123087687/232526624-47d7eb71-9ce1-4169-af11-440491453909.png)
![Screenshot 2023-04-13 at 16 51 36](https://user-images.githubusercontent.com/123087687/232526628-9207bb00-ec25-4346-a989-7ecfc462da08.png)


## Day 20
_12th April_
![Screenshot 2023-04-13 at 16 57 18](https://user-images.githubusercontent.com/123087687/232526658-7e228129-b2ad-445e-9d84-8c9ada40e051.png)
![Screenshot 2023-04-13 at 16 57 34](https://user-images.githubusercontent.com/123087687/232526662-4c98f62c-80b4-4d5d-a8cb-0c0f76913894.png)
![Screenshot 2023-04-13 at 16 57 40](https://user-images.githubusercontent.com/123087687/232526669-4dce381e-0187-48ec-a804-3655e64a7f76.png)
![Screenshot 2023-04-13 at 16 57 05](https://user-images.githubusercontent.com/123087687/232526671-3c36f2ea-123a-421d-8f89-95775e9d3e54.png)


## Day 21
_13th April_

![Screenshot 2023-04-13 at 16 33 57](https://user-images.githubusercontent.com/123087687/232526303-14969bcd-9466-4983-ad58-4798e26f91c0.png)
![Screenshot 2023-04-13 at 16 34 14](https://user-images.githubusercontent.com/123087687/232526309-7fdc2cd1-9164-42b6-b536-00c717316b72.png)
![Screenshot 2023-04-13 at 16 34 07](https://user-images.githubusercontent.com/123087687/232526312-99eb2460-e0dc-4fcf-b881-b319e2a5eb15.png)

## Day 22 - HACKATHON
_14th April_

Creating a Todo list in React with the following features:
- a text input where the todos can be typed
- includes an add button
- using the spread operator to add the item to the end of the list
- includes a functioning delete button

## Day 23 - (HWK)
_15th April - 16th April _

Creating a blogpost page in React with the following features:
- a blogpost containing images, captions and text
- a comment list underneath the main blogpost
- a comment input textbox that allows users to type in their own comment 
- the comment list to add to the end of the lists and not effect them


## Day 24
_17th April_
Introduction to useEffects.
- Changing the document title of a document when todo list is updated.

![useEffect changing the title of a document when to do list updates ](https://user-images.githubusercontent.com/123087687/232524437-87af4371-845b-46be-84f9-b255a339b6b7.png)


## Day 25
_18th April_


## Day 26
_19th April_

## Day 27
_20th April_

## Day 28 - HACKATHON
_21st April_





