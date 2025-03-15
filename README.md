# ✊✋✌️ Rock Paper Scissors Game

Welcome to the **Rock Paper Scissors Game** repository!  
This is a simple and interactive Rock Paper Scissors game built using **HTML**, **CSS**, and **JavaScript**.  
The game allows you to play against the computer, keeps track of wins, losses, and ties, and displays the game history in a table format.

---

## 🚀 **Features**
✅ Play Rock Paper Scissors against the computer  
✅ Random computer moves using `Math.random()`  
✅ Score tracking (Wins, Losses, Ties, Games Played)  
✅ Animated dice roll effect for computer's move  
✅ Reset button to clear game stats and history  
✅ Clean and responsive UI  

---

## 🛠️ **Technologies Used**
- **HTML** – Structuring the web page  
- **CSS** – Styling the game elements  
- **JavaScript** – Handling game logic and interactivity  

---

## 📥 **Installation**
1. **Clone the repository:**
```bash
git clone https://github.com/akashprajapati-cse/Rock-Paper-Scissors.git
```

2. **Navigate to the project folder:**
```bash
cd Rock-Paper-Scissors
```

3. **Open `index.html` in your browser:**  
- Use a local server (e.g., Live Server in VS Code)  
- Or directly open the file in your browser  

---

## 🏃 **Usage**
### ✅ **How to Play:**
1. Click on **Rock**, **Paper**, or **Scissors** to make your move.  
2. The computer will randomly select a move.  
3. The winner will be displayed based on the rules:  
   - Rock beats Scissors  
   - Scissors beats Paper  
   - Paper beats Rock  
   - If both moves are the same → It's a Tie!  
4. The result and game history will be updated automatically.  

### ✅ **Score Tracking:**
- Win, Loss, and Tie counts are displayed in a table.  
- Total games played are also tracked.  

### ✅ **Reset Game:**
- Click the **Reset** button to reset all stats and history.  

---

## 📄 **Game Rules**
| User Move | Computer Move | Result |
|-----------|---------------|--------|
| Rock | Scissors | ✅ Win |
| Scissors | Paper | ✅ Win |
| Paper | Rock | ✅ Win |
| Same | Same | 🤝 Tie |
| Others | Others | ❌ Loss |

---

## 🏆 **Code Highlights**
### ✅ **Generate Computer Move**
```javascript
generateComputerMove = () => {
  const randNum = Math.random();
  if (randNum < 1 / 3) {
    computerMove = 'rock';
  } else if (randNum < 2 / 3) {
    computerMove = 'paper';
  } else {
    computerMove = 'scissors';
  }
};
```

### ✅ **Game Logic**
```javascript
if (usermove === computerMove) {
  tie_count++;
  result.innerHTML = `TIE 🙂`;
} else if (
  (usermove === 'rock' && computerMove === 'scissors') ||
  (usermove === 'paper' && computerMove === 'rock') ||
  (usermove === 'scissors' && computerMove === 'paper')
) {
  win_count++;
  result.innerHTML = `WINNER 🥳`;
} else {
  loses_count++;
  result.innerHTML = `LOSER 😞`;
}
```

### ✅ **Rolling Animation**
```javascript
let rollingInterval;
function rollDice() {
  clearInterval(rollingInterval);
  rollingInterval = setInterval(generateRandomImage, 200);
  setTimeout(stopRolling, 1500);
}
```

---

## 🌟 **Best Practices**
- Keep your browser console open to track any errors.  
- For best experience, run using a local server.  
- Make sure the image files (`rock.png`, `paper.png`, `scissors.png`, `reset.jpg`) are in the project folder.  

---

## 👨‍💻 **Contributors**
- **Akash Prajapati** – [GitHub](https://github.com/akashprajapati-cse)  

---

## 📄 **License**
This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

**⭐ If you like this project, give it a star on GitHub!**  
```

---

### 🔥 **Tips:**
- Make sure that the image files (`rock.png`, `paper.png`, `scissors.png`, `reset.jpg`) are correctly linked and available in the project folder.  
- Once you add this `README.md`, GitHub will automatically display it on the main repository page.  

Let me know if you need more help! 😎
