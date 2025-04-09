<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Аудио NFC Плеер</title>
  </head>
  <body style="text-align: center; padding-top: 50px; font-family: sans-serif">
    <h1>Воспроизведение аудио</h1>
    <audio id="player" autoplay controls>
      <source
        src="https://drive.google.com/uc?export=download&id=1W2ZGcrbmjQFfHZo97O6Rcut1j65nguKr"
        type="audio/mpeg"
      />
      Ваш браузер не поддерживает элемент audio.
    </audio>

    <script>
      // Попытка принудительно запустить аудио (на случай блокировок)
      window.onload = () => {
        const audio = document.getElementById("player");
        audio.play().catch((err) => {
          console.log("Автоплей заблокирован:", err);
        });
      };
    </script>
  </body>
</html>
