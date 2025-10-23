<!doctype html>
<html lang="kk">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Веб-сайтты әзірлеу және интеграциялау — Қадам-қадаммен</title>
<link rel="icon" href="data:,">
<style>
  :root{
    --bg:#ffffff;
    --card:#f8fbff;
    --text:#0b2440;
    --muted:#556174;
    --accent:#1766c6;
    --round:12px;
    --maxw:1100px;
    font-family: Inter, "Helvetica Neue", Arial, sans-serif;
  }
  *{box-sizing:border-box}
  body{margin:0;background:linear-gradient(180deg,#ffffff,#fbfdff);color:var(--text);-webkit-font-smoothing:antialiased}
  .container{max-width:var(--maxw);margin:28px auto;padding:22px}
  header{display:flex;gap:20px;align-items:center;justify-content:space-between;flex-wrap:wrap}
  .hero{max-width:66%}
  h1{font-size:28px;margin:0 0 10px;line-height:1.05}
  p.lead{margin:0;color:var(--muted);font-size:15px}
  .cta{margin-top:12px;display:flex;gap:10px;align-items:center}
  .btn{background:var(--accent);color:white;padding:9px 14px;border-radius:999px;border:none;cursor:pointer;font-weight:600}
  .secondary{background:white;border:1px solid #e6eef9;color:var(--accent);padding:8px 12px;border-radius:999px}
  .hero-illustration{width:260px;height:160px;border-radius:14px;display:flex;align-items:center;justify-content:center}
  nav.toc{display:flex;flex-wrap:wrap;gap:8px;margin:16px 0}
  nav.toc button{background:#fff;border:1px solid #eef4ff;color:var(--text);padding:8px 12px;border-radius:999px;cursor:pointer}
  nav.toc button.active{background:var(--accent);color:white;border-color:var(--accent)}
  main{display:grid;gap:18px}
  section.card{background:linear-gradient(180deg,#ffffff,#f7fbff);border-radius:var(--round);padding:18px;box-shadow:0 6px 20px rgba(11,36,64,0.06);display:grid;grid-template-columns:1fr 320px;gap:18px;align-items:start}
  section.card h2{margin:0 0 8px;font-size:20px}
  section.card p{margin:0 0 8px;color:var(--muted);line-height:1.5}
  .notes{font-size:13px;color:var(--muted)}
  ul{margin:8px 0 0 18px;color:var(--muted)}
  .tag{display:inline-block;background:#e9f2ff;color:var(--accent);padding:6px 10px;border-radius:999px;font-weight:600}
  .svg-wrap{display:flex;align-items:center;justify-content:center;height:100%;min-height:120px;border-radius:10px;background:linear-gradient(180deg,#ffffff,#eef7ff);border:1px dashed #e6eef9}
  .techs{display:flex;flex-wrap:wrap;gap:8px;margin-top:8px}
  .pill{background:white;border:1px solid #e6eef9;padding:8px 12px;border-radius:10px;font-weight:600}
  footer{margin-top:18px;padding:14px 10px;text-align:center;color:var(--muted);font-size:14px}
  /* Responsive */
  @media (max-width:980px){
    .hero{max-width:100%}
    section.card{grid-template-columns:1fr;align-items:stretch}
    .hero-illustration{width:100%;height:140px}
  }
</style>
</head>
<body>
  <div class="container">
    <header>
      <div class="hero">
        <h1>Веб-сайтты әзірлеу және интеграциялау: Қадам-қадаммен</h1>
        <p class="lead">Бұл презентацияда біз заманауи веб-сайттарды құрудың және оларды бизнестің негізгі жүйелерімен интеграциялаудың негізгі кезеңдерін қарастырамыз.</p>
        <div class="cta">
          <span class="tag">1-БӨЛІМ</span>
          <button class="btn" onclick="scrollToId('slide-intro')">Бастау</button>
          <button class="secondary" onclick="downloadHTML()">HTML жүктеу</button>
        </div>
      </div>
      <div class="hero-illustration" aria-hidden="true">
        <!-- Placeholder illustration (replace with real image if needed) -->
        <svg width="240" height="140" viewBox="0 0 240 140" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="hero">
          <rect x="6" y="10" width="228" height="120" rx="10" fill="#f7fbff"/>
          <rect x="20" y="26" width="120" height="68" rx="8" fill="#e6f0ff"/>
          <rect x="150" y="30" width="58" height="12" rx="6" fill="#cfe3ff"/>
          <rect x="150" y="50" width="58" height="10" rx="6" fill="#cfe3ff"/>
          <rect x="20" y="100" width="188" height="8" rx="4" fill="#dfeeff"/>
        </svg>
      </div>
    </header>

    <nav class="toc" id="toc">
      <button data-target="slide-intro" class="active">Кіріспе</button>
      <button data-target="slide-process">Процесс</button>
      <button data-target="slide-tech">Технологиялар</button>
      <button data-target="slide-cms">CMS</button>
      <button data-target="slide-integ">Интеграция</button>
      <button data-target="slide-mobile">Мобильділік</button>
      <button data-target="slide-kz">Қазақстан</button>
      <button data-target="slide-trends">Трендтер</button>
      <button data-target="slide-conclude">Қорытынды</button>
    </nav>

    <main>
      <!-- Intro -->
      <section id="slide-intro" class="card">
        <div>
          <h2>Веб-сайттың маңызы мен мақсаты</h2>
          <p>Веб-сайт – бизнесіңіз бен брендіңіздің виртуалды әлемдегі негізгі алаңы. Ол 24/7 жұмыс істейтін цифрлық кеңсеңіз.</p>
          <ul>
            <li>Клиенттерді тарту</li>
            <li>Пайдалы ақпарат тарату</li>
            <li>Тиімді сату каналы құру</li>
          </ul>
          <p class="notes">Файлдағы дерек: Қазақстанда онлайн нарық жыл сайын 20%-дан астам өсуде.</p>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <!-- small illustrative SVG -->
          <svg width="180" height="110" viewBox="0 0 180 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="2" y="2" width="176" height="106" rx="8" fill="#fff"/>
            <rect x="14" y="14" width="100" height="64" rx="6" fill="#eaf5ff"/>
            <rect x="120" y="22" width="40" height="10" rx="4" fill="#d7ebff"/>
          </svg>
        </div>
      </section>

      <!-- Process -->
      <section id="slide-process" class="card">
        <div>
          <h2>Әзірлеу процесі</h2>
          <p>Сапалы нәтиже үшін әзірлеу процесі келесі негізгі кезеңдерден тұрады:</p>
          <ul>
            <li>Тапсырманы анықтау (ТТ құрастыру, мақсатты анықтау)</li>
            <li>Дизайн және UX/UI — адаптивті және қолданушыға ыңғайлы интерфейс</li>
            <li>Кодтау және вёрстка — HTML, CSS, JavaScript</li>
            <li>Тесттеу және іске қосу — қателерді түзету, мониторинг</li>
          </ul>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="160" height="110" viewBox="0 0 160 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="148" height="98" rx="8" fill="#fff"/>
            <circle cx="40" cy="40" r="22" fill="#e6f0ff"/>
            <rect x="74" y="24" width="70" height="14" rx="6" fill="#d7ebff"/>
            <rect x="74" y="46" width="70" height="12" rx="6" fill="#d7ebff"/>
          </svg>
        </div>
      </section>

      <!-- Tech -->
      <section id="slide-tech" class="card">
        <div>
          <h2>Технологиялық негіз</h2>
          <p>Веб-проект негізін құрайтын негізгі құралдар: құрылым — HTML, стиль — CSS, интерактивтілік — JavaScript. Серверлік тілдер: PHP, Python, Node.js.</p>
          <div class="techs">
            <span class="pill">HTML</span>
            <span class="pill">CSS</span>
            <span class="pill">JavaScript</span>
            <span class="pill">Node.js / PHP / Python</span>
            <span class="pill">API</span>
          </div>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="160" height="110" viewBox="0 0 160 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="8" y="8" width="144" height="94" rx="8" fill="#fff"/>
            <text x="20" y="40" font-size="12" fill="#92b9ff">{"<html>"}...</text>
            <text x="20" y="60" font-size="12" fill="#a6c9ff">CSS — стиль</text>
            <text x="20" y="80" font-size="12" fill="#cfe3ff">JS — динамика</text>
          </svg>
        </div>
      </section>

      <!-- CMS -->
      <section id="slide-cms" class="card">
        <div>
          <h2>CMS және платформалар</h2>
          <p>Файлдағы ұсынылған платформалар әртүрлі мақсаттар үшін:</p>
          <ul>
            <li><strong>1С-Битрикс</strong> — ірі корпоративтік порталдар мен интернет-дүкендер</li>
            <li><strong>Webasyst</strong> — икемді, ашық кодты платформа</li>
            <li><strong>WordPress & Drupal</strong> — блогтар мен шағын/орта бизнес үшін</li>
          </ul>
          <p class="notes">Платформаны таңдау — бюджет пен жоба талаптарына байланысты.</p>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="160" height="110" viewBox="0 0 160 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="148" height="98" rx="8" fill="#fff"/>
            <rect x="16" y="20" width="56" height="48" rx="6" fill="#e9f5ff"/>
            <rect x="84" y="24" width="56" height="16" rx="6" fill="#d7ebff"/>
            <rect x="84" y="46" width="56" height="16" rx="6" fill="#d7ebff"/>
          </svg>
        </div>
      </section>

      <!-- Integration -->
      <section id="slide-integ" class="card">
        <div>
          <h2>Интеграция: CRM & ERP</h2>
          <p>Веб-сайтты ішкі бизнес жүйелерімен біріктіру операциялық тиімділікті арттырады: тапсырыстар, клиент деректері, аналитика.</p>
          <ul>
            <li>Екі жақты синхрондау: клиент деректері — CRM, тапсырыстар — ERP</li>
            <li>Аналитикаға оқиғаларды жіберу (конверсия, трафик)</li>
            <li>API арқылы қауіпсіз және масштабталатын байланыс</li>
          </ul>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="160" height="110" viewBox="0 0 160 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="148" height="98" rx="8" fill="#fff"/>
            <path d="M30 40 L70 40 L110 40" stroke="#cfe3ff" stroke-width="8" stroke-linecap="round" fill="none"/>
            <circle cx="30" cy="40" r="12" fill="#e6f0ff"/>
            <circle cx="110" cy="40" r="12" fill="#e6f0ff"/>
          </svg>
        </div>
      </section>

      <!-- Mobile -->
      <section id="slide-mobile" class="card">
        <div>
          <h2>Мобильділік пен адаптивті дизайн</h2>
          <p>Қазіргі таңда қолданушылардың 70%+ сайттарға смартфондар немесе планшеттер арқылы кіреді. Сондықтан responsive дизайн және жылдамдық өте маңызды.</p>
          <ul>
            <li>Барлық құрылғыларға сай келу (Responsive)</li>
            <li>Жүктелу жылдамдығын оңтайландыру (Speed Optimization)</li>
            <li>Google мобильді индексациясына сәйкестік</li>
          </ul>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="120" height="100" viewBox="0 0 120 100" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="44" height="88" rx="6" fill="#eef9ff"/>
            <rect x="70" y="6" width="44" height="88" rx="6" fill="#eef9ff"/>
          </svg>
        </div>
      </section>

      <!-- Kazakhstan -->
      <section id="slide-kz" class="card">
        <div>
          <h2>Қазақстандағы тәжірибе</h2>
          <p>Файлда көрсетілген жергілікті мысалдар: ArtMedia, Sailet, 1С-Битрикс серіктестері — әрқайсысы өз саласында ерекше тәжірибеге ие.</p>
          <ul>
            <li><strong>ArtMedia:</strong> кең портфолио, жедел іске қосу</li>
            <li><strong>Sailet:</strong> масштабталатын веб және мобильді шешімдер</li>
            <li><strong>1С-Битрикс:</strong> ірі компанияларға интеграция және автоматтандыру</li>
          </ul>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="160" height="110" viewBox="0 0 160 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="148" height="98" rx="8" fill="#fff"/>
            <text x="24" y="58" font-size="12" fill="#a8cfff">Қазақстан тәжірибесі</text>
          </svg>
        </div>
      </section>

      <!-- Trends -->
      <section id="slide-trends" class="card">
        <div>
          <h2>Заманауи трендтер</h2>
          <ul>
            <li>SPA (Single Page Applications) — жылдам әрі интерактивті интерфейстер</li>
            <li>Веб-компоненттер — қайта қолданылатын UI-элементтер</li>
            <li>API-интеграциялар — қауіпсіз және масштабталатын архитектура</li>
          </ul>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="160" height="110" viewBox="0 0 160 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="148" height="98" rx="8" fill="#fff"/>
            <rect x="20" y="24" width="120" height="18" rx="6" fill="#eaf5ff"/>
            <rect x="20" y="52" width="80" height="18" rx="6" fill="#d7ebff"/>
          </svg>
        </div>
      </section>

      <!-- Conclusion -->
      <section id="slide-conclude" class="card">
        <div>
          <h2>Қорытынды</h2>
          <p class="notes">Негізгі тұжырымдар:</p>
          <ol>
            <li>Кәсіби әзірлеу — табыстың кепілі</li>
            <li>Интеграция және автоматтандыру — тиімділікті арттырады</li>
            <li>Заманауи технологиялар — бәсекелестік артықшылығы</li>
          </ol>
          <p style="margin-top:8px;color:var(--muted)">Веб-сайт — бұл жай ғана визитка емес, ол — сіздің цифрлық стратегияңыздың орталығы.</p>
        </div>
        <div class="svg-wrap" aria-hidden="true">
          <svg width="140" height="110" viewBox="0 0 140 110" xmlns="http://www.w3.org/2000/svg">
            <rect x="6" y="6" width="128" height="98" rx="8" fill="#fff"/>
            <path d="M30 70 L60 40 L90 70" stroke="#cfe3ff" stroke-width="8" stroke-linecap="round" fill="none"/>
          </svg>
        </div>
      </section>
    </main>

    <footer>
      Бұл HTML нұсқа файлдағы мәтіндық мазмұнға сәйкес жасалды. SVG-плейсхолдерларды нақты суреттерге ауыстыру үшін `img` тегі бойынша ресурстар қоса аласыз.
    </footer>
  </div>

<script>
  // simple navigation + active state
  const buttons = document.querySelectorAll('nav.toc button');
  buttons.forEach(btn=>{
    btn.addEventListener('click', ()=>{
      buttons.forEach(b=>b.classList.remove('active'));
      btn.classList.add('active');
      const id = btn.dataset.target;
      const el = document.getElementById(id);
      if(el) el.scrollIntoView({behavior:'smooth', block:'start'});
    });
  });

  // highlight active section on scroll
  const sections = Array.from(document.querySelectorAll('main section'));
  function onScroll(){
    const top = window.scrollY + 160;
    let idx = 0;
    sections.forEach((s,i)=>{ if(s.offsetTop <= top) idx = i; });
    buttons.forEach(b=>b.classList.remove('active'));
    if(buttons[idx]) buttons[idx].classList.add('active');
  }
  window.addEventListener('scroll', onScroll, {passive:true});
  onScroll();

  // convenience: scroll to id
  function scrollToId(id){ const el = document.getElementById(id); if(el) el.scrollIntoView({behavior:'smooth'}); }

  // download simple html copy (client-side)
  function downloadHTML(){
    const blob = new Blob([document.documentElement.outerHTML], {type: 'text/html;charset=utf-8'});
    const url = URL.createObjectURL(blob);
    const a = document.createElement('a');
    a.href = url;
    a.download = 'presentation.html';
    document.body.appendChild(a);
    a.click();
    a.remove();
    URL.revokeObjectURL(url);
  }
</script>
</body>
</html>
