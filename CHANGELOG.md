# Changelog

## [Unreleased]
### Setup
- index.html aus Downloads in den Projektordner kopiert
- Sicherungskopie index.backup.html angelegt
- Git-Repo initialisiert, Branch `videos-einbauen`

## Videos eingebunden
- 10 Videos web-optimiert nach `videos/` (H.264, AAC, faststart, max 1080x1920, 30fps, CRF 23)
- Zweite Variante `videos-opt/` (CRF 26, 4 Mbit Cap) zum Größenvergleich
- Vorschaubilder (.jpg) je Video erzeugt, als poster-Attribut eingebunden
- VIDEOS-Array auf die 10 Pfade gesetzt
- CALENDLY_URL gesetzt: https://calendly.com/cavcalvinvisuals/30min
- INSTAGRAM_URL bleibt Platzhalter (auf Wunsch)
- Lokal getestet: 10/10 Karten laden, keine Konsolenfehler, Lightbox + Mobile-Swipe ok

## Anpassungen nach Feedback
- Encodes auf CRF 26 (4 Mbit Cap) umgestellt: 108 MB statt 187 MB
- "Muay Thai Edit" entfernt (jetzt 9 Videos)
- "Long form content intro" nach ganz oben, als breite 16:9-Karte über der vollen Breite
  - dafür in 1920x1080 neu encodiert (CRF 24), eigener Container #gridWide
  - neue Konstante QUERFORMAT steuert, welche Videos die breite Karte bekommen
- Poster-Bilder auf 640px (bzw. 1280px fürs Intro) verkleinert
- Getestet: 9/9 Karten laden, 0 Konsolenfehler, Lightbox mit Ton, Mobile-Swipe ohne Überlauf

## Reihenfolge angepasst
- Neu: Intro (breit) / Rasierer, Education, Clothingbrand / Möbel, Supplement, Superboncamp / Pizza, Rausch Shampoo
- Rausch Shampoo war in der Ansage nicht genannt und steht vorerst am Ende

## Überschriften unter den Videos
- VIDEOS-Array führt jetzt pro Eintrag { datei, titel }
- Jede Karte sitzt in einem .item-Wrapper mit .caption darunter
- Mobile: .item übernimmt Breite und Scroll-Snap, Schrift etwas kleiner

## Titel korrigiert und zwei Videos entfernt
- "UGC Ad · Gartenmöbel" -> "Brand Film · Gartenmöbel" (denova, cinematischer Markenfilm)
- "UGC Ad · Rasierer" -> "UGC Ad · Bartöl" (Produkt ist Mootes Beard Oil)
- "UGC Ad · Gastronomie" -> "UGC Ad · Pizza" (FREDA)
- Supplement Ad und Rausch Shampoo Ad komplett von der Seite entfernt
  Dateien liegen in videos/_nicht-verwendet/, Originale unberührt in "Performance Ads"
- Jetzt 7 Videos: Intro (breit) + 2 volle Reihen à 3

## Feinschliff
- Vollbild-Icon in der Kartenecke entfernt (Klick auf die Karte öffnet weiterhin die Lightbox)
- Überschriften stehen jetzt über dem Video statt darunter
- Hero-Überschrift ohne Gedankenstrich: "Videos, die nicht nur gut aussehen sondern auch performen."

## Weitere Anpassungen
- Statistik: 100+ -> 500+ Videos geschnitten
- Sektionstitel: "Ausgewählte Arbeiten" -> "Meine Kundenprojekte"
- Querformat-Video sitzt jetzt mittig zwischen den Hochformaten (3 / breit / 3)
  statt in einem eigenen Container darüber; .item.wide nutzt grid-column: 1 / -1

## Über-mich-Bereich neu
- "ÜBER MICH" wird nicht mehr in Versalien gesetzt: neue Klasse .eyebrow.normal
- Neuer Intro-Absatz plus 5 Erfahrungsbereiche (.bereiche / .bereich)
  Performance Marketing, Personal Brands & YouTube, Business Consulting,
  Clubs & Events, Motion Design
- Tags ersetzt: Hooks & Retention, Personal Branding, Performance Ads,
  Motion Design, Brand-Look, Short-Form

## Hero neu
- Headline: "Mehr als ein Cutter."
- Neuer Untertext zu Marke, Zeitgeist und Algorithmus ersetzt die alte Selbstvorstellung

## Keywords im Hero hervorgehoben
- Neue Klasse .hl in der Akzentfarbe (identisch mit dem Button-Orange)
- Hervorgehoben: Editor / Zeitgeist versteht / ästhetische Videos /
  Menschen bewegt / echte Verbindungen / Algorithmus für dich arbeiten lässt
