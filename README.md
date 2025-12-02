<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Agendamento de Aulas de Figurinos</title>
<style>
  body {
    font-family: "Arial", sans-serif;
    background-color: #f0e6d2;
    margin: 0;
    padding: 0;
    color: #333;
  }

  header {
    background-color: #4b2e83;
    color: #fff;
    padding: 20px;
    text-align: center;
  }

  header h1 {
    margin: 0;
    font-family: "Georgia", serif;
    font-size: 2.5em;
  }

  section {
    padding: 20px;
    max-width: 900px;
    margin: auto;
  }

  h2 {
    color: #4b2e83;
    border-bottom: 2px solid #4b2e83;
    padding-bottom: 10px;
  }

  p {
    font-size: 1.1em;
  }

  form {
    display: flex;
    flex-direction: column;
    gap: 15px;
    background-color: #fff8f0;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
  }

  label {
    font-weight: bold;
  }

  input, select, textarea {
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 1em;
  }

  button {
    background-color: #4b2e83;
    color: #fff;
    padding: 12px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 1.1em;
    transition: background-color 0.3s;
  }

  button:hover {
    background-color: #6a378f;
  }

  #confirmacao {
    display: none;
    margin-top: 20px;
    padding: 15px;
    background-color: #e0d4b8;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
  }

  footer {
    background-color: #4b2e83;
    color: #fff;
    text-align: center;
    padding: 15px;
    margin-top: 40px;
  }
</style>
</head>
<body>

<header>
  <h1>Marca Sua Aula de Figurinos</h1>
  <p>Aprenda técnicas de figurino para teatro, cinema e moda!</p>
</header>

<section>
  <h2>Agende sua aula</h2>
  <p>Preencha o formulário abaixo para marcar sua aula de figurinos com nossos especialistas. Escolha o melhor dia e horário para você.</p>
  <form id="formAula">
    <label for="nome">Nome completo:</label>
    <input type="text" id="nome" name="nome" required>

    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>

    <label for="telefone">Telefone:</label>
    <input type="tel" id="telefone" name="telefone" required>

    <label for="dia">Dia da aula:</label>
    <select id="dia" name="dia" required>
      <option value="">Selecione o dia</option>
      <option value="Segunda-feira">Segunda-feira</option>
      <option value="Terça-feira">Terça-feira</option>
      <option value="Quarta-feira">Quarta-feira</option>
      <option value="Quinta-feira">Quinta-feira</option>
      <option value="Sexta-feira">Sexta-feira</option>
    </select>

    <label for="hora">Horário:</label>
    <select id="hora" name="hora" required>
      <option value="">Selecione o horário</option>
      <option value="14:00">14:00</option>
      <option value="15:30">15:30</option>
      <option value="17:00">17:00</option>
      <option value="18:30">18:30</option>
    </select>

    <label for="mensagem">Mensagem (opcional):</label>
    <textarea id="mensagem" name="mensagem" rows="4" placeholder="Alguma dúvida ou informação adicional..."></textarea>

    <button type="submit">Enviar agendamento</button>
  </form>
  <div id="confirmacao">
    <h3>Agendamento recebido!</h3>
    <p>Obrigado por marcar sua aula de figurinos. Entraremos em contato em breve para confirmar os detalhes.</p>
  </div>
</section>

<footer>
  <p>© 2024 Escola de Figurinos - Todos os direitos reservados</p>
</footer>

<script>
  // JavaScript para exibir mensagem de confirmação ao enviar o formulário
  document.getElementById('formAula').addEventListener('submit', function(e) {
    e.preventDefault(); // Impede o envio padrão do formulário
    // Aqui, você pode integrar com backend ou enviar por AJAX
    // Para efeito de exemplo, só mostra a mensagem
    document.getElementById('formAula').style.display = 'none';
    document.getElementById('confirmacao').style.display = 'block';
  });
</script>

</body>
</html>
