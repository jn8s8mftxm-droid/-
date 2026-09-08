<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>有機化学バトルフィールド</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0;user-select:none;-webkit-tap-highlight-color:transparent;
font-family:"Hiragino Sans","Noto Sans JP",-apple-system,sans-serif;font-weight:400}
body,html{width:100%;height:100%;overflow:hidden;background:#05080f;color:#e8eef7}
.screen{display:none;width:100%;height:100%;position:absolute;top:0;left:0}
.active{display:flex;flex-direction:column}
.glass-btn{
  background:linear-gradient(145deg,rgba(56,189,248,.28),rgba(99,102,241,.35));
  border:1px solid rgba(148,163,184,.35);color:#f1f5f9;
  padding:10px 16px;font-size:13px;border-radius:10px;cursor:pointer;
  min-width:88px;text-align:center;
}
.glass-btn:active{transform:scale(.97)}
.glass-btn:disabled{opacity:.4;cursor:not-allowed}
.glass-btn.primary{background:linear-gradient(145deg,#0ea5e9,#6366f1)}
.glass-btn.danger{background:linear-gradient(145deg,#ef4444,#b91c1c)}
.glass-btn.success{background:linear-gradient(145deg,#10b981,#059669)}
.glass-btn.warn{background:linear-gradient(145deg,#f59e0b,#d97706)}
.glass-btn.pink{background:linear-gradient(145deg,#ec4899,#a855f7)}
.glass-btn.slate{background:linear-gradient(145deg,#475569,#334155)}
.glass-btn.orange{background:linear-gradient(145deg,#ea580c,#ef4444)}
.glass-btn.wide{width:100%;min-width:0}
.mini-btn{padding:9px 12px;font-size:12px;min-width:72px}

#deck-select-screen{
  background:radial-gradient(ellipse at 30% 20%,#1e3a5f,#0b1220 50%,#05080f);
  padding:36px 20px;align-items:center;gap:16px;text-align:center;
}
#deck-select-screen h2{
  font-size:22px;background:linear-gradient(90deg,#7dd3fc,#a5b4fc);
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
}
.select-card{
  border-radius:16px;padding:16px;margin-bottom:12px;text-align:left;cursor:pointer;
  width:100%;max-width:400px;border:1px solid rgba(255,255,255,.12);color:#fff;
}
.select-card.purple{background:linear-gradient(135deg,#5b21b6,#1d4ed8)}
.select-card.red{background:linear-gradient(135deg,#c2410c,#b91c1c)}
.select-card.green{background:linear-gradient(135deg,#047857,#0f766e)}
.badge{display:inline-block;background:rgba(255,255,255,.18);font-size:10px;padding:3px 8px;border-radius:999px}

#field-screen{position:relative}
#canvas-container{width:100%;height:100%}
.field-ui{
  position:absolute;top:0;left:0;width:100%;padding:24px 10px 0;
  display:flex;justify-content:space-between;align-items:flex-start;
  pointer-events:none;z-index:5;gap:8px;
}
.field-ui *{pointer-events:auto}
.status-box{
  background:rgba(8,12,22,.78);padding:12px 14px;border-radius:14px;font-size:13px;
  border:1px solid rgba(148,163,184,.25);min-width:140px;
}
/* 横一列 */
.field-btns{
  display:flex;flex-direction:row;flex-wrap:wrap;gap:6px;
  justify-content:flex-end;max-width:55%;
}
.field-btns .glass-btn{min-width:70px}

#field-menu{
  display:none;position:absolute;top:0;left:0;width:100%;height:100%;
  background:rgba(0,0,0,.55);z-index:30;align-items:center;justify-content:center;
}
#field-menu .menu-panel{
  background:rgba(15,23,42,.97);border:1px solid rgba(148,163,184,.4);
  border-radius:16px;padding:18px 16px;width:90%;max-width:340px;
  display:flex;flex-direction:column;gap:8px;max-height:80vh;overflow-y:auto;
}
.menu-label{font-size:11px;color:#94a3b8;margin-top:4px}

#battle-screen{
  background:radial-gradient(ellipse at 50% 0%,#1e293b,#0f172a 40%,#020617);
  padding:12px;justify-content:space-between;
}
.battle-header{display:flex;justify-content:space-between;margin-bottom:6px}
#lab-canvas-container{
  width:100%;height:140px;border-radius:14px;overflow:hidden;
  border:1px solid rgba(56,189,248,.35);background:#071018;
}
.battle-log-box{
  background:rgba(15,23,42,.9);border:1px solid rgba(71,85,105,.6);border-radius:12px;
  padding:10px;min-height:52px;font-size:12px;text-align:center;
  display:flex;align-items:center;justify-content:center;white-space:pre-line;margin:6px 0;
}
.quiz-box{
  background:rgba(88,28,135,.45);border:1px solid rgba(192,132,252,.5);border-radius:12px;
  padding:12px;text-align:center;display:flex;flex-direction:column;gap:8px;
}
.quiz-options{display:grid;grid-template-columns:1fr 1fr;gap:6px}
.quiz-btn{
  background:linear-gradient(145deg,#2563eb,#4338ca);border:none;color:#fff;
  padding:10px;border-radius:10px;font-size:12px;cursor:pointer;width:100%;
}
.hand-container{overflow-x:auto;display:flex;gap:8px;padding:4px 0}
.card{
  min-width:84px;width:84px;height:112px;border-radius:12px;padding:6px;
  display:flex;flex-direction:column;justify-content:space-between;cursor:pointer;
  background:linear-gradient(160deg,#fff,#f1f5f9);color:#0f172a;
}
.card.selected{background:linear-gradient(160deg,#fef08a,#fde047);box-shadow:0 0 0 2px #facc15;transform:translateY(-5px)}
.card-rarity{font-size:8px;padding:2px 5px;border-radius:4px;color:#fff;width:fit-content}
.rarity-SSR{background:#f97316}.rarity-SR{background:#a855f7}.rarity-R{background:#3b82f6}
.rarity-SSSR{background:linear-gradient(90deg,#ff006e,#8338ec,#3a86ff)}
.card-attr{font-size:8px;color:#64748b}
.battle-actions{display:flex;gap:6px;justify-content:center;flex-wrap:wrap;margin-top:4px}
.choice-box{
  display:none;position:absolute;left:50%;top:36%;transform:translate(-50%,-50%);
  width:86%;max-width:320px;z-index:50;background:rgba(15,23,42,.97);
  border:1px solid #fbbf24;border-radius:16px;padding:16px;text-align:center;flex-direction:column;gap:10px;
}

#deck-edit-screen,#gacha-screen,#zukan-screen,#achieve-screen,#reaction-list-screen,
#history-screen,#quiz-only-screen,#isomer-screen,#lab-screen,#refine-screen{
  background:linear-gradient(180deg,#0f172a,#020617);padding:24px 12px 12px;overflow:hidden;
}
.deck-list{flex:1;overflow-y:auto;max-height:32vh;margin-top:6px}
.deck-item{
  display:flex;justify-content:space-between;align-items:center;
  background:rgba(30,41,59,.85);padding:8px 10px;margin-bottom:5px;border-radius:10px;
  border:1px solid rgba(71,85,105,.4);
}
.deck-item.in-deck{border-color:rgba(52,211,153,.4);background:rgba(16,185,129,.12)}
.action-btn{background:none;border:none;font-size:16px;cursor:pointer;padding:4px}
.info-box{
  background:rgba(15,23,42,.9);border:1px solid rgba(71,85,105,.5);border-radius:12px;
  padding:10px;margin-top:6px;overflow-y:auto;font-size:11px;line-height:1.5;
}
.synth-bar-wrap{background:rgba(30,41,59,.9);border-radius:10px;padding:10px;margin:6px 0;border:1px solid rgba(56,189,248,.25)}
.synth-bar-bg{height:8px;background:#1e293b;border-radius:999px;overflow:hidden;margin-top:6px}
.synth-bar-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,#22d3ee,#818cf8)}
.preset-row{display:flex;gap:6px;flex-wrap:wrap;margin:4px 0;align-items:center}
.preset-row input{background:#0f172a;border:1px solid #475569;border-radius:8px;color:#e2e8f0;padding:8px 10px;font-size:12px;width:100px}
.scroll-panel{
  flex:1;overflow-y:auto;background:rgba(15,23,42,.85);border:1px solid rgba(71,85,105,.45);
  border-radius:12px;padding:12px;font-size:12px;line-height:1.55;color:#cbd5e1;margin:8px 0;
}
.zukan-item{background:rgba(30,41,59,.8);border-radius:10px;padding:10px;margin-bottom:7px;border-left:3px solid #38bdf8}
.achieve-item{background:rgba(30,41,59,.8);border-radius:10px;padding:10px;margin-bottom:7px;display:flex;justify-content:space-between;align-items:center}
.achieve-item.done{border-left:3px solid #22c55e}.achieve-item.locked{opacity:.55}
.gacha-card-view{
  width:230px;height:170px;border-radius:14px;border:1px solid rgba(168,85,247,.45);
  background:rgba(88,28,135,.3);display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:12px;margin:8px auto;
}
.longpress-popup{
  display:none;position:fixed;left:50%;top:50%;transform:translate(-50%,-50%);
  width:88%;max-width:340px;background:rgba(15,23,42,.98);border:1px solid #38bdf8;
  border-radius:16px;padding:16px;z-index:100;max-height:60vh;overflow-y:auto;
}
.filter-row,.row-btns{display:flex;gap:6px;flex-wrap:wrap;margin:8px 0;align-items:center}
.row-btns .glass-btn{flex:1;min-width:90px}
</style>
</head>
<body>

<div id="deck-select-screen" class="screen active">
  <h2>有機化学バトルフィールド</h2>
  <p style="font-size:13px;color:#94a3b8">スターターデッキを選択</p>
  <div style="width:100%;max-width:400px">
    <div class="select-card purple" onclick="assignStarterDeck('Aromatic')">
      <span class="badge">芳香族</span>
      <h3 style="margin:6px 0;font-size:16px">芳香族・置換反応デッキ</h3>
      <p style="font-size:11px;opacity:.9">ニトロ化・スルホン化で高火力</p>
    </div>
    <div class="select-card red" onclick="assignStarterDeck('Polymer')">
      <span class="badge">付加・高分子</span>
      <h3 style="margin:6px 0;font-size:16px">付加・高分子デッキ</h3>
      <p style="font-size:11px;opacity:.9">ハロゲン付加・重合</p>
    </div>
    <div class="select-card green" onclick="assignStarterDeck('Redox')">
      <span class="badge">酸化・エステル</span>
      <h3 style="margin:6px 0;font-size:16px">酸化・エステル・コントロール</h3>
      <p style="font-size:11px;opacity:.9">エステル化・けん化</p>
    </div>
  </div>
</div>

<div id="field-screen" class="screen">
  <div id="canvas-container"></div>
  <div class="field-ui">
    <div class="status-box">
      <div>🧪 試薬: <span id="field-reagents">150</span></div>
      <div style="color:#4ade80;margin-top:2px">❤️ HP: <span id="field-hp">200</span></div>
      <div style="color:#fbbf24;font-size:12px;margin-top:2px">🎓 <span id="field-rank">初学者</span> · 撃破 <span id="field-kills">0</span></div>
      <div style="color:#67e8f9;font-size:11px;margin-top:2px">🏠 研究室 Lv.<span id="field-lab">1</span></div>
      <div id="daily-hint" style="font-size:10px;color:#a5b4fc;margin-top:5px"></div>
      <div id="zukan-comp-hint" style="font-size:10px;color:#86efac;margin-top:2px"></div>
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
      <div class="menu-label">編成・ガチャ</div>
      <button type="button" class="glass-btn primary wide" onclick="menuGo('deckEdit')">デッキ編集</button>
      <button type="button" class="glass-btn pink wide" onclick="menuGo('gacha')">ガチャ</button>
      <button type="button" class="glass-btn slate wide" onclick="menuGo('refine')">精製</button>
      <div class="menu-label">図鑑・実績・研究室</div>
      <button type="button" class="glass-btn warn wide" onclick="menuGo('zukan')">図鑑</button>
      <button type="button" class="glass-btn success wide" onclick="menuGo('achieve')">実績</button>
      <button type="button" class="glass-btn primary wide" onclick="menuGo('lab')">研究室</button>
      <div class="menu-label">学習モード</div>
      <button type="button" class="glass-btn wide" onclick="menuGoQuiz()">クイズ</button>
      <button type="button" class="glass-btn pink wide" onclick="menuGoIsomer()">異性体</button>
      <button type="button" class="glass-btn slate wide" style="margin-top:8px" onclick="closeFieldMenu(true)">閉じる</button>
    </div>
  </div>
</div>

<div id="battle-screen" class="screen">
  <div class="battle-header">
    <div>
      <div style="color:#4ade80">🧑 HP: <span id="battle-player-hp">200</span></div>
      <div style="color:#38bdf8;font-size:11px">📚 山札: <span id="battle-deck-count">0</span></div>
      <div id="combo-status" style="font-size:11px;color:#fbbf24">🔗 コンボ: 0</div>
      <div id="next-bonus" style="font-size:11px;color:#fbbf24;display:none">次ターン火力UP</div>
      <div id="dot-status" style="font-size:11px;color:#f87171;display:none">☠️ 毒素DoT</div>
      <div id="turn-limit" style="font-size:11px;color:#f472b6;display:none"></div>
    </div>
    <div style="text-align:right">
      <div style="font-size:12px;color:#94a3b8">👾 <span id="monster-name">敵</span> Lv.<span id="monster-level">1</span></div>
      <div style="color:#f87171;font-size:15px"><span id="monster-hp">500</span>/<span id="monster-maxhp">500</span></div>
      <div id="monster-weak" style="font-size:10px;color:#fb923c"></div>
      <div id="monster-cond" style="font-size:10px;color:#e879f9"></div>
    </div>
  </div>
  <div id="lab-canvas-container"></div>
  <div id="quiz-container" class="quiz-box" style="display:none">
    <div style="font-size:11px;color:#e9d5ff">📝 クイズ（正解1.5倍）</div>
    <div id="quiz-question"></div>
    <div id="quiz-options" class="quiz-options"></div>
  </div>
  <div id="battle-log" class="battle-log-box">バトル開始</div>
  <div>
    <div style="font-size:10px;color:#94a3b8">手札 (<span id="hand-count">0</span>/7) 長押しで反応 ※精製も反応可</div>
    <div id="hand-cards" class="hand-container"></div>
  </div>
  <div class="battle-actions">
    <button type="button" id="attack-btn" class="glass-btn orange" style="flex:1.4" onclick="executePlayerAttack()">化学反応実行</button>
    <button type="button" id="skip-btn" class="glass-btn slate" onclick="skipTurn()">ターン終了</button>
    <button type="button" id="flee-btn" class="glass-btn danger" onclick="fleeBattle()">逃げる</button>
    <button type="button" class="glass-btn primary" onclick="openReactionList()">反応一覧</button>
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
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#c4b5fd">📝 クイズモード</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <p style="font-size:12px;color:#94a3b8;margin:8px 0">正解 <span id="qo-score">0</span> / <span id="qo-total">0</span></p>
  <div class="quiz-box" style="display:flex;margin-top:12px">
    <div id="qo-question"></div>
    <div id="qo-options" class="quiz-options"></div>
    <div id="qo-feedback" style="font-size:12px;color:#fbbf24;min-height:20px"></div>
  </div>
  <button type="button" class="glass-btn primary wide" style="margin-top:12px" onclick="nextQuizOnly()">次の問題</button>
</div>

<div id="isomer-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#f9a8d4">🔀 異性体チャレンジ</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <p style="font-size:12px;color:#94a3b8;margin:8px 0">正解で試薬獲得</p>
  <p style="font-size:12px;color:#fbbf24">スコア <span id="iso-score">0</span>　連続 <span id="iso-streak">0</span></p>
  <div class="quiz-box" style="display:flex;margin-top:12px">
    <div id="iso-question"></div>
    <div id="iso-options" class="quiz-options"></div>
    <div id="iso-feedback" style="font-size:12px;color:#fbbf24;min-height:24px"></div>
  </div>
  <button type="button" class="glass-btn pink wide" style="margin-top:12px" onclick="nextIsomerQ()">次の問題</button>
</div>

<div id="lab-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#67e8f9">🏠 研究室</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <div class="scroll-panel">
    <div>レベル <span id="lab-lv">1</span></div>
    <div class="synth-bar-bg" style="margin-top:8px"><div id="lab-bar" class="synth-bar-fill" style="width:0%"></div></div>
    <div style="font-size:11px;color:#94a3b8;margin-top:6px">経験 <span id="lab-exp">0</span> / <span id="lab-next">30</span></div>
    <div id="lab-perks" style="margin-top:12px;line-height:1.7;font-size:12px"></div>
    <button type="button" id="lab-free-gacha-btn" class="glass-btn pink wide" style="margin-top:14px" onclick="labFreeGacha()">今日の無料ガチャ</button>
    <div id="lab-msg" style="font-size:12px;color:#fbbf24;margin-top:8px"></div>
  </div>
</div>

<div id="refine-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#fbbf24">✨ カード精製</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <p style="font-size:12px;color:#94a3b8;margin:8px 0">同名3枚 → 精製版（攻回×1.15）※精製でも通常と同じ反応が起きます</p>
  <div id="refine-list" class="scroll-panel"></div>
</div>

<div id="reaction-list-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#fbbf24">📖 反応一覧</h3>
    <button type="button" class="glass-btn primary" onclick="closeReactionList()">戻る</button>
  </div>
  <div id="full-reaction-list" class="scroll-panel" style="white-space:pre-line"></div>
</div>

<div id="history-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px">
    <h3 style="color:#c4b5fd">📜 履歴 / リプレイ</h3>
    <div class="row-btns">
      <button type="button" class="glass-btn" onclick="showLastReplay()">直前リプレイ</button>
      <button type="button" class="glass-btn slate" onclick="closeHistory()">戻る</button>
    </div>
  </div>
  <div id="history-list" class="scroll-panel" style="white-space:pre-line"></div>
</div>

<div id="zukan-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#fbbf24">📘 図鑑 (<span id="zukan-count">0</span>)</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <div class="filter-row">
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('all')">全て</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('SSSR')">SSSR</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('SSR')">SSR</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('SR')">SR</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('R')">R</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('react')">反応あり</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('heal')">回復</button>
    <button type="button" class="glass-btn mini-btn slate" onclick="setZukanFilter('both')">攻回両用</button>
  </div>
  <div id="zukan-list" class="scroll-panel"></div>
</div>

<div id="achieve-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#a3e635">🏅 実績</h3>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <div id="achieve-list" class="scroll-panel"></div>
</div>

<div id="deck-edit-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px">
    <div>
      <h3 style="font-size:16px">デッキ編集 (<span id="deck-count">0</span>/50)</h3>
      <p style="font-size:11px;color:#94a3b8">最低20 / 最大50</p>
    </div>
    <div class="row-btns">
      <button type="button" class="glass-btn mini-btn warn" onclick="recommendDeck()">おすすめ</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('name')">名前</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('rarity')">レア</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('power')">火力</button>
      <button type="button" id="deck-done-btn" class="glass-btn success" onclick="finishDeckEdit()">完了</button>
    </div>
  </div>
  <div class="preset-row">
    <input id="preset-name-0" placeholder="スロット1名" maxlength="12">
    <button type="button" class="glass-btn mini-btn primary" onclick="saveDeckSlot(0)">保存1</button>
    <button type="button" class="glass-btn mini-btn primary" onclick="loadDeckSlot(0)">読込1</button>
  </div>
  <div class="preset-row">
    <input id="preset-name-1" placeholder="スロット2名" maxlength="12">
    <button type="button" class="glass-btn mini-btn primary" onclick="saveDeckSlot(1)">保存2</button>
    <button type="button" class="glass-btn mini-btn primary" onclick="loadDeckSlot(1)">読込2</button>
  </div>
  <div class="preset-row">
    <input id="preset-name-2" placeholder="スロット3名" maxlength="12">
    <button type="button" class="glass-btn mini-btn primary" onclick="saveDeckSlot(2)">保存3</button>
    <button type="button" class="glass-btn mini-btn primary" onclick="loadDeckSlot(2)">読込3</button>
  </div>
  <div id="preset-labels" style="font-size:11px;color:#94a3b8"></div>
  <div class="synth-bar-wrap">
    <div style="display:flex;justify-content:space-between">
      <span style="font-size:12px;color:#67e8f9">合成可能率</span>
      <span id="synth-rate-text">—</span>
    </div>
    <div class="synth-bar-bg"><div id="synth-rate-bar" class="synth-bar-fill" style="width:0%"></div></div>
    <div id="synth-hint" style="font-size:10px;color:#94a3b8;margin-top:5px"></div>
  </div>
  <div id="deck-list" class="deck-list"></div>
  <div class="info-box" style="max-height:16vh">
    <div style="color:#fbbf24;margin-bottom:4px">📖 反応一覧</div>
    <div id="deck-reaction-list" style="white-space:pre-line;font-size:11px;color:#cbd5e1"></div>
  </div>
</div>

<div id="gacha-screen" class="screen" style="align-items:center;overflow-y:auto">
  <h2 style="color:#e879f9;margin-top:8px">🧪 ガチャ</h2>
  <p style="color:#7dd3fc">試薬: <span id="gacha-reagents">150</span>　ランク: <span id="gacha-rank">初学者</span></p>
  <div id="gacha-result" class="gacha-card-view"><span style="color:#94a3b8">ガチャ結果</span></div>
  <div class="row-btns" style="width:100%;max-width:360px;justify-content:center">
    <button type="button" class="glass-btn pink" onclick="drawGacha()">ガチャ (100)</button>
    <button type="button" class="glass-btn slate" onclick="goBackFromMenu()">戻る</button>
  </div>
  <div class="info-box" style="width:100%;max-width:420px;max-height:34vh">
    <div style="color:#fbbf24;margin-bottom:4px">排出一覧</div>
    <div id="gacha-list" style="white-space:pre-line;color:#cbd5e1"></div>
  </div>
</div>

<div id="longpress-popup" class="longpress-popup">
  <div style="color:#38bdf8;margin-bottom:8px" id="lp-title">反応</div>
  <div id="lp-body" style="font-size:12px;white-space:pre-line;line-height:1.5"></div>
  <button type="button" class="glass-btn slate wide" style="margin-top:12px" onclick="closeLongPress()">閉じる</button>
</div>

<script>
/* ===== データ ===== */
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

const RANKS=[
{name:"初学者",kills:0,reagentBonus:1.0,gachaBoost:0,promoteReward:0},
{name:"高校生",kills:8,reagentBonus:1.15,gachaBoost:0.3,promoteReward:40},
{name:"大学生",kills:20,reagentBonus:1.3,gachaBoost:0.6,promoteReward:60},
{name:"大学院生",kills:40,reagentBonus:1.5,gachaBoost:1.0,promoteReward:80},
{name:"助教",kills:55,reagentBonus:1.7,gachaBoost:1.2,promoteReward:100},
{name:"准教授",kills:75,reagentBonus:1.9,gachaBoost:1.5,promoteReward:120},
{name:"博士",kills:100,reagentBonus:2.2,gachaBoost:1.8,promoteReward:150},
{name:"教授",kills:140,reagentBonus:2.5,gachaBoost:2.2,promoteReward:200}
];
const LAB_THRESH=[0,30,70,120,180,250,330,420,520,650];
const ACHIEVEMENTS=[
{id:"first_win",name:"初勝利",desc:"初めて敵を倒す",reward:30,check:function(s){return s.kills>=1}},
{id:"kills_10",name:"撃破10",desc:"10体倒す",reward:50,check:function(s){return s.kills>=10}},
{id:"kills_50",name:"撃破50",desc:"50体倒す",reward:120,check:function(s){return s.kills>=50}},
{id:"nitro",name:"ニトロ化",desc:"ニトロ化成功",reward:40,check:function(s){return s.flags.nitro}},
{id:"sapon",name:"けん化",desc:"けん化成功",reward:40,check:function(s){return s.flags.sapon}},
{id:"poly",name:"重合",desc:"重合成功",reward:40,check:function(s){return s.flags.poly}},
{id:"acetyl",name:"アセチル化",desc:"アセチル化成功",reward:45,check:function(s){return s.flags.acetyl}},
{id:"dehyd",name:"脱水",desc:"脱水成功",reward:45,check:function(s){return s.flags.dehyd}},
{id:"collect_20",name:"収集家",desc:"図鑑20種",reward:60,check:function(s){return uniqCount(s)>=20}},
{id:"boss",name:"ボス討伐",desc:"ボスを倒す",reward:80,check:function(s){return s.flags.boss}},
{id:"combo3",name:"3連鎖",desc:"コンボ3",reward:50,check:function(s){return s.flags.combo3}},
{id:"refine1",name:"初精製",desc:"1回精製",reward:40,check:function(s){return s.flags.refined}}
];
const DAILY_QUESTS=[
{key:"nitro",label:"ニトロ化を1回"},{key:"sapon",label:"けん化を1回"},{key:"poly",label:"重合を1回"},
{key:"ester",label:"エステル化を1回"},{key:"oxid",label:"酸化を1回"},{key:"acetyl",label:"アセチル化を1回"},{key:"dehyd",label:"脱水を1回"}
];

/* 反応一覧（フル） */
const FULL_REACTION_TEXT=
`【中間体・連鎖】（手札に加えた中間カード・精製カードも同じ反応可）
・ベンゼン + ニトロ基 → ニトロベンゼン（中間）
・ニトロベンゼン（中間可） + 還元剤 / NaBH4 → アニリン（中間）
・アニリン（中間可） + ジアゾ化剤 → アゾベンゼン
・アニリン（中間可） + 無水酢酸 → アセトアニリド
・酢酸 + エタノール → 酢酸エチル（中間）
・酢酸エチル（中間可） + NaOH → けん化
・サリチル酸 + 無水酢酸 → アセチルサリチル酸

【アセチル化】
・アニリン + 無水酢酸 → アセトアニリド
・サリチル酸 + 無水酢酸 → アセチルサリチル酸

【脱水】
・エタノール + 濃硫酸 → エチレン
・1-プロパノール + 濃硫酸 → プロピレン

【油脂・けん化】
・トリパルミチン / トリステアリン / トリオレイン + NaOH
・酢酸 / 酢酸エチル / オレイン酸 + NaOH

【ニトロ化】
・ベンゼン / トルエン / フェノール / ナフタレン / アントラセン + 濃硝酸
・ベンゼン + ニトロ基 → ニトロベンゼン

【スルホン化】
・ベンゼン / ナフタレン + 濃硫酸

【ハロゲン化・付加】
・ベンゼン + 塩素 / 臭素 + 触媒（鉄・AlCl3等）
・エチレン + 塩素 / 臭素 → 付加
・アセチレン + 臭素 → 付加
・シス-2-ブテン / トランス-2-ブテン + 臭素 → 付加

【重合】
・エチレン / スチレン / プロピレン / ビニル基 + 重合触媒(Ziegler)

【酸化】
・エタノール / メタノール / アセトアルデヒド + KMnO4 / K2Cr2O7
・2-プロパノール + 酸化剤 → ケトン
・トルエン + KMnO4 → 側鎖酸化（安息香酸）

【金属ナトリウム】
・エタノール / メタノール / 1-プロパノール + Na → アルコキシド
・フェノール / クレゾール + Na → フェノキシド等

【基 + 官能基】
・メチル基 / エチル基 / フェニル基 / ビニル基
　+ ヒドロキシ基 / カルボキシ基 / アミノ基 / ニトロ基 など

【特殊】
・TNT / ピクリン酸 … 180
・フッ化水素酸 … ∞（1/10で自爆）
・ボツリヌス毒素 … 毎ターン200継続
・同名複数選択 … 威力×枚数
・精製○○ … 通常名と同じ反応、威力1.15倍

【倍率】
・触媒なし 1.5倍 / 触媒あり 2.0倍
・弱点 1.5倍 / クイズ正解 1.5倍 / コンボ +5%/段`;

const CARD_REACTIONS={
"ベンゼン":"・+ニトロ基 → ニトロベンゼン\n・+濃硝酸 → ニトロ化\n・+濃硫酸 → スルホン化\n・+塩素/臭素+触媒 → ハロゲン化",
"トルエン":"・+濃硝酸 → ニトロ化\n・+KMnO4 → 安息香酸",
"フェノール":"・+濃硝酸 → ニトロ化\n・+金属Na → フェノキシド",
"アニリン":"・+ジアゾ化剤 → アゾベンゼン\n・+無水酢酸 → アセトアニリド",
"ニトロベンゼン":"・+還元剤 / NaBH4 → アニリン",
"アゾベンゼン":"・単体投擲で高火力",
"酢酸":"・+エタノール → 酢酸エチル\n・+NaOH → けん化",
"エタノール":"・+酢酸 → エステル\n・+濃硫酸 → 脱水\n・+Na / 酸化剤",
"酢酸エチル":"・+NaOH → けん化",
"エチレン":"・+ハロゲン付加\n・+重合触媒",
"無水酢酸":"・+アニリン / サリチル酸 → アセチル化",
"サリチル酸":"・+無水酢酸 → アセチルサリチル酸",
"アセトアニリド":"・単体投擲可",
"アセチルサリチル酸":"・単体投擲で高火力",
"水酸化ナトリウム":"・けん化全般",
"重合触媒(Ziegler)":"・オレフィン重合",
"過マンガン酸カリウム":"・酸化",
"金属ナトリウム":"・+アルコール / フェノール",
"濃硝酸":"・芳香族ニトロ化",
"濃硫酸":"・触媒・脱水・スルホン化",
"ナフタレン":"・ニトロ化 / スルホン化",
"アントラセン":"・+濃硝酸",
"還元剤":"・ニトロベンゼン → アニリン",
"ジアゾ化剤":"・アニリン → アゾベンゼン"
};

const SYNTH_PAIRS=[
{a:["ベンゼン"],b:["ニトロ基","濃硝酸","濃硫酸","塩素","臭素"]},
{a:["トルエン"],b:["濃硝酸","過マンガン酸カリウム"]},
{a:["フェノール"],b:["濃硝酸","金属ナトリウム"]},
{a:["アニリン"],b:["ジアゾ化剤","無水酢酸"]},
{a:["ニトロベンゼン"],b:["還元剤","水素化ホウ素ナトリウム"]},
{a:["酢酸"],b:["エタノール","水酸化ナトリウム"]},
{a:["エタノール"],b:["酢酸","濃硫酸","金属ナトリウム","過マンガン酸カリウム"]},
{a:["エチレン"],b:["塩素","臭素","重合触媒(Ziegler)"]},
{a:["スチレン","プロピレン"],b:["重合触媒(Ziegler)"]},
{a:["サリチル酸"],b:["無水酢酸"]},
{a:["トリパルミチン","トリステアリン","トリオレイン","オレイン酸","酢酸エチル"],b:["水酸化ナトリウム"]},
{a:["メチル基","エチル基","フェニル基","ビニル基"],b:["ヒドロキシ基","カルボキシ基","アミノ基","ニトロ基"]},
{a:["アセチレン","シス-2-ブテン","トランス-2-ブテン"],b:["臭素"]},
{a:["ナフタレン","アントラセン"],b:["濃硝酸","濃硫酸"]}
];

const QUIZ_BANK=[
{q:"ベンゼンのニトロ化生成物は？",opts:["ニトロベンゼン","フェノール","トルエン","アニリン"],ok:0,ex:"ニトロベンゼンです。"},
{q:"エステル化の触媒は？",opts:["濃硫酸","NaOH","KMnO4","Fe"],ok:0,ex:"濃硫酸です。"},
{q:"第一級アルコール酸化の最終物は？",opts:["カルボン酸","ケトン","エーテル","アルケン"],ok:0,ex:"カルボン酸です。"},
{q:"第二級アルコールの酸化は？",opts:["ケトン","カルボン酸","アルデヒド","エーテル"],ok:0,ex:"ケトンです。"},
{q:"油脂のけん化で出るアルコールは？",opts:["グリセリン","エタノール","メタノール","フェノール"],ok:0,ex:"グリセリンです。"},
{q:"エタノールを濃硫酸で脱水すると？",opts:["エチレン","酢酸","アセトン","メタン"],ok:0,ex:"エチレンです。"},
{q:"ニトロベンゼンを還元すると？",opts:["アニリン","フェノール","ベンゼン","トルエン"],ok:0,ex:"アニリンです。"},
{q:"トルエンをKMnO4酸化すると？",opts:["安息香酸","フェノール","ベンゼン","ベンズアルデヒド"],ok:0,ex:"安息香酸です。"}
];
const ISOMER_BANK=[
{q:"マレイン酸の幾何異性体は？",opts:["フマル酸","コハク酸","シュウ酸","安息香酸"],ok:0,ex:"フマル酸(trans)です。"},
{q:"cis-2-ブテンの異性体は？",opts:["trans-2-ブテン","1-ブテン","イソブテン","ブタン"],ok:0,ex:"シス/トランスです。"},
{q:"フェノールのパラ位メチル体は？",opts:["p-クレゾール","o-クレゾール","m-クレゾール","キシレン"],ok:0,ex:"p-クレゾールです。"},
{q:"オレイン酸の二重結合は主に？",opts:["シス","トランス","両方","なし"],ok:0,ex:"ほぼシスです。"},
{q:"隣同士の置換は？",opts:["オルト","メタ","パラ","なし"],ok:0,ex:"オルトです。"},
{q:"1,4-位の置換は？",opts:["パラ","オルト","メタ","ジェミナル"],ok:0,ex:"パラです。"}
];
const RARITY_ORDER={SSSR:0,SSR:1,SR:2,R:3};

function uniqCount(s){var set={},n=0;(s.collection||[]).forEach(function(c){var k=baseName(c.name);if(!set[k]){set[k]=1;n++;}});return n;}
function baseName(n){return String(n||'').replace(/^精製/,'');}
function fmt(v){return v===Infinity?'∞':v;}
function powerValue(c){if(!c)return 0;if(baseName(c.name)==='ボツリヌス毒素')return 200;if(c.attackPower===Infinity)return 99999;return (c.attackPower||0)+(c.healPower||0);}
function uid(){return Math.random().toString(36).slice(2,11);}
function todayStr(){var d=new Date();return d.getFullYear()+'-'+(d.getMonth()+1)+'-'+d.getDate();}

var gameState={
  reagents:150,playerHP:200,playerMaxHP:200,collection:[],currentDeck:[],kills:0,lastRank:'初学者',
  flags:{nitro:false,sapon:false,poly:false,ester:false,oxid:false,acetyl:false,dehyd:false,fat:false,boss:false,combo3:false,refined:false},
  achieved:{},dailyDate:'',dailyKey:'',dailyDone:false,deckListOrder:[],
  deckSlots:[{name:'',cards:[]},{name:'',cards:[]},{name:'',cards:[]}],
  labLevel:1,labExp:0,labFreeDate:'',zukanRewards:{r30:false,r60:false,r90:false},lastReplay:[],nextDamageBonus:1.0
};

var returnToMenu=false; /* メニュー経由で戻るときメニューを開き直す */
var isBattleOver=false,isProcessing=false,botulinumActive=false,isPractice=false;
var pendingIntermediate=null,fromBattleToReaction=false,fromBattleToHistory=false;
var battleHistory=[],battleTurnCount=0,bossTurnLimit=0,comboCount=0,zukanFilter='all';
var qoScore=0,qoTotal=0,isoScore=0,isoStreak=0;
var bDeck=[],bHand=[],bSelected=[],monsterHP=500,isPlayerTurn=true;

function openFieldMenu(){var m=document.getElementById('field-menu');if(m)m.style.display='flex';}
function closeFieldMenu(clearFlag){
  var m=document.getElementById('field-menu');if(m)m.style.display='none';
  if(clearFlag) returnToMenu=false;
}
function menuGo(s){returnToMenu=true;closeFieldMenu(false);switchState(s);}
function menuGoQuiz(){returnToMenu=true;closeFieldMenu(false);startQuizOnly();}
function menuGoIsomer(){returnToMenu=true;closeFieldMenu(false);startIsomerMode();}
/** メニューから来た画面の「戻る」→ フィールド＋メニュー再表示 */
function goBackFromMenu(){
  switchState('field');
  if(returnToMenu){ openFieldMenu(); }
}

function initDaily(){
  var t=todayStr();
  if(gameState.dailyDate!==t){gameState.dailyDate=t;gameState.dailyKey=DAILY_QUESTS[Math.floor(Math.random()*DAILY_QUESTS.length)].key;gameState.dailyDone=false;}
}
function getDailyLabel(){var q=DAILY_QUESTS.find(function(x){return x.key===gameState.dailyKey;});return q?q.label:'—';}
function getRank(){var r=RANKS[0];for(var i=0;i<RANKS.length;i++){if(gameState.kills>=RANKS[i].kills)r=RANKS[i];}return r;}
function checkRankUp(){
  var r=getRank();
  if(r.name!==gameState.lastRank){
    if(r.promoteReward>0){gameState.reagents+=r.promoteReward;alert('ランクアップ！ '+gameState.lastRank+' → '+r.name+'\n試薬 +'+r.promoteReward);}
    gameState.lastRank=r.name;
  }
}
function addLabExp(n){
  gameState.labExp+=n;
  while(gameState.labLevel<LAB_THRESH.length&&gameState.labExp>=(LAB_THRESH[gameState.labLevel]||99999)){
    gameState.labLevel++;var bonus=20+gameState.labLevel*5;gameState.reagents+=bonus;
    (function(lv,b){setTimeout(function(){alert('研究室 Lv.'+lv+'\n試薬 +'+b);},200);})(gameState.labLevel,bonus);
  }
}
function checkZukanRewards(){
  var n=uniqCount(gameState),pct=Math.floor(n/ALL_CARDS.length*100);
  if(pct>=30&&!gameState.zukanRewards.r30){gameState.zukanRewards.r30=true;gameState.reagents+=40;setTimeout(function(){alert('図鑑30% 試薬+40');},200);}
  if(pct>=60&&!gameState.zukanRewards.r60){gameState.zukanRewards.r60=true;gameState.reagents+=80;setTimeout(function(){alert('図鑑60% 試薬+80');},200);}
  if(pct>=90&&!gameState.zukanRewards.r90){gameState.zukanRewards.r90=true;gameState.reagents+=150;setTimeout(function(){alert('図鑑90% 試薬+150');},200);}
}
function checkAchievements(){
  for(var i=0;i<ACHIEVEMENTS.length;i++){
    var a=ACHIEVEMENTS[i];if(gameState.achieved[a.id])continue;
    if(a.check(gameState)){gameState.achieved[a.id]=true;gameState.reagents+=a.reward;
      (function(name,rw){setTimeout(function(){alert('実績「'+name+'」 試薬 +'+rw);},250);})(a.name,a.reward);}
  }
  checkZukanRewards();
}
function markFlag(f){
  gameState.flags[f]=true;
  if(!gameState.dailyDone&&gameState.dailyKey===f){gameState.dailyDone=true;gameState.reagents+=50;setTimeout(function(){alert('日替わりクリア 試薬+50');},200);}
  checkAchievements();
}

function saveGame(silent){try{localStorage.setItem('organicChemBattleSave',JSON.stringify(gameState));if(!silent)alert('セーブしました');}catch(e){alert('セーブ失敗');}}
function loadGame(){
  var raw=localStorage.getItem('organicChemBattleSave');if(!raw){alert('セーブがありません');return;}
  try{
    var data=JSON.parse(raw);
    gameState.reagents=data.reagents||150;gameState.playerHP=data.playerHP||200;gameState.playerMaxHP=data.playerMaxHP||200;
    gameState.collection=data.collection||[];gameState.currentDeck=data.currentDeck||[];gameState.kills=data.kills||0;gameState.lastRank=data.lastRank||'初学者';
    gameState.flags=Object.assign({nitro:false,sapon:false,poly:false,ester:false,oxid:false,acetyl:false,dehyd:false,fat:false,boss:false,combo3:false,refined:false},data.flags||{});
    gameState.achieved=data.achieved||{};gameState.dailyDate=data.dailyDate||'';gameState.dailyKey=data.dailyKey||'';gameState.dailyDone=!!data.dailyDone;
    gameState.deckListOrder=data.deckListOrder||[];gameState.labLevel=data.labLevel||1;gameState.labExp=data.labExp||0;gameState.labFreeDate=data.labFreeDate||'';
    gameState.zukanRewards=Object.assign({r30:false,r60:false,r90:false},data.zukanRewards||{});gameState.lastReplay=data.lastReplay||[];gameState.nextDamageBonus=1.0;
    if(data.deckSlots&&data.deckSlots[0]&&data.deckSlots[0].cards)gameState.deckSlots=data.deckSlots;
    else gameState.deckSlots=[{name:'',cards:[]},{name:'',cards:[]},{name:'',cards:[]}];
    returnToMenu=false;initDaily();updateFieldUI();switchState('field');alert('ロードしました');
  }catch(e){alert('ロード失敗');}
}

function switchState(s){
  var ids=['deck-select-screen','field-screen','battle-screen','deck-edit-screen','gacha-screen','zukan-screen','achieve-screen','reaction-list-screen','history-screen','quiz-only-screen','isomer-screen','lab-screen','refine-screen'];
  for(var i=0;i<ids.length;i++){var el=document.getElementById(ids[i]);if(el)el.classList.remove('active');}
  if(s!=='field') closeFieldMenu(false);
  if(s==='deckSelection')document.getElementById('deck-select-screen').classList.add('active');
  if(s==='field'){document.getElementById('field-screen').classList.add('active');updateFieldUI();initThreeJS();}
  if(s==='battle'){returnToMenu=false;document.getElementById('battle-screen').classList.add('active');}
  if(s==='deckEdit'){document.getElementById('deck-edit-screen').classList.add('active');renderDeckEdit();}
  if(s==='gacha'){document.getElementById('gacha-screen').classList.add('active');document.getElementById('gacha-reagents').innerText=gameState.reagents;document.getElementById('gacha-rank').innerText=getRank().name;renderGachaList();}
  if(s==='reactionList'){document.getElementById('reaction-list-screen').classList.add('active');document.getElementById('full-reaction-list').innerText=FULL_REACTION_TEXT;}
  if(s==='zukan'){document.getElementById('zukan-screen').classList.add('active');renderZukan();}
  if(s==='achieve'){document.getElementById('achieve-screen').classList.add('active');renderAchieve();}
  if(s==='history'){document.getElementById('history-screen').classList.add('active');document.getElementById('history-list').innerText=battleHistory.slice(-40).join('\n\n')||'履歴なし';}
  if(s==='quizOnly')document.getElementById('quiz-only-screen').classList.add('active');
  if(s==='isomer')document.getElementById('isomer-screen').classList.add('active');
  if(s==='lab'){document.getElementById('lab-screen').classList.add('active');renderLab();}
  if(s==='refine'){document.getElementById('refine-screen').classList.add('active');renderRefine();}
}
function openReactionList(){fromBattleToReaction=true;switchState('reactionList');}
function closeReactionList(){
  if(fromBattleToReaction){fromBattleToReaction=false;document.querySelectorAll('.screen').forEach(function(el){el.classList.remove('active');});document.getElementById('battle-screen').classList.add('active');updateBattleUI();}
  else goBackFromMenu();
}
function openHistory(){fromBattleToHistory=true;switchState('history');}
function closeHistory(){
  if(fromBattleToHistory){fromBattleToHistory=false;document.querySelectorAll('.screen').forEach(function(el){el.classList.remove('active');});document.getElementById('battle-screen').classList.add('active');updateBattleUI();}
  else goBackFromMenu();
}
function showLastReplay(){var r=gameState.lastReplay||[];document.getElementById('history-list').innerText=r.length?'【直前リプレイ】\n\n'+r.join('\n\n'):'リプレイなし';}

function updateFieldUI(){
  initDaily();
  document.getElementById('field-reagents').innerText=gameState.reagents;
  document.getElementById('field-hp').innerText=gameState.playerHP;
  document.getElementById('field-rank').innerText=getRank().name;
  document.getElementById('field-kills').innerText=gameState.kills;
  document.getElementById('field-lab').innerText=gameState.labLevel;
  document.getElementById('daily-hint').innerText=gameState.dailyDone?'📅 日替わり達成済':'📅 今日: '+getDailyLabel();
  var n=uniqCount(gameState),pct=Math.floor(n/ALL_CARDS.length*100);
  document.getElementById('zukan-comp-hint').innerText='図鑑 '+n+'/'+ALL_CARDS.length+'（'+pct+'%）';
}

function assignStarterDeck(type){
  gameState.currentDeck=[];gameState.collection=[];gameState.deckListOrder=[];returnToMenu=false;
  var names=type==='Aromatic'?['ベンゼン','トルエン','濃硝酸','濃硫酸','フェノール','グルコース','ニトロ基']:
    type==='Polymer'?['エチレン','臭素','塩素','重合触媒(Ziegler)','グルコース','エタノール']:
    ['エタノール','酢酸','水酸化ナトリウム','過マンガン酸カリウム','グルコース','アセトアルデヒド'];
  var base=[];for(var i=0;i<names.length;i++){var c=ALL_CARDS.find(function(x){return x.name===names[i];});if(c)base.push(c);}
  for(var j=0;j<40;j++){var src=base[j%base.length];gameState.currentDeck.push(Object.assign({},src,{id:uid()}));gameState.collection.push(Object.assign({},src,{id:uid()}));}
  gameState.playerHP=gameState.playerMaxHP;gameState.lastRank='初学者';initDaily();switchState('field');
}

function finishDeckEdit(){
  if(gameState.currentDeck.length<20){alert('最低20枚');return;}
  goBackFromMenu();
}

/* 以下、前回版と同じコア処理（精製は baseName で反応判定） */

function saveDeckSlot(i){
  if(gameState.currentDeck.length<20){alert('最低20枚必要');return;}
  var inp=document.getElementById('preset-name-'+i);
  var nm=(inp&&inp.value.trim())||(gameState.deckSlots[i]&&gameState.deckSlots[i].name)||('編成'+(i+1));
  gameState.deckSlots[i]={name:nm,cards:gameState.currentDeck.map(function(c){return Object.assign({},c);})};
  if(inp)inp.value=nm;alert('「'+nm+'」保存');renderDeckEdit();
}
function loadDeckSlot(i){
  var slot=gameState.deckSlots[i];if(!slot||!slot.cards||!slot.cards.length){alert('空です');return;}
  var owned={};gameState.collection.forEach(function(c){owned[c.name]=(owned[c.name]||0)+1;});
  var used={},rebuilt=[];
  for(var j=0;j<slot.cards.length;j++){var c=slot.cards[j];if((used[c.name]||0)<(owned[c.name]||0)){used[c.name]=(used[c.name]||0)+1;rebuilt.push(Object.assign({},c,{id:uid()}));}}
  gameState.currentDeck=rebuilt;var inp=document.getElementById('preset-name-'+i);if(inp)inp.value=slot.name||'';renderDeckEdit();alert('読込 '+rebuilt.length+'枚');
}

function setZukanFilter(f){zukanFilter=f;renderZukan();}
function renderZukan(){
  var names=[],seen={};gameState.collection.forEach(function(c){if(!seen[c.name]){seen[c.name]=1;names.push(c.name);}});
  document.getElementById('zukan-count').innerText=names.length;var list=document.getElementById('zukan-list');list.innerHTML='';
  names=names.filter(function(name){
    var bn=baseName(name);var c=gameState.collection.find(function(x){return x.name===name;})||ALL_CARDS.find(function(x){return x.name===bn;});
    if(!c)return false;
    if(zukanFilter==='all')return true;
    if(['SSSR','SSR','SR','R'].indexOf(zukanFilter)>=0)return c.rarity===zukanFilter;
    if(zukanFilter==='react')return !!CARD_REACTIONS[bn];
    if(zukanFilter==='heal')return (c.healPower||0)>0;
    if(zukanFilter==='both')return (c.attackPower||0)>0&&(c.healPower||0)>0;
    return true;
  }).sort(function(a,b){return a.localeCompare(b,'ja');});
  if(!names.length){list.innerHTML='<div style="color:#94a3b8">該当なし</div>';return;}
  names.forEach(function(name){
    var c=gameState.collection.find(function(x){return x.name===name;})||ALL_CARDS.find(function(x){return x.name===baseName(name);});
    var div=document.createElement('div');div.className='zukan-item';
    div.innerHTML='<div>'+name+' <span class="card-rarity rarity-'+c.rarity+'">'+c.rarity+'</span></div><div style="font-size:11px;color:#94a3b8">'+(c.formula||'')+' / '+c.attribute+'</div><div style="font-size:11px;color:#fbbf24">威力:'+fmt(c.attackPower)+' 回復:'+(c.healPower||0)+'</div>';
    list.appendChild(div);
  });
}
function renderAchieve(){
  var list=document.getElementById('achieve-list');list.innerHTML='';
  ACHIEVEMENTS.forEach(function(a){var done=!!gameState.achieved[a.id];var div=document.createElement('div');div.className='achieve-item '+(done?'done':'locked');
    div.innerHTML='<div><div>'+(done?'✅':'🔒')+' '+a.name+'</div><div style="font-size:11px;color:#94a3b8">'+a.desc+'</div></div><div style="color:#fbbf24">+'+a.reward+'</div>';list.appendChild(div);});
}
function renderGachaList(){
  var html='';['SSSR','SSR','SR','R'].forEach(function(r){
    var cards=ALL_CARDS.filter(function(c){return c.rarity===r;});if(!cards.length)return;html+='【'+r+'】\n';
    cards.forEach(function(c){var p;if(c.name==='ボツリヌス毒素')p='DoT200';else if(c.attackPower===Infinity)p='∞';
      else if((c.attackPower||0)>0&&(c.healPower||0)>0)p='攻'+c.attackPower+'/回'+c.healPower;else if(c.healPower>0)p='回復'+c.healPower;else p=String(c.attackPower);
      html+='・'+c.name+'（'+p+'）\n';});html+='\n';
  });document.getElementById('gacha-list').innerText=html.trim();
}

function calcSynthRate(){
  var names=new Set(gameState.currentDeck.map(function(c){return baseName(c.name);}));
  if(!names.size)return {rate:0,ok:0,total:SYNTH_PAIRS.length,missing:[],healCount:0};
  var ok=0,missing=[];
  SYNTH_PAIRS.forEach(function(pair){
    var hasA=pair.a.some(function(n){return names.has(n);}),hasB=pair.b.some(function(n){return names.has(n);});
    if(hasA&&hasB)ok++;else if(hasA&&!hasB)missing.push(pair.a.find(function(n){return names.has(n);})+'の相手不足');
    else if(!hasA&&hasB)missing.push(pair.b.find(function(n){return names.has(n);})+'の相手不足');
  });
  return {rate:Math.round(ok/SYNTH_PAIRS.length*100),ok:ok,total:SYNTH_PAIRS.length,missing:missing.slice(0,4),healCount:gameState.currentDeck.filter(function(c){return (c.healPower||0)>0;}).length};
}
function getReactionHint(selected){
  var n=selected.map(function(c){return baseName(c.name);});
  if(n.indexOf('酢酸')>=0)return 'ヒント: あと「エタノール」か「NaOH」';
  if(n.indexOf('エタノール')>=0)return 'ヒント: あと「酢酸」「濃硫酸」「Na」「酸化剤」';
  if(n.indexOf('ベンゼン')>=0)return 'ヒント: あと「濃硝酸」「ニトロ基」「濃硫酸」';
  if(n.indexOf('アニリン')>=0)return 'ヒント: あと「ジアゾ化剤」か「無水酢酸」';
  if(n.indexOf('ニトロベンゼン')>=0)return 'ヒント: あと「還元剤」';
  if(n.indexOf('エチレン')>=0)return 'ヒント: あと「ハロゲン」か「重合触媒」';
  if(n.indexOf('水酸化ナトリウム')>=0)return 'ヒント: あと油脂・酢酸・酢酸エチル';
  if(n.indexOf('濃硝酸')>=0)return 'ヒント: あと芳香族';
  if(n.indexOf('重合触媒(Ziegler)')>=0)return 'ヒント: あとエチレン・スチレン';
  if(n.indexOf('無水酢酸')>=0)return 'ヒント: あとアニリンかサリチル酸';
  return 'ヒント: 反応一覧を確認';
}

function recommendDeck(){
  if(!gameState.collection.length){alert('所持なし');return;}
  var owned={};gameState.collection.forEach(function(c){owned[c.name]=(owned[c.name]||0)+1;});
  var used={};function pick(name){if((used[name]||0)>=(owned[name]||0))return false;used[name]=(used[name]||0)+1;return true;}
  function total(){var s=0;for(var k in used)s+=used[k];return s;}
  var MAX=50,healN=0;
  var heals=Object.keys(owned).filter(function(n){var c=gameState.collection.find(function(x){return x.name===n;});return c&&(c.healPower||0)>0;})
    .sort(function(a,b){return (gameState.collection.find(function(x){return x.name===b;}).healPower||0)-(gameState.collection.find(function(x){return x.name===a;}).healPower||0);});
  heals.forEach(function(name){while(healN<8&&total()<MAX&&pick(name))healN++;});
  SYNTH_PAIRS.forEach(function(pair){
    for(var t=0;t<10&&total()<MAX-1;t++){
      var aKey=null,bKey=null,i,k;
      for(i=0;i<pair.a.length;i++){for(k in owned){if(baseName(k)===pair.a[i]&&(used[k]||0)<owned[k]){aKey=k;break;}}if(aKey)break;}
      for(i=0;i<pair.b.length;i++){for(k in owned){if(baseName(k)===pair.b[i]&&(used[k]||0)<owned[k]){bKey=k;break;}}if(bKey)break;}
      if(!aKey||!bKey)break;pick(aKey);pick(bKey);
    }
  });
  Object.keys(owned).sort(function(a,b){return powerValue(gameState.collection.find(function(x){return x.name===b;}))-powerValue(gameState.collection.find(function(x){return x.name===a;}));})
    .forEach(function(name){while(total()<MAX&&pick(name)){}});
  var newDeck=[];for(var name in used){var need=used[name];for(var i=0;i<gameState.collection.length&&need>0;i++){if(gameState.collection[i].name===name){newDeck.push(Object.assign({},gameState.collection[i],{id:uid()}));need--;}}}
  gameState.currentDeck=newDeck;renderDeckEdit();
  var syn=calcSynthRate();alert('おすすめ\n'+newDeck.length+'枚 合成'+syn.rate+'% 回復'+syn.healCount);
}

function startQuizOnly(){qoScore=0;qoTotal=0;document.getElementById('qo-score').innerText='0';document.getElementById('qo-total').innerText='0';document.getElementById('qo-feedback').innerText='';switchState('quizOnly');nextQuizOnly();}
function nextQuizOnly(){
  var q=QUIZ_BANK[Math.floor(Math.random()*QUIZ_BANK.length)];
  document.getElementById('qo-question').innerText=q.q;document.getElementById('qo-feedback').innerText='';
  var box=document.getElementById('qo-options');box.innerHTML='';
  q.opts.map(function(t,i){return{text:t,ok:i===q.ok};}).sort(function(){return Math.random()-0.5;}).forEach(function(c){
    var b=document.createElement('button');b.className='quiz-btn';b.innerText=c.text;
    b.onclick=function(){qoTotal++;if(c.ok){qoScore++;document.getElementById('qo-feedback').innerText='⭕ '+q.ex;}else document.getElementById('qo-feedback').innerText='❌ '+q.ex;
      document.getElementById('qo-score').innerText=qoScore;document.getElementById('qo-total').innerText=qoTotal;for(var i=0;i<box.children.length;i++)box.children[i].disabled=true;};
    box.appendChild(b);
  });
}
function startIsomerMode(){isoScore=0;isoStreak=0;document.getElementById('iso-score').innerText='0';document.getElementById('iso-streak').innerText='0';document.getElementById('iso-feedback').innerText='';switchState('isomer');nextIsomerQ();}
function nextIsomerQ(){
  var q=ISOMER_BANK[Math.floor(Math.random()*ISOMER_BANK.length)];
  document.getElementById('iso-question').innerText=q.q;document.getElementById('iso-feedback').innerText='';
  var box=document.getElementById('iso-options');box.innerHTML='';
  q.opts.map(function(t,i){return{text:t,ok:i===q.ok};}).sort(function(){return Math.random()-0.5;}).forEach(function(c){
    var b=document.createElement('button');b.className='quiz-btn';b.innerText=c.text;
    b.onclick=function(){
      if(c.ok){isoStreak++;var gain=8+Math.min(isoStreak,5)*2;isoScore+=gain;gameState.reagents+=gain;document.getElementById('iso-feedback').innerText='⭕ '+q.ex+' 試薬+'+gain;}
      else{isoStreak=0;document.getElementById('iso-feedback').innerText='❌ '+q.ex;}
      document.getElementById('iso-score').innerText=isoScore;document.getElementById('iso-streak').innerText=isoStreak;
      for(var i=0;i<box.children.length;i++)box.children[i].disabled=true;
    };
    box.appendChild(b);
  });
}

function renderLab(){
  document.getElementById('lab-lv').innerText=gameState.labLevel;
  var next=LAB_THRESH[gameState.labLevel]||(LAB_THRESH[LAB_THRESH.length-1]+100),prev=LAB_THRESH[gameState.labLevel-1]||0;
  document.getElementById('lab-exp').innerText=gameState.labExp;document.getElementById('lab-next').innerText=next;
  document.getElementById('lab-bar').style.width=Math.min(100,Math.floor((gameState.labExp-prev)/Math.max(1,next-prev)*100))+'%';
  var perks=['Lv1 基本','Lv2 撃破試薬+5%','Lv3 無料ガチャ(日1)','Lv4 撃破試薬+10%','Lv5 コンボ追加試薬'],html='';
  for(var i=0;i<perks.length;i++)html+='<div style="opacity:'+(gameState.labLevel>i?1:0.45)+'">'+(gameState.labLevel>i?'✅':'🔒')+' '+perks[i]+'</div>';
  document.getElementById('lab-perks').innerHTML=html;
  var can=gameState.labLevel>=3&&gameState.labFreeDate!==todayStr();
  document.getElementById('lab-free-gacha-btn').disabled=!can;
  document.getElementById('lab-msg').innerText=gameState.labLevel<3?'無料ガチャはLv3から':(gameState.labFreeDate===todayStr()?'今日は使用済':'本日分OK');
}
function labFreeGacha(){if(gameState.labLevel<3||gameState.labFreeDate===todayStr())return;gameState.labFreeDate=todayStr();gameState.reagents+=100;returnToMenu=true;switchState('gacha');drawGacha();}

function renderRefine(){
  var counts={};gameState.collection.forEach(function(c){if(String(c.name).indexOf('精製')===0)return;counts[c.name]=(counts[c.name]||0)+1;});
  var list=document.getElementById('refine-list');list.innerHTML='';
  var keys=Object.keys(counts).sort(function(a,b){return a.localeCompare(b,'ja');});
  if(!keys.length){list.innerHTML='<div style="color:#94a3b8">なし</div>';return;}
  keys.forEach(function(name){
    var n=counts[name],div=document.createElement('div');div.className='deck-item';div.innerHTML='<div>'+name+' ×'+n+'</div>';
    var btn=document.createElement('button');btn.type='button';btn.className='glass-btn mini-btn warn';btn.innerText='精製';btn.disabled=n<3;
    btn.onclick=function(){doRefine(name);};div.appendChild(btn);list.appendChild(div);
  });
}
function doRefine(name){
  var cards=gameState.collection.filter(function(c){return c.name===name;});
  if(cards.length<3){alert('3枚必要');return;}
  var rem=3;gameState.collection=gameState.collection.filter(function(c){if(c.name===name&&rem>0){rem--;return false;}return true;});
  var drem=3;gameState.currentDeck=gameState.currentDeck.filter(function(c){if(c.name===name&&drem>0){drem--;return false;}return true;});
  var base=cards[0];
  gameState.collection.push(Object.assign({},base,{name:'精製'+name,attackPower:base.attackPower===Infinity?Infinity:Math.floor((base.attackPower||0)*1.15),healPower:Math.floor((base.healPower||0)*1.15),id:uid()}));
  gameState.flags.refined=true;checkAchievements();alert('精製完了（反応は通常と同じ）');renderRefine();
}

function createHumanoidMesh(){
  var g=new THREE.Group(),skin=new THREE.MeshLambertMaterial({color:0xffdbac}),body=new THREE.MeshLambertMaterial({color:0x0284c7}),leg=new THREE.MeshLambertMaterial({color:0x1e293b});
  var head=new THREE.Mesh(new THREE.SphereGeometry(0.25,16,16),skin);head.position.y=0.85;g.add(head);
  var torso=new THREE.Mesh(new THREE.CylinderGeometry(0.2,0.15,0.6,12),body);torso.position.y=0.45;g.add(torso);
  var armG=new THREE.CylinderGeometry(0.06,0.06,0.4,8);
  var la=new THREE.Mesh(armG,body);la.position.set(-0.28,0.45,0);g.add(la);var ra=new THREE.Mesh(armG,body);ra.position.set(0.28,0.45,0);g.add(ra);
  var legG=new THREE.CylinderGeometry(0.07,0.07,0.45,8);
  var ll=new THREE.Mesh(legG,leg);ll.position.set(-0.1,0.15,0);g.add(ll);var rl=new THREE.Mesh(legG,leg);rl.position.set(0.1,0.15,0);g.add(rl);return g;
}
function createMoleculeMesh(col){
  var g=new THREE.Group(),m=new THREE.MeshLambertMaterial({color:col}),s=new THREE.MeshLambertMaterial({color:0xffffff});
  g.add(new THREE.Mesh(new THREE.SphereGeometry(0.5,16,16),m));
  [[0.7,0.45,0],[-0.7,0.45,0],[0,-0.65,0.45]].forEach(function(p){var a=new THREE.Mesh(new THREE.SphereGeometry(0.25,12,12),s);a.position.set(p[0],p[1],p[2]);g.add(a);});return g;
}

var scene,camera,renderer,playerNode,monsters=[],targetPlayerPos={x:0,z:0},isThreeInit=false,lastSpawnTime=0;
function initThreeJS(){
  if(isThreeInit)return;isThreeInit=true;
  var cont=document.getElementById('canvas-container');
  scene=new THREE.Scene();scene.background=new THREE.Color(0x87c8f0);scene.fog=new THREE.Fog(0x87c8f0,28,60);
  camera=new THREE.PerspectiveCamera(45,innerWidth/innerHeight,0.1,1000);camera.position.set(0,12,10);camera.rotation.x=-Math.PI/3.2;
  renderer=new THREE.WebGLRenderer({antialias:true});renderer.setSize(innerWidth,innerHeight);renderer.setPixelRatio(Math.min(devicePixelRatio,2));cont.appendChild(renderer.domElement);
  var sun=new THREE.DirectionalLight(0xfff5e6,1.3);sun.position.set(5,12,8);scene.add(sun);scene.add(new THREE.AmbientLight(0xb8d4ff,0.55));
  var floor=new THREE.Mesh(new THREE.PlaneGeometry(120,120),new THREE.MeshLambertMaterial({color:0x3d9e5a}));floor.rotation.x=-Math.PI/2;scene.add(floor);
  playerNode=createHumanoidMesh();scene.add(playerNode);for(var i=0;i<3;i++)spawnMonster();
  var drag=false,lx=0,ly=0;
  window.addEventListener('pointerdown',function(e){drag=true;lx=e.clientX;ly=e.clientY;});
  window.addEventListener('pointermove',function(e){if(!drag)return;targetPlayerPos.x=Math.max(-12,Math.min(12,targetPlayerPos.x+(e.clientX-lx)*0.04));targetPlayerPos.z=Math.max(-18,Math.min(8,targetPlayerPos.z+(e.clientY-ly)*0.04));lx=e.clientX;ly=e.clientY;});
  window.addEventListener('pointerup',function(){drag=false;});
  function anim(t){
    requestAnimationFrame(anim);
    if(t-lastSpawnTime>5000){if(monsters.filter(function(m){return m.isActive;}).length<6)spawnMonster();lastSpawnTime=t;}
    playerNode.position.x+=(targetPlayerPos.x-playerNode.position.x)*0.15;playerNode.position.z+=(targetPlayerPos.z-playerNode.position.z)*0.15;
    camera.position.x=playerNode.position.x;camera.position.z=playerNode.position.z+10;
    var active=document.getElementById('field-screen').classList.contains('active');
    monsters.forEach(function(m){
      if(!m.isActive||!active)return;
      m.mesh.rotation.y+=0.012;m.changeDirTimer--;
      if(m.changeDirTimer<=0){m.vx=(Math.random()-0.5)*0.08;m.vz=(Math.random()-0.5)*0.08;m.changeDirTimer=30+Math.random()*60;}
      m.mesh.position.x+=m.vx;m.mesh.position.z+=m.vz;
      if(Math.abs(m.mesh.position.x)>14)m.vx*=-1;if(m.mesh.position.z<-20||m.mesh.position.z>8)m.vz*=-1;
      var dx=playerNode.position.x-m.mesh.position.x,dz=playerNode.position.z-m.mesh.position.z;
      if(Math.sqrt(dx*dx+dz*dz)<=1){m.isActive=false;scene.remove(m.mesh);gameState.currentMonster=m;startBattle(false);}
    });
    renderer.render(scene,camera);
  }
  anim(0);
}
function spawnMonster(){
  var isBoss=Math.random()<0.12,level,colorHex,hp,atk,name,weakness,condition=null,turnLimit=0;
  if(isBoss){
    level=5;colorHex=0x7c3aed;hp=900+Math.floor(Math.random()*200);atk=28+Math.floor(Math.random()*10);turnLimit=8+Math.floor(Math.random()*5);
    var bosses=[{name:'超高分子ラジカル塊',weakness:['Aromatic','Explosive'],condition:'Aromatic'},{name:'濃縮フリーラジカル核',weakness:['Acid','Oxidant'],condition:'Alcohol'},{name:'芳香族クラスター体',weakness:['Halogen','Reagent'],condition:'Ester'}];
    var b=bosses[Math.floor(Math.random()*bosses.length)];name='【BOSS】'+b.name;weakness=b.weakness;condition=b.condition;
  }else{
    level=1+Math.floor(Math.random()*3);colorHex=level===1?0x22c55e:(level===2?0xf97316:0xef4444);hp=450+level*30;atk=12+level*8;
    name=['アルキル変異体','環状高分子体','フリーラジカル塊'][level-1];
    var pool=['Aromatic','Alkenyl','Acid','Alcohol','Halogen','Oxidant','Phenol','Explosive'];weakness=[pool[Math.floor(Math.random()*pool.length)]];
  }
  var mesh=createMoleculeMesh(colorHex);mesh.position.set((Math.random()-0.5)*18,0.5,-Math.random()*12-2);scene.add(mesh);
  monsters.push({name:name,level:level,hp:hp,maxHP:hp,attackPower:atk,mesh:mesh,isActive:true,weakness:weakness,isBoss:isBoss,condition:condition,turnLimit:turnLimit,vx:0,vz:0,changeDirTimer:0});
}

var labScene,labCamera,labRenderer,enemyMesh;
function initLabThreeJS(){
  var cont=document.getElementById('lab-canvas-container');cont.innerHTML='';
  labScene=new THREE.Scene();labScene.background=new THREE.Color(0x071018);
  labCamera=new THREE.PerspectiveCamera(50,cont.clientWidth/Math.max(1,cont.clientHeight),0.1,100);labCamera.position.set(0,1.6,5.2);labCamera.lookAt(0,0.7,0);
  labRenderer=new THREE.WebGLRenderer({antialias:true});labRenderer.setSize(cont.clientWidth,cont.clientHeight);cont.appendChild(labRenderer.domElement);
  labScene.add(new THREE.DirectionalLight(0x67e8f9,1.5));labScene.add(new THREE.AmbientLight(0xffffff,0.45));
  var col=(gameState.currentMonster&&gameState.currentMonster.isBoss)?0x7c3aed:0x22d3ee;
  enemyMesh=createMoleculeMesh(col);enemyMesh.scale.set(1.4,1.4,1.4);enemyMesh.position.set(0,0.9,0);labScene.add(enemyMesh);
  (function anim(){requestAnimationFrame(anim);if(enemyMesh){enemyMesh.rotation.y+=0.014;enemyMesh.position.y=0.9+Math.sin(Date.now()*0.002)*0.08;}if(labRenderer&&labScene&&labCamera)labRenderer.render(labScene,labCamera);})();
}

function startBattle(practice){
  isPractice=!!practice;returnToMenu=false;
  document.querySelectorAll('.screen').forEach(function(el){el.classList.remove('active');});
  document.getElementById('battle-screen').classList.add('active');
  if(!isPractice)initLabThreeJS();else document.getElementById('lab-canvas-container').innerHTML='<div style="display:flex;align-items:center;justify-content:center;height:100%;color:#67e8f9">練習モード</div>';
  setupBattle();
}
function startPractice(){gameState.currentMonster={name:'練習ダミー',level:1,hp:9999,maxHP:9999,attackPower:0,weakness:[],isBoss:false,condition:null,turnLimit:0};startBattle(true);}
function setupBattle(){
  isBattleOver=false;isProcessing=false;botulinumActive=false;gameState.nextDamageBonus=1.0;pendingIntermediate=null;
  battleHistory=[];battleTurnCount=0;comboCount=0;bossTurnLimit=(gameState.currentMonster&&gameState.currentMonster.turnLimit)||0;
  if(!isPractice)gameState.playerHP=gameState.playerMaxHP;
  document.getElementById('next-bonus').style.display='none';document.getElementById('dot-status').style.display='none';document.getElementById('choice-box').style.display='none';
  document.getElementById('combo-status').innerText='🔗 コンボ: 0';
  var tl=document.getElementById('turn-limit');if(bossTurnLimit>0){tl.style.display='block';tl.innerText='⏱ 残り'+bossTurnLimit;}else tl.style.display='none';
  bDeck=gameState.currentDeck.map(function(c){return Object.assign({},c);}).sort(function(){return Math.random()-0.5;});
  bHand=[];bSelected=[];monsterHP=gameState.currentMonster.hp;
  document.getElementById('monster-name').innerText=gameState.currentMonster.name;
  document.getElementById('monster-level').innerText=gameState.currentMonster.level;
  document.getElementById('monster-maxhp').innerText=gameState.currentMonster.maxHP;
  document.getElementById('monster-hp').innerText=monsterHP;
  document.getElementById('battle-player-hp').innerText=gameState.playerHP;
  var weak=gameState.currentMonster.weakness||[];
  document.getElementById('monster-weak').innerText=weak.length?'弱点: '+weak.join(','):'';
  document.getElementById('monster-cond').innerText=gameState.currentMonster.condition?'条件: '+gameState.currentMonster.condition:'';
  for(var i=0;i<5;i++)drawCard();startPlayerTurn(true);
}
function pushHistory(msg){battleHistory.push(msg);if(battleHistory.length>50)battleHistory.shift();}
function finalizeReplay(){gameState.lastReplay=battleHistory.slice();}
function startPlayerTurn(first){
  if(isBattleOver)return;isPlayerTurn=true;isProcessing=false;if(!first)battleTurnCount++;
  if(bossTurnLimit>0&&!isPractice){
    var left=bossTurnLimit-battleTurnCount;document.getElementById('turn-limit').innerText='⏱ 残り'+Math.max(0,left);
    if(left<=0){isBattleOver=true;document.getElementById('battle-log').innerText='ターン切れ 敗北';pushHistory('ターン切れ');finalizeReplay();setTimeout(function(){gameState.playerHP=gameState.playerMaxHP;switchState('field');},1600);return;}
  }
  if(botulinumActive&&monsterHP>0&&!isPractice){monsterHP-=200;document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);pushHistory('毒素 200');if(monsterHP<=0){winBattle('毒素で分解');return;}}
  if(!first)drawCard();document.getElementById('battle-log').innerText=first?(isPractice?'練習モード':'カードを選んで実行'):'あなたのターン';updateBattleUI();
}
function drawCard(){if(bHand.length<7&&bDeck.length>0)bHand.push(bDeck.shift());}
function updateBattleUI(){
  document.getElementById('battle-deck-count').innerText=bDeck.length;document.getElementById('hand-count').innerText=bHand.length;
  document.getElementById('combo-status').innerText='🔗 コンボ: '+comboCount;
  var cont=document.getElementById('hand-cards');cont.innerHTML='';
  bHand.forEach(function(card){
    var sel=bSelected.some(function(c){return c.id===card.id;});
    var div=document.createElement('div');div.className='card'+(sel?' selected':'');
    var timer=null;
    div.addEventListener('pointerdown',function(e){e.preventDefault();timer=setTimeout(function(){showLongPress(card);timer=null;},450);});
    div.addEventListener('pointerup',function(){if(timer){clearTimeout(timer);timer=null;toggleSelectCard(card);}});
    div.addEventListener('pointerleave',function(){if(timer){clearTimeout(timer);timer=null;}});
    var val='';
    if(baseName(card.name)==='ボツリヌス毒素')val='<div style="font-size:9px;color:#dc2626">DoT200</div>';
    else if((card.attackPower||0)>0&&(card.healPower||0)>0)val='<div style="font-size:9px;color:#dc2626">攻'+fmt(card.attackPower)+'</div><div style="font-size:9px;color:#16a34a">回'+card.healPower+'</div>';
    else if(card.healPower>0)val='<div style="font-size:10px;color:#16a34a">+'+card.healPower+'</div>';
    else val='<div style="font-size:10px;color:#dc2626">'+fmt(card.attackPower)+'</div>';
    div.innerHTML='<div class="card-rarity rarity-'+card.rarity+'">'+card.rarity+'</div><div style="font-size:11px">'+card.name+'</div><div style="font-size:9px;color:#64748b">'+(card.formula||'')+'</div><div class="card-attr">'+card.attribute+'</div>'+val;
    cont.appendChild(div);
  });
  var can=isPlayerTurn&&!isProcessing&&!isBattleOver;
  document.getElementById('attack-btn').disabled=!(can&&bSelected.length>0);
  document.getElementById('skip-btn').disabled=!can;document.getElementById('flee-btn').disabled=!can;
}
function showLongPress(card){
  document.getElementById('lp-title').innerText=card.name;
  var bn=baseName(card.name),body=CARD_REACTIONS[bn]||(card.healPower>0?'回復カード':'単体投擲可');
  if(String(card.name).indexOf('精製')===0)body+='\n（精製: 威力1.15倍・反応は通常名と同じ）';
  document.getElementById('lp-body').innerText=body;document.getElementById('longpress-popup').style.display='block';
}
function closeLongPress(){document.getElementById('longpress-popup').style.display='none';}
function toggleSelectCard(card){if(!isPlayerTurn||isBattleOver||isProcessing)return;var idx=bSelected.findIndex(function(c){return c.id===card.id;});if(idx>=0)bSelected.splice(idx,1);else bSelected.push(card);updateBattleUI();}
function skipTurn(){if(!isPlayerTurn||isBattleOver||isProcessing)return;isProcessing=true;bSelected=[];comboCount=0;document.getElementById('battle-log').innerText='ターン終了';pushHistory('ターン終了');updateBattleUI();setTimeout(endPlayerTurn,700);}
function fleeBattle(){if(!isPlayerTurn||isBattleOver||isProcessing)return;isBattleOver=true;isProcessing=true;document.getElementById('battle-log').innerText=isPractice?'練習終了':'脱出';pushHistory(isPractice?'練習終了':'脱出');finalizeReplay();setTimeout(function(){switchState('field');},1000);}
function winBattle(msg){
  isBattleOver=true;finalizeReplay();
  if(isPractice){document.getElementById('battle-log').innerText='練習終了';setTimeout(function(){switchState('field');},1100);return;}
  gameState.kills++;addLabExp(gameState.currentMonster.isBoss?15:5+comboCount);
  if(gameState.currentMonster.isBoss)gameState.flags.boss=true;if(comboCount>=3)gameState.flags.combo3=true;
  checkRankUp();checkAchievements();
  var rank=getRank(),labBonus=1+(gameState.labLevel>=4?0.1:0)+(gameState.labLevel>=2?0.05:0);
  var reward=Math.floor((55+gameState.currentMonster.level*28)*rank.reagentBonus*labBonus);
  if(gameState.currentMonster.isBoss)reward+=100;if(comboCount>=2&&gameState.labLevel>=5)reward+=10*comboCount;
  gameState.reagents+=reward;document.getElementById('battle-log').innerText=msg+'\n試薬 +'+reward+' / コンボ'+comboCount;pushHistory(msg+' +'+reward);
  setTimeout(function(){switchState('field');},1600);
}

function has(n,name){return n.indexOf(name)>=0;}
function executePlayerAttack(){
  if(isBattleOver||!isPlayerTurn||isProcessing||!bSelected.length)return;
  isProcessing=true;document.getElementById('attack-btn').disabled=true;document.getElementById('skip-btn').disabled=true;document.getElementById('flee-btn').disabled=true;
  var baseDamage=0,baseHeal=0,logMessage='',product=null,appliedEffect=null,isReaction=false;
  /* 精製を外して判定 */
  var n=bSelected.map(function(c){return baseName(c.name);}),unique=[];
  n.forEach(function(x){if(unique.indexOf(x)<0)unique.push(x);});
  var hasCat=has(n,'濃硫酸')||has(n,'重合触媒(Ziegler)')||has(n,'塩化アルミニウム')||has(n,'鉄');
  var catMul=hasCat?2.0:1.5,bossCond=gameState.currentMonster&&gameState.currentMonster.condition;
  function dmgLog(t,d){return t+'\n相手に '+(d===Infinity?'∞':d)+' ダメージ！';}

  if(has(n,'アニリン')&&has(n,'無水酢酸')){product={name:'アセトアニリド',formula:'C6H5NHCOCH3',attackPower:60,healPower:0,attribute:'Aromatic',rarity:'SR'};baseDamage=Math.floor(80*catMul);logMessage=dmgLog('アセチル化',baseDamage);markFlag('acetyl');isReaction=true;}
  else if(has(n,'サリチル酸')&&has(n,'無水酢酸')){product={name:'アセチルサリチル酸',formula:'C9H8O4',attackPower:120,healPower:0,attribute:'Ester',rarity:'SSR'};baseDamage=Math.floor(120*catMul);logMessage=dmgLog('アセチル化',baseDamage);markFlag('acetyl');isReaction=true;}
  else if(has(n,'エタノール')&&has(n,'濃硫酸')){baseDamage=Math.floor(100*catMul);logMessage=dmgLog('脱水→エチレン',baseDamage);markFlag('dehyd');isReaction=true;}
  else if(has(n,'1-プロパノール')&&has(n,'濃硫酸')){baseDamage=Math.floor(105*catMul);logMessage=dmgLog('脱水→プロピレン',baseDamage);markFlag('dehyd');isReaction=true;}
  else if(has(n,'ベンゼン')&&has(n,'ニトロ基')){product={name:'ニトロベンゼン',formula:'C6H5NO2',attackPower:70,healPower:0,attribute:'Aromatic',rarity:'SR'};baseDamage=Math.floor(70*catMul);logMessage=dmgLog('→ニトロベンゼン',baseDamage);markFlag('nitro');isReaction=true;}
  else if(has(n,'ニトロベンゼン')&&(has(n,'還元剤')||has(n,'水素化ホウ素ナトリウム'))){product={name:'アニリン',formula:'C6H5NH2',attackPower:65,healPower:0,attribute:'Aromatic',rarity:'SR'};baseDamage=Math.floor(65*catMul);logMessage=dmgLog('還元→アニリン',baseDamage);isReaction=true;}
  else if(has(n,'アニリン')&&has(n,'ジアゾ化剤')){product={name:'アゾベンゼン',formula:'C6H5N=NC6H5',attackPower:110,healPower:0,attribute:'Aromatic',rarity:'SSR'};baseDamage=Math.floor(110*catMul);logMessage=dmgLog('→アゾベンゼン',baseDamage);isReaction=true;}
  else if(has(n,'酢酸')&&has(n,'エタノール')){product={name:'酢酸エチル',formula:'CH3COOC2H5',attackPower:Math.floor(55*catMul),healPower:0,attribute:'Ester',rarity:'R'};baseDamage=Math.floor(55*catMul);logMessage=dmgLog('エステル化',baseDamage);markFlag('ester');isReaction=true;}
  else if(bSelected.length===1&&baseName(bSelected[0].name)==='ボツリヌス毒素'){botulinumActive=true;document.getElementById('dot-status').style.display='block';logMessage='毒素散布';baseDamage=0;}
  else if(bSelected.length===1&&baseName(bSelected[0].name)==='フッ化水素酸'){
    if(Math.random()<0.1){isBattleOver=true;document.getElementById('battle-log').innerText='HFが自分に！敗北 試薬-25';gameState.reagents=Math.max(0,gameState.reagents-25);finalizeReplay();bHand=bHand.filter(function(c){return !bSelected.some(function(s){return s.id===c.id;});});bSelected=[];updateBattleUI();setTimeout(function(){gameState.playerHP=gameState.playerMaxHP;switchState('field');},1800);return;}
    baseDamage=Infinity;logMessage=dmgLog('HF',Infinity);
  }
  else if(bSelected.length===1&&(baseName(bSelected[0].name)==='トリニトロトルエン'||baseName(bSelected[0].name)==='ピクリン酸')){baseDamage=bSelected[0].attackPower||180;logMessage=dmgLog(bSelected[0].name,baseDamage);}
  else if(has(n,'水酸化ナトリウム')&&(has(n,'トリパルミチン')||has(n,'トリステアリン')||has(n,'トリオレイン'))){baseDamage=Math.floor(230*catMul);appliedEffect='sapon';logMessage=dmgLog('油脂けん化',baseDamage);markFlag('sapon');markFlag('fat');isReaction=true;}
  else if(has(n,'水酸化ナトリウム')&&(has(n,'酢酸')||has(n,'酢酸エチル')||has(n,'オレイン酸'))){baseDamage=Math.floor(210*catMul);appliedEffect='sapon';logMessage=dmgLog('けん化',baseDamage);markFlag('sapon');isReaction=true;}
  else if(has(n,'ベンゼン')&&has(n,'濃硝酸')){baseDamage=Math.floor(130*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;}
  else if(has(n,'トルエン')&&has(n,'濃硝酸')){baseDamage=Math.floor(220*catMul);logMessage=dmgLog('トルエンニトロ化',baseDamage);markFlag('nitro');isReaction=true;}
  else if(has(n,'フェノール')&&has(n,'濃硝酸')){baseDamage=Math.floor(150*catMul);logMessage=dmgLog('フェノールニトロ化',baseDamage);markFlag('nitro');isReaction=true;}
  else if(has(n,'ベンゼン')&&has(n,'濃硫酸')){baseDamage=Math.floor(150*catMul);logMessage=dmgLog('スルホン化',baseDamage);isReaction=true;}
  else if(has(n,'ナフタレン')&&has(n,'濃硫酸')){baseDamage=Math.floor(160*catMul);logMessage=dmgLog('スルホン化',baseDamage);isReaction=true;}
  else if(has(n,'ベンゼン')&&(has(n,'塩素')||has(n,'臭素'))&&(has(n,'鉄')||has(n,'塩化アルミニウム')||hasCat)){baseDamage=Math.floor(140*catMul);logMessage=dmgLog('ハロゲン化',baseDamage);isReaction=true;}
  else if(has(n,'エチレン')&&(has(n,'臭素')||has(n,'塩素'))){baseDamage=Math.floor(140*catMul);logMessage=dmgLog('付加',baseDamage);isReaction=true;}
  else if(has(n,'アセチレン')&&has(n,'臭素')){baseDamage=Math.floor(160*catMul);logMessage=dmgLog('付加',baseDamage);isReaction=true;}
  else if(has(n,'シス-2-ブテン')&&has(n,'臭素')){baseDamage=Math.floor(130*catMul);logMessage=dmgLog('シス付加',baseDamage);isReaction=true;}
  else if(has(n,'トランス-2-ブテン')&&has(n,'臭素')){baseDamage=Math.floor(130*catMul);logMessage=dmgLog('トランス付加',baseDamage);isReaction=true;}
  else if(has(n,'エチレン')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(300*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;}
  else if(has(n,'スチレン')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(250*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;}
  else if(has(n,'プロピレン')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(260*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;}
  else if(has(n,'ビニル基')&&has(n,'重合触媒(Ziegler)')){baseDamage=Math.floor(220*catMul);logMessage=dmgLog('重合',baseDamage);markFlag('poly');isReaction=true;}
  else if((has(n,'エタノール')||has(n,'アセトアルデヒド')||has(n,'メタノール'))&&(has(n,'過マンガン酸カリウム')||has(n,'二クロム酸カリウム'))){baseDamage=Math.floor(170*catMul);appliedEffect='oxid';logMessage=dmgLog('酸化',baseDamage);markFlag('oxid');isReaction=true;}
  else if(has(n,'2-プロパノール')&&(has(n,'過マンガン酸カリウム')||has(n,'二クロム酸カリウム'))){baseDamage=Math.floor(160*catMul);logMessage=dmgLog('第二級酸化',baseDamage);markFlag('oxid');isReaction=true;}
  else if(has(n,'トルエン')&&has(n,'過マンガン酸カリウム')){baseDamage=Math.floor(190*catMul);logMessage=dmgLog('側鎖酸化',baseDamage);markFlag('oxid');isReaction=true;}
  else if((has(n,'エタノール')||has(n,'メタノール')||has(n,'1-プロパノール'))&&has(n,'金属ナトリウム')){baseDamage=Math.floor(120*catMul);logMessage=dmgLog('アルコキシド',baseDamage);isReaction=true;}
  else if(has(n,'フェノール')&&has(n,'金属ナトリウム')){baseDamage=Math.floor(140*catMul);logMessage=dmgLog('フェノキシド',baseDamage);isReaction=true;}
  else if((has(n,'o-クレゾール')||has(n,'m-クレゾール')||has(n,'p-クレゾール'))&&has(n,'金属ナトリウム')){baseDamage=Math.floor(135*catMul);logMessage=dmgLog('クレゾール+Na',baseDamage);isReaction=true;}
  else if(has(n,'ナフタレン')&&has(n,'濃硝酸')){baseDamage=Math.floor(170*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;}
  else if(has(n,'アントラセン')&&has(n,'濃硝酸')){baseDamage=Math.floor(200*catMul);logMessage=dmgLog('ニトロ化',baseDamage);markFlag('nitro');isReaction=true;}
  else if(has(n,'メチル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(50*catMul);logMessage=dmgLog('メタノール生成',baseDamage);isReaction=true;}
  else if(has(n,'エチル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(60*catMul);logMessage=dmgLog('エタノール生成',baseDamage);isReaction=true;}
  else if(has(n,'フェニル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(90*catMul);logMessage=dmgLog('フェノール生成',baseDamage);isReaction=true;}
  else if(has(n,'フェニル基')&&has(n,'ニトロ基')){baseDamage=Math.floor(110*catMul);logMessage=dmgLog('ニトロベンゼン生成',baseDamage);isReaction=true;}
  else if(has(n,'フェニル基')&&has(n,'カルボキシ基')){baseDamage=Math.floor(100*catMul);logMessage=dmgLog('安息香酸生成',baseDamage);isReaction=true;}
  else if(has(n,'フェニル基')&&has(n,'アミノ基')){baseDamage=Math.floor(75*catMul);logMessage=dmgLog('アニリン生成',baseDamage);isReaction=true;}
  else if(has(n,'ビニル基')&&has(n,'ヒドロキシ基')){baseDamage=Math.floor(70*catMul);logMessage=dmgLog('ビニルアルコール生成',baseDamage);isReaction=true;}
  else if(unique.length===1){
    var s=bSelected[0],cnt=bSelected.length;
    if(baseName(s.name)==='ボツリヌス毒素'){botulinumActive=true;document.getElementById('dot-status').style.display='block';logMessage='毒素';baseDamage=0;}
    else if(baseName(s.name)==='フッ化水素酸'){baseDamage=Infinity;logMessage=dmgLog('HF',Infinity);}
    else{baseDamage=s.attackPower===Infinity?Infinity:(s.attackPower||0)*cnt;baseHeal=(s.healPower||0)*cnt;
      if(baseDamage>0&&baseHeal>0)logMessage=s.name+'×'+cnt+'\nダメージ '+fmt(baseDamage)+'\n回復 '+baseHeal;
      else if(baseHeal>0)logMessage=s.name+'×'+cnt+'\n回復 '+baseHeal;
      else logMessage=s.name+'×'+cnt+' 投擲\n相手に '+fmt(baseDamage)+' ダメージ！';}
  }
  else if(bSelected.length===1){
    var s1=bSelected[0];baseDamage=s1.attackPower||0;baseHeal=s1.healPower||0;
    if(baseDamage>0&&baseHeal>0)logMessage=s1.name+'\nダメージ '+fmt(baseDamage)+'\n回復 '+baseHeal;
    else if(baseHeal>0)logMessage=s1.name+'\n回復 '+baseHeal;
    else logMessage=s1.name+' を投擲！\n相手に '+fmt(baseDamage)+' ダメージ！';
  }
  else{
    var healSum=bSelected.reduce(function(a,c){return a+(c.healPower||0);},0);
    var atkSum=bSelected.reduce(function(a,c){return a+(c.attackPower===Infinity?0:(c.attackPower||0));},0);
    if(healSum>0&&atkSum===0){baseHeal=healSum;logMessage='複合回復 +'+healSum;}
    else{comboCount=0;logMessage='不活性な組み合わせ\n'+getReactionHint(bSelected);}
  }

  if(isReaction){comboCount++;if(comboCount>=3)gameState.flags.combo3=true;var comboMul=1+Math.min(comboCount,8)*0.05;if(baseDamage!==Infinity&&baseDamage>0)baseDamage=Math.floor(baseDamage*comboMul);logMessage+='\n🔗 コンボ×'+comboCount;}
  if(bossCond&&baseDamage>0&&baseDamage!==Infinity&&!isPractice){
    var attrs=bSelected.map(function(c){return c.attribute;});
    var ok=attrs.indexOf(bossCond)>=0||(product&&product.attribute===bossCond);
    if(bossCond==='Ester'&&has(n,'酢酸')&&has(n,'エタノール'))ok=true;
    if(bossCond==='Alcohol'&&(has(n,'エタノール')||has(n,'メタノール')||has(n,'ヒドロキシ基')))ok=true;
    if(!ok){baseDamage=0;logMessage+='\nボス条件未達';}
  }
  var weakMul=1;
  if(gameState.currentMonster&&gameState.currentMonster.weakness){
    var attrs2=bSelected.map(function(c){return c.attribute;});
    if(attrs2.some(function(a){return gameState.currentMonster.weakness.indexOf(a)>=0;}))weakMul=1.5;
  }
  var finalD=baseDamage;
  if(finalD!==Infinity&&finalD>0)finalD=Math.floor(finalD*gameState.nextDamageBonus*weakMul);
  if(appliedEffect==='oxid'){gameState.nextDamageBonus=1.3;document.getElementById('next-bonus').style.display='block';document.getElementById('next-bonus').innerText='次ターン+30%';}
  else if(appliedEffect==='sapon'){gameState.nextDamageBonus=1.2;document.getElementById('next-bonus').style.display='block';document.getElementById('next-bonus').innerText='次ターン+20%';}
  else if(baseDamage>0||baseHeal>0){gameState.nextDamageBonus=1.0;document.getElementById('next-bonus').style.display='none';}

  bHand=bHand.filter(function(c){return !bSelected.some(function(s){return s.id===c.id;});});bSelected=[];
  if(product){
    pendingIntermediate={card:Object.assign({},product,{id:uid()}),damage:finalD,heal:baseHeal,msg:logMessage,weak:weakMul>1};
    document.getElementById('choice-title').innerText=product.name+' 生成';
    document.getElementById('choice-desc').innerText='攻撃力 '+product.attackPower+' / 手札で連鎖可';
    document.getElementById('choice-box').style.display='flex';updateBattleUI();return;
  }
  applyEffectAndEndTurn(finalD,baseHeal,logMessage,weakMul>1);
}
function chooseAttack(){document.getElementById('choice-box').style.display='none';if(!pendingIntermediate)return;var p=pendingIntermediate;applyEffectAndEndTurn(p.damage,p.heal,p.msg+(p.weak?'\n弱点！':''),p.weak);pendingIntermediate=null;}
function chooseAddToHand(){
  document.getElementById('choice-box').style.display='none';if(!pendingIntermediate)return;
  if(bHand.length<7)bHand.push(pendingIntermediate.card);
  gameState.collection.push(Object.assign({},pendingIntermediate.card));
  document.getElementById('battle-log').innerText=pendingIntermediate.card.name+' を手札に';pushHistory(pendingIntermediate.card.name+'手札');
  pendingIntermediate=null;isProcessing=false;updateBattleUI();setTimeout(endPlayerTurn,1100);
}
function applyEffectAndEndTurn(damage,heal,message,isWeak){
  if(isBattleOver)return;
  if(damage===Infinity||damage>=400){if(gameState.reagents>=25){gameState.reagents-=25;message+='\n試薬25消費';}else if(damage!==Infinity){damage=Math.floor(damage*0.5);message+='\n試薬不足で半減';}}
  if(isWeak)message+='\n弱点！';
  if(damage===Infinity)monsterHP=0;else if(damage>0)monsterHP-=damage;
  if(heal>0){gameState.playerHP=Math.min(gameState.playerMaxHP,gameState.playerHP+heal);document.getElementById('battle-player-hp').innerText=gameState.playerHP;}
  document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);document.getElementById('battle-log').innerText=message;
  document.getElementById('combo-status').innerText='🔗 コンボ: '+comboCount;pushHistory(message);
  if(monsterHP<=0)winBattle(isPractice?'練習クリア':'敵を分解！');else setTimeout(endPlayerTurn,1400);
}
function endPlayerTurn(){
  if(isBattleOver)return;if(isPractice){startPlayerTurn(false);return;}
  isPlayerTurn=false;isProcessing=true;document.getElementById('battle-log').innerText='敵の攻撃…';updateBattleUI();
  setTimeout(function(){
    if(isBattleOver)return;
    if(monsterHP>0){
      var atk=gameState.currentMonster.attackPower||15;
      if(bossTurnLimit>0&&battleTurnCount>=bossTurnLimit-2)atk=Math.floor(atk*1.5);
      gameState.playerHP-=atk;document.getElementById('battle-player-hp').innerText=Math.max(0,gameState.playerHP);
      var msg='敵の攻撃\nあなたに '+atk+' ダメージ！';document.getElementById('battle-log').innerText=msg;pushHistory(msg);
      if(gameState.playerHP<=0){isBattleOver=true;gameState.playerHP=0;gameState.reagents=Math.max(0,gameState.reagents-25);document.getElementById('battle-log').innerText='敗北 試薬-25';finalizeReplay();setTimeout(function(){gameState.playerHP=gameState.playerMaxHP;switchState('field');},1400);return;}
      setTimeout(function(){if(!isBattleOver)startPlayerTurn(false);},1100);
    }else if(!isBattleOver)startPlayerTurn(false);
  },800);
}

function sortDeck(mode){
  var names=[],seen={};gameState.collection.forEach(function(c){if(!seen[c.name]){seen[c.name]=1;names.push(c.name);}});
  function rep(name){return gameState.collection.find(function(c){return c.name===name;})||ALL_CARDS.find(function(c){return c.name===baseName(name);});}
  names.sort(function(a,b){
    var ca=rep(a),cb=rep(b);if(!ca||!cb)return 0;
    if(mode==='name')return a.localeCompare(b,'ja');
    if(mode==='rarity'){var d=(RARITY_ORDER[ca.rarity]||9)-(RARITY_ORDER[cb.rarity]||9);return d||a.localeCompare(b,'ja');}
    if(mode==='power'){var d2=powerValue(cb)-powerValue(ca);return d2||a.localeCompare(b,'ja');}
    return a.localeCompare(b,'ja');
  });
  gameState.deckListOrder=names.slice();
  var rebuilt=[];names.forEach(function(name){gameState.currentDeck.filter(function(c){return c.name===name;}).forEach(function(c){rebuilt.push(c);});});
  gameState.currentDeck=rebuilt;renderDeckEdit();
}
function renderDeckEdit(){
  document.getElementById('deck-count').innerText=gameState.currentDeck.length;
  document.getElementById('deck-reaction-list').innerText=FULL_REACTION_TEXT;
  for(var i=0;i<3;i++){var inp=document.getElementById('preset-name-'+i);if(inp&&gameState.deckSlots[i])inp.value=gameState.deckSlots[i].name||'';}
  document.getElementById('preset-labels').innerText=[0,1,2].map(function(i){var s=gameState.deckSlots[i];return (s&&s.cards&&s.cards.length)?('S'+(i+1)+':'+(s.name||'無題')+'('+s.cards.length+')'):('S'+(i+1)+':空');}).join(' / ');
  var syn=calcSynthRate();
  document.getElementById('synth-rate-text').innerText=syn.rate+'%（'+syn.ok+'/'+syn.total+'）回復'+syn.healCount;
  document.getElementById('synth-rate-bar').style.width=syn.rate+'%';
  document.getElementById('synth-hint').innerText=syn.missing.length?'不足: '+syn.missing.join(' / '):(syn.rate>=50?'充実':'基質と試薬をバランスよく');
  var allNames=[],seen={};gameState.collection.forEach(function(c){if(!seen[c.name]){seen[c.name]=1;allNames.push(c.name);}});
  var ordered;
  if(gameState.deckListOrder&&gameState.deckListOrder.length){ordered=gameState.deckListOrder.filter(function(n){return seen[n];});allNames.filter(function(n){return ordered.indexOf(n)<0;}).sort(function(a,b){return a.localeCompare(b,'ja');}).forEach(function(n){ordered.push(n);});}
  else ordered=allNames.sort(function(a,b){return a.localeCompare(b,'ja');});
  var list=document.getElementById('deck-list');list.innerHTML='';
  ordered.forEach(function(name){
    var owned=gameState.collection.filter(function(c){return c.name===name;}).length;
    var inD=gameState.currentDeck.filter(function(c){return c.name===name;}).length;
    var card=gameState.collection.find(function(c){return c.name===name;});if(!card)return;
    var val;if(baseName(name)==='ボツリヌス毒素')val='DoT200';else if((card.attackPower||0)>0&&(card.healPower||0)>0)val='攻'+fmt(card.attackPower)+'/回'+card.healPower;else if(card.healPower>0)val='HEAL+'+card.healPower;else val='PWR '+fmt(card.attackPower);
    var div=document.createElement('div');div.className='deck-item'+(inD>0?' in-deck':'');
    var left=document.createElement('div');
    left.innerHTML='<span class="card-rarity rarity-'+card.rarity+'">'+card.rarity+'</span> <span style="color:'+(inD>0?'#4ade80':'#e2e8f0')+'">'+name+' ['+inD+'/'+owned+']</span><div style="font-size:9px;color:#94a3b8">'+val+' · '+card.attribute+'</div>';
    var right=document.createElement('div');
    if(inD>0){var rm=document.createElement('button');rm.type='button';rm.className='action-btn';rm.style.color='#f87171';rm.innerText='➖';rm.onclick=function(){removeFromDeck(name);};right.appendChild(rm);}
    var add=document.createElement('button');add.type='button';add.className='action-btn';add.style.color=(inD<owned&&gameState.currentDeck.length<50)?'#38bdf8':'#475569';add.innerText='➕';
    add.disabled=!(inD<owned&&gameState.currentDeck.length<50);add.onclick=function(){addToDeck(name);};right.appendChild(add);
    div.appendChild(left);div.appendChild(right);list.appendChild(div);
  });
  var btn=document.getElementById('deck-done-btn');btn.disabled=gameState.currentDeck.length<20;btn.style.opacity=gameState.currentDeck.length>=20?'1':'0.45';
}
function addToDeck(name){var owned=gameState.collection.filter(function(c){return c.name===name;}).length;var inD=gameState.currentDeck.filter(function(c){return c.name===name;}).length;var card=gameState.collection.find(function(c){return c.name===name;});if(card&&gameState.currentDeck.length<50&&inD<owned){gameState.currentDeck.push(Object.assign({},card,{id:uid()}));renderDeckEdit();}}
function removeFromDeck(name){var i=gameState.currentDeck.findIndex(function(c){return c.name===name;});if(i>=0){gameState.currentDeck.splice(i,1);renderDeckEdit();}}

function drawGacha(){
  if(gameState.reagents<100){alert('試薬不足');return;}
  gameState.reagents-=100;var gr=document.getElementById('gacha-reagents');if(gr)gr.innerText=gameState.reagents;
  var boost=getRank().gachaBoost,rand=Math.random()*100,rarity;
  if(rand<0.1+boost*0.15)rarity='SSSR';else if(rand<0.1+2.9+boost)rarity='SSR';else if(rand<0.1+2.9+15+boost*2)rarity='SR';else rarity='R';
  var cands=ALL_CARDS.filter(function(c){return c.rarity===rarity;});if(!cands.length)cands=ALL_CARDS.filter(function(c){return c.rarity==='R';});
  var pulled=cands[Math.floor(Math.random()*cands.length)];
  var newCard=Object.assign({},pulled,{id:uid()});gameState.collection.push(newCard);saveGame(true);checkAchievements();
  var val;if(newCard.name==='ボツリヌス毒素')val='DoT200';else if((newCard.attackPower||0)>0&&(newCard.healPower||0)>0)val='攻'+fmt(newCard.attackPower)+'/回'+newCard.healPower;else if(newCard.healPower>0)val='HEAL+'+newCard.healPower;else val='PWR '+fmt(newCard.attackPower);
  document.getElementById('gacha-result').innerHTML='<span class="card-rarity rarity-'+newCard.rarity+'">'+newCard.rarity+'</span><div style="font-size:16px;margin:6px 0">'+newCard.name+'</div><div style="font-size:11px;color:#cbd5e1">'+newCard.formula+'</div><div style="font-size:11px;color:#fbbf24;margin-top:4px">'+val+' · '+newCard.attribute+'</div>';
}

initDaily();
</script>
</body>
</html>
