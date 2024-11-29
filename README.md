<!DOCTYPE html>
<html lang="en">
  <head>
    <title>CALCULATOR</title>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width" />
    <link rel="stylesheet" href="calci.css" />
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjs/11.8.0/math.min.js"></script>
    <script>
        function calculate() {
            try{
                const input = calculator.display.value;
                const result = math.evaluate(input);
                calculator.display.value = result; 
            }catch(error){
                calculator.display.value = "Error";
            }
        }
    </script>
  </head>
  <body>
    <div class="container">
        <fieldset id="container">
            <form action="" name="calculator">
                <input id="display" type="text" name="display" readonly>
                <input class="button digits" type="button" value="7" onclick="calculator.display.value += '7'">
                <input class="button digits" type="button" value="8" onclick="calculator.display.value += '8'">
                <input class="button digits" type="button" value="9" onclick="calculator.display.value += '9'">
                <input class="button mathButtons" type="button" value="+" onclick="calculator.display.value += ' + '">
                <br>
                <input class="button digits" type="button" value="4" onclick="calculator.display.value += '4'">
                <input class="button digits" type="button" value="5" onclick="calculator.display.value += '5'">
                <input class="button digits" type="button" value="6" onclick="calculator.display.value += '6'">
                <input class="button mathButtons" type="button" value="-" onclick="calculator.display.value += ' - '">
                <br>
                <input class="button digits" type="button" value="1" onclick="calculator.display.value += '1'">
                <input class="button digits" type="button" value="2" onclick="calculator.display.value += '2'">
                <input class="button digits" type="button" value="3" onclick="calculator.display.value += '3'">
                <input class="button mathButtons" type="button" value="x" onclick="calculator.display.value += ' * '">
                <br>
                <input id="clearButton" class="button" type="button" value="C" onclick="calculator.display.value = ''">
                <input class="button digits" type="button" value="0" onclick="calculator.display.value += '0'">
                <input class="button mathButtons" type="button" value="=" onclick="calculate()">
                <input class="button mathButtons" type="button" value="/" onclick="calculator.display.value += ' / '" >

            </form>
        </fieldset>
    </div>
  </body>
</html>
