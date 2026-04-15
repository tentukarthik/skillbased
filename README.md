<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Beyond the Marksheet</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <style>
    /* ===== BODY BACKGROUND ===== */
    body {
      margin: 0;
      font-family: Arial, sans-serif;

      background: url('https://images.unsplash.com/photo-1522202176988-66273c2fd55f') no-repeat center center/cover;

      color: white;
      text-align: center;
    }

    /* Dark overlay */
    body::before {
      content: "";
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.65);
      z-index: -1;
    }

    /* ===== HEADER ===== */
    header {
      padding: 25px;
      font-size: 30px;
      font-weight: bold;
    }

    header small {
      font-size: 16px;
      font-weight: normal;
    }

    /* ===== MAIN CONTAINER ===== */
    .container {
      margin-top: 80px;
    }

    h2 {
      margin-bottom: 20px;
    }

    /* ===== INPUT ===== */
    input {
      padding: 12px;
      width: 260px;
      border-radius: 10px;
      border: none;
      outline: none;
      font-size: 15px;
    }

    /* ===== BUTTON ===== */
    button {
      padding: 12px 20px;
      border-radius: 10px;
      border: none;
      background-color: #ff9800;
      color: white;
      font-size: 16px;
      cursor: pointer;
      margin-left: 10px;
      transition: 0.3s;
    }

    button:hover {
      background-color: #e68900;
      transform: scale(1.05);
    }

    /* ===== RESULT BOX ===== */
    .result {
      margin-top: 40px;
      padding: 25px;
      border-radius: 15px;

      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(12px);

      display: none;
      width: 80%;
      max-width: 520px;
      margin-left: auto;
      margin-right: auto;
    }

    .result h3 {
      margin-bottom: 10px;
      color: #ffd54f;
    }

    /* ===== FOOTER ===== */
    footer {
      margin-top: 60px;
      padding: 15px;
      font-size: 14px;
      opacity: 0.8;
    }

    /* ===== RESPONSIVE ===== */
    @media (max-width: 600px) {
      input {
        width: 200px;
        margin-bottom: 10px;
      }

      button {
        margin-left: 0;
        margin-top: 10px;
      }
    }
  </style>
</head>

<body>

  <!-- ===== HEADER ===== -->
  <header>
    Beyond the Marksheet 🎓 <br>
    <small>Empowering Skill-Based Career Discovery</small>
  </header>

  <!-- ===== INPUT SECTION ===== -->
  <div class="container">
    <h2>Enter Your Skill</h2>

    <input type="text" id="skillInput" placeholder="e.g., coding, design, writing">
    <br>
    <button onclick="findCareer()">Find Career</button>

    <!-- RESULT -->
    <div id="output" class="result"></div>
  </div>

  <!-- ===== FOOTER ===== -->
  <footer>
    🚀 Skill-Based Career Guidance Project | Ready for GitHub
  </footer>

  <!-- ===== JAVASCRIPT ===== -->
  <script>
    function findCareer() {
      const skill = document.getElementById("skillInput").value.toLowerCase();
      const output = document.getElementById("output");

      let result = "";

      if (skill.includes("coding") || skill.includes("programming")) {
        result = `
          <h3>Software Developer 👨‍💻</h3>
          <p><b>Skills Needed:</b> Java, Python, JavaScript</p>
          <p><b>Career Path:</b> Learn coding → Build projects → DSA → Job</p>
        `;
      } 
      else if (skill.includes("design")) {
        result = `
          <h3>UI/UX Designer 🎨</h3>
          <p><b>Skills Needed:</b> Figma, Photoshop, Creativity</p>
          <p><b>Career Path:</b> Learn tools → Build portfolio → Freelance/Job</p>
        `;
      } 
      else if (skill.includes("writing")) {
        result = `
          <h3>Content Writer ✍️</h3>
          <p><b>Skills Needed:</b> Creativity, Grammar, SEO</p>
          <p><b>Career Path:</b> Blogging → Freelancing → Full-time</p>
        `;
      } 
      else if (skill.includes("communication")) {
        result = `
          <h3>Marketing Specialist 📢</h3>
          <p><b>Skills Needed:</b> Communication, Strategy, Social Media</p>
          <p><b>Career Path:</b> Learn marketing → Campaigns → Brand growth</p>
        `;
      } 
      else if (skill.includes("management")) {
        result = `
          <h3>Business Manager 📊</h3>
          <p><b>Skills Needed:</b> Leadership, Planning, Decision Making</p>
          <p><b>Career Path:</b> BBA/MBA → Internship → Manager Role</p>
        `;
      }
      else {
        result = `
          <h3>Explore More 🌍</h3>
          <p>Try skills like coding, design, writing, communication, or management.</p>
        `;
      }

      output.innerHTML = result;
      output.style.display = "block";
    }
  </script>

</body>
</html>
