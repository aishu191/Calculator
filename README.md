<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Simple Calculator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f0f0f0;
    }
    .calculator {
      width: 300px;
      margin: 50px auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 5px;
      background-color: #fff;
      box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
    }
    .calculator input[type="button"] {
      width: 60px;
      height: 60px;
      margin: 5px;
      font-size: 18px;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      transition: all 0.2s ease;
    }
    .calculator input[type="button"]:hover {
      background-color: #f0f0f0;
    }
    .calculator input[type="text"] {
      width: 100%;
      margin-bottom: 10px;
      padding: 10px;
      font-size: 24px;
      text-align: right;
      border: none;
      border-radius: 5px;
      box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.1);
    }
  </style>
</head>
<body>

<div class="calculator">
  <input type="text" id="display" readonly>
  <input type="button" value="7" onclick="addToDisplay('7')">
  <input type="button" value="8" onclick="addToDisplay('8')">
  <input type="button" value="9" onclick="addToDisplay('9')">
  <input type="button" value="/" onclick="addToDisplay('/')">
  <br>
  <input type="button" value="4" onclick="addToDisplay('4')">
  <input type="button" value="5" onclick="addToDisplay('5')">
  <input type="button" value="6" onclick="addToDisplay('6')">
  <input type="button" value="*" onclick="addToDisplay('*')">
  <br>
  <input type="button" value="1" onclick="addToDisplay('1')">
  <input type="button" value="2" onclick="addToDisplay('2')">
  <input type="button" value="3" onclick="addToDisplay('3')">
  <input type="button" value="-" onclick="addToDisplay('-')">
  <br>
  <input type="button" value="0" onclick="addToDisplay('0')">
  <input type="button" value="." onclick="addToDisplay('.')">
  <input type="button" value="=" onclick="calculate()">
  <input type="button" value="+" onclick="addToDisplay('+')">
  <br>
  <input type="button" value="C" onclick="clearDisplay()">
</div>

<script>
  function addToDisplay(value) {
    document.getElementById('display').value += value;
  }

  function calculate() {
    try {
      document.getElementById('display').value = eval(document.getElementById('display').value);
    } catch (e) {
      document.getElementById('display').value = 'Error';
    }
  }

  function clearDisplay() {
    document.getElementById('display').value = '';
  }
</script>

</body>
</html>
