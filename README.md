<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Página de Vendas - Emagrecimento</title>
  <style>
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
      padding: 30px 20px;
    }

    header h1 {
      font-size: 28px;
      margin-bottom: 10px;
    }

    header p {
      font-size: 18px;
    }

    .video {
      margin: 20px auto;
    }

    iframe {
      width: 90%;
      max-width: 560px;
      height: 315px;
      border-radius: 10px;
    }

    .oferta {
      background: #fff3cd;
      padding: 30px;
      margin: 20px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }

    .oferta h2 {
      font-size: 24px;
      color: #856404;
    }

    #contador {
      font-size: 26px;
      font-weight: bold;
      margin: 20px 0;
      color: #dc3545;
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

    footer {
      margin-top: 40px;
      padding: 20px;
      background: #343a40;
      color: white;
    }
  </style>
</head>
<body>
  <header>
    <h1>🔥 Emagreça Agora com o Método Natural 🔥</h1>
    <p>Perca peso de forma saudável e definitiva!</p>
  </header>

  <section class="video">
    <iframe src="https://www.youtube.com/embed/V5_gS-TXkLw" 
      title="Vídeo sobre emagrecimento" 
      frameborder="0" 
      allowfullscreen>
    </iframe>
  </section>

  <section class="oferta">
    <h2>⚡ Oferta por Tempo Limitado ⚡</h2>
    <div id="contador"></div>
    <a href="https://linkdapagina.com" class="botao">Quero Emagrecer Agora</a>
  </section>

  <footer>
    <p>© 2025 - Sua Marca | Todos os direitos reservados</p>
  </footer>

  <script>
    // Contagem regressiva de 24h
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
  </script>
</body>
</html>