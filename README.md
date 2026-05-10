<!DOCTYPE html>

<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GROWTH VV – Social Media Growth</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;600;700;900&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --black: #05030f;
    --deep: #0a0618;
    --violet: #7c3aed;
    --violet-light: #a855f7;
    --violet-bright: #c084fc;
    --violet-glow: rgba(124,58,237,0.4);
    --white: #ffffff;
    --gray: #a1a1aa;
    --card-bg: rgba(124,58,237,0.06);
    --border: rgba(124,58,237,0.25);
  }
  *, *::before, *::after { margin:0; padding:0; box-sizing:border-box; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--black);
    color: var(--white);
    font-family: 'Montserrat', sans-serif;
    overflow-x: hidden;
  }

/* ── PARTICLES ── */
#particles {
position: fixed; inset: 0; pointer-events: none; z-index: 0;
overflow: hidden;
}
.particle {
position: absolute;
border-radius: 50%;
background: var(–violet);
opacity: 0;
animation: float linear infinite;
}
@keyframes float {
0%   { transform: translateY(100vh) scale(0); opacity: 0; }
10%  { opacity: 0.6; }
90%  { opacity: 0.3; }
100% { transform: translateY(-10vh) scale(1); opacity: 0; }
}

/* ── NAV ── */
nav {
position: fixed; top: 0; left: 0; right: 0; z-index: 100;
display: flex; align-items: center; justify-content: space-between;
padding: 1.2rem 2rem;
background: rgba(5,3,15,0.85);
backdrop-filter: blur(20px);
border-bottom: 1px solid var(–border);
}
.nav-logo {
font-family: ‘Orbitron’, sans-serif;
font-weight: 900; font-size: 1.15rem;
letter-spacing: 0.12em;
background: linear-gradient(135deg, #fff 30%, var(–violet-bright));
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
text-shadow: none;
}
.nav-links { display: flex; gap: 2rem; list-style: none; }
.nav-links a {
color: var(–gray); text-decoration: none;
font-size: 0.78rem; font-weight: 600; letter-spacing: 0.08em;
text-transform: uppercase; transition: color 0.2s;
}
.nav-links a:hover { color: var(–violet-bright); }
.nav-cta {
background: var(–violet); color: #fff;
padding: 0.55rem 1.3rem; border-radius: 6px;
font-size: 0.78rem; font-weight: 700; letter-spacing: 0.06em;
text-decoration: none; text-transform: uppercase;
transition: background 0.2s, box-shadow 0.2s;
box-shadow: 0 0 20px var(–violet-glow);
}
.nav-cta:hover { background: var(–violet-light); box-shadow: 0 0 35px var(–violet-glow); }
.hamburger { display: none; flex-direction: column; gap: 5px; cursor: pointer; }
.hamburger span { width: 22px; height: 2px; background: var(–white); border-radius: 2px; transition: 0.3s; }

/* ── HERO ── */
#home {
min-height: 100vh;
display: flex; flex-direction: column;
align-items: center; justify-content: center;
text-align: center;
padding: 6rem 1.5rem 4rem;
position: relative; z-index: 1;
}
.hero-badge {
display: inline-flex; align-items: center; gap: 0.5rem;
background: rgba(124,58,237,0.12);
border: 1px solid var(–border);
border-radius: 99px; padding: 0.4rem 1rem;
font-size: 0.72rem; font-weight: 600;
letter-spacing: 0.12em; text-transform: uppercase;
color: var(–violet-bright); margin-bottom: 2rem;
animation: fadeUp 0.8s ease both;
}
.hero-badge span { width:6px; height:6px; background: var(–violet-bright); border-radius:50%; display:inline-block; animation: pulse 1.5s infinite; }
@keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.4;transform:scale(1.5)} }

.hero-title {
font-family: ‘Orbitron’, sans-serif;
font-weight: 900;
font-size: clamp(2.8rem, 8vw, 6.5rem);
line-height: 1.0;
letter-spacing: 0.04em;
animation: fadeUp 0.9s 0.1s ease both;
}
.hero-title .line1 {
display: block;
background: linear-gradient(135deg, #fff 30%, var(–violet-bright) 80%);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
text-shadow: none;
filter: drop-shadow(0 0 40px rgba(168,85,247,0.5));
}
.hero-title .line2 {
display: block;
font-size: clamp(1rem, 3vw, 1.8rem);
font-weight: 600;
letter-spacing: 0.3em;
color: var(–gray);
-webkit-text-fill-color: var(–gray);
margin-top: 0.5rem;
}
.hero-sub {
margin-top: 1.5rem;
font-size: clamp(0.9rem, 2.5vw, 1.15rem);
color: var(–gray);
letter-spacing: 0.06em;
animation: fadeUp 1s 0.2s ease both;
}
.hero-sub strong { color: var(–violet-bright); }
.hero-buttons {
margin-top: 2.5rem;
display: flex; gap: 1rem; flex-wrap: wrap; justify-content: center;
animation: fadeUp 1s 0.3s ease both;
}
.btn-primary {
background: linear-gradient(135deg, var(–violet), var(–violet-light));
color: #fff; padding: 0.9rem 2.2rem;
border-radius: 8px; font-weight: 700;
font-size: 0.9rem; letter-spacing: 0.06em;
text-decoration: none; text-transform: uppercase;
box-shadow: 0 0 30px var(–violet-glow);
transition: transform 0.2s, box-shadow 0.2s;
}
.btn-primary:hover { transform: translateY(-2px); box-shadow: 0 0 50px rgba(124,58,237,0.6); }
.btn-whatsapp {
background: rgba(37,211,102,0.1);
border: 1px solid rgba(37,211,102,0.4);
color: #25d366; padding: 0.9rem 2.2rem;
border-radius: 8px; font-weight: 700;
font-size: 0.9rem; letter-spacing: 0.06em;
text-decoration: none; text-transform: uppercase;
transition: transform 0.2s, background 0.2s;
display: flex; align-items: center; gap: 0.5rem;
}
.btn-whatsapp:hover { transform: translateY(-2px); background: rgba(37,211,102,0.18); }
.hero-stats {
margin-top: 4rem;
display: flex; gap: 3rem; flex-wrap: wrap; justify-content: center;
animation: fadeUp 1s 0.4s ease both;
}
.stat { text-align: center; }
.stat-num {
font-family: ‘Orbitron’, sans-serif;
font-size: 1.8rem; font-weight: 900;
background: linear-gradient(135deg, #fff, var(–violet-bright));
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
}
.stat-label { font-size: 0.72rem; color: var(–gray); letter-spacing: 0.1em; text-transform: uppercase; margin-top: 0.2rem; }

@keyframes fadeUp { from{opacity:0;transform:translateY(24px)} to{opacity:1;transform:translateY(0)} }

/* ── SECTION SHARED ── */
section { padding: 6rem 1.5rem; position: relative; z-index: 1; }
.section-label {
text-align: center;
font-size: 0.72rem; font-weight: 700;
letter-spacing: 0.2em; text-transform: uppercase;
color: var(–violet-bright); margin-bottom: 0.8rem;
}
.section-title {
text-align: center;
font-family: ‘Orbitron’, sans-serif;
font-size: clamp(1.6rem, 4vw, 2.8rem);
font-weight: 700; margin-bottom: 0.8rem;
}
.section-desc {
text-align: center; color: var(–gray);
font-size: 0.95rem; max-width: 520px; margin: 0 auto 3.5rem;
line-height: 1.7;
}
.divider {
width: 60px; height: 2px;
background: linear-gradient(90deg, var(–violet), var(–violet-bright));
margin: 0.8rem auto 0;
border-radius: 2px;
}

/* ── SERVICIOS ── */
#servicios { background: var(–deep); }
.services-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
gap: 1.5rem; max-width: 960px; margin: 0 auto;
}
.service-card {
background: var(–card-bg);
border: 1px solid var(–border);
border-radius: 16px; padding: 2rem;
transition: transform 0.3s, box-shadow 0.3s, border-color 0.3s;
}
.service-card:hover {
transform: translateY(-6px);
border-color: var(–violet);
box-shadow: 0 0 40px rgba(124,58,237,0.2);
}
.service-icon { font-size: 2.5rem; margin-bottom: 1rem; }
.service-name {
font-family: ‘Orbitron’, sans-serif;
font-size: 1.1rem; font-weight: 700;
margin-bottom: 1rem; color: var(–white);
}
.service-items { display: flex; gap: 0.5rem; flex-wrap: wrap; }
.service-tag {
background: rgba(124,58,237,0.15);
border: 1px solid var(–border);
border-radius: 99px; padding: 0.3rem 0.8rem;
font-size: 0.75rem; font-weight: 600;
color: var(–violet-bright);
}

/* ── PRECIOS ── */
#precios { background: var(–black); }
.prices-tabs {
display: flex; gap: 0.5rem; justify-content: center;
margin-bottom: 3rem; flex-wrap: wrap;
}
.tab-btn {
background: transparent;
border: 1px solid var(–border);
color: var(–gray); padding: 0.6rem 1.6rem;
border-radius: 8px; cursor: pointer;
font-family: ‘Montserrat’, sans-serif;
font-size: 0.82rem; font-weight: 700;
letter-spacing: 0.06em; text-transform: uppercase;
transition: all 0.2s;
}
.tab-btn.active, .tab-btn:hover {
background: var(–violet); border-color: var(–violet);
color: #fff; box-shadow: 0 0 20px var(–violet-glow);
}
.tab-content { display: none; max-width: 960px; margin: 0 auto; }
.tab-content.active { display: block; }
.price-section-title {
font-family: ‘Orbitron’, sans-serif;
font-size: 0.9rem; font-weight: 700;
color: var(–violet-bright); letter-spacing: 0.15em;
text-transform: uppercase; margin-bottom: 1rem; margin-top: 2rem;
}
.price-grid {
display: grid;
grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
gap: 1rem; margin-bottom: 2rem;
}
.price-card {
background: var(–card-bg);
border: 1px solid var(–border);
border-radius: 12px; padding: 1.4rem;
text-align: center;
transition: all 0.25s;
cursor: default;
}
.price-card:hover {
border-color: var(–violet);
box-shadow: 0 0 25px rgba(124,58,237,0.2);
transform: translateY(-4px);
}
.price-qty {
font-family: ‘Orbitron’, sans-serif;
font-size: 1.1rem; font-weight: 700; color: var(–white);
}
.price-amount {
font-size: 1.4rem; font-weight: 800; margin-top: 0.5rem;
background: linear-gradient(135deg, var(–violet-bright), #fff);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
}
.price-currency { font-size: 0.7rem; color: var(–gray); margin-top: 0.2rem; }

/* ── COMBOS ── */
#combos { background: var(–deep); }
.combos-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
gap: 1.5rem; max-width: 960px; margin: 0 auto;
}
.combo-card {
background: var(–card-bg);
border: 1px solid var(–border);
border-radius: 20px; padding: 2.2rem;
text-align: center; position: relative;
transition: all 0.3s; overflow: hidden;
}
.combo-card::before {
content: ‘’;
position: absolute; top: 0; left: 0; right: 0; height: 2px;
background: linear-gradient(90deg, transparent, var(–violet), transparent);
}
.combo-card.featured {
border-color: var(–violet);
box-shadow: 0 0 50px rgba(124,58,237,0.25);
}
.combo-card:hover { transform: translateY(-8px); box-shadow: 0 0 60px rgba(124,58,237,0.3); }
.combo-badge {
display: inline-block;
background: linear-gradient(135deg, var(–violet), var(–violet-light));
border-radius: 99px; padding: 0.3rem 1rem;
font-size: 0.72rem; font-weight: 700;
letter-spacing: 0.1em; text-transform: uppercase;
margin-bottom: 1rem;
}
.combo-emoji { font-size: 2.5rem; margin-bottom: 0.8rem; display: block; }
.combo-name {
font-family: ‘Orbitron’, sans-serif;
font-size: 1.15rem; font-weight: 800;
margin-bottom: 1.5rem; color: var(–white);
}
.combo-features { list-style: none; margin-bottom: 1.8rem; }
.combo-features li {
padding: 0.4rem 0;
font-size: 0.88rem; color: var(–gray);
border-bottom: 1px solid rgba(124,58,237,0.1);
display: flex; align-items: center; justify-content: center; gap: 0.5rem;
}
.combo-features li::before { content: ‘✦’; color: var(–violet-bright); font-size: 0.6rem; }
.combo-price {
font-family: ‘Orbitron’, sans-serif;
font-size: 2rem; font-weight: 900;
background: linear-gradient(135deg, var(–violet-bright), #fff);
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
margin-bottom: 1.5rem;
}
.btn-combo {
display: block; width: 100%;
background: linear-gradient(135deg, var(–violet), var(–violet-light));
color: #fff; padding: 0.85rem;
border-radius: 8px; font-weight: 700;
font-size: 0.82rem; letter-spacing: 0.08em;
text-decoration: none; text-transform: uppercase;
transition: all 0.2s;
box-shadow: 0 0 20px var(–violet-glow);
}
.btn-combo:hover { box-shadow: 0 0 40px rgba(124,58,237,0.5); transform: translateY(-2px); }

/* ── BENEFICIOS ── */
#beneficios { background: var(–black); }
.benefits-grid {
display: grid;
grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
gap: 1.5rem; max-width: 900px; margin: 0 auto;
}
.benefit-card {
background: var(–card-bg);
border: 1px solid var(–border);
border-radius: 14px; padding: 1.8rem;
text-align: center;
transition: all 0.3s;
}
.benefit-card:hover {
border-color: var(–violet);
box-shadow: 0 0 30px rgba(124,58,237,0.15);
transform: translateY(-4px);
}
.benefit-icon { font-size: 2.2rem; margin-bottom: 1rem; display: block; }
.benefit-title {
font-weight: 700; font-size: 0.95rem;
margin-bottom: 0.5rem; color: var(–white);
}
.benefit-desc { font-size: 0.8rem; color: var(–gray); line-height: 1.6; }

/* ── FAQ ── */
#faq { background: var(–deep); }
.faq-list { max-width: 680px; margin: 0 auto; }
.faq-item {
border: 1px solid var(–border);
border-radius: 12px; margin-bottom: 1rem;
overflow: hidden;
transition: border-color 0.2s;
}
.faq-item.open { border-color: var(–violet); }
.faq-question {
width: 100%; background: var(–card-bg);
border: none; color: var(–white);
padding: 1.3rem 1.5rem;
font-family: ‘Montserrat’, sans-serif;
font-size: 0.9rem; font-weight: 600;
text-align: left; cursor: pointer;
display: flex; justify-content: space-between; align-items: center;
transition: background 0.2s;
}
.faq-question:hover { background: rgba(124,58,237,0.12); }
.faq-icon {
color: var(–violet-bright); font-size: 1.2rem;
transition: transform 0.3s; flex-shrink: 0;
}
.faq-item.open .faq-icon { transform: rotate(45deg); }
.faq-answer {
max-height: 0; overflow: hidden;
transition: max-height 0.4s ease, padding 0.3s;
padding: 0 1.5rem;
font-size: 0.88rem; color: var(–gray); line-height: 1.7;
}
.faq-item.open .faq-answer { max-height: 200px; padding: 0 1.5rem 1.3rem; }

/* ── CONTACTO ── */
#contacto {
background: var(–black);
text-align: center;
}
.contact-card {
background: var(–card-bg);
border: 1px solid var(–border);
border-radius: 20px; padding: 3rem 2rem;
max-width: 560px; margin: 0 auto;
position: relative; overflow: hidden;
}
.contact-card::before {
content: ‘’;
position: absolute; top: 0; left: 0; right: 0; height: 1px;
background: linear-gradient(90deg, transparent, var(–violet), transparent);
}
.contact-glow {
position: absolute; top: -60px; left: 50%;
transform: translateX(-50%);
width: 200px; height: 200px;
background: radial-gradient(circle, rgba(124,58,237,0.3) 0%, transparent 70%);
pointer-events: none;
}
.contact-title {
font-family: ‘Orbitron’, sans-serif;
font-size: 1.5rem; font-weight: 800;
margin-bottom: 0.8rem;
}
.contact-desc { color: var(–gray); font-size: 0.88rem; margin-bottom: 2rem; line-height: 1.7; }
.contact-buttons { display: flex; flex-direction: column; gap: 1rem; }
.btn-contact-wa {
background: linear-gradient(135deg, #128C7E, #25d366);
color: #fff; padding: 1rem;
border-radius: 10px; font-weight: 700;
font-size: 0.9rem; letter-spacing: 0.06em;
text-decoration: none; text-transform: uppercase;
display: flex; align-items: center; justify-content: center; gap: 0.6rem;
transition: all 0.2s; box-shadow: 0 0 20px rgba(37,211,102,0.25);
}
.btn-contact-wa:hover { transform: translateY(-2px); box-shadow: 0 0 40px rgba(37,211,102,0.4); }
.btn-contact-ig {
background: linear-gradient(135deg, #833ab4, #fd1d1d, #f77737);
color: #fff; padding: 1rem;
border-radius: 10px; font-weight: 700;
font-size: 0.9rem; letter-spacing: 0.06em;
text-decoration: none; text-transform: uppercase;
display: flex; align-items: center; justify-content: center; gap: 0.6rem;
transition: all 0.2s; box-shadow: 0 0 20px rgba(131,58,180,0.25);
}
.btn-contact-ig:hover { transform: translateY(-2px); box-shadow: 0 0 40px rgba(131,58,180,0.4); }

/* ── FOOTER ── */
footer {
background: var(–deep);
border-top: 1px solid var(–border);
padding: 2rem 1.5rem; text-align: center;
}
.footer-logo {
font-family: ‘Orbitron’, sans-serif;
font-weight: 900; font-size: 1rem;
background: linear-gradient(135deg, #fff 30%, var(–violet-bright));
-webkit-background-clip: text; -webkit-text-fill-color: transparent;
letter-spacing: 0.15em; margin-bottom: 0.5rem;
}
.footer-slogan { color: var(–gray); font-size: 0.78rem; letter-spacing: 0.08em; }
.footer-copy { color: rgba(161,161,170,0.4); font-size: 0.72rem; margin-top: 1.2rem; }

/* ── GLOW ORBS ── */
.orb {
position: fixed; border-radius: 50%;
pointer-events: none; z-index: 0;
filter: blur(80px); opacity: 0.25;
}
.orb-1 { width: 500px; height: 500px; background: var(–violet); top: -200px; left: -200px; }
.orb-2 { width: 400px; height: 400px; background: var(–violet-light); bottom: -150px; right: -150px; }

/* ── SCROLL REVEAL ── */
.reveal { opacity: 0; transform: translateY(30px); transition: all 0.7s ease; }
.reveal.visible { opacity: 1; transform: translateY(0); }

/* ── MOBILE ── */
@media (max-width: 768px) {
.nav-links { display: none; }
.nav-cta { display: none; }
.hamburger { display: flex; }
nav { padding: 1rem 1.2rem; }
.hero-stats { gap: 1.5rem; }
.stat-num { font-size: 1.4rem; }
section { padding: 4rem 1rem; }
}

/* Mobile nav open */
.mobile-menu {
position: fixed; inset: 0; z-index: 99;
background: rgba(5,3,15,0.97);
backdrop-filter: blur(20px);
display: none; flex-direction: column;
align-items: center; justify-content: center;
gap: 2rem;
}
.mobile-menu.open { display: flex; }
.mobile-menu a {
font-family: ‘Orbitron’, sans-serif;
font-size: 1.2rem; font-weight: 700;
color: var(–white); text-decoration: none;
letter-spacing: 0.1em; text-transform: uppercase;
transition: color 0.2s;
}
.mobile-menu a:hover { color: var(–violet-bright); }
.close-menu {
position: absolute; top: 1.5rem; right: 1.5rem;
background: none; border: none; color: var(–white);
font-size: 1.8rem; cursor: pointer;
}
</style>

</head>
<body>

<!-- Background Orbs -->

<div class="orb orb-1"></div>
<div class="orb orb-2"></div>

<!-- Particles -->

<div id="particles"></div>

<!-- Mobile Menu -->

<div class="mobile-menu" id="mobileMenu">
  <button class="close-menu" onclick="closeMobileMenu()">✕</button>
  <a href="#home" onclick="closeMobileMenu()">Inicio</a>
  <a href="#servicios" onclick="closeMobileMenu()">Servicios</a>
  <a href="#precios" onclick="closeMobileMenu()">Precios</a>
  <a href="#combos" onclick="closeMobileMenu()">Combos</a>
  <a href="#beneficios" onclick="closeMobileMenu()">Beneficios</a>
  <a href="#faq" onclick="closeMobileMenu()">FAQ</a>
  <a href="#contacto" onclick="closeMobileMenu()">Contacto</a>
</div>

<!-- NAV -->

<nav>
  <div class="nav-logo">GROWTH VV</div>
  <ul class="nav-links">
    <li><a href="#home">Inicio</a></li>
    <li><a href="#servicios">Servicios</a></li>
    <li><a href="#precios">Precios</a></li>
    <li><a href="#combos">Combos</a></li>
    <li><a href="#beneficios">Beneficios</a></li>
    <li><a href="#faq">FAQ</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
  <a href="https://wa.me/549XXXXXXXXXX" class="nav-cta">WhatsApp</a>
  <div class="hamburger" onclick="openMobileMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- HOME -->

<section id="home">
  <div class="hero-badge"><span></span> Social Media Growth Agency</div>
  <h1 class="hero-title">
    <span class="line1">GROWTH VV</span>
    <span class="line2">SOCIAL MEDIA GROWTH</span>
  </h1>
  <p class="hero-sub"><strong>Seguidores</strong> • <strong>Likes</strong> • <strong>Views</strong></p>
  <div class="hero-buttons">
    <a href="#precios" class="btn-primary">⚡ Comprar Ahora</a>
    <a href="https://wa.me/549XXXXXXXXXX" class="btn-whatsapp">
      <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.553 4.113 1.519 5.847L.057 23.495a.5.5 0 00.609.61l5.819-1.527A11.952 11.952 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.959 0-3.797-.5-5.4-1.377l-.387-.222-4.02 1.055 1.07-3.91-.245-.397A9.954 9.954 0 012 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z"/></svg>
      WhatsApp
    </a>
  </div>
  <div class="hero-stats">
    <div class="stat">
      <div class="stat-num">500+</div>
      <div class="stat-label">Clientes satisfechos</div>
    </div>
    <div class="stat">
      <div class="stat-num">24/7</div>
      <div class="stat-label">Soporte activo</div>
    </div>
    <div class="stat">
      <div class="stat-num">3</div>
      <div class="stat-label">Plataformas</div>
    </div>
    <div class="stat">
      <div class="stat-num">100%</div>
      <div class="stat-label">Garantía refill</div>
    </div>
  </div>
</section>

<!-- SERVICIOS -->

<section id="servicios">
  <p class="section-label">Lo que ofrecemos</p>
  <h2 class="section-title">Nuestros Servicios</h2>
  <div class="divider"></div>
  <p class="section-desc">Impulsamos tu presencia en las principales redes sociales con resultados reales y entrega garantizada.</p>
  <div class="services-grid reveal">
    <div class="service-card">
      <div class="service-icon">📸</div>
      <div class="service-name">Instagram</div>
      <div class="service-items">
        <span class="service-tag">Seguidores</span>
        <span class="service-tag">Likes</span>
        <span class="service-tag">Views</span>
      </div>
    </div>
    <div class="service-card">
      <div class="service-icon">🎵</div>
      <div class="service-name">TikTok</div>
      <div class="service-items">
        <span class="service-tag">Seguidores</span>
        <span class="service-tag">Likes</span>
        <span class="service-tag">Views</span>
      </div>
    </div>
    <div class="service-card">
      <div class="service-icon">👥</div>
      <div class="service-name">Facebook</div>
      <div class="service-items">
        <span class="service-tag">Seguidores</span>
        <span class="service-tag">Likes</span>
      </div>
    </div>
  </div>
</section>

<!-- PRECIOS -->

<section id="precios">
  <p class="section-label">Inversión</p>
  <h2 class="section-title">Precios</h2>
  <div class="divider"></div>
  <p class="section-desc">Precios en pesos argentinos. Elegí la plataforma y el servicio que necesitás.</p>
  <div class="prices-tabs">
    <button class="tab-btn active" onclick="showTab('ig')">📸 Instagram</button>
    <button class="tab-btn" onclick="showTab('tt')">🎵 TikTok</button>
    <button class="tab-btn" onclick="showTab('fb')">👥 Facebook</button>
  </div>

  <!-- INSTAGRAM -->

  <div class="tab-content active reveal" id="tab-ig">
    <p class="price-section-title">👥 Seguidores</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">500</div><div class="price-amount">$4.500</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">1.000</div><div class="price-amount">$8.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">2.500</div><div class="price-amount">$17.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">5.000</div><div class="price-amount">$30.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$55.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">50.000</div><div class="price-amount">$230.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">100.000</div><div class="price-amount">$420.000</div><div class="price-currency">ARS</div></div>
    </div>
    <p class="price-section-title">❤️ Likes</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">1.000</div><div class="price-amount">$2.800</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">5.000</div><div class="price-amount">$11.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$20.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">50.000</div><div class="price-amount">$85.000</div><div class="price-currency">ARS</div></div>
    </div>
    <p class="price-section-title">👁 Views</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$2.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">50.000</div><div class="price-amount">$6.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">100.000</div><div class="price-amount">$10.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">1.000.000</div><div class="price-amount">$65.000</div><div class="price-currency">ARS</div></div>
    </div>
  </div>

  <!-- TIKTOK -->

  <div class="tab-content" id="tab-tt">
    <p class="price-section-title">👥 Seguidores</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">1.000</div><div class="price-amount">$10.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">5.000</div><div class="price-amount">$45.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$85.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">50.000</div><div class="price-amount">$360.000</div><div class="price-currency">ARS</div></div>
    </div>
    <p class="price-section-title">❤️ Likes</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">1.000</div><div class="price-amount">$3.500</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$22.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">50.000</div><div class="price-amount">$95.000</div><div class="price-currency">ARS</div></div>
    </div>
    <p class="price-section-title">👁 Views</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$2.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">100.000</div><div class="price-amount">$10.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">1.000.000</div><div class="price-amount">$70.000</div><div class="price-currency">ARS</div></div>
    </div>
  </div>

  <!-- FACEBOOK -->

  <div class="tab-content" id="tab-fb">
    <p class="price-section-title">👥 Seguidores</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">500</div><div class="price-amount">$3.500</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">1.000</div><div class="price-amount">$6.800</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">2.500</div><div class="price-amount">$15.500</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">5.000</div><div class="price-amount">$28.000</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$52.000</div><div class="price-currency">ARS</div></div>
    </div>
    <p class="price-section-title">❤️ Likes</p>
    <div class="price-grid">
      <div class="price-card"><div class="price-qty">500</div><div class="price-amount">$1.700</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">1.000</div><div class="price-amount">$2.900</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">2.500</div><div class="price-amount">$6.800</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">5.000</div><div class="price-amount">$12.250</div><div class="price-currency">ARS</div></div>
      <div class="price-card"><div class="price-qty">10.000</div><div class="price-amount">$20.500</div><div class="price-currency">ARS</div></div>
    </div>
  </div>
</section>

<!-- COMBOS -->

<section id="combos">
  <p class="section-label">Packs especiales</p>
  <h2 class="section-title">Combos</h2>
  <div class="divider"></div>
  <p class="section-desc">Los mejores packs para escalar tu perfil. Más valor, menos precio.</p>
  <div class="combos-grid reveal">
    <div class="combo-card">
      <span class="combo-emoji">🔥</span>
      <div class="combo-badge">Emprendedor</div>
      <div class="combo-name">Combo Emprendedor</div>
      <ul class="combo-features">
        <li>2.500 Seguidores</li>
        <li>5.000 Likes</li>
        <li>50.000 Views</li>
      </ul>
      <div class="combo-price">$24.999</div>
      <a href="https://wa.me/549XXXXXXXXXX?text=Hola!%20Quiero%20el%20Combo%20Emprendedor" class="btn-combo">Comprar combo</a>
    </div>
    <div class="combo-card featured">
      <span class="combo-emoji">🚀</span>
      <div class="combo-badge">Más popular</div>
      <div class="combo-name">Combo Viral</div>
      <ul class="combo-features">
        <li>10.000 Seguidores</li>
        <li>10.000 Likes</li>
        <li>500.000 Views</li>
      </ul>
      <div class="combo-price">$74.999</div>
      <a href="https://wa.me/549XXXXXXXXXX?text=Hola!%20Quiero%20el%20Combo%20Viral" class="btn-combo">Comprar combo</a>
    </div>
    <div class="combo-card">
      <span class="combo-emoji">👑</span>
      <div class="combo-badge">Premium</div>
      <div class="combo-name">Combo Marca</div>
      <ul class="combo-features">
        <li>50.000 Seguidores</li>
        <li>50.000 Likes</li>
        <li>1.000.000 Views</li>
      </ul>
      <div class="combo-price">$299.999</div>
      <a href="https://wa.me/549XXXXXXXXXX?text=Hola!%20Quiero%20el%20Combo%20Marca" class="btn-combo">Comprar combo</a>
    </div>
  </div>
</section>

<!-- BENEFICIOS -->

<section id="beneficios">
  <p class="section-label">¿Por qué elegirnos?</p>
  <h2 class="section-title">Beneficios</h2>
  <div class="divider"></div>
  <p class="section-desc">Todo lo que necesitás para crecer con confianza y seguridad.</p>
  <div class="benefits-grid reveal">
    <div class="benefit-card">
      <span class="benefit-icon">⚡</span>
      <div class="benefit-title">Entrega Rápida</div>
      <div class="benefit-desc">Entre minutos y pocas horas. Sin esperas largas ni demoras inexplicables.</div>
    </div>
    <div class="benefit-card">
      <span class="benefit-icon">🔄</span>
      <div class="benefit-title">Garantía Refill</div>
      <div class="benefit-desc">Si hay bajas, reponemos sin costo. Tu inversión siempre está protegida.</div>
    </div>
    <div class="benefit-card">
      <span class="benefit-icon">🛡️</span>
      <div class="benefit-title">Métodos Seguros</div>
      <div class="benefit-desc">Nunca pedimos contraseñas. Crecimiento 100% seguro y sin riesgos para tu cuenta.</div>
    </div>
    <div class="benefit-card">
      <span class="benefit-icon">💬</span>
      <div class="benefit-title">Soporte Personalizado</div>
      <div class="benefit-desc">Atención por WhatsApp e Instagram. Siempre hay alguien para ayudarte.</div>
    </div>
    <div class="benefit-card">
      <span class="benefit-icon">🔒</span>
      <div class="benefit-title">Sin Contraseña</div>
      <div class="benefit-desc">Solo necesitamos el nombre de usuario. Tu privacidad es prioridad.</div>
    </div>
    <div class="benefit-card">
      <span class="benefit-icon">📈</span>
      <div class="benefit-title">Resultados Reales</div>
      <div class="benefit-desc">Crecimiento que se ve. Más autoridad, más alcance, más oportunidades.</div>
    </div>
  </div>
</section>

<!-- FAQ -->

<section id="faq">
  <p class="section-label">Dudas frecuentes</p>
  <h2 class="section-title">FAQ</h2>
  <div class="divider"></div>
  <p class="section-desc">Todo lo que necesitás saber antes de empezar.</p>
  <div class="faq-list reveal">
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">
        ¿Voy a perder seguidores después?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">Puede haber bajas mínimas que son completamente normales en la plataforma. Por eso todos nuestros servicios incluyen garantía de refill, reponemos sin costo adicional.</div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">
        ¿Cuánto tarda en llegar el pedido?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">La entrega es entre minutos y algunas horas dependiendo del volumen del pedido. En la mayoría de los casos comenzás a ver resultados en los primeros minutos.</div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">
        ¿Necesito darles mi contraseña?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">¡Nunca! Solo necesitamos el nombre de usuario de tu cuenta. Tu privacidad y seguridad son nuestra prioridad absoluta.</div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">
        ¿Mi cuenta puede ser baneada?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">Utilizamos métodos seguros y orgánicos que cumplen con las políticas de las plataformas. El riesgo es mínimo y trabajamos con total responsabilidad.</div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">
        ¿Cómo hago un pedido?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">Contactanos por WhatsApp o Instagram DM. Indicanos la red social, el servicio, la cantidad y el usuario de tu cuenta. Es así de simple.</div>
    </div>
    <div class="faq-item">
      <button class="faq-question" onclick="toggleFaq(this)">
        ¿Qué métodos de pago aceptan?
        <span class="faq-icon">+</span>
      </button>
      <div class="faq-answer">Aceptamos transferencia bancaria, Mercado Pago y otros métodos digitales. Consultanos por WhatsApp para más información.</div>
    </div>
  </div>
</section>

<!-- CONTACTO -->

<section id="contacto">
  <p class="section-label">Hablemos</p>
  <h2 class="section-title">Contacto</h2>
  <div class="divider"></div>
  <p class="section-desc">¿Listo para impulsar tu presencia digital? Escribinos ahora.</p>
  <div class="contact-card reveal">
    <div class="contact-glow"></div>
    <div class="contact-title">Hacé tu pedido</div>
    <div class="contact-desc">
      🚀 Impulsamos tu presencia digital<br>
      📈 Seguidores • Likes • Views<br>
      ⚡ Entrega rápida y segura<br>
      📩 Pedidos al DM o WhatsApp
    </div>
    <div class="contact-buttons">
      <a href="https://wa.me/549XXXXXXXXXX" class="btn-contact-wa">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.123.553 4.113 1.519 5.847L.057 23.495a.5.5 0 00.609.61l5.819-1.527A11.952 11.952 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.959 0-3.797-.5-5.4-1.377l-.387-.222-4.02 1.055 1.07-3.91-.245-.397A9.954 9.954 0 012 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z"/></svg>
        Escribir por WhatsApp
      </a>
      <a href="https://instagram.com/growth.vv" class="btn-contact-ig">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
        Instagram DM – @growth.vv
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->

<footer>
  <div class="footer-logo">GROWTH VV</div>
  <div class="footer-slogan">Convertimos perfiles en marcas · Growth for creators</div>
  <div class="footer-copy">© 2025 Growth VV. Todos los derechos reservados.</div>
</footer>

<script>
// Particles
(function() {
  const container = document.getElementById('particles');
  for (let i = 0; i < 30; i++) {
    const p = document.createElement('div');
    p.className = 'particle';
    const size = Math.random() * 4 + 1;
    p.style.cssText = `
      width:${size}px; height:${size}px;
      left:${Math.random()*100}%;
      animation-duration:${Math.random()*15+10}s;
      animation-delay:${Math.random()*15}s;
    `;
    container.appendChild(p);
  }
})();

// Tabs
function showTab(id) {
  document.querySelectorAll('.tab-content').forEach(t => t.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('tab-'+id).classList.add('active');
  event.target.classList.add('active');
}

// FAQ
function toggleFaq(btn) {
  const item = btn.parentElement;
  const isOpen = item.classList.contains('open');
  document.querySelectorAll('.faq-item').forEach(i => i.classList.remove('open'));
  if (!isOpen) item.classList.add('open');
}

// Scroll reveal
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));

// Mobile menu
function openMobileMenu() { document.getElementById('mobileMenu').classList.add('open'); }
function closeMobileMenu() { document.getElementById('mobileMenu').classList.remove('open'); }
</script>

</body>
</html>