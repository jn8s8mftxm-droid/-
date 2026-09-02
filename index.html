<!DOCTYPE html>
<html lang="ja">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
<title>有機化学バトル</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
<style>
*{box-sizing:border-box;margin:0;padding:0;user-select:none;font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif}
body,html{width:100%;height:100%;overflow:hidden;background:#000;color:#fff}
.screen{display:none;width:100%;height:100%;position:absolute;top:0;left:0}
.active{display:flex;flex-direction:column}
.glass-btn{background:linear-gradient(135deg,#3b82f6,#9333ea);border:none;color:#fff;padding:10px 16px;font-weight:bold;font-size:14px;border-radius:14px;cursor:pointer;box-shadow:0 3px 6px rgba(0,0,0,.4)}
.glass-btn:active{transform:scale(.95)}
.glass-btn:disabled{opacity:.5;cursor:not-allowed}
#deck-select-screen{background:linear-gradient(to bottom,#1a263f,#000);padding:40px 20px;align-items:center;justify-content:flex-start;gap:20px;text-align:center}
.select-card{background:linear-gradient(to right,#059669,#0d9488);border-radius:18px;padding:16px;margin-bottom:16px;text-align:left;cursor:pointer;box-shadow:0 4px 8px rgba(0,0,0,.3);width:100%;max-width:400px}
.select-card.red{background:linear-gradient(to right,#ea580c,#dc2626)}
.select-card.purple{background:linear-gradient(to right,#9333ea,#2563eb)}
.badge{background:rgba(255,255,255,.2);font-size:10px;font-weight:bold;padding:2px 6px;border-radius:6px}
#field-screen{position:relative;width:100%;height:100%}
#canvas-container{width:100%;height:100%}
.field-ui{position:absolute;top:0;left:0;width:100%;padding:40px 16px 0;display:flex;justify-content:space-between;pointer-events:none}
.field-ui *{pointer-events:auto}
.status-box{background:rgba(0,0,0,.65);padding:10px;border-radius:12px;font-size:13px;font-weight:bold}
#battle-screen{background:linear-gradient(to bottom,#0f172a,#1e293b);padding:16px 12px 14px;justify-content:space-between}
.battle-header{display:flex;justify-content:space-between;align-items:flex-start;margin-bottom:4px}
#lab-canvas-container{width:100%;height:180px;border-radius:14px;border:2px solid #06b6d4;overflow:hidden;background:#0284c711;position:relative}
.battle-log-box{background:rgba(15,23,42,.85);border:1px solid #334155;border-radius:12px;padding:10px;min-height:52px;font-size:12px;text-align:center;display:flex;align-items:center;justify-content:center;white-space:pre-line;margin:6px 0}
.quiz-box{background:rgba(147,51,234,.4);border:1px solid #a855f7;border-radius:12px;padding:10px;text-align:center;display:flex;flex-direction:column;gap:8px}
.quiz-options{display:grid;grid-template-columns:1fr 1fr;gap:6px}
.quiz-btn{background:rgba(37,99,235,.85);border:none;color:#fff;padding:8px;border-radius:8px;font-size:11px;font-weight:bold;cursor:pointer}
.hand-container{overflow-x:auto;display:flex;gap:7px;padding:5px 0}
.card{min-width:84px;width:84px;height:112px;background:#fff;color:#000;border-radius:10px;padding:4px;display:flex;flex-direction:column;justify-content:space-between;cursor:pointer;box-shadow:0 3px 5px rgba(0,0,0,.3)}
.card.selected{background:#fde047;box-shadow:0 0 10px #fde047;transform:translateY(-4px)}
.card-rarity{font-size:8px;font-weight:bold;padding:1px 4px;border-radius:3px;color:#fff;width:fit-content}
.rarity-SSR{background:#f97316}.rarity-SR{background:#a855f7}.rarity-R{background:#3b82f6}
.rarity-SSSR{background:linear-gradient(90deg,#ff0000,#ff00ff);animation:rainbow 1.5s linear infinite}
.card-attr{font-size:8px;color:#666}
@keyframes rainbow{0%{filter:hue-rotate(0)}100%{filter:hue-rotate(360deg)}}
#deck-edit-screen{background:#111;padding:36px 14px 10px;height:100%;overflow:hidden}
.deck-list{flex:1;overflow-y:auto;margin-top:8px;max-height:36vh}
.deck-item{display:flex;justify-content:space-between;align-items:center;background:#222;padding:7px 9px;margin-bottom:5px;border-radius:8px}
.deck-item.in-deck{background:rgba(34,197,94,.12)}
.action-btn{background:none;border:none;font-size:17px;cursor:pointer}
.info-box{background:rgba(30,30,30,.9);border:1px solid #444;border-radius:10px;padding:9px;margin-top:7px;overflow-y:auto;font-size:11px;line-height:1.45}
.info-title{font-weight:bold;color:#facc15;margin-bottom:5px;font-size:12px}
#gacha-screen{background:linear-gradient(to bottom,#1a0d26,#000);padding:28px 14px 18px;align-items:center;gap:11px;overflow-y:auto}
.gacha-card-view{width:230px;height:170px;border-radius:14px;border:2px solid #a855f7;background:rgba(255,255,255,.05);display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:10px}
.battle-actions{display:flex;gap:7px;justify-content:center;margin-top:6px;flex-wrap:wrap}
.choice-box{background:rgba(15,23,42,.95);border:2px solid #facc15;border-radius:14px;padding:14px;text-align:center;display:none;flex-direction:column;gap:10px;position:absolute;left:50%;top:40%;transform:translate(-50%,-50%);width:85%;max-width:320px;z-index:50}
</style>
</head>
<body>

<div id="deck-select-screen" class="screen active">
  <h2>有機化学バトル</h2>
  <p style="font-size:13px;color:#aaa">初期スターターデッキを選択してください</p>
  <div style="width:100%;max-width:400px">
    <div class="select-card purple" onclick="assignStarterDeck('Aromatic')">
      <span class="badge">ベンゼン・濃硝酸・回復薬品</span>
      <h3 style="margin:4px 0">芳香族・置換反応デッキ</h3>
      <p style="font-size:11px;opacity:.85">ニトロ化・スルホン化で超高火力を狙う専門デッキ！</p>
    </div>
    <div class="select-card red" onclick="assignStarterDeck('Polymer')">
      <span class="badge">エチレン・臭素・回復薬品</span>
      <h3 style="margin:4px 0">付加・高分子デッキ</h3>
      <p style="font-size:11px;opacity:.85">ハロゲン付加や付加重合を使うバランス型</p>
    </div>
    <div class="select-card" onclick="assignStarterDeck('Redox')">
      <span class="badge">アルコール・酢酸・回復薬品</span>
      <h3 style="margin:4px 0">酸化・エステル・コントロール</h3>
      <p style="font-size:11px;opacity:.85">エステル化やけん化反応でテクニカルに勝利！</p>
    </div>
  </div>
</div>

<div id="field-screen" class="screen">
  <div id="canvas-container"></div>
  <div class="field-ui">
    <div class="status-box">
      <div>🧪 試薬: <span id="field-reagents">150</span></div>
      <div style="color:#4ade80">❤️ HP: <span id="field-hp">200</span></div>
      <div style="color:#facc15;font-size:12px">🎓 <span id="field-rank">初学者</span> (撃破 <span id="field-kills">0</span>)</div>
    </div>
    <div style="display:flex;gap:7px;flex-wrap:wrap;justify-content:flex-end">
      <button class="glass-btn" style="background:linear-gradient(135deg,#10b981,#059669);padding:8px 11px;font-size:12px" onclick="saveGame()">セーブ</button>
      <button class="glass-btn" style="background:linear-gradient(135deg,#6366f1,#4f46e5);padding:8px 11px;font-size:12px" onclick="loadGame()">ロード</button>
      <button class="glass-btn" style="background:linear-gradient(135deg,#06b6d4,#3b82f6)" onclick="switchState('deckEdit')">デッキ</button>
      <button class="glass-btn" style="background:linear-gradient(135deg,#ec4899,#a855f7)" onclick="switchState('gacha')">ガチャ</button>
    </div>
  </div>
</div>

<div id="battle-screen" class="screen">
  <div class="battle-header">
    <div>
      <div style="color:#4ade80;font-weight:bold">🧑 HP: <span id="battle-player-hp">200</span></div>
      <div style="color:#06b6d4;font-size:11px">📚 山札: <span id="battle-deck-count">0</span></div>
      <div id="next-bonus" style="font-size:11px;color:#facc15;display:none">次ターン火力UP</div>
      <div id="dot-status" style="font-size:11px;color:#f87171;display:none">☠️ ボツリヌス毒素 毎ターン200</div>
    </div>
    <div style="text-align:right">
      <div style="font-size:12px;color:#aaa">👾 <span id="monster-name">敵</span> Lv.<span id="monster-level">1</span></div>
      <div style="color:#ef4444;font-weight:bold;font-size:15px"><span id="monster-hp">500</span> / <span id="monster-maxhp">500</span></div>
      <div id="monster-weak" style="font-size:10px;color:#f97316"></div>
      <div id="monster-cond" style="font-size:10px;color:#f472b6"></div>
    </div>
  </div>
  <div id="lab-canvas-container"></div>
  <div id="quiz-container" class="quiz-box" style="display:none">
    <div style="font-size:11px;color:#facc15;font-weight:bold">📝 クイズ（正解で1.5倍）</div>
    <div id="quiz-question" style="font-size:13px;font-weight:bold"></div>
    <div id="quiz-options" class="quiz-options"></div>
  </div>
  <div id="battle-log" class="battle-log-box">バトル開始！</div>
  <div>
    <div style="font-size:10px;color:#aaa;margin-bottom:2px">手札 (<span id="hand-count">0</span>/7)</div>
    <div id="hand-cards" class="hand-container"></div>
  </div>
  <div class="battle-actions">
    <button id="attack-btn" class="glass-btn" style="background:linear-gradient(135deg,#ea580c,#ef4444);flex:1;padding:11px" onclick="executePlayerAttack()">化学反応実行</button>
    <button id="skip-btn" class="glass-btn" style="background:linear-gradient(135deg,#64748b,#475569);width:95px;padding:11px" onclick="skipTurn()">ターン終了</button>
    <button id="flee-btn" class="glass-btn" style="background:linear-gradient(135deg,#dc2626,#991b1b);width:85px;padding:11px" onclick="fleeBattle()">逃げる</button>
  </div>
  <div id="choice-box" class="choice-box">
    <div style="font-weight:bold;color:#facc15" id="choice-title">中間物質が生成された！</div>
    <div id="choice-desc" style="font-size:13px"></div>
    <div style="display:flex;gap:10px;justify-content:center">
      <button class="glass-btn" style="background:linear-gradient(135deg,#ea580c,#ef4444)" onclick="chooseAttack()">攻撃する</button>
      <button class="glass-btn" style="background:linear-gradient(135deg,#10b981,#059669)" onclick="chooseAddToHand()">手札に加える</button>
    </div>
  </div>
</div>

<div id="deck-edit-screen" class="screen">
  <div style="display:flex;justify-content:space-between;align-items:center">
    <div><h3>デッキ編集 (<span id="deck-count">0</span>/40)</h3><p style="font-size:11px;color:#888">最低20枚</p></div>
    <button id="deck-done-btn" class="glass-btn" onclick="finishDeckEdit()">完了</button>
  </div>
  <div id="deck-list" class="deck-list"></div>
  <div class="info-box" style="max-height:30vh"><div class="info-title">📖 反応一覧</div><div id="reaction-list" style="white-space:pre-line;color:#ddd"></div></div>
</div>

<div id="gacha-screen" class="screen">
  <h2 style="margin-top:8px">🧪 化合物ガチャ</h2>
  <p style="color:#06b6d4">試薬: <span id="gacha-reagents">150</span> ／ ランク: <span id="gacha-rank">初学者</span></p>
  <div id="gacha-result" class="gacha-card-view"><span style="color:#888">ガチャを回すと出現</span></div>
  <div style="display:flex;gap:8px;flex-wrap:wrap;justify-content:center">
    <button class="glass-btn" style="background:linear-gradient(135deg,#ec4899,#a855f7);padding:10px 18px" onclick="drawGacha()">ガチャ (100)</button>
    <button class="glass-btn" style="background:#333;padding:10px 14px" onclick="switchState('field')">戻る</button>
  </div>
  <div class="info-box" style="width:100%;max-width:420px;max-height:36vh"><div class="info-title">📋 排出一覧</div><div id="gacha-list" style="white-space:pre-line;color:#ddd"></div></div>
</div>

<script>
const ALL_CARDS = [
  {name:"ベンゼン",formula:"C6H6",attackPower:30,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色",odor:"特異臭"},
  {name:"トルエン",formula:"C6H5CH3",attackPower:35,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色",odor:"甘い芳香"},
  {name:"エチレン",formula:"C2H4",attackPower:25,healPower:0,attribute:"Alkenyl",rarity:"R",color:"無色",odor:"わずかに甘い"},
  {name:"エタノール",formula:"C2H5OH",attackPower:25,healPower:0,attribute:"Alcohol",rarity:"R",color:"無色",odor:"アルコール臭"},
  {name:"アセトアルデヒド",formula:"CH3CHO",attackPower:35,healPower:0,attribute:"Aldehyde",rarity:"R",color:"無色",odor:"刺激臭"},
  {name:"酢酸",formula:"CH3COOH",attackPower:40,healPower:0,attribute:"Acid",rarity:"R",color:"無色",odor:"刺激的な酸味"},
  {name:"フェノール",formula:"C6H5OH",attackPower:45,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色〜淡紅",odor:"特異臭"},
  {name:"水酸化ナトリウム",formula:"NaOH",attackPower:35,healPower:0,attribute:"Base",rarity:"SR",color:"白色",odor:"無臭"},
  {name:"濃硝酸",formula:"HNO3",attackPower:30,healPower:0,attribute:"Reagent",rarity:"SR",color:"無色〜淡黄",odor:"刺激臭"},
  {name:"濃硫酸",formula:"H2SO4",attackPower:30,healPower:0,attribute:"Reagent",rarity:"SR",color:"無色",odor:"無臭"},
  {name:"臭素",formula:"Br2",attackPower:35,healPower:0,attribute:"Halogen",rarity:"R",color:"赤褐色",odor:"刺激臭"},
  {name:"塩素",formula:"Cl2",attackPower:35,healPower:0,attribute:"Halogen",rarity:"R",color:"黄緑色",odor:"刺激臭"},
  {name:"過マンガン酸カリウム",formula:"KMnO4",attackPower:40,healPower:0,attribute:"Oxidant",rarity:"SR",color:"紫黒色",odor:"無臭"},
  {name:"水素化ホウ素ナトリウム",formula:"NaBH4",attackPower:40,healPower:0,attribute:"Reductant",rarity:"SR",color:"白色",odor:"無臭"},
  {name:"重合触媒(Ziegler)",formula:"[Cat]",attackPower:30,healPower:0,attribute:"Catalyst",rarity:"SSR",color:"-",odor:"-"},
  {name:"グリシン",formula:"H2NCH2COOH",attackPower:0,healPower:40,attribute:"Nutrient",rarity:"R",color:"白色",odor:"無臭"},
  {name:"グルコース",formula:"C6H12O6",attackPower:0,healPower:65,attribute:"Nutrient",rarity:"SR",color:"白色",odor:"無臭"},
  {name:"トリニトロトルエン",formula:"C7H5N3O6",attackPower:180,healPower:0,attribute:"Explosive",rarity:"SSR",color:"淡黄色",odor:"無臭"},
  {name:"ピクリン酸",formula:"C6H3N3O7",attackPower:180,healPower:0,attribute:"Explosive",rarity:"SSR",color:"黄色",odor:"無臭"},
  {name:"フッ化水素酸",formula:"HF",attackPower:Infinity,healPower:0,attribute:"Acid",rarity:"SSSR",color:"無色",odor:"刺激臭"},
  {name:"ボツリヌス毒素",formula:"BoNT",attackPower:0,healPower:0,attribute:"Toxin",rarity:"SSSR",color:"-",odor:"-"},
  {name:"金属ナトリウム",formula:"Na",attackPower:40,healPower:0,attribute:"Metal",rarity:"SR",color:"銀白色",odor:"無臭"},
  {name:"ニトロベンゼン",formula:"C6H5NO2",attackPower:70,healPower:0,attribute:"Aromatic",rarity:"SR",color:"淡黄色",odor:"アーモンド様"},
  {name:"アニリン",formula:"C6H5NH2",attackPower:65,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色〜褐色",odor:"特異臭"},
  {name:"アゾベンゼン",formula:"C6H5N=NC6H5",attackPower:95,healPower:0,attribute:"Aromatic",rarity:"SSR",color:"橙赤色",odor:"無臭"},
  {name:"酢酸エチル",formula:"CH3COOC2H5",attackPower:55,healPower:0,attribute:"Ester",rarity:"R",color:"無色",odor:"果実様香気"},
  {name:"ニトロ基",formula:"-NO2",attackPower:45,healPower:0,attribute:"FunctionalGroup",rarity:"SR",color:"-",odor:"-"},
  {name:"還元剤",formula:"[Red]",attackPower:30,healPower:0,attribute:"Reductant",rarity:"SR",color:"-",odor:"-"},
  {name:"ジアゾ化剤",formula:"NaNO2/HCl",attackPower:35,healPower:0,attribute:"Reagent",rarity:"SR",color:"-",odor:"-"},
  {name:"o-クレゾール",formula:"CH3C6H4OH",attackPower:40,healPower:0,attribute:"Phenol",rarity:"R",color:"無色",odor:"フェノール臭"},
  {name:"m-クレゾール",formula:"CH3C6H4OH",attackPower:40,healPower:0,attribute:"Phenol",rarity:"R",color:"無色",odor:"フェノール臭"},
  {name:"p-クレゾール",formula:"CH3C6H4OH",attackPower:42,healPower:0,attribute:"Phenol",rarity:"R",color:"無色",odor:"フェノール臭"},
  {name:"カテコール",formula:"C6H4(OH)2",attackPower:50,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色",odor:"-"},
  {name:"レゾルシノール",formula:"C6H4(OH)2",attackPower:48,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色",odor:"-"},
  {name:"ヒドロキノン",formula:"C6H4(OH)2",attackPower:55,healPower:0,attribute:"Phenol",rarity:"SR",color:"無色",odor:"-"},
  {name:"ピロガロール",formula:"C6H3(OH)3",attackPower:60,healPower:0,attribute:"Phenol",rarity:"SR",color:"白色",odor:"-"},
  {name:"フロログルシノール",formula:"C6H3(OH)3",attackPower:58,healPower:0,attribute:"Phenol",rarity:"SR",color:"白色",odor:"-"},
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
  {name:"スルホン基",formula:"-SO3H",attackPower:42,healPower:0,attribute:"FunctionalGroup",rarity:"SR",color:"-",odor:"-"},
  {name:"ハロゲン基",formula:"-X",attackPower:30,healPower:0,attribute:"FunctionalGroup",rarity:"R",color:"-",odor:"-"},
  {name:"マレイン酸",formula:"cis-HOOCCH=CHCOOH",attackPower:55,healPower:0,attribute:"CisTrans",rarity:"SR",color:"白色",odor:"-"},
  {name:"フマル酸",formula:"trans-HOOCCH=CHCOOH",attackPower:55,healPower:0,attribute:"CisTrans",rarity:"SR",color:"白色",odor:"-"},
  {name:"シス-2-ブテン",formula:"cis-CH3CH=CHCH3",attackPower:35,healPower:0,attribute:"CisTrans",rarity:"R",color:"無色",odor:"-"},
  {name:"トランス-2-ブテン",formula:"trans-CH3CH=CHCH3",attackPower:35,healPower:0,attribute:"CisTrans",rarity:"R",color:"無色",odor:"-"},
  {name:"オレイン酸",formula:"C18H34O2",attackPower:50,healPower:0,attribute:"CisTrans",rarity:"SR",color:"無色〜淡黄",odor:"-"},
  {name:"スチルベン",formula:"C6H5CH=CHC6H5",attackPower:60,healPower:0,attribute:"CisTrans",rarity:"SR",color:"無色",odor:"-"},
  {name:"ナフタレン",formula:"C10H8",attackPower:55,healPower:0,attribute:"Aromatic",rarity:"SR",color:"白色",odor:"樟脳様"},
  {name:"アントラセン",formula:"C14H10",attackPower:120,healPower:0,attribute:"Aromatic",rarity:"SSR",color:"無色〜淡黄",odor:"-"}
];

const RANKS = [
  {name:"初学者", kills:0,  reagentBonus:1.0, gachaBoost:0},
  {name:"高校生", kills:8,  reagentBonus:1.15, gachaBoost:0.3},
  {name:"大学生", kills:20, reagentBonus:1.3,  gachaBoost:0.6},
  {name:"大学院生",kills:40, reagentBonus:1.5,  gachaBoost:1.0},
  {name:"博士",   kills:70, reagentBonus:1.8,  gachaBoost:1.5},
  {name:"教授",   kills:120,reagentBonus:2.2,  gachaBoost:2.2}
];

const REACTION_LIST = [
  {dmg:440,text:"トルエン+濃硝酸(触媒) → 440"},
  {dmg:420,text:"けん化(触媒) → 420"},
  {dmg:360,text:"ベンゼン+濃硝酸(触媒) → 360"},
  {dmg:300,text:"エチレン+重合触媒 → 300"},
  {dmg:200,text:"ボツリヌス毒素 → 毎ターン200"},
  {dmg:180,text:"TNT / ピクリン酸 / ベンゼン+塩素 → 180"},
  {dmg:130,text:"エステル化 / ニトロ化 → 130"},
  {dmg:Infinity,text:"フッ化水素酸 → ∞"}
];

let gameState = {
  reagents:150, playerHP:200, playerMaxHP:200,
  collection:[], currentDeck:[], currentMonster:null,
  nextDamageBonus:1.0, kills:0
};

let isBattleOver=false, isProcessing=false, botulinumActive=false;
let pendingIntermediate=null;

function getRank(){
  let r = RANKS[0];
  for(const rank of RANKS){ if(gameState.kills >= rank.kills) r = rank; }
  return r;
}

function saveGame(silent=false){
  const data={reagents:gameState.reagents,playerHP:gameState.playerHP,playerMaxHP:gameState.playerMaxHP,collection:gameState.collection,currentDeck:gameState.currentDeck,kills:gameState.kills};
  localStorage.setItem('organicChemBattleSave',JSON.stringify(data));
  if(!silent) alert('セーブしました！');
}
function loadGame(){
  const saved=localStorage.getItem('organicChemBattleSave');
  if(!saved){alert('セーブデータがありません');return;}
  try{
    const d=JSON.parse(saved);
    gameState.reagents=d.reagents??150; gameState.playerHP=d.playerHP??200; gameState.playerMaxHP=d.playerMaxHP??200;
    gameState.collection=d.collection||[]; gameState.currentDeck=d.currentDeck||[]; gameState.kills=d.kills||0;
    updateFieldUI(); switchState('field'); alert('ロードしました！');
  }catch(e){alert('ロード失敗');}
}

function switchState(s){
  document.querySelectorAll('.screen').forEach(el=>el.classList.remove('active'));
  if(s==='deckSelection') document.getElementById('deck-select-screen').classList.add('active');
  if(s==='field'){document.getElementById('field-screen').classList.add('active');updateFieldUI();initThreeJS();}
  if(s==='battle'){document.getElementById('battle-screen').classList.add('active');initLabThreeJS();setupBattle();}
  if(s==='deckEdit'){document.getElementById('deck-edit-screen').classList.add('active');renderDeckEdit();renderReactionList();}
  if(s==='gacha'){document.getElementById('gacha-screen').classList.add('active');document.getElementById('gacha-reagents').innerText=gameState.reagents;document.getElementById('gacha-rank').innerText=getRank().name;renderGachaList();}
}

function updateFieldUI(){
  document.getElementById('field-reagents').innerText=gameState.reagents;
  document.getElementById('field-hp').innerText=gameState.playerHP;
  document.getElementById('field-rank').innerText=getRank().name;
  document.getElementById('field-kills').innerText=gameState.kills;
}

function assignStarterDeck(type){
  gameState.currentDeck=[]; gameState.collection=[];
  let base=[];
  if(type==='Aromatic') base=[ALL_CARDS[0],ALL_CARDS[0],ALL_CARDS[1],ALL_CARDS[1],ALL_CARDS[8],ALL_CARDS[8],ALL_CARDS[9],ALL_CARDS[6],ALL_CARDS[15],ALL_CARDS[16],ALL_CARDS[24],ALL_CARDS[25]];
  else if(type==='Polymer') base=[ALL_CARDS[2],ALL_CARDS[2],ALL_CARDS[10],ALL_CARDS[11],ALL_CARDS[14],ALL_CARDS[15],ALL_CARDS[16],ALL_CARDS[3]];
  else base=[ALL_CARDS[3],ALL_CARDS[3],ALL_CARDS[5],ALL_CARDS[5],ALL_CARDS[7],ALL_CARDS[12],ALL_CARDS[15],ALL_CARDS[16],ALL_CARDS[4]];
  for(let i=0;i<40;i++){
    const c={...base[i%base.length],id:Math.random().toString(36).substr(2,9)};
    gameState.currentDeck.push(c); gameState.collection.push(c);
  }
  gameState.playerHP=gameState.playerMaxHP; switchState('field');
}

function renderGachaList(){
  const order=["SSSR","SSR","SR","R"]; let html="";
  order.forEach(r=>{
    const cards=ALL_CARDS.filter(c=>c.rarity===r); if(!cards.length) return;
    html+=`【${r}】\n`;
    cards.forEach(c=>{
      let p=c.name==="ボツリヌス毒素"?"毎ターン200":(c.attackPower===Infinity?"∞":(c.healPower>0?`回復${c.healPower}`:c.attackPower));
      html+=`・${c.name}（${p}） ${c.color||""} ${c.odor||""}\n`;
    });
    html+="\n";
  });
  document.getElementById('gacha-list').innerText=html.trim();
}
function renderReactionList(){document.getElementById('reaction-list').innerText=REACTION_LIST.map(r=>`・${r.text}`).join("\n");}

// ===== 詳細な人間モデル（腕・足あり） =====
function createHumanoidMesh() {
  const group = new THREE.Group();
  const bodyMat = new THREE.MeshLambertMaterial({ color: 0x0284c7 });
  const skinMat = new THREE.MeshLambertMaterial({ color: 0xffdbac });
  const legMat  = new THREE.MeshLambertMaterial({ color: 0x1e293b });

  // 頭
  const head = new THREE.Mesh(new THREE.SphereGeometry(0.25, 16, 16), skinMat);
  head.position.y = 0.85;
  group.add(head);

  // 胴体
  const body = new THREE.Mesh(new THREE.CylinderGeometry(0.2, 0.15, 0.6, 16), bodyMat);
  body.position.y = 0.45;
  group.add(body);

  // 腕
  const armGeo = new THREE.CylinderGeometry(0.06, 0.06, 0.4, 8);
  const leftArm = new THREE.Mesh(armGeo, bodyMat);
  leftArm.position.set(-0.28, 0.45, 0);
  const rightArm = new THREE.Mesh(armGeo, bodyMat);
  rightArm.position.set(0.28, 0.45, 0);
  group.add(leftArm);
  group.add(rightArm);

  // 足
  const legGeo = new THREE.CylinderGeometry(0.07, 0.07, 0.45, 8);
  const leftLeg = new THREE.Mesh(legGeo, legMat);
  leftLeg.position.set(-0.1, 0.15, 0);
  const rightLeg = new THREE.Mesh(legGeo, legMat);
  rightLeg.position.set(0.1, 0.15, 0);
  group.add(leftLeg);
  group.add(rightLeg);

  return group;
}

function createMoleculeMesh(col){
  const g=new THREE.Group(), m=new THREE.MeshLambertMaterial({color:col}), s=new THREE.MeshLambertMaterial({color:0xffffff});
  g.add(new THREE.Mesh(new THREE.SphereGeometry(.5,18,18),m));
  [[.7,.45,0],[-.7,.45,0],[0,-.65,.45],[0,.45,-.65]].forEach(p=>{
    const a=new THREE.Mesh(new THREE.SphereGeometry(.25,12,12),s); a.position.set(...p); g.add(a);
  });
  return g;
}

let scene,camera,renderer,playerNode,monsters=[],targetPlayerPos={x:0,z:0},isThreeInit=false,lastSpawnTime=0;
function initThreeJS(){
  if(isThreeInit) return; isThreeInit=true;
  const cont=document.getElementById('canvas-container');
  scene=new THREE.Scene(); scene.background=new THREE.Color(0x87ceeb);
  camera=new THREE.PerspectiveCamera(45,innerWidth/innerHeight,.1,1000); camera.position.set(0,12,10); camera.rotation.x=-Math.PI/3.2;
  renderer=new THREE.WebGLRenderer({antialias:true}); renderer.setSize(innerWidth,innerHeight); cont.appendChild(renderer.domElement);
  scene.add(new THREE.DirectionalLight(0xffffff,1.2)); scene.add(new THREE.AmbientLight(0xffffff,.6));
  const floor=new THREE.Mesh(new THREE.PlaneGeometry(100,100),new THREE.MeshBasicMaterial({color:0x4ade80})); floor.rotation.x=-Math.PI/2; scene.add(floor);
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
      m.mesh.rotation.y+=.01; m.changeDirTimer--;
      if(m.changeDirTimer<=0){m.vx=(Math.random()-.5)*.08;m.vz=(Math.random()-.5)*.08;m.changeDirTimer=30+Math.random()*60;}
      m.mesh.position.x+=m.vx; m.mesh.position.z+=m.vz;
      if(Math.abs(m.mesh.position.x)>14)m.vx*=-1; if(m.mesh.position.z<-20||m.mesh.position.z>8)m.vz*=-1;
      const dx=playerNode.position.x-m.mesh.position.x, dz=playerNode.position.z-m.mesh.position.z;
      if(Math.sqrt(dx*dx+dz*dz)<=1){m.isActive=false;scene.remove(m.mesh);gameState.currentMonster=m;switchState('battle');}
    });
    renderer.render(scene,camera);
  }
  anim(0);
}

function spawnMonster(){
  const isBoss=Math.random()<.12;
  let level,colorHex,hp,atk,name,weakness,condition=null;
  if(isBoss){
    level=5; colorHex=0x7c3aed; hp=900+Math.floor(Math.random()*200); atk=28+Math.floor(Math.random()*10);
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
  monsters.push({name,level,hp,maxHP:hp,attackPower:atk,mesh,isActive:true,weakness,isBoss,condition,vx:0,vz:0,changeDirTimer:0});
}

let labScene,labCamera,labRenderer,enemyMesh;
function initLabThreeJS(){
  const cont=document.getElementById('lab-canvas-container'); cont.innerHTML="";
  labScene=new THREE.Scene(); labScene.background=new THREE.Color(0x0c1a2e);
  labCamera=new THREE.PerspectiveCamera(50,cont.clientWidth/cont.clientHeight,.1,100); labCamera.position.set(0,1.6,5.2); labCamera.lookAt(0,.7,0);
  labRenderer=new THREE.WebGLRenderer({antialias:true}); labRenderer.setSize(cont.clientWidth,cont.clientHeight); cont.appendChild(labRenderer.domElement);
  labScene.add(new THREE.DirectionalLight(0x67e8f9,1.6)); labScene.add(new THREE.AmbientLight(0xffffff,.5));
  const col=gameState.currentMonster?.isBoss?0x7c3aed:0x22d3ee;
  enemyMesh=createMoleculeMesh(col); enemyMesh.scale.set(1.4,1.4,1.4); enemyMesh.position.set(0,.9,0); labScene.add(enemyMesh);
  (function anim(){requestAnimationFrame(anim); if(enemyMesh){enemyMesh.rotation.y+=.012; enemyMesh.position.y=.9+Math.sin(Date.now()*.002)*.07;} labRenderer.render(labScene,labCamera);})();
}

let bDeck=[],bHand=[],bSelected=[],monsterHP=500,isPlayerTurn=true,activeQuiz=null,pendingDamage=0,pendingHeal=0;

function setupBattle(){
  isBattleOver=false; isProcessing=false; botulinumActive=false; gameState.nextDamageBonus=1.0; pendingIntermediate=null;
  gameState.playerHP=gameState.playerMaxHP;
  document.getElementById('next-bonus').style.display='none';
  document.getElementById('dot-status').style.display='none';
  document.getElementById('choice-box').style.display='none';
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

function startPlayerTurn(first=false){
  if(isBattleOver) return;
  isPlayerTurn=true; isProcessing=false;
  if(botulinumActive && monsterHP>0){
    monsterHP-=200; document.getElementById('monster-hp').innerText=Math.max(0,monsterHP);
    if(monsterHP<=0){winBattle("☠️ ボツリヌス毒素が敵を分解！"); return;}
  }
  if(!first) drawCard();
  document.getElementById('battle-log').innerText=first?"カードを選んで化学反応を実行！":(botulinumActive?"☠️ 毒素継続中… あなたのターン":"あなたのターン！");
  updateBattleUI();
}

function drawCard(){if(bHand.length<7&&bDeck.length>0) bHand.push(bDeck.shift());}
function formatPower(v){return v===Infinity?"∞":v;}

function updateBattleUI(){
  document.getElementById('battle-deck-count').innerText=bDeck.length;
  document.getElementById('hand-count').innerText=bHand.length;
  const cont=document.getElementById('hand-cards'); cont.innerHTML="";
  bHand.forEach(card=>{
    const sel=bSelected.some(c=>c.id===card.id);
    const div=document.createElement('div'); div.className=`card ${sel?'selected':''}`;
    div.onclick=()=>toggleSelectCard(card);
    let val=card.name==="ボツリヌス毒素"?`<div style="font-size:9px;color:#dc2626;font-weight:bold">継続200</div>`:
            card.healPower>0?`<div style="font-size:10px;color:#16a34a;font-weight:bold">回復+${card.healPower}</div>`:
            `<div style="font-size:10px;color:#ef4444;font-weight:bold">威力:${formatPower(card.attackPower)}</div>`;
    div.innerHTML=`<div class="card-rarity rarity-${card.rarity}">${card.rarity}</div><div style="font-weight:bold;font-size:11px">${card.name}</div><div style="font-size:9px;color:#666">${card.formula}</div><div class="card-attr">${card.attribute}</div>${val}`;
    cont.appendChild(div);
  });
  const can=isPlayerTurn&&!activeQuiz&&!isProcessing&&!isBattleOver;
  document.getElementById('attack-btn').disabled=!(can&&bSelected.length>0);
  document.getElementById('skip-btn').disabled=!can;
  document.getElementById('flee-btn').disabled=!can;
}

function toggleSelectCard(card){
  if(!isPlayerTurn||activeQuiz||isBattleOver||isProcessing) return;
  const idx=bSelected.findIndex(c=>c.id===card.id);
  if(idx>=0) bSelected.splice(idx,1); else bSelected.push(card);
  updateBattleUI();
}

function skipTurn(){
  if(!isPlayerTurn||isBattleOver||isProcessing||activeQuiz) return;
  isProcessing=true; bSelected=[]; document.getElementById('battle-log').innerText="ターン終了…";
  updateBattleUI(); setTimeout(endPlayerTurn,700);
}
function fleeBattle(){
  if(!isPlayerTurn||isBattleOver||isProcessing) return;
  isBattleOver=true; isProcessing=true;
  document.getElementById('battle-log').innerText="🏃 脱出した…";
  setTimeout(()=>switchState('field'),1100);
}

function winBattle(msg){
  isBattleOver=true;
  gameState.kills++;
  const rank=getRank();
  let reward=Math.floor((40+(gameState.currentMonster?.level||1)*20)*(rank.reagentBonus));
  if(gameState.currentMonster?.isBoss) reward+=80;
  gameState.reagents+=reward;
  document.getElementById('battle-log').innerText=`${msg}\n試薬 +${reward} ／ 撃破数 ${gameState.kills}`;
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
  const hasCatalyst=n.includes("濃硫酸")||n.includes("重合触媒(Ziegler)");
  const bossCond=gameState.currentMonster?.condition||null;

  if(n.includes("ベンゼン")&&n.includes("ニトロ基")){
    product={name:"ニトロベンゼン",formula:"C6H5NO2",attackPower:70,healPower:0,attribute:"Aromatic",rarity:"SR",color:"淡黄色",odor:"アーモンド様"};
    baseDamage=70; logMessage="🧪 ベンゼン + ニトロ基 → ニトロベンゼン 生成！";
  }
  else if(n.includes("ニトロベンゼン")&&(n.includes("還元剤")||n.includes("水素化ホウ素ナトリウム"))){
    product={name:"アニリン",formula:"C6H5NH2",attackPower:65,healPower:0,attribute:"Aromatic",rarity:"SR",color:"無色〜褐色",odor:"特異臭"};
    baseDamage=65; logMessage="🧪 ニトロベンゼン の還元 → アニリン 生成！";
  }
  else if(n.includes("アニリン")&&n.includes("ジアゾ化剤")){
    product={name:"アゾベンゼン",formula:"C6H5N=NC6H5",attackPower:95,healPower:0,attribute:"Aromatic",rarity:"SSR",color:"橙赤色",odor:"無臭"};
    baseDamage=95; logMessage="🧪 アニリン のジアゾ化 → アゾ化合物 生成！";
  }
  else if(n.includes("酢酸")&&n.includes("エタノール")){
    product={name:"酢酸エチル",formula:"CH3COOC2H5",attackPower:hasCatalyst?90:55,healPower:0,attribute:"Ester",rarity:"R",color:"無色",odor:"果実様香気"};
    baseDamage=hasCatalyst?90:55; logMessage="🧪 酢酸 + エタノール → 酢酸エチル 生成！";
  }
  else if(bSelected.length===1&&bSelected[0].name==="ボツリヌス毒素"){
    botulinumActive=true; document.getElementById('dot-status').style.display='block';
    logMessage="☠️ ボツリヌス毒素を散布！ 毎ターン200ダメージ継続！"; baseDamage=0;
  }
  else if(bSelected.length===1&&bSelected[0].name==="フッ化水素酸"){
    if(Math.random()<.1){
      isBattleOver=true; document.getElementById('battle-log').innerText="☠️ 自分にかかってしまった！ 敗北…\n試薬-25";
      gameState.reagents=Math.max(0,gameState.reagents-25);
      setTimeout(()=>{gameState.playerHP=gameState.playerMaxHP;switchState('field');},2000);
      bHand=bHand.filter(c=>!bSelected.some(s=>s.id===c.id)); bSelected=[]; updateBattleUI(); return;
    }
    baseDamage=Infinity; logMessage="☠️ フッ化水素酸！ ダメージ ∞";
  }
  else if(bSelected.length===1&&(bSelected[0].name==="トリニトロトルエン"||bSelected[0].name==="ピクリン酸")){
    baseDamage=180; logMessage=`💥 ${bSelected[0].name} 起爆！ 180ダメージ`;
  }
  else if((n.includes("酢酸")&&n.includes("水酸化ナトリウム"))||(n.includes("酢酸")&&n.includes("エタノール")&&n.includes("水酸化ナトリウム"))){
    baseDamage=hasCatalyst?420:210; appliedEffect="saponification";
    quizToSet={question:"けん化で生じるトリオールは？",options:["グリセリン","エチレングリコール","フェノール","メタノール"],correctIndex:0,explanation:"正解！グリセリンが生成"};
  }
  else if(n.includes("ベンゼン")&&n.includes("濃硝酸")){
    baseDamage=hasCatalyst?360:130;
    quizToSet={question:"ベンゼンのニトロ化生成物は？",options:["ニトロベンゼン","安息香酸","フェノール","クロロベンゼン"],correctIndex:0,explanation:"正解！ニトロベンゼン"};
  }
  else if(n.includes("トルエン")&&n.includes("濃硝酸")){
    baseDamage=hasCatalyst?440:220;
    quizToSet={question:"トルエンの激しいニトロ化生成物は？",options:["トリニトロトルエン(TNT)","ピクリン酸","ニトログリセリン","ペルオキシド"],correctIndex:0,explanation:"正解！TNT"};
  }
  else if(n.includes("ベンゼン")&&n.includes("濃硫酸")){baseDamage=150;}
  else if(n.includes("エチレン")&&(n.includes("臭素")||n.includes("塩素"))){baseDamage=140;}
  else if(n.includes("エチレン")&&n.includes("重合触媒(Ziegler)")){baseDamage=300;}
  else if((n.includes("エタノール")||n.includes("アセトアルデヒド"))&&n.includes("過マンガン酸カリウム")){
    baseDamage=hasCatalyst?340:170; appliedEffect="oxidation";
  }
  else if(n.includes("ベンゼン")&&n.includes("塩素")){baseDamage=180; logMessage="🧪 ヘキサクロロシクロヘキサン生成！ 180";}
  else if(n.includes("エタノール")&&n.includes("金属ナトリウム")){baseDamage=120; logMessage="🧪 ナトリウムエトキシド生成！ 120";}
  else if(n.includes("フェノール")&&n.includes("金属ナトリウム")){baseDamage=140; logMessage="🧪 ナトリウムフェノキシド生成！ 140";}
  else if(n.includes("メチル基")&&n.includes("ヒドロキシ基")){baseDamage=50; logMessage="🧪 メタノール生成！ 50";}
  else if(n.includes("エチル基")&&n.includes("ヒドロキシ基")){baseDamage=60; logMessage="🧪 エタノール生成！ 60";}
  else if(n.includes("フェニル基")&&n.includes("ヒドロキシ基")){baseDamage=90; logMessage="🧪 フェノール生成！ 90";}
  else if(n.includes("フェニル基")&&n.includes("ニトロ基")){baseDamage=110; logMessage="🧪 ニトロベンゼン生成！ 110";}
  else if(bSelected.length===1){
    const s=bSelected[0];
    if(s.healPower>0){baseHeal=s.healPower; logMessage=`🧪 ${s.name} 吸収！ +${baseHeal}`;}
    else{baseDamage=s.attackPower; logMessage=`⚗️ ${s.name} 投擲！ ${formatPower(baseDamage)}`;}
  }else{
    const healSum=bSelected.reduce((a,c)=>a+c.healPower,0);
    if(healSum>0){baseHeal=healSum; logMessage=`🧪 複合回復 +${healSum}`;}
    else logMessage="⚠️ 不活性な組み合わせ";
  }

  if(bossCond && baseDamage>0 && baseDamage!==Infinity){
    const attrs=bSelected.map(c=>c.attribute);
    const ok=attrs.includes(bossCond) || (product && product.attribute===bossCond) ||
             (bossCond==="Ester"&&(n.includes("酢酸")&&n.includes("エタノール"))) ||
             (bossCond==="Alcohol"&&(n.includes("エタノール")||n.includes("ヒドロキシ基")));
    if(!ok){
      baseDamage=0;
      logMessage+=`\n❌ ボス条件「${bossCond}系のみ」を満たしていないため無効！`;
    }
  }

  let weaknessBonus=1.0;
  if(gameState.currentMonster?.weakness){
    const attrs=bSelected.map(c=>c.attribute);
    if(attrs.some(a=>gameState.currentMonster.weakness.includes(a))) weaknessBonus=1.5;
  }

  let finalBase=baseDamage;
  if(finalBase!==Infinity && finalBase>0) finalBase=Math.floor(finalBase*gameState.nextDamageBonus*weaknessBonus);

  if(appliedEffect==="oxidation"){gameState.nextDamageBonus=1.3; document.getElementById('next-bonus').style.display='block'; document.getElementById('next-bonus').innerText="次ターン火力+30%";}
  else if(appliedEffect==="saponification"){gameState.nextDamageBonus=1.2; document.getElementById('next-bonus').style.display='block'; document.getElementById('next-bonus').innerText="次ターン火力+20%";}
  else if(baseDamage>0||baseHeal>0){gameState.nextDamageBonus=1.0; document.getElementById('next-bonus').style.display='none';}

  bHand=bHand.filter(c=>!bSelected.some(s=>s.id===c.id));
  bSelected=[];

  if(product){
    pendingIntermediate={card:{...product,id:Math.random().toString(36).substr(2,9)}, damage:finalBase, heal:baseHeal, msg:logMessage, weak:weaknessBonus>1};
    document.getElementById('choice-title').innerText=`${product.name} が生成された！`;
    document.getElementById('choice-desc').innerText=`攻撃力 ${product.attackPower} ／ 属性 ${product.attribute}\n攻撃するか、手札に加えますか？`;
    document.getElementById('choice-box').style.display='flex';
    updateBattleUI();
    return;
  }

  if(quizToSet){pendingDamage=finalBase; pendingHeal=baseHeal; activeQuiz=quizToSet; showQuiz(quizToSet);}
  else applyEffectAndEndTurn(finalBase,baseHeal,logMessage,weaknessBonus>1);
}

function chooseAttack(){
  document.getElementById('choice-box').style.display='none';
  if(!pendingIntermediate) return;
  const p=pendingIntermediate;
  applyEffectAndEndTurn(p.damage, p.heal, p.msg+(p.weak?"\n💥 弱点を突いた！":""), p.weak);
  pendingIntermediate=null;
}
function chooseAddToHand(){
  document.getElementById('choice-box').style.display='none';
  if(!pendingIntermediate) return;
  if(bHand.length<7) bHand.push(pendingIntermediate.card);
  document.getElementById('battle-log').innerText=`${pendingIntermediate.card.name} を手札に加えた！`;
  pendingIntermediate=null;
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
  if(ok){dmg=pendingDamage===Infinity?Infinity:Math.floor(pendingDamage*1.5); heal=Math.floor(pendingHeal*1.5); log=`⭕ 正解！ 1.5倍！ (${formatPower(dmg)})`;}
  else{log="❌ 不正解… 効果0";}
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
  if(monsterHP<=0) winBattle("🎉 敵分子を分解！");
  else setTimeout(endPlayerTurn,1500);
}

function endPlayerTurn(){
  if(isBattleOver) return;
  isPlayerTurn=false; isProcessing=true;
  document.getElementById('battle-log').innerText="👾 敵の反撃…"; updateBattleUI();
  setTimeout(()=>{
    if(isBattleOver) return;
    if(monsterHP>0){
      const atk=gameState.currentMonster?.attackPower||15;
      gameState.playerHP-=atk;
      document.getElementById('battle-player-hp').innerText=Math.max(0,gameState.playerHP);
      document.getElementById('battle-log').innerText=`👾 敵の攻撃！ ${atk} ダメージ`;
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

function renderDeckEdit(){
  document.getElementById('deck-count').innerText=gameState.currentDeck.length;
  const list=document.getElementById('deck-list'); list.innerHTML="";
  [...new Set(gameState.collection.map(c=>c.name))].forEach(name=>{
    const owned=gameState.collection.filter(c=>c.name===name).length;
    const inD=gameState.currentDeck.filter(c=>c.name===name).length;
    const card=gameState.collection.find(c=>c.name===name);
    const val=card.name==="ボツリヌス毒素"?"継続200":(card.healPower>0?`HEAL+${card.healPower}`:`PWR ${formatPower(card.attackPower)}`);
    const div=document.createElement('div'); div.className=`deck-item ${inD>0?'in-deck':''}`;
    div.innerHTML=`<div style="display:flex;gap:6px;align-items:center"><span class="card-rarity rarity-${card.rarity}">${card.rarity}</span><div><div style="font-size:13px;font-weight:bold;color:${inD>0?'#4ade80':'#fff'}">${name} [${inD}/${owned}]</div><div style="font-size:9px;color:#888">${card.formula} | ${val}</div></div></div>
      <div style="display:flex;gap:4px">${inD>0?`<button class="action-btn" style="color:#ef4444" onclick="removeFromDeck('${name}')">➖</button>`:''}
      <button class="action-btn" style="color:${inD<owned&&gameState.currentDeck.length<40?'#3b82f6':'#555'}" onclick="addToDeck('${name}')" ${inD>=owned||gameState.currentDeck.length>=40?'disabled':''}>➕</button></div>`;
    list.appendChild(div);
  });
  const btn=document.getElementById('deck-done-btn');
  if(gameState.currentDeck.length>=20){btn.disabled=false;btn.style.background='linear-gradient(135deg,#10b981,#14b8a6)';}
  else{btn.disabled=true;btn.style.background='#555';}
}
function addToDeck(name){
  const owned=gameState.collection.filter(c=>c.name===name).length;
  const inD=gameState.currentDeck.filter(c=>c.name===name).length;
  const card=gameState.collection.find(c=>c.name===name);
  if(card&&gameState.currentDeck.length<40&&inD<owned){gameState.currentDeck.push({...card,id:Math.random().toString(36).substr(2,9)});renderDeckEdit();}
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
  gameState.collection.push(newCard); saveGame(true);
  let val=newCard.name==="ボツリヌス毒素"?"継続200/ターン":(newCard.healPower>0?`HEAL+${newCard.healPower}`:`PWR ${formatPower(newCard.attackPower)}`);
  const res=document.getElementById('gacha-result');
  res.innerHTML=`<span class="card-rarity rarity-${newCard.rarity}">${newCard.rarity}</span>
    <div style="font-size:16px;font-weight:bold;margin:4px 0">${newCard.name}</div>
    <div style="font-size:11px;color:#ccc">${newCard.formula}</div>
    <div style="font-size:10px;color:#facc15;margin-top:3px">${val} | ${newCard.attribute}</div>
    <div style="font-size:10px;color:#94a3b8;margin-top:2px">色: ${newCard.color||"-"} ／ 匂い: ${newCard.odor||"-"}</div>`;
  res.style.borderColor=newCard.rarity==='SSSR'?'#ff00ff':(newCard.rarity==='SSR'?'#f97316':(newCard.rarity==='SR'?'#a855f7':'#3b82f6'));
}
</script>
</body>
</html>
