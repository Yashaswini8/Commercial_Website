# Ex02 Commercial Website
## Date:24-05-2026
## Reg No:212224220123

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
## index.html:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ex02 - Commercial Website</title>
    <link rel="stylesheet" href="style.css">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
</head>
<body>

    <header class="navbar">
        <div class="logo">Biz<span>Flex</span></div>
        <nav class="nav-links">
            <a href="#home">Home</a>
            <a href="#products">Products</a>
            <a href="#about">About Us</a>
            <a href="#contact">Contact</a>
        </nav>
        <div class="user-account">
            <a href="#account" class="btn-account"><i class="fa-solid fa-user"></i> Account</a>
        </div>
    </header>

    <section id="home" class="hero-section">
        <div class="hero-content">
            <h1>Next-Gen Solutions For Your Business</h1>
            <p>Experience seamless design, premium quality, and unparalleled performance tailored just for you.</p>
            <a href="#products" class="cta-btn">Explore Products</a>
        </div>
    </section>

    <section id="products" class="products-section">
        <h2>Our Featured Products</h2>
        <div class="product-grid">
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?auto=format&fit=crop&w=400&q=80" alt="Premium Headphones">
                <h3>Wireless Headphones</h3>
                <p class="price">$199.99</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1523275335684-37898b6baf30?auto=format&fit=crop&w=400&q=80" alt="Minimalist Watch">
                <h3>Smart Watch Elite</h3>
                <p class="price">$299.99</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1542291026-7eec264c27ff?auto=format&fit=crop&w=400&q=80" alt="Running Shoes">
                <h3>Aero Comfort Shoes</h3>
                <p class="price">$129.99</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
        </div>
    </section>

    <div class="info-wrapper">
        <section id="about" class="about-card">
            <h2>About Our Company</h2>
            <p>Founded with a vision to innovate, BizFlex delivers top-tier consumer products worldwide. We bridge the gap between structural utility and high-end aesthetics using cutting-edge manufacturing practices.</p>
        </section>

        <section id="contact" class="contact-card">
            <h2>Contact Details</h2>
            <p><i class="fa-solid fa-location-dot"></i> 123 Business Hub, Tech City, IN</p>
            <p><i class="fa-solid fa-envelope"></i> support@bizflex.com</p>
            <p><i class="fa-solid fa-phone"></i> +91 98765 43210</p>
        </section>
    </div>

    <section id="account" class="account-section">
        <div class="account-container">
            <h2>Welcome Back, User!</h2>
            <div class="account-dashboard">
                <div class="dash-item"><i class="fa-solid fa-box"></i> <p>My Orders</p></div>
                <div class="dash-item"><i class="fa-solid fa-heart"></i> <p>Wishlist</p></div>
                <div class="dash-item"><i class="fa-solid fa-gear"></i> <p>Settings</p></div>
            </div>
        </div>
    </section>

    <footer>
        <div class="footer-content">
            <p>&copy; 2026 BizFlex Commercial. All Rights Reserved.</p>
            <div class="social-links">
                <a href="#"><i class="fa-brands fa-facebook"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
                <a href="#"><i class="fa-brands fa-linkedin"></i></a>
            </div>
        </div>
    </footer>

</body>
</html>
```
## style.css:
```
/* STEP 6: Global Styles and Variables */
:root {
    --primary-color: #2563eb;
    --dark-color: #1e293b;
    --light-color: #f8fafc;
    --accent-color: #ff4757;
    --text-color: #334155;
    --transition: all 0.3s ease;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html {
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: var(--text-color);
    background-color: var(--light-color);
    line-height: 1.6;
}

/* STEP 7 & 8: Header & Navigation with Flexbox */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 5%;
    background-color: #ffffff;
    box-shadow: 0 2px 10px rgba(0,0,0,0.05);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 1.6rem;
    font-weight: 700;
    color: var(--dark-color);
}

.logo span {
    color: var(--primary-color);
}

.nav-links {
    display: flex;
    gap: 2rem;
}

.nav-links a {
    text-decoration: none;
    color: var(--text-color);
    font-weight: 500;
    transition: var(--transition);
}

/* STEP 9: Hover Effects */
.nav-links a:hover {
    color: var(--primary-color);
}

.btn-account {
    text-decoration: none;
    background-color: var(--dark-color);
    color: #fff;
    padding: 0.5rem 1.2rem;
    border-radius: 5px;
    font-weight: 500;
    transition: var(--transition);
}

.btn-account:hover {
    background-color: var(--primary-color);
}

/* Homepage / Hero Section using Flexbox */
.hero-section {
    height: 70vh;
    background: linear-gradient(rgba(30, 41, 59, 0.7), rgba(30, 41, 59, 0.8)), 
                url('https://images.unsplash.com/photo-1441986300917-64674bd600d8?auto=format&fit=crop&w=1200&q=80') no-repeat center center/cover;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    color: #fff;
    padding: 0 1rem;
}

.hero-content h1 {
    font-size: 3rem;
    margin-bottom: 1rem;
}

.hero-content p {
    font-size: 1.2rem;
    margin-bottom: 2rem;
    max-width: 600px;
    margin-left: auto;
    margin-right: auto;
}

.cta-btn {
    text-decoration: none;
    background-color: var(--primary-color);
    color: #fff;
    padding: 0.8rem 2rem;
    border-radius: 5px;
    font-weight: 600;
    transition: var(--transition);
}

.cta-btn:hover {
    background-color: #1d4ed8;
    transform: translateY(-2px);
}

/* STEP 8, 10 & 11: Products Section with Flexbox Grid */
.products-section {
    padding: 4rem 5%;
    text-align: center;
}

.products-section h2 {
    font-size: 2.2rem;
    margin-bottom: 2rem;
    color: var(--dark-color);
}

.product-grid {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 2rem;
}

.product-card {
    background: #fff;
    border-radius: 8px;
    box-shadow: 0 4px 15px rgba(0,0,0,0.05);
    padding: 1.5rem;
    width: 300px;
    flex: 1 1 300px;
    max-width: 350px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    transition: var(--transition);
}

.product-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(0,0,0,0.1);
}

.product-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 6px;
    margin-bottom: 1rem;
}

.product-card h3 {
    font-size: 1.2rem;
    color: var(--dark-color);
    margin-bottom: 0.5rem;
}

.product-card .price {
    font-size: 1.3rem;
    font-weight: 700;
    color: var(--primary-color);
    margin-bottom: 1rem;
}

.add-to-cart {
    background-color: transparent;
    border: 2px solid var(--primary-color);
    color: var(--primary-color);
    padding: 0.6rem;
    border-radius: 5px;
    font-weight: 600;
    cursor: pointer;
    transition: var(--transition);
}

.add-to-cart:hover {
    background-color: var(--primary-color);
    color: #fff;
}

/* About & Contact Wrapper Layout */
.info-wrapper {
    display: flex;
    flex-wrap: wrap;
    gap: 2rem;
    padding: 4rem 5%;
    background-color: #e2e8f0;
}

.about-card, .contact-card {
    flex: 1 1 45%;
    background: #fff;
    padding: 2.5rem;
    border-radius: 8px;
}

.info-wrapper h2 {
    margin-bottom: 1rem;
    color: var(--dark-color);
}

.contact-card p {
    margin-bottom: 0.8rem;
    display: flex;
    align-items: center;
    gap: 0.7rem;
}

.contact-card i {
    color: var(--primary-color);
}

/* User Account Area */
.account-section {
    padding: 4rem 5%;
    background: #fff;
}

.account-container {
    max-width: 600px;
    margin: 0 auto;
    text-align: center;
    border: 1px solid #e2e8f0;
    padding: 2rem;
    border-radius: 8px;
}

.account-container h2 {
    margin-bottom: 1.5rem;
}

.account-dashboard {
    display: flex;
    justify-content: space-around;
    gap: 1rem;
}

.dash-item {
    background: var(--light-color);
    padding: 1.5rem;
    border-radius: 6px;
    flex: 1;
    cursor: pointer;
    transition: var(--transition);
}

.dash-item i {
    font-size: 1.5rem;
    color: var(--primary-color);
    margin-bottom: 0.5rem;
}

.dash-item:hover {
    background: var(--dark-color);
    color: #fff;
}

/* Footer Section styling */
footer {
    background-color: var(--dark-color);
    color: #cbd5e1;
    padding: 2rem 5%;
}

.footer-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    gap: 1rem;
}

.social-links {
    display: flex;
    gap: 1.5rem;
}

.social-links a {
    color: #cbd5e1;
    font-size: 1.3rem;
    transition: var(--transition);
}

.social-links a:hover {
    color: var(--primary-color);
    transform: scale(1.1);
}

/* Responsive adjustments for smaller displays */
@media (max-width: 768px) {
    .navbar {
        flex-direction: column;
        gap: 1rem;
    }
    .footer-content {
        flex-direction: column;
        text-align: center;
    }
}
```
## OUTPUT
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/1a3f6e56-c4a9-43d5-a401-a12e632473b3" />
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/33a650d4-ecf8-4269-be09-002f81366bd0" />
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/da835ec3-9db4-4561-a7fd-00dc35783bed" />


## RESULT
The program for creating commercial website using CSS Flexbox is executed successfully.
