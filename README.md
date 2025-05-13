/*CSS Layouts and Responsive Design Assignment*/
/*html*/
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Layout</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <nav class="navbar">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">About</a></li>
            <li><a href="#">Services</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
    </nav>
    <main class="content">
        <section class="hero">This is a responsive page</section>
        <section class="features">
            <div class="feature">Feature 1</div>
            <div class="feature">Feature 2</div>
            <div class="feature">Feature 3</div>
        </section>
    </main>
</body>
</html>
/*Flexbox for layout in style.css*/
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}
.navbar ul {
    display: flex;
    justify-content: space-around;
    list-style: none;
    padding: 15px;
    background-color: #333;
}

.navbar ul li a {
    color: white;
    text-decoration: none;
}

.content {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 20px;
}

.features {
    display: flex;
    justify-content: center;
    gap: 20px;
}

.feature {
    background-color: lightgray;
    padding: 20px;
    border-radius: 5px;
}
/*Using CSS Grid instead*/
.content {
    display: grid;
    grid-template-columns: 1fr;
    gap: 20px;
}

.features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    gap: 20px;
}
/*Adding responsive design with media queries*/
@media (max-width: 768px) {
    .features {
        flex-direction: column;
        align-items: center;
    }
    .navbar ul {
        flex-direction: column;
        text-align: center;
    }
}
/*Alternatively, if using Grid*/
@media (max-width: 768px) {
    .features {
        grid-template-columns: 1fr;
    }
}
