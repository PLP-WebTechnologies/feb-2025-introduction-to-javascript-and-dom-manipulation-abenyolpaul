# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

  

Get App
# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

HTML File (index.html)
html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation Exercise</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1 id="main-heading">DOM Manipulation Demo</h1>
    </header>
    
    <main>
        <section class="content-section">
            <p id="dynamic-text">This text will change when you click the button below.</p>
            <button id="text-changer" class="action-btn">Change Text</button>
        </section>
        
        <section class="content-section">
            <div id="style-demo" class="box">This box will change style</div>
            <button id="style-changer" class="action-btn">Change Style</button>
        </section>
        
        <section class="content-section">
            <div id="element-container">
                <p>Click the button to add or remove elements.</p>
            </div>
            <button id="toggle-element" class="action-btn">Toggle Element</button>
        </section>
    </main>
    
    <footer>
        <p>&copy; 2023 DOM Manipulation Exercise</p>
    </footer>
    
    <script src="script.js"></script>
</body>
</html>


CSS File (styles.css)
css
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
}

header {
    text-align: center;
    margin-bottom: 30px;
}

.content-section {
    margin-bottom: 30px;
    padding: 20px;
    border: 1px solid #ddd;
    border-radius: 5px;
}

.action-btn {
    padding: 8px 16px;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
}

.action-btn:hover {
    background-color: #45a049;
}

.box {
    width: 200px;
    height: 100px;
    background-color: #f0f0f0;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-bottom: 15px;
    transition: all 0.3s ease;
}

.highlight {
    background-color: #ffeb3b;
    border: 2px solid #ffc107;
    transform: scale(1.05);
}

.new-element {
    background-color: #e3f2fd;
    padding: 10px;
    margin: 10px 0;
    border-left: 4px solid #2196F3;
}




JavaScript File (script.js)
javascript
// Wait for DOM to be fully loaded before executing JavaScript
document.addEventListener('DOMContentLoaded', function() {
    // Task 1: Change text content dynamically
    const textChangerBtn = document.getElementById('text-changer');
    const dynamicText = document.getElementById('dynamic-text');
    
    textChangerBtn.addEventListener('click', function() {
        dynamicText.textContent = "The text has been changed successfully!";
        dynamicText.style.color = "#4CAF50";
        dynamicText.style.fontWeight = "bold";
    });
    
    // Task 2: Modify CSS styles via JavaScript
    const styleChangerBtn = document.getElementById('style-changer');
    const styleDemo = document.getElementById('style-demo');
    
    styleChangerBtn.addEventListener('click', function() {
        styleDemo.classList.toggle('highlight');
    });
    
    // Task 3: Add or remove an element when a button is clicked
    const toggleElementBtn = document.getElementById('toggle-element');
    const elementContainer = document.getElementById('element-container');
    let newElementExists = false;
    let newElement = null;
    
    toggleElementBtn.addEventListener('click', function() {
        if (!newElementExists) {
            // Create new element
            newElement = document.createElement('div');
            newElement.className = 'new-element';
            newElement.textContent = 'This is a dynamically added element!';
            elementContainer.appendChild(newElement);
            toggleElementBtn.textContent = 'Remove Element';
            newElementExists = true;
        } else {
            // Remove the element
            elementContainer.removeChild(newElement);
            toggleElementBtn.textContent = 'Add Element';
            newElementExists = false;
        }
    });
    
    // Bonus: Change the main heading color on mouseover
    const mainHeading = document.getElementById('main-heading');
    
    mainHeading.addEventListener('mouseover', function() {
        mainHeading.style.color = '#2196F3';
    });
    
    mainHeading.addEventListener('mouseout', function() {
        mainHeading.style.color = '';
    });
});
Key Features Implemented:
Well-structured HTML5 document with proper DOCTYPE, semantic elements (header, main, section, footer)

DOM Manipulation:

Changes text content dynamically when button is clicked

Modifies CSS styles via JavaScript (toggle class)

Adds/removes elements when button is clicked

User Interaction:

Responds to button clicks

Includes mouseover effects on heading

Semantic HTML:

Uses appropriate semantic elements

Properly structured document

Styling:

Clean, responsive design

Visual feedback for user actions

The solution demonstrates all the requested functionality while maintaining clean, readable code and good practices.

New chat
Message DeepSeek
AI-generated, for reference only


>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨
