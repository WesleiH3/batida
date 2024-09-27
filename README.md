# batida
uma estrutura de dados q se mexe conforme a batida da musica.
<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Batida de DJ</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      background-color: #121212;
      color: white;
    }
    h1 {
      margin-bottom: 20px;
    }
    .pad-container {
      display: grid;
      grid-template-columns: repeat(3, 100px);
      grid-gap: 20px;
    }
    .pad {
      width: 100px;
      height: 100px;
      background-color: #333;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 10px;
      cursor: pointer;
      transition: background-color 0.3s;
    }
    .pad:hover {
      background-color: #555;
    }
  </style>
</head>
<body>

  <h1>Batida de DJ</h1>
  <div class="pad-container">
    <div class="pad" id="kick">Kick</div>
    <div class="pad" id="snare">Snare</div>
    <div class="pad" id="hihat">Hi-hat</div>
  </div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/tone/14.8.34/Tone.min.js"></script>
  <script>
    // Carregar os sons usando Tone.js
    const kick = new Tone.Player("kick.mp3").toDestination();
    const snare = new Tone.Player("snare.mp3").toDestination();
    const hihat = new Tone.Player("hihat.mp3").toDestination();

    // Adicionar eventos de clique nos pads
    document.getElementById('kick').addEventListener('click', () => {
      kick.start();
    });

    document.getElementById('snare').addEventListener('click', () => {
      snare.start();
    });

    document.getElementById('hihat').addEventListener('click', () => {
      hihat.start();
    });
  </script>

</body>
</html>
