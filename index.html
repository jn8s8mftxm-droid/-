<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>有機化学バトルフィールド</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0;user-select:none;-webkit-tap-highlight-color:transparent;font-family:"Hiragino Sans","Noto Sans JP",-apple-system,sans-serif}
body,html{width:100%;height:100%;overflow:hidden;background:#05080f;color:#e8eef7}
.screen{display:none;width:100%;height:100%;position:absolute;top:0;left:0}
.active{display:flex;flex-direction:column}
.glass-btn{background:linear-gradient(145deg,rgba(56,189,248,.28),rgba(99,102,241,.35));border:1px solid rgba(148,163,184,.35);color:#f1f5f9;padding:10px 16px;font-size:13px;border-radius:10px;cursor:pointer;min-width:72px;text-align:center}
.glass-btn:active{transform:scale(.97)}.glass-btn:disabled{opacity:.4}
.glass-btn.primary{background:linear-gradient(145deg,#0ea5e9,#6366f1)}.glass-btn.danger{background:linear-gradient(145deg,#ef4444,#b91c1c)}
.glass-btn.success{background:linear-gradient(145deg,#10b981,#059669)}.glass-btn.warn{background:linear-gradient(145deg,#f59e0b,#d97706)}
.glass-btn.pink{background:linear-gradient(145deg,#ec4899,#a855f7)}.glass-btn.slate{background:linear-gradient(145deg,#475569,#334155)}
.glass-btn.orange{background:linear-gradient(145deg,#ea580c,#ef4444)}.glass-btn.wide{width:100%;min-width:0}
.mini-btn{padding:9px 12px;font-size:12px;min-width:68px}
#deck-select-screen{background:radial-gradient(ellipse at 30% 20%,#1e3a5f,#0b1220 50%,#05080f);padding:36px 20px;align-items:center;gap:16px;text-align:center}
#deck-select-screen h2{font-size:22px;background:linear-gradient(90deg,#7dd3fc,#a5b4fc);-webkit-background-clip:text;-webkit-text-fill-color:transparent}
.select-card{border-radius:16px;padding:16px;margin-bottom:12px;text-align:left;cursor:pointer;width:100%;max-width:400px;border:1px solid rgba(255,255,255,.12);color:#fff}
.select-card.purple{background:linear-gradient(135deg,#5b21b6,#1d4ed8)}.select-card.red{background:linear-gradient(135deg,#c2410c,#b91c1c)}.select-card.green{background:linear-gradient(135deg,#047857,#0f766e)}
.badge{display:inline-block;background:rgba(255,255,255,.18);font-size:10px;padding:3px 8px;border-radius:999px}
#field-screen{position:relative}#canvas-container{width:100%;height:100%}
.field-ui{position:absolute;top:0;left:0;width:100%;padding:24px 10px 0;display:flex;justify-content:space-between;align-items:flex-start;pointer-events:none;z-index:5;gap:8px}
.field-ui *{pointer-events:auto}
.status-box{background:rgba(8,12,22,.78);padding:12px 14px;border-radius:14px;font-size:13px;border:1px solid rgba(148,163,184,.25);min-width:140px}
.field-btns{display:flex;flex-direction:row;flex-wrap:wrap;gap:6px;justify-content:flex-end;max-width:55%}
#field-menu{display:none;position:absolute;top:0;left:0;width:100%;height:100%;background:rgba(0,0,0,.55);z-index:30;align-items:center;justify-content:center;touch-action:none}
#field-menu .menu-panel{background:rgba(15,23,42,.97);border:1px solid rgba(148,163,184,.4);border-radius:16px;padding:18px 16px;width:90%;max-width:340px;display:flex;flex-direction:column;gap:8px;max-height:80vh;overflow-y:auto;touch-action:pan-y}
.menu-label{font-size:11px;color:#94a3b8;margin-top:4px}
/* ボスプレビュー（ぽけとる風） */
#boss-preview-screen{background:radial-gradient(ellipse at 50% 20%,#2e1065,#0f172a 45%,#020617);justify-content:space-between;padding:0;z-index:40}
.boss-top{margin:28px 16px 0;background:linear-gradient(180deg,#bbf7d0,#86efac);border-radius:18px;border:4px solid #78350f;padding:16px;text-align:center;color:#14532d;box-shadow:0 8px 24px rgba(0,0,0,.4)}
.boss-top .boss-title{font-size:13px;color:#92400e;margin-bottom:6px}
.boss-top .boss-name{font-size:20px;font-weight:700;margin:8px 0}
.boss-weak-tag{display:inline-block;background:#a855f7;color:#fff;font-size:12px;padding:4px 12px;border-radius:999px;margin:4px}
.boss-stat{font-size:14px;margin-top:8px;line-height:1.6}
.boss-bottom{padding:16px;display:flex;gap:10px;align-items:center;background:rgba(15,23,42,.85)}
.boss-bottom .glass-btn{flex:1;padding:16px 8px;font-size:14px;border-radius:14px}
#battle-screen{background:radial-gradient(ellipse at 50% 0%,#1e293b,#0f172a 40%,#020617);padding:12px;justify-content:space-between}
.battle-header{display:flex;justify-content:space-between;margin-bottom:6px}
#lab-canvas-container{width:100%;height:140px;border-radius:14px;overflow:hidden;border:1px solid rgba(56,189,248,.35);background:#071018}
.battle-log-box{background:rgba(15,23,42,.9);border:1px solid rgba(71,85,105,.6);border-radius:12px;padding:10px;min-height:52px;font-size:12px;text-align:center;display:flex;align-items:center;justify-content:center;white-space:pre-line;margin:6px 0}
.quiz-box{background:rgba(88,28,135,.45);border:1px solid rgba(192,132,252,.5);border-radius:12px;padding:12px;text-align:center;display:flex;flex-direction:column;gap:8px}
.quiz-options{display:grid;grid-template-columns:1fr 1fr;gap:6px}
.quiz-btn{background:linear-gradient(145deg,#2563eb,#4338ca);border:none;color:#fff;padding:10px;border-radius:10px;font-size:12px;cursor:pointer;width:100%}
.hand-container{overflow-x:auto;display:flex;gap:8px;padding:4px 0}
.card{min-width:84px;width:84px;height:118px;border-radius:12px;padding:6px;display:flex;flex-direction:column;justify-content:space-between;cursor:pointer;background:linear-gradient(160deg,#fff,#f1f5f9);color:#0f172a}
.card.selected{background:linear-gradient(160deg,#fef08a,#fde047);box-shadow:0 0 0 2px #facc15;transform:translateY(-5px)}
.card-rarity{font-size:8px;padding:2px 5px;border-radius:4px;color:#fff;width:fit-content}
.rarity-SSR{background:#f97316}.rarity-SR{background:#a855f7}.rarity-R{background:#3b82f6}
.rarity-SSSR{background:linear-gradient(90deg,#ff006e,#8338ec)}.rarity-ORIGIN{background:linear-gradient(90deg,#14b8a6,#0ea5e9)}
.card-attr{font-size:8px;color:#64748b}.card-dmg{font-size:9px;color:#dc2626}.card-heal{font-size:9px;color:#16a34a}
.battle-actions{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;margin-top:4px}
.choice-box{display:none;position:absolute;left:50%;top:36%;transform:translate(-50%,-50%);width:86%;max-width:320px;z-index:50;background:rgba(15,23,42,.97);border:1px solid #fbbf24;border-radius:16px;padding:16px;text-align:center;flex-direction:column;gap:10px}
#deck-edit-screen,#gacha-screen,#zukan-screen,#achieve-screen,#history-screen,#quiz-only-screen,#isomer-screen,#lab-screen,#refine-screen,#synth-screen,#tree-screen{background:linear-gradient(180deg,#0f172a,#020617);padding:24px 12px 12px;overflow:hidden}
.deck-list{flex:1;overflow-y:auto;max-height:30vh;margin-top:6px}
.deck-item{display:flex;justify-content:space-between;align-items:center;background:rgba(30,41,59,.85);padding:8px 10px;margin-bottom:5px;border-radius:10px;border:1px solid rgba(71,85,105,.4)}
.deck-item.in-deck{border-color:rgba(52,211,153,.4);background:rgba(16,185,129,.12)}
.action-btn{background:none;border:none;font-size:15px;cursor:pointer;padding:3px}
.info-box{background:rgba(15,23,42,.9);border:1px solid rgba(71,85,105,.5);border-radius:12px;padding:10px;margin-top:6px;overflow-y:auto;font-size:11px}
.synth-bar-wrap{background:rgba(30,41,59,.9);border-radius:10px;padding:10px;margin:6px 0;border:1px solid rgba(56,189,248,.25)}
.synth-bar-bg{height:8px;background:#1e293b;border-radius:999px;overflow:hidden;margin-top:6px}
.synth-bar-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,#22d3ee,#818cf8)}
.preset-row{display:flex;gap:6px;flex-wrap:wrap;margin:4px 0;align-items:center}
.preset-row input,.synth-input{background:#0f172a;border:1px solid #475569;border-radius:8px;color:#e2e8f0;padding:8px 10px;font-size:12px}
.scroll-panel{flex:1;overflow-y:auto;background:rgba(15,23,42,.85);border:1px solid rgba(71,85,105,.45);border-radius:12px;padding:12px;font-size:12px;line-height:1.55;color:#cbd5e1;margin:8px 0}
.zukan-item{background:rgba(30,41,59,.8);border-radius:10px;padding:10px;margin-bottom:7px;border-left:3px solid #38bdf8}
.achieve-item{background:rgba(30,41,59,.8);border-radius:10px;padding:10px;margin-bottom:7px;display:flex;justify-content:space-between}
.achieve-item.done{border-left:3px solid #22c55e}.achieve-item.locked{opacity:.55}
.gacha-card-view{width:230px;height:160px;border-radius:14px;border:1px solid rgba(168,85,247,.45);background:rgba(88,28,135,.3);display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:12px;margin:8px auto}
.gacha-card-view.rolling{animation:gachaShake .12s linear infinite}
.gacha-card-view.reveal{animation:gachaPop .45s ease-out}
@keyframes gachaShake{0%{transform:translateX(0)}25%{transform:translateX(-4px)}75%{transform:translateX(4px)}100%{transform:translateX(0)}}
@keyframes gachaPop{0%{transform:scale(.6);opacity:.3}100%{transform:scale(1);opacity:1}}
.longpress-popup,#pool-modal,#rec-modal{display:none;position:fixed;left:50%;top:50%;transform:translate(-50%,-50%);width:88%;max-width:340px;background:rgba(15,23,42,.98);border:1px solid #38bdf8;border-radius:16px;padding:16px;z-index:100;max-height:70vh;overflow-y:auto}
.filter-row,.row-btns{display:flex;gap:6px;flex-wrap:wrap;margin:8px 0;align-items:center}
.row-btns .glass-btn{flex:1;min-width:80px}
.gacha-type-card{background:rgba(30,41,59,.9);border:1px solid rgba(71,85,105,.5);border-radius:12px;padding:12px;margin-bottom:8px}
.gacha-type-card h4{color:#e879f9;font-size:14px;margin-bottom:4px}
.gacha-type-card p{font-size:11px;color:#94a3b8;line-height:1.45}
.gacha-actions{display:flex;gap:6px;margin-top:8px}.gacha-actions .glass-btn{flex:1}
.memo-card{background:rgba(15,23,42,.95);border:1px solid rgba(56,189,248,.4);border-radius:14px;padding:16px;margin:8px 0;min-height:160px;text-align:center}
.memo-hidden{filter:blur(6px)}
.pool-line{display:flex;justify-content:space-between;padding:6px 0;border-bottom:1px solid rgba(71,85,105,.4);font-size:12px}
.tree-node{background:rgba(30,41,59,.9);border-radius:12px;padding:12px;margin-bottom:10px;border-left:4px solid #475569}
.tree-node.done{border-left-color:#22c55e;background:rgba(16,185,129,.12)}
.atom-palette{display:flex;flex-wrap:wrap;gap:6px;margin:6px 0}
.atom-btn{width:48px;height:48px;border-radius:50%;border:2px solid #64748b;background:#1e293b;color:#fff;font-size:13px;font-weight:600;cursor:pointer;display:flex;flex-direction:column;align-items:center;justify-content:center;line-height:1.1}
.atom-btn small{font-size:9px;opacity:.75;font-weight:400}
.atom-btn.C{border-color:#94a3b8;background:#334155}.atom-btn.H{border-color:#e2e8f0;background:#475569}
.atom-btn.O{border-color:#f87171;background:#7f1d1d}.atom-btn.N{border-color:#60a5fa;background:#1e3a5f}
.atom-btn.Cl{border-color:#4ade80;background:#14532d}.atom-btn.S{border-color:#fbbf24;background:#78350f}
.atom-btn.P{border-color:#f472b6;background:#9d174d}
.atom-btn.FG{border-color:#e879f9;background:#581c87;width:auto;padding:0 10px;border-radius:12px;height:40px}
#mol-canvas-wrap{position:relative;width:100%;height:220px;background:#0b1220;border:1px solid #334155;border-radius:12px;overflow:hidden;margin:8px 0}
#mol-canvas{width:100%;height:100%;display:block}
.mol-hint{font-size:11px;color:#94a3b8;line-height:1.45}
.bond-mode{background:rgba(56,189,248,.2);border-color:#38bdf8}
.attr-chip{font-size:11px;padding:6px 10px;border-radius:999px;border:1px solid #475569;background:#1e293b;color:#cbd5e1;cursor:pointer}
.attr-chip.on{background:#0ea5e9;border-color:#38bdf8;color:#fff}
</style>
</head>
<body>

<div id="deck-select-screen" class="screen active">
  <h2>有機化学バトルフィールド</h2>
  <p style="font-size:13px;color:#94a3b8">スターターデッキを選択</p>
  <div style="width:100%;max-width:400px">
    <div class="select-card purple" onclick="assignStarterDeck('Aromatic')"><span class="badge">芳香族</span><h3 style="margin:6px 0;font-size:16px">芳香族・置換反応デッキ</h3></div>
    <div class="select-card red" onclick="assignStarterDeck('Polymer')"><span class="badge">付加・高分子</span><h3 style="margin:6px 0;font-size:16px">付加・高分子デッキ</h3></div>
    <div class="select-card green" onclick="assignStarterDeck('Redox')"><span class="badge">酸化・エステル</span><h3 style="margin:6px 0;font-size:16px">酸化・エステル</h3></div>
  </div>
</div>

<div id="field-screen" class="screen">
  <div id="canvas-container"></div>
  <div class="field-ui">
    <div class="status-box">
      <div>🧪 試薬: <span id="field-reagents">150</span></div>
      <div style="color:#4ade80;margin-top:2px">❤️ HP: <span id="field-hp">200</span></div>
      <div style="color:#fbbf24;font-size:12px;margin-top:2px">🎓 <span id="field-rank">初学者</span> Lv.<span id="field-plv">1</span></div>
      <div style="font-size:10px;color:#94a3b8">経験 <span id="field-pexp">0</span>/<span id="field-pnext">30</span> · 撃破 <span id="field-kills">0</span></div>
      <div style="color:#67e8f9;font-size:11px;margin-top:2px">🏠 研究室 Lv.<span id="field-lab">1</span></div>
      <div id="daily-hint" style="font-size:10px;color:#a5b4fc;margin-top:5px"></div>
      <div id="zukan-comp-hint" style="font-size:10px;color:#86efac;margin-top:2px"></div>
      <div id="tree-hint" style="font-size:10px;color:#f9a8d4;margin-top:2px"></div>
    </div>
    <div class="field-btns">
      <button type="button" class="glass-btn mini-btn success" onclick="saveGame()">セーブ</button>
      <button type="button" class="glass-btn mini-btn primary" onclick="loadGame()">ロード</button>
      <button type="button" class="glass-btn mini-btn" onclick="startPractice()">練習</button>
      <button type="button" class="glass-btn mini-btn warn" onclick="openFieldMenu()">メニュー</button>
    </div>
  </div>
  <div id="field-menu">
    <div class="menu-panel">
      <div style="text-align:center;color:#fbbf24;font-size:15px;margin-bottom:4px">メニュー</div>
      <div class="menu-label">編成・ガチャ・合成</div>
      <button type="button" class="glass-btn primary wide" onclick="menuGo('deckEdit')">デッキ編集</button>
      <button type="button" class="glass-btn pink wide" onclick="menuGo('gacha')">ガチャ</button>
      <button type="button" class="glass-btn slate wide" onclick="menuGo('refine')">精製</button>
      <button type="button" class="glass-btn success wide" onclick="menuGo('synth')">分子ビルダー</button>
      <div class="menu-label">図鑑・実績・反応</div>
      <button type="button" class="glass-btn warn wide" onclick="menuGo('zukan')">図鑑（暗記シート）</button>
      <button type="button" class="glass-btn success wide" onclick="menuGo('achieve')">実績</button>
      <button type="button" class="glass-btn pink wide" onclick="menuGo('tree')">反応ツリー</button>
      <button type="button" class="glass-btn primary wide" onclick="menuGo('lab')">研究室</button>
      <div class="menu-label">学習</div>
      <button type="button" class="glass-btn wide" onclick="menuGoQuiz()">クイズ</button>
      <button type="button" class="glass-btn pink wide" onclick="menuGoIsomer()">異性体</button>
      <button type="button" class="glass-btn slate wide" style="margin-top:8px" onclick="closeFieldMenu(true)">閉じる</button>
    </div>
  </div>
</div>

<!-- ボス遭遇プレビュー（ぽけとる風） -->
<div id="boss-preview-screen" class="screen">
  <div class="boss-top">
    <div class="boss-title">⚔ BOSS ENCOUNTER</div>
    <div id="bp-weak-tags"></div>
    <div class="boss-name" id="bp-name">ボス</div>
    <div class="boss-stat">
      HP <span id="bp-hp">900</span><br>
      攻撃力 <span id="bp-atk">30</span><br>
      <span id="bp-cond"></span><br>
      <span id="bp-turn"></span>
    </div>
  </div>
  <div style="flex:1;display:flex;align-items:center;justify-content:center">
    <div style="font-size:64px;filter:drop-shadow(0 0 20px #a855f7)">👾</div>
  </div>
  <div class="boss-bottom">
    <button type="button" class="glass-btn slate" onclick="cancelBossPreview()">やめる</button>
    <button type="button" class="glass-btn orange" onclick="confirmBossBattle()">挑戦する</button>
    <button type="button" class="glass-btn primary" onclick="bossPreviewToDeck()">デッキ編集</button>
  </div>
</div>

<div id="battle-screen" class="screen">
  <div class="battle-header">
    <div>
      <div style="color:#4ade80">🧑 HP: <span id="battle-player-hp">200</span></div>
      <div style="color:#38bdf8;font-size:11px">📚 山札: <span id="battle-deck-count">0</span></div>
      <div id="combo-status" style="font-size:11px;color:#fbbf24">🔗 連鎖コンボ: 0</div>
      <div id="next-bonus" style="font-size:11px;color:#fbbf24;display:none">次ターン火力UP</div>
      <div id="dot-status" style="font-size:11px;color:#f87171;display:none">☠️ 毒素DoT</div>
      <div id="turn-limit" style="font-size:11px;color:#f472b6;display:none"></div>
    </div>
    <div style="text-align:right">
      <div style="font-size:12px;color:#94a3b8">👾 <span id="monster-name">敵</span> Lv.<span id="monster-level">1</span></div>
      <div style="color:#f87171;font-size:15px"><span id="monster-hp">500</span>/<span id="monster-maxhp">500</span></div>
      <div id="monster-exp" style="font-size:10px;color:#a3e635"></div>
      <div id="monster-weak" style="font-size:10px;color:#fb923c"></div>
      <div id="monster-cond" style="font-size:10px;color:#e879f9"></div>
    </div>
  </div>
  <div id="lab-canvas-container"></div>
  <div id="battle-log" class="battle-log-box">バトル開始</div>
  <div>
    <div style="font-size:10px;color:#94a3b8">手札 (<span id="hand-count">0</span>/7) 長押しで反応</div>
    <div id="hand-cards" class="hand-container"></div>
  </div>
  <div class="battle-actions">
    <button type="button" id="attack-btn" class="glass-btn orange" style="flex:1.4" onclick="executePlayerAttack()">化学反応実行</button>
    <button type="button" id="skip-btn" class="glass-btn slate" onclick="skipTurn()">ターン終了</button>
    <button type="button" id="flee-btn" class="glass-btn danger" onclick="fleeBattle()">逃げる</button>
    <button type="button" class="glass-btn" onclick="openHistory()">履歴</button>
  </div>
  <div id="choice-box" class="choice-box">
    <div style="color:#fbbf24" id="choice-title">中間物質</div>
    <div id="choice-desc" style="font-size:13px;margin:8px 0"></div>
    <div style="display:flex;gap:10px;justify-content:center">
      <button type="button" class="glass-btn orange" onclick="chooseAttack()">攻撃する</button>
      <button type="button" class="glass-btn success" onclick="chooseAddToHand()">手札に加える</button>
    </div>
  </div>
</div>

<div id="quiz-only-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center"><h3 style="color:#c4b5fd">📝 クイズ</h3><button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button></div>
  <p style="font-size:12px;color:#94a3b8;margin:8px 0">正解 <span id="qo-score">0</span> / <span id="qo-total">0</span></p>
  <div class="quiz-box" style="display:flex;margin-top:12px"><div id="qo-question"></div><div id="qo-options" class="quiz-options"></div><div id="qo-feedback" style="font-size:12px;color:#fbbf24;min-height:20px"></div></div>
  <button type="button" class="glass-btn primary wide" style="margin-top:12px" onclick="nextQuizOnly()">次の問題</button>
</div>
<div id="isomer-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center"><h3 style="color:#f9a8d4">🔀 異性体</h3><button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button></div>
  <p style="font-size:12px;color:#fbbf24;margin:8px 0">スコア <span id="iso-score">0</span>　連続 <span id="iso-streak">0</span></p>
  <div class="quiz-box" style="display:flex;margin-top:12px"><div id="iso-question"></div><div id="iso-options" class="quiz-options"></div><div id="iso-feedback" style="font-size:12px;color:#fbbf24;min-height:24px"></div></div>
  <button type="button" class="glass-btn pink wide" style="margin-top:12px" onclick="nextIsomerQ()">次の問題</button>
</div>
<div id="lab-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center"><h3 style="color:#67e8f9">🏠 研究室</h3><button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button></div>
  <div class="scroll-panel">
    <div>レベル <span id="lab-lv">1</span> / 10</div>
    <div class="synth-bar-bg" style="margin-top:8px"><div id="lab-bar" class="synth-bar-fill" style="width:0%"></div></div>
    <div style="font-size:11px;color:#94a3b8;margin-top:6px">経験 <span id="lab-exp">0</span> / <span id="lab-next">30</span></div>
    <div id="lab-perks" style="margin-top:12px;line-height:1.7;font-size:12px"></div>
    <button type="button" id="lab-free-gacha-btn" class="glass-btn pink wide" style="margin-top:14px" onclick="labFreeGacha()">今日の無料ガチャ</button>
    <div id="lab-msg" style="font-size:12px;color:#fbbf24;margin-top:8px"></div>
  </div>
</div>
<div id="refine-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center"><h3 style="color:#fbbf24">✨ 精製</h3><button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button></div>
  <p style="font-size:12px;color:#94a3b8;margin:8px 0">同名3枚→精製（×1.15）</p>
  <div id="refine-list" class="scroll-panel"></div>
</div>
<div id="synth-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#2dd4bf">🧬 分子ビルダー</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <p class="mol-hint">原子を置き結合でつなぐ。手が余っているとカード化不可。ダメージ50〜300／試薬100〜1000。</p>
  <p style="font-size:12px;color:#94a3b8">試薬 <span id="synth-reagents">150</span></p>
  <div class="menu-label">パーツ</div>
  <div class="atom-palette" id="atom-palette"></div>
  <div class="row-btns">
    <button type="button" id="bond-mode-btn" class="glass-btn mini-btn primary" onclick="toggleBondMode()">結合モード: OFF</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="undoMol()">1つ戻す</button>
    <button type="button" class="glass-btn mini-btn danger" onclick="clearMol()">全消去</button>
  </div>
  <div id="mol-canvas-wrap"><canvas id="mol-canvas"></canvas></div>
  <div id="mol-status" style="font-size:12px;color:#cbd5e1;min-height:48px"></div>
  <input id="orig-name" class="synth-input" style="width:100%" placeholder="カード名（空欄で自動）" maxlength="20">
  <button type="button" class="glass-btn success wide" style="margin-top:8px" onclick="createOriginalCard()">分子をカード化</button>
  <div id="synth-msg" style="font-size:12px;color:#fbbf24;margin-top:8px"></div>
</div>
<div id="tree-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#f9a8d4">🌳 反応ツリー (<span id="tree-done">0</span>/<span id="tree-total">0</span>)</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <div id="tree-list" class="scroll-panel"></div>
</div>
<div id="history-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px">
    <h3 style="color:#c4b5fd">📜 履歴</h3>
    <div class="row-btns"><button type="button" class="glass-btn" onclick="showLastReplay()">直前リプレイ</button><button type="button" class="glass-btn slate" onclick="closeHistory()">戻る</button></div>
  </div>
  <div id="history-list" class="scroll-panel" style="white-space:pre-line"></div>
</div>
<div id="zukan-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center"><h3 style="color:#fbbf24">📘 暗記シート (<span id="zukan-count">0</span>)</h3><button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button></div>
  <div class="filter-row">
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('all')">全て</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('SSSR')">SSSR</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('SSR')">SSR</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('SR')">SR</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('R')">R</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('ORIGIN')">オリジン</button>
    <button type="button" class="glass-btn mini-btn primary" onclick="startMemoMode()">暗記モード</button>
  </div>
  <div id="memo-panel" style="display:none">
    <div class="memo-card"><div id="memo-q" style="font-size:18px;margin-bottom:12px"></div><div id="memo-a" class="memo-hidden" style="font-size:13px;line-height:1.6;color:#cbd5e1"></div></div>
    <div class="row-btns"><button type="button" class="glass-btn" onclick="toggleMemoAnswer()">答え表示/隠す</button><button type="button" class="glass-btn primary" onclick="nextMemoCard()">次へ</button><button type="button" class="glass-btn slate" onclick="exitMemoMode()">一覧へ</button></div>
  </div>
  <div id="zukan-list" class="scroll-panel"></div>
</div>
<div id="achieve-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#a3e635">🏅 実績 (<span id="achieve-done">0</span>/<span id="achieve-total">0</span>)</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <div id="achieve-list" class="scroll-panel"></div>
</div>

<div id="deck-edit-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px">
    <div><h3 style="font-size:16px">デッキ編集 (<span id="deck-count">0</span>/50)</h3><p style="font-size:11px;color:#94a3b8">最低20 / 最大50</p></div>
    <div class="row-btns">
      <button type="button" class="glass-btn mini-btn warn" onclick="openRecommendModal()">おすすめ</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('name')">名前</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('rarity')">レア</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('power')">火力</button>
      <button type="button" id="deck-done-btn" class="glass-btn success" onclick="finishDeckEdit()">完了</button>
    </div>
  </div>
  <div class="filter-row" id="attr-filter-row"></div>
  <div class="preset-row"><input id="preset-name-0" placeholder="スロット1" maxlength="12"><button type="button" class="glass-btn mini-btn primary" onclick="saveDeckSlot(0)">保存1</button><button type="button" class="glass-btn mini-btn primary" onclick="loadDeckSlot(0)">読込1</button></div>
  <div class="preset-row"><input id="preset-name-1" placeholder="スロット2" maxlength="12"><button type="button" class="glass-btn mini-btn primary" onclick="saveDeckSlot(1)">保存2</button><button type="button" class="glass-btn mini-btn primary" onclick="loadDeckSlot(1)">読込2</button></div>
  <div class="preset-row"><input id="preset-name-2" placeholder="スロット3" maxlength="12"><button type="button" class="glass-btn mini-btn primary" onclick="saveDeckSlot(2)">保存3</button><button type="button" class="glass-btn mini-btn primary" onclick="loadDeckSlot(2)">読込3</button></div>
  <div id="preset-labels" style="font-size:11px;color:#94a3b8"></div>
  <div class="synth-bar-wrap">
    <div style="display:flex;justify-content:space-between"><span style="font-size:12px;color:#67e8f9">合成可能率</span><span id="synth-rate-text">—</span></div>
    <div class="synth-bar-bg"><div id="synth-rate-bar" class="synth-bar-fill" style="width:0%"></div></div>
    <div id="synth-hint" style="font-size:10px;color:#94a3b8;margin-top:5px"></div>
  </div>
  <div id="deck-list" class="deck-list"></div>
  <div class="info-box" style="max-height:12vh"><div style="color:#fbbf24;margin-bottom:4px">📖 反応メモ</div><div id="deck-reaction-list" style="white-space:pre-line;font-size:11px;color:#cbd5e1"></div></div>
</div>

<div id="gacha-screen" class="screen" style="overflow-y:auto;align-items:stretch">
  <div style="display:flex;justify-content:space-between;align-items:center;width:100%">
    <h2 style="color:#e879f9;font-size:18px">🧪 ガチャ</h2>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <p style="color:#7dd3fc;margin:6px 0">試薬: <span id="gacha-reagents">150</span>　肩書き: <span id="gacha-rank">初学者</span></p>
  <div id="gacha-result" class="gacha-card-view"><span style="color:#94a3b8">結果表示</span></div>
  <div id="gacha-types" class="scroll-panel" style="max-height:48vh;width:100%"></div>
</div>

<div id="longpress-popup" class="longpress-popup">
  <div style="color:#38bdf8;margin-bottom:8px" id="lp-title">反応</div>
  <div id="lp-body" style="font-size:12px;white-space:pre-line;line-height:1.55"></div>
  <button type="button" class="glass-btn slate wide" style="margin-top:12px" onclick="closeLongPress()">閉じる</button>
</div>
<div id="pool-modal">
  <div style="color:#e879f9;margin-bottom:8px;font-size:15px" id="pool-title">排出一覧</div>
  <div id="pool-body"></div>
  <button type="button" class="glass-btn slate wide" style="margin-top:12px" onclick="closePoolModal()">閉じる</button>
</div>
<div id="rec-modal">
  <div style="color:#fbbf24;margin-bottom:10px;font-size:15px">おすすめ編成</div>
  <p style="font-size:12px;color:#94a3b8;margin-bottom:10px">方針を選んでください</p>
  <button type="button" class="glass-btn wide primary" style="margin-bottom:6px" onclick="runRecommend('balance')">バランス（合成＋回復）</button>
  <button type="button" class="glass-btn wide orange" style="margin-bottom:6px" onclick="runRecommend('power')">火力重視</button>
  <button type="button" class="glass-btn wide pink" style="margin-bottom:6px" onclick="runRecommend('combo')">コンボ重視（中間体ルート）</button>
  <button type="button" class="glass-btn wide success" style="margin-bottom:6px" onclick="runRecommend('attr')">属性重視…</button>
  <div id="rec-attr-pick" style="display:none;margin:8px 0"></div>
  <button type="button" class="glass-btn slate wide" style="margin-top:8px" onclick="closeRecommendModal()">閉じる</button>
</div>

<script>
const ALL_CARDS=[
{name:"メタン",formula:"CH4",attackPower:15,healPower:0,attribute:"Alkane",rarity:"R"},
{name:"エタン",formula:"C2H6",attackPower:18,healPower:0,attribute:"Alkane",rarity:"R"},
{name:"プロパン",formula:"C3H8",attackPower:20,healPower:0,attribute:"Alkane",rarity:"R"},
{name:"エチレン",formula:"C2H4",attackPower:25,healPower:0,attribute:"Alkenyl",rarity:"R"},
{name:"プロピレン",formula:"C3H6",attackPower:28,healPower:0,attribute:"Alkenyl",rarity:"R"},
{name:"アセチレン",formula:"C2H2",attackPower:35,healPower:0,attribute:"Alkynyl",rarity:"SR"},
{name:"ベンゼン",formula:"C6H6",attackPower:30,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"トルエン",formula:"C6H5CH3",attackPower:35,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"ナフタレン",formula:"C10H8",attackPower:55,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"アントラセン",formula:"C14H10",attackPower:120,healPower:0,attribute:"Aromatic",rarity:"SSR"},
{name:"スチレン",formula:"C6H5CH=CH2",attackPower:40,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"メタノール",formula:"CH3OH",attackPower:22,healPower:0,attribute:"Alcohol",rarity:"R"},
{name:"エタノール",formula:"C2H5OH",attackPower:25,healPower:0,attribute:"Alcohol",rarity:"R"},
{name:"1-プロパノール",formula:"C3H7OH",attackPower:28,healPower:0,attribute:"Alcohol",rarity:"R"},
{name:"2-プロパノール",formula:"(CH3)2CHOH",attackPower:28,healPower:0,attribute:"Alcohol",rarity:"R"},
{name:"アセトアルデヒド",formula:"CH3CHO",attackPower:35,healPower:0,attribute:"Aldehyde",rarity:"R"},
{name:"アセトン",formula:"CH3COCH3",attackPower:32,healPower:0,attribute:"Ketone",rarity:"R"},
{name:"酢酸",formula:"CH3COOH",attackPower:40,healPower:0,attribute:"Acid",rarity:"R"},
{name:"安息香酸",formula:"C6H5COOH",attackPower:48,healPower:0,attribute:"Acid",rarity:"SR"},
{name:"酢酸エチル",formula:"CH3COOC2H5",attackPower:55,healPower:0,attribute:"Ester",rarity:"R"},
{name:"サリチル酸",formula:"C6H4(OH)COOH",attackPower:55,healPower:0,attribute:"Acid",rarity:"SR"},
{name:"アセチルサリチル酸",formula:"C9H8O4",attackPower:120,healPower:0,attribute:"Ester",rarity:"SSR"},
{name:"無水酢酸",formula:"(CH3CO)2O",attackPower:40,healPower:0,attribute:"Reagent",rarity:"SR"},
{name:"アセトアニリド",formula:"C6H5NHCOCH3",attackPower:60,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"トリパルミチン",formula:"C51H98O6",attackPower:45,healPower:0,attribute:"Fat",rarity:"SR"},
{name:"トリステアリン",formula:"C57H110O6",attackPower:48,healPower:0,attribute:"Fat",rarity:"SR"},
{name:"トリオレイン",formula:"C57H104O6",attackPower:50,healPower:0,attribute:"Fat",rarity:"SR"},
{name:"フェノール",formula:"C6H5OH",attackPower:45,healPower:0,attribute:"Phenol",rarity:"SR"},
{name:"o-クレゾール",formula:"CH3C6H4OH",attackPower:40,healPower:0,attribute:"Phenol",rarity:"R"},
{name:"m-クレゾール",formula:"CH3C6H4OH",attackPower:40,healPower:0,attribute:"Phenol",rarity:"R"},
{name:"p-クレゾール",formula:"CH3C6H4OH",attackPower:42,healPower:0,attribute:"Phenol",rarity:"R"},
{name:"アニリン",formula:"C6H5NH2",attackPower:65,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"ニトロベンゼン",formula:"C6H5NO2",attackPower:70,healPower:0,attribute:"Aromatic",rarity:"SR"},
{name:"アゾベンゼン",formula:"C6H5N=NC6H5",attackPower:110,healPower:0,attribute:"Aromatic",rarity:"SSR"},
{name:"塩素",formula:"Cl2",attackPower:35,healPower:0,attribute:"Halogen",rarity:"R"},
{name:"臭素",formula:"Br2",attackPower:35,healPower:0,attribute:"Halogen",rarity:"R"},
{name:"濃硝酸",formula:"HNO3",attackPower:30,healPower:0,attribute:"Reagent",rarity:"SR"},
{name:"濃硫酸",formula:"H2SO4",attackPower:30,healPower:0,attribute:"Reagent",rarity:"SR"},
{name:"水酸化ナトリウム",formula:"NaOH",attackPower:35,healPower:0,attribute:"Base",rarity:"SR"},
{name:"金属ナトリウム",formula:"Na",attackPower:40,healPower:0,attribute:"Metal",rarity:"SR"},
{name:"過マンガン酸カリウム",formula:"KMnO4",attackPower:40,healPower:0,attribute:"Oxidant",rarity:"SR"},
{name:"二クロム酸カリウム",formula:"K2Cr2O7",attackPower:38,healPower:0,attribute:"Oxidant",rarity:"SR"},
{name:"水素化ホウ素ナトリウム",formula:"NaBH4",attackPower:40,healPower:0,attribute:"Reductant",rarity:"SR"},
{name:"還元剤",formula:"[Red]",attackPower:30,healPower:0,attribute:"Reductant",rarity:"SR"},
{name:"重合触媒(Ziegler)",formula:"[Cat]",attackPower:30,healPower:0,attribute:"Catalyst",rarity:"SSR"},
{name:"塩化アルミニウム",formula:"AlCl3",attackPower:35,healPower:0,attribute:"Catalyst",rarity:"SR"},
{name:"鉄",formula:"Fe",attackPower:25,healPower:0,attribute:"Catalyst",rarity:"R"},
{name:"ジアゾ化剤",formula:"NaNO2/HCl",attackPower:35,healPower:0,attribute:"Reagent",rarity:"SR"},
{name:"メチル基",formula:"-CH3",attackPower:20,healPower:0,attribute:"Hydrocarbon",rarity:"R"},
{name:"エチル基",formula:"-C2H5",attackPower:25,healPower:0,attribute:"Hydrocarbon",rarity:"R"},
{name:"フェニル基",formula:"-C6H5",attackPower:40,healPower:0,attribute:"Hydrocarbon",rarity:"SR"},
{name:"ビニル基",formula:"-CH=CH2",attackPower:35,healPower:0,attribute:"Hydrocarbon",rarity:"R"},
{name:"ヒドロキシ基",formula:"-OH",attackPower:25,healPower:0,attribute:"FunctionalGroup",rarity:"R"},
{name:"カルボキシ基",formula:"-COOH",attackPower:40,healPower:0,attribute:"FunctionalGroup",rarity:"SR"},
{name:"アミノ基",formula:"-NH2",attackPower:30,healPower:0,attribute:"FunctionalGroup",rarity:"R"},
{name:"ニトロ基",formula:"-NO2",attackPower:45,healPower:0,attribute:"FunctionalGroup",rarity:"SR"},
{name:"マレイン酸",formula:"cis",attackPower:55,healPower:0,attribute:"CisTrans",rarity:"SR"},
{name:"フマル酸",formula:"trans",attackPower:55,healPower:0,attribute:"CisTrans",rarity:"SR"},
{name:"シス-2-ブテン",formula:"cis-C4H8",attackPower:35,healPower:0,attribute:"CisTrans",rarity:"R"},
{name:"トランス-2-ブテン",formula:"trans-C4H8",attackPower:35,healPower:0,attribute:"CisTrans",rarity:"R"},
{name:"オレイン酸",formula:"C18H34O2",attackPower:50,healPower:0,attribute:"CisTrans",rarity:"SR"},
{name:"グリシン",formula:"H2NCH2COOH",attackPower:0,healPower:40,attribute:"Nutrient",rarity:"R"},
{name:"グルコース",formula:"C6H12O6",attackPower:0,healPower:65,attribute:"Nutrient",rarity:"SR"},
{name:"スクロース",formula:"C12H22O11",attackPower:0,healPower:50,attribute:"Nutrient",rarity:"R"},
{name:"トリニトロトルエン",formula:"C7H5N3O6",attackPower:180,healPower:0,attribute:"Explosive",rarity:"SSR"},
{name:"ピクリン酸",formula:"C6H3N3O7",attackPower:180,healPower:0,attribute:"Explosive",rarity:"SSR"},
{name:"フッ化水素酸",formula:"HF",attackPower:Infinity,healPower:0,attribute:"Acid",rarity:"SSSR"},
{name:"ボツリヌス毒素",formula:"BoNT",attackPower:0,healPower:0,attribute:"Toxin",rarity:"SSSR"},
{name:"ビタミンC",formula:"C6H8O6",attackPower:70,healPower:55,attribute:"Nutrient",rarity:"SSR"},
{name:"サリチル酸メチル",formula:"C8H8O3",attackPower:85,healPower:40,attribute:"Ester",rarity:"SSR"},
{name:"カフェイン",formula:"C8H10N4O2",attackPower:90,healPower:35,attribute:"Aromatic",rarity:"SSR"}
];

const RANK_BY_LEVEL=[
{name:"初学者",level:1,reagentBonus:1.0,gachaBoost:0,promoteReward:0},
{name:"高校生",level:5,reagentBonus:1.15,gachaBoost:0.3,promoteReward:40},
{name:"大学生",level:12,reagentBonus:1.3,gachaBoost:0.6,promoteReward:60},
{name:"大学院生",level:20,reagentBonus:1.5,gachaBoost:1.0,promoteReward:80},
{name:"助教",level:30,reagentBonus:1.7,gachaBoost:1.2,promoteReward:100},
{name:"准教授",level:42,reagentBonus:1.9,gachaBoost:1.5,promoteReward:120},
{name:"博士",level:55,reagentBonus:2.2,gachaBoost:1.8,promoteReward:150},
{name:"教授",level:70,reagentBonus:2.5,gachaBoost:2.2,promoteReward:200}
];
function expToReachLevel(lv){if(lv<=1)return 0;var t=0;for(var i=1;i<lv;i++)t+=20+i*12;return t;}
/* 研究室 Lv1〜10 */
const LAB_THRESH=[0,30,70,120,180,250,330,420,520,650,800];
const LAB_PERKS=[
"Lv1 基本",
"Lv2 撃破試薬 +5%",
"Lv3 無料ガチャ解放",
"Lv4 撃破試薬 +10%",
"Lv5 コンボ試薬ボーナス",
"Lv6 ガチャ確率微アップ",
"Lv7 撃破経験 +10%",
"Lv8 ガチャ確率アップ",
"Lv9 撃破試薬 +15%",
"Lv10 ガチャ確率大幅アップ＆研究室完成"
];
function labGachaBoost(){
  var lv=gameState.labLevel||1;
  if(lv>=10)return 2.0;
  if(lv>=8)return 1.2;
  if(lv>=6)return 0.6;
  return 0;
}

const REACTION_TREE=[
{id:"nitro_bz",name:"ニトロ化（ベンゼン）",path:"ベンゼン + 濃硝酸",chain:"芳香族",reward:25},
{id:"nitro_tol",name:"ニトロ化（トルエン）",path:"トルエン + 濃硝酸",chain:"芳香族",reward:30},
{id:"nitro_ph",name:"ニトロ化（フェノール）",path:"フェノール + 濃硝酸",chain:"芳香族",reward:25},
{id:"nitro_grp",name:"基ニトロ化",path:"ベンゼン + ニトロ基 → ニトロベンゼン",chain:"中間体連鎖",reward:30},
{id:"reduce_nb",name:"還元",path:"ニトロベンゼン + 還元剤 → アニリン",chain:"中間体連鎖",reward:35},
{id:"azo",name:"ジアゾ〜アゾ",path:"アニリン + ジアゾ化剤",chain:"中間体連鎖",reward:40},
{id:"acetyl_an",name:"アセチル化（アニリン）",path:"アニリン + 無水酢酸",chain:"アセチル",reward:30},
{id:"acetyl_sal",name:"アセチル化（サリチル酸）",path:"サリチル酸 + 無水酢酸",chain:"アセチル",reward:40},
{id:"ester",name:"エステル化",path:"酢酸 + エタノール",chain:"エステル・けん化",reward:30},
{id:"sapon",name:"けん化",path:"酢酸エチル等 + NaOH",chain:"エステル・けん化",reward:30},
{id:"sapon_fat",name:"油脂けん化",path:"トリグリセリド + NaOH",chain:"エステル・けん化",reward:35},
{id:"dehyd",name:"脱水",path:"エタノール + 濃硫酸",chain:"脱水",reward:30},
{id:"add_et",name:"付加",path:"エチレン等 + ハロゲン",chain:"付加・重合",reward:25},
{id:"poly",name:"重合",path:"オレフィン + Ziegler",chain:"付加・重合",reward:40},
{id:"oxid",name:"酸化",path:"アルコール + 酸化剤",chain:"酸化",reward:30},
{id:"side_ox",name:"側鎖酸化",path:"トルエン + KMnO4",chain:"酸化",reward:35},
{id:"sulf",name:"スルホン化",path:"芳香族 + 濃硫酸",chain:"芳香族",reward:25},
{id:"halo",name:"ハロゲン化",path:"ベンゼン + ハロゲン + 触媒",chain:"芳香族",reward:30},
{id:"na_alc",name:"アルコキシド",path:"アルコール + Na",chain:"金属Na",reward:25},
{id:"na_ph",name:"フェノキシド",path:"フェノール + Na",chain:"金属Na",reward:25},
{id:"fg_oh",name:"基＋OH",path:"炭化水素基 + OH",chain:"官能基",reward:20},
{id:"fg_no2",name:"基＋NO2",path:"フェニル + ニトロ基",chain:"官能基",reward:25}
];
const INTERMEDIATE_NAMES=["ニトロベンゼン","アニリン","アゾベンゼン","酢酸エチル","アセトアニリド","アセチルサリチル酸"];
const CARD_REACT_FULL={
"ベンゼン":"・+ニトロ基 → ニトロベンゼン\n・+濃硝酸 → ニトロ化\n・+濃硫酸 → スルホン化\n・+塩素/臭素+触媒 → ハロゲン化",
"トルエン":"・+濃硝酸 → ニトロ化\n・+KMnO4 → 側鎖酸化",
"フェノール":"・+濃硝酸 → ニトロ化\n・+金属Na → フェノキシド",
"アニリン":"・+ジアゾ化剤 → アゾベンゼン\n・+無水酢酸 → アセトアニリド",
"ニトロベンゼン":"・+還元剤/NaBH4 → アニリン",
"アゾベンゼン":"・アニリン+ジアゾ化の最終生成物",
"酢酸":"・+エタノール → 酢酸エチル\n・+NaOH → けん化",
"エタノール":"・+酢酸 → エステル化\n・+濃硫酸 → 脱水\n・+金属Na → アルコキシド\n・+酸化剤 → 酸化",
"酢酸エチル":"・+NaOH → けん化",
"サリチル酸":"・+無水酢酸 → アセチルサリチル酸",
"無水酢酸":"・+アニリン / サリチル酸 → アセチル化",
"濃硝酸":"・芳香族とニトロ化",
"濃硫酸":"・触媒（倍率2.0）・スルホン化",
"ニトロ基":"・+ベンゼン → ニトロベンゼン",
"ヒドロキシ基":"・+炭化水素基 → アルコール等",
"水酸化ナトリウム":"・けん化",
"金属ナトリウム":"・アルコキシド / フェノキシド",
"エチレン":"・付加 / 重合",
"重合触媒(Ziegler)":"・オレフィン重合",
"過マンガン酸カリウム":"・酸化・側鎖酸化",
"還元剤":"・ニトロベンゼン → アニリン",
"ジアゾ化剤":"・アニリン → アゾ",
"塩素":"・付加・ハロゲン化","臭素":"・付加・ハロゲン化"
};
const ACHIEVEMENTS=[
{id:"first_win",name:"初勝利",desc:"初めて敵を倒す",reward:30,check:function(s){return s.kills>=1}},
{id:"kills_30",name:"撃破30",desc:"30体倒す",reward:60,check:function(s){return s.kills>=30}},
{id:"kills_80",name:"撃破80",desc:"80体倒す",reward:120,check:function(s){return s.kills>=80}},
{id:"kills_150",name:"撃破150",desc:"150体倒す",reward:200,check:function(s){return s.kills>=150}},
{id:"nitro",name:"ニトロ化",desc:"ニトロ化成功",reward:40,check:function(s){return s.flags.nitro}},
{id:"sapon",name:"けん化",desc:"けん化成功",reward:40,check:function(s){return s.flags.sapon}},
{id:"poly",name:"重合",desc:"重合成功",reward:40,check:function(s){return s.flags.poly}},
{id:"acetyl",name:"アセチル化",desc:"アセチル化成功",reward:45,check:function(s){return s.flags.acetyl}},
{id:"dehyd",name:"脱水",desc:"脱水成功",reward:45,check:function(s){return s.flags.dehyd}},
{id:"ester",name:"エステル化",desc:"エステル化成功",reward:40,check:function(s){return s.flags.ester}},
{id:"oxid",name:"酸化反応",desc:"酸化成功",reward:40,check:function(s){return s.flags.oxid}},
{id:"fat",name:"油脂の化学",desc:"油脂けん化",reward:45,check:function(s){return s.flags.fat}},
{id:"combo5",name:"連鎖5",desc:"中間体連鎖コンボ5",reward:80,check:function(s){return s.flags.combo5}},
{id:"combo8",name:"連鎖8",desc:"中間体連鎖コンボ8",reward:150,check:function(s){return s.flags.combo8}},
{id:"boss",name:"ボス討伐",desc:"ボスを倒す",reward:80,check:function(s){return s.flags.boss}},
{id:"boss5",name:"ボスハンター",desc:"ボス5体",reward:150,check:function(s){return (s.flags.bossKills||0)>=5}},
{id:"no_cat_boss",name:"無触媒主義",desc:"触媒なしでボス撃破",reward:120,check:function(s){return s.flags.noCatBoss}},
{id:"save_boss",name:"節約実験",desc:"大ダメ試薬消費なしでボス",reward:100,check:function(s){return s.flags.saveBoss}},
{id:"mid_chain",name:"中間体職人",desc:"手札中間体から再反応3回",reward:90,check:function(s){return (s.flags.midReact||0)>=3}},
{id:"tree_10",name:"反応樹10",desc:"反応ツリー10種",reward:80,check:function(s){return treeDoneCount(s)>=10}},
{id:"tree_all",name:"反応樹コンプ",desc:"反応ツリー全解放",reward:200,check:function(s){return treeDoneCount(s)>=REACTION_TREE.length}},
{id:"hard_only",name:"強敵志向",desc:"赤+ボス撃破20",reward:100,check:function(s){return (s.flags.hardKills||0)>=20}},
{id:"mono_attr",name:"単色属性勝利",desc:"同一属性だけで勝利",reward:90,check:function(s){return s.flags.monoWin}},
{id:"origin_deck",name:"フルオリジン",desc:"オリジン3枚以上で勝利",reward:100,check:function(s){return s.flags.originWin}},
{id:"refine5",name:"精製職人",desc:"精製5回",reward:70,check:function(s){return (s.flags.refineCount||0)>=5}},
{id:"collect_40",name:"大図鑑",desc:"図鑑40種",reward:120,check:function(s){return uniqCount(s)>=40}},
{id:"collect_60",name:"図鑑60",desc:"図鑑60種",reward:200,check:function(s){return uniqCount(s)>=60}},
{id:"gacha50",name:"ガチャ中毒",desc:"ガチャ50回",reward:100,check:function(s){return (s.flags.gachaCount||0)>=50}},
{id:"gacha150",name:"ガチャ狂",desc:"ガチャ150回",reward:180,check:function(s){return (s.flags.gachaCount||0)>=150}},
{id:"ssr_get",name:"SSR入手",desc:"SSR所持",reward:50,check:function(s){return (s.collection||[]).some(function(c){return c.rarity==='SSR'})}},
{id:"sssr_get",name:"SSSR入手",desc:"SSSR所持",reward:100,check:function(s){return (s.collection||[]).some(function(c){return c.rarity==='SSSR'})}},
{id:"origin1",name:"オリジネイター",desc:"オリジナル作成",reward:60,check:function(s){return s.flags.origin}},
{id:"origin3",name:"発明家",desc:"オリジナル3枚",reward:90,check:function(s){return (s.flags.originCount||0)>=3}},
{id:"memo20",name:"暗記マスター",desc:"暗記答え表示20回",reward:80,check:function(s){return (s.flags.memoCount||0)>=20}},
{id:"daily5",name:"日替わり5",desc:"日替わり累計5",reward:70,check:function(s){return (s.flags.dailyTotal||0)>=5}},
{id:"rank_hs",name:"高校進学",desc:"高校生以上",reward:30,check:function(s){return (s.playerLevel||1)>=5}},
{id:"rank_uni",name:"大学進学",desc:"大学生以上",reward:50,check:function(s){return (s.playerLevel||1)>=12}},
{id:"rank_doc",name:"博士号",desc:"博士以上",reward:120,check:function(s){return (s.playerLevel||1)>=55}},
{id:"plv_20",name:"レベル20",desc:"プレイヤーLv20",reward:60,check:function(s){return (s.playerLevel||1)>=20}},
{id:"plv_40",name:"レベル40",desc:"プレイヤーLv40",reward:100,check:function(s){return (s.playerLevel||1)>=40}},
{id:"lab5",name:"研究室Lv5",desc:"研究室Lv5",reward:80,check:function(s){return (s.labLevel||1)>=5}},
{id:"lab10",name:"研究室完成",desc:"研究室Lv10",reward:150,check:function(s){return (s.labLevel||1)>=10}},
{id:"quiz10",name:"クイズ10",desc:"クイズ10正解",reward:50,check:function(s){return (s.flags.quizOk||0)>=10}},
{id:"iso10",name:"異性体10",desc:"異性体10正解",reward:50,check:function(s){return (s.flags.isoOk||0)>=10}},
{id:"rich",name:"試薬長者",desc:"試薬800以上",reward:80,check:function(s){return (s.reagents||0)>=800}}
];
const DAILY_QUESTS=[{key:"nitro",label:"ニトロ化を1回"},{key:"sapon",label:"けん化を1回"},{key:"poly",label:"重合を1回"},{key:"ester",label:"エステル化を1回"},{key:"oxid",label:"酸化を1回"},{key:"acetyl",label:"アセチル化を1回"},{key:"dehyd",label:"脱水を1回"}];
const FULL_REACTION_TEXT="中間体連鎖でコンボ増加\nベンゼン+ニトロ基→ニトロベンゼン→還元→アニリン→アゾ/アセチル\n酢酸+エタノール→酢酸エチル→けん化\n触媒なし1.5/あり2.0";
const SYNTH_PAIRS=[{a:["ベンゼン"],b:["ニトロ基","濃硝酸","濃硫酸","塩素","臭素"]},{a:["トルエン"],b:["濃硝酸","過マンガン酸カリウム"]},{a:["フェノール"],b:["濃硝酸","金属ナトリウム"]},{a:["アニリン"],b:["ジアゾ化剤","無水酢酸"]},{a:["ニトロベンゼン"],b:["還元剤","水素化ホウ素ナトリウム"]},{a:["酢酸"],b:["エタノール","水酸化ナトリウム"]},{a:["エタノール"],b:["酢酸","濃硫酸","金属ナトリウム","過マンガン酸カリウム"]},{a:["エチレン"],b:["塩素","臭素","重合触媒(Ziegler)"]},{a:["スチレン","プロピレン"],b:["重合触媒(Ziegler)"]},{a:["サリチル酸"],b:["無水酢酸"]},{a:["トリパルミチン","トリステアリン","トリオレイン","オレイン酸","酢酸エチル"],b:["水酸化ナトリウム"]},{a:["メチル基","エチル基","フェニル基","ビニル基"],b:["ヒドロキシ基","カルボキシ基","アミノ基","ニトロ基"]}];
const COMBO_CORE=["ベンゼン","ニトロ基","濃硝酸","ニトロベンゼン","還元剤","水素化ホウ素ナトリウム","アニリン","ジアゾ化剤","無水酢酸","酢酸","エタノール","酢酸エチル","水酸化ナトリウム"];
const QUIZ_BANK=[{q:"ベンゼンのニトロ化生成物は？",opts:["ニトロベンゼン","フェノール","トルエン","アニリン"],ok:0,ex:"ニトロベンゼンです。"},{q:"エステル化の触媒は？",opts:["濃硫酸","NaOH","KMnO4","Fe"],ok:0,ex:"濃硫酸です。"},{q:"第一級アルコール酸化の最終物は？",opts:["カルボン酸","ケトン","エーテル","アルケン"],ok:0,ex:"カルボン酸です。"},{q:"第二級アルコールの酸化は？",opts:["ケトン","カルボン酸","アルデヒド","エーテル"],ok:0,ex:"ケトンです。"},{q:"油脂のけん化で出るアルコールは？",opts:["グリセリン","エタノール","メタノール","フェノール"],ok:0,ex:"グリセリンです。"},{q:"エタノールを濃硫酸で脱水すると？",opts:["エチレン","酢酸","アセトン","メタン"],ok:0,ex:"エチレンです。"},{q:"ニトロベンゼンを還元すると？",opts:["アニリン","フェノール","ベンゼン","トルエン"],ok:0,ex:"アニリンです。"},{q:"トルエンをKMnO4酸化すると？",opts:["安息香酸","フェノール","ベンゼン","ベンズアルデヒド"],ok:0,ex:"安息香酸です。"}];
const ISOMER_BANK=[{q:"マレイン酸の幾何異性体は？",opts:["フマル酸","コハク酸","シュウ酸","安息香酸"],ok:0,ex:"フマル酸です。"},{q:"cis-2-ブテンの異性体は？",opts:["trans-2-ブテン","1-ブテン","イソブテン","ブタン"],ok:0,ex:"シス/トランスです。"},{q:"フェノールのパラ位メチル体は？",opts:["p-クレゾール","o-クレゾール","m-クレゾール","キシレン"],ok:0,ex:"p-クレゾールです。"},{q:"オレイン酸の二重結合は主に？",opts:["シス","トランス","両方","なし"],ok:0,ex:"ほぼシスです。"},{q:"隣同士の置換は？",opts:["オルト","メタ","パラ","なし"],ok:0,ex:"オルトです。"},{q:"1,4-位の置換は？",opts:["パラ","オルト","メタ","ジェミナル"],ok:0,ex:"パラです。"}];
const RARITY_ORDER={SSSR:0,SSR:1,SR:2,R:3,ORIGIN:2};
const ATTR_LIST=["Alkane","Alkenyl","Alkynyl","Aromatic","Alcohol","Aldehyde","Ketone","Acid","Ester","Phenol","Halogen","Reagent","Base","Metal","Oxidant","Reductant","Catalyst","Hydrocarbon","FunctionalGroup","CisTrans","Fat","Nutrient","Explosive","Toxin"];
const ATTR_JP={Alkane:"アルカン",Alkenyl:"アルケン",Alkynyl:"アルキン",Aromatic:"芳香族",Alcohol:"アルコール",Aldehyde:"アルデヒド",Ketone:"ケトン",Acid:"酸",Ester:"エステル",Phenol:"フェノール",Halogen:"ハロゲン",Reagent:"試薬",Base:"塩基",Metal:"金属",Oxidant:"酸化剤",Reductant:"還元剤",Catalyst:"触媒",Hydrocarbon:"炭化水素基",FunctionalGroup:"官能基",CisTrans:"シス・トランス",Fat:"油脂",Nutrient:"栄養",Explosive:"爆発物",Toxin:"毒素"};
const GACHA_TYPES=[
{id:"normal",name:"通常ガチャ",cost:100,desc:"全カード",rates:function(b){return{SSSR:0.1+b*0.15,SSR:2.9+b,SR:15+b*2,R:100};},pool:function(){return ALL_CARDS.slice();}},
{id:"cheap",name:"練習ガチャ",cost:40,desc:"R・SR",rates:function(){return{SR:25,R:100};},pool:function(){return ALL_CARDS.filter(function(c){return c.rarity==='R'||c.rarity==='SR';});}},
{id:"aromatic",name:"芳香族ガチャ",cost:120,desc:"芳香族",rates:function(b){return{SSR:5+b,SR:30,R:100};},pool:function(){return ALL_CARDS.filter(function(c){return ['Aromatic','Phenol','Reagent','FunctionalGroup'].indexOf(c.attribute)>=0;});}},
{id:"alcohol",name:"アルコール・酸ガチャ",cost:110,desc:"酸・アルコ",rates:function(b){return{SSR:4+b,SR:28,R:100};},pool:function(){return ALL_CARDS.filter(function(c){return ['Alcohol','Acid','Ester','Oxidant','Aldehyde','Ketone','Base'].indexOf(c.attribute)>=0;});}},
{id:"poly",name:"重合・付加ガチャ",cost:130,desc:"オレフィン",rates:function(b){return{SSR:8+b,SR:35,R:100};},pool:function(){return ALL_CARDS.filter(function(c){return ['Alkenyl','Alkynyl','Halogen','Catalyst','Hydrocarbon'].indexOf(c.attribute)>=0;});}},
{id:"heal",name:"回復特化ガチャ",cost:90,desc:"回復",rates:function(){return{SSR:15,SR:40,R:100};},pool:function(){return ALL_CARDS.filter(function(c){return (c.healPower||0)>0;});}},
{id:"premium",name:"SSR・SSSR確定",cost:1000,desc:"SSR93%/SSSR7%",rates:function(){return{SSSR:7,SSR:100};},pool:function(){return ALL_CARDS.filter(function(c){return c.rarity==='SSR'||c.rarity==='SSSR';});}}
];
const MOL_PARTS=[
{id:"C",label:"C",val:4,sym:"C",cls:"C",atk:12},
{id:"H",label:"H",val:1,sym:"H",cls:"H",atk:2},
{id:"O",label:"O",val:2,sym:"O",cls:"O",atk:10},
{id:"N",label:"N",val:3,sym:"N",cls:"N",atk:11},
{id:"P",label:"P",val:3,sym:"P",cls:"P",atk:13},
{id:"Cl",label:"Cl",val:1,sym:"Cl",cls:"Cl",atk:14},
{id:"S",label:"S",val:2,sym:"S",cls:"S",atk:12},
{id:"OH",label:"OH",val:1,sym:"OH",cls:"FG",atk:18,heal:0},
{id:"COOH",label:"COOH",val:1,sym:"COOH",cls:"FG",atk:28,heal:0},
{id:"NH2",label:"NH2",val:1,sym:"NH2",cls:"FG",atk:20,heal:0},
{id:"NO2",label:"NO2",val:1,sym:"NO2",cls:"FG",atk:32,heal:0},
{id:"CH3",label:"CH3",val:1,sym:"CH3",cls:"FG",atk:15,heal:0},
{id:"Nut",label:"栄養",val:1,sym:"Nut",cls:"FG",atk:0,heal:35}
];

function uniqCount(s){var set={},n=0;(s.collection||[]).forEach(function(c){var k=baseName(c.name);if(!set[k]){set[k]=1;n++;}});return n;}
function treeDoneCount(s){var n=0;REACTION_TREE.forEach(function(r){if(s.recipes&&s.recipes[r.id])n++;});return n;}
function baseName(n){return String(n||'').replace(/^精製/,'');}
function fmt(v){return v===Infinity?'∞':v;}
function powerValue(c){if(!c)return 0;if(baseName(c.name)==='ボツリヌス毒素')return 200;if(c.attackPower===Infinity)return 99999;return (c.attackPower||0)+(c.healPower||0);}
function uid(){return Math.random().toString(36).slice(2,11);}
function todayStr(){var d=new Date();return d.getFullYear()+'-'+(d.getMonth()+1)+'-'+d.getDate();}
function cardPowerText(card){
  if(baseName(card.name)==='ボツリヌス毒素')return '<div class="card-dmg">毎ターン200ダメージ</div>';
  var h='';
  if(card.attackPower===Infinity)h+='<div class="card-dmg">∞ダメージ</div>';
  else if((card.attackPower||0)>0)h+='<div class="card-dmg">'+card.attackPower+'ダメージ</div>';
  if((card.healPower||0)>0)h+='<div class="card-heal">'+card.healPower+'回復</div>';
  if(!h)h='<div class="card-dmg">0ダメージ</div>';
  return h;
}
function isIntermediateCard(c){if(!c)return false;if(c._fromMid)return true;return INTERMEDIATE_NAMES.indexOf(baseName(c.name))>=0;}
function getLongPressText(card){
  var bn=baseName(card.name),body=CARD_REACT_FULL[bn]||'';
  if(!body){for(var k in CARD_REACT_FULL){if(bn.indexOf(k)>=0||k.indexOf(bn)>=0){body=CARD_REACT_FULL[k];break;}}}
  if(!body)body=(card.healPower>0)?'回復カード':'単体投擲・特殊カード';
  if(String(card.name).indexOf('精製')===0)body='【精製】威力×1.15\n\n'+(CARD_REACT_FULL[bn]||body);
  if(isIntermediateCard(card))body+='\n\n※中間体：次の合成で連鎖コンボ+1';
  if(card.rarity==='ORIGIN'||card.origin)body+='\n（分子ビルダー製・改名可）';
  return body;
}
function synthCostForDamage(atk){var d=Math.max(50,Math.min(300,atk));return Math.round(100+(d-50)/250*900);}

var gameState={
  reagents:150,playerHP:200,playerMaxHP:200,collection:[],currentDeck:[],
  kills:0,playerLevel:1,playerExp:0,lastRank:'初学者',
  flags:{nitro:false,sapon:false,poly:false,ester:false,oxid:false,acetyl:false,dehyd:false,fat:false,boss:false,combo3:false,combo5:false,combo8:false,refined:false,refineCount:0,gachaCount:0,origin:false,originCount:0,memoCount:0,dailyTotal:0,bossKills:0,healed:false,hfUsed:false,quizOk:0,isoOk:0,noCatBoss:false,saveBoss:false,midReact:0,hardKills:0,monoWin:false,originWin:false},
  achieved:{},recipes:{},dailyDate:'',dailyKey:'',dailyDone:false,deckListOrder:[],
  deckSlots:[{name:'',cards:[]},{name:'',cards:[]},{name:'',cards:[]}],
  labLevel:1,labExp:0,labFreeDate:'',zukanRewards:{r30:false,r60:false,r90:false},lastReplay:[],nextDamageBonus:1.0
};
var returnToMenu=false,menuOpen=false,isBattleOver=false,isProcessing=false,botulinumActive=false,isPractice=false,gachaBusy=false;
var pendingIntermediate=null,fromBattleToHistory=false,pendingBoss=null,fromBossPreview=false;
var battleHistory=[],battleTurnCount=0,bossTurnLimit=0,comboCount=0,zukanFilter='all',deckAttrFilter='all';
var battleUsedCatalyst=false,battleBigSpend=false,battleAttrsUsed={},battleOriginCount=0;
var qoScore=0,qoTotal=0,isoScore=0,isoStreak=0;
var bDeck=[],bHand=[],bSelected=[],monsterHP=500,isPlayerTurn=true;
var memoList=[],memoIdx=0,memoShow=false;
var molAtoms=[],molBonds=[],bondMode=false,bondPick=null,molHistory=[];

function openFieldMenu(){menuOpen=true;var m=document.getElementById('field-menu');if(m)m.style.display='flex';}
function closeFieldMenu(clearFlag){menuOpen=false;var m=document.getElementById('field-menu');if(m)m.style.display='none';if(clearFlag)returnToMenu=false;}
function menuGo(s){returnToMenu=true;fromBossPreview=false;closeFieldMenu(false);switchState(s);}
function menuGoQuiz(){returnToMenu=true;fromBossPreview=false;closeFieldMenu(false);startQuizOnly();}
function menuGoIsomer(){returnToMenu=true;fromBossPreview=false;closeFieldMenu(false);startIsomerMode();}
function goBackFromMenu(){
  if(fromBossPreview&&pendingBoss){fromBossPreview=false;showBossPreview(pendingBoss);return;}
  switchState('field');if(returnToMenu)openFieldMenu();
}

function initDaily(){var t=todayStr();if(gameState.dailyDate!==t){gameState.dailyDate=t;gameState.dailyKey=DAILY_QUESTS[Math.floor(Math.random()*DAILY_QUESTS.length)].key;gameState.dailyDone=false;}}
function getDailyLabel(){var q=DAILY_QUESTS.find(function(x){return x.key===gameState.dailyKey;});return q?q.label:'—';}
function getRank(){var r=RANK_BY_LEVEL[0],lv=gameState.playerLevel||1;for(var i=0;i<RANK_BY_LEVEL.length;i++){if(lv>=RANK_BY_LEVEL[i].level)r=RANK_BY_LEVEL[i];}return r;}
function checkRankUp(){var r=getRank();if(r.name!==gameState.lastRank){if(r.promoteReward>0){gameState.reagents+=r.promoteReward;alert('肩書きアップ！ '+gameState.lastRank+' → '+r.name+'\n試薬 +'+r.promoteReward);}gameState.lastRank=r.name;}}
function addPlayerExp(n){if(n<=0)return;gameState.playerExp+=n;var leveled=false;while(true){var need=expToReachLevel(gameState.playerLevel+1);if(gameState.playerExp>=need){gameState.playerLevel++;leveled=true;}else break;}if(leveled){checkRankUp();setTimeout(function(){alert('プレイヤーレベルアップ！ Lv.'+gameState.playerLevel);},200);}checkAchievements(true);}
function enemyExpReward(m){if(!m)return 5;var base=m.isBoss?55+Math.floor(Math.random()*15):(m.level>=3?22:(m.level===2?14:7));if((gameState.labLevel||1)>=7)base=Math.floor(base*1.1);return base;}
function addLabExp(n){if(gameState.labLevel>=10){gameState.labExp=LAB_THRESH[10]||800;return;}gameState.labExp+=n;while(gameState.labLevel<10&&gameState.labExp>=(LAB_THRESH[gameState.labLevel]||99999)){gameState.labLevel++;var bonus=20+gameState.labLevel*5;gameState.reagents+=bonus;(function(lv,b){setTimeout(function(){alert('研究室 Lv.'+lv+(lv>=10?' 完成！':'')+'\n試薬 +'+b);},200);})(gameState.labLevel,bonus);}checkAchievements(true);}
function checkZukanRewards(){var n=uniqCount(gameState),pct=Math.floor(n/ALL_CARDS.length*100);if(pct>=30&&!gameState.zukanRewards.r30){gameState.zukanRewards.r30=true;gameState.reagents+=40;}if(pct>=60&&!gameState.zukanRewards.r60){gameState.zukanRewards.r60=true;gameState.reagents+=80;}if(pct>=90&&!gameState.zukanRewards.r90){gameState.zukanRewards.r90=true;gameState.reagents+=150;}}
function unlockRecipe(id){if(!id||(gameState.recipes&&gameState.recipes[id]))return;if(!gameState.recipes)gameState.recipes={};var rec=REACTION_TREE.find(function(r){return r.id===id;});if(!rec)return;gameState.recipes[id]=true;gameState.reagents+=rec.reward;setTimeout(function(){alert('反応ツリー解放: '+rec.name+'\n試薬 +'+rec.reward);},300);checkAchievements();}
function checkAchievements(silent){var gained=[];for(var i=0;i<ACHIEVEMENTS.length;i++){var a=ACHIEVEMENTS[i];if(gameState.achieved[a.id])continue;if(a.check(gameState)){gameState.achieved[a.id]=true;gameState.reagents+=a.reward;gained.push(a.name+'(+'+a.reward+')';}}checkZukanRewards();if(gained.length&&!silent)setTimeout(function(){alert('実績達成！\n'+gained.join('\n'));},250);else if(gained.length&&silent){if(!checkAchievements._batch){checkAchievements._batch=gained.slice();setTimeout(function(){if(checkAchievements._batch&&checkAchievements._batch.length)alert('未受け取り実績を遡って付与\n'+checkAchievements._batch.join('\n'));checkAchievements._batch=null;},400);}else checkAchievements._batch=checkAchievements._batch.concat(gained);}}
function markFlag(f){gameState.flags[f]=true;if(!gameState.dailyDone&&gameState.dailyKey===f){gameState.dailyDone=true;gameState.flags.dailyTotal=(gameState.flags.dailyTotal||0)+1;gameState.reagents+=50;setTimeout(function(){alert('日替わりクリア 試薬+50');},200);}checkAchievements();}

function saveGame(silent){try{localStorage.setItem('organicChemBattleSave',JSON.stringify(gameState));if(!silent)alert('セーブしました');}catch(e){alert('セーブ失敗');}}
function loadGame(){
  var raw=localStorage.getItem('organicChemBattleSave');if(!raw){alert('セーブがありません');return;}
  try{
    var data=JSON.parse(raw);
    gameState.reagents=data.reagents||150;gameState.playerHP=data.playerHP||200;gameState.playerMaxHP=data.playerMaxHP||200;
    gameState.collection=data.collection||[];gameState.currentDeck=data.currentDeck||[];gameState.kills=data.kills||0;
    gameState.playerLevel=data.playerLevel||1;gameState.playerExp=data.playerExp||0;gameState.lastRank=data.lastRank||'初学者';
    gameState.flags=Object.assign({nitro:false,sapon:false,poly:false,ester:false,oxid:false,acetyl:false,dehyd:false,fat:false,boss:false,combo3:false,combo5:false,combo8:false,refined:false,refineCount:0,gachaCount:0,origin:false,originCount:0,memoCount:0,dailyTotal:0,bossKills:0,healed:false,hfUsed:false,quizOk:0,isoOk:0,noCatBoss:false,saveBoss:false,midReact:0,hardKills:0,monoWin:false,originWin:false},data.flags||{});
    gameState.achieved=data.achieved||{};gameState.recipes=data.recipes||{};
    gameState.dailyDate=data.dailyDate||'';gameState.dailyKey=data.dailyKey||'';gameState.dailyDone=!!data.dailyDone;
    gameState.deckListOrder=data.deckListOrder||[];gameState.labLevel=Math.min(10,data.labLevel||1);gameState.labExp=data.labExp||0;gameState.labFreeDate=data.labFreeDate||'';
    gameState.zukanRewards=Object.assign({r30:false,r60:false,r90:false},data.zukanRewards||{});gameState.lastReplay=data.lastReplay||[];gameState.nextDamageBonus=1.0;
    if(data.deckSlots&&data.deckSlots[0]&&data.deckSlots[0].cards)gameState.deckSlots=data.deckSlots;else gameState.deckSlots=[{name:'',cards:[]},{name:'',cards:[]},{name:'',cards:[]}];
    var need={高校生:5,大学生:12,大学院生:20,助教:30,准教授:42,博士:55,教授:70};
    if(need[gameState.lastRank]&&gameState.playerLevel<need[gameState.lastRank]){gameState.playerLevel=need[gameState.lastRank];gameState.playerExp=Math.max(gameState.playerExp,expToReachLevel(gameState.playerLevel));}
    returnToMenu=false;fromBossPreview=false;pendingBoss=null;initDaily();checkAchievements(true);updateFieldUI();switchState('field');alert('ロードしました');
  }catch(e){alert('ロード失敗');}
}

function switchState(s){
  var ids=['deck-select-screen','field-screen','battle-screen','deck-edit-screen','gacha-screen','zukan-screen','achieve-screen','history-screen','quiz-only-screen','isomer-screen','lab-screen','refine-screen','synth-screen','tree-screen','boss-preview-screen'];
  for(var i=0;i<ids.length;i++){var el=document.getElementById(ids[i]);if(el)el.classList.remove('active');}
  if(s!=='field')closeFieldMenu(false);
  if(s==='deckSelection')document.getElementById('deck-select-screen').classList.add('active');
  if(s==='field'){document.getElementById('field-screen').classList.add('active');updateFieldUI();initThreeJS();}
  if(s==='bossPreview')document.getElementById('boss-preview-screen').classList.add('active');
  if(s==='battle'){returnToMenu=false;document.getElementById('battle-screen').classList.add('active');}
  if(s==='deckEdit'){document.getElementById('deck-edit-screen').classList.add('active');renderAttrFilters();renderDeckEdit();}
  if(s==='gacha'){document.getElementById('gacha-screen').classList.add('active');document.getElementById('gacha-reagents').innerText=gameState.reagents;document.getElementById('gacha-rank').innerText=getRank().name;renderGachaTypes();}
  if(s==='zukan'){document.getElementById('zukan-screen').classList.add('active');exitMemoMode();renderZukan();}
  if(s==='achieve'){document.getElementById('achieve-screen').classList.add('active');checkAchievements(true);renderAchieve();}
  if(s==='tree'){document.getElementById('tree-screen').classList.add('active');renderTree();}
  if(s==='history'){document.getElementById('history-screen').classList.add('active');document.getElementById('history-list').innerText=battleHistory.slice(-40).join('\n\n')||'履歴なし';}
  if(s==='quizOnly')document.getElementById('quiz-only-screen').classList.add('active');
  if(s==='isomer')document.getElementById('isomer-screen').classList.add('active');
  if(s==='lab'){document.getElementById('lab-screen').classList.add('active');renderLab();}
  if(s==='refine'){document.getElementById('refine-screen').classList.add('active');renderRefine();}
  if(s==='synth'){document.getElementById('synth-screen').classList.add('active');initMolBuilder();}
}
function openHistory(){fromBattleToHistory=true;switchState('history');}
function closeHistory(){if(fromBattleToHistory){fromBattleToHistory=false;document.querySelectorAll('.screen').forEach(function(el){el.classList.remove('active');});document.getElementById('battle-screen').classList.add('active');updateBattleUI();}else goBackFromMenu();}
function showLastReplay(){var r=gameState.lastReplay||[];document.getElementById('history-list').innerText=r.length?'【直前リプレイ】\n\n'+r.join('\n\n'):'リプレイなし';}

function updateFieldUI(){
  initDaily();
  document.getElementById('field-reagents').innerText=gameState.reagents;
  document.getElementById('field-hp').innerText=gameState.playerHP;
  document.getElementById('field-rank').innerText=getRank().name;
  document.getElementById('field-plv').innerText=gameState.playerLevel||1;
  document.getElementById('field-pexp').innerText=gameState.playerExp||0;
  document.getElementById('field-pnext').innerText=expToReachLevel((gameState.playerLevel||1)+1);
  document.getElementById('field-kills').innerText=gameState.kills;
  document.getElementById('field-lab').innerText=gameState.labLevel;
  document.getElementById('daily-hint').innerText=gameState.dailyDone?'📅 日替わり達成済':'📅 今日: '+getDailyLabel();
  var n=uniqCount(gameState);document.getElementById('zukan-comp-hint').innerText='図鑑 '+n+'/'+ALL_CARDS.length;
  document.getElementById('tree-hint').innerText='反応ツリー '+treeDoneCount(gameState)+'/'+REACTION_TREE.length;
}
function renderTree(){document.getElementById('tree-done').innerText=treeDoneCount(gameState);document.getElementById('tree-total').innerText=REACTION_TREE.length;var list=document.getElementById('tree-list');list.innerHTML='';var chains={};REACTION_TREE.forEach(function(r){if(!chains[r.chain])chains[r.chain]=[];chains[r.chain].push(r);});Object.keys(chains).forEach(function(ch){var h=document.createElement('div');h.style.cssText='color:#f9a8d4;font-size:13px;margin:10px 0 6px';h.innerText='▸ '+ch;list.appendChild(h);chains[ch].forEach(function(r){var done=!!(gameState.recipes&&gameState.recipes[r.id]);var div=document.createElement('div');div.className='tree-node'+(done?' done':'');div.innerHTML='<div>'+(done?'✅ ':'🔒 ')+r.name+'</div><div style="font-size:11px;color:#94a3b8">'+r.path+'</div><div style="font-size:11px;color:#fbbf24">'+(done?'解放済':'未解放')+' · 試薬'+r.reward+'</div>';list.appendChild(div);});});}

function assignStarterDeck(type){
  gameState.currentDeck=[];gameState.collection=[];gameState.deckListOrder=[];returnToMenu=false;fromBossPreview=false;pendingBoss=null;
  gameState.playerLevel=1;gameState.playerExp=0;gameState.lastRank='初学者';gameState.recipes={};
  var names=type==='Aromatic'?['ベンゼン','トルエン','濃硝酸','濃硫酸','フェノール','グルコース','ニトロ基']:type==='Polymer'?['エチレン','臭素','塩素','重合触媒(Ziegler)','グルコース','エタノール']:['エタノール','酢酸','水酸化ナトリウム','過マンガン酸カリウム','グルコース','アセトアルデヒド'];
  var base=[];for(var i=0;i<names.length;i++){var c=ALL_CARDS.find(function(x){return x.name===names[i];});if(c)base.push(c);}
  for(var j=0;j<40;j++){var src=base[j%base.length];gameState.currentDeck.push(Object.assign({},src,{id:uid()}));gameState.collection.push(Object.assign({},src,{id:uid()}));}
  gameState.playerHP=gameState.playerMaxHP;initDaily();switchState('field');
}
function finishDeckEdit(){
  if(gameState.currentDeck.length<20){alert('最低20枚');return;}
  if(fromBossPreview&&pendingBoss){fromBossPreview=false;showBossPreview(pendingBoss);return;}
  goBackFromMenu();
}

/* ===== ボスプレビュー ===== */
function showBossPreview(m){
  pendingBoss=m;
  gameState.currentMonster=m;
  document.getElementById('bp-name').innerText=m.name;
  document.getElementById('bp-hp').innerText=m.hp;
  document.getElementById('bp-atk').innerText=m.attackPower;
  var tags=document.getElementById('bp-weak-tags');tags.innerHTML='';
  (m.weakness||[]).forEach(function(w){
    var sp=document.createElement('span');sp.className='boss-weak-tag';
    sp.innerText='弱点: '+(ATTR_JP[w]||w);tags.appendChild(sp);
  });
  document.getElementById('bp-cond').innerText=m.condition?('有効条件: '+(ATTR_JP[m.condition]||m.condition)+' 属性が効く'):'条件なし';
  document.getElementById('bp-turn').innerText=m.turnLimit?('ターン制限: '+m.turnLimit):'';
  switchState('bossPreview');
}
function cancelBossPreview(){pendingBoss=null;fromBossPreview=false;switchState('field');}
function confirmBossBattle(){if(!pendingBoss)return;var m=pendingBoss;pendingBoss=null;fromBossPreview=false;gameState.currentMonster=m;startBattle(false);}
function bossPreviewToDeck(){fromBossPreview=true;returnToMenu=false;switchState('deckEdit');}

/* ===== 分子ビルダー（P含む） ===== */
function initMolBuilder(){
  document.getElementById('synth-reagents').innerText=gameState.reagents;
  var pal=document.getElementById('atom-palette');pal.innerHTML='';
  MOL_PARTS.forEach(function(p){
    var b=document.createElement('button');b.type='button';b.className='atom-btn '+p.cls;
    b.innerHTML=p.label+'<small>'+p.val+'手</small>';
    b.onclick=function(){addMolAtom(p);};pal.appendChild(b);
  });
  var canvas=document.getElementById('mol-canvas');
  function resize(){var w=canvas.parentElement.clientWidth,h=canvas.parentElement.clientHeight;canvas.width=w*devicePixelRatio;canvas.height=h*devicePixelRatio;canvas.style.width=w+'px';canvas.style.height=h+'px';drawMol();}
  resize();
  canvas.onclick=function(e){
    var rect=canvas.getBoundingClientRect(),x=e.clientX-rect.left,y=e.clientY-rect.top;
    if(!bondMode)return;
    var hit=hitAtom(x,y);if(hit==null)return;
    if(bondPick==null){bondPick=hit;drawMol();return;}
    if(bondPick===hit){bondPick=null;drawMol();return;}
    tryAddBond(bondPick,hit);bondPick=null;drawMol();updateMolStatus();
  };
  clearMol();
}
function pushMolHist(){molHistory.push({a:JSON.parse(JSON.stringify(molAtoms)),b:JSON.parse(JSON.stringify(molBonds))});if(molHistory.length>30)molHistory.shift();}
function undoMol(){if(!molHistory.length)return;var last=molHistory.pop();molAtoms=last.a;molBonds=last.b;bondPick=null;drawMol();updateMolStatus();}
function clearMol(){molAtoms=[];molBonds=[];bondPick=null;molHistory=[];drawMol();updateMolStatus();document.getElementById('synth-msg').innerText='';}
function toggleBondMode(){bondMode=!bondMode;bondPick=null;var btn=document.getElementById('bond-mode-btn');btn.innerText='結合モード: '+(bondMode?'ON':'OFF');btn.className='glass-btn mini-btn '+(bondMode?'warn bond-mode':'primary');drawMol();}
function addMolAtom(p){
  pushMolHist();
  var canvas=document.getElementById('mol-canvas'),w=canvas.clientWidth,h=canvas.clientHeight;
  molAtoms.push({id:uid(),sym:p.sym,val:p.val,maxVal:p.val,atk:p.atk||0,heal:p.heal||0,x:40+Math.random()*(w-80),y:40+Math.random()*(h-80),cls:p.cls});
  drawMol();updateMolStatus();
}
function usedBonds(idx){var n=0;molBonds.forEach(function(b){if(b[0]===idx||b[1]===idx)n++;});return n;}
function freeVal(idx){return molAtoms[idx].maxVal-usedBonds(idx);}
function tryAddBond(i,j){
  if(i===j)return;
  if(molBonds.some(function(b){return (b[0]===i&&b[1]===j)||(b[0]===j&&b[1]===i);}))return;
  if(freeVal(i)<=0||freeVal(j)<=0){alert('結合の手が足りません');return;}
  pushMolHist();molBonds.push([i,j]);pullAtomsAdjacent(i,j);layoutConnectedComponent(i);
}
function pullAtomsAdjacent(i,j){
  var a=molAtoms[i],b=molAtoms[j];if(!a||!b)return;
  var dx=b.x-a.x,dy=b.y-a.y,dist=Math.sqrt(dx*dx+dy*dy)||1,target=44;
  var mx=(a.x+b.x)/2,my=(a.y+b.y)/2,nx=dx/dist,ny=dy/dist;
  a.x=mx-nx*target/2;a.y=my-ny*target/2;b.x=mx+nx*target/2;b.y=my+ny*target/2;
  clampAtomPos(a);clampAtomPos(b);
}
function clampAtomPos(a){var canvas=document.getElementById('mol-canvas');if(!canvas)return;var w=canvas.clientWidth,h=canvas.clientHeight;a.x=Math.max(24,Math.min(w-24,a.x));a.y=Math.max(24,Math.min(h-24,a.y));}
function layoutConnectedComponent(startIdx){
  var n=molAtoms.length;if(!n)return;
  var adj=[];for(var i=0;i<n;i++)adj[i]=[];
  molBonds.forEach(function(b){if(b[0]<n&&b[1]<n){adj[b[0]].push(b[1]);adj[b[1]].push(b[0]);}});
  var seen={},queue=[startIdx],order=[];seen[startIdx]=true;
  while(queue.length){var u=queue.shift();order.push(u);adj[u].forEach(function(v){if(!seen[v]){seen[v]=true;queue.push(v);}});}
  if(order.length<=1)return;
  for(var iter=0;iter<8;iter++){
    molBonds.forEach(function(b){
      if(!seen[b[0]]||!seen[b[1]])return;
      var a=molAtoms[b[0]],c=molAtoms[b[1]],dx=c.x-a.x,dy=c.y-a.y,dist=Math.sqrt(dx*dx+dy*dy)||1,f=(dist-44)*0.35,nx=dx/dist,ny=dy/dist;
      a.x+=nx*f*0.5;a.y+=ny*f*0.5;c.x-=nx*f*0.5;c.y-=ny*f*0.5;
    });
    for(var p=0;p<order.length;p++)for(var q=p+1;q<order.length;q++){
      var A=molAtoms[order[p]],B=molAtoms[order[q]],dx2=B.x-A.x,dy2=B.y-A.y,d2=Math.sqrt(dx2*dx2+dy2*dy2)||1;
      if(d2<32){var push=(32-d2)*0.5,nx2=dx2/d2,ny2=dy2/d2;A.x-=nx2*push;A.y-=ny2*push;B.x+=nx2*push;B.y+=ny2*push;}
    }
  }
  order.forEach(function(i){clampAtomPos(molAtoms[i]);});
}
function hitAtom(x,y){for(var i=0;i<molAtoms.length;i++){var a=molAtoms[i],dx=a.x-x,dy=a.y-y;if(dx*dx+dy*dy<400)return i;}return null;}
function drawMol(){
  var canvas=document.getElementById('mol-canvas');if(!canvas)return;
  var ctx=canvas.getContext('2d'),dpr=devicePixelRatio||1;
  ctx.setTransform(dpr,0,0,dpr,0,0);var w=canvas.clientWidth,h=canvas.clientHeight;ctx.clearRect(0,0,w,h);
  ctx.strokeStyle='#64748b';ctx.lineWidth=2;
  molBonds.forEach(function(b){var a=molAtoms[b[0]],c=molAtoms[b[1]];if(!a||!c)return;ctx.beginPath();ctx.moveTo(a.x,a.y);ctx.lineTo(c.x,c.y);ctx.stroke();});
  molAtoms.forEach(function(a,i){
    var free=freeVal(i);
    ctx.beginPath();ctx.arc(a.x,a.y,16,0,Math.PI*2);
    ctx.fillStyle=i===bondPick?'#fbbf24':(a.cls==='O'?'#7f1d1d':a.cls==='N'?'#1e3a5f':a.cls==='Cl'?'#14532d':a.cls==='S'?'#78350f':a.cls==='P'?'#9d174d':a.cls==='FG'?'#581c87':'#334155');
    ctx.fill();ctx.strokeStyle=free>0?'#38bdf8':'#94a3b8';ctx.lineWidth=free>0?2:1;ctx.stroke();
    ctx.fillStyle='#fff';ctx.font='12px sans-serif';ctx.textAlign='center';ctx.textBaseline='middle';ctx.fillText(a.sym,a.x,a.y);
    if(free>0){ctx.fillStyle='#7dd3fc';ctx.font='9px sans-serif';ctx.fillText(free,a.x,a.y+22);}
  });
}
function updateMolStatus(){
  var atk=0,heal=0,open=0;
  molAtoms.forEach(function(a,i){atk+=a.atk;heal+=a.heal;open+=freeVal(i);});
  atk=Math.min(300,atk);var cost=synthCostForDamage(Math.max(50,atk));
  document.getElementById('mol-status').innerHTML='原子 '+molAtoms.length+' · 結合 '+molBonds.length+' · 余手 <b style="color:'+(open?'#f87171':'#4ade80')+'">'+open+'</b><br>ダメージ <b>'+atk+'</b>（上限300）'+(heal?' / 回復'+heal:'')+' · 試薬 <b style="color:#fbbf24">'+cost+'</b><br>'+(open>0?'<span style="color:#f87171">手が余っているためカード化不可</span>':(atk<50?'<span style="color:#fbbf24">最低50ダメージ必要</span>':'<span style="color:#4ade80">完成可能</span>'));
}
function createOriginalCard(){
  if(molAtoms.length<1){alert('原子を置いてください');return;}
  var open=0,atk=0,heal=0,parts=[];
  molAtoms.forEach(function(a,i){open+=freeVal(i);atk+=a.atk;heal+=a.heal;parts.push(a.sym);});
  if(open>0){alert('手が余っている状態ではカードにできません（余手'+open+'）');return;}
  atk=Math.min(300,atk);if(atk<50){alert('ダメージが弱すぎます（最低50）');return;}
  var cost=synthCostForDamage(atk);if(gameState.reagents<cost){alert('試薬不足（必要'+cost+'）');return;}
  gameState.reagents-=cost;
  var custom=document.getElementById('orig-name').value.trim();
  var name=custom||('合成分子·'+parts.slice(0,4).join('')+(parts.length>4?'…':''));
  var card={name:name,formula:parts.join('-'),attackPower:atk,healPower:heal,attribute:heal>0&&atk===0?'Nutrient':(parts.indexOf('P')>=0?'Reagent':(parts.indexOf('NO2')>=0||parts.indexOf('N')>=0?'Aromatic':(parts.indexOf('O')>=0||parts.indexOf('OH')>=0?'Alcohol':'Alkane'))),rarity:'ORIGIN',id:uid(),origin:true};
  gameState.collection.push(card);gameState.flags.origin=true;gameState.flags.originCount=(gameState.flags.originCount||0)+1;
  checkAchievements();saveGame(true);
  document.getElementById('synth-msg').innerText='作成: '+name+'（'+atk+'ダメージ）試薬-'+cost;
  document.getElementById('synth-reagents').innerText=gameState.reagents;document.getElementById('orig-name').value='';clearMol();
}
function renameOriginCard(oldName){
  var samples=gameState.collection.filter(function(c){return c.name===oldName&&(c.rarity==='ORIGIN'||c.origin);});
  if(!samples.length){alert('オリジンカードではありません');return;}
  if(gameState.reagents<25){alert('試薬が足りません（必要25）');return;}
  var neu=prompt('新しい名前（最大20文字）',oldName);if(neu==null)return;
  neu=neu.trim().slice(0,20);if(!neu||neu===oldName)return;
  if(gameState.collection.some(function(c){return c.name===neu;})){alert('同名カードが既にあります');return;}
  gameState.reagents-=25;
  gameState.collection.forEach(function(c){if(c.name===oldName&&(c.rarity==='ORIGIN'||c.origin))c.name=neu;});
  gameState.currentDeck.forEach(function(c){if(c.name===oldName&&(c.rarity==='ORIGIN'||c.origin))c.name=neu;});
  gameState.deckSlots.forEach(function(s){if(s.cards)s.cards.forEach(function(c){if(c.name===oldName)c.name=neu;});});
  saveGame(true);renderDeckEdit();alert('改名完了（試薬-25）\n'+oldName+' → '+neu);
}

/* ガチャ・図鑑など（研究室ブースト込み） */
function renderGachaTypes(){
  var box=document.getElementById('gacha-types');box.innerHTML='';
  GACHA_TYPES.forEach(function(g){
    var pool=g.pool(),byR={};pool.forEach(function(c){byR[c.rarity]=(byR[c.rarity]||0)+1;});
    var div=document.createElement('div');div.className='gacha-type-card';
    div.innerHTML='<h4>'+g.name+'（試薬 '+g.cost+'）</h4><p>'+g.desc+'</p><p style="color:#67e8f9">内訳: '+Object.keys(byR).map(function(r){return r+':'+byR[r];}).join(' / ')+'</p>';
    var row=document.createElement('div');row.className='gacha-actions';
    var listBtn=document.createElement('button');listBtn.type='button';listBtn.className='glass-btn slate';listBtn.innerText='一覧';listBtn.onclick=function(){showPoolModal(g);};
    var pullBtn=document.createElement('button');pullBtn.type='button';pullBtn.className='glass-btn pink';pullBtn.innerText='引く（'+g.cost+'）';pullBtn.onclick=function(){drawGachaType(g.id);};
    row.appendChild(listBtn);row.appendChild(pullBtn);div.appendChild(row);box.appendChild(div);
  });
}
function showPoolModal(g){var pool=g.pool().slice().sort(function(a,b){var d=(RARITY_ORDER[a.rarity]||9)-(RARITY_ORDER[b.rarity]||9);return d||a.name.localeCompare(b.name,'ja');});document.getElementById('pool-title').innerText=g.name;var html='';pool.forEach(function(c){var p=c.name==='ボツリヌス毒素'?'毎ターン200ダメージ':(c.attackPower===Infinity?'∞ダメージ':(c.attackPower||0)+'ダメージ');if((c.healPower||0)>0)p+=' / '+c.healPower+'回復';html+='<div class="pool-line"><span><span class="card-rarity rarity-'+c.rarity+'">'+c.rarity+'</span> '+c.name+'</span><span style="color:#fbbf24">'+p+'</span></div>';});document.getElementById('pool-body').innerHTML=html;document.getElementById('pool-modal').style.display='block';}
function closePoolModal(){document.getElementById('pool-modal').style.display='none';}
function drawGachaType(id){
  if(gachaBusy)return;var g=GACHA_TYPES.find(function(x){return x.id===id;});if(!g)return;
  if(gameState.reagents<g.cost){alert('試薬不足');return;}
  gameState.reagents-=g.cost;document.getElementById('gacha-reagents').innerText=gameState.reagents;
  gachaBusy=true;var res=document.getElementById('gacha-result');res.classList.remove('reveal');res.classList.add('rolling');
  res.innerHTML='<div style="font-size:14px;color:#e879f9">合成中…</div>';
  var ticks=0,iv=setInterval(function(){ticks++;var flash=g.pool()[Math.floor(Math.random()*g.pool().length)];res.innerHTML='<div style="font-size:11px;opacity:.7">'+g.name+'</div><div style="font-size:15px;margin-top:8px">'+flash.name+'</div>';if(ticks>=12){clearInterval(iv);res.classList.remove('rolling');finishGachaPull(g,res);}},80);
}
function finishGachaPull(g,res){
  var boost=getRank().gachaBoost+labGachaBoost(),rates=g.rates(boost),rand=Math.random()*100,rarity='R',order=['SSSR','SSR','SR','R'];
  for(var i=0;i<order.length;i++){if(rates[order[i]]==null)continue;if(rand<rates[order[i]]){rarity=order[i];break;}}
  var pool=g.pool().filter(function(c){return c.rarity===rarity;});if(!pool.length)pool=g.pool();
  var pulled=pool[Math.floor(Math.random()*pool.length)];var newCard=Object.assign({},pulled,{id:uid()});
  gameState.collection.push(newCard);gameState.flags.gachaCount=(gameState.flags.gachaCount||0)+1;saveGame(true);checkAchievements();
  var val=newCard.name==='ボツリヌス毒素'?'毎ターン200ダメージ':(newCard.attackPower===Infinity?'∞ダメージ':((newCard.attackPower||0)>0&&(newCard.healPower||0)>0?newCard.attackPower+'ダメージ / '+newCard.healPower+'回復':(newCard.healPower>0?newCard.healPower+'回復':(newCard.attackPower||0)+'ダメージ')));
  res.classList.add('reveal');res.innerHTML='<div style="font-size:11px;color:#94a3b8">'+g.name+'</div><span class="card-rarity rarity-'+newCard.rarity+'">'+newCard.rarity+'</span><div style="font-size:18px;margin:8px 0">'+newCard.name+'</div><div style="font-size:11px;color:#cbd5e1">'+newCard.formula+'</div><div style="font-size:12px;color:#fbbf24;margin-top:6px">'+val+'</div>';gachaBusy=false;
}

function setZukanFilter(f){zukanFilter=f;renderZukan();}
function getZukanNames(){var names=[],seen={};gameState.collection.forEach(function(c){if(!seen[c.name]){seen[c.name]=1;names.push(c.name);}});return names.filter(function(name){var c=gameState.collection.find(function(x){return x.name===name;})||ALL_CARDS.find(function(x){return x.name===baseName(name);});if(!c)return false;if(zukanFilter==='all')return true;return c.rarity===zukanFilter;}).sort(function(a,b){return a.localeCompare(b,'ja');});}
function renderZukan(){var names=getZukanNames();document.getElementById('zukan-count').innerText=names.length;var list=document.getElementById('zukan-list');list.innerHTML='';list.style.display='block';document.getElementById('memo-panel').style.display='none';if(!names.length){list.innerHTML='<div style="color:#94a3b8">該当なし</div>';return;}names.forEach(function(name){var c=gameState.collection.find(function(x){return x.name===name;})||ALL_CARDS.find(function(x){return x.name===baseName(name);});var div=document.createElement('div');div.className='zukan-item';div.innerHTML='<div>'+name+' <span class="card-rarity rarity-'+c.rarity+'">'+c.rarity+'</span></div><div style="margin-top:6px;font-size:12px">分子式: <b>'+(c.formula||'-')+'</b></div><div style="font-size:12px;color:#94a3b8">'+fmt(c.attackPower)+'ダメージ / '+(c.healPower||0)+'回復</div>';list.appendChild(div);});}
function startMemoMode(){memoList=getZukanNames();if(!memoList.length){alert('空');return;}memoIdx=0;memoShow=false;document.getElementById('zukan-list').style.display='none';document.getElementById('memo-panel').style.display='block';showMemoCard();}
function showMemoCard(){var name=memoList[memoIdx];var c=gameState.collection.find(function(x){return x.name===name;})||ALL_CARDS.find(function(x){return x.name===baseName(name);});document.getElementById('memo-q').innerText=name;var a=document.getElementById('memo-a');a.innerText='分子式: '+(c.formula||'-')+'\n'+fmt(c.attackPower)+'ダメージ / '+(c.healPower||0)+'回復';a.className=memoShow?'':'memo-hidden';}
function toggleMemoAnswer(){memoShow=!memoShow;document.getElementById('memo-a').className=memoShow?'':'memo-hidden';if(memoShow){gameState.flags.memoCount=(gameState.flags.memoCount||0)+1;checkAchievements();}}
function nextMemoCard(){memoIdx=(memoIdx+1)%memoList.length;memoShow=false;showMemoCard();}
function exitMemoMode(){document.getElementById('memo-panel').style.display='none';renderZukan();}
function renderAchieve(){var list=document.getElementById('achieve-list');list.innerHTML='';var done=0;ACHIEVEMENTS.forEach(function(a){var d=!!gameState.achieved[a.id];if(d)done++;var div=document.createElement('div');div.className='achieve-item '+(d?'done':'locked');div.innerHTML='<div><div>'+(d?'✅':'🔒')+' '+a.name+'</div><div style="font-size:11px;color:#94a3b8">'+a.desc+'</div></div><div style="color:#fbbf24">+'+a.reward+'</div>';list.appendChild(div);});document.getElementById('achieve-done').innerText=done;document.getElementById('achieve-total').innerText=ACHIEVEMENTS.length;}

function saveDeckSlot(i){if(gameState.currentDeck.length<20){alert('最低20枚');return;}var inp=document.getElementById('preset-name-'+i);var nm=(inp&&inp.value.trim())||(gameState.deckSlots[i]&&gameState.deckSlots[i].name)||('編成'+(i+1));gameState.deckSlots[i]={name:nm,cards:gameState.currentDeck.map(function(c){return Object.assign({},c);})};if(inp)inp.value=nm;alert('保存');renderDeckEdit();}
function loadDeckSlot(i){var slot=gameState.deckSlots[i];if(!slot||!slot.cards||!slot.cards.length){alert('空');return;}var owned={};gameState.collection.forEach(function(c){owned[c.name]=(owned[c.name]||0)+1;});var used={},rebuilt=[];for(var j=0;j<slot.cards.length;j++){var c=slot.cards[j];if((used[c.name]||0)<(owned[c.name]||0)){used[c.name]=(used[c.name]||0)+1;rebuilt.push(Object.assign({},c,{id:uid()}));}}gameState.currentDeck=rebuilt;var inp=document.getElementById('preset-name-'+i);if(inp)inp.value=slot.name||'';renderDeckEdit();}
function calcSynthRate(){var names=new Set(gameState.currentDeck.map(function(c){return baseName(c.name);}));if(!names.size)return{rate:0,ok:0,total:SYNTH_PAIRS.length,missing:[],healCount:0};var ok=0,missing=[];SYNTH_PAIRS.forEach(function(pair){var hasA=pair.a.some(function(n){return names.has(n);}),hasB=pair.b.some(function(n){return names.has(n);});if(hasA&&hasB)ok++;else if(hasA&&!hasB)missing.push(pair.a.find(function(n){return names.has(n);})+'の相手不足');else if(!hasA&&hasB)missing.push(pair.b.find(function(n){return names.has(n);})+'の相手不足');});return{rate:Math.round(ok/SYNTH_PAIRS.length*100),ok:ok,total:SYNTH_PAIRS.length,missing:missing.slice(0,4),healCount:gameState.currentDeck.filter(function(c){return (c.healPower||0)>0;}).length};}
function getReactionHint(selected){var n=selected.map(function(c){return baseName(c.name);});if(n.indexOf('酢酸')>=0)return 'ヒント: エタノールかNaOH';if(n.indexOf('エタノール')>=0)return 'ヒント: 酢酸・濃硫酸・Na';if(n.indexOf('ベンゼン')>=0)return 'ヒント: 濃硝酸・ニトロ基';return '長押しで反応確認';}

function openRecommendModal(){document.getElementById('rec-attr-pick').style.display='none';document.getElementById('rec-modal').style.display='block';}
function closeRecommendModal(){document.getElementById('rec-modal').style.display='none';}
function runRecommend(mode){
  if(mode==='attr'){
    var box=document.getElementById('rec-attr-pick');box.style.display='block';box.innerHTML='';
    ATTR_LIST.forEach(function(a){
      var b=document.createElement('button');b.type='button';b.className='attr-chip';b.style.margin='3px';b.innerText=ATTR_JP[a]||a;
      b.onclick=function(){closeRecommendModal();recommendDeck('attr',a);};
      box.appendChild(b);
    });
    return;
  }
  closeRecommendModal();recommendDeck(mode,null);
}
function recommendDeck(mode,focusAttr){
  if(!gameState.collection.length){alert('所持なし');return;}
  var owned={};gameState.collection.forEach(function(c){owned[c.name]=(owned[c.name]||0)+1;});
  var used={};function pick(name){if((used[name]||0)>=(owned[name]||0))return false;used[name]=(used[name]||0)+1;return true;}
  function total(){var s=0;for(var k in used)s+=used[k];return s;}
  var MAX=50;
  if(mode==='power'){
    Object.keys(owned).sort(function(a,b){return powerValue(gameState.collection.find(function(x){return x.name===b;}))-powerValue(gameState.collection.find(function(x){return x.name===a;}));}).forEach(function(name){while(total()<MAX&&pick(name)){}});
  }else if(mode==='combo'){
    COMBO_CORE.forEach(function(bn){Object.keys(owned).forEach(function(name){if(baseName(name)===bn)while(total()<MAX&&pick(name)){};});});
    SYNTH_PAIRS.forEach(function(pair){for(var t=0;t<8&&total()<MAX-1;t++){var aKey=null,bKey=null,i,k;for(i=0;i<pair.a.length;i++){for(k in owned){if(baseName(k)===pair.a[i]&&(used[k]||0)<owned[k]){aKey=k;break;}}if(aKey)break;}for(i=0;i<pair.b.length;i++){for(k in owned){if(baseName(k)===pair.b[i]&&(used[k]||0)<owned[k]){bKey=k;break;}}if(bKey)break;}if(!aKey||!bKey)break;pick(aKey);pick(bKey);}});
    Object.keys(owned).forEach(function(name){while(total()<MAX&&pick(name)){}});
  }else if(mode==='attr'&&focusAttr){
    Object.keys(owned).filter(function(n){var c=gameState.collection.find(function(x){return x.name===n;});return c&&c.attribute===focusAttr;}).sort(function(a,b){return powerValue(gameState.collection.find(function(x){return x.name===b;}))-powerValue(gameState.collection.find(function(x){return x.name===a;}));}).forEach(function(name){while(total()<MAX&&pick(name)){}});
    Object.keys(owned).forEach(function(name){while(total()<MAX&&pick(name)){}});
  }else{
    var healN=0;Object.keys(owned).filter(function(n){var c=gameState.collection.find(function(x){return x.name===n;});return c&&(c.healPower||0)>0;}).forEach(function(name){while(healN<8&&total()<MAX&&pick(name))healN++;});
    SYNTH_PAIRS.forEach(function(pair){for(var t=0;t<10&&total()<MAX-1;t++){var aKey=null,bKey=null,i,k;for(i=0;i<pair.a.length;i++){for(k in owned){if(baseName(k)===pair.a[i]&&(used[k]||0)<owned[k]){aKey=k;break;}}if(aKey)break;}for(i=0;i<pair.b.length;i++){for(k in owned){if(baseName(k)===pair.b[i]&&(used[k]||0)<owned[k]){bKey=k;break;}}if(bKey)break;}if(!aKey||!bKey)break;pick(aKey);pick(bKey);}});
    Object.keys(owned).sort(function(a,b){return powerValue(gameState.collection.find(function(x){return x.name===b;}))-powerValue(gameState.collection.find(function(x){return x.name===a;}));}).forEach(function(name){while(total()<MAX&&pick(name)){}});
  }
  var newDeck=[];for(var name in used){var need=used[name];for(var i=0;i<gameState.collection.length&&need>0;i++){if(gameState.collection[i].name===name){newDeck.push(Object.assign({},gameState.collection[i],{id:uid()}));need--;}}}
  gameState.currentDeck=newDeck;renderDeckEdit();
  alert('おすすめ完了: '+(mode==='power'?'火力':mode==='combo'?'コンボ':mode==='attr'?(ATTR_JP[focusAttr]||focusAttr)+'属性':'バランス')+' '+newDeck.length+'枚');
}

function renderAttrFilters(){
  var row=document.getElementById('attr-filter-row');if(!row)return;row.innerHTML='';
  var all=document.createElement('button');all.type='button';all.className='attr-chip'+(deckAttrFilter==='all'?' on':'');all.innerText='全て';
  all.onclick=function(){deckAttrFilter='all';renderAttrFilters();renderDeckEdit();};row.appendChild(all);
  var used={};gameState.collection.forEach(function(c){used[c.attribute]=1;});
  Object.keys(used).sort().forEach(function(a){
    var b=document.createElement('button');b.type='button';b.className='attr-chip'+(deckAttrFilter===a?' on':'');
    b.innerText=ATTR_JP[a]||a;b.onclick=function(){deckAttrFilter=a;renderAttrFilters();renderDeckEdit();};row.appendChild(b);
  });
}

function startQuizOnly(){qoScore=0;qoTotal=0;document.getElementById('qo-score').innerText='0';document.getElementById('qo-total').innerText='0';document.getElementById('qo-feedback').innerText='';switchState('quizOnly');nextQuizOnly();}
function nextQuizOnly(){var q=QUIZ_BANK[Math.floor(Math.random()*QUIZ_BANK.length)];document.getElementById('qo-question').innerText=q.q;document.getElementById('qo-feedback').innerText='';var box=document.getElementById('qo-options');box.innerHTML='';q.opts.map(function(t,i){return{text:t,ok:i===q.ok};}).sort(function(){return Math.random()-0.5;}).forEach(function(c){var b=document.createElement('button');b.className='quiz-btn';b.innerText=c.text;b.onclick=function(){qoTotal++;if(c.ok){qoScore++;gameState.flags.quizOk=(gameState.flags.quizOk||0)+1;checkAchievements();document.getElementById('qo-feedback').innerText='⭕ '+q.ex;}else document.getElementById('qo-feedback').innerText='❌ '+q.ex;document.getElementById('qo-score').innerText=qoScore;document.getElementById('qo-total').innerText=qoTotal;for(var i=0;i<box.children.length;i++)box.children[i].disabled=true;};box.appendChild(b);});}
function startIsomerMode(){isoScore=0;isoStreak=0;document.getElementById('iso-score').innerText='0';document.getElementById('iso-streak').innerText='0';document.getElementById('iso-feedback').innerText='';switchState('isomer');nextIsomerQ();}
function nextIsomerQ(){var q=ISOMER_BANK[Math.floor(Math.random()*ISOMER_BANK.length)];document.getElementById('iso-question').innerText=q.q;document.getElementById('iso-feedback').innerText='';var box=document.getElementById('iso-options');box.innerHTML='';q.opts.map(function(t,i){return{text:t,ok:i===q.ok};}).sort(function(){return Math.random()-0.5;}).forEach(function(c){var b=document.createElement('button');b.className='quiz-btn';b.innerText=c.text;b.onclick=function(){if(c.ok){isoStreak++;var gain=8+Math.min(isoStreak,5)*2;isoScore+=gain;gameState.reagents+=gain;gameState.flags.isoOk=(gameState.flags.isoOk||0)+1;checkAchievements();document.getElementById('iso-feedback').innerText='⭕ +'+gain;}else{isoStreak=0;document.getElementById('iso-feedback').innerText='❌';}document.getElementById('iso-score').innerText=isoScore;document.getElementById('iso-streak').innerText=isoStreak;for(var i=0;i<box.children.length;i++)box.children[i].disabled=true;};box.appendChild(b);});}
function renderLab(){
  document.getElementById('lab-lv').innerText=gameState.labLevel;
  var next=LAB_THRESH[gameState.labLevel]||800,prev=LAB_THRESH[gameState.labLevel-1]||0;
  document.getElementById('lab-exp').innerText=gameState.labExp;document.getElementById('lab-next').innerText=gameState.labLevel>=10?'MAX':next;
  document.getElementById('lab-bar').style.width=gameState.labLevel>=10?'100%':Math.min(100,Math.floor((gameState.labExp-prev)/Math.max(1,next-prev)*100))+'%';
  var html='';for(var i=0;i<LAB_PERKS.length;i++)html+='<div style="opacity:'+(gameState.labLevel>i?1:0.45)+'">'+(gameState.labLevel>i?'✅':'🔒')+' '+LAB_PERKS[i]+'</div>';
  document.getElementById('lab-perks').innerHTML=html;
  document.getElementById('lab-free-gacha-btn').disabled=!(gameState.labLevel>=3&&gameState.labFreeDate!==todayStr());
  document.getElementById('lab-msg').innerText=gameState.labLevel<3?'無料はLv3から':(gameState.labFreeDate===todayStr()?'今日使用済':'OK');
}
function labFreeGacha(){if(gameState.labLevel<3||gameState.labFreeDate===todayStr())return;gameState.labFreeDate=todayStr();gameState.reagents+=100;returnToMenu=true;switchState('gacha');drawGachaType('normal');}
function renderRefine(){var counts={};gameState.collection.forEach(function(c){if(String(c.name).indexOf('精製')===0)return;counts[c.name]=(counts[c.name]||0)+1;});var list=document.getElementById('refine-list');list.innerHTML='';Object.keys(counts).sort(function(a,b){return a.localeCompare(b,'ja');}).forEach(function(name){var n=counts[name],div=document.createElement('div');div.className='deck-item';div.innerHTML='<div>'+name+' ×'+n+'</div>';var btn=document.createElement('button');btn.type='button';btn.className='glass-btn mini-btn warn';btn.innerText='精製';btn.disabled=n<3;btn.onclick=function(){doRefine(name);};div.appendChild(btn);list.appendChild(div);});}
function doRefine(name){var cards=gameState.collection.filter(function(c){return c.name===name;});if(cards.length<3){alert('3枚必要');return;}var rem=3;gameState.collection=gameState.collection.filter(function(c){if(c.name===name&&rem>0){rem--;return false;}return true;});var drem=3;gameState.currentDeck=gameState.currentDeck.filter(function(c){if(c.name===name&&drem>0){drem--;return false;}return true;});var base=cards[0];gameState.collection.push(Object.assign({},base,{name:'精製'+name,attackPower:base.attackPower===Infinity?Infinity:Math.floor((base.attackPower||0)*1.15),healPower:Math.floor((base.healPower||0)*1.15),id:uid()}));gameState.flags.refined=true;gameState.flags.refineCount=(gameState.flags.refineCount||0)+1;checkAchievements();alert('精製完了');renderRefine();}

function createHumanoidMesh(){var g=new THREE.Group(),skin=new THREE.MeshLambertMaterial({color:0xffdbac}),body=new THREE.MeshLambertMaterial({color:0x0284c7}),leg=new THREE.MeshLambertMaterial({color:0x1e293b});var head=new THREE.Mesh(new THREE.SphereGeometry(0.25,16,16),skin);head.position.y=0.85;g.add(head);var torso=new THREE.Mesh(new THREE.CylinderGeometry(0.2,0.15,0.6,12),body);torso.position.y=0.45;g.add(torso);[[-0.28,0.45],[0.28,0.45]].forEach(function(p){var a=new THREE.Mesh(new THREE.CylinderGeometry(0.06,0.06,0.4,8),body);a.position.set(p[0],p[1],0);g.add(a);});[[-0.1,0.15],[0.1,0.15]].forEach(function(p){var a=new THREE.Mesh(new THREE.CylinderGeometry(0.07,0.07,0.45,8),leg);a.position.set(p[0],p[1],0);g.add(a);});return g;}
function createMoleculeMesh(col){var g=new THREE.Group(),m=new THREE.MeshLambertMaterial({color:col}),s=new THREE.MeshLambertMaterial({color:0xffffff});g.add(new THREE.Mesh(new THREE.SphereGeometry(0.5,16,16),m));[[0.7,0.45,0],[-0.7,0.45,0],[0,-0.65,0.45]].forEach(function(p){var a=new THREE.Mesh(new THREE.SphereGeometry(0.25,12,12),s);a.position.set(p[0],p[1],p[2]);g.add(a);});return g;}

var scene,camera,renderer,playerNode,monsters=[],targetPlayerPos={x:0,z:0},isThreeInit=false,lastSpawnTime=0;
function initThreeJS(){
  if(isThreeInit)return;isThreeInit=true;
  var cont=document.getElementById('canvas-container');
  scene=new THREE.Scene();scene.background=new THREE.Color(0x87c8f0);scene.fog=new THREE.Fog(0x87c8f0,28,60);
  camera=new THREE.PerspectiveCamera(45,innerWidth/innerHeight,0.1,1000);camera.position.set(0,12,10);camera.rotation.x=-Math.PI/3.2;
  renderer=new THREE.WebGLRenderer({antialias:true});renderer.setSize(innerWidth,innerHeight);renderer.setPixelRatio(Math.min(devicePixelRatio,2));cont.appendChild(renderer.domElement);
  scene.add(new THREE.DirectionalLight(0xfff5e6,1.3));scene.add(new THREE.AmbientLight(0xb8d4ff,0.55));
  var floor=new THREE.Mesh(new THREE.PlaneGeometry(120,120),new THREE.MeshLambertMaterial({color:0x3d9e5a}));floor.rotation.x=-Math.PI/2;scene.add(floor);
  playerNode=createHumanoidMesh();scene.add(playerNode);for(var i=0;i<3;i++)spawnMonster();
  var drag=false,lx=0,ly=0;
  window.addEventListener('pointerdown',function(e){if(menuOpen)return;if(!document.getElementById('field-screen').classList.contains('active'))return;drag=true;lx=e.clientX;ly=e.clientY;});
  window.addEventListener('pointermove',function(e){if(menuOpen||!drag)return;if(!document.getElementById('field-screen').classList.contains('active'))return;targetPlayerPos.x=Math.max(-12,Math.min(12,targetPlayerPos.x+(e.clientX-lx)*0.04));targetPlayerPos.z=Math.max(-18,Math.min(8,targetPlayerPos.z+(e.clientY-ly)*0.04));lx=e.clientX;ly=e.clientY;});
  window.addEventListener('pointerup',function(){drag=false;});
  var menuEl=document.getElementById('field-menu');
  if(menuEl){['pointerdown','pointermove','touchmove','wheel'].forEach(function(ev){menuEl.addEventListener(ev,function(e){e.stopPropagation();},{passive:false});});}
  function anim(t){
    requestAnimationFrame(anim);
    if(t-lastSpawnTime>5000){if(monsters.filter(function(m){return m.isActive;}).length<6)spawnMonster();lastSpawnTime=t;}
    if(!playerNode)return;
    playerNode.position.x+=(targetPlayerPos.x-playerNode.position.x)*0.15;playerNode.position.z+=(targetPlayerPos.z-playerNode.position.z)*0.15;
    camera.position.x=playerNode.position.x;camera.position.z=playerNode.position.z+10;
    var active=document.getElementById('field-screen').classList.contains('active')&&!menuOpen;
    monsters.forEach(function(m){
      if(!m.isActive||!active)return;
      m.mesh.rotation.y+=0.012;m.changeDirTimer--;
      if(m.changeDirTimer<=0){m.vx=(Math.random()-0.5)*0.08;m.vz=(Math.random()-0.5)*0.08;m.changeDirTimer=30+Math.random()*60;}
      m.mesh.position.x+=m.vx;m.mesh.position.z+=m.vz;
      if(Math.abs(m.mesh.position.x)>14)m.vx*=-1;if(m.mesh.position.z<-20||m.mesh.position.z>8)m.vz*=-1;
      var dx=playerNode.position.x-m.mesh.position.x,dz=playerNode.position.z-m.mesh.position.z;
      if(Math.sqrt(dx*dx+dz*dz)<=1){
        m.isActive=false;scene.remove(m.mesh);
        if(m.isBoss)showBossPreview(m);
        else{gameState.currentMonster=m;startBattle(false);}
      }
    });
    renderer.render(scene,camera);
  }
  anim(0);
}
function spawnMonster(){
  var isBoss=Math.random()<0.12,level,colorHex,hp,atk,name,weakness,condition=null,turnLimit=0;
  if(isBoss){level=5;colorHex=0x7c3aed;hp=900+Math.floor(Math.random()*200);atk=28+Math.floor(Math.random()*10);turnLimit=8+Math.floor(Math.random()*5);
    var bosses=[{name:'超高分子ラジカル塊',weakness:['Aromatic','Explosive'],condition:'Aromatic'},{name:'濃縮フリーラジカル核',weakness:['Acid','Oxidant'],condition:'Alcohol'},{name:'芳香族クラスター体',weakness:['Halogen','Reagent'],condition:'Ester'}];
    var b=bosses[Math.floor(Math.random()*bosses.length)];name='【BOSS】'+b.name;weakness=b.weakness;condition=b.condition;
  }else{level=1+Math.floor(Math.random()*3);colorHex=level===1?0x22c55e:(level===2?0xf97316:0xef4444);hp=450+level*30;atk=12+level*8;name=['アルキル変異体','環状高分子体','フリーラジカル塊'][level-1];
    var pool=['Aromatic','Alkenyl','Acid','Alcohol','Halogen','Oxidant','Phenol','Explosive'];weakness=[pool[Math.floor(Math.random()*pool.length)]];}
  var mesh=createMoleculeMesh(colorHex);mesh.position.set((Math.random()-0.5)*18,0.5,-Math.random()*12-2);scene.add(mesh);
  monsters.push({name:name,level:level,hp:hp,maxHP:hp,attackPower:atk,mesh:mesh,isActive:true,weakness:weakness,isBoss:isBoss,condition:condition,turnLimit:turnLimit,vx:0,vz:0,changeDirTimer:0});
}

var labScene,labCamera,labRenderer,enemyMesh;
function initLabThreeJS(){var cont=document.getElementById('lab-canvas-container');cont.innerHTML='';labScene=new THREE.Scene();labScene.background=new THREE.Color(0x071018);labCamera=new THREE.PerspectiveCamera(50,cont.clientWidth/Math.max(1,cont.clientHeight),0.1,100);labCamera.position.set(0,1.6,5.2);labCamera.lookAt(0,0.7,0);labRenderer=new THREE.WebGLRenderer({antialias:true});labRenderer.setSize(cont.clientWidth,cont.clientHeight);cont.appendChild(labRenderer.domElement);labScene.add(new THREE.DirectionalLight(0x67e8f9,1.5));labScene.add(new THREE.AmbientLight(0xffffff,0.45));var col=(gameState.currentMonster&&gameState.currentMonster.isBoss)?0x7c3aed:0x22d3ee;enemyMesh=createMoleculeMesh(col);enemyMesh.scale.set(1.4,1.4,1.4);enemyMesh.position.set(0,0.9,0);labScene.add(enemyMesh);(function anim(){requestAnimationFrame(anim);if(enemyMesh){enemyMesh.rotation.y+=0.014;enemyMesh.position.y=0.9+Math.sin(Date.now()*0.002)*0.08;}if(labRenderer&&labScene&&labCamera)labRenderer.render(labScene,labCamera);})();}

function startBattle(practice){isPractice=!!practice;returnToMenu=false;fromBossPreview=false;document.querySelectorAll('.screen').forEach(function(el){el.classList.remove('active');});document.getElementById('battle-screen').classList.add('active');if(!isPractice)initLabThreeJS();else document.getElementById('lab-canvas-container').innerHTML='<div style="display:flex;align-items:center;justify-content:center;height:100%;color:#67e8f9">練習</div>';setupBattle();}
function startPractice(){gameState.currentMonster={name:'練習ダミー',level:1,hp:9999,maxHP:9999,attackPower:0,weakness:[],isBoss:false,condition:null,turnLimit:0};startBattle(true);}
function setupBattle(){
  isBattleOver=false;isProcessing=false;botulinumActive=false;gameState.nextDamageBonus=1.0;pendingIntermediate=null;battleHistory=[];battleTurnCount=0;comboCount=0;
  battleUsedCatalyst=false;battleBigSpend=false;battleAttrsUsed={};battleOriginCount=0;
  bossTurnLimit=(gameState.currentMonster&&gameState.currentMonster.turnLimit)||0;
  if(!isPractice)gameState.playerHP=gameState.playerMaxHP;
  document.getElementById('next-bonus').style.display='none';document.getElementById('dot-status').style.display='none';document.getElementById('choice-box').style.display='none';
  document.getElementById('combo-status').innerText='🔗 連鎖コンボ: 0';
  var tl=document.getElementById('turn-limit');if(bossTurnLimit>0){tl.style.display='block';tl.innerText='⏱ 残り'+bossTurnLimit;}else tl.style.display='none';
  bDeck=gameState.currentDeck.map(function(c){return Object.assign({},c);}).sort(function(){return Math.random()-0.5;});
  bHand=[];bSelected=[];monsterHP=gameState.currentMonster.hp;
  document.getElementById('monster-name').innerText=gameState.currentMonster.name;
  document.getElementById('monster-level').innerText=gameState.currentMonster.level;
  document.getElementById('monster-maxhp').innerText=gameState.currentMonster.maxHP;
  document.getElementById('monster-hp').innerText=monsterHP;
  document.getElementById('battle-player-hp').innerText=gameState.playerHP;
  document.getElementById('monster-exp').innerText='経験+'+enemyExpReward(gameState.currentMonster);
  var weak=gameState.currentMonster.weakness||[];
  document.getElementById('monster-weak').innerText=weak.length?'弱点: '+weak.map(function(w){return ATTR_JP[w]||w;}).join(','):'';
  document.getElementById('monster-cond').innerText=gameState.currentMonster.condition?'条件: '+(ATTR_JP[gameState.currentMonster.condition]||gameState.currentMonster.condition):'';
  for(var i=0;i<5;i++)drawCard();startPlayerTurn(true);
}
function pushHistory(msg){battleHistory.push(msg);if(battleHistory.length>50)battleHistory.shift();}
function finalizeReplay(){gameState.lastReplay=battleHistory.slice();}
function startPlayerTurn(first){if(isBattleOver)return;isPlayerTurn=true;isProcessing=false;if(!first)battleTurnCount++;if(bossTurnLimit>0&&!isPractice){var left=bossTurnLimit-battleTurnCount;document.getElementById('turn-limit').innerText='⏱ 残り'+Math.max(0,left);if(left<=0){isBattleOver=true;document.getElementById('battle-log').innerText='ターン切れ';finalizeReplay();setTimeout(function(){gameState.playerHP=gameState.playerMaxHP;switchState('field');},1600);return;}}if(botulinumActive&&monsterHP>0&&!isPractice){monsterHP-=200;document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);if(monsterHP<=0){winBattle('毒素');return;}}if(!first)drawCard();document.getElementById('battle-log').innerText=first?(isPractice?'練習':'カード選択'):'あなたのターン';updateBattleUI();}
function drawCard(){if(bHand.length<7&&bDeck.length>0)bHand.push(bDeck.shift());}
function updateBattleUI(){
  document.getElementById('battle-deck-count').innerText=bDeck.length;document.getElementById('hand-count').innerText=bHand.length;
  document.getElementById('combo-status').innerText='🔗 連鎖コンボ: '+comboCount;
  var cont=document.getElementById('hand-cards');cont.innerHTML='';
  bHand.forEach(function(card){
    var sel=bSelected.some(function(c){return c.id===card.id;});
    var div=document.createElement('div');div.className='card'+(sel?' selected':'');var timer=null;
    div.addEventListener('pointerdown',function(e){e.preventDefault();timer=setTimeout(function(){showLongPress(card);timer=null;},450);});
    div.addEventListener('pointerup',function(){if(timer){clearTimeout(timer);timer=null;toggleSelectCard(card);}});
    div.addEventListener('pointerleave',function(){if(timer){clearTimeout(timer);timer=null;}});
    div.innerHTML='<div class="card-rarity rarity-'+card.rarity+'">'+card.rarity+'</div><div style="font-size:11px">'+card.name+'</div><div style="font-size:9px;color:#64748b">'+(card.formula||'')+'</div><div class="card-attr">'+card.attribute+(isIntermediateCard(card)?' ·中間':'')+'</div>'+cardPowerText(card);
    cont.appendChild(div);
  });
  var can=isPlayerTurn&&!isProcessing&&!isBattleOver;
  document.getElementById('attack-btn').disabled=!(can&&bSelected.length>0);
  document.getElementById('skip-btn').disabled=!can;document.getElementById('flee-btn').disabled=!can;
}
function showLongPress(card){document.getElementById('lp-title').innerText=card.name;document.getElementById('lp-body').innerText=getLongPressText(card);document.getElementById('longpress-popup').style.display='block';}
function closeLongPress(){document.getElementById('longpress-popup').style.display='none';}
function toggleSelectCard(card){if(!isPlayerTurn||isBattleOver||isProcessing)return;var idx=bSelected.findIndex(function(c){return c.id===card.id;});if(idx>=0)bSelected.splice(idx,1);else bSelected.push(card);updateBattleUI();}
function skipTurn(){if(!isPlayerTurn||isBattleOver||isProcessing)return;isProcessing=true;bSelected=[];document.getElementById('battle-log').innerText='ターン終了';updateBattleUI();setTimeout(endPlayerTurn,700);}
function fleeBattle(){if(!isPlayerTurn||isBattleOver||isProcessing)return;isBattleOver=true;isProcessing=true;document.getElementById('battle-log').innerText=isPractice?'練習終了':'脱出';finalizeReplay();setTimeout(function(){switchState('field');},1000);}
function winBattle(msg){
  isBattleOver=true;finalizeReplay();
  if(isPractice){document.getElementById('battle-log').innerText='練習終了';setTimeout(function(){switchState('field');},1100);return;}
  gameState.kills++;
  var m=gameState.currentMonster;
  if(m&&(m.isBoss||m.level>=3))gameState.flags.hardKills=(gameState.flags.hardKills||0)+1;
  if(m&&m.isBoss){gameState.flags.boss=true;gameState.flags.bossKills=(gameState.flags.bossKills||0)+1;if(!battleUsedCatalyst)gameState.flags.noCatBoss=true;if(!battleBigSpend)gameState.flags.saveBoss=true;}
  if(Object.keys(battleAttrsUsed).length===1)gameState.flags.monoWin=true;
  if(battleOriginCount>=3)gameState.flags.originWin=true;
  if(comboCount>=8)gameState.flags.combo8=true;if(comboCount>=5)gameState.flags.combo5=true;if(comboCount>=3)gameState.flags.combo3=true;
  var px=enemyExpReward(m);addPlayerExp(px);addLabExp(m&&m.isBoss?15:5+comboCount);
  checkRankUp();checkAchievements();
  var rank=getRank(),labBonus=1+(gameState.labLevel>=9?0.15:0)+(gameState.labLevel>=4?0.1:0)+(gameState.labLevel>=2?0.05:0);
  var reward=Math.floor((55+(m?m.level:1)*28)*rank.reagentBonus*labBonus);
  if(m&&m.isBoss)reward+=100;if(comboCount>=2&&gameState.labLevel>=5)reward+=10*comboCount;
  gameState.reagents+=reward;
  document.getElementById('battle-log').innerText=msg+'\n試薬 +'+reward+'\n経験 +'+px;
  setTimeout(function(){switchState('field');},1600);
}

function has(n,name){return n.indexOf(name)>=0;}
function executePlayerAttack(){
  if(isBattleOver||!isPlayerTurn||isProcessing||!bSelected.length)return;
  isProcessing=true;document.getElementById('attack-btn').disabled=true;document.getElementById('skip-btn').disabled=true;document.getElementById('flee-btn').disabled=true;
  var baseDamage=0,baseHeal=0,logMessage='',product=null,appliedEffect=null,isReaction=false,recipeId=null;
  var n=bSelected.map(function(c){return baseName(c.name);}),unique=[];n.forEach(function(x){if(unique.indexOf(x)<0)unique.push(x);});
  var hasCat=has(n,'濃硫酸')||has(n,'重合触媒(Ziegler)')||has(n,'塩化アルミニウム')||has(n,'鉄');
  if(hasCat)battleUsedCatalyst=true;
  bSelected.forEach(function(c){battleAttrsUsed[c.attribute]=1;if(c.rarity==='ORIGIN'||c.origin)battleOriginCount++;});
  var usedMidInThis=bSelected.some(function(c){return isIntermediateCard(c);});
  var catMul=hasCat?2.0:1.5,bossCond=gameState.currentMonster&&gameState.currentMonster.condition;
  function dmgLog(t,d){return t+'\n相手に '+(d===Infinity?'∞':d)+' ダメージ！';}

  if(has(n,'アニリン')&&has(n,'無水酢酸')){product={name:'アセトアニリド',formula:'C6H5NHCOCH3',attackPower:60,healPower:0,attribute:'Aromatic',rarity:'SR'};baseDamage=Math.floor(80*catMul);logMessage=dmgLog('アセチル化',baseDamage);markFlag('acetyl');isReaction=true;recipeId='acetyl_an';}
  else if(has(n,'サリチル酸')&&has(n,'無水酢酸')){product={name:'アセチルサリチル酸',formula:'C9H8O4',attackPower:120,healPower:0,attribute:'Ester',rarity:'SSR'};baseDamage=Math.floor(120*catMul);logMessage=dmgLog('アセチル化',baseDamage);markFlag('acetyl');isReaction=true;recipeId='acetyl_sal';}
  else if(has(n,'エタノール')&&has(n,'濃硫酸')){baseDamage=Math.floor(100*catMul);logMessage=dmgLog('脱水',baseDamage);markFlag('dehyd');isReaction=true;recipeId='dehyd';}
  else if(has(n,'1-プロパノール')&&has(n,'濃硫酸')){baseDamage=Math.floor(105*catMul);logMessage=dmgLog('脱水',baseDamage);markFlag('dehyd');isReaction=true;recipeId='dehyd';}
  else if(has(n,'ベンゼン')&&has(n,'ニトロ基')){product={name:'ニトロベンゼン',formula:'C6H5NO2',attackPower:70,healPower:0,attribute:'Aromatic',rarity:'SR'};baseDamage=Math.floor(70*catMul);logMessage=dmgLog('ニトロベンゼン',baseDamage);markFlag('nitro');isReaction=true;recipeId='nitro_grp';}
  else if(has(n,'ニトロベンゼン')&&(has(n,'還元剤')||has(n,'水素化ホウ素ナトリウム'))){product={name:'アニリン',formula:'C6H5NH2',attackPower:65,healPower:0,attribute:'Aromatic',rarity:'SR'};baseDamage=Math.floor(65*catMul);logMessage=dmgLog('還元',baseDamage);isReaction=true;recipeId='reduce_nb';}
  else if(has(n,'アニリン')&&has(n,'ジアゾ化剤')){product={name:'アゾベンゼン',formula:'C6H5N=NC6H5',attackPower:110,healPower:0,attribute:'Aromatic',rarity:'SSR'};baseDamage=Math.floor(110*catMul);logMessage=dmgLog('アゾ',baseDamage);isReaction=true;recipeId='azo';}
  else if(has(n,'酢酸')&&has(n,'エタノール')){product={name:'酢酸エチル',formula:'CH3COOC2H5',attackPower:Math.floor(55*catMul),healPower:0,attribute:'Ester',rarity:'R'};baseDamage=Math.floor(55*catMul);logMessage=dmgLog('エステル化',baseDamage);markFlag('ester');isReaction=true;recipeId='ester';}
  else if(bSelected.length===1&&baseName(bSelected[0].name)==='ボツリヌス毒素'){botulinumActive=true;document.getElementById('dot-status').style.display='block';logMessage='毒素';baseDamage=0;}
  else if(bSelected.length===1&&baseName(bSelected[0].name)==='フッ化水素酸'){gameState.flags.hfUsed=true;if(Math.random()<0.1){isBattleOver=true;document.getElementById('battle-log').innerText='HF自爆 試薬-25';gameState.reagents=Math.max(0,gameState.reagents-25);finalizeReplay();bHand=bHand.filter(function(c){return !bSelected.some(function(s){return s.id===c.id;});});bSelected=[];updateBattleUI();setTimeout(function(){gameState.playerHP=gameState.playerMaxHP;switchState('field');},1800);return;}baseDamage=Infinity;logMessage=dmgLog('HF',Infinity);checkAchievements();}
  else if(bSelected.length===1&&(baseName(bSelected[0].name)==='トリニトロトルエン'||baseName(bSelected[0].name)==='ピクリン酸')){baseDamage=bSelected[0].attackPower||180;logMessage=dmgLog(bSelected[0].name,baseDamage);}
  else if(has(n,'水酸化ナトリウム')&&(has(n,'トリパルミチン')||has(n,'トリステアリン')||has(n,'トリオレイン'))){baseDamage=Math.floor(230*catMul);appliedEffect='sapon';logMessage=dmgLog('油脂けん化',baseDamage);markFlag('sapon');markFlag('fat');isReaction=true;recipeId='sapon_fat';}
  else if(has(n,'水酸化ナトリウム')&&(has(n,'酢酸')||has(n,'酢酸エチル')||has(n,'オレイン酸'))){baseDamage=Math.floor(210*catMul);appliedEffect='sapon';logMessage=dmgLog('けん化',baseDamage);markFlag('sapon');isReaction=true;recipeId='sapon';}
  else if(has(n,'ベンゼン')&&has(n,'濃硝酸')){baseDamage=Math.floor(130*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;recipeId='nitro_bz';}
  else if(has(n,'トルエン')&&has(n,'濃硝酸')){baseDamage=Math.floor(220*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;recipeId='nitro_tol';}
  else if(has(n,'フェノール')&&has(n,'濃硝酸')){baseDamage=Math.floor(150*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;recipeId='nitro_ph';}
  else if(has(n,'ベンゼン')&&has(n,'濃硫酸')){baseDamage=Math.floor(150*catMul);logMessage=dmgLog('スルホン化',baseDamage);isReaction=true;recipeId='sulf';}
  else if(has(n,'ナフタレン')&&has(n,'濃硫酸')){baseDamage=Math.floor(160*catMul);logMessage=dmgLog('スルホン化',baseDamage);isReaction=true;recipeId='sulf';}
  else if(has(n,'ベンゼン')&&(has(n,'塩素')||has(n,'臭素'))&&(has(n,'鉄')||has(n,'塩化アルミニウム')||hasCat)){baseDamage=Math.floor(140*catMul);logMessage=dmgLog('ハロゲン化',baseDamage);isReaction=true;recipeId='halo';}
  else if(has(n,'エチレン')&&(has(n,'臭素')||has(n,'塩素'))){baseDamage=Math.floor(140*catMul);logMessage=dmgLog('付加',baseDamage);isReaction=true;recipeId='add_et';}
  else if(has(n,'アセチレン')&&has(n,'臭素')){baseDamage=Math.floor(160*catMul);logMessage=dmgLog('付加',baseDamage);isReaction=true;recipeId='add_et';}
  else if((has(n,'シス-2-ブテン')||has(n,'トランス-2-ブテン'))&&has(n,'臭素')){baseDamage=Math.floor(130*catMul);logMessage=dmgLog('付加',baseDamage);isReaction=true;recipeId='add_et';}
  else if(has(n,'エチレン')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(300*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;recipeId='poly';}
  else if(has(n,'スチレン')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(250*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;recipeId='poly';}
  else if(has(n,'プロピレン')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(260*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;recipeId='poly';}
  else if(has(n,'ビニル基')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(220*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;recipeId='poly';}
  else if((has(n,'エタノール')||has(n,'アセトアルデヒド')||has(n,'メタノール'))&&(has(n,'過マンガン酸カリウム')||has(n,'二クロム酸カリウム'))){baseDamage=Math.floor(170*catMul);appliedEffect='oxid';logMessage=dmgLog('酸化',baseDamage);markFlag('oxid');isReaction=true;recipeId='oxid';}
  else if(has(n,'2-プロパノール')&&(has(n,'過マンガン酸カリウム')||has(n,'二クロム酸カリウム'))){baseDamage=Math.floor(160*catMul);logMessage=dmgLog('酸化',baseDamage);markFlag('oxid');isReaction=true;recipeId='oxid';}
  else if(has(n,'トルエン')&&has(n,'過マンガン酸カリウム')){baseDamage=Math.floor(190*catMul);logMessage=dmgLog('側鎖酸化',baseDamage);markFlag('oxid');isReaction=true;recipeId='side_ox';}
  else if((has(n,'エタノール')||has(n,'メタノール')||has(n,'1-プロパノール'))&&has(n,'金属ナトリウム')){baseDamage=Math.floor(120*catMul);logMessage=dmgLog('アルコキシド',baseDamage);isReaction=true;recipeId='na_alc';}
  else if(has(n,'フェノール')&&has(n,'金属ナトリウム')){baseDamage=Math.floor(140*catMul);logMessage=dmgLog('フェノキシド',baseDamage);isReaction=true;recipeId='na_ph';}
  else if(has(n,'ナフタレン')&&has(n,'濃硝酸')){baseDamage=Math.floor(170*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;recipeId='nitro_bz';}
  else if(has(n,'アントラセン')&&has(n,'濃硝酸')){baseDamage=Math.floor(200*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;recipeId='nitro_bz';}
  else if(has(n,'メチル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(50*catMul);logMessage=dmgLog('メタノール生成',baseDamage);isReaction=true;recipeId='fg_oh';}
  else if(has(n,'エチル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(60*catMul);logMessage=dmgLog('エタノール生成',baseDamage);isReaction=true;recipeId='fg_oh';}
  else if(has(n,'フェニル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(90*catMul);logMessage=dmgLog('フェノール生成',baseDamage);isReaction=true;recipeId='fg_oh';}
  else if(has(n,'フェニル基')&&has(n,'ニトロ基')){baseDamage=Math.floor(110*catMul);logMessage=dmgLog('ニトロベンゼン生成',baseDamage);isReaction=true;recipeId='fg_no2';}
  else if(has(n,'フェニル基')&&has(n,'カルボキシ基')){baseDamage=Math.floor(100*catMul);logMessage=dmgLog('安息香酸生成',baseDamage);isReaction=true;recipeId='fg_oh';}
  else if(unique.length===1){
    var s=bSelected[0],cnt=bSelected.length;
    if(baseName(s.name)==='ボツリヌス毒素'){botulinumActive=true;document.getElementById('dot-status').style.display='block';logMessage='毒素';baseDamage=0;}
    else if(baseName(s.name)==='フッ化水素酸'){baseDamage=Infinity;logMessage=dmgLog('HF',Infinity);}
    else{baseDamage=s.attackPower===Infinity?Infinity:(s.attackPower||0)*cnt;baseHeal=(s.healPower||0)*cnt;if(baseHeal>0)gameState.flags.healed=true;
      if(baseDamage>0&&baseHeal>0)logMessage=s.name+'×'+cnt+'\n'+fmt(baseDamage)+'ダメージ\n'+baseHeal+'回復';
      else if(baseHeal>0)logMessage=s.name+'×'+cnt+'\n'+baseHeal+'回復';
      else logMessage=s.name+'×'+cnt+' 投擲\n相手に '+fmt(baseDamage)+' ダメージ！';}
  }
  else if(bSelected.length===1){var s1=bSelected[0];baseDamage=s1.attackPower||0;baseHeal=s1.healPower||0;if(baseHeal>0)gameState.flags.healed=true;if(baseDamage>0&&baseHeal>0)logMessage=s1.name+'\n'+fmt(baseDamage)+'ダメージ\n'+baseHeal+'回復';else if(baseHeal>0)logMessage=s1.name+'\n'+baseHeal+'回復';else logMessage=s1.name+' を投擲！\n相手に '+fmt(baseDamage)+' ダメージ！';}
  else{var healSum=bSelected.reduce(function(a,c){return a+(c.healPower||0);},0);var atkSum=bSelected.reduce(function(a,c){return a+(c.attackPower===Infinity?0:(c.attackPower||0));},0);if(healSum>0&&atkSum===0){baseHeal=healSum;gameState.flags.healed=true;logMessage='複合回復 '+healSum+'回復';}else{logMessage='不活性\n'+getReactionHint(bSelected);}}

  if(isReaction){
    if(usedMidInThis){comboCount++;gameState.flags.midReact=(gameState.flags.midReact||0)+1;logMessage+='\n🔗 連鎖コンボ×'+comboCount+'（中間体を使用）';}
    else logMessage+='\n（中間体未使用のため連鎖コンボは据え置き: '+comboCount+'）';
    if(recipeId)unlockRecipe(recipeId);
    var comboMul=1+Math.min(comboCount,8)*0.05;
    if(baseDamage!==Infinity&&baseDamage>0&&comboCount>0)baseDamage=Math.floor(baseDamage*comboMul);
  }

  if(bossCond&&baseDamage>0&&baseDamage!==Infinity&&!isPractice){var attrs=bSelected.map(function(c){return c.attribute;});var ok=attrs.indexOf(bossCond)>=0||(product&&product.attribute===bossCond);if(bossCond==='Ester'&&has(n,'酢酸')&&has(n,'エタノール'))ok=true;if(bossCond==='Alcohol'&&(has(n,'エタノール')||has(n,'メタノール')||has(n,'ヒドロキシ基')))ok=true;if(!ok){baseDamage=0;logMessage+='\nボス条件未達';}}
  var weakMul=1;if(gameState.currentMonster&&gameState.currentMonster.weakness){var attrs2=bSelected.map(function(c){return c.attribute;});if(attrs2.some(function(a){return gameState.currentMonster.weakness.indexOf(a)>=0;}))weakMul=1.5;}
  var finalD=baseDamage;if(finalD!==Infinity&&finalD>0)finalD=Math.floor(finalD*gameState.nextDamageBonus*weakMul);
  if(appliedEffect==='oxid'){gameState.nextDamageBonus=1.3;document.getElementById('next-bonus').style.display='block';document.getElementById('next-bonus').innerText='次ターン+30%';}
  else if(appliedEffect==='sapon'){gameState.nextDamageBonus=1.2;document.getElementById('next-bonus').style.display='block';document.getElementById('next-bonus').innerText='次ターン+20%';}
  else if(baseDamage>0||baseHeal>0){gameState.nextDamageBonus=1.0;document.getElementById('next-bonus').style.display='none';}

  bHand=bHand.filter(function(c){return !bSelected.some(function(s){return s.id===c.id;});});bSelected=[];
  if(product){pendingIntermediate={card:Object.assign({},product,{id:uid(),_fromMid:true}),damage:finalD,heal:baseHeal,msg:logMessage,weak:weakMul>1};document.getElementById('choice-title').innerText=product.name+' 生成';document.getElementById('choice-desc').innerText=product.attackPower+'ダメージ（手札に加えれば連鎖コンボに使える）';document.getElementById('choice-box').style.display='flex';updateBattleUI();return;}
  applyEffectAndEndTurn(finalD,baseHeal,logMessage,weakMul>1);
}
function chooseAttack(){document.getElementById('choice-box').style.display='none';if(!pendingIntermediate)return;var p=pendingIntermediate;applyEffectAndEndTurn(p.damage,p.heal,p.msg+(p.weak?'\n弱点！':''),p.weak);pendingIntermediate=null;}
function chooseAddToHand(){document.getElementById('choice-box').style.display='none';if(!pendingIntermediate)return;if(bHand.length<7)bHand.push(pendingIntermediate.card);gameState.collection.push(Object.assign({},pendingIntermediate.card));document.getElementById('battle-log').innerText=pendingIntermediate.card.name+' を手札に（中間体）';pendingIntermediate=null;isProcessing=false;updateBattleUI();setTimeout(endPlayerTurn,1100);}
function applyEffectAndEndTurn(damage,heal,message,isWeak){if(isBattleOver)return;if(damage===Infinity||damage>=400){if(gameState.reagents>=25){gameState.reagents-=25;battleBigSpend=true;message+='\n試薬25消費';}else if(damage!==Infinity){damage=Math.floor(damage*0.5);message+='\n半減';}}if(isWeak)message+='\n弱点！';if(damage===Infinity)monsterHP=0;else if(damage>0)monsterHP-=damage;if(heal>0){gameState.playerHP=Math.min(gameState.playerMaxHP,gameState.playerHP+heal);document.getElementById('battle-player-hp').innerText=gameState.playerHP;}document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);document.getElementById('battle-log').innerText=message;pushHistory(message);if(monsterHP<=0)winBattle(isPractice?'練習クリア':'敵を分解！');else setTimeout(endPlayerTurn,1400);}
function endPlayerTurn(){if(isBattleOver)return;if(isPractice){startPlayerTurn(false);return;}isPlayerTurn=false;isProcessing=true;document.getElementById('battle-log').innerText='敵の攻撃…';updateBattleUI();setTimeout(function(){if(isBattleOver)return;if(monsterHP>0){var atk=gameState.currentMonster.attackPower||15;if(bossTurnLimit>0&&battleTurnCount>=bossTurnLimit-2)atk=Math.floor(atk*1.5);gameState.playerHP-=atk;document.getElementById('battle-player-hp').innerText=Math.max(0,gameState.playerHP);document.getElementById('battle-log').innerText='敵の攻撃\nあなたに '+atk+' ダメージ！';if(gameState.playerHP<=0){isBattleOver=true;gameState.playerHP=0;gameState.reagents=Math.max(0,gameState.reagents-25);document.getElementById('battle-log').innerText='敗北 試薬-25';finalizeReplay();setTimeout(function(){gameState.playerHP=gameState.playerMaxHP;switchState('field');},1400);return;}setTimeout(function(){if(!isBattleOver)startPlayerTurn(false);},1100);}else if(!isBattleOver)startPlayerTurn(false);},800);}

function sortDeck(mode){var names=[],seen={};gameState.collection.forEach(function(c){if(!seen[c.name]){seen[c.name]=1;names.push(c.name);}});function rep(name){return gameState.collection.find(function(c){return c.name===name;})||ALL_CARDS.find(function(c){return c.name===baseName(name);});}names.sort(function(a,b){var ca=rep(a),cb=rep(b);if(!ca||!cb)return 0;if(mode==='name')return a.localeCompare(b,'ja');if(mode==='rarity'){var d=(RARITY_ORDER[ca.rarity]||9)-(RARITY_ORDER[cb.rarity]||9);return d||a.localeCompare(b,'ja');}if(mode==='power'){var d2=powerValue(cb)-powerValue(ca);return d2||a.localeCompare(b,'ja');}return a.localeCompare(b,'ja');});gameState.deckListOrder=names.slice();var rebuilt=[];names.forEach(function(name){gameState.currentDeck.filter(function(c){return c.name===name;}).forEach(function(c){rebuilt.push(c);});});gameState.currentDeck=rebuilt;renderDeckEdit();}
function renderDeckEdit(){
  document.getElementById('deck-count').innerText=gameState.currentDeck.length;
  document.getElementById('deck-reaction-list').innerText=FULL_REACTION_TEXT;
  for(var i=0;i<3;i++){var inp=document.getElementById('preset-name-'+i);if(inp&&gameState.deckSlots[i])inp.value=gameState.deckSlots[i].name||'';}
  document.getElementById('preset-labels').innerText=[0,1,2].map(function(i){var s=gameState.deckSlots[i];return(s&&s.cards&&s.cards.length)?('S'+(i+1)+':'+(s.name||'無題')+'('+s.cards.length+')'):('S'+(i+1)+':空');}).join(' / ');
  var syn=calcSynthRate();document.getElementById('synth-rate-text').innerText=syn.rate+'% 回復'+syn.healCount;document.getElementById('synth-rate-bar').style.width=syn.rate+'%';document.getElementById('synth-hint').innerText=syn.missing.length?'不足: '+syn.missing.join(' / '):'';
  var allNames=[],seen={};gameState.collection.forEach(function(c){if(!seen[c.name]){seen[c.name]=1;allNames.push(c.name);}});
  var ordered;if(gameState.deckListOrder&&gameState.deckListOrder.length){ordered=gameState.deckListOrder.filter(function(n){return seen[n];});allNames.filter(function(n){return ordered.indexOf(n)<0;}).sort(function(a,b){return a.localeCompare(b,'ja');}).forEach(function(n){ordered.push(n);});}else ordered=allNames.sort(function(a,b){return a.localeCompare(b,'ja');});
  if(deckAttrFilter!=='all')ordered=ordered.filter(function(name){var c=gameState.collection.find(function(x){return x.name===name;});return c&&c.attribute===deckAttrFilter;});
  var list=document.getElementById('deck-list');list.innerHTML='';
  ordered.forEach(function(name){
    var owned=gameState.collection.filter(function(c){return c.name===name;}).length;
    var inD=gameState.currentDeck.filter(function(c){return c.name===name;}).length;
    var card=gameState.collection.find(function(c){return c.name===name;});if(!card)return;
    var val;if(baseName(name)==='ボツリヌス毒素')val='毎ターン200ダメージ';else if((card.attackPower||0)>0&&(card.healPower||0)>0)val=fmt(card.attackPower)+'ダメージ/'+card.healPower+'回復';else if(card.healPower>0)val=card.healPower+'回復';else val=fmt(card.attackPower)+'ダメージ';
    var div=document.createElement('div');div.className='deck-item'+(inD>0?' in-deck':'');
    var left=document.createElement('div');
    left.innerHTML='<span class="card-rarity rarity-'+card.rarity+'">'+card.rarity+'</span> <span style="color:'+(inD>0?'#4ade80':'#e2e8f0')+'">'+name+' ['+inD+'/'+owned+']</span><div style="font-size:9px;color:#94a3b8">'+val+' · '+(ATTR_JP[card.attribute]||card.attribute)+'</div>';
    var right=document.createElement('div');right.style.display='flex';right.style.alignItems='center';right.style.gap='2px';
    if(card.rarity==='ORIGIN'||card.origin){
      var rn=document.createElement('button');rn.type='button';rn.className='action-btn';rn.title='改名(25試薬)';rn.innerText='✏️';rn.onclick=function(){renameOriginCard(name);};right.appendChild(rn);
    }
    if(inD>0){var rm=document.createElement('button');rm.type='button';rm.className='action-btn';rm.style.color='#f87171';rm.innerText='➖';rm.onclick=function(){removeFromDeck(name);};right.appendChild(rm);}
    var add=document.createElement('button');add.type='button';add.className='action-btn';add.style.color=(inD<owned&&gameState.currentDeck.length<50)?'#38bdf8':'#475569';add.innerText='➕';add.disabled=!(inD<owned&&gameState.currentDeck.length<50);add.onclick=function(){addToDeck(name);};right.appendChild(add);
    div.appendChild(left);div.appendChild(right);list.appendChild(div);
  });
  var btn=document.getElementById('deck-done-btn');btn.disabled=gameState.currentDeck.length<20;btn.style.opacity=gameState.currentDeck.length>=20?'1':'0.45';
  if(fromBossPreview)btn.innerText='ボスへ戻る';else btn.innerText='完了';
}
function addToDeck(name){var owned=gameState.collection.filter(function(c){return c.name===name;}).length;var inD=gameState.currentDeck.filter(function(c){return c.name===name;}).length;var card=gameState.collection.find(function(c){return c.name===name;});if(card&&gameState.currentDeck.length<50&&inD<owned){gameState.currentDeck.push(Object.assign({},card,{id:uid()}));renderDeckEdit();}}
function removeFromDeck(name){var i=gameState.currentDeck.findIndex(function(c){return c.name===name;});if(i>=0){gameState.currentDeck.splice(i,1);renderDeckEdit();}}

initDaily();
</script>
</body>
</html>
