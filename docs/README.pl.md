<div align="center">

# 🖥️ TerminalX

**Powłoka terminalowa w jednym pliku Pythona — 196+ wbudowanych komend, menedżer plików TUI, system wtyczek, serwer REST/WebSocket i autodiagnostyka. Zero zewnętrznych zależności.**

[🇬🇧 English](../README.md) · [🇵🇱 Polski](README.pl.md)

![Wersja](https://img.shields.io/badge/wersja-39.2-blue)
![Python](https://img.shields.io/badge/python-3.10%2B-informational)
![Zależności](https://img.shields.io/badge/zależności-0-success)
![Licencja](https://img.shields.io/badge/licencja-własna-lightgrey)

</div>

---

## ✨ Co to jest TerminalX?

TerminalX to **kompletne środowisko powłoki w jednym pliku Pythona** (`TerminalX.py`, ~1,9 MB). Działa jako zamiennik / uzupełnienie cmd, PowerShell czy bash i działa na **Windows, Linux i macOS** wyłącznie z biblioteką standardową.

```bash
python TerminalX.py
```

## 🌟 Wyróżniające się funkcje

### 🧩 System wtyczek (API v2.0)
- Ładowanie / wyładowanie / ponowne łączenie wtyczek w trakcie działania (`plugin list|info|connect|disconnect`, `plug`)
- **Piaskownica (sandbox)** z konfigurowalnymi poziomami bezpieczeństwa i statycznym skanowaniem kodu
- **Baza zaufania** — wtyczki są hashowane i podpisywane (`_plugin_sign` / `_plugin_verify`)
- Zdalne **repozytoria wtyczek** z wyszukiwaniem i instalacją
- Szablony przez `pkg create` i `builder`

### 🌐 Wbudowany stos serwerów sieciowych
Jedno polecenie `serve` uruchamia całą powierzchnię API:
- **REST API v1/v2/v3** z automatycznie generowanym **schematem OpenAPI**
- **Serwer WebSocket** z pełnym handshake i protokołem ramek oraz rozsyłaniem zdarzeń
- **Server-Sent Events (SSE)** — strumień zdarzeń powłoki
- **Panel Web GUI** — kolorowane wyjście ANSI renderowane w przeglądarce
- **Tryb demona** z autoryzacją tokenem, **rate limiting** i **webhookami** (wywoływane na zdarzeniach powłoki)

### 🛟 Tryb odzyskiwania po awarii
Jeśli start się nie powiedzie (uszkodzony config, historia, wtyczka), TerminalX przechodzi do **powłoki recovery**, która:
- diagnozuje terminal, config, aliasy, historię i wtyczki
- oferuje **inteligentne naprawy** każdego podsystemu jednym klawiszem
- tworzy i przywraca **kopie zapasowe konfiguracji**
- blokuje komendy, które powodowały awarię

### ✅ Autodiagnostyka — `selfcheck`
Wbudowany zestaw testów: **ponad 100 sprawdzeń** w kategoriach: tokenizer, config, system plików, historia, aliasy, wtyczki, terminal, obsługa awarii, sieć, benchmarki wydajności, integralność, wersje, schemat konfiguracji, zasoby, składnia, komendy. Uruchom `selfcheck` i otrzymaj kolorowy raport z czasami wykonania.

### 🖼️ Pełny zestaw TUI (curses)
- `nav` — interaktywny menedżer plików (podgląd, filtrowanie, sortowanie, uprawnienia, breadcrumbs)
- `tui` — menu główne
- `procmon` — interaktywny monitor procesów
- `logtail` / `logview` — podgląd i śledzenie logów na żywo
- `fman`, `nano` — menedżer plików i wbudowany **edytor w stylu nano**

### 🤖 AI i produktywność
- `ai` — rozmowa z LLM (streaming, konfigurowalny dostawca) prosto z powłoki
- `translate` — tłumaczenia, `weather` — rozbudowany panel pogodowy z grafiką ASCII, indeksem UV, skalą Beauforta, strzałkami wiatru
- `note`, `todo`, `bm` (zakładki), `cb` (schowek wieloslotowy), `calc`, `qr`, `passgen`, `uuid`, `encrypt`

### 🧠 Inteligentny rdzeń powłoki
- **Potoki, przekierowania, `&&`/`||`, rozwijanie zmiennych** — własny tokenizer/parser
- Uzupełnianie Tab (ścieżki, komendy, wartości configu), interaktywne wyszukiwanie historii **Ctrl+R**
- Aliasay, makra (`macro`), historia sesji z deduplikacją i znacznikami czasu
- **Profile** (`profile list|switch|create|diff|export...`) z automatyczną sugestią środowiska (`envdetect`)
- **Sesje i podział ekranu** (`session`, `split`, w stylu `tmux`)

### ⏰ Automatyzacja
- `sched` — harmonogram: zadania jednorazowe, interwałowe i w **pełnej składni cron** z logami
- `watch` — reguły zdarzeń: uruchamiaj komendy przy **zmianach plików/katalogów, dysków, procesów lub interfejsów sieciowych**
- `cron2` — podgląd/walidacja crontab z ludzkim objaśnieniem pól
- `autostart` — zarządzanie wpisami startowymi (komendy, wtyczki)
- Webhooki i hooki zdarzeń po każdej komendzie

### 🧰 196+ wbudowanych komend
- **Operacje na plikach:** `ls cd pwd cat touch mkdir rm cp mv tree du stat head tail diff chmod chown`
- **Wyszukiwanie:** `grep find ff` (fuzzy-finder z interaktywnym wyborem)
- **Tekst/dane:** `json jq yaml wc wordfreq readability base64 hexdump csvplot highlight` (podświetlanie składni wielu języków)
- **System:** `sysinfo diag ps ps2 kill pkill2 tasklist taskkill free df uptime cpugraph sysmon netmon portscan`
- **Sieć:** `ping traceroute netstat wget curl ipconfig dns whois http ssh net arp`
- **Administracja Windows:** `sfc dism chkdsk bcdedit reg diskpart schtasks gpupdate cipher eventvwr` ... (z ochroną root/UAC)
- **Deweloperskie:** `git docker pip envdiff pyrepl debug` (mini debugger Pythona), `timeit`
- **Warstwa kompatybilności z cmd** — komendy w stylu Windows działają też na Linux/macOS

### 🔌 Integracja z systemem — `integrate`
Zainstaluj TerminalX w systemie jednym krokiem:
- dodanie do **PATH**, tworzenie **symlinków**, **skrótu na pulpicie**, **autostartu**
- rejestracja jako **powłoka** w `/etc/shells`
- **obsługa typów plików** (otwieranie rozszerzeń przez TerminalX), wpisy w **menu kontekstowym** (Windows/Linux/macOS)
- **demon drag & drop** — upuść pliki na cel na pulpicie, by przetworzyć je w powłoce

### 🛡️ Bezpieczeństwo i jakość
- Brak telemetrii — **na stałe wyłączona**, weryfikowana przez selfcheck
- Ochrona root/sudo przed niebezpiecznymi operacjami
- Logi awarii (`crashlog`), buforowany zapis logów z rotacją (`logrotate`, `logscan`, `logs` z eksportem JSON/CSV/HTML)
- Tryb przenośny (`portable`, `--data`, `--plugins`), respektuje **NO_COLOR** / `TERM=dumb`
- `build_exe` — pakietowanie samego siebie do samodzielnego pliku wykonywalnego

### 🌍 i18n
Pełne tłumaczenia **polski i angielski** (`lang/pl.json`, `lang/en.json`) plus automatyczna mapa wiadomości — przełącz w każdej chwili: `lang pl|en`. Pierwsze uruchomienie oferuje **kreator konfiguracji** (`wizard`).

## 📦 Wymagania

- **Python 3.10+** (weryfikowane przy starcie)
- **Zero zależności pip** — wszystko z biblioteki standardowej
- Opcjonalnie: `curses` (dołączony do Pythona na Linux/macOS; włącza pełne TUI)

## 🚀 Szybki start

```bash
# uruchom powłokę
python TerminalX.py

# rozejrzyj się
help            # lista komend
tui             # menu interaktywne
sysinfo         # panel systemowy
selfcheck       # uruchom 100+ wewnętrznych testów
serve           # uruchom panel REST/WS/SSE
wizard          # kreator konfiguracji przy pierwszym starcie
```

### Przydatne zmienne środowiskowe

| Zmienna | Cel |
|---|---|
| `TERMINALX_OFFLINE` | wymuś tryb offline (bez detekcji sieci) |
| `TERMINALX_NO_COLOR` / `NO_COLOR` | wyłącz kolory ANSI |
| `TERMINALX_RC` | niestandardowa ścieżka pliku rc |
| `TERMINALX_CONFIG` | niestandardowa ścieżka configu |
| `TERMINALX_PROFILE` | start z podanym profilem |
| `TERMINALX_THEME` | motyw startowy (`dark` / `light` + własne) |
| `TERMINALX_PLUGINS` | niestandardowy katalog wtyczek |
| `TERMINALX_VERBOSE` / `TERMINALX_DEBUG` | tryb rozwlekły/debug |

## 🗂️ Układ danych

TerminalX trzyma cały stan w swoim katalogu domowym (przyjazny tryb przenośny): `config`, `history`, `aliases`, `lang/`, wtyczki, baza pakietów, baza zaufania, sesje, stan harmonogramu i watch, logi i logi awarii.

## 📄 Licencja

Pełny tekst licencji znajdziesz wewnątrz powłoki: komenda `about` / `license`.

---

<div align="center">

[🇬🇧 English](../README.md) · [🇵🇱 Polski](README.pl.md)

</div>
