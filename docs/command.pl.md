# 📖 TerminalX — Spis komend

[🇬🇧 English](command.md) · [🇵🇱 Polski](command.pl.md)

Wszystkie komendy dostępne w TerminalX v39.2, pogrupowane według kategorii. Aliasy podane w nawiasach. Szczegółowa pomoc: `help <komenda>` w powłoce.

---

## 🗂️ Nawigacja i katalogi

| Komenda | Opis |
|---|---|
| `pwd` | Wyświetl bieżący katalog roboczy (pełna ścieżka) |
| `cd` | Zmień bieżący katalog roboczy |
| `ls` | Wyświetl zawartość katalogu z kolorami, ikonami i sortowaniem `[dir]` |
| `tree` | Drzewo katalogów z kolorowaniem i filtrowaniem |
| `bm` | Zakładki katalogów — dodawaj, przeglądaj, skacz, usuń `[bookmark, bookmarks]` |
| `nav` | Interaktywna przeglądarka plików TUI `[fb, fm, browse, files]` |
| `fman` | Menedżer plików — kopiuj, przenoś, podglądaj, drzewo `[filemanager, files2]` |
| `txhome` | Przejdź do katalogu domowego TerminalX (TX_HOME) `[tx-home, cdhome]` |
| `txplugins` | Przejdź do katalogu wtyczek `[txplugins, cdplugins]` |
| `txmodules` | Przejdź do katalogu modułów `[txmodules, cdmodules]` |
| `txgui` | Przejdź do katalogu nakładki GUI TerminalX `[txgui, cdgui]` |
| `clear` | Wyczyść ekran terminala `[cls]` |

## 📄 Operacje na plikach

| Komenda | Opis |
|---|---|
| `touch` | Utwórz nowy plik lub zaktualizuj czas modyfikacji |
| `mkdir` | Utwórz katalog — obsługuje zagnieżdżone ścieżki (`-p`) `[md]` |
| `cp` | Skopiuj plik lub katalog `[copy]` |
| `mv` | Przenieś lub zmień nazwę pliku/katalogu `[move]` |
| `rm` | Usuń plik lub katalog (z opcjonalnym potwierdzeniem) `[del]` |
| `rmdir` | Usuń katalog rekurencyjnie wraz z zawartością `[rd]` |
| `rename` | Zmień nazwę pliku lub katalogu (obsługuje wzorce) `[ren]` |
| `archive` | Twórz i rozpakowuj archiwa `[tar, untar, unzip]` |
| `du` | Rozmiary katalogów i plików `[diskusage, dk]` |
| `stat` | Szczegółowe metadane pliku: rozmiar, daty, uprawnienia, inode |
| `attrib` | Atrybuty pliku — Windows attrib lub Linux stat `[attr]` |
| `finfo` | Pełne metadane pliku (typ, MIME, kodowanie, hashe, statystyki) `[fileinfo]` |
| `fsutil` | Narzędzia systemu plików (Windows fsutil / stat Linux) `[fileutil]` |
| `compact` | Kompresja NTFS (Windows) lub informacje o kompresji (Linux) `[compress-ntfs]` |
| `cipher` | Szyfrowanie EFS (Windows) / bezpieczne czyszczenie wolnego miejsca `[efs]` |

## 👁️ Podgląd i edycja plików

| Komenda | Opis |
|---|---|
| `cat` | Wyświetl zawartość pliku z podświetlaniem składni `[type, ccat]` |
| `head` | Pokaż pierwsze N linii pliku (domyślnie 10) |
| `tail` | Pokaż koniec pliku — tryb śledzenia na żywo (`-f`) |
| `nano` | Wbudowany edytor tekstu nano-lite z podświetlaniem składni `[edit, ed]` |
| `diff` | Porównaj dwa pliki (unified diff) `[compare, cmp]` |
| `diffview` | Porównaj dwa pliki z kolorowym wyjściem |
| `hexdump` | Podgląd pliku binarnego (hex + ASCII) z kolorowaniem `[xxd, hd, hexview]` |
| `highlight` | Podświetlanie składni plików — kod z kolorami ANSI |
| `wc` | Policz linie, słowa, znaki i bajty w pliku lub tekście `[wordcount, linecount]` |
| `encode` | Obsługa kodowań znaków: Unicode, ANSI, UTF-8, cp1250, naprawa mojibake `[charset]` |

## 🔍 Wyszukiwanie

| Komenda | Opis |
|---|---|
| `grep` | Przeszukuj pliki według wzorca — obsługuje wyrażenia regularne |
| `find` | Przeszukuj drzewo katalogów według nazwy, typu lub daty `[find2]` |
| `ff` | Szybkie wyszukiwanie plików w stylu fzf (rozmyte + interaktywne) `[fzf, fuzzy]` |

## 🧮 Tekst i przetwarzanie danych

| Komenda | Opis |
|---|---|
| `json` | Parser / formatowanie / walidacja JSON `[jsonformat, jsonlint, jsonpp]` |
| `jq` | Mini jq — zapytania JSON (stdlib, bez binarki jq) `[jsonquery]` |
| `jsonview` | Podgląd i filtrowanie JSON `[jv]` |
| `yaml` | Parser / formatowanie YAML (stdlib, bez pyyaml) `[yamlformat, yamllint, yamlpp]` |
| `csvplot` | Wykres słupkowy / liniowy danych CSV w terminalu `[plotcsv, csvgraph]` |
| `base64` | Kodowanie / dekodowanie Base64 `[b64, b64encode, b64decode]` |
| `hash` | Sumy kontrolne MD5, SHA1, SHA256, SHA512 |
| `wordfreq` | Analiza częstości słów w pliku lub tekście `[freqwords, topwords]` |
| `readability` | Analiza czytelności: indeksy Flesch, Fog, SMOG `[textstat, readable]` |

## 🐚 Rdzeń powłoki

| Komenda | Opis |
|---|---|
| `echo` | Wypisz tekst — obsługuje `$VAR` i sekwencje escape |
| `history` | Wyświetl i przeszukaj historię wykonanych komend |
| `alias` | Zarządzaj aliasami komend — dodawaj, listuj, zapisz |
| `unalias` | Usuń alias lub wszystkie aliasy naraz |
| `macro` | Makra i sekwencje komend `[mac, m]` |
| `set` | Wyświetl lub ustaw zmienne powłoki i opcje wykonania |
| `export` | Ustaw i wyeksportuj zmienną środowiskową dla procesów potomnych |
| `unset` | Usuń zmienną powłoki lub środowiska |
| `env` | Wyświetl środowisko lub uruchom komendę z własnym `[environ, environment]` |
| `envs` | Pokaż zmienne środowiskowe z filtrowaniem i sortowaniem `[env2, sysenv]` |
| `printenv` | Pokaż wartość zmiennej środowiskowej |
| `envdiff` | Porównaj zmienne środowiskowe: migawka vs stan bieżący `[envcompare]` |
| `source` | Wczytaj i wykonaj skrypt TerminalX (.msh / .rc) `[., exec-script, run-script]` |
| `for-loop` | Pętla FOR w TerminalX (odpowiednik CMD FOR) `[for, loop]` |
| `pysh` | Zarządzaj modułami .pysh (dynamiczne rozszerzenia powłoki) `[module]` |
| `session` | Zarządzaj sesjami TerminalX (w stylu tmux) `[ses, sessions]` |
| `split` | Pseudo podział ekranu — podziel terminal na panele `[sp]` |
| `tmux` | Skróty w stylu tmux do zarządzania sesjami i podziałami `[tx]` |
| `which` | Znajdź ścieżkę programu w PATH `[where]` |
| `start` | Uruchom program lub otwórz plik w nowym oknie/w tle |
| `call` | Uruchom plik wsadowy lub skrypt powłoki i wróć po zakończeniu `[bat, batch]` |
| `sudo` | Wykonaj komendę jako root lub przejdź w tryb root |
| `elevate` | Podnieś uprawnienia do administratora (UAC/sudo) `[runas, su]` |

## 🩺 Diagnostyka i monitorowanie systemu

| Komenda | Opis |
|---|---|
| `sysinfo` | Pełna diagnostyka: OS, CPU, RAM, dysk, sieć, Python `[info]` |
| `diag` | Diagnostyka systemu: CPU, RAM, dyski, sieć, procesy `[sysdiag]` |
| `sysmon` | Monitor systemu — CPU, RAM, swap, dysk, sieć, procesy `[htop-lite]` |
| `sysmon-quick` | Jednorazowa migawka zasobów (bez TUI) |
| `cpugraph` | Wykres CPU i RAM na żywo w terminalu (odświeżanie 1s) `[cgraph, cpumon]` |
| `procmon` | Monitor procesów — mini Menedżer zadań TUI `[top, procs, tasks]` |
| `resmon` | Monitor zasobów (Windows resmon / htop Linux) `[resource-monitor]` |
| `perfmon` | Monitor wydajności (Windows perfmon / vmstat-top Linux) `[perf, performance]` |
| `free` | Informacje o RAM i swap (cross-platform) `[meminfo]` |
| `df` | Informacje o miejscu na dysku — używane i wolne `[diskfree]` |
| `uptime` | Czas pracy systemu i średnie obciążenie |
| `uptime2` | Czas pracy + obciążenie + czas lokalny `[up]` |
| `uname` | Informacje o systemie — jądro, architektura, host |
| `hostname` | Wyświetl lub zmień nazwę hosta `[host, sysname]` |
| `id` | Pokaż UID, GID i grupy bieżącego użytkownika (Linux/macOS) `[uid]` |
| `whoami` | Pokaż nazwę bieżącego użytkownika (root/user) |
| `systeminfo` | Szczegółowe informacje o systemie: OS, CPU, RAM, sieć `[sysinfo-win]` |
| `selfcheck` | Testy wewnętrzne i autodiagnostyka TerminalX `[test, check, verify]` |
| `timeit` | Zmierz czas wykonania komendy powłoki `[benchmark, bench]` |

## ⚙️ Procesy i usługi

| Komenda | Opis |
|---|---|
| `ps` | Wyświetl procesy systemowe z filtrowaniem po nazwie i PID `[proc, procs-list]` |
| `ps2` | Lista procesów z filtrowaniem po nazwie / PID / użytkowniku `[tlist]` |
| `kill` | Zakończ proces po PID lub nazwie z wyborem sygnału `[killproc]` |
| `pkill2` | Zabij proces po nazwie lub PID (z potwierdzeniem) `[killp, tkill]` |
| `tasklist` | Wyświetl procesy systemowe (Windows tasklist / ps) |
| `taskkill` | Zakończ proces po PID lub nazwie (Windows taskkill) |
| `sc` | Zarządzaj usługami systemowymi (Windows sc / systemctl) `[service]` |
| `dxdiag` | Diagnostyka DirectX (Windows) / OpenGL/GPU (Linux) `[gpu-info, directx]` |

## 🌐 Sieć

| Komenda | Opis |
|---|---|
| `ping` | Test łączności (systemowy ping lub awaryjny TCP) |
| `traceroute` | Trasa pakietu do hosta `[tracert, trace, mtr]` |
| `pathping` | Połączone ping + traceroute |
| `netstat` | Statystyki sieci i aktywne połączenia `[nstat, connections]` |
| `netmon` | Monitor połączeń i interfejsów sieciowych `[monitor]` |
| `ipconfig` | Pokaż konfigurację sieci (Windows ipconfig / Linux ip) `[ifconfig]` |
| `dns` | Zapytania DNS: A, AAAA, PTR, MX, NS, ALL `[nslookup2, dig2]` |
| `whois` | Informacje WHOIS dla domeny lub adresu IP `[who-is, domaininfo]` |
| `arp` | Tabela ARP — adresy MAC/IP w sieci lokalnej `[arp-table]` |
| `portscan` | Wielowątkowy skaner portów TCP `[pscan]` |
| `net` | Komendy Windows NET (użytkownicy, grupy, usługi, udziały) `[net-cmd]` |
| `netsh` | Konfiguracja sieci Windows (netsh) lub ip/nmcli (Linux) `[netconfig]` |
| `ssh` | Połącz się z hostem przez SSH lub zarządzaj profilami połączeń `[ssh-connect]` |
| `mode` | Tryb online/offline — zarządzaj dostępem do sieci `[network, netmode]` |

## ⬇️ Pobieranie i HTTP

| Komenda | Opis |
|---|---|
| `curl` | Żądania HTTP/HTTPS — GET, POST, nagłówki, dane (stdlib) `[fetch, fetch-url]` |
| `http` | Klient HTTP (w stylu curl): GET/POST/HEAD/PUT/DELETE `[curl2]` |
| `wget` | Pobierz plik z adresu URL z paskiem postępu `[download]` |
| `apix` | Interaktywny eksplorator API — sesja z bazowym URL i nagłówkami `[apiexplorer]` |

## 🛠️ Administracja Windows

| Komenda | Opis |
|---|---|
| `reg` | Edytor rejestru Windows (tylko Windows) `[regedit-cli, registry]` |
| `sfc` | Skanowanie plików systemowych (Windows sfc / Linux debsums) `[scannow]` |
| `dism` | DISM — obsługa obrazu Windows `[repair-image]` |
| `chkdsk` | Sprawdź dysk pod kątem błędów — Windows chkdsk / Linux fsck `[checkdisk, fsck]` |
| `diskpart` | Zarządzaj dyskami i partycjami (diskpart / parted) `[partition-mgr]` |
| `format` | Sformatuj dysk / partycję `[fmt-disk]` |
| `bcdedit` | Konfiguracja bootloadera BCD Windows `[bootcfg]` |
| `schtasks` | Harmonizer zadań Windows (schtasks / cron Linux) `[scheduled-tasks]` |
| `gpupdate` | Aktualizacja zasad grupy `[group-policy]` |
| `powercfg` | Konfiguracja zasilania i raporty energii `[poweropts]` |
| `wmic` | Interfejs WMI (Windows) lub informacje o systemie (Linux/macOS) `[wmi]` |
| `eventvwr` | Podgląd zdarzeń systemowych (Podgląd zdarzeń / journalctl) `[eventlog, events]` |
| `shutdown` | Zamknij / zrestartuj / wyloguj system `[poweroff, reboot]` |
| `setx` | Trwale ustaw zmienną środowiskową |
| `clip` | Skopiuj stdin lub plik do schowka systemowego `[clipboard, pbcopy, xclip]` |

## 🔐 Bezpieczeństwo i szyfrowanie

| Komenda | Opis |
|---|---|
| `encrypt` | Szyfruj / odszyfruj pliki hasłem (tylko stdlib) `[dec, decrypt]` |
| `passgen` | Generator silnych haseł, fraz hasłowych i PIN `[pwgen, genpass]` |
| `uuid` | Generator UUID v1/v4/v5 i krótkich ID `[uid, uuidgen]` |

## 👨‍💻 Programowanie

| Komenda | Opis |
|---|---|
| `git` | Wrapper Git z kolorowym UI: status, log, diff, branch, stash |
| `docker` | Wrapper Docker z kolorowym UI: ps, images, stats, logs |
| `pip` | Wrapper systemowego pip / mini-pip powłoki `[pip3]` |
| `pkg` | Menedżer pakietów mini-pip `[terminalx-pip]` |
| `pyrepl` | Mini interaktywny REPL Pythona (wbudowany) `[python, py, repl, pyconsole]` |
| `debugger` | Debugger krokowy skryptów TerminalX — breakpointy, watche `[dbg, dbg-script, debug]` |
| `newcmd` | Kreator: utwórz nową komendę bez edycji kodu powłoki `[addcmd, mkcommand]` |
| `builder` | Tryb budowania — generuj i zarządzaj własnymi modułami powłoki `[build]` |
| `project` | Twórz i zarządzaj projektami terminalowymi polsoft.ITS `[proj]` |
| `envdetect` | Automatyczna detekcja środowiska i sugestia profilu `[env-detect]` |

## ⏰ Automatyzacja i planowanie

| Komenda | Opis |
|---|---|
| `sched` | Wbudowany harmonogram zadań — jednorazowe, interwałowe, składnia cron `[scheduler, at]` |
| `cron2` | Czytelny podgląd i edycja crontab z objaśnieniami `[crontab2, crontab-pl, cron]` |
| `watch` | Zadania automatyczne wyzwalane zdarzeniami systemowymi (pliki, dyski, procesy, sieć) `[watcher, on]` |
| `autostart` | Zarządzaj elementami ładowanymi przy starcie — wtyczki, moduły, komendy `[astart]` |

## 🔌 Wtyczki i rozszerzalność

| Komenda | Opis |
|---|---|
| `plugin` | Zarządzaj wtyczkami — instalacja, sandbox, podpisy, repozytorium `[plugins-dir]` |
| `plug` | Szybkie zarządzanie wtyczkami: connect/disconnect/reconnect/list `[plg]` |
| `pluginpath` | Wyświetl lub zmień katalog wtyczek `[plugpath]` |
| `integrate` | Integracja z systemem: PATH, alias, symlink, pulpit, autostart, menu kontekstowe `[sysintegrate, install, setup]` |
| `portable` | Zarządzaj trybem przenośnym TerminalX `[portabl]` |
| `build` | Zbuduj samodzielny EXE z PyInstaller `[buildexe, makeexe]` |

## 🖥️ Serwer i integracja

| Komenda | Opis |
|---|---|
| `serve` | Serwer REST API na localhost (HTTP/JSON, schemat OpenAPI) `[api, restapi, apiserver]` |
| `wss` | Serwer WebSocket na localhost (RFC 6455) `[websocket, wsserver]` |
| `gui` | Backend GUI przez gniazdo IPC (NDJSON) `[guiserver, ipc, backend]` |

## 🧘 Produktywność i rozrywka

| Komenda | Opis |
|---|---|
| `ai` | Integracja AI — pytania, podpowiedzi, wyjaśnienia komend `[ask]` |
| `translate` | Przetłumacz tekst lub plik przez AI (Claude/OpenAI/Ollama) `[trans, tlumacz]` |
| `weather` | Pogoda ASCII w terminalu przez wttr.in `[pogoda]` |
| `wset` | Ustaw domyślną lokalizację dla komendy pogody `[weather-set]` |
| `note` | Notatki — dodawaj, przeglądaj, szukaj, usuń `[notes]` |
| `todo` | Lista zadań TODO z priorytetami i statusem `[task, tasks]` |
| `cb` | Wewnętrzny schowek TerminalX — wieloslotowy, trwały `[cboard, cbuf]` |
| `qr` | Kod QR w terminalu (bloki Unicode lub grafika ASCII) `[qrcode]` |
| `calc` | Kalkulator wyrażeń matematycznych `[math]` |
| `clock` | Żywy zegar cyfrowy w terminalu `[zegar]` |
| `timer` | Stoper, odliczanie i budzik |

## 🎨 Konfiguracja i wygląd

| Komenda | Opis |
|---|---|
| `theme` | Przełącz / twórz / zarządzaj motywami kolorów `[motyw]` |
| `boxstyle` | Zmień styl ramek UI — single, round, double, heavy, ascii `[framestyle, box]` |
| `status` | Przełącz lub skonfiguruj pasek statusu powłoki `[sb]` |
| `shortcuts` | Pokaż wszystkie skróty klawiszowe TerminalX `[keys, hotkeys]` |
| `config` | Zarządzaj konfiguracją powłoki — odczyt, zapis, reset `[cfg, settings]` |
| `profile` | Zarządzaj profilami konfiguracji TerminalX `[prof, profiles]` |
| `lang` | Zarządzaj językiem interfejsu TerminalX |
| `wizard` | Interaktywny kreator konfiguracji TerminalX `[setup]` |
| `verbose` | Przełącz tryb rozwlekły (echo komend przed wykonaniem) `[verb]` |
| `debug` | Przełącz tryb debugowania powłoki — pełny ślad wykonania `[dbg]` |

## 🚑 Odzyskiwanie, logi i informacje

| Komenda | Opis |
|---|---|
| `recovery` | Tryb odzyskiwania — diagnoza i naprawa TerminalX `[safe, rescue]` |
| `crashlog` | Przeglądaj i zarządzaj raportami awarii powłoki `[crash, errors]` |
| `logs` | Zaawansowany podgląd i eksport logów powłoki (JSON/CSV/HTML) `[log2]` |
| `logview` | Pokaż lokalny log powłoki z filtrowaniem i poziomami `[log]` |
| `logtail` | Żywy podgląd logów (tryb śledzenia) `[logfollow, tailf]` |
| `logscan` | Przeskanuj plik log pod kątem błędów/wzorców `[logerr, logfilter]` |
| `logrotate` | Rotuj plik log — archiwizuj stare wpisy, zwolnij miejsce `[rotatelog]` |
| `about` | Informacje o autorze, wersji i licencji `[info, credits]` |
| `version` | Pokaż wersję TerminalX i datę builda `[ver, --version, -V]` |
| `changelog` | Historia zmian TerminalX `[changes]` |
| `help` | Pokaż wszystkie komendy lub szczegółową pomoc dla jednej `[?]` |
| `date` | Wyświetl lub ustaw datę i czas systemowy `[time]` |
| `deactivate` | Dezaktywuj wirtualne środowisko Python (venv) |

---

<div align="center">

[🇬🇧 English](command.md) · [🇵🇱 Polski](command.pl.md)

</div>
