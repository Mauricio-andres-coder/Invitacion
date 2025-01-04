<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Invitación Boda Civil</title>
    <style>
        body {
            background-image: url('Foto_Sanpedro2.jpeg');
            background-size: cover; /* Asegura que la imagen cubra toda la pantalla */
            background-position: center; /* Centra la imagen */
            background-repeat: no-repeat; /* Evita repeticiones */
            height: 100vh; /* Altura completa de la ventana */
            margin: 0; /* Elimina márgenes */
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            color: white;
        }
        h2 {
            color: white;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.7); /* Sombra para destacar texto */
            display: flex;
            align-items: center;
        }
        h2 i {
            margin-left: 10px; /* Espacio entre el texto y el ícono del corazón */
        }
        p, .date, a {
            color: white;
        }
        a.button {
            display: inline-block;
            background-color: #33FFB2;
            color: white;
            padding: 10px 20px;
            text-decoration: none;
            border-radius: 5px;
            font-weight: bold;
        }
        #countdown {
            margin-left: 20px; /* Espacio entre el texto y el contador */
            color: #FF5733; /* Cambia el color del texto del contador */
        }
        #countdown .number {
            font-size: 2em; /* Tamaño de los números */
            font-weight: bold; /* Números en negrita */
            color: #FFD700; /* Color de los números */
        }
        #countdown .label {
            font-size: 1em; /* Tamaño de las etiquetas */
            color: #FFD700; /* Color de las etiquetas */
        }
    </style>
</head>
<body>
    <h2>¡Nos Casamos! <i class="fa-solid fa-heart"></i></h2>
    <p>Te invitamos a celebrar nuestra boda civil.</p>
    <div class="date">Fecha: 10 de Enero de 2025</div>
    <div class="date">Lugar: Juzgado 8 del Registro Civil</div>

    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <a href="https://www.google.com/maps/place/Juzgado+civil+8/@19.4114809,-99.1611409,17z/data=!3m1!4b1!4m6!3m5!1s0x85d1ff3cfd8b33f1:0x809ea7dac69472e4!8m2!3d19.4114759!4d-99.158566!16s%2Fg%2F1thsg85_?hl=es&entry=ttu&g_ep=EgoyMDI0MTIxMS4wIKXMDSoASAFQAw%3D%3D/"> 
        <i class="fa-solid fa-location-dot"></i> Como Llegar a la Ceremonia
    </a>

    <div id="countdown">
        <div class="time">
            <div class="number" id="days">0</div>
            <div class="label">Días</div>
        </div>
    </div>

    <script>
        const weddingDate = new Date("2025-01-10T12:00:00").getTime(); 
        function updateCountdown() {
            const now = new Date().getTime();
            const timeLeft = weddingDate - now;

            if (timeLeft > 0) {
                const days = Math.floor(timeLeft / (1000 * 60 * 60 * 24));
                document.getElementById("days").innerText = days;
            } else {
                document.getElementById("countdown").innerHTML = "<h2>¡Hoy es el gran día!</h2>";
            }
        }

        setInterval(updateCountdown, 1000);
    </script>
</body>
</html>


