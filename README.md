# Zainab---Rehan
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Forever Mine 💖</title>

<style>
body {
  margin: 0;
  height: 100vh;
  overflow: hidden;
  font-family: Arial, sans-serif;
  background: linear-gradient(135deg, orange, yellow);
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

/* floating hearts */
.heart {
  position: absolute;
  top: -10px;
  font-size: 20px;
  animation: fall linear forwards;
}

@keyframes fall {
  to {
    transform: translateY(100vh);
    opacity: 0;
  }
}

/* buttons */
button {
  padding: 12px 25px;
  font-size: 18px;
  border: none;
  border-radius: 12px;
  cursor: pointer;
  margin: 10px;
  transition: 0.3s;
}

#yesBtn {
  background: green;
  color: white;
}

#noBtn {
  position: absolute;
  background: red;
  color: white;
}

/* typing text */
.typing {
  font-size: 22px;
  color: white;
  white-space: nowrap;
  overflow: hidden;
  border-right: 3px solid white;
  width: 0;
  animation: typing 4s steps(40) forwards, blink 0.7s infinite;
}

@keyframes typing {
  from { width: 0 }
  to { width: 100% }
}

@keyframes blink {
  50% { border-color: transparent }
}

.hidden { display: none; }

.final {
  color: white;
}
</style>
</head>

<body>

<div id="main">
  <div class="typing">Will you forever be mine? Zainab 💖</div>
  <p style="color:white;">From: Rehan 💌</p>

  <button id="yesBtn">Yes 💖</button>
  <button id="noBtn">No 😢</button>
</div>

<div id="final" class="hidden final">
  <h1>I know you're forever mine ❤️</h1>
  <img src="https://media.tenor.com/0AV1Q4Hf6hAAAAAC/cat-kiss.gif" width="220">
</div>

<script>

// floating hearts
setInterval(() => {
  const heart = document.createElement("div");
  heart.classList.add("heart");
  heart.innerHTML = "💖";
  heart.style.left = Math.random() * window.innerWidth + "px";
  heart.style.animationDuration = (2 + Math.random() * 3) + "s";
  document.body.appendChild(heart);

  setTimeout(() => heart.remove(), 5000);
}, 300);

// NO button escapes
const noBtn = document.getElementById("noBtn");

noBtn.addEventListener("mouseover", () => {
  noBtn.style.top = Math.random() * window.innerHeight + "px";
  noBtn.style.left = Math.random() * window.innerWidth + "px";
});

// YES button action
document.getElementById("yesBtn").addEventListener("click", () => {
  document.getElementById("main").classList.add("hidden");
  document.getElementById("final").classList.remove("hidden");
});

</script>

</body>
</html>
