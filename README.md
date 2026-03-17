<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy 19th Suhani</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@600&family=Quicksand:wght@300;500&family=Playfair+Display:italic,wght@0,400;1,700&display=swap" rel="stylesheet">
    <style>
        :root {
            --soft-pink: #fce4ec;
            --aesthetic-rose: #f8bbd0;
            --deep-mauve: #8e24aa;
        }

        body {
            font-family: 'Quicksand', sans-serif;
            background-color: var(--soft-pink);
            overflow: hidden;
            margin: 0;
            color: #4a4a4a;
        }

        .slide {
            height: 100vh;
            width: 100vw;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            position: absolute;
            top: 0;
            left: 0;
            transition: transform 0.8s cubic-bezier(0.645, 0.045, 0.355, 1);
            padding: 1rem;
            text-align: center;
        }

        .cursive {
            font-family: 'Dancing Script', cursive;
        }

        .serif-italic {
            font-family: 'Playfair Display', serif;
            font-style: italic;
        }

        .floating-heart {
            position: absolute;
            color: rgba(248, 187, 208, 0.6);
            animation: float 6s infinite linear;
            z-index: -1;
            pointer-events: none;
        }

        @keyframes float {
            0% { transform: translateY(100vh) rotate(0deg); opacity: 1; }
            100% { transform: translateY(-10vh) rotate(360deg); opacity: 0; }
        }

        .glass {
            background: rgba(255, 255, 255, 0.6);
            backdrop-filter: blur(12px);
            border-radius: 24px;
            border: 1px solid rgba(255, 255, 255, 0.5);
            box-shadow: 0 10px 30px rgba(142, 36, 170, 0.1);
            padding: 2rem;
            max-width: 500px;
            width: 90%;
            z-index: 10;
        }

        .photo-container {
            width: 220px;
            height: 300px;
            margin: 0 auto 1.5rem auto;
            border: 5px solid white;
            border-radius: 20px;
            box-shadow: 0 8px 20px rgba(0,0,0,0.1);
            overflow: hidden;
            background-color: #fdfdfd;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .photo-container img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .rotated-img {
            transform: rotate(-90deg) scale(1.5);
        }

        .btn-next {
            margin-top: 1.5rem;
            padding: 12px 35px;
            background: white;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.3s;
            border: 1px solid var(--aesthetic-rose);
            font-weight: 600;
            color: #883355;
            box-shadow: 0 4px 10px rgba(248, 187, 208, 0.3);
        }

        .btn-next:hover {
            background: var(--aesthetic-rose);
            color: white;
            transform: translateY(-3px);
            box-shadow: 0 6px 15px rgba(248, 187, 208, 0.5);
        }

        .btn-container {
            position: relative;
            height: 80px;
            width: 100%;
            margin-top: 10px;
        }

        #no-btn {
            position: absolute;
            transition: all 0.15s ease-out;
            white-space: nowrap;
        }
    </style>
</head>
<body>

    <div id="hearts-container"></div>

    <!-- Slide 1: Welcome -->
    <section class="slide" id="slide-0">
        <div class="glass">
            <h1 class="text-4xl mb-4 cursive text-pink-500">Welcome, Suhani</h1>
            <p class="text-lg mb-6">Today, the universe celebrates one of its most beautiful souls.</p>
            <div class="photo-container">
                <img src="1.jpeg" alt="Suhani">
            </div>
            <button class="btn-next" onclick="nextSlide(1)">Enter your world ✨</button>
        </div>
    </section>

    <!-- Slide 2: The Big 19 -->
    <section class="slide translate-x-full" id="slide-1">
        <div class="glass">
            <h2 class="text-6xl font-bold mb-2 text-pink-400">19</h2>
            <p class="text-2xl cursive text-pink-400 mb-6">Nineteen years of magic.</p>
            <div class="photo-container">
                <!-- Kept rotation for this specific landscape-oriented photo -->
                <img src="2.jpeg" class="rotated-img" alt="Together">
            </div>
            <p class="serif-italic text-lg">"Nineteen: The age where your soul begins to bloom in full color."</p>
            <button class="btn-next" onclick="nextSlide(2)">What makes you special?</button>
        </div>
    </section>

    <!-- Slide 3: The Curious Mind -->
    <section class="slide translate-x-full" id="slide-2">
        <div class="glass">
            <h2 class="text-3xl mb-4 font-light text-pink-600">Your Curious Soul</h2>
            <p class="mb-4 text-sm">You don't just see people; you see <i>souls</i>. Your curiosity about human nature is your superpower.</p>
            <div class="photo-container">
                <img src="3.jpeg" alt="Nature">
            </div>
            <p class="serif-italic text-sm">"The meeting of two personalities is like the contact of two chemical substances." — Jung</p>
            <button class="btn-next" onclick="nextSlide(3)">A little game?</button>
        </div>
    </section>

    <!-- Slide 4: The Question -->
    <section class="slide translate-x-full" id="slide-3">
        <div class="glass">
            <h2 class="text-xl mb-6">Psychology Check: Is it true that you're my favorite human being?</h2>
            <div class="photo-container">
                <img src="4.jpeg" alt="Fun">
            </div>
            <div class="btn-container" id="interaction-box">
                <button class="bg-pink-400 text-white px-8 py-2 rounded-full hover:bg-pink-500 transition shadow-lg" onclick="nextSlide(4)">YES!</button>
                <button id="no-btn" class="bg-gray-100 px-8 py-2 rounded-full text-gray-400 border border-gray-200" onmouseover="moveButton()">No</button>
            </div>
        </div>
    </section>

    <!-- Slide 5: Deep Thoughts -->
    <section class="slide translate-x-full" id="slide-4">
        <div class="glass">
            <h2 class="text-3xl cursive mb-4 text-pink-600">Soul Whispers</h2>
            <div class="photo-container">
                <img src="5.jpeg" alt="Memories">
            </div>
            <p class="mb-4 text-sm leading-relaxed italic">"Happiness is the only thing that doubles when you share it."</p>
            <p class="text-sm">I love how you think deeply about the stars and the mind.</p>
            <button class="btn-next" onclick="nextSlide(5)">The Final Wish</button>
        </div>
    </section>

    <!-- Slide 6: Final Wish -->
    <section class="slide translate-x-full" id="slide-5">
        <div class="glass">
            <h1 class="text-4xl cursive text-pink-500 mb-4">Happy 19th, Suhani!</h1>
            <p class="mb-6 text-sm">May your year be as deep as your thoughts and as beautiful as your soul. I'm so lucky to have you in my life.</p>
            <div class="photo-container border-pink-300">
                <img src="6.jpeg" alt="Birthday Girl">
            </div>
            <p class="font-bold text-pink-600 text-xl">I love you so much! ❤️</p>
        </div>
    </section>

    <script>
        let currentSlide = 0;

        function nextSlide(n) {
            const current = document.getElementById(`slide-${currentSlide}`);
            const next = document.getElementById(`slide-${n}`);
            current.style.transform = 'translateX(-100vw)';
            next.style.transform = 'translateX(0)';
            currentSlide = n;
        }

        function createHeart() {
            const container = document.getElementById('hearts-container');
            if (!container) return;
            const heart = document.createElement('div');
            heart.classList.add('floating-heart');
            const icons = ['🌸', '❤️', '✨', '☁️'];
            heart.innerHTML = icons[Math.floor(Math.random() * icons.length)];
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = (Math.random() * 3 + 4) + 's';
            heart.style.fontSize = (Math.random() * 15 + 15) + 'px';
            container.appendChild(heart);
            setTimeout(() => heart.remove(), 6000);
        }

        setInterval(createHeart, 500);

        function moveButton() {
            const btn = document.getElementById('no-btn');
            const container = document.getElementById('interaction-box');
            const rect = container.getBoundingClientRect();
            const maxX = rect.width - btn.offsetWidth;
            const maxY = rect.height - btn.offsetHeight;
            btn.style.left = Math.random() * maxX + 'px';
            btn.style.top = Math.random() * maxY + 'px';
        }
    </script>
</body>
</html>
