# Lab - Running JavaScript on Start

## Overview

This lab will further help you understand the concepts surrounding Running JavaScript on Start.

Flatapets, a pet adoption center, wants to add functionality to their website that displays a list of pets that are available for adoption. You will need to use your knowledge of Running JavaScript on Start to complete this lab.

## Tools and Resources

It is recommended that you use the Visual Studio Code (VSCode) IDE for this lab.

Useful considerations and terminology:

**Event**: Something a user does on a web page or something that happens on a web page.

**Event handler**: A callback function that executes code in response to an event.

**DOMContentLoaded event**: An event that occurs when the web page’s DOM is fully parsed from the underlying HTML.

Here are some other useful resources:

- MDN
  - [Document](https://developer.mozilla.org/en-US/docs/Web/API/Document)
    - [Document: DOMContentLoaded event](https://developer.mozilla.org/en-US/docs/Web/API/Document/DOMContentLoaded_event)

## Instructions

In this lab, you will practice adding an event listener to allow for the `document` object to listen for the `DOMContentLoaded` event and execute code in response to the event.

**Fork and clone** this lab into your local environment. Navigate into its
directory in the terminal, then run `code .` to open the files in Visual Studio
Code.

Then, open the `index.html` file on your browser to run the application.

Write your code in the `index.js` file. There is some starter code provided in `index.js`.

These are your tasks:

1. Add an event listener to the `document` object that will allow the `document` object to listen for the `DOMContentLoaded` event and will call the `updateDOMElements()` function in response to the `DOMContentLoaded` event.
2. `updateDOMElements()`: The `updateDOMElements()` function has been declared for you, but you will need to write the code that should go inside of this function. When the `updateDOMElements()` function is called, the following actions should take place:
    - The `displayPetDetails()` function is called and the first item from the array stored in the `pets` variable is passed in as an argument to the `displayPetDetails()` function.
    - Iterate over the array stored in the `pets` variable using an array iterator method such as `forEach()`. For each of the pets in the array stored in the `pets` variable, the `addPetImageToPetsDiv()` function is called and the pet is passed in as an argument to the `addPetImageToPetsDiv()` function.
3. `displayPetDetails(pet)`: The `displayPetDetails()` function has been declared for you, but you will need to write the code that should go inside of this function. It has 1 parameter named `pet` whose value should be an `object` that contains the following keys: `name`, `image`, and `description`, when the correct value is passed as an argument into the function. When the `displayPetDetails()` function is called, the following actions should take place:
    - The `textContent` attribute for the `<h2>` element with the class `name` is set to the value of the `name` key for the `object` stored in the `pet` parameter.
    - The `src` attribute for the `<img>` element with the class `detail-image` is set to the value of the `image` key for the `object` stored in the `pet` parameter.
    - The `alt` attribute for the `<img>` element with the class `detail-image` is set to the value of the `name` key for the `object` stored in the `pet` parameter.
    - The `textContent` attribute for the `<p>` element with the id `description-display` is set to the value of the `description` key for the `object` stored in the `pet` parameter.
4. `addPetImageToPetsDiv(pet)`: The `addPetImageToPetsDiv()` function has been declared for you, but you will need to write the code that should go inside of this function. It has 1 parameter named `pet` whose value should be an `object` that contains the following keys: `name`, `image`, and `description`, when the correct value is passed as an argument into the function. When the `addPetImageToPetsDiv()` function is called, the following actions should take place:
    - A new `<img>` element is created.
    - The `src` attribute for the `<img>` element is set to the value of the `image` key for the `object` stored in the `pet` parameter.
    - The `alt` attribute for the `<img>` element is set to the value of the `name` key for the `object` stored in the `pet` parameter.
    - The `<img>` element is appended to the `<div>` element with the id of `pets`.
    - An event listener is added to the `<img>` element that will allow the `<img>` element to listen for a `click` event. The event handler (callback function) for the event listener should call the `displayPetDetails()` function and pass in the `pet` parameter as an argument to the `displayPetDetails()` function.

## Submission and Grading Criteria

When you’re done with this lab, remember to commit and push your changes to GitHub, then submit your work to Canvas using CodeGrade.