## JAI SHREE RAM
Aspiring Data Analyst with hands-on experience in SQL, Power BI, and Azure Databricks. Focused on data-driven decision making, ETL pipelines, and building efficient, scalable data solutions.
![image alt](https://github.com/DatawithAshutosh/DatawithAshutosh/blob/main/read.me.png?raw=true)

 Hi,I am ASHUTOSH PANDEY

 <!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Hacker Style</title>

<style>
body {
  margin: 0;
  background: black;
  color: #00ff00;
  font-family: "Courier New", monospace;
  overflow: hidden;
}

/* Matrix background */
canvas {
  position: fixed;
  top: 0;
  left: 0;
  z-index: -1;
}

/* Center text */
.container {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Typing effect */
.typing {
  font-size: 40px;
  border-right: 3px solid #00ff00;
  white-space: nowrap;
  overflow: hidden;
  width: 0;
  animation: typing 4s steps(25, end) forwards, blink 0.8s infinite;
}

/* Glitch effect */
.typing::before, .typing::after {
  content: "WELCOME TO MY PROFILE";
  position: absolute;
  left: 0;
}

.typing::before {
  color: red;
  animation: glitch 0.3s infinite;
}

.typing::after {
  color: blue;
  animation: glitch 0.3s infinite reverse;
}

/* Animations */
@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

@keyframes blink {
  50% { border-color: transparent }
}

@keyframes glitch {
  0% { transform: translate(0px); }
  20% { transform: translate(-2px, 2px); }
  40% { transform: translate(-2px, -2px); }
  60% { transform: translate(2px, 2px); }
  80% { transform: translate(2px, -2px); }
  100% { transform: translate(0px); }
}
</style>
</head>

<body>

<canvas id="matrix"></canvas>

<div class="container">
  <div class="typing">WELCOME TO MY PROFILE</div>
</div>

<script>
const canvas = document.getElementById("matrix");
const ctx = canvas.getContext("2d");

canvas.height = window.innerHeight;
canvas.width = window.innerWidth;

const letters = "01ABCDEFGHIJKLMNOPQRSTUVWXYZ";
const fontSize = 14;
const columns = canvas.width / fontSize;

const drops = Array(Math.floor(columns)).fill(1);

function draw() {
  ctx.fillStyle = "rgba(0,0,0,0.05)";
  ctx.fillRect(0, 0, canvas.width, canvas.height);

  ctx.fillStyle = "#0f0";
  ctx.font = fontSize + "px monospace";

  for (let i = 0; i < drops.length; i++) {
    const text = letters[Math.floor(Math.random() * letters.length)];
    ctx.fillText(text, i * fontSize, drops[i] * fontSize);

    if (drops[i] * fontSize > canvas.height && Math.random() > 0.975)
      drops[i] = 0;

    drops[i]++;
  }
}

setInterval(draw, 33);
</script>

</body>
</html>
