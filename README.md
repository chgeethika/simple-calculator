## Aim:Design a Webpage using JavaScript eith a minimum of five mathematical operations.
# program:

## style.css
.calculator {
    height:300px;
    width: 200px;
    margin: 50px auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 3px;
    text-align: center;
    background-color: skyblue;
  }
  
  #display {
    width: 100%;
    margin-bottom: 10px;
    padding: 5px;
  }
  
  .keys {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-gap: 5px;
  }
  
  button {
    padding: 10px;
    font-size: 18px;
    background-color: grey;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #ccc;
  }  
  
## index.js

let expression = '';

function appendNumber(num) {
  expression += num;
  updateDisplay();
}

function appendOperator(op) {
  expression += op;
  updateDisplay();
}

function clearDisplay() {
  expression = '';
  updateDisplay();
}

function calculate() {
  try {
    const result = eval(expression);
    document.getElementById('display').value = result;
    expression = result.toString();
  } catch (error) {
    document.getElementById('display').value = 'Error';
    expression = '';
  }
}

function updateDisplay() {
  document.getElementById('display').value = expression;
}

## calc.html

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
    <div>
        <center><h1>CH.Geethika(212221040032)</h1></center>
    </div>
  <div class="calculator">
    <input type="text" id="display" readonly>
    <div class="keys">
      <button onclick="appendNumber()">(</button>
      <button onclick="appendNumber()">)</button>
      <button onclick="clearDisplay()">C</button>
      <button onclick="appendOperator('%')">%</button>
      <button onclick="appendNumber('7')">7</button>
      <button onclick="appendNumber('8')">8</button>
      <button onclick="appendNumber('9')">9</button>
      <button onclick="appendOperator('*')">*</button>
      <button onclick="appendNumber('4')">4</button>
      <button onclick="appendNumber('5')">5</button>
      <button onclick="appendNumber('6')">6</button>
      <button onclick="appendOperator('-')">-</button>
      <button onclick="appendNumber('1')">1</button>
      <button onclick="appendNumber('2')">2</button>
      <button onclick="appendNumber('3')">3</button>
      <button onclick="appendOperator('+')">+</button>
      <button onclick="appendNumber('0')">0</button>
      <button onclick="clearDisplay()">.</button>
      <button onclick="appendOperator('/')">/</button>
      <button onclick="calculate()">=</button>
      
    </div>
  </div>
  <script src="index.js"></script>
</body>
</html>

# Output:
![Screenshot (446)](https://github.com/chgeethika/simple-calculator/assets/142209368/1793c9ba-6a45-4200-862e-ffe99f907859)

![Screenshot (447)](https://github.com/chgeethika/simple-calculator/assets/142209368/c89b66d0-b77a-449d-8d5a-029792b0b858)

