
<style>
  @import url('https://fonts.googleapis.com/css2?family=Rajdhani:wght@400;600;700&family=JetBrains+Mono:wght@400;500&display=swap');
  .xb-root{background:#0e0e0e;color:#f2f2f2;font-family:'Rajdhani',sans-serif;padding:28px 24px;border-radius:8px;border:1px solid #1e1e1e;}
  .xb-banner{background:linear-gradient(135deg,#0a1a0a 0%,#0e0e0e 40%,#0d1f0d 100%);border:1px solid #107c10;border-radius:6px;padding:28px 24px 22px;margin-bottom:20px;position:relative;overflow:hidden;}
  .xb-banner::before{content:'';position:absolute;top:-40px;right:-40px;width:160px;height:160px;border-radius:50%;background:rgba(16,124,16,0.08);}
  .xb-banner::after{content:'';position:absolute;bottom:-30px;left:-30px;width:100px;height:100px;border-radius:50%;background:rgba(82,176,67,0.06);}
  .xb-name-row{display:flex;align-items:center;gap:14px;margin-bottom:14px;}
  .xb-avatar{width:52px;height:52px;border-radius:4px;background:#107c10;display:flex;align-items:center;justify-content:center;font-family:'JetBrains Mono',monospace;font-size:18px;font-weight:500;color:#000;flex-shrink:0;border:1px solid #52b043;}
  .xb-name{font-size:26px;font-weight:700;letter-spacing:-0.01em;line-height:1;}
  .xb-role{font-family:'JetBrains Mono',monospace;font-size:11px;color:#52b043;margin-top:4px;letter-spacing:0.1em;}
  .xb-bio{font-family:'JetBrains Mono',monospace;font-size:11.5px;color:#b3b3b3;line-height:1.75;border-left:2px solid #107c10;padding-left:14px;}
  .xb-bio strong{color:#9bc848;font-weight:500;}
  .xb-facts{display:flex;gap:8px;margin-bottom:20px;flex-wrap:wrap;}
  .xb-fact{background:#111;border:1px solid #1e1e1e;border-radius:4px;padding:9px 14px;font-family:'JetBrains Mono',monospace;font-size:11px;color:#b3b3b3;display:flex;align-items:center;gap:7px;flex:1;min-width:180px;}
  .xb-fact i{color:#52b043;font-size:15px;}
  .xb-fact strong{color:#f2f2f2;}
  .xb-links{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:20px;}
  .xb-link{display:inline-flex;align-items:center;gap:7px;padding:8px 16px;border-radius:3px;font-family:'JetBrains Mono',monospace;font-size:11px;font-weight:500;text-decoration:none;letter-spacing:0.05em;transition:opacity 0.15s;cursor:pointer;}
  .xb-link:hover{opacity:0.8;}
  .xb-link-primary{background:#107c10;color:#000;}
  .xb-link-ghost{background:transparent;border:1px solid #1e1e1e;color:#b3b3b3;}
  .xb-link-ghost:hover{border-color:#52b043;color:#52b043;}
  .xb-section-label{font-family:'JetBrains Mono',monospace;font-size:10px;color:#52b043;letter-spacing:0.2em;text-transform:uppercase;margin-bottom:12px;display:flex;align-items:center;gap:10px;}
  .xb-section-label::after{content:'';flex:1;height:1px;background:#1e1e1e;}
  .xb-stack-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(90px,1fr));gap:8px;margin-bottom:20px;}
  .xb-chip{background:#111;border:1px solid #1e1e1e;border-radius:3px;padding:10px 8px;text-align:center;font-family:'JetBrains Mono',monospace;font-size:10px;color:#6e6e6e;display:flex;flex-direction:column;align-items:center;gap:6px;cursor:default;transition:border-color 0.15s,color 0.15s;}
  .xb-chip:hover{border-color:#107c10;color:#f2f2f2;}
  .xb-chip i{font-size:20px;color:#52b043;}
  .xb-stats-bar{display:grid;grid-template-columns:repeat(4,1fr);border:1px solid #1e1e1e;border-radius:4px;overflow:hidden;margin-bottom:20px;}
  .xb-stat{padding:16px 12px;border-right:1px solid #1e1e1e;background:#111;text-align:center;}
  .xb-stat:last-child{border-right:none;}
  .xb-stat-num{font-size:28px;font-weight:700;color:#52b043;line-height:1;display:block;margin-bottom:4px;}
  .xb-stat-label{font-family:'JetBrains Mono',monospace;font-size:9px;color:#6e6e6e;text-transform:uppercase;letter-spacing:0.12em;}
  .xb-terminal{background:#080808;border:1px solid #1e1e1e;border-radius:4px;padding:18px 20px;margin-bottom:20px;font-family:'JetBrains Mono',monospace;font-size:12px;line-height:2;}
  .xb-terminal .prompt{color:#107c10;}
  .xb-terminal .key{color:#6e6e6e;}
  .xb-terminal .val{color:#f2f2f2;}
  .xb-terminal .val-green{color:#9bc848;}
  .xb-terminal .val-highlight{color:#f2f2f2;background:rgba(16,124,16,0.15);border:1px solid rgba(82,176,67,0.25);padding:1px 8px;border-radius:3px;}
  .xb-badge{display:inline-flex;align-items:center;gap:5px;font-family:'JetBrains Mono',monospace;font-size:9px;padding:3px 9px;border-radius:2px;letter-spacing:0.08em;vertical-align:middle;}
  .xb-badge-green{background:rgba(16,124,16,0.15);border:1px solid rgba(82,176,67,0.3);color:#9bc848;}
  .xb-badge-dot{width:6px;height:6px;border-radius:50%;background:#52b043;animation:pulse 2s infinite;}
  @keyframes pulse{0%,100%{opacity:1}50%{opacity:0.3}}
  .xb-contrib{background:#080808;border:1px solid #1e1e1e;border-radius:4px;padding:16px;margin-bottom:4px;}
  .xb-contrib-row{display:flex;gap:3px;flex-wrap:wrap;}
  .xb-day{width:11px;height:11px;border-radius:1px;flex-shrink:0;}
</style>

<div class="xb-root">

  <div class="xb-banner">
    <div class="xb-name-row">
      <div class="xb-avatar">CT</div>
      <div>
        <div class="xb-name">Camilo Tacue Salazar</div>
        <div class="xb-role">full-stack developer · popayán, colombia</div>
      </div>
    </div>
    <p class="xb-bio">
      Desarrollador Full-Stack con más de <strong>1 año de experiencia</strong> en proyectos reales.<br>
      Especializado en <strong>Angular</strong>, <strong>React</strong> y <strong>TypeScript</strong> · <strong>Node.js</strong> · bases de datos relacionales y no relacionales.<br>
      Me destaco en trabajo colaborativo bajo <strong>Scrum</strong> y fuerte compromiso con la calidad del código.
    </p>
  </div>

  <div class="xb-facts">
    <div class="xb-fact">
      <i class="ti ti-device-mobile" aria-hidden="true"></i>
      Aprendiendo: <strong>&nbsp;Expo · Desarrollo Mobile</strong>
    </div>
    <div class="xb-fact">
      <i class="ti ti-sword" aria-hidden="true"></i>
      Dato curioso: fanático del <strong>&nbsp;hack and slash</strong>
    </div>
  </div>

  <div class="xb-links">
    <a class="xb-link xb-link-primary" href="https://my-code-studio.vercel.app/" target="_blank">
      <i class="ti ti-world" aria-hidden="true"></i> Portfolio
    </a>
    <a class="xb-link xb-link-ghost" href="https://mail.google.com/mail/?view=cm&fs=1&to=c4m1loo12@gmail.com" target="_blank">
      <i class="ti ti-mail" aria-hidden="true"></i> Email
    </a>
    <a class="xb-link xb-link-ghost" href="https://drive.google.com/file/d/1ksZTXPpR1k1LdJ9NR3dcSwvfse93bJ2P/view?usp=sharing" target="_blank">
      <i class="ti ti-file-cv" aria-hidden="true"></i> CV
    </a>
    <a class="xb-link xb-link-ghost" href="https://www.linkedin.com/in/camilo-salazar-35717932a" target="_blank">
      <i class="ti ti-brand-linkedin" aria-hidden="true"></i> LinkedIn
    </a>
    <span class="xb-badge xb-badge-green"><span class="xb-badge-dot"></span> disponible</span>
  </div>

  <div class="xb-stats-bar">
    <div class="xb-stat"><span class="xb-stat-num">1+</span><span class="xb-stat-label">años exp.</span></div>
    <div class="xb-stat"><span class="xb-stat-num">2</span><span class="xb-stat-label">empresas</span></div>
    <div class="xb-stat"><span class="xb-stat-num">10+</span><span class="xb-stat-label">tecnologías</span></div>
    <div class="xb-stat"><span class="xb-stat-num">∞</span><span class="xb-stat-label">aprendiendo</span></div>
  </div>

  <div class="xb-section-label">stack tecnológico</div>

  <div class="xb-stack-grid">
    <div class="xb-chip"><i class="ti ti-brand-angular"></i>Angular</div>
    <div class="xb-chip"><i class="ti ti-brand-react"></i>React</div>
    <div class="xb-chip"><i class="ti ti-brand-typescript"></i>TypeScript</div>
    <div class="xb-chip"><i class="ti ti-brand-javascript"></i>JavaScript</div>
    <div class="xb-chip"><i class="ti ti-brand-html5"></i>HTML5</div>
    <div class="xb-chip"><i class="ti ti-brand-css3"></i>CSS3</div>
    <div class="xb-chip"><i class="ti ti-palette"></i>SCSS</div>
    <div class="xb-chip"><i class="ti ti-wind"></i>Tailwind</div>
    <div class="xb-chip"><i class="ti ti-brand-nodejs"></i>Node.js</div>
    <div class="xb-chip"><i class="ti ti-coffee"></i>Java</div>
    <div class="xb-chip"><i class="ti ti-leaf"></i>Spring</div>
    <div class="xb-chip"><i class="ti ti-database"></i>MongoDB</div>
    <div class="xb-chip"><i class="ti ti-database"></i>MySQL</div>
    <div class="xb-chip"><i class="ti ti-database"></i>Supabase</div>
    <div class="xb-chip"><i class="ti ti-brand-git"></i>Git</div>
    <div class="xb-chip"><i class="ti ti-brand-figma"></i>Figma</div>
    <div class="xb-chip"><i class="ti ti-device-mobile"></i>Expo</div>
  </div>

  <div class="xb-section-label">actualmente</div>

  <div class="xb-terminal">
    <div><span class="prompt">›</span> <span class="key">status        </span> <span class="val">trabajando en <span class="val-green">Tinge Studio</span> (Full-Stack)</span></div>
    <div><span class="prompt">›</span> <span class="key">aprendiendo   </span> <span class="val-highlight">Expo · Desarrollo Mobile</span></div>
    <div><span class="prompt">›</span> <span class="key">disponible    </span> <span class="val-green">proyectos freelance ✓</span></div>
    <div><span class="prompt">›</span> <span class="key">ubicación     </span> <span class="val">Popayán, Colombia</span></div>
    <div><span class="prompt">›</span> <span class="key">stack actual  </span> <span class="val">React · TypeScript · Supabase · Webflow</span></div>
  </div>

  <div class="xb-section-label">actividad github</div>

  <div class="xb-contrib">
    <div id="contrib-grid" class="xb-contrib-row"></div>
  </div>
  <p style="font-family:'JetBrains Mono',monospace;font-size:10px;color:#6e6e6e;margin:4px 0 0;text-align:right;">
    github.com/Camilo-Salazar1206
  </p>

</div>

<script>
  const grid = document.getElementById('contrib-grid');
  const colors = ['#0e0e0e','#0d2e0d','#107c10','#52b043','#9bc848'];
  function rng(i){return((i*1103515245+12345)&0x7fffffff)%100;}
  for(let i=0;i<182;i++){
    const v=rng(i+42);
    let c=colors[0];
    if(v>85)c=colors[4];
    else if(v>70)c=colors[3];
    else if(v>50)c=colors[2];
    else if(v>35)c=colors[1];
    const d=document.createElement('div');
    d.className='xb-day';
    d.style.background=c;
    grid.appendChild(d);
  }
</script>
