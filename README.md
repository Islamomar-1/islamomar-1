<html>
  <head>
    <title>Calculator</title>
    <style>
      /* Add some styling for the calculator */
      .calculator {
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 20px;
      }

      .display {
        background-color: lightgray;
        width: 300px;
        height: 50px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding: 0 10px;
        font-size: 20px;
        border-radius: 10px;
        margin-bottom: 20px;
      }

      .buttons {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-gap: 10px;
      }

      .btn {
        background-color: white;
        border: 1px solid gray;
        width: 100%;
        height: 50px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 20px;
        cursor: pointer;
        border-radius: 10px;
      }
    </style>
  </head>
  <body>
    <div class="calculator">
      <div class="display" id="display"></div>
      <div class="buttons">
        <div class="btn" onclick="appendDisplay('7')">7</div>
        <div class="btn" onclick="appendDisplay('8')">8</div>
        <div class="btn" onclick="appendDisplay('9')">9</div>
        <div class="btn" onclick="performOperation('/')">&divide;</div>
        <div class="btn" onclick="appendDisplay('4')">4</div>
        <div class="btn" onclick="appendDisplay('5')">5</div>
        <div class="btn" onclick="appendDisplay('6')">6</div>
        <div class="btn" onclick="performOperation('*')">&times;</div>
        <div class="btn" onclick="appendDisplay('1')">1</div>
        <div class="btn" onclick="appendDisplay('2')">2</div>
        <div class="btn" onclick="appendDisplay('3')">3</div>
        <div class="btn" onclick="performOperation('-')">-</div>
        <div class="btn" onclick="appendDisplay('0')">0</div>
        <div class="btn" onclick="appendDisplay('.')">.</div>
        <div class="btn" onclick="performOperation('=')">=</div>
        <div class="btn" onclick="performOperation('+')">+</div>
      </div>
    </div>
    
    <script>
      let displayValue = "0";
      let firstValue = null;
      let operator = null;
      let waitingForSecondValue = false;
      
      const display = document.querySelector("
