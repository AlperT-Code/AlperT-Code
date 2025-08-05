<h1 align="center">Hi there 👋, I'm Alper Taşdemir</h1>
<h3 align="center">I'm a passionate developer from Türkiye</h3>

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&width=435&lines=Full-Stack+Developer;Game+Developer;Open+Source+Contributor" alt="Typing SVG" />
</p>

---

### 🦖 Play with the Dino!

> Just click inside the box and press the **Spacebar** to jump!

<div align="center">
  <canvas id="dinoGame" width="600" height="150" style="border:1px solid #ccc;"></canvas>
</div>

<script>
let canvas = document.getElementById("dinoGame");
let ctx = canvas.getContext("2d");

let dino = { x: 50, y: 100, vy: 0, jumping: false };
let gravity = 2;
let cactus = { x: 600, y: 100, width: 20, height: 40 };

function draw() {
  ctx.clearRect(0, 0, canvas.width, canvas.height);
  ctx.fillStyle = "#555";
  ctx.fillRect(0, 140, canvas.width, 10);
  ctx.fillStyle = "green";
  ctx.fillRect(cactus.x, cactus.y - cactus.height, cactus.width, cactus.height);
  ctx.fillStyle = "black";
  ctx.fillRect(dino.x, dino.y - 30, 20, 30);
}

function update() {
  if (dino.jumping) {
    dino.vy -= gravity;
    dino.y -= dino.vy;
    if (dino.y >= 100) {
      dino.y = 100;
      dino.jumping = false;
      dino.vy = 0;
    }
  }

  cactus.x -= 5;
  if (cactus.x < -20) cactus.x = 600;

  draw();

  if (
    dino.x + 20 > cactus.x &&
    dino.x < cactus.x + cactus.width &&
    dino.y > cactus.y - cactus.height
  ) {
    alert("💥 Game Over!");
    cactus.x = 600;
  }

  requestAnimationFrame(update);
}

document.addEventListener("keydown", (e) => {
  if (e.code === "Space" && !dino.jumping) {
    dino.jumping = true;
    dino.vy = 20;
  }
});

update();
</script>

---

### 🚀 Languages & Tools

<p align="left">
  <img src="https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white"/>
  <img src="https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white"/>
  <img src="https://img.shields.io/badge/javascript-%23F7DF1E.svg?style=for-the-badge&logo=javascript&logoColor=black"/>
  <img src="https://img.shields.io/badge/python-%2314354C.svg?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=c-sharp&logoColor=white"/>
  <img src="https://img.shields.io/badge/unity-%23000000.svg?style=for-the-badge&logo=unity&logoColor=white"/>
</p>

---

### 📫 Reach Me

- 🌐 Website: [edgeoyun.com](https://edgeoyun.com)
- 📧 E-Mail: **alper@gmail.com** *(örnek)*
- 🧠 Fun Fact: I love turning coffee into code ☕💻

---

<p align="center">Made with ❤️ by Alper</p>
