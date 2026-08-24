 <!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>PIERRE GRAPHISME | Photographie • Vidéo • Design</title>

    <meta name="description"
          content="PIERRE GRAPHISME - Photographie, vidéographie, montage vidéo, création de logos et affiches publicitaires.">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #0b0b0b;
            color: white;
            line-height: 1.6;
        }

        /* ================= HEADER ================= */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(0, 0, 0, 0.92);
            border-bottom: 1px solid rgba(255,255,255,0.1);
        }

        .navbar {
            max-width: 1200px;
            margin: auto;
            padding: 18px 25px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 25px;
            font-weight: bold;
            letter-spacing: 2px;
        }

        .logo span {
            color: #ff8c00;
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 28px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: 0.3s;
        }

        nav a:hover {
            color: #ff8c00;
        }

        /* ================= HERO ================= */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 120px 20px 60px;

            background:
                linear-gradient(rgba(0,0,0,.70), rgba(0,0,0,.85)),
                radial-gradient(circle at center, #444, #050505 70%);
        }

        .hero-content {
            max-width: 900px;
        }

        .hero h1 {
            font-size: clamp(45px, 8vw, 90px);
            line-height: 1;
            margin-bottom: 25px;
            text-transform: uppercase;
        }

        .hero h1 span {
            color: #ff8c00;
        }

        .hero p {
            font-size: 20px;
            color: #ddd;
            margin-bottom: 35px;
        }

        .buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .btn {
            display: inline-block;
            padding: 14px 28px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            transition: .3s;
        }

        .btn-primary {
            background: #ff8c00;
            color: #111;
        }

        .btn-primary:hover {
            background: white;
            transform: translateY(-3px);
        }

        .btn-outline {
            border: 2px solid white;
            color: white;
        }

        .btn-outline:hover {
            background: white;
            color: #111;
        }

        /* ================= SECTIONS ================= */

        section {
            padding: 90px 20px;
        }

        .container {
            max-width: 1200px;
            margin: auto;
        }

        .section-title {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-title h2 {
            font-size: 42px;
            text-transform: uppercase;
            margin-bottom: 10px;
        }

        .section-title h2 span {
            color: #ff8c00;
        }

        .section-title p {
            color: #aaa;
        }

        /* ================= SERVICES ================= */

        #services {
            background: #111;
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .service {
            background: #191919;
            padding: 35px 25px;
            text-align: center;
            border-radius: 15px;
            border: 1px solid #292929;
            transition: .3s;
        }

        .service:hover {
            transform: translateY(-8px);
            border-color: #ff8c00;
        }

        .service-icon {
            font-size: 50px;
            margin-bottom: 20px;
        }

        .service h3 {
            color: #ff8c00;
            margin-bottom: 12px;
        }

        .service p {
            color: #bbb;
        }

        /* ================= ABOUT ================= */

        .about {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-image {
            min-height: 400px;
            border-radius: 20px;
            background:
                linear-gradient(135deg, #ff8c00, #111 45%, #333);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 90px;
        }

        .about-text h2 {
            font-size: 42px;
            margin-bottom: 20px;
        }

        .about-text h2 span {
            color: #ff8c00;
        }

        .about-text p {
            color: #bbb;
            margin-bottom: 15px;
        }

        /* ================= GALERIE ================= */

        #galerie {
            background: #080808;
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
        }

        .gallery-item {
            height: 250px;
            border-radius: 12px;
            overflow: hidden;
            position: relative;
            background: linear-gradient(135deg, #333, #111);
            cursor: pointer;
        }

        .gallery-item img,
        .gallery-item video {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: .5s;
        }

        .gallery-item:hover img,
        .gallery-item:hover video {
            transform: scale(1.08);
        }

        .gallery-overlay {
            position: absolute;
            inset: 0;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(0,0,0,.45);
            opacity: 0;
            transition: .3s;
            font-size: 40px;
        }

        .gallery-item:hover .gallery-overlay {
            opacity: 1;
        }

        /* ================= VIDEO ================= */

        .video-section {
            background: #151515;
        }

        .video-box {
            max-width: 900px;
            margin: auto;
            border-radius: 15px;
            overflow: hidden;
            background: #000;
        }

        .video-box video {
            width: 100%;
            display: block;
        }

        /* ================= CONTACT ================= */

        .contact {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .contact-info h3 {
            color: #ff8c00;
            font-size: 28px;
            margin-bottom: 20px;
        }

        .contact-info p {
            margin: 15px 0;
            color: #ccc;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 15px;
        }

        input,
        textarea {
            width: 100%;
            padding: 15px;
            border: 1px solid #333;
            border-radius: 8px;
            background: #151515;
            color: white;
            outline: none;
        }

        input:focus,
        textarea:focus {
            border-color: #ff8c00;
        }

        textarea {
            height: 150px;
            resize: vertical;
        }

        button {
            padding: 15px;
            border: none;
            border-radius: 8px;
            background: #ff8c00;
            color: #111;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
        }

        button:hover {
            background: white;
        }

        /* ================= FOOTER ================= */

        footer {
            background: #050505;
            text-align: center;
            padding: 35px 20px;
            border-top: 1px solid #222;
        }

        footer strong {
            color: #ff8c00;
        }

        .social {
            margin: 20px 0;
        }

        .social a {
            color: white;
            margin: 0 10px;
            text-decoration: none;
        }

        .social a:hover {
            color: #ff8c00;
        }

        /* ================= RESPONSIVE ================= */

        @media (max-width: 900px) {

            nav ul {
                gap: 12px;
            }

            .services-grid,
            .gallery {
                grid-template-columns: repeat(2, 1fr);
            }

            .about,
            .contact {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 600px) {

            .navbar {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            .services-grid,
            .gallery {
                grid-template-columns: 1fr;
            }

            .section-title h2 {
                font-size: 32px;
            }

            .hero h1 {
                font-size: 50px;
            }
        }
    </style>
</head>

<body>

<!-- ================= MENU ================= -->

<header>
    <div class="navbar">

        <div class="logo">
            PIERRE <span>GRAPHISME</span>
        </div>

        <nav>
            <ul>
                <li><a href="#accueil">Accueil</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#galerie">Galerie</a></li>
                <li><a href="#apropos">À propos</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>

    </div>
</header>


<!-- ================= ACCUEIL ================= -->

<section class="hero" id="accueil">

    <div class="hero-content">

        <h1>
            PIERRE <span>GRAPHISME</span>
        </h1>

        <p>
            Photographie • Vidéographie • Design graphique
        </p>

        <p>
            Nous transformons vos idées en images,
            vidéos et créations visuelles professionnelles.
        </p>

        <div class="buttons">

            <a href="#galerie" class="btn btn-primary">
                Voir nos réalisations
            </a>

            <a href="#contact" class="btn btn-outline">
                Nous contacter
            </a>

        </div>

    </div>

</section>


<!-- ================= SERVICES ================= -->

<section id="services">

    <div class="container">

        <div class="section-title">
            <h2>Nos <span>Services</span></h2>
            <p>Des solutions créatives pour vos projets.</p>
        </div>

        <div class="services-grid">

            <div class="service">
                <div class="service-icon">📸</div>
                <h3>Photographie</h3>
                <p>
                    Photos professionnelles pour cérémonies,
                    événements, portraits et communication.
                </p>
            </div>

            <div class="service">
                <div class="service-icon">🎥</div>
                <h3>Vidéographie</h3>
                <p>
                    Captation vidéo professionnelle de vos
                    événements et projets.
                </p>
            </div>

            <div class="service">
                <div class="service-icon">🎬</div>
                <h3>Montage vidéo</h3>
                <p>
                    Montage dynamique et professionnel pour
                    films, événements et réseaux sociaux.
                </p>
            </div>

            <div class="service">
                <div class="service-icon">🎨</div>
                <h3>Affiches publicitaires</h3>
                <p>
                    Création d'affiches modernes et
                    attractives pour votre communication.
                </p>
            </div>

            <div class="service">
                <div class="service-icon">✨</div>
                <h3>Création de logos</h3>
                <p>
                    Des identités visuelles uniques pour
                    donner une image forte à votre marque.
                </p>
            </div>

            <div class="service">
                <div class="service-icon">📺</div>
                <h3>Vidéo publicitaire</h3>
                <p>
                    Création de spots publicitaires adaptés
                    à Facebook, Instagram, TikTok et YouTube.
                </p>
            </div>

        </div>

    </div>

</section>


<!-- ================= GALERIE ================= -->

<section id="galerie">

    <div class="container">

        <div class="section-title">
            <h2>Notre <span>Galerie</span></h2>
            <p>Quelques exemples de nos réalisations.</p>
        </div>

        <div class="gallery">

            <!-- Remplacez image1.jpg par vos photos -->

            <div class="gallery-item">
                <img src="images/image1.jpg" alt="Photographie Pierre Graphisme">
                <div class="gallery-overlay">📸</div>
            </div>

            <div class="gallery-item">
                <img src="images/image2.jpg" alt="Photographie professionnelle">
                <div class="gallery-overlay">📸</div>
            </div>

            <div class="gallery-item">
                <img src="images/image3.jpg" alt="Événement">
                <div class="gallery-overlay">📸</div>
            </div>

            <div class="gallery-item">
                <img src="images/image4.jpg" alt="Création graphique">
                <div class="gallery-overlay">🎨</div>
            </div>

            <div class="gallery-item">
                <img src="images/image5.jpg" alt="Design graphique">
                <div class="gallery-overlay">🎨</div>
            </div>

            <div class="gallery-item">
                <img src="images/image6.jpg" alt="Reportage vidéo">
                <div class="gallery-overlay">🎥</div>
            </div>

        </div>

    </div>

</section>


<!-- ================= VIDEO ================= -->

<section class="video-section">

    <div class="container">

        <div class="section-title">
            <h2>Nos <span>Vidéos</span></h2>
            <p>Découvrez nos productions audiovisuelles.</p>
        </div>

        <div class="video-box">

            <!-- Remplacez video.mp4 par votre vidéo -->

            <video controls poster="images/video-cover.jpg">
                <source src="videos/video.mp4" type="video/mp4">
                Votre navigateur ne supporte pas la vidéo.
            </video>

        </div>

    </div>

</section>


<!-- ================= A PROPOS ================= -->

<section id="apropos">

    <div class="container">

        <div class="about">

            <div class="about-image">
                📷
            </div>

            <div class="about-text">

                <h2>
                    À propos de <span>Pierre Graphisme</span>
                </h2>

                <p>
                    PIERRE GRAPHISME est un studio créatif spécialisé
                    dans la photographie, la vidéo et le design graphique.
                </p>

                <p>
                    Notre objectif est de donner vie à vos idées grâce
                    à des images modernes, créatives et professionnelles.
                </p>

                <p>
                    Que vous soyez particulier, entreprise,
                    association ou organisation, nous vous accompagnons
                    dans la réalisation de vos projets visuels.
                </p>

                <a href="#contact" class="btn btn-primary">
                    Parlons de votre projet
                </a>

            </div>

        </div>

    </div>

</section>


<!-- ================= CONTACT ================= -->

<section id="contact">

    <div class="container">

        <div class="section-title">

            <h2>Nous <span>Contacter</span></h2>

            <p>
                Vous avez un projet ? Contactez PIERRE GRAPHISME.
            </p>

        </div>

        <div class="contact">

            <div class="contact-info">

                <h3>PIERRE GRAPHISME</h3>

                <p>📸 Photographe professionnel</p>

                <p>🎥 Cameraman / Vidéaste</p>

                <p>🎨 Graphiste</p>

                <p>🎬 Montage vidéo</p>

                <p>📢 Publicité et communication visuelle</p>

                <p>📱 Réseaux sociaux</p>

            </div>


            <form onsubmit="envoyerMessage(event)">

                <input
                    type="text"
                    id="nom"
                    placeholder="Votre nom"
                    required
                >

                <input
                    type="email"
                    id="email"
                    placeholder="Votre adresse email"
                    required
                >

                <input
                    type="text"
                    id="sujet"
                    placeholder="Sujet"
                    required
                >

                <textarea
                    id="message"
                    placeholder="Votre message..."
                    required
                ></textarea>

                <button type="submit">
                    Envoyer le message
                </button>

            </form>

        </div>

    </div>

</section>


<!-- ================= FOOTER ================= -->

<footer>

    <h3>
        PIERRE <strong>GRAPHISME</strong>
    </h3>

    <div class="social">

        <a href="#">Facebook</a>
        <a href="#">WhatsApp</a>
        <a href="#">Instagram</a>
        <a href="#">TikTok</a>

    </div>

    <p>
        © 2026 PIERRE GRAPHISME — Tous droits réservés.
    </p>

</footer>


<!-- ================= JAVASCRIPT ================= -->

<script>

function envoyerMessage(event) {

    event.preventDefault();

    const nom = document.getElementById("nom").value;
    const sujet = document.getElementById("sujet").value;
    const message = document.getElementById("message").value;

    const texte =
        "Bonjour Pierre Graphisme,%0A%0A" +
        "Nom : " + nom + "%0A" +
        "Sujet : " + sujet + "%0A%0A" +
        message;

    /*
       REMPLACEZ 22500000000 PAR VOTRE NUMÉRO
       WHATSAPP AVEC L'INDICATIF DU PAYS.
    */

    const numero = "22500000000";

    window.open(
        "https://wa.me/" + numero + "?text=" + texte,
        "_blank"
    );
}

</script>

</body>
</html>
