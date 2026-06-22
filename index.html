<!DOCTYPE html>
<html lang="de">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=0">
    <title>Theos KI-Engine</title>
    <link rel="stylesheet" href="https://unpkg.com/@chrisoakman/chessboardjs@1.0.0/dist/chessboard-1.0.0.min.css">
    
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/@emailjs/browser@4/dist/email.min.js"></script>
    <script type="text/javascript">
        window.addEventListener('DOMContentLoaded', function() {
            if (window.emailjs) {
                window.emailjs.init({
                  publicKey: "nopyo_6xb4xN_cWdW", 
                });
            }
        });
    </script>

    <style>
        body { 
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif; 
            display: flex; flex-direction: column; align-items: center; 
            background-color: #f4f4f9; color: #333; margin-top: 10px; 
            padding: 0 15px 50px 15px; box-sizing: border-box;
        }
        
        h2 { text-align: center; margin-bottom: 5px; color: #1a1a1a; }
        
        .auth-panel {
            background: #fff; padding: 10px 15px; border-radius: 8px; 
            box-shadow: 0 2px 4px rgba(0,0,0,0.1); margin-bottom: 15px;
            width: 100%; max-width: 400px; display: flex; justify-content: space-between; align-items: center;
        }

        .settings {
            margin-bottom: 15px; display: flex; flex-wrap: wrap; 
            justify-content: center; gap: 15px; font-size: 0.95em;
            background: #e9ecef; padding: 10px; border-radius: 8px; width: 100%; max-width: 400px;
        }
        
        .settings-group { display: flex; align-items: center; gap: 5px; }
        
        select {
            padding: 6px 10px; font-size: 1em; border-radius: 5px;
            border: 1px solid #ccc; background-color: white; cursor: pointer;
        }

        #app-container {
            width: 100%; max-width: 400px; display: none; 
            flex-direction: column; align-items: center;
        }

        #board { 
            width: 100%; box-shadow: 0 6px 12px rgba(0,0,0,0.3); 
            touch-action: none; border-radius: 4px; overflow: hidden;
        }
        
        #status { 
            margin-top: 15px; font-size: 1.2em; font-weight: bold; 
            text-align: center; color: #0056b3; min-height: 28px; width: 100%;
        }
        
        #calc-info {
            font-size: 0.85em; color: #666; margin-top: 5px; text-align: center; font-style: italic;
            display: flex; flex-direction: column; gap: 4px; width: 100%;
        }

        .cloud-status { font-weight: bold; color: #d39e00; }

        .control-panel { 
            margin-top: 15px; display: flex; gap: 8px; flex-wrap: wrap; 
            justify-content: center; width: 100%;
        }
        
        button { 
            padding: 10px 12px; font-size: 0.9em; cursor: pointer; font-weight: bold;
            background-color: #0056b3; color: white; border: none; border-radius: 6px; 
            transition: all 0.2s; flex-grow: 1; text-align: center; box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        button:hover { background-color: #004494; transform: translateY(-1px); }
        button.secondary { background-color: #28a745; }
        button.secondary:hover { background-color: #218838; }
        button.accent { background-color: #17a2b8; }
        button.accent:hover { background-color: #138496; }
        button.danger { background-color: #dc3545; }
        button.danger:hover { background-color: #c82333; }
        button.gold { background-color: #ffc107; color: #000; width: 100%; margin-top: 5px; }
        button.gold:hover { background-color: #e0a800; }
        button.export { background-color: #6c757d; }
        button.export:hover { background-color: #5a6268; }
        button.purple { background-color: #6f42c1; }
        button.purple:hover { background-color: #5a32a3; }
        button.cloud-save { background-color: #20c997; color: white; }
        button.cloud-save:hover { background-color: #1aa179; }

        /* Login Modal */
        #auth-modal {
            display: flex; position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
            background: rgba(0,0,0,0.8); z-index: 1000; justify-content: center; align-items: center;
        }
        
        .modal-content {
            background: white; padding: 25px; border-radius: 8px; width: 300px;
            display: flex; flex-direction: column; gap: 10px; box-shadow: 0 10px 25px rgba(0,0,0,0.5);
        }
        
        .modal-content input { padding: 10px; border: 1px solid #ccc; border-radius: 4px; font-size: 1em; }
        .highlight-move { box-shadow: inset 0 0 0 5px rgba(20, 85, 30, 0.5) !important; cursor: pointer; }
        .hidden-input { display: none; }
    </style>
</head>
<body>

    <h2>Theos KI-Engine</h2>
    
    <div class="auth-panel">
        <div>Account: <span id="user-info" style="font-weight:bold; color: #dc3545;">Nicht angemeldet</span></div>
        <button id="logout-btn" onclick="window.logoutUser()" class="danger" style="display:none; padding: 5px 10px; font-size: 0.85em; flex-grow: 0;">Ausloggen</button>
    </div>

    <div id="auth-modal">
        <div class="modal-content">
            <h3 style="margin-top:0; text-align: center;">Login erforderlich</h3>
            <p style="font-size:0.85em; color:#666; text-align: center;">Login/Sign up</p>
            
            <div id="login-section" style="display: flex; flex-direction: column; gap: 10px;">
                <input type="text" id="name-input" placeholder="Vorname (Nur für Neu-Registrierung)" />
                <input type="email" id="email-input" placeholder="E-Mail Adresse (mit @)" />
                <input type="password" id="password-input" placeholder="Passwort (min. 6 Zeichen)" />
                <button onclick="window.loginUser()">Einloggen</button>
                <button class="secondary" onclick="window.registerUser()">Neu Registrieren</button>
            </div>

            <div id="verify-section" style="display:none; flex-direction:column; gap:10px;">
                <p style="font-size:0.85em; color:#0056b3; text-align: center; font-weight: bold;">Wir haben dir einen Code gesendet!</p>
                <input type="text" id="code-input" placeholder="6-stelliger Code" style="text-align: center; font-size: 1.2em; letter-spacing: 2px;" />
                <button class="secondary" onclick="window.verifyCode()">Code bestätigen</button>
                <button class="danger" onclick="window.cancelVerification()">Abbrechen</button>
            </div>

            <div id="auth-error" style="color:#dc3545; font-size:0.85em; font-weight:bold; text-align: center;"></div>
        </div>
    </div>

    <div id="history-modal" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.8); z-index:1000; justify-content:center; align-items:center;">
        <div class="modal-content" style="width: 90%; max-width: 500px; max-height: 80vh; display: flex; flex-direction: column;">
            <div style="flex-shrink: 0;">
                <h3 style="margin-top:0; text-align: center;">Deine Cloud-Partien</h3>
                <p style="font-size:0.85em; color:#666; text-align: center;">Wähle eine Partie zum Exportieren aus.</p>
            </div>
            <div id="match-list" style="flex-grow: 1; overflow-y: auto; display: flex; flex-direction: column; gap: 10px; padding-right: 5px;">
            </div>
            <div style="flex-shrink: 0; margin-top: 10px; padding-top: 10px; border-top: 1px solid #eee;">
                <button class="secondary" onclick="document.getElementById('history-modal').style.display='none'" style="width: 100%;">Schließen</button>
            </div>
        </div>
    </div>

    <div id="app-container">
        <div class="settings">
            <div class="settings-group">
                <label for="color-select">Farbe:</label>
                <select id="color-select" onchange="window.resetGame()">
                    <option value="w">Weiß</option>
                    <option value="b">Schwarz</option>
                </select>
            </div>
            <div class="settings-group">
                <label for="depth-select">Tiefe:</label>
                <select id="depth-select">
                    <option value="1">1 (Schnell)</option>
                    <option value="2">2 (Normal)</option>
                    <option value="3" selected>3 (Meister)</option>
                    <option value="4">4 (Großmeister - Langsam)</option>
                    <option value="5">5 (Titan - Sehr langsam!)</option>
                    <option value="6">6 (Gottmodus - Extrem langsam!)</option>
                </select>
            </div>
        </div>

        <div id="board"></div>
        <div id="status">Spiel bereit. Du bist am Zug.</div>
        <div id="calc-info">
            <div>Persönliches Gehirn: <span id="brain-count">0</span> Stellungen</div>
            <div class="cloud-status" id="cloud-indicator">☁️ Warte auf Cloud-Sync...</div>
        </div>

        <div class="control-panel">
            <button onclick="window.resetGame()">Neu</button>
            <button class="export" onclick="window.showMatchHistory()">Verlauf</button>
            <button class="secondary" onclick="window.exportBrain()">Datei Sichern</button>
            <button class="accent" onclick="document.getElementById('file-input').click()">Datei Laden</button>
            <button class="purple" onclick="window.exportFullCloud()">Alles Sichern</button>
            <button class="purple" onclick="document.getElementById('full-file-input').click()">Alles Laden</button>
            <button class="accent" style="background-color: #007bff;" onclick="window.fetchBrainFromCloud()">Aus Cloud laden</button>
            <button class="cloud-save" onclick="window.saveBrainToCloud()">In Cloud speichern</button>
            <button class="danger" onclick="window.clearBrain()">Wipe</button>
        </div>
        
        <div class="control-panel" style="margin-top: 5px;">
            <button id="train-fast-btn" class="gold" onclick="window.startTrainingCamp(2)">⚡ Training (Schnell)</button>
            <button id="train-deep-btn" class="gold" onclick="window.startTrainingCamp(4)" style="background-color: #fd7e14; color: white;">🔥 Deep-Learning</button>
            <button id="cancel-training-btn" class="danger" style="display: none; width: 100%; margin-top: 5px;" onclick="window.cancelTraining()">🛑 Training abbrechen</button>
            
            <input type="file" id="file-input" class="hidden-input" accept=".json" onchange="window.importBrain(event)">
            <input type="file" id="full-file-input" class="hidden-input" accept=".json" onchange="window.importFullCloud(event)">
        </div>
    </div>

    <script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/chess.js/0.10.3/chess.min.js"></script>
    <script src="https://unpkg.com/@chrisoakman/chessboardjs@1.0.0/dist/chessboard-1.0.0.min.js"></script>

    <script type="module">
        import { initializeApp } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-app.js";
        import { getAuth, signInWithEmailAndPassword, createUserWithEmailAndPassword, signOut, onAuthStateChanged } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-auth.js";
        import { getFirestore, doc, setDoc, collection, getDocs, deleteDoc } from "https://www.gstatic.com/firebasejs/11.6.1/firebase-firestore.js";

        const firebaseConfig = {
          apiKey: "AIzaSyAwylCrju4hDPuSVf4WufcJW5x0afcitvE",
          authDomain: "schach-2cead.firebaseapp.com",
          projectId: "schach-2cead",
          storageBucket: "schach-2cead.firebasestorage.app",
          messagingSenderId: "600803864465",
          appId: "1:600803864465:web:ef8a584e619f92f4f3b430"
        };
        const appId = typeof __app_id !== 'undefined' ? __app_id : 'chess-ai-personal';
        
        const app = initializeApp(firebaseConfig);
        const auth = getAuth(app);
        const db = getFirestore(app);
        
        let currentUser = null;
        window.aiMemory = {}; 
        window.newCloudKnowledge = {}; 
        window.pendingRegistration = null;

        var board = null;
        var game = new Chess();
        var $status = $('#status');
        var $calcInfo = $('#calc-info');
        var historyOfMoves = []; 
        var playerColor = 'w'; 
        var positionsEvaluated = 0; 
        var isTraining = false;
        var trainingGamesPlayed = 0;
        var trainingGamesMax = 0;
        window.currentTrainingDepth = 2;

        function initBoard() {
            if (!board) {
                var config = {
                    draggable: true, position: 'start', onDragStart: onDragStart,
                    onDrop: onDrop, onSnapEnd: onSnapEnd,
                    pieceTheme: 'https://chessboardjs.com/img/chesspieces/wikipedia/{piece}.png'
                };
                board = Chessboard('board', config);
                $(window).resize(function() { if(board) board.resize(); });
            } else {
                board.resize();
            }
        }

        // --- AUTHENTIFIZIERUNG & DATENABRUF ---
        onAuthStateChanged(auth, (user) => {
            currentUser = user;
            if (user) {
                $('#auth-modal').hide();
                $('#app-container').css('display', 'flex');
                
                initBoard(); 
                
                $('#user-info').text(user.email).css('color', '#28a745');
                $('#logout-btn').show();
                $('#cloud-indicator').text('☁️ Verbinde mit deinem privaten Tresor...').css('color', '#d39e00');
                
                const memoryColRef = collection(db, 'artifacts', appId, 'users', user.uid, 'chessData');
                
                getDocs(memoryColRef).then((querySnapshot) => {
                    window.aiMemory = {}; 
                    let blockCount = 0;
                    
                    querySnapshot.forEach((docSnap) => {
                        Object.assign(window.aiMemory, docSnap.data());
                        blockCount++;
                    });
                    
                    window.updateBrainCount();
                    $('#cloud-indicator').text(`☁️ Privat-Gehirn erfolgreich geladen (${blockCount} Blöcke)!`).css('color', '#28a745');
                }).catch((error) => {
                    console.error("Fetch Error:", error);
                    $('#cloud-indicator').text('☁️ Fehler: Firebase Blockiert!').css('color', '#dc3545');
                });
                
                setTimeout(window.resetGame, 500);
            } else {
                window.cancelVerification();
                $('#auth-modal').css('display', 'flex');
                $('#app-container').hide();
                $('#user-info').text('Nicht angemeldet').css('color', '#dc3545');
                $('#logout-btn').hide();
                window.aiMemory = {};
            }
        });

        // --- LOGIN LOGIK ---
        window.loginUser = async function() {
            try {
                $('#auth-error').text('').css('color', '#dc3545');
                const email = $('#email-input').val().trim();
                const password = $('#password-input').val();
                await signInWithEmailAndPassword(auth, email, password);
            } catch(e) { 
                $('#auth-error').text("Login fehlgeschlagen: " + e.message); 
            }
        };
        
        window.registerUser = async function() {
            try {
                $('#auth-error').text('').css('color', '#dc3545');
                const name = $('#name-input').val().trim();
                const email = $('#email-input').val().trim();
                const password = $('#password-input').val();
                
                if(!name) {
                    $('#auth-error').text("Bitte gib für die Registrierung deinen Vornamen ein.");
                    return;
                }
                if(!email.includes('@') || !email.includes('.')) {
                    $('#auth-error').text("Bitte gib eine vollständige E-Mail ein.");
                    return;
                }
                if(password.length < 6) {
                    $('#auth-error').text("Das Passwort muss min. 6 Zeichen lang sein.");
                    return;
                }

                if (typeof window.emailjs === 'undefined') {
                    $('#auth-error').text("E-Mail-Dienst blockiert (evtl. Adblocker?). Bitte Seite neu laden.").css('color', '#dc3545');
                    return;
                }

                const verificationCode = Math.floor(100000 + Math.random() * 900000).toString();
                $('#auth-error').text('Sende Bestätigungscode... ✉️').css('color', '#d39e00');

                const templateParams = {
                    vorname: name,
                    code: verificationCode,
                    to_email: email
                };

                await window.emailjs.send('service_u23gqgg', 'template_n8nl0zf', templateParams);

                window.pendingRegistration = { email, password, code: verificationCode };
                $('#login-section').hide();
                $('#verify-section').show();
                $('#auth-error').text('');

            } catch(e) { 
                $('#auth-error').text("Fehler beim E-Mail Versand: " + (e.text || e.message)).css('color', '#dc3545'); 
            }
        };

        window.verifyCode = async function() {
            const enteredCode = $('#code-input').val().trim();
            if(!window.pendingRegistration) return;

            if(enteredCode === window.pendingRegistration.code) {
                try {
                    $('#auth-error').text('Erstelle Account in der Cloud...').css('color', '#28a745');
                    await createUserWithEmailAndPassword(auth, window.pendingRegistration.email, window.pendingRegistration.password);
                } catch(e) {
                    $('#auth-error').text("Firebase Fehler: " + e.message).css('color', '#dc3545');
                    window.cancelVerification();
                }
            } else {
                $('#auth-error').text("Der Code ist leider falsch. Bitte überprüfe deine Eingabe.").css('color', '#dc3545');
            }
        };

        window.cancelVerification = function() {
            window.pendingRegistration = null;
            $('#verify-section').hide();
            $('#login-section').show();
            $('#code-input').val('');
            $('#auth-error').text('');
        };
        
        window.logoutUser = async function() { await signOut(auth); };

        window.updateBrainCount = function() {
            document.getElementById('brain-count').innerText = Object.keys(window.aiMemory).length;
        };

        function removeHighlights() { $('#board .square-55d63').removeClass('highlight-move'); }
        
        function getBaseFen(fen) { return fen.split(' ').slice(0, 2).join(' '); }
        
        function getFenBucket(fen) {
            let hash = 0;
            for (let i = 0; i < fen.length; i++) {
                hash = (hash << 5) - hash + fen.charCodeAt(i);
                hash |= 0;
            }
            return Math.abs(hash) % 1000000; 
        }

        function onDragStart (source, piece, position, orientation) {
            if (isTraining || game.game_over() || piece.charAt(0) !== playerColor) return false;
            removeHighlights();
            var moves = game.moves({ square: source, verbose: true });
            if (moves.length === 0) return false;
            for (var i = 0; i < moves.length; i++) $('#board .square-' + moves[i].to).addClass('highlight-move');
        }

        function onDrop (source, target) {
            removeHighlights();
            var move = game.move({ from: source, to: target, promotion: 'q' });
            if (move === null) return 'snapback';
            historyOfMoves.push(getBaseFen(game.fen()));
            $status.html("KI denkt nach... 🧠").css("color", "#dc3545"); 
            window.setTimeout(makeAiMove, 10);
        }

        function onSnapEnd () { board.position(game.fen()); }

        var pieceValues = { 'p': 100, 'n': 320, 'b': 330, 'r': 500, 'q': 900, 'k': 20000 };

        function evaluateBoard(gameObj, currentDepth) {
            currentDepth = currentDepth || 0; 
            if (gameObj.in_checkmate()) return gameObj.turn() === 'w' ? -10000000 - currentDepth : 10000000 + currentDepth;
            if (gameObj.in_draw() || gameObj.in_stalemate() || gameObj.in_threefold_repetition()) return 0; 

            var totalEvaluation = 0;
            var boardArray = gameObj.board();
            for (var i = 0; i < 8; i++) {
                for (var j = 0; j < 8; j++) {
                    var piece = boardArray[i][j];
                    if (piece) {
                        var val = pieceValues[piece.type];
                        if (piece.type === 'n' || piece.type === 'b' || piece.type === 'p') {
                            val += (7 - (Math.abs(3.5 - i) + Math.abs(3.5 - j))) * 5; 
                        }
                        totalEvaluation += piece.color === 'w' ? val : -val;
                    }
                }
            }
            var currentFen = getBaseFen(gameObj.fen());
            if (window.aiMemory[currentFen]) totalEvaluation += window.aiMemory[currentFen]; 
            return totalEvaluation;
        }

        function minimax(gameObj, depth, alpha, beta, isMaximizingPlayer) {
            positionsEvaluated++;
            if (depth === 0 || gameObj.game_over()) return evaluateBoard(gameObj, depth); 

            var moves = gameObj.moves();
            moves.sort(function(a, b) { 
                return ((b.includes('#') ? 100 : 0) + (b.includes('+') ? 50 : 0) + (b.includes('x') ? 10 : 0)) - ((a.includes('#') ? 100 : 0) + (a.includes('+') ? 50 : 0) + (a.includes('x') ? 10 : 0));
            });

            if (isMaximizingPlayer) {
                var bestVal = -Infinity;
                for (var i = 0; i < moves.length; i++) {
                    gameObj.move(moves[i]);
                    bestVal = Math.max(bestVal, minimax(gameObj, depth - 1, alpha, beta, !isMaximizingPlayer));
                    gameObj.undo();
                    alpha = Math.max(alpha, bestVal);
                    if (beta <= alpha) break; 
                }
                return bestVal;
            } else {
                var bestVal = Infinity;
                for (var i = 0; i < moves.length; i++) {
                    gameObj.move(moves[i]);
                    bestVal = Math.min(bestVal, minimax(gameObj, depth - 1, alpha, beta, !isMaximizingPlayer));
                    gameObj.undo();
                    beta = Math.min(beta, bestVal);
                    if (beta <= alpha) break; 
                }
                return bestVal;
            }
        }

        function makeAiMove () {
            if (game.game_over()) { window.updateStatusUI(); return; }

            var depth = parseInt(document.getElementById('depth-select').value);
            positionsEvaluated = 0; 
            var startTime = new Date().getTime();

            var possibleMoves = game.moves();
            possibleMoves.sort(function(a, b) { 
                return ((b.includes('#') ? 100 : 0) + (b.includes('+') ? 50 : 0) + (b.includes('x') ? 10 : 0)) - ((a.includes('#') ? 100 : 0) + (a.includes('+') ? 50 : 0) + (a.includes('x') ? 10 : 0));
            });

            var bestMove = possibleMoves[0]; 
            var aiColor = playerColor === 'w' ? 'b' : 'w';
            var isAiWhite = (aiColor === 'w');
            var bestValue = isAiWhite ? -Infinity : Infinity; 

            for (var i = 0; i < possibleMoves.length; i++) {
                var move = possibleMoves[i];
                game.move(move); 
                var boardValue = minimax(game, depth - 1, -Infinity, Infinity, !isAiWhite);
                game.undo(); 
                boardValue += (Math.random() * 0.1) * (isAiWhite ? 1 : -1);

                if (isAiWhite) { if (boardValue > bestValue) { bestValue = boardValue; bestMove = move; } } 
                else { if (boardValue < bestValue) { bestValue = boardValue; bestMove = move; } }
            }

            var calcTime = ((new Date().getTime() - startTime) / 1000).toFixed(1);
            game.move(bestMove);
            historyOfMoves.push(getBaseFen(game.fen()));
            board.position(game.fen());
            
            $('#cloud-indicator').text(`☁️ Berechnet: ${positionsEvaluated} Züge in ${calcTime}s`).css('color', '#666');
            window.updateStatusUI();
        }

        window.updateStatusUI = function() {
            var statusHTML = '';
            var turnColor = game.turn(); 
            var moveColorText = turnColor === 'b' ? 'Schwarz' : 'Weiß';

            $status.css("color", "#333"); 
            var isGameOver = false;
            var winnerColor = null;

            if (game.in_checkmate()) {
                statusHTML = '🏆 Schachmatt! ' + moveColorText + ' verliert.';
                isGameOver = true;
                winnerColor = turnColor === 'w' ? 'b' : 'w';
            } else if (game.in_draw()) {
                statusHTML = '🤝 Unentschieden!';
                isGameOver = true;
                winnerColor = 'draw';
            } else {
                statusHTML = moveColorText + ' ist am Zug.';
                if (game.in_check()) statusHTML += ' (Schach!)';
            }
            
            $status.html(statusHTML);
            window.updateBrainCount();

            if (isGameOver) {
                setTimeout(function() { learnFromGame(winnerColor, false); }, 100);
            }
        };

        // --- PARTIEN-VERLAUF & EXPORTIEREN (PGN) ---
        window.fetchedMatches = [];
        window.showMatchHistory = async function() {
            if (!currentUser) return;
            
            document.getElementById('history-modal').style.display = 'flex';
            $('#match-list').html('<p style="text-align:center;">Lade Partien aus der Cloud... ☁️</p>');

            try {
                const matchesColRef = collection(db, 'artifacts', appId, 'users', currentUser.uid, 'savedMatches');
                const snapshot = await getDocs(matchesColRef);
                
                window.fetchedMatches = [];
                snapshot.forEach(doc => {
                    window.fetchedMatches.push({ id: doc.id, ...doc.data() });
                });

                window.fetchedMatches.sort((a, b) => new Date(b.date) - new Date(a.date));

                if (window.fetchedMatches.length === 0) {
                    $('#match-list').html('<p style="text-align:center; color:#666;">Noch keine Partien in der Cloud gespeichert.</p>');
                    return;
                }

                let html = '';
                window.fetchedMatches.forEach((m, index) => {
                    let d = new Date(m.date).toLocaleString('de-DE');
                    let resultText = "Unentschieden";
                    if(m.winner === 'w') resultText = "Weiß gewinnt";
                    if(m.winner === 'b') resultText = "Schwarz gewinnt";
                    
                    html += `
                        <div style="border: 1px solid #ccc; padding: 10px; border-radius: 5px; display: flex; justify-content: space-between; align-items: center;">
                            <div style="text-align: left;">
                                <strong>${d}</strong><br>
                                <span style="font-size: 0.85em; color: #666;">${m.movesCount} Halbzüge | ${resultText}</span>
                            </div>
                            <button class="accent" style="width: auto; padding: 5px 10px; flex-grow: 0;" onclick="window.downloadSpecificPGN(${index})">PGN Download</button>
                        </div>
                    `;
                });
                $('#match-list').html(html);

            } catch (err) {
                $('#match-list').html('<p style="color:red; text-align:center;">Fehler beim Laden: ' + err.message + '</p>');
            }
        };

        window.downloadSpecificPGN = function(index) {
            let match = window.fetchedMatches[index];
            if (!match || !match.pgn) return;
            var dataStr = "data:text/plain;charset=utf-8," + encodeURIComponent(match.pgn);
            var dl = document.createElement('a');
            dl.setAttribute("href", dataStr);
            dl.setAttribute("download", `Partie_${new Date(match.date).getTime()}.pgn`);
            document.body.appendChild(dl); dl.click(); dl.remove();
        };

        // --- LERNEN UND CLOUD SYNC ---
        function learnFromGame(winnerColor, isSilent) {
            var baseReward = 0;
            if (winnerColor === 'w') baseReward = 300;      
            if (winnerColor === 'b') baseReward = -300;    
            
            if (baseReward !== 0 && currentUser) {
                var totalMoves = historyOfMoves.length;
                
                historyOfMoves.forEach(function(baseFen, index) {
                    var factor = Math.pow(0.9, totalMoves - 1 - index); 
                    var calculatedReward = Math.round(baseReward * factor);

                    if (!window.aiMemory[baseFen]) window.aiMemory[baseFen] = 0;
                    window.aiMemory[baseFen] += calculatedReward;
                    
                    if (window.aiMemory[baseFen] > 2000) window.aiMemory[baseFen] = 2000;
                    if (window.aiMemory[baseFen] < -2000) window.aiMemory[baseFen] = -2000;
                    
                    window.newCloudKnowledge[baseFen] = window.aiMemory[baseFen];
                });
                
                window.updateBrainCount();
            }

            if (currentUser && Object.keys(window.newCloudKnowledge).length > 0) {
                let bucketUpdates = {};
                for (let fen in window.newCloudKnowledge) {
                    let bucket = getFenBucket(fen);
                    if (!bucketUpdates[bucket]) bucketUpdates[bucket] = {};
                    bucketUpdates[bucket][fen] = window.newCloudKnowledge[fen];
                }

                let promises = [];
                for (let bucket in bucketUpdates) {
                    const activeRef = doc(db, 'artifacts', appId, 'users', currentUser.uid, 'chessData', 'live_learning_' + bucket);
                    promises.push(setDoc(activeRef, bucketUpdates[bucket], { merge: true }));
                }

                Promise.all(promises).then(() => {
                    if (!isSilent) $('#cloud-indicator').text('☁️ Neues Wissen verteilt gespeichert!').css('color', '#28a745');
                    window.newCloudKnowledge = {}; 
                }).catch((error) => {
                    console.error("Cloud Push Failed:", error);
                    $('#cloud-indicator').text('☁️ Fehler: ' + error.message).css('color', '#dc3545');
                });
            }

            if (currentUser && historyOfMoves.length > 0) {
                const pgnData = game.pgn();
                const matchRef = doc(collection(db, 'artifacts', appId, 'users', currentUser.uid, 'savedMatches'));
                setDoc(matchRef, {
                    pgn: pgnData,
                    winner: winnerColor,
                    movesCount: historyOfMoves.length,
                    date: new Date().toISOString()
                }).catch(e => console.error("Partie konnte nicht gespeichert werden:", e));
            }
        }

        window.startTrainingCamp = function(depthMode) {
            window.currentTrainingDepth = depthMode;
            var modeName = depthMode === 4 ? "Deep-Learning (Tiefe 4)" : "Schnell (Tiefe 2)";
            var gamesToPlay = parseInt(prompt("Wie viele Partien simulieren?\n\nModus: " + modeName + "\n(Tiefe 4 dauert deutlich länger!)", "1"));
            
            if (gamesToPlay > 0) {
                isTraining = true;
                trainingGamesPlayed = 0;
                trainingGamesMax = gamesToPlay;
                
                $('#train-fast-btn').hide();
                $('#train-deep-btn').hide();
                $('#cancel-training-btn').show();

                game.reset();
                historyOfMoves = [];
                $status.html("⚡ Trainingslager läuft! Partie 1 / " + trainingGamesMax + " [" + modeName + "]").css("color", "#d39e00");
                setTimeout(runTrainingStep, 10);
            }
        };

        window.cancelTraining = function() {
            if (isTraining) {
                isTraining = false;
                $('#cancel-training-btn').hide();
                $('#train-fast-btn').show();
                $('#train-deep-btn').show();
                $status.html("🛑 Trainingslager manuell abgebrochen!").css("color", "#dc3545");
                setTimeout(window.resetGame, 1500);
            }
        };

        function runTrainingStep() {
            if (!isTraining) return;
            if (game.game_over() || historyOfMoves.length > 150) { 
                var result = 'draw';
                if (game.in_checkmate()) result = game.turn() === 'w' ? 'b' : 'w';
                learnFromGame(result, true); 
                
                trainingGamesPlayed++;
                var modeName = window.currentTrainingDepth === 4 ? "Deep-Learning" : "Schnell";
                $status.html("⚡ Trainingslager: Partie " + (trainingGamesPlayed + 1) + " / " + trainingGamesMax + " [" + modeName + "]");
                
                if (trainingGamesPlayed >= trainingGamesMax) {
                    isTraining = false;
                    $('#cancel-training-btn').hide();
                    $('#train-fast-btn').show();
                    $('#train-deep-btn').show();
                    alert("🎉 Trainingslager beendet! Alle Gedanken und Partien wurden gespeichert.");
                    window.resetGame(); 
                    return;
                }
                game.reset();
                historyOfMoves = [];
                board.position('start', false); 
            } else {
                var depth = window.currentTrainingDepth; 
                var possibleMoves = game.moves();
                possibleMoves.sort((a, b) => { 
                    return ((b.includes('#') ? 100 : 0) + (b.includes('+') ? 50 : 0) + (b.includes('x') ? 10 : 0)) - ((a.includes('#') ? 100 : 0) + (a.includes('+') ? 50 : 0) + (a.includes('x') ? 10 : 0));
                });
                
                var isAiWhite = (game.turn() === 'w');
                var bestMove = possibleMoves[0];
                var bestValue = isAiWhite ? -Infinity : Infinity; 

                for (var i = 0; i < possibleMoves.length; i++) {
                    var move = possibleMoves[i];
                    game.move(move); 
                    var boardValue = minimax(game, depth - 1, -Infinity, Infinity, !isAiWhite);
                    game.undo(); 
                    boardValue += (Math.random() * 20) * (isAiWhite ? 1 : -1); 
                    if (isAiWhite) { if (boardValue > bestValue) { bestValue = boardValue; bestMove = move; } }
                    else { if (boardValue < bestValue) { bestValue = boardValue; bestMove = move; } }
                }

                game.move(bestMove);
                
                var newFen = getBaseFen(game.fen());
                historyOfMoves.push(newFen);

                if (!window.aiMemory[newFen]) window.aiMemory[newFen] = 0;
                
                var thoughtValue = bestValue;
                if (thoughtValue === Infinity) thoughtValue = 2000;
                if (thoughtValue === -Infinity) thoughtValue = -2000;
                thoughtValue = Math.round(thoughtValue);
                if (thoughtValue > 2000) thoughtValue = 2000;
                if (thoughtValue < -2000) thoughtValue = -2000;

                window.aiMemory[newFen] = Math.round((window.aiMemory[newFen] + thoughtValue) / 2);
                window.newCloudKnowledge[newFen] = window.aiMemory[newFen];
                
                if (historyOfMoves.length % 5 === 0) board.position(game.fen(), false); 
            }
            setTimeout(runTrainingStep, 10);
        }

        // --- NEU: ERZWUNGENES SPEICHERN IN DIE CLOUD ---
        window.saveBrainToCloud = async function() {
            if (!currentUser) {
                alert("Bitte logge dich ein, um in die Cloud zu speichern.");
                return;
            }
            
            const totalKeys = Object.keys(window.aiMemory).length;
            if (totalKeys === 0) {
                alert("Das Gehirn ist momentan noch leer. Es gibt nichts zu speichern.");
                return;
            }

            $('#cloud-indicator').text('☁️ Speichere gesamtes Gehirn in die Cloud (Bitte warten)...').css('color', '#d39e00');

            try {
                let bucketUpdates = {};
                
                // Wir verteilen das GANZE Gehirn auf die 1000 Eimer
                for (let fen in window.aiMemory) {
                    let bucket = getFenBucket(fen);
                    if (!bucketUpdates[bucket]) bucketUpdates[bucket] = {};
                    bucketUpdates[bucket][fen] = window.aiMemory[fen];
                }

                let promises = [];
                for (let bucket in bucketUpdates) {
                    const activeRef = doc(db, 'artifacts', appId, 'users', currentUser.uid, 'chessData', 'live_learning_' + bucket);
                    // merge: true sorgt dafür, dass alte Daten in Eimern erhalten bleiben, falls wir sie gerade nicht anfassen
                    promises.push(setDoc(activeRef, bucketUpdates[bucket], { merge: true }));
                }

                await Promise.all(promises);
                $('#cloud-indicator').text('☁️ Gehirn erfolgreich in der Cloud gesichert!').css('color', '#28a745');
                alert("Erfolgreich! " + totalKeys + " Stellungen wurden sicher in deine Cloud hochgeladen.");
                
            } catch(err) {
                console.error("Cloud Save Error:", err);
                $('#cloud-indicator').text('☁️ Fehler beim Speichern!').css('color', '#dc3545');
                alert("Fehler beim Cloud-Speichern: " + err.message);
            }
        };

        window.clearBrain = async function() {
            if(confirm("ACHTUNG: Willst du dein komplettes privates Gehirn formatieren?")) {
                if(currentUser) {
                    $('#cloud-indicator').text('☁️ Lösche Daten...').css('color', '#dc3545');
                    try {
                        const memoryColRef = collection(db, 'artifacts', appId, 'users', currentUser.uid, 'chessData');
                        const snapshot = await getDocs(memoryColRef);
                        let promises = [];
                        snapshot.forEach(docSnap => promises.push(deleteDoc(docSnap.ref)));
                        await Promise.all(promises);
                        
                        window.aiMemory = {};
                        window.updateBrainCount();
                        window.resetGame();
                        alert("Gehirn formatiert.");
                        $('#cloud-indicator').text('☁️ Privat-Gehirn formatiert.').css('color', '#28a745');
                    } catch(err) { alert("Fehler beim Löschen: " + err.message); }
                }
            }
        };

        window.exportBrain = function() {
            var dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(window.aiMemory, null, 2));
            var dl = document.createElement('a');
            dl.setAttribute("href", dataStr);
            dl.setAttribute("download", "schach_privat_backup.json");
            document.body.appendChild(dl); dl.click(); dl.remove();
        };

        // --- ALLES SICHERN (Cloud-Backup: Gehirn + Alle Partien) ---
        window.exportFullCloud = async function() {
            if (!currentUser) {
                alert("Bitte logge dich ein, um ein komplettes Cloud-Backup herunterzuladen.");
                return;
            }
            $('#cloud-indicator').text('☁️ Erstelle Komplett-Backup...').css('color', '#d39e00');
            try {
                const matchesColRef = collection(db, 'artifacts', appId, 'users', currentUser.uid, 'savedMatches');
                const matchesSnap = await getDocs(matchesColRef);
                let matchesData = [];
                matchesSnap.forEach(doc => {
                    matchesData.push({ id: doc.id, ...doc.data() });
                });

                const fullBackup = {
                    timestamp: new Date().toISOString(),
                    userEmail: currentUser.email,
                    brainSize: Object.keys(window.aiMemory).length,
                    matchesCount: matchesData.length,
                    brain: window.aiMemory,
                    matches: matchesData
                };

                var dataStr = "data:text/json;charset=utf-8," + encodeURIComponent(JSON.stringify(fullBackup, null, 2));
                var dl = document.createElement('a');
                dl.setAttribute("href", dataStr);
                dl.setAttribute("download", `schach_komplett_backup_${new Date().getTime()}.json`);
                document.body.appendChild(dl); dl.click(); dl.remove();

                $('#cloud-indicator').text('☁️ Komplett-Backup heruntergeladen!').css('color', '#28a745');
            } catch (err) {
                console.error("Backup Error:", err);
                $('#cloud-indicator').text('☁️ Fehler beim Backup!').css('color', '#dc3545');
                alert("Fehler beim Erstellen des Backups: " + err.message);
            }
        };

        // --- ALLES LADEN (Cloud-Backup wiederherstellen) ---
        window.importFullCloud = async function(event) {
            var input = event.target;
            var reader = new FileReader();
            
            reader.onload = async function() {
                try {
                    var importedData = JSON.parse(reader.result);
                    if (typeof importedData === 'object' && currentUser) {
                        
                        if (!importedData.brain || !importedData.matches) {
                            alert("Das ist kein gültiges Komplett-Backup! Benutze für reine Gehirn-Dateien bitte 'Datei Laden'.");
                            return;
                        }

                        $('#cloud-indicator').text('☁️ Stelle Komplett-Backup wieder her (Bitte warten)...').css('color', '#d39e00');
                        
                        Object.assign(window.aiMemory, importedData.brain);
                        window.updateBrainCount();

                        let promises = [];
                        
                        // Das importierte Gehirn auf die neuen 1000 Eimer aufteilen!
                        let bucketUpdates = {};
                        for (let fen in importedData.brain) {
                            let bucket = getFenBucket(fen);
                            if (!bucketUpdates[bucket]) bucketUpdates[bucket] = {};
                            bucketUpdates[bucket][fen] = importedData.brain[fen];
                        }

                        for (let bucket in bucketUpdates) {
                            const activeRef = doc(db, 'artifacts', appId, 'users', currentUser.uid, 'chessData', 'live_learning_' + bucket);
                            promises.push(setDoc(activeRef, bucketUpdates[bucket], { merge: true }));
                        }

                        importedData.matches.forEach(match => {
                            let matchRef;
                            if (match.id) {
                                matchRef = doc(db, 'artifacts', appId, 'users', currentUser.uid, 'savedMatches', match.id);
                            } else {
                                matchRef = doc(collection(db, 'artifacts', appId, 'users', currentUser.uid, 'savedMatches'));
                            }
                            
                            let matchData = { ...match };
                            delete matchData.id; 
                            
                            promises.push(setDoc(matchRef, matchData, { merge: true }));
                        });
                        
                        await Promise.all(promises);

                        alert("Komplett-Backup erfolgreich in deine Cloud geladen!\n" + Object.keys(importedData.brain).length + " Stellungen und " + importedData.matches.length + " Partien wiederhergestellt.");
                        $('#cloud-indicator').text('☁️ Komplett-Backup erfolgreich wiederhergestellt!').css('color', '#28a745');
                        window.resetGame();

                    } else if (!currentUser) {
                        alert("Bitte logge dich erst ein!");
                    }
                } catch (e) { 
                    alert("Fehler beim Lesen der JSON-Datei: " + e.message); 
                }
                input.value = ''; 
            };
            
            if (input.files[0]) reader.readAsText(input.files[0]);
        };

        window.fetchBrainFromCloud = async function() {
            if (!currentUser) {
                alert("Bitte logge dich ein, um Daten aus der Cloud zu laden.");
                return;
            }
            $('#cloud-indicator').text('☁️ Lade Daten aus der Cloud...').css('color', '#d39e00');
            try {
                const memoryColRef = collection(db, 'artifacts', appId, 'users', currentUser.uid, 'chessData');
                const querySnapshot = await getDocs(memoryColRef);
                
                window.aiMemory = {}; 
                let blockCount = 0;
                
                querySnapshot.forEach((docSnap) => {
                    Object.assign(window.aiMemory, docSnap.data());
                    blockCount++;
                });
                
                window.updateBrainCount();
                $('#cloud-indicator').text(`☁️ Cloud-Gehirn manuell geladen (${blockCount} Blöcke)!`).css('color', '#28a745');
                alert(`Erfolgreich synchronisiert! ${Object.keys(window.aiMemory).length} Stellungen geladen.`);
                window.resetGame();
            } catch (error) {
                console.error("Fetch Error:", error);
                $('#cloud-indicator').text('☁️ Fehler beim Cloud-Sync!').css('color', '#dc3545');
                alert("Fehler: " + error.message);
            }
        };

        window.importBrain = function(event) {
            var input = event.target;
            var reader = new FileReader();
            reader.onload = function() {
                try {
                    var importedData = JSON.parse(reader.result);
                    if (typeof importedData === 'object' && currentUser) {
                        $('#cloud-indicator').text('☁️ Lade Daten hoch (Bitte warten)...').css('color', '#d39e00');
                        
                        Object.assign(window.aiMemory, importedData);
                        window.updateBrainCount();

                        let promises = [];
                        let bucketUpdates = {};
                        for (let fen in importedData) {
                            let bucket = getFenBucket(fen);
                            if (!bucketUpdates[bucket]) bucketUpdates[bucket] = {};
                            bucketUpdates[bucket][fen] = importedData[fen];
                        }

                        for (let bucket in bucketUpdates) {
                            const activeRef = doc(db, 'artifacts', appId, 'users', currentUser.uid, 'chessData', 'live_learning_' + bucket);
                            promises.push(setDoc(activeRef, bucketUpdates[bucket], { merge: true }));
                        }
                        
                        Promise.all(promises).then(() => {
                            alert("Wissen erfolgreich hochgeladen!");
                            $('#cloud-indicator').text('☁️ Erfolgreich hochgeladen!').css('color', '#28a745');
                            window.resetGame();
                        }).catch((err) => {
                            console.error("Cloud Push Failed:", err);
                            alert("Fehler beim Cloud-Upload: " + err.message);
                            $('#cloud-indicator').text('☁️ Fehler beim Upload!').css('color', '#dc3545');
                        });
                        
                    } else if (!currentUser) alert("Bitte logge dich erst ein!");
                } catch (e) { alert("Fehler beim Lesen der JSON-Datei."); }
                input.value = ''; 
            };
            if (input.files[0]) reader.readAsText(input.files[0]);
        };

        window.resetGame = function() {
            if (isTraining || !currentUser) return; 

            $('#cancel-training-btn').hide();
            $('#train-fast-btn').show();
            $('#train-deep-btn').show();

            playerColor = document.getElementById('color-select').value;
            game.reset(); 
            if (board) {
                board.resize(); 
                board.start();
                board.orientation(playerColor === 'w' ? 'white' : 'black');
            }
            historyOfMoves = []; removeHighlights();
            window.updateStatusUI();
            
            if (playerColor === 'b') {
                $status.html("KI denkt nach... 🧠").css("color", "#dc3545");
                window.setTimeout(makeAiMove, 10);
            }
        };

    </script>
</body>
</html>
