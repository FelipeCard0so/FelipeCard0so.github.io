<html><head>
<style>
body {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    background-color: #333333; /* Fundo cinza escuro */
}

a {
    text-decoration: none;
}

.box {
    font-size: 20px;
    color: white;
    height: 250px;
    width: 350px;
    border-radius: 10px;
    background: #191919;
    flex-direction: column;
    display: flex;
    align-items: center;
    justify-content: center;
    border: 2px solid blue; /* Borda vermelho */
    box-shadow: 0px 0px 20px blue; /* Sombra neon vermelho */
    animation: neon-glow 1.5s infinite alternate;
}

.button-container {
    display: flex;
    justify-content: space-around;
    height: 50px;
    width: 150px;
}

button {
    height: 30px;
    width: 50px;
    background: red; /* Botão cinza */
    border-radius: 5px;
    color: white;
    font-weight: 600;
    border: none;
}

@keyframes neon-glow {
    from {
        border-color: blue; /* Borda azul */
        box-shadow: 0px 0px 20px yellow;
    }
    to {
        border-color: blue; /* Borda azul */
        box-shadow: 0px 0px 20px blue, 0px 0px 40px blue, 0px 0px 80px blue;
    }
}
</style>
</head>
<body>
<div class="box">
    <p id="question">Bora saír hoje?</p>
    <p id="thanks" style="display: none;">Que delícia, sabia que iria topar!! kkk.</p>
    <div class="button-container">
        <button onclick="showThanks()">
            <a>Sim</a>
        </button>
        <button id="no" style="background: red;">Não</button> <!-- Botão vermelho -->
    </div>
</div>
<script>
let button = document.getElementById('no');
let height = window.innerHeight - 50;
let width = window.innerWidth - 50;
button.addEventListener('mouseover', function () {
    button.style.position = "absolute";
    button.style.top = Math.random() * height + "px";
    button.style.left = Math.random() * width + "px";
})

function showThanks() {
    document.getElementById('question').style.display = 'none';
    document.getElementById('thanks').style.display = 'block';
}
</script>


</body></html>
