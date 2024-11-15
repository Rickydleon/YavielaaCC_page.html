<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Un Viaje de Momentos Especiales</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f0f0f0;
            color: #333;
            margin: 0;
            padding: 0;
            text-align: center;
        }
        h1 {
            color: #333;
            margin-top: 20px;
            font-size: 28px;
        }
        h2 {
            color: #e60073;
            font-size: 36px;
            margin-top: 10px;
        }
        p {
            width: 80%;
            margin: 0 auto;
            font-size: 18px;
            line-height: 1.6;
        }
        .question {
            font-size: 24px;
            color: #4a4a4a;
            margin-top: 30px;
        }
        .instructions {
            font-size: 14px;
            color: #777;
            margin-top: 10px;
        }
        .buttons {
            margin-top: 20px;
        }
        .buttons button {
            background-color: #333;
            color: white;
            border: none;
            padding: 10px 20px;
            font-size: 18px;
            border-radius: 5px;
            cursor: pointer;
            margin: 10px;
        }
        .buttons button:hover {
            background-color: #555;
        }
    </style>
    <script>
        function showMemory1() {
            document.getElementById("initialText").style.display = "none";
            document.getElementById("memory1").style.display = "block";
        }

        function showQuestion1() {
            document.getElementById("memory1").style.display = "none";
            document.getElementById("question1").style.display = "block";
        }

        function showQuestion2() {
            document.getElementById("question1").style.display = "none";
            document.getElementById("question2").style.display = "block";
        }

        function showLoveMessage() {
            document.getElementById("question2").style.display = "none";
            document.getElementById("loveMessage").style.display = "block";
        }

        function showNextStep() {
            document.getElementById("loveMessage").style.display = "none";
            document.getElementById("nextStep").style.display = "block";
        }

        function revealFinalQuestion() {
            document.getElementById("nextStep").style.display = "none";
            document.getElementById("finalQuestion").style.display = "block";
        }

        function positiveResponse() {
            alert('Que feliz me haces al saber que si quieres, así tanto como yo.');
        }

        function extraLoveResponse() {
            alert('¡Esa respuesta me encanta! 💖 Cada día estoy más feliz de tenerte en mi vida.');
        }

        function playfulResponse() {
            alert('Esa es una respuesta con truco… pero me gusta cómo suena 😉');
        }

        function excitedResponse() {
            alert('Sabía que sentías lo mismo. ¡Estoy muy emocionado! 😊');
        }
    </script>
</head>
<body>
    <h2>Yaviela, mi vida</h2>
    <h1>Quiero que me prestes atención...</h1>
    <p id="initialText">Te preparé algo especial. Toca "Comenzar" cuando estés lista para empezar nuestro viaje y recuerda que debes tocar "Siguiente" para avanzar en cada paso.</p>
    
    <button onclick="showMemory1()" style="background-color: #4a90e2; color: white; padding: 10px 25px; border: none; font-size: 18px; border-radius: 5px; cursor: pointer; margin-top: 20px;">
        Comenzar
    </button>

    <div id="memory1" style="display: none;">
        <p class="question">📅 7 de noviembre</p>
        <p>Esa fue la fecha de nuestro primer beso. Ese momento fue increíble, y desde entonces, no dejo de pensar en ti. Tocaste algo en mí que nunca había sentido antes.</p>
        <button onclick="showQuestion1()">Siguiente</button>
        <p class="instructions">Toca "Siguiente" para continuar.</p>
    </div>

    <div id="question1" style="display: none;">
        <p class="question">📍 La Distancia</p>
        <p>Aunque estemos lejos ahora, siento que cada día nos acercamos más. Te extraño tanto que cada mensaje, cada llamada se siente como una pequeña reunión entre nosotros.</p>
        <button onclick="showQuestion2()">Siguiente</button>
        <p class="instructions">Toca "Siguiente" para continuar.</p>
    </div>

    <div id="question2" style="display: none;">
        <p class="question">💖 Lo mucho que te quiero</p>
        <p>No tengo palabras para describir lo que siento por ti. Solo sé que quiero una vida contigo, compartiendo momentos únicos y especiales. Eres la persona que quiero en mi vida para siempre.</p>
        <button onclick="showLoveMessage()">Siguiente</button>
        <p class="instructions">Toca "Siguiente" para continuar.</p>
    </div>

    <div id="loveMessage" style="display: none;">
        <p class="question">Luego de leer todo esto...</p>
        <p>Después de leer todo lo que siento y recordar estos momentos, quiero hacerte una pregunta importante.</p>
        <button onclick="showNextStep()">Siguiente</button>
        <p class="instructions">Toca "Siguiente" para ver la pregunta final.</p>
    </div>

    <div id="nextStep" style="display: none;">
        <p class="question">¿Quieres ser mi novia?</p>
        <p>Responde con sinceridad y sin presiones… pero quiero saber si te gustaría dar este paso conmigo.</p>
        <div class="buttons">
            <button onclick="positiveResponse()">Sí, claro que sí</button>
            <button onclick="extraLoveResponse()">No estaba segura, pero ahora… ¡Sí!</button>
            <button onclick="playfulResponse()">¿Por qué no? ¡Me encantan los riesgos! 😜</button>
            <button onclick="positiveResponse()">Depende… ¿Vas a invitarme a cenar primero? 😆</button>
            <button onclick="positiveResponse()">Solo como amigos, pero con cariño</button>
        </div>
        <p class="instructions">Selecciona una respuesta para completar tu viaje.</p>
    </div>
</body>
</html>
