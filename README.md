# Calculator-web
calculator 
Calculator Project Report
📌 1. Title
Simple Calculator using HTML, CSS, and JavaScript
📖 2. Introduction
A calculator is a basic electronic device used to perform mathematical calculations such as addition, subtraction, multiplication, and division.
In this project, we developed a simple calculator using web technologies like HTML, CSS, and JavaScript.
🎯 3. Objective
To create a basic calculator interface
To perform arithmetic operations
To understand DOM manipulation in JavaScript
To improve frontend development skills
🛠️ 4. Tools & Technologies Used
HTML → Structure of calculator
CSS → Styling and design
JavaScript → Functionality and logic
Browser → To run the project
⚙️ 5. Features
Addition (+)
Subtraction (−)
Multiplication (×)
Division (÷)
Clear (AC) button
Delete (Del) button
Real-time display
🧩 6. Working Principle
User clicks buttons (numbers/operators)
Input is stored in a string
When "=" is pressed → calculation is performed using JavaScript
Result is displayed on the screen
💻 7. Code Implementation
🔹 HTML Code
<input type="text" id="inputBox" placeholder="0">
<button>1</button>
<button>2</button>
<button>+</button>
<button>=</button>
<button>AC</button>
<button>Del</button>
🔹 CSS Code (Basic)
body {
    display: flex;
    justify-content: center;
    align-items: center;
}
button {
    padding: 10px;
    margin: 5px;
}
🔹 JavaScript Code
let input = document.getElementById('inputBox');
let button = document.querySelectorAll('button');

let string = "";
let arr = Array.from(button);

arr.forEach(button => {
    button.addEventListener('click',(e) => {

        if(e.target.innerHTML == '='){
            string = eval(string);
            input.value = string;
        }
        else if(e.target.innerHTML == 'AC'){
            string = "";
            input.value = string;
        }
        else if(e.target.innerHTML == 'Del'){
            string = string.substring(0, string.length-1);
            input.value = string;
        }
        else{
            string += e.target.innerHTML;
            input.value = string;
        }
    })
})
📊 8. Output
Calculator interface displayed on screen
Performs operations correctly
Shows result instantly
⚠️ 9. Limitations
Uses eval() (not secure for advanced apps)
Only basic operations supported
No keyboard input support
🚀 10. Future Enhancements
Scientific calculator functions
Keyboard support
Better UI design
Replace eval() with safer logic
📝 11. Conclusion
This project helped in understanding how web technologies work together to create interactive applications. It improved knowledge of JavaScript events and DOM manipulation.
📚 12. References
MDN Web Docs
W3Schools
JavaScript tutorials
