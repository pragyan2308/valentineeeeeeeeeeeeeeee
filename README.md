<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Udit, Will You Be My Valentine?</title>

<style>
body {
    margin: 0;
    min-height: 100vh;
    background: linear-gradient(135deg, #ff9aa2, #ffd1dc);
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Comic Sans MS', cursive;
}

.card {
    background: white;
    padding: 25px;
    border-radius: 25px;
    text-align: center;
    box-shadow: 0 15px 40px rgba(0,0,0,0.25);
    width: 90%;
    max-width: 360px;
}

h1 {
    color: #ff2f68;
}

p {
    color: #ff5c8a;
    font-size: 18px;
}

.cat-gif {
    width: 180px;
    border-radius: 20px;
    margin: 10px 0;
}

button {
    padding: 12px 25px;
    border: none;
    border-radius: 25px;
    font-size: 18px;
    cursor: pointer;
    margin: 8px;
    transition: 0.3s;
}

.yes {
    background: #ff2f68;
    color: white;
}

.no {
    background: #ffe0ea;
    color: #ff2f68;
}

.message {
    display: none;
    margin-top: 15px;
    font-size: 20px;
    color: #ff2f68;
}
</style>
</head>

<body>

<div class="card">
    <h1>Udit 💕</h1>
    <p>Will you be my Valentine? 💌</p>

    <img id="catImg" class="cat-gif"
    src="https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif">

    <div>
        <button class="yes" onclick="yesClicked()">Yes 😻</button>
        <button class="no" onclick="noClicked()">No 🙀</button>
    </div>

    <div class="message" id="loveMessage"></div>
</div>

<audio autoplay loop>
  <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3">
</audio>

<script>
let noCount = 0;

function yesClicked() {
    document.getElementById("loveMessage").style.display = "block";
    document.getElementById("loveMessage").innerHTML =
        "YAYYY!!! 💖<br>Udit, you’re officially my Valentine 😽🐾";
}

function noClicked() {
    noCount++;

    const msg = document.getElementById("loveMessage");
    const cat = document.getElementById("catImg");
    msg.style.display = "block";

    if (noCount === 1) {
        msg.innerHTML = "Excuse me? 😼 Try again.";
        cat.src = "https://media.giphy.com/media/mlvseq9yvZhba/giphy.gif";
    }
    else if (noCount === 2) {
        msg.innerHTML = "Udit pls… cat is judging you 🐱👀";
        cat.src = "https://media.giphy.com/media/3oriO0OEd9QIDdllqo/giphy.gif";
    }
    else if (noCount === 3) {
        msg.innerHTML = "Okay now this is illegal 😤💔";
        cat.src = "https://media.giphy.com/media/l1J9u3TZfpmeDLkD6/giphy.gif";
    }
    else {
        msg.innerHTML = "Decision revoked 😌💘<br>You’re my Valentine now.";
        cat.src = "https://media.giphy.com/media/JIX9t2j0ZTN9S/giphy.gif";
    }
}
</script>

</body>
</html>
