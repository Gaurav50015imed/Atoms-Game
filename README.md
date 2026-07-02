# Chain Reaction ⚛️

A fully playable, single-file HTML5 clone of the classic mobile game "Chain Reaction" (Atoms). This is a volatile, turn-based strategy game for two players played on a single device. 

## 🎮 Play the Game
Because this game is completely self-contained, no installation or server is required.
1. Download or clone this repository.
2. Open the `index.html` (or `chain_reaction_game.html`) file directly in any web browser (Chrome, Safari, Firefox, etc.).
3. Alternatively, host it for free using GitHub Pages to play it via a web link!

## ✨ Features
* **Zero Dependencies:** Built entirely with vanilla HTML, CSS, and JavaScript. Everything is packed into one file.
* **Mobile Optimized:** Includes specific touch-event handling, scroll-locking, and viewport meta-tags to ensure it plays perfectly on smartphones and tablets.
* **Haptic Feedback:** Integrates `navigator.vibrate` to provide physical feedback on supported mobile devices when placing atoms and triggering explosions.
* **Visual Polish:** Uses the HTML5 `<canvas>` API for smooth 60fps rendering, featuring glowing neon shadows, 3D atom highlights, and cascading staggered animations for massive chain reactions.

## 📖 How to Play

**The Goal:** Eliminate all of your opponent's atoms from the board.

**The Rules:**
1. The game is played on a 9x6 grid. Player 1 plays as **Red**, and Player 2 plays as **Green**.
2. Players take turns placing one atom of their color in either an empty cell or a cell they already occupy.
3. **Critical Mass:** Every cell has a maximum capacity. When a cell reaches this capacity, it explodes:
   * **Corners:** Explode at 2 atoms.
   * **Edges:** Explode at 3 atoms.
   * **Inner Cells:** Explode at 4 atoms.
4. **Explosions:** When a cell explodes, it resets to zero, and its atoms scatter into the adjacent cells (Up, Down, Left, Right). 
5. **Takeovers:** If your scattered atoms land in a cell owned by your opponent, that cell changes to your color and gains an atom. This can trigger a massive *chain reaction* if it pushes adjacent cells past their critical mass!

## 🛠️ Technical Stack
* **HTML5:** Layout and Canvas element.
* **CSS3:** Flexbox for layout, overlay styling, and UI animations.
* **JavaScript (ES6):** * 2D Array matrix for game state management.
  * Recursion and `setTimeout` for staggered visual chain reactions.
  * Unified Mouse/Touch event listeners for cross-device compatibility.

## 🚀 Potential Future Updates
* [ ] Add an AI Opponent (Minimax algorithm).
* [ ] Support for 3 or 4 local players.
* [ ] Customizable grid sizes (e.g., 10x10, 15x10).
* [ ] Dark mode/Light mode themes.

---
*Created as a fun project to explore 2D arrays, recursion, and HTML5 Canvas.*
