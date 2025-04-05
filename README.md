# **Namaste** 🙏, I'm Swarajit Dey!  
**🚀 Full-Stack Developer | AI/ML & GenAI Enthusiast | IoT Explorer | UI/UX Designer**  

[![Email](https://img.shields.io/badge/Email-swarajit19082003%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:swarajit19082003@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Swarajit_Dey-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/swarajit-dey-758b84222/)
[![Twitter](https://img.shields.io/badge/Twitter-Follow_Me-1DA1F2?style=flat&logo=twitter)](https://x.com/Swarajitdey4)   

<!-- Animated divider -->
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=22F729&width=435&lines=Building+the+future+with+code+%F0%9F%92%BB;Turning+ideas+into+reality+%F0%9F%A7%91%E2%80%8D%F0%9F%92%BB;AI+Enthusiast+%F0%9F%A4%96;Full-Stack+Developer+%F0%9F%9B%A0" alt="Typing SVG" />
</div>

---

### **🔥 Tech Stack**  
<!-- Animated tech stack with icons -->
<div align="center">
  <img src="https://skillicons.dev/icons?i=react,nodejs,mongodb,tailwind,py,tensorflow,arduino,raspberrypi,figma,xd&theme=dark&perline=5" />
</div>

---

### **🎮 Interactive Memory Game**
Try this simple memory game I built with JavaScript! (Click "Run" below)

```html
<!-- HTML/CSS/JS Memory Game - Paste this in a .html file to play -->
<!DOCTYPE html>
<html>
<head>
  <style>
    #game-board {
      display: grid;
      grid-template-columns: repeat(4, 80px);
      gap: 10px;
      margin: 20px auto;
      max-width: 360px;
    }
    .card {
      width: 80px;
      height: 80px;
      background: #6e48aa;
      border-radius: 10px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 30px;
      cursor: pointer;
      transition: all 0.3s ease;
      transform-style: preserve-3d;
    }
    .card.flipped {
      background: #fff;
      transform: rotateY(180deg);
    }
    .card.matched {
      background: #9dff00;
      cursor: default;
    }
    @keyframes celebrate {
      0% { transform: scale(1); }
      50% { transform: scale(1.2); }
      100% { transform: scale(1); }
    }
    .celebrate {
      animation: celebrate 0.5s ease;
    }
  </style>
</head>
<body>
  <h2>🧠 Memory Booster Game</h2>
  <div id="game-board"></div>
  <p id="message">Match all pairs to win!</p>

  <script>
    const symbols = ["🚀", "🎮", "🧠", "✨", "🤖", "🎨", "⚡", "🔮"];
    let cards = [...symbols, ...symbols];
    let flippedCards = [];
    let matchedCards = [];
    
    function shuffle(array) {
      return array.sort(() => Math.random() - 0.5);
    }
    
    function createBoard() {
      const gameBoard = document.getElementById('game-board');
      gameBoard.innerHTML = '';
      shuffledCards = shuffle(cards);
      
      shuffledCards.forEach((symbol, index) => {
        const card = document.createElement('div');
        card.classList.add('card');
        card.dataset.index = index;
        card.dataset.symbol = symbol;
        card.addEventListener('click', flipCard);
        gameBoard.appendChild(card);
      });
    }
    
    function flipCard() {
      if (flippedCards.length < 2 && !this.classList.contains('flipped')) {
        this.classList.add('flipped');
        this.textContent = this.dataset.symbol;
        flippedCards.push(this);
        
        if (flippedCards.length === 2) {
          setTimeout(checkForMatch, 500);
        }
      }
    }
    
    function checkForMatch() {
      const [card1, card2] = flippedCards;
      
      if (card1.dataset.symbol === card2.dataset.symbol) {
        card1.classList.add('matched', 'celebrate');
        card2.classList.add('matched', 'celebrate');
        matchedCards.push(card1, card2);
        
        if (matchedCards.length === cards.length) {
          document.getElementById('message').textContent = "🎉 You won! Great memory!";
        }
      } else {
        card1.classList.remove('flipped');
        card2.classList.remove('flipped');
        card1.textContent = '';
        card2.textContent = '';
      }
      
      flippedCards = [];
    }
    
    createBoard();
  </script>
</body>
</html>
