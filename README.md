# Morse Training Station

An interactive Morse code trainer that runs entirely in a single HTML file — no build step, no dependencies, no server required.

## Features

### Four training modes

**Learn** — Browse the full Morse code library organized by category (alphabet, numbers, punctuation, prosigns, Q-codes, abbreviations). Tap any character to see its pattern, NATO phonetic name, a memory tip, and hear it played aloud.

**Receive** — Hear Morse code played through your speakers and identify the character. Multiple-choice answers for beginner levels, free-text input for advanced levels. Auto-advances on correct answers.

**Send** — Press and hold the spacebar (or tap the on-screen pad) to key in dots and dashes. Release under 150 ms for a dot, over 150 ms for a dash. Auto-submits 2 seconds after your last keypress.

**Reference** — Full lookup tables for the alphabet, numbers, punctuation, prosigns, Q-codes, and common ham radio abbreviations.

### Training options

- **6 receive levels** — L1: 6 common letters · L2: 14 letters · L3: digits · L4: words · L5: phrases · ADV: mixed
- **5 send levels** — same progression, single characters through phrases
- **WPM control** — 5–30 words per minute, adjustable mid-session
- **Farnsworth spacing** — extra gaps between characters to help beginners copy at full character speed
- **Visual flash mode** — LED-style flasher synced to the audio for visual learners
- **SOS mode** — one-tap drill on the international distress signal
- **Score, streak, and accuracy** tracked separately for receive and send
- **Progress persists** across sessions via `localStorage`
- **Dark / light theme** toggle

### Keyboard shortcuts (Receive tab)

| Key | Action |
|-----|--------|
| Letter key | Select that answer button |
| `R` | Replay current sequence |
| `Enter` / `Space` | Confirm "Got It" after a wrong answer |

### Keyboard shortcuts (Send tab)

| Key | Action |
|-----|--------|
| `Space` (hold) | Key a dot or dash |
| `Enter` | Submit immediately (skip the 2-second wait) |

## Usage

Open `morse_code_trainer.html` in any modern browser. No installation needed.

```
open morse_code_trainer.html      # macOS
start morse_code_trainer.html     # Windows
xdg-open morse_code_trainer.html  # Linux
```

Works offline. Mobile-friendly.

## Browser requirements

Web Audio API is required for sound (all evergreen browsers). Touch events are handled for mobile; passive event listeners are feature-detected automatically.

## File structure

```
morse_code_trainer.html   # entire app — HTML, CSS, and JavaScript in one file
```

## Morse code coverage

| Category | Count |
|----------|-------|
| Letters (A–Z) | 26 |
| Numbers (0–9) | 10 |
| Punctuation | 4 (`.` `,` `?` `/`) |
| Prosigns | 7 (AR, SK, BT, KN, AS, SOS, HH) |
| Q-codes | 12 (QRN, QRM, QRO, QRP, QRS, QRT, QRZ, QSB, QSL, QSO, QTH, QSY) |
| Abbreviations | 16 (73, 88, CQ, DE, K, R, PSE, TNX, UR, RST, FB, WX, OM, YL, DX, HI) |
