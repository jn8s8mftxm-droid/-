<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=no">
    <title>有機化学バトルワールド - 拡張版</title>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <style>
        * { box-sizing: border-box; margin: 0; padding: 0; user-select: none; font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif; }
        body, html { width: 100%; height: 100%; overflow: hidden; background-color: #000; color: #fff; }
        
        .screen { display: none; width: 100%; height: 100%; position: absolute; top: 0; left: 0; }
        .active { display: flex; flex-direction: column; }

        .glass-btn {
            background: linear-gradient(135deg, #3b82f6, #9333ea);
            border: none; color: white; padding: 10px 16px; font-weight: bold; font-size: 14px;
            border-radius: 14px; cursor: pointer; box-shadow: 0 3px 6px rgba(0,0,0,0.4); transition: transform 0.1s;
        }
        .glass-btn:active { transform: scale(0.95); }
        .glass-btn:disabled { opacity: 0.5; cursor: not-allowed; }

        #deck-select-screen {
            background: linear-gradient(to bottom, #1a263f, #000);
            padding: 40px 20px; align-items: center; justify-content: flex-start; gap: 20px; text-align: center;
        }
        .select-card {
            background: linear-gradient(to right, #059669, #0d9488);
            border-radius: 18px; padding: 16px; margin-bottom: 16px; text-align: left; cursor: pointer;
            box-shadow: 0 4px 8px rgba(0,0,0,0.3); width: 100%; max-width: 400px;
        }
        .select-card.red { background: linear-gradient(to right, #ea580c, #dc2626); }
        .select-card.purple { background: linear-gradient(to right, #9333ea, #2563eb); }
        .badge { background: rgba(255,255,255,0.2); font-size: 10px; font-weight: bold; padding: 2px 6px; border-radius: 6px; }

        #field-screen { position: relative; width: 100%; height: 100%; }
        #canvas-container { width: 100%; height: 100%; }
        .field-ui { position: absolute; top: 0; left: 0; width: 100%; padding: 40px 16px 0; display: flex; justify-content: space-between; pointer-events: none; }
        .field-ui * { pointer-events: auto; }
        .status-box { background: rgba(0,0,0,0.6); padding: 10px; border-radius: 12px; font-size: 14px; font-weight: bold; }

        #battle-screen { 
            background: linear-gradient(to bottom, #0f172a, #1e293b); 
            padding: 40px 16px 20px; justify-content: space-between; 
        }
        .battle-header { display: flex; justify-content: space-between; align-items: flex-start; }
        #lab-canvas-container { 
            width: 100%; height: 120px; border-radius: 16px; 
            border: 2px solid #06b6d4; overflow: hidden; background: #0284c711;
        }
        .battle-log-box { background: rgba(15, 23, 42, 0.8); border: 1px solid #334155; border-radius: 12px; padding: 10px; min-height: 55px; font-size: 12px; text-align: center; display: flex; align-items: center; justify-content: center; white-space: pre-line; }
        
        .quiz-box { background: rgba(147, 51, 234, 0.4); border: 1px solid #a855f7; border-radius: 12px; padding: 10px; text-align: center; display: flex; flex-direction: column; gap: 8px; }
        .quiz-options { display: grid; grid-template-columns: 1fr 1fr; gap: 6px; }
        .quiz-btn { background: rgba(37, 99, 235, 0.85); border: none; color: white; padding: 8px; border-radius: 8px; font-size: 11px; font-weight: bold; cursor: pointer; }
        .quiz-btn:active { background: #1d4ed8; }

        .hand-container { overflow-x: auto; display: flex; gap: 8px; padding: 8px 0; }
        .card {
            min-width: 90px; width: 90px; height: 120px; background: white; color: black; border-radius: 10px; padding: 6px;
            display: flex; flex-direction: column; justify-content: space-between; cursor: pointer; box-shadow: 0 4px 6px rgba(0,0,0,0.3);
        }
        .card.selected { background: #fde047; box-shadow: 0 0 10px #fde047; transform: translateY(-5px); }
        .card-rarity { font-size: 8px; font-weight: bold; padding: 1px 4px; border-radius: 3px; color: white; width: fit-content; }
        .rarity-SSR { background: #f97316; } .rarity-SR { background: #a855f7; } .rarity-R { background: #3b82f6; }
        .rarity-SSSR { background: linear-gradient(90deg, #ff0000, #ff00ff); animation: rainbow 1.5s linear infinite; }

        @keyframes rainbow {
            0% { filter: hue-rotate(0deg); }
            100% { filter: hue-rotate(360deg); }
        }

        #deck-edit-screen { background: #111; padding: 40px 16px; height: 100%; }
        .deck-list { flex: 1; overflow-y: auto; margin-top: 10px; }
        .deck-item { display: flex; justify-content: space-between; align-items: center; background: #222; padding: 8px 10px; margin-bottom: 6px; border-radius: 8px; }
        .deck-item.in-deck { background: rgba(34, 197, 94, 0.12); }
        .action-btn { background: none; border: none; font-size: 18px; cursor: pointer; }

        #gacha-screen { background: linear-gradient(to bottom, #1a0d26, #000); padding: 40px 20px; align-items: center; gap: 20px; }
        .gacha-card-view { width: 220px; height: 160px; border-radius: 16px; border: 2px solid #a855f7; background: rgba(255,255,255,0.05); display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; padding: 10px; }
    </style>
</head>
<body>

    <div id="deck-select-screen" class="screen active">
        <h2>有機化学バトルワールド</h2>
        <p style="font-size: 13px; color: #aaa;">初期スターターデッキを選択してください</p>
        <div style="width: 100%; max-width: 400px;">
            <div class="select-card purple" onclick="assignStarterDeck('Aromatic')">
                <span class="badge">ベンゼン・濃硝酸・回復薬品</span>
                <h3 style="margin: 4px 0;">芳香族・置換反応デッキ</h3>
                <p style="font-size: 11px; opacity: 0.8;">ニトロ化・スルホン化で超高火力を狙う専門デッキ！</p>
            </div>
            <div class="select-card red" onclick="assignStarterDeck('Polymer')">
                <span class="badge">エチレン・臭素・回復薬品</span>
                <h3 style="margin: 4px 0;">付加・高分子デッキ</h3>
                <p style="font-size: 11px; opacity: 0.8;">ハロゲン付加や付加重合を使うバランス型</p>
            </div>
            <div class="select-card" onclick="assignStarterDeck('Redox')">
                <span class="badge">アルコール・酢酸・回復薬品</span>
                <h3 style="margin: 4px 0;">酸化・エステル・コントロール</h3>
                <p style="font-size: 11px; opacity: 0.8;">エステル化やけん化反応でテクニカルに勝利！</p>
            </div>
        </div>
    </div>

    <div id="field-screen" class="screen">
        <div id="canvas-container"></div>
        <div class="field-ui">
            <div class="status-box">
                <div style="color: white;">🧪 試薬: <span id="field-reagents">150</span></div>
                <div style="color: #4ade80;">❤️ HP: <span id="field-hp">200</span>/200</div>
            </div>
            <div style="display: flex; gap: 8px; flex-wrap: wrap; justify-content: flex-end;">
                <button class="glass-btn" style="background: linear-gradient(135deg, #10b981, #059669); padding: 8px 12px; font-size: 12px;" onclick="saveGame()">セーブ</button>
                <button class="glass-btn" style="background: linear-gradient(135deg, #6366f1, #4f46e5); padding: 8px 12px; font-size: 12px;" onclick="loadGame()">ロード</button>
                <button class="glass-btn" style="background: linear-gradient(135deg, #06b6d4, #3b82f6);" onclick="switchState('deckEdit')">デッキ</button>
                <button class="glass-btn" style="background: linear-gradient(135deg, #ec4899, #a855f7);" onclick="switchState('gacha')">ガチャ</button>
            </div>
        </div>
    </div>

    <div id="battle-screen" class="screen">
        <div class="battle-header">
            <div>
                <div style="color: #4ade80; font-weight: bold;">🧑 HP: <span id="battle-player-hp">200</span> / <span id="battle-player-maxhp">200</span></div>
                <div style="color: #06b6d4; font-size: 11px;">📚 山札: <span id="battle-deck-count">0</span>枚</div>
            </div>
            <div style="text-align: right;">
                <div style="font-size: 11px; color: #aaa;">👾 <span id="monster-name">敵分子</span> (Lv.<span id="monster-level">1</span>)</div>
                <div style="color: #ef4444; font-weight: bold;"><span id="monster-hp">500</span> / <span id="monster-maxhp">500</span></div>
                <div style="margin-top: 6px; display: flex; gap: 6px; justify-content: flex-end;">
                    <button class="glass-btn" style="background: linear-gradient(135deg, #06b6d4, #3b82f6); padding: 6px 10px; font-size: 11px;" onclick="switchState('deckEdit')">デッキ</button>
                    <button class="glass-btn" style="background: linear-gradient(135deg, #ec4899, #a855f7); padding: 6px 10px; font-size: 11px;" onclick="switchState('gacha')">ガチャ</button>
                </div>
            </div>
        </div>

        <div id="lab-canvas-container"></div>

        <div id="quiz-container" class="quiz-box" style="display: none;">
            <div style="font-size: 11px; color: #facc15; font-weight: bold;">📝 化学反応クイズ（正解で威力1.5倍 / 不正解は0）</div>
            <div id="quiz-question" style="font-size: 13px; font-weight: bold;"></div>
            <div id="quiz-options" class="quiz-options"></div>
        </div>

        <div id="battle-log" class="battle-log-box">実験室でのバトル開始！</div>

        <div>
            <div style="font-size: 10px; color: #aaa; margin-bottom: 2px;">手札 (<span id="hand-count">0</span>/7) ※複数枚選択で反応発生</div>
            <div id="hand-cards" class="hand-container"></div>
        </div>

        <div style="text-align: center;">
            <button id="attack-btn" class="glass-btn" style="background: linear-gradient(135deg, #ea580c, #ef4444); width: 85%; padding: 10px;" onclick="executePlayerAttack()">化学反応実行</button>
        </div>
    </div>

    <div id="deck-edit-screen" class="screen">
        <div style="display: flex; justify-content: space-between; align-items: center;">
            <div>
                <h3>デッキ編集 (<span id="deck-count">0</span>/40)</h3>
                <p style="font-size: 11px; color: #888;">🟢 デッキ中 ⚪ 未編成（所持枚数まで）</p>
            </div>
            <button id="deck-done-btn" class="glass-btn" onclick="finishDeckEdit()">完了</button>
        </div>
        <div id="deck-list" class="deck-list"></div>
    </div>

    <div id="gacha-screen" class="screen">
        <h2 style="margin-top: 20px;">🧪 化合物ガチャ</h2>
        <p style="color: #06b6d4;">所持試薬: <span id="gacha-reagents">150</span></p>
        
        <div id="gacha-result" class="gacha-card-view">
            <span style="color: #888;">ガチャを回すと出現</span>
        </div>

        <div style="display: flex; gap: 10px; flex-wrap: wrap; justify-content: center;">
            <button class="glass-btn" style="background: linear-gradient(135deg, #ec4899, #a855f7); padding: 12px 24px;" onclick="drawGacha()">ガチャ (試薬100)</button>
            <button class="glass-btn" style="background: linear-gradient(135deg, #10b981, #059669);" onclick="saveGame()">セーブ</button>
            <button class="glass-btn" style="background: linear-gradient(135deg, #6366f1, #4f46e5);" onclick="loadGame()">ロード</button>
            <button class="glass-btn" style="background: #333;" onclick="switchState('field')">フィールドに戻る</button>
        </div>
    </div>

    <script>
        const ALL_CARDS = [
            { name: "ベンゼン", formula: "C6H6", attackPower: 30, healPower: 0, attribute: "Aromatic", rarity: "SR" },
            { name: "トルエン", formula: "C6H5CH3", attackPower: 35, healPower: 0, attribute: "Aromatic", rarity: "SR" },
            { name: "エチレン", formula: "C2H4", attackPower: 25, healPower: 0, attribute: "Alkenyl", rarity: "R" },
            { name: "エタノール", formula: "C2H5OH", attackPower: 25, healPower: 0, attribute: "Alcohol", rarity: "R" },
            { name: "アセトアルデヒド", formula: "CH3CHO", attackPower: 35, healPower: 0, attribute: "Aldehyde", rarity: "R" },
            { name: "酢酸", formula: "CH3COOH", attackPower: 40, healPower: 0, attribute: "Acid", rarity: "R" },
            { name: "フェノール", formula: "C6H5OH", attackPower: 45, healPower: 0, attribute: "Phenol", rarity: "SR" },
            { name: "水酸化ナトリウム", formula: "NaOH", attackPower: 35, healPower: 0, attribute: "Base", rarity: "SR" },
            { name: "濃硝酸", formula: "HNO3", attackPower: 30, healPower: 0, attribute: "Reagent", rarity: "SR" },
            { name: "濃硫酸", formula: "H2SO4", attackPower: 30, healPower: 0, attribute: "Reagent", rarity: "SR" },
            { name: "臭素", formula: "Br2", attackPower: 35, healPower: 0, attribute: "Halogen", rarity: "R" },
            { name: "塩素", formula: "Cl2", attackPower: 35, healPower: 0, attribute: "Halogen", rarity: "R" },
            { name: "過マンガン酸カリウム", formula: "KMnO4", attackPower: 40, healPower: 0, attribute: "Oxidant", rarity: "SR" },
            { name: "水素化ホウ素ナトリウム", formula: "NaBH4", attackPower: 40, healPower: 0, attribute: "Reductant", rarity: "SR" },
            { name: "重合触媒(Ziegler)", formula: "[Cat]", attackPower: 30, healPower: 0, attribute: "Catalyst", rarity: "SSR" },
            { name: "グリシン", formula: "H2NCH2COOH", attackPower: 0, healPower: 40, attribute: "Nutrient", rarity: "R" },
            { name: "グルコース", formula: "C6H12O6", attackPower: 0, healPower: 65, attribute: "Nutrient", rarity: "SR" },
            { name: "トリニトロトルエン", formula: "C7H5N3O6", attackPower: 180, healPower: 0, attribute: "Explosive", rarity: "SSR" },
            { name: "ピクリン酸", formula: "C6H3N3O7", attackPower: 180, healPower: 0, attribute: "Explosive", rarity: "SSR" },
            { name: "フッ化水素酸", formula: "HF", attackPower: Infinity, healPower: 0, attribute: "Acid", rarity: "SSSR" },

            { name: "o-クレゾール", formula: "CH3C6H4OH", attackPower: 40, healPower: 0, attribute: "Phenol", rarity: "R" },
            { name: "m-クレゾール", formula: "CH3C6H4OH", attackPower: 40, healPower: 0, attribute: "Phenol", rarity: "R" },
            { name: "p-クレゾール", formula: "CH3C6H4OH", attackPower: 42, healPower: 0, attribute: "Phenol", rarity: "R" },
            { name: "カテコール", formula: "C6H4(OH)2", attackPower: 50, healPower: 0, attribute: "Phenol", rarity: "SR" },
            { name: "レゾルシノール", formula: "C6H4(OH)2", attackPower: 48, healPower: 0, attribute: "Phenol", rarity: "SR" },
            { name: "ヒドロキノン", formula: "C6H4(OH)2", attackPower: 55, healPower: 0, attribute: "Phenol", rarity: "SR" },
            { name: "ピロガロール", formula: "C6H3(OH)3", attackPower: 60, healPower: 0, attribute: "Phenol", rarity: "SR" },
            { name: "フロログルシノール", formula: "C6H3(OH)3", attackPower: 58, healPower: 0, attribute: "Phenol", rarity: "SR" },

            { name: "メチル基", formula: "-CH3", attackPower: 20, healPower: 0, attribute: "Hydrocarbon", rarity: "R" },
            { name: "エチル基", formula: "-C2H5", attackPower: 25, healPower: 0, attribute: "Hydrocarbon", rarity: "R" },
            { name: "プロピル基", formula: "-C3H7", attackPower: 28, healPower: 0, attribute: "Hydrocarbon", rarity: "R" },
            { name: "イソプロピル基", formula: "-CH(CH3)2", attackPower: 30, healPower: 0, attribute: "Hydrocarbon", rarity: "R" },
            { name: "ブチル基", formula: "-C4H9", attackPower: 32, healPower: 0, attribute: "Hydrocarbon", rarity: "R" },
            { name: "フェニル基", formula: "-C6H5", attackPower: 40, healPower: 0, attribute: "Hydrocarbon", rarity: "SR" },
            { name: "ベンジル基", formula: "-CH2C6H5", attackPower: 38, healPower: 0, attribute: "Hydrocarbon", rarity: "SR" },
            { name: "ビニル基", formula: "-CH=CH2", attackPower: 35, healPower: 0, attribute: "Hydrocarbon", rarity: "R" },

            { name: "ヒドロキシ基", formula: "-OH", attackPower: 25, healPower: 0, attribute: "FunctionalGroup", rarity: "R" },
            { name: "カルボキシ基", formula: "-COOH", attackPower: 40, healPower: 0, attribute: "FunctionalGroup", rarity: "SR" },
            { name: "アミノ基", formula: "-NH2", attackPower: 30, healPower: 0, attribute: "FunctionalGroup", rarity: "R" },
            { name: "アルデヒド基", formula: "-CHO", attackPower: 35, healPower: 0, attribute: "FunctionalGroup", rarity: "R" },
            { name: "ニトロ基", formula: "-NO2", attackPower: 45, healPower: 0, attribute: "FunctionalGroup", rarity: "SR" },
            { name: "スルホン基", formula: "-SO3H", attackPower: 42, healPower: 0, attribute: "FunctionalGroup", rarity: "SR" },
            { name: "ハロゲン基", formula: "-X", attackPower: 30, healPower: 0, attribute: "FunctionalGroup", rarity: "R" },

            { name: "マレイン酸", formula: "cis-HOOCCH=CHCOOH", attackPower: 55, healPower: 0, attribute: "CisTrans", rarity: "SR" },
            { name: "フマル酸", formula: "trans-HOOCCH=CHCOOH", attackPower: 55, healPower: 0, attribute: "CisTrans", rarity: "SR" },
            { name: "シス-2-ブテン", formula: "cis-CH3CH=CHCH3", attackPower: 35, healPower: 0, attribute: "CisTrans", rarity: "R" },
            { name: "トランス-2-ブテン", formula: "trans-CH3CH=CHCH3", attackPower: 35, healPower: 0, attribute: "CisTrans", rarity: "R" },
            { name: "オレイン酸", formula: "C18H34O2", attackPower: 50, healPower: 0, attribute: "CisTrans", rarity: "SR" },
            { name: "スチルベン", formula: "C6H5CH=CHC6H5", attackPower: 60, healPower: 0, attribute: "CisTrans", rarity: "SR" },

            { name: "ナフタレン", formula: "C10H8", attackPower: 55, healPower: 0, attribute: "Aromatic", rarity: "SR" },
            { name: "アントラセン", formula: "C14H10", attackPower: 70, healPower: 0, attribute: "Aromatic", rarity: "SSR" }
        ];

        let gameState = {
            reagents: 150, playerHP: 200, playerMaxHP: 200,
            collection: [], currentDeck: [], currentMonster: null
        };

        let isBattleOver = false;

        // ===== セーブ / ロード =====
        function saveGame() {
            const data = {
                reagents: gameState.reagents,
                playerHP: gameState.playerHP,
                playerMaxHP: gameState.playerMaxHP,
                collection: gameState.collection,
                currentDeck: gameState.currentDeck
            };
            localStorage.setItem('organicChemBattleSave', JSON.stringify(data));
            alert('セーブしました！');
        }

        function loadGame() {
            const saved = localStorage.getItem('organicChemBattleSave');
            if (!saved) {
                alert('セーブデータがありません');
                return;
            }
            try {
                const data = JSON.parse(saved);
                gameState.reagents = data.reagents ?? 150;
                gameState.playerHP = data.playerHP ?? 200;
                gameState.playerMaxHP = data.playerMaxHP ?? 200;
                gameState.collection = data.collection || [];
                gameState.currentDeck = data.currentDeck || [];
                updateFieldUI();
                switchState('field');
                alert('ロードしました！');
            } catch (e) {
                alert('ロードに失敗しました');
            }
        }

        function switchState(stateName) {
            document.querySelectorAll('.screen').forEach(s => s.classList.remove('active'));
            if(stateName === 'deckSelection') document.getElementById('deck-select-screen').classList.add('active');
            if(stateName === 'field') {
                document.getElementById('field-screen').classList.add('active');
                updateFieldUI();
                initThreeJS();
            }
            if(stateName === 'battle') {
                document.getElementById('battle-screen').classList.add('active');
                initLabThreeJS();
                setupBattle();
            }
            if(stateName === 'deckEdit') {
                document.getElementById('deck-edit-screen').classList.add('active');
                renderDeckEdit();
            }
            if(stateName === 'gacha') {
                document.getElementById('gacha-screen').classList.add('active');
                document.getElementById('gacha-reagents').innerText = gameState.reagents;
            }
        }

        function assignStarterDeck(type) {
            gameState.currentDeck = [];
            gameState.collection = [];

            let baseCards = [];
            if (type === 'Aromatic') {
                baseCards = [
                    ALL_CARDS[0], ALL_CARDS[0], ALL_CARDS[1], ALL_CARDS[1],
                    ALL_CARDS[8], ALL_CARDS[8], ALL_CARDS[9], ALL_CARDS[9],
                    ALL_CARDS[6], ALL_CARDS[6], ALL_CARDS[15], ALL_CARDS[16],
                    ALL_CARDS[16], ALL_CARDS[0]
                ];
            } else if (type === 'Polymer') {
                baseCards = [
                    ALL_CARDS[2], ALL_CARDS[2], ALL_CARDS[10], ALL_CARDS[11],
                    ALL_CARDS[14], ALL_CARDS[15], ALL_CARDS[16], ALL_CARDS[16],
                    ALL_CARDS[3], ALL_CARDS[5], ALL_CARDS[15]
                ];
            } else {
                baseCards = [
                    ALL_CARDS[3], ALL_CARDS[3], ALL_CARDS[5], ALL_CARDS[5],
                    ALL_CARDS[7], ALL_CARDS[7], ALL_CARDS[12], ALL_CARDS[12],
                    ALL_CARDS[15], ALL_CARDS[16], ALL_CARDS[16], ALL_CARDS[4],
                    ALL_CARDS[9]
                ];
            }

            for (let i = 0; i < 40; i++) {
                let card = baseCards[i % baseCards.length] || ALL_CARDS[0];
                let cCopy = { ...card, id: Math.random().toString(36).substr(2, 9) };
                gameState.currentDeck.push(cCopy);
                gameState.collection.push(cCopy);
            }

            gameState.playerHP = gameState.playerMaxHP;
            switchState('field');
        }

        function updateFieldUI() {
            document.getElementById('field-reagents').innerText = gameState.reagents;
            document.getElementById('field-hp').innerText = gameState.playerHP;
        }

        function createHumanoidMesh() {
            let group = new THREE.Group();
            let bodyMat = new THREE.MeshLambertMaterial({ color: 0x0284c7 });
            let skinMat = new THREE.MeshLambertMaterial({ color: 0xffdbac });
            let head = new THREE.Mesh(new THREE.SphereGeometry(0.25, 16, 16), skinMat);
            head.position.y = 0.85;
            group.add(head);
            let body = new THREE.Mesh(new THREE.CylinderGeometry(0.2, 0.15, 0.6, 16), bodyMat);
            body.position.y = 0.45;
            group.add(body);
            let armGeo = new THREE.CylinderGeometry(0.06, 0.06, 0.4, 8);
            let leftArm = new THREE.Mesh(armGeo, bodyMat);
            leftArm.position.set(-0.28, 0.45, 0);
            let rightArm = new THREE.Mesh(armGeo, bodyMat);
            rightArm.position.set(0.28, 0.45, 0);
            group.add(leftArm); group.add(rightArm);
            let legGeo = new THREE.CylinderGeometry(0.07, 0.07, 0.45, 8);
            let legMat = new THREE.MeshLambertMaterial({ color: 0x1e293b });
            let leftLeg = new THREE.Mesh(legGeo, legMat);
            leftLeg.position.set(-0.1, 0.15, 0);
            let rightLeg = new THREE.Mesh(legGeo, legMat);
            rightLeg.position.set(0.1, 0.15, 0);
            group.add(leftLeg); group.add(rightLeg);
            return group;
        }

        function createMoleculeMesh(colorHex) {
            let group = new THREE.Group();
            let mainMat = new THREE.MeshLambertMaterial({ color: colorHex });
            let subMat = new THREE.MeshLambertMaterial({ color: 0xffffff });
            let bondMat = new THREE.MeshLambertMaterial({ color: 0xcccccc });
            let center = new THREE.Mesh(new THREE.SphereGeometry(0.4, 16, 16), mainMat);
            group.add(center);
            let positions = [[0.6, 0.4, 0], [-0.6, 0.4, 0], [0, -0.6, 0.4], [0, 0.4, -0.6]];
            positions.forEach(pos => {
                let atom = new THREE.Mesh(new THREE.SphereGeometry(0.2, 12, 12), subMat);
                atom.position.set(...pos);
                group.add(atom);
                let bond = new THREE.Mesh(new THREE.CylinderGeometry(0.05, 0.05, 0.6), bondMat);
                bond.position.set(pos[0]/2, pos[1]/2, pos[2]/2);
                bond.quaternion.setFromUnitVectors(new THREE.Vector3(0, 1, 0), new THREE.Vector3(...pos).normalize());
                group.add(bond);
            });
            return group;
        }

        let scene, camera, renderer, playerNode, monsters = [], targetPlayerPos = { x: 0, z: 0 }, isThreeInit = false;
        let lastSpawnTime = 0;

        function initThreeJS() {
            if(isThreeInit) return;
            isThreeInit = true;

            const container = document.getElementById('canvas-container');
            scene = new THREE.Scene();
            scene.background = new THREE.Color(0x87ceeb);

            camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 1000);
            camera.position.set(0, 12, 10);
            camera.rotation.x = -Math.PI / 3.2;

            renderer = new THREE.WebGLRenderer({ antialias: true });
            renderer.setSize(window.innerWidth, window.innerHeight);
            container.appendChild(renderer.domElement);

            scene.add(new THREE.DirectionalLight(0xffffff, 1.2));
            scene.add(new THREE.AmbientLight(0xffffff, 0.6));

            let floor = new THREE.Mesh(new THREE.PlaneGeometry(100, 100), new THREE.MeshBasicMaterial({ color: 0x4ade80 }));
            floor.rotation.x = -Math.PI / 2;
            scene.add(floor);

            playerNode = createHumanoidMesh();
            scene.add(playerNode);

            for(let i=0; i<3; i++) spawnMonster();

            let isDragging = false, lastX = 0, lastY = 0;
            window.addEventListener('pointerdown', e => { isDragging = true; lastX = e.clientX; lastY = e.clientY; });
            window.addEventListener('pointermove', e => {
                if(!isDragging) return;
                targetPlayerPos.x = Math.max(-12, Math.min(12, targetPlayerPos.x + (e.clientX - lastX) * 0.04));
                targetPlayerPos.z = Math.max(-18, Math.min(8, targetPlayerPos.z + (e.clientY - lastY) * 0.04));
                lastX = e.clientX; lastY = e.clientY;
            });
            window.addEventListener('pointerup', () => isDragging = false);

            function animate(time) {
                requestAnimationFrame(animate);

                if(time - lastSpawnTime > 5000) {
                    let activeCount = monsters.filter(m => m.isActive).length;
                    if(activeCount < 6) spawnMonster();
                    lastSpawnTime = time;
                }

                playerNode.position.x += (targetPlayerPos.x - playerNode.position.x) * 0.15;
                playerNode.position.z += (targetPlayerPos.z - playerNode.position.z) * 0.15;
                camera.position.x = playerNode.position.x;
                camera.position.z = playerNode.position.z + 10;

                const isFieldActive = document.getElementById('field-screen').classList.contains('active');

                monsters.forEach(m => {
                    if(!m.isActive) return;
                    if (!isFieldActive) return;

                    m.mesh.rotation.y += 0.01;

                    m.changeDirTimer--;
                    if(m.changeDirTimer <= 0) {
                        m.vx = (Math.random() - 0.5) * 0.08;
                        m.vz = (Math.random() - 0.5) * 0.08;
                        m.changeDirTimer = Math.floor(Math.random() * 60) + 30;
                    }

                    m.mesh.position.x += m.vx;
                    m.mesh.position.z += m.vz;

                    if(Math.abs(m.mesh.position.x) > 14) m.vx *= -1;
                    if(m.mesh.position.z < -20 || m.mesh.position.z > 8) m.vz *= -1;

                    let dx = playerNode.position.x - m.mesh.position.x;
                    let dz = playerNode.position.z - m.mesh.position.z;
                    let dist = Math.sqrt(dx * dx + dz * dz);

                    if(dist <= 1.0) {
                        m.isActive = false; 
                        scene.remove(m.mesh);
                        gameState.currentMonster = m; 
                        switchState('battle');
                    }
                });
                renderer.render(scene, camera);
            }
            animate(0);
        }

        function spawnMonster() {
            let level = Math.floor(Math.random() * 3) + 1;
            let colorHex = level === 1 ? 0x22c55e : (level === 2 ? 0xf97316 : 0xef4444);
            let hp = 450 + level * 30;
            let atk = 12 + level * 8;
            let nameList = ["アルキル変異体", "環状高分子体", "フリーラジカル塊"];
            let name = nameList[level - 1];

            let mesh = createMoleculeMesh(colorHex);
            mesh.position.set((Math.random() - 0.5) * 18, 0.5, -Math.random() * 12 - 2);
            scene.add(mesh);

            monsters.push({
                name: name, level: level, hp: hp, maxHP: hp, attackPower: atk, mesh: mesh, isActive: true,
                vx: 0, vz: 0, changeDirTimer: 0
            });
        }

        let labScene, labCamera, labRenderer, flaskMesh, isLabInit = false;
        function initLabThreeJS() {
            if(isLabInit) return;
            isLabInit = true;

            const container = document.getElementById('lab-canvas-container');
            labScene = new THREE.Scene();
            labScene.background = new THREE.Color(0x0f172a);

            labCamera = new THREE.PerspectiveCamera(45, container.clientWidth / container.clientHeight, 0.1, 100);
            labCamera.position.set(0, 1.5, 4);

            labRenderer = new THREE.WebGLRenderer({ antialias: true });
            labRenderer.setSize(container.clientWidth, container.clientHeight);
            container.appendChild(labRenderer.domElement);

            labScene.add(new THREE.DirectionalLight(0x06b6d4, 1.5));
            labScene.add(new THREE.AmbientLight(0xffffff, 0.4));

            let group = new THREE.Group();
            let glassMat = new THREE.MeshLambertMaterial({ color: 0x38bdf8, wireframe: true });
            let body = new THREE.Mesh(new THREE.ConeGeometry(0.8, 1.2, 16), glassMat);
            let neck = new THREE.Mesh(new THREE.CylinderGeometry(0.2, 0.2, 0.6, 16), glassMat);
            neck.position.y = 0.8;
            group.add(body); group.add(neck);
            flaskMesh = group;
            labScene.add(flaskMesh);

            function animateLab() {
                requestAnimationFrame(animateLab);
                if(flaskMesh) flaskMesh.rotation.y += 0.01;
                labRenderer.render(labScene, labCamera);
            }
            animateLab();
        }

        let bDeck = [], bHand = [], bSelected = [];
        let monsterHP = 500, isPlayerTurn = true, activeQuiz = null, pendingDamage = 0, pendingHeal = 0;

        function setupBattle() {
            isBattleOver = false;
            bDeck = [...gameState.currentDeck].sort(() => Math.random() - 0.5);
            bHand = []; bSelected = [];
            monsterHP = gameState.currentMonster ? gameState.currentMonster.hp : 500;

            document.getElementById('monster-name').innerText = gameState.currentMonster.name;
            document.getElementById('monster-level').innerText = gameState.currentMonster.level;
            document.getElementById('monster-maxhp').innerText = gameState.currentMonster.maxHP;
            document.getElementById('monster-hp').innerText = monsterHP;
            document.getElementById('battle-player-hp').innerText = gameState.playerHP;

            for(let i=0; i<5; i++) drawCard();
            startPlayerTurn(true);
        }

        function startPlayerTurn(isFirst = false) {
            if (isBattleOver) return;
            isPlayerTurn = true;
            if(!isFirst) drawCard();
            document.getElementById('battle-log').innerText = isFirst ? "カードを選んで化学反応を実行してください！" : "あなたのターン！山札からカードを1枚引きました。";
            updateBattleUI();
        }

        function drawCard() { if(bHand.length < 7 && bDeck.length > 0) bHand.push(bDeck.shift()); }

        function formatPower(val) {
            return val === Infinity ? "∞" : val;
        }

        function updateBattleUI() {
            document.getElementById('battle-deck-count').innerText = bDeck.length;
            document.getElementById('hand-count').innerText = bHand.length;
            let handContainer = document.getElementById('hand-cards');
            handContainer.innerHTML = '';

            bHand.forEach(card => {
                let isSel = bSelected.some(c => c.id === card.id);
                let div = document.createElement('div');
                div.className = `card ${isSel ? 'selected' : ''}`;
                div.onclick = () => toggleSelectCard(card);
                let val = card.healPower > 0 
                    ? `<div style="font-size: 10px; color: #16a34a; font-weight: bold;">回復:+${card.healPower}</div>` 
                    : `<div style="font-size: 10px; color: #ef4444; font-weight: bold;">威力:${formatPower(card.attackPower)}</div>`;
                div.innerHTML = `
                    <div class="card-rarity rarity-${card.rarity}">${card.rarity}</div>
                    <div style="font-weight: bold; font-size: 11px;">${card.name}</div>
                    <div style="font-size: 9px; color: #666;">${card.formula}</div>
                    ${val}
                `;
                handContainer.appendChild(div);
            });
            document.getElementById('attack-btn').disabled = !(isPlayerTurn && bSelected.length > 0 && !activeQuiz);
        }

        function toggleSelectCard(card) {
            if(!isPlayerTurn || activeQuiz || isBattleOver) return;
            let idx = bSelected.findIndex(c => c.id === card.id);
            if(idx >= 0) bSelected.splice(idx, 1);
            else bSelected.push(card);
            updateBattleUI();
        }

        function executePlayerAttack() {
            if (isBattleOver) return;
            let baseDamage = 0, baseHeal = 0, quizToSet = null, logMessage = "";
            let n = bSelected.map(c => c.name);
            let hasCatalyst = n.includes("濃硫酸") || n.includes("重合触媒(Ziegler)");

            if (bSelected.length === 1 && bSelected[0].name === "フッ化水素酸") {
                baseDamage = Infinity;
                logMessage = `☠️【究極試薬】フッ化水素酸を投擲！ ダメージ ∞ ！！`;
            }
            else if (bSelected.length === 1 && (bSelected[0].name === "トリニトロトルエン" || bSelected[0].name === "ピクリン酸")) {
                baseDamage = 180;
                logMessage = `💥【爆薬】${bSelected[0].name}を起爆！ ${baseDamage} ダメージ！`;
            }
            else if ((n.includes("酢酸") && n.includes("エタノール") && n.includes("水酸化ナトリウム")) || (n.includes("酢酸") && n.includes("水酸化ナトリウム"))) {
                baseDamage = hasCatalyst ? 420 : 210;
                quizToSet = {
                    question: "【けん化】油脂やエステルに水酸化ナトリウムなどの強塩基を加えて加熱加水分解した際、生成するトリオール（アルコール）は？",
                    options: ["グリセリン", "エチレングリコール", "フェノール", "メタノール"],
                    correctIndex: 0, explanation: "正解！エステルが加水分解され、脂肪酸塩（石けん）とグリセリン（高級トリオール）が生成されます！"
                };
            }
            else if (n.includes("酢酸") && n.includes("エタノール")) {
                baseDamage = hasCatalyst ? 260 : 130;
                quizToSet = {
                    question: hasCatalyst ? "【触媒エステル化】酢酸とエタノールに濃硫酸（脱水触媒）を加えて加熱生成する芳香性の液体は？" : "【エステル化】カルボン酸とアルコールから水が取れて生じる化合物の構造は？",
                    options: ["酢酸エチル", "ジエチルエーテル", "アセトン", "アセトアルデヒド"],
                    correctIndex: 0, explanation: "正解！酢酸エチル(CH3COOCH2CH3)が生成される『エステル化』です！"
                };
            }
            else if (n.includes("ベンゼン") && n.includes("濃硝酸")) {
                baseDamage = hasCatalyst ? 360 : 130;
                quizToSet = {
                    question: "【ニトロ化】ベンゼンに濃硝酸を作用させた際に生成する化合物は？",
                    options: ["ニトロベンゼン", "安息香酸", "フェノール", "クロロベンゼン"],
                    correctIndex: 0, explanation: "正解！ニトロ基(-NO2)が置換導入されます！"
                };
            }
            else if (n.includes("トルエン") && n.includes("濃硝酸")) {
                baseDamage = hasCatalyst ? 440 : 220;
                quizToSet = {
                    question: "【爆発的ニトロ化】トルエンを濃硝酸・濃硫酸で激しくニトロ化して得られる化合物は？",
                    options: ["トリニトロトルエン(TNT)", "ピクロン酸", "ニトログリセリン", "ペルオキシド"],
                    correctIndex: 0, explanation: "正解！TNT（トリニトロトルエン）が合成され絶大な威力！"
                };
            }
            else if (n.includes("ベンゼン") && n.includes("濃硫酸")) {
                baseDamage = 150;
                quizToSet = {
                    question: "【スルホン化】ベンゼンに濃硫酸を加熱作用させて生じる親水性基を持つ化合物は？",
                    options: ["ベンゼンスルホン酸", "ベンゼン硫酸エステル", "スルホベンゼン", "フェノール"],
                    correctIndex: 0, explanation: "正解！ベンゼンスルホン酸(-SO3H)が生成されます！"
                };
            }
            else if (n.includes("エチレン") && (n.includes("臭素") || n.includes("塩素"))) {
                baseDamage = 140;
                let isBr = n.includes("臭素");
                quizToSet = {
                    question: isBr ? "【付加脱色】赤褐色の臭素水にエチレンを通した際の色の変化と生成物は？" : "【付加反応】エチレンに塩素が付加して生じる化合物は？",
                    options: isBr ? ["赤褐色が消え 1,2-ジブロモエタン", "赤褐色のまま エタノール", "黄色に変色 ブロモベンゼン", "無色のまま 酢酸"] : ["1,2-ジクロロエタン", "クロロエタン", "塩化ビニル", "クロロホルム"],
                    correctIndex: 0, explanation: "正解！二重結合が開いてハロゲンが『付加』し赤褐色が脱色します！"
                };
            }
            else if (n.includes("エチレン") && n.includes("重合触媒(Ziegler)")) {
                baseDamage = 400;
                quizToSet = {
                    question: "【付加重合】多数のエチレン分子が触媒のもと二重結合を開いて連続結合する高分子は？",
                    options: ["ポリエチレン(PE)", "ポリプロピレン(PP)", "PET樹脂", "ポリスチレン(PS)"],
                    correctIndex: 0, explanation: "正解！『付加重合』によりポリエチレン(PE)が生成！"
                };
            }
            else if ((n.includes("エタノール") || n.includes("アセトアルデヒド")) && n.includes("過マンガン酸カリウム")) {
                baseDamage = hasCatalyst ? 340 : 170;
                quizToSet = {
                    question: "【酸化反応】第一級アルコール(エタノール)を強く酸化させた際の最終生成物は？",
                    options: ["酢酸", "アセトン", "ジエチルエーテル", "メタン"],
                    correctIndex: 0, explanation: "正解！アルコール→アルデヒド→カルボン酸(酢酸)へ酸化されます！"
                };
            }
            else if (bSelected.length === 1) {
                let single = bSelected[0];
                if(single.healPower > 0) {
                    baseHeal = single.healPower;
                    logMessage = `🧪【代謝】${single.name} を吸収！ HPが ${baseHeal} 回復！`;
                } else {
                    baseDamage = single.attackPower;
                    logMessage = `⚗️【単体攻撃】${single.name} を投擲！ ${formatPower(baseDamage)} ダメージ！`;
                }
            } else {
                let healSum = bSelected.reduce((sum, c) => sum + c.healPower, 0);
                let atkSum = bSelected.reduce((sum, c) => sum + (c.attackPower === Infinity ? 99999 : c.attackPower), 0);
                if(healSum > 0 && atkSum === 0) {
                    baseHeal = healSum;
                    logMessage = `🧪【複合代謝】薬品を同時吸収！ HPが ${baseHeal} 回復！`;
                } else {
                    logMessage = "⚠️【不活性】この組み合わせでは特殊化学反応が起きませんでした。";
                }
            }

            bHand = bHand.filter(c => !bSelected.some(sc => sc.id === c.id));
            bSelected = [];

            if(quizToSet) {
                pendingDamage = baseDamage; pendingHeal = baseHeal;
                activeQuiz = quizToSet; showQuiz(quizToSet);
            } else {
                applyEffectAndEndTurn(baseDamage, baseHeal, logMessage);
            }
        }

        function showQuiz(quiz) {
            document.getElementById('battle-log').style.display = 'none';
            let qContainer = document.getElementById('quiz-container');
            qContainer.style.display = 'flex';
            document.getElementById('quiz-question').innerText = quiz.question;

            let optBox = document.getElementById('quiz-options');
            optBox.innerHTML = '';
            let choices = quiz.options.map((opt, i) => ({ text: opt, isCorrect: i === quiz.correctIndex }));
            choices.sort(() => Math.random() - 0.5);

            choices.forEach((choice) => {
                let btn = document.createElement('button');
                btn.className = 'quiz-btn';
                btn.innerText = choice.text;
                btn.onclick = () => answerQuiz(choice.isCorrect);
                optBox.appendChild(btn);
            });
            updateBattleUI();
        }

        function answerQuiz(isCorrect) {
            let finalDmg = 0, finalHeal = 0, quizLog = "";
            if(isCorrect) {
                finalDmg = pendingDamage === Infinity ? Infinity : Math.floor(pendingDamage * 1.5);
                finalHeal = Math.floor(pendingHeal * 1.5);
                let resStr = finalHeal > 0 ? `HPが ${finalHeal} 大回復！` : `${formatPower(finalDmg)} 大ダメージ！`;
                quizLog = `⭕ 正解！${activeQuiz.explanation}\n反応成功！威力1.5倍！(${resStr})`;
            } else {
                finalDmg = 0; finalHeal = 0;
                quizLog = "❌ 不正解…！ 反応失敗につき効果0です。";
            }

            document.getElementById('quiz-container').style.display = 'none';
            document.getElementById('battle-log').style.display = 'flex';
            activeQuiz = null;
            applyEffectAndEndTurn(finalDmg, finalHeal, quizLog);
        }

        function applyEffectAndEndTurn(damage, heal, message) {
            if (isBattleOver) return;

            if (damage === Infinity) {
                monsterHP = 0;
            } else {
                monsterHP -= damage;
            }
            if(heal > 0) {
                gameState.playerHP = Math.min(gameState.playerMaxHP, gameState.playerHP + heal);
                document.getElementById('battle-player-hp').innerText = gameState.playerHP;
            }
            document.getElementById('monster-hp').innerText = Math.max(0, monsterHP);
            document.getElementById('battle-log').innerText = message;

            if(monsterHP <= 0) {
                isBattleOver = true;
                let reward = 40 + (gameState.currentMonster ? gameState.currentMonster.level * 20 : 20);
                gameState.reagents += reward;
                document.getElementById('battle-log').innerText = `🎉 敵分子を分解！ 試薬 +${reward} 獲得！`;
                setTimeout(() => { switchState('field'); }, 1600);
            } else {
                setTimeout(endPlayerTurn, 2000);
            }
        }

        function endPlayerTurn() {
            if (isBattleOver) return;

            isPlayerTurn = false;
            document.getElementById('battle-log').innerText = "👾 敵分子の反撃...";
            updateBattleUI();

            setTimeout(() => {
                if (isBattleOver) return;

                if(monsterHP > 0) {
                    let enemyAtk = gameState.currentMonster ? gameState.currentMonster.attackPower : 15;
                    gameState.playerHP -= enemyAtk;
                    document.getElementById('battle-player-hp').innerText = Math.max(0, gameState.playerHP);
                    document.getElementById('battle-log').innerText = `👾 敵の反撃！ プレイヤーに ${enemyAtk} ダメージを受けた！`;

                    if(gameState.playerHP <= 0) {
                        isBattleOver = true;
                        gameState.playerHP = 0;
                        document.getElementById('battle-log').innerText = "💀 敗北しました...";
                        setTimeout(() => {
                            gameState.playerHP = gameState.playerMaxHP;
                            switchState('field');
                        }, 1500);
                        return;
                    }
                    setTimeout(() => {
                        if (!isBattleOver) startPlayerTurn();
                    }, 1500);
                } else {
                    if (!isBattleOver) startPlayerTurn();
                }
            }, 1000);
        }

        function renderDeckEdit() {
            document.getElementById('deck-count').innerText = gameState.currentDeck.length;
            let list = document.getElementById('deck-list');
            list.innerHTML = '';

            let uniqueNames = [...new Set(gameState.collection.map(c => c.name))];
            uniqueNames.forEach(name => {
                let ownedCount = gameState.collection.filter(c => c.name === name).length;
                let inDeckCount = gameState.currentDeck.filter(c => c.name === name).length;
                let card = gameState.collection.find(c => c.name === name);
                let isInDeck = inDeckCount > 0;
                let valStr = card.healPower > 0 ? `HEAL: +${card.healPower}` : `PWR: ${formatPower(card.attackPower)}`;

                let div = document.createElement('div');
                div.className = `deck-item ${isInDeck ? 'in-deck' : ''}`;
                div.innerHTML = `
                    <div style="display: flex; gap: 6px; align-items: center;">
                        <span class="card-rarity rarity-${card.rarity}">${card.rarity}</span>
                        <div>
                            <div style="font-size: 13px; font-weight: bold; color: ${isInDeck ? '#4ade80' : '#fff'};">
                                ${name} [${inDeckCount}/${ownedCount}]
                            </div>
                            <div style="font-size: 9px; color: #888;">${card.formula} | ${valStr}</div>
                        </div>
                    </div>
                    <div style="display: flex; gap: 4px;">
                        ${isInDeck ? `<button class="action-btn" style="color:#ef4444;" onclick="removeFromDeck('${name}')">➖</button>` : ''}
                        <button class="action-btn" style="color:${inDeckCount < ownedCount && gameState.currentDeck.length < 40 ? '#3b82f6' : '#555'};" 
                                onclick="addToDeck('${name}')" ${inDeckCount >= ownedCount || gameState.currentDeck.length >= 40 ? 'disabled' : ''}>➕</button>
                    </div>
                `;
                list.appendChild(div);
            });

            let doneBtn = document.getElementById('deck-done-btn');
            doneBtn.disabled = false;
            doneBtn.style.background = 'linear-gradient(135deg, #10b981, #14b8a6)';
        }

        function addToDeck(cardName) {
            let ownedCount = gameState.collection.filter(c => c.name === cardName).length;
            let inDeckCount = gameState.currentDeck.filter(c => c.name === cardName).length;
            let card = gameState.collection.find(c => c.name === cardName);
            if (card && gameState.currentDeck.length < 40 && inDeckCount < ownedCount) {
                gameState.currentDeck.push({ ...card, id: Math.random().toString(36).substr(2, 9) });
                renderDeckEdit();
            }
        }

        function removeFromDeck(cardName) {
            let idx = gameState.currentDeck.findIndex(c => c.name === cardName);
            if(idx >= 0) {
                gameState.currentDeck.splice(idx, 1);
                renderDeckEdit();
            }
        }

        function finishDeckEdit() {
            switchState('field');
        }

        function drawGacha() {
            if(gameState.reagents < 100) return;
            gameState.reagents -= 100;
            document.getElementById('gacha-reagents').innerText = gameState.reagents;

            // 確率: SSSR 0.2% / SSR 2.8% / SR 15% / R 82%
            let rand = Math.random() * 100;
            let rarity;
            if (rand < 0.2) rarity = 'SSSR';
            else if (rand < 0.2 + 2.8) rarity = 'SSR';
            else if (rand < 0.2 + 2.8 + 15) rarity = 'SR';
            else rarity = 'R';

            let candidates = ALL_CARDS.filter(c => c.rarity === rarity);
            if (candidates.length === 0) candidates = ALL_CARDS.filter(c => c.rarity === 'R');
            let pulled = candidates[Math.floor(Math.random() * candidates.length)];

            let newCard = { ...pulled, id: Math.random().toString(36).substr(2, 9) };
            gameState.collection.push(newCard);

            let valStr = newCard.healPower > 0 ? `HEAL: +${newCard.healPower}` : `PWR: ${formatPower(newCard.attackPower)}`;
            let resDiv = document.getElementById('gacha-result');
            resDiv.innerHTML = `
                <span class="card-rarity rarity-${newCard.rarity}" style="margin-bottom: 4px;">${newCard.rarity}</span>
                <div style="font-size: 16px; font-weight: bold; color: white;">${newCard.name}</div>
                <div style="font-size: 11px; color: #ccc;">${newCard.formula}</div>
                <div style="font-size: 10px; color: #facc15; margin-top: 4px;">${valStr} | 属性: ${newCard.attribute}</div>
            `;
            resDiv.style.borderColor = newCard.rarity === 'SSSR' ? '#ff00ff' : (newCard.rarity === 'SSR' ? '#f97316' : (newCard.rarity === 'SR' ? '#a855f7' : '#3b82f6'));
        }
    </script>
</body>
</html>
