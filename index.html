<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">

<title>Clique Rápido PRO Ultimate</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- ====== GOOGLE ADSENSE ====== -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8918456146021986"
crossorigin="anonymous"></script>

<style>
body {
    background: #121212;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
}

.tela {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #121212;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
}

input {
    padding: 10px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    margin-bottom: 10px;
    text-align: center;
}

button {
    padding: 15px 30px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    margin: 5px;
    cursor: pointer;
}

.box {
    background: #1e1e1e;
    width: 320px;
    margin: 20px auto;
    padding: 20px;
    border-radius: 15px;
}

#aviso {
    position: fixed;
    top: 40%;
    width: 100%;
    font-size: 50px;
    font-weight: bold;
    color: #00e676;
    display: none;
    z-index: 999;
}

.emoji {
    position: fixed;
    bottom: -50px;
    font-size: 30px;
    animation: subir 3s linear forwards;
    pointer-events: none;
}

@keyframes subir {
    from { transform: translateY(0); opacity: 1; }
    to { transform: translateY(-100vh); opacity: 0; }
}
</style>
</head>

<body>

<!-- ====== TELA INICIAL ====== -->
<div id="telaStart" class="tela">
    <h1>🎮 Clique Rápido PRO</h1>
    <input id="nomeJogador" placeholder="Digite seu nome" maxlength="12">
    <button id="btnStart">▶️ START</button>
</div>

<div id="aviso"></div>
<div id="emojis"></div>

<!-- ====== TELA DO JOGO ====== -->
<div id="jogo" style="display:none;">
    <div class="box">
        <p>Jogador: <span id="jogador"></span></p>
        <p>Fase: <span id="fase">1</span></p>
        <p>Tempo: <span id="tempo">20</span>s</p>
        <p>Pontos: <span id="pontos">0</span></p>

        <button onclick="clicar()">CLIQUE</button><br>
        <button onclick="assistirAnuncio()">📺 +10s</button><br>
        <button onclick="novoJogo()">🎮 Novo Jogo</button>

        <div id="ranking">
            <h3>🏆 Ranking</h3>
            <ol id="listaRanking"></ol>
        </div>
    </div>
</div>

<!-- ====== SONS ====== -->
<audio id="somClique" src="https://www.soundjay.com/button/sounds/button-16.mp3"></audio>
<audio id="somFim" src="https://www.soundjay.com/misc/sounds/fail-buzzer-01.mp3"></audio>
<audio id="musica" loop src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>

<script>
/* ====== VARIÁVEIS ====== */
let tempo = 20;
let pontos = 0;
let fase = 1;
let rodando = false;
let timer = null;
let avisoTimer = null;
let nome = "";

/* ====== LOCALSTORAGE SEGURO ====== */
let partidas = parseInt(localStorage.getItem("partidas")) || 0;

let ranking = [];
try {
    ranking = JSON.parse(localStorage.getItem("ranking")) || [];
} catch (e) {
    ranking = [];
    localStorage.removeItem("ranking");
}

/* ====== EMOJIS ====== */
const emojis = ["🎉","🔥","⭐","💎","🚀","😄"];

/* ====== START ====== */
document.getElementById("btnStart").addEventListener("click", startGame);

function startGame() {
    nome = document.getElementById("nomeJogador").value || "Jogador";
    document.getElementById("jogador").innerText = nome;

    document.getElementById("telaStart").style.display = "none";
    document.getElementById("jogo").style.display = "block";

    mostrarRanking();
    iniciar();
}

/* ====== CLIQUE ====== */
function clicar() {
    if (!rodando) return;

    pontos++;
    document.getElementById("pontos").innerText = pontos;
    document.getElementById("somClique").play();

    const musica = document.getElementById("musica");
    if (musica.paused) {
        musica.volume = 0.3;
        musica.play();
    }

    soltarEmoji();
}

/* ====== INICIAR FASE ====== */
function iniciar() {
    rodando = false;
    clearInterval(timer);
    clearInterval(avisoTimer);
    mostrarAviso(5);
}

/* ====== CONTAGEM ====== */
function mostrarAviso(n) {
    const aviso = document.getElementById("aviso");
    aviso.style.display = "block";
    aviso.innerText = n;

    let c = n;
    avisoTimer = setInterval(() => {
        c--;
        if (c > 0) {
            aviso.innerText = c;
        } else {
            clearInterval(avisoTimer);
            aviso.innerText = "VAI!";
            setTimeout(() => {
                aviso.style.display = "none";
                comecarJogo();
            }, 500);
        }
    }, 1000);
}

/* ====== COMEÇA JOGO ====== */
function comecarJogo() {
    rodando = true;
    timer = setInterval(() => {
        tempo--;
        document.getElementById("tempo").innerText = tempo;

        if (tempo <= 0) {
            proximaFase();
        }
    }, 1000);
}

/* ====== FASE ====== */
function proximaFase() {
    clearInterval(timer);
    fase++;
    document.getElementById("fase").innerText = fase;

    if (fase > 5) {
        fimDeJogo();
        return;
    }

    tempo = Math.max(5, 20 - fase * 2);
    document.getElementById("tempo").innerText = tempo;
    iniciar();
}

/* ====== FIM ====== */
function fimDeJogo() {
    rodando = false;
    clearInterval(timer);

    const musica = document.getElementById("musica");
    musica.pause();
    musica.currentTime = 0;

    document.getElementById("somFim").play();
    salvarRanking();
    alert("Fim de jogo! " + nome + " fez " + pontos + " pontos!");
    mostrarRanking();
}

/* ====== ANÚNCIO ====== */
function assistirAnuncio() {
    if (!rodando) return;
    alert("Simulando anúncio\n+10 segundos!");
    tempo += 10;
    document.getElementById("tempo").innerText = tempo;
}

/* ====== RANKING ====== */
function salvarRanking() {
    partidas++;
    localStorage.setItem("partidas", partidas);

    ranking.push({
        jogador: nome,
        pontos: pontos
    });

    ranking.sort((a, b) => b.pontos - a.pontos);
    ranking = ranking.slice(0, 5);

    localStorage.setItem("ranking", JSON.stringify(ranking));
}

function mostrarRanking() {
    const lista = document.getElementById("listaRanking");
    lista.innerHTML = "";

    ranking.forEach(r => {
        const li = document.createElement("li");
        li.textContent = r.jogador + " — " + r.pontos + " pts";
        lista.appendChild(li);
    });
}

/* ====== NOVO JOGO ====== */
function novoJogo() {
    clearInterval(timer);
    clearInterval(avisoTimer);

    const musica = document.getElementById("musica");
    musica.pause();
    musica.currentTime = 0;

    tempo = 20;
    pontos = 0;
    fase = 1;

    document.getElementById("fase").innerText = fase;
    document.getElementById("tempo").innerText = tempo;
    document.getElementById("pontos").innerText = pontos;

    iniciar();
}

/* ====== EMOJI ====== */
function soltarEmoji() {
    const e = document.createElement("div");
    e.className = "emoji";
    e.innerText = emojis[Math.floor(Math.random() * emojis.length)];
    e.style.left = Math.random() * 90 + "vw";

    document.getElementById("emojis").appendChild(e);

    setTimeout(() => {
        e.remove();
    }, 3000);
}
</script>

</body>
</html>
