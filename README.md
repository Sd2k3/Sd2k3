# **Namaste** 🙏, I'm Swarajit Dey!  
**🚀 Full-Stack Developer | AI/ML & GenAI Enthusiast | IoT Explorer | UI/UX Designer**  

[![Email](https://img.shields.io/badge/Email-swarajit19082003%40gmail.com-D14836?style=flat&logo=gmail&logoColor=white)](mailto:swarajit19082003@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Swarajit_Dey-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/swarajit-dey-758b84222/)
[![Twitter](https://img.shields.io/badge/Twitter-Follow_Me-1DA1F2?style=flat&logo=twitter)](https://x.com/Swarajitdey4)   

<!-- Animated typing SVG with more effects -->
<div align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=24&duration=3000&pause=500&color=22F729&width=435&lines=Building+the+future+with+code+%F0%9F%92%BB;Turning+ideas+into+reality+%F0%9F%A7%91%E2%80%8D%F0%9F%92%BB;AI+Enthusiast+%F0%9F%A4%96;Full-Stack+Developer+%F0%9F%9B%A0;Open+to+collaborations+%F0%9F%92%AC" alt="Typing SVG" />
</div>

<!-- Animated wave divider -->
<div align="center">
  <img src="https://github.com/Sd2k3/Sd2k3/blob/output/github-contribution-grid-snake.svg" alt="Snake animation" />
</div>

### **🔥 Tech Stack**  

<!-- Animated tech stack with icons -->
<div align="center">
  <img src="https://skillicons.dev/icons?i=react,nodejs,mongodb,tailwind,py,tensorflow,arduino,raspberrypi,figma,xd,js,ts,nextjs,express,firebase,aws,gcp&theme=dark&perline=8" />
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

<!-- Tetris Game -->
<div align="center">
  <h3>🎮 Play Tetris while exploring my profile!</h3>
  <img src="https://raw.githubusercontent.com/Sd2k3/Sd2k3/main/tetris.gif" alt="Tetris Game" width="300"/>
</div>

<!-- Matrix Rain Animation -->
<div align="center">
  <h3>💻 Matrix Code Rain</h3>
  <img src="https://raw.githubusercontent.com/Sd2k3/Sd2k3/main/matrix.gif" alt="Matrix Rain" width="400"/>
</div>

---

### **📊 GitHub Stats**  
<!-- Animated GitHub Stats -->
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Sd2k3&show_icons=true&theme=radical&hide_border=true&include_all_commits=true&count_private=true&line_height=24" alt="Swarajit's GitHub Stats" />  
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sd2k3&layout=compact&theme=radical&hide_border=true&langs_count=8" alt="Top Languages" />
</div>

<!-- GitHub Streak Stats -->
<div align="center">
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=Sd2k3&theme=radical&hide_border=true" alt="GitHub Streak" />
</div>

<!-- 3D Contribution Graph -->
<div align="center">
  <h3>📈 3D Contribution Graph</h3>
  <img src="https://github-profile-3d.herokuapp.com/profile/Sd2k3?theme=dracula&color=7F00FF&bg_color=0D1117" alt="3D Contribution Graph" width="800"/>
</div>

---

### **🚀 Featured Project**  
#### **[NEURONEST: AI-Powered Dementia Care Platform](https://pinky-umber.vercel.app/)**  
🏆 **Code-e-Manipal Hackathon Winner** (Top team among 1500+ participants)  
✨ **Proven Impact:** 89% improvement in memory recall | 72% reduction in safety incidents  
🛠 **Tech Stack:** React, Node.js, TensorFlow, and innovative AI algorithms  

<!-- Project GIF -->
<div align="center">
  <img src="https://raw.githubusercontent.com/Sd2k3/Sd2k3/main/project-demo.gif" alt="Project Demo" width="600"/>
</div>

---

### **🎲 Interactive Games Section**

#### **Tic-Tac-Toe Challenge**
```python
# Mini Tic-Tac-Toe Game in Python
def print_board(board):
    for row in board:
        print(" | ".join(row))
        print("-" * 9)

def check_winner(board):
    # Check rows, columns, and diagonals
    for i in range(3):
        if board[i][0] == board[i][1] == board[i][2] != " ":
            return board[i][0]
        if board[0][i] == board[1][i] == board[2][i] != " ":
            return board[0][i]
    if board[0][0] == board[1][1] == board[2][2] != " ":
        return board[0][0]
    if board[0][2] == board[1][1] == board[2][0] != " ":
        return board[0][2]
    return None

# Initialize board
board = [[" " for _ in range(3)] for _ in range(3)]
current_player = "X"
