# Quno!

Quno is a digital version of the classic card game UNO — with a twist. Every game is shuffled using **true quantum randomness**, not just pseudorandom functions. This makes Quno the first online UNO-style game to use actual quantum mechanics to influence gameplay.

---

## 🔍 What is This?

Quno is a single-player browser game (HTML, CSS, JavaScript) where you play against a computer opponent. The game uses a real-world **quantum random number generator (QRNG)** from the **Australian National University (ANU)** to shuffle the deck.

This means that the outcome of every game is not just "random" in the computer science sense — it's **physically random**, derived from unpredictable quantum events.

---

## 🃏 Gameplay Overview

- You and the AI start with 7 cards each.
- One card is placed face up on the pile.
- Your goal is to get rid of all your cards first.
- On your turn, you can:
  - Play a card that matches the color or value.
  - Play a Wild card and choose the color.
  - Draw a card if you can't play.
- Special cards affect gameplay:
  - `+2`, `Draw4`: opponent draws cards.
  - `⏩`: skip turn.
  - `↺`: reverse (treated as skip since it's a 2-player game).
  - `DeckSwap`: swaps your hand with the opponent.
- First to 0 cards wins.

---

## 🎮 Controls

- **Click** on a card to play it.
- **Click "Draw Card"** if you can't play.
- When you play a `Wild`, a prompt will ask you to choose a color.

---

## 📦 Code Structure

### 1. **HTML & CSS**
- The structure is defined in a single HTML file.
- Styling includes:
  - A wood texture background.
  - Card layout with rounded colored rectangles.
  - Centered pile and horizontal player hands.
  - Responsive opponent and player card areas.

### 2. **JavaScript Modules**

#### a. **Deck Setup**
```js
const COLORS = ['Red', 'Green', 'Blue', 'Yellow'];
const VALUES = ['0', '1', ..., '+2'];
const SPECIALS = ['Wild', 'Draw4', 'DeckSwap'];
