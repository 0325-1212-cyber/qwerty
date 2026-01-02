<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Portfolio</title>
  <style>
    body {
      background-color: #ffe6f0;
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      color: #333;
    }

    .container {
      max-width: 700px;
      margin: 0 auto;
      padding: 20px;
      text-align: center;
    }

    #profilePicture {
      width: 200px;
      height: 200px;
      object-fit: cover;
      border-radius: 50%;
      margin: 20px auto;
      display: block;
      border: 4px solid #ff99cc;
    }

    h1, h2 {
      color: #cc0066;
    }

    ul {
      list-style-type: disc;
      padding-left: 20px;
      text-align: left;
      display: inline-block;
    }

    a {
      color: #cc0066;
      text-decoration: none;
    }

    a:hover {
      text-decoration: underline;
    }

    hr {
      border: none;
      border-top: 2px solid #ff99cc;
      margin: 20px 0;
    }

    /* Tabs styling */
    .tabs {
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      margin-bottom: 20px;
    }

    .tab-button {
      background: #ff99cc;
      border: none;
      padding: 10px 20px;
      margin: 5px;
      cursor: pointer;
      font-weight: bold;
      color: #fff;
      border-radius: 5px;
      transition: background 0.3s;
    }

    .tab-button:hover {
      background: #cc0066;
    }

    .tab-button.active {
      background: #cc0066;
    }

    .tab-content {
      display: none;
      animation: fadeIn 0.5s;
    }

    .tab-content.active {
      display: block;
    }

    @keyframes fadeIn {
      from {opacity: 0;}
      to {opacity: 1;}
    }

    /* Achievement image centered */
    .achievement-img {
      width: 300px;
      height: auto;
      border-radius: 10px;
      margin: 15px auto;   /* centers horizontally */
      border: 3px solid #ff99cc;
      display: block;      /* ensures centering works */
    }
  </style>
</head>
<body>
  <div class="container">
    <img id="profilePicture" src="fff.jpg" alt="Samantha Gail J. Fuentes" />

    <h1>Welcome to my Portfolio</h1>
    <p>I am <strong>Samantha Gail J. Fuentes</strong>, currently studying at Laguna State Polytechnic University taking the program Bachelor of Science in Information Technology. I live in Nagcarlan, Laguna.</p>

    <hr />

    <!-- Tabs -->
    <div class="tabs">
      <button class="tab-button active" onclick="openTab('about')">About Me</button>
      <button class="tab-button" onclick="openTab('hobbies')">Hobbies</button>
      <button class="tab-button" onclick="openTab('achievements')">Achievements</button>
      <button class="tab-button" onclick="openTab('contact')">Contact</button>
    </div>

    <!-- Tab Contents -->
    <section id="about" class="tab-content active">
      <h2>About Me</h2>
      <p>I am Samantha Gail Fuentes who is pursuing a program Bachelor of Science in Information Technology. I am passionate about coding and software development. I am interested in emerging technologies always looking forward to innovation and staying ahead in the digital landscape.</p>
    </section>

    <section id="hobbies" class="tab-content">
      <h2>Hobbies and Interests</h2>
      <ul>
        <li>Reading</li>
        <li>Singing</li>
        <li>Watching Movies</li>
      </ul>
    </section>

    <section id="achievements" class="tab-content">
      <h2>Achievements</h2>
      <p>Here are some of my proudest accomplishments:</p>
      <ul>
        <li>Cisco – Python 1</li>
        <p>
I have successfully completed Phyton Essentials 1 and gained this certificate.</p>
      </ul>
      <img class="achievement-img" src="111.jpg" alt="My Achievement Picture" />
    </section>

    <section id="contact" class="tab-content">
      <h2>Contact Me</h2>
      <p><strong>Mobile Number:</strong> 09-10-510-7325</p>
      <p><strong>Facebook:</strong> <a href="https://www.facebook.com/samanthagail.fuentes" target="_blank">Samantha Gail Javier Fuentes</a></p>
      <p><strong>Email:</strong> 0325-1212@lspu.edu.ph</p>
      <p><strong>Samantha Gail J. Fuentes</strong><br>ALL Rights Reserved © 2025</p>
    </section>
  </div>

  <script>
    function openTab(tabId) {
      document.querySelectorAll('.tab-content').forEach(tab => {
        tab.classList.remove('active');
      });

      document.querySelectorAll('.tab-button').forEach(btn => {
        btn.classList.remove('active');
      });

      document.getElementById(tabId).classList.add('active');
      event.target.classList.add('active');
    }
  </script>
</body>
</html>
