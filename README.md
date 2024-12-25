# Ex.07 Restaurant Website
## Date: 25.12.24

## AIM:
To develop a static Restaurant website to display the food items and services provided by them.

## DESIGN STEPS:

### Step 1:
Requirement collection.

### Step 2:
Creating the layout using HTML and CSS.

### Step 3:
Updating the sample content.

### Step 4:
Choose the appropriate style and color scheme.

### Step 5:
Validate the layout in various browsers.

### Step 6:
Validate the HTML code.

### Step 7:
Publish the website in the given URL.

## PROGRAM:

index.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>La Bella Cucina - Fine Italian Dining</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html" class="active">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="administration.html">Administration</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section class="hero">
            <div class="hero-content">
                <h1>La Bella Cucina</h1>
                <p>Experience authentic Italian cuisine in an elegant atmosphere</p>
                <a href="menu.html" class="cta-button">View Our Menu</a>
            </div>
        </section>

        <section class="features">
            <div class="feature">
                <h2>Fine Dining</h2>
                <p>Experience culinary excellence with our carefully crafted dishes</p>
            </div>
            <div class="feature">
                <h2>Fresh Ingredients</h2>
                <p>We use only the finest locally sourced ingredients</p>
            </div>
            <div class="feature">
                <h2>Expert Chefs</h2>
                <p>Our master chefs bring years of experience to your table</p>
            </div>
        </section>
    </main>

    <footer>
        <p>© 2024 La Bella Cucina. Designed by Dinesh</p>
    </footer>
</body>
</html>


style.css

/* Color Scheme */
:root {
    --primary-color: #2C3639;
    --secondary-color: #A27B5C;
    --accent-color: #DCD7C9;
    --text-color: #3F4E4F;
    --white: #ffffff;
    --black: #000000;
}

/* Reset and Base Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Georgia', serif;
    line-height: 1.6;
    color: var(--text-color);
}

/* Header and Navigation */
header {
    background-color: var(--primary-color);
    padding: 1rem 0;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
}

nav ul {
    display: flex;
    justify-content: center;
    list-style: none;
    gap: 2rem;
}

nav a {
    color: var(--white);
    text-decoration: none;
    font-size: 1.1rem;
    padding: 0.5rem 1rem;
    transition: color 0.3s;
}

nav a:hover,
nav a.active {
    color: var(--accent-color);
}

/* Hero Section */
.hero {
    height: 100vh;
    background-image: url('https://images.unsplash.com/photo-1414235077428-338989a2e8c0');
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: var(--white);
    position: relative;
}

.hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background: rgba(0, 0, 0, 0.5);
}

.hero-content {
    position: relative;
    z-index: 1;
}

.hero h1 {
    font-size: 4rem;
    margin-bottom: 1rem;
}

.hero p {
    font-size: 1.5rem;
    margin-bottom: 2rem;
}

.cta-button {
    display: inline-block;
    padding: 1rem 2rem;
    background-color: var(--secondary-color);
    color: var(--white);
    text-decoration: none;
    border-radius: 5px;
    transition: background-color 0.3s;
}

.cta-button:hover {
    background-color: var(--primary-color);
}

/* Features Section */
.features {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    padding: 4rem 2rem;
    background-color: var(--accent-color);
}

.feature {
    text-align: center;
    padding: 2rem;
}

.feature h2 {
    color: var(--primary-color);
    margin-bottom: 1rem;
}

/* Menu Page */
.menu-page {
    padding: 6rem 2rem 2rem;
}

.menu-section {
    margin-bottom: 3rem;
}

.menu-items {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
    margin-top: 1rem;
}

.menu-item {
    padding: 1.5rem;
    border: 1px solid var(--accent-color);
    border-radius: 5px;
}

.menu-item h3 {
    color: var(--secondary-color);
    margin-bottom: 0.5rem;
}

.price {
    display: block;
    color: var(--primary-color);
    font-weight: bold;
    margin-top: 0.5rem;
}

/* Administration Page */
.admin-page {
    padding: 6rem 2rem 2rem;
}

.team-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.team-member {
    text-align: center;
}

.member-photo {
    width: 200px;
    height: 200px;
    border-radius: 50%;
    margin: 0 auto 1rem;
    background-size: cover;
    background-position: center;
}

/* Contact Page */
.contact-page {
    padding: 6rem 2rem 2rem;
}

.contact-info {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 2rem;
    margin-top: 2rem;
}

.contact-section {
    text-align: center;
    padding: 2rem;
    background-color: var(--accent-color);
    border-radius: 5px;
}

.contact-section h2 {
    color: var(--primary-color);
    margin-bottom: 1rem;
}

/* Footer */
footer {
    background-color: var(--primary-color);
    color: var(--white);
    text-align: center;
    padding: 1rem;
    margin-top: 2rem;
}

/* Responsive Design */
@media (max-width: 768px) {
    nav ul {
        flex-direction: column;
        align-items: center;
    }

    .hero h1 {
        font-size: 2.5rem;
    }

    .features {
        grid-template-columns: 1fr;
    }
}

admini.html


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Administration - La Bella Cucina</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="administration.html" class="active">Administration</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <main class="admin-page">
        <h1>Our Team</h1>
        
        <div class="team-grid">
            <div class="team-member">
                <div class="member-photo" style="background-image: url('CIV\ Sept\ 26.png')"></div>
                <h3>Marco Rossi</h3>
                <p>Executive Chef</p>
            </div>
            <div class="team-member">
                <div class="member-photo" style="background-image: url('download.jpeg')"></div>
                <h3>Sofia Bianchi</h3>
                <p>Restaurant Manager</p>
            </div>
            <div class="team-member">
                <div class="member-photo" style="background-image: url('nn.jpg')"></div>
                <h3>Luca Romano</h3>
                <p>Sous Chef</p>
            </div>
            <div class="team-member">
                <div class="member-photo" style="background-image: url('How_to_hire_an_Executive_Chef_.jpg')"></div>
                <h3>Isabella Conti</h3>
                <p>Pastry Chef</p>
            </div>
            <div class="team-member">
                <div class="member-photo" style="background-image: url('OIP.jpeg')"></div>
                <h3>Giuseppe Marino</h3>
                <p>Head Sommelier</p>
            </div>
            <div class="team-member">
                <div class="member-photo" style="background-image: url('chef-leaning-counter-dish-kitchen-68238659.webp')"></div>
                <h3>Elena Ferrari</h3>
                <p>Events Coordinator</p>
            </div>
        </div>
    </main>

    <footer>
        <p>© 2024 La Bella Cucina. Designed by Dinesh</p>
    </footer>
</body>
</html>


contact.html


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Us - La Bella Cucina</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="menu.html">Menu</a></li>
                <li><a href="administration.html">Administration</a></li>
                <li><a href="contact.html" class="active">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <main class="contact-page">
        <h1>Contact Us</h1>
        
        <div class="contact-info">
            <div class="contact-section">
                <h2>Location</h2>
                <p>123 Italian Street</p>
                <p>Cuisine District</p>
                <p>New York, NY 10001</p>
            </div>
            
            <div class="contact-section">
                <h2>Hours</h2>
                <p>Monday - Thursday: 5:00 PM - 10:00 PM</p>
                <p>Friday - Saturday: 5:00 PM - 11:00 PM</p>
                <p>Sunday: 4:00 PM - 9:00 PM</p>
            </div>
            
            <div class="contact-section">
                <h2>Contact</h2>
                <p>Phone: (555) 123-4567</p>
                <p>Email: info@labellacucina.com</p>
            </div>
        </div>
    </main>

    <footer>
        <p>© 2024 La Bella Cucina. Designed by Dinesh</p>
    </footer>
</body>
</html>

menu.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Menu - La Bella Cucina</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <nav>
            <ul>
                <li><a href="index.html">Home</a></li>
                <li><a href="menu.html" class="active">Menu</a></li>
                <li><a href="administration.html">Administration</a></li>
                <li><a href="contact.html">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <main class="menu-page">
        <h1>Our Menu</h1>
        
        <section class="menu-section">
            <h2>Appetizers</h2>
            <div class="menu-items">
                <div class="menu-item">
                    <h3>Bruschetta</h3>
                    <p>Toasted bread with fresh tomatoes, garlic, and basil</p>
                    <span class="price">$12</span>
                </div>
                <div class="menu-item">
                    <h3>Caprese Salad</h3>
                    <p>Fresh mozzarella, tomatoes, and basil with balsamic glaze</p>
                    <span class="price">$14</span>
                </div>
                <div class="menu-item">
                    <h3>Calamari Fritti</h3>
                    <p>Crispy fried calamari with marinara sauce</p>
                    <span class="price">$16</span>
                </div>
            </div>
        </section>

        <section class="menu-section">
            <h2>Main Courses</h2>
            <div class="menu-items">
                <div class="menu-item">
                    <h3>Fettuccine Alfredo</h3>
                    <p>Homemade pasta in creamy parmesan sauce</p>
                    <span class="price">$24</span>
                </div>
                <div class="menu-item">
                    <h3>Osso Buco</h3>
                    <p>Braised veal shanks with gremolata</p>
                    <span class="price">$32</span>
                </div>
                <div class="menu-item">
                    <h3>Risotto ai Funghi</h3>
                    <p>Creamy mushroom risotto with truffle oil</p>
                    <span class="price">$26</span>
                </div>
            </div>
        </section>

        <section class="menu-section">
            <h2>Desserts</h2>
            <div class="menu-items">
                <div class="menu-item">
                    <h3>Tiramisu</h3>
                    <p>Classic Italian coffee-flavored dessert</p>
                    <span class="price">$10</span>
                </div>
                <div class="menu-item">
                    <h3>Panna Cotta</h3>
                    <p>Vanilla cream with berry compote</p>
                    <span class="price">$9</span>
                </div>
                <div class="menu-item">
                    <h3>Cannoli</h3>
                    <p>Sicilian pastry filled with sweet ricotta</p>
                    <span class="price">$8</span>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>© 2024 La Bella Cucina. Designed by Dinesh</p>
    </footer>
</body>
</html>



## OUTPUT:

![alt text](<rest/Screenshot 2024-12-25 133738.png>)
![alt text](<rest/Screenshot 2024-12-25 133835.png>)
![alt text](<rest/Screenshot 2024-12-25 133926.png>)
![alt text](<rest/Screenshot 2024-12-25 133904.png>)
![alt text](<rest/Screenshot 2024-12-25 133912.png>)


## RESULT:
The program for designing software company website using HTML and CSS is completed successfully.
