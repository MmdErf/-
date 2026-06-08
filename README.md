# -[مجله تورم و آسیب‌شناسی اجتماعی.html](https://github.com/user-attachments/files/28726351/default.html)
<!DOCTYPE html>
<html lang="fa" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>تورم و آسیب‌شناسی اجتماعی</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700;800&display=swap');

:root {
  --navy: #0d1b2a;
  --blue: #1b4f72;
  --accent: #e74c3c;
  --gold: #f39c12;
  --light: #ecf0f1;
  --card-bg: #1a2a3a;
}

* { margin: 0; padding: 0; box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  font-family: 'Vazirmatn', Tahoma, sans-serif;
  background: #0a0f1a;
  color: #e8e8e8;
  direction: rtl;
  overflow-x: hidden;
}

/* ─── SCROLLBAR ─── */
::-webkit-scrollbar { width: 6px; }
::-webkit-scrollbar-track { background: #0a0f1a; }
::-webkit-scrollbar-thumb { background: var(--gold); border-radius: 3px; }

/* ─── COVER PAGE ─── */
.cover {
  min-height: 100vh;
  background: linear-gradient(160deg, #0d1b2a 0%, #1a0a2e 50%, #0d1b2a 100%);
  display: flex; flex-direction: column;
  align-items: center; justify-content: center;
  position: relative; overflow: hidden;
  padding: 40px 20px;
}

.cover-bg {
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse at 20% 30%, rgba(231,76,60,0.12) 0%, transparent 50%),
    radial-gradient(ellipse at 80% 70%, rgba(243,156,18,0.08) 0%, transparent 50%);
}

/* Animated particles */
.particles { position: absolute; inset: 0; pointer-events: none; }
.particle {
  position: absolute;
  width: 3px; height: 3px;
  border-radius: 50%;
  background: var(--gold);
  opacity: 0;
  animation: float-up linear infinite;
}
@keyframes float-up {
  0% { transform: translateY(100vh) scale(0); opacity: 0; }
  10% { opacity: 0.6; }
  90% { opacity: 0.3; }
  100% { transform: translateY(-20px) scale(1); opacity: 0; }
}

.cover-badge {
  background: rgba(231,76,60,0.2);
  border: 1px solid rgba(231,76,60,0.5);
  color: #e74c3c;
  padding: 6px 20px;
  border-radius: 30px;
  font-size: 12px;
  letter-spacing: 2px;
  margin-bottom: 28px;
  animation: fadeInDown 1s ease;
}

.cover-title {
  font-size: clamp(28px, 6vw, 64px);
  font-weight: 800;
  text-align: center;
  line-height: 1.4;
  animation: fadeInUp 1s ease 0.3s both;
}

.cover-title .highlight {
  background: linear-gradient(90deg, #e74c3c, #f39c12);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.cover-subtitle {
  font-size: 14px;
  color: rgba(255,255,255,0.5);
  text-align: center;
  margin-top: 16px;
  animation: fadeInUp 1s ease 0.5s both;
}

.bismillah {
  font-size: 20px;
  color: var(--gold);
  text-align: center;
  margin-bottom: 32px;
  animation: fadeInDown 1s ease 0.1s both;
  opacity: 0.9;
}

/* Big animated coin */
.cover-visual {
  margin: 40px 0;
  position: relative;
  width: 200px; height: 200px;
  animation: fadeInUp 1s ease 0.7s both;
}
.coin-ring {
  position: absolute; inset: 0;
  border-radius: 50%;
  border: 2px solid rgba(243,156,18,0.3);
  animation: spin-slow 8s linear infinite;
}
.coin-ring:nth-child(2) {
  inset: 10px;
  border-color: rgba(231,76,60,0.2);
  animation-duration: 12s;
  animation-direction: reverse;
}
.coin-ring:nth-child(3) {
  inset: 20px;
  border-color: rgba(243,156,18,0.15);
  animation-duration: 6s;
}
@keyframes spin-slow { from { transform: rotate(0deg); } to { transform: rotate(360deg); } }

.coin-center {
  position: absolute;
  inset: 30px;
  background: radial-gradient(circle at 35% 35%, #f5d76e, #c49a0a);
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  font-size: 60px;
  box-shadow: 0 0 40px rgba(243,156,18,0.4), inset 0 4px 8px rgba(255,255,255,0.2);
  animation: pulse-coin 2s ease-in-out infinite;
}
@keyframes pulse-coin {
  0%, 100% { transform: scale(1); box-shadow: 0 0 40px rgba(243,156,18,0.4); }
  50% { transform: scale(1.05); box-shadow: 0 0 60px rgba(243,156,18,0.6); }
}

/* Falling numbers animation */
.falling-numbers {
  position: absolute; inset: 0;
  pointer-events: none; overflow: hidden;
}
.fall-num {
  position: absolute;
  font-size: 11px;
  color: rgba(243,156,18,0.25);
  font-weight: 600;
  animation: fall linear infinite;
  top: -20px;
}
@keyframes fall {
  from { transform: translateY(-20px); opacity: 0.4; }
  to { transform: translateY(100vh); opacity: 0; }
}

.toc {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 12px;
  max-width: 700px;
  margin-top: 40px;
  animation: fadeInUp 1s ease 1s both;
}
.toc-item {
  background: rgba(255,255,255,0.05);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 12px;
  padding: 14px 18px;
  cursor: pointer;
  transition: all 0.3s;
  text-decoration: none;
  color: inherit;
  display: block;
}
.toc-item:hover {
  background: rgba(243,156,18,0.1);
  border-color: var(--gold);
  transform: translateY(-3px);
}
.toc-num { font-size: 22px; font-weight: 800; color: var(--gold); display: block; }
.toc-label { font-size: 12px; color: rgba(255,255,255,0.6); margin-top: 4px; }

@keyframes fadeInUp { from { opacity: 0; transform: translateY(30px); } to { opacity: 1; transform: translateY(0); } }
@keyframes fadeInDown { from { opacity: 0; transform: translateY(-20px); } to { opacity: 1; transform: translateY(0); } }

/* ─── DIVIDER ─── */
.page-divider {
  height: 2px;
  background: linear-gradient(90deg, transparent, var(--gold), transparent);
  margin: 0;
}

/* ─── SECTION COMMON ─── */
.section {
  padding: 80px 24px;
  max-width: 900px;
  margin: 0 auto;
  position: relative;
}

.section-label {
  font-size: 11px;
  letter-spacing: 3px;
  color: var(--gold);
  text-transform: uppercase;
  margin-bottom: 12px;
}

.section-title {
  font-size: clamp(22px, 4vw, 36px);
  font-weight: 800;
  line-height: 1.4;
  margin-bottom: 32px;
}

.section-title span {
  color: var(--gold);
}

/* Scroll-reveal */
.reveal {
  opacity: 0;
  transform: translateY(40px);
  transition: opacity 0.7s ease, transform 0.7s ease;
}
.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}

/* ─── INTRO SECTION ─── */
.intro-bg {
  background: linear-gradient(180deg, #0a0f1a 0%, #111827 100%);
}

.intro-quote {
  border-right: 3px solid var(--accent);
  padding: 20px 24px;
  background: rgba(231,76,60,0.06);
  border-radius: 0 12px 12px 0;
  font-size: 16px;
  line-height: 2;
  color: rgba(255,255,255,0.85);
  margin: 32px 0;
  font-style: italic;
}

.intro-body p {
  font-size: 14.5px;
  line-height: 2.2;
  color: rgba(255,255,255,0.75);
  margin-bottom: 20px;
  text-align: justify;
}

/* Animated GDP chart SVG */
.chart-anim {
  width: 100%;
  height: 120px;
  margin: 32px 0;
  position: relative;
}
.chart-anim svg { width: 100%; height: 100%; }
.chart-line {
  stroke-dasharray: 1000;
  stroke-dashoffset: 1000;
  animation: draw-line 3s ease forwards 0.5s;
}
@keyframes draw-line {
  to { stroke-dashoffset: 0; }
}

/* ─── CONCEPTS SECTION ─── */
.concepts-bg { background: #0d1420; }

.concept-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 20px;
  margin-top: 32px;
}

.concept-card {
  background: linear-gradient(135deg, #1a2a3a, #111827);
  border: 1px solid rgba(255,255,255,0.07);
  border-radius: 16px;
  padding: 28px 24px;
  position: relative;
  overflow: hidden;
  transition: transform 0.3s, border-color 0.3s;
}
.concept-card:hover {
  transform: translateY(-6px);
  border-color: var(--gold);
}
.concept-card::before {
  content: '';
  position: absolute;
  top: 0; right: 0;
  width: 80px; height: 80px;
  background: radial-gradient(circle, rgba(243,156,18,0.15), transparent);
  border-radius: 0 16px 0 80px;
}
.card-icon { font-size: 36px; margin-bottom: 16px; display: block; }
.card-title { font-size: 16px; font-weight: 700; color: var(--gold); margin-bottom: 12px; }
.card-body { font-size: 13px; line-height: 2; color: rgba(255,255,255,0.65); }

/* Comparison bar */
.compare-bar {
  margin: 40px 0;
  background: rgba(255,255,255,0.03);
  border-radius: 16px;
  padding: 28px;
  border: 1px solid rgba(255,255,255,0.06);
}
.compare-title { font-size: 14px; font-weight: 600; color: rgba(255,255,255,0.7); margin-bottom: 20px; }
.bar-row { margin-bottom: 16px; }
.bar-label { font-size: 12px; color: rgba(255,255,255,0.5); margin-bottom: 6px; display: flex; justify-content: space-between; }
.bar-track { height: 8px; background: rgba(255,255,255,0.08); border-radius: 4px; overflow: hidden; }
.bar-fill {
  height: 100%; border-radius: 4px;
  width: 0;
  transition: width 1.5s ease;
}
.bar-fill.red { background: linear-gradient(90deg, #c0392b, #e74c3c); }
.bar-fill.gold { background: linear-gradient(90deg, #d4ac0d, #f39c12); }
.bar-fill.blue { background: linear-gradient(90deg, #1a5276, #2980b9); }

/* ─── CPI SECTION ─── */
.cpi-bg { background: linear-gradient(180deg, #0d1420 0%, #0a0f1a 100%); }

.cpi-visual {
  display: flex;
  gap: 12px;
  flex-wrap: wrap;
  margin: 32px 0;
  justify-content: center;
}
.cpi-item {
  background: rgba(255,255,255,0.04);
  border: 1px solid rgba(255,255,255,0.08);
  border-radius: 12px;
  padding: 16px 14px;
  text-align: center;
  min-width: 100px;
  transition: all 0.4s;
  cursor: default;
  position: relative;
  overflow: hidden;
}
.cpi-item:hover {
  background: rgba(243,156,18,0.1);
  border-color: var(--gold);
  transform: scale(1.05);
}
.cpi-item .emoji { font-size: 28px; display: block; margin-bottom: 8px; }
.cpi-item .cpi-name { font-size: 11px; color: rgba(255,255,255,0.5); }
.cpi-item .cpi-pct {
  font-size: 16px; font-weight: 700; color: var(--accent);
  display: block; margin-top: 4px;
}

.thermometer-wrap {
  display: flex;
  align-items: flex-end;
  justify-content: center;
  gap: 32px;
  flex-wrap: wrap;
  margin: 40px 0;
}
.thermo {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 8px;
}
.thermo-tube {
  width: 28px;
  height: 140px;
  background: rgba(255,255,255,0.06);
  border-radius: 14px;
  position: relative;
  overflow: hidden;
  border: 1px solid rgba(255,255,255,0.1);
}
.thermo-fill {
  position: absolute;
  bottom: 0; left: 0; right: 0;
  border-radius: 14px;
  width: 0;
  transition: height 2s ease, background 2s ease;
}
.thermo-label { font-size: 11px; color: rgba(255,255,255,0.5); text-align: center; max-width: 70px; }
.thermo-val { font-size: 14px; font-weight: 700; }

/* ─── STAGFLATION ─── */
.stag-bg { background: #0a0f1a; }

.stag-diagram {
  position: relative;
  height: 260px;
  margin: 40px 0;
}
.stag-circle {
  position: absolute;
  border-radius: 50%;
  display: flex; align-items: center; justify-content: center;
  flex-direction: column;
  text-align: center;
  font-size: 12px;
  font-weight: 600;
  animation: breathe 3s ease-in-out infinite;
  border: 2px solid;
}
@keyframes breathe {
  0%, 100% { transform: scale(1); }
  50% { transform: scale(1.04); }
}
.sc1 {
  width: 160px; height: 160px;
  background: rgba(231,76,60,0.12);
  border-color: rgba(231,76,60,0.4);
  top: 20px; right: 20px;
  color: #e74c3c;
  animation-delay: 0s;
}
.sc2 {
  width: 160px; height: 160px;
  background: rgba(243,156,18,0.12);
  border-color: rgba(243,156,18,0.4);
  top: 20px; left: 50%;
  transform: translateX(-50%);
  color: #f39c12;
  animation-delay: 1s;
}
.sc3 {
  width: 160px; height: 160px;
  background: rgba(41,128,185,0.12);
  border-color: rgba(41,128,185,0.4);
  top: 20px; left: 20px;
  color: #3498db;
  animation-delay: 2s;
}
.sc-center {
  position: absolute;
  width: 90px; height: 90px;
  background: rgba(255,255,255,0.08);
  border: 2px solid rgba(255,255,255,0.2);
  border-radius: 50%;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  display: flex; align-items: center; justify-content: center;
  font-size: 11px; font-weight: 700;
  color: white; text-align: center;
  z-index: 2;
}

/* ─── SOCIAL DAMAGE SECTIONS ─── */
.damage-bg { background: linear-gradient(180deg, #0a0f1a, #120a0a); }

.stat-row {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 16px;
  margin: 32px 0;
}
.stat-box {
  text-align: center;
  background: rgba(255,255,255,0.03);
  border-radius: 14px;
  padding: 24px 16px;
  border: 1px solid rgba(255,255,255,0.06);
  transition: all 0.3s;
}
.stat-box:hover {
  background: rgba(231,76,60,0.08);
  border-color: var(--accent);
}
.stat-num {
  font-size: 32px;
  font-weight: 800;
  background: linear-gradient(90deg, #e74c3c, #f39c12);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  display: block;
}
.stat-label { font-size: 12px; color: rgba(255,255,255,0.5); margin-top: 6px; }

/* Research card */
.research-card {
  background: linear-gradient(135deg, #1a0e0e, #1a1a2e);
  border-radius: 18px;
  padding: 32px;
  border: 1px solid rgba(231,76,60,0.2);
  margin: 32px 0;
  position: relative;
  overflow: hidden;
}
.research-card::after {
  content: '"';
  position: absolute;
  top: -20px; left: 16px;
  font-size: 150px;
  color: rgba(231,76,60,0.06);
  font-family: Georgia, serif;
  line-height: 1;
}
.rc-source {
  font-size: 11px;
  color: var(--gold);
  letter-spacing: 1px;
  margin-bottom: 16px;
  display: flex; align-items: center; gap: 8px;
}
.rc-source::before {
  content: '';
  display: inline-block;
  width: 20px; height: 2px;
  background: var(--gold);
}
.rc-body { font-size: 13.5px; line-height: 2.2; color: rgba(255,255,255,0.72); text-align: justify; }
.rc-body p { margin-bottom: 14px; }
.rc-body p:last-child { margin-bottom: 0; }

/* Key finding */
.key-finding {
  background: linear-gradient(135deg, rgba(243,156,18,0.1), rgba(231,76,60,0.08));
  border: 1px solid rgba(243,156,18,0.25);
  border-radius: 14px;
  padding: 22px 26px;
  margin: 24px 0;
  display: flex; gap: 16px; align-items: flex-start;
}
.kf-icon { font-size: 28px; flex-shrink: 0; }
.kf-text { font-size: 13.5px; line-height: 2; color: rgba(255,255,255,0.8); }

/* People icons animation */
.people-row {
  display: flex; gap: 8px; flex-wrap: wrap;
  justify-content: center;
  margin: 28px 0;
}
.person-icon {
  font-size: 28px;
  transition: all 0.4s;
  filter: grayscale(1) opacity(0.3);
  cursor: default;
}
.person-icon.affected { filter: none; animation: shake 0.5s ease; }
@keyframes shake {
  0%, 100% { transform: translateX(0); }
  25% { transform: translateX(-4px); }
  75% { transform: translateX(4px); }
}

/* ─── POLITICAL SECTION ─── */
.political-bg { background: linear-gradient(180deg, #120a0a, #0a0f1a); }

.timeline {
  position: relative;
  padding-right: 30px;
  margin: 32px 0;
}
.timeline::before {
  content: '';
  position: absolute;
  right: 9px; top: 0; bottom: 0;
  width: 2px;
  background: linear-gradient(180deg, var(--gold), transparent);
}
.tl-item {
  position: relative;
  padding: 0 24px 32px 0;
  opacity: 0;
  transform: translateX(20px);
  transition: all 0.6s ease;
}
.tl-item.visible { opacity: 1; transform: translateX(0); }
.tl-item::before {
  content: '';
  position: absolute;
  right: 4px; top: 4px;
  width: 12px; height: 12px;
  border-radius: 50%;
  background: var(--gold);
  border: 2px solid #0a0f1a;
  box-shadow: 0 0 10px var(--gold);
}
.tl-title { font-size: 14px; font-weight: 700; color: var(--gold); margin-bottom: 8px; }
.tl-body { font-size: 13px; line-height: 2; color: rgba(255,255,255,0.65); text-align: justify; }

/* Trust meter */
.trust-meter {
  background: rgba(255,255,255,0.03);
  border-radius: 14px;
  padding: 24px;
  margin: 28px 0;
  border: 1px solid rgba(255,255,255,0.06);
}
.tm-label { font-size: 13px; color: rgba(255,255,255,0.6); margin-bottom: 12px; }
.tm-bar {
  height: 12px;
  background: rgba(255,255,255,0.06);
  border-radius: 6px;
  overflow: hidden;
  margin-bottom: 20px;
}
.tm-fill {
  height: 100%;
  border-radius: 6px;
  width: 0;
  transition: width 2s ease;
}

/* ─── PSYCHOLOGY SECTION ─── */
.psych-bg { background: linear-gradient(180deg, #0a0f1a, #0d0d1a); }

.stress-meter-wrap { text-align: center; margin: 40px 0; }
.stress-meter {
  width: 200px; height: 100px;
  margin: 0 auto 20px;
  position: relative;
}
.stress-meter svg { width: 100%; height: 100%; overflow: visible; }
.stress-arc {
  stroke-dasharray: 314;
  stroke-dashoffset: 314;
  animation: fill-arc 2.5s ease forwards 0.5s;
}
@keyframes fill-arc { to { stroke-dashoffset: 80; } }
.stress-needle {
  transform-origin: 100px 100px;
  transform: rotate(-90deg);
  animation: needle-swing 2.5s ease forwards 0.5s;
}
@keyframes needle-swing { to { transform: rotate(40deg); } }

.emotion-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  gap: 12px;
  margin: 28px 0;
}
.emotion-card {
  background: rgba(255,255,255,0.03);
  border: 1px solid rgba(255,255,255,0.06);
  border-radius: 12px;
  padding: 20px 16px;
  text-align: center;
  transition: all 0.3s;
}
.emotion-card:hover {
  transform: translateY(-4px);
  border-color: rgba(155,89,182,0.5);
  background: rgba(155,89,182,0.08);
}
.emotion-card .em-icon { font-size: 32px; margin-bottom: 10px; }
.emotion-card .em-name { font-size: 12px; font-weight: 600; color: rgba(255,255,255,0.7); }

/* ─── CONCLUSION ─── */
.conclusion-bg {
  background: linear-gradient(160deg, #1a0a2e, #0a0f1a);
  padding: 100px 24px;
  text-align: center;
}
.conclusion-inner { max-width: 700px; margin: 0 auto; }
.conc-icon {
  font-size: 64px;
  display: block;
  margin-bottom: 24px;
  animation: spin-slow 10s linear infinite;
}
.conc-title {
  font-size: 28px;
  font-weight: 800;
  margin-bottom: 24px;
  background: linear-gradient(90deg, #e74c3c, #f39c12, #e74c3c);
  background-size: 200%;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  animation: shimmer 3s linear infinite;
}
@keyframes shimmer { from { background-position: 0%; } to { background-position: 200%; } }
.conc-body { font-size: 14px; line-height: 2.2; color: rgba(255,255,255,0.7); text-align: justify; }
.conc-body p { margin-bottom: 16px; }

/* ─── PROGRESS NAV ─── */
.progress-nav {
  position: fixed;
  left: 16px;
  top: 50%;
  transform: translateY(-50%);
  display: flex; flex-direction: column; gap: 8px;
  z-index: 100;
}
.pn-dot {
  width: 8px; height: 8px;
  border-radius: 50%;
  background: rgba(255,255,255,0.2);
  cursor: pointer;
  transition: all 0.3s;
  border: 1px solid rgba(255,255,255,0.1);
}
.pn-dot.active { background: var(--gold); transform: scale(1.4); }

@media (max-width: 600px) {
  .progress-nav { display: none; }
  .stag-diagram { height: 420px; }
  .sc1 { right: 10px; }
  .sc3 { left: 10px; }
}
</style>
</head>
<body>

<!-- NAV DOTS -->
<nav class="progress-nav" id="pnav">
  <div class="pn-dot active" onclick="scrollToSection(0)" title="جلد"></div>
  <div class="pn-dot" onclick="scrollToSection(1)" title="مقدمه"></div>
  <div class="pn-dot" onclick="scrollToSection(2)" title="تورم چیست"></div>
  <div class="pn-dot" onclick="scrollToSection(3)" title="CPI"></div>
  <div class="pn-dot" onclick="scrollToSection(4)" title="فقرا"></div>
  <div class="pn-dot" onclick="scrollToSection(5)" title="آسیب اجتماعی"></div>
  <div class="pn-dot" onclick="scrollToSection(6)" title="سیاسی"></div>
  <div class="pn-dot" onclick="scrollToSection(7)" title="روانی"></div>
  <div class="pn-dot" onclick="scrollToSection(8)" title="نتیجه"></div>
</nav>

<!-- ══════════════════════════════════════ -->
<!-- COVER -->
<!-- ══════════════════════════════════════ -->
<section id="s0" class="cover">
  <div class="cover-bg"></div>

  <div class="particles" id="particles"></div>
  <div class="falling-numbers" id="falling"></div>

  <div class="bismillah">بِسْمِ اللهِ الرَّحْمٰنِ الرَّحِيمِ</div>
  <div class="cover-badge">پژوهش علوم اجتماعی</div>

  <div class="cover-visual">
    <div class="coin-ring"></div>
    <div class="coin-ring"></div>
    <div class="coin-ring"></div>
    <div class="coin-center">💰</div>
  </div>

  <h1 class="cover-title">
    <span class="highlight">تورم</span><br>
    و آسیب‌شناسی اجتماعی
  </h1>
  <p class="cover-subtitle">بررسی پیامدهای اقتصادی، اجتماعی، سیاسی و روانی تورم</p>

  <nav class="toc">
    <a class="toc-item" onclick="scrollToSection(1)">
      <span class="toc-num">۱</span>
      <div class="toc-label">مقدمه</div>
    </a>
    <a class="toc-item" onclick="scrollToSection(2)">
      <span class="toc-num">۲</span>
      <div class="toc-label">مفهوم تورم</div>
    </a>
    <a class="toc-item" onclick="scrollToSection(3)">
      <span class="toc-num">۳</span>
      <div class="toc-label">شاخص CPI</div>
    </a>
    <a class="toc-item" onclick="scrollToSection(4)">
      <span class="toc-num">۴</span>
      <div class="toc-label">تورم و فقرا</div>
    </a>
    <a class="toc-item" onclick="scrollToSection(5)">
      <span class="toc-num">۵</span>
      <div class="toc-label">آسیب اجتماعی</div>
    </a>
    <a class="toc-item" onclick="scrollToSection(6)">
      <span class="toc-num">۶</span>
      <div class="toc-label">آسیب سیاسی</div>
    </a>
    <a class="toc-item" onclick="scrollToSection(7)">
      <span class="toc-num">۷</span>
      <div class="toc-label">آسیب روانی</div>
    </a>
  </nav>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- INTRO -->
<!-- ══════════════════════════════════════ -->
<section id="s1" class="intro-bg" style="padding:60px 0">
<div class="section">
  <div class="section-label reveal">بخش اول · مقدمه</div>
  <h2 class="section-title reveal">اقتصاد، فراتر از <span>آمار و ارقام</span></h2>

  <div class="intro-quote reveal">
    تورم صرفاً یک شاخص انتزاعی یا عددی بی‌روح در گزارش‌های بانک مرکزی نیست؛ بلکه نیرویی اجتماعی است که «بطن» جامعه را بازتعریف می‌کند، مناسبات انسانی را دستخوش تغییر می‌سازد و مرزهای اخلاقی را جابه‌جا می‌کند.
  </div>

  <div class="intro-body">
    <p class="reveal">اقتصاد و مشکلات اقتصادی همواره نقشی فراتر از آمار و ارقام صرف در زندگی انسان‌ها ایفا کرده‌اند، به‌گونه‌ای که چشم‌پوشی از آنها، خیانتی است به عمق یک تحلیل اجتماعی. در این میان، تورم یکی از ملموس‌ترین و مزمن‌ترین مشکلات اقتصادی‌ای است که ما ایرانیان سال‌هاست با آن دست‌وپنجه نرم می‌کنیم.</p>
    <p class="reveal">در تقابل با نگاه تقلیل‌گرایی که تورم را منحصراً پدیده‌ای پولی و حاصل افزایش سطح عمومی قیمت‌ها می‌پندارد، نظریه‌های جدیدتر آن را بسیار فراتر می‌برند. از این منظر، تورم نه یک پیامد خنثی، که موتور محرک تضاد طبقاتی و سازوکاری برای بازتولید نابرابری‌های موجود است.</p>
    <p class="reveal">در این نوشته تلاش بر آن است که ابتدا تصویری روشن و اصولی از مفهوم تورم و ابعاد پیرامونی آن ترسیم گردد و در ادامه، آسیب‌های اجتماعی‌ای که این پدیده می‌تواند در بستر جامعه ایجاد کند، مورد واکاوی قرار گیرد.</p>
  </div>

  <!-- Animated line chart -->
  <div class="chart-anim reveal">
    <svg viewBox="0 0 800 120" preserveAspectRatio="none">
      <defs>
        <linearGradient id="lineGrad" x1="0" y1="0" x2="1" y2="0">
          <stop offset="0%" stop-color="#e74c3c"/>
          <stop offset="100%" stop-color="#f39c12"/>
        </linearGradient>
        <linearGradient id="fillGrad" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%" stop-color="rgba(231,76,60,0.15)"/>
          <stop offset="100%" stop-color="transparent"/>
        </linearGradient>
      </defs>
      <!-- grid lines -->
      <line x1="0" y1="30" x2="800" y2="30" stroke="rgba(255,255,255,0.04)" stroke-width="1"/>
      <line x1="0" y1="60" x2="800" y2="60" stroke="rgba(255,255,255,0.04)" stroke-width="1"/>
      <line x1="0" y1="90" x2="800" y2="90" stroke="rgba(255,255,255,0.04)" stroke-width="1"/>
      <!-- fill -->
      <path d="M0,90 C100,85 150,70 200,72 C250,74 300,60 350,50 C400,40 430,55 480,45 C530,35 580,20 650,15 C700,12 750,8 800,5 L800,120 L0,120Z"
            fill="url(#fillGrad)"/>
      <!-- line -->
      <path class="chart-line"
            d="M0,90 C100,85 150,70 200,72 C250,74 300,60 350,50 C400,40 430,55 480,45 C530,35 580,20 650,15 C700,12 750,8 800,5"
            fill="none" stroke="url(#lineGrad)" stroke-width="2.5"/>
      <text x="10" y="115" fill="rgba(255,255,255,0.3)" font-size="10" font-family="Tahoma">سال‌های گذشته</text>
      <text x="720" y="15" fill="rgba(231,76,60,0.7)" font-size="10" font-family="Tahoma">اکنون</text>
    </svg>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- CONCEPTS -->
<!-- ══════════════════════════════════════ -->
<section id="s2" class="concepts-bg" style="padding:60px 0">
<div class="section">
  <div class="section-label reveal">بخش دوم · مفاهیم</div>
  <h2 class="section-title reveal">تورم به‌عنوان یک <span>پدیده اقتصادی</span></h2>

  <div class="intro-body">
    <p class="reveal">به گفته فدرال رزرو، تورم زمانی رخ می‌دهد که قیمت کالاها و خدمات به مرور زمان افزایش یابد. این افزایش قیمت از دو مسیر اصلی شکل می‌گیرد: یا تقاضا از عرضه پیشی می‌گیرد، یا هزینه منابع تولید بالا می‌رود و این فشار به قیمت نهایی محصول منتقل می‌شود. به زبان ساده‌تر، تورم یعنی پول شما فردا کمتر از امروز می‌ارزد.</p>
  </div>

  <div class="concept-cards">
    <div class="concept-card reveal">
      <span class="card-icon">🌧️</span>
      <div class="card-title">تورم غیرپولی</div>
      <div class="card-body">این نوع تورم ریشه در دنیای واقعی عرضه و تقاضا دارد، نه در سیاست‌های پولی دولت. وقتی یک رویداد خارجی — مثل خشکسالی، جنگ یا بحران زنجیره تأمین — بازار را مختل می‌کند، قیمت‌ها موقتاً بالا می‌روند. تورم غیرپولی یک پدیده کوتاه‌مدت است و معمولاً با تثبیت بازار خودبه‌خود اصلاح می‌شود.</div>
    </div>
    <div class="concept-card reveal">
      <span class="card-icon">🖨️</span>
      <div class="card-title">تورم پولی</div>
      <div class="card-body">این نوع تورم جدی‌تر و ماندگارتر است. تورم پولی تحریف قیمت‌ها در اثر کاهش ارزش پول است. وقتی دولت پول بیشتری چاپ می‌کند، هر واحد پول ارزش کمتری پیدا می‌کند و همین باعث می‌شود قیمت همه چیز بالا برود. چون ساختاری و سیستماتیک است، آسیب‌های عمیق‌تری به جامعه وارد می‌کند.</div>
    </div>
    <div class="concept-card reveal">
      <span class="card-icon">❄️</span>
      <div class="card-title">تورم منفی (دفلاسیون)</div>
      <div class="card-body">با افزایش ارزش پول، قیمت‌ها کاهش می‌یابند؛ پدیده‌ای که به آن تورم منفی می‌گویند. دولت‌هایی که با کمبود بودجه روبرو هستند، به جای اصلاح ساختار اقتصادی، راه ساده‌تر را انتخاب می‌کنند: چاپ پول. این انتخاب در کوتاه‌مدت مشکل را پنهان می‌کند، اما در بلندمدت قدرت خرید مردم را نابود می‌کند.</div>
    </div>
  </div>

  <div class="compare-bar reveal" id="compareBars">
    <div class="compare-title">مقایسه شدت آسیب انواع تورم بر گروه‌های مختلف</div>
    <div class="bar-row">
      <div class="bar-label"><span>تورم پولی · تأثیر بر فقرا</span><span>۸۷٪</span></div>
      <div class="bar-track"><div class="bar-fill red" data-width="87%"></div></div>
    </div>
    <div class="bar-row">
      <div class="bar-label"><span>تورم پولی · تأثیر بر ثروتمندان</span><span>۳۲٪</span></div>
      <div class="bar-track"><div class="bar-fill gold" data-width="32%"></div></div>
    </div>
    <div class="bar-row">
      <div class="bar-label"><span>تورم غیرپولی · تأثیر بر فقرا</span><span>۵۴٪</span></div>
      <div class="bar-track"><div class="bar-fill blue" data-width="54%"></div></div>
    </div>
  </div>

  <!-- Distrust in currency -->
  <div class="research-card reveal">
    <div class="rc-source">کاهش اعتماد به پول · پیامد تورم مزمن</div>
    <div class="rc-body">
      <p>شاید عمیق‌ترین آسیب تورم پولی، نه در قیمت‌ها، بلکه در ذهن مردم باشد. وقتی تورم مزمن می‌شود، مردم به تدریج اعتماد خود را به پول ملی از دست می‌دهند.</p>
      <p>این بی‌اعتمادی خود را به شکل‌های مختلفی نشان می‌دهد: دلاریزه شدن اقتصاد، سرمایه‌گذاری در دارایی‌های فیزیکی مثل طلا و ملک به جای تولید، و کوتاه شدن افق برنامه‌ریزی — کسی جرأت نمی‌کند برای پنج سال آینده نقشه بکشد.</p>
      <p>این چرخه معیوب است: بی‌اعتمادی به پول، خود تورم را تشدید می‌کند. چون وقتی همه عجله دارند پول را خرج کنند قبل از اینکه ارزشش برود، تقاضا بالا می‌رود و قیمت‌ها بازهم بالاتر می‌روند.</p>
    </div>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- CPI -->
<!-- ══════════════════════════════════════ -->
<section id="s3" class="cpi-bg" style="padding:60px 0">
<div class="section">
  <div class="section-label reveal">بخش سوم · اندازه‌گیری</div>
  <h2 class="section-title reveal">شاخص قیمت مصرف‌کننده <span>(CPI)</span></h2>

  <div class="intro-body">
    <p class="reveal">یکی از ابزارهای اصلی برای اندازه‌گیری تورم، شاخص قیمت مصرف‌کننده یا CPI است. این شاخص تغییر قیمت یک سبد مشخص از کالاها و خدمات — مثل خوراک، مسکن، حمل‌ونقل و بهداشت — را در طول زمان رصد می‌کند.</p>
    <p class="reveal">وقتی شاخص قیمت مصرف‌کننده بالا می‌رود، یعنی همان سبد کالایی که ماه گذشته با چند تومان می‌خریدید، امروز گران‌تر شده. به همین دلیل CPI در واقع دماسنج تورم است — اما مثل هر ابزاری، محدودیت دارد. این شاخص میانگین می‌گیرد و ممکن است فشار واقعی روی خانوارهای کم‌درآمد را که بخش بزرگ‌تری از درآمدشان صرف خوراک و مسکن می‌شود، دست کم نشان دهد.</p>
  </div>

  <!-- CPI basket items -->
  <div class="cpi-visual reveal" id="cpiBasket">
    <div class="cpi-item"><span class="emoji">🍞</span><span class="cpi-name">خوراک</span><span class="cpi-pct">+۴۲٪</span></div>
    <div class="cpi-item"><span class="emoji">🏠</span><span class="cpi-name">مسکن</span><span class="cpi-pct">+۶۱٪</span></div>
    <div class="cpi-item"><span class="emoji">🚌</span><span class="cpi-name">حمل‌ونقل</span><span class="cpi-pct">+۳۸٪</span></div>
    <div class="cpi-item"><span class="emoji">💊</span><span class="cpi-name">بهداشت</span><span class="cpi-pct">+۵۵٪</span></div>
    <div class="cpi-item"><span class="emoji">👕</span><span class="cpi-name">پوشاک</span><span class="cpi-pct">+۲۹٪</span></div>
    <div class="cpi-item"><span class="emoji">📚</span><span class="cpi-name">آموزش</span><span class="cpi-pct">+۴۷٪</span></div>
  </div>

  <!-- Thermometers -->
  <div class="thermometer-wrap reveal" id="thermos">
    <div class="thermo">
      <div class="thermo-tube">
        <div class="thermo-fill red" data-h="90%" style="background:linear-gradient(0deg,#c0392b,#e74c3c)"></div>
      </div>
      <div class="thermo-val" style="color:#e74c3c">بالا</div>
      <div class="thermo-label">تورم مزمن</div>
    </div>
    <div class="thermo">
      <div class="thermo-tube">
        <div class="thermo-fill gold" data-h="55%" style="background:linear-gradient(0deg,#d4ac0d,#f39c12)"></div>
      </div>
      <div class="thermo-val" style="color:#f39c12">متوسط</div>
      <div class="thermo-label">تورم متعارف</div>
    </div>
    <div class="thermo">
      <div class="thermo-tube">
        <div class="thermo-fill blue" data-h="20%" style="background:linear-gradient(0deg,#1a5276,#2980b9)"></div>
      </div>
      <div class="thermo-val" style="color:#3498db">پایین</div>
      <div class="thermo-label">تورم سالم</div>
    </div>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- POVERTY -->
<!-- ══════════════════════════════════════ -->
<section id="s4" class="damage-bg" style="padding:60px 0">
<div class="section">
  <div class="section-label reveal">بخش چهارم · تأثیرات اجتماعی</div>
  <h2 class="section-title reveal">تورم و <span>فقرا</span></h2>

  <!-- People animation -->
  <div class="people-row reveal" id="peopleRow">
    <span class="person-icon">👤</span><span class="person-icon">👤</span>
    <span class="person-icon">👤</span><span class="person-icon">👤</span>
    <span class="person-icon">👤</span><span class="person-icon">👤</span>
    <span class="person-icon">👤</span><span class="person-icon">👤</span>
    <span class="person-icon">👤</span><span class="person-icon">👤</span>
  </div>

  <div class="research-card reveal">
    <div class="rc-source">ایسترلی و فیشر · ۲۰۰۱ · تورم و فقرا</div>
    <div class="rc-body">
      <p>ایسترلی و فیشر (2001) در مقاله «تورم و فقرا» به بررسی این پرسش پرداختند که آیا تورم نسبت به سایر گروه‌های اجتماعی، آسیب بیشتری به اقشار کم‌درآمد وارد می‌کند یا خیر. این پژوهش از دو دسته داده استفاده کرد: نخست داده‌های یک نظرسنجی جهانی شامل ۳۱ هزار و ۸۶۹ نفر در ۳۸ کشور؛ و دوم شاخص‌های عینی اقتصادی شامل سهم درآمدی فقیرترین اقشار، نرخ فقر و حداقل دستمزد واقعی.</p>
      <p>نتایج نشان داد که افراد فقیر بیش از افراد ثروتمند، تورم را یکی از مهم‌ترین مشکلات جامعه تلقی می‌کنند. همچنین افراد کم‌سواد و دارای تحصیلات پایین‌تر نگرانی بیشتری درباره تورم ابراز می‌کنند؛ زیرا این گروه‌ها معمولاً دسترسی کمتری به ابزارهای مالی دارند که بتواند ارزش دارایی‌های آنان را حفظ کند.</p>
      <p>در مجموع، ایسترلی و فیشر نتیجه گرفتند که بار اصلی هزینه‌های تورم بیشتر بر دوش گروه‌های فرودست و کم‌درآمد جامعه قرار می‌گیرد و تورم می‌تواند از طریق کاهش قدرت خرید، افزایش فقر و تشدید نابرابری اقتصادی، وضعیت رفاهی فقرا را تضعیف کند. از این‌رو نتایج این پژوهش از دیدگاهی حمایت می‌کند که تورم را نوعی مالیات پنهان می‌داند که آثار آن بیش از همه متوجه اقشار آسیب‌پذیر جامعه است.</p>
      <p>افزون بر این، پژوهش نشان داد در کشورهایی که نرخ تورم بالاتر است، شهروندان بیشتر با این گزاره موافق‌اند که ثروتمندان ثروتمندتر می‌شوند و فقرا فقیرتر.</p>
    </div>
  </div>

  <div class="stat-row reveal">
    <div class="stat-box">
      <span class="stat-num">۳۸</span>
      <div class="stat-label">کشور مورد بررسی</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">۳۱k</span>
      <div class="stat-label">نفر مشارکت‌کننده</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">↓</span>
      <div class="stat-label">کاهش سهم درآمدی فقرا</div>
    </div>
    <div class="stat-box">
      <span class="stat-num">↑</span>
      <div class="stat-label">افزایش نرخ فقر</div>
    </div>
  </div>

  <div class="key-finding reveal">
    <div class="kf-icon">💡</div>
    <div class="kf-text">افزایش تورم با کاهش سهم درآمدی فقیرترین اقشار جامعه همراه است؛ در شرایط تورمی، سهم فقرا از کل درآمد ملی کاهش می‌یابد، توزیع درآمد نابرابرتر می‌شود و قدرت خرید اقشار کم‌درآمد و مزدبگیر در دوره‌های تورمی کاهش می‌یابد.</div>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- SOCIAL DAMAGE -->
<!-- ══════════════════════════════════════ -->
<section id="s5" style="padding:60px 0; background:linear-gradient(180deg,#120a0a,#0a0f1a)">
<div class="section">
  <div class="section-label reveal">بخش پنجم · پیامدهای اجتماعی</div>
  <h2 class="section-title reveal">تورم و <span>آسیب‌های اجتماعی</span></h2>

  <div class="research-card reveal">
    <div class="rc-source">کمیسیون اروپا · کشورهای نوردیک و بالتیک</div>
    <div class="rc-body">
      <p>در گزارشی با عنوان «تورم و پیامدهای اجتماعی آن: مطالعه کشورهای نوردیک و بالتیک»، پژوهشگران کمیسیون اروپا به بررسی آثار اجتماعی تورم بر گروه‌های مختلف جامعه پرداختند. نویسندگان استدلال می‌کنند که تورم از طریق کاهش قدرت خرید خانوارها، به‌ویژه در میان اقشار کم‌درآمد، زمینه بروز و تشدید انواع آسیب‌های اجتماعی را فراهم می‌سازد.</p>
      <p>یافته‌های گزارش نشان می‌دهد که یکی از مهم‌ترین پیامدهای اجتماعی تورم، افزایش فقر و محرومیت اجتماعی است. با افزایش هزینه‌های زندگی، بسیاری از خانوارها در تأمین نیازهای اساسی خود با دشواری مواجه می‌شوند و این مسئله آنان را در معرض محرومیت مادی و اجتماعی قرار می‌دهد.</p>
      <p>گزارش همچنین به پدیده «طرد اجتماعی» به‌عنوان یکی از پیامدهای مهم تورم اشاره می‌کند. کاهش توان اقتصادی خانوارها می‌تواند موجب محدود شدن حضور آنان در عرصه‌های اجتماعی، فرهنگی و عمومی شود و به تدریج احساس انزوا و کنار گذاشته شدن از جامعه را افزایش دهد.</p>
      <p>یکی دیگر از یافته‌های مهم پژوهش، گسترش «فقر انرژی» در نتیجه افزایش قیمت حامل‌های انرژی است؛ بخشی از خانوارها توانایی تأمین نیازهای اولیه خود در زمینه گرمایش، سرمایش و مصرف انرژی را از دست می‌دهند.</p>
      <p>در نهایت، پژوهشگران نتیجه می‌گیرند که تداوم تورم می‌تواند به تضعیف انسجام اجتماعی منجر شود. افزایش فقر، محرومیت، طرد اجتماعی و نابرابری، زمینه کاهش همبستگی اجتماعی و افزایش شکاف‌های موجود در جامعه را فراهم می‌کند.</p>
    </div>
  </div>

  <div class="key-finding reveal">
    <div class="kf-icon">🇮🇷</div>
    <div class="kf-text">بر اساس آمارهای منتشرشده از سوی مرکز آمار ایران، نرخ سرقت در ایران در سال‌های ۱۳۹۰ الی ۱۴۰۱ رو به افزایش بوده است. در همین حال مشاهده می‌شود که تورم و ضریب جینی نیز عملکردی نامطلوب دارند. در طی پژوهش با به‌کارگیری رویکرد شبیه‌سازی زنجیره مارکوف مونت‌کارلو در چارچوب بیزی اثبات شده است که تورم و نابرابری اقتصادی سبب افزایش جرم سرقت می‌شود.</div>
  </div>

  <div class="concept-cards">
    <div class="concept-card reveal">
      <span class="card-icon">🚫</span>
      <div class="card-title">طرد اجتماعی</div>
      <div class="card-body">کاهش توان اقتصادی خانوارها موجب محدود شدن حضور آنان در عرصه‌های اجتماعی، فرهنگی و عمومی می‌شود و احساس انزوا را افزایش می‌دهد.</div>
    </div>
    <div class="concept-card reveal">
      <span class="card-icon">⚡</span>
      <div class="card-title">فقر انرژی</div>
      <div class="card-body">بخشی از خانوارها توانایی تأمین نیازهای اولیه گرمایش، سرمایش و مصرف انرژی را از دست می‌دهند که پیامدهای رفاهی گسترده‌ای دارد.</div>
    </div>
    <div class="concept-card reveal">
      <span class="card-icon">↕️</span>
      <div class="card-title">تشدید نابرابری</div>
      <div class="card-body">خانوارهای کم‌درآمد سهم بیشتری از درآمد خود را صرف کالاهای ضروری می‌کنند؛ پس افزایش قیمت این کالاها فشار نامتناسبی بر آنان وارد می‌کند.</div>
    </div>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- POLITICAL -->
<!-- ══════════════════════════════════════ -->
<section id="s6" class="political-bg" style="padding:60px 0">
<div class="section">
  <div class="section-label reveal">بخش ششم · پیامدهای سیاسی</div>
  <h2 class="section-title reveal">تورم و <span>آسیب‌های سیاسی</span></h2>

  <div class="intro-body">
    <p class="reveal">زیلسترا (1975) در بررسی پیامدهای اجتماعی و سیاسی تورم، استدلال می‌کند که آثار تورم فراتر از حوزه اقتصاد بوده و می‌تواند ساختارهای سیاسی و حکمرانی جوامع را نیز تحت تأثیر قرار دهد. از دیدگاه وی، تورم مداوم و کنترل‌نشده نه تنها موجب کاهش ارزش پول و افت رفاه اقتصادی می‌شود، بلکه به تدریج اعتماد عمومی به نهادهای اقتصادی و سیاسی را نیز تضعیف می‌کند.</p>
  </div>

  <!-- Trust meters -->
  <div class="trust-meter reveal" id="trustMeters">
    <div class="tm-label">اعتماد عمومی به نهادهای دولتی در شرایط تورمی ↓</div>
    <div class="tm-bar"><div class="tm-fill" data-w="25%" style="background:linear-gradient(90deg,#c0392b,#e74c3c)"></div></div>
    <div class="tm-label">میزان مطالبات اجتماعی از دولت ↑</div>
    <div class="tm-bar"><div class="tm-fill" data-w="82%" style="background:linear-gradient(90deg,#f39c12,#e67e22)"></div></div>
    <div class="tm-label">ثبات سیاسی در کشورهای با تورم بالا ↓</div>
    <div class="tm-bar"><div class="tm-fill" data-w="30%" style="background:linear-gradient(90deg,#1a5276,#2980b9)"></div></div>
  </div>

  <div class="timeline reveal" id="politicalTimeline">
    <div class="tl-item">
      <div class="tl-title">وابستگی به حمایت‌های دولتی</div>
      <div class="tl-body">در شرایط تورمی، گروه‌های مختلف اجتماعی و اقتصادی بیش از گذشته به حمایت‌های دولتی وابسته می‌شوند. افزایش هزینه‌های زندگی و کاهش قدرت خرید سبب می‌شود شهروندان و بنگاه‌های اقتصادی مطالبات بیشتری از دولت داشته باشند.</div>
    </div>
    <div class="tl-item">
      <div class="tl-title">نارضایتی عمومی و بی‌اعتمادی</div>
      <div class="tl-body">هنگامی که افراد احساس کنند سطح زندگی آنان به طور مستمر در حال کاهش است و سیاست‌گذاران توانایی کنترل شرایط اقتصادی را ندارند، اعتماد آنان به کارآمدی دولت و نهادهای سیاسی کاهش می‌یابد.</div>
    </div>
    <div class="tl-item">
      <div class="tl-title">تهدید ثبات سیاسی</div>
      <div class="tl-body">افزایش مطالبات اجتماعی، فشار بر دولت برای مداخله بیشتر در اقتصاد و گسترش نارضایتی عمومی، می‌تواند ظرفیت نظام سیاسی برای مدیریت بحران‌ها را تضعیف کند.</div>
    </div>
    <div class="tl-item">
      <div class="tl-title">فرسایش مشروعیت سیاسی</div>
      <div class="tl-body">در نهایت، زیلسترا نتیجه می‌گیرد که کنترل تورم تنها برای حفظ ثبات اقتصادی ضروری نیست، بلکه از منظر حفظ انسجام سیاسی و اعتماد عمومی نیز اهمیت دارد. تداوم تورم می‌تواند در بلندمدت ثبات سیاسی و اجتماعی جوامع را تهدید کند.</div>
    </div>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- PSYCHOLOGY -->
<!-- ══════════════════════════════════════ -->
<section id="s7" class="psych-bg" style="padding:60px 0">
<div class="section">
  <div class="section-label reveal">بخش هفتم · پیامدهای روانی</div>
  <h2 class="section-title reveal">تورم و <span>آسیب‌های روانی</span></h2>

  <!-- Stress Meter -->
  <div class="stress-meter-wrap reveal">
    <div class="stress-meter">
      <svg viewBox="0 0 200 110">
        <defs>
          <linearGradient id="stressGrad" x1="0" y1="0" x2="1" y2="0">
            <stop offset="0%" stop-color="#2ecc71"/>
            <stop offset="50%" stop-color="#f39c12"/>
            <stop offset="100%" stop-color="#e74c3c"/>
          </linearGradient>
        </defs>
        <!-- bg arc -->
        <path d="M20,100 A80,80 0 0,1 180,100" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="14" stroke-linecap="round"/>
        <!-- colored arc -->
        <path class="stress-arc" d="M20,100 A80,80 0 0,1 180,100" fill="none" stroke="url(#stressGrad)" stroke-width="14" stroke-linecap="round"/>
        <!-- needle -->
        <line class="stress-needle" x1="100" y1="100" x2="100" y2="28" stroke="white" stroke-width="2.5" stroke-linecap="round"/>
        <circle cx="100" cy="100" r="5" fill="white"/>
        <!-- labels -->
        <text x="14" y="118" fill="rgba(255,255,255,0.4)" font-size="9" font-family="Tahoma">آرام</text>
        <text x="162" y="118" fill="rgba(255,255,255,0.4)" font-size="9" font-family="Tahoma">بحران</text>
      </svg>
    </div>
    <div style="font-size:13px;color:rgba(255,255,255,0.5)">سطح استرس اقتصادی در جامعه</div>
  </div>

  <div class="research-card reveal">
    <div class="rc-source">اسمیت و همکاران · ۲۰۲۴ · استرس ناشی از تورم</div>
    <div class="rc-body">
      <p>اسمیت و همکاران (2024) در پژوهشی با عنوان «استرس ناشی از تورم در ایالات متحده آمریکا» به بررسی پیامدهای روانی افزایش قیمت‌ها و فشارهای اقتصادی ناشی از تورم پرداختند. این پژوهش نشان داد که تورم صرفاً یک پدیده اقتصادی نیست، بلکه می‌تواند به عنوان یک عامل استرس‌زای اجتماعی و روانی عمل کرده و سلامت روان افراد را تحت تأثیر قرار دهد.</p>
      <p>نتایج پژوهش نشان داد که استرس ناشی از تورم در میان بخش قابل توجهی از جمعیت مشاهده می‌شود و حتی در شرایطی که نرخ تورم روندی کاهشی پیدا کرده بود، میزان نگرانی و فشار روانی ناشی از افزایش قیمت‌ها همچنان رو به افزایش بوده است. این یافته بیانگر آن است که آثار روانی تورم تنها به نرخ فعلی افزایش قیمت‌ها وابسته نیست.</p>
      <p>گروه‌های کم‌درآمد، افراد دارای ناامنی غذایی، افرادی که بخشی از درآمد خود را از دست داده‌اند و کسانی که با مشکلات اقتصادی بیشتری مواجه هستند، سطوح بالاتری از استرس ناشی از تورم را تجربه می‌کنند.</p>
      <p>پژوهشگران همچنین نشان دادند که فشار اقتصادی ناشی از تورم می‌تواند رفتارهای روزمره افراد را تغییر دهد: کاهش مصرف برخی کالاها، تعویق خریدهای ضروری، افزایش ساعات کار، انجام مشاغل اضافی و حتی به تأخیر انداختن مراقبت‌های درمانی.</p>
      <p>در مجموع، نتایج این پژوهش نشان می‌دهد که تورم دارای پیامدهای مهم روانی و اجتماعی است و می‌تواند از طریق ایجاد استرس اقتصادی، کاهش احساس امنیت مالی و افزایش نگرانی‌های معیشتی، سلامت روان افراد را تضعیف کند.</p>
    </div>
  </div>

  <div class="emotion-grid reveal">
    <div class="emotion-card"><div class="em-icon">😰</div><div class="em-name">اضطراب مزمن</div></div>
    <div class="emotion-card"><div class="em-icon">😞</div><div class="em-name">افسردگی</div></div>
    <div class="emotion-card"><div class="em-icon">😨</div><div class="em-name">احساس ناامنی</div></div>
    <div class="emotion-card"><div class="em-icon">😟</div><div class="em-name">نگرانی مزمن</div></div>
    <div class="emotion-card"><div class="em-icon">😤</div><div class="em-name">تنش خانوادگی</div></div>
    <div class="emotion-card"><div class="em-icon">😶</div><div class="em-name">کاهش رفاه روانی</div></div>
  </div>
</div>
</section>

<div class="page-divider"></div>

<!-- ══════════════════════════════════════ -->
<!-- CONCLUSION -->
<!-- ══════════════════════════════════════ -->
<section id="s8" class="conclusion-bg">
<div class="conclusion-inner reveal">
  <span class="conc-icon">⚖️</span>
  <h2 class="conc-title">تورم، پدیده‌ای فراتر از اقتصاد</h2>
  <div class="conc-body">
    <p>اقتصاد و مشکلات اقتصادی همواره نقشی فراتر از آمار و ارقام صرف در زندگی انسان‌ها ایفا کرده‌اند. تورم نه یک پیامد خنثی، که موتور محرک تضاد طبقاتی و سازوکاری برای بازتولید نابرابری‌های موجود است.</p>
    <p>این نوشته نشان داد که تورم از مسیرهای متعددی آسیب می‌رساند: از طریق کاهش قدرت خرید فقرا، تشدید نابرابری اجتماعی، ایجاد طرد اجتماعی، تضعیف اعتماد سیاسی، و در نهایت آسیب به سلامت روانی جامعه. بار این آسیب‌ها همواره بر دوش گروه‌های آسیب‌پذیرتر سنگین‌تر است.</p>
    <p>از این رو، مقابله با تورم صرفاً یک ضرورت اقتصادی نیست؛ بلکه یک وظیفه اجتماعی، سیاسی و انسانی است.</p>
  </div>
</div>
</section>

<script>
// ── Particles ──
(function(){
  const wrap = document.getElementById('particles');
  for(let i=0;i<30;i++){
    const p = document.createElement('div');
    p.className = 'particle';
    p.style.cssText = `left:${Math.random()*100}%;width:${2+Math.random()*3}px;height:${2+Math.random()*3}px;animation-duration:${6+Math.random()*10}s;animation-delay:${Math.random()*10}s;`;
    wrap.appendChild(p);
  }
})();

// ── Falling numbers ──
(function(){
  const wrap = document.getElementById('falling');
  const nums = ['۱۰٪','۲۵٪','↑','$','تومان','CPI','↑%','تورم'];
  for(let i=0;i<18;i++){
    const el = document.createElement('div');
    el.className = 'fall-num';
    el.textContent = nums[Math.floor(Math.random()*nums.length)];
    el.style.cssText = `left:${Math.random()*100}%;animation-duration:${8+Math.random()*12}s;animation-delay:${Math.random()*12}s;`;
    wrap.appendChild(el);
  }
})();

// ── Scroll reveal ──
const revealEls = document.querySelectorAll('.reveal');
const io = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){ e.target.classList.add('visible'); }
  });
},{threshold:0.12});
revealEls.forEach(el=>io.observe(el));

// ── Timeline items ──
const tlItems = document.querySelectorAll('.tl-item');
const tlObs = new IntersectionObserver((entries)=>{
  entries.forEach((e,i)=>{
    if(e.isIntersecting){
      setTimeout(()=>e.target.classList.add('visible'), i*150);
    }
  });
},{threshold:0.1});
tlItems.forEach(el=>tlObs.observe(el));

// ── Bars ──
function animateBars(container){
  container.querySelectorAll('.bar-fill[data-width]').forEach(b=>{
    b.style.width = b.dataset.width;
  });
}
const barObs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{ if(e.isIntersecting) animateBars(e.target); });
},{threshold:0.3});
const compBars = document.getElementById('compareBars');
if(compBars) barObs.observe(compBars);

// ── Trust meters ──
const tmObs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.querySelectorAll('.tm-fill[data-w]').forEach(f=>{
        f.style.width = f.dataset.w;
      });
    }
  });
},{threshold:0.3});
const tm = document.getElementById('trustMeters');
if(tm) tmObs.observe(tm);

// ── Thermometers ──
const thermoObs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.querySelectorAll('.thermo-fill[data-h]').forEach(f=>{
        f.style.height = f.dataset.h;
      });
    }
  });
},{threshold:0.3});
const thermos = document.getElementById('thermos');
if(thermos) thermoObs.observe(thermos);

// ── People icons ──
const peopleObs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      const icons = e.target.querySelectorAll('.person-icon');
      icons.forEach((ic,i)=>{
        if(i<7) setTimeout(()=>ic.classList.add('affected'),i*120);
      });
    }
  });
},{threshold:0.5});
const pr = document.getElementById('peopleRow');
if(pr) peopleObs.observe(pr);

// ── Nav dots ──
const sections = ['s0','s1','s2','s3','s4','s5','s6','s7','s8'];
function scrollToSection(i){ document.getElementById(sections[i]).scrollIntoView({behavior:'smooth'}); }
const dots = document.querySelectorAll('.pn-dot');
const secObs = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting && e.intersectionRatio>0.4){
      const idx = sections.indexOf(e.target.id);
      if(idx>=0){ dots.forEach(d=>d.classList.remove('active')); if(dots[idx]) dots[idx].classList.add('active'); }
    }
  });
},{threshold:0.4});
sections.forEach(id=>{ const el=document.getElementById(id); if(el) secObs.observe(el); });
</script>
</body>
</html>
