<div align="center">

# 🖥️ TerminalX

**A single-file terminal shell in pure Python — 196+ built-in commands, TUI file manager, plugin system, REST/WebSocket server and self-diagnostics. No external dependencies.**

[🇬🇧 English](README.md) · [🇵🇱 Polski](README.pl.md)

![Version](https://img.shields.io/badge/version-39.2-blue)
![Python](https://img.shields.io/badge/python-3.10%2B-informational)
![Dependencies](https://img.shields.io/badge/dependencies-0-success)
![License](https://img.shields.io/badge/license-custom-lightgrey)

</div>

---

## ✨ What is TerminalX?

TerminalX is a **complete shell environment shipped as one Python file** (`TerminalX.py`, ~1.9 MB). It works as a replacement / companion to cmd, PowerShell or bash, and runs on **Windows, Linux and macOS** using only the standard library.

```bash
python TerminalX.py
```

## 🌟 Standout Features

### 🧩 Plugin System (API v2.0)
- Load / unload / reconnect plugins at runtime (`plugin list|info|connect|disconnect`, `plug`)
- **Sandboxed execution** with configurable security levels, static source scanning
- **Trust database** — plugins are hashed and signed (`_plugin_sign` / `_plugin_verify`)
- Remote **plugin repositories** with search and install
- Scaffolding via `pkg create` and `builder`

### 🌐 Built-in Network Server Stack
A single `serve` command spins up an entire API surface:
- **REST API v1/v2/v3** with auto-generated **OpenAPI schema**
- **WebSocket server** with proper handshake + frame protocol and event broadcasting
- **Server-Sent Events (SSE)** stream of shell events
- **Web GUI panel** — ANSI-to-HTML colored output rendered in the browser
- **Daemon mode** with token authentication, **rate limiting** and **webhooks** (fire on shell events)

### 🛟 Crash Recovery Mode
If startup fails (broken config, corrupted history, bad plugin), TerminalX drops into a **recovery shell** that:
- diagnoses the terminal, config, aliases, history, plugins
- offers one-key **smart fixes** for each subsystem
- creates and restores **configuration backups**
- blocks commands known to have caused the crash

### ✅ Self-Diagnostics — `selfcheck`
A built-in test suite of **100+ checks** across categories: tokenizer, config, filesystem, history, aliases, plugins, terminal, crash handling, network, performance benchmarks, integrity, versions, config schema validation, resources, syntax, commands. Run `selfcheck` and get a colored pass/fail report with perf timings.

### 🖼️ Full TUI Suite (curses)
- `nav` — interactive file manager (preview, filtering, sorting, permissions, breadcrumbs)
- `tui` — main menu
- `procmon` — interactive process monitor
- `logtail` / `logview` — live log tailing and viewer
- `fman`, `nano` — file manager and built-in **nano-like editor**

### 🤖 AI & Productivity
- `ai` — chat with an LLM (streaming, configurable provider) straight from the shell
- `translate` — translation, `weather` — rich weather dashboard with ASCII art, UV index, Beaufort scale, wind arrows
- `note`, `todo`, `bm` (bookmarks), `cb` (multi-slot clipboard), `calc`, `qr`, `passgen`, `uuid`, `encrypt`

### 🧠 Smart Shell Core
- **Pipelines, redirects, `&&`/`||`, variable expansion** — own tokenizer/parser
- Tab completion (paths, commands, config values), **Ctrl+R** interactive history search
- Aliases, macros (`macro`), session history with dedup and timestamps
- **Profiles** (`profile list|switch|create|diff|export...`) with auto-detected environment suggestions (`envdetect`)
- **Sessions & split panes** (`session`, `split`, `tmux`-like)

### ⏰ Automation
- `sched` — scheduler: one-shot, interval and **full cron syntax** jobs with logs
- `watch` — event rules: trigger commands on **file/dir changes, disk, process or network interface events**
- `cron2` — crontab viewer/validator with human-readable field explanation
- `autostart` — manage startup entries (commands, plugins)
- Webhooks and event hooks fire after every command

### 🧰 196+ Built-in Commands
- **File ops:** `ls cd pwd cat touch mkdir rm cp mv tree du stat head tail diff chmod chown`
- **Search:** `grep find ff` (fuzzy-finder with interactive picker)
- **Text/data:** `json jq yaml wc wordfreq readability base64 hexdump csvplot highlight` (syntax highlighting for many languages)
- **System:** `sysinfo diag ps ps2 kill pkill2 tasklist taskkill free df uptime cpugraph sysmon netmon portscan`
- **Network:** `ping traceroute netstat wget curl ipconfig dns whois http ssh net arp`
- **Windows admin:** `sfc dism chkdsk bcdedit reg diskpart schtasks gpupdate cipher eventvwr` ... (guarded by root/UAC checks)
- **Dev:** `git docker pip envdiff pyrepl debug` (mini Python debugger), `timeit`
- **Windows shell compatibility layer** — cmd-style commands work on Linux/macOS too

### 🔌 OS Integration — `integrate`
Install TerminalX into your system in one step:
- add to **PATH**, create **symlinks**, **desktop shortcut**, **autostart**
- register as a **shell** in `/etc/shells`
- **file-type handlers** (open extensions with TerminalX), **context menu** entries (Windows/Linux/macOS)
- **drag & drop daemon** — drop files on a desktop target to process them in the shell

### 🛡️ Security & Quality
- No telemetry — **hardcoded off**, verified by selfcheck
- Root/sudo guard before dangerous operations
- Crash logs (`crashlog`), buffered log writer with rotation (`logrotate`, `logscan`, `logs` with JSON/CSV/HTML export)
- Portable mode (`portable`, `--data`, `--plugins`), respects **NO_COLOR** / `TERM=dumb`
- `build_exe` — package itself into a standalone executable

### 🌍 i18n
Full **Polish and English** translations (`lang/pl.json`, `lang/en.json`) plus an auto message map — switch anytime with `lang pl|en`. First run offers a **setup wizard** (`wizard`).

## 📦 Requirements

- **Python 3.10+** (enforced at boot)
- **Zero pip dependencies** — everything is standard library
- Optional: `curses` (bundled with Python on Linux/macOS; enables full TUI)

## 🚀 Quick Start

```bash
# run the shell
python TerminalX.py

# look around
help            # command list
tui             # interactive menu
sysinfo         # system dashboard
selfcheck       # run 100+ internal tests
serve           # start REST/WS/SSE web panel
wizard          # first-run configuration wizard
```

### Useful environment variables

| Variable | Purpose |
|---|---|
| `TERMINALX_OFFLINE` | force offline mode (no network detection) |
| `TERMINALX_NO_COLOR` / `NO_COLOR` | disable ANSI colors |
| `TERMINALX_RC` | custom rc-file path |
| `TERMINALX_CONFIG` | custom config path |
| `TERMINALX_PROFILE` | start with a given profile |
| `TERMINALX_THEME` | start theme (`dark` / `light` + custom) |
| `TERMINALX_PLUGINS` | custom plugins directory |
| `TERMINALX_VERBOSE` / `TERMINALX_DEBUG` | verbose/debug output |

## 🗂️ Data Layout

TerminalX keeps all state in its home directory (portable-friendly): `config`, `history`, `aliases`, `lang/`, plugins, package DB, trust DB, sessions, scheduler & watch state, logs and crash logs.

## 📄 License

See `about` / `license` command inside the shell for the full license text.

---

<div align="center">

[🇬🇧 English](README.md) · [🇵🇱 Polski](README.pl.md)

</div>
