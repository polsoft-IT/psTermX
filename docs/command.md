# 📖 TerminalX — Command Reference

[🇬🇧 English](command.md) · [🇵🇱 Polski](command.pl.md)

All commands available in TerminalX v39.2, grouped by category. Aliases are shown in brackets. Run `help <cmd>` in the shell for detailed help on any command.

---

## 🗂️ Navigation & Directories

| Command | Description |
|---|---|
| `pwd` | Print the current working directory (full path) |
| `cd` | Change the current working directory |
| `ls` | List directory contents with colors, icons and sorting `[dir]` |
| `tree` | Show a directory tree with coloring and filtering |
| `bm` | Directory bookmarks — add, browse, jump, delete `[bookmark, bookmarks]` |
| `nav` | Interactive TUI file browser `[fb, fm, browse, files]` |
| `fman` | File manager — copy, move, preview, tree `[filemanager, files2]` |
| `txhome` | Go to the TerminalX home directory (TX_HOME) `[tx-home, cdhome]` |
| `txplugins` | Go to the plugins directory `[txplugins, cdplugins]` |
| `txmodules` | Go to the modules directory `[txmodules, cdmodules]` |
| `txgui` | Go to the TerminalX GUI overlay directory `[txgui, cdgui]` |
| `clear` | Clear the terminal screen `[cls]` |

## 📄 File Operations

| Command | Description |
|---|---|
| `touch` | Create a new file or update its modification time |
| `mkdir` | Create a directory — supports nested paths (`-p`) `[md]` |
| `cp` | Copy a file or directory `[copy]` |
| `mv` | Move or rename a file/directory `[move]` |
| `rm` | Delete a file or directory (with optional confirmation) `[del]` |
| `rmdir` | Delete a directory recursively with its contents `[rd]` |
| `rename` | Rename a file or directory (supports patterns) `[ren]` |
| `archive` | Create and extract archives `[tar, untar, unzip]` |
| `du` | Directory and file sizes `[diskusage, dk]` |
| `stat` | Detailed file metadata: size, dates, permissions, inode |
| `attrib` | File attributes — Windows attrib or Linux stat `[attr]` |
| `finfo` | Full file metadata (type, MIME, encoding, hashes, statistics) `[fileinfo]` |
| `fsutil` | File system tools (Windows fsutil / stat Linux) `[fileutil]` |
| `compact` | NTFS compression (Windows) or compression info (Linux) `[compress-ntfs]` |
| `cipher` | EFS encryption (Windows) / secure free-space wipe `[efs]` |

## 👁️ Viewing & Editing Files

| Command | Description |
|---|---|
| `cat` | Show file contents with syntax highlighting `[type, ccat]` |
| `head` | Show the first N lines of a file (default 10) |
| `tail` | Show the end of a file — live follow mode (`-f`) |
| `nano` | Built-in nano-lite text editor with syntax highlighting `[edit, ed]` |
| `diff` | Compare two files (unified diff) `[compare, cmp]` |
| `diffview` | Compare two files with color output |
| `hexdump` | Binary file viewer (hex + ASCII) with coloring `[xxd, hd, hexview]` |
| `highlight` | Syntax highlighting for files — code with ANSI colors |
| `wc` | Count lines, words, characters and bytes `[wordcount, linecount]` |
| `encode` | Character encoding support: Unicode, ANSI, UTF-8, cp1250, mojibake fix `[charset]` |

## 🔍 Search

| Command | Description |
|---|---|
| `grep` | Search files by pattern — supports regular expressions |
| `find` | Search the directory tree by name, type or date `[find2]` |
| `ff` | Fast fzf-like file search (fuzzy + interactive) `[fzf, fuzzy]` |

## 🧮 Text & Data Processing

| Command | Description |
|---|---|
| `json` | JSON parser / formatter / validator `[jsonformat, jsonlint, jsonpp]` |
| `jq` | Mini jq — JSON queries (stdlib, no jq binary) `[jsonquery]` |
| `jsonview` | JSON viewer and filter `[jv]` |
| `yaml` | YAML parser / formatter (stdlib, no pyyaml) `[yamlformat, yamllint, yamlpp]` |
| `csvplot` | Bar / line chart of CSV data in the terminal `[plotcsv, csvgraph]` |
| `base64` | Base64 encoding / decoding `[b64, b64encode, b64decode]` |
| `hash` | Checksums MD5, SHA1, SHA256, SHA512 |
| `wordfreq` | Word frequency analysis in a file or text `[freqwords, topwords]` |
| `readability` | Readability analysis: Flesch, Fog, SMOG indices `[textstat, readable]` |

## 🐚 Shell Core

| Command | Description |
|---|---|
| `echo` | Print text — supports `$VAR` and escape sequences |
| `history` | Show and search the history of executed commands |
| `alias` | Manage command aliases — add, list, save |
| `unalias` | Remove an alias or all aliases at once |
| `macro` | Macros and command sequences `[mac, m]` |
| `set` | Show or set shell variables and execution options |
| `export` | Set and export an environment variable to child processes |
| `unset` | Remove a shell or environment variable |
| `env` | Show the environment or run a command with a custom one `[environ, environment]` |
| `envs` | Show environment variables with filtering and sorting `[env2, sysenv]` |
| `printenv` | Show the value of an environment variable |
| `envdiff` | Compare environment variables: snapshot vs current `[envcompare]` |
| `source` | Load and execute a TerminalX script (.msh / .rc) `[., exec-script, run-script]` |
| `for-loop` | FOR loop in TerminalX (equivalent of CMD FOR) `[for, loop]` |
| `pysh` | Manage .pysh modules (dynamic shell extensions) `[module]` |
| `session` | Manage TerminalX sessions (tmux-style) `[ses, sessions]` |
| `split` | Pseudo split-screen — split the terminal into panels `[sp]` |
| `tmux` | tmux-style shortcuts for managing sessions and splits `[tx]` |
| `which` | Find a program's path in PATH `[where]` |
| `start` | Run a program or open a file in a new window/background |
| `call` | Run a batch file or shell script and return when done `[bat, batch]` |
| `sudo` | Run a command as root or switch to root mode |
| `elevate` | Elevate privileges to administrator (UAC/sudo) `[runas, su]` |

## 🩺 System Diagnostics & Monitoring

| Command | Description |
|---|---|
| `sysinfo` | Full diagnostics: OS, CPU, RAM, disk, network, Python `[info]` |
| `diag` | System diagnostics: CPU, RAM, disks, network, processes `[sysdiag]` |
| `sysmon` | System monitor — CPU, RAM, swap, disk, network, processes `[htop-lite]` |
| `sysmon-quick` | One-shot resource snapshot (no TUI) |
| `cpugraph` | Live CPU and RAM graph in the terminal (1s refresh) `[cgraph, cpumon]` |
| `procmon` | Process monitor — mini Task Manager TUI `[top, procs, tasks]` |
| `resmon` | Resource monitor (Windows resmon / htop Linux) `[resource-monitor]` |
| `perfmon` | Performance monitor (Windows perfmon / vmstat-top Linux) `[perf, performance]` |
| `free` | RAM and swap information (cross-platform) `[meminfo]` |
| `df` | Disk space info — used and free space `[diskfree]` |
| `uptime` | System uptime and average load |
| `uptime2` | System uptime + load average + local time `[up]` |
| `uname` | Operating system info — kernel, architecture, host |
| `hostname` | Show or change the system hostname `[host, sysname]` |
| `id` | Show UID, GID and groups of the current user (Linux/macOS) `[uid]` |
| `whoami` | Show the current user name (root/user) |
| `systeminfo` | Detailed system information: OS, CPU, RAM, network `[sysinfo-win]` |
| `selfcheck` | Internal tests and self-check for TerminalX `[test, check, verify]` |
| `timeit` | Measure shell command execution time `[benchmark, bench]` |

## ⚙️ Processes & Services

| Command | Description |
|---|---|
| `ps` | List system processes with name and PID filtering `[proc, procs-list]` |
| `ps2` | Process list with name / PID / user filtering `[tlist]` |
| `kill` | Terminate a process by PID or name with signal choice `[killproc]` |
| `pkill2` | Kill a process by name or PID (with confirmation) `[killp, tkill]` |
| `tasklist` | List system processes (Windows tasklist / ps) |
| `taskkill` | Terminate a process by PID or name (Windows taskkill) |
| `sc` | Manage system services (Windows sc / systemctl) `[service]` |
| `dxdiag` | DirectX diagnostics (Windows) / OpenGL/GPU info (Linux) `[gpu-info, directx]` |

## 🌐 Network

| Command | Description |
|---|---|
| `ping` | Test connectivity (system ping or TCP fallback) |
| `traceroute` | Packet route to a host `[tracert, trace, mtr]` |
| `pathping` | Combined ping + traceroute |
| `netstat` | Network statistics and active connections `[nstat, connections]` |
| `netmon` | Network connection and interface monitor `[monitor]` |
| `ipconfig` | Show network configuration (Windows ipconfig / Linux ip) `[ifconfig]` |
| `dns` | DNS queries: A, AAAA, PTR, MX, NS, ALL `[nslookup2, dig2]` |
| `whois` | WHOIS information for a domain or IP `[who-is, domaininfo]` |
| `arp` | ARP table — MAC/IP addresses on the local network `[arp-table]` |
| `portscan` | Multi-threaded TCP port scanner `[pscan]` |
| `net` | Windows NET commands (users, groups, services, shares) `[net-cmd]` |
| `netsh` | Configure Windows networking (netsh) or ip/nmcli (Linux) `[netconfig]` |
| `ssh` | Connect to a host over SSH or manage connection profiles `[ssh-connect]` |
| `mode` | Online/offline mode — manage network access `[network, netmode]` |

## ⬇️ Downloads & HTTP

| Command | Description |
|---|---|
| `curl` | HTTP/HTTPS requests — GET, POST, headers, data (stdlib) `[fetch, fetch-url]` |
| `http` | HTTP client (curl-like): GET/POST/HEAD/PUT/DELETE `[curl2]` |
| `wget` | Download a file from a URL with a progress bar `[download]` |
| `apix` | Interactive API explorer — session with base URL and headers `[apiexplorer]` |

## 🛠️ Windows Administration

| Command | Description |
|---|---|
| `reg` | Windows registry editor (Windows only) `[regedit-cli, registry]` |
| `sfc` | System file scan (Windows sfc / Linux debsums) `[scannow]` |
| `dism` | DISM — Windows image servicing `[repair-image]` |
| `chkdsk` | Check disk for errors — Windows chkdsk / Linux fsck `[checkdisk, fsck]` |
| `diskpart` | Manage disks and partitions (diskpart / parted) `[partition-mgr]` |
| `format` | Format a disk / partition `[fmt-disk]` |
| `bcdedit` | Windows BCD bootloader configuration `[bootcfg]` |
| `schtasks` | Windows task scheduler (schtasks / cron Linux) `[scheduled-tasks]` |
| `gpupdate` | Group policy update `[group-policy]` |
| `powercfg` | Power configuration and energy reports `[poweropts]` |
| `wmic` | WMI interface (Windows) or system info (Linux/macOS) `[wmi]` |
| `eventvwr` | System event viewer (Event Viewer / journalctl) `[eventlog, events]` |
| `shutdown` | Shut down / restart / log off the system `[poweroff, reboot]` |
| `setx` | Persistently set an environment variable |
| `clip` | Copy stdin or a file to the system clipboard `[clipboard, pbcopy, xclip]` |

## 🔐 Security & Encryption

| Command | Description |
|---|---|
| `encrypt` | Encrypt / decrypt files with a password (stdlib only) `[dec, decrypt]` |
| `passgen` | Strong password, passphrase and PIN generator `[pwgen, genpass]` |
| `uuid` | UUID v1/v4/v5 generator and short IDs `[uid, uuidgen]` |

## 👨‍💻 Development

| Command | Description |
|---|---|
| `git` | Git wrapper with colored UI: status, log, diff, branch, stash |
| `docker` | Docker wrapper with colored UI: ps, images, stats, logs |
| `pip` | System pip wrapper / shell mini-pip `[pip3]` |
| `pkg` | Mini-pip package manager `[terminalx-pip]` |
| `pyrepl` | Mini interactive Python REPL (built-in) `[python, py, repl, pyconsole]` |
| `debugger` | Step debugger for TerminalX scripts — breakpoints, watches `[dbg, dbg-script, debug]` |
| `newcmd` | Wizard: create a new command without editing shell code `[addcmd, mkcommand]` |
| `builder` | Builder mode — generate and manage your own shell modules `[build]` |
| `project` | Create and manage terminal projects `[proj]` |
| `envdetect` | Automatic environment detection and profile suggestion `[env-detect]` |

## ⏰ Automation & Scheduling

| Command | Description |
|---|---|
| `sched` | Built-in task scheduler — one-shot, interval, cron syntax `[scheduler, at]` |
| `cron2` | Readable crontab viewer and editor with explanations `[crontab2, crontab-pl, cron]` |
| `watch` | Automated jobs triggered by system events (files, disks, processes, network) `[watcher, on]` |
| `autostart` | Manage items loaded at startup — plugins, modules, commands `[astart]` |

## 🔌 Plugins & Extensibility

| Command | Description |
|---|---|
| `plugin` | Manage plugins — install, sandbox, signing, repository `[plugins-dir]` |
| `plug` | Quick plugin management: connect/disconnect/reconnect/list `[plg]` |
| `pluginpath` | Show or change the plugins directory `[plugpath]` |
| `integrate` | System integration: PATH, alias, symlink, desktop, autostart, context menu `[sysintegrate, install, setup]` |
| `portable` | Manage TerminalX portable mode `[portabl]` |
| `build` | Build standalone EXE with PyInstaller `[buildexe, makeexe]` |

## 🖥️ Server & Integration

| Command | Description |
|---|---|
| `serve` | REST API server on localhost (HTTP/JSON, OpenAPI schema) `[api, restapi, apiserver]` |
| `wss` | WebSocket server on localhost (RFC 6455) `[websocket, wsserver]` |
| `gui` | GUI backend over IPC socket (NDJSON) `[guiserver, ipc, backend]` |

## 🧘 Productivity & Fun

| Command | Description |
|---|---|
| `ai` | AI integration — questions, hints, command explanations `[ask]` |
| `translate` | Translate text or a file via AI (Claude/OpenAI/Ollama) `[trans, tlumacz]` |
| `weather` | ASCII weather in the terminal via wttr.in `[pogoda]` |
| `wset` | Set the default location for the weather command `[weather-set]` |
| `note` | Notes — add, browse, search, delete `[notes]` |
| `todo` | TODO task list with priorities and status `[task, tasks]` |
| `cb` | TerminalX internal clipboard — multi-slot, persistent `[cboard, cbuf]` |
| `qr` | QR code in the terminal (Unicode blocks or ASCII art) `[qrcode]` |
| `calc` | Math expression calculator `[math]` |
| `clock` | Live digital clock in the terminal `[zegar]` |
| `timer` | Stopwatch, countdown and alarm |

## 🎨 Configuration & Appearance

| Command | Description |
|---|---|
| `theme` | Switch / create / manage color themes `[motyw]` |
| `boxstyle` | Change UI frame style — single, round, double, heavy, ascii `[framestyle, box]` |
| `status` | Toggle or configure the shell status bar `[sb]` |
| `shortcuts` | Show all TerminalX keyboard shortcuts `[keys, hotkeys]` |
| `config` | Manage shell configuration — read, write, reset `[cfg, settings]` |
| `profile` | Manage TerminalX configuration profiles `[prof, profiles]` |
| `lang` | Manage the TerminalX interface language |
| `wizard` | Interactive TerminalX configuration wizard `[setup]` |
| `verbose` | Toggle verbose mode (echo commands before execution) `[verb]` |
| `debug` | Toggle shell debug mode — full execution trace `[dbg]` |
| `mode` | Online/offline mode `[network]` — *(also listed under Network)* |

## 🚑 Recovery, Logs & Info

| Command | Description |
|---|---|
| `recovery` | Recovery mode — diagnose and repair TerminalX `[safe, rescue]` |
| `crashlog` | View and manage shell crash reports `[crash, errors]` |
| `logs` | Advanced shell log viewer and exporter (JSON/CSV/HTML) `[log2]` |
| `logview` | Show the local shell log with filtering and levels `[log]` |
| `logtail` | Live log viewer (follow mode) `[logfollow, tailf]` |
| `logscan` | Scan a log file for errors/patterns `[logerr, logfilter]` |
| `logrotate` | Rotate a log file — archive old entries, free space `[rotatelog]` |
| `about` | Author, version, and license information `[info, credits]` |
| `version` | Show the TerminalX version and build date `[ver, --version, -V]` |
| `changelog` | TerminalX change history `[changes]` |
| `help` | Show all commands or detailed help for one `[?]` |
| `date` | Show or set the system date and time `[time]` |
| `deactivate` | Deactivate Python virtual environment (venv) |

---

<div align="center">

[🇬🇧 English](command.md) · [🇵🇱 Polski](command.pl.md)

</div>
