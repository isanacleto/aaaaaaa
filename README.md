<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>aaaaaa</title>
    <style>
        #conteudo {
            background: #ff7a7a;
            width: 100%;
            height: 100%;
            position: fixed;
            top: 0;
            left: 0;
            padding: 10px;
            text-align: center;
            font-family: sans-serif;
        }

        .btn {
            background: black;
            color: white;
            border: none;
            padding: 10px;
            width: 80px;
            border-radius: 5px;
            margin: 5px;
        }

        .fixed {
            position: fixed;
        }

        .absolute {
            position: absolute;
        }
    </style>
</head>

<body>
    <div id="conteudo">
        <h2>Escolha uma opção :)</h2>
        <div style="margin: auto;width: 170px;">
            <button class="btn fixed" onclick="sim()">01 Recomendado</button>
            <button class="btn absolute" onclick="desvia(this)" onmouseover="desvia(this)">02 Não recomendado</button>
        </div>
    </div>

    <script>
        function sim() {
            alert("Você aceitou sair num encontro >>romântico<< comigo! :)");
            // redireciona para um URL após clicar no SIM
            location.href = "https://music.youtube.com/watch?v=izGwDsrQ1eQ";
        }

        function desvia(btn) {
            // btn declarado na função
            btn.style.bottom = geraPosicao(10, 90);
            btn.style.left = geraPosicao(10, 90);
            console.log('opa, desviei...');
        }

        function geraPosicao(min, max) {
            return (Math.random() * (max - min) + min) + "%";
        }
    </script>
</body>

</html>
