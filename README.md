# Interactive Dice Roll Application

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Vercel Deployment](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)](https://diceroll-vasavi.vercel.app/)
[![GitHub Repository](https://img.shields.io/badge/GitHub-Repository-181717?style=for-the-badge&logo=github)](https://github.com/cse260001082/Dice_roll)

A responsive, lightweight web-based Dice Roll simulator built using vanilla HTML5, CSS3, and JavaScript. The application enables users to roll either a single die or two dice with smooth physical roll animations, calculates real-time totals, and tracks the history of recent rolls in a dedicated feed.

---

## Live Deployment and Repository Links

- **Live Application:** [https://diceroll-vasavi.vercel.app/](https://diceroll-vasavi.vercel.app/)
- **GitHub Repository:** [https://github.com/cse260001082/Dice_roll](https://github.com/cse260001082/Dice_roll)

---

## Features

- **Single and Double Dice Modes:** Users can roll one die or two dice simultaneously with dedicated controls.
- **Shake Roll Animation:** Uses CSS keyframe animations to simulate a physical dice roll before revealing the result.
- **Instant Result and Computation:**
  - Single Die: Outputs the face value directly (1 through 6).
  - Double Dice: Displays both individual die outcomes and calculates their sum (e.g., `4 + 5 = 9`).
- **Roll History Tracking:** Dynamically logs previous rolls and maintains a maximum buffer of the 10 most recent entries.
- **Scalable Vector Graphics (SVG):** Custom vector-based dice faces ensuring high-fidelity visuals across high-DPI displays.
- **Responsive Layout:** Centered card interface styled to adapt across desktop, tablet, and mobile viewport sizes.
- **Zero Dependencies:** Pure vanilla implementation requiring no third-party libraries, build steps, or runtime dependencies.

---

## Project Structure

```text
Dice_roll/
├── images/
│   ├── dice1.svg       # Vector asset for die face 1
│   ├── dice2.svg       # Vector asset for die face 2
│   ├── dice3.svg       # Vector asset for die face 3
│   ├── dice4.svg       # Vector asset for die face 4
│   ├── dice5.svg       # Vector asset for die face 5
│   └── dice6.svg       # Vector asset for die face 6
├── index.html          # Semantic markup and structure
├── style.css           # Styling, layout, and shake keyframe animation
├── script.js           # Randomization logic, DOM updates, and history tracking
└── README.md           # Project documentation
```

---

## Tech Stack

| Component | Technology | Description |
|---|---|---|
| Frontend Markup | HTML5 | Semantic page layout, interactive buttons, and media containers |
| Styling & Animations | CSS3 | Flexbox alignment, responsive breakpoints, and keyframe shake effects |
| Application Logic | JavaScript (ES6+) | Random number generation, asynchronous timing, and dynamic DOM manipulation |
| Assets | SVG | Scalable vector graphic representations of dice faces |
| Deployment | Vercel | Production hosting and continuous delivery |

---

## Getting Started

### Option 1: Run Locally via Browser

1. Clone the repository:
   ```bash
   git clone https://github.com/cse260001082/Dice_roll.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Dice_roll
   ```
3. Open `index.html` directly in any web browser.

### Option 2: Run via Local Development Server

Using **Python**:
```bash
python -m http.server 8000
```
Open `http://localhost:8000` in your browser.

Using **Node.js (npx serve)**:
```bash
npx serve .
```

---

## Implementation Details

1. **Random Generation:**  
   Uses standard uniform random distribution to generate values between 1 and 6:
   ```javascript
   function getRandom() {
     return Math.floor(Math.random() * 6) + 1;
   }
   ```

2. **Animation and Timing:**  
   Applies the `.shake` class to trigger CSS rotation oscillation. A 500ms `setTimeout` introduces roll latency before settling on the target value.

3. **DOM Updates and History Capping:**  
   Updates the image sources dynamically (`images/dice{n}.svg`) and prepends the new result to the roll history list, automatically truncating entries beyond 10 items.

---

## Author

- **GitHub:** [@cse260001082](https://github.com/cse260001082)
- **Live Demo:** [https://diceroll-vasavi.vercel.app/](https://diceroll-vasavi.vercel.app/)
