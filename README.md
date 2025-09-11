# 🖥️ TermBoard — A colourful terminal dashboard for devs

> Live CPU • Memory • Network • GitHub stars • Clock - right in your terminal, powered by [Rich](https://github.com/Textualize/rich).


---

## ✨ Features

* **Live system monitor** — CPU %, memory usage, network I/O
* **GitHub flex** — sums up your **total stargazers** across public repos ⭐
* **Beautiful TUI** — clean panels, colours, and a neat clock
* **Zero setup faff** — a single Python file, cross‑platform

---

## 🚀 Quick Start

> Requires **Python 3.8+**

```bash
# 1) Clone (or download the file)
git clone https://github.com/<your-username>/termboard.git
cd termboard

# 2) (Optional) Create a virtual env
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate

# 3) Install deps
pip install -r requirements.txt  # or: pip install rich psutil requests

# 4) Run it
python termboard.py  # or: python3 termboard.py
```

> **Quit:** press `Q` or `Ctrl+C`.

---

## 🔧 Configuration

Open `termboard.py` and tweak the **Config** section near the top:

```python
# Config
REFRESH_SEC = 1.0
GITHUB_USER = "Rayaan2009"  # change if needed
```

* `REFRESH_SEC` — how often the dashboard refreshes (seconds)
* `GITHUB_USER` — the GitHub account used to total up stars

> **Note:** The GitHub request is **unauthenticated** by default and subject to rate‑limits. If the GitHub panel shows `N/A`, you may have hit the limit or be offline.

---

## 🧠 How it works (high‑level)

* **`psutil`** grabs CPU %, memory stats, and network I/O counters
* **`requests`** hits the public `GET /users/{username}/repos` API and sums `stargazers_count`
* **`rich`** renders a responsive layout with a System table, GitHub panel, and Clock panel using `Live`

---

## 🕹 Controls

* `Q` or `Ctrl+C` - exit gracefully

---

## 📦 Requirements

Create a `requirements.txt` (optional but tidy):

```txt
rich
psutil
requests
```

---

## 🧪 Troubleshooting

* **GitHub stars show `N/A`** → likely rate‑limited or no internet. Try again in a minute, or reduce refresh rate.
* **Network numbers look huge** → they’re **cumulative since boot** (KB sent/received). That’s expected.
* **`pip` can’t find packages** → check you’re in the virtual env; try `pip install --upgrade pip`.
* **Windows terminal colours look off** → use Windows Terminal / PowerShell 7+.

---

## 🗺 Roadmap Ideas (PRs welcome)

* CLI args: `--user`, `--refresh`, `--no-github`
* Per‑core CPU bars + load average
* Disk usage panel
* GitHub auth via `GITHUB_TOKEN` env for higher rate‑limits
* Tiny charts/sparklines for CPU/memory
* Theme switch (light/dark/mono)

---

## 🤝 Contributing

1. Fork the repo
2. Create a branch: `git checkout -b feat/per-core`
3. Commit: `git commit -m "feat: per-core cpu bars"`
4. Push & open a PR — short description + before/after screenshot

Code style: keep it readable, commented, and friendly.

---

## 📣 Make it Popular

* **Good repo name:** `termboard` or `rich-termboard`
* **Topics:** `terminal`, `tui`, `rich`, `psutil`, `dashboard`, `monitoring`, `python`
* **README tips:** keep the GIF up top, add a short tagline, and a one‑liner install
* **Share it:** post a quick clip on X/Threads/LinkedIn + a screenshot on Reddit r/commandline

---

## 📝 License

MIT — do what you like, just keep the notice. Add a `LICENSE` file with the standard MIT text.

---

## 🙌 Credits

* Built with the excellent [Textualize Rich](https://github.com/Textualize/rich)
* System stats via [psutil](https://github.com/giampaolo/psutil)

---

## 📂 Project Structure

```
termboard/
├─ termboard.py       # main script
├─ requirements.txt   # dependencies (optional)
├─ demo.gif           # your screen recording/gif
└─ README.md          # this file
```

---

<p align="center">
  Made with ❤️ by <strong>Rayaan2009</strong>
</p>

Happy hacking — smash that star button if this made your terminal prettier. 💙
