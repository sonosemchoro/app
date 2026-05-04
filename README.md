<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sono Sem Choro™ — Seu Bebê Dormindo Bem em Dias</title>
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap" rel="stylesheet">
<style>
  :root {
    --rosa: #F2C4CE;
    --rosa-escuro: #E8A0B0;
    --bege: #F9F3EE;
    --bege-2: #F0E8DF;
    --verde: #4CAF82;
    --verde-escuro: #3A9A6E;
    --vermelho: #D63031;
    --texto: #2C2020;
    --texto-suave: #6B5454;
    --branco: #FFFFFF;
    --sombra: rgba(44, 32, 32, 0.08);
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Plus Jakarta Sans', sans-serif;
    background: var(--branco);
    color: var(--texto);
    -webkit-font-smoothing: antialiased;
    text-align: center;
  }

  /* ─── BARRA DE URGÊNCIA ─── */
  .urgencia-bar {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 999;
    background: var(--vermelho);
    color: white;
    text-align: center;
    padding: 10px 16px;
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.01em;
    animation: pulse-bar 3s ease-in-out infinite;
  }
  @keyframes pulse-bar {
    0%, 100% { background: #D63031; }
    50% { background: #C0392B; }
  }

  /* ─── LAYOUT GERAL ─── */
  .page-wrapper {
    margin-top: 40px;
    overflow: hidden;
  }

  .container {
    max-width: 620px;
    margin: 0 auto;
    padding: 0 20px;
  }

  section {
    padding: 56px 0;
  }

  /* ─── HERO ─── */
  .hero {
    background: linear-gradient(160deg, #FFF5F7 0%, var(--bege) 100%);
    padding: 64px 0 56px;
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    top: -80px;
    right: -80px;
    width: 280px;
    height: 280px;
    background: radial-gradient(circle, rgba(242,196,206,0.35) 0%, transparent 70%);
    border-radius: 50%;
  }

  .hero::after {
    content: '';
    position: absolute;
    bottom: -60px;
    left: -60px;
    width: 200px;
    height: 200px;
    background: radial-gradient(circle, rgba(249,243,238,0.8) 0%, transparent 70%);
    border-radius: 50%;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background: var(--rosa);
    color: #8B3A4A;
    font-size: 12px;
    font-weight: 700;
    padding: 6px 14px;
    border-radius: 999px;
    text-transform: uppercase;
    letter-spacing: 0.08em;
    margin-bottom: 24px;
  }

  .hero h1 {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(30px, 7vw, 44px);
    line-height: 1.2;
    color: var(--texto);
    margin-bottom: 20px;
    position: relative;
    z-index: 1;
  }

  .hero h1 em {
    font-style: italic;
    color: #C0566B;
  }

  .hero .subheadline {
    font-size: clamp(16px, 3.5vw, 18px);
    color: var(--texto-suave);
    line-height: 1.65;
    margin-bottom: 36px;
    position: relative;
    z-index: 1;
    font-weight: 400;
  }

  .preco-hero {
    display: flex;
    align-items: center;
    gap: 12px;
    margin-bottom: 10px;
    flex-wrap: wrap;
  }

  .preco-de {
    font-size: 15px;
    color: var(--texto-suave);
    text-decoration: line-through;
  }

  .preco-por {
    font-family: 'DM Serif Display', serif;
    font-size: 38px;
    color: #C0566B;
    font-weight: 400;
  }

  .desconto-tag {
    background: #FDE8EC;
    color: #C0566B;
    font-size: 12px;
    font-weight: 700;
    padding: 4px 10px;
    border-radius: 999px;
  }

  .preco-sub {
    font-size: 13px;
    color: var(--texto-suave);
    margin-bottom: 28px;
  }

  /* ─── BOTÃO CTA ─── */
  .cta-btn {
    display: block;
    width: 100%;
    background: linear-gradient(135deg, #4CAF82 0%, #3A9A6E 100%);
    color: white;
    font-family: 'Plus Jakarta Sans', sans-serif;
    font-size: 17px;
    font-weight: 800;
    text-align: center;
    padding: 18px 24px;
    border-radius: 16px;
    border: none;
    cursor: pointer;
    text-decoration: none;
    letter-spacing: 0.01em;
    box-shadow: 0 8px 32px rgba(76, 175, 130, 0.35);
    transition: transform 0.18s ease, box-shadow 0.18s ease;
    position: relative;
    overflow: hidden;
  }

  .cta-btn::after {
    content: '';
    position: absolute;
    inset: 0;
    background: linear-gradient(135deg, rgba(255,255,255,0.15), transparent);
    pointer-events: none;
  }

  .cta-btn:hover {
    transform: translateY(-2px);
    box-shadow: 0 12px 40px rgba(76, 175, 130, 0.45);
  }

  .cta-btn:active { transform: translateY(0); }

  .cta-note {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 6px;
    font-size: 12px;
    color: var(--texto-suave);
    margin-top: 10px;
    flex-wrap: wrap;
  }

  /* ─── SEÇÃO PROBLEMA ─── */
  .problema {
    background: var(--bege);
  }

  .section-label {
    font-size: 11px;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 0.12em;
    color: var(--rosa-escuro);
    margin-bottom: 12px;
  }

  .section-title {
    font-family: 'DM Serif Display', serif;
    font-size: clamp(24px, 5.5vw, 34px);
    line-height: 1.25;
    margin-bottom: 20px;
  }

  .section-sub {
    font-size: 16px;
    color: var(--texto-suave);
    line-height: 1.65;
    margin-bottom: 28px;
  }

  .problema-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  .problema-list li {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    font-size: 15px;
    color: var(--texto-suave);
    background: white;
    border-radius: 14px;
    padding: 14px 16px;
    box-shadow: 0 2px 12px var(--sombra);
    line-height: 1.5;
    text-align: left;
  }

  .problema-list .ico {
    font-size: 20px;
    flex-shrink: 0;
    margin-top: 1px;
  }

  /* ─── PRODUTO ─── */
  .produto {
    background: linear-gradient(160deg, #FFF 0%, #FFF5F7 100%);
  }

  .produto-card {
    background: white;
    border-radius: 24px;
    padding: 32px 24px;
    box-shadow: 0 4px 32px var(--sombra);
    border: 1.5px solid #F2E0E4;
    margin-top: 28px;
    text-align: left;
  }

  .produto-nome {
    font-family: 'DM Serif Display', serif;
    font-size: 28px;
    color: #C0566B;
    margin-bottom: 8px;
  }

  .produto-desc {
    font-size: 15px;
    color: var(--texto-suave);
    line-height: 1.6;
    margin-bottom: 24px;
    padding-bottom: 24px;
    border-bottom: 1px solid #F2E0E4;
  }

  .beneficios-lista {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .beneficios-lista li {
    display: flex;
    align-items: flex-start;
    gap: 12px;
    font-size: 15px;
    color: var(--texto);
    line-height: 1.5;
    font-weight: 500;
    text-align: left;
  }

  .check-ico {
    width: 22px;
    height: 22px;
    background: linear-gradient(135deg, #4CAF82, #3A9A6E);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    color: white;
    font-size: 12px;
    margin-top: 1px;
  }

  /* ─── DEPOIMENTOS ─── */
  .depoimentos {
    background: var(--bege);
  }

  .depo-grid {
    display: flex;
    flex-direction: column;
    gap: 16px;
    margin-top: 32px;
  }

  .depo-card {
    background: white;
    border-radius: 20px;
    padding: 24px 20px;
    box-shadow: 0 2px 20px var(--sombra);
    border-left: 4px solid var(--rosa);
    position: relative;
    text-align: left;
  }

  .depo-card::before {
    content: '"';
    font-family: 'DM Serif Display', serif;
    font-size: 64px;
    color: var(--rosa);
    position: absolute;
    top: 8px;
    right: 20px;
    line-height: 1;
    opacity: 0.5;
  }

  .depo-text {
    font-size: 15px;
    line-height: 1.65;
    color: var(--texto);
    margin-bottom: 16px;
    font-style: italic;
  }

  .depo-autor {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .depo-avatar {
    width: 38px;
    height: 38px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 16px;
    flex-shrink: 0;
  }

  .depo-nome {
    font-size: 13px;
    font-weight: 700;
    color: var(--texto);
  }

  .depo-info {
    font-size: 12px;
    color: var(--texto-suave);
  }

  .estrelas {
    color: #F7C948;
    font-size: 13px;
    margin-bottom: 2px;
  }

  /* ─── PLANOS ─── */
  .planos {
    background: linear-gradient(160deg, white 0%, #FFF5F7 100%);
  }

  .planos-grid {
    display: flex;
    flex-direction: column;
    gap: 20px;
    margin-top: 32px;
  }

  .plano-card {
    background: white;
    border-radius: 24px;
    padding: 28px 24px;
    box-shadow: 0 4px 24px var(--sombra);
    border: 2px solid #F2E0E4;
    position: relative;
    transition: transform 0.2s ease;
    text-align: left;
  }

  .plano-card:hover { transform: translateY(-3px); }

  .plano-card.destaque {
    border-color: var(--rosa-escuro);
    box-shadow: 0 8px 40px rgba(232, 160, 176, 0.3);
  }

  .plano-badge {
    position: absolute;
    top: -12px;
    left: 50%;
    transform: translateX(-50%);
    background: linear-gradient(135deg, #C0566B, #E8A0B0);
    color: white;
    font-size: 11px;
    font-weight: 800;
    padding: 5px 16px;
    border-radius: 999px;
    text-transform: uppercase;
    letter-spacing: 0.06em;
    white-space: nowrap;
  }

  .plano-nome {
    font-family: 'DM Serif Display', serif;
    font-size: 22px;
    color: var(--texto);
    margin-bottom: 4px;
  }

  .plano-preco-de {
    font-size: 13px;
    color: var(--texto-suave);
    text-decoration: line-through;
    margin-bottom: 2px;
  }

  .plano-preco {
    font-family: 'DM Serif Display', serif;
    font-size: 42px;
    color: #C0566B;
    line-height: 1;
    margin-bottom: 6px;
  }

  .plano-preco span {
    font-family: 'Plus Jakarta Sans', sans-serif;
    font-size: 16px;
    font-weight: 600;
  }

  .plano-divider {
    height: 1px;
    background: #F2E0E4;
    margin: 20px 0;
  }

  .plano-itens {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 10px;
    margin-bottom: 24px;
  }

  .plano-itens li {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 14px;
    color: var(--texto);
    line-height: 1.4;
  }

  .plano-itens .ico-check {
    color: var(--verde);
    font-size: 16px;
    flex-shrink: 0;
  }

  .plano-itens .item-bonus {
    font-weight: 600;
    color: #C0566B;
  }

  /* ─── GARANTIA ─── */
  .garantia {
    background: var(--bege);
  }

  .garantia-card {
    background: white;
    border-radius: 24px;
    padding: 36px 24px;
    text-align: center;
    box-shadow: 0 4px 24px var(--sombra);
    border: 2px dashed var(--rosa-escuro);
  }

  .garantia-ico {
    font-size: 56px;
    margin-bottom: 16px;
    display: block;
    animation: float 3s ease-in-out infinite;
  }

  @keyframes float {
    0%, 100% { transform: translateY(0); }
    50% { transform: translateY(-6px); }
  }

  .garantia-titulo {
    font-family: 'DM Serif Display', serif;
    font-size: 26px;
    color: #C0566B;
    margin-bottom: 12px;
  }

  .garantia-texto {
    font-size: 15px;
    color: var(--texto-suave);
    line-height: 1.65;
  }

  /* ─── FAQ ─── */
  .faq { background: white; }

  .faq-item {
    border-bottom: 1px solid #F2E0E4;
    padding: 20px 0;
  }

  .faq-item:first-of-type { border-top: 1px solid #F2E0E4; }

  .faq-pergunta {
    font-size: 15px;
    font-weight: 700;
    color: var(--texto);
    cursor: pointer;
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    gap: 12px;
    line-height: 1.45;
    user-select: none;
    -webkit-tap-highlight-color: transparent;
    text-align: left;
  }

  .faq-toggle {
    font-size: 20px;
    color: #C0566B;
    flex-shrink: 0;
    transition: transform 0.25s ease;
    line-height: 1;
    margin-top: 1px;
  }

  .faq-item.open .faq-toggle { transform: rotate(45deg); }

  .faq-resposta {
    display: none;
    font-size: 14px;
    color: var(--texto-suave);
    line-height: 1.65;
    padding-top: 12px;
    text-align: left;
  }

  .faq-item.open .faq-resposta { display: block; }

  /* ─── CTA FINAL ─── */
  .cta-final {
    background: linear-gradient(160deg, #FFF5F7 0%, #F9F3EE 100%);
    text-align: center;
  }

  .cta-final .section-title { font-size: clamp(24px, 5.5vw, 36px); }

  /* ─── FOOTER ─── */
  footer {
    background: var(--bege-2);
    padding: 28px 20px;
    text-align: center;
  }

  footer p {
    font-size: 12px;
    color: var(--texto-suave);
    line-height: 1.7;
  }

  footer a { color: var(--texto-suave); text-decoration: underline; }

  /* ─── ANIMATIONS ─── */
  .fade-in {
    opacity: 0;
    transform: translateY(24px);
    transition: opacity 0.6s ease, transform 0.6s ease;
  }

  .fade-in.visible {
    opacity: 1;
    transform: translateY(0);
  }

  /* ─── MOBILE TWEAKS ─── */
  @media (min-width: 480px) {
    .planos-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 20px;
    }

    .depo-grid {
      display: grid;
      grid-template-columns: 1fr;
    }
  }

  @media (max-width: 360px) {
    .hero h1 { font-size: 26px; }
    .plano-preco { font-size: 34px; }
  }

  /* Pulse animation for CTA */
  @keyframes pulse-cta {
    0%, 100% { box-shadow: 0 8px 32px rgba(76, 175, 130, 0.35); }
    50% { box-shadow: 0 8px 48px rgba(76, 175, 130, 0.55); }
  }

  .cta-btn.pulse { animation: pulse-cta 2s ease-in-out infinite; }

  /* Divider decorativa */
  .divider-wave {
    height: 32px;
    background: var(--bege);
    clip-path: ellipse(55% 100% at 50% 0%);
  }
</style>
</head>
<body>

<!-- BARRA DE URGÊNCIA -->
<div class="urgencia-bar">
  ⚠️ Oferta disponível apenas hoje. O acesso pode sair do ar a qualquer momento
</div>

<div class="page-wrapper">

  <!-- ─── HERO ─── -->
  <section class="hero">
    <div class="container">
      <div class="badge fade-in">🌙 Método Comprovado por Mães</div>
      <h1 class="fade-in">
        Seu bebê <em>não precisa</em> chorar para aprender a dormir.
      </h1>
      <p class="subheadline fade-in">
        Descubra o método simples que está ajudando mães a organizar o sono dos seus bebês em poucos dias, sem sofrimento e sem culpa.
      </p>

      <div class="preco-hero fade-in">
        <span class="preco-de">De R$97</span>
        <span class="preco-por">R$27</span>
        <span class="desconto-tag">72% OFF</span>
      </div>
      <p class="preco-sub">Acesso imediato • Pagamento único • Sem mensalidade</p>

      <a href="#planos" class="cta-btn pulse fade-in">
        👉 QUERO MEU BEBÊ DORMINDO MELHOR
      </a>
      <div class="cta-note fade-in">
        🔒 Compra segura &nbsp;|&nbsp; 🛡️ Garantia 7 dias &nbsp;|&nbsp; ⚡ Acesso imediato
      </div>
    </div>
  </section>

  <!-- ─── PROBLEMA ─── -->
  <section class="problema">
    <div class="container">
      <div class="section-label fade-in">Isso soa familiar?</div>
      <h2 class="section-title fade-in">
        Você está exausta e seu bebê ainda não dorme a noite toda.
      </h2>
      <p class="section-sub fade-in">
        Acordar várias vezes por noite não precisa ser o seu normal. Na maioria dos casos existe um motivo claro, e uma saída simples.
      </p>
      <ul class="problema-list">
        <li class="fade-in">
          <span class="ico">😫</span>
          <span>Seu bebê acorda 3, 4 ou 5 vezes por noite e você não sabe mais o que fazer</span>
        </li>
        <li class="fade-in">
          <span class="ico">😰</span>
          <span>Você tenta de tudo, mas nada parece funcionar por mais de uma noite</span>
        </li>
        <li class="fade-in">
          <span class="ico">💭</span>
          <span>Recebe conselhos contraditórios de todo lado e não sabe em quem confiar</span>
        </li>
        <li class="fade-in">
          <span class="ico">😔</span>
          <span>Sente culpa por estar tão cansada e às vezes até irritada com o bebê</span>
        </li>
        <li class="fade-in">
          <span class="ico">🌙</span>
          <span>Sonha com uma noite de sono completo há semanas (ou meses)</span>
        </li>
      </ul>
    </div>
  </section>

  <!-- ─── PRODUTO ─── -->
  <section class="produto">
    <div class="container">
      <div class="section-label fade-in">A Solução</div>
      <h2 class="section-title fade-in">
        Um guia que coloca ordem no caos, de forma gentil e prática.
      </h2>
      <p class="section-sub fade-in">
        Sem teoria desnecessária. Só o que você precisa saber e fazer, começando hoje à noite.
      </p>

      <div class="produto-card fade-in">
        <div class="produto-nome">Sono Sem Choro™</div>
        <p class="produto-desc">
          Um guia prático e direto ao ponto que mostra exatamente o que fazer para melhorar o sono do seu bebê, mesmo que hoje ele acorde várias vezes durante a noite.
        </p>
        <ul class="beneficios-lista">
          <li>
            <span class="check-ico">✓</span>
            <span>Entenda <strong>por que</strong> seu bebê não dorme e o que está acontecendo no corpo dele</span>
          </li>
          <li>
            <span class="check-ico">✓</span>
            <span>Descubra os <strong>erros comuns</strong> que sabotam o sono, que a maioria das mães comete sem saber</span>
          </li>
          <li>
            <span class="check-ico">✓</span>
            <span>Siga uma <strong>rotina pronta por idade</strong>, do recém-nascido até os 24 meses</span>
          </li>
          <li>
            <span class="check-ico">✓</span>
            <span>Saiba exatamente <strong>o que fazer em cada despertar</strong> noturno</span>
          </li>
          <li>
            <span class="check-ico">✓</span>
            <span>Aplique um <strong>plano simples</strong> que funciona sem deixar seu bebê chorando sozinho</span>
          </li>
        </ul>
      </div>

      <br>
      <a href="#planos" class="cta-btn fade-in">
        👉 QUERO MEU BEBÊ DORMINDO MELHOR
      </a>
    </div>
  </section>

  <!-- ─── DEPOIMENTOS ─── -->
  <section class="depoimentos">
    <div class="container">
      <div class="section-label fade-in">Histórias Reais</div>
      <h2 class="section-title fade-in">
        Mães que já aplicaram e mudaram as noites delas.
      </h2>

      <div class="depo-grid">
        <div class="depo-card fade-in">
          <div class="estrelas">★★★★★</div>
          <p class="depo-text">"Meu bebê acordava umas 5 vezes por noite. Em poucos dias aplicando o método, tudo mudou. Agora ele dorme mais de 6 horas seguidas. Eu estava no limite."</p>
          <div class="depo-autor">
            <div class="depo-avatar" style="background:#FADADD;">🤱</div>
            <div>
              <div class="depo-nome">Camila R.</div>
              <div class="depo-info">Mãe da Sofia, 8 meses</div>
            </div>
          </div>
        </div>

        <div class="depo-card fade-in">
          <div class="estrelas">★★★★★</div>
          <p class="depo-text">"Achei que nunca ia conseguir dormir direito sem deixar meu filho chorando. Me surpreendi muito. Ele foi pegando o ritmo aos poucos e agora a noite é outra."</p>
          <div class="depo-autor">
            <div class="depo-avatar" style="background:#F9F3EE;">🌸</div>
            <div>
              <div class="depo-nome">Fernanda M.</div>
              <div class="depo-info">Mãe do Lucas, 5 meses</div>
            </div>
          </div>
        </div>

        <div class="depo-card fade-in">
          <div class="estrelas">★★★★★</div>
          <p class="depo-text">"Era exatamente o que eu precisava. Sem enrolação, sem teoria chata. Apliquei na primeira noite e já senti diferença. Valeu muito cada centavo."</p>
          <div class="depo-autor">
            <div class="depo-avatar" style="background:#E8F5EE;">💚</div>
            <div>
              <div class="depo-nome">Juliana S.</div>
              <div class="depo-info">Mãe da Isabela, 14 meses</div>
            </div>
          </div>
        </div>

        <div class="depo-card fade-in">
          <div class="estrelas">★★★★★</div>
          <p class="depo-text">"Tentei de tudo antes de encontrar esse guia. Consultei pediatra, vi vídeos, li artigos. Só aqui encontrei um passo a passo que fez sentido de verdade. Mudou nossa família."</p>
          <div class="depo-autor">
            <div class="depo-avatar" style="background:#FDE8EC;">🍀</div>
            <div>
              <div class="depo-nome">Beatriz L.</div>
              <div class="depo-info">Mãe do Davi, 11 meses</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- ─── PLANOS ─── -->
  <section class="planos" id="planos">
    <div class="container">
      <div class="section-label fade-in">Escolha seu plano</div>
      <h2 class="section-title fade-in">Acesso imediato logo após o pagamento.</h2>
      <p class="section-sub fade-in">Leitura no celular, tablet ou computador. Disponível para sempre.</p>

      <div class="planos-grid">
        <!-- PLANO ESSENCIAL -->
        <div class="plano-card fade-in">
          <div class="plano-nome">Essencial</div>
          <div class="plano-preco-de">De R$97</div>
          <div class="plano-preco"><span>R$</span>27</div>
          <p style="font-size:13px; color:var(--texto-suave); margin-bottom:4px;">Pagamento único</p>
          <div class="plano-divider"></div>
          <ul class="plano-itens">
            <li><span class="ico-check">✅</span> Ebook completo Sono Sem Choro™</li>
            <li><span class="ico-check">✅</span> Checklist de erros que sabotam o sono</li>
            <li><span class="ico-check">✅</span> Rotina pronta por idade (0–24 meses)</li>
          </ul>
          <a href="#" class="cta-btn" style="font-size:14px; padding:14px 16px; background: linear-gradient(135deg,#5BA0D0,#4088C0); box-shadow:0 6px 24px rgba(64,136,192,0.3);">
            Quero o Essencial →
          </a>
        </div>

        <!-- PLANO COMPLETO -->
        <div class="plano-card destaque fade-in">
          <div class="plano-badge">⭐ Mais escolhido</div>
          <div class="plano-nome">Completo</div>
          <div class="plano-preco-de">De R$197</div>
          <div class="plano-preco" style="color:#C0566B;"><span>R$</span>47</div>
          <p style="font-size:13px; color:var(--texto-suave); margin-bottom:4px;">Pagamento único</p>
          <div class="plano-divider"></div>
          <ul class="plano-itens">
            <li><span class="ico-check">✅</span> Ebook completo Sono Sem Choro™</li>
            <li><span class="ico-check">✅</span> Checklist de erros que sabotam o sono</li>
            <li><span class="ico-check">✅</span> Rotina pronta por idade (0–24 meses)</li>
            <li><span class="ico-check">✅</span> <span class="item-bonus">🌙 Protocolo 3 Noites de Paz</span></li>
            <li><span class="ico-check">✅</span> <span class="item-bonus">🗺️ Mapa do Sono Noturno</span></li>
            <li><span class="ico-check">✅</span> <span class="item-bonus">🔄 Simulador de Rotina</span></li>
            <li><span class="ico-check">✅</span> <span class="item-bonus">🚨 Guia de Emergência da Madrugada</span></li>
            <li><span class="ico-check">✅</span> <span class="item-bonus">📋 Plano de Ajustes Semanais</span></li>
          </ul>
          <a href="#" class="cta-btn pulse" style="font-size:15px; padding:16px;">
            👉 QUERO O COMPLETO
          </a>
          <p style="font-size:12px; color:var(--verde-escuro); margin-top:8px; font-weight:600;">
            ✨ Economia de R$150 hoje!
          </p>
        </div>
      </div>
    </div>
  </section>

  <!-- ─── GARANTIA ─── -->
  <section class="garantia">
    <div class="container">
      <div class="garantia-card fade-in">
        <span class="garantia-ico">🛡️</span>
        <h3 class="garantia-titulo">Garantia de 7 Dias</h3>
        <p class="garantia-texto">
          Teste por 7 dias com risco zero. Se você aplicar o método e não sentir nenhuma diferença na rotina do seu bebê, é só mandar um e-mail e devolvemos 100% do seu dinheiro. Sem perguntas, sem burocracia.
          <br><br>
          <strong>Você não tem nada a perder.</strong> Só noites boas de sono a ganhar. 🌙
        </p>
      </div>
    </div>
  </section>

  <!-- ─── FAQ ─── -->
  <section class="faq">
    <div class="container">
      <div class="section-label fade-in">Perguntas frequentes</div>
      <h2 class="section-title fade-in">Ficou alguma dúvida?</h2>

      <div style="margin-top:28px;">
        <div class="faq-item fade-in">
          <div class="faq-pergunta" onclick="toggleFaq(this)">
            Funciona para qual idade de bebê?
            <span class="faq-toggle">+</span>
          </div>
          <div class="faq-resposta">O método foi desenvolvido para bebês de 0 a 24 meses, com rotinas e orientações adaptadas para cada faixa etária do desenvolvimento.</div>
        </div>

        <div class="faq-item fade-in">
          <div class="faq-pergunta" onclick="toggleFaq(this)">
            Preciso deixar meu bebê chorar?
            <span class="faq-toggle">+</span>
          </div>
          <div class="faq-resposta">Não. O Sono Sem Choro™ é baseado em uma abordagem gentil que respeita o desenvolvimento emocional do bebê. O objetivo é criar as condições certas para o sono, sem sofrimento para nenhum dos dois.</div>
        </div>

        <div class="faq-item fade-in">
          <div class="faq-pergunta" onclick="toggleFaq(this)">
            Como recebo o acesso após a compra?
            <span class="faq-toggle">+</span>
          </div>
          <div class="faq-resposta">O acesso é imediato. Assim que o pagamento for confirmado, você recebe um e-mail com o link para visualizar ou baixar o material no celular, tablet ou computador.</div>
        </div>

        <div class="faq-item fade-in">
          <div class="faq-pergunta" onclick="toggleFaq(this)">
            E se eu não gostar?
            <span class="faq-toggle">+</span>
          </div>
          <div class="faq-resposta">Você tem 7 dias de garantia total. Se por qualquer motivo não ficar satisfeita, basta mandar um e-mail e devolvemos 100% do valor pago, sem nenhuma pergunta.</div>
        </div>

        <div class="faq-item fade-in">
          <div class="faq-pergunta" onclick="toggleFaq(this)">
            Precisa ter algum conhecimento antes?
            <span class="faq-toggle">+</span>
          </div>
          <div class="faq-resposta">Não precisa de nada. O guia foi escrito de forma simples e direta, pensando em mães exaustas que precisam de orientações práticas, não de textos complicados.</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ─── CTA FINAL ─── -->
  <section class="cta-final">
    <div class="container">
      <div class="section-label fade-in">Você merece descansar.</div>
      <h2 class="section-title fade-in">
        Essa noite pode ser diferente. Depende só de uma decisão.
      </h2>
      <p class="section-sub fade-in">
        Centenas de mães já mudaram as noites delas com o Sono Sem Choro™. Hoje pode ser a sua vez.
      </p>

      <div class="fade-in" style="background:white; border-radius:20px; padding:24px; border:2px solid #F2E0E4; margin-bottom:24px; text-align:left;">
        <div style="font-size:13px; color:var(--texto-suave); text-decoration:line-through; margin-bottom:4px;">De R$97</div>
        <div style="font-family:'DM Serif Display',serif; font-size:48px; color:#C0566B; line-height:1; margin-bottom:4px;">
          <span style="font-family:'Plus Jakarta Sans',sans-serif; font-size:20px; font-weight:600;">R$</span>27
        </div>
        <div style="font-size:13px; color:var(--texto-suave);">Pagamento único • Acesso imediato • Sem mensalidade</div>
      </div>

      <a href="#planos" class="cta-btn pulse fade-in" style="font-size:18px; padding:20px 24px;">
        👉 QUERO MEU BEBÊ DORMINDO MELHOR
      </a>
      <div class="cta-note fade-in" style="margin-top:14px;">
        🔒 Ambiente seguro &nbsp;|&nbsp; 🛡️ Garantia 7 dias &nbsp;|&nbsp; ⚡ Acesso em minutos
      </div>
    </div>
  </section>

</div><!-- /page-wrapper -->

<!-- ─── FOOTER ─── -->
<footer>
  <p>
    © 2025 Sono Sem Choro™ — Todos os direitos reservados.<br>
    <a href="#">Política de Privacidade</a> &nbsp;|&nbsp;
    <a href="#">Termos de Uso</a> &nbsp;|&nbsp;
    <a href="#">Suporte</a>
  </p>
  <p style="margin-top:8px;">
    Este produto é um guia digital (ebook). Os resultados podem variar de bebê para bebê.
  </p>
</footer>

<script>
  // ─── FAQ Toggle ───
  function toggleFaq(el) {
    const item = el.parentElement;
    item.classList.toggle('open');
  }

  // ─── Fade-in on scroll ───
  const fadeEls = document.querySelectorAll('.fade-in');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1, rootMargin: '0px 0px -40px 0px' });

  fadeEls.forEach(el => observer.observe(el));

  // ─── Stagger children in lists ───
  document.querySelectorAll('.problema-list, .beneficios-lista, .plano-itens, .depo-grid').forEach(list => {
    const children = list.querySelectorAll('.fade-in');
    children.forEach((child, i) => {
      child.style.transitionDelay = `${i * 80}ms`;
    });
  });
</script>

</body>
</html>
