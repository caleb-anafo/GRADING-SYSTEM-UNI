<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Discover Ghana - Land of Culture & Adventure</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #006B36;
            --secondary: #FCD116;
            --accent: #CE1126;
            --light: #FAFAFA;
            --dark: #333333;
            --text: #444444;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            color: var(--text);
            line-height: 1.6;
            background-color: var(--light);
        }

        h1, h2, h3, h4 {
            font-family: 'Playfair Display', serif;
            color: var(--dark);
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        header {
            background-color: var(--primary);
            color: white;
            padding: 15px 0;
            position: fixed;
            width: 100%;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--secondary);
        }

        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }

        .nav-links {
            display: flex;
            list-style: none;
        }

        .nav-links li {
            margin-left: 30px;
        }

        .nav-links a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--secondary);
        }

        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), url('https://imgs.search.brave.com/CEzCd_bvBCXUb5eBxvewmvokqJUUji15UU62gFmt0AA/rs:fit:500:0:1:0/g:ce/aHR0cHM6Ly9tZWRp/YS5nZXR0eWltYWdl/cy5jb20vaWQvMTQ5/OTQ4NDg5Ny9waG90/by9hLWhpZ2gtYW5n/bGUtdmlldy1vZi10/aGUtaW5kZXBlbmRl/bmNlLWFyY2gtYW5k/LXRoZS1ibGFjay1z/dGFyLWdhdGUtc3Vy/bW91bnRlZC1ieS10/aGUtYmxhY2suanBn/P3M9NjEyeDYxMiZ3/PTAmaz0yMCZjPTYt/U0Z0ODVvZndSQzRt/blRlTjdrN2p5Tmo0/eFRCdmJWMVVscWtZ/c0RhbGs9') no-repeat center center/cover;
            color: white;
            display: flex;
            align-items: center;
            text-align: center;
            padding-top: 80px;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: white;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }

        .btn {
            display: inline-block;
            background-color: var(--secondary);
            color: var(--dark);
            padding: 12px 30px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }

        .btn:hover {
            background-color: var(--accent);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.2);
        }

        .section-title {
            text-align: center;
            margin: 60px 0 40px;
            font-size: 2.5rem;
            color: var(--primary);
        }

        .section-subtitle {
            text-align: center;
            margin-bottom: 50px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .attractions {
            padding: 80px 0;
        }

        .attraction-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .attraction-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            transition: transform 0.3s;
        }

        .attraction-card:hover {
            transform: translateY(-10px);
        }

        .card-image {
            height: 200px;
            overflow: hidden;
        }

        .card-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .attraction-card:hover .card-image img {
            transform: scale(1.1);
        }

        .card-content {
            padding: 20px;
        }

        .card-content h3 {
            margin-bottom: 10px;
            color: var(--primary);
        }

        .card-content p {
            margin-bottom: 15px;
            font-size: 0.9rem;
        }

        .read-more {
            color: var(--primary);
            font-weight: 600;
            text-decoration: none;
            display: inline-block;
            margin-top: 10px;
        }

        .regions {
            padding: 80px 0;
            background-color: #f9f9f9;
        }

        .region-tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .tab-btn {
            padding: 10px 20px;
            margin: 0 10px;
            background-color: white;
            border: 1px solid #ddd;
            border-radius: 5px;
            cursor: pointer;
            transition: all 0.3s;
        }

        .tab-btn:hover {
            border-color: var(--primary);
        }

        .tab-btn.active {
            background-color: var(--primary);
            color: white;
            border-color: var(--primary);
        }

        .tab-content {
            display: none;
        }

        .tab-content.active {
            display: block;
            animation: fadeIn 0.5s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .region-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        .culture-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .culture-icon {
            height: 100px;
            display: flex;
            align-items: center;
            justify-content: center;
            background-color: var(--secondary);
            color: var(--dark);
            font-size: 2.5rem;
        }

        .culture-details {
            padding: 20px;
        }

        .culture-details h4 {
            margin-bottom: 10px;
            color: var(--primary);
        }

        .visitor-info {
            padding: 80px 0;
        }

        .info-boxes {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .info-box {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            position: relative;
        }

        .info-box h3 {
            margin-bottom: 15px;
            color: var(--primary);
        }

        .info-box ul {
            list-style: none;
        }

        .info-box ul li {
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }

        .info-box ul li:before {
            content: "•";
            color: var(--secondary);
            position: absolute;
            left: 0;
            font-size: 1.5rem;
            line-height: 1;
        }

        .resources {
            padding: 80px 0;
            background-color: #f9f9f9;
        }

        .resource-cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .resource-card {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
        }

        .resource-header {
            background-color: var(--primary);
            color: white;
            padding: 15px 20px;
        }

        .resource-body {
            padding: 20px;
        }

        .resource-body ul {
            list-style: none;
        }

        .resource-body ul li {
            margin-bottom: 10px;
            padding-left: 25px;
            position: relative;
        }

        .resource-body ul li:before {
            content: "✓";
            color: var(--secondary);
            position: absolute;
            left: 0;
            font-weight: bold;
        }

        .resource-footer {
            padding: 15px 20px;
            border-top: 1px solid #eee;
            text-align: right;
        }

        .contact-section {
            padding: 80px 0;
            background-color: var(--primary);
            color: white;
        }

        .contact-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
        }

        .contact-info h3 {
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .contact-info p {
            margin-bottom: 15px;
        }

        .contact-info a {
            color: var(--secondary);
            text-decoration: none;
        }

        .contact-info a:hover {
            text-decoration: underline;
        }

        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            margin-bottom: 15px;
            border: none;
            border-radius: 5px;
            background-color: rgba(255,255,255,0.9);
        }

        .contact-form textarea {
            height: 150px;
            resize: vertical;
        }

        .contact-form .btn {
            padding: 12px 30px;
            border: none;
            cursor: pointer;
        }

        footer {
            background-color: var(--dark);
            color: white;
            padding: 50px 0 20px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-column h3 {
            color: var(--secondary);
            margin-bottom: 20px;
        }

        .footer-column ul {
            list-style: none;
        }

        .footer-column ul li {
            margin-bottom: 10px;
        }

        .footer-column ul li a {
            color: white;
            text-decoration: none;
            transition: color 0.3s;
        }

        .footer-column ul li a:hover {
            color: var(--secondary);
        }

        .social-links {
            display: flex;
            margin-top: 20px;
        }

        .social-links a {
            color: white;
            font-size: 1.2rem;
            margin-right: 15px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--secondary);
        }

        .copyright {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.1);
        }

        /* Mobile styles */
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }

            .nav-links {
                display: none;
                position: absolute;
                top: 70px;
                left: 0;
                right: 0;
                background-color: var(--primary);
                flex-direction: column;
                padding: 20px;
                box-shadow: 0 5px 10px rgba(0,0,0,0.1);
            }

            .nav-links.active {
                display: flex;
            }

            .nav-links li {
                margin: 10px 0;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .region-tabs {
                flex-direction: column;
                align-items: center;
            }

            .tab-btn {
                margin: 5px 0;
                width: 100%;
                max-width: 250px;
                text-align: center;
            }
        }

        /* Animations */
        @keyframes slideInUp {
            from {
                transform: translateY(20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        .animate {
            animation: slideInUp 0.5s ease forwards;
        }
    </style>
</head>
<body>
    <header>
        <nav class="container">
            <div class="logo">Discover Ghana</div>
            <button class="mobile-menu-btn" id="mobileMenuBtn">☰</button>
            <ul class="nav-links" id="navLinks">
                <li><a href="#attractions">Attractions</a></li>
                <li><a href="#regions">Regions</a></li>
                <li><a href="#info">Visitor Info</a></li>
                <li><a href="#resources">Resources</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h1>Discover the Rich Culture of Ghana</h1>
            <p>From vibrant festivals to breathtaking landscapes, explore Ghana's diverse regions and welcoming people</p>
            <a href="#attractions" class="btn">Explore Now</a>
        </div>
    </section>

    <section id="attractions" class="attractions">
        <div class="container">
            <h2 class="section-title">Top Tourist Attractions</h2>
            <p class="section-subtitle">Discover Ghana's most breathtaking sites that attract visitors from around the world</p>
            
            <div class="attraction-grid">
                <div class="attraction-card animate">
                    <div class="card-image">
                        <img src="https://placehold.co/600x400" alt="Cape Coast Castle, a historic slave trade fort with ocean views in Ghana" />
                    </div>
                    <div class="card-content">
                        <h3>Cape Coast Castle</h3>
                        <p>This historic castle is a poignant reminder of the transatlantic slave trade, offering powerful tours and ocean views.</p>
                        <a href="#" class="read-more">Learn More →</a>
                    </div>
                </div>
                
                <div class="attraction-card animate">
                    <div class="card-image">
                        <img src="https://placehold.co/600x400" alt="Kakum National Park canopy walkway through lush rainforest in Ghana" />
                    </div>
                    <div class="card-content">
                        <h3>Kakum National Park</h3>
                        <p>Walk among the treetops on the famous canopy walkway through this lush rainforest ecosystem.</p>
                        <a href="#" class="read-more">Learn More →</a>
                    </div>
                </div>
                
                <div class="attraction-card animate">
                    <div class="card-image">
                        <img src="https://placehold.co/600x400" alt="Mole National Park wildlife safari with elephants in northern Ghana" />
                    </div>
                    <div class="card-content">
                        <h3>Mole National Park</h3>
                        <p>Ghana's largest wildlife refuge, home to elephants, antelopes, and baboons in their natural habitat.</p>
                        <a href="#" class="read-more">Learn More →</a>
                    </div>
                </div>
                
                <div class="attraction-card animate">
                    <div class="card-image">
                        <img src="https://placehold.co/600x400" alt="Wli Waterfalls, the highest waterfalls in West Africa surrounded by lush vegetation" />
                    </div>
                    <div class="card-content">
                        <h3>Wli Waterfalls</h3>
                        <p>The highest waterfalls in West Africa, with a refreshing natural pool at the base for swimming.</p>
                        <a href="#" class="read-more">Learn More →</a>
                    </div>
                </div>
                
                <div class="attraction-card animate">
                    <div class="card-image">
                        <img src="https://placehold.co/600x400" alt="Busua Beach surfers catching waves at Ghana's premier beach destination" />
                    </div>
                    <div class="card-content">
                        <h3>Busua Beach</h3>
                        <p>Ghana's premier beach destination with golden sands, surf schools, and laid-back beach bars.</p>
                        <a href="#" class="read-more">Learn More →</a>
                    </div>
                </div>
                
                <div class="attraction-card animate">
                    <div class="card-image">
                        <img src="https://placehold.co/600x400" alt="Larabanga Mosque, Ghana's oldest mosque with Sudanic architecture" />
                    </div>
                    <div class="card-content">
                        <h3>Larabanga Mosque</h3>
                        <p>Ghana's oldest mosque and a fine example of Sudanic architecture made of mud and sticks.</p>
                        <a href="#" class="read-more">Learn More →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="regions" class="regions">
        <div class="container">
            <h2 class="section-title">Cultural Highlights by Region</h2>
            <p class="section-subtitle">Explore Ghana's rich cultural tapestry across its diverse regions</p>
            
            <div class="region-tabs">
                <div class="tab-btn active" data-tab="ashanti">Ashanti Region</div>
                <div class="tab-btn" data-tab="volta">Volta Region</div>
                <div class="tab-btn" data-tab="northern">Northern Region</div>
                <div class="tab-btn" data-tab="central">Central Region</div>
                <div class="tab-btn" data-tab="greater-accra">Greater Accra</div>
                <div class="tab-btn"  data-tab="western">Western Region</div>
                <div class="tab-btn" data-tab="eatern">Eastern Region</div>
                <div class="tab-btn" data-tab="upper east">Upper East Region</div>
                <div class="tab-btn" data-tab="uper west">Upper WEst Region</div>
                <div class="tab-btn" data-tab="brong ahafo">Brong Ahafo Region</div>
                </div>
                
            <div class="tab-content active" id="ashanti">
                <div class="region-grid">
                    <div class="culture-card">
                        <div class="culture-icon">👑</div>
                        <div class="culture-details">
                            <h4>Ashanti Kingdom</h4>
                            <p>The Ashanti Empire remains a vibrant traditional kingdom with rich history and culture.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🛍️</div>
                        <div class="culture-details">
                            <h4>Kente Cloth</h4>
                            <p>Visit Bonwire, the home of Ghana's famous handwoven Kente cloth with vibrant patterns.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🥁</div>
                        <div class="culture-details">
                            <h4>Adae Festival</h4>
                            <p>Witness this sacred Ashanti royal festival with drumming, dancing, and royal procession.</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="tab-content" id="volta">
                <div class="region-grid">
                    <div class="culture-card">
                        <div class="culture-icon">🌊</div>
                        <div class="culture-details">
                            <h4>Volta River</h4>
                            <p>Explore the massive Volta Lake and river system that shaped the region's culture.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🎭</div>
                        <div class="culture-details">
                            <h4>Ewe Culture</h4>
                            <p>Experience unique Ewe traditions including Agbadza dance and Anlo culture.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">⛰️</div>
                        <div class="culture-details">
                            <h4>Mountainous Landscapes</h4>
                            <p>Hike the lush mountains and visit traditional villages with breathtaking views.</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="tab-content" id="northern">
                <div class="region-grid">
                    <div class="culture-card">
                        <div class="culture-icon">🏰</div>
                        <div class="culture-details">
                            <h4>Dagomba Kingdom</h4>
                            <p>Discover the ancient Dagomba kingdom with its unique architectural heritage.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🐘</div>
                        <div class="culture-details">
                            <h4>Traditional Hunting</h4>
                            <p>Learn about the Gonja people's traditional elephant hunting culture and rituals.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🕌</div>
                        <div class="culture-details">
                            <h4>Islamic Influence</h4>
                            <p>Experience the strong Islamic culture in Ghana's northern regions.</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="tab-content" id="central">
                <div class="region-grid">
                    <div class="culture-card">
                        <div class="culture-icon">🎶</div>
                        <div class="culture-details">
                            <h4>Fante Culture</h4>
                            <p>The Fante people are known for their elaborate festivals and rich musical traditions.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">⛵</div>
                        <div class="culture-details">
                            <h4>Fishing Culture</h4>
                            <p>Coastal villages maintain traditional fishing methods passed down for generations.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🏛️</div>
                        <div class="culture-details">
                            <h4>Colonial History</h4>
                            <p>Explore Ghana's colonial past through the region's historic forts and castles.</p>
                        </div>
                    </div>
                </div>
            </div>
            
            <div class="tab-content" id="greater-accra">
                <div class="region-grid">
                    <div class="culture-card">
                        <div class="culture-icon">🏙️</div>
                        <div class="culture-details">
                            <h4>Modern Ghana</h4>
                            <p>The cosmopolitan capital blends modern urban culture with traditional values.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🎶</div>
                        <div class="culture-details">
                            <h4>Music Scene</h4>
                            <p>Accra is the heart of Ghana's vibrant highlife, hiplife, and afrobeats music culture.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🍽️</div>
                        <div class="culture-details">
                            <h4>Gastronomy</h4>
                            <p>Experience the best of Ghanaian cuisine from street food to fine dining.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="tab-content" id="western">
                <div class="region-grid">
                    <div class="culture-card">
                        <div class="culture-icon">🌊</div>
                        <div class="culture-details">
                            <h4>Rainforest</h4>
                            <p>Explore the massive Rainforest that shaped the region's culture.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">🎭</div>
                        <div class="culture-details">
                            <h4>Ewe Culture</h4>
                            <p>Experience unique Ewe traditions including Agbadza dance and Anlo culture.</p>
                        </div>
                    </div>
                    
                    <div class="culture-card">
                        <div class="culture-icon">⛰️</div>
                        <div class="culture-details">
                            <h4>Mountainous Landscapes</h4>
                            <p>Hike the lush mountains and visit traditional villages with breathtaking views.</p>
                        </div>
                    </div>
                </div>
            </div>
    </section>

    <section id="info" class="visitor-info">
        <div class="container">
            <h2 class="section-title">Visitor Information</h2>
            <p class="section-subtitle">Essential information for planning your Ghanaian adventure</p>
            
            <div class="info-boxes">
                <div class="info-box animate">
                    <h3>Travel Requirements</h3>
                    <ul>
                        <li>Visa requirements based on nationality</li>
                        <li>Yellow fever vaccination certificate required</li>
                        <li>Most visitors need passport valid for 6+ months</li>
                        <li>Tourist visa valid for 30-90 days depending on country</li>
                    </ul>
                </div>
                
                <div class="info-box animate">
                    <h3>Best Time to Visit</h3>
                    <ul>
                        <li>November-April: Dry season (best for wildlife viewing)</li>
                        <li>June-August: Cooler temperatures in south</li>
                        <li>Avoid heavy rains in May-June and September-October</li>
                        <li>Major festivals mostly December-January</li>
                    </ul>
                </div>
                
                <div class="info-box animate">
                    <h3>Getting Around</h3>
                    <ul>
                        <li>Domestic flights between major cities</li>
                        <li>STC and VIP intercity buses most comfortable</li>
                        <li>Taxis available in all urban areas (negotiate fares)</li>
                        <li>Self-drive possible but local driving can be chaotic</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="resources" class="resources">
        <div class="container">
            <h2 class="section-title">Tour Operator & Researcher Resources</h2>
            <p class="section-subtitle">Tools and information for professionals in the tourism industry</p>
            
            <div class="resource-cards">
                <div class="resource-card animate">
                    <div class="resource-header">
                        <h3>Tour Operators</h3>
                    </div>
                    <div class="resource-body">
                        <ul>
                            <li>Ministry of Tourism accreditation process</li>
                            <li>Licensed operator directory</li>
                            <li>Suggested itineraries for different durations</li>
                            <li>Cultural sensitivity guidelines</li>
                            <li>Guide training resources</li>
                        </ul>
                    </div>
                    <div class="resource-footer">
                        <a href="#" class="btn">Access Resources</a>
                    </div>
                </div>
                
                <div class="resource-card animate">
                    <div class="resource-header">
                        <h3>Researchers & Academics</h3>
                    </div>
                    <div class="resource-body">
                        <ul>
                            <li>Ethnic group database with contact information</li>
                            <li>Historical archives access</li>
                            <li>Research permit application process</li>
                            <li>University partnerships</li>
                            <li>Cultural preservation initiatives</li>
                        </ul>
                    </div>
                    <div class="resource-footer">
                        <a href="#" class="btn">Access Resources</a>
                    </div>
                </div>
                
                <div class="resource-card animate">
                    <div class="resource-header">
                        <h3>Local Communities</h3>
                    </div>
                    <div class="resource-body">
                        <ul>
                            <li>Community tourism development programs</li>
                            <li>Homestay network information</li>
                            <li>Artisan cooperatives</li>
                            <li>Cultural performance groups</li>
                            <li>Revenue sharing models</li>
                        </ul>
                    </div>
                    <div class="resource-footer">
                        <a href="#" class="btn">Access Resources</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="contact-section">
        <div class="container">
            <h2 class="section-title" style="color: white;">Contact Us</h2>
            <p class="section-subtitle" style="color: white;">Have questions or need more information? Get in touch with our team</p>

            <div class="contact-container">
                <div class="contact-info">
                    <h3>Ghana Tourism Authority</h3>
                    <p><strong>Address:</strong> P.O. Box 4386, Accra, Ghana</p>
                    <p><strong>Phone:</strong> <a href="tel:+233302681130">+233 30 268 1130</a></p>
                    <p><strong>Email:</strong> <a href="mailto:info@ghanatourism.gov.gh">info@ghanatourism.gov.gh</a></p>
                    <p><strong>Hours:</strong> Monday-Friday, 8:30am-5:00pm</p>
                </div>
                <div class="contact-form">
                    <form id="contactForm">
                        <input type="text" placeholder="Your Name" required>
                        <input type="email" placeholder="Your Email" required>
                        <input type="text" placeholder="Subject">
                        <textarea placeholder="Your Message" required></textarea>
                        <button type="submit" class="btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>About Ghana</h3>
                    <ul>
                        <li><a href="#">History</a></li>
                        <li><a href="#">Culture & Heritage</a></li>
                        <li><a href="#">People & Languages</a></li>
                        <li><a href="#">Geography</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Plan Your Trip</h3>
                    <ul>
                        <li><a href="#">Visas & Requirements</a></li>
                        <li><a href="#">When to Visit</a></li>
                        <li><a href="#">Getting Around</a></li>
                        <li><a href="#">Accommodation</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Resources</h3>
                    <ul>
                        <li><a href="#">Guides & Brochures</a></li>
                        <li><a href="#">Tour Operators</a></li>
                        <li><a href="#">Events Calendar</a></li>
                        <li><a href="#">Travel Advisories</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Connect</h3>
                    <div class="social-links">
                        <a href="https://facebook.com" target="_blank">FB</a>
                        <a href="https://twitter.com" target="_blank">TW</a>
                        <a href="https://instagram.com" target="_blank">IG</a>
                        <a href="https://youtube.com" target="_blank">YT</a>
                    </div>
                    <h3>Newsletter</h3>
                    <form class="newsletter-form">
                        <input type="email" placeholder="Your Email">
                        <button type="submit" class="btn">Subscribe</button>
                    </form>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 Ghana Tourism Authority. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        document.getElementById('mobileMenuBtn').addEventListener('click', function() {
            document.getElementById('navLinks').classList.toggle('active');
        });
        
        // Smooth scrolling for navigation links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                // Close mobile menu if open
                document.getElementById('navLinks').classList.remove('active');
            });
        });
        
        // Region tabs functionality
        const tabBtns = document.querySelectorAll('.tab-btn');
        const tabContents = document.querySelectorAll('.tab-content');
        
        tabBtns.forEach(btn => {
            btn.addEventListener('click', () => {
                // Remove active class from all buttons and contents
                tabBtns.forEach(btn => btn.classList.remove('active'));
                tabContents.forEach(content => content.classList.remove('active'));
                
                // Add active class to clicked button
                btn.classList.add('active');
                
                // Show corresponding content
                const tabId = btn.getAttribute('data-tab');
                document.getElementById(tabId).classList.add('active');
            });
        });
        
        // Contact form submission
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });
        
        // Newsletter form submission
        document.querySelector('.newsletter-form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for subscribing to our newsletter!');
            this.reset();
        });
        
        // Animation on scroll
        const animateElements = document.querySelectorAll('.animate');
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('fadeIn');
                }
            });
        }, {
            threshold: 0.1
        });
        
        animateElements.forEach(element => {
            observer.observe(element);
        });
    </script>
</body>
</html>
