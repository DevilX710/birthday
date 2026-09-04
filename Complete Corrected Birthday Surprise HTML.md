```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">

<meta
  name="viewport"
  content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover"
>

<title>For You 🎂💗</title>

<style>

/* =========================================================
   RESET
========================================================= */

*{
  box-sizing:border-box;
  -webkit-tap-highlight-color:transparent;
}

html,
body{
  margin:0;
  padding:0;
  width:100%;
  min-height:100%;
}

body{
  min-height:100vh;
  min-height:-webkit-fill-available;

  font-family:
    -apple-system,
    BlinkMacSystemFont,
    "Segoe UI",
    Arial,
    sans-serif;

  background:
    linear-gradient(
      135deg,
      #ffd9e9,
      #e8dcff,
      #d9f3ff
    );

  color:#4b3650;
  overflow:hidden;
}

/* =========================================================
   BUTTONS
========================================================= */

button{
  font:inherit;
  border:0;
  cursor:pointer;
  -webkit-appearance:none;
  appearance:none;
}

button:disabled{
  cursor:default;
}

/* =========================================================
   FLOATING BACKGROUND
========================================================= */

.bg span{
  position:fixed;
  bottom:-40px;

  opacity:.45;
  font-size:22px;

  animation:float 9s linear infinite;

  pointer-events:none;
}

.bg span:nth-child(1){
  left:8%;
}

.bg span:nth-child(2){
  left:27%;
  animation-delay:2s;
}

.bg span:nth-child(3){
  left:48%;
  animation-delay:4s;
}

.bg span:nth-child(4){
  left:70%;
  animation-delay:1s;
}

.bg span:nth-child(5){
  left:88%;
  animation-delay:3s;
}

@keyframes float{
  to{
    transform:
      translateY(-115vh)
      rotate(25deg);

    opacity:0;
  }
}

/* =========================================================
   MAIN LAYOUT
========================================================= */

.wrap{
  width:92vw;
  max-width:540px;

  margin:0 auto;
  padding:20px;

  min-height:100vh;
  min-height:-webkit-fill-available;

  display:flex;
  align-items:center;

  position:relative;
  z-index:2;
}

.card{
  width:100%;
  min-height:650px;

  padding:30px 25px;

  border:1px solid rgba(255,255,255,.9);

  background:rgba(255,255,255,.60);

  -webkit-backdrop-filter:blur(18px);
  backdrop-filter:blur(18px);

  border-radius:32px;

  box-shadow:
    0 25px 70px rgba(107,75,114,.14);

  display:flex;
  align-items:center;
  justify-content:center;

  text-align:center;
}

/* =========================================================
   SCREENS
========================================================= */

.screen{
  display:none;
  width:100%;

  animation:
    enter .55s ease;
}

.screen.active{
  display:block;
}

@keyframes enter{
  from{
    opacity:0;
    transform:
      translateY(16px)
      scale(.98);
  }

  to{
    opacity:1;
    transform:none;
  }
}

/* =========================================================
   TEXT
========================================================= */

.emoji{
  font-size:76px;
  margin-bottom:15px;

  animation:
    bob 2s ease-in-out infinite;
}

@keyframes bob{
  50%{
    transform:
      translateY(-8px)
      rotate(2deg);
  }
}

h1{
  font-size:38px;
  margin:8px 0 12px;
}

h2{
  font-size:28px;
  margin:8px 0 15px;
}

p{
  font-size:17px;
  line-height:1.6;
  color:#66536a;
}

.small{
  font-size:14px;
  color:#89748d;
}

/* =========================================================
   BUTTON STYLES
========================================================= */

.primary{
  background:#ff76aa;
  color:white;

  padding:14px 23px;

  border-radius:999px;

  font-weight:800;

  box-shadow:
    0 9px 20px rgba(255,118,170,.21);

  margin:8px;

  transition:
    transform .15s ease,
    opacity .15s ease;
}

.secondary{
  background:white;
  color:#704e75;

  padding:14px 23px;

  border-radius:999px;

  font-weight:800;

  margin:8px;

  transition:
    transform .15s ease;
}

.primary:not(:disabled):active,
.secondary:not(:disabled):active{
  transform:scale(.96);
}

/* =========================================================
   STORY / PEN SCENE
========================================================= */

.scene{
  height:245px;

  margin:20px 0;

  border-radius:24px;

  background:
    linear-gradient(
      #fff8fc 0 62%,
      #e8d7c9 62%
    );

  position:relative;
  overflow:hidden;

  border:1px solid rgba(123,92,105,.08);
}

.board{
  position:absolute;

  top:18px;
  left:50%;

  transform:translateX(-50%);

  width:64%;
  height:82px;

  border:7px solid #9c806b;

  border-radius:9px;

  background:#b9d8c2;
}

.desk{
  position:absolute;

  bottom:28px;
  left:12%;

  width:76%;
  height:20px;

  border-radius:8px;

  background:#a98264;
}

.person{
  position:absolute;
  left:12%;
  bottom:45px;

  font-size:58px;
}

.girl{
  position:absolute;
  right:12%;
  bottom:45px;

  font-size:58px;
}

.pen{
  display:none;

  position:absolute;

  left:20%;
  bottom:92px;

  font-size:30px;
}

.pen.fly{
  display:block;

  animation:
    fly 1.35s forwards;
}

@keyframes fly{
  to{
    transform:
      translate(250px,-35px)
      rotate(720deg);
  }
}

.bonk{
  display:none;

  position:absolute;

  right:6%;
  top:70px;

  font-weight:900;
  font-size:27px;
}

.bonk.show{
  display:block;

  animation:
    pop .45s ease;
}

@keyframes pop{
  from{
    transform:scale(0);
  }

  to{
    transform:scale(1);
  }
}

.story{
  background:rgba(255,250,252,.73);

  padding:16px;

  border-radius:19px;

  margin:15px 0;

  line-height:1.5;
}

/* =========================================================
   STAR GAME
========================================================= */

.game{
  height:315px;

  position:relative;

  margin:18px 0;

  border-radius:24px;

  background:rgba(255,255,255,.50);

  overflow:hidden;

  border:1px solid rgba(118,92,118,.08);

  touch-action:manipulation;
}

.star{
  position:absolute;

  background:transparent;

  font-size:34px;

  padding:0;

  display:none;

  box-shadow:none;

  line-height:1;

  width:50px;
  height:50px;

  text-align:center;

  touch-action:manipulation;
}

.stats{
  display:flex;
  justify-content:space-between;

  font-weight:800;

  margin:8px;
}

.bar{
  height:10px;

  background:rgba(255,255,255,.72);

  border-radius:20px;

  overflow:hidden;

  margin:10px 4px;
}

.fill{
  height:100%;
  width:0;

  background:#ff76aa;

  transition:.2s;
}

/* =========================================================
   SCRATCH CARD
========================================================= */

.scratch-wrap{
  margin:20px auto;

  width:100%;
  max-width:390px;
}

.scratch-card{
  position:relative;

  height:275px;

  width:100%;

  border-radius:25px;

  overflow:hidden;

  background:#fffafd;

  box-shadow:
    0 16px 35px rgba(107,75,114,.12);

  border:1px solid rgba(255,255,255,.9);
}

.scratch-reveal{
  height:100%;

  padding:25px 18px;

  display:flex;

  flex-direction:column;

  align-items:center;

  justify-content:center;
}

.scratch-icon{
  font-size:48px;
  margin-bottom:8px;
}

.scratch-question{
  font-size:23px;

  font-weight:900;

  line-height:1.25;

  margin:5px 0 16px;
}

.gift-input{
  width:100%;

  padding:13px 15px;

  border:2px solid #f0d6e4;

  border-radius:15px;

  outline:none;

  background:white;

  color:#4b3650;

  font-size:16px;

  text-align:center;

  -webkit-appearance:none;
}

.gift-input:focus{
  border-color:#ff76aa;
}

.scratch-next{
  opacity:.55;

  pointer-events:none;
}

.scratch-next.ready{
  opacity:1;
  pointer-events:auto;
}

#scratchCanvas{
  position:absolute;

  left:0;
  top:0;

  width:100%;
  height:100%;

  touch-action:none;

  cursor:crosshair;
}

/* =========================================================
   QUESTION
========================================================= */

.question{
  font-size:42px;

  font-weight:900;

  line-height:1.15;

  margin:24px 0;
}

/* =========================================================
   CONFETTI
========================================================= */

.hearts{
  position:fixed;

  inset:0;

  pointer-events:none;

  z-index:20;
}

.heart{
  position:absolute;

  font-size:25px;

  animation:
    burst 1.25s ease forwards;
}

@keyframes burst{
  to{
    transform:
      translate(var(--x),var(--y))
      scale(1.4);

    opacity:0;
  }
}

/* =========================================================
   MOBILE
========================================================= */

@media(max-width:500px){

  .wrap{
    width:100%;
    padding:12px;
  }

  .card{
    min-height:calc(100vh - 24px);
    min-height:calc(-webkit-fill-available - 24px);

    padding:24px 17px;

    border-radius:28px;
  }

  h1{
    font-size:31px;
  }

  h2{
    font-size:25px;
  }

  .scene{
    height:220px;
  }

  .game{
    height:285px;
  }

  .question{
    font-size:36px;
  }

  .scratch-card{
    height:265px;
  }

  .scratch-question{
    font-size:21px;
  }

  .primary,
  .secondary{
    padding:13px 19px;
  }
}

/* =========================================================
   VERY SMALL PHONES
========================================================= */

@media(max-height:680px){

  .card{
    min-height:600px;
    padding-top:18px;
    padding-bottom:18px;
  }

  .emoji{
    font-size:62px;
    margin-bottom:8px;
  }

  .scene{
    height:190px;
    margin:12px 0;
  }

  .game{
    height:245px;
  }

  .letter{
    max-height:300px;
    overflow:auto;
  }

}

</style>
</head>


<body>

<!-- =======================================================
     BACKGROUND
======================================================= -->

<div class="bg">

  <span>💗</span>
  <span>✨</span>
  <span>💖</span>
  <span>⭐</span>
  <span>💗</span>

</div>

<div
  class="hearts"
  id="hearts"
></div>


<!-- =======================================================
     MAIN CARD
======================================================= -->

<div class="wrap">

<main class="card">


<!-- =======================================================
     SCREEN 1 — START
======================================================= -->

<section
  class="screen active"
  id="s1"
>

  <div class="emoji">
    🎁
  </div>

  <h1>
    A little surprise...
  </h1>

  <p>
    There's something I made for your birthday.
  </p>

  <p class="small">
    But before you get it...
    you have to go through the story first 👀
  </p>

  <button
    class="primary"
    type="button"
    onclick="go(2)"
  >
    START THE SURPRISE 💗
  </button>

</section>


<!-- =======================================================
     SCREEN 2 — PEN STORY
======================================================= -->

<section
  class="screen"
  id="s2"
>

  <h2>
    Every friendship has a beginning...
  </h2>

  <p>
    Ours started in probably the most awkward way possible. 😭
  </p>

  <div class="scene">

    <div class="board"></div>

    <div class="desk"></div>

    <div class="person">
      🧑🏻
    </div>

    <div class="girl">
      👧🏻
    </div>

    <div
      class="pen"
      id="pen"
    >
      🖊️
    </div>

    <div
      class="bonk"
      id="bonk"
    >
      💥 BONK
    </div>

  </div>

  <div
    class="story"
    id="story"
  >
    One completely normal day in class...
    <br>
    <b>
      My friend asked me for a pen.
    </b>
  </div>

  <button
    class="primary"
    id="storyBtn"
    type="button"
    onclick="throwPen()"
  >
    PASS THE PEN 🖊️
  </button>

</section>


<!-- =======================================================
     SCREEN 3 — BIRTHDAY
======================================================= -->

<section
  class="screen"
  id="s3"
>

  <div class="emoji">
    🎂
  </div>

  <h1>
    HAPPY BIRTHDAYYY!
  </h1>

  <h2>
    🎉 💗 🎉
  </h2>

  <p>
    And somehow, after that absolutely terrible
    first impression...
  </p>

  <div class="story">

    <b>
      We're still friends 4–5 years later. 😭
    </b>

    <br>
    <br>

    From accidentally throwing a pen at you
    to still being here years later...
    that's actually kinda crazy.

  </div>

  <button
    class="primary"
    type="button"
    onclick="confetti();go(4)"
  >
    KEEP GOING →
  </button>

</section>


<!-- =======================================================
     SCREEN 4 — MESSAGE
======================================================= -->

<section
  class="screen"
  id="s4"
>

  <h2>
    Your actual birthday message 💌
  </h2>

  <div class="letter">

    <b>
      Dear birthday girl,
    </b>

    <br>
    <br>

    Happy birthdayyy! 🎂💗

    <br>
    <br>

    I'm genuinely glad that one random pen
    somehow started a friendship that lasted
    this long. 😭

    <br>
    <br>

    I hope this year brings you loads of good
    moments, laughs, and everything you're
    hoping for.

    <br>
    <br>

    Thanks for being one of those people who
    makes life more fun just by being around.

    <br>
    <br>

    <b>
      Now go enjoy your birthday, idiot. 😭💗
    </b>

  </div>

  <button
    class="primary"
    type="button"
    onclick="go(5)"
  >
    BUT WAIT... 🎁
  </button>

</section>


<!-- =======================================================
     SCREEN 5 — STAR GAME
======================================================= -->

<section
  class="screen"
  id="s5"
>

  <h2>
    You don't get the gift THAT easily 👀
  </h2>

  <p>
    Catch <b>7 stars</b> before the timer runs out.
  </p>

  <div class="stats">

    <span>
      ⭐
      <span id="score">
        0
      </span>/7
    </span>

    <span>
      ⏱️
      <span id="time">
        20
      </span>s
    </span>

  </div>

  <div class="bar">

    <div
      class="fill"
      id="fill"
    ></div>

  </div>

  <div
    class="game"
    id="game"
  >

    <button
      class="star"
      id="star"
      type="button"
      onclick="catchStar()"
    >
      ⭐
    </button>

  </div>

  <p
    class="small"
    id="gameMsg"
  >
    Catch them all to unlock the gift!
  </p>

</section>


<!-- =======================================================
     SCREEN 6 — GIFT UNLOCKED
======================================================= -->

<section
  class="screen"
  id="s6"
>

  <div class="emoji">
    🎁✨
  </div>

  <h1>
    GIFT UNLOCKED!
  </h1>

  <p>
    You actually did it 😭💗
  </p>

  <p class="small">
    But wait...
    <br>
    Your gift is still hidden 👀
  </p>

  <button
    class="primary"
    type="button"
    onclick="go(7)"
  >
    UNWRAP THE GIFT 🎁
  </button>

</section>


<!-- =======================================================
     SCREEN 7 — SCRATCH CARD
======================================================= -->

<section
  class="screen"
  id="s7"
>

  <h2>
    Your gift is hiding here... 👀🎁
  </h2>

  <p>
    Scratch the card to reveal what's underneath.
  </p>

  <div class="scratch-wrap">

    <div class="scratch-card">

      <!-- CONTENT UNDER SCRATCH LAYER -->

      <div class="scratch-reveal">

        <div class="scratch-icon">
          🎁
        </div>

        <div class="scratch-question">
          What gift do you want from me? 👀💗
        </div>

        <input
          id="giftAnswer"
          class="gift-input"
          type="text"
          maxlength="120"
          autocomplete="off"
          placeholder="Tell me what you want..."
        >

        <button
          class="primary scratch-next"
          id="scratchNext"
          type="button"
          onclick="saveGiftAnswer()"
          disabled
        >
          SUBMIT MY ANSWER 💗
        </button>

      </div>

      <!-- SCRATCH LAYER -->

      <canvas
        id="scratchCanvas"
      ></canvas>

    </div>

  </div>

  <p
    class="small"
    id="scratchMsg"
  >
    Scratch the card with your finger or mouse ✨
  </p>

  <p
    class="small"
    id="submitStatus"
  ></p>

</section>


<!-- =======================================================
     SCREEN 8 — ONE LAST QUESTION
======================================================= -->

<section
  class="screen"
  id="s8"
>

  <h2>
    One last thing...
  </h2>

  <p>
    Before you leave, I have one very important
    question. 👀
  </p>

  <div class="question">

    Do you
    <br>
    love me? 💗

  </div>

  <button
    class="primary"
    type="button"
    onclick="yes()"
  >
    YES 😭💗
  </button>

  <button
    class="secondary"
    id="noBtn"
    type="button"
    onclick="nope()"
  >
    NO 💀
  </button>

  <p
    class="small"
    id="noMsg"
  ></p>

</section>


<!-- =======================================================
     SCREEN 9 — FINAL
======================================================= -->

<section
  class="screen"
  id="s9"
>

  <div class="emoji">
    💗
  </div>

  <h1>
    I KNEW IT 😭
  </h1>

  <p>
    From that legendary pen incident...
  </p>

  <p>
    to 4–5 years of friendship...
  </p>

  <div class="story">

    <b>
      Happy birthday, bestie. 💗
    </b>

    <br>
    <br>

    You're stuck with me now. 😭

  </div>

  <button
    class="primary"
    type="button"
    onclick="location.reload()"
  >
    REPLAY ↻
  </button>

</section>


</main>
</div>


<script>

/* =========================================================
   GOOGLE APPS SCRIPT
   YOUR REAL WEB APP URL
========================================================= */

var ANSWER_ENDPOINT =
  "https://script.google.com/macros/s/AKfycbxkyiN9qVhKKK7l2XfnJjXNUSltx6YfGW-VkvOimv7eoZfhB7a4iX1TAsG5_sQBLOmW/exec";


/* =========================================================
   GLOBAL VARIABLES
========================================================= */

var timer = null;

var score = 0;

var seconds = 20;

var noCount = 0;

var currentScreen = 1;

var gameRunning = false;

var giftSubmitted = false;


/* =========================================================
   SCREEN NAVIGATION
========================================================= */

function go(n){

  currentScreen = n;

  var screens =
    document.querySelectorAll(".screen");

  var i;

  for(i = 0; i < screens.length; i++){

    screens[i].classList.remove("active");

  }

  var target =
    document.getElementById("s" + n);

  if(target){

    target.classList.add("active");

  }

  /*
   * Stop the star game when leaving it.
   */

  if(n !== 5){

    stopGame();

  }

  /*
   * Start star game.
   */

  if(n === 5){

    setTimeout(function(){

      startGame();

    },100);

  }

  /*
   * Prepare scratch card.
   *
   * This now happens on SCREEN 7.
   */

  if(n === 7){

    setTimeout(function(){

      initScratch();

    },100);

  }

}


/* =========================================================
   PEN STORY
========================================================= */

function throwPen(){

  var pen =
    document.getElementById("pen");

  var bonk =
    document.getElementById("bonk");

  var story =
    document.getElementById("story");

  var btn =
    document.getElementById("storyBtn");

  btn.disabled = true;

  pen.style.display = "block";

  pen.classList.remove("fly");

  /*
   * Force animation restart.
   */

  void pen.offsetWidth;

  pen.classList.add("fly");

  setTimeout(function(){

    bonk.classList.add("show");

    story.innerHTML =
      "<b>And somehow... the pen went straight to HER. 💀</b>" +
      "<br>" +
      "Yeah. That was our first ever meeting. 😭";

    btn.textContent =
      "OKAY... WHAT HAPPENED AFTER? →";

    btn.disabled = false;

    btn.onclick = function(){

      go(3);

    };

  },1400);

}


/* =========================================================
   STAR GAME
========================================================= */

function startGame(){

  stopGame();

  gameRunning = true;

  score = 0;

  seconds = 20;

  document.getElementById("score").textContent =
    "0";

  document.getElementById("time").textContent =
    "20";

  document.getElementById("fill").style.width =
    "0%";

  document.getElementById("gameMsg").textContent =
    "Catch them all to unlock the gift!";

  moveStar();

  timer = setInterval(function(){

    /*
     * If user left the game, stop everything.
     */

    if(currentScreen !== 5){

      stopGame();

      return;

    }

    seconds--;

    if(seconds < 0){

      seconds = 0;

    }

    document.getElementById("time").textContent =
      String(seconds);

    if(seconds <= 0){

      stopGame();

      document.getElementById("star").style.display =
        "none";

      document.getElementById("gameMsg").textContent =
        "TIME'S UP 😭 Try again!";

      /*
       * Restart only if user is still on the game.
       */

      setTimeout(function(){

        if(currentScreen === 5){

          startGame();

        }

      },900);

    }

  },1000);

}


/* =========================================================
   STOP GAME
========================================================= */

function stopGame(){

  if(timer !== null){

    clearInterval(timer);

    timer = null;

  }

  gameRunning = false;

}


/* =========================================================
   MOVE STAR
========================================================= */

function moveStar(){

  var game =
    document.getElementById("game");

  var star =
    document.getElementById("star");

  if(!game || !star){

    return;

  }

  var gameWidth =
    game.clientWidth;

  var gameHeight =
    game.clientHeight;

  var starSize = 50;

  var maxLeft =
    Math.max(
      5,
      gameWidth - starSize - 5
    );

  var maxTop =
    Math.max(
      5,
      gameHeight - starSize - 5
    );

  var left =
    5 +
    Math.random() *
    Math.max(
      1,
      maxLeft - 5
    );

  var top =
    5 +
    Math.random() *
    Math.max(
      1,
      maxTop - 5
    );

  star.style.left =
    Math.round(left) + "px";

  star.style.top =
    Math.round(top) + "px";

  star.style.display =
    "block";

}


/* =========================================================
   CATCH STAR
========================================================= */

function catchStar(){

  if(!gameRunning){

    return;

  }

  if(currentScreen !== 5){

    return;

  }

  score++;

  document.getElementById("score").textContent =
    String(score);

  document.getElementById("fill").style.width =
    ((score / 7) * 100) + "%";

  if(score >= 7){

    stopGame();

    document.getElementById("star").style.display =
      "none";

    document.getElementById("gameMsg").textContent =
      "GIFT UNLOCKED! 🎁✨";

    confetti();

    setTimeout(function(){

      if(currentScreen === 5){

        /*
         * Go to GIFT UNLOCKED screen first.
         */

        go(6);

      }

    },700);

  }else{

    moveStar();

  }

}


/* =========================================================
   NO BUTTON
========================================================= */

function nope(){

  noCount++;

  var button =
    document.getElementById("noBtn");

  var message =
    document.getElementById("noMsg");

  var messages = [

    "nice try 😭",

    "you really chose NO? 💀",

    "think again 👀",

    "that button is getting suspiciously hard to click 😭",

    "we both know you're just testing me 💗"

  ];

  var index =
    Math.min(
      noCount - 1,
      messages.length - 1
    );

  message.textContent =
    messages[index];

  /*
   * Keep the button inside the card.
   */

  var x =
    (Math.random() * 100) - 50;

  var y =
    (Math.random() * 50) - 25;

  button.style.transform =
    "translate(" +
    x +
    "px," +
    y +
    "px)";

}


/* =========================================================
   YES BUTTON
========================================================= */

function yes(){

  confetti();

  setTimeout(function(){

    go(9);

  },250);

}


/* =========================================================
   SCRATCH CARD VARIABLES
========================================================= */

var scratchStarted = false;

var scratchCanvas = null;

var scratchCtx = null;

var scratchDown = false;

var scratchPixels = 0;

var scratchLastX = 0;

var scratchLastY = 0;


/* =========================================================
   INITIALIZE SCRATCH CARD
========================================================= */

function initScratch(){

  /*
   * Prevent duplicate event listeners.
   */

  if(scratchStarted){

    /*
     * If returning to the scratch screen,
     * make sure canvas remains hidden if already completed.
     */

    return;

  }

  scratchCanvas =
    document.getElementById("scratchCanvas");

  if(!scratchCanvas){

    return;

  }

  var card =
    scratchCanvas.parentNode;

  var width =
    card.clientWidth;

  var height =
    card.clientHeight;

  if(width <= 0 || height <= 0){

    setTimeout(function(){

      initScratch();

    },200);

    return;

  }

  scratchStarted = true;

  scratchCanvas.width =
    width;

  scratchCanvas.height =
    height;

  scratchCanvas.style.width =
    width + "px";

  scratchCanvas.style.height =
    height + "px";

  scratchCtx =
    scratchCanvas.getContext("2d");

  if(!scratchCtx){

    scratchStarted = false;

    return;

  }

  scratchPixels = 0;

  scratchCanvas.style.display =
    "block";

  drawScratchLayer(
    width,
    height
  );

  /*
   * iOS 12 Safari compatibility:
   *
   * Do NOT rely on Pointer Events.
   *
   * Use touch + mouse events.
   */

  scratchCanvas.addEventListener(
    "touchstart",
    scratchTouchStart,
    false
  );

  scratchCanvas.addEventListener(
    "touchmove",
    scratchTouchMove,
    false
  );

  scratchCanvas.addEventListener(
    "touchend",
    scratchTouchEnd,
    false
  );

  scratchCanvas.addEventListener(
    "mousedown",
    scratchMouseDown,
    false
  );

  scratchCanvas.addEventListener(
    "mousemove",
    scratchMouseMove,
    false
  );

  scratchCanvas.addEventListener(
    "mouseup",
    scratchMouseUp,
    false
  );

  scratchCanvas.addEventListener(
    "mouseleave",
    scratchMouseUp,
    false
  );

}


/* =========================================================
   DRAW SCRATCH LAYER
========================================================= */

function drawScratchLayer(
  width,
  height
){

  var gradient =
    scratchCtx.createLinearGradient(
      0,
      0,
      width,
      height
    );

  gradient.addColorStop(
    0,
    "#c8c8d4"
  );

  gradient.addColorStop(
    0.5,
    "#eeeeF4"
  );

  gradient.addColorStop(
    1,
    "#b8b8c7"
  );

  scratchCtx.globalCompositeOperation =
    "source-over";

  scratchCtx.fillStyle =
    gradient;

  scratchCtx.fillRect(
    0,
    0,
    width,
    height
  );

  scratchCtx.fillStyle =
    "rgba(255,255,255,.55)";

  scratchCtx.font =
    "900 22px Arial";

  scratchCtx.textAlign =
    "center";

  scratchCtx.textBaseline =
    "middle";

  scratchCtx.fillText(
    "SCRATCH ME ✨",
    width / 2,
    height / 2 - 15
  );

  scratchCtx.font =
    "14px Arial";

  scratchCtx.fillText(
    "something is hidden underneath 👀",
    width / 2,
    height / 2 + 20
  );

}


/* =========================================================
   TOUCH START
========================================================= */

function scratchTouchStart(event){

  event.preventDefault();

  if(
    !event.touches ||
    !event.touches.length
  ){

    return;

  }

  scratchDown = true;

  var touch =
    event.touches[0];

  scratchLastX =
    touch.clientX;

  scratchLastY =
    touch.clientY;

  scratchAt(
    touch.clientX,
    touch.clientY
  );

}


/* =========================================================
   TOUCH MOVE
========================================================= */

function scratchTouchMove(event){

  event.preventDefault();

  if(!scratchDown){

    return;

  }

  if(
    !event.touches ||
    !event.touches.length
  ){

    return;

  }

  var touch =
    event.touches[0];

  scratchLine(
    scratchLastX,
    scratchLastY,
    touch.clientX,
    touch.clientY
  );

  scratchLastX =
    touch.clientX;

  scratchLastY =
    touch.clientY;

}


/* =========================================================
   TOUCH END
========================================================= */

function scratchTouchEnd(event){

  event.preventDefault();

  scratchDown = false;

  checkScratch();

}


/* =========================================================
   MOUSE DOWN
========================================================= */

function scratchMouseDown(event){

  event.preventDefault();

  scratchDown = true;

  scratchLastX =
    event.clientX;

  scratchLastY =
    event.clientY;

  scratchAt(
    event.clientX,
    event.clientY
  );

}


/* =========================================================
   MOUSE MOVE
========================================================= */

function scratchMouseMove(event){

  if(!scratchDown){

    return;

  }

  event.preventDefault();

  scratchLine(
    scratchLastX,
    scratchLastY,
    event.clientX,
    event.clientY
  );

  scratchLastX =
    event.clientX;

  scratchLastY =
    event.clientY;

}


/* =========================================================
   MOUSE UP
========================================================= */

function scratchMouseUp(){

  if(!scratchDown){

    return;

  }

  scratchDown = false;

  checkScratch();

}


/* =========================================================
   SCRATCH SINGLE POINT
========================================================= */

function scratchAt(
  clientX,
  clientY
){

  if(
    !scratchCtx ||
    !scratchCanvas
  ){

    return;

  }

  var rect =
    scratchCanvas.getBoundingClientRect();

  var x =
    clientX - rect.left;

  var y =
    clientY - rect.top;

  scratchCtx.globalCompositeOperation =
    "destination-out";

  scratchCtx.beginPath();

  scratchCtx.arc(
    x,
    y,
    25,
    0,
    Math.PI * 2
  );

  scratchCtx.fill();

  scratchPixels++;

  if(scratchPixels % 5 === 0){

    checkScratch();

  }

}


/* =========================================================
   SCRATCH LINE
========================================================= */

function scratchLine(
  fromX,
  fromY,
  toX,
  toY
){

  if(
    !scratchCtx ||
    !scratchCanvas
  ){

    return;

  }

  var rect =
    scratchCanvas.getBoundingClientRect();

  var x1 =
    fromX - rect.left;

  var y1 =
    fromY - rect.top;

  var x2 =
    toX - rect.left;

  var y2 =
    toY - rect.top;

  scratchCtx.globalCompositeOperation =
    "destination-out";

  scratchCtx.lineWidth =
    50;

  scratchCtx.lineCap =
    "round";

  scratchCtx.lineJoin =
    "round";

  scratchCtx.beginPath();

  scratchCtx.moveTo(
    x1,
    y1
  );

  scratchCtx.lineTo(
    x2,
    y2
  );

  scratchCtx.stroke();

  scratchPixels++;

  if(scratchPixels % 5 === 0){

    checkScratch();

  }

}


/* =========================================================
   CHECK SCRATCH PROGRESS
========================================================= */

function checkScratch(){

  if(
    !scratchCtx ||
    !scratchCanvas
  ){

    return;

  }

  /*
   * Already revealed.
   */

  if(
    scratchCanvas.style.display ===
    "none"
  ){

    return;

  }

  var data =
    scratchCtx.getImageData(
      0,
      0,
      scratchCanvas.width,
      scratchCanvas.height
    ).data;

  var clear = 0;

  var total =
    data.length / 4;

  var i;

  /*
   * Check alpha channel.
   *
   * Alpha 0 = scratched away.
   */

  for(
    i = 3;
    i < data.length;
    i += 4
  ){

    if(data[i] < 40){

      clear++;

    }

  }

  var percentage =
    clear / total;

  /*
   * Reveal after 35% is scratched.
   */

  if(percentage > 0.35){

    scratchCanvas.style.display =
      "none";

    document.getElementById(
      "scratchMsg"
    ).textContent =
      "You found it 😭💗 Now answer honestly...";

    var input =
      document.getElementById(
        "giftAnswer"
      );

    if(input){

      setTimeout(function(){

        input.focus();

      },100);

    }

  }

}


/* =========================================================
   GIFT ANSWER INPUT
========================================================= */

function setupGiftInput(){

  var input =
    document.getElementById(
      "giftAnswer"
    );

  var button =
    document.getElementById(
      "scratchNext"
    );

  if(
    !input ||
    !button
  ){

    return;

  }

  input.addEventListener(
    "input",
    function(){

      var ready =
        input.value
          .replace(/^\s+|\s+$/g,"")
          .length > 0;

      button.disabled =
        !ready;

      if(ready){

        button.classList.add(
          "ready"
        );

      }else{

        button.classList.remove(
          "ready"
        );

      }

    },
    false
  );

  /*
   * Also support pressing Enter.
   */

  input.addEventListener(
    "keydown",
    function(event){

      if(event.key === "Enter"){

        event.preventDefault();

        if(!button.disabled){

          saveGiftAnswer();

        }

      }

    },
    false
  );

}


/* =========================================================
   SEND GIFT ANSWER
========================================================= */

function saveGiftAnswer(){

  if(giftSubmitted){

    return;

  }

  var input =
    document.getElementById(
      "giftAnswer"
    );

  var button =
    document.getElementById(
      "scratchNext"
    );

  var status =
    document.getElementById(
      "submitStatus"
    );

  if(
    !input ||
    !button ||
    !status
  ){

    return;

  }

  var answer =
    input.value
      .replace(/^\s+|\s+$/g,"");

  if(!answer){

    input.focus();

    return;

  }

  /*
   * Prevent double-clicks.
   */

  giftSubmitted = true;

  button.disabled = true;

  button.classList.remove(
    "ready"
  );

  button.textContent =
    "SENDING... 💗";

  status.textContent =
    "Sending your answer... 👀";

  /*
   * Use text/plain so this remains
   * a simple cross-origin request.
   *
   * no-cors prevents Google Apps Script's
   * redirect/CORS response from making a
   * successful request look like a failure.
   */

  var payload = {

    answer:answer,

    page:
      window.location.href,

    submittedAt:
      new Date().toISOString()

  };

  fetch(
    ANSWER_ENDPOINT,
    {
      method:"POST",

      mode:"no-cors",

      headers:{
        "Content-Type":
          "text/plain;charset=utf-8"
      },

      body:
        JSON.stringify(payload)
    }
  )
  .then(function(){

    /*
     * We cannot inspect the response in
     * no-cors mode, but the POST request
     * has been sent.
     */

    document.getElementById(
      "submitStatus"
    ).textContent =
      "Answer sent 💗";

    button.textContent =
      "SENT 💗";

    confetti();

    setTimeout(function(){

      /*
       * IMPORTANT:
       *
       * Scratch card is Screen 7.
       * After submitting, go to Screen 8.
       */

      go(8);

    },800);

  })
  .catch(function(error){

    console.error(
      "Gift answer submission error:",
      error
    );

    /*
     * Allow another attempt.
     */

    giftSubmitted = false;

    button.disabled = false;

    button.classList.add(
      "ready"
    );

    button.textContent =
      "TRY AGAIN 💗";

    status.textContent =
      "Something went wrong 😭 Please try again.";

  });

}


/* =========================================================
   CONFETTI / HEART BURST
========================================================= */

function confetti(){

  var box =
    document.getElementById(
      "hearts"
    );

  var symbols = [

    "💗",
    "💖",
    "✨",
    "🎉",
    "⭐"

  ];

  var i;

  for(
    i = 0;
    i < 38;
    i++
  ){

    var heart =
      document.createElement(
        "div"
      );

    heart.className =
      "heart";

    heart.textContent =
      symbols[
        Math.floor(
          Math.random() *
          symbols.length
        )
      ];

    heart.style.left =
      "50%";

    heart.style.top =
      "50%";

    heart.style.setProperty(
      "--x",
      (Math.random() * 650 - 325) +
      "px"
    );

    heart.style.setProperty(
      "--y",
      (Math.random() * 700 - 350) +
      "px"
    );

    box.appendChild(
      heart
    );

    setTimeout(
      (function(item){

        return function(){

          if(item.parentNode){

            item.parentNode.removeChild(
              item
            );

          }

        };

      })(heart),
      1300
    );

  }

}


/* =========================================================
   PAGE INITIALIZATION
========================================================= */

document.addEventListener(
  "DOMContentLoaded",
  function(){

    setupGiftInput();

  },
  false
);

</script>

</body>
</html>
```