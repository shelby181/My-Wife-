<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Juste pour toi ❤️</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    min-height: 100vh;
    overflow-x: hidden;
    font-family: Georgia, serif;
    color: white;
    text-align: center;
    background: linear-gradient(135deg, #090014, #310d2c, #16051f);
}

.container {
    padding: 60px 20px;
    position: relative;
    z-index: 2;
}

h1 {
    font-size: 40px;
    color: #ff9fcb;
    text-shadow: 0 0 15px #ff2e93;
    animation: glow 2s infinite alternate;
}

@keyframes glow {
    from { text-shadow: 0 0 10px #ff2e93; }
    to { text-shadow: 0 0 30px #ff69b4, 0 0 45px white; }
}

.subtitle {
    margin-top: 20px;
    font-size: 18px;
    color: #f8cde5;
}

.heart {
    font-size: 110px;
    margin: 40px 0;
    animation: heartbeat 1.3s infinite;
    filter: drop-shadow(0 0 20px #ff287f);
}

@keyframes heartbeat {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.18); }
}

.card {
    max-width: 500px;
    width: 95%;
    margin: auto;
    padding: 25px;
    border-radius: 25px;
    background: rgba(255,255,255,.08);
    border: 1px solid rgba(255,255,255,.2);
    box-shadow: 0 0 25px rgba(255,50,150,.15);
    line-height: 1.9;
}

button {
    margin: 25px 8px;
    padding: 15px 25px;
    border: none;
    border-radius: 30px;
    background: linear-gradient(45deg, #e91e63, #a60070);
    color: white;
    font-size: 16px;
    font-weight: bold;
    box-shadow: 0 0 20px rgba(255,50,150,.4);
    cursor: pointer;
}

button:active {
    transform: scale(.95);
}

#secret {
    display: none;
    max-width: 500px;
    width: 95%;
    margin: 20px auto;
    padding: 25px;
    border-radius: 20px;
    background: rgba(255,255,255,.12);
    color: #ffc6e4;
    line-height: 2;
    animation: appear 1.2s;
}

@keyframes appear {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
}

.floating-heart {
    position: fixed;
    bottom: -30px;
    color: #ff5b9d;
    pointer-events: none;
    animation: floatUp linear forwards;
    z-index: 1;
}

@keyframes floatUp {
    to {
        transform: translateY(-110vh) rotate(360deg);
        opacity: 0;
    }
}

footer {
    padding: 30px 10px;
    color: #d9a8c5;
    font-size: 13px;
}
</style>
</head>

<body>

<div class="container">

    <h1>Juste pour toi ❤️</h1>

    <p class="subtitle">
        Gen kèk sipriz ki pa bezwen anpil mo pou yo espesyal... ✨
    </p>

    <div class="heart">❤️</div>

    <div class="card">
        <h2>Yon ti espas pou ou 💌</h2>

        <p>
            Pafwa, se ti jès ki pi senp yo ki pote
            pi gwo souri yo.
            Jodi a, mwen te vle kreye yon ti kote
            espesyal pou fè w sonje gen yon moun
            ki kontan dèske ou fè pati lavi li. ❤️
        </p>
    </div>

    <button onclick="openSecret()">
        💌 Dekouvri mesaj mwen an
    </button>

    <div id="secret">
        <h2>Yon bagay mwen vle ou konnen ❤️</h2>
        <br>

        Ou pa bezwen fè anyen ekstraòdinè
        pou w espesyal.
        Prezans ou, souri ou ak fason ou ye a
        deja gen yon valè espesyal.
        <br><br>

        Mwen swete chak fwa ou vizite ti paj sa a,
        li raple w gen anpil bèl bagay ki merite
        fè w souri.
        <br><br>

        ❤️ Toujou kenbe bèl limyè ou a.
        <br><br>
        Avèk anpil tandrès... 💋
    </div>

</div>

<footer>
    Fait avec amour ❤️ | Juste pour toi
</footer>

<script>

// TI KÈ K AP MONTE
function createHeart() {
    const heart = document.createElement("div");

    heart.className = "floating-heart";
    heart.innerHTML = Math.random() > 0.5 ? "❤️" : "💕";

    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (15 + Math.random() * 25) + "px";
    heart.style.animationDuration = (5 + Math.random() * 5) + "s";

    document.body.appendChild(heart);

    setTimeout(() => heart.remove(), 10000);
}

setInterval(createHeart, 400);

// MESAJ SEKRÈ
function openSecret() {
    document.getElementById("secret").style.display = "block";
}

</script>

</body>
</html>
