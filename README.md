<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Calculadora Simple</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="calculator">
        <input id="display" type="text" class="display" disabled />
        <div class="buttons">
            <button class="button" onclick="appendToDisplay('7')">7</button>
            <button class="button" onclick="appendToDisplay('8')">8</button>
            <button class="button" onclick="appendToDisplay('9')">9</button>
            <button class="button operator" onclick="appendToDisplay('/')">/</button>
            
            <button class="button" onclick="appendToDisplay('4')">4</button>
            <button class="button" onclick="appendToDisplay('5')">5</button>
            <button class="button" onclick="appendToDisplay('6')">6</button>
            <button class="button operator" onclick="appendToDisplay('*')">*</button>
            
            <button class="button" onclick="appendToDisplay('1')">1</button>
            <button class="button" onclick="appendToDisplay('2')">2</button>
            <button class="button" onclick="appendToDisplay('3')">3</button>
            <button class="button operator" onclick="appendToDisplay('-')">-</button>
            
            <button class="button" onclick="appendToDisplay('0')">0</button>
            <button class="button" onclick="appendToDisplay('.')">.</button>
            <button class="button equal" onclick="calculateResult()">=</button>
            <button class="button operator" onclick="appendToDisplay('+')">+</button>
            
            <button class="button clear" onclick="clearDisplay()">C</button>
        </div>
    </div>

    <script src="script.js"></script>
</body>
</html>

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Arial', sans-serif;
    background-color: #f0f2f5;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
}

.calculator {
    background-color: #fff;
    border-radius: 15px;
    box-shadow: 0 5px 20px rgba(0, 0, 0, 0.1);
    padding: 20px;
    width: 280px;
    text-align: center;
}

.display {
    width: 100%;
    height: 50px;
    text-align: right;
    font-size: 32px;
    padding: 10px;
    margin-bottom: 20px;
    border: 2px solid #ccc;
    border-radius: 10px;
    background-color: #f7f7f7;
    color: #333;
    font-weight: bold;
}

.buttons {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 10px;
}

.button {
    background-color: #4CAF50;
    color: white;
    font-size: 22px;
    padding: 20px;
    border: none;
    border-radius: 10px;
    cursor: pointer;
    transition: background-color 0.3s, transform 0.2s;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
}

.button:hover {
    background-color: #45a049;
    transform: scale(1.1);
}

.button:active {
    background-color: #388e3c;
}

.operator {
    background-color: #f57c00;
}

.operator:hover {
    background-color: #e65100;
}

.equal {
    background-color: #2196F3;
}

.equal:hover {
    background-color: #1976D2;
}

.clear {
    background-color: #f44336;
}

.clear:hover {
    background-color: #d32f2f;
}

function appendToDisplay(value) {
    document.getElementById("display").value += value;
}

function clearDisplay() {
    document.getElementById("display").value = '';
}

function calculateResult() {
    try {
        let display = document.getElementById("display");
        display.value = eval(display.value);
    } catch (e) {
        display.value = 'Error';
    }
}
