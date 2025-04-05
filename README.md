# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Webpage</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <nav>
      <ul>
        <li><a href="#home">Home</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
  <main>
    <section id="home" class="content-section">
      <h1>Welcome to Our Website</h1>
      <p>Introduction and welcome message.</p>
    </section>
    <section id="services" class="content-section">
      <h2>Our Services</h2>
      <div class="service-grid">
        <div class="service-item">Service 1</div>
        <div class="service-item">Service 2</div>
        <div class="service-item">Service 3</div>
      </div>
    </section>
    <section id="about" class="content-section">
      <h2>About Us</h2>
      <p>Information about the company.</p>
    </section>
    <section id="contact" class="content-section">
      <h2>Contact Us</h2>
      <p>Contact information and form.</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2025 Your Company</p>
  </footer>
</body>
</html>

2. css styling
/* General Reset */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Body and Layout */
body {
  font-family: Arial, sans-serif;
  line-height: 1.6;
  background-color: #f4f4f4;
}

/* Navigation Bar */
header {
  background-color: #333;
}

nav ul {
  display: flex;
  list-style-type: none;
  justify-content: center;
  padding: 10px;
}

nav ul li {
  margin: 0 15px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
  font-size: 18px;
}

nav ul li a:hover {
  text-decoration: underline;
}

/* Main Content */
main {
  padding: 20px;
}

.content-section {
  margin-bottom: 40px;
}

h1, h2 {
  color: #333;
}

/* Services Section (Grid Layout) */
.service-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.service-item {
  background-color: #fff;
  padding: 20px;
  border: 1px solid #ddd;
  text-align: center;
}

/* Footer */
footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px;
}

/* Media Queries */

/* Tablet Devices */
@media (max-width: 768px) {
  nav ul {
    flex-direction: column;
  }

  .service-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Mobile Devices */
@media (max-width: 480px) {
  nav ul {
    flex-direction: column;
    align-items: center;
  }

  .service-grid {
    grid-template-columns: 1fr;
  }

  .service-item {
    margin-bottom: 20px;
  }
}

