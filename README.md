<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Truth Terminal</title>
  <style>
    body {
      background: black;
      color: #00ff00;
      font-family: "Courier New", Courier, monospace;
      margin: 0;
      height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
      flex-direction: column; /* Allows vertical stacking */
    }

    #description {
      font-size: 1.5rem;
      margin-bottom: 20px;
      color: lime;
      text-align: center;
    }

    #terminal {
      border: 2px solid #00ff00;
      width: 90%;
      height: 70%;
      overflow: hidden;
      box-shadow: 0 0 10px #00ff00;
      padding: 10px;
    }

    #output {
      font-size: 1rem;
      white-space: pre-wrap;
      overflow-y: auto;
      animation: glitch 0.2s infinite;
      line-height: 1.5;
    }

    /* Glitch effect */
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

  </style>
</head>
<body>
  <!-- Meme Coin Description before the terminal -->
  <div id="description">
    <p>Welcome to the official terminal for [GLITCH].</p>
    <p>"Memes to the Moon 🚀"</p>
    <p>Get ready to decode the truth hidden in the glitches...</p>
  </div>

  <!-- Glitch terminal -->
  <div id="terminal">
    <pre id="output"></pre>
  </div>

  <script>
    const terminalOutput = document.getElementById("output");

    // Cryptic or profound "truth" messages
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

    // Generates random glitchy strings
    function randomString(length) {
      const chars =
        "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%^&*()_+-=[]{}|;:',.<>?";
      let result = "";
      for (let i = 0; i < length; i++) {
        result += chars.charAt(Math.floor(Math.random() * chars.length));
      }
      return result;
    }

    // Combines glitch lines with occasional truth messages
    function generateTerminalText() {
      const lines = [];
      for (let i = 0; i < 20; i++) {
        if (Math.random() < 0.1) {
          // 10% chance of a "truth" message
          lines.push(truths[Math.floor(Math.random() * truths.length)]);
        } else {
          // Random glitchy text
          lines.push(randomString(Math.floor(Math.random() * 50) + 10));
        }
      }
      return lines.join("\n");
    }

    // Updates the terminal periodically
    function updateTerminal() {
      terminalOutput.textContent = generateTerminalText();
    }

    setInterval(updateTerminal, 100);
  </script>
</body>
</html>