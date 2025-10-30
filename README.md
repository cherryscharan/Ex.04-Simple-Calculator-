# Ex04 Simple Calculator - React Project
## Date: 01-10-2025
# Register Number:212223220015

## AIM
To  develop a Simple Calculator using React.js with clean and responsive design, ensuring a smooth user experience across different screen sizes.

## ALGORITHM
### STEP 1
Create a React App.

### STEP 2
Open a terminal and run:
  <ul><li>npx create-react-app simple-calculator</li>
  <li>cd simple-calculator</li>
  <li>npm start</li></ul>

### STEP 3
Inside the src/ folder, create a new file Calculator.js and define the basic structure.

### STEP 4
Plan the UI: Display screen, number buttons (0-9), operators (+, -, *, /), clear (C), and equal (=).

### STEP 5
Create a new file Calculator.css in src/ and add the styling.

### STEP 6
Open src/App.js and modify it.

### STEP 7
Start the development server.
  npm start

### STEP 8
Open http://localhost:3000/ in the browser.

### STEP 9
Test the calculator by entering numbers and operations.

### STEP 10
Fix styling issues and refine content placement.

### STEP 11
Deploy the website.

### STEP 12
Upload to GitHub Pages for free hosting.

## PROGRAM
App.jsx
```
import React, { useState } from "react";
import "./App.css";


function App() {
  const [input, setInput] = useState("");
  const [result, setResult] = useState("");

  const handleClick = (value) => {
    setInput((prev) => prev + value);
  };

  const handleClear = () => {
    setInput("");
    setResult("");
  };

  const handleCalculate = () => {
    try {
      const evalResult = eval(input); 
      setResult(evalResult.toString());
    } catch {
      setResult("Error");
    }
  };

  return (
    <div className="calculator-container">
      <h1>Calculator Using React</h1>
      

      <div className="calculator">
        <div className="display-box">
          <input type="text" value={input} readOnly className="display" />
          {result && <div className="result">= {result}</div>}
        </div>

        <div className="buttons">
          <button onClick={() => handleClick("7")}>7</button>
          <button onClick={() => handleClick("8")}>8</button>
          <button onClick={() => handleClick("9")}>9</button>
          <button onClick={() => handleClick("/")}>÷</button>

          <button onClick={() => handleClick("4")}>4</button>
          <button onClick={() => handleClick("5")}>5</button>
          <button onClick={() => handleClick("6")}>6</button>
          <button onClick={() => handleClick("*")}>×</button>

          <button onClick={() => handleClick("1")}>1</button>
          <button onClick={() => handleClick("2")}>2</button>
          <button onClick={() => handleClick("3")}>3</button>
          <button onClick={() => handleClick("-")}>−</button>

          <button onClick={() => handleClick("0")}>0</button>
          <button onClick={() => handleClick(".")}>.</button>
          <button onClick={handleCalculate}>=</button>
          <button onClick={() => handleClick("+")}>+</button>

          <button className="clear" onClick={handleClear}>
            Clear
          </button>
        </div>
      </div>
     
    </div>
    
  );
}

export default App;

```
App.css
```

body{
  background-image:url('./assets/gradient.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.calculator-container {
  text-align: center;
  margin: 150px;
  font-family: Arial, sans-serif;
}

h2 {
  margin-bottom: 5px;
}

p {
  font-size: 14px;
  margin: 3px 0;
}


.calculator {
  background: #f5f5f5;
  width: 300px;
  margin: 20px auto;
  padding: 20px;
  border-radius: 12px;
  box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.2);
}

.display-box {
  text-align: right;
  margin-bottom: 15px;
}

.display {
  width: 100%;
  height: 50px;
  font-size: 20px;
  text-align: right;
  padding: 10px;
  border: none;
  border-radius: 6px;
  background:white;
  box-shadow: inset 0px 2px 4px rgba(0, 0, 0, 0.1);
}

.result {
  margin-top: 5px;
  font-size: 18px;
  font-weight: bold;
  color: #333;
}

.buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 10px;
}

button {
  padding: 15px;
  font-size: 18px;
  border: none;
  border-radius: 8px;
  background: salmon;
  color: white;
  cursor: pointer;
  transition: background 0.3s;
}

button:hover {
  background: grey;
}

button.clear {
  grid-column: span 4;
  background: black;
}

button.clear:hover {
  background: gray;
}


@media (max-width: 400px) {
  .calculator {
    width: 90%;
  }

  button {
    padding: 12px;
    font-size: 16px;
  }
}

```


## OUTPUT

<img width="1017" height="462" alt="image" src="https://github.com/user-attachments/assets/c5580bea-e3e7-4efa-aee9-1c9aced22ed8" />



## RESULT
The program for developing a simple calculator in React.js is executed successfully.
