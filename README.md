## Ex04 Simple Calculator - React Project

## AIM
To develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
STEP 1
Create a React App.

STEP 2
Open a terminal and run:

npx create-react-app simple-calculator
cd simple-calculator
npm start
STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

STEP 5
Create a new file Calculator.css in src/ and add the styling.

STEP 6
Open src/App.js and modify it.

STEP 7
Start the development server. npm start

STEP 8
Open http://localhost:3000/ in the browser.

STEP 9
Test the calculator by entering numbers and operations.

STEP 10
Fix styling issues and refine content placement.

STEP 11
Deploy the website.

STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
Index.html
```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Glass Calculator</title>
  <link rel="stylesheet" href="index.css">
</head>
<body>

<div class="calculator">
  <input type="text" id="display" disabled placeholder="0">

  <div class="buttons">
    <button onclick="clearDisplay()">C</button>
    <button onclick="deleteLast()">DEL</button>
    <button onclick="append('%')">%</button>
    <button onclick="append('/')">/</button>

    <button onclick="append('7')">7</button>
    <button onclick="append('8')">8</button>
    <button onclick="append('9')">9</button>
    <button onclick="append('*')">*</button>

    <button onclick="append('4')">4</button>
    <button onclick="append('5')">5</button>
    <button onclick="append('6')">6</button>
    <button onclick="append('-')">-</button>

    <button onclick="append('1')">1</button>
    <button onclick="append('2')">2</button>
    <button onclick="append('3')">3</button>
    <button onclick="append('+')">+</button>

    <button onclick="append('0')">0</button>
    <button onclick="append('.')">.</button>
    <button class="equal" onclick="calculate()">=</button>
  </div>
</div>

<script src="index.js"></script>
</body>
</html>

```
Index.css
```
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #ff9a9e, #fad0c4, #fad0c4);
}

.calculator {
  background: rgba(255, 255, 255, 0.15);
  padding: 25px;
  border-radius: 20px;
  width: 320px;
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: 0 8px 20px rgba(0,0,0,0.2);
}

#display {
  width: 100%;
  height: 60px;
  font-size: 26px;
  text-align: right;
  padding: 10px;
  border-radius: 12px;
  border: none;
  margin-bottom: 20px;
  background: rgba(255,255,255,0.2);
  color: #222;
  font-weight: bold;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 12px;
}

button {
  padding: 18px;
  font-size: 18px;
  border: none;
  border-radius: 12px;
  background: rgba(255,255,255,0.25);
  color: #222;
  cursor: pointer;
  backdrop-filter: blur(8px);
  transition: all 0.2s ease-in-out;
}

button:hover {
  background: rgba(255,255,255,0.4);
  transform: translateY(-2px);
}

.equal {
  grid-column: span 2;
  background: #ff6f61;
  color: #fff;
  font-weight: bold;
  box-shadow: 0 4px 10px rgba(255,111,97,0.5);
}

.equal:hover {
  background: #ff5a4b;
}

```


Index.js

```
function append(value) {
  document.getElementById('display').value += value;
}

function clearDisplay() {
  document.getElementById('display').value = '';
}

function deleteLast() {
  const current = document.getElementById('display').value;
  document.getElementById('display').value = current.slice(0, -1);
}

function calculate() {
  try {
    document.getElementById('display').value = eval(document.getElementById('display').value);
  } catch (error) {
    document.getElementById('display').value = 'Error';
  }
}

```
  


## OUTPUT

<img width="1268" height="634" alt="Screenshot 2025-10-30 093802" src="https://github.com/user-attachments/assets/64a212dc-a4d8-4013-b2fa-61789221addb" />


## RESULT
The program for developing a simple calculator in React.js is executed successfully.
