<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>La Taquería del Rey 🌮 · Granada Norte, Bogotá</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Playfair+Display:ital,wght@0,700;1,400&family=DM+Sans:opsz,wght@9..40,300;9..40,400;9..40,500;9..40,600&display=swap" rel="stylesheet">
<style>
:root {
  --rojo:    #C0392B;
  --rojo2:   #E74C3C;
  --verde:   #14532D;
  --verde2:  #1a6b38;
  --oro:     #F4A922;
  --oro2:    #FCD34D;
  --crema:   #FFFBF2;
  --carbon:  #0F0A04;
  --cafe:    #1C1007;
  --naranja: #EA580C;
  --azul:    #1A3C5E;
  --gris:    #F5F0E8;
  --morado:  #6B3FA0;
}
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'DM Sans',sans-serif;background:var(--crema);color:var(--carbon);overflow-x:hidden;}
 
/* NAV */
nav{position:fixed;top:0;width:100%;z-index:200;background:var(--carbon);display:flex;align-items:center;justify-content:space-between;padding:0 4%;height:60px;border-bottom:3px solid var(--oro);}
.nav-logo{font-family:'Bebas Neue',sans-serif;font-size:1.5rem;color:var(--oro);letter-spacing:2px;text-decoration:none;}
.nav-links{display:flex;gap:1.4rem;list-style:none;flex-wrap:wrap;}
.nav-links a{color:#E5E7EB;text-decoration:none;font-size:.75rem;letter-spacing:1px;text-transform:uppercase;font-weight:500;transition:color .2s;}
.nav-links a:hover{color:var(--oro);}
.nav-cta{background:var(--rojo);color:#fff!important;padding:.3rem .8rem;border-radius:4px;}
 
/* HERO */
.hero{min-height:100vh;background:var(--carbon);display:grid;place-items:center;position:relative;overflow:hidden;padding-top:60px;}
.hero-bg{position:absolute;inset:0;background:radial-gradient(ellipse 70% 50% at 50% 60%,rgba(192,57,43,.2) 0%,transparent 70%),repeating-linear-gradient(-45deg,transparent,transparent 80px,rgba(244,169,34,.03) 80px,rgba(244,169,34,.03) 81px);}
.hero-inner{text-align:center;position:relative;z-index:2;padding:4rem 2rem;animation:fadeUp .8s ease both;}
.hero-flags{font-size:2rem;margin-bottom:1.2rem;display:flex;justify-content:center;gap:.6rem;}
.hero h1{font-family:'Bebas Neue',sans-serif;font-size:clamp(3.5rem,12vw,9.5rem);line-height:.9;color:var(--crema);letter-spacing:4px;}
.hero h1 em{color:var(--oro);font-style:normal;}
.hero-tagline{font-family:'Playfair Display',serif;font-style:italic;color:var(--naranja);font-size:clamp(.95rem,2.3vw,1.4rem);margin:1.2rem 0 .5rem;}
.hero-sub{color:#9CA3AF;font-size:.8rem;letter-spacing:1.5px;text-transform:uppercase;margin-bottom:2.2rem;}
.hero-btns{display:flex;gap:1rem;justify-content:center;flex-wrap:wrap;}
.btn-primary{background:var(--rojo);color:#fff;padding:.8rem 2rem;border-radius:5px;font-weight:600;font-size:.88rem;letter-spacing:1px;text-transform:uppercase;text-decoration:none;transition:background .2s,transform .15s;}
.btn-primary:hover{background:var(--naranja);transform:translateY(-2px);}
.btn-outline{border:2px solid var(--oro);color:var(--oro);padding:.8rem 2rem;border-radius:5px;font-weight:600;font-size:.88rem;letter-spacing:1px;text-transform:uppercase;text-decoration:none;transition:all .2s;}
.btn-outline:hover{background:var(--oro);color:var(--carbon);transform:translateY(-2px);}
 
/* STRIPS */
.stars-strip{background:var(--oro);padding:.55rem 2rem;display:flex;align-items:center;justify-content:center;gap:1rem;flex-wrap:wrap;}
.stars-strip span{font-size:.82rem;font-weight:600;color:var(--carbon);}
.stars-strip .sep{opacity:.35;}
.ticker{background:var(--rojo);overflow:hidden;padding:.5rem 0;}
.ticker-inner{display:flex;white-space:nowrap;animation:ticker 28s linear infinite;}
.ticker-item{color:#fff;font-size:.75rem;letter-spacing:2px;text-transform:uppercase;font-weight:500;padding:0 2rem;}
.ticker-item::after{content:'✦';margin-left:2rem;color:var(--oro2);}
 
/* SECTION COMMONS */
.sec-label{font-size:.68rem;letter-spacing:3px;text-transform:uppercase;font-weight:600;margin-bottom:.4rem;}
.sec-title{font-family:'Bebas Neue',sans-serif;font-size:clamp(2.2rem,5vw,3.6rem);letter-spacing:2px;line-height:1;}
.bar{width:48px;height:4px;border-radius:2px;margin:.8rem 0 1.4rem;}
 
/* ABOUT */
.about{display:grid;grid-template-columns:1fr 1fr;min-height:480px;}
.about-text{background:var(--verde);color:var(--crema);padding:5rem 7% 5rem 8%;display:flex;flex-direction:column;justify-content:center;}
.about-text .sec-label{color:var(--oro2);}
.about-text .sec-title{color:var(--crema);}
.about-text .bar{background:var(--oro);}
.about-text p{line-height:1.75;opacity:.9;margin-bottom:.9rem;font-size:.97rem;max-width:440px;}
.about-visual{background:var(--cafe);display:flex;align-items:center;justify-content:center;position:relative;overflow:hidden;}
.about-visual::before{content:'';position:absolute;inset:0;background:radial-gradient(circle at 50% 50%,rgba(244,169,34,.15) 0%,transparent 65%);}
.about-emoji{font-size:8rem;position:relative;z-index:1;animation:float 4s ease-in-out infinite;filter:drop-shadow(0 0 30px rgba(244,169,34,.5));}
.about-stat{position:absolute;bottom:1.8rem;left:50%;transform:translateX(-50%);text-align:center;z-index:2;}
.about-stat strong{font-family:'Bebas Neue',sans-serif;font-size:2.8rem;color:var(--oro);}
.about-stat span{display:block;color:#9CA3AF;font-size:.7rem;letter-spacing:2px;text-transform:uppercase;}
 
/* DOMICILIOS BANNER */
.domicilios{background:var(--verde2);color:#fff;padding:1rem 5%;display:flex;align-items:center;justify-content:center;gap:2rem;flex-wrap:wrap;}
.domicilios span{font-size:.88rem;letter-spacing:.5px;}
.domicilios strong{font-family:'Bebas Neue',sans-serif;font-size:1.4rem;letter-spacing:2px;color:var(--oro2);}
 
/* ═══════════════════════════════════════
   MENU SECTION
═══════════════════════════════════════ */
.menu-wrap{background:var(--crema);padding:5rem 4%;}
.menu-wrap-header{text-align:center;margin-bottom:3rem;}
.menu-wrap-header .sec-label{color:var(--rojo);}
.menu-wrap-header .bar{background:var(--rojo);margin:.8rem auto 1.4rem;}
.menu-wrap-header p{color:#6B7280;font-size:.92rem;max-width:500px;margin:0 auto;}
 
/* Category tabs */
.cat-tabs{display:flex;gap:.5rem;flex-wrap:wrap;justify-content:center;margin-bottom:3rem;}
.cat-tab{background:none;border:2px solid #D1C9BB;color:#6B7280;padding:.4rem 1rem;border-radius:50px;font-size:.75rem;font-weight:600;letter-spacing:.8px;text-transform:uppercase;cursor:pointer;transition:all .2s;font-family:'DM Sans',sans-serif;}
.cat-tab:hover,.cat-tab.active{background:var(--rojo);border-color:var(--rojo);color:#fff;}
 
/* Category blocks */
.cat-block{margin-bottom:4rem;}
.cat-block-header{display:flex;align-items:center;gap:1rem;margin-bottom:1.8rem;padding-bottom:.8rem;border-bottom:3px solid;}
.cat-block-header h2{font-family:'Bebas Neue',sans-serif;font-size:2rem;letter-spacing:2px;}
.cat-block-header .cat-emoji{font-size:1.8rem;}
 
/* Color themes per category */
.cat-tacos .cat-block-header{border-color:var(--rojo);}
.cat-tacos .cat-block-header h2{color:var(--rojo);}
.cat-burritos .cat-block-header{border-color:var(--verde);}
.cat-burritos .cat-block-header h2{color:var(--verde);}
.cat-combos .cat-block-header{border-color:var(--naranja);}
.cat-combos .cat-block-header h2{color:var(--naranja);}
.cat-crujientes .cat-block-header{border-color:var(--oro);}
.cat-crujientes .cat-block-header h2{color:#b8860b;}
.cat-esquites .cat-block-header{border-color:#8B4513;}
.cat-esquites .cat-block-header h2{color:#8B4513;}
.cat-bebidas .cat-block-header{border-color:var(--azul);}
.cat-bebidas .cat-block-header h2{color:var(--azul);}
.cat-cocteles .cat-block-header{border-color:var(--morado);}
.cat-cocteles .cat-block-header h2{color:var(--morado);}
.cat-dulces .cat-block-header{border-color:#E91E8C;}
.cat-dulces .cat-block-header h2{color:#E91E8C;}
.cat-adiciones .cat-block-header{border-color:#555;}
.cat-adiciones .cat-block-header h2{color:#555;}
.cat-aguas .cat-block-header{border-color:#2E7D32;}
.cat-aguas .cat-block-header h2{color:#2E7D32;}
 
/* Item grid */
.items-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:1.2rem;}
.items-grid.wide{grid-template-columns:repeat(auto-fill,minmax(280px,1fr));}
.item-card{background:#fff;border-radius:10px;padding:1.1rem 1.3rem 1.2rem;box-shadow:0 2px 10px rgba(0,0,0,.05);border:1px solid #EDE8DF;transition:transform .2s,box-shadow .2s;display:flex;flex-direction:column;}
.item-card:hover{transform:translateY(-4px);box-shadow:0 6px 20px rgba(0,0,0,.1);}
.item-header{display:flex;justify-content:space-between;align-items:flex-start;gap:.8rem;margin-bottom:.4rem;}
.item-name{font-family:'Bebas Neue',sans-serif;font-size:1.2rem;letter-spacing:.8px;line-height:1.1;flex:1;}
.item-price{font-family:'Bebas Neue',sans-serif;font-size:1.25rem;color:var(--rojo);white-space:nowrap;flex-shrink:0;}
.item-desc{font-size:.8rem;color:#6B7280;line-height:1.6;flex:1;}
.item-badge{display:inline-block;font-size:.62rem;font-weight:700;letter-spacing:.8px;text-transform:uppercase;padding:.15rem .5rem;border-radius:3px;margin-bottom:.45rem;width:fit-content;}
.badge-red{background:var(--rojo);color:#fff;}
.badge-green{background:var(--verde2);color:#fff;}
.badge-gold{background:var(--oro);color:var(--carbon);}
.badge-orange{background:var(--naranja);color:#fff;}
 
/* simple list style for adiciones */
.items-list{display:grid;grid-template-columns:repeat(auto-fill,minmax(200px,1fr));gap:.7rem;}
.list-item{background:#fff;border-radius:8px;padding:.7rem 1rem;display:flex;justify-content:space-between;align-items:center;box-shadow:0 1px 6px rgba(0,0,0,.05);border:1px solid #EDE8DF;}
.list-item span{font-size:.88rem;font-weight:500;}
.list-item .lp{font-family:'Bebas Neue',sans-serif;font-size:1.1rem;color:var(--rojo);}
 
/* Taco por unidad */
.tacos-unit{background:var(--rojo);border-radius:10px;padding:1.2rem 1.4rem;color:#fff;}
.tacos-unit h3{font-family:'Bebas Neue',sans-serif;font-size:1.3rem;letter-spacing:1px;margin-bottom:.8rem;color:var(--oro2);}
.tacos-unit .tu-item{display:flex;justify-content:space-between;padding:.3rem 0;border-bottom:1px solid rgba(255,255,255,.15);font-size:.88rem;}
.tacos-unit .tu-item:last-child{border-bottom:none;}
.tacos-unit .tu-price{font-family:'Bebas Neue',sans-serif;font-size:1rem;color:var(--oro2);}
 
/* Temperatura / Postre */
.special-cards{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:1.2rem;margin-top:1.5rem;}
.special-card{background:#fff;border-radius:10px;padding:1.2rem 1.3rem;box-shadow:0 2px 10px rgba(0,0,0,.05);border:1px solid #EDE8DF;text-align:center;}
.special-card h3{font-family:'Bebas Neue',sans-serif;font-size:1.2rem;letter-spacing:1px;margin-bottom:.5rem;}
.special-card p{font-size:.82rem;color:#6B7280;line-height:1.6;}
.special-card .sp{font-family:'Bebas Neue',sans-serif;font-size:1.3rem;color:var(--rojo);margin-top:.5rem;}
 
/* BIRRIA FEATURE */
.birria-feat{background:var(--carbon);display:grid;grid-template-columns:1fr 1fr;min-height:460px;}
.birria-vis{position:relative;overflow:hidden;background:var(--cafe);display:flex;align-items:center;justify-content:center;}
.birria-vis::before{content:'';position:absolute;inset:0;background:radial-gradient(circle at 40% 50%,rgba(192,57,43,.35) 0%,transparent 65%);}
.flame{font-size:5rem;animation:float 2.5s ease-in-out infinite;filter:drop-shadow(0 0 20px rgba(234,88,12,.7));position:relative;z-index:1;}
.birria-text{padding:4rem 7%;display:flex;flex-direction:column;justify-content:center;color:var(--crema);}
.birria-text .sec-label{color:var(--oro2);}
.birria-text .sec-title{color:var(--oro);}
.birria-text .bar{background:var(--rojo2);}
.birria-text p{line-height:1.75;opacity:.85;font-size:.97rem;max-width:440px;margin-bottom:1.1rem;}
.birria-pill{display:inline-flex;align-items:center;gap:.5rem;background:var(--rojo);color:#fff;border-radius:50px;padding:.5rem 1.2rem;font-weight:600;font-size:.85rem;width:fit-content;}
 
/* REVIEWS */
.reviews-sec{padding:5rem 5%;background:var(--gris);}
.reviews-sec .sec-label{color:var(--verde2);}
.reviews-sec .bar{background:var(--verde2);}
.reviews-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(250px,1fr));gap:1.2rem;margin-top:2rem;}
.review-card{background:#fff;border-radius:12px;padding:1.4rem;box-shadow:0 2px 10px rgba(0,0,0,.05);border:1px solid #EDE8DF;}
.review-stars{color:var(--oro);font-size:1rem;margin-bottom:.6rem;}
.review-card p{font-size:.87rem;line-height:1.7;color:#374151;font-style:italic;margin-bottom:.8rem;}
.review-author{font-size:.75rem;font-weight:600;color:#9CA3AF;}
.rating-hero{display:flex;align-items:center;gap:1.2rem;margin-bottom:2rem;flex-wrap:wrap;}
.rating-num{font-family:'Bebas Neue',sans-serif;font-size:4.5rem;color:var(--rojo);line-height:1;}
.rating-info strong{display:block;font-size:.95rem;margin-bottom:.15rem;}
.rating-info span{font-size:.82rem;color:#6B7280;}
 
/* INSTAGRAM */
.insta-sec{padding:5rem 5%;background:var(--crema);text-align:center;}
.insta-sec .sec-label{color:#E1306C;}
.insta-sec .bar{background:#E1306C;margin:.8rem auto 1.2rem;}
.insta-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:.5rem;max-width:660px;margin:2rem auto;}
.insta-tile{aspect-ratio:1;border-radius:8px;overflow:hidden;position:relative;cursor:pointer;display:flex;align-items:center;justify-content:center;font-size:3rem;}
.insta-tile:hover .ig-ov{opacity:1;}
.ig-ov{position:absolute;inset:0;background:rgba(225,48,108,.8);display:flex;align-items:center;justify-content:center;color:#fff;font-size:1.6rem;opacity:0;transition:opacity .22s;}
.insta-btn{display:inline-flex;align-items:center;gap:.6rem;background:linear-gradient(135deg,#f09433,#e6683c 25%,#dc2743 50%,#cc2366 75%,#bc1888);color:#fff;padding:.75rem 2rem;border-radius:50px;font-weight:600;font-size:.9rem;text-decoration:none;transition:transform .2s,opacity .2s;margin-top:.5rem;}
.insta-btn:hover{transform:translateY(-2px);opacity:.9;}
 
/* LOCATION */
.loc-sec{background:var(--verde);display:grid;grid-template-columns:1fr 1fr;gap:3rem;padding:5rem 7%;align-items:center;}
.loc-text{color:var(--crema);}
.loc-text .sec-label{color:var(--oro2);}
.loc-text .sec-title{color:var(--crema);}
.loc-text .bar{background:var(--oro);}
.loc-rows{display:flex;flex-direction:column;gap:1rem;margin-top:.5rem;}
.loc-row{display:flex;align-items:flex-start;gap:.8rem;}
.loc-icon{font-size:1.3rem;flex-shrink:0;margin-top:.1rem;}
.loc-row-text strong{display:block;font-size:.9rem;margin-bottom:.1rem;}
.loc-row-text span{font-size:.85rem;opacity:.75;}
.map-card{background:rgba(255,255,255,.08);border:2px solid rgba(244,169,34,.3);border-radius:14px;height:280px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:.7rem;color:var(--crema);text-decoration:none;transition:background .2s;}
.map-card:hover{background:rgba(255,255,255,.13);}
.map-card span:first-child{font-size:3.5rem;}
.map-card strong{font-family:'Bebas Neue',sans-serif;font-size:1.2rem;letter-spacing:2px;color:var(--oro);}
.map-card small{font-size:.78rem;opacity:.6;letter-spacing:1px;}
 
/* FOOTER */
footer{background:var(--carbon);color:var(--crema);text-align:center;padding:3.5rem 2rem;border-top:3px solid var(--oro);}
.footer-logo{font-family:'Bebas Neue',sans-serif;font-size:2.2rem;color:var(--oro);letter-spacing:3px;margin-bottom:.4rem;}
.footer-links{display:flex;justify-content:center;gap:1.5rem;margin:1rem 0;flex-wrap:wrap;}
.footer-links a{color:#9CA3AF;text-decoration:none;font-size:.78rem;letter-spacing:1px;text-transform:uppercase;transition:color .2s;}
.footer-links a:hover{color:var(--oro);}
footer p{font-size:.8rem;opacity:.4;margin-top:.3rem;}
 
/* ANIMATIONS */
@keyframes fadeUp{from{opacity:0;transform:translateY(28px);}to{opacity:1;transform:none;}}
@keyframes float{0%,100%{transform:translateY(0);}50%{transform:translateY(-10px);}}
@keyframes ticker{from{transform:translateX(0);}to{transform:translateX(-50%);}}
.reveal{opacity:0;transform:translateY(24px);transition:opacity .65s ease,transform .65s ease;}
.reveal.visible{opacity:1;transform:none;}
 
/* RESPONSIVE */
@media(max-width:900px){
  .nav-links{display:none;}
  .about{grid-template-columns:1fr;}
  .about-visual{height:220px;}
  .birria-feat{grid-template-columns:1fr;}
  .birria-vis{height:220px;}
  .loc-sec{grid-template-columns:1fr;gap:2rem;}
  .map-card{height:180px;}
}
@media(max-width:480px){
  .hero-btns{flex-direction:column;align-items:center;}
}
</style>
</head>
<body>
 
<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">La Taquería del Rey</a>
  <ul class="nav-links">
    <li><a href="#tacos">Tacos</a></li>
    <li><a href="#burritos">Burritos</a></li>
    <li><a href="#crujientes">Crujientes</a></li>
    <li><a href="#bebidas">Bebidas</a></li>
    <li><a href="#ubicacion">Ubicación</a></li>
    <li><a href="https://www.instagram.com/lataqueriadelrey/" target="_blank" class="nav-cta">Instagram</a></li>
  </ul>
</nav>
 
<!-- HERO -->
<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-inner">
    <div class="hero-flags">🇲🇽 &nbsp;🌮&nbsp; 🤴🏻</div>
    <h1>LA<br><em>TAQUERÍA</em><br>DEL REY</h1>
    <p class="hero-tagline">Auténtica cocina de Jalisco en el norte de Bogotá</p>
    <p class="hero-sub">Birria · Tacos · Burritos · Esquites · Cocteles · Domicilios</p>
    <div class="hero-btns">
      <a href="#menu" class="btn-primary">Ver el Menú Completo</a>
      <a href="tel:3503571220" class="btn-outline">📞 350 357 1220</a>
    </div>
  </div>
</section>
 
<!-- STARS -->
<div class="stars-strip">
  <span>⭐⭐⭐⭐⭐</span>
  <span class="sep">|</span>
  <span>4.9 / 5 Google</span>
  <span class="sep">|</span>
  <span>+730 reseñas</span>
  <span class="sep">|</span>
  <span>📍 Cra. 49b #168-15 · Granada Norte</span>
  <span class="sep">|</span>
  <span>📞 350 357 1220</span>
</div>
 
<!-- TICKER -->
<div class="ticker">
  <div class="ticker-inner">
    <span class="ticker-item">Birria del Rey</span><span class="ticker-item">Quesabirria</span><span class="ticker-item">Tacos Mixtos</span><span class="ticker-item">Nachos del Rey</span><span class="ticker-item">Burritos Birria</span><span class="ticker-item">Esquites</span><span class="ticker-item">Margarita Corona</span><span class="ticker-item">Aguas Frescas</span><span class="ticker-item">Domicilios 350 357 1220</span>
    <span class="ticker-item">Birria del Rey</span><span class="ticker-item">Quesabirria</span><span class="ticker-item">Tacos Mixtos</span><span class="ticker-item">Nachos del Rey</span><span class="ticker-item">Burritos Birria</span><span class="ticker-item">Esquites</span><span class="ticker-item">Margarita Corona</span><span class="ticker-item">Aguas Frescas</span><span class="ticker-item">Domicilios 350 357 1220</span>
  </div>
</div>
 
<!-- DOMICILIOS -->
<div class="domicilios">
  <span>🛵 ¡Pedidos a domicilio!</span>
  <strong>350 357 1220</strong>
  <span>· Llámanos o escríbenos por WhatsApp</span>
</div>
 
<!-- ABOUT -->
<section class="about">
  <div class="about-text reveal">
    <p class="sec-label">Nuestra Historia</p>
    <h2 class="sec-title">De Jalisco<br>a Bogotá</h2>
    <div class="bar"></div>
    <p>Nacimos en el corazón de Jalisco, México, trayendo las recetas más auténticas y los sabores más intensos directamente al norte de Bogotá.</p>
    <p>Cada taco, cada birria, cada preparación lleva el alma de la tradición mexicana: ingredientes frescos, chiles seleccionados y pasión genuina.</p>
  </div>
  <div class="about-visual">
    <div class="about-emoji">🌮</div>
    <div class="about-stat">
      <strong>4.9★</strong>
      <span>+730 reseñas Google</span>
    </div>
  </div>
</section>
 
<!-- ══════════════════════════════════════════
     MENU COMPLETO
══════════════════════════════════════════ -->
<div class="menu-wrap" id="menu">
  <div class="menu-wrap-header reveal">
    <p class="sec-label">Todo lo que ofrecemos</p>
    <h2 class="sec-title">Menú Completo</h2>
    <div class="bar"></div>
    <p>Precios en pesos colombianos (COP) · Recetas originales de Jalisco, México</p>
  </div>
 
  <!-- ── TACOS ── -->
  <div class="cat-block cat-tacos reveal" id="tacos">
    <div class="cat-block-header">
      <span class="cat-emoji">🌮</span>
      <h2>Tacos</h2>
    </div>
    <div class="items-grid wide">
      <div class="item-card">
        <div class="item-badge badge-gold">⭐ Estrella</div>
        <div class="item-header">
          <span class="item-name">Birria del Rey</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">3 Tortillas de maíz con carne de res y queso, con consomé de 3oz como salsa para remojar, arroz Mexicano y agua fresca de chavo de Yoy. Tamarindo o Jamaica.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Birria</span>
          <span class="item-price">$23.000</span>
        </div>
        <p class="item-desc">3 Tortillas de maíz con carne de res y queso, con consomé de 3oz como salsa para remojar.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Pollo Hawai</span>
          <span class="item-price">$23.000</span>
        </div>
        <p class="item-desc">3 Tortillas de maíz con pollo, queso, piña y gullo guacamole y salsa Hawaii.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Chili Chicharrón</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">3 Tortillas de maíz con chicharrón, pico e' gallo, guacamole y salsa chicharrita.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio Mixto del Rey</span>
          <span class="item-price">$25.000</span>
        </div>
        <p class="item-desc">1 Taco de birria, 1 taco de pollo Hawai, 1 taco chili chicharrón, con sus respectivas salsas.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio de Birria Mixto Pollo Hawai</span>
          <span class="item-price">$23.000</span>
        </div>
        <p class="item-desc">2 Tacos de birria, 1 taco de pollo Hawai, con sus respectivas salsas.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio Birria Mixto Chili</span>
          <span class="item-price">$25.000</span>
        </div>
        <p class="item-desc">2 Tacos de birria, 1 taco de chili chicharrón, con sus respectivas salsas.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio Pollo Hawai Mixto Chili Chicharrón</span>
          <span class="item-price">$25.000</span>
        </div>
        <p class="item-desc">2 Tacos de pollo hawai, 1 taco de chili chicharrón, con sus respectivas salsas.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio Chili Chicharrón Mixto Birria</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">2 Tacos de chili chicharrón, 1 taco de birria, con sus respectivas salsas.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio Chili Chicharrón Mixto Pollo Hawai</span>
          <span class="item-price">$25.000</span>
        </div>
        <p class="item-desc">2 Tacos de chili chicharrón, 1 taco de pollo hawai, con sus respectivas salsas.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Trio Pollo Hawai Mixto Chili Birria</span>
          <span class="item-price">$25.000</span>
        </div>
        <p class="item-desc">1 Taco de birria, 1 taco de pollo hawai, 1 taco chili chicharrón — con sus respectivas salsas.</p>
      </div>
    </div>
 
    <!-- TACO POR UNIDAD -->
    <div style="margin-top:1.5rem; max-width:300px;">
      <div class="tacos-unit">
        <h3>🌮 Taco por Unidad</h3>
        <div class="tu-item"><span>1 Taco de Birria</span><span class="tu-price">$9.500</span></div>
        <div class="tu-item"><span>1 Taco de Pollo Hawai</span><span class="tu-price">$9.000</span></div>
        <div class="tu-item"><span>1 Taco de Chili Chicharrón</span><span class="tu-price">$9.500</span></div>
      </div>
    </div>
  </div>
 
  <!-- ── BURRITOS ── -->
  <div class="cat-block cat-burritos reveal" id="burritos">
    <div class="cat-block-header">
      <span class="cat-emoji">🌯</span>
      <h2>Burritos</h2>
    </div>
    <div class="items-grid">
      <div class="item-card">
        <div class="item-badge badge-green">Clásico</div>
        <div class="item-header">
          <span class="item-name">Burrito Birria</span>
          <span class="item-price">$34.000</span>
        </div>
        <p class="item-desc">Carne de res, arroz, frijol, totopos desmechonados, guacamole, pico e' gallo, sour cream y salsa cheddar.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Burrito Pollo Hawai</span>
          <span class="item-price">$34.000</span>
        </div>
        <p class="item-desc">Pollo hawai, limón, arroz, frijol, guacamole, pico e' gallo, sour cream y salsa cheddar.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Burrito Chili Chicharrón</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">Chicharrón, arroz, frijol, guacamole, pico e' gallo, sour cream, desmechonados y sour cream.</p>
      </div>
    </div>
    <div style="margin-top:1.2rem;">
      <p style="font-family:'Bebas Neue',sans-serif;font-size:1.2rem;letter-spacing:1px;color:var(--verde);margin-bottom:.8rem;">BURRITOS MIXTOS</p>
      <div class="items-grid">
        <div class="item-card">
          <div class="item-header">
            <span class="item-name">Mixto Birria – Pollo Hawai</span>
            <span class="item-price">$34.000</span>
          </div>
        </div>
        <div class="item-card">
          <div class="item-header">
            <span class="item-name">Mixto Birria – Chili Chicharrón</span>
            <span class="item-price">$25.000</span>
          </div>
        </div>
        <div class="item-card">
          <div class="item-header">
            <span class="item-name">Mixto Pollo Hawai – Chili Chicharrón</span>
            <span class="item-price">$25.000</span>
          </div>
        </div>
      </div>
    </div>
  </div>
 
  <!-- ── COMBOS ── -->
  <div class="cat-block cat-combos reveal" id="combos">
    <div class="cat-block-header">
      <span class="cat-emoji">🍱</span>
      <h2>Combos</h2>
    </div>
    <div class="items-grid wide">
      <div class="item-card">
        <div class="item-badge badge-orange">Combo</div>
        <div class="item-header">
          <span class="item-name">Birria</span>
          <span class="item-price">$17.000</span>
        </div>
        <p class="item-desc">3oz de birria + coca cola 250 ml</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-orange">Combo</div>
        <div class="item-header">
          <span class="item-name">Pollo Hawai</span>
          <span class="item-price">$19.000</span>
        </div>
        <p class="item-desc">2 tacos de pollo hawai + coca cola 250 ml</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-orange">Combo</div>
        <div class="item-header">
          <span class="item-name">Chili Chicharrón</span>
          <span class="item-price">$21.000</span>
        </div>
        <p class="item-desc">2 tacos de chili chicharrón + coca cola 250 ml</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-orange">Combo</div>
        <div class="item-header">
          <span class="item-name">Mixto Birria – Pollo Hawai</span>
          <span class="item-price">$19.000</span>
        </div>
        <p class="item-desc">1 taco de birria, 1 taco de pollo hawai + coca cola 250 ml</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-orange">Combo</div>
        <div class="item-header">
          <span class="item-name">Mixto Birria – Chili Chicharrón</span>
          <span class="item-price">$19.000</span>
        </div>
        <p class="item-desc">1 taco de birria, 1 taco chili chicharrón + coca cola 250 ml</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-orange">Combo</div>
        <div class="item-header">
          <span class="item-name">Mixto Pollo Hawai – Chili Chicharrón</span>
          <span class="item-price">$18.000</span>
        </div>
        <p class="item-desc">1 taco de pollo hawai + 1 taco chili chicharrón + coca cola 250 ml</p>
      </div>
    </div>
  </div>
 
  <!-- ── CRUJIENTES ── -->
  <div class="cat-block cat-crujientes reveal" id="crujientes">
    <div class="cat-block-header">
      <span class="cat-emoji">🧀</span>
      <h2>Crujientes</h2>
    </div>
    <div class="items-grid wide">
      <div class="item-card">
        <div class="item-badge badge-gold">Para compartir</div>
        <div class="item-header">
          <span class="item-name">Nachos del Rey</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">Totopos. Carne de res, queso, maíz, guacamole, pico e' gallo, sour cream.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Maduritos del Rey</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">Moneditas de plátano maduro crujiente. Carne de res, queso, maíz, guacamole, pico e' gallo, sour cream.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Mixto Nachos / Maduritos</span>
          <span class="item-price">$28.000</span>
        </div>
        <p class="item-desc">Mitad de totopos, mitad de moneditas de plátano maduro crujiente. Carne de res, queso, maíz, guacamole, pico e' gallo, sour cream.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Dorilocos</span>
          <span class="item-price">Personal $13.000 / Familiar $46.000</span>
        </div>
        <p class="item-desc">Doritos o tostácos, carne de res, queso maíz tierno, guacamole, pico e' gallo, sour cream.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Tostilocos</span>
          <span class="item-price">Personal $13.000 / Familiar $49.000</span>
        </div>
        <p class="item-desc">Trae el paquete de tu preferencia inferior a 40 gramos y te lo armamos — <strong>$12.000</strong>. Paquete entre 150 a 180 gramos — <strong>$40.000</strong>.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Porción Totopos</span>
          <span class="item-price">$12.000</span>
        </div>
        <p class="item-desc">Totopos de maíz con guacamole.</p>
      </div>
    </div>
  </div>
 
  <!-- ── ESQUITES ── -->
  <div class="cat-block cat-esquites reveal" id="esquites">
    <div class="cat-block-header">
      <span class="cat-emoji">🌽</span>
      <h2>Esquites</h2>
    </div>
    <div class="items-grid">
      <div class="item-card">
        <div class="item-badge badge-red">Estrella</div>
        <div class="item-header">
          <span class="item-name">Birria</span>
          <span class="item-price">$13.000</span>
        </div>
        <p class="item-desc">Carne de res maíz tierno, sour cream, limón, totopos o maduritos desmechonados a tu elección.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Pollo Hawai</span>
          <span class="item-price">$13.000</span>
        </div>
        <p class="item-desc">Pollo Hawai, maíz tierno, sour cream, limón, totopos o maduritos desmechonados a tu elección.</p>
      </div>
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Chili Chicharrón</span>
          <span class="item-price">$15.000</span>
        </div>
        <p class="item-desc">Chicharrón, maíz tierno, sour cream, limón, totopos o maduritos desmechonados a tu elección.</p>
      </div>
    </div>
    <div style="margin-top:1.2rem;">
      <p style="font-family:'Bebas Neue',sans-serif;font-size:1.1rem;letter-spacing:1px;color:#8B4513;margin-bottom:.8rem;">ESQUITES MIXTOS — Elige 2 mixturas</p>
      <div class="items-list">
        <div class="list-item"><span>Mixto Birria – Pollo Hawai</span><span class="lp">$13.000</span></div>
        <div class="list-item"><span>Mixto Birria – Chili Chicharrón</span><span class="lp">$14.000</span></div>
        <div class="list-item"><span>Mixto Pollo Hawai – Chili Chicharrón</span><span class="lp">$14.000</span></div>
      </div>
    </div>
  </div>
 
  <!-- ── ADICIONES ── -->
  <div class="cat-block cat-adiciones reveal" id="adiciones">
    <div class="cat-block-header">
      <span class="cat-emoji">➕</span>
      <h2>Adiciones</h2>
    </div>
    <div class="items-list">
      <div class="list-item"><span>Consomé Carnudo 5oz</span><span class="lp">$10.000</span></div>
      <div class="list-item"><span>Chicharrón</span><span class="lp">$8.000</span></div>
      <div class="list-item"><span>Carne</span><span class="lp">$8.000</span></div>
      <div class="list-item"><span>Pollo</span><span class="lp">$9.000</span></div>
      <div class="list-item"><span>Queso</span><span class="lp">$8.000</span></div>
      <div class="list-item"><span>Guacamole</span><span class="lp">$8.000</span></div>
      <div class="list-item"><span>Arroz</span><span class="lp">$4.000</span></div>
      <div class="list-item"><span>Consomé 3oz</span><span class="lp">$3.000</span></div>
      <div class="list-item"><span>Pico e' Gallo</span><span class="lp">$3.000</span></div>
    </div>
  </div>
 
  <!-- ── DULCES ── -->
  <div class="cat-block cat-dulces reveal" id="dulces">
    <div class="cat-block-header">
      <span class="cat-emoji">🍬</span>
      <h2>Dulces</h2>
    </div>
    <div class="items-list">
      <div class="list-item"><span>Bazukazo</span><span class="lp">$8.000</span></div>
      <div class="list-item"><span>Pulparindo</span><span class="lp">$5.000</span></div>
      <div class="list-item"><span>Miguelín Enchilada</span><span class="lp">$4.500</span></div>
      <div class="list-item"><span>Miguelín</span><span class="lp">$4.500</span></div>
      <div class="list-item"><span>Mazapán</span><span class="lp">$4.500</span></div>
      <div class="list-item"><span>Pulparindo</span><span class="lp">$4.000</span></div>
      <div class="list-item"><span>Pica Fresa Grande</span><span class="lp">$3.000</span></div>
      <div class="list-item"><span>Pinta Azul</span><span class="lp">$2.500</span></div>
      <div class="list-item"><span>Vero Mango</span><span class="lp">$2.500</span></div>
      <div class="list-item"><span>Vero Elite</span><span class="lp">$2.500</span></div>
      <div class="list-item"><span>Sandy Brocha</span><span class="lp">$2.500</span></div>
      <div class="list-item"><span>Trabajenguas</span><span class="lp">$2.500</span></div>
      <div class="list-item"><span>Pica Fresa Pequeña</span><span class="lp">$1.500</span></div>
    </div>
  </div>
 
  <!-- ── POSTRE ── -->
  <div class="cat-block reveal">
    <div class="cat-block-header" style="border-color:#E91E8C;">
      <span class="cat-emoji">🍨</span>
      <h2 style="color:#E91E8C;">Postre del Rey</h2>
    </div>
    <div class="items-grid">
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Postre del Rey</span>
          <span class="item-price">$15.000</span>
        </div>
        <p class="item-desc">Esquinas de chocoramo, helado, chantilly, trozos de lujo.</p>
      </div>
    </div>
  </div>
 
  <!-- ── BEBIDAS ── -->
  <div class="cat-block cat-bebidas reveal" id="bebidas">
    <div class="cat-block-header">
      <span class="cat-emoji">🥤</span>
      <h2>Otras Bebidas</h2>
    </div>
    <div style="display:grid;grid-template-columns:repeat(auto-fill,minmax(280px,1fr));gap:1.5rem;">
      <!-- Coca Cola -->
      <div class="item-card">
        <div class="item-header"><span class="item-name">Coca Cola</span></div>
        <div class="items-list" style="margin-top:.5rem;">
          <div class="list-item"><span>Original 250 ml</span><span class="lp">$3.500</span></div>
          <div class="list-item"><span>Zero 250 ml</span><span class="lp">$3.500</span></div>
          <div class="list-item"><span>Original 500 ml</span><span class="lp">$5.000</span></div>
          <div class="list-item"><span>Zero 500 ml</span><span class="lp">$5.000</span></div>
        </div>
      </div>
      <!-- Agua -->
      <div class="item-card">
        <div class="item-header"><span class="item-name">Agua Manantial</span></div>
        <div class="items-list" style="margin-top:.5rem;">
          <div class="list-item"><span>Sin gas 600 ml</span><span class="lp">$4.500</span></div>
          <div class="list-item"><span>Con gas 600 ml</span><span class="lp">$4.500</span></div>
        </div>
      </div>
      <!-- Cola y Pola -->
      <div class="item-card">
        <div class="item-header">
          <span class="item-name">Cola y Pola</span>
          <span class="item-price">$5.000</span>
        </div>
      </div>
    </div>
 
    <!-- SHOT DE TEQUILA -->
    <div style="margin-top:1.5rem;">
      <p style="font-family:'Bebas Neue',sans-serif;font-size:1.2rem;letter-spacing:1px;color:var(--azul);margin-bottom:.8rem;">🥃 Shot de Tequila / Saborizador — Trago 2oz con sal</p>
      <div class="items-list">
        <div class="list-item"><span>Blanco</span><span class="lp">$15.000</span></div>
        <div class="list-item"><span>Reposado</span><span class="lp">$16.000</span></div>
      </div>
    </div>
 
    <!-- CERVEZAS -->
    <div style="margin-top:1.5rem;">
      <p style="font-family:'Bebas Neue',sans-serif;font-size:1.2rem;letter-spacing:1px;color:var(--azul);margin-bottom:.8rem;">🍺 Cervezas</p>
      <div class="items-list">
        <div class="list-item"><span>Tecate</span><span class="lp">$6.000</span></div>
        <div class="list-item"><span>Coronita Original</span><span class="lp">$9.000</span></div>
        <div class="list-item"><span>Coronita Chelado</span><span class="lp">$8.000</span></div>
        <div class="list-item"><span>Coronita Michelada</span><span class="lp">$8.000</span></div>
        <div class="list-item"><span>Coronita Cubana (limón, sal, tajín)</span><span class="lp">$10.000</span></div>
        <div class="list-item"><span>Coronita Chamoyada (limón, tajín, chamoy, salsa picante)</span><span class="lp">$11.000</span></div>
        <div class="list-item"><span>Coronita Sangriento (limón, tajín, chamoy)</span><span class="lp">$12.000</span></div>
      </div>
    </div>
  </div>
 
  <!-- ── AGUAS FRESCAS ── -->
  <div class="cat-block cat-aguas reveal" id="aguas">
    <div class="cat-block-header">
      <span class="cat-emoji">🫙</span>
      <h2>Aguas Frescas del Chavo</h2>
    </div>
    <div class="items-grid">
      <div class="item-card">
        <div class="item-header"><span class="item-name">Tamarindo</span></div>
        <div class="items-list" style="margin-top:.5rem;">
          <div class="list-item"><span>Vaso pequeño (9oz)</span><span class="lp">$4.500</span></div>
          <div class="list-item"><span>Vaso grande (16oz)</span><span class="lp">$6.500</span></div>
        </div>
      </div>
      <div class="item-card">
        <div class="item-header"><span class="item-name">Jamaica</span></div>
        <div class="items-list" style="margin-top:.5rem;">
          <div class="list-item"><span>Vaso pequeño (9oz)</span><span class="lp">$4.500</span></div>
          <div class="list-item"><span>Vaso grande (16oz)</span><span class="lp">$6.500</span></div>
        </div>
      </div>
      <div class="item-card">
        <div class="item-header"><span class="item-name">Horchata</span></div>
        <div class="items-list" style="margin-top:.5rem;">
          <div class="list-item"><span>Vaso pequeño (9oz)</span><span class="lp">$5.000</span></div>
          <div class="list-item"><span>Vaso grande (16oz)</span><span class="lp">$7.000</span></div>
        </div>
      </div>
    </div>
  </div>
 
  <!-- ── COCTELES MEDIO LITRO ── -->
  <div class="cat-block cat-cocteles reveal" id="cocteles">
    <div class="cat-block-header">
      <span class="cat-emoji">🍹</span>
      <h2>Cocteles Medio Litro</h2>
    </div>
    <div class="items-grid wide">
      <div class="item-card">
        <div class="item-badge badge-red">🍹 Coctel</div>
        <div class="item-header">
          <span class="item-name">Margarita Corona</span>
          <span class="item-price">$40.000</span>
        </div>
        <p class="item-desc">Tequila, zumo de limón, chamoy, tajín, triple sec y cerveza corona.</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-red">🍹 Coctel</div>
        <div class="item-header">
          <span class="item-name">Mezcalina de Jamaica</span>
          <span class="item-price">$38.000</span>
        </div>
        <p class="item-desc">Mezcal, zumo de limón, chamoy, tajín y jarabe de Jamaica natural.</p>
      </div>
      <div class="item-card">
        <div class="item-badge badge-red">🍹 Coctel</div>
        <div class="item-header">
          <span class="item-name">Margarita de Tamarindo</span>
          <span class="item-price">$38.000</span>
        </div>
        <p class="item-desc">Tequila, chamoy, tajín, triple sec, tamarindo y dulce de su elección: Bazucazo, Pulparindo/s o Miguelín.</p>
      </div>
    </div>
  </div>
 
</div><!-- END menu-wrap -->
 
<!-- BIRRIA FEATURE -->
<section class="birria-feat" id="birria">
  <div class="birria-vis">
    <div class="flame">🔥</div>
  </div>
  <div class="birria-text reveal">
    <p class="sec-label">La estrella de la casa</p>
    <h2 class="sec-title">La Mejor<br>Birria<br>de Bogotá</h2>
    <div class="bar"></div>
    <p>Marinamos la carne por horas en una mezcla de chiles de árbol, guajillo y ancho, con especias de Jalisco. La cocinamos a fuego lento hasta lograr esa textura que se deshace sola.</p>
    <p>El consomé resultante es oro líquido — sírvelo como sopa o dipea tus tacos en él.</p>
    <div class="birria-pill">🇲🇽 Receta Original de Jalisco</div>
  </div>
</section>
 
<!-- REVIEWS -->
<section class="reviews-sec" id="resenas">
  <div class="reveal">
    <p class="sec-label">Lo que dicen</p>
    <h2 class="sec-title">Reseñas</h2>
    <div class="bar"></div>
    <div class="rating-hero">
      <div class="rating-num">4.9</div>
      <div class="rating-info">
        <strong>⭐⭐⭐⭐⭐ Excelente</strong>
        <span>+730 reseñas verificadas · Google Maps</span>
      </div>
    </div>
  </div>
  <div class="reviews-grid">
    <div class="review-card reveal">
      <div class="review-stars">⭐⭐⭐⭐⭐</div>
      <p>"Comida deliciosa y ambiente agradable. La birria es la mejor que he probado en Bogotá. ¡Muy recomendado!"</p>
      <div class="review-author">— Cliente verificado · Google</div>
    </div>
    <div class="review-card reveal">
      <div class="review-stars">⭐⭐⭐⭐⭐</div>
      <p>"Los tacos de birria son auténticos. El consomé sabe exactamente como en México. ¡Volveré siempre!"</p>
      <div class="review-author">— Cliente verificado · Google</div>
    </div>
    <div class="review-card reveal">
      <div class="review-stars">⭐⭐⭐⭐⭐</div>
      <p>"Servicio excelente y precios muy buenos para la calidad. Los nachos del rey y los cocteles son increíbles."</p>
      <div class="review-author">— Cliente verificado · Google</div>
    </div>
    <div class="review-card reveal">
      <div class="review-stars">⭐⭐⭐⭐⭐</div>
      <p>"¡Espectacular! Ambiente, atención y comida. Una experiencia mexicana auténtica en Bogotá."</p>
      <div class="review-author">— Cliente verificado · Google</div>
    </div>
  </div>
</section>
 
<!-- INSTAGRAM -->
<section class="insta-sec" id="instagram">
  <p class="sec-label reveal">Síguenos</p>
  <h2 class="sec-title reveal">@lataqueriadelrey</h2>
  <div class="bar reveal"></div>
  <p class="reveal" style="color:#6B7280;">2.190 seguidores · Bogotá, Colombia · Fotos y promociones</p>
  <div class="insta-grid reveal">
    <div class="insta-tile" style="background:#fef3cd">🌮<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#fee2e2">🫕<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#d1fae5">🌯<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#ffedd5">🔥<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#fef9c3">🌽<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#ecfdf5">🥤<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#fff1f2">🍺<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#fefce8">🇲🇽<div class="ig-ov">❤️</div></div>
    <div class="insta-tile" style="background:#fce7f3">🍹<div class="ig-ov">❤️</div></div>
  </div>
  <a class="insta-btn reveal" href="https://www.instagram.com/lataqueriadelrey/" target="_blank">📸 Ver en Instagram</a>
</section>
 
<!-- LOCATION -->
<section class="loc-sec" id="ubicacion">
  <div class="loc-text reveal">
    <p class="sec-label">Visítanos</p>
    <h2 class="sec-title">Encuéntranos</h2>
    <div class="bar"></div>
    <div class="loc-rows">
      <div class="loc-row">
        <span class="loc-icon">📍</span>
        <div class="loc-row-text"><strong>Dirección</strong><span>Cra. 49b #168-15, Granada Norte, Bogotá</span></div>
      </div>
      <div class="loc-row">
        <span class="loc-icon">📞</span>
        <div class="loc-row-text"><strong>Domicilios</strong><span>350 357 1220</span></div>
      </div>
      <div class="loc-row">
        <span class="loc-icon">💰</span>
        <div class="loc-row-text"><strong>Precio por persona</strong><span>$20.000 – $40.000 COP</span></div>
      </div>
      <div class="loc-row">
        <span class="loc-icon">⭐</span>
        <div class="loc-row-text"><strong>Calificación</strong><span>4.9 / 5 · +730 reseñas en Google</span></div>
      </div>
    </div>
  </div>
  <a class="map-card reveal" href="https://maps.app.goo.gl/Cf4ZXRs62nG5LUuu7" target="_blank">
    <span>🗺️</span>
    <strong>Ver en Google Maps</strong>
    <small>Cra. 49b #168-15 · Granada Norte</small>
  </a>
</section>
 
<!-- FOOTER -->
<footer>
  <div class="footer-logo">La Taquería del Rey 🌮</div>
  <div class="footer-links">
    <a href="#tacos">Tacos</a>
    <a href="#burritos">Burritos</a>
    <a href="#crujientes">Crujientes</a>
    <a href="#bebidas">Bebidas</a>
    <a href="#cocteles">Cocteles</a>
    <a href="https://www.instagram.com/lataqueriadelrey/" target="_blank">Instagram</a>
    <a href="https://maps.app.goo.gl/Cf4ZXRs62nG5LUuu7" target="_blank">Google Maps</a>
  </div>
  <p>🛵 Domicilios: 350 357 1220</p>
  <p>Cra. 49b #168-15 · Granada Norte · Bogotá, Colombia</p>
  <p style="margin-top:1rem;">© 2025 La Taquería del Rey · Todos los derechos reservados</p>
</footer>
 
<script>
const io = new IntersectionObserver(entries => {
  entries.forEach(e => { if(e.isIntersecting){ e.target.classList.add('visible'); io.unobserve(e.target); }});
}, { threshold:.08 });
document.querySelectorAll('.reveal').forEach(el => io.observe(el));
</script>
</body>
</html>
