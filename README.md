# Invitacion
Invitacion de boda
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación de Boda</title>
    <style>{
        background-image:url(Invitacion/Foto_sanpedro.jpeg);}
        
     </style>
</head>
<body>
    <h1>¡Nos Casamos!</h1>
    <p>Te invitamos a celebrar nuestra boda.</p>
    <image src="Foto_sanpedro.jpeg" />
    <div class="date">Fecha: 21 de Noviembre de 2026</div>
    <div class="date">Lugar: Jardin Paraiso, Tequequitengo</div>
    <p>Por favor, confirma tu asistencia:</p>
    <a href="#" class="button">Confirmar Asistencia</a>
   
</body>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Cuenta Regresiva para Nuestra Boda</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background-color: #f8f1f1;
      color: #000;
      margin: 0;
      padding: 0;
    }
    h1 {
      font-size: 2.5em;
      margin-top: 50px;
    }
    #countdown {
      font-size: 2em;
      margin: 20px 0;
    }
    .time {
      display: inline-block;
      margin: 10px;
      text-align: center;
    }
    .number {
      font-size: 3em;
      font-weight: bold;
      color: #000000;
    }
    .label {
      font-size: 1em;
    }
  </style>
</head>
<body>
  <h1>¡Nos casamos!</h1>
  <div id="countdown">
    <div class="time">
      <div class="number" id="days">0</div>
      <div class="label">Días</div>
    </div>
    <div class="time">
      <div class="number" id="hours">0</div>
      <div class="label">Horas</div>
    </div>
    <div class="time">
      <div class="number" id="minutes">0</div>
      <div class="label">Minutos</div>
    </div>
    <div class="time">
      <div class="number" id="seconds">0</div>
      <div class="label">Segundos</div>
    </div>
  </div>
  <script>
    const weddingDate = new Date("2026-11-21T16:00:00").getTime(); 
    function updateCountdown() {
      const now = new Date().getTime();
      const timeLeft = weddingDate - now;

      if (timeLeft > 0) {
        const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
        const hours = Math.floor((timeLeft % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((timeLeft % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((timeLeft % (1000 * 60)) / 1000);

        document.getElementById("days").innerText = days;
        document.getElementById("hours").innerText = hours;
        document.getElementById("minutes").innerText = minutes;
        document.getElementById("seconds").innerText = seconds;
      } else {
        document.getElementById("countdown").innerHTML = "<h2>¡Hoy es el gran día!</h2>";
      }
    }

    setInterval(updateCountdown, 1000);
  </script>
</body>
</html>

