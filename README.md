<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora Web</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 50px; }
        .calculator { width: 300px; margin: auto; padding: 20px; border: 1px solid #ccc; border-radius: 10px; background: #f3f3f3; }
        #display { width: 100%; font-size: 2em; margin-bottom: 10px; text-align: right; padding: 5px; }
        .buttons button { width: 23%; padding: 15px; font-size: 1.5em; margin: 5px; cursor: pointer; }
        .buttons button:hover { background: #ddd; }
    </style>
</head>
<body>
    <div class="calculator">
        <input id="display" type="text" readonly>
        <div class="buttons">
            <button onclick="clearDisplay()">C</button>
            <button onclick="appendValue('/')">/</button>
            <button onclick="appendValue('*')">*</button>
            <button onclick="appendValue('-')">-</button>
            <button onclick="appendValue('7')">7</button>
            <button onclick="appendValue('8')">8</button>
            <button onclick="appendValue('9')">9</button>
            <button onclick="appendValue('+')">+</button>
            <button onclick="appendValue('4')">4</button>
            <button onclick="appendValue('5')">5</button>
            <button onclick="appendValue('6')">6</button>
            <button onclick="calculateResult()">=</button>
            <button onclick="appendValue('1')">1</button>
            <button onclick="appendValue('2')">2</button>
            <button onclick="appendValue('3')">3</button>
            <button onclick="appendValue('0')">0</button>
        </div>
    </div>
    <script>
        function appendValue(value) { document.getElementById('display').value += value; }
        function clearDisplay() { document.getElementById('display').value = ''; }
        function calculateResult() { 
            try { document.getElementById('display').value = eval(document.getElementById('display').value); } 
            catch (e) { document.getElementById('display').value = 'Erro'; } 
        }
    </script>
</body>
</html>

