# Bless.com
Blessing 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>BLESS WINNERS - Lucky Draw Slot Machine</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Arial', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2a6c, #b21f1f, #fdbb2d);
            color: white;
            min-height: 100vh;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            text-align: center;
        }
        
        header {
            margin-bottom: 30px;
            padding: 20px;
            background: rgba(0, 0, 0, 0.7);
            border-radius: 15px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }
        
        h1 {
            font-size: 3rem;
            margin-bottom: 10px;
            text-shadow: 0 2px 10px rgba(0, 0, 0, 0.5);
            color: #ffcc00;
        }
        
        h2 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #ffcc00;
        }
        
        .subtitle {
            font-size: 1.2rem;
            margin-bottom: 20px;
            color: #ffcc00;
        }
        
        .entry-fee {
            background: rgba(255, 0, 0, 0.7);
            display: inline-block;
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        .prize-info {
            background: rgba(0, 150, 0, 0.7);
            display: inline-block;
            padding: 10px 20px;
            border-radius: 30px;
            font-weight: bold;
            margin-bottom: 20px;
        }
        
        .game-area {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
        }
        
        .slot-machine {
            flex: 1;
            min-width: 300px;
            background: linear-gradient(145deg, #222, #444);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.7);
            border: 5px solid #ffcc00;
        }
        
        .slot-display {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
            height: 200px;
            background: #000;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .slot {
            flex: 1;
            border-right: 2px solid #ffcc00;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            font-weight: bold;
            color: #ffcc00;
            overflow: hidden;
            position: relative;
        }
        
        .slot:last-child {
            border-right: none;
        }
        
        .slot-inner {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            transition: transform 0.1s;
        }
        
        .slot-item {
            height: 200px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.5rem;
            color: #ffcc00;
        }
        
        .controls {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 20px;
        }
        
        button {
            padding: 12px 25px;
            font-size: 1.2rem;
            font-weight: bold;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        #spin-btn {
            background: linear-gradient(to right, #ff416c, #ff4b2b);
            color: white;
        }
        
        #spin-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(255, 65, 108, 0.5);
        }
        
        #reset-btn {
            background: linear-gradient(to right, #2193b0, #6dd5ed);
            color: white;
        }
        
        #reset-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 20px rgba(33, 147, 176, 0.5);
        }
        
        .participants {
            flex: 1;
            min-width: 300px;
            background: rgba(0, 0, 0, 0.7);
            border-radius: 15px;
            padding: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }
        
        .participant-list {
            max-height: 400px;
            overflow-y: auto;
            margin-top: 15px;
            text-align: left;
            padding: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
        }
        
        .participant {
            padding: 10px;
            margin-bottom: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            display: flex;
            justify-content: space-between;
        }
        
        .winner-display {
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            border-radius: 15px;
            margin-top: 20px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
            display: none;
            border: 3px solid #ffcc00;
        }
        
        .winner-name {
            font-size: 2.5rem;
            color: #ffcc00;
            margin: 10px 0;
            text-shadow: 0 0 10px rgba(255, 204, 0, 0.7);
        }
        
        .winner-phone {
            font-size: 1.5rem;
            margin-bottom: 10px;
        }
        
        .winner-prize {
            font-size: 2.2rem;
            color: #4cff00;
            margin: 15px 0;
            text-shadow: 0 0 10px rgba(76, 255, 0, 0.7);
            animation: pulse 1.5s infinite;
        }
        
        .winner-message {
            font-size: 1.8rem;
            color: #ffcc00;
            margin: 20px 0;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        
        .confetti {
            position: fixed;
            width: 10px;
            height: 10px;
            background-color: #f00;
            opacity: 0;
            top: 0;
            animation: confetti-fall 5s linear forwards;
        }
        
        @keyframes confetti-fall {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 1;
            }
            100% {
                transform: translateY(100vh) rotate(360deg);
                opacity: 0;
            }
        }
        
        .registration {
            background: rgba(0, 0, 0, 0.7);
            padding: 20px;
            border-radius: 15px;
            margin-top: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }
        
        .form-group {
            margin-bottom: 15px;
            text-align: left;
        }
        
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        
        input {
            width: 100%;
            padding: 10px;
            border-radius: 5px;
            border: none;
            background: rgba(255, 255, 255, 0.9);
        }
        
        #register-btn {
            background: linear-gradient(to right, #00b09b, #96c93d);
            color: white;
            width: 100%;
            margin-top: 10px;
        }
        
        .prize-history {
            background: rgba(0, 0, 0, 0.7);
            padding: 20px;
            border-radius: 15px;
            margin-top: 30px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.5);
        }
        
        .history-list {
            max-height: 200px;
            overflow-y: auto;
            margin-top: 15px;
            text-align: left;
            padding: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
        }
        
        .history-item {
            padding: 10px;
            margin-bottom: 10px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 5px;
            display: flex;
            justify-content: space-between;
        }
        
        .history-prize {
            color: #4cff00;
            font-weight: bold;
        }
        
        footer {
            margin-top: 30px;
            padding: 15px;
            background: rgba(0, 0, 0, 0.7);
            border-radius: 10px;
            font-size: 0.9rem;
        }
        
        .money-bag {
            font-size: 3rem;
            margin: 10px 0;
            animation: bounce 2s infinite;
        }
        
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        @media (max-width: 768px) {
            .game-area {
                flex-direction: column;
            }
            
            h1 {
                font-size: 2.2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>BLESS WINNERS</h1>
            <div class="subtitle">Lucky Draw Slot Machine</div>
            <div class="entry-fee">Entry Fee: 10,000 UGX per number</div>
            <div class="prize-info">Auto Prize: 25,000 - 150,000 UGX for Winner!</div>
            <p>Watch the slot machine spin and discover if you're today's lucky winner!</p>
        </header>
        
        <div class="game-area">
            <div class="slot-machine">
                <h2>WINNER SELECTION SLOT</h2>
                <div class="slot-display">
                    <div class="slot">
                        <div class="slot-inner" id="slot1"></div>
                    </div>
                    <div class="slot">
                        <div class="slot-inner" id="slot2"></div>
                    </div>
                    <div class="slot">
                        <div class="slot-inner" id="slot3"></div>
                    </div>
                </div>
                <div class="controls">
                    <button id="spin-btn">SPIN TO WIN!</button>
                    <button id="reset-btn">RESET</button>
                </div>
            </div>
            
            <div class="participants">
                <h2>REGISTERED PARTICIPANTS</h2>
                <div class="participant-list" id="participant-list">
                    <!-- Participants will be listed here -->
                </div>
            </div>
        </div>
        
        <div class="winner-display" id="winner-display">
            <h2>CONGRATULATIONS!</h2>
            <div class="money-bag">💰</div>
            <div class="winner-message">YOU ARE OUR LUCKY WINNER!</div>
            <div class="winner-name" id="winner-name">Winner Name</div>
            <div class="winner-phone" id="winner-phone">Phone Number</div>
            <div class="winner-prize" id="winner-prize">Prize Amount</div>
            <p>Your prize will be automatically credited to your mobile money account!</p>
        </div>
        
        <div class="prize-history">
            <h2>RECENT WINNERS & PRIZES</h2>
            <div class="history-list" id="history-list">
                <!-- Prize history will be listed here -->
            </div>
        </div>
        
        <div class="registration">
            <h2>REGISTER FOR THE NEXT DRAW</h2>
            <div class="form-group">
                <label for="name">Full Name:</label>
                <input type="text" id="name" placeholder="Enter your full name">
            </div>
            <div class="form-group">
                <label for="phone">Phone Number:</label>
                <input type="text" id="phone" placeholder="Enter your phone number">
            </div>
            <button id="register-btn">REGISTER NOW</button>
        </div>
        
        <footer>
            <p>BLESS WINNERS Lucky Draw | Each entry costs 10,000 UGX | Purchase multiple entries to increase your chances</p>
            <p>© 2023 BLESS WINNERS. All rights reserved.</p>
        </footer>
    </div>

    <script>
        // Initial participants data
        const initialParticipants = [
            { name: "Tuyisege Ronald", phone: "0765342617" },
            { name: "Hategeka Derrick", phone: "0773829193" },
            { name: "Ingabire Caleb", phone: "0756537289" },
            { name: "Habimana Junior", phone: "0766534287" },
            { name: "Kwizera Martin", phone: "0777635566" },
            { name: "Turinayo Ruth", phone: "0753467543" },
            { name: "Tuiringire Kenneth", phone: "0752868278" },
            { name: "Mucunguzi Daniel", phone: "0776534278" },
            { name: "Mbabazi Blessing", phone: "0776994892" }
        ];

        let participants = [...initialParticipants];
        let isSpinning = false;
        let spinInterval;
        let prizeHistory = [];
        
        // Initialize the game
        function initGame() {
            displayParticipants();
            initializeSlots();
            displayPrizeHistory();
            
            // Add event listeners
            document.getElementById('spin-btn').addEventListener('click', startSpin);
            document.getElementById('reset-btn').addEventListener('click', resetGame);
            document.getElementById('register-btn').addEventListener('click', registerParticipant);
        }
        
        // Display all participants
        function displayParticipants() {
            const participantList = document.getElementById('participant-list');
            participantList.innerHTML = '';
            
            participants.forEach(participant => {
                const participantDiv = document.createElement('div');
                participantDiv.className = 'participant';
                participantDiv.innerHTML = `
                    <span>${participant.name}</span>
                    <span>${participant.phone}</span>
                `;
                participantList.appendChild(participantDiv);
            });
        }
        
        // Display prize history
        function displayPrizeHistory() {
            const historyList = document.getElementById('history-list');
            historyList.innerHTML = '';
            
            if (prizeHistory.length === 0) {
                historyList.innerHTML = '<div class="history-item">No winners yet. Be the first!</div>';
                return;
            }
            
            prizeHistory.slice(-5).reverse().forEach(entry => {
                const historyDiv = document.createElement('div');
                historyDiv.className = 'history-item';
                historyDiv.innerHTML = `
                    <span>${entry.name} - ${entry.phone}</span>
                    <span class="history-prize">${formatCurrency(entry.prize)} UGX</span>
                `;
                historyList.appendChild(historyDiv);
            });
        }
        
        // Initialize slot display
        function initializeSlots() {
            for (let i = 1; i <= 3; i++) {
                const slot = document.getElementById(`slot${i}`);
                slot.innerHTML = '';
                
                // Create multiple items for the spinning effect
                for (let j = 0; j < 20; j++) {
                    const item = document.createElement('div');
                    item.className = 'slot-item';
                    // Add random numbers/names for the spinning effect
                    if (j % 2 === 0) {
                        const randomIndex = Math.floor(Math.random() * participants.length);
                        item.textContent = participants[randomIndex].name.substring(0, 3);
                    } else {
                        item.textContent = Math.floor(Math.random() * 10);
                    }
                    slot.appendChild(item);
                }
            }
        }
        
        // Start the slot machine spin
        function startSpin() {
            if (isSpinning || participants.length === 0) return;
            
            isSpinning = true;
            document.getElementById('winner-display').style.display = 'none';
            
            // Reset slots
            initializeSlots();
            
            // Start spinning animation
            let spinCount = 0;
            const maxSpins = 50 + Math.floor(Math.random() * 30);
            
            spinInterval = setInterval(() => {
                spinCount++;
                
                // Update slots with random values
                for (let i = 1; i <= 3; i++) {
                    const slot = document.getElementById(`slot${i}`);
                    const randomIndex = Math.floor(Math.random() * participants.length);
                    
                    if (i === 3 && spinCount > maxSpins - 10) {
                        // Slow down the last slot for dramatic effect
                        if (spinCount % 3 === 0) {
                            updateSlot(slot, participants[randomIndex], i);
                        }
                    } else {
                        updateSlot(slot, participants[randomIndex], i);
                    }
                }
                
                // Stop spinning after maxSpins
                if (spinCount > maxSpins) {
                    clearInterval(spinInterval);
                    isSpinning = false;
                    selectWinner();
                }
            }, 100);
        }
        
        // Update a single slot
        function updateSlot(slot, participant, slotNum) {
            const items = slot.querySelectorAll('.slot-item');
            
            // Update all items with new values
            items.forEach((item, index) => {
                if (slotNum === 3) {
                    // Last slot shows participant names
                    const randomIndex = Math.floor(Math.random() * participants.length);
                    item.textContent = participants[randomIndex].name.substring(0, 3);
                } else {
                    // First two slots show numbers
                    item.textContent = Math.floor(Math.random() * 10);
                }
            });
            
            // Add slight visual effect
            slot.style.transform = `translateY(${Math.sin(Date.now() / 100) * 2}px)`;
        }
        
        // Select and display the winner
        function selectWinner() {
            const winnerIndex = Math.floor(Math.random() * participants.length);
            const winner = participants[winnerIndex];
            
            // Generate random prize between 25,000 and 150,000 UGX
            const prizeAmount = Math.floor(Math.random() * (150000 - 25000 + 1)) + 25000;
            
            // Update the display with winner information
            document.getElementById('winner-name').textContent = winner.name;
            document.getElementById('winner-phone').textContent = winner.phone;
            document.getElementById('winner-prize').textContent = formatCurrency(prizeAmount) + " UGX";
            document.getElementById('winner-display').style.display = 'block';
            
            // Add to prize history
            prizeHistory.push({
                name: winner.name,
                phone: winner.phone,
                prize: prizeAmount,
                date: new Date().toLocaleDateString()
            });
            
            // Update history display
            displayPrizeHistory();
            
            // Create confetti effect
            createConfetti();
            
            // Show prize notification
            showPrizeNotification(prizeAmount);
            
            // Simulate automatic prize transfer
            simulatePrizeTransfer(winner, prizeAmount);
        }
        
        // Format currency with commas
        function formatCurrency(amount) {
            return amount.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ",");
        }
        
        // Show prize notification
        function showPrizeNotification(prize) {
            const notification = document.createElement('div');
            notification.style.position = 'fixed';
            notification.style.top = '20px';
            notification.style.right = '20px';
            notification.style.background = 'linear-gradient(to right, #00b09b, #96c93d)';
            notification.style.color = 'white';
            notification.style.padding = '15px 25px';
            notification.style.borderRadius = '10px';
            notification.style.boxShadow = '0 5px 15px rgba(0,0,0,0.3)';
            notification.style.zIndex = '1000';
            notification.style.fontWeight = 'bold';
            notification.style.fontSize = '1.2rem';
            notification.innerHTML = `🎉 Prize Awarded: ${formatCurrency(prize)} UGX 🎉`;
            
            document.body.appendChild(notification);
            
            // Remove notification after 5 seconds
            setTimeout(() => {
                notification.style.transition = 'opacity 1s';
                notification.style.opacity = '0';
                setTimeout(() => {
                    document.body.removeChild(notification);
                }, 1000);
            }, 5000);
        }
        
        // Simulate automatic prize transfer
        function simulatePrizeTransfer(winner, prize) {
            setTimeout(() => {
                const transferMsg = document.createElement('div');
                transferMsg.style.position = 'fixed';
                transferMsg.style.bottom = '20px';
                transferMsg.style.left = '50%';
                transferMsg.style.transform = 'translateX(-50%)';
                transferMsg.style.background = 'rgba(0, 100, 0, 0.9)';
                transferMsg.style.color = 'white';
                transferMsg.style.padding = '15px 25px';
                transferMsg.style.borderRadius = '10px';
                transferMsg.style.boxShadow = '0 5px 15px rgba(0,0,0,0.3)';
                transferMsg.style.zIndex = '1000';
                transferMsg.style.fontWeight = 'bold';
                transferMsg.style.fontSize = '1.1rem';
                transferMsg.innerHTML = `✅ ${formatCurrency(prize)} UGX sent to ${winner.name} (${winner.phone})`;
                
                document.body.appendChild(transferMsg);
                
                // Remove message after 7 seconds
                setTimeout(() => {
                    transferMsg.style.transition = 'opacity 1s';
                    transferMsg.style.opacity = '0';
                    setTimeout(() => {
                        document.body.removeChild(transferMsg);
                    }, 1000);
                }, 7000);
            }, 2000);
        }
        
        // Create confetti animation
        function createConfetti() {
            const colors = ['#ff0000', '#00ff00', '#0000ff', '#ffff00', '#ff00ff', '#00ffff'];
            
            for (let i = 0; i < 150; i++) {
                const confetti = document.createElement('div');
                confetti.className = 'confetti';
                confetti.style.left = Math.random() * 100 + 'vw';
                confetti.style.backgroundColor = colors[Math.floor(Math.random() * colors.length)];
                confetti.style.width = Math.random() * 10 + 5 + 'px';
                confetti.style.height = Math.random() * 10 + 5 + 'px';
                confetti.style.animationDelay = Math.random() * 5 + 's';
                
                document.body.appendChild(confetti);
                
                // Remove confetti after animation
                setTimeout(() => {
                    confetti.remove();
                }, 5000);
            }
        }
        
        // Reset the game
        function resetGame() {
            if (isSpinning) {
                clearInterval(spinInterval);
                isSpinning = false;
            }
            
            document.getElementById('winner-display').style.display = 'none';
            initializeSlots();
        }
        
        // Register a new participant
        function registerParticipant() {
            const nameInput = document.getElementById('name');
            const phoneInput = document.getElementById('phone');
            
            const name = nameInput.value.trim();
            const phone = phoneInput.value.trim();
            
            if (name && phone) {
                participants.push({ name, phone });
                displayParticipants();
                
                // Clear inputs
                nameInput.value = '';
                phoneInput.value = '';
                
                // Show success message
                alert('Registration successful! Good luck in the draw!');
            } else {
                alert('Please enter both name and phone number.');
            }
        }
        
        // Initialize the game when page loads
        window.onload = initGame;
    </script>
</body>
</html>
