# Scrolly Telling – Map It

Eine kurze Scrolly-Telling-Sequenz als statische Website. Beim Scrollen wird der jeweils
nächste Frame grösser und deckender, der alte kleiner und transparenter — als Filmstreifen,
der sauber einrastet und bei dem sich die Frames nie überlagern.

## Inhalt

- `index.html` — die komplette Seite (Vanilla HTML/CSS/JS, kein Build-Schritt)
- `assets/frame1.png … frame4.png` — die vier Frame-Bilder (web-optimiert)

## Frames

1. Digital planen und kommunizieren
2. Das Leben vor Ort zeigen
3. Energieplanung zugänglich machen
4. Mitsprache ermöglichen

## Lokal ansehen

```bash
python3 -m http.server 8777
```

Dann `http://localhost:8777` öffnen.

## Verhalten

- Crossfade beim Scrollen (Skalierung + Deckkraft je nach Distanz zum aktiven Frame)
- Deckkraft-Böden: Bild 50 %, Text 30 % beim inaktiven Nachbarn
- Textgrösse konstant, nur die Position wandert; Text vertikal auf Bildmitte, fester
  Abstand zur rechten Bildkante
- Einrasten per CSS `scroll-snap`, konstanter Abstand zwischen den Frames (keine Überlappung)
- Weicher CSS-Kartenschatten für Frame 1–3
- Responsiv + `prefers-reduced-motion`
