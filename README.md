<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>IEC Group of Institutions</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background-color: #141414;
      color: #fff;
      overflow-x: hidden;
    }

    /* ---------- INTRO PAGE ---------- */
    #intro {
      position: fixed;
      top: 0; left: 0;
      width: 100%; height: 100%;
      background: black;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      text-align: center;
      z-index: 2000;
      transition: opacity 1s ease;
    }

    #intro h1 {
      font-size: 2rem;
      font-weight: 700;
      color: #e50914;
      opacity: 0;
      transform: scale(0.9);
      animation: fadeInZoom 2s forwards;
    }

    #intro p {
      margin-top: 15px;
      font-size: 1rem;
      color: #bbb;
      opacity: 0;
      animation: fadeIn 2.5s forwards;
    }

    #intro button {
      margin-top: 30px;
      background: #e50914;
      border: none;
      padding: 12px 28px;
      color: #fff;
      font-size: 1rem;
      border-radius: 6px;
      cursor: pointer;
      opacity: 0;
      animation: fadeIn 3s forwards;
      transition: background 0.3s, transform 0.3s;
    }
    #intro button:hover {
      background: #b20710;
      transform: scale(1.1);
    }

    @keyframes fadeInZoom {
      to { opacity: 1; transform: scale(1); }
    }
    @keyframes fadeIn {
      to { opacity: 1; }
    }

    /* ---------- MAIN SITE ---------- */
    #main {
      opacity: 0;
      transition: opacity 1s ease;
    }

    header {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 15px 50px;
      background-color: #000;
      position: sticky;
      top: 0;
      z-index: 1000;
    }
    header img { height: 60px; }
    nav a {
      color: #fff;
      text-decoration: none;
      margin-left: 25px;
      font-weight: 500;
      transition: color 0.3s ease, text-shadow 0.3s ease;
    }
    nav a:hover {
      color: #e50914;
      text-shadow: 0 0 8px rgba(229,9,20,0.8);
    }

    section { padding: 60px 80px; }
    h1, h2 { font-weight: 700; color: #e50914; }
    .card {
      background: #1f1f1f;
      padding: 25px;
      border-radius: 12px;
      margin-bottom: 20px;
      transition: transform 0.3s, box-shadow 0.3s;
    }
    .card:hover {
      transform: scale(1.05);
      box-shadow: 0 8px 20px rgba(229, 9, 20, 0.6);
    }

    footer {
      background: #000;
      text-align: center;
      padding: 20px;
      font-size: 14px;
      color: #aaa;
      margin-top: 40px;
    }

    /* ---------- CHATBOT ---------- */
    #chatbot {
      position: fixed;
      bottom: 20px;
      right: 20px;
      width: 350px;
      background: #1f1f1f;
      border-radius: 12px;
      overflow: hidden;
      display: none;
      flex-direction: column;
      box-shadow: 0 6px 20px rgba(0,0,0,0.8);
      z-index: 1500;
    }
    #chatbot header {
      background: #e50914;
      padding: 10px;
      color: #fff;
      text-align: center;
      font-weight: bold;
    }
    #chatbot-messages {
      height: 250px;
      overflow-y: auto;
      padding: 15px;
      font-size: 14px;
    }
    .chatbot-input { display: flex; border-top: 1px solid #333; }
    .chatbot-input input {
      flex: 1; padding: 10px;
      border: none; outline: none;
      background: #111; color: #fff;
    }
    .chatbot-input button {
      background: #e50914;
      border: none; color: #fff;
      padding: 10px 20px;
      cursor: pointer;
      transition: background 0.3s, transform 0.2s;
    }
    .chatbot-input button:hover {
      background: #b20710;
      transform: scale(1.1);
    }
    .chatbot-btn {
      position: fixed;
      bottom: 20px; right: 20px;
      background: #e50914;
      border: none; border-radius: 50%;
      width: 60px; height: 60px;
      color: #fff; font-size: 22px;
      cursor: pointer;
      box-shadow: 0 4px 12px rgba(229,9,20,0.6);
      transition: transform 0.3s;
      z-index: 1400;
    }
    .chatbot-btn:hover {
      transform: scale(1.1);
      background: #b20710;
    }

    /* Quick reply buttons */
    .quick-replies {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      padding: 10px;
      border-top: 1px solid #333;
      background: #111;
    }
    .quick-replies button {
      flex: 1;
      padding: 8px;
      font-size: 12px;
      border: none;
      border-radius: 6px;
      background: #e50914;
      color: white;
      cursor: pointer;
      transition: background 0.3s;
    }
    .quick-replies button:hover {
      background: #b20710;
    }
  </style>
</head>
<body>

  <!-- INTRO PAGE -->
  <div id="intro">
    <h1>MINI INTERNSHIP PROJECT</h1>
    <p>BY MOHAMMAD LAEEQUE ANWAR <br> BTECH CSE AI & ML | 2nd YEAR | SECTION B</p>
    <button onclick="enterSite()">Enter Site</button>
    <audio id="intro-audio" src="https://raw.githubusercontent.com/nelsondelfino/netflix-ta-dum/main/ta-dum.mp3"></audio>
  </div>

  <!-- MAIN SITE -->
  <div id="main">
    <header>
      <img src="" alt="IEC CET">
      <nav>
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#courses">Courses</a>
        <a href="#facilities">Facilities</a>
        <a href="#placements">Placements</a>
        <a href="#contact">Contact</a>
      </nav>
    </header>

    <section id="home">
      <h1>Welcome to IEC Group of Institutions</h1>
      <p>Shaping future leaders through innovation, excellence, and commitment.</p>
    </section>

    <section id="about">
      <h2>About Us</h2>
      <div class="card">
        <p>IEC Group of Institutions, established with the vision of delivering quality education, offers UG, PG, and diploma programs in Engineering, Management, Pharmacy, and more.</p>
      </div>
    </section>

    <section id="courses">
      <h2>Our Courses</h2>
      <div class="card">
        <p><strong>UG Programs:</strong> B.Tech, B.Pharm, BBA, BCA, B.Com</p>
        <p><strong>PG Programs:</strong> M.Tech, MBA, MCA, M.Pharm</p>
        <p><strong>Diploma Programs:</strong> Polytechnic & PG Diplomas</p>
      </div>
    </section>

    <section id="facilities">
      <h2>Facilities</h2>
      <div class="card">
        <p>Hostels, auditorium, library, labs, gym, cafeteria, transport, sports, Wi-Fi campus.</p>
      </div>
    </section>

    <section id="placements">
      <h2>Placements</h2>
      <div class="card">
        <p>Top recruiters: <strong>TCS, Adobe, IBM, Paytm, Infosys</strong> & more. Highest package: ₹12 LPA.</p>
      </div>
    </section>

    <section id="contact">
      <h2>Contact Us</h2>
      <div class="card">
        <p><strong>Address:</strong> IEC Group of Institutions, Greater Noida, Delhi NCR</p>
        <p><strong>Email:</strong> info@iec.edu.in</p>
        <p><strong>Phone:</strong> +91-xxxxxxxxxx</p>
      </div>
    </section>

    <footer>
      &copy; 2025 IEC Group of Institutions | All Rights Reserved
    </footer>
  </div>

  <!-- CHATBOT -->
  <button class="chatbot-btn" onclick="toggleChatbot()">💬</button>
  <div id="chatbot">
    <header>IEC Chatbot</header>
    <div id="chatbot-messages"></div>
    <div class="chatbot-input">
      <input type="text" id="chatbot-input" placeholder="Ask me anything...">
      <button onclick="sendMessage()">Send</button>
    </div>
    <div class="quick-replies">
      <button onclick="sendOption('About IEC')">About IEC</button>
      <button onclick="sendOption('Courses')">Courses</button>
      <button onclick="sendOption('Facilities')">Facilities</button>
      <button onclick="sendOption('Placements')">Placements</button>
      <button onclick="sendOption('Contact')">Contact</button>
    </div>
  </div>

  <script>
    function enterSite() {
      document.getElementById('intro-audio').play();
      const intro = document.getElementById('intro');
      const main = document.getElementById('main');
      intro.style.opacity = '0';
      setTimeout(() => {
        intro.style.display = 'none';
        main.style.opacity = '1';
      }, 1000);
    }

    function toggleChatbot() {
      const bot = document.getElementById('chatbot');
      bot.style.display = (bot.style.display === 'flex') ? 'none' : 'flex';
    }

    function sendMessage() {
      const input = document.getElementById('chatbot-input');
      processMessage(input.value);
      input.value = "";
    }

    function sendOption(option) {
      processMessage(option);
    }

    function processMessage(msg) {
      const messages = document.getElementById('chatbot-messages');
      if(msg.trim() !== "") {
        const userMsg = document.createElement('div');
        userMsg.textContent = "You: " + msg;
        messages.appendChild(userMsg);

        const botMsg = document.createElement('div');
        switch(msg.toLowerCase()) {
          case 'about iec':
            botMsg.textContent = "Bot: IEC is a premier institute in Greater Noida offering Engineering, Management, and Pharmacy programs.";
            break;
          case 'courses':
            botMsg.textContent = "Bot: We offer B.Tech, MBA, MCA, BCA, B.Pharm, M.Tech, and more.";
            break;
          case 'facilities':
            botMsg.textContent = "Bot: IEC provides hostels, labs, library, sports, cafeteria, Wi-Fi campus, and more.";
            break;
          case 'placements':
            botMsg.textContent = "Bot: Top recruiters include TCS, Infosys, Adobe, Paytm, IBM with packages up to ₹12 LPA.";
            break;
          case 'contact':
            botMsg.textContent = "Bot: Email - info@iec.edu.in | Phone: +91-xxxxxxxxxx";
            break;
          default:
            botMsg.textContent = "Bot: Thanks for asking! This is a demo chatbot.";
        }
        messages.appendChild(botMsg);

        messages.scrollTop = messages.scrollHeight;
      }
    }
  </script>
</body>
</html>
