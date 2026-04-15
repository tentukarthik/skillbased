<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beyond the Marksheet | Career Discovery</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            /* Replace the linear-gradient with a URL if you want a specific image */
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            background-size: cover;
            background-attachment: fixed;
            min-height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 40px 20px;
        }

        header {
            text-align: center;
            color: white;
            margin-bottom: 50px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }

        .container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            max-width: 1200px;
            width: 100%;
        }

        /* Glassmorphism Card Effect */
        .career-card {
            background: rgba(255, 255, 255, 0.15);
            backdrop-filter: blur(10px);
            -webkit-backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
            border-radius: 20px;
            padding: 30px;
            text-align: center;
            transition: transform 0.3s ease;
            color: white;
        }

        .career-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.25);
        }

        .career-icon {
            font-size: 3rem;
            margin-bottom: 15px;
        }

        .career-card h2 {
            margin-bottom: 15px;
            font-size: 1.5rem;
            letter-spacing: 1px;
        }

        .skill-btn {
            background: #ffffff;
            color: #1a2a6c;
            border: none;
            padding: 10px 20px;
            border-radius: 50px;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(0,0,0,0.2);
        }

        .skill-btn:hover {
            background: #fdbb2d;
            transform: scale(1.05);
        }

        .skills-list {
            margin-top: 20px;
            display: none; /* Hidden by default */
            text-align: left;
            background: rgba(0, 0, 0, 0.2);
            padding: 15px;
            border-radius: 10px;
            animation: fadeIn 0.5s ease;
        }

        .skills-list ul {
            list-style: none;
        }

        .skills-list li {
            margin: 8px 0;
            padding-left: 20px;
            position: relative;
        }

        .skills-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #fdbb2d;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body>

    <header>
        <h1>Beyond the Marksheet</h1>
        <p>Discover your future based on what you can <b>do</b>, not just what you've <b>scored</b>.</p>
    </header>

    <div class="container">
        <div class="career-card">
            <div class="career-icon">💻</div>
            <h2>Full Stack Developer</h2>
            <button class="skill-btn" onclick="toggleSkills('skills1')">View Required Skills</button>
            <div id="skills1" class="skills-list">
                <ul>
                    <li>JavaScript / TypeScript</li>
                    <li>React or Next.js</li>
                    <li>Database Management (SQL/NoSQL)</li>
                    <li>Problem Solving & Logic</li>
                </ul>
            </div>
        </div>

        <div class="career-card">
            <div class="career-icon">🎨</div>
            <h2>UI/UX Designer</h2>
            <button class="skill-btn" onclick="toggleSkills('skills2')">View Required Skills</button>
            <div id="skills2" class="skills-list">
                <ul>
                    <li>Figma / Adobe XD</li>
                    <li>Visual Hierarchy</li>
                    <li>User Research</li>
                    <li>Prototyping & Wireframing</li>
                </ul>
            </div>
        </div>

        <div class="career-card">
            <div class="career-icon">📊</div>
            <h2>Data Scientist</h2>
            <button class="skill-btn" onclick="toggleSkills('skills3')">View Required Skills</button>
            <div id="skills3" class="skills-list">
                <ul>
                    <li>Python / R Programming</li>
                    <li>Statistical Analysis</li>
                    <li>Machine Learning Models</li>
                    <li>Data Visualization</li>
                </ul>
            </div>
        </div>
    </div>

    <script>
        function toggleSkills(id) {
            const skillDiv = document.getElementById(id);
            const allLists = document.querySelectorAll('.skills-list');
            
            // Optional: Close other open lists when opening a new one
            allLists.forEach(list => {
                if(list.id !== id) list.style.display = 'none';
            });

            // Toggle logic
            if (skillDiv.style.display === "block") {
                skillDiv.style.display = "none";
            } else {
                skillDiv.style.display = "block";
            }
        }
    </script>
</body>
</html>
