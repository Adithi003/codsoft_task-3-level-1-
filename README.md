# codsoft_task-3-level-1-
Calculator code and output task 3 (level 1)
<!DOCTYPE html>
<html>
<head>
  <title>Calculator</title>
  <style>
    .calculator {
      width: 300px;
      margin: 0 auto;
      border: 1px solid #ccc;
      padding: 10px;
      text-align: center;
    }

    .calculator input {
      width: 60px;
      margin-bottom: 5px;
      margin-right: 5px;
    }
  </style>
</head>
<body>
  <div class="calculator">
    <input type="text" id="result" readonly>
    <br>
    <input type="button" value="1" onclick="appendToResult('1')">
    <input type="button" value="2" onclick="appendToResult('2')">
    <input type="button" value="3" onclick="appendToResult('3')">
    <input type="button" value="+" onclick="appendToResult('+')">
    <br>
    <input type="button" value="4" onclick="appendToResult('4')">
    <input type="button" value="5" onclick="appendToResult('5')">
    <input type="button" value="6" onclick="appendToResult('6')">
    <input type="button" value="-" onclick="appendToResult('-')">
    <br>
    <input type="button" value="7" onclick="appendToResult('7')">
    <input type="button" value="8" onclick="appendToResult('8')">
    <input type="button" value="9" onclick="appendToResult('9')">
    <input type="button" value="*" onclick="appendToResult('*')">
    <br>
    <input type="button" value="0" onclick="appendToResult('0')">
    <input type="button" value="/" onclick="appendToResult('/')">
    <input type="button" value="=" onclick="calculateResult()">
    <input type="button" value="Clear" onclick="clearResult()">
  </div>

  <script>
    function appendToResult(value) {
      document.getElementById("result").value += value;
    }

    function calculateResult() {
      var result = document.getElementById("result").value;
      var answer = eval(result);
      document.getElementById("result").value = answer;
    }

    function clearResult() {
      document.getElementById("result").value = "";
    }
  </script>
</body>
</html>
