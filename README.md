# 🎓 CampusEvents — Campus Event Management System

> HCI Assignment — Prototype built with plain HTML, CSS, and JavaScript. No frameworks, no install needed.

---

## 📋 What it does

A fully interactive web app that lets students:

- **Browse & search** campus events (workshops, seminars, sports, club events)
- **Register** for events with a validated form
- **Rate & review** events they attended
- **Track** their upcoming and past events

---

## 🖥️ Screens

| Screen | Description |
|--------|-------------|
| **Home** | Event listing with search and category filters |
| **Event Detail** | Full info — date, time, venue, facilitator, seats |
| **Registration** | Form with inline validation (name, student ID, email, faculty) |
| **Feedback** | Star ratings (overall + content, organisation, venue) + written review |
| **My Events** | Registered upcoming events and past attended events |

---

## 🚀 How to run it

### Option 1 — Just open the file (easiest)
```
1. Download or clone this repo
2. Double-click index.html
3. It opens in your browser — done!
```

### Option 2 — Clone with Git
```bash
git clone https://github.com/YOUR-USERNAME/campus-events.git
cd campus-events
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

### Option 3 — Live server (recommended for development)
If you have VS Code:
1. Install the **Live Server** extension (ritwickdey.LiveServer)
2. Right-click `index.html` → **Open with Live Server**
3. Changes auto-reload in the browser

Or with Python:
```bash
cd campus-events
python -m http.server 8000
# Then open http://localhost:8000
```

---

## 📁 Project structure

```
campus-events/
│
├── index.html        ← Entire app (HTML + CSS + JS in one file)
└── README.md         ← This file
```

Everything is in a single `index.html` — no build tools, no npm, no dependencies.

---

## ✏️ How to contribute / edit

### Adding a new event
Open `index.html` and find the `events` array near the top of the `<script>` section:

```javascript
const events = [
  {
    id: 7,                              // Use next available number
    title: "Your Event Title",
    type: "workshop",                   // workshop | seminar | sports | club
    icon: "🎯",                         // Any emoji
    date: "Mon, 20 Apr 2026",
    time: "10:00 – 12:00",
    venue: "Room 101, Block A",
    seats: 30,                          // Available seats
    total: 30,                          // Total capacity
    desc: "Description of the event.",
    facilitator: "Dr. Someone",
    color: "#dbeafe"                    // Background color for the banner
  },
  // ... add more here
];
```

### Changing styles
All CSS is in the `<style>` block at the top of `index.html`. Key variables are in `:root`:

```css
:root {
  --blue: #185FA5;      /* Primary action color */
  --green: #3B6D11;     /* Success / seminar color */
  --amber: #854F0B;     /* Sports color */
  --purple: #534AB7;    /* Club events color */
}
```

---


## 🏛️ HCI Principles applied

| Principle | How it's implemented |
|-----------|----------------------|
| **Visibility & feedback** | Inline error messages, toast notifications, seat counts turn red when full |
| **Error prevention** | Email validated with regex, confirmation checkbox before submitting |
| **Consistency** | Same card style, tag colours, and button styles across all screens |
| **Simplicity** | One primary action per screen; back button always visible |

---

## 📝 Usability issues found (peer testing)

1. **Filters not immediately noticed** → Suggested fix: Add a label "Filter by:" above the filter buttons
2. **Registration form feels long** → Suggested fix: Split into a 2-step form (Personal Info → Confirm)
3. **No way to cancel registration** → Suggested fix: Add a "Withdraw" button in My Events → Upcoming tab

---

## 👥 Team

| Name | Role |
|------|------|
| [Your Name] | Developer / Designer |
| [Teammate 1] | Tester / Report |
| [Teammate 2] | Presentation |

---

## 📄 License

MIT — free to use and modify for academic purposes.
