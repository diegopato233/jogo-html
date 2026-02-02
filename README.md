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
