# Frontend Mentor - Results summary component solution

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

Thanks for checking out my solution! I had a lotta of fun with this one! 

### The challenge

Users should be able to (This is the FrontEnd Mentor part of the challange):

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

Personal Challange:

To make sure our data could be changed, a javascript fetch function was created, in order to fetch data from a json file/backend server.

### Screenshot


![Solution Desktop Preview](Solution%20Desktop%20Preview.png)

![Solution Mobile Preview](Solution%20Mobile%20Preview.png)

## My process

  - Set up the HTML first, made sure all the info was correct
  - Mobile First Coding
  - Backend connection
  
### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

Learned how to connect data from a JSON or Backend Server to the HTML directly, there`s probrably an easier way, but for now, I'm really proud of the code bellow:

...script role="json-fetch">
   let divSummary = document.querySelector('#summary');
    
    fetch('data.json').then(function (response) {
    return response.json();
     }).then(function (obj) {
      obj.data.map((category) => {
      divSummary.innerHTML += 
      `<div id="${category.category}">
      <div id="${category.category}-img">
      <img src="${category.icon}" alt="${category.icon} id="${category.icon}"></img>
      <p>${category.category}</p></div>                          
      <p><span id="bold">${category.score}</span> / 100</p>
      </div>`
      })
    }).catch(function (error) {
    console.error("Something went wrong with the data")
    console.log(error);
    });
    </script>
                

### Continued development

I feel comfortable now to build my first Landing Page from the start.

## Author

- Frontend Mentor - [@balascobaco](https://www.frontendmentor.io/profile/balascobaco)
- Twitter - [@balascobaco](https://twitter.com/balascobaco)

