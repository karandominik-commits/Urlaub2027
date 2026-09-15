# Reiseplanung Thailand und Indonesien 2027

Statische Website, kein Build-Schritt nötig. Chart.js wird per CDN geladen. Alle Dateien liegen flach im Wurzelverzeichnis.

## Was jetzt zu tun ist

1. Die sieben HTML-Dateien sowie `style.css` und `placeholder.svg` im Repository ersetzen.
2. `files.zip` löschen, die Datei wird nicht gebraucht.
3. Unter Settings, Pages die Quelle auf Branch `main` und Ordner `/ (root)` stellen.
4. Nach ein bis zwei Minuten ist die Seite unter `https://karandominik-commits.github.io/Urlaub2027/` erreichbar.

## Bilder ergänzen

Die Unterkunftsseite erwartet je ein Foto, ebenfalls im Wurzelverzeichnis:

- `luna-nai-yang.jpg`
- `sands-khao-lak.jpg`
- `longtail-koh-phangan.jpg`
- `sandy-bay-koh-phangan.jpg`
- `bamboo-kingdom-ao-luek.jpg`
- `blu-monkey-khao-thong.jpg`

Fehlt eine Datei, zeigt die Seite automatisch `placeholder.svg`. Am besten eigene Fotos oder solche aus den Buchungsbestätigungen verwenden, Querformat, etwa 1200 mal 800 Pixel. Bilder von Hotelseiten direkt zu verlinken ist keine gute Idee, die Links brechen und die Rechte liegen beim Hotel.

## Datenschutz

Das Repository ist öffentlich, und GitHub Pages ist im kostenlosen Tarif ebenfalls immer öffentlich. Jeder mit dem Link kann die Seite sehen. Sie enthält deshalb bewusst keine Buchungsnummern, PINs, Geburtsdaten, Adressen, Telefonnummern oder Zahlungsdaten.

Die HTML-Dateien tragen ein `noindex`-Tag. Das hält seriöse Suchmaschinen fern, ist aber keine Zugangssperre.

Soll die Seite wirklich nicht öffentlich sein, gibt es zwei Wege: ein privates Repository mit GitHub Pages, was ein kostenpflichtiges Konto voraussetzt, oder ein Hoster wie Netlify oder Cloudflare Pages, wo sich ein Passwortschutz einrichten lässt.

## Aktualisieren

Alle Zahlen stehen direkt im HTML. Beim Ändern beachten:

- Die Gesamtsumme steht auf `index.html` und `kosten.html`.
- Das Tortendiagramm in `kosten.html` hat die Werte an zwei Stellen, in der Legende und im `data`-Array des Skripts. Der Divisor `23111` in der Tooltip-Funktion muss zur neuen Summe passen.
- Die Zahl der gebuchten und offenen Nächte steht auf `index.html` und `unterkuenfte.html`.
