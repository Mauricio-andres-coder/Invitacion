<DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación de Boda</title>
    <style>
        body {
            background-image: url('Foto_sanpedro.jpeg'); /* Ruta corregida */
            background-size: cover; /* Asegura que la imagen cubra toda la pantalla */
            background-position: center; /* Centra la imagen */
            background-repeat: no-repeat; /* Evita repeticiones */
            height: 100vh; /* Altura completa de la ventana */
            margin: 0; /* Elimina márgenes */
        }
        h1 {
            color: green;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7); /* Sombra para destacar texto */
        }
        p, .date, a {
            color: white;
        }
        a.button {
            display: inline-block;
            background-color: #FF69B4;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <h1>¡Nos Casamos!</h1>
    <p>Te invitamos a celebrar nuestra boda.</p>
    <div class="date">Fecha: 21 de Noviembre de 2026</div>
    <div class="date">Lugar: Jardín Paraíso, Tequequitengo</div>
    <p>Por favor, confirma tu asistencia:</p>
    <a href="#" class="button">Confirmar Asistencia</a>
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
                const hours = Math.floor((timeLeft % (1000 * 60 * 60 )) / (1000 * 60 * 60));
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
