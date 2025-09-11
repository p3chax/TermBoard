# 🖥️ TermBoard - A colourful terminal dashboard for devs

> Live CPU • Memory • Network • GitHub stars • Clock - right in your terminal, powered by [Rich](https://github.com/Textualize/rich).

---

## ✨ Features

* Live system monitor — CPU %, memory usage, network I/O
* GitHub flex — sums up total stargazers across public repos ⭐
* Beautiful TUI — clean panels, colours, and a neat clock
* Cross‑platform — just run it anywhere Python works

---

## 🚀 Quick Start

Requires **Python 3.8+**

```bash
git clone https://github.com/Rayaan2009/termboard.git
cd termboard

python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate

pip install -r requirements.txt

python termboard.py
```

Press `Q` or `Ctrl+C` to exit.

---

## 🔧 Configuration

Edit the config section near the top of `termboard.py`:

```python
REFRESH_SEC = 1.0
GITHUB_USER = "Rayaan2009"
```

---

## 🧠 How it Works

* `psutil` grabs CPU, memory, and network data
* `requests` pulls GitHub repo data and sums stars
* `rich` lays everything out in a live dashboard

---

## 🕹 Controls

* `Q` or `Ctrl+C` — quit

---

## 📦 Requirements

```txt
rich
psutil
requests
```

---

## 🧪 Troubleshooting

* Stars show `N/A`: you might be offline or rate‑limited
* Network numbers are cumulative since boot — that’s normal
* On Windows, use Windows Terminal or PowerShell 7+ for best colours

---

## 🗺 Roadmap

* CLI flags: `--user`, `--refresh`
* Per‑core CPU view
* Disk usage panel
* Authenticated GitHub support
* Tiny sparklines for CPU/memory

---

## 🤝 Contributing

Fork, branch, commit, PR. Keep code clean and commented.

---

## 📝 License

MIT License, see LICENSE file.

---

## 🙌 Credits

* Built with [Textualize Rich](https://github.com/Textualize/rich)
* System stats from [psutil](https://github.com/giampaolo/psutil)

---

## 📂 Project Structure

```
termboard/
├─ termboard.py
└─ README.md
```

<p align="center">
Made with ❤️ by <strong>Rayaan2009</strong>
</p>

Happy hacking - smash that ⭐ if you enjoy TermBoard!
