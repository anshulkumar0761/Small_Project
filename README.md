# 💻 Hacker Simulator

A fun, terminal-style **fake hacking simulation** built with pure HTML, CSS and JavaScript. Green text on a black screen, random delays, and blinking dots, just like in the movies.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

🔗 **Live Demo:** [Click here to try it](https://YOUR-USERNAME.github.io/hacker-simulator/)

---

## ⚠️ Disclaimer

This project is **only a visual prank / simulation**. It does **not** hack anything, read any files, or send any data anywhere. All the messages on screen are hard-coded text. It was made purely for learning and fun.

---

## 🎬 What it looks like

```
> Initializing Hacking...
> Reading your files...
> Password Detected...
> Sending all files to the server...
> cleaning up...
```

Each line appears after a random delay (1 to 6 seconds), followed by animated dots that blink: `.` → `..` → `...`

---

## ✨ Features

- 🖥️ Retro terminal look (black background, green monospace text)
- ⏱️ Random delay before every new line
- 🔵 Blinking dots animation after each line
- 📦 No libraries, no frameworks, just one `index.html` file
- 📱 Responsive viewport setup

---

## 🚀 How to run

**Option 1: Open directly**

1. Download or clone this repository
2. Double-click `index.html`

**Option 2: Clone with Git**

```bash
git clone https://github.com/anshulkumar0761/hacker-simulator.git
cd hacker-simulator
```

Then open `index.html` in any browser.

---

## 🧠 How it works

| Part | What it does |
|---|---|
| `text` array | Stores all the messages to display |
| `sleep(ms)` | Returns a Promise that waits for `ms` milliseconds |
| `delay()` | Waits for a random time between 1 and 6 seconds |
| `addLine(message)` | Creates a `<p>` element, adds it to the page and returns it |
| `addDots(p)` | Animates dots on that line, 2 rounds of `.` `..` `...` |
| `run()` | Main loop: wait, add line, animate dots, repeat |

### Core idea

```javascript
async function run() {
    for (const message of text) {
        await delay();               // wait randomly
        const p = addLine(message);  // show the line
        await addDots(p);            // animate the dots
    }
}
```

`await` makes sure each step finishes before the next one starts.

---

## 📚 What I learned

- **Promises** and `async` / `await`
- Using `setTimeout` to create delays
- DOM manipulation: `createElement`, `textContent`, `appendChild`
- Passing **parameters** to functions and using `return`
- Debugging with the browser console (F12)

---

## 📁 Project structure

```
hacker-simulator/
├── index.html
└── README.md
```

---

## 🤝 Contributing

Suggestions and improvements are welcome! Feel free to fork the repo and open a pull request.

---

## 👤 Author

**Anshul Kumar**
GitHub: [@anshulkumar0761](https://github.com/anshulkumar0761)
---

⭐ If you liked this project, give it a star!
