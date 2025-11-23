









<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Akbar! 🎂</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            font-family: 'Georgia', serif;
            overflow-x: hidden;
            position: relative;
            color: #fff;
        }

        .container {
            text-align: center;
            z-index: 10;
            padding: 20px;
            max-width: 800px;
            width: 90%;
        }

        h1 {
            font-size: clamp(2.2rem, 6vw, 3.5rem);
            color: #4cc9f0;
            text-shadow: 0 0 20px rgba(76, 201, 240, 0.5);
            margin-bottom: 20px;
            animation: glow 2s ease-in-out infinite;
        }

        @keyframes glow {
            0%, 100% { text-shadow: 0 0 20px rgba(76, 201, 240, 0.5); }
            50% { text-shadow: 0 0 40px rgba(76, 201, 240, 0.8), 0 0 60px rgba(76, 201, 240, 0.6); }
        }

        .date {
            font-size: clamp(1.2rem, 4vw, 1.5rem);
            color: #a5b4fc;
            margin-bottom: 30px;
            letter-spacing: 3px;
        }

        .cake-container {
            margin: 40px 0;
            position: relative;
            display: inline-block;
        }

        .cake {
            font-size: clamp(80px, 20vw, 150px);
            animation: bounce 2s ease-in-out infinite;
            cursor: pointer;
            filter: drop-shadow(0 10px 20px rgba(76, 201, 240, 0.3));
            transition: transform 0.3s ease;
        }

        .cake:hover {
            transform: scale(1.1);
        }

        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }

        .candle {
            position: absolute;
            top: -30px;
            left: 50%;
            transform: translateX(-50%);
            font-size: clamp(25px, 8vw, 40px);
            animation: flicker 0.5s ease-in-out infinite;
            transition: opacity 0.5s;
        }

        @keyframes flicker {
            0%, 100% { opacity: 1; transform: scale(1); }
            25% { opacity: 0.8; transform: scale(1.05); }
            50% { opacity: 0.9; transform: scale(0.95); }
            75% { opacity: 0.7; transform: scale(1.1); }
        }

        .wish-box {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(76, 201, 240, 0.2);
            border-radius: 20px;
            padding: 30px;
            margin: 30px auto;
            max-width: 600px;
            box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
            opacity: 0;
            transform: translateY(20px);
            transition: all 0.8s ease;
        }

        .wish-box.show {
            opacity: 1;
            transform: translateY(0);
        }

        .wish-text {
            color: #e0e0e0;
            font-size: clamp(1rem, 3vw, 1.1rem);
            line-height: 1.8;
            margin: 15px 0;
            font-style: italic;
        }

        .prayer {
            color: #4cc9f0;
            font-weight: bold;
            margin: 10px 0;
            font-size: clamp(1rem, 3vw, 1.2rem);
        }

        .buttons-container {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 20px;
        }

        button {
            background: linear-gradient(135deg, #4361ee 0%, #4cc9f0 100%);
            border: none;
            padding: 15px 30px;
            font-size: clamp(1rem, 3vw, 1.2rem);
            border-radius: 50px;
            cursor: pointer;
            color: #fff;
            font-weight: bold;
            box-shadow: 0 5px 20px rgba(76, 201, 240, 0.4);
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            min-width: 200px;
        }

        button:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 30px rgba(76, 201, 240, 0.6);
        }

        button.secondary {
            background: rgba(76, 201, 240, 0.1);
            color: #4cc9f0;
            border: 1px solid rgba(76, 201, 240, 0.3);
        }

        .particle {
            position: absolute;
            width: 10px;
            height: 10px;
            background: #4cc9f0;
            border-radius: 50%;
            pointer-events: none;
            animation: float 3s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0) translateX(0); opacity: 0; }
            50% { opacity: 1; }
        }

        .heart {
            position: absolute;
            font-size: 30px;
            animation: heartFloat 4s ease-in-out infinite;
            opacity: 0;
            z-index: 5;
        }

        @keyframes heartFloat {
            0% { transform: translateY(0) scale(0); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(-500px) scale(1.5); opacity: 0; }
        }

        .firework {
            position: absolute;
            width: 5px;
            height: 5px;
            border-radius: 50%;
            animation: explode 1s ease-out forwards;
            z-index: 5;
        }

        @keyframes explode {
            0% { transform: translate(0, 0); opacity: 1; }
            100% { transform: translate(var(--x), var(--y)); opacity: 0; }
        }

        .hidden {
            display: none;
        }

        .message {
            margin-top: 20px;
            font-size: clamp(1rem, 3vw, 1.1rem);
            color: #a5b4fc;
            animation: fadeIn 2s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .floating-text {
            position: absolute;
            font-size: clamp(0.9rem, 2.5vw, 1.2rem);
            color: #4cc9f0;
            animation: floatAround 15s linear infinite;
            opacity: 0.7;
        }

        @keyframes floatAround {
            0% { transform: translate(0, 0) rotate(0deg); }
            25% { transform: translate(100px, 50px) rotate(90deg); }
            50% { transform: translate(50px, 100px) rotate(180deg); }
            75% { transform: translate(-50px, 50px) rotate(270deg); }
            100% { transform: translate(0, 0) rotate(360deg); }
        }

        /* Responsive adjustments */
        @media (max-width: 768px) {
            .container {
                padding: 15px;
            }
            
            .wish-box {
                padding: 20px;
            }
            
            .buttons-container {
                flex-direction: column;
                align-items: center;
            }
            
            button {
                width: 100%;
                max-width: 300px;
                padding: 12px 25px;
            }
        }

        @media (max-width: 480px) {
            .cake {
                font-size: 100px;
            }
            
            .candle {
                font-size: 30px;
                top: -20px;
            }
            
            .wish-box {
                padding: 15px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>✨ Happy Birthday Akbar! ✨</h1>
        <div class="date">November 25th</div>
        
        <div class="cake-container" id="cakeContainer">
            <div class="candle" id="candle">🕯️</div>
            <div class="cake" id="cake">🎂</div>
        </div>

        <div class="buttons-container">
            <button onclick="blowCandle()">
                <span>🌬️</span> Blow the Candle
            </button>
            <button onclick="playMusic()" class="secondary" id="musicBtn">
                <span>🎵</span> Play Music
            </button>
        </div>
        
        <div class="wish-box" id="wishBox">
            <p class="prayer">🙏 My Prayers & Wishes for You 🙏</p>
            <p class="wish-text">
                May this year bring you endless joy, boundless success, and countless beautiful moments to cherish.
            </p>
            <p class="wish-text">
                May you be blessed with good health, inner peace, and the strength to achieve all your dreams.
            </p>
            <p class="wish-text">
                May every step you take be guided by wisdom, and may happiness follow you wherever you go.
            </p>
            <p class="wish-text">
                May our love grow stronger with each passing day, and may we create many more wonderful memories together.
            </p>
            <p class="wish-text">
                You are my greatest blessing, and I'm so grateful to celebrate another year of your amazing life! 💙
            </p>
            <p class="prayer">I love you more than words can say! 🎉✨</p>
            
            <div class="buttons-container">
                <button onclick="celebrate()" id="celebrateBtn">
                    <span>🎊</span> Celebrate!
                </button>
                <button onclick="shareLove()" class="secondary">
                    <span>💌</span> Send Love
                </button>
            </div>
        </div>

        <div class="message hidden" id="birthdayMessage">
            Wishing you the happiest of birthdays, my love! May this year be your best one yet. 💙
        </div>
    </div>

    <script>
        let candleBlown = false;
        let musicPlaying = false;
        let audioContext;
        let oscillator;
        let gainNode;

        function createParticles() {
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const particle = document.createElement('div');
                    particle.className = 'particle';
                    particle.style.left = Math.random() * 100 + '%';
                    particle.style.top = Math.random() * 100 + '%';
                    particle.style.animationDelay = Math.random() * 2 + 's';
                    particle.style.background = `hsl(${Math.random() * 60 + 180}, 100%, 60%)`;
                    document.body.appendChild(particle);
                    
                    setTimeout(() => particle.remove(), 3000);
                }, i * 50);
            }
        }

        function createFloatingText() {
            const texts = ["Happy Birthday!", "I Love You!", "Best Wishes!", "You're Amazing!"];
            for (let i = 0; i < 8; i++) {
                const text = document.createElement('div');
                text.className = 'floating-text';
                text.textContent = texts[Math.floor(Math.random() * texts.length)];
                text.style.left = Math.random() * 100 + '%';
                text.style.top = Math.random() * 100 + '%';
                text.style.animationDelay = Math.random() * 5 + 's';
                text.style.animationDuration = (15 + Math.random() * 10) + 's';
                document.body.appendChild(text);
            }
        }

        function blowCandle() {
            if (candleBlown) return;
            candleBlown = true;
            
            const candle = document.getElementById('candle');
            const cake = document.getElementById('cake');
            const wishBox = document.getElementById('wishBox');
            const message = document.getElementById('birthdayMessage');
            
            // Create blowing effect
            for (let i = 0; i < 10; i++) {
                setTimeout(() => {
                    const particle = document.createElement('div');
                    particle.className = 'particle';
                    particle.style.left = '50%';
                    particle.style.top = '40%';
                    particle.style.background = '#ffffff';
                    particle.style.width = '5px';
                    particle.style.height = '5px';
                    particle.style.animation = `float 1s ease-out forwards`;
                    document.body.appendChild(particle);
                    
                    setTimeout(() => particle.remove(), 1000);
                }, i * 100);
            }
            
            candle.style.animation = 'none';
            candle.style.opacity = '0';
            
            setTimeout(() => {
                cake.style.animation = 'none';
                cake.style.transform = 'scale(1.2)';
            }, 500);
            
            setTimeout(() => {
                wishBox.classList.add('show');
                message.classList.remove('hidden');
                createParticles();
                playBirthdayTune();
            }, 1000);
        }

        function playBirthdayTune() {
            // Simple birthday tune using Web Audio API
            try {
                audioContext = new (window.AudioContext || window.webkitAudioContext)();
                gainNode = audioContext.createGain();
                gainNode.connect(audioContext.destination);
                gainNode.gain.value = 0.3;
                
                // Play simple birthday melody
                const notes = [
                    {freq: 523, duration: 0.3}, // C
                    {freq: 523, duration: 0.3}, // C
                    {freq: 587, duration: 0.6}, // D
                    {freq: 523, duration: 0.6}, // C
                    {freq: 698, duration: 0.6}, // F
                    {freq: 659, duration: 1.2}, // E
                    
                    {freq: 523, duration: 0.3}, // C
                    {freq: 523, duration: 0.3}, // C
                    {freq: 587, duration: 0.6}, // D
                    {freq: 523, duration: 0.6}, // C
                    {freq: 784, duration: 0.6}, // G
                    {freq: 698, duration: 1.2}, // F
                ];
                
                let startTime = audioContext.currentTime;
                
                notes.forEach((note, index) => {
                    playNote(note.freq, startTime + index * 0.5, note.duration);
                });
            } catch (e) {
                console.log("Web Audio API not supported");
            }
        }
        
        function playNote(frequency, startTime, duration) {
            const oscillator = audioContext.createOscillator();
            oscillator.connect(gainNode);
            oscillator.frequency.value = frequency;
            oscillator.type = 'sine';
            
            oscillator.start(startTime);
            oscillator.stop(startTime + duration);
        }

        function playMusic() {
            const musicBtn = document.getElementById('musicBtn');
            
            if (!musicPlaying) {
                playBirthdayTune();
                musicBtn.innerHTML = '<span>🔇</span> Stop Music';
                musicPlaying = true;
            } else {
                if (gainNode) {
                    gainNode.gain.value = 0;
                }
                musicBtn.innerHTML = '<span>🎵</span> Play Music';
                musicPlaying = false;
            }
        }

        function celebrate() {
            createFireworks();
            createHearts();
            
            // Add confetti effect
            for (let i = 0; i < 100; i++) {
                setTimeout(() => {
                    const confetti = document.createElement('div');
                    confetti.className = 'particle';
                    confetti.style.left = Math.random() * 100 + '%';
                    confetti.style.top = '-10px';
                    confetti.style.background = `hsl(${Math.random() * 60 + 180}, 100%, 60%)`;
                    confetti.style.width = '10px';
                    confetti.style.height = '10px';
                    confetti.style.borderRadius = '0';
                    confetti.style.transform = `rotate(${Math.random() * 360}deg)`;
                    confetti.style.animation = `float ${1 + Math.random() * 2}s ease-in forwards`;
                    document.body.appendChild(confetti);
                    
                    setTimeout(() => confetti.remove(), 3000);
                }, i * 30);
            }
        }

        function createFireworks() {
            for (let i = 0; i < 50; i++) {
                setTimeout(() => {
                    const firework = document.createElement('div');
                    firework.className = 'firework';
                    firework.style.left = Math.random() * window.innerWidth + 'px';
                    firework.style.top = Math.random() * window.innerHeight + 'px';
                    firework.style.background = `hsl(${Math.random() * 60 + 180}, 100%, 60%)`;
                    
                    const angle = Math.random() * Math.PI * 2;
                    const distance = Math.random() * 200 + 100;
                    firework.style.setProperty('--x', Math.cos(angle) * distance + 'px');
                    firework.style.setProperty('--y', Math.sin(angle) * distance + 'px');
                    
                    document.body.appendChild(firework);
                    setTimeout(() => firework.remove(), 1000);
                }, i * 100);
            }
        }

        function createHearts() {
            const hearts = ['❤️', '💙', '💚', '💜', '🧡', '💖', '💝'];
            for (let i = 0; i < 30; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.textContent = hearts[Math.floor(Math.random() * hearts.length)];
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.animationDelay = Math.random() * 2 + 's';
                    document.body.appendChild(heart);
                    
                    setTimeout(() => heart.remove(), 4000);
                }, i * 150);
            }
        }

        function shareLove() {
            const message = document.getElementById('birthdayMessage');
            message.textContent = "Sending all my love to you on your special day! 💌";
            message.classList.remove('hidden');
            
            // Create floating hearts
            for (let i = 0; i < 20; i++) {
                setTimeout(() => {
                    const heart = document.createElement('div');
                    heart.className = 'heart';
                    heart.textContent = '💙';
                    heart.style.left = Math.random() * 100 + '%';
                    heart.style.animationDelay = Math.random() * 1 + 's';
                    document.body.appendChild(heart);
                    
                    setTimeout(() => heart.remove(), 4000);
                }, i * 100);
            }
        }

        // Initialize
        createParticles();
        createFloatingText();
        setInterval(createParticles, 5000);
        
        // Add click effect on cake
        document.getElementById('cake').addEventListener('click', blowCandle);
    </script>
</body>
</html>
