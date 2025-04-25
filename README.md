<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Beauty Vocabulary Practice</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #fdf6f0;
      padding: 20px;
    }
    h1 {
      color: #b561a8;
    }
    .wordbank, .exercise {
      background-color: #fff;
      padding: 15px;
      margin-bottom: 20px;
      border-radius: 10px;
      box-shadow: 0 2px 5px rgba(0,0,0,0.1);
    }
    input[type="text"] {
      padding: 5px;
      border-radius: 5px;
      border: 1px solid #ccc;
      width: 150px;
    }
    .correct {
      background-color: #c8f7c5;
    }
    .incorrect {
      background-color: #f7c5c5;
    }
    button {
      margin-top: 10px;
      padding: 10px 20px;
      background-color: #b561a8;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
  </style>
</head>
<body>
  <h1>Beauty Vocabulary Practice</h1>

  <div class="wordbank">
    <h2>Word Bank</h2>
    <p>hairdresser, stylist, appointment, mirror, scissors, comb, blow-dry, shampoo, conditioner, trim, layers, bangs, ponytail, braid, curly</p>
  </div>

  <div class="exercise">
    <h2>Fill in the Gaps</h2>
    <ol>
      <li>The ___ trimmed my hair. <input type="text" id="q1"></li>
      <li>My ___ suggested a new haircut. <input type="text" id="q2"></li>
      <li>I booked an ___ for 3 PM. <input type="text" id="q3"></li>
      <li>She looked in the ___ after her haircut. <input type="text" id="q4"></li>
      <li>The hairdresser used ___ to trim my bangs. <input type="text" id="q5"></li>
      <li>The stylist used a ___ before cutting. <input type="text" id="q6"></li>
      <li>Can you ___ my hair straight? <input type="text" id="q7"></li>
      <li>They used a nice-smelling ___. <input type="text" id="q8"></li>
      <li>Apply ___ after shampooing. <input type="text" id="q9"></li>
      <li>I just need a ___ today. <input type="text" id="q10"></li>
    </ol>
    <button onclick="checkAnswers()">Check Your Answers</button>
  </div>

  <script>
    const answers = [
      "hairdresser",
      "stylist",
      "appointment",
      "mirror",
      "scissors",
      "comb",
      "blow-dry",
      "shampoo",
      "conditioner",
      "trim"
    ];

    function checkAnswers() {
      for (let i = 0; i < answers.length; i++) {
        const input = document.getElementById(`q${i+1}`);
        if (input.value.trim().toLowerCase() === answers[i]) {
          input.className = "correct";
        } else {
          input.className = "incorrect";
        }
      }
    }
  </script>
</body>
</html>
