<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>Interação com Foto do Mar</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #e6f2ff;
      text-align: center;
      padding: 50px;
    }
    #imagem-mar {
      display: none;
      max-width: 90%;
      margin-top: 20px;
      border-radius: 12px;
      box-shadow: 0 0 10px rgba(0,0,0,0.3);
    }
    input[type="text"] {
      padding: 10px;
      font-size: 16px;
      width: 60%;
    }
    button {
      padding: 10px 20px;
      font-size: 16px;
      margin-left: 10px;
      cursor: pointer;
    }
    #mensagem {
      margin-top: 30px;
      font-size: 18px;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>Faça uma pergunta</h1>
  <input type="text" id="pergunta" placeholder="Digite sua pergunta aqui">
  <button onclick="responderPergunta()">Perguntar</button>
  <div id="mensagem"></div>
  <img id="imagem-mar" src="mar3.jpg" alt="Foto do Mar">

  <script>
    function responderPergunta() {
      const pergunta = document.getElementById('pergunta').value.toLowerCase();
      const imagem = document.getElementById('imagem-mar');
      const mensagem = document.getElementById('mensagem');

      if (pergunta.includes("cade a foto do mar")) {
        imagem.style.display = 'block';
        mensagem.innerText = "Aqui está a foto do mar:";
      } else if (pergunta.includes("pedido de namoro")) {
        imagem.style.display = 'none';
        mensagem.innerText = "Foi ao entardecer, com o som das ondas e o céu dourado, que um pedido de namoro aconteceu à beira-mar.";
      } else {
        imagem.style.display = 'none';
        mensagem.innerText = "Não entendi sua pergunta. Tente perguntar novamente.";
      }
    }
  </script>
</body>
</html>
