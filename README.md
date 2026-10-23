<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>VT – Developer ID</title>
<style>
:root{--bg:#eef0f5;--fg:#12141c;--muted:#5b6070;--btn:#12141c;--btnfg:#fff;
box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
@media (prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0b0d13;--fg:#e8eaf2;--muted:#8d93a8;--btn:#e8eaf2;--btnfg:#0b0d13;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#0b0d13;--fg:#e8eaf2;--muted:#8d93a8;--btn:#e8eaf2;--btnfg:#0b0d13;color-scheme:dark}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
*{box-sizing:border-box}
body{margin:0;min-height:100vh;background:var(--bg);color:var(--fg);font-family:Inter,system-ui,-apple-system,"Segoe UI",sans-serif;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:20px;padding:24px 16px}
.scene{perspective:1100px;width:min(320px,86vw);aspect-ratio:320/500}
.tilt{width:100%;height:100%;transform-style:preserve-3d;transition:transform .15s ease-out}
.tilt.rest{transition:transform .6s cubic-bezier(.2,.8,.2,1)}
.flip{width:100%;height:100%;position:relative;transform-style:preserve-3d;transition:transform .8s cubic-bezier(.3,1.2,.4,1);cursor:pointer}
.flip.on{transform:rotateY(180deg)}
.face{position:absolute;inset:0;border-radius:22px;backface-visibility:hidden;-webkit-backface-visibility:hidden;overflow:hidden;color:#f2f4fb;padding:22px;display:flex;flex-direction:column;
background:linear-gradient(155deg,#1b2140,#0e1124 55%,#1a1030);box-shadow:0 24px 50px -18px rgba(0,0,0,.6),inset 0 0 0 1px rgba(255,255,255,.1)}
.back{transform:rotateY(180deg)}
.glare{position:absolute;inset:0;pointer-events:none;border-radius:inherit;background:radial-gradient(circle at var(--gx,50%) var(--gy,0%),rgba(255,255,255,.28),transparent 55%);mix-blend-mode:overlay}
.holo{position:absolute;inset:0;pointer-events:none;opacity:.35;background:linear-gradient(115deg,transparent 20%,rgba(120,220,255,.35),rgba(255,120,220,.3),rgba(255,230,120,.3),transparent 80%);background-size:250% 250%;background-position:var(--hx,50%) 50%;mix-blend-mode:color-dodge}
.top{display:flex;justify-content:space-between;align-items:center;font-size:10px;letter-spacing:.2em;text-transform:uppercase;color:#9aa3c7}
.chip{width:34px;height:26px;border-radius:6px;background:linear-gradient(135deg,#e8c97a,#b88a2e)}
.avatar{margin:26px auto 14px;width:116px;height:116px;border-radius:50%;display:grid;place-items:center;font-size:40px;font-weight:700;letter-spacing:.04em;background:conic-gradient(from 200deg,#5b8cff,#b46bff,#ff6bb0,#5b8cff);position:relative}
.avatar::after{content:"";position:absolute;inset:4px;border-radius:50%;background:#12162b}
.avatar span{position:relative;z-index:1}
h1{margin:0;text-align:center;font-size:26px}
.role{text-align:center;color:#aab3d6;font-size:13px;margin:4px 0 14px}
.tags{display:flex;flex-wrap:wrap;gap:6px;justify-content:center}
.tag{font-size:11px;padding:4px 10px;border-radius:999px;background:rgba(255,255,255,.09);border:1px solid rgba(255,255,255,.12)}
.bar{margin-top:auto;display:flex;align-items:flex-end;justify-content:space-between;gap:12px}
.meta{font-size:10px;color:#8d96bb;line-height:1.6;letter-spacing:.08em}
.meta b{color:#e3e7f8;font-weight:600}
#bars{display:flex;align-items:stretch;height:34px;gap:1.5px;opacity:.85}
#bars i{display:block;background:#e8ebf8}
.hint{position:absolute;bottom:8px;left:0;right:0;text-align:center;font-size:9px;letter-spacing:.2em;color:#6d7699;text-transform:uppercase}
.back h2{margin:6px 0 12px;font-size:13px;letter-spacing:.18em;text-transform:uppercase;color:#9aa3c7;font-weight:600}
.links{display:flex;flex-direction:column;gap:8px}
.links a{display:flex;justify-content:space-between;align-items:center;padding:11px 14px;border-radius:12px;color:#f2f4fb;text-decoration:none;font-size:14px;background:rgba(255,255,255,.07);border:1px solid rgba(255,255,255,.1);transition:background .2s,transform .2s}
.links a:hover,.links a:focus-visible{background:rgba(255,255,255,.16);transform:translateX(4px);outline:none}
.badge{margin-top:auto;margin-bottom:14px;padding:12px;border-radius:12px;font-size:12px;line-height:1.5;text-align:center;background:linear-gradient(135deg,rgba(91,140,255,.25),rgba(180,107,255,.25));border:1px solid rgba(255,255,255,.14)}
.controls{display:flex;gap:10px}
button{font:inherit;font-size:13px;padding:9px 16px;border:0;border-radius:999px;background:var(--btn);color:var(--btnfg);cursor:pointer}
p.note{margin:0;font-size:12px;color:var(--muted)}
@media (prefers-reduced-motion:reduce){.tilt,.flip{transition:none}}
</style>
</head>
<body>
<div class="scene" id="scene">
  <div class="tilt rest" id="tilt">
    <div class="flip" id="flip" role="button" tabindex="0" aria-label="ID card, press to flip">
      <section class="face front">
        <div class="top"><span>Developer ID</span><div class="chip"></div></div>
        <div class="avatar"><span>VT</span></div>
        <h1>VT</h1>
        <div class="role">BSc Mathematics &amp; Statistics</div>
        <div class="tags"><span class="tag">Machine Learning</span><span class="tag">Data Science</span><span class="tag">Quant Finance</span></div>
        <div class="bar">
          <div class="meta">INST <b>QMUL</b><br>CLASS <b>2030</b><br>ID <b id="idn">VT-0000</b></div>
          <div id="bars"></div>
        </div>
        <div class="hint">tap to flip</div>
        <div class="holo"></div><div class="glare"></div>
      </section>
      <section class="face back">
        <div class="top"><span>Find me</span><div class="chip"></div></div>
        <h2 style="margin-top:22px">Links</h2>
        <div class="links">
          <a href="https://github.com/yourusername" target="_blank" rel="noopener">GitHub <span>↗</span></a>
          <a href="https://linkedin.com/in/yourusername" target="_blank" rel="noopener">LinkedIn <span>↗</span></a>
          <a href="https://yourportfolio.dev" target="_blank" rel="noopener">Portfolio <span>↗</span></a>
        </div>
        <div class="badge">Microsoft Learn Student Ambassador<br>Social Media Manager, QMMS</div>
        <div class="hint">tap to flip back</div>
        <div class="holo"></div><div class="glare"></div>
      </section>
    </div>
  </div>
</div>
<div class="controls"><button id="spin">Flip card</button><button id="theme">Toggle theme</button></div>
<p class="note">Drag your cursor (or finger) across the card</p>
<script>
(function(){
  var tilt=document.getElementById('tilt'),flip=document.getElementById('flip'),scene=document.getElementById('scene');
  var reduce=window.matchMedia('(prefers-reduced-motion: reduce)').matches;
  function toggle(){flip.classList.toggle('on')}
  flip.addEventListener('click',function(e){if(e.target.closest('a'))return;toggle()});
  flip.addEventListener('keydown',function(e){if(e.key==='Enter'||e.key===' '){e.preventDefault();toggle()}});
  document.getElementById('spin').addEventListener('click',toggle);
  function move(e){
    if(reduce)return;
    var r=scene.getBoundingClientRect(),x=(e.clientX-r.left)/r.width,y=(e.clientY-r.top)/r.height;
    x=Math.max(0,Math.min(1,x));y=Math.max(0,Math.min(1,y));
    tilt.classList.remove('rest');
    tilt.style.transform='rotateX('+((0.5-y)*22)+'deg) rotateY('+((x-0.5)*22)+'deg)';
    document.querySelectorAll('.face').forEach(function(f){
      f.style.setProperty('--gx',((flip.classList.contains('on')?1-x:x)*100)+'%');
      f.style.setProperty('--gy',(y*100)+'%');
      f.style.setProperty('--hx',(x*100)+'%');
    });
  }
  function rest(){tilt.classList.add('rest');tilt.style.transform=''}
  scene.addEventListener('pointermove',move);
  scene.addEventListener('pointerleave',rest);
  scene.addEventListener('pointerup',function(e){if(e.pointerType==='touch')rest()});
  // barcode
  var seed=2026,bars=document.getElementById('bars');
  function rnd(){seed=(seed*9301+49297)%233280;return seed/233280}
  for(var i=0;i<26;i++){var b=document.createElement('i');b.style.width=(1+Math.floor(rnd()*3))+'px';bars.appendChild(b)}
  document.getElementById('idn').textContent='VT-'+String(Math.floor(1000+rnd()*8999));
  // theme
  var root=document.documentElement;
  document.getElementById('theme').addEventListener('click',function(){
    var dark=root.getAttribute('data-theme')==='dark'||(root.getAttribute('data-theme')!=='light'&&window.matchMedia('(prefers-color-scheme: dark)').matches);
    root.setAttribute('data-theme',dark?'light':'dark');
  });
})();
</script>
</body>
</html>
