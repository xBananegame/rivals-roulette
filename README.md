# Rivals Roulette

Fan-Tool für **Marvel Rivals** (DE/EN): Glücksrad für zufällige Charaktere, StratRoulette mit Bibliothek und ein "Guess the Character"-Ratespiel.

**Fan-Projekt – nicht mit NetEase Games oder Marvel verbunden.**

## Features

- **Random Charakter** – alle 51 Helden (Stand Season 8.5, Juni 2026) im Glücksrad, wahlweise nach Rollen gruppiert ("Einfach") oder durchgemischt ("Gemischt"). Helden lassen sich fürs nächste Drehen auslassen und per Klick oder "Zurücksetzen" zurückholen.
- **StratRoulette** – zieht eine zufällige Team-Strategie; alle Strats sind zusätzlich in der Bibliothek nachlesbar.
- **Guess the Character** – ein geheimer Held wird gezogen; über Geschlecht, Spezies, Zugehörigkeit, Rolle, Reichweite und HP rätst du dich heran (Grün = richtig, Gelb = teilweise/nah dran, Rot = falsch).
- Zweisprachig (Deutsch/Englisch, umschaltbar oben rechts), Sound-Effekte (abschaltbar), responsiv für Desktop und Handy.

## Nutzung

Einfach `index.html` im Browser öffnen – keine Installation, kein Build, keine Abhängigkeiten.

## Charakterbilder einfügen

Die Seite sucht Bilder automatisch im Ordner `img/` anhand des Heldennamens. Fehlt ein Bild, wird stattdessen eine Initialen-Kachel in der Rollenfarbe angezeigt – die Seite funktioniert also auch ganz ohne Bilder.

1. Bilddateien als **PNG** in den Ordner `img/` legen.
2. Dateinamen exakt wie in [`img/README.md`](img/README.md) benennen (z. B. `img/spider-man.png`).
3. Fertig – beim nächsten Laden erscheinen die Bilder im Glücksrad-Ergebnis, in der Suche und im Ratespiel.

Am besten funktionieren quadratische Bilder oder Portraits (sie werden oben-mittig zugeschnitten).

**Wichtiger Hinweis:** Die offiziellen Charakter-Artworks gehören NetEase Games/Marvel. Dieses Repository enthält deshalb keine Spielgrafiken. Ob und welche Bilder du in deiner eigenen (privaten) Kopie hinterlegst, liegt in deiner Verantwortung.

## Auf GitHub veröffentlichen (GitHub Pages)

```bash
git init
git add .
git commit -m "Rivals Roulette"
git branch -M main
git remote add origin https://github.com/DEIN-NAME/rivals-roulette.git
git push -u origin main
```

Danach im Repository unter **Settings → Pages** als Source "Deploy from a branch" wählen, Branch `main` und Ordner `/ (root)`. Nach ein paar Minuten ist die Seite unter `https://DEIN-NAME.github.io/rivals-roulette/` erreichbar – inklusive der Bilder aus `img/`.

## Inhalte anpassen

Alles liegt in `index.html`:

- **Helden**: Array `HEROES` – Kurztexte (`i.de` / `i.en`), Guess-Attribute (`g`, `sp`, `af`, `rg`, `hp`) und optional ein eigener Bildpfad (`img:"..."`).
- **Strategien**: Array `STRATS` – Titel und Beschreibung jeweils auf Deutsch und Englisch, optional eine Heldenliste (`h`).
- **Übersetzungen der Oberfläche**: Objekt `UI`.

Die HP-Werte sind ca.-Angaben und können sich mit Balance-Patches ändern.
