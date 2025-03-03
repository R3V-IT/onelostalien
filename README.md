<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>OneLostAlien | Games, Music, Apps & Photography</title>
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">
    <!-- Font Awesome for icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        /* Base styles for the entire site */
        :root {
            --primary-color: #6200ea;
            --secondary-color: #03dac6;
            --dark-bg: #121212;
            --light-text: #f5f5f5;
            --card-bg: #1e1e1e;
            --header-font: 'Montserrat', sans-serif;
            --body-font: 'Open Sans', sans-serif;
        }
        
        body {
            font-family: var(--body-font);
            line-height: 1.6;
            margin: 0;
            padding: 0;
            background-color: var(--dark-bg);
            color: var(--light-text);
        }
        
        /* Typography */
        h1, h2, h3, h4 {
            font-family: var(--header-font);
            font-weight: 700;
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 0.5rem;
        }
        
        h2 {
            font-size: 2.2rem;
            margin-bottom: 1rem;
            color: var(--secondary-color);
        }
        
        h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
        }
        
        p {
            font-size: 1rem;
            margin-bottom: 1rem;
        }
        
        a {
            color: var(--secondary-color);
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        a:hover {
            color: #04f7e0;
            text-decoration: underline;
        }
        
        /* Layout */
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header and Navigation */
        header {
            background: linear-gradient(to right, #4a00e0, #8e2de2);
            color: white;
            padding: 2rem 0;
            position: relative;
            overflow: hidden;
        }
        
        header::after {
            content: "";
            position: absolute;
            bottom: -10px;
            left: 0;
            width: 100%;
            height: 20px;
            background: linear-gradient(to right, #4a00e0, #8e2de2);
            transform: skewY(-1deg);
            z-index: -1;
        }
        
        .header-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
        }
        
        .tagline {
            font-size: 1.2rem;
            font-style: italic;
            margin-bottom: 1.5rem;
        }
        
        nav {
            background: rgba(18, 18, 18, 0.9);
            padding: 1rem 0;
            position: sticky;
            top: 0;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
        }
        
        nav ul {
            list-style: none;
            padding: 0;
            margin: 0;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
        }
        
        nav ul li {
            margin: 0 1rem;
        }
        
        nav ul li a {
            color: var(--light-text);
            font-size: 1.1rem;
            font-weight: 600;
            padding: 0.5rem 1rem;
            display: block;
            position: relative;
        }
        
        nav ul li a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--secondary-color);
            transition: width 0.3s ease;
        }
        
        nav ul li a:hover::after {
            width: 100%;
        }
        
        /* Hero Section */
        .hero {
            padding: 5rem 0;
            background: url('/api/placeholder/1200/400') no-repeat center center/cover;
            text-align: center;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.7);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
        }
        
        .hero h2 {
            font-size: 3rem;
            margin-bottom: 1rem;
            color: var(--light-text);
        }
        
        .hero p {
            font-size: 1.3rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--secondary-color);
            color: #121212;
            padding: 0.8rem 1.8rem;
            border-radius: 30px;
            font-weight: 700;
            text-transform: uppercase;
            letter-spacing: 1px;
            transition: all 0.3s ease;
            border: 2px solid var(--secondary-color);
        }
        
        .btn:hover {
            background-color: transparent;
            color: var(--secondary-color);
            text-decoration: none;
        }
        
        /* Sections */
        section {
            padding: 4rem 0;
        }
        
        .section-heading {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        /* Card Layouts */
        .cards-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
        }
        
        .card {
            background-color: var(--card-bg);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
        }
        
        .card-img {
            width: 100%;
            height: 180px;
            object-fit: cover;
        }
        
        .card-content {
            padding: 1.5rem;
        }
        
        .card-title {
            font-size: 1.4rem;
            margin-bottom: 0.5rem;
        }
        
        .card-desc {
            font-size: 0.9rem;
            margin-bottom: 1.5rem;
            color: #b0b0b0;
        }
        
        .card-link {
            display: inline-block;
            padding: 0.5rem 1rem;
            background-color: var(--primary-color);
            color: white;
            border-radius: 5px;
            font-weight: 600;
            transition: background-color 0.3s ease;
        }
        
        .card-link:hover {
            background-color: #7c4dff;
            text-decoration: none;
        }
        
        /* Games Section */
        .game-card {
            text-align: center;
        }
        
        .game-preview {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            margin-bottom: 1rem;
        }
        
        .game-preview img {
            width: 100%;
            transition: transform 0.5s ease;
        }
        
        .game-preview:hover img {
            transform: scale(1.1);
        }
        
        .play-now {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%) scale(0);
            background-color: var(--secondary-color);
            color: #000;
            padding: 0.7rem 1.5rem;
            border-radius: 30px;
            font-weight: 700;
            transition: transform 0.3s ease;
            z-index: 2;
        }
        
        .game-preview:hover .play-now {
            transform: translate(-50%, -50%) scale(1);
        }
        
        .game-preview::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .game-preview:hover::after {
            opacity: 1;
        }
        
        /* Diary Section */
        .diary-section {
            background-color: #1a1a1a;
            padding: 4rem 0;
        }
        
        .diary-container {
            max-width: 800px;
            margin: 0 auto;
        }
        
        .diary-entry {
            background-color: var(--card-bg);
            padding: 2rem;
            border-radius: 10px;
            margin-bottom: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .entry-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
            padding-bottom: 1rem;
            border-bottom: 1px solid #333;
        }
        
        .entry-date {
            color: var(--secondary-color);
            font-size: 0.9rem;
            font-weight: 600;
        }
        
        .entry-title {
            margin-bottom: 1rem;
        }
        
        .entry-content {
            line-height: 1.8;
        }
        
        .entry-tags {
            display: flex;
            gap: 0.5rem;
            margin-top: 1.5rem;
            flex-wrap: wrap;
        }
        
        .tag {
            padding: 0.3rem 0.8rem;
            background-color: rgba(98, 0, 234, 0.3);
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        /* Music Section */
        .music-section {
            background: linear-gradient(135deg, #1a1a1a 0%, #303030 100%);
        }
        
        .music-container {
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        
        .spotify-embed {
            width: 100%;
            max-width: 900px;
            margin-bottom: 3rem;
        }
        
        .music-list {
            width: 100%;
            max-width: 800px;
        }
        
        .music-item {
            display: flex;
            align-items: center;
            background-color: rgba(30, 30, 30, 0.7);
            padding: 1rem;
            border-radius: 8px;
            margin-bottom: 1rem;
            transition: transform 0.3s ease;
        }
        
        .music-item:hover {
            transform: translateX(10px);
        }
        
        .music-item img {
            width: 60px;
            height: 60px;
            border-radius: 5px;
            margin-right: 1rem;
        }
        
        .music-info {
            flex-grow: 1;
        }
        
        .music-title {
            font-size: 1.1rem;
            margin-bottom: 0.2rem;
        }
        
        .music-artist {
            font-size: 0.9rem;
            color: #b0b0b0;
        }
        
        .music-play {
            color: var(--secondary-color);
            font-size: 1.5rem;
            cursor: pointer;
            transition: transform 0.3s ease;
        }
        
        .music-play:hover {
            transform: scale(1.2);
        }
        
        /* Photography Section */
        .photography-section {
            background: linear-gradient(135deg, #121212 0%, #252525 100%);
            padding: 4rem 0;
        }
        
        .gallery-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 8px;
            height: 250px;
            cursor: pointer;
        }
        
        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }
        
        .gallery-item:hover img {
            transform: scale(1.1);
        }
        
        .gallery-item::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(0,0,0,0) 50%, rgba(0,0,0,0.7) 100%);
            opacity: 0;
            transition: opacity 0.3s ease;
        }
        
        .gallery-item:hover::after {
            opacity: 1;
        }
        
        .gallery-caption {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            padding: 1rem;
            color: white;
            z-index: 1;
            opacity: 0;
            transform: translateY(20px);
            transition: opacity 0.3s ease, transform 0.3s ease;
        }
        
        .gallery-item:hover .gallery-caption {
            opacity: 1;
            transform: translateY(0);
        }
        
        .gallery-title {
            font-size: 1.1rem;
            margin: 0 0 0.2rem;
        }
        
        .gallery-location {
            font-size: 0.8rem;
            margin: 0;
            opacity: 0.8;
        }
        
        .gallery-filter {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        .filter-btn {
            padding: 0.5rem 1.2rem;
            background-color: var(--card-bg);
            border: none;
            border-radius: 5px;
            color: var(--light-text);
            cursor: pointer;
            transition: all 0.3s ease;
        }
        
        .filter-btn.active, .filter-btn:hover {
            background-color: var(--primary-color);
        }
        
        .lightbox {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.9);
            z-index: 1000;
            display: none;
            justify-content: center;
            align-items: center;
        }
        
        .lightbox.active {
            display: flex;
        }
        
        .lightbox img {
            max-width: 90%;
            max-height: 90%;
            object-fit: contain;
        }
        
        .lightbox-close {
            position: absolute;
            top: 20px;
            right: 20px;
            color: white;
            font-size: 2rem;
            cursor: pointer;
            z-index: 1001;
        }
        
        .lightbox-caption {
            position: absolute;
            bottom: 20px;
            left: 0;
            width: 100%;
            color: white;
            text-align: center;
            padding: 1rem;
        }
        
        /* Apps Section */
        .app-card {
            display: flex;
            flex-direction: column;
        }
        
        .app-features {
            margin-top: 1rem;
            padding-left: 1.5rem;
        }
        
        .app-features li {
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            color: #b0b0b0;
        }
        
        .app-store-badges {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
            flex-wrap: wrap;
        }
        
        .app-badge {
            padding: 0.5rem 1rem;
            background-color: #333;
            border-radius: 5px;
            display: flex;
            align-items: center;
            transition: background-color 0.3s ease;
        }
        
        .app-badge i {
            font-size: 1.2rem;
            margin-right: 0.5rem;
        }
        
        .app-badge:hover {
            background-color: #444;
            text-decoration: none;
        }
        
        /* Contact Section */
        .contact-section {
            background: linear-gradient(to right, #121212, #1e1e1e);
            padding: 4rem 0;
        }
        
        .contact-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
        }
        
        .contact-info {
            flex: 1;
            min-width: 300px;
        }
        
        .contact-form {
            flex: 2;
            min-width: 300px;
        }
        
        .info-item {
            display: flex;
            align-items: center;
            margin-bottom: 1.5rem;
        }
        
        .info-item i {
            width: 40px;
            height: 40px;
            background-color: var(--primary-color);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-right: 1rem;
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-control {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #333;
            background-color: rgba(30, 30, 30, 0.7);
            border-radius: 5px;
            color: white;
            font-family: var(--body-font);
        }
        
        .form-control:focus {
            outline: none;
            border-color: var(--primary-color);
        }
        
        textarea.form-control {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: #0f0f0f;
            padding: 3rem 0 1rem;
            text-align: center;
        }
        
        .footer-links {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            margin-bottom: 2rem;
            gap: 1.5rem;
        }
        
        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        .social-link {
            width: 40px;
            height: 40px;
            background-color: #333;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            transition: background-color 0.3s ease, transform 0.3s ease;
        }
        
        .social-link:hover {
            background-color: var(--primary-color);
            transform: translateY(-5px);
        }
        
        .copyright {
            font-size: 0.9rem;
            color: #777;
        }
        
        /* Game Canvas Section - For the actual games */
        .game-canvas-container {
            width: 100%;
            height: 500px;
            background-color: #000;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
            margin-bottom: 2rem;
        }
        
        #game-canvas {
            width: 100%;
            height: 100%;
        }
        
        .game-controls {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin-bottom: 2rem;
        }
        
        .game-btn {
            padding: 0.7rem 1.5rem;
            background-color: var(--primary-color);
            color: white;
            border: none;
            border-radius: 5px;
            font-weight: 600;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        
        .game-btn:hover {
            background-color: #7c4dff;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.8rem;
            }
            
            .hero h2 {
                font-size: 2rem;
            }
            
            .cards-grid {
                grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            }
            
            .contact-container {
                flex-direction: column;
            }
            
            .gallery-container {
                grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
            }
        }
        
        @media (max-width: 576px) {
            nav ul {
                flex-direction: column;
                align-items: center;
            }
            
            nav ul li {
                margin: 0.5rem 0;
            }
            
            .gallery-container {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>

<body>
    <!-- Header -->
    <header>
        <div class="container">
            <div class="header-content">
                <h1>OneLostAlien</h1>
                <p class="tagline">Games, Music, Apps, Photography & Thoughts from Another Dimension</p>
            </div>
        </div>
    </header>
    
    <!-- Navigation -->
    <nav>
        <div class="container">
            <ul>
                <li><a href="#home">Home</a></li>
                <li><a href="#games">Games</a></li>
                <li><a href="#photography">Photography</a></li>
                <li><a href="#diary">Diary</a></li>
                <li><a href="#music">Music</a></li>
                <li><a href="#apps">Apps</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>
    
    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <h2>Welcome to My Creative Universe</h2>
                <p>Explore my collection of games, photography, music, apps, and thoughts. I'm a creator passionate about bringing unique experiences to life.</p>
                <a href="#photography" class="btn">View My Photography</a>
            </div>
        </div>
    </section>
    
    <!-- Games Section -->
    <section id="games">
        <div class="container">
            <div class="section-heading">
                <h2>Mini Games</h2>
                <p>Check out these fun games I've created! Click on any game to play it right now.</p>
            </div>
            
            <div class="cards-grid">
                <!-- Game 1 -->
                <div class="card game-card">
                    <div class="game-preview">
                        <img src="/api/placeholder/400/250" alt="Space Shooter Game">
                        <a href="games/space-shooter.html" class="play-now">Play Now</a>
                    </div>
                    <div class="card-content">
                        <h3 class="card-title">Space Shooter</h3>
                        <p class="card-desc">Navigate through an asteroid field and shoot down enemy ships in this arcade-style space shooter.</p>
                        <a href="games/space-shooter.html" class="card-link">Start Game</a>
                    </div>
                </div>
                
                <!-- Game 2 -->
                <div class="card game-card">
                    <div class="game-preview">
                        <img src="/api/placeholder/400/250" alt="Puzzle Adventure Game">
                        <a href="games/puzzle-adventure.html" class="play-now">Play Now</a>
                    </div>
                    <div class="card-content">
                        <h3 class="card-title">Puzzle Adventure</h3>
                        <p class="card-desc">Solve increasingly difficult puzzles while exploring a mysterious world full of secrets.</p>
                        <a href="games/puzzle-adventure.html" class="card-link">Start Game</a>
                    </div>
                </div>
                
                <!-- Game 3 -->
                <div class="card game-card">
                    <div class="game-preview">
                        <img src="/api/placeholder/400/250" alt="Cookie Clicker Game">
                        <a href="games/cookie-clicker.html" class="play-now">Play Now</a>
                    </div>
                    <div class="card-content">
                        <h3 class="card-title">Cookie Clicker</h3>
                        <p class="card-desc">Click your way to a cookie empire! Upgrade your production and watch your cookie count rise.</p>
                        <a href="games/cookie-clicker.html" class="card-link">Start Game</a>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Photography Section -->
    <section id="photography" class="photography-section">
        <div class="container">
            <div class="section-heading">
                <h2>My Photography</h2>
                <p>Capturing moments and perspectives from around the world. Click on any image to view in full size.</p>
            </div>
            
            <div class="gallery-filter">
                <button class="filter-btn active" data-filter="all">All</button>
                <button class="filter-btn" data-filter="nature">Nature</button>
                <button class="filter-btn" data-filter="urban">Urban</button>
                <button class="filter-btn" data-filter="portrait">Portrait</button>
                <button class="filter-btn" data-filter="abstract">Abstract</button>
            </div>
            
            <div class="gallery-container">
                <!-- Photo 1 -->
                <div class="gallery-item" data-category="nature">
                    <img src="/api/placeholder/600/600" alt="Mountain Sunrise">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Mountain Sunrise</h4>
                        <p class="gallery-location">Yosemite National Park, CA</p>
                    </div>
                </div>
                
                <!-- Photo 2 -->
                <div class="gallery-item" data-category="urban">
                    <img src="/api/placeholder/600/600" alt="City Lights">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">City Lights</h4>
                        <p class="gallery-location">New York City, NY</p>
                    </div>
                </div>
                
                <!-- Photo 3 -->
                <div class="gallery-item" data-category="portrait">
                    <img src="/api/placeholder/600/600" alt="Street Musician">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Street Musician</h4>
                        <p class="gallery-location">New Orleans, LA</p>
                    </div>
                </div>
                
                <!-- Photo 4 -->
                <div class="gallery-item" data-category="abstract">
                    <img src="/api/placeholder/600/600" alt="Light Patterns">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Light Patterns</h4>
                        <p class="gallery-location">Studio Work</p>
                    </div>
                </div>
                
                <!-- Photo 5 -->
                <div class="gallery-item" data-category="nature">
                    <img src="/api/placeholder/600/600" alt="Ocean Waves">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Ocean Waves</h4>
                        <p class="gallery-location">Big Sur, CA</p>
                    </div>
                </div>
                
                <!-- Photo 6 -->
                <div class="gallery-item" data-category="urban">
                    <img src="/api/placeholder/600/600" alt="Night Market">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Night Market</h4>
                        <p class="gallery-location">Tokyo, Japan</p>
                    </div>
                </div>
                
                <!-- Photo 7 -->
                <div class="gallery-item" data-category="portrait">
                    <img src="/api/placeholder/600/600" alt="Elderly Craftsman">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Elderly Craftsman</h4>
                        <p class="gallery-location">Florence, Italy</p>
                    </div>
                </div>
                
                <!-- Photo 8 -->
                <div class="gallery-item" data-category="abstract">
                    <img src="/api/placeholder/600/600" alt="Water Reflections">
                    <div class="gallery-caption">
                        <h4 class="gallery-title">Water Reflections</h4>
                        <p class="gallery-location">Lake Tahoe, NV</p>
                    </div>
                </div>
            </div>
            
            <!-- Lightbox for images -->
            <div class="lightbox">
                <span class="lightbox-close">&times;</span>
                <img src="" alt="Enlarged Photo">
                <div class="lightbox-caption">
                    <h3 class="lightbox-title"></h3>
                    <p class="lightbox-location"></p>
                </div>
            </div>
        </div>
        
        <!-- Admin Photo Upload Section (Requires Login) -->
        <div class="container" style="margin-top: 3rem; text-align: center;">
            <h3>Admin Photo Management</h3>
            <p>Manage your photography collection through the secure admin panel.</p>
            <div id="admin-login-container">
                <button id="admin-login-btn" class="btn">Admin Login</button>
            </div>
            <div id="admin-photo-tools" style="display: none; margin-top: 1rem;">
                <input type="file" id="photo-upload" accept="image/*" style="display: none;">
                <button id="upload-photo-btn" class="btn">Upload New Photo</button>
                <button id="manage-photos-btn" class="btn" style="margin-left: 1rem; background-color: var(--primary-color);">Manage Existing Photos</button>
                <button id="admin-logout-btn" class="btn" style="margin-left: 1rem; background-color: #666;">Logout</button>
            </div>
        </div>
    </section>
    
    <!-- Diary Section -->
            <!-- Lightbox for images -->
            <div class="lightbox">
                <span class="lightbox-close">&times;</span>
                <img src="" alt="Enlarged Photo">
                <div class="lightbox-caption">
                    <h3 class="lightbox-title"></h3>
                    <p class="lightbox-location"></p>
                </div>
            </div>
        </div>
        
        <!-- Admin Photo Upload Section (Requires Login) -->
        <div class="container" style="margin-top: 3rem; text-align: center;">
            <h3>Admin Photo Management</h3>
            <p>Manage your photography collection through the secure admin panel.</p>
            <div id="admin-login-container">
                <button id="admin-login-btn" class="btn">Admin Login</button>
            </div>
            <div id="admin-photo-tools" style="display: none; margin-top: 1rem;">
                <input type="file" id="photo-upload" accept="image/*" style="display: none;">
                <button id="upload-photo-btn" class="btn">Upload New Photo</button>
                <button id="manage-photos-btn" class="btn" style="margin-left: 1rem; background-color: var(--primary-color);">Manage Existing Photos</button>
                <button id="admin-logout-btn" class="btn" style="margin-left: 1rem; background-color: #666;">Logout</button>
            </div>
        </div>
    </section>
    
    <!-- Diary Section -->
