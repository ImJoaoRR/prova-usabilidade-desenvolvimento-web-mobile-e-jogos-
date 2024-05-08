<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Calculadora de Média de Alunos</title>
</head>
<body>
    <h1>Calculadora de Média de Alunos</h1>
    <div>
        <label for="nome">Nome do Aluno:</label>
        <input type="text" id="nome">
    </div>
    <div>
        <label for="nota1">Nota 1:</label>
        <input type="number" id="nota1" step="0.1">
    </div>
    <div>
        <label for="nota2">Nota 2:</label>
        <input type="number" id="nota2" step="0.1">
    </div>
    <div>
        <label for="nota3">Nota 3:</label>
        <input type="number" id="nota3" step="0.1">
    </div>
    <div>
        <label for="nota4">Nota 4:</label>
        <input type="number" id="nota4" step="0.1">
    </div>
    <button onclick="calcularMedia()">Calcular Média</button>
    <div id="resultado"></div>

    <script>
        function calcularMedia() {
            var nome = document.getElementById("nome").value;
            var nota1 = parseFloat(document.getElementById("nota1").value);
            var nota2 = parseFloat(document.getElementById("nota2").value);
            var nota3 = parseFloat(document.getElementById("nota3").value);
            var nota4 = parseFloat(document.getElementById("nota4").value);

            var media = (nota1 + nota2 + nota3 + nota4) / 4;

            var resultado = document.getElementById("resultado");
            resultado.innerHTML = "Aluno: " + nome + "<br>" +
                                   "Notas: " + nota1 + ", " + nota2 + ", " + nota3 + ", " + nota4 + "<br>" +
                                   "Média: " + media.toFixed(2);
        }
    </script>
</body>
</html>
