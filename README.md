# techpulse
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>TechPulse — El futuro digital, explicado</title>
  <meta name="description" content="Reviews honestas, tutoriales y noticias de tecnología en español." />
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet" />
  <style>
    :root{--bg:#07090f;--surface:#0e1118;--border:#1e2332;--accent:#00e5ff;--accent2:#ff3d71;--accent3:#7c4dff;--text:#e8eaf2;--muted:#7a7f96;--card-bg:#111520;--fh:'Syne',sans-serif;--fb:'DM Sans',sans-serif}
    *,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
    html{scroll-behavior:smooth}
    body{background:var(--bg);color:var(--text);font-family:var(--fb);font-size:16px;line-height:1.7;overflow-x:hidden}
    a{color:inherit;text-decoration:none}
    body::before{content:'';position:fixed;inset:0;background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='1'/%3E%3C/svg%3E");opacity:.03;pointer-events:none;z-index:0}

    /* NAVBAR */
    header{position:sticky;top:0;z-index:100;background:rgba(7,9,15,.88);backdrop-filter:blur(16px);border-bottom:1px solid var(--border)}
    nav{max-width:1280px;margin:0 auto;padding:0 2rem;display:flex;align-items:center;justify-content:space-between;height:62px}
    .logo{font-family:var(--fh);font-size:1.4rem;font-weight:800;display:flex;align-items:center;gap:8px;letter-spacing:-.5px}
    .logo span{color:var(--accent)}
    .logo-dot{width:8px;height:8px;border-radius:50%;background:var(--accent);animation:pulse 2s infinite}
    @keyframes pulse{0%,100%{box-shadow:0 0 0 0 rgba(0,229,255,.5)}50%{box-shadow:0 0 0 6px rgba(0,229,255,0)}}
    .nav-links{display:flex;gap:1.8rem;list-style:none;font-size:.88rem;font-weight:500;color:var(--muted)}
    .nav-links a:hover{color:var(--accent);transition:color .2s}
    .nav-btn{background:var(--accent);color:var(--bg);font-weight:700;font-size:.82rem;padding:.42rem 1rem;border-radius:6px;transition:opacity .2s}
    .nav-btn:hover{opacity:.85}

    /* HERO */
    .hero{max-width:1280px;margin:0 auto;padding:5rem 2rem 4rem;display:grid;grid-template-columns:1fr 1fr;gap:3rem;align-items:center}
    .hero-tag{display:inline-flex;align-items:center;gap:6px;font-size:.72rem;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--accent);border:1px solid rgba(0,229,255,.3);padding:.28rem .8rem;border-radius:99px;margin-bottom:1.2rem}
    .hero h1{font-family:var(--fh);font-size:clamp(2.2rem,4.5vw,3.5rem);font-weight:800;line-height:1.1;letter-spacing:-1.5px;margin-bottom:1.2rem}
    .hero h1 em{font-style:normal;color:var(--accent)}
    .hero p{color:var(--muted);font-size:1rem;max-width:400px;margin-bottom:1.8rem}
    .hero-btns{display:flex;gap:1rem;flex-wrap:wrap}
    .btn-p{background:var(--accent);color:var(--bg);font-weight:700;padding:.72rem 1.5rem;border-radius:8px;font-size:.92rem;transition:transform .2s,box-shadow .2s}
    .btn-p:hover{transform:translateY(-2px);box-shadow:0 8px 24px rgba(0,229,255,.25)}
    .btn-g{border:1px solid var(--border);color:var(--text);font-weight:500;padding:.72rem 1.5rem;border-radius:8px;font-size:.92rem;transition:border-color .2s,color .2s}
    .btn-g:hover{border-color:var(--accent);color:var(--accent)}
    .hero-visual{position:relative;height:360px;display:flex;align-items:center;justify-content:center}
    .hc{position:absolute;border-radius:50%;border:1px solid var(--border);animation:spin linear infinite}
    .hc:nth-child(1){width:300px;height:300px;animation-duration:30s}
    .hc:nth-child(2){width:200px;height:200px;animation-duration:20s;animation-direction:reverse;border-color:rgba(0,229,255,.15)}
    .hc:nth-child(3){width:110px;height:110px;animation-duration:12s;border-color:rgba(255,61,113,.2)}
    @keyframes spin{to{transform:rotate(360deg)}}
    .hi{position:relative;font-size:3.2rem;z-index:1;filter:drop-shadow(0 0 28px rgba(0,229,255,.4))}
    .dot-c{position:absolute;width:7px;height:7px;border-radius:50%;background:var(--accent);top:-3.5px;left:50%;transform:translateX(-50%)}
    .dot-c.r{background:var(--accent2);top:auto;bottom:-3.5px}

    /* TICKER */
    .ticker-wrap{border-top:1px solid var(--border);border-bottom:1px solid var(--border);overflow:hidden;background:var(--surface);padding:.55rem 0}
    .ticker{display:flex;gap:3rem;white-space:nowrap;animation:tick 32s linear infinite}
    .ticker span{font-size:.78rem;font-weight:500;color:var(--muted)}
    .ticker span::before{content:'⬡ ';color:var(--accent)}
    @keyframes tick{from{transform:translateX(0)}to{transform:translateX(-50%)}}

    /* LAYOUT */
    .wrap{max-width:1280px;margin:0 auto;padding:3.5rem 2rem}
    .sec-label{font-size:.72rem;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--accent);margin-bottom:.4rem}
    .sec-title{font-family:var(--fh);font-size:clamp(1.5rem,2.5vw,2rem);font-weight:800;letter-spacing:-.5px;margin-bottom:1.8rem}

    /* CARDS */
    .card{background:var(--card-bg);border:1px solid var(--border);border-radius:14px;overflow:hidden;transition:transform .25s,border-color .25s,box-shadow .25s;cursor:pointer}
    .card:hover{transform:translateY(-4px);border-color:rgba(0,229,255,.25);box-shadow:0 12px 36px rgba(0,0,0,.45)}
    .thumb{width:100%;aspect-ratio:16/9;display:flex;align-items:center;justify-content:center;font-size:3rem;background:linear-gradient(135deg,#0e1118,#1a2035)}
    .cbody{padding:1.25rem}
    .ctag{font-size:.68rem;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--accent);margin-bottom:.5rem}
    .ctag.r{color:var(--accent2)}
    .ctitle{font-family:var(--fh);font-size:1rem;font-weight:700;line-height:1.3;margin-bottom:.6rem;letter-spacing:-.2px}
    .ctitle.big{font-size:1.4rem}
    .cexc{font-size:.85rem;color:var(--muted);margin-bottom:.9rem;display:-webkit-box;-webkit-line-clamp:3;-webkit-box-orient:vertical;overflow:hidden}
    .cmeta{display:flex;align-items:center;justify-content:space-between;font-size:.76rem;color:var(--muted)}
    .author{display:flex;align-items:center;gap:.4rem}
    .av{width:22px;height:22px;border-radius:50%;background:linear-gradient(135deg,var(--accent),var(--accent2));display:flex;align-items:center;justify-content:center;font-size:.55rem;font-weight:700;color:var(--bg)}
    .rt{background:var(--border);padding:.18rem .5rem;border-radius:4px}

    /* GRIDS */
    .feat{display:grid;grid-template-columns:1.35fr 1fr;gap:1.4rem;margin-bottom:1.4rem}
    .g3{display:grid;grid-template-columns:repeat(3,1fr);gap:1.4rem}
    .g2{display:grid;grid-template-columns:repeat(2,1fr);gap:1.4rem}

    /* SIDEBAR */
    .two-col{display:grid;grid-template-columns:1fr 300px;gap:2rem;align-items:start}
    .sidebar>*+*{margin-top:1.4rem}
    .widget{background:var(--card-bg);border:1px solid var(--border);border-radius:14px;padding:1.3rem}
    .wtitle{font-family:var(--fh);font-size:.95rem;font-weight:700;margin-bottom:.9rem;padding-bottom:.55rem;border-bottom:1px solid var(--border)}
    .nl-form{display:flex;flex-direction:column;gap:.65rem}
    .nl-form input{background:var(--bg);border:1px solid var(--border);border-radius:7px;padding:.6rem .9rem;color:var(--text);font-family:var(--fb);font-size:.88rem;outline:none;transition:border-color .2s}
    .nl-form input:focus{border-color:var(--accent)}
    .nl-form button{background:var(--accent);color:var(--bg);font-weight:700;font-size:.88rem;padding:.62rem;border-radius:7px;border:none;cursor:pointer;font-family:var(--fb);transition:opacity .2s}
    .nl-form button:hover{opacity:.85}
    .tr-list{display:flex;flex-direction:column;gap:.85rem}
    .tr-item{display:flex;gap:.75rem;align-items:flex-start;cursor:pointer}
    .tr-item:hover .tr-title{color:var(--accent);transition:color .2s}
    .tr-num{font-family:var(--fh);font-size:1.3rem;font-weight:800;color:var(--border);line-height:1;min-width:26px}
    .tr-title{font-size:.85rem;font-weight:500;line-height:1.4}
    .tr-sub{font-size:.73rem;color:var(--muted)}

    /* ADS */
    .ad{background:var(--surface);border:1px dashed var(--border);border-radius:11px;display:flex;flex-direction:column;align-items:center;justify-content:center;padding:1.3rem;gap:.3rem;min-height:130px;color:var(--muted);font-size:.78rem;text-align:center}
    .ad .ai{font-size:1.5rem;opacity:.35}
    .ad p{opacity:.45}
    .ad-lbl{font-size:.62rem;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;opacity:.28}

    /* REVIEWS */
    .score{display:inline-flex;align-items:center;gap:4px;background:var(--accent2);color:#fff;font-weight:800;font-size:.82rem;padding:.22rem .6rem;border-radius:5px;margin-bottom:.45rem}
    .stars{color:#ffd700;font-size:.82rem;letter-spacing:1px}

    /* TUTORIALS */
    .tut{background:var(--card-bg);border:1px solid var(--border);border-radius:14px;padding:1.25rem;display:flex;gap:.9rem;align-items:flex-start;transition:transform .2s,border-color .2s;cursor:pointer}
    .tut:hover{transform:translateY(-3px);border-color:rgba(0,229,255,.2)}
    .ti{font-size:1.8rem;min-width:44px;height:44px;display:flex;align-items:center;justify-content:center;background:rgba(0,229,255,.07);border-radius:9px}
    .tt{font-weight:700;margin-bottom:.28rem;font-size:.92rem}
    .tm{font-size:.76rem;color:var(--muted)}
    .lv{font-size:.66rem;font-weight:700;padding:.12rem .45rem;border-radius:4px;margin-left:.4rem}
    .lv.b{background:rgba(0,229,255,.14);color:var(--accent)}
    .lv.a{background:rgba(255,61,113,.14);color:var(--accent2)}
    .lv.m{background:rgba(124,77,255,.14);color:var(--accent3)}

    /* ARTICLE OVERLAY */
    #article-overlay{display:none;position:fixed;inset:0;z-index:200;background:rgba(7,9,15,.97);overflow-y:auto;padding:2rem}
    #article-overlay.open{display:block}
    .article-inner{max-width:740px;margin:0 auto}
    .art-back{display:inline-flex;align-items:center;gap:.5rem;color:var(--muted);font-size:.88rem;margin-bottom:2rem;cursor:pointer;transition:color .2s}
    .art-back:hover{color:var(--accent)}
    .art-tag{font-size:.7rem;font-weight:700;letter-spacing:1.5px;text-transform:uppercase;color:var(--accent);margin-bottom:.8rem}
    .art-title{font-family:var(--fh);font-size:clamp(1.8rem,4vw,2.8rem);font-weight:800;line-height:1.1;letter-spacing:-1px;margin-bottom:1.2rem}
    .art-meta{display:flex;align-items:center;gap:1rem;margin-bottom:2rem;padding-bottom:1.5rem;border-bottom:1px solid var(--border);font-size:.82rem;color:var(--muted)}
    .art-content{font-size:1.02rem;line-height:1.85;color:#c8cad8}
    .art-content h2{font-family:var(--fh);font-size:1.4rem;font-weight:700;color:var(--text);margin:2rem 0 .8rem}
    .art-content h3{font-family:var(--fh);font-size:1.15rem;font-weight:700;color:var(--text);margin:1.5rem 0 .6rem}
    .art-content p{margin-bottom:1.2rem}
    .art-content ul,.art-content ol{margin:0 0 1.2rem 1.5rem}
    .art-content li{margin-bottom:.4rem}
    .art-content strong{color:var(--text);font-weight:600}
    .art-content blockquote{border-left:3px solid var(--accent);padding:.5rem 1rem;margin:1.5rem 0;color:var(--muted);font-style:italic}
    .art-content code{background:var(--surface);border:1px solid var(--border);border-radius:5px;padding:.15rem .45rem;font-size:.88rem;font-family:monospace;color:var(--accent)}
    .art-content pre{background:var(--surface);border:1px solid var(--border);border-radius:8px;padding:1rem;overflow-x:auto;margin-bottom:1.2rem}
    .art-content pre code{background:none;border:none;padding:0}
    .art-ad{margin:2rem 0}

    /* LOADING */
    .spinner{display:inline-block;width:18px;height:18px;border:2px solid var(--border);border-top-color:var(--accent);border-radius:50%;animation:spin .7s linear infinite}
    .loading-state{display:flex;align-items:center;gap:.7rem;color:var(--muted);font-size:.88rem}

    /* GENERATING OVERLAY */
    #gen-overlay{position:fixed;inset:0;z-index:300;background:var(--bg);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:1.8rem}
    .gen-logo{font-family:var(--fh);font-size:2rem;font-weight:800}
    .gen-logo span{color:var(--accent)}
    .gen-bar-wrap{width:320px;height:4px;background:var(--border);border-radius:2px;overflow:hidden}
    .gen-bar{height:100%;background:linear-gradient(90deg,var(--accent),var(--accent2));border-radius:2px;width:0%;transition:width .4s ease}
    .gen-status{color:var(--muted);font-size:.9rem;text-align:center;max-width:340px}
    .gen-count{font-family:var(--fh);font-size:3.5rem;font-weight:800;color:var(--accent);line-height:1}

    /* CATS */
    .cats{display:flex;gap:.8rem;flex-wrap:wrap;margin-bottom:2rem}
    .cat{display:flex;align-items:center;gap:.45rem;padding:.45rem 1rem;border:1px solid var(--border);border-radius:99px;font-size:.82rem;font-weight:500;color:var(--muted);cursor:pointer;transition:all .2s}
    .cat:hover,.cat.on{border-color:var(--accent);color:var(--accent);background:rgba(0,229,255,.06)}

    /* FOOTER */
    footer{border-top:1px solid var(--border);margin-top:3rem;padding:2.5rem 2rem;background:var(--surface)}
    .fi{max-width:1280px;margin:0 auto;display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:2.5rem}
    .fb p{color:var(--muted);font-size:.85rem;margin-top:.7rem;max-width:250px}
    .fc h4{font-family:var(--fh);font-weight:700;font-size:.9rem;margin-bottom:.9rem}
    .fc ul{list-style:none;display:flex;flex-direction:column;gap:.5rem}
    .fc li{font-size:.85rem;color:var(--muted);cursor:pointer;transition:color .2s}
    .fc li:hover{color:var(--accent)}
    .fb2{max-width:1280px;margin:1.8rem auto 0;padding-top:1.4rem;border-top:1px solid var(--border);display:flex;justify-content:space-between;font-size:.78rem;color:var(--muted)}

    @media(max-width:900px){
      .hero{grid-template-columns:1fr}.hero-visual{display:none}
      .feat{grid-template-columns:1fr}.g3{grid-template-columns:1fr 1fr}
      .two-col{grid-template-columns:1fr}.fi{grid-template-columns:1fr 1fr}
      .nav-links{display:none}
    }
    @media(max-width:560px){.g3{grid-template-columns:1fr}.g2{grid-template-columns:1fr}.fi{grid-template-columns:1fr}}
  </style>
</head>
<body>

<!-- GENERATING OVERLAY -->
<div id="gen-overlay">
  <div class="gen-logo">Tech<span>Pulse</span></div>
  <div class="gen-count" id="gen-count">0/20</div>
  <div class="gen-bar-wrap"><div class="gen-bar" id="gen-bar"></div></div>
  <div class="gen-status" id="gen-status">Generando 20 artículos con IA... ☕ Esto tarda ~2 minutos</div>
</div>

<!-- ARTICLE OVERLAY -->
<div id="article-overlay">
  <div class="article-inner">
    <div class="art-back" onclick="closeArticle()">← Volver al blog</div>
    <div class="art-tag" id="ao-tag"></div>
    <div class="art-title" id="ao-title"></div>
    <div class="art-meta" id="ao-meta"></div>
    <div class="ad art-ad"><div class="ai">📢</div><div class="ad-lbl">Anuncio</div><p>Google AdSense — 728×90</p></div>
    <div class="art-content" id="ao-content"></div>
    <div class="ad art-ad" style="margin-top:2.5rem"><div class="ai">📢</div><div class="ad-lbl">Anuncio</div><p>Google AdSense — 300×250</p></div>
  </div>
</div>

<!-- NAVBAR -->
<header>
  <nav>
    <div class="logo"><div class="logo-dot"></div>Tech<span>Pulse</span></div>
    <ul class="nav-links">
      <li><a href="#noticias">Noticias</a></li>
      <li><a href="#reviews">Reviews</a></li>
      <li><a href="#ia">IA & Futuro</a></li>
      <li><a href="#tutoriales">Tutoriales</a></li>
    </ul>
    <a href="#newsletter" class="nav-btn">Newsletter</a>
  </nav>
</header>

<!-- HERO -->
<section>
  <div class="hero">
    <div>
      <div class="hero-tag">✦ Blog de tecnología en español</div>
      <h1>El <em>futuro</em> digital,<br/>explicado para ti</h1>
      <p>Reviews honestas, tutoriales paso a paso y las últimas noticias del mundo tech. Sin tecnicismos innecesarios.</p>
      <div class="hero-btns">
        <a href="#noticias" class="btn-p">Explorar artículos</a>
        <a href="#reviews" class="btn-g">Ver reviews →</a>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hc"><div class="dot-c"></div><div class="dot-c r"></div></div>
      <div class="hc"></div><div class="hc"></div>
      <div class="hi">⚡</div>
    </div>
  </div>
</section>

<!-- TICKER -->
<div class="ticker-wrap">
  <div class="ticker">
    <span>Apple lanza iOS 20 con IA nativa</span><span>Google Gemini Ultra supera a GPT-5</span>
    <span>Samsung Galaxy S26 filtrado</span><span>NVIDIA presenta RTX 6090</span>
    <span>OpenAI anuncia nuevos modelos</span><span>Meta estrena gafas AR</span><span>Tesla FSD llega a Europa</span>
    <span>Apple lanza iOS 20 con IA nativa</span><span>Google Gemini Ultra supera a GPT-5</span>
    <span>Samsung Galaxy S26 filtrado</span><span>NVIDIA presenta RTX 6090</span>
    <span>OpenAI anuncia nuevos modelos</span><span>Meta estrena gafas AR</span><span>Tesla FSD llega a Europa</span>
  </div>
</div>

<!-- NOTICIAS -->
<div class="wrap" id="noticias">
  <div class="sec-label">Lo más reciente</div>
  <div class="sec-title">Artículos destacados</div>
  <div class="cats">
    <div class="cat on" data-cat="all">🔥 Todo</div>
    <div class="cat" data-cat="ia">🤖 IA</div>
    <div class="cat" data-cat="moviles">📱 Móviles</div>
    <div class="cat" data-cat="portatiles">💻 Portátiles</div>
    <div class="cat" data-cat="gaming">🎮 Gaming</div>
    <div class="cat" data-cat="seguridad">🔒 Seguridad</div>
  </div>
  <div class="two-col">
    <div id="main-articles"><div class="loading-state"><div class="spinner"></div> Generando artículos...</div></div>
    <aside class="sidebar">
      <div class="ad"><div class="ai">📢</div><div class="ad-lbl">Anuncio</div><p>Google AdSense 300×250</p></div>
      <div class="widget" id="newsletter">
        <div class="wtitle">📬 Newsletter semanal</div>
        <p style="font-size:.83rem;color:var(--muted);margin-bottom:.9rem">Recibe los mejores artículos tech cada lunes.</p>
        <div class="nl-form">
          <input type="email" placeholder="tu@email.com" />
          <button>Suscribirme gratis →</button>
        </div>
      </div>
      <div class="widget">
        <div class="wtitle">🔥 Trending</div>
        <div class="tr-list" id="trending-list"><div class="loading-state"><div class="spinner"></div></div></div>
      </div>
      <div class="ad"><div class="ai">📢</div><div class="ad-lbl">Anuncio</div><p>Google AdSense 300×600</p></div>
    </aside>
  </div>
</div>

<!-- REVIEWS -->
<div class="wrap" id="reviews" style="padding-top:0">
  <div class="sec-label">Análisis en profundidad</div>
  <div class="sec-title">Reviews & Comparativas</div>
  <div class="g3" id="reviews-grid"><div class="loading-state"><div class="spinner"></div> Generando reviews...</div></div>
</div>

<!-- AD BANNER -->
<div style="max-width:1280px;margin:0 auto;padding:0 2rem 2rem">
  <div class="ad" style="min-height:90px;flex-direction:row;gap:1rem">
    <div class="ai">📢</div><div><div class="ad-lbl">Anuncio</div><p>Google AdSense — Banner 728×90</p></div>
  </div>
</div>

<!-- IA -->
<div class="wrap" id="ia" style="padding-top:0">
  <div class="sec-label">El mañana, hoy</div>
  <div class="sec-title">IA & Futuro tecnológico</div>
  <div class="g2" id="ia-grid"><div class="loading-state"><div class="spinner"></div></div></div>
</div>

<!-- TUTORIALES -->
<div class="wrap" id="tutoriales" style="padding-top:0">
  <div class="sec-label">Aprende a tu ritmo</div>
  <div class="sec-title">Tutoriales paso a paso</div>
  <div style="display:flex;flex-direction:column;gap:1rem" id="tut-list"><div class="loading-state"><div class="spinner"></div></div></div>
</div>

<!-- FOOTER -->
<footer>
  <div class="fi">
    <div class="fb">
      <div class="logo"><div class="logo-dot"></div>Tech<span>Pulse</span></div>
      <p>El blog de tecnología en español más honesto. Reviews sin patrocinios ocultos, tutoriales claros y noticias verificadas.</p>
    </div>
    <div class="fc"><h4>Secciones</h4><ul><li>Noticias</li><li>Reviews</li><li>Tutoriales</li><li>IA & Futuro</li><li>Gaming</li></ul></div>
    <div class="fc"><h4>Categorías</h4><ul><li>Smartphones</li><li>Portátiles</li><li>Gaming</li><li>Seguridad</li><li>Cloud</li></ul></div>
    <div class="fc"><h4>Legal</h4><ul><li>Política de privacidad</li><li>Política de cookies</li><li>Aviso legal</li><li>Contacto</li><li>Sobre nosotros</li></ul></div>
  </div>
  <div class="fb2">
    <span>© 2025 TechPulse. Todos los derechos reservados.</span>
    <span>Hecho con ❤️ para la comunidad tech hispanohablante</span>
  </div>
</footer>

<script>
const ARTICLES = [
  {id:1,type:'noticia',cat:'ia',icon:'🤖',tag:'Inteligencia Artificial',title:'GPT-5 vs Gemini Ultra: El duelo definitivo de las IAs en 2025',author:'Alejandro López',date:'18 may 2025',read:'9 min',featured:true,
   prompt:'Escribe un artículo de blog en español, extenso y bien estructurado (mínimo 800 palabras) titulado "GPT-5 vs Gemini Ultra: El duelo definitivo de las IAs en 2025". Incluye: introducción enganchante, comparativa en rendimiento general, escritura creativa, código, razonamiento lógico, precios y planes, velocidad de respuesta, privacidad, conclusión con recomendación final. Usa subtítulos H2 y H3, listas y negritas. Tono cercano y divulgativo. Formatea con HTML usando <h2>, <h3>, <p>, <ul>, <li>, <strong>, <blockquote>. Añade al menos una cita destacada. No incluyas DOCTYPE ni body, solo el contenido del artículo.'},
  {id:2,type:'noticia',cat:'moviles',icon:'📱',tag:'Móviles',title:'Samsung Galaxy S26 Ultra: todo lo que sabemos hasta ahora',author:'María Ruiz',date:'17 may 2025',read:'5 min',
   prompt:'Escribe un artículo de blog en español (mínimo 700 palabras) sobre las filtraciones del Samsung Galaxy S26 Ultra. Cubre: diseño esperado, cámara (rumores de 200MP+), procesador, batería, S Pen, fecha de lanzamiento estimada, precio aproximado. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:3,type:'noticia',cat:'ia',icon:'🧠',tag:'IA & Futuro',title:'Los agentes de IA autónomos están cambiando el trabajo para siempre',author:'Carlos Reyes',date:'16 may 2025',read:'7 min',
   prompt:'Escribe un artículo de blog en español (mínimo 750 palabras) sobre cómo los agentes de IA autónomos están transformando el mercado laboral. Incluye: qué son los agentes IA, sectores más afectados, casos de uso reales, debate sobre sustitución vs. creación de empleos, habilidades más valiosas en el futuro. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>, <blockquote>. Tono reflexivo y periodístico. No incluyas DOCTYPE ni body.'},
  {id:4,type:'noticia',cat:'gaming',icon:'🎮',tag:'Gaming',title:'PlayStation 6: fecha, precio y especificaciones filtradas',author:'Javier Mora',date:'15 may 2025',read:'6 min',
   prompt:'Escribe un artículo de blog en español (mínimo 700 palabras) sobre las filtraciones de PlayStation 6. Cubre: CPU/GPU esperados, RAM, SSD, retrocompatibilidad, mando DualSense 2, precio estimado, fecha de lanzamiento, comparación con Xbox Next. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. Tono entusiasta para gamers. No incluyas DOCTYPE ni body.'},
  {id:5,type:'noticia',cat:'portatiles',icon:'💻',tag:'Portátiles',title:'MacBook Air M4: autonomía de 22 horas y un 40% más rápido',author:'Laura Pérez',date:'14 may 2025',read:'6 min',
   prompt:'Escribe un artículo de blog en español (mínimo 700 palabras) sobre el MacBook Air M4. Incluye: novedades del chip M4, mejoras de rendimiento frente a M3, autonomía de batería, diseño, opciones, precio, para quién es ideal y para quién no. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:6,type:'noticia',cat:'seguridad',icon:'🔒',tag:'Seguridad',title:'El mayor hackeo de 2025: 2.000 millones de contraseñas expuestas',author:'Alejandro López',date:'13 may 2025',read:'5 min',
   prompt:'Escribe un artículo de blog en español (mínimo 650 palabras) sobre una brecha de seguridad masiva (ficticia pero verosímil) de 2025 que expone 2.000 millones de contraseñas. Cubre: cómo ocurrió, qué datos están comprometidos, cómo saber si estás afectado, qué hacer inmediatamente, cómo protegerte en el futuro. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>, <blockquote>. Tono urgente y útil. No incluyas DOCTYPE ni body.'},
  {id:7,type:'review',cat:'moviles',icon:'🎧',tag:'Review',title:'Sony WH-1000XM6: ¿Los mejores auriculares del mercado?',author:'María Ruiz',date:'12 may 2025',read:'10 min',score:'9.4',stars:'★★★★★',
   prompt:'Escribe una review completa en español (mínimo 800 palabras) de los auriculares Sony WH-1000XM6. Estructura: introducción, diseño, calidad de sonido, cancelación de ruido, micrófono, autonomía (40h), conectividad, app Sony Headphones, comparativa vs Bose QC Ultra, pros y cons, veredicto final con puntuación. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:8,type:'review',cat:'portatiles',icon:'💻',tag:'Review',title:'Dell XPS 16 (2025): potencia creativa sin concesiones',author:'Carlos Reyes',date:'11 may 2025',read:'11 min',score:'8.9',stars:'★★★★☆',
   prompt:'Escribe una review completa en español (mínimo 800 palabras) del Dell XPS 16 2025. Cubre: diseño premium, pantalla OLED 4K, rendimiento Intel Core Ultra 9, GPU RTX 4070, RAM, SSD, batería, teclado, puertos, precio, para quién es ideal. Pros y cons. Puntuación. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:9,type:'review',cat:'gaming',icon:'🖥️',tag:'Comparativa',title:'LG OLED C5 vs Samsung S95F: ¿Cuál es mejor para gaming?',author:'Javier Mora',date:'10 may 2025',read:'12 min',score:'9.1',stars:'★★★★★',
   prompt:'Escribe una comparativa en español (mínimo 850 palabras) entre LG OLED C5 y Samsung S95F para gaming. Compara: tipo de panel, brillo, contraste, tiempo de respuesta, VRR, HDMI 2.1, G-Sync, upscaling IA, consumo, precio. Conclusión: cuál elegir según perfil. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:10,type:'review',cat:'moviles',icon:'📱',tag:'Review',title:'iPhone 17 Pro Max: la IA que lo cambia todo',author:'Laura Pérez',date:'9 may 2025',read:'13 min',score:'9.6',stars:'★★★★★',
   prompt:'Escribe una review completa en español (mínimo 900 palabras) del iPhone 17 Pro Max. Cubre: diseño titanio, chip A19 Pro, cámaras (triple 48MP), Apple Intelligence en español, pantalla ProMotion 120Hz, batería, precio. Pros y cons. Comparativa con Samsung S25 Ultra. Veredicto. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>, <blockquote>. No incluyas DOCTYPE ni body.'},
  {id:11,type:'review',cat:'portatiles',icon:'⌚',tag:'Comparativa',title:'Apple Watch Ultra 3 vs Galaxy Watch 8 Ultra: duelo de gigantes',author:'Alejandro López',date:'8 may 2025',read:'10 min',score:'8.7',stars:'★★★★☆',
   prompt:'Escribe una comparativa en español (mínimo 800 palabras) entre Apple Watch Ultra 3 y Samsung Galaxy Watch 8 Ultra. Compara: diseño, resistencia, salud (ECG, SpO2), GPS, deportes, batería, ecosistema, precio. Conclusión clara. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:12,type:'ia',cat:'ia',icon:'🤖',tag:'IA & Futuro',title:'¿Puede la IA reemplazar a un médico? La realidad en 2025',author:'Carlos Reyes',date:'7 may 2025',read:'8 min',
   prompt:'Escribe un artículo de divulgación en español (mínimo 750 palabras) sobre el uso de la IA en medicina en 2025. Temas: diagnóstico por imagen, detección de cáncer, IA en urgencias, limitaciones éticas, privacidad de datos médicos, lo que la IA NO puede hacer, el rol del médico en el futuro. Equilibrado. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>, <blockquote>. No incluyas DOCTYPE ni body.'},
  {id:13,type:'ia',cat:'ia',icon:'🌐',tag:'IA & Futuro',title:'Computación cuántica: cuándo llegará a tu vida cotidiana',author:'Laura Pérez',date:'6 may 2025',read:'7 min',
   prompt:'Escribe un artículo divulgativo en español (mínimo 700 palabras) sobre computación cuántica para el público general. Incluye: qué es y cómo funciona con analogías simples, estado actual en 2025, aplicaciones futuras (farmacia, criptografía, IA), limitaciones actuales, timeline estimado. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:14,type:'ia',cat:'ia',icon:'🚗',tag:'IA & Futuro',title:'Coches autónomos en Europa: la gran promesa que tarda en llegar',author:'Javier Mora',date:'5 may 2025',read:'6 min',
   prompt:'Escribe un artículo en español (mínimo 700 palabras) sobre el estado de los coches autónomos en Europa en 2025. Incluye: niveles de autonomía (L1-L5), dónde estamos realmente, barreras legales en la UE, los actores principales (Tesla, Waymo, BYD), debate de seguridad, cuándo será realidad masiva. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:15,type:'ia',cat:'ia',icon:'🏠',tag:'IA & Futuro',title:'Smart Home en 2025: los gadgets que realmente merece la pena comprar',author:'María Ruiz',date:'4 may 2025',read:'7 min',
   prompt:'Escribe un artículo en español (mínimo 750 palabras) sobre gadgets de hogar inteligente que realmente merecen la pena en 2025. Cubre por categoría (termostatos, timbres, enchufes, bombillas, robots aspiradores, altavoces, cámaras): el mejor producto y precio aproximado. Usa HTML: <h2>, <h3>, <p>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:16,type:'tutorial',cat:'seguridad',icon:'🐧',tag:'Tutorial',title:'Instala Ubuntu 25 en tu PC sin borrar Windows: guía completa',author:'Carlos Reyes',date:'3 may 2025',read:'15 min',level:'b',
   prompt:'Escribe un tutorial completo en español (mínimo 900 palabras) para instalar Ubuntu 25 en dual boot con Windows. Pasos: requisitos previos, crear partición desde Windows, descargar Ubuntu, crear USB booteable (Rufus/BalenaEtcher), configurar BIOS/UEFI, instalación paso a paso, configurar GRUB. Incluye advertencias de seguridad. Usa HTML: <h2>, <h3>, <p>, <ol>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:17,type:'tutorial',cat:'seguridad',icon:'🔐',tag:'Tutorial',title:'Cómo montar tu propio servidor VPN con Raspberry Pi y WireGuard',author:'Alejandro López',date:'2 may 2025',read:'20 min',level:'a',
   prompt:'Escribe un tutorial técnico en español (mínimo 950 palabras) para configurar un servidor VPN con Raspberry Pi 5 y WireGuard. Pasos: requisitos hardware, instalar Raspberry Pi OS, instalar WireGuard, generar claves, configurar servidor y clientes (Windows/Android/iOS), port forwarding, probar conexión. Usa HTML: <h2>, <h3>, <p>, <ol>, <ul>, <li>, <strong>, <code>. No incluyas DOCTYPE ni body.'},
  {id:18,type:'tutorial',cat:'ia',icon:'🤖',tag:'Tutorial',title:'Usa la API de OpenAI con Python: tutorial desde cero para principiantes',author:'Laura Pérez',date:'1 may 2025',read:'18 min',level:'b',
   prompt:'Escribe un tutorial en español (mínimo 900 palabras) para usar la API de OpenAI con Python desde cero. Pasos: crear cuenta, obtener API key, instalar Python y pip, instalar openai library, primer script de chat, entender parámetros (temperature, max_tokens), crear chatbot simple, variables de entorno. Usa HTML: <h2>, <h3>, <p>, <ol>, <ul>, <li>, <strong>, <code>. No incluyas DOCTYPE ni body.'},
  {id:19,type:'tutorial',cat:'seguridad',icon:'🛡️',tag:'Tutorial',title:'Protege tus contraseñas con Bitwarden: configuración paso a paso',author:'María Ruiz',date:'30 abr 2025',read:'12 min',level:'b',
   prompt:'Escribe un tutorial en español (mínimo 800 palabras) para configurar Bitwarden como gestor de contraseñas. Incluye: por qué necesitas un gestor, Bitwarden gratis vs premium, instalación en navegador y móvil, importar contraseñas de Chrome/Firefox, activar 2FA, consejos para contraseña maestra. Usa HTML: <h2>, <h3>, <p>, <ol>, <ul>, <li>, <strong>. No incluyas DOCTYPE ni body.'},
  {id:20,type:'tutorial',cat:'ia',icon:'⚛️',tag:'Tutorial',title:'Crea tu primera app con React en 2025: guía para principiantes',author:'Carlos Reyes',date:'29 abr 2025',read:'22 min',level:'m',
   prompt:'Escribe un tutorial completo en español (mínimo 1000 palabras) para crear una app con React desde cero en 2025. Incluye: qué es React y por qué aprenderlo, instalar Node.js y npm, crear proyecto con Vite, estructura de carpetas, primer componente, props y estado (useState), useEffect, fetching de API pública, desplegar en Vercel gratis. Usa HTML: <h2>, <h3>, <p>, <ol>, <ul>, <li>, <strong>, <code>. No incluyas DOCTYPE ni body.'}
];

const generated = {};
let count = 0;

async function genArticle(a) {
  try {
    const res = await fetch('https://api.anthropic.com/v1/messages', {
      method:'POST',
      headers:{'Content-Type':'application/json'},
      body: JSON.stringify({
        model:'claude-sonnet-4-20250514',
        max_tokens:1000,
        messages:[{role:'user',content:a.prompt}]
      })
    });
    const data = await res.json();
    generated[a.id] = data.content?.map(b=>b.text||'').join('') || '<p>Error al generar el artículo.</p>';
  } catch(e) {
    generated[a.id] = '<p>Error al generar el artículo. Por favor recarga la página.</p>';
  }
  count++;
  const pct = (count/ARTICLES.length)*100;
  document.getElementById('gen-bar').style.width = pct+'%';
  document.getElementById('gen-count').textContent = count+'/'+ARTICLES.length;
  const msgs = ['Generando artículos con IA... ☕','Redactando reviews en profundidad... 📝','Escribiendo tutoriales paso a paso... 🎓','Últimos retoques... ✨'];
  document.getElementById('gen-status').textContent = msgs[Math.min(Math.floor(count/5), msgs.length-1)];
}

async function genAll() {
  const batches=[];
  for(let i=0;i<ARTICLES.length;i+=3) batches.push(ARTICLES.slice(i,i+3));
  for(const batch of batches){
    await Promise.all(batch.map(genArticle));
    await new Promise(r=>setTimeout(r,200));
  }
  document.getElementById('gen-overlay').style.display='none';
  renderAll();
}

function excerpt(html, words=28) {
  const d=document.createElement('div');
  d.innerHTML=html;
  const txt=d.textContent||d.innerText||'';
  return txt.split(' ').slice(0,words).join(' ')+'...';
}

function cardHTML(a, big=false) {
  const exc = generated[a.id] ? excerpt(generated[a.id], big?40:26) : a.title;
  return `<div class="card" onclick="openArticle(${a.id})">
    <div class="thumb">${a.icon}</div>
    <div class="cbody">
      <div class="ctag">${a.tag}</div>
      <div class="ctitle ${big?'big':''}">${a.title}</div>
      <div class="cexc">${exc}</div>
      <div class="cmeta">
        <div class="author"><div class="av">${a.author.split(' ').map(w=>w[0]).join('')}</div>${a.author} · ${a.date}</div>
        <div class="rt">${a.read}</div>
      </div>
    </div>
  </div>`;
}

function reviewHTML(a) {
  const exc = generated[a.id] ? excerpt(generated[a.id],22) : a.title;
  return `<div class="card" onclick="openArticle(${a.id})">
    <div class="thumb">${a.icon}</div>
    <div class="cbody">
      <div class="ctag r">${a.tag}</div>
      <div class="score">${a.score} / 10</div>
      <div class="stars" style="display:block;margin-bottom:.5rem">${a.stars}</div>
      <div class="ctitle">${a.title}</div>
      <div class="cexc">${exc}</div>
      <div class="cmeta">
        <span style="color:var(--accent);font-size:.78rem;font-weight:600">Leer análisis →</span>
        <div class="rt">${a.read}</div>
      </div>
    </div>
  </div>`;
}

function tutHTML(a) {
  const lvMap={b:['b','Principiante'],a:['a','Avanzado'],m:['m','Intermedio']};
  const [cls,lbl]=lvMap[a.level]||['b','Principiante'];
  return `<div class="tut" onclick="openArticle(${a.id})">
    <div class="ti">${a.icon}</div>
    <div><div class="tt">${a.title}</div><div class="tm">${a.read} de lectura <span class="lv ${cls}">${lbl}</span></div></div>
  </div>`;
}

function renderSection(cat='all') {
  const noticias = ARTICLES.filter(a=>a.type==='noticia');
  const filtered = cat==='all' ? noticias : noticias.filter(a=>a.cat===cat);
  const pool = filtered.length>=2 ? filtered : [...filtered,...noticias.filter(a=>!filtered.includes(a))];
  const [f1,f2,...rest]=pool;
  document.getElementById('main-articles').innerHTML=`
    <div class="feat">${f1?cardHTML(f1,true):''}${f2?cardHTML(f2):''}</div>
    <div class="g3">${rest.slice(0,3).map(a=>cardHTML(a)).join('')}</div>`;
}

function renderAll() {
  renderSection();

  const reviews=ARTICLES.filter(a=>a.type==='review');
  document.getElementById('reviews-grid').innerHTML=reviews.map(reviewHTML).join('');

  const ia=ARTICLES.filter(a=>a.type==='ia');
  document.getElementById('ia-grid').innerHTML=ia.map(a=>cardHTML(a)).join('');

  const tuts=ARTICLES.filter(a=>a.type==='tutorial');
  document.getElementById('tut-list').innerHTML=tuts.map(tutHTML).join('');

  const reads=[42,31,28,19];
  document.getElementById('trending-list').innerHTML=ARTICLES.slice(0,4).map((a,i)=>`
    <div class="tr-item" onclick="openArticle(${a.id})">
      <div class="tr-num">0${i+1}</div>
      <div><div class="tr-title">${a.title}</div><div class="tr-sub">${reads[i]}k lecturas</div></div>
    </div>`).join('');

  document.querySelectorAll('.cat').forEach(el=>{
    el.addEventListener('click',()=>{
      document.querySelectorAll('.cat').forEach(c=>c.classList.remove('on'));
      el.classList.add('on');
      renderSection(el.dataset.cat);
    });
  });
}

function openArticle(id) {
  const a=ARTICLES.find(x=>x.id===id);
  if(!a) return;
  document.getElementById('ao-tag').textContent=a.tag;
  document.getElementById('ao-title').textContent=a.title;
  document.getElementById('ao-meta').innerHTML=`
    <div class="author"><div class="av">${a.author.split(' ').map(w=>w[0]).join('')}</div>${a.author}</div>
    <span>·</span><span>${a.date}</span><span>·</span><span>${a.read} de lectura</span>`;
  document.getElementById('ao-content').innerHTML=generated[id]||'<div class="loading-state"><div class="spinner"></div> Cargando...</div>';
  const ov=document.getElementById('article-overlay');
  ov.classList.add('open');
  ov.scrollTo(0,0);
  document.body.style.overflow='hidden';
}

function closeArticle() {
  document.getElementById('article-overlay').classList.remove('open');
  document.body.style.overflow='';
}

document.addEventListener('keydown',e=>{if(e.key==='Escape') closeArticle();});
genAll();
</script>
</body>
</html>