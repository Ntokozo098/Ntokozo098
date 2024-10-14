/* General Styles */
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
    transition: background-color 0.5s ease, color 0.5s ease;
    line-height: 1.6;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
    transition: background-color 0.5s ease;
}

.profile-header img {
    border-radius: 50%;
    width: 150px;
    height: 150px;
    margin-bottom: 20px;
    animation: fadeIn 1.5s ease;
}

button {
    background-color: #007BFF;
    color: white;
    padding: 10px 20px;
    border: none;
    cursor: pointer;
    border-radius: 5px;
    margin-top: 10px;
    animation: bounce 2s infinite;
}

button:hover {
    background-color: #0056b3;
}

.about, .skills, .projects, .dashboard {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
    transition: background-color 0.5s ease, box-shadow 0.5s ease;
}

.skills ul, .projects ul {
    list-style: none;
    padding: 0;
}

.skills ul li, .projects ul li {
    background-color: #eaeaea;
    margin: 10px 0;
    padding: 10px;
    border-radius: 5px;
    transition: background-color 0.5s ease, transform 0.3s ease;
    display: flex;
    align-items: center;
}

.skills ul li img {
    width: 40px;
    height: 40px;
    margin-right: 10px;
}

.skills ul li:hover, .projects ul li:hover {
    background-color: #d4d4d4;
    transform: scale(1.05);
}

.projects ul li a {
    text-decoration: none;
    color: #007BFF;
    transition: color 0.3s ease, font-size 0.3s ease;
}

.projects ul li a:hover {
    color: #0056b3;
    font-size: 1.1em;
    letter-spacing: 1px;
}

.dashboard img {
    width: 100%;
    height: auto;
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

footer {
    text-align: center;
    margin: 20px;
    font-size: 14px;
}

/* Light Theme Colors */
:root {
    --background-color: #f4f4f4;
    --text-color: #333;
    --card-background: #fff;
    --card-shadow: rgba(0, 0, 0, 0.1);
}

/* Dark Mode Colors */
body.dark-mode {
    background-color: #222;
    color: #f4f4f4;
}

header.dark-mode {
    background-color: #111;
}

.dark-mode .about, .dark-mode .skills, .dark-mode .projects, .dark-mode .dashboard {
    background-color: #333;
    box-shadow: 0 2px 5px rgba(255, 255, 255, 0.1);
}

.dark-mode .skills ul li, .dark-mode .projects ul li {
    background-color: #444;
}

/* Animations */
@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

@keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
        transform: translateY(0);
    }
    40% {
        transform: translateY(-10px);
    }
    60% {
        transform: translateY(-5px);
    }
}
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>Your Name - GitHub Profile</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <header>
        <div class="profile-header">
            <img src="profile-pic.jpg" alt="Profile Picture" class="profile-pic">
            <h1>Your Name</h1>
            <p>Information and Communication Technology Student | C# | ASP.NET | Python | Django | CSS | HTML</p>
        </div>
        <button id="toggle-dark-mode">Toggle Dark Mode</button>
    </header>
    
    <section class="about">
        <h2>About Me</h2>
        <p>I am currently pursuing a degree in Information and Communication Technology. My skills include C#, ASP.NET, Windows Forms, Python (Django), CSS, and HTML. I enjoy developing web and desktop applications and am continuously working to expand my knowledge in software development.</p>
    </section>

    <section class="skills">
        <h2>Skills</h2>
        <ul>
            <li>
                <img src="csharp-icon.png" alt="C# Icon"> C# (ASP.NET, Windows Forms)
            </li>
            <li>
                <img src="python-icon.png" alt="Python Icon"> Python (Django)
            </li>
            <li>
                <img src="html-icon.png" alt="HTML Icon"> HTML & CSS
            </li>
            <li>
                <img src="js-icon.png" alt="JavaScript Icon"> JavaScript (Basics)
            </li>
        </ul>
    </section>

    <section class="projects">
        <h2>Projects</h2>
        <ul>
            <li><a href="https://github.com/yourusername/project1">Project 1 - Web Application</a></li>
            <li><a href="https://github.com/yourusername/project2">Project 2 - Desktop Application</a></li>
            <li><a href="https://github.com/yourusername/project3">Project 3 - Django Project</a></li>
        </ul>
    </section>

    <section class="dashboard">
        <h2>Dashboard</h2>
        <img src="dashboard-example.png" alt="Dashboard Example">
    </section>

    <footer>
        <p>&copy; 2024 Your Name | <a href="mailto:youremail@example.com">youremail@example.com</a> | <a href="https://github.com/yourusername">GitHub</a></p>
    </footer>

    <script src="script.js"></script>
</body>
</html>
// Toggle dark mode
const toggleDarkMode = document.getElementById('toggle-dark-mode');
toggleDarkMode.addEventListener('click', function () {
    document.body.classList.toggle('dark-mode');
});
