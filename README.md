<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Página de Vendas</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>🔥 Emagreça Agora com o Método Natural 🔥</h1>
    <p>Perca peso de forma saudável e definitiva</p>
  </header>

  <section class="video">
    <iframe width="560" height="315"
      src="https://www.youtube.com/embed/V5_gS-TXkLw"
      title="Vídeo sobre emagrecimento"
      frameborder="0"
      allowfullscreen>
    </iframe>
  </section>

  <section class="oferta">
    <h2>Oferta por Tempo Limitado!</h2>
    <div id="contador"></div>
    <a href="https://linkdapagina.com" class="botao">Quero Emagrecer Agora</a>
  </section>

  <script src="script.js"></script>
</body>
</html>
body {
  font-family: Arial, sans-serif;
  text-align: center;
  margin: 0;
  padding: 0;
  background: #f8f9fa;
}

header {
  background: #ff4747;
  color: white;
  padding: 20px;
}

.video {
  margin: 20px;
}

.botao {
  display: inline-block;
  background: #28a745;
  color: white;
  padding: 15px 25px;
  border-radius: 8px;
  font-size: 20px;
  text-decoration: none;
  transition: 0.3s;
}

.botao:hover {
  background: #218838;
}

#contador {
  font-size: 24px;
  font-weight: bold;
  margin: 20px 0;
}// Contagem regressiva de 24h
const fim = new Date();
fim.setHours(fim.getHours() + 24);

function atualizarContador() {
  const agora = new Date().getTime();
  const distancia = fim - agora;

  const horas = Math.floor((distancia % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  const minutos = Math.floor((distancia % (1000 * 60 * 60)) / (1000 * 60));
  const segundos = Math.floor((distancia % (1000 * 60)) / 1000);

  document.getElementById("contador").innerHTML =
    horas + "h " + minutos + "m " + segundos + "s ";

  if (distancia < 0) {
    document.getElementById("contador").innerHTML = "Oferta Expirada!";
  }
}

setInterval(atualizarContador, 1000);
