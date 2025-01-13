# Assignment: Responsive Web Design

## Objective:
Create a responsive webpage using modern CSS techniques, specifically Flexbox, Grid, and Media Queries. The goal is to ensure the webpage adapts gracefully to various screen sizes.

## Assignment Tasks

### Designing a Responsive Layout
a. Create a webpage with the following sections:

Header (including a logo and navigation links).
Main content area (with two columns: one for text content and the other for an image).
Footer (with links to social media and a copyright notice).
b. Use Flexbox to style the navigation menu in the header.
c. Use CSS Grid to structure the main content area.

### Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically.
Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns.
Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.

### Bonus

Add animations or transitions when resizing the screen.

/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    display: flex;
    justify-content: space-between;
    padding: 20px;
    background-color: #333;
    color: white;
}

header .logo {
    font-size: 24px;
}

header nav ul {
    list-style: none;
    display: flex;
    gap: 15px;
}

header nav a {
    color: white;
    text-decoration: none;
}

footer {
    text-align: center;
    background-color: #333;
    color: white;
    padding: 15px;
}

footer .social-media a {
    color: white;
    text-decoration: none;
    margin: 0 10px;
}

/* Main content styling */
main {
    padding: 20px;
}

.content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

.text {
    background-color: #f4f4f4;
    padding: 20px;
}

.image img {
    width: 100%;
    height: auto;
    border-radius: 8px;
}

/* Flexbox for navigation menu */
header nav ul {
    display: flex;
    justify-content: space-between;
    gap: 15px;
}

/* Media Queries for Responsiveness */

/* Small screens (up to 600px) */
@media (max-width: 600px) {
    header {
        flex-direction: column;
        align-items: center;
    }

    header nav ul {
        flex-direction: column;
        align-items: center;
    }

    .content {
        grid-template-columns: 1fr;
    }

    footer .social-media {
        margin-top: 10px;
    }
}

/* Medium screens (601px to 1024px) */
@media (min-width: 601px) and (max-width: 1024px) {
    header {
        flex-direction: row;
        justify-content: space-between;
    }

    .content {
        grid-template-columns: 1fr;
    }

    footer .social-media {
        margin-top: 10px;
    }
}

/* Large screens (above 1024px) */
@media (min-width: 1025px) {
    header nav ul {
        display: flex;
    }

    .content {
        grid-template-columns: 1fr 1fr;
    }
}

/* Bonus: Add transition effect for screen resizing */
* {
    transition: all 0.3s ease;
}
