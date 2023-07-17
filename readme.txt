<!DOCTYPE html>
<html lang="pt=BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CALCULADORA</title>
    <style>
        *{margin: 0; padding: 0        }
        .fundo {background-image: linear-gradient(45deg, black, white);
        height: 100vh;
        color: aliceblue;
        font-family: Arial, Helvetica, sans-serif;
    text-align: center;
}
        .calculadora {
            position: absolute;
            background-color: black;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            border-radius: 15px;
            padding: 15px;
            opacity: 80%;
        }
        .botao {
            width: 50px;
            height: 50px;
            font-size: 25px;
            margin: 3px;
            cursor: pointer;
            background-color: darkgray;
            border: none;
            color: white;
        }
        .botao:hover{
            background-color: black;
        }
        #resultado {
            width: 207px;
            background-color: white;
            height: 30px;
            margin: 5px;
            font-size: 25px;
            color: black;
            text-align: right;
            padding: 5px;


        }

    </style>
</head>
<body>
    <DIv class="fundo">
        <h1>Calculo Danniel</h1>
        <div class="calculadora">
            <h1>Calculadora</h1>
            <p id="resultado"></p>
            <table>
                <tr>
                    <td><button class="botao" onclick="clean">C</button></td>
                    <td><button class="botao"><</button></td>
                    <td><button class="botao" onclick="insert('/')">/</button></td>
                    <td><button class="botao" onclick="insert('*')">X</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('7')">7</button></td>
                    <td><button class="botao" onclick="insert('8')">8</button></td>
                    <td><button class="botao" onclick="insert('9')">9</button></td>
                    <td><button class="botao" onclick="insert('-')">-</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('4')">4</button></td>
                    <td><button class="botao" onclick="insert('5')">5</button></td>
                    <td><button class="botao" onclick="insert('6')">6</button></td>
                    <td><button class="botao" onclick="insert('+')">+</button></td>
                </tr>
                <tr>
                    <td><button class="botao" onclick="insert('1')">1</button></td>
                    <td><button class="botao" onclick="insert('2')">2</button></td>
                    <td><button class="botao" onclick="insert('3')">3</button></td>
                    <td rowspan="2"><button class="botao" style="height: 106px;">=</button></td>
                </tr>
                <tr>
                    <td colspan="2"><button class="botao" style="width: 106px;">0</button></td>
                    <td><button class="botao">.</button></td>
                </tr>
            </table>
        </div>
    </DIv>
    <script>
        function insert(num) 
        {
            var numero = document.getElementById('resultado').innerHTML;
            document.getElementById('resultado').innerHTML = numero + num;
        }
        function clean() {
            document.getElementById('resultado').innerHTML = "";
        }
    </script>
</body>
</html>