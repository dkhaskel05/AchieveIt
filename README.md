# 🎯 AchieveIt — Student Life OS

> A beautifully designed, fully offline Student Productivity App built with pure HTML, CSS and JavaScript. No frameworks. No dependencies. One file opens everything.

![AchieveIt Banner](https://img.shields.io/badge/AchieveIt-Student%20Life%20OS-5b8c5a?style=for-the-badge&logo=target&logoColor=white)
![HTML](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)

---

## 📸 Features at a Glance

| Section | What it does |
|---|---|
| 🌅 **Daily Splash** | Opens with a motivational quote + time-based greeting every session |
| 📋 **Task Manager** | Add, organise, complete & timer-track tasks across 5 folders |
| 📊 **Daily Score** | Productivity score (0–100) with heatmap, bars & end-of-day message |
| 🗓 **Class Schedule** | Full timetable, CSV upload, per-class attendance tracking |
| 📝 **Exam Tracker** | Upcoming exams with 2-week + 3-day reminders & prep slider |
| 🎯 **Goals** | Life goals with pace prediction ("you'll achieve this in ~4 months") |
| 🔔 **Notifications** | Smart alerts: overdue tasks, attendance warnings, exam countdowns |
| 🌙 **Dark Mode** | Full dark theme, preference saved in localStorage |

---

## 🚀 Getting Started

### Option 1 — Open directly (simplest)
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/achieveit.git

# Open in browser — no build step needed
open achieveit/index.html
```

### Option 2 — GitHub Pages (recommended)
1. Fork or push this repo to your GitHub account
2. Go to **Settings → Pages**
3. Set Source to **main branch / root**
4. Your app will be live at `https://your-username.github.io/achieveit/`

### Option 3 — Local server
```bash
cd achieveit
python3 -m http.server 8080
# Visit http://localhost:8080
```

---

## 📁 Project Structure

```
achieveit/
├── index.html          ← Entire app (HTML + CSS + JS, self-contained)
├── README.md           ← This file
├── LICENSE             ← MIT License
├── .gitignore          ← Git ignore rules
└── sample-schedule.csv ← Example CSV for class schedule import
```

---

## 🗓 CSV Schedule Upload Format

Upload your semester timetable as a `.csv` file. The app will parse it automatically and store it for the entire semester.

**Format:**
```
Subject,Day,StartTime,EndTime,Room,Faculty
Data Structures,Mon Wed Fri,09:00,10:00,Lab-3,Dr. Sharma
Operating Systems,Tue Thu,11:00,12:00,Room-201,Prof. Mehta
Database Management,Mon Wed,14:00,15:00,Room-105,Dr. Gupta
Mathematics-III,Tue Thu Sat,08:00,09:00,Room-301,Dr. Joshi
```

**Rules:**
- First row can be a header (will be skipped)
- Multiple days separated by spaces: `Mon Wed Fri`
- Valid days: `Mon`, `Tue`, `Wed`, `Thu`, `Fri`, `Sat`
- Time in 24-hour format: `09:00`, `14:30`

---

## 📊 Daily Score Calculation

Your daily productivity score (0–100) is computed from:

| Factor | Weight | How it's measured |
|---|---|---|
| Task Completion | 35% | Completed tasks ÷ total tasks |
| Class Attendance | 25% | Average attendance % across subjects |
| Study Time | 25% | Timer sessions (target: 2 hours/day) |
| Goal Progress | 15% | Average progress across all life goals |

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `Ctrl + N` / `Cmd + N` | Open new task modal |
| `Escape` | Close any open modal |

---

## 💾 Data Storage

All data is stored locally in your browser using **localStorage**. Nothing is sent to any server.

| Key | Contents |
|---|---|
| `ai_t` | Tasks array |
| `ai_c` | Classes array |
| `ai_e` | Exams array |
| `ai_g` | Goals array |
| `ai_d` | Daily log (scores, activity) |
| `ai_theme` | Dark/light preference |

To reset all data, open your browser DevTools → Application → Local Storage → Clear all `ai_*` keys.

---

## 🛠 Tech Stack

- **HTML5** — Semantic structure, forms, modals
- **CSS3** — Custom properties, Flexbox, Grid, animations, responsive design
- **Vanilla JavaScript** — DOM manipulation, localStorage, file parsing, timers
- **Google Fonts** — Nunito + Fraunces (loaded from CDN)

**Zero dependencies. No npm. No build tools. No frameworks.**

---

## 📚 Concepts Used (Assignment Coverage)

### HTML
- Semantic tags: `header`, `nav`, `main`, `aside`, `section`, `article`, `footer`
- Forms, inputs, selects, range sliders, file inputs
- SVG for the score ring animation
- Tables for the timetable view

### CSS
- Custom properties (design tokens) for full theming
- CSS Flexbox and Grid for all layouts
- Responsive design with media queries (mobile, tablet, desktop)
- Animations: splash float, card entry, timer glow, modal transitions
- Dark mode via `[data-theme="dark"]` attribute

### JavaScript
- Variables, arrays, objects, functions, loops, conditionals
- DOM manipulation and event handling
- `localStorage` for persistent data
- `FileReader` API for CSV parsing
- `setInterval` / `Date` for timers and clock
- Template strings, arrow functions, Array methods

### Git & GitHub
- Repository with README, LICENSE, .gitignore
- GitHub Pages deployment ready

---

## 🎓 Assignment Bonus Features Implemented

- ✅ Level 1 — Search tasks
- ✅ Level 2 — Filter by status (All / Pending / Done / Overdue)
- ✅ Level 3 — Local Storage persistence
- ✅ Level 4 — Dark Mode toggle
- ✅ **Extra** — Task timer with elapsed time tracking
- ✅ **Extra** — Important task flag with visual priority
- ✅ **Extra** — Class schedule with attendance tracking
- ✅ **Extra** — Exam tracker with auto-reminders
- ✅ **Extra** — Life goals with pace prediction
- ✅ **Extra** — Daily productivity score & activity heatmap
- ✅ **Extra** — Push notifications (in-app) for deadlines & motivation
- ✅ **Extra** — CSV schedule upload for entire semester
- ✅ **Extra** — Motivational splash screen with daily quotes
- ✅ **Extra** — Personalised productivity advice
- ✅ **Extra** — End-of-day message ("Well done!" / "Keep going!")

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 👨‍💻 Developer

Built as a Web Development assignment project.

> *"An investment in knowledge pays the best interest."* — Benjamin Franklin
