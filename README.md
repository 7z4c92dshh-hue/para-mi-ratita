<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
   <link rel="icon" type="image/png" href="1.JPG">
  <title>unclick+</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      background: #0049F7;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: "mi corazón";
      font-style: normal;
      color: #FFA6E7;
      cursor: pointer;
      padding: 20px;
    }

    .container {
      text-align: center;
      width: 100%;
      max-width: 500px;
      padding: 24px;
      border-radius: 20px;
      backdrop-filter: blur(10px);
    }

    img {
      width: 100%;
      max-height: 300px;
      object-fit: cover;
      border-radius: 16px;
      margin-bottom: 18px;
    }

    h1 {
      font-size: 1.4rem;
      line-height: 1.4;
      margin: 0;
    }

    p {
      margin-top: 10px;
      opacity: 0.6;
      font-size: 0.8rem;
    }
  </style>
</head>

<body onclick="changeVibe()">
  <div class="container">
  <img id="vibeImage" src="WhatsApp Image 2026-01-20 at 21.00.37 (3).jpeg" alt="vibe image" />
  <h1 id="phrase">FELIZ MES MI AMOR ❤️ </h1>
</div>


<script>
  const phrases = [
    "Soy la más feliz a tu lado,\n\n Aprendería todos los idiomas con tal de entendernos\nY amarnos toda la vida\nSomos amores Eternos,\nAmo nuestra confianza genuina",
    "Te amo mi niño precioso",
    "Feliz 20 mi cielito",
    "´Después de todo, qué gusto estar vivos, y juntos´",
    "Te quiero con la eternidad que concede la brevedad de un momento inolvidable.",
    "Sin duda amarte es lo que quiero hacer toda la vida",
    "Eres mi hilo rojo, el de todas mis vidas"
  ];

  const images = [
    "WhatsApp Image 2026-01-20 at 21.00.37 (3).jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.37 (2).jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.37 (1).jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.37.jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.36 (1).jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.36.jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.35 (3).jpeg",
    "WhatsApp Image 2026-01-20 at 21.00.35 (1).jpeg"

  ];

  const phraseEl = document.getElementById("phrase");
  const imageEl = document.getElementById("vibeImage");

  // ESTADO INICIAL ESTÁ MOSTRANDO EL TEXTO
  let showing = "text";
  imageEl.style.display = "none";

  function changeVibe() {
    if (showing === "text") {
      // ocultar el texto
      phraseEl.style.display = "none";

      // mostrar imagen
      imageEl.src = images[Math.floor(Math.random() * images.length)];
      imageEl.style.display = "block";

      showing = "image";
    } else {
      // ocultar imagen
      imageEl.style.display = "none";

      // mostrar texto
      phraseEl.textContent =
        phrases[Math.floor(Math.random() * phrases.length)];
      phraseEl.style.display = "block";

      showing = "text";
    }
  }
</script>

</body>
</html>
