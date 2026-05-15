# ⏱️ StopWatch

A clean, minimal stopwatch web app built with **HTML**, **CSS**, and **vanilla JavaScript** — no libraries, no frameworks, just pure frontend code.

---

## ✨ Features

- ▶️ **Start** the timer with one click
- ⏹️ **Stop** / pause the timer at any point
- 🔄 **Reset** back to `00 : 00 : 00`
- Displays **Minutes : Seconds : Milliseconds**
- Auto-pads single digits with a leading zero (e.g., `05` instead of `5`)
- Clean dark-themed UI with colored action buttons

---

## 🗂️ Project Structure

```
stopwatch/
├── index.html   # App layout and structure
├── style.css    # Dark theme styling
└── script.js    # Timer logic and button controls
```

---

## 🚀 How to Run

No installation needed. Just open the project locally:

1. **Clone this repository**
   ```bash
   git clone https://github.com/mahfooz091/stopWatch.git
   ```

2. **Open `index.html` in your browser**
   ```bash
   cd stopwatch
   open index.html
   ```
   Or simply double-click `index.html` in your file explorer.

---

## 🧠 How It Works

### Timer Logic (`script.js`)

The timer uses `setInterval()` to call a function every **10 milliseconds**.

| Variable | Tracks |
|----------|--------|
| `msec`   | Milliseconds (0–99) |
| `secs`   | Seconds (0–59) |
| `mins`   | Minutes (counts up) |

**Rollover logic:**
- When `msec` hits `100` → reset to `0`, increment `secs`
- When `secs` hits `60` → reset to `0`, increment `mins`

**Zero-padding:** Uses the ternary operator to format single digits:
```js
let msecString = msec < 10 ? `0${msec}` : msec;
```

### Button Controls

| Button | Action |
|--------|--------|
| **Start** | Clears any existing interval, then starts a fresh one |
| **Stop**  | Pauses the timer by clearing the interval |
| **Reset** | Stops the timer and resets all values to `0` |

---

## 🎨 Styling Highlights

- Dark background (`rgba(0,0,0,0.7)`) for a sleek look
- Buttons use **CSS custom properties** (`--clr`) for individual colors:
  - 🔴 Stop → Red
  - 🟢 Start → Green
  - 🔵 Reset → Blue
- Fully centered layout using **Flexbox**

---

## 🛠️ Built With

- HTML5
- CSS3 (Flexbox, CSS Variables)
- JavaScript (ES6 — `setInterval`, `clearInterval`, template literals, ternary operators)


---

## 🙋‍♂️ Author

**Mahfooz Alam**  
B.Tech CSE Student | Parul University  
