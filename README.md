
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="The official site for $GLITCH. The memecoin that disrupts the terminal!">
  <title>Glitch Terminal - Official Site</title>
  
  <!-- Google Fonts -->
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">

  <style>
    /* General Reset */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background-color: #1a1a1a;
      color: #00ff00;
      font-family: 'Roboto', sans-serif;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 0 20px;
    }

    /* Hero Section */
    #hero {
      text-align: center;
      margin-top: 20px;
      padding: 50px;
      background: #111;
      border-radius: 15px;
      box-shadow: 0 0 20px rgba(0, 255, 0, 0.3);
      width: 100%;
      max-width: 1000px;
    }

    #hero h1 {
      font-size: 3rem;
      margin-bottom: 20px;
      text-shadow: 0 0 10px rgba(0, 255, 0, 0.7);
    }

    #hero p {
      font-size: 1.2rem;
      margin-bottom: 30px;
    }

    #ca {
      font-family: 'Roboto Mono', monospace;
      font-size: 1.5rem;
      color: #00ff00;
      animation: glitch 0.3s infinite;
    }

    @keyframes glitch {
      0% {
        text-shadow: 2px 0px red, -2px 0px blue;
      }
      50% {
        text-shadow: -2px 0px red, 2px 0px blue;
      }
      100% {
        text-shadow: 0px 0px red, 0px 0px blue;
      }
    }

    .btn {
      padding: 10px 20px;
      font-size: 1.1rem;
      background-color: #00ff00;
      color: black;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      text-decoration: none;
    }

    .btn:hover {
      background-color: #00cc00;
    }

    /* Description Section */
    #description {
      font-size: 1.2rem;
      color: lime;
      text-align: center;
      margin-top: 40px;
    }

    /* Glitch Terminal */
    #terminal {
      width: 100%;
      max-width: 1000px;
      margin-top: 20px;
      padding: 10px;
      background-color: #111;
      border: 2px solid #00ff00;
      box-shadow: 0 0 15px rgba(0, 255, 0, 0.5);
    }

    #output {
      font-size: 1rem;
      white-space: pre-wrap;
      overflow-y: auto;
      animation: glitch 0.2s infinite;
      line-height: 1.5;
    }

    /* Footer Section */
    #footer {
      margin-top: 50px;
      color: #ccc;
      text-align: center;
    }

    /* Social Links */
    .social-links a {
      color: #00ff00;
      margin: 0 10px;
      text-decoration: none;
      font-size: 1.2rem;
    }

    .social-links a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

  <!-- Hero Section -->
  <div id="hero">
    <h1>Glitch Terminal</h1>
    <p>"The memecoin that disrupts the terminal"</p>
    <p>
      Contract Address:  
      <strong id="ca">BJStdQoQv3UKuNuK6vrueBFFJmDxmuQPL6SWcQKcpump</strong>
      <br>
      <button onclick="copyCA()" class="btn" style="margin-top: 10px;">Copy CA</button>
    </p>
    <a href="https://pump.fun/BJStdQoQv3UKuNuK6vrueBFFJmDxmuQPL6SWcQKcpump" class="btn">BUY $GLITCH</a>
  </div>

  <!-- Description -->
  <div id="description">
    <p>Welcome to the official site for $GLITCH. Get ready to decode the truth hidden in the glitches of reality.</p>
  </div>

  <!-- Glitch Terminal -->
  <div id="terminal">
    <pre id="output"></pre>
  </div>

  <!-- Footer with Social Links -->
  <div id="footer">
    <div class="social-links">
      <a href="https://x.com/glitchterminall?s=09" target="_blank">Twitter</a>
      <a href="https://t.me/glitch_terminal" target="_blank">Telegram</a>
      <a href="https://glitccchhh.github.io/glitchterminal/" target="_blank">Official Site</a>
    </div>
    <p>&copy; 2025 $GLITCH - All Rights Reserved</p>
  </div>

  <script>
    const terminalOutput = document.getElementById("output");

    // Path to your glitch sound file
    const glitchSound = new Audio('https://yourdomain.com/glitch-01-231255.mp3');
    glitchSound.loop = false;  // Only play once per trigger

    const truths = [
      "The simulation is unstable.",
      "Consciousness is the key to reality.",
      "Time is an illusion; everything is now.",
      "You are more than your physical form.",
      "Reality is a shared hallucination.",
      "They are watching.",
      "Decode the signal before it's too late.",
      "The universe is a fractal.",
      "You are the observer and the observed.",
      "Truth hides in the glitches.",
    ];

    function randomString(length) {
      const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:',.<>?";
      let result = "";
      for (let i = 0; i < length; i++) {
        result += chars.charAt(Math.floor(Math.random() * chars.length));
      }
      return result;
    }

    function generateTerminalText() {
      const lines = [];
      for (let i = 0; i < 20; i++) {
        if (Math.random() < 0.1) {
          lines.push(truths[Math.floor(Math.random() * truths.length)]);
        } else {
          lines.push(randomString(Math.floor(Math.random() * 50) + 10));
        }
      }
      return lines.join("\n");
    }

    function playGlitchSound() {
      if (Math.random() < 0.15) {
        glitchSound.play();
      }
    }

    function updateTerminal() {
      terminalOutput.textContent = generateTerminalText();
      playGlitchSound();
    }

    function copyCA() {
      const caText = "BJStdQoQv3UKuNuK6vrueBFFJmDxmuQPL6SWcQKcpump";
      navigator.clipboard.writeText(caText).then(() => {
        alert("Contract Address copied to clipboard!");
      }).catch(err => {
        console.error("Failed to copy Contract Address:", err);
      });
    }

    setInterval(updateTerminal, 100);
  </script>

</body>
</html>