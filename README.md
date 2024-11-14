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
