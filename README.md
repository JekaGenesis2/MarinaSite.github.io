<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Марина Наумова — Психолог в Нижнем Новгороде</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400&family=Raleway:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --cream:    #F9F1E7;
    --sand:     #EDD9BD;
    --terracotta: #B5643A;
    --bark:     #6B3D25;
    --warm-dark:#2C1A0E;
    --leaf:     #8B9D6A;
    --white:    #FFFDF9;
  }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Raleway', sans-serif;
    background: var(--cream);
    color: var(--warm-dark);
    overflow-x: hidden;
  }

  /* ─── DECORATIVE LEAVES SVG ─── */
  .leaf-bg {
    position: absolute;
    pointer-events: none;
    opacity: .13;
  }

  /* ─── HERO ─── */
  .hero {
    position: relative;
    min-height: 100vh;
    display: grid;
    grid-template-columns: 1fr 1fr;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 70% at 30% 60%, #e8c8a0 0%, transparent 70%);
    z-index: 0;
  }

  .hero-photo-col {
    position: relative;
    z-index: 1;
    display: flex;
    align-items: flex-end;
    justify-content: center;
    padding-top: 80px;
  }

  /* Placeholder portrait frame — replace src with real photo */
  .hero-photo-frame {
    width: 420px;
    max-width: 90%;
    aspect-ratio: 3/4;
    border-radius: 240px 240px 0 0;
    background: linear-gradient(160deg, var(--sand) 0%, #d4a97a 100%);
    overflow: hidden;
    box-shadow: 0 30px 80px rgba(107,61,37,.18);
    position: relative;
  }

  .hero-photo-frame img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    object-position: top center;
    display: block;
  }

  .photo-placeholder {
 background-image: url('https://sun9-20.userapi.com/s/v1/ig2/zfLVncv9Tqr_nXIWU-OYB-q6Z3uG7Ja47LXIOiWlIMmQTsoHVShobgPW-J-JrBbRSqOv0W6CXxXTc-146PGtl8EE.jpg?quality=95&as=32x43,48x64,72x96,108x144,160x213,240x320,360x480,480x640,540x720,640x853,720x960,756x1008&from=bu&u=zpnIk_fe86v74WctIrKL7ucyprh-ZresQaT7kpGD7-g&cs=756x0');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: var(--bark);
    font-size: 14px;
    text-align: center;
    gap: 12px;
    padding: 20px;
  }

  .photo-placeholder svg { opacity: .4; }

  .hero-text-col {
    position: relative;
    z-index: 1;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 80px 60px 80px 40px;
  }

  .eyebrow {
    font-family: 'Raleway', sans-serif;
    font-weight: 600;
    font-size: 11px;
    letter-spacing: .25em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 16px;
  }

  h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(42px, 5vw, 64px);
    font-weight: 700;
    line-height: 1.08;
    color: var(--bark);
    margin-bottom: 10px;
  }

  h1 span {
    display: block;
    font-style: italic;
    font-weight: 400;
    color: var(--terracotta);
    font-size: .7em;
  }

  .hero-subtitle {
    font-size: 17px;
    line-height: 1.6;
    color: #5c3820;
    margin: 24px 0 36px;
    max-width: 380px;
    font-weight: 300;
  }

  .hero-quote {
    font-family: 'Playfair Display', serif;
    font-style: italic;
    font-size: 15px;
    color: var(--bark);
    opacity: .75;
    border-left: 3px solid var(--terracotta);
    padding-left: 18px;
    margin-bottom: 40px;
    line-height: 1.6;
  }

  .btn-primary {
    display: inline-block;
    background: var(--terracotta);
    color: var(--white);
    padding: 16px 36px;
    border-radius: 50px;
    font-family: 'Raleway', sans-serif;
    font-weight: 600;
    font-size: 15px;
    text-decoration: none;
    letter-spacing: .04em;
    transition: background .2s, transform .15s, box-shadow .2s;
    box-shadow: 0 8px 24px rgba(181,100,58,.3);
    border: none;
    cursor: pointer;
  }

  .btn-primary:hover {
    background: var(--bark);
    transform: translateY(-2px);
    box-shadow: 0 14px 32px rgba(107,61,37,.35);
  }

  .btn-outline {
    display: inline-block;
    background: transparent;
    color: var(--terracotta);
    padding: 14px 32px;
    border-radius: 50px;
    font-family: 'Raleway', sans-serif;
    font-weight: 600;
    font-size: 15px;
    text-decoration: none;
    letter-spacing: .04em;
    border: 2px solid var(--terracotta);
    transition: all .2s;
    cursor: pointer;
  }

  .btn-outline:hover { background: var(--terracotta); color: var(--white); }

  .hero-badges {
    display: flex;
    gap: 12px;
    margin-top: 28px;
    flex-wrap: wrap;
  }

  .badge {
    background: rgba(255,255,255,.7);
    border: 1px solid rgba(181,100,58,.2);
    border-radius: 40px;
    padding: 8px 16px;
    font-size: 12px;
    font-weight: 600;
    color: var(--bark);
    backdrop-filter: blur(4px);
  }

  /* ─── SECTION SHARED ─── */
  section { padding: 90px 24px; }

  .section-inner { max-width: 1100px; margin: 0 auto; }

  .section-label {
    font-size: 11px;
    font-weight: 600;
    letter-spacing: .2em;
    text-transform: uppercase;
    color: var(--terracotta);
    margin-bottom: 12px;
  }

  h2 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(30px, 4vw, 46px);
    font-weight: 700;
    color: var(--bark);
    line-height: 1.15;
    margin-bottom: 20px;
  }

  h2 em {
    font-style: italic;
    font-weight: 400;
    color: var(--terracotta);
  }

  /* ─── ABOUT ─── */
  .about {
    background: var(--white);
  }

  .about-grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: center;
  }

  .about-text p {
    font-size: 16px;
    line-height: 1.8;
    color: #4a2e1a;
    margin-bottom: 18px;
    font-weight: 300;
  }

  .about-stats {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
    margin-top: 36px;
  }

  .stat-card {
    background: var(--cream);
    border-radius: 20px;
    padding: 24px 20px;
    text-align: center;
  }

  .stat-number {
    font-family: 'Playfair Display', serif;
    font-size: 42px;
    font-weight: 700;
    color: var(--terracotta);
    line-height: 1;
  }

  .stat-label {
    font-size: 12px;
    font-weight: 500;
    color: var(--bark);
    margin-top: 6px;
    line-height: 1.4;
  }

  .about-guarantees h3 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    color: var(--bark);
    margin-bottom: 20px;
  }

  .guarantee-list {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }

  .guarantee-list li {
    display: flex;
    align-items: flex-start;
    gap: 14px;
    font-size: 15px;
    line-height: 1.5;
    color: #4a2e1a;
    font-weight: 400;
  }

  .check-icon {
    width: 22px;
    height: 22px;
    min-width: 22px;
    background: var(--leaf);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 1px;
  }

  .check-icon svg { display: block; }

  /* ─── SERVICES ─── */
  .services {
    background: var(--cream);
    position: relative;
    overflow: hidden;
  }

  .services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 24px;
    margin-top: 48px;
  }

  .service-card {
    background: var(--white);
    border-radius: 24px;
    padding: 36px 28px;
    border: 1px solid rgba(181,100,58,.1);
    transition: transform .2s, box-shadow .2s;
    position: relative;
    overflow: hidden;
  }

  .service-card::after {
    content: '';
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 3px;
    background: var(--terracotta);
    transform: scaleX(0);
    transition: transform .25s;
    transform-origin: left;
  }

  .service-card:hover { transform: translateY(-6px); box-shadow: 0 20px 50px rgba(107,61,37,.12); }
  .service-card:hover::after { transform: scaleX(1); }

  .service-icon {
    width: 52px; height: 52px;
    background: var(--sand);
    border-radius: 16px;
    display: flex; align-items: center; justify-content: center;
    margin-bottom: 20px;
    font-size: 24px;
  }

  .service-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 20px;
    color: var(--bark);
    margin-bottom: 10px;
  }

  .service-card p {
    font-size: 14px;
    line-height: 1.65;
    color: #6a4030;
    font-weight: 300;
  }

  .service-price {
    margin-top: 20px;
    font-weight: 700;
    font-size: 20px;
    color: var(--terracotta);
    font-family: 'Playfair Display', serif;
  }

  .service-price span {
    font-family: 'Raleway', sans-serif;
    font-size: 13px;
    font-weight: 400;
    color: #7a5040;
  }

  /* ─── HOW IT WORKS ─── */
  .how {
    background: var(--bark);
    color: var(--cream);
    position: relative;
    overflow: hidden;
  }

  .how h2 { color: var(--sand); }
  .how .section-label { color: var(--sand); opacity: .7; }

  .steps {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 32px;
    margin-top: 52px;
    position: relative;
  }

  .steps::before {
    content: '';
    position: absolute;
    top: 32px;
    left: calc(12.5% + 24px);
    right: calc(12.5% + 24px);
    height: 1px;
    background: rgba(237,217,189,.25);
  }

  .step {
    text-align: center;
    position: relative;
  }

  .step-num {
    width: 64px; height: 64px;
    border-radius: 50%;
    background: var(--terracotta);
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 20px;
    font-family: 'Playfair Display', serif;
    font-size: 24px;
    font-weight: 700;
    color: var(--white);
    position: relative;
    z-index: 1;
  }

  .step h3 {
    font-family: 'Playfair Display', serif;
    font-size: 17px;
    color: var(--sand);
    margin-bottom: 10px;
  }

  .step p {
    font-size: 13px;
    line-height: 1.65;
    color: rgba(237,217,189,.7);
    font-weight: 300;
  }

  /* ─── TOPICS ─── */
  .topics {
    background: var(--white);
  }

  .topics-intro {
    max-width: 580px;
    margin-bottom: 48px;
  }

  .topics-intro p {
    font-size: 16px;
    line-height: 1.7;
    color: #4a2e1a;
    font-weight: 300;
  }

  .topics-cloud {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .topic-tag {
    background: var(--cream);
    border: 1.5px solid rgba(181,100,58,.2);
    border-radius: 40px;
    padding: 10px 20px;
    font-size: 14px;
    font-weight: 500;
    color: var(--bark);
    transition: all .2s;
  }

  .topic-tag:hover {
    background: var(--terracotta);
    color: var(--white);
    border-color: var(--terracotta);
  }

  /* ─── BOOKING ─── */
  .booking {
    background: linear-gradient(135deg, var(--cream) 0%, #e8c8a0 100%);
    position: relative;
    overflow: hidden;
  }

  .booking-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
    align-items: start;
  }

  .booking-info h2 { margin-bottom: 16px; }

  .booking-info p {
    font-size: 16px;
    line-height: 1.7;
    color: #4a2e1a;
    font-weight: 300;
    margin-bottom: 24px;
  }

  .contact-links {
    display: flex;
    flex-direction: column;
    gap: 14px;
    margin-top: 32px;
  }

  .contact-link {
    display: flex;
    align-items: center;
    gap: 14px;
    font-size: 15px;
    color: var(--bark);
    text-decoration: none;
    font-weight: 500;
    transition: color .2s;
  }

  .contact-link:hover { color: var(--terracotta); }

  .contact-link .icon {
    width: 40px; height: 40px;
    background: var(--white);
    border-radius: 12px;
    display: flex; align-items: center; justify-content: center;
    flex-shrink: 0;
    box-shadow: 0 2px 8px rgba(107,61,37,.1);
  }

  /* ─── FORM ─── */
  .form-card {
    background: var(--white);
    border-radius: 28px;
    padding: 44px 40px;
    box-shadow: 0 20px 60px rgba(107,61,37,.12);
  }

  .form-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 26px;
    color: var(--bark);
    margin-bottom: 8px;
  }

  .form-card .form-desc {
    font-size: 14px;
    color: #7a5040;
    margin-bottom: 28px;
    font-weight: 300;
  }

  .field-group { margin-bottom: 18px; }

  label {
    display: block;
    font-size: 12px;
    font-weight: 600;
    letter-spacing: .06em;
    text-transform: uppercase;
    color: var(--bark);
    margin-bottom: 7px;
  }

  input, select, textarea {
    width: 100%;
    padding: 13px 16px;
    border: 1.5px solid rgba(181,100,58,.2);
    border-radius: 12px;
    background: var(--cream);
    font-family: 'Raleway', sans-serif;
    font-size: 15px;
    color: var(--warm-dark);
    outline: none;
    transition: border-color .2s, box-shadow .2s;
    appearance: none;
  }

  input:focus, select:focus, textarea:focus {
    border-color: var(--terracotta);
    box-shadow: 0 0 0 3px rgba(181,100,58,.12);
  }

  textarea { resize: vertical; min-height: 90px; }

  .field-row { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }

  .form-card .btn-primary { width: 100%; text-align: center; margin-top: 4px; font-size: 16px; padding: 17px; }

  .form-note {
    font-size: 11px;
    color: #9a7060;
    text-align: center;
    margin-top: 12px;
    line-height: 1.5;
  }

  /* ─── SUCCESS ─── */
  .success-msg {
    display: none;
    text-align: center;
    padding: 20px 0;
  }

  .success-msg .big-check {
    font-size: 52px;
    margin-bottom: 12px;
  }

  .success-msg h4 {
    font-family: 'Playfair Display', serif;
    font-size: 22px;
    color: var(--bark);
    margin-bottom: 8px;
  }

  .success-msg p {
    font-size: 14px;
    color: #7a5040;
    font-weight: 300;
  }

  /* ─── FOOTER ─── */
  footer {
    background: var(--warm-dark);
    color: rgba(237,217,189,.6);
    text-align: center;
    padding: 36px 24px;
    font-size: 13px;
    font-weight: 300;
  }

  footer strong { color: var(--sand); }

  /* ─── NAV ─── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 0 40px;
    height: 68px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(249,241,231,.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(181,100,58,.1);
  }

  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 18px;
    font-weight: 700;
    color: var(--bark);
    text-decoration: none;
  }

  .nav-logo span { color: var(--terracotta); font-style: italic; }

  .nav-links {
    display: flex;
    gap: 32px;
    list-style: none;
  }

  .nav-links a {
    font-size: 13px;
    font-weight: 600;
    letter-spacing: .05em;
    color: var(--bark);
    text-decoration: none;
    text-transform: uppercase;
    transition: color .2s;
  }

  .nav-links a:hover { color: var(--terracotta); }

  .nav-cta {
    background: var(--terracotta);
    color: var(--white) !important;
    padding: 9px 22px;
    border-radius: 40px;
  }

  .nav-cta:hover { background: var(--bark); color: var(--white) !important; }

  /* ─── SCROLL MARGIN ─── */
  [id] { scroll-margin-top: 80px; }

  /* ─── RESPONSIVE ─── */
  @media (max-width: 900px) {
    .hero { grid-template-columns: 1fr; min-height: auto; }
    .hero-photo-col { padding-top: 90px; padding-bottom: 0; order: 1; }
    .hero-text-col { order: 2; padding: 40px 24px 60px; }
    .hero-photo-frame { width: 280px; }
    .about-grid, .booking-layout { grid-template-columns: 1fr; gap: 40px; }
    .services-grid { grid-template-columns: 1fr 1fr; }
    .steps { grid-template-columns: 1fr 1fr; }
    .steps::before { display: none; }
    nav { padding: 0 20px; }
    .nav-links { display: none; }
    .form-card { padding: 28px 22px; }
    .field-row { grid-template-columns: 1fr; }
  }

  @media (max-width: 560px) {
    .services-grid { grid-template-columns: 1fr; }
    .steps { grid-template-columns: 1fr 1fr; gap: 20px; }
    .about-stats { grid-template-columns: 1fr 1fr; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a href="#" class="nav-logo">Марина <span>Наумова</span></a>
  <ul class="nav-links">
    <li><a href="#about">О психологе</a></li>
    <li><a href="#services">Услуги</a></li>
    <li><a href="#topics">Темы</a></li>
    <li><a href="#booking" class="nav-cta">Записаться</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero" style="padding:0;">
  <div class="hero-photo-col">
    <div class="hero-photo-frame">
      <!-- Замените src на вашу фотографию -->
      <div class="photo-placeholder">
        <p style="font-size:13px;color:#6B3D25;opacity:.6;"></p>
      </div>
    </div>
  </div>

  <div class="hero-text-col">
    <p class="eyebrow">Психолог · Нижний Новгород</p>
    <h1>
      Марина Наумова
      <span>психолог-консультант</span>
    </h1>
    <p class="hero-subtitle">
      Помогаю разобраться в себе, справиться с тревогой и сложными отношениями — 
      в тёплой, безопасной атмосфере. Онлайн-консультации и встречи в Нижнем Новгороде.
    </p>
    <blockquote class="hero-quote">
      «Изменения начинаются там, где появляется понимание себя.»
    </blockquote>
    <a href="#booking" class="btn-primary">Записаться на консультацию</a>
    <div class="hero-badges">
      <span class="badge">Онлайн и оффлайн</span>
      <span class="badge">2 000 ₽ / час</span>
      <span class="badge">Конфиденциально</span>
    </div>
  </div>

  <!-- decorative leaf top-right -->
  <svg class="leaf-bg" style="top:-40px;right:-20px;width:280px;" viewBox="0 0 300 300" fill="none">
    <path d="M260 20 C320 80, 280 180, 140 200 C80 210, 20 160, 60 80 C90 20, 200 -20, 260 20Z" fill="#B5643A"/>
    <path d="M140 200 C200 130, 240 60, 260 20" stroke="#6B3D25" stroke-width="1.5" fill="none"/>
  </svg>
</section>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="section-inner">
    <div class="about-grid">
      <div class="about-text">
        <p class="section-label">О психологе</p>
        <h2>Создаю пространство,<br>где можно быть <em>собой</em></h2>
        <p>
          Меня зовут Марина Наумова, я практикующий психолог-консультант в Нижнем Новгороде. 
          Работаю с тревогой, самооценкой, кризисами и отношениями — помогаю найти ответы 
          внутри себя, а не снаружи.
        </p>
        <p>
          В своей работе я сочетаю когнитивно-поведенческий подход, нарративную терапию 
          и элементы схема-терапии. Главное для меня — чтобы вы чувствовали себя услышанными 
          и в безопасности.
        </p>
        <div class="about-stats">
          <div class="stat-card">
            <div class="stat-number">3+</div>
            <div class="stat-label">года практики</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">150+</div>
            <div class="stat-label">клиентов прошли путь</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">500+</div>
            <div class="stat-label">часов консультаций</div>
          </div>
          <div class="stat-card">
            <div class="stat-number">∞</div>
            <div class="stat-label">без осуждения и оценок</div>
          </div>
        </div>
      </div>

      <div class="about-guarantees">
        <h3>Гарантии безопасности</h3>
        <ul class="guarantee-list">
          <li>
            <span class="check-icon">
              <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 6l3 3 5-5" stroke="white" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </span>
            <span><strong>Конфиденциальность</strong> — всё, что вы рассказываете, остаётся между нами.</span>
          </li>
          <li>
            <span class="check-icon">
              <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 6l3 3 5-5" stroke="white" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </span>
            <span><strong>Без осуждения и оценок</strong> — любой опыт принимается с уважением.</span>
          </li>
          <li>
            <span class="check-icon">
              <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 6l3 3 5-5" stroke="white" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </span>
            <span><strong>Бережное отношение к вашим чувствам</strong> — никакого давления и форсирования.</span>
          </li>
          <li>
            <span class="check-icon">
              <svg width="12" height="12" viewBox="0 0 12 12" fill="none"><path d="M2 6l3 3 5-5" stroke="white" stroke-width="1.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
            </span>
            <span><strong>Работа в вашем темпе</strong> — мы двигаемся так, как комфортно именно вам.</span>
          </li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div class="section-inner">
    <p class="section-label">Услуги</p>
    <h2>Форматы работы</h2>
    <div class="services-grid">
      <div class="service-card">
        <div class="service-icon">🌿</div>
        <h3>Индивидуальная консультация</h3>
        <p>Личная встреча или онлайн-сессия один на один. Разбираемся с вашим запросом глубоко и без спешки.</p>
        <div class="service-price">2 000 ₽ <span>/ 60 минут</span></div>
      </div>
      <div class="service-card">
        <div class="service-icon">💬</div>
        <h3>Онлайн-консультация</h3>
        <p>Видеозвонок в удобном для вас мессенджере — Zoom, Telegram или WhatsApp. Из любой точки мира.</p>
        <div class="service-price">2 000 ₽ <span>/ 60 минут</span></div>
      </div>
      <div class="service-card">
        <div class="service-icon">🔄</div>
        <h3>Курс из 5 сессий</h3>
        <p>Комплексная работа с запросом на протяжении нескольких встреч. Помогает достичь устойчивых изменений.</p>
        <div class="service-price">9 000 ₽ <span>/ 5 сессий</span></div>
      </div>
    </div>
  </div>
</section>

<!-- HOW IT WORKS -->
<section class="how" id="how">
  <div class="section-inner">
    <p class="section-label">Как это работает</p>
    <h2>Четыре шага <em>до первой встречи</em></h2>
    <div class="steps">
      <div class="step">
        <div class="step-num">1</div>
        <h3>Оставьте заявку</h3>
        <p>Заполните форму ниже или напишите в мессенджер — это займёт минуту.</p>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <h3>Согласуем время</h3>
        <p>Я свяжусь с вами в течение нескольких часов и подберём удобный слот.</p>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <h3>Первая встреча</h3>
        <p>Знакомство, обсуждение запроса и определение направления работы.</p>
      </div>
      <div class="step">
        <div class="step-num">4</div>
        <h3>Начало изменений</h3>
        <p>Мы работаем вместе в вашем темпе, двигаясь к тому, что важно именно вам.</p>
      </div>
    </div>
  </div>
</section>

<!-- TOPICS -->
<section class="topics" id="topics">
  <div class="section-inner">
    <p class="section-label">С чем я работаю</p>
    <h2>Темы консультаций</h2>
    <div class="topics-intro">
      <p>Если вы узнаёте себя хотя бы в одном из перечисленных запросов — это уже повод поговорить. Вы не обязаны справляться в одиночку.</p>
    </div>
    <div class="topics-cloud">
      <span class="topic-tag">Тревога и страхи</span>
      <span class="topic-tag">Низкая самооценка</span>
      <span class="topic-tag">Отношения с партнёром</span>
      <span class="topic-tag">Трудности в общении</span>
      <span class="topic-tag">Стресс на работе</span>
      <span class="topic-tag">Эмоциональное выгорание</span>
      <span class="topic-tag">Панические атаки</span>
      <span class="topic-tag">Сложности с родителями</span>
      <span class="topic-tag">Расставание и потери</span>
      <span class="topic-tag">Потеря смысла</span>
      <span class="topic-tag">Прокрастинация</span>
      <span class="topic-tag">Одиночество</span>
      <span class="topic-tag">Самоопределение</span>
      <span class="topic-tag">Обиды и прощение</span>
      <span class="topic-tag">Кризис среднего возраста</span>
      <span class="topic-tag">Сложный выбор</span>
    </div>
  </div>
</section>

<!-- BOOKING -->
<section class="booking" id="booking">
  <div class="section-inner">
    <div class="booking-layout">
      <div class="booking-info">
        <p class="section-label">Запись</p>
        <h2>Сделайте первый <em>шаг</em></h2>
        <p>Оставьте заявку, и я свяжусь с вами в ближайшее время, чтобы договориться о встрече. Никаких обязательств — первый контакт ни к чему не обязывает.</p>
        <p>Работаю в Нижнем Новгороде очно и онлайн для клиентов из любого города.</p>

        <div class="contact-links">
          <a href="tel:+79519026159" class="contact-link">
            <span class="icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#B5643A" stroke-width="2" stroke-linecap="round"><path d="M22 16.9v3a2 2 0 01-2.2 2 19.8 19.8 0 01-8.6-3.1 19.5 19.5 0 01-6-6 19.8 19.8 0 01-3.1-8.7A2 2 0 014.1 2h3a2 2 0 012 1.7c.1 1 .4 1.9.7 2.8a2 2 0 01-.5 2.1l-1.3 1.3a16 16 0 006 6l1.3-1.3a2 2 0 012.1-.5c.9.3 1.8.6 2.8.7A2 2 0 0122 16.9z"/></svg>
            </span>
            8 951 902-6159
          </a>
          <a href="mailto:marina.naumova.02@list.ru" class="contact-link">
            <span class="icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="#B5643A" stroke-width="2" stroke-linecap="round"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
            </span>
            marina.naumova.02@list.ru
          </a>
          <a href="https://t.me/marina_naumova_psy" class="contact-link" target="_blank">
            <span class="icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none"><path d="M21.8 2L2.6 9.7c-1.3.5-1.3 1.3-.2 1.6l5 1.6 1.9 5.7c.3.7.4 1 1.1 1 .6 0 .9-.3 1.2-.6l2.9-2.8 5.9 4.3c1.1.6 1.9.3 2.1-.9l3-15.3c.4-1.5-.5-2.2-1.7-1.3z" fill="#B5643A"/></svg>
            </span>
            Написать в Telegram
          </a>
        </div>
      </div>

     
        <div class="success-msg" id="successMsg">
          <div class="big-check">🌿</div>
          <h4>Заявка отправлена!</h4>
          <p>Марина свяжется с вами в течение нескольких часов для подтверждения встречи.</p>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p><strong>Марина Наумова</strong> — психолог-консультант</p>
  <p style="margin-top:8px;">Нижний Новгород · Онлайн · 8 951 902-6159 · marina.naumova.02@list.ru</p>
  <p style="margin-top:16px;font-size:11px;opacity:.5;">© 2026 Марина Наумова. Все права защищены.</p>
</footer>

<script>
  function submitForm() {
    const name = document.getElementById('fname').value.trim();
    const phone = document.getElementById('phone').value.trim();
    const contact = document.getElementById('contact').value;

    if (!name || !phone || !contact) {
      alert('Пожалуйста, заполните обязательные поля: имя, телефон и способ связи.');
      return;
    }

    document.getElementById('bookingForm').style.display = 'none';
    document.getElementById('successMsg').style.display = 'block';
  }

  // Smooth nav highlight
  const sections = document.querySelectorAll('[id]');
  const navLinks = document.querySelectorAll('.nav-links a');

  window.addEventListener('scroll', () => {
    let current = '';
    sections.forEach(s => {
      if (window.scrollY >= s.offsetTop - 120) current = s.id;
    });
    navLinks.forEach(a => {
      a.style.color = a.getAttribute('href') === '#' + current ? 'var(--terracotta)' : '';
    });
  });
</script>
</body>
</html>
