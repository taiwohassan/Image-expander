

Expanding Cards Project

Overview

This project is a simple interactive webpage built with HTML, CSS, and JavaScript. It showcases a set of picture cards that expand when clicked, turning into the active card, while the other cards shrink. The effect is achieved by dynamically adding and removing the active class using JavaScript.

Features
Interactive cards that expand on click.
Only one card is active at a time, while others shrink.
Simple, intuitive design using HTML, CSS, and JavaScript.


How It Works
The webpage contains multiple cards.
When a card is clicked, it becomes the active card.
The active card expands and highlights, while all other cards contract.
Clicking another card removes the active class from the current card and applies it to the newly clicked one.
Code Explanation
JavaScript
The core functionality is handled by the following JavaScript:

javascript
Copy code
const panels = document.querySelectorAll('.panel')

panels.forEach((panel) => {
    panel.addEventListener('click', () => {
        removeActiveClasses()
        panel.classList.add('active')
    })
})

function removeActiveClasses() {
    panels.forEach((panel) => {
        panel.classList.remove('active')
    })
}
The querySelectorAll('.panel') method selects all elements with the class panel.
We loop through each panel and add an event listener for the click event.
When a panel is clicked, it becomes the active panel by adding the active class.
The removeActiveClasses() function ensures that the previously active panel gets its active class removed.
CSS
To make the card visually expand and contract, the active class in CSS is styled accordingly. Example styles may look like this:

css: The styling of the Background Image

Copy code
.panel {
    flex: 1;
    transition: flex 0.5s ease;
}

.panel.active {
    flex: 5;
}
Flexbox is used to control the expansion of the cards.
The transition property ensures a smooth animation when the card expands or shrinks.
How to Use
Clone this repository or download the files.
Open the index.html file in your browser.
Click on any of the picture cards to see the expanding effect.
Project Structure
plaintext
Copy code
/
├── index.html
├── style.css
└── script.js
index.html: The main HTML structure of the webpage.
style.css: The stylesheet defining the layout and style of the cards.
script.js: The JavaScript file that adds the interactive behavior to the cards.
Technologies Used
HTML: Structuring the content of the webpage.
CSS: Styling the cards and layout.
JavaScript: Adding interactivity to the cards.