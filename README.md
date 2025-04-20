<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Tienda de Belleza</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background-color: #fff5f8;
      padding: 20px;
    }

    header {
      text-align: center;
      padding: 20px 0;
      background-color: #ffccda;
      margin-bottom: 20px;
    }

    header h1 {
      color: #5c2a4a;
    }

    .share-button {
      text-align: center;
      margin-bottom: 30px;
    }

    .share-button button {
      background-color: #cc3366;
      color: white;
      border: none;
      padding: 10px 20px;
      border-radius: 8px;
      cursor: pointer;
    }

    .share-button p {
      color: green;
      display: none;
      margin-top: 10px;
    }

    .seccion {
      margin-bottom: 40px;
    }

    .seccion h2 {
      margin-bottom: 20px;
      color: #cc3366;
    }

    .cards-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    @media (max-width: 768px) {
      .cards-container {
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      }
    }

    .card {
      background-color: white;
      border-radius: 12px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      padding: 20px;
      transition: transform 0.3s;
      text-align: center;
    }

    .card:hover {
      transform: translateY(-5px);
    }

    .card img {
      max-width: 100%;
      height: 150px;
      object-fit: cover;
      border-radius: 8px;
      margin-bottom: 15px;
    }

    .card h3 {
      margin-bottom: 10px;
      color: #d6336c;
    }

    .card p {
      color: #555;
    }
  </style>
</head>
<body>
  <header>
    <h1>Tienda de Belleza</h1>
  </header>

  <div class="share-button">
    <button onclick="compartirPagina()">Compartir esta página</button>
    <p id="mensaje-copiado">¡Enlace copiado al portapapeles!</p>
  </div>

  <script>
    function compartirPagina() {
      const url = window.location.href;
      navigator.clipboard.writeText(url).then(() => {
        const mensaje = document.getElementById("mensaje-copiado");
        mensaje.style.display = "block";
        setTimeout(() => {
          mensaje.style.display = "none";
        }, 2000);
      });
    }
  </script>

  <section class="seccion">
    <h2>Maquillaje</h2>
    <div class="cards-container">
      <div class="card">
        <img src="" alt="Base Líquida">
        <h3>Base Líquida</h3>
        <p>Cobertura natural para unificar el tono de tu piel.</p>
      </div>
      <div class="card">
        <img src="" alt="Polvo Compacto">
        <h3>Polvo Compacto</h3>
        <p>Acabado mate para fijar tu maquillaje durante horas.</p>
      </div>
      <div class="card">
        <img src="" alt="Paleta de Sombras">
        <h3>Paleta de Sombras</h3>
        <p>Colores intensos para crear looks espectaculares.</p>
      </div>
      <div class="card">
        <img src="" alt="Labial Mate">
        <h3>Labial Mate</h3>
        <p>Color duradero con acabado aterciopelado.</p>
      </div>
      <div class="card">
        <img src="" alt="Rubor Líquido">
        <h3>Rubor Líquido</h3>
        <p>Fácil de difuminar para un efecto natural.</p>
      </div>
      <div class="card">
        <img src="" alt="Rubor Compacto">
        <h3>Rubor Compacto</h3>
        <p>Textura suave y colores radiantes para tus mejillas.</p>
      </div>
    </div>
  </section>
