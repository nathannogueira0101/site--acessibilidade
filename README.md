# site--acessibilidade
<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Portal Futebol - Layout</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=Montserrat:wght@400;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --container-w:900px;
      --container-h:480px;
    }
    body {
      background: #222;
      display:flex;
      align-items:center;
      justify-content:center;
      min-height:100vh;
      margin:0;
      font-family: "Montserrat", sans-serif;
    }
    .card {
      width:var(--container-w);
      height:var(--container-h);
      position:relative;
      border-radius:12px;
      overflow:hidden;
      background: url('https://img.cdndsgni.com/preview/10321525.jpg') center/cover no-repeat;
      box-shadow: 0 10px 30px rgba(0,0,0,0.6);
    }
    .overlay {
      position:absolute;
      inset:0;
      background: linear-gradient(180deg, rgba(0,0,0,0.12), rgba(0,0,0,0.18));
      pointer-events:none;
    }
    .left-panel {
      position:absolute;
      top:36px;
      left:36px;
      width:420px;
      height:210px;
      padding:20px 18px;
      background: linear-gradient(90deg,#f7e26b, #9ad24b);
      border-radius:10px;
      display:flex;
      flex-direction:column;
      justify-content:flex-start;
      align-items:flex-start;
      box-shadow: 0 6px 10px rgba(0,0,0,0.25);
      border:4px solid rgba(105,0,255,0.06);
    }
    .left-panel::after {
      content:"";
      position:absolute;
      top:12px; left:12px; right:12px; bottom:12px;
      border:3px solid rgba(88,0,255,0.55);
      border-radius:6px;
      pointer-events:none;
    }
    .left-panel .title {
      margin:0 0 6px 0;
      font-family: "Playfair Display", serif;
      font-size:28px;
      font-weight:900;
      font-style:italic;
      color:#0b0b0b;
    }
    .left-panel .subtitle {
      margin:0;
      font-family: "Playfair Display", serif;
      font-size:34px;
      line-height:1.1;
      color:#061b00;
      text-shadow: 0 1px 0 rgba(255,255,255,0.15);
    }
    .top-pill {
      position:absolute;
      top:36px;
      right:36px;
      background:#0b57ff;
      color:#fff;
      padding:10px 18px;
      border-radius:22px;
      font-family:"Montserrat", sans-serif;
      font-size:16px;
      font-weight:700;
      box-shadow: 0 6px 10px rgba(0,0,0,0.25);
    }
    .player-card {
      position:absolute;
      top:110px;
      right:36px;
      width:260px;
      height:200px;
      border-radius:12px;
      overflow:hidden;
      box-shadow: 0 8px 20px rgba(0,0,0,0.4);
      background:#ccc;
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .player-card img {
      width:100%;
      height:100%;
      object-fit:cover;
      filter: grayscale(0.2) contrast(1.05);
    }
    .small-bubble {
      position:absolute;
      bottom:36px;
      left:36px;
      width:220px;
      height:60px;
      background: linear-gradient(90deg, #eeeeee, #d6d6d6);
      border-radius:12px;
      box-shadow: 0 6px 12px rgba(0,0,0,0.25);
      display:flex;
      align-items:center;
      justify-content:center;
      font-family: "Playfair Display", serif;
      font-size:15px;
      font-weight:700;
      color:#0b0b0b;
      text-align:center;
      padding:8px;
    }
    @media(max-width:980px){
      .card { transform: scale(0.85); transform-origin: center; }
    }
    @media(max-width:760px){
      body { padding:24px; }
      .card { width:100%; height:400px; }
      .left-panel { top:18px; left:18px; width:48%; }
      .top-pill { top:18px; right:18px; }
      .player-card { top:100px; right:18px; width:35%; height:170px; }
      .small-bubble { bottom:18px; left:18px; width:46%; }
    }
  </style>
</head>
<body>
  <div class="card">
    <div class="overlay"></div>
    <div class="left-panel">
      <div class="title">Portal Futebol:</div>
      <div class="subtitle">Fique por dentro<br>do seu time do<br>coração</div>
    </div>
    <div class="top-pill">Atualizações 24 horas</div>
    <div class="player-card">
      <img src="https://i.etsystatic.com/41905212/r/il/1a68b2/1530809155/il_1140xN.1530809155_nuf7.jpg" alt="Jogador">
    </div>
    <div class="small-bubble">
      Saiba sobre seus<br>jogadores favoritos
    </div>
  </div>
</body>
</html>
<section style="max-width:900px; margin:40px auto; padding:20px; background:#2f2f2f; border-radius:10px; display:flex; align-items:flex-start; gap:20px; color:#fff; font-family:'Montserrat', sans-serif;">
  <!-- Texto explicativo com título e bolha de ícone -->
  <div style="flex:1;">
    <h2 style="margin:0 0 12px; font-family:'Playfair Display', serif; font-size:28px; color:#f5f5f5;">
      Informações sobre o site
      <span style="margin-left:8px; vertical-align:middle; font-size:24px;">ⓘ</span>
    </h2>
    <div style="background:#fff; color:#333; padding:16px; border-radius:8px; line-height:1.5; box-shadow:0 4px 12px rgba(0,0,0,0.3);">
      No nosso site o telespectador terá todas as informações sobre seu time do peito, tendo disponíveis os jogos que foram passados caso alguém perdeu, os jogos que estão acontecendo AO VIVO!!<br><br>
      Também, você terá com antecedência as escalações e entrevistas dos jogadores, antes e depois. Caso a pessoa não puder ouvir os jogos e entrevistas, teremos uma narração acontecendo logo abaixo do placar, assim ninguém perderá nada sobre seu timão.
    </div>
  </div>

  <!-- Imagem do jogador à direita -->
  <div style="flex:0 0 200px; border-radius:8px; overflow:hidden; box-shadow:0 4px 12px rgba(0,0,0,0.3);">
    <img src="PLAYER2_IMAGE_URL" alt="Jogador" style="width:100%; display:block; object-fit:cover;">
  </div>
</section> 
<section style="max-width:900px; margin:40px auto; padding:20px; background: linear-gradient(90deg, #1cb743, #005c0f); border-radius:10px; color:#000; font-family:'Montserrat', sans-serif; display:flex; align-items:center; gap:20px;">
  <!-- Texto: Título e caixa de mensagem -->
  <div style="flex:1;">
    <h2 style="margin:0 0 15px; font-family:'Playfair Display', serif; font-size:30px; color:#000; text-align:center;">Comunicados</h2>
    <div style="background:#3f7e00; color:#fff; padding:18px; border-radius:8px 20px 8px 8px; position:relative; box-shadow:0 4px 12px rgba(0,0,0,0.25);">
      <!-- Ícone (lápis minimalista) -->
      <div style="position:absolute; top:-14px; left:-14px; background:#fff; width:28px; height:28px; border-radius:50%; display:flex; align-items:center; justify-content:center; box-shadow:0 2px 6px rgba(0,0,0,0.2); font-size:16px;">✏️</div>
      <strong>Lembrete dos Jogos</strong>
      <p style="margin-top:10px; font-size:16px; line-height:1.4;">
        Faltando 30 minutos para o jogo começar, será notificado no seu celular que o jogo está prestes a começar
      </p>
    </div>
    <!-- Botão de "Voltar ao Início" centralizado -->
    <div style="margin-top:16px; text-align:center;">
      <button style="padding:8px 16px; background:#000; color:#fff; border:none; border-radius:20px; font-size:14px; cursor:pointer; box-shadow:0 2px 6px rgba(0,0,0,0.2);">
        VOLTAR AO INÍCIO
      </button>
    </div>
  </div>

  <!-- Imagem do jogador à direita -->
  <div style="flex:0 0 200px; border-radius:8px; overflow:hidden; box-shadow:0 4px 12px rgba(0,0,0,0.25);">
    <img src="PLAYER3_IMAGE_URL" alt="Jogador em ação" style="width:100%; height:100%; object-fit:cover; display:block;">
  </div>
</section>
<section style="max-width:900px; margin:40px auto; padding:20px; background: linear-gradient(90deg, #1cb743, #005c0f); border-radius:10px; color:#000; font-family:'Montserrat', sans-serif; display:flex; align-items:center; gap:20px; flex-wrap:wrap;">
  <!-- Texto: Título e caixa de mensagem -->
  <div style="flex:1; min-width:280px;">
    <h2 style="margin:0 0 15px; font-family:'Playfair Display', serif; font-size:30px; color:#fff; text-align:center;">Comunicados</h2>
    <div style="background:#3f7e00; color:#fff; padding:18px; border-radius:8px 20px 8px 8px; position:relative; box-shadow:0 4px 12px rgba(0,0,0,0.25);">
      <!-- Ícone (lápis minimalista) -->
      <div style="position:absolute; top:-14px; left:-14px; background:#fff; width:28px; height:28px; border-radius:50%; display:flex; align-items:center; justify-content:center; box-shadow:0 2px 6px rgba(0,0,0,0.2); font-size:16px;">✏️</div>
      <strong>Lembrete dos Jogos</strong>
      <p style="margin-top:10px; font-size:16px; line-height:1.4;">
        Faltando 30 minutos para o jogo começar, será notificado no seu celular que o jogo está prestes a começar
      </p>
    </div>
    <!-- Botão de "Voltar ao Início" centralizado -->
    <div style="margin-top:16px; text-align:center;">
      <button style="padding:8px 16px; background:#000; color:#fff; border:none; border-radius:20px; font-size:14px; cursor:pointer; box-shadow:0 2px 6px rgba(0,0,0,0.2);">
        VOLTAR AO INÍCIO
      </button>
    </div>
  </div>

  <!-- Imagem do jogador à direita -->
  <div style="flex:0 0 200px; border-radius:8px; overflow:hidden; box-shadow:0 4px 12px rgba(0,0,0,0.25); min-width:180px;">
    <img src="e3ebff6c-ef50-46aa-a62c-0d5cb82a9681.png" alt="Jogador em ação" style="width:100%; height:100%; object-fit:cover; display:block;">
  </div>
</section>

