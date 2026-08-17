# when-you-have-nothing-to-do
<!DOCTYPE html>
<html>
<head>
  <title>Catch the Box</title>
  <style>
    body {
      text-align: center;
      font-family: Arial;
      background: #111;
      color: white;
    }

    #game {
      width: 350px;
      height: 500px;
      background: #222;
      margin: 20px auto;
      position: relative;
      overflow: hidden;
    }

    #box {
      width: 50px;
      height: 50px;
      background: red;
      position: absolute;
      cursor: pointer;
    }
  </style>
</head>

<body>

<h1>🎯 Catch the Box</h1>
<p>Score: <span id="score">0</span></p>

<div id="game">
  <div id="box"></div>
</div>

<script>
let score = 0;

const box = document.getElementById("box");
const game = document.getElementById("game");

box.onclick = function() {
  score++;
  document.getElementById("score").textContent = score;

  let x = Math.random() * (game.clientWidth - 50);
  let y = Math.random() * (game.clientHeight - 50);

  box.style.left = x + "px";
  box.style.top = y + "px";
};
</script>

</body>
</html>