<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>有機化学バトルフィールド</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0;user-select:none;-webkit-tap-highlight-color:transparent;
  font-family:"Hiragino Sans","Hiragino Kaku Gothic ProN","Noto Sans JP",-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;
  font-weight:400}
body,html{width:100%;height:100%;overflow:hidden;background:#05080f;color:#e8eef7}
.screen{display:none;width:100%;height:100%;position:absolute;top:0;left:0}
.active{display:flex;flex-direction:column}
.glass-btn{
  background:linear-gradient(145deg,rgba(56,189,248,.25),rgba(99,102,241,.35));
  border:1px solid rgba(148,163,184,.35); color:#f1f5f9;
  padding:10px 16px; font-weight:400; font-size:13px; border-radius:12px; cursor:pointer;
  box-shadow:0 4px 16px rgba(0,0,0,.35), inset 0 1px 0 rgba(255,255,255,.12);
  backdrop-filter:blur(8px);
}
.glass-btn:active{transform:scale(.96)}
.glass-btn:disabled{opacity:.4;cursor:not-allowed}
.glass-btn.primary{background:linear-gradient(145deg,#0ea5e9,#6366f1);border-color:rgba(125,211,252,.5)}
.glass-btn.danger{background:linear-gradient(145deg,#ef4444,#b91c1c);border-color:rgba(252,165,165,.4)}
.glass-btn.success{background:linear-gradient(145deg,#10b981,#059669);border-color:rgba(110,231,183,.4)}
.glass-btn.warn{background:linear-gradient(145deg,#f59e0b,#d97706);border-color:rgba(252,211,77,.4)}
.glass-btn.pink{background:linear-gradient(145deg,#ec4899,#a855f7);border-color:rgba(244,114,182,.4)}
.glass-btn.slate{background:linear-gradient(145deg,#475569,#334155);border-color:rgba(148,163,184,.3)}
.glass-btn.orange{background:linear-gradient(145deg,#ea580c,#ef4444);border-color:rgba(253,186,116,.5)}

#deck-select-screen{
  background:radial-gradient(ellipse at 30% 20%,#1e3a5f 0%,#0b1220 45%,#05080f 100%);
  padding:36px 20px; align-items:center; justify-content:flex-start; gap:18px; text-align:center;
}
#deck-select-screen h2{
  font-size:22px; letter-spacing:.04em; font-weight:400;
  background:linear-gradient(90deg,#7dd3fc,#a5b4fc,#c4b5fd);
  -webkit-background-clip:text; -webkit-text-fill-color:transparent;
}
.select-card{
  border-radius:18px; padding:16px 18px; margin-bottom:14px; text-align:left; cursor:pointer;
  width:100%; max-width:400px; border:1px solid rgba(255,255,255,.12);
  box-shadow:0 8px 28px rgba(0,0,0,.4), inset 0 1px 0 rgba(255,255,255,.15);
}
.select-card:active{transform:scale(.98)}
.select-card.purple{background:linear-gradient(135deg,#5b21b6,#1d4ed8)}
.select-card.red{background:linear-gradient(135deg,#c2410c,#b91c1c)}
.select-card.green{background:linear-gradient(135deg,#047857,#0f766e)}
.badge{display:inline-block;background:rgba(255,255,255,.18);font-size:10px;padding:3px 8px;border-radius:999px}

#field-screen{position:relative;width:100%;height:100%}
#canvas-container{width:100%;height:100%}
.field-ui{
  position:absolute; top:0; left:0; width:100%; padding:36px 14px 0;
  display:flex; justify-content:space-between; pointer-events:none; z-index:5; gap:10px;
}
.field-ui *{pointer-events:auto}
.status-box{
  background:rgba(8,12,22,.72); padding:12px 14px; border-radius:14px; font-size:13px;
  border:1px solid rgba(148,163,184,.25); backdrop-filter:blur(12px);
  box-shadow:0 8px 24px rgba(0,0,0,.35); min-width:150px;
}
.field-btns{display:flex;gap:6px;flex-wrap:wrap;justify-content:flex-end;max-width:230px}
.mini-btn{padding:8px 11px;font-size:11px}

#battle-screen{
  background:radial-gradient(ellipse at 50% 0%,#1e293b 0%,#0f172a 40%,#020617 100%);
  padding:14px 12px 12px; justify-content:space-between;
}
.battle-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:6px}
#lab-canvas-container{
  width:100%; height:158px; border-radius:16px; overflow:hidden; position:relative;
  border:1px solid rgba(56,189,248,.35);
  box-shadow:0 0 24px rgba(14,165,233,.15), inset 0 0 40px rgba(14,165,233,.06);
  background:linear-gradient(180deg,#0c1a2e,#071018);
}
.battle-log-box{
  background:rgba(15,23,42,.88); border:1px solid rgba(71,85,105,.6); border-radius:14px;
  padding:11px 12px; min-height:54px; font-size:12px; text-align:center;
  display:flex; align-items:center; justify-content:center; white-space:pre-line; margin:6px 0;
}
.quiz-box{
  background:rgba(88,28,135,.45); border:1px solid rgba(192,132,252,.5); border-radius:14px;
  padding:12px; text-align:center; display:flex; flex-direction:column; gap:8px;
}
.quiz-options{display:grid;grid-template-columns:1fr 1fr;gap:6px}
.quiz-btn{
  background:linear-gradient(145deg,rgba(37,99,235,.9),rgba(67,56,202,.9));
  border:1px solid rgba(147,197,253,.35); color:#fff; padding:9px; border-radius:10px;
  font-size:11px; cursor:pointer;
}
.hand-container{overflow-x:auto;display:flex;gap:8px;padding:6px 2px 4px}
.card{
  min-width:86px; width:86px; height:116px; border-radius:12px; padding:6px;
  display:flex; flex-direction:column; justify-content:space-between; cursor:pointer;
  background:linear-gradient(160deg,#ffffff 0%,#f1f5f9 100%); color:#0f172a;
  box-shadow:0 6px 16px rgba(0,0,0,.35);
}
.card.selected{
  background:linear-gradient(160deg,#fef08a,#fde047);
  box-shadow:0 0 0 2px #facc15, 0 8px 20px rgba(250,204,21,.35);
  transform:translateY(-6px);
}
.card-rarity{font-size:8px;padding:2px 5px;border-radius:4px;color:#fff;width:fit-content}
.rarity-SSR{background:linear-gradient(90deg,#f97316,#ea580c)}
.rarity-SR{background:linear-gradient(90deg,#a855f7,#7c3aed)}
.rarity-R{background:linear-gradient(90deg,#3b82f6,#2563eb)}
.rarity-SSSR{background:linear-gradient(90deg,#ff006e,#8338ec,#3a86ff);animation:rainbow 2s linear infinite;background-size:200% 100%}
.card-attr{font-size:8px;color:#64748b}
@keyframes rainbow{0%{background-position:0% 50%}100%{background-position:200% 50%}}

#deck-edit-screen{background:#0a0f1a;padding:32px 14px 10px;height:100%;overflow:hidden}
.deck-list{flex:1;overflow-y:auto;margin-top:8px;max-height:42vh}
.deck-item{
  display:flex; justify-content:space-between; align-items:center;
  background:rgba(30,41,59,.85); padding:9px 11px; margin-bottom:6px; border-radius:11px;
  border:1px solid rgba(71,85,105,.4);
}
.deck-item.in-deck{background:rgba(16,185,129,.12); border-color:rgba(52,211,153,.35)}
.action-btn{background:none;border:none;font-size:17px;cursor:pointer;padding:4px}
.info-box{
  background:rgba(15,23,42,.9); border:1px solid rgba(71,85,105,.5); border-radius:12px;
  padding:10px; margin-top:8px; overflow-y:auto; font-size:11px; line-height:1.5;
}
.info-title{color:#fbbf24;margin-bottom:6px;font-size:12px}
.synth-bar-wrap{background:rgba(30,41,59,.9);border-radius:10px;padding:10px 12px;margin:8px 0;border:1px solid rgba(56,189,248,.25)}
.synth-bar-bg{height:8px;background:#1e293b;border-radius:999px;overflow:hidden;margin-top:6px}
.synth-bar-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,#22d3ee,#818cf8);transition:width .3s}

#gacha-screen{
  background:radial-gradient(ellipse at 50% 0%,#2e1065 0%,#0f0520 50%,#05080f 100%);
  padding:28px 14px 18px; align-items:center; gap:12px; overflow-y:auto;
}
.gacha-card-view{
  width:240px; height:180px; border-radius:16px; border:1px solid rgba(168,85,247,.45);
  background:linear-gradient(160deg,rgba(88,28,135,.35),rgba(15,23,42,.8));
  display:flex; flex-direction:column; align-items:center; justify-content:center;
  text-align:center; padding:12px;
  box-shadow:0 0 32px rgba(168,85,247,.2);
}
.battle-actions{display:flex;gap:6px;justify-content:center;margin-top:6px;flex-wrap:wrap}
.choice-box{
  background:rgba(15,23,42,.96); border:1px solid rgba(250,204,21,.55); border-radius:16px;
  padding:16px; text-align:center; display:none; flex-direction:column; gap:10px;
  position:absolute; left:50%; top:38%; transform:translate(-50%,-50%); width:86%; max-width:320px; z-index:50;
  box-shadow:0 20px 50px rgba(0,0,0,.55);
}
#reaction-list-screen,#zukan-screen,#achieve-screen,#history-screen{
  background:linear-gradient(180deg,#0f172a,#020617); padding:24px 14px 18px; overflow:hidden;
}
.scroll-panel{
  flex:1; overflow-y:auto; background:rgba(15,23,42,.85); border:1px solid rgba(71,85,105,.45);
  border-radius:14px; padding:12px; font-size:12px; line-height:1.55; color:#cbd5e1; margin:8px 0;
}
.zukan-item{
  background:rgba(30,41,59,.8); border-radius:12px; padding:11px; margin-bottom:8px;
  border:1px solid rgba(71,85,105,.35); border-left:3px solid #38bdf8;
}
.achieve-item{
  background:rgba(30,41,59,.8); border-radius:12px; padding:11px; margin-bottom:8px;
  display:flex; justify-content:space-between; align-items:center; border:1px solid rgba(71,85,105,.35);
}
.achieve-item.done{border-left:3px solid #22c55e}
.achieve-item.locked{opacity:.55;border-left:3px solid #64748b}
.longpress-popup{
  display:none; position:fixed; left:50%; top:50%; transform:translate(-50%,-50%);
  width:88%; max-width:340px; background:rgba(15,23,42,.97); border:1px solid rgba(56,189,248,.5);
  border-radius:16px; padding:16px; z-index:100; max-height:60vh; overflow-y:auto;
  box-shadow:0 24px 60px rgba(0,0,0,.6);
}
</style>
</head>
<body>

<div id="deck-select-screen" class="screen active">
  <h2>有機化学バトルフィールド</h2>
  <p style="font-size:13px;color:#94a3b8">初期スターターデッキを選択してください</p>
  <div style="width:100%;max-width:400px">
    <div class="select-card purple" onclick="assignStarterDeck('Aromatic')">
      <span class="badge">ベンゼン・濃硝酸・回復薬品</span>
      <h3 style="margin:6px 0 4px;font-size:16px;font-weight:400">芳香族・置換反応デッキ</h3>
      <p style="font-size:11px;opacity:.9;line-height:1.4">ニトロ化・スルホン化で超高火力を狙う専門デッキ！</p>
    </div>
    <div class="select-card red" onclick="assignStarterDeck('Polymer')">
      <span class="badge">エチレン・臭素・回復薬品</span>
      <h3 style="margin:6px 0 4px;font-size:16px;font-weight:400">付加・高分子デッキ</h3>
      <p style="font-size:11px;opacity:.9;line-height:1.4">ハロゲン付加や付加重合を使うバランス型</p>
    </div>
    <div class="select-card green" onclick="assignStarterDeck('Redox')">
      <span class="badge">アルコール・酢酸・回復薬品</span>
      <h3 style="margin:6px 0 4px;font-size:16px;font-weight:400">酸化・エステル・コントロール</h3>
      <p style="font-size:11px;opacity:.9;line-height:1.4">エステル化やけん化反応でテクニカルに勝利！</p>
    </div>
  </div>
</div>

<div id="field-screen" class="screen">
  <div id="canvas-container"></div>
  <div class="field-ui">
    <div class="status-box">
      <div>🧪 試薬: <span id="field-reagents">150</span></div>
      <div style="color:#4ade80;margin-top:3px">❤️ HP: <span id="field-hp">200</span></div>
      <div style="color:#fbbf24;font-size:12px;margin-top:3px">🎓 <span id="field-rank">初学者</span> · 撃破 <span id="field-kills">0</span></div>
      <div id="daily-hint" style="font-size:10px;color:#67e8f9;margin-top:6px"></div>
    </div>
    <div class="field-btns">
      <button class="glass-btn mini-btn success" onclick="saveGame()">セーブ</button>
      <button class="glass-btn mini-btn" style="background:linear-gradient(145deg,#6366f1,#4f46e5)" onclick="loadGame()">ロード</button>
      <button class="glass-btn mini-btn primary" onclick="switchState('deckEdit')">デッキ</button>
      <button class="glass-btn mini-btn pink" onclick="switchState('gacha')">ガチャ</button>
      <button class="glass-btn mini-btn warn" onclick="switchState('zukan')">図鑑</button>
      <button class="glass-btn mini-btn" style="background:linear-gradient(145deg,#84cc16,#65a30d);border-color:rgba(190,242,100,.35)" onclick="switchState('achieve')">実績</button>
      <button class="glass-btn mini-btn" style="background:linear-gradient(145deg,#14b8a6,#0d9488)" onclick="startPractice()">練習</button>
    </div>
  </div>
</div>

<div id="battle-screen" class="screen">
  <div class="battle-header">
    <div>
      <div style="color:#4ade80">🧑 HP: <span id="battle-player-hp">200</span></div>
      <div style="color:#38bdf8;font-size:11px;margin-top:2px">📚 山札: <span id="battle-deck-count">0</span></div>
      <div id="next-bonus" style="font-size:11px;color:#fbbf24;display:none;margin-top:2px">次ターン火力UP</div>
      <div id="dot-status" style="font-size:11px;color:#f87171;display:none;margin-top:2px">☠️ ボツリヌス毒素 毎ターン200</div>
      <div id="turn-limit" style="font-size:11px;color:#f472b6;display:none;margin-top:2px"></div>
    </div>
    <div style="text-align:right">
      <div style="font-size:12px;color:#94a3b8">👾 <span id="monster-name">敵</span> Lv.<span id="monster-level">1</span></div>
      <div style="color:#f87171;font-size:15px;margin-top:2px"><span id="monster-hp">500</span> / <span id="monster-maxhp">500</span></div>
      <div id="monster-weak" style="font-size:10px;color:#fb923c;margin-top:2px"></div>
      <div id="monster-cond" style="font-size:10px;color:#e879f9;margin-top:1px"></div>
    </div>
  </div>
  <div id="lab-canvas-container"></div>
  <div id="quiz-container" class="quiz-box" style="display:none">
    <div style="font-size:11px;color:#e9d5ff">📝 クイズ（正解で1.5倍）</div>
    <div id="quiz-question" style="font-size:13px"></div>
    <div id="quiz-options" class="quiz-options"></div>
  </div>
  <div id="battle-log" class="battle-log-box">バトル開始！</div>
  <div>
    <div style="font-size:10px;color:#94a3b8;margin-bottom:3px">手札 (<span id="hand-count">0</span>/7)　※長押しで反応ヒント</div>
    <div id="hand-cards" class="hand-container"></div>
  </div>
  <div class="battle-actions">
    <button id="attack-btn" class="glass-btn orange" style="flex:1;padding:11px;font-size:13px" onclick="executePlayerAttack()">化学反応実行</button>
    <button id="skip-btn" class="glass-btn slate" style="width:78px;padding:11px;font-size:12px" onclick="skipTurn()">ターン終了</button>
    <button id="flee-btn" class="glass-btn danger" style="width:70px;padding:11px;font-size:12px" onclick="fleeBattle()">逃げる</button>
    <button class="glass-btn primary" style="width:78px;padding:11px;font-size:12px" onclick="openReactionList()">反応一覧</button>
    <button class="glass-btn" style="background:linear-gradient(145deg,#8b5cf6,#6d28d9);width:70px;padding:11px;font-size:12px" onclick="openHistory()">履歴</button>
  </div>
  <div id="choice-box" class="choice-box">
    <div style="color:#fbbf24" id="choice-title">中間物質が生成された！</div>
    <div id="choice-desc" style="font-size:13px"></div>
    <div style="display:flex;gap:10px;justify-content:center">
      <button class="glass-btn orange" onclick="chooseAttack()">攻撃する</button>
      <button class="glass-btn success" onclick="chooseAddToHand()">手札に加える</button>
    </div>
  </div>
</div>

<div id="reaction-list-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#fbbf24;font-weight:400">📖 反応一覧</h3>
    <button class="glass-btn primary" style="padding:8px 14px" onclick="closeReactionList()">戻る</button>
  </div>
  <div id="full-reaction-list" class="scroll-panel"></div>
</div>

<div id="history-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#c4b5fd;font-weight:400">📜 バトル履歴</h3>
    <button class="glass-btn" style="background:linear-gradient(145deg,#8b5cf6,#6d28d9);padding:8px 14px" onclick="closeHistory()">戻る</button>
  </div>
  <div id="history-list" class="scroll-panel" style="white-space:pre-line"></div>
</div>

<div id="zukan-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#fbbf24;font-weight:400">📘 化合物図鑑 (<span id="zukan-count">0</span>)</h3>
    <button class="glass-btn slate" style="padding:8px 14px" onclick="switchState('field')">戻る</button>
  </div>
  <div id="zukan-list" class="scroll-panel"></div>
</div>

<div id="achieve-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <h3 style="color:#a3e635;font-weight:400">🏅 実績</h3>
    <button class="glass-btn slate" style="padding:8px 14px" onclick="switchState('field')">戻る</button>
  </div>
  <div id="achieve-list" class="scroll-panel"></div>
</div>

<div id="deck-edit-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:6px">
    <div>
      <h3 style="font-size:16px;font-weight:400">デッキ編集 (<span id="deck-count">0</span>/50)</h3>
      <p style="font-size:11px;color:#94a3b8">最低20枚 ／ 最大50枚</p>
    </div>
    <div style="display:flex;gap:6px;flex-wrap:wrap">
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('name')">名前順</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('rarity')">レア順</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('power')">火力順</button>
      <button type="button" class="glass-btn mini-btn slate" onclick="sortDeck('attr')">属性順</button>
      <button id="deck-done-btn" type="button" class="glass-btn success" onclick="finishDeckEdit()">完了</button>
    </div>
  </div>
  <div class="synth-bar-wrap">
    <div style="display:flex;justify-content:space-between;align-items:center">
      <span style="font-size:12px;color:#67e8f9">合成可能率</span>
      <span id="synth-rate-text" style="font-size:13px;color:#e2e8f0">—</span>
    </div>
    <div class="synth-bar-bg"><div id="synth-rate-bar" class="synth-bar-fill" style="width:0%"></div></div>
    <div id="synth-hint" style="font-size:10px;color:#94a3b8;margin-top:6px;line-height:1.4"></div>
  </div>
  <div id="deck-list" class="deck-list"></div>
  <div class="info-box" style="max-height:28vh">
    <div class="info-title">📖 反応一覧</div>
    <div id="deck-reaction-list" style="white-space:pre-line;color:#cbd5e1;font-size:11px"></div>
  </div>
</div>

<div id="gacha-screen" class="screen">
  <h2 style="margin-top:6px;font-weight:400;background:linear-gradient(90deg,#e879f9,#a78bfa);-webkit-background-clip:text;-webkit-text-fill-color:transparent">🧪 化合物ガチャ</h2>
  <p style="color:#7dd3fc">試薬: <span id="gacha-reagents">150</span> ／ ランク: <span id="gacha-rank">初学者</span></p>
  <div id="gacha-result" class="gacha-card-view"><span style="color:#94a3b8">ガチャを回すと出現</span></div>
  <div style="display:flex;gap:8px;flex-wrap:wrap;justify-content:center">
    <button class="glass-btn pink" style="padding:11px 20px" onclick="drawGacha()">ガチャ (100)</button>
    <button class="glass-btn slate" style="padding:11px 14px" onclick="switchState('field')">戻る</button>
  </div>
  <div class="info-box" style="width:100%;max-width:420px;max-height:36vh"><div class="info-title">📋 排出一覧</div><div id="gacha-list" style="white-space:pre-line;color:#cbd5e1"></div></div>
</div>

<div id="longpress-popup" class="longpress-popup">
  <div style="color:#38bdf8;margin-bottom:8px" id="lp-title">このカードでできる反応</div>
  <div id="lp-body" style="font-size:12px;line-height:1.55;white-space:pre-line;color:#e2e8f0"></div>
  <button class="glass-btn slate" style="margin-top:14px;width:100%" onclick="closeLongPress()">閉じる</button>
</div>

<script>
const ALL_CARDS = [
  {name:"メタン",formula:"CH4",attackPower:15,healPower:0,attribute:"Alkane",rarity:"R",color:"無色",odor:"無臭"},
  {name:"エタン",formula:"C2H6",attackPower:18,healPower:0,attribute:"Alkane",rarity:"R",color:"無色",odor:"無臭"},
  {name:"プロパン",formula:"C3H8",attackPower:20,healPower:0,attribute:"Alkane",rarity:"R",color:"無色",odor:"無臭"},
  {name:"ブタン",formula:"C4H10",attackPower:22,healPower:0,attribute:"Alkane",rarity:"R",color:"無色",odor:"無臭"},
  {name:"エチレン",formula:"C2H4",attackPower:25,healPower:0,attribute:"Alkenyl",rarity:"R",color:"無色",odor:"わずかに甘い"},
  {name:"プロピレン",formula:"C3H6",attackPower:28,healPower:0,attribute:"Alkenyl",rarity:"R",color:"無色",odor:"-"},
  {name:"アセチレン",formula:"C2H2",attackPower:35,healPower:0,attribute:"Alkynyl",rarity:"SR",color:"無色",odor:"特異臭"},
  {name:"ベンゼン",formula:"C6H6",attackPower:30,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色",odor:"特異臭"},
  {name:"トルエン",formula:"C6H5CH3",attackPower:35,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色",odor:"甘い芳香"},
  {name:"キシレン",formula:"C6H4(CH3)2",attackPower:38,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色",odor:"芳香"},
  {name:"ナフタレン",formula:"C10H8",attackPower:55,healPower:0,attribute:"Aromatic",rarity:"SR",color:"白色",odor:"樟脳様"},
  {name:"アントラセン",formula:"C14H10",attackPower:120,healPower:0,attribute:"Aromatic",rarity:"SSR",color:"無色〜淡黄",odor:"-"},
  {name:"スチレン",formula:"C6H5CH=CH2",attackPower:40,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色",odor:"特異臭"},
  {name:"メタノール",formula:"CH3OH",attackPower:22,healPower:0,attribute:"Alcohol",rarity:"R",color:"無色",odor:"アルコール臭"},
  {name:"エタノール",formula:"C2H5OH",attackPower:25,healPower:0,attribute:"Alcohol",rarity:"R",color:"無色",odor:"アルコール臭"},
  {name:"1-プロパノール",formula:"C3H7OH",attackPower:28,healPower:0,attribute:"Alcohol",rarity:"R",color:"無色",odor:"-"},
  {name:"2-プロパノール",formula:"(CH3)2CHOH",attackPower:28,healPower:0,attribute:"Alcohol",rarity:"R",color:"無色",odor:"-"},
  {name:"エチレングリコール",formula:"HOCH2CH2OH",attackPower:35,healPower:0,attribute:"Alcohol",rarity:"SR",color:"無色",odor:"無臭"},
  {name:"グリセリン",formula:"C3H5(OH)3",attackPower:40,healPower:0,attribute:"Alcohol",rarity:"SR",color:"無色",odor:"無臭"},
  {name:"ジエチルエーテル",formula:"(C2H5)2O",attackPower:30,healPower:0,attribute:"Ether",rarity:"R",color:"無色",odor:"特異臭"},
  {name:"ホルムアルデヒド",formula:"HCHO",attackPower:30,healPower:0,attribute:"Aldehyde",rarity:"R",color:"無色",odor:"刺激臭"},
  {name:"アセトアルデヒド",formula:"CH3CHO",attackPower:35,healPower:0,attribute:"Aldehyde",rarity:"R",color:"無色",odor:"刺激臭"},
  {name:"アセトン",formula:"CH3COCH3",attackPower:32,healPower:0,attribute:"Ketone",rarity:"R",color:"無色",odor:"特異臭"},
  {name:"ベンズアルデヒド",formula:"C6H5CHO",attackPower:45,healPower:0,attribute:"Aldehyde",rarity:"SR",color:"無色",odor:"アーモンド様"},
  {name:"ギ酸",formula:"HCOOH",attackPower:35,healPower:0,attribute:"Acid",rarity:"R",color:"無色",odor:"刺激臭"},
  {name:"酢酸",formula:"CH3COOH",attackPower:40,healPower:0,attribute:"Acid",rarity:"R",color:"無色",odor:"刺激的な酸味"},
  {name:"シュウ酸",formula:"(COOH)2",attackPower:50,healPower:0,attribute:"Acid",rarity:"SR",color:"無色",odor:"無臭"},
  {name:"安息香酸",formula:"C6H5COOH",attackPower:48,healPower:0,attribute:"Acid",rarity:"SR",color:"白色",odor:"-"},
  {name:"酢酸エチル",formula:"CH3COOC2H5",attackPower:55,healPower:0,attribute:"Ester",rarity:"R",color:"無色",odor:"果実様香気"},
  {name:"サリチル酸",formula:"C6H4(OH)COOH",attackPower:55,healPower:0,attribute:"Acid",rarity:"SR",color:"白色",odor:"-"},
  {name:"アセチルサリチル酸",formula:"C9H8O4",attackPower:120,healPower:0,attribute:"Ester",rarity:"SSR",color:"白色",odor:"-"},
  {name:"無水酢酸",formula:"(CH3CO)2O",attackPower:40,healPower:0,attribute:"Reagent",rarity:"SR",color:"無色",odor:"刺激臭"},
  {name:"アセトアニリド",formula:"C6H5NHCOCH3",attackPower:60,healPower:0,attribute:"Aromatic",rarity:"SR",color:"白色",odor:"-"},
  {name:"トリパルミチン",formula:"C51H98O6",attackPower:45,healPower:0,attribute:"Fat",rarity:"SR",color:"白色",odor:"-"},
  {name:"トリステアリン",formula:"C57H110O6",attackPower:48,healPower:0,attribute:"Fat",rarity:"SR",color:"白色",odor:"-"},
  {name:"トリオレイン",formula:"C57H104O6",attackPower:50,healPower:0,attribute:"Fat",rarity:"SR",color:"淡黄",odor:"-"},
  {name:"フェノール",formula:"C6H5OH",attackPower:45,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色〜淡紅",odor:"特異臭"},
  {name:"o-クレゾール",formula:"CH3C6H4OH",attackPower:40,healPower:0,attribute:"Phenol",rarity:"R",color:"無色",odor:"フェノール臭"},
  {name:"m-クレゾール",formula:"CH3C6H4OH",attackPower:40,healPower:0,attribute:"Phenol",rarity:"R",color:"無色",odor:"フェノール臭"},
  {name:"p-クレゾール",formula:"CH3C6H4OH",attackPower:42,healPower:0,attribute:"Phenol",rarity:"R",color:"無色",odor:"フェノール臭"},
  {name:"カテコール",formula:"C6H4(OH)2",attackPower:50,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色",odor:"-"},
  {name:"レゾルシノール",formula:"C6H4(OH)2",attackPower:48,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色",odor:"-"},
  {name:"ヒドロキノン",formula:"C6H4(OH)2",attackPower:55,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色",odor:"-"},
  {name:"ピロガロール",formula:"C6H3(OH)3",attackPower:60,healPower:0,attribute:"Phenol",rarity:"SR",color:"白色",odor:"-"},
  {name:"アニリン",formula:"C6H5NH2",attackPower:65,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色〜褐色",odor:"特異臭"},
  {name:"ニトロベンゼン",formula:"C6H5NO2",attackPower:70,healPower:0,attribute:"Aromatic",rarity:"SR",color:"淡黄色",odor:"アーモンド様"},
  {name:"アゾベンゼン",formula:"C6H5N=NC6H5",attackPower:110,healPower:0,attribute:"Aromatic",rarity:"SSR",color:"橙赤色",odor:"無臭"},
  {name:"塩素",formula:"Cl2",attackPower:35,healPower:0,attribute:"Halogen",rarity:"R",color:"黄緑色",odor:"刺激臭"},
  {name:"臭素",formula:"Br2",attackPower:35,healPower:0,attribute:"Halogen",rarity:"R",color:"赤褐色",odor:"刺激臭"},
  {name:"ヨウ素",formula:"I2",attackPower:30,healPower:0,attribute:"Halogen",rarity:"R",color:"紫黒色",odor:"特異臭"},
  {name:"濃硝酸",formula:"HNO3",attackPower:30,healPower:0,attribute:"Reagent",rarity:"SR",color:"無色〜淡黄",odor:"刺激臭"},
  {name:"濃硫酸",formula:"H2SO4",attackPower:30,healPower:0,attribute:"Reagent",rarity:"SR",color:"無色",odor:"無臭"},
  {name:"水酸化ナトリウム",formula:"NaOH",attackPower:35,healPower:0,attribute:"Base",rarity:"SR",color:"白色",odor:"無臭"},
  {name:"水酸化カルシウム",formula:"Ca(OH)2",attackPower:28,healPower:0,attribute:"Base",rarity:"R",color:"白色",odor:"無臭"},
  {name:"金属ナトリウム",formula:"Na",attackPower:40,healPower:0,attribute:"Metal",rarity:"SR",color:"銀白色",odor:"無臭"},
  {name:"過マンガン酸カリウム",formula:"KMnO4",attackPower:40,healPower:0,attribute:"Oxidant",rarity:"SR",color:"紫黒色",odor:"無臭"},
  {name:"二クロム酸カリウム",formula:"K2Cr2O7",attackPower:38,healPower:0,attribute:"Oxidant",rarity:"SR",color:"橙赤色",odor:"無臭"},
  {name:"水素化ホウ素ナトリウム",formula:"NaBH4",attackPower:40,healPower:0,attribute:"Reductant",rarity:"SR",color:"白色",odor:"無臭"},
  {name:"還元剤",formula:"[Red]",attackPower:30,healPower:0,attribute:"Reductant",rarity:"SR",color:"-",odor:"-"},
  {name:"重合触媒(Ziegler)",formula:"[Cat]",attackPower:30,healPower:0,attribute:"Catalyst",rarity:"SSR",color:"-",odor:"-"},
  {name:"塩化アルミニウム",formula:"AlCl3",attackPower:35,healPower:0,attribute:"Catalyst",rarity:"SR",color:"白色",odor:"-"},
  {name:"鉄",formula:"Fe",attackPower:25,healPower:0,attribute:"Catalyst",rarity:"R",color:"灰色",odor:"無臭"},
  {name:"ジアゾ化剤",formula:"NaNO2/HCl",attackPower:35,healPower:0,attribute:"Reagent",rarity:"SR",color:"-",odor:"-"},
  {name:"メチル基",formula:"-CH3",attackPower:20,healPower:0,attribute:"Hydrocarbon",rarity:"R",color:"-",odor:"-"},
  {name:"エチル基",formula:"-C2H5",attackPower:25,healPower:0,attribute:"Hydrocarbon",rarity:"R",color:"-",odor:"-"},
  {name:"プロピル基",formula:"-C3H7",attackPower:28,healPower:0,attribute:"Hydrocarbon",rarity:"R",color:"-",odor:"-"},
  {name:"イソプロピル基",formula:"-CH(CH3)2",attackPower:30,healPower:0,attribute:"Hydrocarbon",rarity:"R",color:"-",odor:"-"},
  {name:"ブチル基",formula:"-C4H9",attackPower:32,healPower:0,attribute:"Hydrocarbon",rarity:"R",color:"-",odor:"-"},
  {name:"フェニル基",formula:"-C6H5",attackPower:40,healPower:0,attribute:"Hydrocarbon",rarity:"SR",color:"-",odor:"-"},
  {name:"ベンジル基",formula:"-CH2C6H5",attackPower:38,healPower:0,attribute:"Hydrocarbon",rarity:"SR",color:"-",odor:"-"},
  {name:"ビニル基",formula:"-CH=CH2",attackPower:35,healPower:0,attribute:"Hydrocarbon",rarity:"R",color:"-",odor:"-"},
  {name:"ヒドロキシ基",formula:"-OH",attackPower:25,healPower:0,attribute:"FunctionalGroup",rarity:"R",color:"-",odor:"-"},
  {name:"カルボキシ基",formula:"-COOH",attackPower:40,healPower:0,attribute:"FunctionalGroup",rarity:"SR",color:"-",odor:"-"},
  {name:"アミノ基",formula:"-NH2",attackPower:30,healPower:0,attribute:"FunctionalGroup",rarity:"R",color:"-",odor:"-"},
  {name:"アルデヒド基",formula:"-CHO",attackPower:35,healPower:0,attribute:"FunctionalGroup",rarity:"R",color:"-",odor:"-"},
  {name:"ニトロ基",formula:"-NO2",attackPower:45,healPower:0,attribute:"FunctionalGroup",rarity:"SR",color:"-",odor:"-"},
  {name:"スルホン基",formula:"-SO3H",attackPower:42,healPower:0,attribute:"FunctionalGroup",rarity:"SR",color:"-",odor:"-"},
  {name:"ハロゲン基",formula:"-X",attackPower:30,healPower:0,attribute:"FunctionalGroup",rarity:"R",color:"-",odor:"-"},
  {name:"マレイン酸",formula:"cis-HOOCCH=CHCOOH",attackPower:55,healPower:0,attribute:"CisTrans",rarity:"SR",color:"白色",odor:"-"},
  {name:"フマル酸",formula:"trans-HOOCCH=CHCOOH",attackPower:55,healPower:0,attribute:"CisTrans",rarity:"SR",color:"白色",odor:"-"},
  {name:"シス-2-ブテン",formula:"cis-CH3CH=CHCH3",attackPower:35,healPower:0,attribute:"CisTrans",rarity:"R",color:"無色",odor:"-"},
  {name:"トランス-2-ブテン",formula:"trans-CH3CH=CHCH3",attackPower:35,healPower:0,attribute:"CisTrans",rarity:"R",color:"無色",odor:"-"},
  {name:"オレイン酸",formula:"C18H34O2",attackPower:50,healPower:0,attribute:"CisTrans",rarity:"SR",color:"無色〜淡黄",odor:"-"},
  {name:"スチルベン",formula:"C6H5CH=CHC6H5",attackPower:60,healPower:0,attribute:"CisTrans",rarity:"SR",color:"無色",odor:"-"},
  {name:"グリシン",formula:"H2NCH2COOH",attackPower:0,healPower:40,attribute:"Nutrient",rarity:"R",color:"白色",odor:"無臭"},
  {name:"グルコース",formula:"C6H12O6",attackPower:0,healPower:65,attribute:"Nutrient",rarity:"SR",color:"白色",odor:"無臭"},
  {name:"スクロース",formula:"C12H22O11",attackPower:0,healPower:50,attribute:"Nutrient",rarity:"R",color:"白色",odor:"無臭"},
  {name:"トリニトロトルエン",formula:"C7H5N3O6",attackPower:180,healPower:0,attribute:"Explosive",rarity:"SSR",color:"淡黄色",odor:"無臭"},
  {name:"ピクリン酸",formula:"C6H3N3O7",attackPower:180,healPower:0,attribute:"Explosive",rarity:"SSR",color:"黄色",odor:"無臭"},
  {name:"フッ化水素酸",formula:"HF",attackPower:Infinity,healPower:0,attribute:"Acid",rarity:"SSSR",color:"無色",odor:"刺激臭"},
  {name:"ボツリヌス毒素",formula:"BoNT",attackPower:0,healPower:0,attribute:"Toxin",rarity:"SSSR",color:"-",odor:"-"}
];

const RANKS = [
  {name:"初学者", kills:0,  reagentBonus:1.0, gachaBoost:0,   promoteReward:0},
  {name:"高校生", kills:8,  reagentBonus:1.15,gachaBoost:0.3, promoteReward:40},
  {name:"大学生", kills:20, reagentBonus:1.3, gachaBoost:0.6, promoteReward:60},
  {name:"大学院生",kills:40, reagentBonus:1.5, gachaBoost:1.0, promoteReward:80},
  {name:"助教",   kills:55, reagentBonus:1.7, gachaBoost:1.2, promoteReward:100},
  {name:"准教授", kills:75, reagentBonus:1.9, gachaBoost:1.5, promoteReward:120},
  {name:"博士",   kills:100,reagentBonus:2.2, gachaBoost:1.8, promoteReward:150},
  {name:"教授",   kills:140,reagentBonus:2.5, gachaBoost:2.2, promoteReward:200}
];

const ACHIEVEMENTS = [
  {id:"first_win", name:"初勝利", desc:"初めて敵を倒す", reward:30, check:s=>s.kills>=1},
  {id:"kills_10", name:"撃破10", desc:"敵を10体倒す", reward:50, check:s=>s.kills>=10},
  {id:"kills_50", name:"撃破50", desc:"敵を50体倒す", reward:120, check:s=>s.kills>=50},
  {id:"nitro", name:"ニトロ化の達人", desc:"ニトロ化反応を成功", reward:40, check:s=>s.flags.nitro},
  {id:"sapon", name:"けん化マスター", desc:"けん化を成功", reward:40, check:s=>s.flags.sapon},
  {id:"poly", name:"高分子合成", desc:"重合反応を成功", reward:40, check:s=>s.flags.poly},
  {id:"acetyl", name:"アセチル化", desc:"アセチル化を成功", reward:45, check:s=>s.flags.acetyl},
  {id:"dehyd", name:"脱水反応", desc:"脱水反応を成功", reward:45, check:s=>s.flags.dehyd},
  {id:"fat", name:"油脂のけん化", desc:"油脂をけん化", reward:50, check:s=>s.flags.fat},
  {id:"collect_20", name:"収集家", desc:"図鑑20種登録", reward:60, check:s=>new Set(s.collection.map(c=>c.name)).size>=20},
  {id:"collect_40", name:"大図鑑", desc:"図鑑40種登録", reward:100, check:s=>new Set(s.collection.map(c=>c.name)).size>=40},
  {id:"boss", name:"ボス討伐", desc:"ボスを倒す", reward:80, check:s=>s.flags.boss}
];

const DAILY_QUESTS = [
  {key:"nitro", label:"ニトロ化を1回成功させる"},
  {key:"sapon", label:"けん化を1回成功させる"},
  {key:"poly", label:"重合を1回成功させる"},
  {key:"ester", label:"エステル化を1回成功させる"},
  {key:"oxid", label:"酸化反応を1回成功させる"},
  {key:"acetyl", label:"アセチル化を1回成功させる"},
  {key:"dehyd", label:"脱水反応を1回成功させる"}
];

const FULL_REACTION_TEXT = `【中間体・連鎖】
・ベンゼン + ニトロ基 → ニトロベンゼン
・ニトロベンゼン + 還元剤 / NaBH4 → アニリン
・アニリン + ジアゾ化剤 → アゾベンゼン
・酢酸 + エタノール → 酢酸エチル

【アセチル化】
・アニリン + 無水酢酸 → アセトアニリド
・サリチル酸 + 無水酢酸 → アセチルサリチル酸

【脱水】
・エタノール + 濃硫酸 → エチレン
・1-プロパノール + 濃硫酸 → プロピレン

【油脂・けん化】
・トリパルミチン / トリステアリン / トリオレイン + 水酸化ナトリウム → けん化
・酢酸 / 酢酸エチル / オレイン酸 + 水酸化ナトリウム → けん化

【ニトロ化】
・ベンゼン / トルエン / フェノール / ナフタレン / アントラセン + 濃硝酸

【スルホン化】
・ベンゼン / ナフタレン + 濃硫酸

【ハロゲン化・付加】
・ベンゼン + 塩素 / 臭素 + 触媒（鉄・AlCl3等）
・エチレン + 塩素 / 臭素 → 付加（脱色）
・アセチレン + 臭素 → 付加
・シス-2-ブテン / トランス-2-ブテン + 臭素 → 付加

【重合】
・エチレン / スチレン / プロピレン / ビニル基 + 重合触媒(Ziegler)

【酸化】
・エタノール / メタノール / アセトアルデヒド + KMnO4 / K2Cr2O7
・2-プロパノール + 酸化剤 → ケトン
・トルエン + KMnO4 → 安息香酸

【金属ナトリウム】
・エタノール / メタノール / 1-プロパノール + Na → アルコキシド
・フェノール / クレゾール + Na → フェノキシド等

【基 + 官能基】
・メチル基 / エチル基 / プロピル基 / イソプロピル基 / ブチル基 / フェニル基 / ベンジル基 / ビニル基
　+ ヒドロキシ基 / カルボキシ基 / アミノ基 / アルデヒド基 / ニトロ基 / スルホン基 / ハロゲン基

【特殊】
・トリニトロトルエン / ピクリン酸 … 180
・フッ化水素酸 … ∞（1/10で自爆）
・ボツリヌス毒素 … 毎ターン200継続

【倍率】
・触媒なし 1.5倍 / 触媒あり 2.0倍
・弱点 1.5倍 / クイズ正解 1.5倍`;

const CARD_REACTIONS = {
  "ベンゼン":"・+ニトロ基 → ニトロベンゼン\n・+濃硝酸 → ニトロ化\n・+濃硫酸 → スルホン化\n・+塩素/臭素+触媒 → ハロゲン化",
  "トルエン":"・+濃硝酸 → ニトロ化\n・+KMnO4 → 側鎖酸化 → 安息香酸",
  "フェノール":"・+濃硝酸 → ニトロ化\n・+金属Na → フェノキシド",
  "アニリン":"・+ジアゾ化剤 → アゾベンゼン\n・+無水酢酸 → アセトアニリド",
  "ニトロベンゼン":"・+還元剤 / NaBH4 → アニリン",
  "アゾベンゼン":"・単体投擲で高火力攻撃\n・（これ以上の連鎖反応はなし）",
  "酢酸":"・+エタノール → 酢酸エチル\n・+NaOH → けん化",
  "エタノール":"・+酢酸 → エステル化 → 酢酸エチル\n・+濃硫酸 → 脱水 → エチレン\n・+Na → アルコキシド\n・+KMnO4 → 酸化",
  "酢酸エチル":"・+水酸化ナトリウム → けん化\n・単体投擲も可能（エステル属性）",
  "エチレン":"・+塩素/臭素 → 付加\n・+重合触媒 → ポリエチレン",
  "無水酢酸":"・+アニリン → アセトアニリド\n・+サリチル酸 → アセチルサリチル酸",
  "サリチル酸":"・+無水酢酸 → アセチルサリチル酸",
  "アセトアニリド":"・単体投擲可能\n・アセチル化生成物",
  "アセチルサリチル酸":"・単体投擲で高火力（エステル）\n・アスピリン相当の生成物",
  "トリパルミチン":"・+NaOH → 油脂のけん化",
  "トリステアリン":"・+NaOH → 油脂のけん化",
  "トリオレイン":"・+NaOH → 油脂のけん化",
  "濃硫酸":"・触媒・脱水剤\n・+エタノール → 脱水",
  "水酸化ナトリウム":"・けん化全般（酢酸エチル・油脂・酢酸など）",
  "重合触媒(Ziegler)":"・+エチレン/スチレン/プロピレン → 重合",
  "過マンガン酸カリウム":"・アルコール・アルデヒド・トルエンの酸化",
  "金属ナトリウム":"・+アルコール → アルコキシド\n・+フェノール → フェノキシド",
  "アセチレン":"・+臭素 → 付加",
  "プロピレン":"・+重合触媒 → ポリプロピレン",
  "スチレン":"・+重合触媒 → ポリスチレン",
  "1-プロパノール":"・+濃硫酸 → 脱水\n・+Na → アルコキシド",
  "2-プロパノール":"・+酸化剤 → ケトン",
  "メタノール":"・+酸化剤 → 酸化\n・+Na → アルコキシド",
  "ナフタレン":"・+濃硝酸 → ニトロ化\n・+濃硫酸 → スルホン化",
  "アントラセン":"・+濃硝酸 → ニトロ化",
  "オレイン酸":"・+NaOH → けん化"
};

const SYNTH_PAIRS = [
  {a:["ベンゼン"], b:["ニトロ基","濃硝酸","濃硫酸","塩素","臭素"]},
  {a:["トルエン"], b:["濃硝酸","過マンガン酸カリウム"]},
  {a:["フェノール"], b:["濃硝酸","金属ナトリウム"]},
  {a:["アニリン"], b:["ジアゾ化剤","無水酢酸"]},
  {a:["ニトロベンゼン"], b:["還元剤","水素化ホウ素ナトリウム"]},
  {a:["酢酸"], b:["エタノール","水酸化ナトリウム"]},
  {a:["エタノール"], b:["酢酸","濃硫酸","金属ナトリウム","過マンガン酸カリウム","二クロム酸カリウム"]},
  {a:["エチレン"], b:["塩素","臭素","重合触媒(Ziegler)"]},
  {a:["スチレン","プロピレン"], b:["重合触媒(Ziegler)"]},
  {a:["サリチル酸"], b:["無水酢酸"]},
  {a:["トリパルミチン","トリステアリン","トリオレイン","オレイン酸","酢酸エチル"], b:["水酸化ナトリウム"]},
  {a:["メタノール","1-プロパノール","2-プロパノール"], b:["過マンガン酸カリウム","二クロム酸カリウム","金属ナトリウム","濃硫酸"]},
  {a:["メチル基","エチル基","プロピル基","イソプロピル基","ブチル基","フェニル基","ベンジル基","ビニル基"], b:["ヒドロキシ基","カルボキシ基","アミノ基","アルデヒド基","ニトロ基","スルホン基","ハロゲン基"]},
  {a:["アセチレン","シス-2-ブテン","トランス-2-ブテン"], b:["臭素"]},
  {a:["ナフタレン","アントラセン"], b:["濃硝酸","濃硫酸"]}
];

const RARITY_ORDER={SSSR:0,SSR:1,SR:2,R:3};

let gameState = {
  reagents:150, playerHP:200, playerMaxHP:200,
  collection:[], currentDeck:[], currentMonster:null,
  nextDamageBonus:1.0, kills:0,
  flags:{nitro:false,sapon:false,poly:false,ester:false,oxid:false,acetyl:false,dehyd:false,fat:false,boss:false},
  achieved:{}, lastRank:"初学者",
  dailyDate:"", dailyKey:"", dailyDone:false,
  deckListOrder:[]
};

let isBattleOver=false, isProcessing=false, botulinumActive=false, isPractice=false;
let pendingIntermediate=null, fromBattleToReaction=false, fromBattleToHistory=false;
let battleHistory=[], battleTurnCount=0, bossTurnLimit=0;

function todayStr(){const d=new Date();return d.getFullYear()+"-"+(d.getMonth()+1)+"-"+(d.getDate());}
function initDaily(){
  const t=todayStr();
  if(gameState.dailyDate!==t){
    gameState.dailyDate=t;
    gameState.dailyKey=DAILY_QUESTS[Math.floor(Math.random()*DAILY_QUESTS.length)].key;
    gameState.dailyDone=false;
  }
}
function getDailyLabel(){
  const q=DAILY_QUESTS.find(x=>x.key===gameState.dailyKey);
  return q?q.label:"—";
}
function getRank(){
  let r=RANKS[0];
  for(const rank of RANKS){if(gameState.kills>=rank.kills)r=rank;}
  return r;
}
function checkRankUp(){
  const r=getRank();
  if(r.name!==gameState.lastRank){
    const reward=r.promoteReward||0;
    if(reward>0){gameState.reagents+=reward; alert(`🎓 ランクアップ！ ${gameState.lastRank} → ${r.name}\n試薬 +${reward}`);}
    gameState.lastRank=r.name;
  }
}
function checkAchievements(){
  ACHIEVEMENTS.forEach(a=>{
    if(gameState.achieved[a.id]) return;
    if(a.check(gameState)){
      gameState.achieved[a.id]=true;
      gameState.reagents+=a.reward;
      setTimeout(()=>alert(`🏅 実績達成「${a.name}」\n試薬 +${a.reward}`),300);
    }
  });
}
function markFlag(f){
  gameState.flags[f]=true;
  if(!gameState.dailyDone && gameState.dailyKey===f){
    gameState.dailyDone=true;
    gameState.reagents+=50;
    setTimeout(()=>alert("📅 日替わり反応クリア！ 試薬 +50"),200);
  }
  checkAchievements();
}

function saveGame(silent=false){
  localStorage.setItem('organicChemBattleSave',JSON.stringify({...gameState}));
  if(!silent) alert('セーブしました！');
}
function loadGame(){
  const saved=localStorage.getItem('organicChemBattleSave');
  if(!saved){alert('セーブデータがありません');return;}
  try{
    Object.assign(gameState,JSON.parse(saved));
    if(!gameState.flags) gameState.flags={};
    if(!gameState.achieved) gameState.achieved={};
    if(!gameState.deckListOrder) gameState.deckListOrder=[];
    gameState.collection.forEach(c=>{
      if(c.name==="アゾベンゼン") c.attackPower=110;
      if(c.name==="アセチルサリチル酸") c.attackPower=120;
    });
    gameState.currentDeck.forEach(c=>{
      if(c.name==="アゾベンゼン") c.attackPower=110;
      if(c.name==="アセチルサリチル酸") c.attackPower=120;
    });
    initDaily(); updateFieldUI(); switchState('field'); alert('ロードしました！');
  }catch(e){alert('ロード失敗');}
}

function switchState(s){
  document.querySelectorAll('.screen').forEach(el=>el.classList.remove('active'));
  if(s==='deckSelection') document.getElementById('deck-select-screen').classList.add('active');
  if(s==='field'){document.getElementById('field-screen').classList.add('active');updateFieldUI();initThreeJS();}
  if(s==='battle') document.getElementById('battle-screen').classList.add('active');
  if(s==='deckEdit'){document.getElementById('deck-edit-screen').classList.add('active');renderDeckEdit();}
  if(s==='gacha'){document.getElementById('gacha-screen').classList.add('active');document.getElementById('gacha-reagents').innerText=gameState.reagents;document.getElementById('gacha-rank').innerText=getRank().name;renderGachaList();}
  if(s==='reactionList'){document.getElementById('reaction-list-screen').classList.add('active');document.getElementById('full-reaction-list').innerText=FULL_REACTION_TEXT;}
  if(s==='zukan'){document.getElementById('zukan-screen').classList.add('active');renderZukan();}
  if(s==='achieve'){document.getElementById('achieve-screen').classList.add('active');renderAchieve();}
  if(s==='history'){document.getElementById('history-screen').classList.add('active');document.getElementById('history-list').innerText=battleHistory.slice(-30).join("\n\n")||"履歴なし";}
}
function openReactionList(){fromBattleToReaction=true;switchState('reactionList');}
function closeReactionList(){
  if(fromBattleToReaction){fromBattleToReaction=false;document.querySelectorAll('.screen').forEach(el=>el.classList.remove('active'));document.getElementById('battle-screen').classList.add('active');updateBattleUI();}
  else switchState('field');
}
function openHistory(){fromBattleToHistory=true;switchState('history');}
function closeHistory(){
  if(fromBattleToHistory){fromBattleToHistory=false;document.querySelectorAll('.screen').forEach(el=>el.classList.remove('active'));document.getElementById('battle-screen').classList.add('active');updateBattleUI();}
  else switchState('field');
}

function updateFieldUI(){
  initDaily();
  document.getElementById('field-reagents').innerText=gameState.reagents;
  document.getElementById('field-hp').innerText=gameState.playerHP;
  document.getElementById('field-rank').innerText=getRank().name;
  document.getElementById('field-kills').innerText=gameState.kills;
  document.getElementById('daily-hint').innerText=gameState.dailyDone?`📅 日替わり達成済`:`📅 今日: ${getDailyLabel()}`;
}

function assignStarterDeck(type){
  gameState.currentDeck=[]; gameState.collection=[]; gameState.deckListOrder=[];
  let base=[];
  if(type==='Aromatic') base=["ベンゼン","トルエン","濃硝酸","濃硫酸","フェノール","グルコース","ニトロ基"].map(n=>ALL_CARDS.find(c=>c.name===n));
  else if(type==='Polymer') base=["エチレン","臭素","塩素","重合触媒(Ziegler)","グルコース","エタノール"].map(n=>ALL_CARDS.find(c=>c.name===n));
  else base=["エタノール","酢酸","水酸化ナトリウム","過マンガン酸カリウム","グルコース","アセトアルデヒド"].map(n=>ALL_CARDS.find(c=>c.name===n));
  base=base.filter(Boolean);
  for(let i=0;i<40;i++){const c={...base[i%base.length],id:Math.random().toString(36).substr(2,9)};gameState.currentDeck.push(c);gameState.collection.push(c);}
  gameState.playerHP=gameState.playerMaxHP; gameState.lastRank="初学者"; initDaily(); switchState('field');
}

function renderGachaList(){
  const order=["SSSR","SSR","SR","R"]; let html="";
  order.forEach(r=>{
    const cards=ALL_CARDS.filter(c=>c.rarity===r); if(!cards.length)return;
    html+=`【${r}】\n`;
    cards.forEach(c=>{let p=c.name==="ボツリヌス毒素"?"毎ターン200":(c.attackPower===Infinity?"∞":(c.healPower>0?`回復${c.healPower}`:c.attackPower));html+=`・${c.name}（${p}）\n`;});
    html+="\n";
  });
  document.getElementById('gacha-list').innerText=html.trim();
}
function renderZukan(){
  const names=[...new Set(gameState.collection.map(c=>c.name))];
  document.getElementById('zukan-count').innerText=names.length+"/"+ALL_CARDS.length;
  const list=document.getElementById('zukan-list'); list.innerHTML="";
  if(!names.length){list.innerHTML="<div style='color:#94a3b8'>まだ登録がありません</div>";return;}
  names.sort((a,b)=>a.localeCompare(b,'ja')).forEach(name=>{
    const c=ALL_CARDS.find(x=>x.name===name)||gameState.collection.find(x=>x.name===name);
    const div=document.createElement('div'); div.className='zukan-item';
    div.innerHTML=`<div>${c.name} <span class="card-rarity rarity-${c.rarity}">${c.rarity}</span></div>
      <div style="font-size:11px;color:#94a3b8">${c.formula} ／ ${c.attribute}</div>
      <div style="font-size:11px;margin-top:4px">色: ${c.color||"-"} ／ 匂い: ${c.odor||"-"}</div>
      <div style="font-size:11px;color:#fbbf24;margin-top:2px">威力:${c.attackPower===Infinity?"∞":c.attackPower} 回復:${c.healPower||0}</div>`;
    list.appendChild(div);
  });
}
function renderAchieve(){
  const list=document.getElementById('achieve-list'); list.innerHTML="";
  ACHIEVEMENTS.forEach(a=>{
    const done=!!gameState.achieved[a.id];
    const div=document.createElement('div'); div.className=`achieve-item ${done?'done':'locked'}`;
    div.innerHTML=`<div><div>${done?'✅':'🔒'} ${a.name}</div><div style="font-size:11px;color:#94a3b8">${a.desc}</div></div><div style="color:#fbbf24;font-size:12px">+${a.reward}</div>`;
    list.appendChild(div);
  });
}

function calcSynthRate(){
  const names=new Set(gameState.currentDeck.map(c=>c.name));
  if(names.size===0) return {rate:0, ok:0, total:SYNTH_PAIRS.length, missing:[]};
  let ok=0; const missing=[];
  SYNTH_PAIRS.forEach(pair=>{
    const hasA=pair.a.some(n=>names.has(n));
    const hasB=pair.b.some(n=>names.has(n));
    if(hasA && hasB) ok++;
    else if(hasA && !hasB) missing.push(pair.a.find(n=>names.has(n))+" 側はあるが相手役不足");
    else if(!hasA && hasB) missing.push(pair.b.find(n=>names.has(n))+" 側はあるが相手役不足");
  });
  return {rate:Math.round((ok/SYNTH_PAIRS.length)*100), ok, total:SYNTH_PAIRS.length, missing:missing.slice(0,4)};
}

function createHumanoidMesh(){
  const group=new THREE.Group();
  const bodyMat=new THREE.MeshLambertMaterial({color:0x0284c7});
  const skinMat=new THREE.MeshLambertMaterial({color:0xffdbac});
  const legMat=new THREE.MeshLambertMaterial({color:0x1e293b});
  const head=new THREE.Mesh(new THREE.SphereGeometry(0.25,20,20),skinMat); head.position.y=0.85; group.add(head);
  const body=new THREE.Mesh(new THREE.CylinderGeometry(0.2,0.15,0.6,16),bodyMat); body.position.y=0.45; group.add(body);
  const armGeo=new THREE.CylinderGeometry(0.06,0.06,0.4,10);
  const la=new THREE.Mesh(armGeo,bodyMat); la.position.set(-0.28,0.45,0);
  const ra=new THREE.Mesh(armGeo,bodyMat); ra.position.set(0.28,0.45,0);
  group.add(la); group.add(ra);
  const legGeo=new THREE.CylinderGeometry(0.07,0.07,0.45,10);
  const ll=new THREE.Mesh(legGeo,legMat); ll.position.set(-0.1,0.15,0);
  const rl=new THREE.Mesh(legGeo,legMat); rl.position.set(0.1,0.15,0);
  group.add(ll); group.add(rl);
  return group;
}
function createMoleculeMesh(col){
  const g=new THREE.Group(),m=new THREE.MeshLambertMaterial({color:col}),s=new THREE.MeshLambertMaterial({color:0xffffff});
  g.add(new THREE.Mesh(new THREE.SphereGeometry(.5,20,20),m));
  [[.7,.45,0],[-.7,.45,0],[0,-.65,.45],[0,.45,-.65]].forEach(p=>{const a=new THREE.Mesh(new THREE.SphereGeometry(.25,14,14),s);a.position.set(...p);g.add(a);});
  return g;
}

let scene,camera,renderer,playerNode,monsters=[],targetPlayerPos={x:0,z:0},isThreeInit=false,lastSpawnTime=0;
function initThreeJS(){
  if(isThreeInit) return; isThreeInit=true;
  const cont=document.getElementById('canvas-container');
  scene=new THREE.Scene(); scene.background=new THREE.Color(0x87c8f0);
  scene.fog=new THREE.Fog(0x87c8f0, 28, 60);
  camera=new THREE.PerspectiveCamera(45,innerWidth/innerHeight,.1,1000); camera.position.set(0,12,10); camera.rotation.x=-Math.PI/3.2;
  renderer=new THREE.WebGLRenderer({antialias:true}); renderer.setSize(innerWidth,innerHeight); renderer.setPixelRatio(Math.min(devicePixelRatio,2)); cont.appendChild(renderer.domElement);
  const sun=new THREE.DirectionalLight(0xfff5e6,1.35); sun.position.set(5,12,8); scene.add(sun);
  scene.add(new THREE.AmbientLight(0xb8d4ff,.55));
  scene.add(new THREE.HemisphereLight(0x87ceeb,0x3d8b40,.4));
  const floor=new THREE.Mesh(new THREE.PlaneGeometry(120,120),new THREE.MeshLambertMaterial({color:0x3d9e5a})); floor.rotation.x=-Math.PI/2; scene.add(floor);
  playerNode=createHumanoidMesh(); scene.add(playerNode);
  for(let i=0;i<3;i++) spawnMonster();
  let drag=false,lx=0,ly=0;
  addEventListener('pointerdown',e=>{drag=true;lx=e.clientX;ly=e.clientY});
  addEventListener('pointermove',e=>{if(!drag)return; targetPlayerPos.x=Math.max(-12,Math.min(12,targetPlayerPos.x+(e.clientX-lx)*.04)); targetPlayerPos.z=Math.max(-18,Math.min(8,targetPlayerPos.z+(e.clientY-ly)*.04)); lx=e.clientX;ly=e.clientY});
  addEventListener('pointerup',()=>drag=false);
  function anim(t){
    requestAnimationFrame(anim);
    if(t-lastSpawnTime>5000){if(monsters.filter(m=>m.isActive).length<6)spawnMonster();lastSpawnTime=t;}
    playerNode.position.x+=(targetPlayerPos.x-playerNode.position.x)*.15;
    playerNode.position.z+=(targetPlayerPos.z-playerNode.position.z)*.15;
    camera.position.x=playerNode.position.x; camera.position.z=playerNode.position.z+10;
    const active=document.getElementById('field-screen').classList.contains('active');
    monsters.forEach(m=>{
      if(!m.isActive||!active)return;
      m.mesh.rotation.y+=.012; m.changeDirTimer--;
      if(m.changeDirTimer<=0){m.vx=(Math.random()-.5)*.08;m.vz=(Math.random()-.5)*.08;m.changeDirTimer=30+Math.random()*60;}
      m.mesh.position.x+=m.vx; m.mesh.position.z+=m.vz;
      if(Math.abs(m.mesh.position.x)>14)m.vx*=-1; if(m.mesh.position.z<-20||m.mesh.position.z>8)m.vz*=-1;
      const dx=playerNode.position.x-m.mesh.position.x, dz=playerNode.position.z-m.mesh.position.z;
      if(Math.sqrt(dx*dx+dz*dz)<=1){m.isActive=false;scene.remove(m.mesh);gameState.currentMonster=m;startBattle(false);}
    });
    renderer.render(scene,camera);
  }
  anim(0);
}

function spawnMonster(){
  const isBoss=Math.random()<.12;
  let level,colorHex,hp,atk,name,weakness,condition=null,turnLimit=0;
  if(isBoss){
    level=5; colorHex=0x7c3aed; hp=900+Math.floor(Math.random()*200); atk=28+Math.floor(Math.random()*10);
    turnLimit=8+Math.floor(Math.random()*5);
    const bosses=[
      {name:"超高分子ラジカル塊",weakness:["Aromatic","Explosive"],condition:"Aromatic"},
      {name:"濃縮フリーラジカル核",weakness:["Acid","Oxidant"],condition:"Alcohol"},
      {name:"芳香族クラスター体",weakness:["Halogen","Reagent"],condition:"Ester"}
    ];
    const b=bosses[Math.floor(Math.random()*bosses.length)];
    name="【BOSS】"+b.name; weakness=b.weakness; condition=b.condition;
  }else{
    level=1+Math.floor(Math.random()*3); colorHex=level===1?0x22c55e:(level===2?0xf97316:0xef4444);
    hp=450+level*30; atk=12+level*8;
    name=["アルキル変異体","環状高分子体","フリーラジカル塊"][level-1];
    const pool=["Aromatic","Alkenyl","Acid","Alcohol","Halogen","Oxidant","Phenol","Explosive"];
    weakness=[pool[Math.floor(Math.random()*pool.length)]];
  }
  const mesh=createMoleculeMesh(colorHex); mesh.position.set((Math.random()-.5)*18,.5,-Math.random()*12-2); scene.add(mesh);
  monsters.push({name,level,hp,maxHP:hp,attackPower:atk,mesh,isActive:true,weakness,isBoss,condition,turnLimit,vx:0,vz:0,changeDirTimer:0});
}

let labScene,labCamera,labRenderer,enemyMesh;
function initLabThreeJS(){
  const cont=document.getElementById('lab-canvas-container'); cont.innerHTML="";
  labScene=new THREE.Scene(); labScene.background=new THREE.Color(0x071018);
  labCamera=new THREE.PerspectiveCamera(50,cont.clientWidth/cont.clientHeight,.1,100); labCamera.position.set(0,1.6,5.2); labCamera.lookAt(0,.7,0);
  labRenderer=new THREE.WebGLRenderer({antialias:true}); labRenderer.setSize(cont.clientWidth,cont.clientHeight); labRenderer.setPixelRatio(Math.min(devicePixelRatio,2)); cont.appendChild(labRenderer.domElement);
  const key=new THREE.DirectionalLight(0x67e8f9,1.7); key.position.set(2,3,4); labScene.add(key);
  labScene.add(new THREE.AmbientLight(0xffffff,.45));
  const rim=new THREE.DirectionalLight(0xa78bfa,.6); rim.position.set(-3,1,-2); labScene.add(rim);
  const col=gameState.currentMonster?.isBoss?0x7c3aed:0x22d3ee;
  enemyMesh=createMoleculeMesh(col); enemyMesh.scale.set(1.45,1.45,1.45); enemyMesh.position.set(0,.9,0); labScene.add(enemyMesh);
  (function anim(){requestAnimationFrame(anim); if(enemyMesh){enemyMesh.rotation.y+=.014; enemyMesh.position.y=.9+Math.sin(Date.now()*.002)*.08;} labRenderer.render(labScene,labCamera);})();
}

let bDeck=[],bHand=[],bSelected=[],monsterHP=500,isPlayerTurn=true,activeQuiz=null,pendingDamage=0,pendingHeal=0;

function startBattle(practice){
  isPractice=!!practice;
  document.querySelectorAll('.screen').forEach(el=>el.classList.remove('active'));
  document.getElementById('battle-screen').classList.add('active');
  if(!isPractice) initLabThreeJS();
  else document.getElementById('lab-canvas-container').innerHTML="<div style='display:flex;align-items:center;justify-content:center;height:100%;color:#67e8f9'>練習モード（敵なし）</div>";
  setupBattle();
}
function startPractice(){
  gameState.currentMonster={name:"練習用ダミー",level:1,hp:9999,maxHP:9999,attackPower:0,weakness:[],isBoss:false,condition:null,turnLimit:0};
  startBattle(true);
}

function setupBattle(){
  isBattleOver=false; isProcessing=false; botulinumActive=false; gameState.nextDamageBonus=1.0; pendingIntermediate=null;
  battleHistory=[]; battleTurnCount=0;
  bossTurnLimit=gameState.currentMonster?.turnLimit||0;
  if(!isPractice) gameState.playerHP=gameState.playerMaxHP;
  document.getElementById('next-bonus').style.display='none';
  document.getElementById('dot-status').style.display='none';
  document.getElementById('choice-box').style.display='none';
  const tl=document.getElementById('turn-limit');
  if(bossTurnLimit>0){tl.style.display='block'; tl.innerText=`⏱ ターン制限: 残り${bossTurnLimit}`;}
  else tl.style.display='none';
  bDeck=[...gameState.currentDeck].sort(()=>Math.random()-.5); bHand=[]; bSelected=[];
  monsterHP=gameState.currentMonster?.hp||500;
  document.getElementById('monster-name').innerText=gameState.currentMonster.name;
  document.getElementById('monster-level').innerText=gameState.currentMonster.level;
  document.getElementById('monster-maxhp').innerText=gameState.currentMonster.maxHP;
  document.getElementById('monster-hp').innerText=monsterHP;
  document.getElementById('battle-player-hp').innerText=gameState.playerHP;
  const weak=gameState.currentMonster.weakness||[];
  document.getElementById('monster-weak').innerText=weak.length?`弱点: ${weak.join(",")}`:"";
  document.getElementById('monster-cond').innerText=gameState.currentMonster.condition?`条件: ${gameState.currentMonster.condition}系のみ有効`:"";
  for(let i=0;i<5;i++) drawCard();
  startPlayerTurn(true);
}

function pushHistory(msg){battleHistory.push(msg); if(battleHistory.length>40) battleHistory.shift();}

function startPlayerTurn(first=false){
  if(isBattleOver) return;
  isPlayerTurn=true; isProcessing=false;
  if(!first) battleTurnCount++;
  if(bossTurnLimit>0 && !isPractice){
    const left=bossTurnLimit-battleTurnCount;
    document.getElementById('turn-limit').innerText=`⏱ ターン制限: 残り${Math.max(0,left)}`;
    if(left<=0){
      isBattleOver=true;
      document.getElementById('battle-log').innerText="⏱ ターン切れ！ ボスが暴走して敗北…";
      pushHistory("ターン切れ敗北");
      setTimeout(()=>{gameState.playerHP=gameState.playerMaxHP;switchState('field');},1800);
      return;
    }
  }
  if(botulinumActive && monsterHP>0 && !isPractice){
    monsterHP-=200; document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);
    pushHistory("ボツリヌス毒素: 200ダメージ");
    if(monsterHP<=0){winBattle("☠️ ボツリヌス毒素が敵を分解！"); return;}
  }
  if(!first) drawCard();
  document.getElementById('battle-log').innerText=first?(isPractice?"練習モード：自由に反応を試せます":"カードを選んで化学反応を実行！"):"あなたのターン！";
  updateBattleUI();
}

function drawCard(){if(bHand.length<7&&bDeck.length>0) bHand.push(bDeck.shift());}
function formatPower(v){return v===Infinity?"∞":v;}
function powerValue(c){
  if(c.name==="ボツリヌス毒素") return 200;
  if(c.attackPower===Infinity) return 99999;
  if(c.healPower>0) return c.healPower;
  return c.attackPower||0;
}

function updateBattleUI(){
  document.getElementById('battle-deck-count').innerText=bDeck.length;
  document.getElementById('hand-count').innerText=bHand.length;
  const cont=document.getElementById('hand-cards'); cont.innerHTML="";
  bHand.forEach(card=>{
    const sel=bSelected.some(c=>c.id===card.id);
    const div=document.createElement('div'); div.className=`card ${sel?'selected':''}`;
    let pressTimer=null;
    div.addEventListener('pointerdown',e=>{
      e.preventDefault();
      pressTimer=setTimeout(()=>{showLongPress(card); pressTimer=null;},450);
    });
    div.addEventListener('pointerup',()=>{
      if(pressTimer){clearTimeout(pressTimer);pressTimer=null; toggleSelectCard(card);}
    });
    div.addEventListener('pointerleave',()=>{if(pressTimer){clearTimeout(pressTimer);pressTimer=null;}});
    div.addEventListener('pointercancel',()=>{if(pressTimer){clearTimeout(pressTimer);pressTimer=null;}});
    let val=card.name==="ボツリヌス毒素"?`<div style="font-size:9px;color:#dc2626">継続200</div>`:
            card.healPower>0?`<div style="font-size:10px;color:#16a34a">回復+${card.healPower}</div>`:
            `<div style="font-size:10px;color:#dc2626">威力:${formatPower(card.attackPower)}</div>`;
    div.innerHTML=`<div class="card-rarity rarity-${card.rarity}">${card.rarity}</div><div style="font-size:11px;line-height:1.2">${card.name}</div><div style="font-size:9px;color:#64748b">${card.formula}</div><div class="card-attr">${card.attribute}</div>${val}`;
    cont.appendChild(div);
  });
  const can=isPlayerTurn&&!activeQuiz&&!isProcessing&&!isBattleOver;
  document.getElementById('attack-btn').disabled=!(can&&bSelected.length>0);
  document.getElementById('skip-btn').disabled=!can;
  document.getElementById('flee-btn').disabled=!can;
}

function showLongPress(card){
  document.getElementById('lp-title').innerText=`${card.name} でできる反応`;
  const body=CARD_REACTIONS[card.name]
    || (card.healPower>0 ? "回復カード（複合反応なし）" : "単体投擲が可能です");
  document.getElementById('lp-body').innerText=body;
  document.getElementById('longpress-popup').style.display='block';
}
function closeLongPress(){document.getElementById('longpress-popup').style.display='none';}

function toggleSelectCard(card){
  if(!isPlayerTurn||activeQuiz||isBattleOver||isProcessing) return;
  const idx=bSelected.findIndex(c=>c.id===card.id);
  if(idx>=0) bSelected.splice(idx,1); else bSelected.push(card);
  updateBattleUI();
}

function skipTurn(){
  if(!isPlayerTurn||isBattleOver||isProcessing||activeQuiz) return;
  isProcessing=true; bSelected=[]; document.getElementById('battle-log').innerText="ターン終了…";
  pushHistory("ターン終了"); updateBattleUI(); setTimeout(endPlayerTurn,700);
}
function fleeBattle(){
  if(!isPlayerTurn||isBattleOver||isProcessing) return;
  isBattleOver=true; isProcessing=true;
  document.getElementById('battle-log').innerText=isPractice?"練習を終了しました":"🏃 脱出した…";
  pushHistory(isPractice?"練習終了":"脱出");
  setTimeout(()=>switchState('field'),1100);
}

function winBattle(msg){
  isBattleOver=true;
  if(isPractice){
    document.getElementById('battle-log').innerText="練習終了（報酬なし）";
    setTimeout(()=>switchState('field'),1200);
    return;
  }
  gameState.kills++;
  if(gameState.currentMonster?.isBoss) gameState.flags.boss=true;
  checkRankUp(); checkAchievements();
  const rank=getRank();
  let reward=Math.floor((55+(gameState.currentMonster?.level||1)*28)*(rank.reagentBonus));
  if(gameState.currentMonster?.isBoss) reward+=100;
  gameState.reagents+=reward;
  document.getElementById('battle-log').innerText=`${msg}\n試薬 +${reward} ／ 撃破数 ${gameState.kills}`;
  pushHistory(msg+` / +${reward}`);
  setTimeout(()=>switchState('field'),1700);
}

function executePlayerAttack(){
  if(isBattleOver||!isPlayerTurn||isProcessing||activeQuiz||bSelected.length===0) return;
  isProcessing=true;
  document.getElementById('attack-btn').disabled=true;
  document.getElementById('skip-btn').disabled=true;
  document.getElementById('flee-btn').disabled=true;

  let baseDamage=0, baseHeal=0, quizToSet=null, logMessage="", product=null, appliedEffect=null;
  const n=bSelected.map(c=>c.name);
  const hasCatalyst = n.includes("濃硫酸") || n.includes("重合触媒(Ziegler)") || n.includes("塩化アルミニウム") || n.includes("鉄");
  const catMul = hasCatalyst ? 2.0 : 1.5;
  const bossCond=gameState.currentMonster?.condition||null;
  function dmgLog(text,dmg){return text+"\n相手に "+(dmg===Infinity?"∞":dmg)+" ダメージ！";}

  if(n.includes("アニリン")&&n.includes("無水酢酸")){
    product={name:"アセトアニリド",formula:"C6H5NHCOCH3",attackPower:60,healPower:0,attribute:"Aromatic",rarity:"SR",color:"白色",odor:"-"};
    baseDamage=Math.floor(80*catMul); logMessage=dmgLog("🧪 アニリンのアセチル化 → アセトアニリド 生成！",baseDamage); markFlag("acetyl");
    quizToSet={question:"アニリンをアセチル化すると？",options:["アセトアニリド","ニトロベンゼン","フェノール","アゾベンゼン"],correctIndex:0,explanation:"正解！アセトアニリドです。"};
  }
  else if(n.includes("サリチル酸")&&n.includes("無水酢酸")){
    product={name:"アセチルサリチル酸",formula:"C9H8O4",attackPower:120,healPower:0,attribute:"Ester",rarity:"SSR",color:"白色",odor:"-"};
    baseDamage=Math.floor(120*catMul); logMessage=dmgLog("🧪 サリチル酸のアセチル化 → アセチルサリチル酸！",baseDamage); markFlag("acetyl");
  }
  else if(n.includes("エタノール")&&n.includes("濃硫酸")){
    baseDamage=Math.floor(100*catMul); logMessage=dmgLog("🧪 エタノールの脱水 → エチレン 生成！",baseDamage); markFlag("dehyd");
    quizToSet={question:"エタノールを濃硫酸で加熱脱水すると？",options:["エチレン","ジエチルエーテル","アセトアルデヒド","酢酸"],correctIndex:0,explanation:"正解！エチレンが主生成物になります。"};
  }
  else if(n.includes("1-プロパノール")&&n.includes("濃硫酸")){
    baseDamage=Math.floor(105*catMul); logMessage=dmgLog("🧪 1-プロパノールの脱水 → プロピレン 生成！",baseDamage); markFlag("dehyd");
  }
  else if(n.includes("ベンゼン")&&n.includes("ニトロ基")){
    product={name:"ニトロベンゼン",formula:"C6H5NO2",attackPower:70,healPower:0,attribute:"Aromatic",rarity:"SR",color:"淡黄色",odor:"アーモンド様"};
    baseDamage=Math.floor(70*catMul); logMessage=dmgLog("🧪 ベンゼン + ニトロ基 → ニトロベンゼン が生成！",baseDamage); markFlag("nitro");
    quizToSet={question:"ベンゼンのニトロ化の反応機構は？",options:["求電子置換","求核置換","付加反応","脱離反応"],correctIndex:0,explanation:"正解！求電子置換です。"};
  }
  else if(n.includes("ニトロベンゼン")&&(n.includes("還元剤")||n.includes("水素化ホウ素ナトリウム"))){
    product={name:"アニリン",formula:"C6H5NH2",attackPower:65,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色〜褐色",odor:"特異臭"};
    baseDamage=Math.floor(65*catMul); logMessage=dmgLog("🧪 ニトロベンゼンの還元 → アニリン が生成！",baseDamage);
    quizToSet={question:"ニトロベンゼンを還元すると？",options:["アニリン","フェノール","ベンゼン","トルエン"],correctIndex:0,explanation:"正解！アニリンです。"};
  }
  else if(n.includes("アニリン")&&n.includes("ジアゾ化剤")){
    product={name:"アゾベンゼン",formula:"C6H5N=NC6H5",attackPower:110,healPower:0,attribute:"Aromatic",rarity:"SSR",color:"橙赤色",odor:"無臭"};
    baseDamage=Math.floor(110*catMul); logMessage=dmgLog("🧪 ジアゾ化 → アゾベンゼン が生成！",baseDamage);
    quizToSet={question:"アニリンのジアゾ化に必要な試薬は？",options:["NaNO2 + HCl","HNO3","H2SO4","NaOH"],correctIndex:0,explanation:"正解！亜硝酸ナトリウムと塩酸です。"};
  }
  else if(n.includes("酢酸")&&n.includes("エタノール")){
    product={name:"酢酸エチル",formula:"CH3COOC2H5",attackPower:Math.floor(55*catMul),healPower:0,attribute:"Ester",rarity:"R",color:"無色",odor:"果実様香気"};
    baseDamage=Math.floor(55*catMul); logMessage=dmgLog("🧪 エステル化 → 酢酸エチル が生成！",baseDamage); markFlag("ester");
    quizToSet={question:"エステル化の触媒として一般的なのは？",options:["濃硫酸","NaOH","KMnO4","Fe"],correctIndex:0,explanation:"正解！濃硫酸です。"};
  }
  else if(bSelected.length===1&&bSelected[0].name==="ボツリヌス毒素"){
    botulinumActive=true; document.getElementById('dot-status').style.display='block';
    logMessage="☠️ ボツリヌス毒素を散布！\n毎ターン200ダメージが継続します"; baseDamage=0;
  }
  else if(bSelected.length===1&&bSelected[0].name==="フッ化水素酸"){
    if(Math.random()<.1){
      isBattleOver=true; document.getElementById('battle-log').innerText="☠️ 自分にかかってしまった！ 敗北…\n試薬-25";
      gameState.reagents=Math.max(0,gameState.reagents-25);
      setTimeout(()=>{gameState.playerHP=gameState.playerMaxHP;switchState('field');},2000);
      bHand=bHand.filter(c=>!bSelected.some(s=>s.id===c.id)); bSelected=[]; updateBattleUI(); return;
    }
    baseDamage=Infinity; logMessage=dmgLog("☠️ フッ化水素酸を投擲！",Infinity);
  }
  else if(bSelected.length===1&&(bSelected[0].name==="トリニトロトルエン"||bSelected[0].name==="ピクリン酸")){
    baseDamage=180; logMessage=dmgLog(`💥 ${bSelected[0].name} を起爆！`,180);
    quizToSet={question:"TNTの原料となる芳香族は？",options:["トルエン","ベンゼン","フェノール","アニリン"],correctIndex:0,explanation:"正解！トルエンです。"};
  }
  else if(n.includes("水酸化ナトリウム")&&(n.includes("トリパルミチン")||n.includes("トリステアリン")||n.includes("トリオレイン"))){
    baseDamage=Math.floor(230*catMul); appliedEffect="saponification"; logMessage=dmgLog("🧪 油脂のけん化！ セッケンとグリセリンが生成！",baseDamage); markFlag("sapon"); markFlag("fat");
    quizToSet={question:"油脂のけん化で生じるアルコールは？",options:["グリセリン","エタノール","メタノール","フェノール"],correctIndex:0,explanation:"正解！グリセリンです。"};
  }
  else if(n.includes("水酸化ナトリウム")&&(n.includes("酢酸")||n.includes("酢酸エチル")||n.includes("オレイン酸"))){
    baseDamage=Math.floor(210*catMul); appliedEffect="saponification"; logMessage=dmgLog("🧪 けん化反応が進行！",baseDamage); markFlag("sapon");
  }
  else if(n.includes("ベンゼン")&&n.includes("濃硝酸")){
    baseDamage=Math.floor(130*catMul); logMessage=dmgLog("🧪 ベンゼンのニトロ化が進行！",baseDamage); markFlag("nitro");
    quizToSet={question:"ベンゼンのニトロ化生成物は？",options:["ニトロベンゼン","安息香酸","フェノール","クロロベンゼン"],correctIndex:0,explanation:"正解！ニトロベンゼンです。"};
  }
  else if(n.includes("トルエン")&&n.includes("濃硝酸")){
    baseDamage=Math.floor(220*catMul); logMessage=dmgLog("🧪 トルエンのニトロ化が進行！",baseDamage); markFlag("nitro");
    quizToSet={question:"トルエンがベンゼンよりニトロ化されやすい理由は？",options:["メチル基の電子供与性","メチル基の電子求引性","立体障害","水素結合"],correctIndex:0,explanation:"正解！電子供与性です。"};
  }
  else if(n.includes("フェノール")&&n.includes("濃硝酸")){
    baseDamage=Math.floor(150*catMul); logMessage=dmgLog("🧪 フェノールのニトロ化が進行！",baseDamage); markFlag("nitro");
  }
  else if(n.includes("ベンゼン")&&n.includes("濃硫酸")){
    baseDamage=Math.floor(150*catMul); logMessage=dmgLog("🧪 ベンゼンのスルホン化 → ベンゼンスルホン酸！",baseDamage);
    quizToSet={question:"ベンゼンのスルホン化生成物は？",options:["ベンゼンスルホン酸","フェノール","ニトロベンゼン","安息香酸"],correctIndex:0,explanation:"正解！ベンゼンスルホン酸です。"};
  }
  else if(n.includes("ナフタレン")&&n.includes("濃硫酸")){baseDamage=Math.floor(160*catMul); logMessage=dmgLog("🧪 ナフタレンのスルホン化！",baseDamage);}
  else if(n.includes("ベンゼン")&&(n.includes("塩素")||n.includes("臭素"))&&(n.includes("鉄")||n.includes("塩化アルミニウム")||hasCatalyst)){
    baseDamage=Math.floor(140*catMul); logMessage=dmgLog("🧪 ベンゼンのハロゲン化（求電子置換）！",baseDamage);
    quizToSet={question:"ベンゼンの塩素化に使う触媒は？",options:["Fe または FeCl3","NaOH","KMnO4","白金"],correctIndex:0,explanation:"正解！ルイス酸触媒です。"};
  }
  else if(n.includes("エチレン")&&(n.includes("臭素")||n.includes("塩素"))){
    baseDamage=Math.floor(140*catMul); logMessage=dmgLog("🧪 エチレンへのハロゲン付加！（脱色）",baseDamage);
    quizToSet={question:"エチレンに臭素水を加えると？",options:["赤褐色が消える","色が濃くなる","沈殿が生じる","発光する"],correctIndex:0,explanation:"正解！付加で脱色します。"};
  }
  else if(n.includes("アセチレン")&&n.includes("臭素")){baseDamage=Math.floor(160*catMul); logMessage=dmgLog("🧪 アセチレンへの臭素付加！",baseDamage);}
  else if(n.includes("シス-2-ブテン")&&n.includes("臭素")){baseDamage=Math.floor(130*catMul); logMessage=dmgLog("🧪 シス-2-ブテンへの臭素付加！",baseDamage);}
  else if(n.includes("トランス-2-ブテン")&&n.includes("臭素")){baseDamage=Math.floor(130*catMul); logMessage=dmgLog("🧪 トランス-2-ブテンへの臭素付加！",baseDamage);}
  else if(n.includes("エチレン")&&n.includes("重合触媒(Ziegler)")){
    baseDamage=Math.floor(300*catMul); logMessage=dmgLog("🧪 エチレンの重合 → ポリエチレン！",baseDamage); markFlag("poly");
    quizToSet={question:"Ziegler触媒で得られるポリエチレンの特徴は？",options:["高密度・直鎖状","低密度・分岐","環状","三次元網目"],correctIndex:0,explanation:"正解！HDPEです。"};
  }
  else if(n.includes("スチレン")&&n.includes("重合触媒(Ziegler)")){baseDamage=Math.floor(250*catMul); logMessage=dmgLog("🧪 スチレンの重合 → ポリスチレン！",baseDamage); markFlag("poly");}
  else if(n.includes("プロピレン")&&n.includes("重合触媒(Ziegler)")){baseDamage=Math.floor(260*catMul); logMessage=dmgLog("🧪 プロピレンの重合 → ポリプロピレン！",baseDamage); markFlag("poly");}
  else if(n.includes("ビニル基")&&n.includes("重合触媒(Ziegler)")){baseDamage=Math.floor(220*catMul); logMessage=dmgLog("🧪 ビニル基の重合！",baseDamage); markFlag("poly");}
  else if((n.includes("エタノール")||n.includes("アセトアルデヒド")||n.includes("メタノール"))&&(n.includes("過マンガン酸カリウム")||n.includes("二クロム酸カリウム"))){
    baseDamage=Math.floor(170*catMul); appliedEffect="oxidation"; logMessage=dmgLog("🧪 酸化反応が進行！",baseDamage); markFlag("oxid");
    quizToSet={question:"第一級アルコールを酸化すると最終的に？",options:["カルボン酸","ケトン","エーテル","アルケン"],correctIndex:0,explanation:"正解！カルボン酸です。"};
  }
  else if(n.includes("2-プロパノール")&&(n.includes("過マンガン酸カリウム")||n.includes("二クロム酸カリウム"))){
    baseDamage=Math.floor(160*catMul); logMessage=dmgLog("🧪 第二級アルコールの酸化 → ケトン！",baseDamage); markFlag("oxid");
    quizToSet={question:"第二級アルコールの酸化生成物は？",options:["ケトン","カルボン酸","アルデヒド","エーテル"],correctIndex:0,explanation:"正解！ケトンです。"};
  }
  else if(n.includes("トルエン")&&n.includes("過マンガン酸カリウム")){
    baseDamage=Math.floor(190*catMul); logMessage=dmgLog("🧪 トルエン側鎖酸化 → 安息香酸！",baseDamage); markFlag("oxid");
    quizToSet={question:"トルエンをKMnO4で酸化すると？",options:["安息香酸","フェノール","ベンゼン","ベンズアルデヒド"],correctIndex:0,explanation:"正解！安息香酸です。"};
  }
  else if((n.includes("エタノール")||n.includes("メタノール")||n.includes("1-プロパノール"))&&n.includes("金属ナトリウム")){
    baseDamage=Math.floor(120*catMul); logMessage=dmgLog("🧪 アルコール + Na → アルコキシド＆水素発生！",baseDamage);
    quizToSet={question:"アルコールと金属Naの反応で発生する気体は？",options:["水素","酸素","二酸化炭素","塩素"],correctIndex:0,explanation:"正解！水素です。"};
  }
  else if(n.includes("フェノール")&&n.includes("金属ナトリウム")){baseDamage=Math.floor(140*catMul); logMessage=dmgLog("🧪 フェノール + Na → ナトリウムフェノキシド！",baseDamage);}
  else if((n.includes("o-クレゾール")||n.includes("m-クレゾール")||n.includes("p-クレゾール"))&&n.includes("金属ナトリウム")){baseDamage=Math.floor(135*catMul); logMessage=dmgLog("🧪 クレゾール + Na → ナトリウム塩！",baseDamage);}
  else if(bSelected.length===1&&bSelected[0].name==="アントラセン"){baseDamage=120; logMessage=dmgLog("⚗️ アントラセンを投擲！",120);}
  else if(bSelected.length===1&&bSelected[0].name==="ナフタレン"){baseDamage=55; logMessage=dmgLog("⚗️ ナフタレンを投擲！",55);}
  else if(n.includes("ナフタレン")&&n.includes("濃硝酸")){baseDamage=Math.floor(170*catMul); logMessage=dmgLog("🧪 ナフタレンのニトロ化！",baseDamage); markFlag("nitro");}
  else if(n.includes("アントラセン")&&n.includes("濃硝酸")){baseDamage=Math.floor(200*catMul); logMessage=dmgLog("🧪 アントラセンのニトロ化！",baseDamage); markFlag("nitro");}
  else if(n.includes("メチル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(50*catMul); logMessage=dmgLog("🧪 メタノール生成！",baseDamage);}
  else if(n.includes("エチル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(60*catMul); logMessage=dmgLog("🧪 エタノール生成！",baseDamage);}
  else if(n.includes("プロピル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(65*catMul); logMessage=dmgLog("🧪 プロパノール生成！",baseDamage);}
  else if(n.includes("イソプロピル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(70*catMul); logMessage=dmgLog("🧪 イソプロパノール生成！",baseDamage);}
  else if(n.includes("ブチル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(75*catMul); logMessage=dmgLog("🧪 ブタノール生成！",baseDamage);}
  else if(n.includes("フェニル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(90*catMul); logMessage=dmgLog("🧪 フェノール生成！",baseDamage);}
  else if(n.includes("ベンジル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(80*catMul); logMessage=dmgLog("🧪 ベンジルアルコール生成！",baseDamage);}
  else if(n.includes("ビニル基")&&n.includes("ヒドロキシ基")){baseDamage=Math.floor(70*catMul); logMessage=dmgLog("🧪 ビニルアルコール生成！",baseDamage);}
  else if((n.includes("メチル基")||n.includes("エチル基")||n.includes("プロピル基")||n.includes("ブチル基"))&&n.includes("カルボキシ基")){baseDamage=Math.floor(85*catMul); logMessage=dmgLog("🧪 カルボン酸生成！",baseDamage);}
  else if((n.includes("メチル基")||n.includes("エチル基")||n.includes("プロピル基")||n.includes("ブチル基"))&&n.includes("アミノ基")){baseDamage=Math.floor(55*catMul); logMessage=dmgLog("🧪 アミン生成！",baseDamage);}
  else if((n.includes("メチル基")||n.includes("エチル基")||n.includes("プロピル基")||n.includes("ブチル基"))&&n.includes("アルデヒド基")){baseDamage=Math.floor(70*catMul); logMessage=dmgLog("🧪 アルデヒド生成！",baseDamage);}
  else if((n.includes("メチル基")||n.includes("エチル基")||n.includes("プロピル基")||n.includes("ブチル基"))&&n.includes("ニトロ基")){baseDamage=Math.floor(95*catMul); logMessage=dmgLog("🧪 ニトロ化合物生成！",baseDamage);}
  else if((n.includes("メチル基")||n.includes("エチル基")||n.includes("プロピル基")||n.includes("ブチル基"))&&n.includes("スルホン基")){baseDamage=Math.floor(90*catMul); logMessage=dmgLog("🧪 スルホン酸生成！",baseDamage);}
  else if((n.includes("メチル基")||n.includes("エチル基")||n.includes("プロピル基")||n.includes("ブチル基"))&&n.includes("ハロゲン基")){baseDamage=Math.floor(65*catMul); logMessage=dmgLog("🧪 ハロゲン化アルキル生成！",baseDamage);}
  else if(n.includes("フェニル基")&&n.includes("カルボキシ基")){baseDamage=Math.floor(100*catMul); logMessage=dmgLog("🧪 安息香酸生成！",baseDamage);}
  else if(n.includes("フェニル基")&&n.includes("アミノ基")){baseDamage=Math.floor(75*catMul); logMessage=dmgLog("🧪 アニリン生成！",baseDamage);}
  else if(n.includes("フェニル基")&&n.includes("ニトロ基")){baseDamage=Math.floor(110*catMul); logMessage=dmgLog("🧪 ニトロベンゼン生成！",baseDamage);}
  else if(n.includes("フェニル基")&&n.includes("スルホン基")){baseDamage=Math.floor(105*catMul); logMessage=dmgLog("🧪 ベンゼンスルホン酸生成！",baseDamage);}
  else if(n.includes("フェニル基")&&n.includes("ハロゲン基")){baseDamage=Math.floor(80*catMul); logMessage=dmgLog("🧪 ハロゲン化ベンゼン生成！",baseDamage);}
  else if(n.includes("ベンジル基")&&n.includes("カルボキシ基")){baseDamage=Math.floor(95*catMul); logMessage=dmgLog("🧪 フェニル酢酸生成！",baseDamage);}
  else if(n.includes("ベンジル基")&&n.includes("アミノ基")){baseDamage=Math.floor(70*catMul); logMessage=dmgLog("🧪 ベンジルアミン生成！",baseDamage);}
  else if(bSelected.length===1){
    const s=bSelected[0];
    if(s.healPower>0){baseHeal=s.healPower; logMessage=`🧪 ${s.name} を使用！\nHPが ${baseHeal} 回復した！`;}
    else{baseDamage=s.attackPower; logMessage=`⚗️ ${s.name} を投擲！\n相手に ${formatPower(baseDamage)} ダメージ！`;}
  }else{
    const healSum=bSelected.reduce((a,c)=>a+c.healPower,0);
    if(healSum>0){baseHeal=healSum; logMessage=`🧪 複合回復！\nHPが ${healSum} 回復した！`;}
    else logMessage="⚠️ 不活性な組み合わせだった…";
  }

  if(bossCond && baseDamage>0 && baseDamage!==Infinity && !isPractice){
    const attrs=bSelected.map(c=>c.attribute);
    const ok=attrs.includes(bossCond)||(product&&product.attribute===bossCond)||
             (bossCond==="Ester"&&n.includes("酢酸")&&n.includes("エタノール"))||
             (bossCond==="Alcohol"&&(n.includes("エタノール")||n.includes("ヒドロキシ基")||n.includes("メタノール")));
    if(!ok){baseDamage=0; logMessage+=`\n❌ ボス条件「${bossCond}系のみ」を満たさず無効`;}
  }

  let weaknessBonus=1.0;
  if(gameState.currentMonster?.weakness){
    const attrs=bSelected.map(c=>c.attribute);
    if(attrs.some(a=>gameState.currentMonster.weakness.includes(a))) weaknessBonus=1.5;
  }
  let finalBase=baseDamage;
  if(finalBase!==Infinity && finalBase>0) finalBase=Math.floor(finalBase*gameState.nextDamageBonus*weaknessBonus);
  if(finalBase!==baseDamage && finalBase>0 && baseDamage!==Infinity){
    logMessage=logMessage.replace(/相手に .+ ダメージ！/,`相手に ${finalBase} ダメージ！`);
  }

  if(appliedEffect==="oxidation"){gameState.nextDamageBonus=1.3; document.getElementById('next-bonus').style.display='block'; document.getElementById('next-bonus').innerText="次ターン火力+30%";}
  else if(appliedEffect==="saponification"){gameState.nextDamageBonus=1.2; document.getElementById('next-bonus').style.display='block'; document.getElementById('next-bonus').innerText="次ターン火力+20%";}
  else if(baseDamage>0||baseHeal>0){gameState.nextDamageBonus=1.0; document.getElementById('next-bonus').style.display='none';}

  bHand=bHand.filter(c=>!bSelected.some(s=>s.id===c.id));
  bSelected=[];

  if(product){
    pendingIntermediate={card:{...product,id:Math.random().toString(36).substr(2,9)}, damage:finalBase, heal:baseHeal, msg:logMessage, weak:weaknessBonus>1};
    document.getElementById('choice-title').innerText=`${product.name} が生成された！`;
    document.getElementById('choice-desc').innerText=`攻撃力 ${product.attackPower} ／ 属性 ${product.attribute}`;
    document.getElementById('choice-box').style.display='flex';
    updateBattleUI(); return;
  }
  if(quizToSet){pendingDamage=finalBase; pendingHeal=baseHeal; activeQuiz=quizToSet; showQuiz(quizToSet);}
  else applyEffectAndEndTurn(finalBase,baseHeal,logMessage,weaknessBonus>1);
}

function chooseAttack(){
  document.getElementById('choice-box').style.display='none';
  if(!pendingIntermediate) return;
  const p=pendingIntermediate;
  applyEffectAndEndTurn(p.damage,p.heal,p.msg+(p.weak?"\n💥 弱点を突いた！":""),p.weak);
  pendingIntermediate=null;
}
function chooseAddToHand(){
  document.getElementById('choice-box').style.display='none';
  if(!pendingIntermediate) return;
  if(bHand.length<7) bHand.push(pendingIntermediate.card);
  gameState.collection.push({...pendingIntermediate.card});
  document.getElementById('battle-log').innerText=`${pendingIntermediate.card.name} を手札に加えた！`;
  pushHistory(pendingIntermediate.card.name+"を手札へ");
  pendingIntermediate=null;
  isProcessing=false;
  updateBattleUI();
  setTimeout(endPlayerTurn,1200);
}

function showQuiz(q){
  document.getElementById('battle-log').style.display='none';
  document.getElementById('quiz-container').style.display='flex';
  document.getElementById('quiz-question').innerText=q.question;
  const box=document.getElementById('quiz-options'); box.innerHTML="";
  const ch=q.options.map((t,i)=>({text:t,ok:i===q.correctIndex})).sort(()=>Math.random()-.5);
  ch.forEach(c=>{const b=document.createElement('button'); b.className='quiz-btn'; b.innerText=c.text; b.onclick=()=>answerQuiz(c.ok); box.appendChild(b);});
  updateBattleUI();
}
function answerQuiz(ok){
  let dmg=0,heal=0,log="";
  if(ok){dmg=pendingDamage===Infinity?Infinity:Math.floor(pendingDamage*1.5); heal=Math.floor(pendingHeal*1.5); log=`⭕ 正解！ ${activeQuiz.explanation}\n相手に ${formatPower(dmg)} ダメージ！`;}
  else log="❌ 不正解… 効果0";
  document.getElementById('quiz-container').style.display='none';
  document.getElementById('battle-log').style.display='flex';
  activeQuiz=null; applyEffectAndEndTurn(dmg,heal,log,false);
}

function applyEffectAndEndTurn(damage,heal,message,isWeak=false){
  if(isBattleOver) return;
  if(damage===Infinity||damage>=400){
    if(gameState.reagents>=25){gameState.reagents-=25; message+="\n🧪 試薬25消費";}
    else if(damage!==Infinity){damage=Math.floor(damage*.5); message+="\n⚠️ 試薬不足で半減";}
  }
  if(isWeak) message+="\n💥 弱点を突いた！";
  if(damage===Infinity) monsterHP=0; else if(damage>0) monsterHP-=damage;
  if(heal>0){gameState.playerHP=Math.min(gameState.playerMaxHP,gameState.playerHP+heal); document.getElementById('battle-player-hp').innerText=gameState.playerHP;}
  document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);
  document.getElementById('battle-log').innerText=message;
  pushHistory(message);
  if(monsterHP<=0) winBattle(isPractice?"練習：仮想敵を分解！":"🎉 敵分子を分解！");
  else setTimeout(endPlayerTurn,1500);
}

function endPlayerTurn(){
  if(isBattleOver) return;
  if(isPractice){startPlayerTurn(); return;}
  isPlayerTurn=false; isProcessing=true;
  document.getElementById('battle-log').innerText="👾 敵の反撃…"; updateBattleUI();
  setTimeout(()=>{
    if(isBattleOver) return;
    if(monsterHP>0){
      let atk=gameState.currentMonster?.attackPower||15;
      if(bossTurnLimit>0 && battleTurnCount>=bossTurnLimit-2) atk=Math.floor(atk*1.5);
      gameState.playerHP-=atk;
      document.getElementById('battle-player-hp').innerText=Math.max(0,gameState.playerHP);
      const msg=`👾 敵の攻撃！\nあなたに ${atk} ダメージ！`;
      document.getElementById('battle-log').innerText=msg; pushHistory(msg);
      if(gameState.playerHP<=0){
        isBattleOver=true; gameState.playerHP=0;
        gameState.reagents=Math.max(0,gameState.reagents-25);
        document.getElementById('battle-log').innerText="💀 敗北… 試薬-25";
        setTimeout(()=>{gameState.playerHP=gameState.playerMaxHP; switchState('field');},1500);
        return;
      }
      setTimeout(()=>{if(!isBattleOver) startPlayerTurn();},1200);
    }else if(!isBattleOver) startPlayerTurn();
  },850);
}

function sortDeck(mode){
  const names=[...new Set(gameState.collection.map(c=>c.name))];
  const getRep=name=>gameState.collection.find(c=>c.name===name)||ALL_CARDS.find(c=>c.name===name);
  names.sort((a,b)=>{
    const ca=getRep(a), cb=getRep(b);
    if(!ca||!cb) return 0;
    let cmp=0;
    if(mode==='name') cmp=a.localeCompare(b,'ja');
    else if(mode==='rarity'){
      cmp=(RARITY_ORDER[ca.rarity]??9)-(RARITY_ORDER[cb.rarity]??9);
      if(cmp===0) cmp=a.localeCompare(b,'ja');
    }else if(mode==='power'){
      cmp=powerValue(cb)-powerValue(ca);
      if(cmp===0) cmp=a.localeCompare(b,'ja');
    }else if(mode==='attr'){
      cmp=(ca.attribute||'').localeCompare(cb.attribute||'','ja');
      if(cmp===0) cmp=a.localeCompare(b,'ja');
    }
    return cmp;
  });
  gameState.deckListOrder=names.slice();
  const rebuilt=[];
  names.forEach(name=>{
    gameState.currentDeck.filter(c=>c.name===name).forEach(c=>rebuilt.push(c));
  });
  gameState.currentDeck=rebuilt;
  renderDeckEdit();
}

function renderDeckEdit(){
  document.getElementById('deck-count').innerText=gameState.currentDeck.length;
  document.getElementById('deck-reaction-list').innerText=FULL_REACTION_TEXT;

  const syn=calcSynthRate();
  document.getElementById('synth-rate-text').innerText=`${syn.rate}%（${syn.ok}/${syn.total}系統）`;
  document.getElementById('synth-rate-bar').style.width=syn.rate+"%";
  document.getElementById('synth-hint').innerText=syn.missing.length
    ? "不足例: "+syn.missing.join(" ／ ")
    : (syn.rate>=60?"反応の組み合わせが充実しています":"官能基と炭化水素基・基質と試薬をバランスよく入れると上がります");

  const allNames=[...new Set(gameState.collection.map(c=>c.name))];
  let ordered;
  if(gameState.deckListOrder && gameState.deckListOrder.length){
    ordered=gameState.deckListOrder.filter(n=>allNames.includes(n));
    allNames.filter(n=>!ordered.includes(n)).sort((a,b)=>a.localeCompare(b,'ja')).forEach(n=>ordered.push(n));
  }else{
    ordered=allNames.sort((a,b)=>a.localeCompare(b,'ja'));
  }

  const list=document.getElementById('deck-list'); list.innerHTML="";
  ordered.forEach(name=>{
    const owned=gameState.collection.filter(c=>c.name===name).length;
    const inD=gameState.currentDeck.filter(c=>c.name===name).length;
    const card=gameState.collection.find(c=>c.name===name);
    if(!card) return;
    const val=card.name==="ボツリヌス毒素"?"継続200":(card.healPower>0?`HEAL+${card.healPower}`:`PWR ${formatPower(card.attackPower)}`);
    const div=document.createElement('div'); div.className=`deck-item ${inD>0?'in-deck':''}`;
    div.innerHTML=`<div style="display:flex;gap:7px;align-items:center"><span class="card-rarity rarity-${card.rarity}">${card.rarity}</span><div><div style="font-size:13px;color:${inD>0?'#4ade80':'#e2e8f0'}">${name} [${inD}/${owned}]</div><div style="font-size:9px;color:#94a3b8">${card.formula} · ${val} · ${card.attribute}</div></div></div>
      <div style="display:flex;gap:4px">${inD>0?`<button class="action-btn" style="color:#f87171" onclick="removeFromDeck('${name}')">➖</button>`:''}
      <button class="action-btn" style="color:${inD<owned&&gameState.currentDeck.length<50?'#38bdf8':'#475569'}" onclick="addToDeck('${name}')" ${inD>=owned||gameState.currentDeck.length>=50?'disabled':''}>➕</button></div>`;
    list.appendChild(div);
  });
  const btn=document.getElementById('deck-done-btn');
  if(gameState.currentDeck.length>=20){btn.disabled=false;btn.style.opacity='1';}
  else{btn.disabled=true;btn.style.opacity='.45';}
}
function addToDeck(name){
  const owned=gameState.collection.filter(c=>c.name===name).length;
  const inD=gameState.currentDeck.filter(c=>c.name===name).length;
  const card=gameState.collection.find(c=>c.name===name);
  if(card&&gameState.currentDeck.length<50&&inD<owned){gameState.currentDeck.push({...card,id:Math.random().toString(36).substr(2,9)});renderDeckEdit();}
}
function removeFromDeck(name){const i=gameState.currentDeck.findIndex(c=>c.name===name); if(i>=0){gameState.currentDeck.splice(i,1);renderDeckEdit();}}
function finishDeckEdit(){if(gameState.currentDeck.length<20){alert('最低20枚必要');return;} switchState('field');}

function drawGacha(){
  if(gameState.reagents<100) return;
  gameState.reagents-=100; document.getElementById('gacha-reagents').innerText=gameState.reagents;
  const boost=getRank().gachaBoost;
  let rand=Math.random()*100;
  let rarity;
  if(rand<0.1+boost*0.15) rarity='SSSR';
  else if(rand<0.1+2.9+boost) rarity='SSR';
  else if(rand<0.1+2.9+15+boost*2) rarity='SR';
  else rarity='R';
  let cands=ALL_CARDS.filter(c=>c.rarity===rarity); if(!cands.length) cands=ALL_CARDS.filter(c=>c.rarity==='R');
  const pulled=cands[Math.floor(Math.random()*cands.length)];
  const newCard={...pulled,id:Math.random().toString(36).substr(2,9)};
  gameState.collection.push(newCard); saveGame(true); checkAchievements();
  let val=newCard.name==="ボツリヌス毒素"?"継続200/ターン":(newCard.healPower>0?`HEAL+${newCard.healPower}`:`PWR ${formatPower(newCard.attackPower)}`);
  const res=document.getElementById('gacha-result');
  res.innerHTML=`<span class="card-rarity rarity-${newCard.rarity}">${newCard.rarity}</span>
    <div style="font-size:17px;margin:6px 0">${newCard.name}</div>
    <div style="font-size:11px;color:#cbd5e1">${newCard.formula}</div>
    <div style="font-size:11px;color:#fbbf24;margin-top:4px">${val} · ${newCard.attribute}</div>
    <div style="font-size:10px;color:#94a3b8;margin-top:3px">色: ${newCard.color||"-"} ／ 匂い: ${newCard.odor||"-"}</div>`;
  res.style.borderColor=newCard.rarity==='SSSR'?'#e879f9':(newCard.rarity==='SSR'?'#fb923c':(newCard.rarity==='SR'?'#c084fc':'#60a5fa'));
}

initDaily();
</script>
</body>
</html>
