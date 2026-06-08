# 🧱 MathBuilder — Mathe-Spiel

iPad-freundliches Mathe-Übungsspiel für dein Kind.
Gebaut mit Python + Flask. Kein Internet nach dem Setup nötig.

---

## 🚀 Setup (einmalig)

### Schritt 1 — Python installieren
Falls noch nicht installiert: https://python.org/downloads

### Schritt 2 — Flask installieren
Terminal / Eingabeaufforderung öffnen:
```
pip install flask
```

### Schritt 3 — App starten
In diesen Ordner navigieren, dann:
```
python app.py
```

Du siehst dann:
```
* Running on http://0.0.0.0:5000
```

### Schritt 4 — Auf dem iPad öffnen
Safari öffnen und eingeben:
```
http://DEINE_PC_IP:5000
```

**PC IP-Adresse finden:**
- Windows: Eingabeaufforderung → `ipconfig` → IPv4-Adresse
- Mac: Systemeinstellungen → Netzwerk → WLAN → IP-Adresse

Beispiel: `http://192.168.1.42:5000`

> PC und iPad müssen im gleichen WLAN sein!

---

## 🎮 Features

- **5 automatische Level** — steigen automatisch bei 80% Genauigkeit
  - Level 1: Einmaleins 1×1 bis 10×10 + einfache Division
  - Level 2: Zweistellig × Einstellig (Stellenwert-Raster)
  - Level 3: Zweistellig × Zweistellig (volles Raster, Farbhighlighting)
  - Level 4: Schriftliche Division exakt (2-3-stellig ÷ 1-2-stellig)
  - Level 5: Division mit Rest
- **3 Persönlichkeiten:** Mutig 🦁 / Zauberer 🧙 / Künstlerin 🎨
- **2 Modi:** Mit Hilfe (Hinweise + Streak −2) / Ohne Gnade (Streak reset)
- **Dreistufige Hints:** 0–10s nichts, 10–20s Aufgabe, 20s+ Aufgabe + Ergebnis + Tipp
- **Farbhighlighting:** Aktive Ziffern leuchten orange/cyan auf
- **Konfetti** bei jedem Baustein 🎉
- **Sprachausgabe** via Web Speech API (kein API-Key nötig)

---

## 📁 Dateistruktur

```
mathbuilder/
├── app.py              ← 8 Zeilen Flask (für die ältere Tochter lesbar!)
├── requirements.txt    ← nur "flask"
├── README.md           ← diese Datei
└── templates/
    └── index.html      ← das ganze Spiel (HTML + CSS + JS)
```

---

## 🔧 Für die ältere Tochter (Coden lernen)

Der Code ist absichtlich lesbar strukturiert:
- `app.py` — 8 Zeilen. Zeigt wie Flask eine Webseite ausliefert.
- `templates/index.html` — das ganze Spiel in einer Datei:
  - HTML: Bildschirme und UI-Elemente
  - CSS: alle visuellen Styles
  - JavaScript: Spiellogik, Fragen, Sprachausgabe

**Übungsaufgaben:**
1. Eine neue Persönlichkeit hinzufügen (CW-Objekt kopieren)
2. Einen neuen Multiplikations-Hint schreiben (hint1 Funktion)
3. Die Weltfarben für einen neuen Art-Style ändern
4. Einen Session-Highscore hinzufügen (localStorage)
