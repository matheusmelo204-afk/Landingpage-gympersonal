<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Trainer</title>
    <style>
        body { margin: 0; font-family: Arial, sans-serif; background-color: #0b0b0b; color: white; }
        header { position: relative; height: 90vh; background: url('https://images.unsplash.com/photo-1558611848-73f7eb4001a1') center/cover no-repeat; display: flex; align-items: center; justify-content: center; text-align: center; }
        header h1 { font-size: 3rem; color: #ff007f; text-shadow: 2px 2px 8px black; }
        section { padding: 40px 20px; max-width: 1000px; margin: auto; }
        .sobre { display: flex; flex-wrap: wrap; align-items: center; gap: 20px; }
        .sobre img { max-width: 350px; border-radius: 15px; }
        .planos { display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 20px; }
        .plano { background: #111; padding: 20px; border-radius: 15px; text-align: center; border: 1px solid #222; }
        .plano h3 { color: #ff007f; }
        .resultados { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 20px; }
        .resultados img { width: 100%; border-radius: 10px; }
        form { display: flex; flex-direction: column; gap: 10px; }
        input, textarea { padding: 10px; border: none; border-radius: 5px; }
        button { background: #ff007f; color: white; padding: 10px; border: none; border-radius: 5px; cursor: pointer; }
        @media (max-width: 768px) {
            header h1 { font-size: 2rem; padding: 0 10px; }
            .sobre { flex-direction: column; text-align: center; }
        }
    </style>
</head>
<body>

<header>
    <h1>TRANSFORME SEU CORPO E VIDA</h1>
</header>

<section class="sobre">
    <img src="assets/sobre_mim.jpg" alt="Sobre mim">
    <div>
        <h2>Sobre Mim</h2>
        <p>Licenciada e Bacharel em educação física, Pós-graduada em Personal training, especialista em biomecânica e fisiologia do exercício. Resultados reais, métodos comprovados.</p>
    </div>
</section>

<section>
    <h2>Planos de Treinamento</h2>
    <div class="planos">
        <div class="plano">
            <h3>Plano Online</h3>
            <p>R$ 100,00 / mês</p>
        </div>
        <div class="plano">
            <h3>Plano Presencial</h3>
            <p>R$ 300,00 / mês</p>
        </div>
    </div>
</section>

<section>
    <h2>Resultados Reais</h2>
    <div class="resultados">
        <img src="assets/resultado1.jpg" alt="Resultado 1">
        <img src="assets/resultado2.jpg" alt="Resultado 2">
        <img src="assets/resultado3.jpg" alt="Resultado 3">
        <img src="assets/resultado4.jpg" alt="Resultado 4">
    </div>
</section>

<section>
    <h2>Contato</h2>
    <form onsubmit="enviarWhatsApp(event)">
        <input type="text" id="nome" placeholder="Seu nome" required>
        <input type="tel" id="telefone" placeholder="Seu telefone" required>
        <textarea id="mensagem" placeholder="Sua mensagem" required></textarea>
        <button type="submit">Enviar pelo WhatsApp</button>
    </form>
</section>

<script>
function enviarWhatsApp(e) {
    e.preventDefault();
    let nome = document.getElementById('nome').value;
    let telefone = document.getElementById('telefone').value;
    let mensagem = document.getElementById('mensagem').value;
    let texto = `Nome: ${nome}%0ATelefone: ${telefone}%0AMensagem: ${mensagem}`;
    window.open(`https://wa.me/qr/FHAPIRUDD5LEO1?text=${texto}`, '_blank');
}
</script>

</body>
</html>
