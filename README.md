no disponible 

<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Botón Copiar Texto</title>
  <style>
    body {
      background: #111;
      font-family: sans-serif;
      display: flex;
      height: 100vh;
      align-items: center;
      justify-content: center;
    }

    .copy-box {
      background: #222;
      border: 1px solid #333;
      padding: 20px;
      border-radius: 10px;
      color: #fff;
      width: 300px;
      text-align: center;
      position: relative;
    }

    #textoCopiar {
      user-select: all;
      background: #1a1a1a;
      padding: 10px;
      border-radius: 6px;
      margin-bottom: 10px;
      font-size: 14px;
      color: #0f0;
    }

    .copiar-btn {
      background-color: #00ff99;
      border: none;
      padding: 10px 20px;
      color: #000;
      font-weight: bold;
      border-radius: 8px;
      cursor: pointer;
      transition: 0.3s;
    }

    .copiar-btn:hover {
      background-color: #00cc7a;
    }
  </style>
</head>
<body>

  <div class="copy-box">
    <div id="textoCopiar">Este es el texto que puedes copiar</div>
    <button class="copiar-btn" onclick="copiarTexto()">📋 Copiar Texto</button>
  </div>

  <script>
    function copiarTexto() {
      const texto = document.getElementById('textoCopiar').innerText;
      navigator.clipboard.writeText(texto).then(() => {
        alert('✅ Texto copiado al portapapeles');
      });
    }
  </script>

</body>
</html>