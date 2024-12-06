
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tigre Fortune</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #2c3e50;
      color: #ecf0f1;
      margin: 0;
      padding: 0;
    }

    h1 {
      margin-top: 20px;
    }

    .container {
      margin: 50px auto;
      width: 350px;
      padding: 20px;
      border: 2px solid #ecf0f1;
      border-radius: 10px;
      background-color: #34495e;
    }

    button {
      margin: 10px;
      padding: 15px 30px;
      font-size: 18px;
      color: #2c3e50;
      background-color: #ecf0f1;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }

    button:hover {
      background-color: #bdc3c7;
    }

    .result {
      margin-top: 20px;
      font-size: 24px;
      font-weight: bold;
    }

    .balance {
      font-size: 20px;
      margin-bottom: 20px;
    }
  </style>
</head>
<body>
  <h1>Tigre Fortune</h1>
  <div class="container">
    <div class="balance">Saldo: <span id="saldo">100</span> moedas</div>
    <p>Escolha sua aposta (10 moedas por rodada):</p>
    <button onclick="apostar('Tigre')">Tigre</button>
    <button onclick="apostar('Dragão')">Dragão</button>
    <button onclick="apostar('Empate')">Empate</button>
    <div class="result" id="resultado"></div>
  </div>

  <script>
    let saldo = 100; // Saldo inicial do jogador

    function apostar(aposta) {
      if (saldo < 10) {
        document.getElementById("resultado").innerText = "Saldo insuficiente! Recarregue suas moedas.";
        return;
      }

      // Deduz 10 moedas por rodada
      saldo -= 10;

      const opcoes = ['Tigre', 'Dragão', 'Empate'];
      const resultadoAleatorio = opcoes[Math.floor(Math.random() * opcoes.length)];

      let mensagem;
      if (aposta === resultadoAleatorio) {
        const ganho = aposta === 'Empate' ? 50 : 20; // Empate paga mais
        saldo += ganho;
        mensagem = `Resultado: ${resultadoAleatorio}. Você ganhou ${ganho} moedas!`;
      } else {
        mensagem = `Resultado: ${resultadoAleatorio}. Você perdeu!`;
      }

      // Atualiza o saldo e o resultado
      document.getElementById("saldo").innerText = saldo;
      document.getElementById("resultado").innerText = mensagem;
    }
  </script>
</body>
</html>
