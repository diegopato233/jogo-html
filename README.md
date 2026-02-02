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

/* ====== BANNER ADS ====== */
#adBox {
    margin-top: 15px;
    padding: 10px;
    background: #000;
    border-radius: 10px;
}
</style>
</head>

<body>

<!-- ====== TELA START ====== -->
<div id="telaStart" class="tela">
    <h1>🎮 Clique Rápido PRO</h1>
    <input id="nomeJogador" placeholder="Digite seu nome" maxlength="12">
    <button id="btnStart">▶️ START</button>
</div>

<div id="aviso"></div>
<div id="emojis"></div>

<!-- ====== TELA JOGO ====== -->
<div id="jogo" style="display:none;">
    <div class="box">

        <p>Jogador: <span id="jogador"></span></p>
        <p>Fase: <span id="fase">1</span></p>
        <p>Tempo: <span id="tempo">20</span>s</p>
        <p>Pontos: <span id="pontos">0</span></p>

        <button onclick="clicar()">CLIQUE</button><br>
        <button onclick="assistirAnuncio()">📺 +10s</button><br>
        <button onclick="novoJogo()">🎮 Novo Jogo</button>

        <!-- ====== ANÚNCIO ====== -->
        <div id="adBox">
            <ins class="adsbygoogle"
                style="display:block"
                data-ad-client="ca-pub-8918456146021986"
                data-ad-slot="1234567890"
                data-ad-format="auto"
                data-full-width-responsive="true"></ins>
        </div>

        <div id="ranking">
            <h3>🏆 Ranking</h3>
            <ol id="listaRanking"></ol>
        </div>
    </div>
</div>

<!-- ====== SONS ====== -->
<audio id="somClique" src="https://www.soundjay.com/button/sounds/button-16.mp3"></audio>
<audio id="musica" loop src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3"></audio>

<
