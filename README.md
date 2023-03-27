# 100DAYSOFCODE
A log of all my coding tasks during the School of Code

DAY 1
Arrays

DAY 2 
Objects

Day 3 - HACKATHON
Create a Rock, Paper, Scissors Game.

Day 4
Introduction to the DOM. Using event listeners, create elements and changing text content using JS.

Day 5 
Continuing with the DOM Model. Selecting elements in HTML, event listeners.

Day 6
Creating a Rock, Paper, Scissors game using the DOM model

Day 7
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


Day 8 - HACKATHON

Use APIs to create a trivia game.
Grabbing the questions, using the DOM model to change the HTML for each question.


DAY 9 (HWK)
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

Day 10

CSS Flexbox & CSS Grid
