<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>LCMS Groupement</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600;700;800&family=Inter:wght@400;500;600&display=swap" rel="stylesheet">
  <style>
    :root{
      --blue:#0b2f67;
      --blue2:#153f86;
      --yellow:#f6c21a;
      --red:#d91f26;
      --bg:#f4f7fb;
      --text:#1d2433;
      --muted:#6b7280;
      --card:#ffffff;
      --line:#d9e2ef;
      --shadow:0 18px 45px rgba(10,32,84,.12);
      --radius:24px;
    }
    *{box-sizing:border-box}
    html,body{margin:0;padding:0;background:linear-gradient(180deg,#ffffff 0%,#f7f9fd 100%);color:var(--text);font-family:Inter,system-ui,sans-serif}
    img{max-width:100%;display:block}
    a{text-decoration:none;color:inherit}
    .page{max-width:1440px;margin:0 auto;overflow:hidden}
    .hero{position:relative;min-height:520px;display:grid;grid-template-columns:1.1fr .95fr;gap:0;background:#fff}
    .hero::before{
      content:"";
      position:absolute;
      inset:auto -180px -180px auto;
      width:520px;height:520px;
      background:radial-gradient(circle at 30% 30%, rgba(217,31,38,.95), rgba(217,31,38,.95) 50%, rgba(246,194,26,.95) 51%, rgba(246,194,26,.95) 63%, rgba(11,47,103,.98) 64%, rgba(11,47,103,.98) 78%, transparent 79%);
      border-radius:50%;
      filter:blur(0.2px);
      opacity:.95;
    }
    .hero-left{
      padding:36px 32px 30px;
      background:linear-gradient(180deg,var(--blue2),var(--blue));
      color:#fff;
      display:flex;
      flex-direction:column;
      justify-content:space-between;
      min-height:520px;
    }
    .brand{display:flex;align-items:center;gap:16px}
    .brand-mark{
      width:80px;height:80px;border-radius:50%;
      background:linear-gradient(145deg,#fff, #edf3ff);
      display:grid;place-items:center;
      box-shadow:inset 0 0 0 8px rgba(255,255,255,.08)
    }
    .brand-mark span{
      width:48px;height:48px;border-radius:50%;
      border:9px solid var(--yellow);
      border-top-color:var(--red);
      border-left-color:transparent;
      border-right-color:transparent
    }
    .eyebrow{
      font-size:12px;letter-spacing:.16em;
      text-transform:uppercase;color:#dbe7ff
    }
    .hero h1{
      font-family:Montserrat,sans-serif;
      font-size:56px;line-height:1.02;
      margin:16px 0 12px;
      max-width:10ch
    }
    .hero p{
      font-size:18px;line-height:1.6;
      color:#eef3ff;max-width:52ch
    }
    .cta{display:flex;gap:14px;flex-wrap:wrap;margin-top:18px}
    .btn{
      padding:14px 22px;border-radius:14px;
      font-weight:700;font-family:Montserrat,sans-serif
    }
    .btn.primary{background:var(--yellow);color:#0c2c63}
    .btn.secondary{border:2px solid rgba(255,255,255,.65);color:#fff}
    .partners{display:grid;gap:14px;margin-top:28px}
    .partner-card{
      background:#fff;color:#123;
      display:flex;align-items:center;gap:14px;
      padding:14px 16px;border-radius:18px;box-shadow:var(--shadow);
      min-height:84px
    }
    .partner-badge{
      width:52px;height:52px;border-radius:12px;
      background:linear-gradient(145deg,#eef4ff,#fff);
      display:grid;place-items:center;color:var(--blue);font-weight:800
    }
    .hero-right{
      padding:26px 26px 20px;
      background:#fff;
      display:grid;
      grid-template-rows:auto 1fr
    }
    .intro{
      background:#fff;border:1px solid var(--line);
      border-radius:22px;padding:24px;box-shadow:var(--shadow);
      margin-bottom:18px
    }
    .intro h2{
      margin:0 0 10px;
      font-family:Montserrat,sans-serif;
      color:var(--blue);font-size:24px
    }
    .intro p{margin:0;color:#24314d;line-height:1.65}
    .gallery{
      display:grid;
      grid-template-columns:1.2fr .8fr .8fr;
      grid-template-rows:210px 210px;
      gap:10px
    }
    .g1{
      grid-column:1/4;grid-row:1/2;
      border-radius:22px;
      background:linear-gradient(135deg,#c61d23,#ff4b4b);
      position:relative;overflow:hidden
    }
    .g2,.g3,.g4,.g5,.g6{
      border-radius:18px;background:#e9eef7;position:relative;overflow:hidden
    }
    .g2{background:linear-gradient(135deg,#8fd18a,#2f7d32)}
    .g3{background:linear-gradient(135deg,#f1e8d0,#d6c4a2)}
    .g4{background:linear-gradient(135deg,#d8ecff,#8bc7ff)}
    .g5{background:linear-gradient(135deg,#f1b08e,#ff7d4e)}
    .g6{background:linear-gradient(135deg,#eef0f4,#bcc7d8)}
    .glabel{
      position:absolute;left:14px;bottom:14px;
      background:rgba(255,255,255,.88);
      padding:8px 12px;border-radius:999px;
      font-weight:700;color:var(--blue)
    }
    .content{
      display:grid;
      grid-template-columns:1fr 1fr 1fr 1fr;
      gap:18px;
      padding:22px 24px 34px;
      background:#fff;
      align-items:stretch
    }
    .feature{
      background:#f9fbff;border:1px solid var(--line);
      border-radius:18px;padding:18px;box-shadow:0 8px 28px rgba(10,32,84,.06)
    }
    .feature .icon{
      width:48px;height:48px;border-radius:14px;
      background:var(--blue);margin-bottom:12px
    }
    .feature h3{
      margin:0 0 6px;
      font-family:Montserrat,sans-serif;
      color:var(--blue);font-size:18px
    }
    .feature p{margin:0;color:var(--muted);line-height:1.6;font-size:14px}
    .about{
      display:grid;
      grid-template-columns:1.1fr .9fr;
      gap:18px;
      padding:0 24px 24px;
      background:#fff
    }
    .panel{
      background:#f9fbff;border:1px solid var(--line);
      border-radius:22px;padding:24px;box-shadow:0 8px 28px rgba(10,32,84,.06)
    }
    .panel h2{margin:0 0 12px;font-family:Montserrat,sans-serif;color:var(--blue)}
    .list{margin:0;padding-left:18px;line-height:1.9}
    .contact-band{
      background:linear-gradient(180deg,var(--blue),#07254e);
      color:#fff;padding:28px 24px;
      display:grid;
      grid-template-columns:1.1fr .9fr;
      gap:18px;
      position:relative;overflow:hidden
    }
    .contact-band::after{
      content:"";
      position:absolute;right:-140px;bottom:-140px;
      width:460px;height:460px;border-radius:50%;
      background:conic-gradient(from 20deg,var(--yellow) 0 34%, var(--red) 34% 64%, transparent 64% 100%);
      opacity:.95
    }
    .contact-box,.legal{position:relative;z-index:1}
    .contact-title{
      font-family:Montserrat,sans-serif;
      font-size:22px;margin:0 0 8px;color:var(--yellow)
    }
    .contact-item{margin:8px 0;color:#eef3ff}
    .footer-note{font-size:14px;color:#d8e2fb;line-height:1.7}
    @media (max-width: 1100px){
      .hero,.about,.contact-band{grid-template-columns:1fr}
      .content{grid-template-columns:1fr 1fr}
      .hero h1{font-size:44px}
    }
    @media (max-width: 720px){
      .hero-left,.hero-right,.content,.about,.contact-band{padding-left:16px;padding-right:16px}
      .hero{grid-template-columns:1fr}
      .content{grid-template-columns:1fr}
      .gallery{grid-template-columns:1fr 1fr;grid-template-rows:180px 180px 180px}
      .g1{grid-column:1/3}
      .hero h1{font-size:38px}
    }
  </style>
</head>
<body>
  <main class="page">
    <section class="hero">
      <div class="hero-left">
        <div>
          <div class="brand">
            <div class="brand-mark"><span></span></div>
            <div>
              <div class="eyebrow">LCMS Groupement</div>
              <div style="font-weight:700;font-family:Montserrat,sans-serif">La Congolaise des Mines et des Services</div>
            </div>
          </div>
          <h1>Un groupement solide, des expertises complémentaires.</h1>
          <p>Solutions industrielles, logistiques et techniques pour vos projets, avec une coordination professionnelle et des prestations adaptées aux exigences du terrain.</p>
          <div class="cta">
            <a class="btn primary" href="#contact">Nous contacter</a>
            <a class="btn secondary" href="#services">Nos services</a>
          </div>
        </div>
        <div class="partners">
          <div class="partner-card"><div class="partner-badge">LCMS</div><div><strong>La Congolaise des Mines et des Services</strong><br><span style="color:#5d6a85">Coordination du groupement</span></div></div>
          <div class="partner-card"><div class="partner-badge">O</div><div><strong>OUMARCO</strong><br><span style="color:#5d6a85">Partenaire opérationnel</span></div></div>
          <div class="partner-card"><div class="partner-badge">T</div><div><strong>TRANEX</strong><br><span style="color:#5d6a85">Transport et express</span></div></div>
          <div class="partner-card"><div class="partner-badge">PS</div><div><strong>PRECIEUX SERVICES</strong><br><span style="color:#5d6a85">Support et services</span></div></div>
        </div>
      </div>
      <div class="hero-right">
        <div class="intro">
          <h2>Présentation du groupement</h2>
          <p>Constitué autour de la société La Congolaise des Mines et des Services, le groupement unit des compétences complémentaires pour offrir des prestations coordonnées, fiables et adaptées aux besoins industriels et techniques.</p>
        </div>
        <div class="gallery">
          <div class="g1"><div class="glabel">Équipe terrain</div></div>
          <div class="g2"><div class="glabel">Intervention</div></div>
          <div class="g3"><div class="glabel">Sécurité</div></div>
          <div class="g4"><div class="glabel">Coordination</div></div>
          <div class="g5"><div class="glabel">Suivi chantier</div></div>
          <div class="g6"><div class="glabel">Accompagnement</div></div>
        </div>
      </div>
    </section>

    <section id="services" class="content">
      <article class="feature"><div class="icon"></div><h3>Assistance administrative</h3><p>Gestion documentaire, suivi de dossiers et coordination des échanges avec les partenaires.</p></article>
      <article class="feature"><div class="icon"></div><h3>Assistance technique</h3><p>Support opérationnel, supervision des travaux et adaptation aux contraintes du terrain.</p></article>
      <article class="feature"><div class="icon"></div><h3>Assistance financière</h3><p>Organisation, contrôle et alignement des ressources pour sécuriser l’exécution des projets.</p></article>
      <article class="feature"><div class="icon"></div><h3>Logistique & opérations</h3><p>Mutualisation des moyens, transport, approvisionnement et continuité de service.</p></article>
    </section>

    <section class="about">
      <div class="panel">
        <h2>À propos</h2>
        <p>Le groupement présente une vision commune de développement et d’assistance mutuelle pour renforcer les capacités opérationnelles et la mise en commun des expertises.</p>
        <ul class="list">
          <li>Un groupement solide de partenaires complémentaires.</li>
          <li>Prestations coordonnées, fiables et adaptées.</li>
          <li>Respect des engagements professionnels.</li>
        </ul>
      </div>
      <div class="panel">
        <h2>Valeurs</h2>
        <ul class="list">
          <li>Intégrité.</li>
          <li>Qualité.</li>
          <li>Professionnalisme.</li>
          <li>Esprit de partenariat.</li>
        </ul>
      </div>
    </section>

    <section id="contact" class="contact-band">
      <div class="contact-box">
        <h3 class="contact-title">Nous contacter</h3>
        <div class="contact-item">Téléphone: +242 06 467 37 34 / 05 503 82 22</div>
        <div class="contact-item">Email: lacongolaisedesminesetdesservices@gmail.com</div>
        <div class="contact-item">Siège social: 11 Avenue Daniel EVONGO - Arr-2-Soulouka-Nkay</div>
      </div>
      <div class="legal">
        <h3 class="contact-title">Références</h3>
        <div class="footer-note">Société à Responsabilité Limitée au capital de 1 500 000 FCFA</div>
        <div class="footer-note">RCCM : CG/NKY/01/2019-B12-00036</div>
        <div class="footer-note">NIU : P23000001542817</div>
      </div>
    </section>
  </main>
</body>
</html>
