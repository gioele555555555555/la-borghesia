# la-borghesia
sito di un ristorante
<!DOCTYPE html>
<html lang="it">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Borghesia</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&display=swap" rel="stylesheet">
    <style>
        /* Reset di base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background-color: #000000;
            font-family: 'Courier New', Courier, monospace;
            text-align: center;
            padding: 50px;
            overflow-x: hidden;
        }

        h1 {
            font-size: 80px;
            font-family: 'Playfair Display', serif;
            color: #095406;
            text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
            margin-bottom: 40px;
        }

        h2 {
            font-size: 40px;
            font-family: 'Playfair Display', serif;
            color: #2c3e50;
            margin-top: 50px;
        }

        .container {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-top: 50px;
            animation: fadeIn 1s ease-out;
        }

        /* Ridurre la dimensione delle immagini */
        .image {
            width: 10%;  /* Ridurre la dimensione della larghezza delle immagini */
            max-width: 300px;  /* Impostare una larghezza massima per evitare immagini troppo grandi */
            height: auto;
            border-radius: 20px;
            box-shadow: 5px 5px 15px rgba(0, 0, 0, 0.2);
            position: absolute;
            transition: transform 0.5s ease, box-shadow 0.5s ease;  /* Aggiungi transizione per l'effetto hover */
        }

        .image1 {
            top: -180px;
            left: 100px;
            transform: scale(2.5);
        }

        .image2 {
            top: -180px;
            right: 70px;
            transform: scale(2.5);
        }


        /* Stile per i bottoni */
        .buttons-container {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 40px;
            flex-wrap: wrap;
        }

        .button {
            padding: 15px 30px;
            background-color: #095406;
            color: white;
            border: none;
            border-radius: 25px;
            font-size: 20px;
            cursor: pointer;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }

        .button:hover {
            background-color: #34495e;
            transform: scale(1.1);
        }

        .button:active {
            background-color: #1a252f;
        }

        /* Sezione descrizione */
        .about-section {
            background-color: #fff;
            padding: 60px 20px;
            color: #2c3e50;
            border-radius: 20px;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
            margin-top: 50px;
            animation: fadeIn 2s ease-out;
        }

        .about-section p {
            font-size: 18px;
            line-height: 1.6;
            margin-bottom: 20px;
        }

        .gallary-section {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 50px;
            flex-wrap: wrap;
        }

        .gallary-image {
            width: 80%;
            max-width: 320px;
            height: auto;
            border-radius: 10px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
            object-fit: cover;
        }

        /* Media Queries per dispositivi mobili */
        @media (max-width: 1024px) { /* Tablet */
            h1 {
                font-size: 60px;
            }

            h2 {
                font-size: 35px;
            }

            .container {
                flex-direction: column;
                margin-top: 20px;
            }

            .image1,
            .image2 {
                top: initial;
                left: initial;
                right: initial;
                transform: scale(1);
            }

            .buttons-container {
                flex-direction: column;
                gap: 15px;
            }

            .gallary-image {
                max-width: 100%;
            }
        }

        @media (max-width: 768px) { /* Tablet e Mobile */
            h1 {
                font-size: 50px;
            }

            h2 {
                font-size: 30px;
            }

            .container {
                flex-direction: column;
                margin-top: 20px;
            }

            .image1,
            .image2 {
                top: initial;
                left: initial;
                right: initial;
                transform: scale(1);
            }

            .buttons-container {
                flex-direction: column;
                gap: 15px;
            }

            .gallary-image {
                max-width: 100%;
            }
        }

        @media (max-width: 480px) { /* Mobile */
            h1 {
                font-size: 35px;
            }

            h2 {
                font-size: 24px;
            }

            .button {
                font-size: 16px;
                padding: 12px 20px;
            }

            .image1, .image2 {
                max-width: 100%;
                transform: scale(1);
            }
        }

        /* Media Queries per desktop */
        @media (min-width: 1200px) {
            h1 {
                font-size: 90px;
            }

            h2 {
                font-size: 45px;
            }

            .container {
                flex-direction: row;
            }

            .image1, .image2 {
                transform: scale(2.5);
            }

            .buttons-container {
                justify-content: space-around;
            }
        }

        /* Media Queries per schermi molto grandi */
        @media (min-width: 1600px) {
            h1 {
                font-size: 100px;
            }

            .button {
                padding: 20px 40px;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="logo">
            <a href="https://imgbb.com/"><img src="https://i.ibb.co/S7fh11jz/logo.png" alt="logo" border="0"></a>
        </div>
        <!-- Bottone per la traduzione -->
        <button id="translateBtn" class="button" style="position: absolute; top: 20px; right: 20px;">Translate</button>
    </header>

    <h1 id="title">La Borghesia</h1>
    <div class="container">
        <a href="https://ibb.co/b54sK4hN">
            <img class="image image1" src="https://i.ibb.co/Kxt2rtZV/ristorante.jpg" alt="Vista interna del ristorante La Borghesia con un ambiente elegante" border="0">
        </a>
        <a href="https://ibb.co/svXv4Svb">
            <img class="image image2" src="https://i.ibb.co/ynxnCTnd/castello2.png" alt="Vista esterna del castello che ospita La Borghesia" border="0">
        </a>
    </div>

    <!-- Sezione bottoni -->
    <div class="buttons-container">
        <a href="file:///C:/Users/Notebook/Desktop/menu%20(2).html" target="_blank">
            <button class="button" id="menuBtn">Menu</button>
        </a>
        <a href="storia.html" target="_blank">
            <button class="button" id="historyBtn">Storia</button>
        </a>
        <a href="chisiamo.html" target="_blank">
            <button class="button" id="aboutBtn">Chi Siamo</button>
        </a>
    </div>

    <!-- Sezione descrizione -->
    <section class="about-section">
        <h2 id="sectionTitle"><font color="green">La Borghesia</font></h2>
        <p id="description">
            La Borghesia è un luogo dove la tradizione e l'eleganza si incontrano per offrire un'esperienza unica.
            Vi invitiamo a scoprire i sapori autentici della nostra cucina raffinata, preparata con ingredienti freschi e di alta qualità.
            Lasciatevi conquistare dall'atmosfera esclusiva e dai piatti prelibati che raccontano la nostra passione per la gastronomia.
        </p>
    </section>

    <!-- Galleria Immagini -->
    <section class="gallary-section">
        <a href="https://ibb.co/ZRK74wDw">
            <img class="gallary-image" src="https://i.ibb.co/0pZv4WbW/interni.jpg" alt="foto interni" border="0">
        </a>
        <a href="https://ibb.co/Z1tZzNPM">
            <img class="gallary-image" src="https://i.ibb.co/S7WLwJ83/esterni.jpg" alt="foto esterni" border="0">
        </a>
        <a href="https://ibb.co/YTWdg4Y3">
            <img class="gallary-image" src="https://i.ibb.co/n801pqZb/lago.jpg" alt="foto lago" border="0">
        </a>
    </section>

    <script>
        // Funzione per tradurre il contenuto in inglese
        const translateBtn = document.getElementById('translateBtn');

        translateBtn.addEventListener('click', function() {
            let isEnglish = document.documentElement.lang === "en";

            if (isEnglish) {
                // Ripristina alla lingua italiana
                document.documentElement.lang = "it";
                document.getElementById("title").innerText = "La Borghesia";
                document.getElementById("sectionTitle").innerHTML = "<font color='green'>La Borghesia</font>";
                document.getElementById("description").innerHTML =
                    "La Borghesia è un luogo dove la tradizione e l'eleganza si incontrano per offrire un'esperienza unica. Vi invitiamo a scoprire i sapori autentici della nostra cucina raffinata, preparata con ingredienti freschi e di alta qualità. Lasciatevi conquistare dall'atmosfera esclusiva e dai piatti prelibati che raccontano la nostra passione per la gastronomia.";
                document.getElementById("menuBtn").innerText = "Menu";
                document.getElementById("historyBtn").innerText = "Storia";
                document.getElementById("aboutBtn").innerText = "Chi Siamo";
                translateBtn.innerText = "Translate";
            } else {
                // Traduci in inglese
                document.documentElement.lang = "en";
                document.getElementById("title").innerText = "La Borghesia";
                document.getElementById("sectionTitle").innerHTML = "<font color='green'>La Borghesia</font>";
                document.getElementById("description").innerHTML =
                    "La Borghesia is a place where tradition and elegance meet to offer a unique experience. We invite you to discover the authentic flavors of our refined cuisine, prepared with fresh, high-quality ingredients. Let yourself be captivated by the exclusive atmosphere and the delicious dishes that tell the story of our passion for gastronomy.";
                document.getElementById("menuBtn").innerText = "Menu";
                document.getElementById("historyBtn").innerText = "History";
                document.getElementById("aboutBtn").innerText = "About Us";
                translateBtn.innerText = "Traduci";
            }
        });
    </script>
</body>
</html>
