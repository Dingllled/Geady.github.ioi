<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Arcade Hub | Unblocked Games</title>
    <style>
        /* Base Styling */
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #0d0e12;
            color: #ffffff;
            padding: 20px;
        }

        /* Header & Navigation */
        header {
            text-align: center;
            margin-bottom: 40px;
            padding: 20px 0;
        }
        h1 {
            font-size: 2.5rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            background: linear-gradient(45deg, #00ffcc, #0077ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }
        header p {
            color: #8a8f98;
            font-size: 1.1rem;
        }

        /* Search Bar Section */
        .search-container {
            max-width: 500px;
            margin: 0 auto 40px auto;
        }
        .search-box {
            width: 100%;
            padding: 14px 20px;
            background-color: #1a1c23;
            border: 2px solid #2d313f;
            border-radius: 30px;
            color: #fff;
            font-size: 1rem;
            outline: none;
            transition: all 0.3s ease;
        }
        .search-box:focus {
            border-color: #00ffcc;
            box-shadow: 0 0 15px rgba(0, 255, 204, 0.2);
        }

        /* Games Layout Grid */
        .games-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
            gap: 25px;
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Game Card Styling */
        .game-card {
            background-color: #16181f;
            border: 1px solid #252836;
            border-radius: 16px;
            overflow: hidden;
            transition: transform 0.3s cubic-bezier(0.25, 0.8, 0.25, 1), box-shadow 0.3s ease;
            display: flex;
            flex-direction: column;
            text-decoration: none;
        }
        .game-card:hover {
            transform: translateY(-8px);
            border-color: #00ffcc;
            box-shadow: 0 10px 20px rgba(0, 255, 204, 0.15);
        }

        /* Thumbnail Placeholder (Can change to <img> tags later) */
        .thumbnail {
            width: 100%;
            height: 140px;
            background: linear-gradient(135deg, #1f2330, #2d3245);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3rem;
        }

        /* Game Text Details */
        .game-info {
            padding: 15px;
            text-align: center;
            background-color: #16181f;
        }
        .game-title {
            font-size: 1.1rem;
            font-weight: 600;
            color: #fff;
            margin-bottom: 5px;
            transition: color 0.2s ease;
        }
        .game-card:hover .game-title {
            color: #00ffcc;
        }
        .game-category {
            font-size: 0.8rem;
            color: #6c7281;
            text-transform: uppercase;
            letter-spacing: 1px;
        }
    </style>
</head>
<body>

    <header>
        <h1>Arcade Hub</h1>
        <p>Your portal for unblocked static browser games</p>
    </header>

    <div class="search-container">
        <input type="text" id="search" class="search-box" placeholder="Search your favourite games..." onkeyup="filterGames()">
    </div>

    <!-- Games Grid Component -->
    <div class="games-grid" id="gamesGrid">
        
        <!-- Game Item 1 -->
        <a href="games/retro-runner/index.html" class="game-card">
            <div class="thumbnail">🏃‍♂️</div>
            <div class="game-info">
                <div class="game-title">Retro Runner</div>
                <div class="game-category">Platformer</div>
            </div>
        </a>

        <!-- Game Item 2 -->
        <a href="games/block-puzzle/index.html" class="game-card">
            <div class="thumbnail">🧱</div>
            <div class="game-info">
                <div class="game-title">Block Puzzle</div>
                <div class="game-category">Puzzle</div>
            </div>
        </a>

        <!-- Game Item 3 -->
        <a href="games/space-blaster/index.html" class="game-card">
            <div class="thumbnail">🚀</div>
            <div class="game-info">
                <div class="game-title">Space Blaster</div>
                <div class="game-category">Arcade</div>
            </div>
        </a>

    </div>

    <!-- Filter Script Logic -->
    <script>
        function filterGames() {
            const searchInput = document.getElementById('search').value.toLowerCase();
            const cards = document.getElementsByClassName('game-card');

            for (let i = 0; i < cards.length; i++) {
                const title = cards[i].querySelector('.game-title').innerText.toLowerCase();
                if (title.includes(searchInput)) {
                    cards[i].style.display = "flex";
                } else {
                    cards[i].style.display = "none";
                }
            }
        }
    </script>
</body>
</html>
