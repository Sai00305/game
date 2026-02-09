# game
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Math Quest</title>
<style>
  body {
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }

  .card {
    background: #1e293b;
    padding: 30px;
    width: 350px;
    border-radius: 15px;
    box-shadow: 0 20px 40px rgba(0,0,0,0.4);
    text-align: center;
  }

  h1 {
    margin-bottom: 10px;
    color: #38bdf8;
  }

  input {
    width: 80%;
    padding: 10px;
    border-radius: 8px;
    border: none;
    margin-top: 15px;
    font-size: 16px;
  }

  button {
    margin-top: 15px;
    padding: 10px 25px;
    border: none;
    border-radius: 20px;
    background: #38bdf8;
    color: #000;
    font-size: 16px;
    cursor: pointer;
  }

  button:hover {
    background: #0ea5e9;
  }

  .msg {
    margin-top: 15px;
    font-weight: bold;
  }
</style>
</head>
<body>

<div class="card" id="game">
  <h1>🧠 Math Quest</h1>
  <p>Find the missing number:</p>
  <p><b>2, 6, 12, 20, ?</b></p>
  <input id="answer" placeholder="Enter answer">
  <br>
  <button onclick="check1()">Submit</button>
  <div class="msg" id="msg"></div>
</div>

<script>
function check1() {
  if (document.getElementById("answer").value == "30") {
    document.getElementById("game").innerHTML = `
      <h1>✅ Correct!</h1>
      <p>Digits add to 9 and differ by 3.</p>
      <p><b>Which two-digit number?</b></p>
      <input id="answer2">
      <br>
      <button onclick="check2()">Submit</button>
      <div class="msg"></div>
    `;
  } else {
    document.getElementById("msg").innerText = "❌ Try again!";
  }
}

function check2() {
  if (document.getElementById("answer2").value == "63") {
    document.getElementById("game").innerHTML = `
      <h1>🔥 Nice!</h1>
      <p>How many sides do 3 triangles have in total?</p>
      <input id="answer3">
      <br>
      <button onclick="check3()">Submit</button>
    `;
  } else {
    alert("Wrong answer!");
  }
}

function check3() {
  if (document.getElementById("answer3").value == "9") {
    document.getElementById("game").innerHTML = `
      <h1>🎉 Classroom Unlocked!</h1>
      <p style="font-size:22px">🏫 Room Number</p>
      <h1 style="font-size:40px;color:#38bdf8">313</h1>
    `;
  } else {
    alert("Try again!");
  }
}
</script>

</body>
</html>

