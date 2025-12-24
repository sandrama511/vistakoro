# vistakoro
Koro
<!DOCTYPE html>
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vista Korosu - Ankara</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Georgia', 'Times New Roman', serif;
            line-height: 1.8;
            color: #2c3e50;
            background-color: #fafafa;
        }

        /* Header and Navigation */
        header {
            background-color: #1a1a1a;
            color: #ffffff;
            padding: 1.5rem 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 8px rgba(0,0,0,0.15);
        }

        nav {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 2rem;
        }

        .logo {
            font-size: 2rem;
            font-weight: 300;
            letter-spacing: 6px;
            font-family: 'Georgia', serif;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 3rem;
        }

        .nav-links a {
            color: #ffffff;
            text-decoration: none;
            font-weight: 400;
            font-size: 0.95rem;
            letter-spacing: 1px;
            transition: color 0.3s;
            font-family: 'Arial', sans-serif;
        }

        .nav-links a:hover {
            color: #c9a961;
        }

        .menu-toggle {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        /* Main Content */
        main {
            max-width: 1200px;
            margin: 0 auto;
            padding: 3rem 2rem;
        }

        section {
            display: none;
            animation: fadeIn 0.6s ease-in;
        }

        section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 5rem 2rem 4rem;
            background-color: #ffffff;
            margin-bottom: 4rem;
            border-bottom: 1px solid #e0e0e0;
        }

        .hero h1 {
            font-size: 3.5rem;
            color: #1a1a1a;
            margin-bottom: 1.5rem;
            font-weight: 300;
            letter-spacing: 3px;
        }

        .hero p {
            font-size: 1.2rem;
            color: #666;
            max-width: 700px;
            margin: 0 auto;
            font-family: 'Arial', sans-serif;
        }

        /* Content Sections */
        h2 {
            font-size: 2.5rem;
            color: #1a1a1a;
            margin-bottom: 2rem;
            font-weight: 300;
            letter-spacing: 2px;
            padding-bottom: 1rem;
            border-bottom: 2px solid #c9a961;
        }

        h3 {
            font-size: 1.6rem;
            color: #1a1a1a;
            margin-bottom: 1.5rem;
            font-weight: 400;
        }

        .content-box {
            background: #ffffff;
            padding: 3rem;
            margin-bottom: 3rem;
            border: 1px solid #e0e0e0;
        }

        .content-box p {
            font-size: 1.1rem;
            line-height: 1.9;
            color: #555;
            margin-bottom: 1.5rem;
            font-family: 'Arial', sans-serif;
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .info-card {
            background: #f8f8f8;
            padding: 2.5rem;
            border: 1px solid #e0e0e0;
            text-align: center;
        }

        .info-card h3 {
            font-size: 1.3rem;
            margin-bottom: 0.5rem;
            color: #1a1a1a;
            font-weight: 400;
        }

        .info-card p {
            font-size: 1rem;
            color: #666;
            font-family: 'Arial', sans-serif;
        }

        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 3rem;
            margin: 3rem 0;
        }

        .team-member {
            background: #f8f8f8;
            padding: 2.5rem;
            border: 1px solid #e0e0e0;
        }

        .team-member h4 {
            font-size: 1.4rem;
            color: #1a1a1a;
            margin-bottom: 0.5rem;
            font-weight: 400;
        }

        .team-member .role {
            color: #c9a961;
            font-size: 1rem;
            margin-bottom: 0.5rem;
            font-family: 'Arial', sans-serif;
        }

        .team-member .subtitle {
            color: #888;
            font-size: 0.9rem;
            font-style: italic;
            font-family: 'Arial', sans-serif;
        }

        /* Gallery */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .gallery-item {
            background: #f8f8f8;
            border: 1px solid #e0e0e0;
            padding: 3rem 2rem;
            text-align: center;
            min-height: 300px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #aaa;
            font-size: 1rem;
            font-family: 'Arial', sans-serif;
        }

        /* Application Notice */
        .application-notice {
            background: #2c3e50;
            color: white;
            padding: 3rem;
            margin-top: 3rem;
            text-align: center;
        }

        .application-notice h3 {
            color: white;
            margin-bottom: 1rem;
            font-weight: 400;
        }

        .application-notice p {
            font-size: 1.1rem;
            line-height: 1.8;
            font-family: 'Arial', sans-serif;
        }

        .requirements-box {
            margin-top: 3rem;
            padding: 2.5rem;
            background: #f8f8f8;
            border: 1px solid #e0e0e0;
        }

        .requirements-box ul {
            list-style-position: inside;
            font-size: 1.1rem;
            line-height: 2.2;
            color: #555;
            font-family: 'Arial', sans-serif;
        }

        /* Contact */
        .contact-info {
            background: #ffffff;
            padding: 3rem;
            border: 1px solid #e0e0e0;
        }

        .contact-item {
            margin: 2.5rem 0;
            padding: 2rem;
            background: #f8f8f8;
            border-left: 3px solid #c9a961;
        }

        .contact-item strong {
            color: #1a1a1a;
            font-size: 1.2rem;
            display: block;
            margin-bottom: 1rem;
            font-family: 'Arial', sans-serif;
        }

        .contact-item p,
        .contact-item a {
            font-size: 1.1rem;
            line-height: 1.8;
            color: #555;
            font-family: 'Arial', sans-serif;
        }

        .social-link {
            display: inline-block;
            background: #1a1a1a;
            color: white;
            padding: 1rem 2.5rem;
            text-decoration: none;
            margin-top: 1rem;
            transition: background 0.3s;
            font-family: 'Arial', sans-serif;
            letter-spacing: 1px;
        }

        .social-link:hover {
            background: #c9a961;
        }

        .closing-note {
            margin-top: 3rem;
            padding: 2rem;
            background: #f8f8f8;
            text-align: center;
            border: 1px solid #e0e0e0;
        }

        .closing-note p {
            font-size: 1.1rem;
            color: #555;
            font-family: 'Arial', sans-serif;
        }

        /* Footer */
        footer {
            background: #1a1a1a;
            color: white;
            text-align: center;
            padding: 3rem 2rem;
            margin-top: 5rem;
            font-family: 'Arial', sans-serif;
        }

        footer p {
            margin: 0.5rem 0;
            font-size: 0.95rem;
            letter-spacing: 1px;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: #1a1a1a;
                flex-direction: column;
                padding: 2rem;
                gap: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .hero h1 {
                font-size: 2.2rem;
            }

            h2 {
                font-size: 2rem;
            }

            .content-box {
                padding: 2rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <nav>
            <div class="logo">VISTA</div>
            <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#" onclick="showSection('ana-sayfa')">Ana Sayfa</a></li>
                <li><a href="#" onclick="showSection('hakkimizda')">Hakkımızda</a></li>
                <li><a href="#" onclick="showSection('basvuru')">Başvuru</a></li>
                <li><a href="#" onclick="showSection('galeri')">Galeri</a></li>
                <li><a href="#" onclick="showSection('iletisim')">İletişim</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <!-- Ana Sayfa -->
        <section id="ana-sayfa" class="active">
            <div class="hero">
                <h1>Vista Korosu</h1>
                <p>Ankara'nın kalbinde, müziğin evrensel dilini konuşan bir aile</p>
            </div>

            <div class="content-box">
                <h2>Hoş Geldiniz</h2>
                <p>
                    Vista Korosu, 2022 yılında kurulmuş, folk şarkılara özel ilgi duyan, 
                    Türk, Balkan, Rus, Kürt ve İtalyan repertuvarlarıyla zenginleşen 
                    karma bir amatör korodur. Yaklaşık 45 üyeli büyük ve büyüyen ailemizle, 
                    birlikte olmak, şarkı söylemek ve müziğin güzelliğini yaymak amacındayız.
                </p>
            </div>

            <div class="info-grid">
                <div class="info-card">
                    <h3>Kuruluş</h3>
                    <p>2022</p>
                </div>
                <div class="info-card">
                    <h3>Üyeler</h3>
                    <p>45+ kişi</p>
                </div>
                <div class="info-card">
                    <h3>Tür</h3>
                    <p>Karma Koro</p>
                </div>
                <div class="info-card">
                    <h3>Repertuvar</h3>
                    <p>Çok kültürlü folk</p>
                </div>
            </div>
        </section>

        <!-- Hakkımızda -->
        <section id="hakkimizda">
            <h2>Hakkımızda</h2>
            
            <div class="content-box">
                <h3>Vista Korosu</h3>
                <p>
                    Vista Korosu, 2022 yılında İnci Aygan tarafından kurulan, 
                    folk şarkılara özel bir ilgi duyan karma amatör bir korodur. 
                    Türk, Balkan, Rus, Kürt ve İtalyan müzik geleneklerinden beslenen 
                    zengin repertuvarımızla, müziğin evrensel dilini konuşuyoruz.
                </p>
                <p>
                    Yaklaşık 45 üyeli büyük ve sürekli büyüyen ailemizle amacımız: 
                    Birlikte olmak, şarkı söylemek ve müziğin güzelliğini her yere yaymak. 
                    Vista Korosu sadece bir koro değil, müzik sevgisiyle bir araya gelmiş 
                    bir ailedir.
                </p>
            </div>

            <h3>Ekibimiz</h3>
            <div class="team-grid">
                <div class="team-member">
                    <h4>İnci Aygan</h4>
                    <p class="role">Kurucu ve Şef</p>
                    <p class="subtitle">Devlet Korosu Profesyonel Sanatçısı</p>
                </div>
                <div class="team-member">
                    <h4>Hande Lüleci</h4>
                    <p class="role">Piyanist</p>
                    <p class="subtitle">Devlet Korosu Profesyonel Sanatçısı</p>
                </div>
            </div>
        </section>

        <!-- Başvuru -->
        <section id="basvuru">
            <h2>Başvuru</h2>
            
            <div class="content-box">
                <h3>Vista Korosu Ailesine Katılın</h3>
                <p>
                    Vista Korosu ailesine katılmak ve bu müzikal yolculuğun bir parçası olmak ister misiniz? 
                    Müzik sevgisini paylaşan herkesi ailemize davet ediyoruz.
                </p>

                <div class="application-notice">
                    <h3>Başvuru Dönemi</h3>
                    <p>
                        Başvurular şu an kapalıdır. Başvurular belirli tarihlerde açılmaktadır. 
                        Başvuru dönemleri hakkında güncel bilgi almak için lütfen sosyal medya 
                        hesaplarımızı takip edin veya bizimle iletişime geçin.
                    </p>
                </div>

                <div class="requirements-box">
                    <h3>Kimler Başvurabilir?</h3>
                    <ul>
                        <li>Müzik sevgisi olan herkes</li>
                        <li>Profesyonel müzik eğitimi şart değildir</li>
                        <li>Her yaştan katılımcı kabul edilir</li>
                        <li>Düzenli provasına katılım gösterebilecek kişiler</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- Galeri -->
        <section id="galeri">
            <h2>Galeri</h2>
            
            <div class="content-box">
                <p>
                    Vista Korosu'nun konserleri, provaları ve özel anlarından fotoğraflar.
                </p>

                <div class="gallery-grid">
                    <div class="gallery-item">Fotoğraf eklenecek</div>
                    <div class="gallery-item">Fotoğraf eklenecek</div>
                    <div class="gallery-item">Fotoğraf eklenecek</div>
                    <div class="gallery-item">Fotoğraf eklenecek</div>
                    <div class="gallery-item">Fotoğraf eklenecek</div>
                    <div class="gallery-item">Fotoğraf eklenecek</div>
                </div>

                <p style="margin-top: 2rem; text-align: center; color: #888; font-style: italic;">
                    Daha fazla fotoğraf için <a href="https://www.instagram.com/vistakorosu/" target="_blank" style="color: #c9a961; text-decoration: none;">Instagram hesabımızı</a> ziyaret edin.
                </p>
            </div>
        </section>

        <!-- İletişim -->
        <section id="iletisim">
            <h2>İletişim</h2>
            
            <div class="contact-info">
                <div class="contact-item">
                    <strong>Adres</strong>
                    <p>
                        Tunalı Hilmi Cad. 114/42<br>
                        Kavaklıdere, Ankara<br>
                        Sevda - Cenap And Müzik Vakfı
                    </p>
                </div>

                <div class="contact-item">
                    <strong>Sosyal Medya</strong>
                    <a href="https://www.instagram.com/vistakorosu/" target="_blank" class="social-link">
                        Instagram
                    </a>
                </div>

                <div class="closing-note">
                    <p>
                        Sorularınız için sosyal medya hesaplarımızdan bize ulaşabilirsiniz. 
                        Vista Korosu ailesi olarak sizlerle tanışmayı dört gözle bekliyoruz.
                    </p>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>Vista Korosu</p>
        <p>Ankara, Türkiye</p>
    </footer>

    <script>
        function showSection(sectionId) {
            const sections = document.querySelectorAll('section');
            sections.forEach(section => {
                section.classList.remove('active');
            });

            document.getElementById(sectionId).classList.add('active');
            document.getElementById('navLinks').classList.remove('active');
            window.scrollTo(0, 0);
        }

        function toggleMenu() {
            document.getElementById('navLinks').classList.toggle('active');
        }

        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById('navLinks').classList.remove('active');
            });
        });
    </script>
</body>
</html>
