# Claude Counter

A lightweight browser extension that enhances **claude.ai** with real-time insights into your usage, including token count, cache timing, and rate limits.

---

## ✨ Features

### 🔢 Token Count

* Displays an **approximate token count** for the current conversation
* Includes a **visual progress bar** against the 200k context window

### ⏱ Cache Timer

* Shows how long your conversation remains cached
* Helps you continue chats within the **cheaper cached window**

### 📊 Usage Bars

* Tracks:

  * **Session usage (5-hour window)**
  * **Weekly usage (7-day window)**
* Includes:

  * Accurate progress bars
  * Reset countdown timers
* Uses Claude’s internal API for **more precise data** than the default `/usage` page

---

## 📦 Installation

### Chrome / Edge / Chromium

1. Download:
   👉 [https://github.com/Claude-Count-Credit/releases/download/V0.4.2/claude-counter-0.4.2.1.zip](https://github.com/Claude-Count-Credit/releases/download/V0.4.2/claude-counter-0.4.2.1.zip)
2. Open:
   `chrome://extensions`
3. Enable **Developer mode**
4. Drag and drop the ZIP file into the page

---

### Firefox

1. Download:
   👉 [https://github.com/Claude-Count-Credit/releases/download/V0.4.2/claude-counter-0.4.2.xpi](https://github.com/Claude-Count-Credit/releases/download/V0.4.2/claude-counter-0.4.2.xpi)
2. Drag the file into any Firefox window
3. Click **Add**

---

### Userscript

1. Install from:
   👉 [https://github.com/Claude-Count-Credit/blob/main/userscript/claude-counter.user.js](https://github.com/Claude-Count-Credit/blob/main/userscript/claude-counter.user.js)
2. Use with a userscript manager like Tampermonkey

---

## ⚙️ How It Works

* Intercepts Claude API responses to extract:

  * Conversation metadata
  * Usage statistics
* Uses a bundled tokenizer (`o200k_base`) to estimate token counts
* Combines:

  * `/usage` endpoint
  * Live SSE `message_limit` data
* Result: **more accurate usage tracking** than Claude’s default UI
* Observes DOM changes to dynamically inject UI elements

---

## 🔒 Privacy

* ✅ No external servers
* ✅ No tracking or analytics
* ✅ All data stays local in your browser
* Reads only:

  * `lastActiveOrg` cookie (to fetch usage data)
* Makes requests exclusively to:

  * `claude.ai`

---

## 🙌 Credits

* Token counting via:
  **gpt-tokenizer** (MIT)
* Inspired by:
  **Claude Usage Tracker** by lugia19

