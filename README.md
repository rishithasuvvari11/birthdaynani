<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>A Little Secret for Nani ♡</title>

<style>
:root {
  --pink: #f2c9c8;
  --rose: #b75b6b;
  --wine: #7b3445;
  --paper: #fffaf4;
  --ink: #56343b;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  min-height: 100vh;
  background: linear-gradient(135deg, #fffaf4, #f7dedd);
  color: var(--ink);
  font-family: Georgia, serif;
}

button, input { font: inherit; }

button {
  cursor: pointer;
  border: none;
  padding: 12px 18px;
  border-radius: 5px;
  background: var(--wine);
  color: white;
  margin: 5px;
}

button:hover { background: var(--rose); }

input {
  padding: 12px;
  border: 1px solid #dfc7bd;
  border-radius: 5px;
  background: #fffaf7;
  color: var(--ink);
}

.hidden { display: none !important; }

.screen {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px;
}

.card {
  background: var(--paper);
  border: 1px solid #eadbd0;
  box-shadow: 0 18px 55px #784a4a1b;
  padding: 35px 25px;
  text-align: center;
  width: min(650px, 100%);
  margin: 20px auto;
  position: relative;
}

.login { max-width: 390px; }

h1 {
  font-size: clamp(38px, 9vw, 65px);
  color: var(--wine);
  font-weight: normal;
}

h2 {
  color: var(--wine);
  font-size: clamp(25px, 6vw, 38px);
  font-weight: normal;
}

p { line-height: 1.8; }

.small {
  color: #987c7d;
  font-size: 12px;
}

.script {
  font-family: "Brush Script MT", cursive;
  font-size: clamp(55px, 12vw, 90px);
  color: #9d3048;
  line-height: .95;
}

.eyebrow {
  text-transform: uppercase;
  letter-spacing: 3px;
  font: 11px Arial, sans-serif;
  color: var(--rose);
}

.ribbon {
  display: inline-block;
  background: var(--wine);
  color: white;
  padding: 8px 25px;
  letter-spacing: 3px;
}

main {
  max-width: 760px;
  margin: auto;
  padding: 55px 12px 20px;
}

.topbar {
  position: fixed;
  z-index: 10;
  top: 0;
  left: 0;
  right: 0;
  padding: 13px;
  background: #fffaf4ed;
  border-bottom: 1px solid #eadbd0;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font: 10px Arial, sans-serif;
  letter-spacing: 1px;
}

.page { display: none; animation: fade .5s ease; }
.page.active { display: block; }

.envelope {
  width: min(300px, 85%);
  height: 185px;
  background: #efd3bd;
  margin: 30px auto;
  position: relative;
  cursor: pointer;
  display: grid;
  place-items: center;
  box-shadow: 0 10px 25px #a36c5620;
}

.envelope:before {
  content: "♡";
  position: absolute;
  font-size: 50px;
  color: var(--wine);
  z-index: 2;
}

.letter {
  background: #fff6ec;
  border: 1px solid #ead8cf;
  padding: 25px;
  max-width: 480px;
  margin: 20px auto;
  line-height: 1.9;
  white-space: pre-line;
  text-align: left;
}

.coupon {
  max-width: 380px;
  margin: 25px auto;
  padding: 15px;
  background: #e4c19a;
  border: 1px dashed white;
}

.coupon-inner {
  background: #fff6e9;
  padding: 25px 10px;
}

.scratch {
  width: 100%;
  min-height: 110px;
  background: linear-gradient(135deg, #b9796b, #d8a27f);
  color: white;
  border: 2px dashed white;
  font-size: 17px;
}

.scratch.revealed {
  background: #fffaf1;
  color: var(--wine);
  border: 1px solid #e7c8b9;
}

.meter {
  width: 170px;
  height: 170px;
  border: 3px solid #e7b9ba;
  border-radius: 50%;
  margin: 25px auto;
  display: grid;
  place-items: center;
  background: radial-gradient(circle, white 45%, #f8e4e2);
  font-size: 28px;
  color: var(--wine);
}

.atm {
  max-width: 360px;
  margin: 20px auto;
  padding: 20px;
  background: #263331;
  border: 8px solid #9a9b92;
  color: #c7e4d5;
  font-family: Arial, sans-serif;
}

.atmscreen {
  background: #172321;
  border: 1px solid #597c6b;
  padding: 20px 8px;
  margin: 15px 0;
}

.keypad {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 5px;
}

.keypad button {
  background: #aeb8b0;
  color: #26352e;
  margin: 0;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(130px, 1fr));
  gap: 12px;
  margin: 20px 0;
}

.photo {
  height: 160px;
  background: #f5dfd6;
  border: 1px solid #e7cfc4;
  position: relative;
  display: grid;
  place-items: center;
  overflow: hidden;
  color: var(--wine);
}

.photo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.photo input {
  position: absolute;
  inset: 0;
  opacity: 0;
  width: 100%;
  cursor: pointer;
}

.cake { font-size: 80px; margin: 20px; }

.heart {
  color: #c7354e;
  font-size: 85px;
  animation: beat 1s infinite;
}

.footer {
  text-align: center;
  padding: 25px;
  color: #a58a86;
  font: 10px Arial, sans-serif;
  letter-spacing: 2px;
}

.floating {
  position: fixed;
  bottom: -30px;
  pointer-events: none;
  animation: floatUp 3s linear forwards;
  z-index: 20;
}

@keyframes fade {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes beat {
  50% { transform: scale(1.15); }
}

@keyframes floatUp {
  to { transform: translateY(-110vh) rotate(30deg); opacity: 0; }
}

@media(max-width:480px) {
  .card { padding: 28px 18px; }
  .topbar { font-size: 9px; }
}
</style>
</head>

<body>

<div class="topbar">
  <span>♡ A LITTLE SECRET FOR NANI</span>
  <span id="progress">THE BEGINNING</span>
  <button id="sound">♫ sound</button>
</div>

<!-- PASSCODE SCREEN -->
<section class="screen" id="loginScreen">
  <div class="card login">
    <div style="font-size:35px">♡</div>
    <div class="eyebrow">A little secret for</div>
    <h2>NANI</h2>
    <p class="small">Something beautiful is hiding behind this tiny lock.</p>

    <p class="eyebrow">Enter the passkey</p>
    <input id="passcode" type="password"
           inputmode="numeric" maxlength="20"
           placeholder="♡ Enter passcode">

    <p id="error" style="color:#b73550;font-size:13px"></p>
    <button id="unlock" style="width:100%">Open my surprise ♡</button>

    <p class="small">A tiny little world, made just for you.</p>
    <p class="small">CREATED WITH LOVE BY RISHI</p>
  </div>
</section>

<main id="site" class="hidden">

<!-- BIRTHDAY WELCOME -->
<section class="page active" id="welcome">
  <div class="card">
    <div class="eyebrow">A day made for you</div>
    <div class="script">Happy<br>Birthday</div>
    <p style="font-size:25px;color:#c99b91">♥ ✧ ♥</p>
    <p class="small">THE WORLD GOT BRIGHTER THE DAY YOU ARRIVED</p>
    <h2>Happiest Birthday</h2>
    <div class="ribbon">NANI</div>
    <p>To someone special, my favourite person, and the reason ordinary days feel magical.</p>
    <button data-go="letter">Open the little letter ♡</button>
    <button data-go="letter">Continue →</button>
  </div>
</section>

<!-- LETTER -->
<section class="page" id="letter">
  <div class="card">
    <div class="eyebrow">A note from my heart</div>
    <h2>A letter written for you</h2>

    <div class="envelope" id="envelope">💌</div>
    <p class="small">Tap the envelope to open your letter.</p>

    <div class="letter hidden" id="letterText">My dearest Nani,

Happy birthday to the person who makes my heart feel safe and my life feel a little more special.

You deserve the kindest days, the warmest smiles, and moments so beautiful that you never want to lose.

I hope this new chapter brings you gentle mornings, loud laughter, brave dreams, and everything your heart quietly deserves.

With a little extra love,
Rishi ♡</div>

    <button data-go="coupon">Next chapter →</button>
  </div>
</section>

<!-- SCRATCH COUPON -->
<section class="page" id="coupon">
  <div class="card">
    <div class="eyebrow">A little birthday play · Part I</div>
    <h2>Find your secret surprise</h2>
    <p class="small">A tiny coupon, made just for you.</p>

    <div class="coupon">
      <div class="coupon-inner">
        <h3>Your birthday coupon ♡</h3>
        <button class="scratch" id="scratch">✧ TAP TO REVEAL ✧</button>
        <p class="small">Your surprise is waiting.</p>
      </div>
    </div>

    <p id="couponHint" class="small"></p>
    <button data-go="meter">Proceed to love meter ♥</button>
  </div>
</section>

<!-- LOVE METER -->
<section class="page" id="meter">
  <div class="card">
    <div class="eyebrow">A tiny experiment · Part II</div>
    <h2>How much love is in the air?</h2>
    <p>Let's run a very scientific experiment.</p>

    <div class="meter" id="meterDial">♡</div>
    <h2 id="percent">20%</h2>

    <button id="measure">Measure the love ♥</button>
    <br>
    <button data-go="atm">Visit the Memory ATM →</button>
  </div>
</section>

<!-- MEMORY ATM -->
<section class="page" id="atm">
  <div class="card">
    <div class="eyebrow">Your special memory chapter</div>
    <h2>Memory ATM</h2>
    <p class="small">Enter PIN 1117 to open your memory vault.</p>

    <div class="atm">
      <h2 style="color:white;font-family:Arial">HBL ATM</h2>
      <div class="atmscreen" id="atmScreen">
        <p>WELCOME TO PHOTO BANK</p>
        <p>ENTER YOUR PIN</p>
        <input id="atmPin" inputmode="numeric" maxlength="4"
               placeholder="••••" style="width:100px;text-align:center">
        <button id="atmEnter">ENTER</button>
      </div>
      <div class="keypad" id="keypad"></div>
    </div>

    <div id="photoVault" class="hidden">
      <h2>Your memory album ♡</h2>
      <p>Upload your favourite pictures together.</p>

      <div class="gallery">
        <label class="photo">
          <span>＋ Add photo 1</span>
          <input type="file" accept="image/*">
        </label>
        <label class="photo">
          <span>＋ Add photo 2</span>
          <input type="file" accept="image/*">
        </label>
        <label class="photo">
          <span>＋ Add photo 3</span>
          <input type="file" accept="image/*">
        </label>
      </div>

      <p class="small">Photos are displayed locally and aren't uploaded to a server.</p>
    </div>

    <button data-go="cake">Continue to birthday ritual ♥</button>
  </div>
</section>

<!-- BIRTHDAY CAKE -->
<section class="page" id="cake">
  <div class="card">
    <div class="eyebrow">A special birthday ritual</div>
    <h2>Blow out the candles first</h2>
    <div class="cake">🎂</div>
    <p>Close your eyes, make a wish, and tap below.</p>
    <h2 id="candle">20 🕯️</h2>
    <button id="blow">Blow out the candles ✨</button>
    <br>
    <button data-go="cut">Now cut the cake →</button>
  </div>
</section>

<!-- CUT CAKE -->
<section class="page" id="cut">
  <div class="card">
    <div class="eyebrow">Your birthday moment</div>
    <h2>Now cut the cake!</h2>
    <div class="cake" id="cakeEmoji">🎂</div>
    <p id="cakeMessage">Make a wish, birthday star.</p>
    <button id="cutCake">Cut the cake ♡</button>
    <br>
    <button data-go="gift">Accept your gift →</button>
  </div>
</section>

<!-- FINAL GIFT -->
<section class="page" id="gift">
  <div class="card">
    <div class="eyebrow">A little gift, from me to you</div>
    <div class="heart">♥</div>
    <h2>Happy Birthday,<br>Nani</h2>

    <p>May this year bring you peace in your heart, magic in your everyday life, and people who love you in all the ways you deserve.</p>

    <div class="letter" style="text-align:center">
      You are one of those people who make a normal day feel special.

      Keep smiling, keep dreaming, and never forget how wonderful you are. ♡

      — Rishi
    </div>

    <button id="finale">Open one last surprise ♥</button>
    <button data-go="welcome">Replay from beginning</button>

    <div id="finalMessage" class="hidden">
      <h2>You are loved. Always. ♥</h2>
      <p>End of this little surprise — beginning of another beautiful memory.</p>
    </div>
  </div>
</section>

<div class="footer">MADE WITH ♡ BY RISHI · JUST FOR NANI</div>
</main>

<script>
const PASSCODE = "1117";

const $ = selector => document.querySelector(selector);

const pages = [...document.querySelectorAll(".page")];

function showPage(id) {
  pages.forEach(page => {
    page.classList.toggle("active", page.id === id);
  });

  const page = pages.find(p => p.id === id);
  $("#progress").textContent = page?.querySelector("h2")?.textContent
    || "A LITTLE SECRET";

  window.scrollTo({top: 0, behavior: "smooth"});
  hearts(4);
}

document.querySelectorAll("[data-go]").forEach(button => {
  button.addEventListener("click", () => showPage(button.dataset.go));
});

function hearts(count = 5) {
  for (let i = 0; i < count; i++) {
    const heart = document.createElement("span");
    heart.className = "floating";
    heart.textContent = ["♥", "♡", "✧", "💗"][
      Math.floor(Math.random() * 4)
    ];
    heart.style.left = Math.random() * 95 + "vw";
    heart.style.animationDuration = 2 + Math.random() * 2 + "s";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 4200);
  }
}

// Passcode
function unlock() {
  if ($("#passcode").value === PASSCODE) {
    $("#loginScreen").classList.add("hidden");
    $("#site").classList.remove("hidden");
    hearts(15);
  } else {
    $("#error").textContent = "Incorrect passcode. Try again ♡";
    $("#passcode").select();
  }
}

$("#unlock").addEventListener("click", unlock);

$("#passcode").addEventListener("keydown", event => {
  if (event.key === "Enter") unlock();
});

// Opening the letter
$("#envelope").addEventListener("click", () => {
  $("#letterText").classList.remove("hidden");
  $("#envelope").textContent = "💌 ♡";
  hearts(8);
});

// Scratch coupon
const prizes = [
  "UNLIMITED HUGS ♥",
  "One wish, just for you",
  "Your favourite treat is on me",
  "A long, happy conversation ♡"
];

$("#scratch").addEventListener("click", () => {
  const prize = prizes[Math.floor(Math.random() * prizes.length)];
  $("#scratch").textContent = prize;
  $("#scratch").classList.add("revealed");
  $("#couponHint").textContent = "Your prize is happiness ♥";
  hearts(6);
});

// Love meter
$("#measure").addEventListener("click", () => {
  $("#percent").textContent = "∞%";
  $("#meterDial").textContent = "♥";
  $("#measure").textContent = "Love measured: infinite!";
  hearts(12);
});

// ATM keypad
for (let i = 1; i <= 9; i++) {
  const button = document.createElement("button");
  button.textContent = i;
  button.onclick = () => {
    $("#atmPin").value = ($("#atmPin").value + i).slice(0, 4);
  };
  $("#keypad").appendChild(button);
}

[
  ["CLR", () => $("#atmPin").value = ""],
  ["0", () => $("#atmPin").value = ($("#atmPin").value + "0").slice(0, 4)],
  ["⌫", () => $("#atmPin").value = $("#atmPin").value.slice(0, -1)]
].forEach(([label, action]) => {
  const button = document.createElement("button");
  button.textContent = label;
  button.onclick = action;
  $("#keypad").appendChild(button);
});

function enterPin() {
  if ($("#atmPin").value === "1117") {
    $("#atmScreen").innerHTML =
      "<strong>WELCOME TO YOUR MEMORY BANK ♥</strong>";
    $("#photoVault").classList.remove("hidden");
    hearts(8);
  } else {
    alert("Incorrect PIN. Try 1117.");
  }
}

$("#atmEnter").addEventListener("click", enterPin);

$("#atmPin").addEventListener("keydown", event => {
  if (event.key === "Enter") enterPin();
});

// Photo uploads
document.querySelectorAll(".photo input").forEach(input => {
  input.addEventListener("change", event => {
    const file = event.target.files[0];
    if (!file) return;

    const label = event.target.closest(".photo");
    let image = label.querySelector("img");

    if (!image) {
      image = document.createElement("img");
      label.appendChild(image);
    }

    image.src = URL.createObjectURL(file);
    label.querySelector("span")?.remove();
  });
});

// Blow out the candles
$("#blow").addEventListener("click", () => {
  $("#candle").textContent = "♡";
  $("#blow").textContent = "Wish sent into the universe ✨";
  hearts(16);
});

// Cut the cake
$("#cutCake").addEventListener("click", () => {
  $("#cakeEmoji").textContent = "🍰";
  $("#cakeMessage").textContent =
    "Cake officially cut! First slice is yours, birthday star. ♥";
  $("#cutCake").textContent = "Sweetest moment unlocked";
  hearts(12);
});

// Final surprise
$("#finale").addEventListener("click", () => {
  $("#finalMessage").classList.remove("hidden");
  $("#finale").textContent = "Surprise opened ♥";
  hearts(25);
});

// A small sound effect, activated by the user
$("#sound").addEventListener("click", () => {
  try {
    const AudioContext = window.AudioContext || window.webkitAudioContext;
    const context = new AudioContext();
    const oscillator = context.createOscillator();
    const gain = context.createGain();

    oscillator.type = "sine";
    oscillator.frequency.value = 660;
    gain.gain.value = 0.06;

    oscillator.connect(gain);
    gain.connect(context.destination);

    oscillator.start();
    oscillator.stop(context.currentTime + 0.18);

    $("#sound").textContent = "♫ chime ♥";
    oscillator.onended = () => context.close();
  } catch (error) {
    $("#sound").textContent = "Sound unavailable";
  }
});
</script>
</body>
</html># birthdaynani
its a birthday special and unique wishes to him
