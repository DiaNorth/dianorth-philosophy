<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>DiaNorth — Philosophy</title>
<link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body { background: #080808; color: #f0ebe0; font-family: 'DM Sans', system-ui, sans-serif; overflow-x: hidden; -webkit-font-smoothing: antialiased; }
  ::-webkit-scrollbar { width: 3px; }
  ::-webkit-scrollbar-track { background: #080808; }
  ::-webkit-scrollbar-thumb { background: rgba(240,235,224,0.12); }
  ::selection { background: rgba(180,130,60,0.25); }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(28px); }
    to   { opacity: 1; transform: none; }
  }
  .fade-in { opacity: 0; }
  .fade-in[data-visible] { animation: fadeInUp 1.2s cubic-bezier(0.22,1,0.36,1) both; }
  .d1[data-visible] { animation-delay: 0.12s; }
  .d2[data-visible] { animation-delay: 0.24s; }
  .d3[data-visible] { animation-delay: 0.36s; }
  .d4[data-visible] { animation-delay: 0.5s; }

  /* Hover utilities */
  .nav-link:hover { color: #c9a96e !important; }
  .cta-arrow:hover { gap: 22px !important; }
  .lang-btn:hover { color: #c9a96e !important; border-color: #c9a96e !important; }
  .icon-btn:hover { opacity: 1 !important; }
  .story-card { cursor: default; }
  .product-card:hover { background: #070707 !important; }
  .product-link:hover { opacity: 0.65 !important; }
  .cta-main-btn:hover { background: #c9a96e !important; color: #080808 !important; border-color: #c9a96e !important; }

  /* Lang toggle hidden class */
  .lang-en, .lang-jp { display: none; }
  body.lang-en .lang-en { display: block; }
  body.lang-jp .lang-jp { display: block; }
  body.lang-en .lang-en-inline { display: inline; }
  body.lang-jp .lang-jp-inline { display: inline; }
  .lang-en-inline, .lang-jp-inline { display: none; }

  /* Products grid image placeholder */
  .img-placeholder {
    aspect-ratio: 4/5;
    background: repeating-linear-gradient(32deg,#0c0c0c 0px,#0c0c0c 8px,#0a0a0a 8px,#0a0a0a 16px);
    position: relative;
    overflow: hidden;
    margin-bottom: 26px;
  }
  .img-placeholder-label {
    position: absolute;
    bottom: 14px; left: 14px; right: 14px;
    font-family: monospace;
    font-size: 8px;
    color: rgba(255,255,255,0.11);
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }
  /* Story image placeholder */
  .story-img {
    aspect-ratio: 3/4;
    background: repeating-linear-gradient(-42deg,#0f0f0f 0px,#0f0f0f 10px,#0b0b0b 10px,#0b0b0b 20px);
    position: relative;
    overflow: hidden;
    margin-bottom: 20px;
  }
  .story-img-label {
    position: absolute;
    inset: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 16px;
    text-align: center;
    font-family: monospace;
    font-size: 8.5px;
    color: rgba(255,255,255,0.12);
    letter-spacing: 0.1em;
    line-height: 1.9;
    text-transform: uppercase;
  }
  .story-img-fade {
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 35%;
    background: linear-gradient(to top, rgba(4,4,4,0.85), transparent);
  }

  @media (max-width: 768px) {
    #stories-grid { grid-template-columns: repeat(2,1fr) !important; }
    #products-grid { grid-template-columns: repeat(2,1fr) !important; }
    #hero-content { left: 24px !important; right: 24px !important; width: auto !important; bottom: 80px !important; }
    #manifesto-section { padding: 80px 24px !important; }
    #stories-section { padding: 80px 24px !important; }
    #criteria-section { padding: 80px 24px !important; }
    #products-section { padding: 80px 24px !important; }
    #cta-section { padding: 100px 24px !important; }
  }
</style>
</head>

<body class="lang-jp">

<!-- ═══════════════════════════════════════════
     HERO
════════════════════════════════════════════ -->
<section id="hero" style="position:relative;height:100vh;min-height:820px;overflow:hidden;">

  <!-- Background atmospheric -->
  <div style="position:absolute;inset:0;background:radial-gradient(ellipse at 72% 82%, rgba(70,26,4,0.8) 0%, transparent 42%), radial-gradient(ellipse at 55% 25%, rgba(10,18,42,0.95) 0%, transparent 60%), linear-gradient(168deg, #06080f 0%, #101828 50%, #050407 100%);">
    <div style="position:absolute;inset:0;background:repeating-linear-gradient(-22deg, transparent 0px, transparent 55px, rgba(255,255,255,0.008) 55px, rgba(255,255,255,0.008) 56px);"></div>
    <!-- Hero image goes here — replace this div with <img> tag -->
    <div id="hero-img-placeholder" style="position:absolute;top:50%;left:58%;transform:translate(-50%,-50%);text-align:center;pointer-events:none;user-select:none;">
      <div style="font-family:monospace;font-size:9px;color:rgba(255,255,255,0.09);letter-spacing:0.14em;text-transform:uppercase;line-height:2.4;white-space:nowrap;">snowy mountain fjord — dark overcast sky<br>man seated at campfire · seen from behind<br>cold ambient light · amber fire glow<br>— place full-bleed hero photograph here —</div>
    </div>
  </div>

  <!-- Gradient overlays -->
  <div style="position:absolute;inset:0;background:linear-gradient(to right, rgba(6,6,8,0.97) 0%, rgba(6,6,8,0.82) 40%, rgba(6,6,8,0.2) 68%, transparent 100%);"></div>
  <div style="position:absolute;bottom:0;left:0;right:0;height:40%;background:linear-gradient(to top, rgba(8,8,8,0.85), transparent);"></div>

  <!-- Content -->
  <div id="hero-content" style="position:absolute;bottom:108px;left:80px;width:min(600px,48vw);z-index:2;">

    <div class="fade-in" data-visible style="font-family:'DM Sans',sans-serif;font-size:10.5px;font-weight:500;letter-spacing:0.26em;color:#c9a96e;text-transform:uppercase;margin-bottom:28px;">
      <span class="lang-en-inline">DIANORTH SELECTION</span>
      <span class="lang-jp-inline">ダイアノース セレクション</span>
    </div>

    <h1 class="fade-in d1" data-visible style="font-family:'Oswald',sans-serif;font-weight:700;font-size:clamp(52px,7.5vw,104px);line-height:0.93;letter-spacing:-0.01em;color:#f0ebe0;text-transform:uppercase;white-space:pre-line;margin-bottom:32px;">
      <span class="lang-en-inline">FOR THOSE WHO&#10;CHOOSE WHAT'S REAL.</span>
      <span class="lang-jp-inline">本物を&#10;選ぶ人へ。</span>
    </h1>

    <div class="fade-in d2" data-visible style="width:52px;height:1.5px;background:#c9a96e;margin-bottom:32px;"></div>

    <p class="fade-in d2" data-visible style="font-family:'DM Sans',sans-serif;font-size:16.5px;font-weight:400;line-height:1.72;color:rgba(240,235,224,0.88);white-space:pre-line;margin-bottom:14px;">
      <span class="lang-en-inline">It's not about what you do.&#10;It's about why you do it.</span>
      <span class="lang-jp-inline">何をするかではない。&#10;なぜするかだ。</span>
    </p>

    <p class="fade-in d3" data-visible style="font-family:'DM Sans',sans-serif;font-size:13px;font-weight:300;line-height:1.8;color:rgba(240,235,224,0.5);white-space:pre-line;margin-bottom:52px;">
      <span class="lang-en-inline">Products chosen with purpose.&#10;For journeys that transform.</span>
      <span class="lang-jp-inline">目的を持って選ばれた製品。&#10;変革をもたらす旅のために。</span>
    </p>

    <a href="#manifesto" class="fade-in d4 cta-arrow" data-visible style="display:inline-flex;align-items:center;gap:14px;text-decoration:none;font-family:'DM Sans',sans-serif;font-size:10.5px;font-weight:500;letter-spacing:0.24em;color:#f0ebe0;text-transform:uppercase;transition:gap 0.4s ease;">
      <span class="lang-en-inline">DISCOVER MORE</span>
      <span class="lang-jp-inline">さらに探る</span>
      <svg width="22" height="10" viewBox="0 0 22 10" fill="none"><line x1="0" y1="5" x2="19" y2="5" stroke="currentColor" stroke-width="1.2"/><polyline points="13,0 22,5 13,10" stroke="currentColor" stroke-width="1.2" fill="none"/></svg>
    </a>
  </div>

  <!-- Watermark -->
  <div style="position:absolute;bottom:38px;right:56px;z-index:2;">
    <span style="font-family:'DM Sans',sans-serif;font-size:9px;font-weight:400;letter-spacing:0.28em;color:#c9a96e;text-transform:uppercase;">
      <span class="lang-en-inline">DESIGNED FOR REAL LIFE</span>
      <span class="lang-jp-inline">リアルライフのために</span>
    </span>
  </div>

  <!-- Lang toggle — floating -->
  <div style="position:absolute;top:28px;right:56px;z-index:10;">
    <button id="lang-toggle" class="lang-btn" onclick="toggleLang()" style="background:transparent;border:1px solid rgba(240,235,224,0.18);color:rgba(240,235,224,0.5);cursor:pointer;font-family:'DM Sans',sans-serif;font-size:9.5px;font-weight:500;letter-spacing:0.16em;padding:6px 14px;text-transform:uppercase;transition:color 0.25s,border-color 0.25s;">
      <span class="lang-en-inline">日本語</span>
      <span class="lang-jp-inline">English</span>
    </button>
  </div>

</section>


<!-- ═══════════════════════════════════════════
     MANIFESTO
════════════════════════════════════════════ -->
<section id="manifesto" id="manifesto-section" style="background:#080808;padding:160px 80px;">
  <div style="max-width:960px;margin:0 auto;">

    <div class="fade-in" style="display:flex;align-items:center;gap:18px;margin-bottom:88px;">
      <span style="font-family:'DM Sans',sans-serif;font-size:9.5px;font-weight:500;letter-spacing:0.3em;color:#c9a96e;text-transform:uppercase;white-space:nowrap;">
        <span class="lang-en-inline">OUR PHILOSOPHY</span>
        <span class="lang-jp-inline">私たちの哲学</span>
      </span>
      <div style="flex:1;height:1px;background:rgba(240,235,224,0.07);"></div>
    </div>

    <p class="fade-in d1" style="font-family:'DM Sans',sans-serif;font-size:clamp(24px,3.8vw,48px);font-weight:300;font-style:italic;line-height:1.38;color:rgba(240,235,224,0.3);letter-spacing:-0.01em;margin-bottom:20px;">
      <span class="lang-en-inline">The price of a product doesn't come from the product.</span>
      <span class="lang-jp-inline">製品の価格は製品から来るのではない。</span>
    </p>

    <p class="fade-in d2" style="font-family:'DM Sans',sans-serif;font-size:clamp(24px,3.8vw,48px);font-weight:300;font-style:italic;line-height:1.38;color:#f0ebe0;letter-spacing:-0.01em;margin-bottom:72px;">
      <span class="lang-en-inline">It comes from the distance between buying just anything — and choosing something with meaning.</span>
      <span class="lang-jp-inline">「何でもいいから買う」と「意味のあるものを選ぶ」の間の距離から来る。</span>
    </p>

    <div class="fade-in d3" style="display:flex;align-items:center;gap:24px;">
      <div style="width:44px;height:1.5px;background:#c9a96e;flex-shrink:0;"></div>
      <p style="font-family:'DM Sans',sans-serif;font-size:14.5px;font-weight:400;font-style:italic;color:rgba(240,235,224,0.55);letter-spacing:0.02em;">
        <span class="lang-en-inline">DiaNorth exists for those who understand that distance.</span>
        <span class="lang-jp-inline">ダイアノースは、その距離を理解する人のために存在する。</span>
      </p>
    </div>

  </div>
</section>


<!-- ═══════════════════════════════════════════
     STORIES
════════════════════════════════════════════ -->
<section id="stories-section" style="background:#040404;padding:128px 48px;">

  <div class="fade-in" style="display:flex;align-items:center;gap:18px;margin-bottom:64px;max-width:1440px;margin-left:auto;margin-right:auto;">
    <span style="font-family:'DM Sans',sans-serif;font-size:9.5px;font-weight:500;letter-spacing:0.3em;color:#c9a96e;text-transform:uppercase;white-space:nowrap;">
      <span class="lang-en-inline">REAL PEOPLE. REAL REASONS.</span>
      <span class="lang-jp-inline">リアルな人々。リアルな理由。</span>
    </span>
    <div style="flex:1;height:1px;background:rgba(240,235,224,0.07);"></div>
  </div>

  <div id="stories-grid" style="display:grid;grid-template-columns:repeat(5,1fr);gap:18px;max-width:1440px;margin:0 auto;">

    <!-- Story 1 -->
    <div class="fade-in story-card">
      <div class="story-img">
        <!-- REPLACE: upload image and put src here -->
        <!-- <img src="YOUR_IMAGE_URL" style="width:100%;height:100%;object-fit:cover;"> -->
        <div class="story-img-label lang-en-inline">runner at dawn · cold weather</div>
        <div class="story-img-label lang-jp-inline">早朝のランナー · 寒冷地</div>
        <div class="story-img-fade"></div>
      </div>
      <h3 style="font-family:'Oswald',sans-serif;font-size:13px;font-weight:600;letter-spacing:0.12em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
        <span class="lang-en-inline">The Runner</span>
        <span class="lang-jp-inline">ランナー</span>
      </h3>
      <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.72;color:rgba(240,235,224,0.42);">
        <span class="lang-en-inline">Before dawn. In the cold. Not for records — for clarity.</span>
        <span class="lang-jp-inline">夜明け前。寒さの中。記録のためではなく——明晰さのために。</span>
      </p>
    </div>

    <!-- Story 2 -->
    <div class="fade-in d1 story-card">
      <div class="story-img">
        <div class="story-img-label lang-en-inline">woman · outdoor yoga</div>
        <div class="story-img-label lang-jp-inline">女性 · 屋外ヨガ</div>
        <div class="story-img-fade"></div>
      </div>
      <h3 style="font-family:'Oswald',sans-serif;font-size:13px;font-weight:600;letter-spacing:0.12em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
        <span class="lang-en-inline">The Yogi</span>
        <span class="lang-jp-inline">ヨギ</span>
      </h3>
      <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.72;color:rgba(240,235,224,0.42);">
        <span class="lang-en-inline">She breathes. The world quiets. Presence is the practice.</span>
        <span class="lang-jp-inline">彼女は息をする。世界が静まる。存在そのものが修行だ。</span>
      </p>
    </div>

    <!-- Story 3 -->
    <div class="fade-in d2 story-card">
      <div class="story-img">
        <div class="story-img-label lang-en-inline">man at campfire · mountain lake</div>
        <div class="story-img-label lang-jp-inline">男性 · 焚き火 · 山岳湖畔</div>
        <div class="story-img-fade"></div>
      </div>
      <h3 style="font-family:'Oswald',sans-serif;font-size:13px;font-weight:600;letter-spacing:0.12em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
        <span class="lang-en-inline">The Campfire Man</span>
        <span class="lang-jp-inline">焚き火の男</span>
      </h3>
      <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.72;color:rgba(240,235,224,0.42);">
        <span class="lang-en-inline">He sits with the fire. No notifications. Only fire.</span>
        <span class="lang-jp-inline">彼は火とともに座る。通知なし。ただ、火だけ。</span>
      </p>
    </div>

    <!-- Story 4 -->
    <div class="fade-in d3 story-card">
      <div class="story-img">
        <div class="story-img-label lang-en-inline">father + child · hiking trail</div>
        <div class="story-img-label lang-jp-inline">父親と子供 · ハイキング</div>
        <div class="story-img-fade"></div>
      </div>
      <h3 style="font-family:'Oswald',sans-serif;font-size:13px;font-weight:600;letter-spacing:0.12em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
        <span class="lang-en-inline">The Father</span>
        <span class="lang-jp-inline">父親</span>
      </h3>
      <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.72;color:rgba(240,235,224,0.42);">
        <span class="lang-en-inline">He carries more than gear. He carries intention.</span>
        <span class="lang-jp-inline">彼は装備以上のものを運ぶ。意図を運ぶ。</span>
      </p>
    </div>

    <!-- Story 5 -->
    <div class="fade-in d4 story-card">
      <div class="story-img">
        <div class="story-img-label lang-en-inline">young person · mountain path</div>
        <div class="story-img-label lang-jp-inline">若者 · 山道</div>
        <div class="story-img-fade"></div>
      </div>
      <h3 style="font-family:'Oswald',sans-serif;font-size:13px;font-weight:600;letter-spacing:0.12em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
        <span class="lang-en-inline">The Student</span>
        <span class="lang-jp-inline">学生</span>
      </h3>
      <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.72;color:rgba(240,235,224,0.42);">
        <span class="lang-en-inline">Still learning. Still moving. Always questioning.</span>
        <span class="lang-jp-inline">まだ学んでいる。まだ動いている。常に問い続ける。</span>
      </p>
    </div>

  </div>
</section>


<!-- ═══════════════════════════════════════════
     CRITERIA
════════════════════════════════════════════ -->
<section id="criteria-section" style="background:#080808;padding:148px 80px;">
  <div style="max-width:680px;margin:0 auto;text-align:center;">

    <div class="fade-in" style="display:flex;align-items:center;justify-content:center;gap:18px;margin-bottom:52px;">
      <div style="width:40px;height:1px;background:#c9a96e;"></div>
      <span style="font-family:'DM Sans',sans-serif;font-size:9.5px;font-weight:500;letter-spacing:0.3em;color:#c9a96e;text-transform:uppercase;">
        <span class="lang-en-inline">WHY THESE PRODUCTS</span>
        <span class="lang-jp-inline">なぜこれらの製品なのか</span>
      </span>
      <div style="width:40px;height:1px;background:#c9a96e;"></div>
    </div>

    <p class="fade-in d1" style="font-family:'DM Sans',sans-serif;font-size:clamp(15px,1.9vw,21px);font-weight:300;font-style:italic;line-height:1.8;color:rgba(240,235,224,0.68);">
      <span class="lang-en-inline">A store tries to convince you a product has value. This page exists to show you that DiaNorth has criteria. When you believe in the criteria, price stops being the center of the conversation.</span>
      <span class="lang-jp-inline">店は製品に価値があるとあなたを説得しようとする。このページは、ダイアノースには基準があることを示すために存在する。その基準を信じるとき、価格はもはや会話の中心ではなくなる。</span>
    </p>

  </div>
</section>


<!-- ═══════════════════════════════════════════
     PRODUCTS
════════════════════════════════════════════ -->
<section id="products-section" style="background:#040404;padding:128px 48px;">

  <div class="fade-in" style="display:flex;align-items:center;gap:18px;margin-bottom:64px;max-width:1440px;margin-left:auto;margin-right:auto;">
    <span style="font-family:'DM Sans',sans-serif;font-size:9.5px;font-weight:500;letter-spacing:0.3em;color:#c9a96e;text-transform:uppercase;white-space:nowrap;">
      <span class="lang-en-inline">SELECTED FOR A REASON</span>
      <span class="lang-jp-inline">理由があって選ばれた</span>
    </span>
    <div style="flex:1;height:1px;background:rgba(240,235,224,0.07);"></div>
  </div>

  <div id="products-grid" style="display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:rgba(240,235,224,0.05);max-width:1440px;margin:0 auto;">

    <!-- Product 1 -->
    <div class="fade-in product-card" style="background:#040404;padding-bottom:36px;transition:background 0.3s;">
      <div class="img-placeholder">
        <!-- REPLACE: <img src="YOUR_IMAGE_URL" style="width:100%;height:100%;object-fit:cover;"> -->
        <div class="img-placeholder-label">thermal base layer</div>
      </div>
      <div style="padding:0 22px;">
        <h3 style="font-family:'Oswald',sans-serif;font-size:13.5px;font-weight:500;letter-spacing:0.09em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
          <span class="lang-en-inline">Thermal Base Layer Pro</span>
          <span class="lang-jp-inline">サーマルベースレイヤー Pro</span>
        </h3>
        <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.68;color:rgba(240,235,224,0.42);margin-bottom:22px;">
          <span class="lang-en-inline">Because warmth without bulk is a form of freedom.</span>
          <span class="lang-jp-inline">かさばらない温かさは、自由の一形態だから。</span>
        </p>
        <div style="display:flex;align-items:center;justify-content:space-between;border-top:1px solid rgba(240,235,224,0.07);padding-top:16px;">
          <span style="font-family:'DM Sans',sans-serif;font-size:13.5px;font-weight:400;color:#f0ebe0;letter-spacing:0.04em;">¥18,000</span>
          <a href="#" class="product-link" style="font-family:'DM Sans',sans-serif;font-size:9px;font-weight:500;letter-spacing:0.2em;color:#c9a96e;text-transform:uppercase;text-decoration:none;transition:opacity 0.2s;">VIEW →</a>
        </div>
      </div>
    </div>

    <!-- Product 2 -->
    <div class="fade-in d1 product-card" style="background:#040404;padding-bottom:36px;transition:background 0.3s;">
      <div class="img-placeholder">
        <div class="img-placeholder-label">alpine wind shell</div>
      </div>
      <div style="padding:0 22px;">
        <h3 style="font-family:'Oswald',sans-serif;font-size:13.5px;font-weight:500;letter-spacing:0.09em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
          <span class="lang-en-inline">Alpine Wind Shell</span>
          <span class="lang-jp-inline">アルパイン ウィンドシェル</span>
        </h3>
        <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.68;color:rgba(240,235,224,0.42);margin-bottom:22px;">
          <span class="lang-en-inline">Because the mountain doesn't negotiate. Neither do we.</span>
          <span class="lang-jp-inline">山は交渉しない。私たちも同様だ。</span>
        </p>
        <div style="display:flex;align-items:center;justify-content:space-between;border-top:1px solid rgba(240,235,224,0.07);padding-top:16px;">
          <span style="font-family:'DM Sans',sans-serif;font-size:13.5px;font-weight:400;color:#f0ebe0;letter-spacing:0.04em;">¥32,000</span>
          <a href="#" class="product-link" style="font-family:'DM Sans',sans-serif;font-size:9px;font-weight:500;letter-spacing:0.2em;color:#c9a96e;text-transform:uppercase;text-decoration:none;transition:opacity 0.2s;">VIEW →</a>
        </div>
      </div>
    </div>

    <!-- Product 3 -->
    <div class="fade-in d2 product-card" style="background:#040404;padding-bottom:36px;transition:background 0.3s;">
      <div class="img-placeholder">
        <div class="img-placeholder-label">trail running pack 12L</div>
      </div>
      <div style="padding:0 22px;">
        <h3 style="font-family:'Oswald',sans-serif;font-size:13.5px;font-weight:500;letter-spacing:0.09em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
          <span class="lang-en-inline">Trail Running Pack 12L</span>
          <span class="lang-jp-inline">トレイルランニングパック 12L</span>
        </h3>
        <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.68;color:rgba(240,235,224,0.42);margin-bottom:22px;">
          <span class="lang-en-inline">Because what you carry shapes how far you go.</span>
          <span class="lang-jp-inline">何を運ぶかが、どこまで行けるかを決めるから。</span>
        </p>
        <div style="display:flex;align-items:center;justify-content:space-between;border-top:1px solid rgba(240,235,224,0.07);padding-top:16px;">
          <span style="font-family:'DM Sans',sans-serif;font-size:13.5px;font-weight:400;color:#f0ebe0;letter-spacing:0.04em;">¥24,000</span>
          <a href="#" class="product-link" style="font-family:'DM Sans',sans-serif;font-size:9px;font-weight:500;letter-spacing:0.2em;color:#c9a96e;text-transform:uppercase;text-decoration:none;transition:opacity 0.2s;">VIEW →</a>
        </div>
      </div>
    </div>

    <!-- Product 4 -->
    <div class="fade-in d3 product-card" style="background:#040404;padding-bottom:36px;transition:background 0.3s;">
      <div class="img-placeholder">
        <div class="img-placeholder-label">summit down jacket</div>
      </div>
      <div style="padding:0 22px;">
        <h3 style="font-family:'Oswald',sans-serif;font-size:13.5px;font-weight:500;letter-spacing:0.09em;text-transform:uppercase;color:#f0ebe0;margin-bottom:10px;">
          <span class="lang-en-inline">Summit Down Jacket</span>
          <span class="lang-jp-inline">サミット ダウンジャケット</span>
        </h3>
        <p style="font-family:'DM Sans',sans-serif;font-size:12px;font-weight:300;font-style:italic;line-height:1.68;color:rgba(240,235,224,0.42);margin-bottom:22px;">
          <span class="lang-en-inline">Because cold is only a problem if you're unprepared.</span>
          <span class="lang-jp-inline">寒さは、準備ができていない人だけの問題だから。</span>
        </p>
        <div style="display:flex;align-items:center;justify-content:space-between;border-top:1px solid rgba(240,235,224,0.07);padding-top:16px;">
          <span style="font-family:'DM Sans',sans-serif;font-size:13.5px;font-weight:400;color:#f0ebe0;letter-spacing:0.04em;">¥58,000</span>
          <a href="#" class="product-link" style="font-family:'DM Sans',sans-serif;font-size:9px;font-weight:500;letter-spacing:0.2em;color:#c9a96e;text-transform:uppercase;text-decoration:none;transition:opacity 0.2s;">VIEW →</a>
        </div>
      </div>
    </div>

  </div>
</section>


<!-- ═══════════════════════════════════════════
     FINAL CTA
════════════════════════════════════════════ -->
<section id="cta-section" style="background:#080808;padding:190px 80px;text-align:center;border-top:1px solid rgba(240,235,224,0.05);">

  <div class="fade-in" style="font-family:'DM Sans',sans-serif;font-size:9.5px;font-weight:500;letter-spacing:0.32em;color:#c9a96e;text-transform:uppercase;margin-bottom:48px;">
    <span class="lang-en-inline">READY TO CHOOSE</span>
    <span class="lang-jp-inline">選ぶ準備はできていますか</span>
  </div>

  <p class="fade-in d1" style="font-family:'DM Sans',sans-serif;font-size:clamp(17px,2.3vw,27px);font-weight:300;font-style:italic;line-height:1.72;color:rgba(240,235,224,0.62);white-space:pre-line;max-width:520px;margin:0 auto 72px;">
    <span class="lang-en-inline">The store is where you find the products.&#10;This page is where you understand why they matter.</span>
    <span class="lang-jp-inline">ストアは製品を見つける場所。&#10;このページは、なぜそれらが重要かを理解する場所。</span>
  </p>

  <!-- REPLACE href with your actual store URL -->
  <a href="/all-products" class="fade-in d2 cta-main-btn" style="display:inline-block;font-family:'DM Sans',sans-serif;font-size:10.5px;font-weight:500;letter-spacing:0.24em;text-transform:uppercase;background:transparent;border:1px solid rgba(240,235,224,0.28);color:#f0ebe0;padding:18px 54px;text-decoration:none;transition:background 0.38s,color 0.38s,border-color 0.38s;">
    <span class="lang-en-inline">ENTER THE STORE →</span>
    <span class="lang-jp-inline">ストアへ →</span>
  </a>

  <div style="margin-top:148px;padding-top:44px;border-top:1px solid rgba(240,235,224,0.05);display:flex;flex-direction:column;align-items:center;gap:16px;">
    <!-- REPLACE src with your Wix Media Manager logo URL -->
    <img src="uploads/Dianorth logo 05_result.webp" alt="DiaNorth" style="height:28px;width:auto;mix-blend-mode:screen;opacity:0.35;display:block;" onerror="this.style.display='none'" />
    <p style="font-family:'DM Sans',sans-serif;font-size:9px;color:rgba(240,235,224,0.16);letter-spacing:0.2em;text-transform:uppercase;">© 2025 DiaNorth Hokkaido. All rights reserved.</p>
  </div>

</section>


<!-- ═══════════════════════════════════════════
     JS — Scroll animations + Lang toggle
════════════════════════════════════════════ -->
<script>
  // ── Scroll-triggered fade-in ──────────────
  (function() {
    var els = document.querySelectorAll('.fade-in:not([data-visible])');
    if (!els.length) return;
    var obs = new IntersectionObserver(function(entries) {
      entries.forEach(function(e) {
        if (e.isIntersecting && !e.target.hasAttribute('data-visible')) {
          e.target.setAttribute('data-visible', '1');
        }
      });
    }, { threshold: 0.07, rootMargin: '0px 0px -24px 0px' });
    els.forEach(function(el) { obs.observe(el); });
  })();

  // ── Language toggle ───────────────────────
  function toggleLang() {
    var body = document.body;
    if (body.classList.contains('lang-jp')) {
      body.classList.remove('lang-jp');
      body.classList.add('lang-en');
    } else {
      body.classList.remove('lang-en');
      body.classList.add('lang-jp');
    }
  }
</script>

</body>
</html>
