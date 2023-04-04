# learn_git
<!DOCTYPE html>
<html lang="en" data-theme="accent-1">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link rel="icon" type="image/png" sizes="32x32" href="./images/favicon-32x32.png">
  <title>Frontend Mentor | Calculator app</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=League+Spartan:wght@700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="styles.css">
  <script src="app.js" defer></script>
  <!-- Feel free to remove these styles or customise in your own stylesheet 👍 -->
  <!-- <style>
    .attribution { font-size: 11px; text-align: center; }
    .attribution a { color: hsl(228, 45%, 44%); }
  </style> -->
</head>

<body>
  <main class="calc__container">

    <!-- Calc head section -->
    <div class="calc__head">
      <h1 class="calc__head-text">calc</h1>
      <div>
        <div class="theme__switch-wrapper">
          <p class="theme__tag">THEME</p>
          <div class="theme__switcher">
            <span class="theme__tag theme__number">12</span>
            <label class="switch">
              <input type="checkbox">
              <span class="slider round"></span>
            </label>
          </div>
        </div>
      </div>
    </div>

    <!-- Calc screen -->
    <input class="screen" type="text"></input>

    <!-- Calc btns -->
    <div class="calc__btns">
      <button class="btn btn-9" value="9">9</button>
      <button class="btn btn-8" value="8">8</button>
      <button class="btn btn-7" value="7">7</button>
      <button class="btn btn-6" value="6">6</button>
      <button class="btn btn-5" value="5">5</button>
      <button class="btn btn-4" value="4">4</button>
      <button class="btn btn-3" value="3">3</button>
      <button class="btn btn-2" value="2">2</button>
      <button class="btn btn-1" value="1">1</button>
      <button class="btn btn-0" value="0">0</button>
      <button class="btn dot">.</button>
      <button class="btn add">+</button>
      <button class="btn sub">-</button>
      <button class="btn multi">*</button>
      <button class="btn div">/</button>
      <button class="del">DEL</button>
      <button class="reset">RESET</button>
      <button class="eval">=</button>
    </div>
  </main>


  <!-- <div class="attribution">
    Challenge by <a href="https://www.frontendmentor.io?ref=challenge" target="_blank">Frontend Mentor</a>.
    Coded by <a href="#">Your Name Here</a>.
  </div> -->
</body>

</html>


:root[data-theme="accent-1"] {
  /* Backgrounds */
  --main-bg: hsl(222, 26%, 31%);
  --toggle-bg: hsl(223, 31%, 20%);
  --screen-bg: hsl(224, 36%, 15%);

  /* Keys */
  --key-bg: hsl(225, 21%, 49%);
  --key-shadow: hsl(224, 28%, 35%);
  --red-key: hsl(6, 63%, 50%);
  --red-key-shadow: hsl(6, 70%, 34%);
  --grey-key: hsl(30, 25%, 89%);
  --grey-key-shadow: hsl(28, 16%, 65%);
  /* Text */
  --text-primary: hsl(221, 14%, 31%);
  --white-btn: hsl(0, 0%, 100%);
  --white: hsl(0, 0%, 100%);

  /* Buttons Shadow */
  --shadow: 0 5px 0 var(--grey-key-shadow);
  --shadow-active: 0 3px 0 var(--grey-key-shadow);
}
:root[data-theme="accent-2"] {
  /* Backgrounds */
  --main-bg: hsl(0, 0%, 90%);
  --toggle-bg: hsl(0, 5%, 81%);
  --screen-bg: hsl(0, 0%, 93%);

  /* Keys */
  --key-bg: hsl(185, 42%, 37%);
  --key-shadow: hsl(185, 58%, 25%);
  --red-key: hsl(25, 98%, 40%);
  --red-key-shadow: hsl(25, 99%, 27%);
  --grey-key: hsl(45, 7%, 89%);
  --grey-key-shadow: hsl(35, 11%, 61%);
  /* Text */
  --text-primary: hsl(60, 10%, 19%);
  --white-btn: hsl(0, 0%, 100%);
  --white: var(--text-primary);

  /* Buttons Shadow */
  --shadow: 0 5px 0 var(--grey-key-shadow);
  --shadow-active: 0 3px 0 var(--grey-key-shadow);
}
html {
  font-size: 62.5%;
}
* {
  font-size: 1.6rem;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  padding: 2em 0;
  background: var(--main-bg);
  font-family: "League Spartan";
}

.calc__container {
  display: flex;
  align-items: center;
  flex-direction: column;
  width: 85%;
  margin: 0 auto;
  max-width: 500px;
}
.calc__head {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  width: 100%;
  color: var(--white);
}
.calc__head-text {
  font-size: 3.2rem;
  line-height: 0;
}
.theme__switch-wrapper {
  display: flex;
  align-items: flex-end;
  gap: 2em;
}
.theme__switcher {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
.theme__tag {
  font-size: 1.3rem;
  color: var(--white);
}
.theme__number {
  letter-spacing: 1.6rem;
  margin-left: auto;
}
.screen {
  all: unset;
  position: relative;
  font-size: 4.5rem;
  color: var(--white);
  text-align: right;
  padding: 3rem;
  width: 100%;
  box-sizing: inherit;
  height: 9rem;
  display: block;
  background: var(--screen-bg);
  margin-top: 3.6rem;
  border-radius: 1rem;
}
.calc__btns {
  display: grid;
  margin-top: 2.4rem;
  grid-template-columns: repeat(4, 1fr);
  grid-template-areas:
    "b-7 b-8 b-9 del"
    "b-4 b-5 b-6 plus"
    "b-1 b-2 b-3 minus"
    "dt b-0 div multi"
    "reset reset  eval eval";
  grid-auto-rows: 5.7rem;
  background: var(--toggle-bg);
  width: 100%;
  border-radius: 1rem;
  gap: clamp(1.2rem, 3.3vw, 2rem);
  padding: 2rem;
}
.calc__btns :is(button) {
  all: unset;
  font-size: 3.2rem;
  background: var(--grey-key);
  text-align: center;
  color: var(--text-primary);
  border-radius: 0.6rem;
  cursor: pointer;
  transition: all 0.3s;
}
.calc__btns :is(button.del, button.reset) {
  box-shadow: 0 4.5px 0 var(--key-shadow);
  color: var(--white-btn);
}
.calc__btns :is(button.del, button.reset):active {
  box-shadow: 0 2px 0 var(--key-shadow);
  opacity: 0.8;
  transform: scale(0.99);
}
.calc__btns :is(button.eval) {
  color: var(--white-btn);
  box-shadow: 0 4.5px 0 var(--red-key-shadow);
  font-size: 1rem;
}
.calc__btns :is(button.eval):active {
  box-shadow: 0 2px 0 var(--red-key-shadow);
  opacity: 0.8;
  transform: scale(0.99);
}
.calc__btns :is(button):not(button.del, button.reset, button.eval) {
  box-shadow: 0 4.5px 0 var(--grey-key-shadow);
}
.calc__btns :is(button):not(button.del, button.reset, button.eval):active {
  box-shadow: 0 2px 0 var(--grey-key-shadow);
  opacity: 0.8;
  transform: scale(0.99);
}
button.del,
button.reset {
  font-size: 2rem;
  background: var(--key-bg);
  color: var(--white);
}
button.eval {
  background: var(--red-key);
  color: var(--white);
}
button.multi {
  font-size: 2rem;
}
button.btn-9 {
  grid-area: b-9;
}
button.btn-8 {
  grid-area: b-8;
}
button.btn-7 {
  grid-area: b-7;
}
button.btn-6 {
  grid-area: b-6;
}
button.btn-5 {
  grid-area: b-5;
}
button.btn-4 {
  grid-area: b-4;
}
button.btn-3 {
  grid-area: b-3;
}
button.btn-2 {
  grid-area: b-2;
}
button.btn-1 {
  grid-area: b-1;
}
button.btn-0 {
  grid-area: b-0;
}
button.eval {
  grid-area: eval;
}
button.reset {
  grid-area: reset;
}
button.del {
  grid-area: del;
}
button.add {
  grid-area: plus;
}
button.sub {
  grid-area: minus;
}
button.multi {
  grid-area: multi;
}
button.div {
  grid-area: div;
}
button.dot {
  grid-area: dt;
}
/* TOGGLE BTN */
.switch {
  position: relative;
  display: inline-block;
  width: 54px;
  height: 28px;
}
.switch input {
  opacity: 0;
  width: 0;
  height: 0;
}
.slider.round {
  position: absolute;
  cursor: pointer;
  inset: 0;
  border-radius: 34px;
  background-color: var(--toggle-bg);
  transition: 0.4s;
}
.slider.round:before {
  position: absolute;
  content: "";
  height: 20px;
  width: 20px;
  left: 4px;
  bottom: 4px;
  border-radius: 50%;
  background-color: var(--red-key);
  transition: 0.4s;
}
input:checked + .slider:before {
  transform: translateX(26px);
}





"use strict";
const btn = document.querySelectorAll(".btn");
const screen = document.querySelector(".screen");
const delBtn = document.querySelector(".del");
const resetBtn = document.querySelector(".reset");
const evalBtn = document.querySelector(".eval");
const themeSlider = document.querySelector(".slider");

//BUTTONS AND SCREEN_OUTPUT
btn.forEach((e) => {
  e.addEventListener("click", (e) => {
    const value = e.target.textContent;
    screen.value += value;
  });
});

//DELETE BTN
delBtn.addEventListener("click", () => {
  const value = screen.value.split("");
  value.pop();
  screen.value = value.join("");
});

//RESET BTN
resetBtn.addEventListener("click", () => {
  screen.value = null;
});

//EVAL BTN
evalBtn.addEventListener("click", () => {
  if (screen.value) {
    screen.value = eval(screen.value);
  } else {
    screen.value = 0;
  }
});

// THEME TOGGLE
themeSlider.addEventListener("click", () => {
  const rootEl = document.documentElement;
  let dataAttr = rootEl.getAttribute("data-theme"),
    switchTheme;

  switchTheme = dataAttr === "accent-1" ? "accent-2" : "accent-1";
  rootEl.setAttribute("data-theme", switchTheme);
});



