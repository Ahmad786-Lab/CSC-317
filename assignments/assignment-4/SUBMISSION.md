CSC 317 Assignment 4 Submission

Name: Muhammad Ahmad
Student ID: 923336346
GitHub Username: Ahmad786-lab
Assignment Number: 4

Description:
In this assignment, I created a simple iOS-style calculator using HTML, CSS, and JavaScript. The calculator performs basic arithmetic operations and provides a clean, user-friendly interface.

Approach / What I Did:

I structured the HTML to be clear and semantic, organizing buttons and display areas in a way that mimics an iPhone-style calculator. I styled it using CSS Flexbox for layout and added interactivity using JavaScript. I ensured that each button responds to user clicks and updates the display accordingly.

Assignment Explanation:

This code builds a calculator layout with number and operator buttons. JavaScript handles button clicks, performs calculations, and updates the display in real time.

Code Explanation:

The evaluate() function performs the selected math operation (add, subtract, multiply, divide) between two numbers when the equals button is clicked. It updates the calculator display with the result and resets the current operation afterward.

function evaluate() {
  if (currentOperation === null || shouldResetDisplay) return;

  secondOperand = parseFloat(display.textContent);
  let result;

  switch (currentOperation) {
    case 'add':
      result = firstOperand + secondOperand;
      break;
    case 'subtract':
      result = firstOperand - secondOperand;
      break;
    case 'multiply':
      result = firstOperand * secondOperand;
      break;
    case 'divide':
      result = secondOperand === 0 ? 'Error' : firstOperand / secondOperand;
      break;
    default:
      return;
  }
  display.textContent = result;
  currentOperation = null;
}  
