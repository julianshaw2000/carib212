<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Carib212 • Luxury Ocho Rios Apartment with Spectacular Sea Views</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;500;600;700;800&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        :root {
            --caribbean-blue: #006B8F;
            --turquoise: #00B4D8;
            --coral: #FF6B6B;
            --sand: #F4E8D8;
            --cream: #FAF7F2;
            --deep-sea: #003049;
            --gold: #D4A574;
            --white: #FFFFFF;
            --text-dark: #1A1A1A;
            --text-light: #666666;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'DM Sans', sans-serif;
            color: var(--text-dark);
            line-height: 1.7;
            overflow-x: hidden;
            background: var(--cream);
        }

        /* Smooth Scrolling */
        html {
            scroll-behavior: smooth;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(20px);
            padding: 1.5rem 0;
            border-bottom: 1px solid rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
        }

        nav.scrolled {
            padding: 1rem 0;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.05);
        }

        .nav-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 3rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Playfair Display', serif;
            font-size: 2rem;
            font-weight: 700;
            color: var(--caribbean-blue);
            letter-spacing: -0.02em;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 3rem;
            list-style: none;
            align-items: center;
        }

        .nav-links a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            font-size: 0.95rem;
            position: relative;
            transition: color 0.3s ease;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--caribbean-blue);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--caribbean-blue);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .cta-button {
            background: var(--caribbean-blue);
            color: white;
            padding: 0.75rem 1.75rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .cta-button:hover {
            background: var(--deep-sea);
            transform: translateY(-2px);
            box-shadow: 0 8px 20px rgba(0, 107, 143, 0.3);
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;
            background: linear-gradient(135deg, var(--caribbean-blue) 0%, var(--turquoise) 100%);
            padding: 8rem 0 4rem;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background:
                radial-gradient(circle at 20% 50%, rgba(255, 255, 255, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 80% 80%, rgba(255, 255, 255, 0.05) 0%, transparent 50%);
            animation: pulse 8s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }

        .hero-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 3rem;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
            position: relative;
            z-index: 1;
        }

        .hero-content {
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(40px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero-subtitle {
            color: rgba(255, 255, 255, 0.9);
            font-size: 1.1rem;
            font-weight: 500;
            letter-spacing: 0.1em;
            text-transform: uppercase;
            margin-bottom: 1.5rem;
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero-title {
            font-family: 'Playfair Display', serif;
            font-size: 4.5rem;
            font-weight: 800;
            color: white;
            line-height: 1.1;
            margin-bottom: 1.5rem;
            animation: fadeInUp 1s ease-out 0.3s both;
        }

        .hero-description {
            font-size: 1.25rem;
            color: rgba(255, 255, 255, 0.95);
            margin-bottom: 2.5rem;
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .hero-buttons {
            display: flex;
            gap: 1.5rem;
            animation: fadeInUp 1s ease-out 0.5s both;
        }

        .primary-button {
            background: white;
            color: var(--caribbean-blue);
            padding: 1rem 2.5rem;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.05rem;
            transition: all 0.3s ease;
            display: inline-block;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
        }

        .primary-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(0, 0, 0, 0.2);
        }

        .secondary-button {
            background: transparent;
            color: white;
            padding: 1rem 2.5rem;
            border: 2px solid white;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.05rem;
            transition: all 0.3s ease;
            display: inline-block;
        }

        .secondary-button:hover {
            background: white;
            color: var(--caribbean-blue);
            transform: translateY(-3px);
        }

        .hero-image {
            position: relative;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .hero-image-wrapper {
            position: relative;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 30px 80px rgba(0, 0, 0, 0.3);
            transform: perspective(1000px) rotateY(-5deg);
            transition: transform 0.5s ease;
        }

        .hero-image-wrapper:hover {
            transform: perspective(1000px) rotateY(0deg);
        }

        .hero-image-wrapper img {
            width: 100%;
            height: 600px;
            object-fit: cover;
            display: block;
        }

        /* Features Strip */
        .features-strip {
            background: var(--deep-sea);
            padding: 2rem 0;
            position: relative;
        }

        .features-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 3rem;
            display: flex;
            justify-content: space-around;
            gap: 3rem;
        }

        .feature-item {
            display: flex;
            align-items: center;
            gap: 1rem;
            color: white;
        }

        .feature-icon {
            font-size: 2rem;
        }

        .feature-text h4 {
            font-weight: 600;
            font-size: 1.1rem;
            margin-bottom: 0.25rem;
        }

        .feature-text p {
            font-size: 0.9rem;
            opacity: 0.8;
        }

        /* Section Styles */
        section {
            padding: 8rem 0;
        }

        .section-container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 0 3rem;
        }

        .section-header {
            text-align: center;
            margin-bottom: 5rem;
        }

        .section-subtitle {
            color: var(--caribbean-blue);
            font-size: 0.95rem;
            font-weight: 600;
            letter-spacing: 0.15em;
            text-transform: uppercase;
            margin-bottom: 1rem;
        }

        .section-title {
            font-family: 'Playfair Display', serif;
            font-size: 3.5rem;
            font-weight: 700;
            color: var(--text-dark);
            line-height: 1.2;
        }

        /* Adventures Section */
        .adventures-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 2.5rem;
        }

        .adventure-card {
            background: white;
            border-radius: 16px;
            overflow: hidden;
            transition: all 0.4s ease;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
        }

        .adventure-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.15);
        }

        .adventure-image {
            height: 280px;
            overflow: hidden;
            position: relative;
        }

        .adventure-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s ease;
        }

        .adventure-card:hover .adventure-image img {
            transform: scale(1.1);
        }

        .adventure-content {
            padding: 2rem;
        }

        .adventure-content h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.75rem;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 1rem;
        }

        .adventure-content p {
            color: var(--text-light);
            line-height: 1.7;
        }

        /* Local Guide Section */
        #local-guide {
            background: var(--sand);
        }

        .guide-intro {
            text-align: center;
            max-width: 700px;
            margin: 0 auto 4rem;
            font-size: 1.2rem;
            color: var(--text-light);
        }

        .guide-categories {
            display: grid;
            gap: 4rem;
        }

        .guide-category h3 {
            font-family: 'Playfair Display', serif;
            font-size: 2.5rem;
            font-weight: 600;
            color: var(--caribbean-blue);
            margin-bottom: 2.5rem;
            text-align: center;
        }

        .guide-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 2rem;
        }

        .guide-card {
            background: white;
            border-radius: 12px;
            overflow: hidden;
            transition: all 0.3s ease;
            box-shadow: 0 2px 15px rgba(0, 0, 0, 0.06);
        }

        .guide-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
        }

        .guide-card-image {
            height: 220px;
            overflow: hidden;
        }

        .guide-card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s ease;
        }

        .guide-card:hover .guide-card-image img {
            transform: scale(1.05);
        }

        .guide-card-content {
            padding: 1.75rem;
        }

        .guide-card-content h4 {
            font-family: 'Playfair Display', serif;
            font-size: 1.4rem;
            font-weight: 600;
            color: var(--text-dark);
            margin-bottom: 0.75rem;
        }

        .guide-card-content p {
            color: var(--text-light);
            margin-bottom: 1rem;
            font-size: 0.95rem;
        }

        .guide-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-bottom: 1rem;
        }

        .tag {
            background: var(--sand);
            color: var(--caribbean-blue);
            padding: 0.35rem 0.9rem;
            border-radius: 20px;
            font-size: 0.85rem;
            font-weight: 500;
        }

        .map-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            color: var(--caribbean-blue);
            text-decoration: none;
            font-weight: 600;
            font-size: 0.9rem;
            transition: gap 0.3s ease;
        }

        .map-link:hover {
            gap: 0.75rem;
        }

        /* Gallery Section */
        .gallery-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .gallery-item {
            position: relative;
            border-radius: 12px;
            overflow: hidden;
            cursor: pointer;
            aspect-ratio: 4/3;
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.15);
        }

        .gallery-item::after {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(to bottom, transparent 60%, rgba(0, 0, 0, 0.6));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover::after {
            opacity: 1;
        }

        /* Map Section */
        #map {
            background: var(--cream);
        }

        .map-wrapper {
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
            height: 500px;
            background: var(--caribbean-blue);
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-size: 1.2rem;
        }

        /* Booking Section */
        #booking {
            background: linear-gradient(135deg, var(--caribbean-blue) 0%, var(--deep-sea) 100%);
            color: white;
        }

        .booking-container {
            max-width: 1000px;
            margin: 0 auto;
            text-align: center;
        }

        .booking-container .section-subtitle {
            color: rgba(255, 255, 255, 0.9);
        }

        .booking-container .section-title {
            color: white;
            margin-bottom: 3rem;
        }

        .booking-options {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2.5rem;
            margin-top: 4rem;
        }

        .booking-card {
            background: rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 3rem 2rem;
            transition: all 0.3s ease;
        }

        .booking-card:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-5px);
        }

        .booking-card-icon {
            font-size: 3rem;
            margin-bottom: 1.5rem;
        }

        .booking-card h3 {
            font-family: 'Playfair Display', serif;
            font-size: 1.8rem;
            font-weight: 600;
            margin-bottom: 1rem;
        }

        .booking-card p {
            color: rgba(255, 255, 255, 0.9);
            margin-bottom: 1.5rem;
            line-height: 1.7;
        }

        .booking-card .cta-button {
            background: white;
            color: var(--caribbean-blue);
            margin-top: 1rem;
        }

        .booking-card .cta-button:hover {
            background: var(--sand);
        }

        .phone-number {
            font-weight: 600;
            font-size: 1.1rem;
            margin-top: 0.5rem;
            display: block;
        }

        /* Footer */
        footer {
            background: var(--deep-sea);
            color: white;
            padding: 3rem 0;
            text-align: center;
        }

        footer p {
            opacity: 0.8;
        }

        /* Mobile Menu Toggle */
        .menu-toggle {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--text-dark);
            cursor: pointer;
        }

        /* Responsive Design */
        @media (max-width: 1024px) {
            .hero-container {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero-title {
                font-size: 3.5rem;
            }

            .hero-buttons {
                justify-content: center;
            }

            .hero-image-wrapper {
                transform: none;
            }

            .adventures-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .guide-grid {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 768px) {
            .nav-container {
                padding: 0 1.5rem;
            }

            .menu-toggle {
                display: block;
            }

            .nav-links {
                position: fixed;
                top: 80px;
                left: 0;
                right: 0;
                background: white;
                flex-direction: column;
                padding: 2rem;
                box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
                transform: translateY(-120%);
                transition: transform 0.3s ease;
                gap: 1.5rem;
            }

            .nav-links.active {
                transform: translateY(0);
            }

            .hero {
                padding: 6rem 0 3rem;
            }

            .hero-title {
                font-size: 2.5rem;
            }

            .hero-description {
                font-size: 1.1rem;
            }

            .hero-buttons {
                flex-direction: column;
                width: 100%;
            }

            .primary-button,
            .secondary-button {
                width: 100%;
                text-align: center;
            }

            .features-container {
                flex-direction: column;
                gap: 1.5rem;
            }

            section {
                padding: 4rem 0;
            }

            .section-container {
                padding: 0 1.5rem;
            }

            .section-title {
                font-size: 2.5rem;
            }

            .adventures-grid {
                grid-template-columns: 1fr;
            }

            .guide-grid {
                grid-template-columns: 1fr;
            }

            .gallery-grid {
                grid-template-columns: 1fr;
            }

            .booking-options {
                grid-template-columns: 1fr;
            }
        }

        /* Scroll Reveal Animation */
        .reveal {
            opacity: 0;
            transform: translateY(40px);
            transition: all 0.8s ease;
        }

        .reveal.active {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav id="navbar">
        <div class="nav-container">
            <a href="#" class="logo">Carib212</a>
            <button class="menu-toggle" onclick="toggleMenu()">☰</button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#adventures">Adventures</a></li>
                <li><a href="#apartments">Apartments</a></li>
                <li><a href="#local-guide">Local Guide</a></li>
                <li><a href="#booking" class="cta-button">Book Now</a></li>
            </ul>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-container">
            <div class="hero-content">
                <div class="hero-subtitle">Ocho Rios, Jamaica</div>
                <h1 class="hero-title">Your Caribbean Paradise Awaits</h1>
                <p class="hero-description">Experience breathtaking sea views, modern luxury, and authentic Jamaican culture from your private oceanfront retreat. Perfect for remote work or the vacation of a lifetime.</p>
                <div class="hero-buttons">
                    <a href="#booking" class="primary-button">Book Your Stay</a>
                    <a href="#apartments" class="secondary-button">View Gallery</a>
                </div>
            </div>
            <div class="hero-image">
                <div class="hero-image-wrapper">
                    <img src="https://images.unsplash.com/photo-1540541338287-41700207dee6?w=800" alt="Luxury Caribbean apartment with ocean view" loading="eager">
                </div>
            </div>
        </div>
    </section>

    <!-- Features Strip -->
    <div class="features-strip">
        <div class="features-container">
            <div class="feature-item reveal">
                <div class="feature-icon">🌊</div>
                <div class="feature-text">
                    <h4>Ocean Views</h4>
                    <p>Spectacular sea panoramas</p>
                </div>
            </div>
            <div class="feature-item reveal">
                <div class="feature-icon">📶</div>
                <div class="feature-text">
                    <h4>High-Speed WiFi</h4>
                    <p>Perfect for remote work</p>
                </div>
            </div>
            <div class="feature-item reveal">
                <div class="feature-icon">🅿️</div>
                <div class="feature-text">
                    <h4>Free Parking</h4>
                    <p>Secure on-site parking</p>
                </div>
            </div>
            <div class="feature-item reveal">
                <div class="feature-icon">🏖️</div>
                <div class="feature-text">
                    <h4>Prime Location</h4>
                    <p>Minutes from attractions</p>
                </div>
            </div>
        </div>
    </div>

    <!-- Adventures Section -->
    <section id="adventures">
        <div class="section-container">
            <div class="section-header reveal">
                <div class="section-subtitle">Explore</div>
                <h2 class="section-title">Adventures Nearby</h2>
            </div>
            <div class="adventures-grid">
                <div class="adventure-card reveal">
                    <div class="adventure-image">
                        <img src="https://images.unsplash.com/photo-1559827260-dc66d52bef19?w=600" alt="Blue Hole turquoise waters">
                    </div>
                    <div class="adventure-content">
                        <h3>Blue Hole</h3>
                        <p>Discover stunning turquoise waters and hidden caves in this natural swimming paradise. An unforgettable experience in Jamaica's pristine wilderness.</p>
                    </div>
                </div>
                <div class="adventure-card reveal">
                    <div class="adventure-image">
                        <img src="https://images.unsplash.com/photo-1544551763-46a013bb70d5?w=600" alt="Dunn's River Falls cascading waterfalls">
                    </div>
                    <div class="adventure-content">
                        <h3>Dunn's River Falls</h3>
                        <p>Climb the famous terraced waterfalls and enjoy breathtaking views of one of Jamaica's most iconic natural attractions.</p>
                    </div>
                </div>
                <div class="adventure-card reveal">
                    <div class="adventure-image">
                        <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=600" alt="Chukka Park adventure activities">
                    </div>
                    <div class="adventure-content">
                        <h3>Chukka Park Rides</h3>
                        <p>Experience thrilling zipline rides, ATV adventures, and outdoor activities at Jamaica's premier adventure park.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Local Guide Section -->
    <section id="local-guide">
        <div class="section-container">
            <div class="section-header reveal">
                <div class="section-subtitle">Insider Tips</div>
                <h2 class="section-title">Local Guide</h2>
            </div>
            <p class="guide-intro reveal">Julian's handpicked recommendations for authentic Jamaican food, pristine beaches, and vibrant reggae culture around Ocho Rios</p>

            <div class="guide-categories">
                <!-- Food & Markets -->
                <div class="guide-category reveal">
                    <h3>Food & Markets</h3>
                    <div class="guide-grid">
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1544025162-d76694265947?w=400" alt="Miss T's Kitchen">
                            </div>
                            <div class="guide-card-content">
                                <h4>Miss T's Kitchen</h4>
                                <p>Authentic Jamaican breakfast in a lush garden setting. Experience true local flavors with traditional dishes.</p>
                                <a href="https://maps.app.goo.gl/nnVfbEAgZMKZTuDh6" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1615485290382-441e4d049cb5?w=400" alt="Atkins Fish Pot">
                            </div>
                            <div class="guide-card-content">
                                <h4>Atkins Fish Pot</h4>
                                <p>Best fresh fish in Ocho Rios, located right next to the scenic White River. A local favorite.</p>
                                <a href="https://maps.app.goo.gl/thSfXZENqYRfgYih6" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1488459716781-31db52582fe9?w=400" alt="Organic Farmers Market">
                            </div>
                            <div class="guide-card-content">
                                <h4>Friday's Farmers Market</h4>
                                <p>Laid-back organic market with fresh fruit, coconuts & herbal remedies. Best before 1:00 PM.</p>
                                <div class="guide-tags">
                                    <span class="tag">Fresh Fruit</span>
                                    <span class="tag">Coconuts</span>
                                    <span class="tag">Herbs</span>
                                </div>
                                <a href="https://maps.app.goo.gl/GBjWXY9ptmndi8wL9" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1571574621004-4e3e7e4e3e5c?w=400" alt="Spiritual Coconuts">
                            </div>
                            <div class="guide-card-content">
                                <h4>Spiritual Coconuts</h4>
                                <p>Fresh coconut water and traditional herbal remedies for all ailments. A wellness oasis.</p>
                                <a href="https://maps.app.goo.gl/dsQyjhKZzUxQumyq6" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Dining -->
                <div class="guide-category reveal">
                    <h3>Dining</h3>
                    <div class="guide-grid">
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?w=400" alt="Ciao Bella Art Cafe">
                            </div>
                            <div class="guide-card-content">
                                <h4>Ciao Bella Art Cafe</h4>
                                <p>Italian comfort food, brunch & art vibe at Taj Mahal Plaza. Perfect for a relaxed meal with great atmosphere.</p>
                                <a href="https://www.google.com/maps/search/?api=1&query=Ciao+Bella+Art+Cafe+%26+Restaurant+Ocho+Rios" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1559339352-11d035aa65de?w=400" alt="Margaritaville">
                            </div>
                            <div class="guide-card-content">
                                <h4>Margaritaville</h4>
                                <p>Beach-club vibe with pool & nightlife. Tourist-friendly fun with great food and drinks by the sea.</p>
                                <a href="https://maps.app.goo.gl/gvA6b14och2jEozi6" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- Live Reggae & Nightlife -->
                <div class="guide-category reveal">
                    <h3>Live Reggae & Nightlife</h3>
                    <div class="guide-grid">
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1514320291840-2e0a9bf2a9ae?w=400" alt="Ocean's 11">
                            </div>
                            <div class="guide-card-content">
                                <h4>Ocean's 11</h4>
                                <p>Local legend on the waterfront with frequent live reggae & karaoke nights. Authentic Jamaican vibes and energy.</p>
                                <a href="https://maps.app.goo.gl/E73MYjyt2ZveB7e16" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                        <div class="guide-card">
                            <div class="guide-card-image">
                                <img src="https://images.unsplash.com/photo-1563805042-7684c019e1cb?w=400" alt="Plant-Based Ice Cream">
                            </div>
                            <div class="guide-card-content">
                                <h4>Plant-Based Ice Cream</h4>
                                <p>Great vegan-friendly dessert stop after the market. Delicious, healthy treats to cool you down.</p>
                                <a href="https://maps.app.goo.gl/9CyaJK8yS277wjU38" target="_blank" class="map-link">Open in Google Maps →</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Apartments/Gallery Section -->
    <section id="apartments">
        <div class="section-container">
            <div class="section-header reveal">
                <div class="section-subtitle">Your Home Away</div>
                <h2 class="section-title">The Apartment</h2>
            </div>
            <div class="gallery-grid">
                <div class="gallery-item reveal">
                    <img src="https://images.unsplash.com/photo-1502672260266-1c1ef2d93688?w=600" alt="Living room with ocean view">
                </div>
                <div class="gallery-item reveal">
                    <img src="https://images.unsplash.com/photo-1522771739844-6a9f6d5f14af?w=600" alt="Modern kitchen">
                </div>
                <div class="gallery-item reveal">
                    <img src="https://images.unsplash.com/photo-1540518614846-7eded433c457?w=600" alt="Bedroom with sea view">
                </div>
                <div class="gallery-item reveal">
                    <img src="https://images.unsplash.com/photo-1631049307264-da0ec9d70304?w=600" alt="Balcony overlooking ocean">
                </div>
                <div class="gallery-item reveal">
                    <img src="https://images.unsplash.com/photo-1564078516393-cf04bd966897?w=600" alt="Modern bathroom">
                </div>
                <div class="gallery-item reveal">
                    <img src="https://images.unsplash.com/photo-1629079447777-1e605162dc8d?w=600" alt="Outdoor terrace">
                </div>
            </div>
        </div>
    </section>

    <!-- Map Section -->
    <section id="map">
        <div class="section-container">
            <div class="section-header reveal">
                <div class="section-subtitle">Location</div>
                <h2 class="section-title">Find Us in Paradise</h2>
            </div>
            <div class="map-wrapper reveal">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d30592.20123!2d-77.1037!3d18.4071!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8eda24c74abe7adb%3A0x2d6c5da6cdeb44c8!2sOcho%20Rios%2C%20Jamaica!5e0!3m2!1sen!2sus!4v1234567890" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
            </div>
        </div>
    </section>

    <!-- Booking Section -->
    <section id="booking">
        <div class="section-container">
            <div class="booking-container">
                <div class="section-header reveal">
                    <div class="section-subtitle">Reserve Now</div>
                    <h2 class="section-title">Book Your Stay</h2>
                </div>
                <div class="booking-options">
                    <div class="booking-card reveal">
                        <div class="booking-card-icon">📱</div>
                        <h3>WhatsApp</h3>
                        <p>Contact Julian directly for inquiries and personalized booking assistance</p>
                        <span class="phone-number">UK: +44 7448 154768</span>
                        <span class="phone-number">JM: +1 876 707-1967</span>
                        <a href="https://wa.me/447448154768" target="_blank" class="cta-button">Message on WhatsApp</a>
                    </div>
                    <div class="booking-card reveal">
                        <div class="booking-card-icon">🏠</div>
                        <h3>Airbnb</h3>
                        <p>Book instantly through Airbnb with verified reviews and secure payment</p>
                        <a href="https://airbnb.com/h/carib212.com" target="_blank" class="cta-button">Book on Airbnb</a>
                    </div>
                    <div class="booking-card reveal">
                        <div class="booking-card-icon">💳</div>
                        <h3>Pay Online</h3>
                        <p>Secure direct payment in your preferred currency (USD or JMD)</p>
                        <a href="#" class="cta-button">Pay Now</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="section-container">
            <div class="logo" style="margin-bottom: 1rem;">Carib212</div>
            <p>&copy; 2025 Carib212. All rights reserved. Your Caribbean home in Ocho Rios, Jamaica.</p>
        </div>
    </footer>

    <script>
        // Navbar scroll effect
        window.addEventListener('scroll', () => {
            const navbar = document.getElementById('navbar');
            if (window.scrollY > 50) {
                navbar.classList.add('scrolled');
            } else {
                navbar.classList.remove('scrolled');
            }
        });

        // Mobile menu toggle
        function toggleMenu() {
            const navLinks = document.getElementById('navLinks');
            navLinks.classList.toggle('active');
        }

        // Scroll reveal animation
        const reveals = document.querySelectorAll('.reveal');

        function checkReveals() {
            reveals.forEach(reveal => {
                const windowHeight = window.innerHeight;
                const revealTop = reveal.getBoundingClientRect().top;
                const revealPoint = 100;

                if (revealTop < windowHeight - revealPoint) {
                    reveal.classList.add('active');
                }
            });
        }

        window.addEventListener('scroll', checkReveals);
        checkReveals(); // Check on load

        // Smooth scroll for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                    // Close mobile menu if open
                    document.getElementById('navLinks').classList.remove('active');
                }
            });
        });
    </script>
</body>
</html>