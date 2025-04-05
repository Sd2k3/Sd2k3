# **Namaste** 🙏, I'm Swarajit Dey!  
**🚀 Full-Stack Developer | AI/ML & GenAI Enthusiast | IoT Explorer | UI/UX Designer**  

[![Email](https://img.shields.io/badge/Email-swarajit19082003%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:swarajit19082003@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Swarajit_Dey-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/swarajit-dey-758b84222/)
[![Twitter](https://img.shields.io/badge/Twitter-Follow_Me-1DA1F2?style=flat&logo=twitter)]([https://twitter.com/yourhandle](https://x.com/Swarajitdey4))   

<!-- Animated divider -->
<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1000&color=22F729&width=435&lines=Building+the+future+with+code+%F0%9F%92%BB;Turning+ideas+into+reality+%F0%9F%A7%91%E2%80%8D%F0%9F%92%BB;AI+Enthusiast+%F0%9F%A4%96;Full-Stack+Developer+%F0%9F%9B%A0" alt="Typing SVG" />
</div>

### **🔥 Tech Stack**  

<!-- Animated tech stack with icons -->
<div align="center">
  <img src="https://skillicons.dev/icons?i=react,nodejs,mongodb,tailwind,py,tensorflow,arduino,raspberrypi,figma,xd&theme=dark&perline=5" />
</div>

#### **🌐 Web Development**  
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)  

#### **🤖 AI/ML & Generative AI**  
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)  

#### **⚡ IoT & Others**  
![Arduino](https://img.shields.io/badge/Arduino-00979D?style=for-the-badge&logo=arduino&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry_Pi-A22846?style=for-the-badge&logo=raspberry-pi&logoColor=white)  

#### **🎨 UI/UX Design**  
![Figma](https://img.shields.io/badge/Figma-F24E1E?style=for-the-badge&logo=figma&logoColor=white)
![Adobe XD](https://img.shields.io/badge/Adobe_XD-FF61F6?style=for-the-badge&logo=adobe-xd&logoColor=white)  

---

### **📊 GitHub Stats**  
![Swarajit's GitHub Stats](https://github-readme-stats.vercel.app/api?username=Sd2k3&show_icons=true&theme=radical&hide_border=true&include_all_commits=true)  

![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Sd2k3&layout=compact&theme=radical&hide_border=true)  

---

### **🚀 Featured Project**  
#### **[NEURONEST: AI-Powered Dementia Care Platform](https://pinky-umber.vercel.app/)**  
🏆 **Code-e-Manipal Hackathon Winner** (Top team among 1500+ participants)  
✨ **Proven Impact:** 89% improvement in memory recall | 72% reduction in safety incidents  
🛠 **Tech Stack:** React, Node.js, TensorFlow, and innovative AI algorithms  


---

### **📫 Let’s Collaborate!**  
- 💡 **Passionate About:** AI-driven healthcare solutions, IoT innovations, and accessible design  
- 📧 **Email:** [swarajit19082003@gmail.com](mailto:swarajit19082003@gmail.com)  
- 🔗 **LinkedIn:** [Let's connect!](https://www.linkedin.com/in/swarajit-dey-758b84222/)  

---

![Visitor Count](https://komarev.com/ghpvc/?username=Sd2k3&label=Profile%20Views&color=blue&style=flat)  

**"Code is poetry. Build something amazing today!"** ✨ 

---

Here's a simple Snake game you can play:

<div>
  <svg id="snake-game" width="200" height="200"></svg>
  <div>
    <button id="start-btn" onclick="startGame()">Start Game</button>
    <div id="score">Score: 0</div>
  </div>
</div>

<script>
  const svg = document.getElementById('snake-game');
  const scoreDisplay = document.getElementById('score');
  const startBtn = document.getElementById('start-btn');
  
  const gridSize = 20;
  const tileSize = 10;
  let snake = [{x: 10, y: 10}];
  let food = {x: 5, y: 5};
  let direction = 'right';
  let gameInterval;
  let score = 0;
  
  function draw() {
    // Clear SVG
    svg.innerHTML = '';
    
    // Draw snake
    snake.forEach(segment => {
      const rect = document.createElementNS('http://www.w3.org/2000/svg', 'rect');
      rect.setAttribute('x', segment.x * tileSize);
      rect.setAttribute('y', segment.y * tileSize);
      rect.setAttribute('width', tileSize);
      rect.setAttribute('height', tileSize);
      rect.setAttribute('fill', '#00ff00');
      svg.appendChild(rect);
    });
    
    // Draw food
    const foodRect = document.createElementNS('http://www.w3.org/2000/svg', 'rect');
    foodRect.setAttribute('x', food.x * tileSize);
    foodRect.setAttribute('y', food.y * tileSize);
    foodRect.setAttribute('width', tileSize);
    foodRect.setAttribute('height', tileSize);
    foodRect.setAttribute('fill', '#ff0000');
    svg.appendChild(foodRect);
  }
  
  function update() {
    const head = {...snake[0]};
    
    // Move head
    switch(direction) {
      case 'up': head.y--; break;
      case 'down': head.y++; break;
      case 'left': head.x--; break;
      case 'right': head.x++; break;
    }
    
    // Check wall collision
    if (head.x < 0 || head.x >= gridSize || head.y < 0 || head.y >= gridSize) {
      gameOver();
      return;
    }
    
    // Check self collision
    if (snake.some(segment => segment.x === head.x && segment.y === head.y)) {
      gameOver();
      return;
    }
    
    // Add new head
    snake.unshift(head);
    
    // Check food collision
    if (head.x === food.x && head.y === food.y) {
      score++;
      scoreDisplay.textContent = `Score: ${score}`;
      placeFood();
    } else {
      // Remove tail if no food eaten
      snake.pop();
    }
    
    draw();
  }
  
  function placeFood() {
    food = {
      x: Math.floor(Math.random() * gridSize),
      y: Math.floor(Math.random() * gridSize)
    };
    
    // Make sure food doesn't spawn on snake
    while (snake.some(segment => segment.x === food.x && segment.y === food.y)) {
      food = {
        x: Math.floor(Math.random() * gridSize),
        y: Math.floor(Math.random() * gridSize)
      };
    }
  }
  
  function gameOver() {
    clearInterval(gameInterval);
    startBtn.style.display = 'block';
    alert(`Game Over! Your score: ${score}`);
  }
  
  function startGame() {
    snake = [{x: 10, y: 10}];
    direction = 'right';
    score = 0;
    scoreDisplay.textContent = `Score: ${score}`;
    placeFood();
    startBtn.style.display = 'none';
    draw();
    
    gameInterval = setInterval(update, 100);
  }
  
  // Keyboard controls
  document.addEventListener('keydown', e => {
    switch(e.key) {
      case 'ArrowUp': if (direction !== 'down') direction = 'up'; break;
      case 'ArrowDown': if (direction !== 'up') direction = 'down'; break;
      case 'ArrowLeft': if (direction !== 'right') direction = 'left'; break;
      case 'ArrowRight': if (direction !== 'left') direction = 'right'; break;
    }
  });
</script>

