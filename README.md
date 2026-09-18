# Ex02 Commercial Website
## Name: SHIVAA PALANIYAPPAN V
## Reg No: 212223110050
## Date: 27/08/2026

## AIM
To create a commercial website using CSS Flexbox.

## ALGORITHM
### STEP 1
Create an HTML file (index.html)

### STEP 2
Create a CSS file (style.css)

### STEP 3
Include a navigation bar with links to different sections.

### STEP 4
Add structured sections for Homepage, Products / Services, About Us, Contact Details and User Account.

### STEP 5
Include social media links at the footer with copyright information.

### STEP 6
Define global styles for fonts, colors, and layout.

### STEP 7
Style the header, navigation bar, and sections.

### STEP 8
Use Flexbox for layout design.

### STEP 9
Add hover effects and transitions for interactivity.

### STEP 10
Add Images and Media.

### STEP 11
Use optimized images for a professional look.

### STEP 12
Open the HTML file in a browser to check layout and functionality.

### STEP 13
Fix styling issues and refine content placement.

### STEP 14
Deploy the website.

### STEP 15
Upload to GitHub Pages for free hosting.

## PROGRAM
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>FreshBlend - Premium Juice & Smoothie Store</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
        }

        /* Navigation */
        .navbar {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 20px rgba(0,0,0,0.1);
        }

        .nav-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            max-width: 1200px;
            margin: 0 auto;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: bold;
            color: #F07878;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .nav-links a:hover {
            color: #F07878;
        }

        .nav-cta {
            background: linear-gradient(135deg, #F07878, #F5E373);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 25px;
            text-decoration: none;
            font-weight: bold;
            transition: transform 0.3s ease;
        }

        .nav-cta:hover {
            transform: translateY(-2px);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #ffeaa7 0%, #F5C99B 100%);
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 2rem;
            position: relative;
            overflow: hidden;
        }

        .hero-container {
            max-width: 1200px;
            margin: 0 auto;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 4rem;
            align-items: center;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            font-weight: bold;
            line-height: 1.2;
            margin-bottom: 1.5rem;
            color: #2d3436;
        }

        .hero-content .highlight {
            color: #F07878;
        }

        .hero-content p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: white;
            line-height: 1.6;
        }

        .hero-cta {
            background: linear-gradient(135deg, #F07878, #fdcb6e);
            color: white;
            padding: 1rem 2rem;
            border-radius: 30px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            display: inline-block;
            transition: all 0.3s ease;
            box-shadow: 0 8px 25px rgba(253, 121, 168, 0.3);
        }

        .hero-cta:hover {
            transform: translateY(-3px);
            box-shadow: 0 12px 35px rgba(253, 121, 168, 0.4);
        }

        .hero-visual {
            position: relative;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .product-showcase {
            position: relative;
            transform: rotate(-15deg);
        }

        .main-product {
            width: 250px;
            height: 400px;
            border-radius: 15px;
            position: relative;
        }

        .smoothie-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 15px;
        }

        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
        }

        .float-item {
            position: absolute;
            border-radius: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2rem;
        }

        .float-item:nth-child(1) {
            top: 10%;
            left: -10%;
            width: 100px;
            height: 100px;
            background: linear-gradient(45deg, #ff7675, #fd79a8);
        }

        .float-item:nth-child(2) {
            top: 60%;
            right: -10%;
            width: 100px;
            height: 100px;
            background: linear-gradient(45deg, #74b9ff, #0984e3);
        }

        .float-item:nth-child(3) {
            bottom: 20%;
            left: -10%;
            width: 80px;
            height: 80px;
            background: linear-gradient(45deg, #55a3ff, #a29bfe);
        }

        /* Products Section */
        .products {
            padding: 6rem 2rem;
            background: #f8f9fa;
        }

        .products-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .products h2 {
            text-align: center;
            font-size: 2.5rem;
            margin-bottom: 3rem;
            color: #2d3436;
        }

        /* Products Section - Flexbox Version */
        .products-flex-container {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            justify-content: center;
        }

        .product-card {
            max-width: 350px;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .product-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 20px 40px rgba(0,0,0,0.15);
        }

        .product-image {
            height: 200px;
            background: #f8f9fa;
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .product-image img {
            height: 100%;
            transition: transform 0.3s ease;
        }

        .product-card:hover .product-image img {
            transform: scale(1.1);
        }

        .product-info {
            padding: 1.5rem;
        }

        .product-info h3 {
            font-size: 1.5rem;
            margin-bottom: 0.5rem;
            color: #2d3436;
        }

        .product-info p {
            color: #636e72;
            margin-bottom: 1rem;
        }

        .product-details {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 1rem;
        }

        .price {
            font-size: 1.5rem;
            font-weight: bold;
            color: #e17055;
        }

        .calories {
            background: #ddd6fe;
            color: #7c3aed;
            padding: 0.3rem 0.8rem;
            border-radius: 15px;
            font-size: 0.9rem;
            font-weight: bold;
        }

        .add-to-cart {
            width: 100%;
            background: linear-gradient(135deg, #fd79a8, #fdcb6e);
            color: white;
            border: none;
            padding: 0.8rem;
            border-radius: 10px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .add-to-cart:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(253, 121, 168, 0.3);
        }

        /* Featured Section */
        .featured-section {
            padding: 4rem 2rem;
            background: #f8f9fa;
        }

        .featured-container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .featured-grid {
            display: grid;
            grid-template-columns: 1fr 300px 1fr;
            grid-template-rows: 200px 200px;
            gap: 1.5rem;
            height: 420px;
        }

        .featured-card {
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0,0,0,0.1);
            transition: transform 0.3s ease;
        }

        .featured-card:hover {
            transform: translateY(-5px);
        }

        .special-offer {
            grid-row: span 2;
            background: linear-gradient(135deg, #ffeaa7, #fab1a0);
            position: relative;
            display: flex;
            flex-direction: column;
        }

        .offer-badge {
            background: #ff6b6b;
            color: white;
            padding: 0.8rem;
            text-align: center;
            font-weight: bold;
            font-size: 0.9rem;
        }

        .offer-image {
            flex: 1;
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 2rem;
        }

        .offer-image img {
            width: 100%;
            height: auto;
            border-radius: 15px;
        }

        .energy-drinks {
            background: linear-gradient(135deg, #ff7675, #fd79a8);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .energy-drinks .card-content h3 {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            font-weight: normal;
        }

        .big-number {
            font-size: 4rem;
            font-weight: bold;
            line-height: 1;
            margin: 0.5rem 0;
        }

        .energy-drinks .card-content p {
            font-size: 1rem;
            opacity: 0.9;
        }

        .latest-products {
            background: linear-gradient(135deg, #ffd93d, #fdcb6e);
            display: flex;
            align-items: center;
            justify-content: center;
            position: relative;
            overflow: hidden;
        }

        .products-showcase {
            display: flex;
            align-items: center;
            justify-content: center;
            width: 100%;
            height: 100%;
        }

        .product-bottles {
            display: flex;
            gap: 1rem;
            align-items: center;
        }

        .bottle {
            font-size: 3rem;
            animation: bounce 2s ease-in-out infinite;
        }

        .bottle-1 {
            animation-delay: 0s;
        }

        .bottle-2 {
            animation-delay: 0.3s;
            font-size: 3.5rem;
        }

        .bottle-3 {
            animation-delay: 0.6s;
        }

        .our-products {
            background: linear-gradient(135deg, #74b9ff, #0984e3);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .product-label {
            font-weight: bold;
            font-size: 1.1rem;
            padding: 1rem;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar">
        <div class="nav-container">
            <div class="logo">FreshBlend</div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
            <a href="#order" class="nav-cta">Order Now</a>
        </div>
    </nav>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="hero-container">
            <div class="hero-content">
                <h1>THE FUTURE OF <span class="highlight">FRESH</span><br>DRINKS IS HERE</h1>
                <p>Experience premium quality juices and smoothies crafted with the finest ingredients. Every sip is a journey to wellness and taste perfection.</p>
                <a href="#products" class="hero-cta">Explore Menu</a>
            </div>
            <div class="hero-visual">
                <div class="product-showcase">
                    <div class="main-product">
                        <img src="bottle.png" alt="Delicious Smoothie" class="smoothie-image">
                    </div>
                </div>
                <div class="floating-elements">
                    <div class="float-item">🍓</div>
                    <div class="float-item">🥝</div>
                    <div class="float-item">🍊</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Products Section -->
    <!-- Products Section -->
<section class="products" id="products">
    <div class="products-container">
        <h2>Our Premium Selection</h2>
        <div class="products-flex-container">
            <div class="product-card">
                <div class="product-image">
                    <img src="mango.png" alt="Tropical Mango Blast">
                </div>
                <div class="product-info">
                    <h3>Tropical Mango Blast</h3>
                    <p>Fresh mangoes blended with coconut milk and a hint of lime. Pure tropical paradise in every sip.</p>
                    <div class="product-details">
                        <span class="price">$8.99</span>
                        <span class="calories">180 cal</span>
                    </div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <img src="strawberry.png" alt="Strawberry Dream">
                </div>
                <div class="product-info">
                    <h3>Strawberry Dream</h3>
                    <p>Organic strawberries with Greek yogurt and honey. A creamy delight packed with antioxidants.</p>
                    <div class="product-details">
                        <span class="price">$7.49</span>
                        <span class="calories">145 cal</span>
                    </div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <img src="green.png" alt="Green Detox Power">
                </div>
                <div class="product-info">
                    <h3>Green Detox Power</h3>
                    <p>Spinach, apple, cucumber, and ginger. The ultimate cleansing smoothie for health enthusiasts.</p>
                    <div class="product-details">
                        <span class="price">$9.99</span>
                        <span class="calories">95 cal</span>
                    </div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <img src="blueberry.png" alt="Blueberry Antioxidant">
                </div>
                <div class="product-info">
                    <h3>Blueberry Antioxidant</h3>
                    <p>Mixed berries with acai and banana. Superfood smoothie for brain health and energy boost.</p>
                    <div class="product-details">
                        <span class="price">$8.79</span>
                        <span class="calories">165 cal</span>
                    </div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <img src="orange.png" alt="Citrus Energy Boost">
                </div>
                <div class="product-info">
                    <h3>Citrus Energy Boost</h3>
                    <p>Fresh oranges, lemon, and ginger with a splash of turmeric. Natural energy in a glass.</p>
                    <div class="product-details">
                        <span class="price">$6.99</span>
                        <span class="calories">120 cal</span>
                    </div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>

            <div class="product-card">
                <div class="product-image">
                    <img src="bottle.png" alt="Grape Rejuvenator">
                </div>
                <div class="product-info">
                    <h3>Grape Rejuvenator</h3>
                    <p>Purple grapes with pomegranate and chia seeds. Rich in resveratrol and natural antioxidants.</p>
                    <div class="product-details">
                        <span class="price">$7.99</span>
                        <span class="calories">155 cal</span>
                    </div>
                    <button class="add-to-cart">Add to Cart</button>
                </div>
            </div>
        </div>
    </div>
</section>
<footer style="background-color: #222; color: #fff; text-align: center; padding: 20px 10px;">
  <p>&copy; 2025 Vanisha Ramesh 212222040174. All rights reserved.</p>
</footer>

</body>
</html>
```

## OUTPUT
![image](https://github.com/user-attachments/assets/833c709d-cdcb-4cfe-84f1-6f32b6578b0b)

![image](https://github.com/user-attachments/assets/c1c7495a-bbb2-417b-8d69-bc1f3151d573)



## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
