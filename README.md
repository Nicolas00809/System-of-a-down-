# System-of-a-down-
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>System of a Down - A Voz do Metal Alternativo</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset e estilos gerais */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #8B0000;
            --secondary: #1a1a1a;
            --accent: #D4AF37;
            --text: #f0f0f0;
            --light-bg: #2a2a2a;
        }
        
        body {
            background-color: var(--secondary);
            color: var(--text);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        a {
            text-decoration: none;
            color: var(--accent);
            transition: all 0.3s ease;
        }
        
        a:hover {
            color: var(--primary);
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        .section-padding {
            padding: 80px 0;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary), #a52a2a);
            color: white;
            padding: 12px 30px;
            border-radius: 30px;
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: none;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(139, 0, 0, 0.3);
        }
        
        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(139, 0, 0, 0.4);
            background: linear-gradient(45deg, #a52a2a, var(--primary));
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 50px;
            position: relative;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--accent);
            display: inline-block;
            padding-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }
        
        .section-title h2::after {
            content: '';
            position: absolute;
            width: 100px;
            height: 3px;
            background: linear-gradient(to right, transparent, var(--primary), transparent);
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Cabeçalho */
        header {
            background-color: rgba(26, 26, 26, 0.95);
            padding: 20px 0;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            transition: all 0.3s ease;
        }
        
        header.scrolled {
            padding: 15px 0;
            background-color: rgba(26, 26, 26, 0.98);
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            display: flex;
            align-items: center;
        }
        
        .logo h1 {
            font-size: 2rem;
            color: var(--accent);
            text-shadow: 0 0 10px rgba(212, 175, 55, 0.5);
            letter-spacing: 3px;
        }
        
        .logo span {
            color: var(--primary);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 30px;
        }
        
        nav ul li a {
            font-weight: 600;
            font-size: 1.1rem;
            padding: 5px 10px;
            border-radius: 3px;
            position: relative;
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            background-color: var(--primary);
            bottom: 0;
            left: 0;
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        .menu-toggle {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        /* Banner Hero */
        .hero {
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), 
                        url('https://images.unsplash.com/photo-1514525253161-7a46d19cd819?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
            height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 0 20px;
        }
        
        .hero-content h2 {
            font-size: 4rem;
            margin-bottom: 20px;
            text-shadow: 2px 2px 10px rgba(0, 0, 0, 0.8);
            color: var(--accent);
        }
        
        .hero-content p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 30px;
            color: var(--text);
        }
        
        /* Sobre */
        .about {
            background-color: var(--light-bg);
        }
        
        .about-content {
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            gap: 40px;
        }
        
        .about-text {
            flex: 1;
            min-width: 300px;
        }
        
        .about-text p {
            margin-bottom: 20px;
            text-align: justify;
        }
        
        .about-image {
            flex: 1;
            min-width: 300px;
            text-align: center;
            position: relative;
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            width: 100%;
            height: 100%;
            border: 3px solid var(--primary);
            top: -15px;
            left: -15px;
            z-index: -1;
        }
        
        .about-image img {
            max-width: 100%;
            border-radius: 5px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.5);
        }
        
        /* Membros */
        .members-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 30px;
        }
        
        .member-card {
            background: linear-gradient(145deg, #2a2a2a, #1f1f1f);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            position: relative;
        }
        
        .member-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(139, 0, 0, 0.2);
        }
        
        .member-image {
            height: 300px;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: flex-end;
            justify-content: center;
            padding: 20px;
            position: relative;
        }
        
        .member-number {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--primary);
            color: white;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            font-size: 1.2rem;
        }
        
        .member-info {
            padding: 20px;
            text-align: center;
        }
        
        .member-info h3 {
            color: var(--accent);
            margin-bottom: 10px;
            font-size: 1.5rem;
        }
        
        .member-role {
            color: var(--primary);
            font-weight: bold;
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        /* Discografia */
        .discography {
            background-color: var(--light-bg);
        }
        
        .albums-container {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
        }
        
        .album-card {
            background: linear-gradient(145deg, #2a2a2a, #1f1f1f);
            border-radius: 10px;
            overflow: hidden;
            width: 280px;
            transition: transform 0.3s ease;
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        .album-card:hover {
            transform: scale(1.05);
        }
        
        .album-cover {
            height: 280px;
            background-size: cover;
            background-position: center;
            display: flex;
            align-items: flex-end;
            position: relative;
        }
        
        .album-year {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--accent);
            color: var(--secondary);
            padding: 5px 10px;
            border-radius: 20px;
            font-weight: bold;
        }
        
        .album-info {
            padding: 20px;
            text-align: center;
        }
        
        .album-info h3 {
            margin-bottom: 10px;
            color: var(--accent);
        }
        
        .album-info p {
            color: #aaa;
            font-size: 0.9rem;
        }
        
        /* Tour */
        .tour-dates {
            max-width: 900px;
            margin: 0 auto;
        }
        
        .tour-item {
            background: linear-gradient(145deg, #2a2a2a, #1f1f1f);
            margin-bottom: 20px;
            border-radius: 10px;
            overflow: hidden;
            display: flex;
            flex-wrap: wrap;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease;
        }
        
        .tour-item:hover {
            transform: translateX(10px);
        }
        
        .tour-date {
            background: linear-gradient(45deg, var(--primary), #a52a2a);
            padding: 20px;
            min-width: 150px;
            text-align: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            font-weight: bold;
        }
        
        .tour-date .day {
            font-size: 2rem;
            line-height: 1;
        }
        
        .tour-info {
            padding: 20px;
            flex: 1;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
        
        .tour-info h3 {
            margin-bottom: 5px;
            color: var(--accent);
        }
        
        .tour-btn {
            padding: 20px;
            display: flex;
            align-items: center;
        }
        
        /* Contato */
        .contact {
            background-color: var(--light-bg);
        }
        
        .contact-content {
            display: flex;
            flex-wrap: wrap;
            gap: 40px;
        }
        
        .contact-info, .contact-form {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-info h3 {
            margin-bottom: 20px;
            color: var(--accent);
            font-size: 1.8rem;
        }
        
        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-right: 10px;
            color: var(--primary);
            width: 20px;
        }
        
        .social-links {
            margin-top: 30px;
        }
        
        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background-color: var(--secondary);
            border-radius: 50%;
            margin-right: 15px;
            font-size: 1.2rem;
            transition: all 0.3s ease;
        }
        
        .social-links a:hover {
            background-color: var(--primary);
            transform: translateY(-5px);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        
        .form-group input, .form-group textarea, .form-group select {
            width: 100%;
            padding: 12px 15px;
            background-color: var(--secondary);
            border: 1px solid #444;
            border-radius: 5px;
            color: var(--text);
            font-size: 1rem;
            transition: border 0.3s ease;
        }
        
        .form-group input:focus, .form-group textarea:focus, .form-group select:focus {
            border-color: var(--primary);
            outline: none;
        }
        
        .form-group textarea {
            height: 150px;
            resize: vertical;
        }
        
        /* Rodapé */
        footer {
            background-color: var(--secondary);
            padding: 50px 0 20px;
            text-align: center;
            border-top: 3px solid var(--primary);
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 30px;
        }
        
        .footer-column {
            flex: 1;
            min-width: 250px;
            margin-bottom: 30px;
        }
        
        .footer-column h3 {
            color: var(--accent);
            margin-bottom: 20px;
            font-size: 1.3rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: #aaa;
        }
        
        .footer-column ul li a:hover {
            color: var(--accent);
            padding-left: 5px;
        }
        
        .copyright {
            padding-top: 20px;
            border-top: 1px solid #444;
            color: #777;
            font-size: 0.9rem;
        }
        
        /* Responsividade */
        @media (max-width: 992px) {
            .hero-content h2 {
                font-size: 3rem;
            }
            
            .section-title h2 {
                font-size: 2rem;
            }
            
            nav ul {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                width: 100%;
                background-color: var(--secondary);
                flex-direction: column;
                padding: 20px 0;
                box-shadow: 0 5px 10px rgba(0, 0, 0, 0.3);
            }
            
            nav ul.active {
                display: flex;
            }
            
            nav ul li {
                margin: 10px 0;
                text-align: center;
            }
            
            .menu-toggle {
                display: block;
            }
            
            .tour-item {
                flex-direction: column;
            }
            
            .tour-date {
                min-width: 100%;
                flex-direction: row;
                justify-content: space-around;
            }
        }
        
        @media (max-width: 768px) {
            .hero-content h2 {
                font-size: 2.5rem;
            }
            
            .hero-content p {
                font-size: 1.1rem;
            }
            
            .about-image::before {
                display: none;
            }
        }
        
        @media (max-width: 576px) {
            .hero-content h2 {
                font-size: 2rem;
            }
            
            .section-padding {
                padding: 60px 0;
            }
        }
    </style>
</head>
<body>
    <!-- Cabeçalho -->
    <header id="header">
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    <h1>SYSTEM <span>OF A DOWN</span></h1>
                </div>
                <div class="menu-toggle" id="menuToggle">
                    <i class="fas fa-bars"></i>
                </div>
                <nav>
                    <ul id="navMenu">
                        <li><a href="#home">Início</a></li>
                        <li><a href="#about">Sobre</a></li>
                        <li><a href="#members">Membros</a></li>
                        <li><a href="#discography">Discografia</a></li>
                        <li><a href="#tour">Shows</a></li>
                        <li><a href="#contact">Contato</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Banner Hero -->
    <section id="home" class="hero">
        <div class="hero-content">
            <h2>SYSTEM OF A DOWN</h2>
            <p>A banda que redefine o metal com sua sonoridade única e letras politizadas</p>
            <a href="#about" class="btn">Explorar a Banda</a>
        </div>
    </section>

    <!-- Sobre -->
    <section id="about" class="about section-padding">
        <div class="container">
            <div class="section-title">
                <h2>Sobre a Banda</h2>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <p>System of a Down é uma banda americana de metal alternativo formada em Los Angeles, Califórnia, em 1994. A banda é conhecida por sua sonoridade distintiva que incorpora elementos de heavy metal, rock alternativo, rock armênio e música experimental.</p>
                    <p>O grupo é composto por Serj Tankian (vocal, teclado), Daron Malakian (guitarra, vocal), Shavo Odadjian (baixo) e John Dolmayan (bateria). Todos os membros são de origem armênia, e suas raízes culturais frequentemente influenciam sua música.</p>
                    <p>O System of a Down é conhecido por suas letras politizadas que abordam questões como genocídio, guerra, censura e injustiça social. Seu álbum de estreia autointitulado (1998) e os subsequentes "Toxicity" (2001) e "Steal This Album!" (2002) os estabeleceram como uma das bandas mais inovadoras do metal moderno.</p>
                    <p>Após um hiato de 5 anos (2006-2011), a banda retomou suas atividades e continua a realizar turnês mundialmente, mantendo-se fiel à sua missão de criar música poderosa e com mensagem.</p>
                    <a href="#discography" class="btn" style="margin-top: 20px;">Ver Discografia</a>
                </div>
                <div class="about-image">
                    <!-- Imagem representativa - na prática, seria uma imagem real da banda -->
                    <div style="width:100%; height:400px; background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa; border-radius:5px;">
                        <i class="fas fa-music" style="font-size: 3rem; margin-right: 15px;"></i>
                        <span style="font-size: 1.5rem;">SYSTEM OF A DOWN</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Membros -->
    <section id="members" class="members section-padding">
        <div class="container">
            <div class="section-title">
                <h2>Membros da Banda</h2>
            </div>
            <div class="members-grid">
                <!-- Membro 1 -->
                <div class="member-card">
                    <div class="member-number">1</div>
                    <div class="member-image" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <i class="fas fa-user" style="font-size: 5rem;"></i>
                    </div>
                    <div class="member-info">
                        <h3>Serj Tankian</h3>
                        <div class="member-role">Vocalista e Tecladista</div>
                        <p>Conhecido por seu vocal distintivo e letras politizadas. Também possui carreira solo e é ativista político.</p>
                    </div>
                </div>
                
                <!-- Membro 2 -->
                <div class="member-card">
                    <div class="member-number">2</div>
                    <div class="member-image" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <i class="fas fa-guitar" style="font-size: 5rem;"></i>
                    </div>
                    <div class="member-info">
                        <h3>Daron Malakian</h3>
                        <div class="member-role">Guitarrista e Vocalista</div>
                        <p>Principal compositor da banda e fundador. Também lidera a banda Scars on Broadway.</p>
                    </div>
                </div>
                
                <!-- Membro 3 -->
                <div class="member-card">
                    <div class="member-number">3</div>
                    <div class="member-image" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <i class="fas fa-drum" style="font-size: 5rem;"></i>
                    </div>
                    <div class="member-info">
                        <h3>John Dolmayan</h3>
                        <div class="member-role">Baterista</div>
                        <p>Conhecido por seu estilo complexo e preciso. Também é colecionador de quadrinhos e arte.</p>
                    </div>
                </div>
                
                <!-- Membro 4 -->
                <div class="member-card">
                    <div class="member-number">4</div>
                    <div class="member-image" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <i class="fas fa-guitar" style="font-size: 5rem;"></i>
                    </div>
                    <div class="member-info">
                        <h3>Shavo Odadjian</h3>
                        <div class="member-role">Baixista</div>
                        <p>Também atua como diretor criativo da banda. Tem seu próprio selo musical, UrSession.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Discografia -->
    <section id="discography" class="discography section-padding">
        <div class="container">
            <div class="section-title">
                <h2>Discografia</h2>
            </div>
            <div class="albums-container">
                <!-- Álbum 1 -->
                <div class="album-card">
                    <div class="album-cover" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <div class="album-year">1998</div>
                        <i class="fas fa-compact-disc" style="font-size: 4rem;"></i>
                    </div>
                    <div class="album-info">
                        <h3>System of a Down</h3>
                        <p>Álbum de estreia que estabeleceu o som único da banda</p>
                    </div>
                </div>
                
                <!-- Álbum 2 -->
                <div class="album-card">
                    <div class="album-cover" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <div class="album-year">2001</div>
                        <i class="fas fa-compact-disc" style="font-size: 4rem;"></i>
                    </div>
                    <div class="album-info">
                        <h3>Toxicity</h3>
                        <p>O álbum mais bem-sucedido da banda, com hits como "Chop Suey!"</p>
                    </div>
                </div>
                
                <!-- Álbum 3 -->
                <div class="album-card">
                    <div class="album-cover" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <div class="album-year">2002</div>
                        <i class="fas fa-compact-disc" style="font-size: 4rem;"></i>
                    </div>
                    <div class="album-info">
                        <h3>Steal This Album!</h3>
                        <p>Coletânea de músicas não lançadas anteriormente</p>
                    </div>
                </div>
                
                <!-- Álbum 4 -->
                <div class="album-card">
                    <div class="album-cover" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <div class="album-year">2005</div>
                        <i class="fas fa-compact-disc" style="font-size: 4rem;"></i>
                    </div>
                    <div class="album-info">
                        <h3>Mezmerize</h3>
                        <p>Primeira parte do álbum duplo, com Daron Malakian nos vocais principais</p>
                    </div>
                </div>
                
                <!-- Álbum 5 -->
                <div class="album-card">
                    <div class="album-cover" style="background:linear-gradient(45deg, #333, #555); display:flex; align-items:center; justify-content:center; color:#aaa;">
                        <div class="album-year">2005</div>
                        <i class="fas fa-compact-disc" style="font-size: 4rem;"></i>
                    </div>
                    <div class="album-info">
                        <h3>Hypnotize</h3>
                        <p>Segunda parte do álbum duplo, último lançamento de estúdio da banda</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Tour -->
    <section id="tour" class="tour section-padding">
        <div class="container">
            <div class="section-title">
                <h2>Próximos Shows</h2>
            </div>
            <div class="tour-dates">
                <!-- Show 1 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <div>
                            <div class="day">15</div>
                            <div>OUT 2023</div>
                        </div>
                    </div>
                    <div class="tour-info">
                        <h3>São Paulo, Brasil</h3>
                        <p>Allianz Parque</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
                
                <!-- Show 2 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <div>
                            <div class="day">18</div>
                            <div>OUT 2023</div>
                        </div>
                    </div>
                    <div class="tour-info">
                        <h3>Rio de Janeiro, Brasil</h3>
                        <p>Estádio do Maracanã</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
                
                <!-- Show 3 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <div>
                            <div class="day">22</div>
                            <div>OUT 2023</div>
                        </div>
                    </div>
                    <div class="tour-info">
                        <h3>Belo Horizonte, Brasil</h3>
                        <p>Estádio Mineirão</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
                
                <!-- Show 4 -->
                <div class="tour-item">
                    <div class="tour-date">
                        <div>
                            <div class="day">27</div>
                            <div>OUT 2023</div>
                        </div>
                    </div>
                    <div class="tour-info">
                        <h3>Porto Alegre, Brasil</h3>
                        <p>Arena do Grêmio</p>
                    </div>
                    <div class="tour-btn">
                        <a href="#" class="btn">Comprar Ingressos</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contact" class="contact section-padding">
        <div class="container">
            <div class="section-title">
                <h2>Contato</h2>
            </div>
            <div class="contact-content">
                <div class="contact-info">
                    <h3>Entre em Contato</h3>
                    <p><i class="fas fa-map-marker-alt"></i> Los Angeles, California, EUA</p>
                    <p><i class="fas fa-envelope"></i> contact@systemofadown.com</p>
                    <p><i class="fas fa-phone"></i> +1 (555) 123-4567</p>
                    
                    <div class="social-links">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-youtube"></i></a>
                        <a href="#"><i class="fab fa-spotify"></i></a>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">Nome</label>
                            <input type="text" id="name" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="email" id="email" required>
                        </div>
                        
                        <div class="form-group">
                            <label for="subject">Assunto</label>
                            <select id="subject">
                                <option value="general">Informação Geral</option>
                                <option value="show">Shows e Turnês</option>
                                <option value="media">Imprensa e Mídia</option>
                                <option value="other">Outro</option>
                            </select>
                        </div>
                        
                        <div class="form-group">
                            <label for="message">Mensagem</label>
                            <textarea id="message" required></textarea>
                        </div>
                        
                        <button type="submit" class="btn">Enviar Mensagem</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Rodapé -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>System of a Down</h3>
                    <p>A banda que redefine o metal com sua sonoridade única e letras politizadas.</p>
                </div>
                
                <div class="footer-column">
                    <h3>Links Rápidos</h3>
                    <ul>
                        <li><a href="#home">Início</a></li>
                        <li><a href="#about">Sobre</a></li>
                        <li><a href="#members">Membros</a></li>
                        <li><a href="#discography">Discografia</a></li>
                        <li><a href="#tour">Shows</a></li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Álbuns</h3>
                    <ul>
                        <li><a href="#">System of a Down (1998)</a></li>
                        <li><a href="#">Toxicity (2001)</a></li>
                        <li><a href="#">Steal This Album! (2002)</a></li>
                        <li><a href="#">Mezmerize (2005)</a></li>
                        <li><a href="#">Hypnotize (2005)</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 System of a Down. Todos os direitos reservados. | Site criado para fins educacionais</p>
            </div>
        </div>
    </footer>

    <script>
        // Menu mobile toggle
        document.getElementById('menuToggle').addEventListener('click', function() {
            document.getElementById('navMenu').classList.toggle('active');
        });
        
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.getElementById('header');
            if (window.scrollY > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu after clicking a link
                    document.getElementById('navMenu').classList.remove('active');
                }
            });
        });
        
        // Simple form validation
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Obrigado pela sua mensagem! Entraremos em contato em breve.');
            this.reset();
        });
    </script>
</body>
</html>
