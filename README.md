<!doctype html>
<html lang="kk">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Презентация — Website & Cloud</title>

  <!-- Опционально: подключение шрифта -->
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;700;800&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">

  <style>
    :root{
      --blue:#4f6bff;
      --deep-blue:#5b6cff;
      --accent:#ffb400;
      --muted:#555;
      --card-gap:24px;
      --bg:#f6f7fb;
      --white:#fff;
    }
    *{box-sizing:border-box}
    body{
      font-family: "Roboto", "Montserrat", Arial, sans-serif;
      margin:0;
      background:var(--bg);
      color:#222;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      padding:30px;
    }

    .presentation{
      max-width:1100px;
      margin:0 auto;
      background:linear-gradient(180deg, rgba(255,255,255,0.98), rgba(255,255,255,0.98));
      box-shadow:0 8px 30px rgba(20,30,60,0.08);
      border-radius:6px;
      overflow:hidden;
    }

    /* common top bar like in slide */
    .topbar{
      height:46px;
      background:linear-gradient(90deg,var(--deep-blue),var(--blue));
      display:flex;
      align-items:center;
      padding:0 18px;
      color:white;
      gap:12px;
    }
    .topbar .dots{
      margin-left:auto;
      display:flex;
      gap:8px;
      align-items:center;
    }
    .dot{
      width:10px;height:10px;border-radius:50%;background:rgba(255,255,255,0.9)
    }

    /* Slide layout */
    .slide{
      display:flex;
      gap:24px;
      padding:34px;
      align-items:stretch;
      background:white;
    }

    /* First slide specifics */
    .left{
      flex:1 1 60%;
      padding-right:12px;
      display:flex;
      flex-direction:column;
      justify-content:flex-start;
    }
    .title-big{
      font-family: "Montserrat", sans-serif;
      font-weight:800;
      color:var(--blue);
      font-size:72px;
      letter-spacing:1px;
      margin:6px 0 8px 0;
      display:flex;
      align-items:center;
      gap:12px;
    }
    .title-dot{
      width:14px;height:14px;border-radius:50%;background:var(--accent);
      display:inline-block;
    }
    .subtitle{
      font-size:20px;
      color:var(--muted);
      margin-bottom:18px;
    }
    .bullets{
      margin-top:8px;
      font-size:16px;
      color:#222;
      line-height:1.7;
      padding-left:18px;
    }
    .bullets li{margin:8px 0}

    .right{
      flex:0 0 360px;
      display:flex;
      align-items:center;
      justify-content:center;
      padding-left:12px;
    }
    .mockup{
      width:100%;
      background:linear-gradient(180deg,#7b2f7a,#6e2a7f);
      border-radius:6px;
      padding:18px;
      box-shadow:0 8px 30px rgba(0,0,0,0.08) inset;
      display:flex;
      align-items:center;
      justify-content:center;
    }
    .mockup img{
      width:100%;
      height:auto;
      border-radius:4px;
      object-fit:cover;
    }

    /* second slide */
    .slide-2{
      padding:40px 34px;
      display:block;
      background:white;
    }
    .h2{
      text-align:center;
      font-family:"Montserrat",sans-serif;
      font-size:40px;
      margin:4px 0 28px 0;
      font-weight:800;
      color:#111;
    }

    .cards{
      display:flex;
      gap:var(--card-gap);
      justify-content:space-between;
      align-items:stretch;
      padding:0 18px 36px 18px;
    }
    .card{
      flex:1;
      border-radius:8px;
      border:3px solid #f1f1f1;
      padding:18px;
      background:linear-gradient(180deg, rgba(255,255,255,0.98), rgba(255,255,255,0.98));
      display:flex;
      flex-direction:column;
      align-items:center;
      justify-content:flex-start;
      min-height:220px;
      position:relative;
    }

    /* colored outlines like в слайде */
    .card.one{ border-color:#f6b21d; }
    .card.two{ border-color:#4f6bff; }
    .card.three{ border-color:#ff6b7a; }

    .badge{
      width:72px;height:72px;border-radius:50%;
      display:flex;align-items:center;justify-content:center;
      color:white;font-weight:800;font-size:24px;
      margin-bottom:14px;
      box-shadow:0 6px 18px rgba(30,40,90,0.06);
    }
    .card.one .badge{ background:#f6b21d; }
    .card.two .badge{ background:#4f6bff; }
    .card.three .badge{ background:#ff6b7a; }

    .logo{
      margin-top:6px;
      width:86px;height:86px;
      display:flex;align-items:center;justify-content:center;
      filter:grayscale(0);
    }
    .logo img{ max-width:100%; max-height:100%; object-fit:contain; }

    .card p{ margin-top:12px; color:var(--muted); font-size:14px; text-align:center; padding:0 6px; }

    /* responsive */
    @media (max-width:880px){
      .slide{flex-direction:column}
      .right{order:-1;flex-basis:auto;padding-bottom:8px}
      .title-big{font-size:48px}
      .mockup{height:200px}
      .cards{flex-direction:column}
      .card{min-height:140px}
    }
  </style>
</head>
<body>

  <div class="presentation">
    <div class="topbar">
      <div style="font-weight:700">PROJECT</div>
      <div style="opacity:0.9">— simple demo</div>
      <div class="dots">
        <div class="dot"></div>
        <div class="dot"></div>
        <div class="dot"></div>
      </div>
    </div>

    <!-- Slide 1 -->
    <section class="slide" aria-label="Slide 1 — Website">
      <div class="left">
        <div class="title-big">WEBSITE <span class="title-dot" title="акцент"></span></div>
        <div class="subtitle">Веб-сайтты әзірлеу және интеграциялау:</div>

        <ul class="bullets">
          <li>Веб-сайт — интернет арқылы ашылатын веб-беттер жиынтығы.</li>
          <li>Негізгі құрылымы: HTML, CSS, JavaScript.</li>
          <li>Жасалу кезеңдері: жоспарлау → дизайн → кодтау → тест → жариялау.</li>
          <li>GitHub Pages — сайтты тегін интернетке шығару тәсілі.</li>
        </ul>

      </div>

      <div class="right">
        <div class="mockup">
          <!-- сюда можно поставить изображение слайда/макета -->
          <img src="PHOTO-2025-10-16-01-13-43.jpg" alt="website mockup">
        </div>
      </div>
    </section>

    <!-- Slide 2 -->
    <section class="slide-2" aria-label="Slide 2 — Cloud services">
      <h2 class="h2">Булттық қызметтер</h2>

      <div class="cards">
        <div class="card one" role="group" aria-label="Google Drive">
          <div class="badge">01</div>
          <div class="logo"><img src="https://upload.wikimedia.org/wikipedia/commons/1/1a/Google_Drive_logo.png" alt="Google Drive logo"></div>
          <p>Google Drive — файлдарды сақтау және ортақ пайдалану.</p>
        </div>

        <div class="card two" role="group" aria-label="GitHub">
          <div class="badge">02</div>
          <div class="logo"><img src="https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png" alt="GitHub logo"></div>
          <p>GitHub — код репозиторийлері, версия бақылау және Pages.</p>
        </div>

        <div class="card three" role="group" aria-label="Firebase">
          <div class="badge">03</div>
          <div class="logo"><img src="https://www.gstatic.com/devrel-devsite/prod/vc5a9b89f1a1c2a0e1b8f8f9f0b3a4f2f4f2e8b9d8f8e8a7f0d2a7a8/logo/firebase_2x.png" alt="Firebase logo"></div>
          <p>Firebase — бэкенд қызметтері: auth, database, hosting және тағы басқа.</p>
        </div>
      </div>
    </section>

  </div>

</body>
</html>
