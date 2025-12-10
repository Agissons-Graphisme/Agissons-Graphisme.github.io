<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Agissons - Design Graphique Engagé</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: #0a0a0a;
            color: #f5f5f5;
            line-height: 1.6;
        }

        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.95);
            backdrop-filter: blur(10px);
            z-index: 1000;
            border-bottom: 1px solid #ff3838;
        }

        nav ul {
            display: flex;
            justify-content: center;
            list-style: none;
            padding: 1.5rem;
            gap: 3rem;
        }

        nav a {
            color: #f5f5f5;
            text-decoration: none;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 2px;
            font-size: 0.9rem;
            transition: color 0.3s;
        }

        nav a:hover {
            color: #ff3838;
        }

        section {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 6rem 2rem 2rem;
        }

        .container {
            max-width: 1200px;
            width: 100%;
        }

        #accueil {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a1a 100%);
            position: relative;
            overflow: hidden;
        }

        #accueil::before {
            content: '';
            position: absolute;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(255, 56, 56, 0.1) 0%, transparent 70%);
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            animation: pulse 4s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: translate(-50%, -50%) scale(1); }
            50% { transform: translate(-50%, -50%) scale(1.2); }
        }

        .hero {
            text-align: center;
            position: relative;
            z-index: 1;
        }

        h1 {
            font-size: 5rem;
            font-weight: 900;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #ff3838 0%, #ff6b6b 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-transform: uppercase;
            letter-spacing: -2px;
        }

        .tagline {
            font-size: 1.5rem;
            color: #999;
            font-weight: 300;
            margin-bottom: 3rem;
        }

        .cta {
            display: inline-block;
            padding: 1rem 3rem;
            background: #ff3838;
            color: #fff;
            text-decoration: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            border: 2px solid #ff3838;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .cta::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: #fff;
            transition: left 0.3s;
            z-index: -1;
        }

        .cta:hover::before {
            left: 0;
        }

        .cta:hover {
            color: #ff3838;
        }

        #mission {
            background: #0f0f0f;
        }

        .mission-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
        }

        .mission-card {
            padding: 2.5rem;
            background: #1a1a1a;
            border-left: 4px solid #ff3838;
            transition: transform 0.3s;
        }

        .mission-card:hover {
            transform: translateX(10px);
        }

        .mission-card h3 {
            font-size: 1.8rem;
            margin-bottom: 1rem;
            color: #ff3838;
        }

        #contact {
            background: #0a0a0a;
        }

        .contact-form {
            max-width: 700px;
            margin: 0 auto;
            background: #1a1a1a;
            padding: 3rem;
            border: 1px solid #333;
        }

        .contact-form h2 {
            font-size: 2.5rem;
            margin-bottom: 2rem;
            color: #ff3838;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 600;
            text-transform: uppercase;
            font-size: 0.85rem;
            letter-spacing: 1px;
            color: #999;
        }

        input, textarea {
            width: 100%;
            padding: 1rem;
            background: #0a0a0a;
            border: 1px solid #333;
            color: #f5f5f5;
            font-family: inherit;
            font-size: 1rem;
            transition: border-color 0.3s;
        }

        input:focus, textarea:focus {
            outline: none;
            border-color: #ff3838;
        }

        textarea {
            resize: vertical;
            min-height: 150px;
        }

        button {
            width: 100%;
            padding: 1.2rem;
            background: #ff3838;
            color: #fff;
            border: none;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 2px;
            cursor: pointer;
            transition: background 0.3s;
            font-size: 1rem;
        }

        button:hover {
            background: #ff1a1a;
        }

        .partners-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2rem;
        }

        .partner-card {
            background: #1a1a1a;
            padding: 2rem;
            text-align: center;
            border: 1px solid #333;
            transition: all 0.3s;
            text-decoration: none;
            color: #f5f5f5;
            display: block;
        }

        .partner-card:hover {
            transform: translateY(-10px);
            border-color: #ff3838;
            box-shadow: 0 10px 30px rgba(255, 56, 56, 0.3);
        }

        .partner-image {
            width: 120px;
            height: 120px;
            margin: 0 auto 1.5rem;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: transform 0.3s;
        }

        .partner-card:hover .partner-image {
            transform: scale(1.1);
        }

        .partner-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #ff3838;
        }

        .partner-card p {
            color: #999;
            font-size: 0.95rem;
        }

        #partenaires {
            background: #0a0a0a;
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 3rem;
            }

            nav ul {
                gap: 1.5rem;
                padding: 1rem;
            }

            .contact-form {
                padding: 2rem;
            }
        }
    </style>
</head>
<body>
    <nav>
        <ul>
            <li><a href="#accueil">Accueil</a></li>
            <li><a href="#mission">Notre Engagement</a></li>
            <li><a href="#partenaires">Partenaires</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="accueil">
        <div class="container">
            <div class="hero">
                <h1>Agissons</h1>
                <p class="tagline">Graphisme au service du bien commun</p>
                <a href="#contact" class="cta">Collaborons ensemble</a>
            </div>
        </div>
    </section>

    <section id="mission">
        <div class="container">
            <div class="mission-content">
                <div class="mission-card">
                    <h3>Associations</h3>
                    <p>Nous mettons notre créativité au service des associations qui œuvrent pour un monde meilleur. Ensemble, donnons de la visibilité à vos actions.</p>
                </div>
                <div class="mission-card">
                    <h3>Éthique</h3>
                    <p>Nous choisissons nos partenaires selon leurs valeurs. Économie sociale et solidaire, environnement, justice sociale : votre cause est notre priorité.</p>
                </div>
                <div class="mission-card">
                    <h3>Impact</h3>
                    <p>Chaque projet est une opportunité de créer du changement. Design graphique, identité visuelle, communication : des outils puissants pour vos missions.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="partenaires">
        <div class="container">
            <h2 style="text-align: center; font-size: 2.5rem; margin-bottom: 2rem; color: #ff3838; text-transform: uppercase; letter-spacing: 2px;">Mon Parcours</h2>
            <div style="max-width: 900px; margin: 0 auto; text-align: center; color: #ccc; font-size: 1.1rem; line-height: 1.8; margin-bottom: 4rem;">
                <p style="margin-bottom: 1.5rem;">Formé en graphisme, j'ai passé 3 ans à accompagner des créateurs de contenu sur Twitch et YouTube dans leur développement visuel. De l'identité de marque aux animations en passant par les miniatures percutantes, j'ai appris à créer des visuels qui captivent et convertissent.</p>
                <p style="margin-bottom: 1.5rem;">Aujourd'hui, je souhaite mettre cette expertise au service d'une cause qui me tient à cœur : donner aux associations les moyens d'une communication professionnelle, efficace et accessible.</p>
                <p style="color: #ff3838; font-weight: 600; font-size: 1.2rem;">Parce qu'une mission importante mérite une visibilité forte, sans exploser les budgets.</p>
            </div>
            
            <h3 style="text-align: center; font-size: 2rem; margin-bottom: 3rem; color: #f5f5f5; text-transform: uppercase; letter-spacing: 1px;">Mes Services</h3>
            <div class="partners-grid">
                <div class="partner-card" style="cursor: default;">
                    <div class="partner-image" style="background: linear-gradient(135deg, #e74c3c 0%, #c0392b 100%);">
                        <svg viewBox="0 0 200 200" style="width: 80px; height: 80px;">
                            <rect x="60" y="70" width="80" height="60" fill="none" stroke="white" stroke-width="6" rx="5"/>
                            <circle cx="85" cy="95" r="8" fill="white"/>
                            <path d="M105 95 L125 115 L145 85" stroke="white" stroke-width="6" fill="none"/>
                        </svg>
                    </div>
                    <h3>Identité Visuelle</h3>
                    <p>Logo, charte graphique, supports print et digitaux pour une image cohérente et percutante</p>
                </div>

                <div class="partner-card" style="cursor: default;">
                    <div class="partner-image" style="background: linear-gradient(135deg, #3498db 0%, #2980b9 100%);">
                        <svg viewBox="0 0 200 200" style="width: 80px; height: 80px;">
                            <rect x="60" y="65" width="80" height="70" fill="none" stroke="white" stroke-width="6" rx="3"/>
                            <line x1="75" y1="85" x2="125" y2="85" stroke="white" stroke-width="4"/>
                            <line x1="75" y1="100" x2="125" y2="100" stroke="white" stroke-width="4"/>
                            <line x1="75" y1="115" x2="105" y2="115" stroke="white" stroke-width="4"/>
                        </svg>
                    </div>
                    <h3>Communication Digitale</h3>
                    <p>Visuels réseaux sociaux, bannières web, newsletters pour maximiser votre présence en ligne</p>
                </div>

                <div class="partner-card" style="cursor: default;">
                    <div class="partner-image" style="background: linear-gradient(135deg, #9b59b6 0%, #8e44ad 100%);">
                        <svg viewBox="0 0 200 200" style="width: 80px; height: 80px;">
                            <path d="M70 120 L100 70 L130 120" fill="none" stroke="white" stroke-width="6"/>
                            <circle cx="100" cy="70" r="12" fill="white"/>
                            <line x1="85" y1="120" x2="115" y2="120" stroke="white" stroke-width="6"/>
                        </svg>
                    </div>
                    <h3>Supports de Campagne</h3>
                    <p>Affiches, flyers, dépliants pour vos événements et actions de sensibilisation</p>
                </div>

                <div class="partner-card" style="cursor: default;">
                    <div class="partner-image" style="background: linear-gradient(135deg, #1abc9c 0%, #16a085 100%);">
                        <svg viewBox="0 0 200 200" style="width: 80px; height: 80px;">
                            <rect x="65" y="75" width="70" height="50" fill="none" stroke="white" stroke-width="6" rx="5"/>
                            <polygon points="100,95 110,105 90,105" fill="white"/>
                        </svg>
                    </div>
                    <h3>Contenus Visuels</h3>
                    <p>Infographies, illustrations, templates pour clarifier vos messages et toucher vos cibles</p>
                </div>

                <div class="partner-card" style="cursor: default;">
                    <div class="partner-image" style="background: linear-gradient(135deg, #f39c12 0%, #d68910 100%);">
                        <svg viewBox="0 0 200 200" style="width: 80px; height: 80px;">
                            <circle cx="100" cy="100" r="40" fill="none" stroke="white" stroke-width="6"/>
                            <path d="M100 65 L100 100 L125 115" stroke="white" stroke-width="6" fill="none"/>
                        </svg>
                    </div>
                    <h3>Tarifs Solidaires</h3>
                    <p>Prix adaptés aux budgets associatifs, devis transparent et possibilité de paiement échelonné</p>
                </div>

                <div class="partner-card" style="cursor: default;">
                    <div class="partner-image" style="background: linear-gradient(135deg, #27ae60 0%, #229954 100%);">
                        <svg viewBox="0 0 200 200" style="width: 80px; height: 80px;">
                            <path d="M100 60 L120 90 L150 95 L125 120 L130 150 L100 135 L70 150 L75 120 L50 95 L80 90 Z" fill="white"/>
                        </svg>
                    </div>
                    <h3>Accompagnement Complet</h3>
                    <p>De la conception à la livraison, conseils stratégiques inclus pour un impact maximal</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <div class="contact-form">
                <h2>Parlons de votre projet</h2>
                <form id="mailForm">
                    <div class="form-group">
                        <label for="nom">Nom</label>
                        <input type="text" id="nom" name="nom" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    <div class="form-group">
                        <label for="sujet">Sujet</label>
                        <input type="text" id="sujet" name="sujet" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    <button type="submit">Envoyer</button>
                </form>
            </div>
        </div>
    </section>

    <script>
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                target.scrollIntoView({ behavior: 'smooth' });
            });
        });

        document.getElementById('mailForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            const nom = document.getElementById('nom').value;
            const email = document.getElementById('email').value;
            const sujet = document.getElementById('sujet').value;
            const message = document.getElementById('message').value;
            
            const mailtoLink = `mailto:kbonvoisin.contact@gmail.com?subject=${encodeURIComponent(sujet)}&body=${encodeURIComponent(`Nom: ${nom}\nEmail: ${email}\n\nMessage:\n${message}`)}`;
            
            window.location.href = mailtoLink;
        });
    </script>
</body>
</html>
