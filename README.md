# Laiba-My-Love
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Laiba Zulfiqar ❤️</title>
  <style>
    body {
      margin: 0;
      font-family: 'Georgia', serif;
      color: #fff;
      text-align: center;
      padding: 40px;
      background: url('background.jpg') no-repeat center center fixed;
      background-size: cover;
    }
    h1 {
      font-size: 48px;
      text-shadow: 2px 2px #e91e63;
    }
    p {
      font-size: 24px;
      line-height: 1.8;
      margin-top: 30px;
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
      background-color: rgba(0, 0, 0, 0.5);
      padding: 20px;
      border-radius: 20px;
      box-shadow: 0 0 20px #fff3;
    }
    .heart {
      font-size: 50px;
      animation: beat 1s infinite;
      color: #ff1744;
    }
    @keyframes beat {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.3); }
    }
    canvas {
      position: fixed;
      top: 0;
      left: 0;
      pointer-events: none;
      z-index: 999;
    }
  </style>
</head>
<body>

  <audio autoplay loop>
    <source src="music.mp3" type="audio/mpeg" />
  </audio>

  <canvas id="fireworks"></canvas>

  <h1>💘 Laiba Zulfiqar — Mere Dil Ki Dastaan 💘</h1>

  <p>Laiba...<br>
  Tujhe dekha toh laga khuda ne dua qabool ki hai,<br>
  Tere chehre pe chamak hai, jaise chand ne roshni chura li hai.<br>
  Tu meri har khushi ka sabab hai,<br>
  Tu ho toh lagta hai zindagi ne husn pehna hai...</p>

  <p>Teri baat ka har lafz mehka mehka sa lagta hai,<br>
  Tera naam meri saanson mein narm phoolon jaisa lagta hai.<br>
  Zulfiqar jaise talwar ho par pyaar se bhari,<br>
  Laiba, tu meri mohabbat ki sabse haseen tasveer hai...</p>

  <p>Tere bina har pal adhoora hai,<br>
  Tere saath har din ek nayi roshni ka noor hai.<br>
  Tere honthon ki muskurahat meri jaan le leti hai,<br>
  Par main khushi khushi jeeta hoon, kyunke tu muskaraati hai...</p>

  <p>Tere saath waqt ruk jaaye, toh bhi kam lage,<br>
  Tere ek "hello" se dil shaam-o-subah ban jaye,<br>
  Tujhmein woh jadoo hai, jo lafzon se bayan nahi hota,<br>
  Tujhse mohabbat meri zindagi ka asal matlab hai...</p>

  <h1 class="heart">❤️</h1>
  <h2 style="margin-top: 40px;">Tu meri jaan hai, Laiba.</h2>

  <script src="fireworks.js"></script>
</body>
</html>
const canvas = document.getElementById("fireworks");
const ctx = canvas.getContext("2d");
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let particles = [];

function random(min, max) {
  return Math.random() * (max - min) + min;
}

function createFirework() {
  const x = random(100, canvas.width - 100);
  const y = random(100, canvas.height / 2);
  const count = 100;
  for (let i = 0; i < count; i++) {
    particles.push({
      x, y,
      radius: 2,
      dx: random(-5, 5),
      dy: random(-5, 5),
      life: 100,
      color: `hsl(${Math.floor(random(0, 360))}, 100%, 50%)`
    });
  }
}

function update() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  particles.forEach((p, i) => {
    p.x += p.dx;
    p.y += p.dy;
    p.life--;
    if (p.life <= 0) particles.splice(i, 1);/* Body background and font */
body {
  margin: 0;
  padding: 0;
  font-family: 'Segoe UI', cursive;
  background: linear-gradient(to right, #fbd3e9, #bb377d);
  color: #fff;
  text-align: center;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  animation: fadeIn 2s ease-in;
}

/* I Love You with Lock */
.love-lock {
  font-size: 32px;
  font-weight: bold;
  color: #fff;
  text-shadow: 1px 1px 3px #ff4081;
  margin-bottom: 40px;
  animation: popIn 1.5s ease-out forwards;
}
.love-lock::before {
  content: "🔒 ";
  font-size: 36px;
}

/* Proceed button */
.proceed-btn {
  padding: 14px 32px;
  background: #fff;
  color: #bb377d;
  font-size: 20px;
  font-weight: bold;
  border: none;
  border-radius: 30px;
  box-shadow: 0 0 20px rgba(255,255,255,0.3);
  cursor: pointer;
  transition: all 0.3s ease;
  text-transform: uppercase;
}
.proceed-btn:hover {
  background: #ffebf0;
  color: #e91e63;
  box-shadow: 0 0 25px rgba(255,255,255,0.6);
  transform: scale(1.05);
}

/* Fade and pop animations */
@keyframes fadeIn {
  from {opacity: 0;}
  to {opacity: 1;}
}
@keyframes popIn {
  0% {transform: scale(0);}
  100% {transform: scale(1);}
}

    ctx.beginPath();
    ctx.arc(p.x, p.y, p.radius, 0, Math.PI * 2);
    ctx.fillStyle = p.color;
    ctx.fill();
  });
}

setInterval(() => {
  createFirework();
}, 1500);

function animate() {
  update();
  requestAnimationFrame(animate);
}

animate();
