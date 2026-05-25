

<h2 class="sr-only">保險理財規劃工具：輸入年收入、選擇客戶最在意的保障需求，自動產出個人化的專業分析建議與預算配置。</h2>

<style>
.ip-wrap { padding: 1rem 0; }
.ip-hero { background: #1E3A8A; border-radius: var(--border-radius-lg); padding: 1.25rem 1.5rem; margin-bottom: 1rem; }
.ip-hero-badge { display: inline-flex; align-items: center; gap: 5px; background: rgba(255,209,102,0.18); border: 1px solid rgba(255,209,102,0.3); border-radius: 100px; padding: 3px 12px; font-size: 11px; font-weight: 500; color: #FFD166; margin-bottom: 10px; }
.ip-hero h1 { font-size: 18px; font-weight: 500; color: #fff; margin: 0 0 4px; }
.ip-hero p { font-size: 12px; color: rgba(255,255,255,0.55); margin: 0; }
.ip-card { background: var(--color-background-primary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 1rem 1.25rem; margin-bottom: 1rem; }
.ip-card-title { font-size: 13px; font-weight: 500; color: var(--color-text-primary); display: flex; align-items: center; gap: 8px; margin-bottom: 1rem; }
.ip-grid2 { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
@media (max-width: 480px) { .ip-grid2 { grid-template-columns: 1fr; } }
.ip-grid3 { display: grid; grid-template-columns: repeat(3, minmax(0,1fr)); gap: 8px; }
@media (max-width: 480px) { .ip-grid3 { grid-template-columns: 1fr; } }
.ip-label { font-size: 11px; font-weight: 500; color: var(--color-text-secondary); display: block; margin-bottom: 6px; text-transform: uppercase; letter-spacing: 0.04em; }
.ip-mode { display: flex; gap: 6px; }
.ip-mode-btn { flex: 1; padding: 8px; font-size: 12px; font-weight: 500; border: 0.5px solid var(--color-border-secondary); border-radius: var(--border-radius-md); background: var(--color-background-secondary); color: var(--color-text-secondary); cursor: pointer; transition: all 0.15s; }
.ip-mode-btn.on { background: #1E3A8A; color: #fff; border-color: #1E3A8A; }
.ip-stat { background: var(--color-background-secondary); border-radius: var(--border-radius-md); padding: 12px; text-align: center; }
.ip-stat-lbl { font-size: 11px; color: var(--color-text-secondary); margin-bottom: 3px; }
.ip-stat-val { font-size: 20px; font-weight: 500; }
.ip-stat-unit { font-size: 10px; color: var(--color-text-tertiary); margin-top: 1px; }

.ip-focus-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(130px,1fr)); gap: 8px; }
.ip-focus-chip {
  border: 1.5px solid var(--color-border-tertiary);
  border-radius: var(--border-radius-md);
  padding: 10px 10px 8px;
  cursor: pointer;
  transition: all 0.18s;
  text-align: left;
  background: var(--color-background-primary);
  position: relative;
}
.ip-focus-chip:hover { border-color: var(--color-border-secondary); }
.ip-focus-chip.sel { border-width: 2px; }
.ip-focus-chip.navy.sel  { border-color: #1E3A8A; background: #EFF6FF; }
.ip-focus-chip.cyan.sel  { border-color: #0891b2; background: #ECFEFF; }
.ip-focus-chip.amber.sel { border-color: #b45309; background: #FFFBEB; }
.chip-check { position: absolute; top: 7px; right: 8px; width: 16px; height: 16px; border-radius: 50%; border: 1.5px solid var(--color-border-secondary); display: flex; align-items: center; justify-content: center; font-size: 10px; }
.ip-focus-chip.navy.sel  .chip-check { background: #1E3A8A; border-color: #1E3A8A; color: #fff; }
.ip-focus-chip.cyan.sel  .chip-check { background: #0891b2; border-color: #0891b2; color: #fff; }
.ip-focus-chip.amber.sel .chip-check { background: #b45309; border-color: #b45309; color: #fff; }
.chip-icon { font-size: 20px; margin-bottom: 5px; }
.chip-name { font-size: 12px; font-weight: 500; color: var(--color-text-primary); }
.chip-desc { font-size: 11px; color: var(--color-text-secondary); margin-top: 2px; line-height: 1.4; }

.ip-prog-row { margin-bottom: 12px; }
.ip-prog-header { display: flex; justify-content: space-between; align-items: baseline; margin-bottom: 5px; }
.ip-prog-left { display: flex; align-items: center; gap: 6px; }
.ip-prog-name { font-size: 13px; font-weight: 500; color: var(--color-text-primary); }
.ip-prog-sub { font-size: 11px; color: var(--color-text-secondary); }
.ip-prog-amt { font-size: 13px; font-weight: 500; }
.ip-prog-track { height: 7px; background: var(--color-background-secondary); border-radius: 100px; overflow: hidden; }
.ip-prog-fill { height: 100%; border-radius: 100px; transition: width 0.65s cubic-bezier(.4,0,.2,1); width: 0%; }
.ip-boost-badge { font-size: 10px; font-weight: 500; padding: 2px 7px; border-radius: 100px; margin-left: 6px; vertical-align: middle; }

.ip-script { border-radius: var(--border-radius-lg); padding: 1rem 1.25rem; font-size: 13px; line-height: 1.85; color: var(--color-text-primary); border: 0.5px solid var(--color-border-tertiary); background: var(--color-background-secondary); }
.ip-script-section { margin-bottom: 14px; }
.ip-script-section:last-child { margin-bottom: 0; }
.ip-script-head { font-size: 13px; font-weight: 500; margin-bottom: 4px; display: flex; align-items: center; gap: 6px; flex-wrap: wrap; }
.ip-tag { display: inline-block; font-size: 10px; font-weight: 500; padding: 2px 8px; border-radius: 100px; }
.ip-tag.navy  { background: #EFF6FF; color: #1e40af; }
.ip-tag.cyan  { background: #ECFEFF; color: #0e7490; }
.ip-tag.amber { background: #FFFBEB; color: #92400e; }
.ip-tag.focus { background: #dcfce7; color: #15803d; }
.ip-focus-block { border-left: 3px solid; padding: 10px 14px; border-radius: 0 var(--border-radius-md) var(--border-radius-md) 0; margin-top: 8px; margin-bottom: 6px; font-size: 13px; line-height: 1.7; }
.ip-focus-block.navy  { border-color: #1E3A8A; background: #EFF6FF; color: #1e3a8a; }
.ip-focus-block.cyan  { border-color: #0891b2; background: #ECFEFF; color: #0e7490; }
.ip-focus-block.amber { border-color: #b45309; background: #FFFBEB; color: #92400e; }
.ip-warn { background: var(--color-background-danger); border: 0.5px solid var(--color-border-danger); border-radius: var(--border-radius-md); padding: 9px 12px; font-size: 12px; color: var(--color-text-danger); margin-top: 10px; }
.ip-cta { display: flex; align-items: center; justify-content: center; gap: 8px; width: 100%; padding: 13px; background: #1E3A8A; color: #fff; border: none; border-radius: var(--border-radius-md); font-size: 14px; font-weight: 500; cursor: pointer; transition: opacity 0.15s; }
.ip-cta:hover { opacity: 0.88; }
.ip-cta2 { display: flex; align-items: center; justify-content: center; gap: 6px; padding: 12px 16px; background: var(--color-background-secondary); color: var(--color-text-secondary); border: 0.5px solid var(--color-border-secondary); border-radius: var(--border-radius-md); font-size: 13px; cursor: pointer; transition: all 0.15s; white-space: nowrap; }
.ip-cta2:hover { color: #1E3A8A; border-color: #1E3A8A; }
.ip-slider-row { display: flex; align-items: center; gap: 10px; margin-bottom: 8px; }
.ip-slider-row label { font-size: 12px; color: var(--color-text-secondary); white-space: nowrap; min-width: 60px; }
.ip-rate-val { font-size: 16px; font-weight: 500; color: #1E3A8A; min-width: 36px; text-align: right; }
.ip-slider-hints { display: flex; justify-content: space-between; font-size: 10px; color: var(--color-text-tertiary); }
</style>

<div class="ip-wrap">

<div class="ip-hero">
  <div class="ip-hero-badge"><i class="ti ti-shield-check" aria-hidden="true"></i> 保險理財精算工具</div>
  <h1>專屬保險預算智能規劃</h1>
  <p>依收入結構與客戶需求，精算個人化保費配置與專業建議</p>
</div>

<div class="ip-card">
  <div class="ip-card-title"><i class="ti ti-user" aria-hidden="true"></i> 基本資料</div>
  <div class="ip-grid2" style="margin-bottom:12px;">
    <div>
      <label class="ip-label">客戶姓名／稱呼</label>
      <input type="text" id="clientName" placeholder="例：陳先生" oninput="calc()" style="width:100%;" />
    </div>
    <div>
      <label class="ip-label">規劃模式</label>
      <div class="ip-mode">
        <button class="ip-mode-btn on" id="btnS" onclick="setMode('single')">個人</button>
        <button class="ip-mode-btn" id="btnD" onclick="setMode('dual')">雙薪</button>
      </div>
    </div>
  </div>
  <div id="sinBlock">
    <label class="ip-label">年收入</label>
    <div style="display:flex;align-items:center;gap:8px;">
      <input type="number" id="inc1" value="100" min="1" max="9999" step="1" oninput="calc()" style="flex:1;" />
      <span style="font-size:13px;color:var(--color-text-secondary);white-space:nowrap;">萬元 / 年</span>
    </div>
  </div>
  <div id="dualBlock" style="display:none;">
    <div class="ip-grid2">
      <div>
        <label class="ip-label">本人年收入（萬）</label>
        <input type="number" id="inc2a" value="80" min="1" step="1" oninput="calc()" style="width:100%;" />
      </div>
      <div>
        <label class="ip-label">配偶年收入（萬）</label>
        <input type="number" id="inc2b" value="60" min="1" step="1" oninput="calc()" style="width:100%;" />
      </div>
    </div>
  </div>
</div>

<div class="ip-card">
  <div class="ip-card-title"><i class="ti ti-chart-bar" aria-hidden="true"></i> 保費佔比
    <span class="ip-rate-val" id="rateDisp" style="margin-left:auto;">8%</span>
  </div>
  <div class="ip-slider-row">
    <label>保費比例</label>
    <input type="range" id="rateSlider" min="7" max="10" step="1" value="8" oninput="calc()" style="flex:1;" />
  </div>
  <div class="ip-slider-hints"><span>7% 保守</span><span>8% 建議</span><span>10% 完整</span></div>
</div>

<div class="ip-card">
  <div class="ip-card-title"><i class="ti ti-target" aria-hidden="true"></i> 客戶最在意的保障需求
    <span style="font-size:11px;color:var(--color-text-secondary);font-weight:400;margin-left:4px;">可複選，將影響話術與配置比重</span>
  </div>
  <div class="ip-focus-grid">
    <div class="ip-focus-chip navy" id="chip-med" onclick="toggleFocus('med')">
      <div class="chip-check" id="chk-med"></div>
      <div class="chip-icon">🏥</div>
      <div class="chip-name">醫療保障</div>
      <div class="chip-desc">自費手術、癌症治療、長期住院</div>
    </div>
    <div class="ip-focus-chip cyan" id="chip-ltc" onclick="toggleFocus('ltc')">
      <div class="chip-check" id="chk-ltc"></div>
      <div class="chip-icon">🦽</div>
      <div class="chip-name">長照失能</div>
      <div class="chip-desc">失能照護、收入中斷、家庭負擔</div>
    </div>
    <div class="ip-focus-chip amber" id="chip-life" onclick="toggleFocus('life')">
      <div class="chip-check" id="chk-life"></div>
      <div class="chip-icon">🛡️</div>
      <div class="chip-name">壽險意外</div>
      <div class="chip-desc">家庭責任、房貸、子女教育</div>
    </div>
  </div>
  <div style="margin-top:10px;font-size:11px;color:var(--color-text-tertiary);">
    <i class="ti ti-info-circle" aria-hidden="true" style="font-size:13px;vertical-align:-2px;margin-right:3px;"></i>
    未選擇時以標準 40/30/30 配置呈現；選擇後系統自動調高該區塊比重並強化對應話術
  </div>
</div>

<div id="resultSection" style="display:none;">

  <div class="ip-card">
    <div class="ip-card-title"><i class="ti ti-calculator" aria-hidden="true"></i> 精算結果</div>
    <div class="ip-grid3">
      <div class="ip-stat">
        <div class="ip-stat-lbl">年收入合計</div>
        <div class="ip-stat-val" id="sIncome" style="color:var(--color-text-primary);">—</div>
        <div class="ip-stat-unit">萬元</div>
      </div>
      <div class="ip-stat">
        <div class="ip-stat-lbl">建議年保費</div>
        <div class="ip-stat-val" id="sBudget" style="color:#1E3A8A;">—</div>
        <div class="ip-stat-unit">元 / 年</div>
      </div>
      <div class="ip-stat">
        <div class="ip-stat-lbl">每月保費</div>
        <div class="ip-stat-val" id="sMonthly" style="color:#15803d;">—</div>
        <div class="ip-stat-unit">元 / 月</div>
      </div>
    </div>
  </div>

  <div class="ip-card">
    <div class="ip-card-title"><i class="ti ti-chart-pie" aria-hidden="true"></i> 三大保障配置</div>

    <div id="focusNote" style="display:none;background:var(--color-background-success);border:0.5px solid var(--color-border-success);border-radius:var(--border-radius-md);padding:8px 12px;font-size:12px;color:var(--color-text-success);margin-bottom:14px;">
      <i class="ti ti-adjustments-horizontal" aria-hidden="true" style="font-size:13px;vertical-align:-2px;margin-right:4px;"></i>
      <span id="focusNoteText"></span>
    </div>

    <div class="ip-prog-row">
      <div class="ip-prog-header">
        <div class="ip-prog-left">
          <span style="font-size:15px;">🏥</span>
          <span class="ip-prog-name">醫療防護</span>
          <span class="ip-prog-sub">實支實付・癌症・重大傷病</span>
          <span class="ip-boost-badge" id="badge-med" style="display:none;background:#EFF6FF;color:#1e40af;">重點</span>
        </div>
        <span class="ip-prog-amt" id="amt1" style="color:#1E3A8A;">—</span>
      </div>
      <div class="ip-prog-track">
        <div class="ip-prog-fill" id="bar1" style="background:#1E3A8A;"></div>
      </div>
      <div style="font-size:11px;color:var(--color-text-tertiary);margin-top:3px;text-align:right;" id="pct1"></div>
    </div>

    <div class="ip-prog-row">
      <div class="ip-prog-header">
        <div class="ip-prog-left">
          <span style="font-size:15px;">🦽</span>
          <span class="ip-prog-name">長照失能</span>
          <span class="ip-prog-sub">失能・長照・收入保障</span>
          <span class="ip-boost-badge" id="badge-ltc" style="display:none;background:#ECFEFF;color:#0e7490;">重點</span>
        </div>
        <span class="ip-prog-amt" id="amt2" style="color:#0891b2;">—</span>
      </div>
      <div class="ip-prog-track">
        <div class="ip-prog-fill" id="bar2" style="background:#0891b2;"></div>
      </div>
      <div style="font-size:11px;color:var(--color-text-tertiary);margin-top:3px;text-align:right;" id="pct2"></div>
    </div>

    <div class="ip-prog-row" style="margin-bottom:0;">
      <div class="ip-prog-header">
        <div class="ip-prog-left">
          <span style="font-size:15px;">🛡️</span>
          <span class="ip-prog-name">壽險意外</span>
          <span class="ip-prog-sub">定期壽險・意外險</span>
          <span class="ip-boost-badge" id="badge-life" style="display:none;background:#FFFBEB;color:#92400e;">重點</span>
        </div>
        <span class="ip-prog-amt" id="amt3" style="color:#b45309;">—</span>
      </div>
      <div class="ip-prog-track">
        <div class="ip-prog-fill" id="bar3" style="background:#FFD166;"></div>
      </div>
      <div style="font-size:11px;color:var(--color-text-tertiary);margin-top:3px;text-align:right;" id="pct3"></div>
    </div>
  </div>

  <div id="dualCard" style="display:none;" class="ip-card">
    <div class="ip-card-title"><i class="ti ti-users" aria-hidden="true"></i> 雙方保費建議分配</div>
    <div class="ip-grid2">
      <div class="ip-stat">
        <div class="ip-stat-lbl">本人建議保費</div>
        <div class="ip-stat-val" id="dual1" style="color:#1E3A8A;">—</div>
        <div class="ip-stat-unit" id="dual1r">元 / 年</div>
      </div>
      <div class="ip-stat">
        <div class="ip-stat-lbl">配偶建議保費</div>
        <div class="ip-stat-val" id="dual2" style="color:#0891b2;">—</div>
        <div class="ip-stat-unit" id="dual2r">元 / 年</div>
      </div>
    </div>
  </div>

  <div class="ip-card">
    <div class="ip-card-title">
      <i class="ti ti-message-dots" aria-hidden="true"></i> 專業分析建議
      <span style="margin-left:auto;font-size:10px;background:var(--color-background-info);color:var(--color-text-info);padding:2px 8px;border-radius:100px;font-weight:500;">依需求客製化</span>
    </div>
    <div class="ip-script" id="salesScript"></div>
  </div>

  <div class="ip-card" style="background:var(--color-background-secondary);">
    <div style="text-align:center;margin-bottom:14px;">
      <div style="font-size:15px;font-weight:500;color:var(--color-text-primary);margin-bottom:3px;">準備好深入了解您的保障規劃了嗎？</div>
      <div style="font-size:12px;color:var(--color-text-secondary);">預約一對一免費諮詢，量身打造完整保障計畫</div>
    </div>
    <div style="display:flex;gap:8px;flex-wrap:wrap;">
      <button class="ip-cta" onclick="handleCTA()" style="flex:2;min-width:180px;">
        <i class="ti ti-calendar-plus" aria-hidden="true" style="font-size:16px;"></i>
        立即預約免費諮詢
      </button>
      <button class="ip-cta2" onclick="handleReport()">
        <i class="ti ti-file-analytics" aria-hidden="true" style="font-size:15px;"></i>
        產出完整報告 ↗
      </button>
    </div>
    <div style="text-align:center;font-size:11px;color:var(--color-text-tertiary);margin-top:10px;">
      本次諮詢完全免費・不涉及任何強迫購買・決定權永遠在您手中
    </div>
  </div>

</div>

</div>

<script>
let mode = 'single';
const focus = { med: false, ltc: false, life: false };

function setMode(m) {
  mode = m;
  document.getElementById('sinBlock').style.display = m==='single' ? '' : 'none';
  document.getElementById('dualBlock').style.display = m==='dual' ? '' : 'none';
  document.getElementById('btnS').classList.toggle('on', m==='single');
  document.getElementById('btnD').classList.toggle('on', m==='dual');
  calc();
}

function toggleFocus(k) {
  focus[k] = !focus[k];
  const chip = document.getElementById('chip-'+k);
  const chk  = document.getElementById('chk-'+k);
  if (focus[k]) {
    chip.classList.add('sel');
    chk.innerHTML = '<i class="ti ti-check" aria-hidden="true"></i>';
  } else {
    chip.classList.remove('sel');
    chk.innerHTML = '';
  }
  calc();
}

function fmt(n) { return Math.round(n).toLocaleString('zh-TW'); }

function getAlloc() {
  const keys = Object.keys(focus).filter(k => focus[k]);
  if (keys.length === 0) return { med: 40, ltc: 30, life: 30 };
  const base = { med: 30, ltc: 22, life: 22 };
  const boost = 26;
  const perKey = Math.round(boost / keys.length);
  const alloc = { ...base };
  keys.forEach(k => { alloc[k] += perKey; });
  const total = alloc.med + alloc.ltc + alloc.life;
  if (total !== 100) alloc.med += (100 - total);
  return alloc;
}

function calc() {
  const rate = parseInt(document.getElementById('rateSlider').value);
  document.getElementById('rateDisp').textContent = rate + '%';

  let totalW, a = 0, b = 0;
  if (mode === 'single') {
    totalW = parseFloat(document.getElementById('inc1').value) || 0;
  } else {
    a = parseFloat(document.getElementById('inc2a').value) || 0;
    b = parseFloat(document.getElementById('inc2b').value) || 0;
    totalW = a + b;
  }
  if (totalW <= 0) { document.getElementById('resultSection').style.display = 'none'; return; }

  const budget  = Math.round(totalW * 10000 * rate / 100);
  const monthly = Math.round(budget / 12);
  const alloc   = getAlloc();
  const med  = Math.round(budget * alloc.med  / 100);
  const ltc  = Math.round(budget * alloc.ltc  / 100);
  const life = Math.round(budget * alloc.life / 100);

  document.getElementById('sIncome').textContent  = fmt(totalW);
  document.getElementById('sBudget').textContent  = fmt(budget);
  document.getElementById('sMonthly').textContent = fmt(monthly);
  document.getElementById('amt1').textContent = 'NT$ ' + fmt(med);
  document.getElementById('amt2').textContent = 'NT$ ' + fmt(ltc);
  document.getElementById('amt3').textContent = 'NT$ ' + fmt(life);
  document.getElementById('pct1').textContent = alloc.med  + '%';
  document.getElementById('pct2').textContent = alloc.ltc  + '%';
  document.getElementById('pct3').textContent = alloc.life + '%';

  setTimeout(() => {
    document.getElementById('bar1').style.width = alloc.med  + '%';
    document.getElementById('bar2').style.width = alloc.ltc  + '%';
    document.getElementById('bar3').style.width = alloc.life + '%';
  }, 50);

  ['med','ltc','life'].forEach(k => {
    const badge = document.getElementById('badge-'+k);
    badge.style.display = focus[k] ? 'inline-block' : 'none';
  });

  const focusNote = document.getElementById('focusNote');
  const focusKeys = Object.keys(focus).filter(k => focus[k]);
  if (focusKeys.length > 0) {
    const map = { med:'醫療保障', ltc:'長照失能', life:'壽險意外' };
    const names = focusKeys.map(k => map[k]).join('、');
    document.getElementById('focusNoteText').textContent =
      '已依「' + names + '」強化配置比重，以下建議話術已同步調整';
    focusNote.style.display = '';
  } else {
    focusNote.style.display = 'none';
  }

  if (mode === 'dual' && (a+b) > 0) {
    const d1 = Math.round(budget * a / (a+b));
    const d2 = budget - d1;
    const r1 = Math.round(a/(a+b)*100);
    document.getElementById('dual1').textContent = 'NT$ ' + fmt(d1);
    document.getElementById('dual2').textContent = 'NT$ ' + fmt(d2);
    document.getElementById('dual1r').textContent = '佔家庭預算 ' + r1 + '%';
    document.getElementById('dual2r').textContent = '佔家庭預算 ' + (100-r1) + '%';
    document.getElementById('dualCard').style.display = '';
  } else {
    document.getElementById('dualCard').style.display = 'none';
  }

  buildScript({ budget, monthly, med, ltc, life, rate, totalW, alloc });
  document.getElementById('resultSection').style.display = '';
}

function buildScript({ budget, monthly, med, ltc, life, rate, totalW, alloc }) {
  const name = document.getElementById('clientName').value.trim() || '您';
  const focusKeys = Object.keys(focus).filter(k => focus[k]);
  const hasMed  = focus.med;
  const hasLtc  = focus.ltc;
  const hasLife = focus.life;
  const isCustom = focusKeys.length > 0;
  const isTight = rate <= 7;

  let intro = `${name}，根據您的財務狀況精算，建議年度保費為
    <strong style="color:#1E3A8A;">NT$${fmt(budget)}</strong>（月均約 NT$${fmt(monthly)}）。`;

  if (isCustom) {
    const map = { med:'醫療保障', ltc:'長照失能保障', life:'壽險意外保障' };
    const names = focusKeys.map(k => map[k]).join('和');
    intro += `依據您最在意的<span class="ip-tag focus">${names}</span>，我們已針對性地調整配置比重，以下是為您量身制定的規劃建議。`;
  } else {
    intro += `以下依三大保障黃金比例，為您提供全方位的規劃建議。`;
  }

  let medBlock = `
    <div class="ip-script-section">
      <div class="ip-script-head">
        <span>🏥 醫療防護</span>
        <span class="ip-tag navy">NT$${fmt(med)} / 年</span>
        <span class="ip-tag navy">${alloc.med}%</span>
        ${hasMed ? '<span class="ip-tag focus">您的重點需求</span>' : ''}
      </div>`;

  if (hasMed) {
    medBlock += `<div class="ip-focus-block navy">
      ${name}特別重視醫療保障，這非常有遠見。目前自費醫療費用持續攀升，標靶治療一個療程動輒百萬，實支實付醫療險是轉嫁這類風險最直接的工具。建議優先確認住院日額、手術自費項目上限是否充足，並補強癌症與重大傷病的一次金保障，讓治療過程無後顧之憂。
    </div>`;
  } else {
    medBlock += `<span style="color:var(--color-text-secondary);">台灣癌症發生率每 2 人中即有 1 人，新式治療費用高昂。建議此區塊年配 NT$${fmt(med)}，確保住院與自費手術有完整後盾。</span>`;
  }
  medBlock += `</div>`;

  let ltcBlock = `
    <div class="ip-script-section">
      <div class="ip-script-head">
        <span>🦽 長照失能保障</span>
        <span class="ip-tag cyan">NT$${fmt(ltc)} / 年</span>
        <span class="ip-tag cyan">${alloc.ltc}%</span>
        ${hasLtc ? '<span class="ip-tag focus">您的重點需求</span>' : ''}
      </div>`;

  if (hasLtc) {
    ltcBlock += `<div class="ip-focus-block cyan">
      ${name}提到長照與失能是最大的擔憂，這個風險意識非常成熟。台灣平均需要長照年數達 7.3 年，每月照護費用約 5〜10 萬，是一般家庭最難承受的財務衝擊。建議以失能扶助險為核心，搭配長照險，確保即便因意外或疾病喪失工作能力，每月仍有穩定的保險金維持家庭運作，不讓照護重擔落在摯愛身上。
    </div>`;
  } else {
    ltcBlock += `<span style="color:var(--color-text-secondary);">長照風險往往被低估，卻是一個家庭最難承受的財務衝擊。年配 NT$${fmt(ltc)} 可建立基本的失能與長照保障防線。</span>`;
  }
  ltcBlock += `</div>`;

  let lifeBlock = `
    <div class="ip-script-section">
      <div class="ip-script-head">
        <span>🛡️ 責任意外防護</span>
        <span class="ip-tag amber">NT$${fmt(life)} / 年</span>
        <span class="ip-tag amber">${alloc.life}%</span>
        ${hasLife ? '<span class="ip-tag focus">您的重點需求</span>' : ''}
      </div>`;

  if (hasLife) {
    lifeBlock += `<div class="ip-focus-block amber">
      ${name}重視對家人的責任保障，這正是許多顧問最推崇的保險觀念。定期壽險的核心在於「以最小保費換取最大保額」，確保萬一身故，房貸、子女教育費用與日常生活支出都不會成為家人的負擔。建議以「家庭負債＋未來收入替代」作為保額計算基準，搭配意外險補足日常風險缺口，讓摯愛永遠有依靠。
    </div>`;
  } else {
    lifeBlock += `<span style="color:var(--color-text-secondary);">定期壽險確保家人責任有所依靠，意外險補足日常缺口。年配 NT$${fmt(life)} 可建立基本的責任防護網。</span>`;
  }
  lifeBlock += `</div>`;

  let warnHtml = '';
  if (isTight) {
    warnHtml = `<div class="ip-warn">
      <i class="ti ti-alert-triangle" aria-hidden="true" style="font-size:13px;vertical-align:-2px;margin-right:4px;"></i>
      目前保費比例偏低（${rate}%），建議逐步調升至年收入 8%〜10%，特別是${focusKeys.length > 0 ? '您重視的保障區塊' : '醫療與長照區塊'}，保障缺口風險較高。
    </div>`;
  }

  document.getElementById('salesScript').innerHTML =
    `<div class="ip-script-section">${intro}</div>${medBlock}${ltcBlock}${lifeBlock}${warnHtml}`;
}

function handleCTA() {
  const name = document.getElementById('clientName').value.trim() || '客戶';
  const focusKeys = Object.keys(focus).filter(k => focus[k]);
  const map = { med:'醫療保障', ltc:'長照失能', life:'壽險意外' };
  const focusTxt = focusKeys.length > 0
    ? '（客戶特別重視：' + focusKeys.map(k=>map[k]).join('、') + '）'
    : '';
  sendPrompt(`請幫我用繁體中文，以保險顧問的角色，為客戶「${name}」撰寫一份正式的保險諮詢預約確認信${focusTxt}，包含：感謝對方填寫分析工具、說明三大保障諮詢內容、確認下一步聯繫方式，語氣專業且溫暖。`);
}

function handleReport() {
  const name = document.getElementById('clientName').value.trim() || '客戶';
  const rate = document.getElementById('rateSlider').value;
  const focusKeys = Object.keys(focus).filter(k => focus[k]);
  const map = { med:'醫療保障', ltc:'長照失能', life:'壽險意外' };
  const focusTxt = focusKeys.length > 0
    ? '\n客戶重點需求：' + focusKeys.map(k=>map[k]).join('、')
    : '\n配置模式：標準三大保障均衡配置';
  const totalW = mode === 'single'
    ? (parseFloat(document.getElementById('inc1').value)||0)
    : (parseFloat(document.getElementById('inc2a').value)||0)+(parseFloat(document.getElementById('inc2b').value)||0);
  const budget = Math.round(totalW * 10000 * parseInt(rate) / 100);
  sendPrompt(`請依以下資料，用繁體中文產出一份完整保險財務規劃報告（含摘要、三大保障說明、針對重點需求的深度建議、常見問答）：\n客戶：${name}\n年收入：${totalW}萬\n建議年保費：NT$${fmt(budget)}（保費比 ${rate}%）${focusTxt}`);
}

calc();
</script>
