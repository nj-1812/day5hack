00 — V Anushree — index.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSE Toolbox</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container wide">
    <h1>🧰 CSE Toolbox</h1>
    <p>17 mini apps built by the CSE Hackathon Bootcamp class</p>

    <div class="grid">
      <a href="clock.html">⏰ Digital Clock</a>
      <a href="counter.html">🔢 Counter</a>
      <a href="calculator.html">➗ Calculator</a>
      <a href="bmi.html">⚖️ BMI Calculator</a>
      <a href="age.html">🎂 Age Calculator</a>
      <a href="dice.html">🎲 Dice Roller</a>
      <a href="coin.html">🪙 Coin Toss</a>
      <a href="temperature.html">🌡️ Temperature</a>
      <a href="quotes.html">💬 Quotes</a>
      <a href="todo.html">✅ To-Do List</a>
      <a href="stopwatch.html">⏱️ Stopwatch</a>
      <a href="password.html">🔐 Password Maker</a>
      <a href="charcount.html">🔤 Character Counter</a>
      <a href="table.html">✖️ Times Table</a>
      <a href="guess.html">🎯 Guess the Number</a>
      <a href="mood.html">😊 Mood Picker</a>
      <a href="bill.html">🧾 Bill Splitter</a>
      <a href="about.html">👥 Meet the Team</a>
    </div>

    <p class="credit">Home page built by V Anushree</p>
  </div>
</body>
</html>
01 — Akaansha Vikram — style.css
css
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap");

/* Shared design for CSE Toolbox – built by Akaansha Vikram */

* {
  box-sizing: border-box;
}

body {
  margin: 0;
  min-height: 100vh;
  font-family: "Poppins", Arial, sans-serif;
  background: linear-gradient(135deg, #667eea, #764ba2);
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 40px 15px;
}

.container {
  background: white;
  width: 100%;
  max-width: 420px;
  padding: 30px;
  border-radius: 20px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.25);
  text-align: center;
}

.wide {
  max-width: 800px;
}

h1 {
  color: #4f46e5;
  font-size: 26px;
}

input,
textarea {
  width: 100%;
  padding: 10px;
  margin: 6px 0;
  font-family: inherit;
  font-size: 16px;
  border: 2px solid #e5e7eb;
  border-radius: 10px;
}

button {
  padding: 10px 18px;
  margin: 5px;
  font-family: inherit;
  font-size: 16px;
  font-weight: 600;
  color: white;
  background: linear-gradient(135deg, #667eea, #764ba2);
  border: none;
  border-radius: 10px;
  cursor: pointer;
}

button:hover {
  opacity: 0.85;
}

.result {
  font-size: 22px;
  font-weight: 600;
  color: #4338ca;
  margin-top: 15px;
}

.big {
  font-size: 60px;
  font-weight: 700;
  color: #4f46e5;
  margin: 15px 0;
}

.back {
  display: inline-block;
  margin-bottom: 10px;
  color: #764ba2;
  text-decoration: none;
  font-weight: 600;
}

.credit {
  margin-top: 25px;
  font-size: 13px;
  color: #6b7280;
}

ul {
  list-style: none;
  padding: 0;
  text-align: left;
}

li {
  padding: 8px 12px;
  margin: 6px 0;
  background: #f3f4f6;
  border-radius: 8px;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
  gap: 12px;
}

.grid a {
  display: block;
  padding: 18px 10px;
  background: #eef2ff;
  color: #4338ca;
  border-radius: 12px;
  text-decoration: none;
  font-weight: 600;
}

.grid a:hover {
  background: #e0e7ff;
}
02 — S Krishitha — clock.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Digital Clock</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>⏰ Digital Clock</h1>
    <div class="big" id="time"></div>
    <p id="date"></p>
    <p class="credit">Built by S Krishitha</p>
  </div>

  <script>
    function showTime() {
      const now = new Date();
      document.querySelector("#time").textContent = now.toLocaleTimeString();
      document.querySelector("#date").textContent = now.toDateString();
    }

    showTime();
    setInterval(showTime, 1000);
  </script>
</body>
</html>
03 — Harshini S — counter.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Counter</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🔢 Counter</h1>
    <div class="big" id="count">0</div>
    <button id="minus">−</button>
    <button id="reset">Reset</button>
    <button id="plus">+</button>
    <p class="credit">Built by Harshini S</p>
  </div>

  <script>
    let count = 0;
    const display = document.querySelector("#count");

    document.querySelector("#plus").addEventListener("click", () => {
      count++;
      display.textContent = count;
    });

    document.querySelector("#minus").addEventListener("click", () => {
      if (count > 0) {
        count--;
        display.textContent = count;
      }
    });

    document.querySelector("#reset").addEventListener("click", () => {
      count = 0;
      display.textContent = count;
    });
  </script>
</body>
</html>
04 — Sanjay D S — calculator.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>➗ Calculator</h1>
    <input id="a" type="number" placeholder="First number">
    <input id="b" type="number" placeholder="Second number">
    <button onclick="calculate('+')">+</button>
    <button onclick="calculate('-')">−</button>
    <button onclick="calculate('*')">×</button>
    <button onclick="calculate('/')">÷</button>
    <div class="result" id="result"></div>
    <p class="credit">Built by Sanjay D S</p>
  </div>

  <script>
    function calculate(op) {
      const a = Number(document.querySelector("#a").value);
      const b = Number(document.querySelector("#b").value);
      let answer;

      if (op === "+") answer = a + b;
      if (op === "-") answer = a - b;
      if (op === "*") answer = a * b;
      if (op === "/") {
        answer = (b === 0) ? "Cannot divide by zero" : a / b;
      }

      document.querySelector("#result").textContent = "Result: " + answer;
    }
  </script>
</body>
</html>
05 — Kandakuri Sirivani Swathi — bmi.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>BMI Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>⚖️ BMI Calculator</h1>
    <input id="weight" type="number" placeholder="Weight (kg)">
    <input id="height" type="number" placeholder="Height (cm)">
    <button id="calcBtn">Calculate</button>
    <div class="result" id="result"></div>
    <p class="credit">Built by Kandakuri Sirivani Swathi</p>
  </div>

  <script>
    document.querySelector("#calcBtn").addEventListener("click", () => {
      const weight = Number(document.querySelector("#weight").value);
      const height = Number(document.querySelector("#height").value) / 100;

      if (weight <= 0 || height <= 0) {
        document.querySelector("#result").textContent = "Please enter valid values";
        return;
      }

      const bmi = weight / (height * height);
      let category;

      if (bmi < 18.5) category = "Underweight";
      else if (bmi < 25) category = "Normal";
      else if (bmi < 30) category = "Overweight";
      else category = "Obese";

      document.querySelector("#result").textContent =
        "BMI: " + bmi.toFixed(1) + " (" + category + ")";
    });
  </script>
</body>
</html>
06 — Joshika R — age.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Age Calculator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🎂 Age Calculator</h1>
    <input id="dob" type="date">
    <button id="calcBtn">Find My Age</button>
    <div class="result" id="result"></div>
    <p class="credit">Built by Joshika R</p>
  </div>

  <script>
    document.querySelector("#calcBtn").addEventListener("click", () => {
      const value = document.querySelector("#dob").value;

      if (value === "") {
        document.querySelector("#result").textContent = "Please pick your birth date";
        return;
      }

      const birth = new Date(value);
      const today = new Date();
      let age = today.getFullYear() - birth.getFullYear();
      const monthDiff = today.getMonth() - birth.getMonth();

      if (monthDiff < 0 || (monthDiff === 0 && today.getDate() < birth.getDate())) {
        age--;
      }

      document.querySelector("#result").textContent = "You are " + age + " years old";
    });
  </script>
</body>
</html>
07 — Dill Anto Jason C — dice.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Dice Roller</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🎲 Dice Roller</h1>
    <div class="big" id="dice">⚀</div>
    <button id="rollBtn">Roll</button>
    <div class="result" id="result"></div>
    <p class="credit">Built by Dill Anto Jason C</p>
  </div>

  <script>
    const faces = ["⚀", "⚁", "⚂", "⚃", "⚄", "⚅"];

    document.querySelector("#rollBtn").addEventListener("click", () => {
      const index = Math.floor(Math.random() * 6);
      document.querySelector("#dice").textContent = faces[index];
      document.querySelector("#result").textContent = "You rolled " + (index + 1);
    });
  </script>
</body>
</html>
08 — Nirupam S — coin.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Coin Toss</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🪙 Coin Toss</h1>
    <div class="big" id="coin">?</div>
    <button id="tossBtn">Toss</button>
    <p id="score">Heads: 0 | Tails: 0</p>
    <p class="credit">Built by Nirupam S</p>
  </div>

  <script>
    let heads = 0;
    let tails = 0;

    document.querySelector("#tossBtn").addEventListener("click", () => {
      if (Math.random() < 0.5) {
        heads++;
        document.querySelector("#coin").textContent = "Heads";
      } else {
        tails++;
        document.querySelector("#coin").textContent = "Tails";
      }

      document.querySelector("#score").textContent =
        "Heads: " + heads + " | Tails: " + tails;
    });
  </script>
</body>
</html>
09 — Nirmal Kumar Vandhana Shree — temperature.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Temperature Converter</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🌡️ Temperature Converter</h1>
    <input id="temp" type="number" placeholder="Enter temperature">
    <button id="toF">°C → °F</button>
    <button id="toC">°F → °C</button>
    <div class="result" id="result"></div>
    <p class="credit">Built by Nirmal Kumar Vandhana Shree</p>
  </div>

  <script>
    const input = document.querySelector("#temp");
    const result = document.querySelector("#result");

    document.querySelector("#toF").addEventListener("click", () => {
      if (input.value === "") return;
      const f = Number(input.value) * 9 / 5 + 32;
      result.textContent = input.value + "°C = " + f.toFixed(1) + "°F";
    });

    document.querySelector("#toC").addEventListener("click", () => {
      if (input.value === "") return;
      const c = (Number(input.value) - 32) * 5 / 9;
      result.textContent = input.value + "°F = " + c.toFixed(1) + "°C";
    });
  </script>
</body>
</html>
10 — Jonish Manojin AG — quotes.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Quote Generator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>💬 Daily Motivation</h1>
    <p class="result" id="quote">Click for a quote!</p>
    <button id="quoteBtn">New Quote</button>
    <p class="credit">Built by Jonish Manojin AG</p>
  </div>

  <script>
    const quotes = [
      "Every expert was once a beginner.",
      "Bugs are just lessons in disguise.",
      "Small steps every day lead to big results.",
      "Code a little, learn a lot.",
      "Mistakes mean you are trying.",
      "Your first project does not need to be perfect, it needs to be finished.",
      "Curiosity is the best programming language."
    ];

    document.querySelector("#quoteBtn").addEventListener("click", () => {
      const index = Math.floor(Math.random() * quotes.length);
      document.querySelector("#quote").textContent = quotes[index];
    });
  </script>
</body>
</html>
11 — Bavathaarini NS — todo.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>✅ To-Do List</h1>
    <input id="taskInput" type="text" placeholder="Type a task">
    <button id="addBtn">Add Task</button>
    <ul id="list"></ul>
    <p>Click a task to remove it.</p>
    <p class="credit">Built by Bavathaarini NS</p>
  </div>

  <script>
    const input = document.querySelector("#taskInput");
    const list = document.querySelector("#list");

    document.querySelector("#addBtn").addEventListener("click", () => {
      const task = input.value.trim();
      if (task === "") return;

      const li = document.createElement("li");
      li.textContent = task;
      li.style.cursor = "pointer";
      li.addEventListener("click", () => li.remove());

      list.appendChild(li);
      input.value = "";
    });
  </script>
</body>
</html>
12 — Viswaa S — stopwatch.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Stopwatch</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>⏱️ Stopwatch</h1>
    <div class="big" id="display">00:00</div>
    <button id="startBtn">Start</button>
    <button id="stopBtn">Stop</button>
    <button id="resetBtn">Reset</button>
    <p class="credit">Built by Viswaa S</p>
  </div>

  <script>
    let seconds = 0;
    let timer = null;
    const display = document.querySelector("#display");

    function show() {
      const m = Math.floor(seconds / 60);
      const s = seconds % 60;
      display.textContent = String(m).padStart(2, "0") + ":" + String(s).padStart(2, "0");
    }

    document.querySelector("#startBtn").addEventListener("click", () => {
      if (timer !== null) return;
      timer = setInterval(() => {
        seconds++;
        show();
      }, 1000);
    });

    document.querySelector("#stopBtn").addEventListener("click", () => {
      clearInterval(timer);
      timer = null;
    });

    document.querySelector("#resetBtn").addEventListener("click", () => {
      clearInterval(timer);
      timer = null;
      seconds = 0;
      show();
    });
  </script>
</body>
</html>
13 — Jesu Ronith — password.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Password Generator</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🔐 Password Generator</h1>
    <input id="length" type="number" value="12" min="4" max="32">
    <button id="genBtn">Generate</button>
    <div class="result" id="password"></div>
    <p class="credit">Built by Jesu Ronith</p>
  </div>

  <script>
    const chars = "ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789!@#$%&*";

    document.querySelector("#genBtn").addEventListener("click", () => {
      const length = Number(document.querySelector("#length").value);

      if (length < 4 || length > 32) {
        document.querySelector("#password").textContent = "Choose a length from 4 to 32";
        return;
      }

      let password = "";
      for (let i = 0; i < length; i++) {
        const index = Math.floor(Math.random() * chars.length);
        password = password + chars[index];
      }

      document.querySelector("#password").textContent = password;
    });
  </script>
</body>
</html>
14 — S S Padmasree — charcount.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Character Counter</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🔤 Character Counter</h1>
    <textarea id="text" rows="6" placeholder="Start typing..."></textarea>
    <div class="result" id="stats">Characters: 0 | Words: 0</div>
    <p class="credit">Built by S S Padmasree</p>
  </div>

  <script>
    document.querySelector("#text").addEventListener("input", (event) => {
      const text = event.target.value;
      const chars = text.length;
      const words = text.trim() === "" ? 0 : text.trim().split(/\s+/).length;

      document.querySelector("#stats").textContent =
        "Characters: " + chars + " | Words: " + words;
    });
  </script>
</body>
</html>
15 — R Manmohan — table.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Times Table</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>✖️ Times Table</h1>
    <input id="number" type="number" placeholder="Enter a number">
    <button id="showBtn">Show Table</button>
    <ul id="list"></ul>
    <p class="credit">Built by R Manmohan</p>
  </div>

  <script>
    document.querySelector("#showBtn").addEventListener("click", () => {
      const n = Number(document.querySelector("#number").value);
      const list = document.querySelector("#list");
      list.innerHTML = "";

      for (let i = 1; i <= 10; i++) {
        const li = document.createElement("li");
        li.textContent = n + " × " + i + " = " + (n * i);
        list.appendChild(li);
      }
    });
  </script>
</body>
</html>
16 — Sahanaa D P — guess.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Guess the Number</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🎯 Guess the Number</h1>
    <p>I'm thinking of a number from 1 to 20.</p>
    <input id="guess" type="number" placeholder="Your guess">
    <button id="guessBtn">Guess</button>
    <div class="result" id="message"></div>
    <p id="attempts">Attempts: 0</p>
    <p class="credit">Built by Sahanaa D P</p>
  </div>

  <script>
    let secret = Math.floor(Math.random() * 20) + 1;
    let attempts = 0;
    const message = document.querySelector("#message");

    document.querySelector("#guessBtn").addEventListener("click", () => {
      const guess = Number(document.querySelector("#guess").value);

      if (guess < 1 || guess > 20) {
        message.textContent = "Enter a number from 1 to 20";
        return;
      }

      attempts++;
      document.querySelector("#attempts").textContent = "Attempts: " + attempts;

      if (guess === secret) {
        message.textContent = "🎉 Correct! It was " + secret + ". New game started.";
        secret = Math.floor(Math.random() * 20) + 1;
        attempts = 0;
      } else if (guess < secret) {
        message.textContent = "Too low ⬆️";
      } else {
        message.textContent = "Too high ⬇️";
      }
    });
  </script>
</body>
</html>
17 — Natasha Amalie — mood.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mood Picker</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>😊 Mood Picker</h1>
    <p>How are you feeling today?</p>
    <button onclick="setMood('😄', 'Happy! Keep shining.', '#fde68a')">😄</button>
    <button onclick="setMood('😴', 'Tired? Take a short break.', '#c7d2fe')">😴</button>
    <button onclick="setMood('😤', 'Stressed? Breathe and take one step at a time.', '#fecaca')">😤</button>
    <button onclick="setMood('🤩', 'Excited! Go build something.', '#bbf7d0')">🤩</button>
    <div class="big" id="emoji"></div>
    <div class="result" id="message"></div>
    <p class="credit">Built by Natasha Amalie</p>
  </div>

  <script>
    function setMood(emoji, message, colour) {
      document.querySelector("#emoji").textContent = emoji;
      document.querySelector("#message").textContent = message;
      document.body.style.background = colour;
    }
  </script>
</body>
</html>
18 — Amirthaa M — bill.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bill Splitter</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container">
    <a class="back" href="index.html">← Home</a>
    <h1>🧾 Bill Splitter</h1>
    <input id="bill" type="number" placeholder="Total bill (₹)">
    <input id="tip" type="number" placeholder="Tip %" value="10">
    <input id="people" type="number" placeholder="Number of people" value="2">
    <button id="splitBtn">Split</button>
    <div class="result" id="result"></div>
    <p class="credit">Built by Amirthaa M</p>
  </div>

  <script>
    document.querySelector("#splitBtn").addEventListener("click", () => {
      const bill = Number(document.querySelector("#bill").value);
      const tip = Number(document.querySelector("#tip").value);
      const people = Number(document.querySelector("#people").value);

      if (bill <= 0 || people <= 0) {
        document.querySelector("#result").textContent = "Enter a valid bill and number of people";
        return;
      }

      const total = bill + (bill * tip / 100);
      const each = total / people;

      document.querySelector("#result").textContent =
        "Total: ₹" + total.toFixed(2) + " | Each pays: ₹" + each.toFixed(2);
    });
  </script>
</body>
</html>
19 — Domi Riya — about.html
html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Meet the Team</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <div class="container wide">
    <a class="back" href="index.html">← Home</a>
    <h1>👥 Meet the Team</h1>
    <p>The 20 builders of CSE Toolbox</p>
    <ul id="team"></ul>
    <p class="credit">Team page built by Domi Riya</p>
  </div>

  <script>
    const team = [
      { name: "V Anushree", work: "Home page" },
      { name: "Akaansha Vikram", work: "Shared design (style.css)" },
      { name: "S Krishitha", work: "Digital Clock" },
      { name: "Harshini S", work: "Counter" },
      { name: "Sanjay D S", work: "Calculator" },
      { name: "Kandakuri Sirivani Swathi", work: "BMI Calculator" },
      { name: "Joshika R", work: "Age Calculator" },
      { name: "Dill Anto Jason C", work: "Dice Roller" },
      { name: "Nirupam S", work: "Coin Toss" },
      { name: "Nirmal Kumar Vandhana Shree", work: "Temperature Converter" },
      { name: "Jonish Manojin AG", work: "Quote Generator" },
      { name: "Bavathaarini NS", work: "To-Do List" },
      { name: "Viswaa S", work: "Stopwatch" },
      { name: "Jesu Ronith", work: "Password Generator" },
      { name: "S S Padmasree", work: "Character Counter" },
      { name: "R Manmohan", work: "Times Table" },
      { name: "Sahanaa D P", work: "Guess the Number" },
      { name: "Natasha Amalie", work: "Mood Picker" },
      { name: "Amirthaa M", work: "Bill Splitter" },
      { name: "Domi Riya", work: "Meet the Team page" }
    ];

    const list = document.querySelector("#team");

    team.forEach((member, index) => {
      const li = document.createElement("li");
      li.textContent = String(index).padStart(2, "0") + " — " + member.name + " · " + member.work;
      list.appendChild(li);
    });
  </script>
</body>
</html>

