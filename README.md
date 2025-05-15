<!DOCTYPE html>
<html lang="ku" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ئەمۆر کافێ - قاوە و شیرینی</title>
    <style>
        :root {
            --primary-color: #8B5A2B;
            --secondary-color: #D2B48C;
            --accent-color: #A0522D;
            --light-color: #F5F5DC;
            --dark-color: #3E2723;
            --text-color: #4E342E;
            --white: #FFFFFF;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: var(--light-color);
            color: var(--text-color);
            line-height: 1.6;
        }
        
        header {
            background: linear-gradient(135deg, var(--primary-color), var(--dark-color));
            color: var(--white);
            padding: 1rem 0;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            position: sticky;
            top: 0;
            z-index: 100;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 2rem;
            font-weight: 700;
            display: flex;
            align-items: center;
        }
        
        .logo i {
            margin-left: 10px;
            color: var(--secondary-color);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-right: 20px;
        }
        
        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 5px 10px;
            border-radius: 4px;
        }
        
        nav ul li a:hover {
            color: var(--secondary-color);
            background-color: rgba(255, 255, 255, 0.1);
        }
        
        .hero {
            background: url('https://images.unsplash.com/photo-1445116572660-236099ec97a0?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80') no-repeat center center/cover;
            height: 500px;
            display: flex;
            align-items: center;
            position: relative;
        }
        
        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
        }
        
        .hero-content {
            position: relative;
            z-index: 1;
            color: var(--white);
            max-width: 600px;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            color: var(--secondary-color);
        }
        
        .hero p {
            font-size: 1.2rem;
            margin-bottom: 30px;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent-color);
            color: var(--white);
            padding: 12px 30px;
            border-radius: 30px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: var(--primary-color);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .section-title {
            text-align: center;
            margin: 60px 0 40px;
            font-size: 2.5rem;
            color: var(--primary-color);
            position: relative;
        }
        
        .section-title::after {
            content: '';
            display: block;
            width: 100px;
            height: 4px;
            background-color: var(--accent-color);
            margin: 15px auto;
        }
        
        .menu {
            padding: 60px 0;
            background-color: var(--white);
        }
        
        .menu-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .menu-item {
            background-color: var(--white);
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s, box-shadow 0.3s;
        }
        
        .menu-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.15);
        }
        
        .menu-item-img {
            height: 200px;
            overflow: hidden;
        }
        
        .menu-item-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .menu-item:hover .menu-item-img img {
            transform: scale(1.1);
        }
        
        .menu-item-content {
            padding: 20px;
        }
        
        .menu-item-title {
            font-size: 1.5rem;
            margin-bottom: 10px;
            color: var(--primary-color);
        }
        
        .menu-item-desc {
            color: var(--text-color);
            margin-bottom: 15px;
            font-size: 0.9rem;
        }
        
        .menu-item-price {
            font-size: 1.2rem;
            font-weight: 700;
            color: var(--accent-color);
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .add-to-cart {
            background-color: var(--secondary-color);
            color: var(--dark-color);
            padding: 8px 15px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            border: none;
        }
        
        .add-to-cart:hover {
            background-color: var(--accent-color);
            color: var(--white);
        }
        
        .about {
            padding: 60px 0;
            background-color: var(--light-color);
        }
        
        .about-content {
            display: flex;
            align-items: center;
            gap: 40px;
        }
        
        .about-img {
            flex: 1;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }
        
        .about-img img {
            width: 100%;
            height: auto;
            display: block;
        }
        
        .about-text {
            flex: 1;
        }
        
        .about-text h3 {
            font-size: 2rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .about-text p {
            margin-bottom: 15px;
        }
        
        .contact {
            padding: 60px 0;
            background-color: var(--white);
        }
        
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .contact-info {
            background-color: var(--light-color);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-info h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .contact-info p {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .contact-info i {
            margin-left: 10px;
            color: var(--accent-color);
        }
        
        .contact-form {
            background-color: var(--light-color);
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .contact-form h3 {
            font-size: 1.5rem;
            margin-bottom: 20px;
            color: var(--primary-color);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--accent-color);
            outline: none;
        }
        
        .form-group textarea {
            height: 150px;
            resize: vertical;
        }
        
        footer {
            background-color: var(--dark-color);
            color: var(--white);
            padding: 40px 0 20px;
            text-align: center;
        }
        
        .footer-content {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            margin-bottom: 30px;
        }
        
        .footer-section {
            flex: 1;
            min-width: 250px;
            margin-bottom: 20px;
        }
        
        .footer-section h3 {
            font-size: 1.3rem;
            margin-bottom: 20px;
            color: var(--secondary-color);
        }
        
        .footer-section p,
        .footer-section a {
            color: var(--light-color);
            margin-bottom: 10px;
            display: block;
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-section a:hover {
            color: var(--secondary-color);
        }
        
        .social-icons {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
        }
        
        .social-icons a {
            color: var(--white);
            background-color: var(--primary-color);
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }
        
        .social-icons a:hover {
            background-color: var(--secondary-color);
            color: var(--dark-color);
            transform: translateY(-3px);
        }
        
        .copyright {
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            padding-top: 20px;
            font-size: 0.9rem;
            color: var(--secondary-color);
        }
        
        .cart-icon {
            position: relative;
            font-size: 1.5rem;
            cursor: pointer;
        }
        
        .cart-count {
            position: absolute;
            top: -10px;
            right: -10px;
            background-color: var(--secondary-color);
            color: var(--dark-color);
            width: 20px;
            height: 20px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.7rem;
            font-weight: bold;
        }
        
        /* سەرەوخوارکردنی بۆ مۆبایل */
        @media (max-width: 768px) {
            .header-content {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 20px;
                justify-content: center;
            }
            
            .hero {
                height: 400px;
            }
            
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .about-content {
                flex-direction: column;
            }
            
            .menu-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
</head>
<body>
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">
                    ئەمۆر کافێ <i class="fas fa-coffee"></i>
                </div>
                <nav>
                    <ul>
                        <li><a href="#home">سەرەکی</a></li>
                        <li><a href="#menu">مینوو</a></li>
                        <li><a href="#about">دەربارە</a></li>
                        <li><a href="#contact">پەیوەندی</a></li>
                        <li>
                            <div class="cart-icon">
                                <i class="fas fa-shopping-cart"></i>
                                <span class="cart-count">0</span>
                            </div>
                        </li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <h1>ئەمۆر کافێ</h1>
                <p>باشترین قاوە و شیرینی لە باشترین ژینگەدا پێشکەشت دەکەین. هەموو ڕۆژێک لە کاتژمێر ٨ی بەیانی تا ١٠ی شەو.</p>
                <a href="#menu" class="btn">بینینی مینوو</a>
            </div>
        </div>
    </section>

    <section class="menu" id="menu">
        <div class="container">
            <h2 class="section-title">مینووی ئێمە</h2>
            <div class="menu-grid" id="menu-items">
                <!-- Menu items will be added dynamically by JavaScript -->
            </div>
        </div>
    </section>

    <section class="about" id="about">
        <div class="container">
            <h2 class="section-title">دەربارەی ئێمە</h2>
            <div class="about-content">
                <div class="about-img">
                    <img src="https://images.unsplash.com/photo-1555396273-367ea4eb4db5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80" alt="دەربارەی ئەمۆر کافێ">
                </div>
                <div class="about-text">
                    <h3>چیرۆکی ئەمۆر کافێ</h3>
                    <p>ئەمۆر کافێ لە ساڵی ٢٠١٠ دامەزراوە و لەم ماوەیەدا بووەتە یەکێک لە دیارترین شوێنەکانی قاوەخواردنەوە لە هەرێمەکەمان. ئێمە خۆمان قاوەکە لە باشترین دانەوەری جیهان هەڵدەبژێرین و بە پیشەگەرییەکی تایبەت دادەنێین.</p>
                    <p>هەروەها شیرینی و دەرچەکانی ئێمە بە دەستی چێشتلێنەرە پیشەگەرەکانی ئێمە دروست دەکرێن و هەموو ڕۆژێک بە تازەیی ئامادە دەکرێن.</p>
                    <p>ئامانجی ئێمە تەنها فرۆشتنی قاوە و شیرینی نییە، بەڵکو دروستکردنی ژینگەیەکی گەرم و دۆستانەیە بۆ کڕیارەکانمان کە بتوانن لە کاتی خواردنەوەی قاوەکەیان پشوو بدەن و چێژ لە کات ببینن.</p>
                </div>
            </div>
        </div>
    </section>

    <section class="contact" id="contact">
        <div class="container">
            <h2 class="section-title">پەیوەندی بە ئێمەوە</h2>
            <div class="contact-grid">
                <div class="contact-info">
                    <h3>زانیاری پەیوەندی</h3>
                    <p><i class="fas fa-map-marker-alt"></i> ناونیشان: شەقامی نەسر، هەولێر، هەرێمی کوردستان</p>
                    <p><i class="fas fa-phone"></i> تەلەفۆن: ٠٧٥٠ ١٢٣ ٤٥ ٦٧</p>
                    <p><i class="fas fa-envelope"></i> ئیمەیڵ: info@amorcafe.com</p>
                    <p><i class="fas fa-clock"></i> کاتەکانی کارکردن: ٨:٠٠ بەیانی - ١٠:٠٠ شەو (هەموو ڕۆژێک)</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                    </div>
                </div>
                <div class="contact-form">
                    <h3>نامە بنێرە</h3>
                    <form id="contactForm">
                        <div class="form-group">
                            <label for="name">ناو</label>
                            <input type="text" id="name" name="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">ئیمەیڵ</label>
                            <input type="email" id="email" name="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">نامە</label>
                            <textarea id="message" name="message" required></textarea>
                        </div>
                        <button type="submit" class="btn">ناردنی نامە</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-section">
                    <h3>ئەمۆر کافێ</h3>
                    <p>باشترین قاوە و شیرینی لە باشترین ژینگەدا پێشکەشت دەکەین. ئێمە خەڵکی قاوە و خۆشەویستیمان.</p>
                </div>
                <div class="footer-section">
                    <h3>لینکە خێراکان</h3>
                    <a href="#home">سەرەکی</a>
                    <a href="#menu">مینوو</a>
                    <a href="#about">دەربارە</a>
                    <a href="#contact">پەیوەندی</a>
                </div>
                <div class="footer-section">
                    <h3>پەیوەندیکردن</h3>
                    <p><i class="fas fa-map-marker-alt"></i> هەولێر، هەرێمی کوردستان</p>
                    <p><i class="fas fa-phone"></i> ٠٧٥٠ ١٢٣ ٤٥ ٦٧</p>
                    <p><i class="fas fa-envelope"></i> info@amorcafe.com</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; ٢٠٢٣ ئەمۆر کافێ. هەموو مافەکان پارێزراون.</p>
            </div>
        </div>
    </footer>

    <script>
        // Database for menu items
        const menuItems = [
            {
                id: 1,
                name: "ئەسپرێسۆ",
                description: "قاوەیەکی توند و ڕەوان بە تامی قاوەی تازە.",
                price: "٣٥٠٠ د.",
                image: "https://images.unsplash.com/photo-1517701550927-30cf4ba1dba5?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "قاوە"
            },
            {
                id: 2,
                name: "کاپوچینۆ",
                description: "ئەسپرێسۆ بە شیری گەرم و کەف.",
                price: "٤٠٠٠ د.",
                image: "https://images.unsplash.com/photo-1538587888044-79f13ddd7e89?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "قاوە"
            },
            {
                id: 3,
                name: "لاتێ",
                description: "ئەسپرێسۆ بە شیری گەرم و تەنیا کەمێک کەف.",
                price: "٤٠٠٠ د.",
                image: "https://images.unsplash.com/photo-1568649929103-28ffbefaca1e?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "قاوە"
            },
            {
                id: 4,
                name: "مۆکا",
                description: "ئەسپرێسۆ بە شیرەکاکاو و شیری گەرم.",
                price: "٤٥٠٠ د.",
                image: "https://images.unsplash.com/photo-1515446134809-993c501ca304?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "قاوە"
            },
            {
                id: 5,
                name: "چای",
                description: "چایەکی بەتام بە هەڵبژاردنی چایەکانی سەری زەوی.",
                price: "٢٠٠٠ د.",
                image: "https://images.unsplash.com/photo-1564890369478-c89ca6d9cde9?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "خواردنەوە"
            },
            {
                id: 6,
                name: "کرواسان",
                description: "کرواسانی پڕ بە بەهێز و خوێی.",
                price: "٣٠٠٠ د.",
                image: "https://images.unsplash.com/photo-1620146344904-097a0002d797?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "شیرینی"
            },
            {
                id: 7,
                name: "کێکی چاکۆلێت",
                description: "کێکێکی نەرم و خۆش بە چاکۆلێتی تازە.",
                price: "٤٠٠٠ د.",
                image: "https://images.unsplash.com/photo-1578985545062-69928b1d9587?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "شیرینی"
            },
            {
                id: 8,
                name: "مافین",
                description: "مافینێکی نەرم بە چاکۆلێت یان بلووبێری.",
                price: "٢٥٠٠ د.",
                image: "https://images.unsplash.com/photo-1606313564200-e75d5e30476c?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80",
                category: "شیرینی"
            }
        ];

        // Shopping cart
        let cart = [];

        // Display menu items
        const menuContainer = document.getElementById('menu-items');
        
        function displayMenuItems() {
            menuContainer.innerHTML = '';
            menuItems.forEach(item => {
                const menuItem = document.createElement('div');
                menuItem.className = 'menu-item';
                menuItem.innerHTML = `
                    <div class="menu-item-img">
                        <img src="${item.image}" alt="${item.name}">
                    </div>
                    <div class="menu-item-content">
                        <h3 class="menu-item-title">${item.name}</h3>
                        <p class="menu-item-desc">${item.description}</p>
                        <div class="menu-item-price">
                            <span>${item.price}</span>
                            <button class="add-to-cart" data-id="${item.id}">زیادکردن بۆ سەبەتە</button>
                        </div>
                    </div>
                `;
                menuContainer.appendChild(menuItem);
            });
            
            // Add event listeners to add to cart buttons
            document.querySelectorAll('.add-to-cart').forEach(button => {
                button.addEventListener('click', addToCart);
            });
        }
        
        // Add item to cart
        function addToCart(e) {
            const itemId = parseInt(e.target.getAttribute('data-id'));
            const item = menuItems.find(item => item.id === itemId);
            
            // Check if item already exists in cart
            const existingItem = cart.find(cartItem => cartItem.id === itemId);
            
            if (existingItem) {
                existingItem.quantity += 1;
            } else {
                cart.push({
                    ...item,
                    quantity: 1
                });
            }
            
            updateCartCount();
            // In a real app, you might want to show a notification here
        }
        
        // Update cart count in header
        function updateCartCount() {
            const totalItems = cart.reduce((total, item) => total + item.quantity, 0);
            document.querySelector('.cart-count').textContent = totalItems;
        }
        
        // Handle contact form submission
        const contactForm = document.getElementById('contactForm');
        contactForm.addEventListener('submit', function(e) {
            e.preventDefault();
            
            const name = document.getElementById('name').value;
            const email = document.getElementById('email').value;
            const message = document.getElementById('message').value;
            
            // In a real app, you would send this data to a server
            console.log('Form submitted:', { name, email, message });
            
            alert('سپاس بۆ نامەکەت! بەم زوانە پەیوەندیت پێوە دەکەین.');
            contactForm.reset();
        });
        
        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            displayMenuItems();
        });
    </script>
</body>
</html>
