<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Clique Rápido</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- ADSENSE -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8918456146021986"
crossorigin="anonymous"></script>

<style>
body {
    background: #111;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
}

.tela {
    position: fixed;
    inset: 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

button, input {
    padding: 15px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    margin: 10px;
}

.box {
    background: #222;
    padding: 20px;
    border-radius: 15px;
    width: 300px;
}
</style>
</head>

<body>

<div id="start" class="tela">
    <h1>🎮 Clique Rápido</h1>
    <input id="nome" placeholder="Seu nome">
    <button onclick="start()">START</button>
</div>

<div id="game" class="tela" style="display:none;">
    <div class="box">
        <p>Jogador: <span id="jogador"></span></p>
        <p>Tempo: <span id="tempo">10</span></p>
        <p>Pontos: <span id="pontos">0</span></p>

        <button onclick="clicar()">CLIQUE</button>

        <div style="margin-top:10px">
            <ins class="adsbygoogle"
                style="display:block"
                data-ad-client="ca-pub-8918456146021986"
                data-ad-slot="1234567890"
                data-ad-format="auto"></ins>
        </div>
    </div>
</div>

<script>
let tempo = 10;
let pontos = 0;
let timer = null;
let rodando = false;
let nome = "";

function start() {
    nome = document.getElementById("nome").value || "Jogador";

    document.getElementById("jogador").innerText = nome;
    document.getElementById("start").style.display = "none";
    document.getElementById("game").style.display = "flex";

    tempo = 10;
    pontos = 0;
    document.getElementById("tempo").innerText = tempo;
    document.getElementById("pontos").innerText = pontos;

    rodando = true;
    clearInterval(timer);

    timer = setInterval(() => {
        tempo--;
        document.getElementById("tempo").innerText = tempo;

        if (tempo <= 0) {
            clearInterval(timer);
            rodando = false;
        }
    }, 1000);

    try {
        (window.adsbygoogle = window.adsbygoogle || []).push({});
    } catch {}
}

function clicar() {
    if (!rodando) return;
    pontos++;
    document.getElementById("pontos").innerText = pontos;
}
</script>

</body>
</html>
