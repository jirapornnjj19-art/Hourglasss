
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>FORMA — Your Body, Refined</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,600;0,700;1,400;1,600&family=Jost:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════
   DESIGN TOKENS
═══════════════════════════════════════ */
:root {
  --ink:     #1C1612;
  --bark:    #3A2A20;
  --terr:    #B86B4E;
  --peach:   #E8A882;
  --blush:   #F2D5C4;
  --sand:    #F8F2EC;
  --sage:    #7A9E7E;
  --sage-lt: #C8DECA;
  --mist:    #EAF0EA;
  --white:   #FFFFFF;
  --border:  rgba(58,42,32,0.10);
  --shadow:  0 2px 24px rgba(58,42,32,0.08);
  --radius:  18px;
  --r-sm:    10px;
}

/* ═══════════════════════════════════════
   RESET + BASE
═══════════════════════════════════════ */
*,*::before,*::after{margin:0;padding:0;box-sizing:border-box;}
html{-webkit-text-size-adjust:100%;}
body{
  font-family:'Jost',sans-serif;
  background:var(--sand);
  color:var(--ink);
  font-size:14px;
  line-height:1.65;
  min-height:100vh;
  overflow-x:hidden;
}
button{font-family:'Jost',sans-serif;cursor:pointer;}
input{font-family:'Jost',sans-serif;}
svg{display:block;}

/* ═══════════════════════════════════════
   TOP NAV (desktop)
═══════════════════════════════════════ */
.topnav{
  position:fixed;top:0;left:0;right:0;z-index:200;
  background:rgba(248,242,236,0.94);
  backdrop-filter:blur(16px);
  border-bottom:1px solid var(--border);
  height:58px;display:flex;align-items:center;
  padding:0 24px;gap:0;justify-content:space-between;
}
.topnav-logo{
  font-family:'Playfair Display',serif;
  font-size:20px;font-weight:700;letter-spacing:4px;
  color:var(--terr);
  flex-shrink:0;
}
.topnav-tabs{display:flex;gap:2px;overflow-x:auto;scrollbar-width:none;}
.topnav-tabs::-webkit-scrollbar{display:none;}
.tn-tab{
  padding:6px 15px;border-radius:30px;border:none;
  background:transparent;color:#7A6A60;
  font-size:12.5px;font-weight:500;letter-spacing:0.3px;
  white-space:nowrap;transition:all .2s;
}
.tn-tab.active,.tn-tab:hover{background:var(--terr);color:var(--white);}

/* ═══════════════════════════════════════
   PAGES
═══════════════════════════════════════ */
.page{display:none;padding:74px 18px 100px;max-width:820px;margin:0 auto;}
.page.active{display:block;}

/* ═══════════════════════════════════════
   TYPOGRAPHY
═══════════════════════════════════════ */
.pg-eyebrow{
  font-size:10.5px;letter-spacing:2.5px;font-weight:600;
  color:var(--terr);text-transform:uppercase;margin-bottom:4px;
}
.pg-title{
  font-family:'Playfair Display',serif;
  font-size:28px;font-weight:700;line-height:1.2;
  color:var(--bark);margin-bottom:3px;
}
.pg-sub{font-size:13px;color:#8A7A70;margin-bottom:24px;}

/* ═══════════════════════════════════════
   CARD
═══════════════════════════════════════ */
.card{
  background:var(--white);border:1px solid var(--border);
  border-radius:var(--radius);padding:20px;
  box-shadow:var(--shadow);margin-bottom:14px;
}
.card-label{
  font-size:10px;letter-spacing:2px;font-weight:600;
  color:var(--terr);text-transform:uppercase;margin-bottom:8px;
}
.card-title{
  font-family:'Playfair Display',serif;
  font-size:17px;font-weight:600;margin-bottom:10px;color:var(--bark);
}

/* ═══════════════════════════════════════
   DASHBOARD STATS
═══════════════════════════════════════ */
.stat-strip{
  display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:14px;
}
.stat-box{
  background:var(--white);border:1px solid var(--border);
  border-radius:14px;padding:14px 10px;text-align:center;
}
.stat-val{font-size:21px;font-weight:600;color:var(--terr);line-height:1.1;}
.stat-lbl{font-size:10px;color:#9A8A80;margin-top:3px;letter-spacing:.5px;}
.stat-goal{font-size:9.5px;color:var(--sage);margin-top:2px;}

.prog-wrap{margin-bottom:13px;}
.prog-row{display:flex;justify-content:space-between;font-size:12px;margin-bottom:4px;}
.prog-row strong{color:var(--bark);}
.prog-row span{color:#9A8A80;}
.prog-track{height:7px;background:#F0E8E0;border-radius:100px;overflow:hidden;}
.prog-fill{height:100%;border-radius:100px;background:linear-gradient(90deg,var(--terr),var(--peach));}

.today-strip{
  display:flex;align-items:center;gap:6px;margin-bottom:10px;
}
.today-badge{
  background:var(--terr);color:var(--white);
  padding:3px 12px;border-radius:20px;font-size:11px;font-weight:600;letter-spacing:.5px;
}
.today-day{font-size:12px;color:#9A8A80;}

.ex-preview-row{
  display:flex;align-items:center;gap:12px;
  padding:9px 12px;background:var(--sand);border-radius:10px;margin-bottom:7px;
}
.ex-preview-icon{
  width:36px;height:36px;border-radius:9px;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;
  font-size:17px;
}
.ic-glute{background:linear-gradient(135deg,#F2D5C4,#E8A882);}
.ic-upper{background:linear-gradient(135deg,#C8DECA,#7A9E7E);}
.ic-core{background:linear-gradient(135deg,#D8D0F0,#A898D8);}
.ic-pull{background:linear-gradient(135deg,#C8E0F0,#78A8C8);}
.ic-cardio{background:linear-gradient(135deg,#FFEAB5,#F4C56A);}

.ex-preview-name{flex:1;font-weight:500;font-size:13px;}
.ex-preview-sets{font-size:12px;color:var(--terr);font-weight:600;}

/* ═══════════════════════════════════════
   LOG WIDGET
═══════════════════════════════════════ */
.log-row{display:flex;gap:8px;margin-top:12px;}
.log-inp{
  flex:1;padding:9px 12px;border:1.5px solid var(--border);
  border-radius:10px;font-size:13px;background:var(--sand);color:var(--ink);
  outline:none;transition:border .2s;
}
.log-inp:focus{border-color:var(--terr);}
.log-btn{
  padding:9px 18px;background:var(--terr);color:var(--white);
  border:none;border-radius:10px;font-size:12.5px;font-weight:600;
}
.log-msg{font-size:12px;color:var(--sage);margin-top:8px;min-height:18px;}

/* ═══════════════════════════════════════
   DAY TABS
═══════════════════════════════════════ */
.day-tabs{
  display:flex;gap:7px;overflow-x:auto;padding-bottom:8px;
  margin-bottom:20px;scrollbar-width:none;
}
.day-tabs::-webkit-scrollbar{display:none;}
.day-tab{
  flex-shrink:0;padding:8px 18px;border-radius:24px;
  border:1.5px solid var(--border);background:var(--white);
  color:#8A7A70;font-size:12.5px;font-weight:500;transition:all .2s;
}
.day-tab.active{background:var(--bark);color:var(--white);border-color:var(--bark);}
.day-tab.rest{color:var(--sage);border-color:var(--sage-lt);}
.day-cnt{display:none;}
.day-cnt.active{display:block;}

/* ═══════════════════════════════════════
   EXERCISE CARD (workout page)
═══════════════════════════════════════ */
.ex-card{
  background:var(--white);border:1px solid var(--border);
  border-radius:var(--radius);overflow:hidden;margin-bottom:14px;
  transition:box-shadow .2s;
}
.ex-card:hover{box-shadow:0 8px 36px rgba(184,107,78,.13);}
.ex-card-top{display:flex;gap:14px;padding:18px 18px 14px;}
.ex-illus{
  width:88px;height:88px;border-radius:12px;flex-shrink:0;
  display:flex;align-items:center;justify-content:center;
  overflow:hidden;position:relative;
}
.ex-illus.c-glute{background:linear-gradient(135deg,#F5D5C0,#EAA080);}
.ex-illus.c-upper{background:linear-gradient(135deg,#CCE8C8,#88B888);}
.ex-illus.c-core{background:linear-gradient(135deg,#D8D0F8,#9888D0);}
.ex-illus.c-pull{background:linear-gradient(135deg,#C0D8F0,#6898C0);}
.ex-illus.c-shoulder{background:linear-gradient(135deg,#E8E0F0,#B0A0D0);}
.ex-illus svg{width:72px;height:72px;}

.ex-meta h3{font-size:15px;font-weight:600;margin-bottom:5px;color:var(--bark);}
.tag-row{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:5px;}
.tag{padding:2px 10px;border-radius:20px;font-size:10.5px;font-weight:600;}
.tag-sets{background:#FFF0EB;color:var(--terr);}
.tag-muscle{background:var(--mist);color:#4A7A4E;}
.tag-mand{background:#FEF9E0;color:#8A6800;border:1px solid #F4D060;}

.ex-cue{
  margin:0 18px 18px;
  background:linear-gradient(135deg,#FFF8F5,#FFF2EB);
  border-left:3px solid var(--terr);
  border-radius:0 10px 10px 0;
  padding:10px 14px;font-size:12.5px;line-height:1.6;color:var(--bark);
}
.ex-cue strong{color:var(--terr);}

.rest-pill{
  display:inline-flex;align-items:center;gap:5px;
  background:var(--mist);color:var(--sage);
  padding:4px 12px;border-radius:20px;font-size:11px;font-weight:600;
  margin:0 18px 16px;
}

/* ═══════════════════════════════════════
   SVG FIGURES  (stick figure illustrations)
═══════════════════════════════════════ */
/* inline via JS */

/* ═══════════════════════════════════════
   LIBRARY GRID
═══════════════════════════════════════ */
.lib-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;}
.lib-card{
  background:var(--white);border:1px solid var(--border);border-radius:16px;
  overflow:hidden;cursor:pointer;transition:all .2s;
}
.lib-card:hover{transform:translateY(-3px);box-shadow:var(--shadow);}
.lib-thumb{
  height:110px;display:flex;align-items:center;justify-content:center;
  position:relative;overflow:hidden;
}
.lib-thumb svg{width:90px;height:90px;}
.lib-info{padding:12px 14px;}
.lib-name{font-weight:600;font-size:13px;margin-bottom:3px;color:var(--bark);}
.lib-muscle{font-size:11px;color:#9A8A80;}
.lib-mand-dot{
  position:absolute;top:8px;right:8px;
  background:var(--terr);color:white;
  font-size:9px;font-weight:700;padding:2px 7px;border-radius:10px;
  letter-spacing:.5px;
}

.lib-detail{display:none;}
.lib-detail.active{display:block;}
.back-btn{
  display:inline-flex;align-items:center;gap:6px;
  padding:8px 16px;border-radius:20px;border:1.5px solid var(--border);
  background:var(--white);color:#8A7A70;font-size:12.5px;
  margin-bottom:18px;transition:all .2s;
}
.back-btn:hover{border-color:var(--terr);color:var(--terr);}

.muscle-chips{display:flex;flex-wrap:wrap;gap:6px;margin:10px 0 16px;}
.m-chip{padding:4px 12px;border-radius:20px;font-size:11.5px;font-weight:500;}
.m-chip.pri{background:#FFF0EB;color:var(--terr);}
.m-chip.sec{background:var(--mist);color:#4A7A4E;}

.steps-ol{list-style:none;counter-reset:st;}
.steps-ol li{
  counter-increment:st;display:flex;gap:12px;
  padding:10px 0;border-bottom:1px solid var(--border);
  font-size:13px;color:var(--bark);
}
.steps-ol li::before{
  content:counter(st);min-width:26px;height:26px;
  background:var(--terr);color:white;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  font-size:11px;font-weight:700;flex-shrink:0;
}

/* ═══════════════════════════════════════
   CARDIO
═══════════════════════════════════════ */
.cardio-hero{
  background:linear-gradient(135deg,var(--bark),#5A3828);
  border-radius:22px;padding:28px;color:var(--white);margin-bottom:14px;
  position:relative;overflow:hidden;
}
.cardio-hero::after{
  content:'';position:absolute;
  right:-50px;top:-50px;width:200px;height:200px;border-radius:50%;
  background:rgba(232,168,130,.1);
}
.cardio-hero h3{
  font-family:'Playfair Display',serif;font-size:20px;
  margin-bottom:20px;color:var(--peach);
}
.cardio-metrics{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-bottom:20px;}
.cm-val{font-size:30px;font-weight:300;color:var(--blush);}
.cm-unit{font-size:11px;opacity:.65;}
.cm-lbl{font-size:12px;margin-top:4px;opacity:.8;}
.cardio-tips{font-size:12.5px;opacity:.85;line-height:1.8;}

.phase-grid{display:grid;grid-template-columns:repeat(2,1fr);gap:10px;}
.phase-box{
  background:var(--white);border:1px solid var(--border);
  border-radius:14px;padding:14px;
}
.phase-tag{font-size:9.5px;color:var(--terr);font-weight:700;letter-spacing:1px;margin-bottom:4px;}
.phase-h{font-weight:600;font-size:13px;margin-bottom:5px;color:var(--bark);}
.phase-p{font-size:12px;color:#8A7A70;line-height:1.5;}

/* ═══════════════════════════════════════
   NUTRITION
═══════════════════════════════════════ */
.macro-bar-card{
  background:var(--white);border:1px solid var(--border);
  border-radius:var(--radius);padding:20px;margin-bottom:14px;
}
.macro-visual{
  display:flex;height:16px;border-radius:100px;overflow:hidden;gap:2px;margin:12px 0;
}
.mv-p{flex:35;background:var(--terr);}
.mv-c{flex:40;background:var(--sage);}
.mv-f{flex:25;background:var(--peach);}
.macro-legend{display:flex;gap:16px;flex-wrap:wrap;}
.ml-dot{width:10px;height:10px;border-radius:50%;display:inline-block;margin-right:6px;}
.ml-item{display:flex;align-items:center;font-size:12.5px;}
.ml-val{font-weight:600;margin-left:4px;color:var(--bark);}

.timing-row{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:14px;}
.t-card{
  background:var(--white);border:1px solid var(--border);border-radius:14px;
  padding:13px;text-align:center;
}
.t-icon{font-size:22px;margin-bottom:5px;}
.t-when{font-size:9.5px;color:var(--terr);font-weight:700;letter-spacing:.5px;margin-bottom:3px;}
.t-title{font-size:12.5px;font-weight:600;margin-bottom:3px;color:var(--bark);}
.t-desc{font-size:11px;color:#9A8A80;line-height:1.4;}

.meal-list{display:flex;flex-direction:column;gap:10px;}
.meal-row{
  display:flex;align-items:center;gap:12px;
  background:var(--white);border:1px solid var(--border);border-radius:14px;padding:13px 16px;
}
.meal-em{font-size:26px;flex-shrink:0;}
.meal-body h4{font-size:13px;font-weight:600;margin-bottom:2px;color:var(--bark);}
.meal-body p{font-size:11.5px;color:#9A8A80;}
.meal-macros{margin-left:auto;text-align:right;flex-shrink:0;}
.meal-macros b{display:block;font-size:12px;color:var(--terr);font-weight:600;}
.meal-macros small{font-size:10.5px;color:#9A8A80;}

/* ═══════════════════════════════════════
   CYCLE MODE
═══════════════════════════════════════ */
.phase-cards-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-bottom:16px;}
.cyc-card{border-radius:18px;padding:18px;}
.cyc-card.follicular{background:linear-gradient(135deg,#FFF0EB,#F5D0C0);border:1px solid #E8BBA8;}
.cyc-card.ovulation{background:linear-gradient(135deg,#FFF8E0,#FFE4A8);border:1px solid #F4C86A;}
.cyc-card.luteal{background:linear-gradient(135deg,#F0EEF8,#D8D0F0);border:1px solid #C0B4E0;}
.cyc-card.menstrual{background:linear-gradient(135deg,#F4F4F4,#E8E8E8);border:1px solid #D0D0D0;}
.cyc-phase{font-family:'Playfair Display',serif;font-size:16px;font-weight:600;margin-bottom:2px;}
.cyc-days{font-size:10.5px;opacity:.65;margin-bottom:8px;}
.cyc-int{
  display:inline-block;padding:2px 10px;border-radius:20px;
  font-size:9.5px;font-weight:700;letter-spacing:.5px;margin-bottom:8px;
}
.int-high{background:var(--terr);color:white;}
.int-mod{background:#F4C86A;color:#5A4000;}
.int-low{background:#C0B4E0;color:#3A2A5A;}
.int-rest{background:#C8C8C8;color:#484848;}
.cyc-tips{list-style:none;}
.cyc-tips li{font-size:11.5px;padding:2px 0;opacity:.85;}
.cyc-tips li::before{content:'→ ';color:var(--terr);}

.phase-sel-row{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:16px;}
.psel-btn{
  padding:7px 16px;border-radius:20px;border:1.5px solid var(--border);
  background:var(--white);color:#8A7A70;font-size:12px;font-weight:500;transition:all .2s;
}
.psel-btn.active{background:var(--terr);color:white;border-color:var(--terr);}
.cyc-workout{display:none;}
.cyc-workout.active{display:block;}

/* ═══════════════════════════════════════
   BOTTOM NAV (mobile)
═══════════════════════════════════════ */
.botnav{
  display:none;position:fixed;bottom:0;left:0;right:0;
  background:rgba(255,255,255,0.97);
  border-top:1px solid var(--border);
  padding:6px 0 env(safe-area-inset-bottom,6px);z-index:200;
}
.botnav-inner{display:flex;justify-content:space-around;}
.bn-b{
  display:flex;flex-direction:column;align-items:center;gap:2px;
  background:none;border:none;color:#9A8A80;
  font-size:9.5px;font-weight:500;padding:4px 8px;border-radius:12px;
  transition:color .2s;
}
.bn-b.active{color:var(--terr);}
.bn-icon{font-size:21px;line-height:1;}

/* ═══════════════════════════════════════
   ANIMATIONS
═══════════════════════════════════════ */
@keyframes fadeUp{from{opacity:0;transform:translateY(18px);}to{opacity:1;transform:translateY(0);}}
.page.active .card,
.page.active .ex-card,
.page.active .lib-card,
.page.active .cyc-card,
.page.active .stat-box{animation:fadeUp .38s ease both;}
.page.active .stat-box:nth-child(2){animation-delay:.04s;}
.page.active .stat-box:nth-child(3){animation-delay:.08s;}
.page.active .stat-box:nth-child(4){animation-delay:.04s;}
.page.active .stat-box:nth-child(5){animation-delay:.08s;}
.page.active .stat-box:nth-child(6){animation-delay:.12s;}
.page.active .card:nth-child(2){animation-delay:.06s;}
.page.active .card:nth-child(3){animation-delay:.12s;}
.page.active .card:nth-child(4){animation-delay:.18s;}

/* ═══════════════════════════════════════
   RESPONSIVE
═══════════════════════════════════════ */
@media(max-width:600px){
  .topnav{display:none;}
  .botnav{display:block;}
  .page{padding:16px 15px 90px;}
  .phase-cards-grid{grid-template-columns:1fr 1fr;}
  .lib-grid{grid-template-columns:repeat(2,1fr);}
  .phase-grid{grid-template-columns:1fr;}
}
@media(min-width:601px){.botnav{display:none;}}

/* ═══════════════════════════════════════
   UTILITY
═══════════════════════════════════════ */
.divider{height:1px;background:var(--border);margin:16px 0;}
.tip-pill{
  display:inline-flex;align-items:center;gap:5px;
  background:var(--mist);color:var(--sage);
  padding:5px 13px;border-radius:20px;font-size:12px;font-weight:500;
  margin-bottom:12px;
}
.mand-banner{
  background:linear-gradient(135deg,#FEF9E0,#FFF3BE);
  border:1px solid #F0D060;border-radius:12px;
  padding:8px 14px;font-size:11.5px;color:#7A6000;margin-bottom:14px;
  display:flex;align-items:center;gap:7px;
}
</style>
</head>
<body>

<!-- ════════════════════════
     TOP NAV
════════════════════════ -->
<nav class="topnav">
  <div class="topnav-logo">FORMA</div>
  <div class="topnav-tabs">
    <button class="tn-tab active" onclick="showPage('dash',this)">Dashboard</button>
    <button class="tn-tab" onclick="showPage('plan',this)">Workout Plan</button>
    <button class="tn-tab" onclick="showPage('lib',this)">Exercise Library</button>
    <button class="tn-tab" onclick="showPage('cardio',this)">Cardio</button>
    <button class="tn-tab" onclick="showPage('nutrition',this)">Nutrition</button>
    <button class="tn-tab" onclick="showPage('cycle',this)">Cycle Mode</button>
  </div>
</nav>

<!-- ══════════════════════════════════════════════
     PAGE 1 — DASHBOARD
══════════════════════════════════════════════ -->
<div id="dash" class="page active">
  <div class="pg-eyebrow">Welcome back 🌸</div>
  <h1 class="pg-title">Your Dashboard</h1>
  <p class="pg-sub">Hourglass Program · Week 1 · Track. Train. Transform.</p>

  <div class="stat-strip">
    <div class="stat-box"><div class="stat-val">56.4</div><div class="stat-lbl">WEIGHT kg</div></div>
    <div class="stat-box"><div class="stat-val">30.4%</div><div class="stat-lbl">BODY FAT</div><div class="stat-goal">goal 22%</div></div>
    <div class="stat-box"><div class="stat-val">27"</div><div class="stat-lbl">WAIST</div><div class="stat-goal">goal 24"</div></div>
    <div class="stat-box"><div class="stat-val">27.3%</div><div class="stat-lbl">MUSCLE</div><div class="stat-goal">goal 32%</div></div>
    <div class="stat-box"><div class="stat-val">37.5"</div><div class="stat-lbl">HIPS</div><div class="stat-goal">keep ≥36"</div></div>
    <div class="stat-box"><div class="stat-val">4</div><div class="stat-lbl">VISCERAL</div><div class="stat-goal">goal 1</div></div>
  </div>

  <div class="card">
    <div class="card-label">Body Composition Progress</div>
    <div class="prog-wrap">
      <div class="prog-row"><strong>Body Fat</strong><span>30.4% → 22%</span></div>
      <div class="prog-track"><div class="prog-fill" style="width:9%"></div></div>
    </div>
    <div class="prog-wrap">
      <div class="prog-row"><strong>Waist</strong><span>27" → 24"</span></div>
      <div class="prog-track"><div class="prog-fill" style="width:6%"></div></div>
    </div>
    <div class="prog-wrap">
      <div class="prog-row"><strong>Muscle Mass</strong><span>27.3% → 32%</span></div>
      <div class="prog-track"><div class="prog-fill" style="width:8%"></div></div>
    </div>
    <div class="prog-wrap" style="margin-bottom:0">
      <div class="prog-row"><strong>Body Age</strong><span>32 → 18</span></div>
      <div class="prog-track"><div class="prog-fill" style="width:5%"></div></div>
    </div>
  </div>

  <div class="card">
    <div class="today-strip">
      <div class="today-badge">TODAY · DAY 1</div>
      <div class="today-day">Glute Focus + Lower Body</div>
    </div>
    <div class="ex-preview-row">
      <div class="ex-preview-icon ic-glute">🍑</div>
      <div class="ex-preview-name">Hip Thrusts (Smith Machine)</div>
      <div class="ex-preview-sets">4×12</div>
    </div>
    <div class="ex-preview-row">
      <div class="ex-preview-icon ic-glute">🦵</div>
      <div class="ex-preview-name">Leg Press (High Foot)</div>
      <div class="ex-preview-sets">4×15</div>
    </div>
    <div class="ex-preview-row">
      <div class="ex-preview-icon ic-glute">💎</div>
      <div class="ex-preview-name">Romanian Deadlift</div>
      <div class="ex-preview-sets">3×12</div>
    </div>
    <div class="ex-preview-row">
      <div class="ex-preview-icon ic-core">🌀</div>
      <div class="ex-preview-name">Hyperextension (Roman Chair)</div>
      <div class="ex-preview-sets">3×15</div>
    </div>
    <div class="ex-preview-row">
      <div class="ex-preview-icon ic-cardio">🚶</div>
      <div class="ex-preview-name">Incline Walk (Post-Workout)</div>
      <div class="ex-preview-sets">30 min</div>
    </div>
  </div>

  <div class="card">
    <div class="card-label">Log Today</div>
    <div class="log-row">
      <input type="number" class="log-inp" id="wInput" placeholder="Weight (kg)">
      <input type="text" class="log-inp" id="waistIn" placeholder="Waist (inches)">
      <button class="log-btn" onclick="logIt()">Save</button>
    </div>
    <div class="log-msg" id="logMsg"></div>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     PAGE 2 — WORKOUT PLAN
══════════════════════════════════════════════ -->
<div id="plan" class="page">
  <div class="pg-eyebrow">4-Day Program</div>
  <h1 class="pg-title">Weekly Workout Plan</h1>
  <p class="pg-sub">Hourglass · Fat Loss · Glute Build Priority</p>

  <div class="mand-banner">⭐ <strong>Gold exercises</strong> = Mandatory exercises from your program list</div>

  <div class="day-tabs">
    <button class="day-tab active" onclick="showDay('d1',this)">Day 1 🍑</button>
    <button class="day-tab" onclick="showDay('d2',this)">Day 2 💪</button>
    <button class="day-tab" onclick="showDay('d3',this)">Day 3 🔥</button>
    <button class="day-tab" onclick="showDay('d4',this)">Day 4 ⭐</button>
    <button class="day-tab rest" onclick="showDay('d5',this)">Rest 🌸</button>
  </div>

  <!-- ── DAY 1 : GLUTE + LOWER ── -->
  <div id="d1" class="day-cnt active">
    <div class="tip-pill">🍑 Glutes + Lower Body — Priority Day</div>

    <!-- Hip Thrust -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-ht-plan"></div>
        <div class="ex-meta">
          <h3>Hip Thrusts</h3>
          <div class="tag-row">
            <span class="tag tag-sets">4 Sets × 12 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Glutes Max</span>
            <span class="tag tag-muscle">Hamstrings</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Drive through heels, squeeze glutes HARD at top — hold 1 sec. Chin tucked, ribs down. Bar on hip crease with pad. Don't hyperextend lower back.</div>
      <div class="rest-pill">⏱ 90 sec rest</div>
    </div>

    <!-- Leg Press -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-lp-plan"></div>
        <div class="ex-meta">
          <h3>Leg Press (High Foot)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">4 Sets × 15 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Glutes</span>
            <span class="tag tag-muscle">Hamstrings</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Feet HIGH on platform, hip-width. Press through heels, not toes. Lower 3 sec, press powerfully. Never lock knees at top.</div>
      <div class="rest-pill">⏱ 90 sec rest</div>
    </div>

    <!-- RDL -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-rdl-plan"></div>
        <div class="ex-meta">
          <h3>Romanian Deadlift (RDL)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">3 Sets × 12 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Hamstrings</span>
            <span class="tag tag-muscle">Glutes</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Push hips BACKWARD — not knees down. Keep dumbbells close to shins. Feel hamstring stretch. Drive hips forward to stand, squeeze glutes at top.</div>
      <div class="rest-pill">⏱ 75 sec rest</div>
    </div>

    <!-- Hyperextension -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-hyp-plan"></div>
        <div class="ex-meta">
          <h3>Hyperextension (Roman Chair)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">3 Sets × 15 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Glutes</span>
            <span class="tag tag-muscle">Lower Back</span>
            <span class="tag tag-muscle">Hamstrings</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Hips at the pad edge. Lower torso slowly, then raise to parallel — not hyperextended. Squeeze glutes at top. Cross arms on chest or hold plate for added challenge.</div>
      <div class="rest-pill">⏱ 60 sec rest</div>
    </div>
  </div>

  <!-- ── DAY 2 : UPPER BODY + SHOULDERS ── -->
  <div id="d2" class="day-cnt">
    <div class="tip-pill">💪 Upper Body — Shoulders + Back + Chest</div>

    <!-- Shoulder Press -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-shoulder" id="ill-sp-plan"></div>
        <div class="ex-meta">
          <h3>Shoulder Press (Dumbbells)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">4 Sets × 10 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Anterior Delt</span>
            <span class="tag tag-muscle">Medial Delt</span>
            <span class="tag tag-muscle">Triceps</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Sit tall, core braced. Press dumbbells straight up — don't flare elbows too wide. Lower to ear level with control (2 sec). Wider shoulders = smaller-looking waist!</div>
      <div class="rest-pill">⏱ 90 sec rest</div>
    </div>

    <!-- Lateral Raise -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-shoulder" id="ill-lr-plan"></div>
        <div class="ex-meta">
          <h3>Lateral Raise (Dumbbells)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">4 Sets × 15 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Medial Delt</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Slight forward lean, lead with elbows. Raise to shoulder height — pinky slightly higher. Lower SLOWLY (3 sec). No swinging! This builds the shoulder width that creates your hourglass.</div>
      <div class="rest-pill">⏱ 60 sec rest</div>
    </div>

    <!-- Overhead Raise -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-shoulder" id="ill-ovh-plan"></div>
        <div class="ex-meta">
          <h3>Overhead Raise (Front Raise)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">3 Sets × 12 Reps</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Anterior Delt</span>
            <span class="tag tag-muscle">Upper Chest</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Hold dumbbells in front of thighs. Raise arms straight forward to shoulder height (thumbs up). Don't swing. Control the lowering phase (3 sec). Builds front shoulder for a rounded 3D look.</div>
      <div class="rest-pill">⏱ 60 sec rest</div>
    </div>

    <!-- External Rotation -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-upper" id="ill-er-plan"></div>
        <div class="ex-meta">
          <h3>External Rotation (Shoulder Stability)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">3 Sets × 15 Reps each</span>
            <span class="tag tag-mand">⭐ Mandatory</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Infraspinatus</span>
            <span class="tag tag-muscle">Rear Delt</span>
            <span class="tag tag-muscle">Rotator Cuff</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Lie on side or stand, elbow tucked at 90°. Rotate forearm outward against light dumbbell or cable. Slow and controlled. Essential for shoulder health and injury prevention — do this every upper day.</div>
      <div class="rest-pill">⏱ 45 sec rest</div>
    </div>

    <!-- Lat Pulldown -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-pull" id="ill-lpd-plan"></div>
        <div class="ex-meta">
          <h3>Lat Pulldown (Wide Grip)</h3>
          <div class="tag-row">
            <span class="tag tag-sets">4 Sets × 12 Reps</span>
          </div>
          <div class="tag-row">
            <span class="tag tag-muscle">Lats</span>
            <span class="tag tag-muscle">Rear Delts</span>
            <span class="tag tag-muscle">Biceps</span>
          </div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Lean back 15°. Pull bar to upper chest driving elbows DOWN and BACK. Squeeze shoulder blades. Slow 3-sec release. V-taper makes waist appear much smaller!</div>
      <div class="rest-pill">⏱ 90 sec rest</div>
    </div>
  </div>

  <!-- ── DAY 3 : CORE + WAIST ── -->
  <div id="d3" class="day-cnt">
    <div class="tip-pill">🔥 Core Sculpt + Waist Cinch</div>

    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-core" id="ill-obliq-plan"></div>
        <div class="ex-meta">
          <h3>Roman Chair Oblique Crunches</h3>
          <div class="tag-row"><span class="tag tag-sets">4 Sets × 20 Reps</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Obliques</span><span class="tag tag-muscle">Core</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> On hyperextension bench, bend sideways from the hips. Pure lateral crunch — no rotation. Hold the stretch at bottom, crunch hard at top. Carves the waist from both sides.</div>
      <div class="rest-pill">⏱ 60 sec rest</div>
    </div>

    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-core" id="ill-plank-plan"></div>
        <div class="ex-meta">
          <h3>Plank with Hip Dips</h3>
          <div class="tag-row"><span class="tag tag-sets">3 Sets × 40 sec</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Deep Core</span><span class="tag tag-muscle">Obliques</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Forearm plank position. Dip hips 2–3 inches each side in controlled reps. Breathe steadily. Activates the transverse abdominis — your internal waist-cinching corset.</div>
      <div class="rest-pill">⏱ 60 sec rest</div>
    </div>

    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-core" id="ill-lraise-plan"></div>
        <div class="ex-meta">
          <h3>Hanging Knee Raises</h3>
          <div class="tag-row"><span class="tag tag-sets">3 Sets × 12 Reps</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Lower Abs</span><span class="tag tag-muscle">Hip Flexors</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Hang from lat pulldown bar. Raise knees to chest — exhale on the way up. No swinging. Lower with control. Targets the lower belly region most effectively.</div>
      <div class="rest-pill">⏱ 60 sec rest</div>
    </div>

    <!-- Shoulder stability day 3 (light) -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-shoulder" id="ill-er2-plan"></div>
        <div class="ex-meta">
          <h3>External Rotation (Maintenance)</h3>
          <div class="tag-row"><span class="tag tag-sets">2 Sets × 15 Reps</span><span class="tag tag-mand">⭐ Mandatory</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Rotator Cuff</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Light band or dumbbell. Shoulder stability maintenance set. Keep these light and perfect form always. This is injury prevention — don't skip it.</div>
      <div class="rest-pill">⏱ 30 sec rest</div>
    </div>
  </div>

  <!-- ── DAY 4 : FULL GLUTE ROUND 2 ── -->
  <div id="d4" class="day-cnt">
    <div class="tip-pill">⭐ Glute Round 2 + All Mandatory Finishers</div>

    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-bss-plan"></div>
        <div class="ex-meta">
          <h3>Bulgarian Split Squat (Smith)</h3>
          <div class="tag-row"><span class="tag tag-sets">4 Sets × 10 Reps each</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Glutes</span><span class="tag tag-muscle">Quads</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Rear foot on bench. Drop straight down — lean torso slightly forward to bias glutes. Drive through front heel. This is the queen of unilateral glute exercises.</div>
      <div class="rest-pill">⏱ 90 sec rest</div>
    </div>

    <!-- Hip Thrust again (frequency matters) -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-ht2-plan"></div>
        <div class="ex-meta">
          <h3>Hip Thrusts (Pause Rep)</h3>
          <div class="tag-row"><span class="tag tag-sets">4 Sets × 10 Reps</span><span class="tag tag-mand">⭐ Mandatory</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Glutes Max</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Same as Day 1 but ADD a 2-second pause at the top each rep. This increases time under tension for maximum glute growth. Go slightly lighter than Day 1.</div>
      <div class="rest-pill">⏱ 90 sec rest</div>
    </div>

    <!-- Hyperextension -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-glute" id="ill-hyp2-plan"></div>
        <div class="ex-meta">
          <h3>Hyperextension — Weighted</h3>
          <div class="tag-row"><span class="tag tag-sets">3 Sets × 12 Reps</span><span class="tag tag-mand">⭐ Mandatory</span></div>
          <div class="tag-row"><span class="tag tag-muscle">Lower Back</span><span class="tag tag-muscle">Glutes</span><span class="tag tag-muscle">Hamstrings</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Hold a weight plate or dumbbell to chest. Same mechanics — hips at pad, raise to parallel only. The added load builds posterior chain strength that supports all glute work.</div>
      <div class="rest-pill">⏱ 75 sec rest</div>
    </div>

    <!-- Shoulder Press finisher -->
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus c-shoulder" id="ill-sp2-plan"></div>
        <div class="ex-meta">
          <h3>Arnold Press (Shoulder Finisher)</h3>
          <div class="tag-row"><span class="tag tag-sets">3 Sets × 12 Reps</span><span class="tag tag-mand">⭐ Mandatory</span></div>
          <div class="tag-row"><span class="tag tag-muscle">All 3 Delt Heads</span><span class="tag tag-muscle">Triceps</span></div>
        </div>
      </div>
      <div class="ex-cue"><strong>Form Cue:</strong> Start with palms facing you, elbows at chest. As you press up, rotate palms forward. Full shoulder coverage. Slow and controlled. Builds that full, rounded shoulder shape.</div>
      <div class="rest-pill">⏱ 75 sec rest</div>
    </div>
  </div>

  <!-- REST DAY -->
  <div id="d5" class="day-cnt">
    <div class="card" style="text-align:center;padding:40px 20px;">
      <div style="font-size:52px;margin-bottom:14px;">🌸</div>
      <div class="card-title" style="font-size:22px;margin-bottom:8px;">Active Recovery</div>
      <p style="color:#9A8A80;font-size:13px;max-width:280px;margin:0 auto 22px;">Rest is where your muscles actually GROW. Protect today like you protect your training.</p>
      <div style="text-align:left;display:inline-block;">
        <div class="ex-preview-row" style="margin-bottom:8px;"><div class="ex-preview-icon ic-cardio">🧘</div><div class="ex-preview-name">Yoga or gentle stretching — 20 min</div></div>
        <div class="ex-preview-row" style="margin-bottom:8px;"><div class="ex-preview-icon ic-cardio">🚶</div><div class="ex-preview-name">Leisurely flat walk — 20–30 min</div></div>
        <div class="ex-preview-row" style="margin-bottom:8px;"><div class="ex-preview-icon ic-core">💆</div><div class="ex-preview-name">Foam roll: glutes, hamstrings, lats</div></div>
        <div class="ex-preview-row"><div class="ex-preview-icon ic-cardio">💧</div><div class="ex-preview-name">Hydrate — aim for 2.5L water</div></div>
      </div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     PAGE 3 — EXERCISE LIBRARY
══════════════════════════════════════════════ -->
<div id="lib" class="page">
  <div class="pg-eyebrow">Reference Guide</div>
  <h1 class="pg-title">Exercise Library</h1>
  <p class="pg-sub">⭐ = Mandatory exercises in your program</p>

  <div id="lib-grid">
    <div class="lib-grid">
      <div class="lib-card" onclick="libShow('hipthrust')">
        <div class="lib-thumb c-glute" id="lt-ht"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Hip Thrusts</div><div class="lib-muscle">Glutes Max · Priority</div></div>
      </div>
      <div class="lib-card" onclick="libShow('rdl')">
        <div class="lib-thumb c-glute" id="lt-rdl"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Romanian Deadlift</div><div class="lib-muscle">Hamstrings · Glutes</div></div>
      </div>
      <div class="lib-card" onclick="libShow('legpress')">
        <div class="lib-thumb c-glute" id="lt-lp"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Leg Press</div><div class="lib-muscle">Glutes · Quads · Hams</div></div>
      </div>
      <div class="lib-card" onclick="libShow('hyperext')">
        <div class="lib-thumb c-glute" id="lt-hyp"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Hyperextension</div><div class="lib-muscle">Glutes · Lower Back</div></div>
      </div>
      <div class="lib-card" onclick="libShow('overheadraise')">
        <div class="lib-thumb c-shoulder" id="lt-ovh"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Overhead Raise</div><div class="lib-muscle">Anterior Delt · Upper Chest</div></div>
      </div>
      <div class="lib-card" onclick="libShow('extrotation')">
        <div class="lib-thumb c-upper" id="lt-er"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">External Rotation</div><div class="lib-muscle">Rotator Cuff · Rear Delt</div></div>
      </div>
      <div class="lib-card" onclick="libShow('shoulderpress')">
        <div class="lib-thumb c-shoulder" id="lt-sp"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Shoulder Press</div><div class="lib-muscle">All Delts · Triceps</div></div>
      </div>
      <div class="lib-card" onclick="libShow('lateralraise')">
        <div class="lib-thumb c-shoulder" id="lt-lr"><div class="lib-mand-dot">⭐ MUST</div></div>
        <div class="lib-info"><div class="lib-name">Lateral Raise</div><div class="lib-muscle">Medial Delt · Hourglass</div></div>
      </div>
    </div>
  </div>

  <div id="lib-detail" class="lib-detail">
    <button class="back-btn" onclick="libHide()">← Back to Library</button>
    <div id="lib-detail-content"></div>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     PAGE 4 — CARDIO
══════════════════════════════════════════════ -->
<div id="cardio" class="page">
  <div class="pg-eyebrow">Daily Protocol</div>
  <h1 class="pg-title">Cardio Plan</h1>
  <p class="pg-sub">Incline walking — fat loss without muscle loss</p>

  <div class="cardio-hero">
    <h3>Daily Incline Walk 🚶‍♀️</h3>
    <div class="cardio-metrics">
      <div><div class="cm-val">10–12</div><div class="cm-unit">%</div><div class="cm-lbl">Incline</div></div>
      <div><div class="cm-val">5.5</div><div class="cm-unit">km/h</div><div class="cm-lbl">Speed</div></div>
      <div><div class="cm-val">30</div><div class="cm-unit">min</div><div class="cm-lbl">Duration</div></div>
    </div>
    <div class="cardio-tips">
      ✓ Always AFTER strength training — not before<br>
      ✓ Don't hold the handrails (posture + calorie burn)<br>
      ✓ Engages glutes — builds that shape while burning fat<br>
      ✓ Targets visceral fat — reduce waist measurement
    </div>
  </div>

  <div class="card">
    <div class="card-label">Treadmill Phase Protocol</div>
    <div class="phase-grid">
      <div class="phase-box"><div class="phase-tag">WARM-UP · 5 MIN</div><div class="phase-h">Easy Walk</div><div class="phase-p">5% incline · 4.5 km/h. Prepare hips and calves.</div></div>
      <div class="phase-box"><div class="phase-tag">MAIN · 20 MIN</div><div class="phase-h">Fat Burn Zone</div><div class="phase-p">10–12% incline · 5.5 km/h. Stay at 60–70% max HR.</div></div>
      <div class="phase-box"><div class="phase-tag">PUSH · 5 MIN</div><div class="phase-h">Glute Activator</div><div class="phase-p">15% incline · 5 km/h. Feel those glutes fire!</div></div>
      <div class="phase-box"><div class="phase-tag">COOL-DOWN · 5 MIN</div><div class="phase-h">Recovery Walk</div><div class="phase-p">Flat · 4 km/h. Heart rate recovery.</div></div>
    </div>
  </div>

  <div class="card">
    <div class="card-label">Heart Rate Target Zones</div>
    <div class="prog-wrap">
      <div class="prog-row"><strong>🟢 Fat Burn (60–70%)</strong><span>114–133 BPM</span></div>
      <div class="prog-track"><div class="prog-fill" style="width:65%;background:linear-gradient(90deg,var(--sage),var(--sage-lt))"></div></div>
    </div>
    <div class="prog-wrap" style="margin-bottom:0">
      <div class="prog-row"><strong>🟡 Cardio Zone (70–80%)</strong><span>133–152 BPM</span></div>
      <div class="prog-track"><div class="prog-fill" style="width:75%"></div></div>
    </div>
    <p style="font-size:11.5px;color:#9A8A80;margin-top:10px;">Stay in the green fat-burn zone for incline walks. This preserves muscle while maximising fat oxidation.</p>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     PAGE 5 — NUTRITION
══════════════════════════════════════════════ -->
<div id="nutrition" class="page">
  <div class="pg-eyebrow">Fuel Your Body</div>
  <h1 class="pg-title">Nutrition Plan</h1>
  <p class="pg-sub">Flexible, sustainable · ~1,450 kcal · High protein</p>

  <div class="macro-bar-card">
    <div class="card-label">Daily Macros</div>
    <div class="macro-visual">
      <div class="mv-p"></div><div class="mv-c"></div><div class="mv-f"></div>
    </div>
    <div class="macro-legend">
      <div class="ml-item"><span class="ml-dot" style="background:var(--terr)"></span>Protein<span class="ml-val">115–120g</span></div>
      <div class="ml-item"><span class="ml-dot" style="background:var(--sage)"></span>Carbs<span class="ml-val">145–160g</span></div>
      <div class="ml-item"><span class="ml-dot" style="background:var(--peach)"></span>Fat<span class="ml-val">45–50g</span></div>
    </div>
    <div class="divider"></div>
    <p style="font-size:12.5px;color:#8A7A70;line-height:1.7;">
      🥩 <strong>Protein</strong>: ~2g per kg of bodyweight. Every meal = palm-size protein source.<br>
      🍚 <strong>Carbs</strong>: Timing matters — most carbs around workouts.<br>
      🥑 <strong>Fat</strong>: Healthy fats for hormones. Avocado, olive oil, salmon, nuts.
    </p>
  </div>

  <div class="card">
    <div class="card-label">Carb Timing Strategy</div>
    <div class="timing-row">
      <div class="t-card"><div class="t-icon">🌅</div><div class="t-when">PRE-WORKOUT</div><div class="t-title">Complex Carbs + Protein</div><div class="t-desc">Rice + chicken · Oats + eggs · 60–90 min before</div></div>
      <div class="t-card"><div class="t-icon">⚡</div><div class="t-when">TRAINING</div><div class="t-title">Water + Electrolytes</div><div class="t-desc">Optional banana if session &gt;90 min</div></div>
      <div class="t-card"><div class="t-icon">🌙</div><div class="t-when">POST-WORKOUT</div><div class="t-title">Protein + Fast Carbs</div><div class="t-desc">Shake + fruit · Yogurt + rice · Within 30–60 min</div></div>
    </div>
    <p style="font-size:12px;color:#9A8A80;line-height:1.6;"><strong style="color:var(--bark);">Rest days:</strong> Lower carbs slightly (–30–40g). Keep protein the same. Slightly more fat is fine.</p>
  </div>

  <div class="card">
    <div class="card-label">Flexible Meal Ideas</div>
    <div class="meal-list">
      <div class="meal-row"><div class="meal-em">🍳</div><div class="meal-body"><h4>Breakfast</h4><p>3 eggs + 2 whites, sourdough toast, half avo + black coffee</p></div><div class="meal-macros"><b>~32g P</b><small>~380 kcal</small></div></div>
      <div class="meal-row"><div class="meal-em">🍱</div><div class="meal-body"><h4>Pre-Workout Lunch</h4><p>Grilled chicken 150g, jasmine rice ¾ cup, stir-fried veggies</p></div><div class="meal-macros"><b>~42g P</b><small>~480 kcal</small></div></div>
      <div class="meal-row"><div class="meal-em">🥤</div><div class="meal-body"><h4>Post-Workout Snack</h4><p>Whey protein shake + 1 banana OR Greek yogurt + berries</p></div><div class="meal-macros"><b>~30g P</b><small>~250 kcal</small></div></div>
      <div class="meal-row"><div class="meal-em">🐟</div><div class="meal-body"><h4>Dinner</h4><p>Salmon 150g, sweet potato, steamed broccoli + olive oil drizzle</p></div><div class="meal-macros"><b>~38g P</b><small>~420 kcal</small></div></div>
      <div class="meal-row"><div class="meal-em">🧁</div><div class="meal-body"><h4>Evening Snack (Optional)</h4><p>Cottage cheese 150g + honey OR casein pudding</p></div><div class="meal-macros"><b>~22g P</b><small>~180 kcal</small></div></div>
    </div>
  </div>
</div>

<!-- ══════════════════════════════════════════════
     PAGE 6 — CYCLE MODE
══════════════════════════════════════════════ -->
<div id="cycle" class="page">
  <div class="pg-eyebrow">Train Smart</div>
  <h1 class="pg-title">Cycle Mode 🌸</h1>
  <p class="pg-sub">Auto-adjust your training to your hormones</p>

  <div class="card" style="background:linear-gradient(135deg,#FFF8F5,#FFF0EB);border-color:var(--blush);">
    <p style="font-size:13px;line-height:1.75;color:var(--bark);">🌸 <strong>Train WITH your cycle, not against it.</strong> Hormones fluctuate over ~28 days, directly affecting strength, recovery, energy, and mood. Use each phase strategically.</p>
  </div>

  <div class="phase-cards-grid">
    <div class="cyc-card follicular">
      <div class="cyc-phase">Follicular</div>
      <div class="cyc-days">Days 1–14</div>
      <span class="cyc-int int-high">HIGH INTENSITY</span>
      <ul class="cyc-tips">
        <li>Estrogen rising — energy peaks</li>
        <li>Best time for heavy lifting</li>
        <li>Push for PRs on hip thrust</li>
        <li>Full 4-day program</li>
      </ul>
    </div>
    <div class="cyc-card ovulation">
      <div class="cyc-phase">Ovulation</div>
      <div class="cyc-days">Day 14–16</div>
      <span class="cyc-int int-high">PEAK POWER</span>
      <ul class="cyc-tips">
        <li>Estrogen + testosterone peak</li>
        <li>Strongest you'll feel!</li>
        <li>Go heavy on all glute work</li>
        <li>Watch joint laxity</li>
      </ul>
    </div>
    <div class="cyc-card luteal">
      <div class="cyc-phase">Luteal</div>
      <div class="cyc-days">Days 15–28</div>
      <span class="cyc-int int-mod">MODERATE</span>
      <ul class="cyc-tips">
        <li>Energy dips, reduce 10–15%</li>
        <li>More rest between sets</li>
        <li>Focus on form over load</li>
        <li>Add 20–30g carbs (cravings)</li>
        <li>Prioritise sleep</li>
      </ul>
    </div>
    <div class="cyc-card menstrual">
      <div class="cyc-phase">Menstrual</div>
      <div class="cyc-days">Days 1–5</div>
      <span class="cyc-int int-rest">RECOVERY</span>
      <ul class="cyc-tips">
        <li>Light movement or full rest</li>
        <li>Gentle yoga/stretching</li>
        <li>Reduced incline walk</li>
        <li>Iron-rich foods (spinach, meat)</li>
        <li>Extra sleep + hydration</li>
      </ul>
    </div>
  </div>

  <div class="card">
    <div class="card-label">Phase-Adjusted Workout</div>
    <p style="font-size:12px;color:#9A8A80;margin-bottom:12px;">Select your current phase to see today's adapted plan:</p>
    <div class="phase-sel-row">
      <button class="psel-btn active" onclick="showCyc('foll',this)">Follicular</button>
      <button class="psel-btn" onclick="showCyc('ovul',this)">Ovulation</button>
      <button class="psel-btn" onclick="showCyc('lut',this)">Luteal (PMS)</button>
      <button class="psel-btn" onclick="showCyc('mens',this)">Period</button>
    </div>

    <div id="cyc-foll" class="cyc-workout active">
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🍑</div><div class="ex-preview-name">Hip Thrusts — full working weight</div><div class="ex-preview-sets">4×12</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🦵</div><div class="ex-preview-name">Leg Press — full load</div><div class="ex-preview-sets">4×15</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">💎</div><div class="ex-preview-name">RDL — go heavy</div><div class="ex-preview-sets">4×10</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-upper">🏋️</div><div class="ex-preview-name">Shoulder Press — push it</div><div class="ex-preview-sets">4×10</div></div>
      <div class="ex-preview-row"><div class="ex-preview-icon ic-cardio">🚶</div><div class="ex-preview-name">Incline walk 30 min</div><div class="ex-preview-sets">30 min</div></div>
    </div>

    <div id="cyc-ovul" class="cyc-workout">
      <div class="tip-pill">🌟 Peak strength — PR day!</div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🍑</div><div class="ex-preview-name">Hip Thrusts — PR attempt</div><div class="ex-preview-sets">5×8</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🔱</div><div class="ex-preview-name">Bulgarian Split Squat — heavy</div><div class="ex-preview-sets">4×10</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-upper">💫</div><div class="ex-preview-name">Lateral Raise — increase weight</div><div class="ex-preview-sets">4×12</div></div>
      <div class="ex-preview-row"><div class="ex-preview-icon ic-cardio">🚶</div><div class="ex-preview-name">Incline walk 30 min</div><div class="ex-preview-sets">30 min</div></div>
    </div>

    <div id="cyc-lut" class="cyc-workout">
      <div class="tip-pill">⚠️ Reduce load by 10–15% this week</div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🍑</div><div class="ex-preview-name">Hip Thrusts — lighter</div><div class="ex-preview-sets">3×15</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🦵</div><div class="ex-preview-name">Leg Press — moderate</div><div class="ex-preview-sets">3×15</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-core">🌀</div><div class="ex-preview-name">Hyperextension — bodyweight only</div><div class="ex-preview-sets">3×15</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-core">💆</div><div class="ex-preview-name">Stretching + foam rolling</div><div class="ex-preview-sets">10 min</div></div>
      <div class="ex-preview-row"><div class="ex-preview-icon ic-cardio">🚶</div><div class="ex-preview-name">Incline walk — reduce to 20 min</div><div class="ex-preview-sets">20 min</div></div>
    </div>

    <div id="cyc-mens" class="cyc-workout">
      <div class="tip-pill">🌸 Listen to your body. Rest is VALID.</div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-cardio">🧘</div><div class="ex-preview-name">Gentle yoga / stretching</div><div class="ex-preview-sets">20 min</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-cardio">🚶</div><div class="ex-preview-name">Easy flat walk (skip incline if cramping)</div><div class="ex-preview-sets">20 min</div></div>
      <div class="ex-preview-row" style="margin-bottom:7px;"><div class="ex-preview-icon ic-glute">🍑</div><div class="ex-preview-name">Hip Thrusts — optional, light weight only</div><div class="ex-preview-sets">2×12</div></div>
      <div class="ex-preview-row"><div class="ex-preview-icon ic-cardio">💤</div><div class="ex-preview-name">Prioritise 8h sleep + iron-rich foods</div><div class="ex-preview-sets">Priority</div></div>
    </div>
  </div>
</div>

<!-- ════════════════════════
     BOTTOM NAV (mobile)
════════════════════════ -->
<nav class="botnav">
  <div class="botnav-inner">
    <button class="bn-b active" onclick="showPage('dash',this,'bn')"><span class="bn-icon">📊</span>Home</button>
    <button class="bn-b" onclick="showPage('plan',this,'bn')"><span class="bn-icon">💪</span>Workout</button>
    <button class="bn-b" onclick="showPage('lib',this,'bn')"><span class="bn-icon">📚</span>Library</button>
    <button class="bn-b" onclick="showPage('cardio',this,'bn')"><span class="bn-icon">🏃</span>Cardio</button>
    <button class="bn-b" onclick="showPage('nutrition',this,'bn')"><span class="bn-icon">🥗</span>Nutrition</button>
    <button class="bn-b" onclick="showPage('cycle',this,'bn')"><span class="bn-icon">🌸</span>Cycle</button>
  </div>
</nav>

<script>
/* ═══════════════════════
   SVG FIGURE LIBRARY
═══════════════════════ */
const SVG = {
  hipthrust:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- bench -->
    <rect x="8" y="48" width="64" height="8" rx="3" fill="rgba(255,255,255,0.5)"/>
    <!-- body horizontal -->
    <rect x="20" y="38" width="42" height="7" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <!-- legs up -->
    <rect x="22" y="20" width="7" height="22" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <rect x="42" y="20" width="7" height="22" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <!-- feet -->
    <rect x="19" y="16" width="13" height="6" rx="3" fill="rgba(255,255,255,0.7)"/>
    <rect x="39" y="16" width="13" height="6" rx="3" fill="rgba(255,255,255,0.7)"/>
    <!-- head -->
    <circle cx="66" cy="40" r="7" fill="rgba(255,255,255,0.8)"/>
    <!-- bar -->
    <rect x="10" y="36" width="52" height="4" rx="2" fill="rgba(184,107,78,0.6)"/>
    <!-- up arrow -->
    <path d="M36 28 L40 20 L44 28" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round" fill="none"/>
  </svg>`,

  rdl:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- torso bent forward -->
    <rect x="12" y="34" width="40" height="8" rx="4" fill="rgba(255,255,255,0.8)" transform="rotate(-30,32,38)"/>
    <!-- legs straight -->
    <rect x="36" y="42" width="7" height="24" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <rect x="46" y="42" width="7" height="24" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <!-- arms down -->
    <rect x="20" y="44" width="6" height="20" rx="3" fill="rgba(255,255,255,0.7)"/>
    <rect x="28" y="44" width="6" height="20" rx="3" fill="rgba(255,255,255,0.7)"/>
    <!-- dumbbells -->
    <rect x="16" y="62" width="14" height="5" rx="2.5" fill="rgba(184,107,78,0.7)"/>
    <!-- head -->
    <circle cx="14" cy="28" r="7" fill="rgba(255,255,255,0.8)"/>
    <!-- arrow down then up -->
    <path d="M58 30 L62 38 L58 46" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round" fill="none"/>
  </svg>`,

  legpress:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- seat -->
    <rect x="8" y="44" width="30" height="8" rx="3" fill="rgba(255,255,255,0.5)"/>
    <!-- backrest -->
    <rect x="6" y="20" width="8" height="30" rx="4" fill="rgba(255,255,255,0.5)"/>
    <!-- body reclined -->
    <rect x="10" y="36" width="28" height="8" rx="4" fill="rgba(255,255,255,0.8)"/>
    <!-- legs pressing up-diag -->
    <rect x="34" y="24" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.8)" transform="rotate(-45,37,33)"/>
    <rect x="44" y="24" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.8)" transform="rotate(-45,47,33)"/>
    <!-- platform -->
    <rect x="52" y="8" width="16" height="24" rx="4" fill="rgba(255,255,255,0.4)"/>
    <!-- head -->
    <circle cx="14" cy="28" r="7" fill="rgba(255,255,255,0.8)"/>
    <!-- arrow -->
    <path d="M50 30 L56 22" stroke="rgba(184,107,78,0.9)" stroke-width="2.5" stroke-linecap="round"/>
  </svg>`,

  hyperext:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- roman chair frame -->
    <rect x="10" y="50" width="60" height="6" rx="3" fill="rgba(255,255,255,0.4)"/>
    <rect x="16" y="38" width="20" height="6" rx="3" fill="rgba(255,255,255,0.4)"/>
    <!-- body angled -->
    <rect x="28" y="28" width="38" height="8" rx="4" fill="rgba(255,255,255,0.8)" transform="rotate(20,47,32)"/>
    <!-- head -->
    <circle cx="65" cy="22" r="7" fill="rgba(255,255,255,0.8)"/>
    <!-- legs down -->
    <rect x="22" y="38" width="7" height="20" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <rect x="32" y="38" width="7" height="20" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <!-- arrow up -->
    <path d="M50 36 L54 26 L58 36" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round" fill="none"/>
  </svg>`,

  shoulderpress:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- torso seated -->
    <rect x="32" y="36" width="16" height="22" rx="5" fill="rgba(255,255,255,0.8)"/>
    <!-- arms raised -->
    <rect x="18" y="18" width="7" height="22" rx="3.5" fill="rgba(255,255,255,0.8)" transform="rotate(15,22,29)"/>
    <rect x="55" y="18" width="7" height="22" rx="3.5" fill="rgba(255,255,255,0.8)" transform="rotate(-15,58,29)"/>
    <!-- dumbbells -->
    <rect x="12" y="12" width="16" height="6" rx="3" fill="rgba(122,158,126,0.7)"/>
    <rect x="52" y="12" width="16" height="6" rx="3" fill="rgba(122,158,126,0.7)"/>
    <!-- head -->
    <circle cx="40" cy="28" r="8" fill="rgba(255,255,255,0.8)"/>
    <!-- seat -->
    <rect x="26" y="56" width="28" height="6" rx="3" fill="rgba(255,255,255,0.4)"/>
    <!-- arrows up -->
    <path d="M26 20 L22 10" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round"/>
    <path d="M54 20 L58 10" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round"/>
  </svg>`,

  lateralraise:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- torso -->
    <rect x="32" y="30" width="16" height="26" rx="5" fill="rgba(255,255,255,0.8)"/>
    <!-- arms out -->
    <rect x="6" y="36" width="26" height="7" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <rect x="48" y="36" width="26" height="7" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <!-- dumbbells -->
    <rect x="2" y="33" width="8" height="13" rx="3" fill="rgba(122,158,126,0.7)"/>
    <rect x="70" y="33" width="8" height="13" rx="3" fill="rgba(122,158,126,0.7)"/>
    <!-- head -->
    <circle cx="40" cy="22" r="8" fill="rgba(255,255,255,0.8)"/>
    <!-- legs -->
    <rect x="33" y="54" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.7)"/>
    <rect x="40" y="54" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.7)"/>
    <!-- upward arrows -->
    <path d="M8 38 L8 28" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round"/>
    <path d="M72 38 L72 28" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round"/>
  </svg>`,

  overheadraise:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- torso -->
    <rect x="32" y="34" width="16" height="22" rx="5" fill="rgba(255,255,255,0.8)"/>
    <!-- arms raised forward/up -->
    <rect x="28" y="10" width="7" height="26" rx="3.5" fill="rgba(255,255,255,0.8)" transform="rotate(-10,31,23)"/>
    <rect x="45" y="10" width="7" height="26" rx="3.5" fill="rgba(255,255,255,0.8)" transform="rotate(10,49,23)"/>
    <!-- dumbbells at top -->
    <rect x="22" y="8" width="14" height="6" rx="3" fill="rgba(176,160,208,0.8)"/>
    <rect x="44" y="8" width="14" height="6" rx="3" fill="rgba(176,160,208,0.8)"/>
    <!-- head -->
    <circle cx="40" cy="26" r="8" fill="rgba(255,255,255,0.8)"/>
    <!-- legs -->
    <rect x="33" y="54" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.7)"/>
    <rect x="40" y="54" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.7)"/>
    <!-- arrows -->
    <path d="M28 22 L24 12" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round"/>
    <path d="M52 22 L56 12" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round"/>
  </svg>`,

  extrotation:`<svg viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
    <!-- person lying on side -->
    <rect x="10" y="44" width="60" height="8" rx="4" fill="rgba(255,255,255,0.8)"/>
    <!-- top arm bent 90deg -->
    <rect x="34" y="28" width="7" height="18" rx="3.5" fill="rgba(255,255,255,0.8)"/>
    <!-- forearm rotating outward -->
    <rect x="34" y="28" width="20" height="7" rx="3.5" fill="rgba(255,255,255,0.7)" transform="rotate(-30,38,32)"/>
    <!-- small dumbbell -->
    <circle cx="55" cy="22" r="5" fill="rgba(104,152,192,0.8)"/>
    <!-- arc showing rotation -->
    <path d="M42 28 Q52 20 56 28" stroke="rgba(184,107,78,0.9)" stroke-width="2" stroke-linecap="round" fill="none" stroke-dasharray="3,2"/>
    <!-- head -->
    <circle cx="14" cy="40" r="7" fill="rgba(255,255,255,0.8)"/>
    <!-- elbow indicator -->
    <circle cx="38" cy="46" r="4" fill="rgba(184,107,78,0.4)"/>
    <text x="30" y="66" fill="rgba(58,42,32,0.5)" font-size="7" font-family="Jost">elbow anchored</text>
  </svg>`,
};

/* populate SVG illustrations in plan page */
function injectSVG(idSuffix, key){
  const els = document.querySelectorAll('[id$="-'+idSuffix+'"]');
  els.forEach(el=>{if(SVG[key]) el.innerHTML = SVG[key];});
}

/* inject in workout plan cards */
document.getElementById('ill-ht-plan').innerHTML = SVG.hipthrust;
document.getElementById('ill-lp-plan').innerHTML = SVG.legpress;
document.getElementById('ill-rdl-plan').innerHTML = SVG.rdl;
document.getElementById('ill-hyp-plan').innerHTML = SVG.hyperext;
document.getElementById('ill-sp-plan').innerHTML = SVG.shoulderpress;
document.getElementById('ill-lr-plan').innerHTML = SVG.lateralraise;
document.getElementById('ill-ovh-plan').innerHTML = SVG.overheadraise;
document.getElementById('ill-er-plan').innerHTML = SVG.extrotation;
document.getElementById('ill-er2-plan').innerHTML = SVG.extrotation;
document.getElementById('ill-ht2-plan').innerHTML = SVG.hipthrust;
document.getElementById('ill-hyp2-plan').innerHTML = SVG.hyperext;
document.getElementById('ill-sp2-plan').innerHTML = SVG.shoulderpress;
document.getElementById('ill-bss-plan').innerHTML = SVG.legpress; // closest visual
document.getElementById('ill-obliq-plan').innerHTML = SVG.hyperext;
document.getElementById('ill-plank-plan').innerHTML = SVG.extrotation;
document.getElementById('ill-lraise-plan').innerHTML = SVG.overheadraise;

/* inject in library thumbnails */
document.getElementById('lt-ht').insertAdjacentHTML('afterbegin', SVG.hipthrust);
document.getElementById('lt-rdl').insertAdjacentHTML('afterbegin', SVG.rdl);
document.getElementById('lt-lp').insertAdjacentHTML('afterbegin', SVG.legpress);
document.getElementById('lt-hyp').insertAdjacentHTML('afterbegin', SVG.hyperext);
document.getElementById('lt-ovh').insertAdjacentHTML('afterbegin', SVG.overheadraise);
document.getElementById('lt-er').insertAdjacentHTML('afterbegin', SVG.extrotation);
document.getElementById('lt-sp').insertAdjacentHTML('afterbegin', SVG.shoulderpress);
document.getElementById('lt-lr').insertAdjacentHTML('afterbegin', SVG.lateralraise);

/* ═══════════════════════
   EXERCISE LIBRARY DATA
═══════════════════════ */
const LIB = {
  hipthrust:{
    name:'Hip Thrusts',svgKey:'hipthrust',color:'c-glute',mandatory:true,
    primary:['Gluteus Maximus'],secondary:['Hamstrings','Core Stabilisers'],
    steps:[
      'Position a flat bench horizontally behind a loaded barbell (or Smith machine bar).',
      'Sit on the floor with your upper back against the edge of the bench.',
      'Roll the bar (with pad for comfort) over your hips. Feet flat on floor, hip-width apart.',
      'Brace your core, chin tucked. Drive through heels to lift hips upward.',
      'At the top: squeeze glutes HARD and hold for 1 full second. Hips level, no tilt.',
      'Lower slowly (2–3 seconds) — don\'t let hips touch the floor between reps.',
      'Repeat. Keep tension on the glute throughout the entire set.',
    ],
    tip:'This is your #1 glute-building exercise. Frequency matters — train it 2× per week.',
  },
  rdl:{
    name:'Romanian Deadlift (RDL)',svgKey:'rdl',color:'c-glute',mandatory:true,
    primary:['Hamstrings','Gluteus Maximus'],secondary:['Lower Back','Core'],
    steps:[
      'Stand hip-width, dumbbells in front of thighs, palms facing you.',
      'Soft bend in knees — maintain this angle throughout the whole movement.',
      'Push hips BACKWARD (like closing a car door with your bum). Torso falls forward.',
      'Keep dumbbells close to your shins. Go until you feel a deep hamstring stretch.',
      'Stop before your lower back rounds — range varies by flexibility.',
      'Drive hips FORWARD to return to standing. Squeeze glutes at the top.',
      'Tempo: 3 sec down, 1 sec up.',
    ],
    tip:'This is a HIP HINGE, not a squat. All movement comes from your hips going backward.',
  },
  legpress:{
    name:'Leg Press (Glute Focus)',svgKey:'legpress',color:'c-glute',mandatory:true,
    primary:['Gluteus Maximus','Hamstrings'],secondary:['Quadriceps','Calves'],
    steps:[
      'Place feet in the UPPER third of the leg press platform, hip-width, toes slightly out.',
      'High foot position = more glute. Low foot position = more quad.',
      'Lower the platform slowly — 3-second count. Knees track over toes.',
      'Go deep — knees near chest — for maximum glute stretch.',
      'Press through HEELS, not toes or the ball of your foot.',
      'Extend without locking knees at the top.',
      'Never bounce at the bottom. Control always.',
    ],
    tip:'The single biggest mistake: feet too low. Keep them high and wide for glutes.',
  },
  hyperext:{
    name:'Hyperextension (Roman Chair)',svgKey:'hyperext',color:'c-glute',mandatory:true,
    primary:['Glutes','Hamstrings'],secondary:['Erector Spinae','Lower Back'],
    steps:[
      'Set up on the Roman chair: pad at hip crease, ankle pads locked in.',
      'Cross arms on chest (or hold a plate/dumbbell for added resistance).',
      'Lower your upper body toward the floor in a controlled way.',
      'Feel the stretch through hamstrings and glutes.',
      'Raise your torso back up — stop at parallel with the floor. No hyperextension!',
      'Squeeze glutes hard at the top. Hold 1 second.',
      'Lower slowly (3 sec). Repeat.',
    ],
    tip:'Keep the movement glute-focused: think "squeeze the glutes to come up" not "use your back."',
  },
  overheadraise:{
    name:'Overhead Raise (Front Raise)',svgKey:'overheadraise',color:'c-shoulder',mandatory:true,
    primary:['Anterior Deltoid'],secondary:['Upper Pectoralis','Serratus Anterior'],
    steps:[
      'Stand tall, dumbbells in front of thighs, palms facing back (or thumbs up).',
      'Brace core and keep a slight bend in elbows.',
      'Raise both arms straight forward and upward — to shoulder height or slightly above.',
      'Keep thumbs pointing up (reduces rotator cuff impingement).',
      'Hold at shoulder height for 1 second.',
      'Lower SLOWLY back to start — 3-second count. Don\'t drop the weights.',
      'Avoid swinging the torso — keep movement arm-only.',
    ],
    tip:'Use lighter weight than you think. Perfect slow reps build more shoulder than heavy sloppy ones.',
  },
  extrotation:{
    name:'External Rotation (Shoulder Stability)',svgKey:'extrotation',color:'c-upper',mandatory:true,
    primary:['Infraspinatus','Teres Minor'],secondary:['Posterior Deltoid','Rotator Cuff'],
    steps:[
      'Lie on your side, top arm bent at 90° with elbow tucked against your ribs.',
      'Hold a very light dumbbell in the top hand, forearm pointing toward floor.',
      'Keeping elbow pressed to ribs, rotate forearm UPWARD (outward) as far as comfortable.',
      'Hold 1 second at the top. Lower slowly.',
      'Alternative: Stand, cable set at elbow height. Same 90° elbow, rotate outward.',
      'Complete all reps on one side, then switch.',
    ],
    tip:'NEVER heavy. This is rehabilitation and shoulder health. Light, perfect, pain-free. Do every upper body session.',
  },
  shoulderpress:{
    name:'Shoulder Press (Dumbbell)',svgKey:'shoulderpress',color:'c-shoulder',mandatory:true,
    primary:['Anterior Deltoid','Medial Deltoid'],secondary:['Triceps','Upper Trapezius'],
    steps:[
      'Sit on a bench with back support (or stand). Hold dumbbells at shoulder height, palms forward.',
      'Elbows at roughly 90° and slightly in front of your body plane.',
      'Brace core. Press dumbbells straight up — don\'t flare elbows excessively wide.',
      'Bring dumbbells close at the top without clashing them.',
      'Lower slowly to starting position — 2-second count.',
      'Don\'t shrug your traps. Keep shoulders down and packed throughout.',
    ],
    tip:'Wider shoulders visually narrow the waist — this is one of the most important hourglass exercises!',
  },
  lateralraise:{
    name:'Lateral Raise (Dumbbell)',svgKey:'lateralraise',color:'c-shoulder',mandatory:true,
    primary:['Medial Deltoid'],secondary:['Supraspinatus','Upper Trapezius'],
    steps:[
      'Stand with dumbbells at sides. Slight forward lean at the waist (10–15°).',
      'Slight bend in elbows — maintain this throughout.',
      'Raise both arms out to the sides — lead with your elbows, not your hands.',
      'Pinky slightly higher than thumb at the top (like tilting a jug).',
      'Raise to shoulder height. Don\'t go above — no need.',
      'Hold 1 second at the top.',
      'Lower SLOWLY — 3 full seconds back down. This eccentric is crucial for growth.',
    ],
    tip:'SLOW is the secret. Drop the weight and go slow. The medial delt is a small muscle — it grows from tension, not momentum.',
  },
};

/* ═══════════════════════
   NAVIGATION
═══════════════════════ */
function showPage(id, btn, navType){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  if(navType==='bn'){
    document.querySelectorAll('.bn-b').forEach(b=>b.classList.remove('active'));
  } else {
    document.querySelectorAll('.tn-tab').forEach(b=>b.classList.remove('active'));
  }
  if(btn) btn.classList.add('active');
  window.scrollTo(0,0);
}

function showDay(id, btn){
  document.querySelectorAll('.day-cnt').forEach(d=>d.classList.remove('active'));
  document.querySelectorAll('.day-tab').forEach(b=>b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  btn.classList.add('active');
}

/* ═══════════════════════
   LIBRARY
═══════════════════════ */
function libShow(key){
  const ex = LIB[key];
  if(!ex) return;
  document.getElementById('lib-grid').style.display='none';
  const det = document.getElementById('lib-detail');
  det.classList.add('active');
  const pri = ex.primary.map(m=>`<span class="m-chip pri">${m}</span>`).join('');
  const sec = ex.secondary.map(m=>`<span class="m-chip sec">${m}</span>`).join('');
  const sts = ex.steps.map(s=>`<li><span>${s}</span></li>`).join('');
  document.getElementById('lib-detail-content').innerHTML = `
    <div class="ex-card">
      <div class="ex-card-top">
        <div class="ex-illus ${ex.color}" style="width:100px;height:100px;flex-shrink:0;">${SVG[ex.svgKey]||''}</div>
        <div class="ex-meta">
          <h3 style="font-size:17px;">${ex.name}</h3>
          ${ex.mandatory?'<div class="tag-row"><span class="tag tag-mand">⭐ Mandatory Exercise</span></div>':''}
        </div>
      </div>
      <div style="padding:0 18px 8px;">
        <div style="font-size:10px;color:var(--terr);font-weight:700;letter-spacing:1.5px;margin-bottom:4px;">PRIMARY MUSCLES</div>
        <div class="muscle-chips">${pri}</div>
        <div style="font-size:10px;color:#8A7A70;font-weight:700;letter-spacing:1.5px;margin-bottom:4px;">SECONDARY MUSCLES</div>
        <div class="muscle-chips">${sec}</div>
        <div class="divider"></div>
        <div style="font-family:'Playfair Display',serif;font-size:16px;font-weight:600;margin-bottom:10px;color:var(--bark);">How to Perform</div>
        <ol class="steps-ol">${sts}</ol>
        <div class="divider"></div>
        <div class="ex-cue"><strong>Coach's Tip:</strong> ${ex.tip}</div>
      </div>
    </div>`;
}

function libHide(){
  document.getElementById('lib-grid').style.display='block';
  document.getElementById('lib-detail').classList.remove('active');
}

/* ═══════════════════════
   CYCLE MODE
═══════════════════════ */
function showCyc(phase, btn){
  document.querySelectorAll('.cyc-workout').forEach(c=>c.classList.remove('active'));
  document.querySelectorAll('.psel-btn').forEach(b=>b.classList.remove('active'));
  document.getElementById('cyc-'+phase).classList.add('active');
  btn.classList.add('active');
}

/* ═══════════════════════
   LOG
═══════════════════════ */
function logIt(){
  const w = document.getElementById('wInput').value;
  const wa = document.getElementById('waistIn').value;
  const msg = document.getElementById('logMsg');
  if(!w && !wa){ msg.textContent='Please enter at least one measurement.'; return; }
  msg.textContent = `✓ Saved${w?' — '+w+' kg':''}${wa?' — Waist '+wa+'"':''}. Keep going! 🌸`;
  document.getElementById('wInput').value='';
  document.getElementById('waistIn').value='';
}
</script>
</body>
</html>
