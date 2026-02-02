<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">

<!-- Título que aparece na aba do navegador -->
<title>Clique Rápido PRO Ultimate</title>

<!-- Deixa o site responsivo no celular -->
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<!-- ====== GOOGLE ADSENSE ====== -->
<script async src="https://pagead2.googlesyndication.com/pagead/js/adsbygoogle.js?client=ca-pub-8918456146021986"
     crossorigin="anonymous"></script>

<style>
/* ====== ESTILO GERAL DA PÁGINA ====== */
body {
    background: #121212;
    color: white;
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 0;
}

/* ====== TELAS (Start e Jogo) ====== */
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

/* ====== CAMPO DE TEXTO ====== */
input {
    padding: 10px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    margin-bottom: 10px;
    text-align: center;
}

/* ====== BOTÕES ====== */
button {
    padding: 15px 30px;
    font-size: 18px;
    border-radius: 10px;
    border: none;
    margin: 5px;
    cursor: pointer;
}

/* ====== CAIXA DO JOGO ====== */
.box {
    background: #1e1e1e;
    width: 320px;
    margin: 20px auto;
    padding: 20px;
    border-radius: 15px;
}

/* ====== AVISO DE CONTAGEM ====== */
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

/* ====== EMOJIS FLUTUANTES ====== */
.emoji {
    position: fixed;
    bottom: -50px;
    font-size: 30px;
    animation: subir 3s linear forwards;
    pointer-events: none;
}

/* ====== ANIMAÇÃO DOS EMOJIS ====== */
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

<!-- Texto grande de contagem regressiva -->
<div id="aviso"></div>

<!-- Área onde os emojis animados aparecem -->
<div id="emojis"></div>

<!-- ====== TELA DO JOGO ====== -->
<div id="jogo" style="display:none;">
    <div class="box">

        <p>Jogador: <span id="jogador"></span></p>
        <p>Fase: <span id="fase">1</span></p>
        <p>Tempo: <span id="tempo">20</span>s</p>
        <p>Pontos: <span id="pontos">0</span></p>

        <!-- Botão principal de clique -->
        <button onclick="clicar()">CLIQUE</button><br>

        <!-- Botão que simula anúncio para ganhar tempo -->
        <button onclick="assistirAnuncio()">📺 +10s</button><br>

        <!-- Botão para reiniciar o jogo -->
        <button onclick="novoJogo()">🎮 Novo Jogo</button>

        <!-- ====== BANNER ADSENSE ====== -->
        <div style="margin-top:15px">
            <ins class="adsbygoogle"
                style="display:block"
                data-ad-client="ca-pub-8918456146021986"
                data-ad-slot="1234567890"
                data-ad-format="auto"
                data-full-width-responsive="true"></ins>
        </div>

        <!-- Ranking dos melhores jogadores -->
        <div id="ranking">
            <h3>🏆 Ranking</h3>
            <ol id="listaRanking"></ol>
        </div>
    </div>
</div>

<script>
/* ====== VARIÁVEIS PRINCIPAIS ====== */
let tempo = 20;
let pontos = 0;
let fase = 1;
let rodando = false;
let timer = null;
let avisoTimer = null;
let nome = "";

/* ====== STORAGE BLINDADO ====== */
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

/* ====== BOTÃO START ====== */
document.getElementById("btnStart").addEventListener("click", startGame);

/* ====== INICIA O JOGO ====== */
function startGame() {
    nome = document.getElementById("nomeJogador").value || "Jogador";
    document.getElementById("jogador").innerText = nome;

    document.getElementById("telaStart").style.display = "none";
    document.getElementById("jogo").style.display = "block";

    mostrarRanking();
    iniciar();

    try {
        (window.adsbygoogle = window.adsbygoogle || []).push({});
    } catch (e) {}
}

/* ====== FUNÇÃO DE CLIQUE ====== */
function clicar() {
    if (!rodando) return;

    pontos++;
    document.getElementById("pontos").innerText = pontos;

    soltarEmoji();
}

/* ====== INICIA CONTAGEM ====== */
function iniciar() {
    rodando = false;
    clearInterval(timer);
    clearInterval(avisoTimer);
    mostrarAviso(5);
}

/* ====== MOSTRA 5,4,3,2,1, VAI ====== */
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

/* ====== COMEÇA A FASE ====== */
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

/* ====== PASSA DE FASE ====== */
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

/* ====== FIM DE JOGO ====== */
function fimDeJogo() {
    rodando = false;
    clearInterval(timer);
    salvarRanking();
    alert("Fim de jogo! " + nome + " fez " + pontos + " pontos!");
    mostrarRanking();
}

/* ====== SIMULA ANÚNCIO ====== */
function assistirAnuncio() {
    if (!rodando) return;
    alert("Simulando anúncio\n+10 segundos!");
    tempo += 10;
    document.getElementById("tempo").innerText = tempo;
}

/* ====== SALVA NO RANKING ====== */
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

/* ====== MOSTRA RANKING ====== */
function mostrarRanking() {
    const lista = document.getElementById("listaRanking");
    lista.innerHTML = "";

    ranking.forEach((r, i) => {
        const li = document.createElement("li");

        let medalha = "";
        if (i === 0) medalha = "🥇";
        else if (i === 1) medalha = "🥈";
        else if (i === 2) medalha = "🥉";

        li.innerHTML = `${medalha} ${r.jogador} — ${r.pontos} pts`;
        lista.appendChild(li);
    });
}

/* ====== REINICIA ====== */
function novoJogo() {
    clearInterval(timer);
    clearInterval(avisoTimer);

    tempo = 20;
    pontos = 0;
    fase = 1;

    document.getElementById("fase").innerText = fase;
    document.getElementById("tempo").innerText = tempo;
    document.getElementById("pontos").innerText = pontos;

    iniciar();
}

/* ====== EMOJIS ====== */
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
