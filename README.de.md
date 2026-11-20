# BowerFS

[English](README.md) | Deutsch | [Українська](README.uk.md)

Ein Windows-Dateimanager für große Bild- und Videobibliotheken. Vollständig offline: kein Internet,
keine Telemetrie, kein Konto. Idee: Mariia Mashura. Technische Umsetzung: Claude (Anthropic).

## Download

Laden Sie `BowerFS-<Version>-win64.zip` von der Seite **Releases** dieses Repositorys, entpacken Sie
es in einen beliebigen Ordner (auch ein USB-Stick geht) und starten Sie `BowerFS.exe`. Es gibt
keinen Installer und es wird nichts in die Registry geschrieben. Windows 10 und 11, 64 Bit.

Download prüfen: Die SHA-256-Summe des Archivs steht in `SHA256SUMS.txt`.

```powershell
Get-FileHash BowerFS-<Version>-win64.zip -Algorithm SHA256
```

## Erster Start

1. Das Programm fragt, wo es seine Daten ablegen soll (Datenbank, Miniaturbild-Cache, Logs).
   Standard ist `Dokumente\BowerFS`. Später lässt sich der Ordner unter *Extras → Einstellungen*
   verschieben.
2. Windows SmartScreen meldet evtl. eine unbekannte App, weil das Programm nicht signiert ist:
   *Weitere Informationen → Trotzdem ausführen*.
3. Lässt sich eine Datei nicht umbenennen oder löschen („Zugriff verweigert“), obwohl sie nicht
   schreibgeschützt ist, blockiert ein Antivirenprogramm (z. B. AVG) oder der „Überwachte
   Ordnerzugriff“ von Windows das unbekannte Programm. Fügen Sie `BowerFS.exe` zu den erlaubten
   Programmen hinzu.

## Funktionen

- Bis zu vier Fenster (zwei oben, zwei unten) mit Tabs; Ordnerbaum, Favoriten, Tags.
- Vorschau für Bilder (JPG, PNG, WebP, GIF, TIFF, BMP, HEIC, RAW, PSD, SVG), Video, Audio, PDF,
  DOCX, XLSX, Text und Code, Archive (ZIP, 7z), Schriften und 3D-Modelle (STL, OBJ, PLY, GLB, glTF).
- Suche nach exakten Duplikaten per Inhalt, mit Vorschau nebeneinander; Duplikate kommen in den Papierkorb.
- Kopieren, Verschieben, Umbenennen und Stapel-Umbenennung mit Vorschau jeder Änderung,
  Protokoll der Vorgänge und Rückgängig.
- Zwei Dateien vergleichen: nebeneinander, überblendet, als Differenz oder im Wechsel.
- Drag and drop zwischen Fenstern und zum bzw. vom Windows-Explorer.
- Oberfläche auf Englisch, Deutsch und Ukrainisch, helles und dunkles Design, anpassbare Tastenkürzel.

Auf Laufwerken ohne Papierkorb (Netzwerk, USB) wird endgültig gelöscht; deshalb fragt das Programm
dort zweimal.

## Tastenkürzel

F3 Vorschau, F5 kopieren, F6 verschieben, F2 umbenennen, Strg+M Stapel-Umbenennung,
F8 / Entf in den Papierkorb, F9 vergleichen, Strg+D Duplikate, Strg+Z rückgängig,
Strg+T / Strg+W neuer / schließen Tab, Strg+Umschalt+N weiteres Fenster, Tab nächstes Fenster,
F1 Info. Alle lassen sich in den Einstellungen ändern.

## Optionale Werkzeuge

Legen Sie `ffmpeg.exe` und `ffprobe.exe` in den Ordner `tools` neben `BowerFS.exe`, für
Videominiaturen und Bildfolgen (sonst Suche im PATH). Sie sind nicht enthalten.

## Datenschutz

BowerFS baut keine Netzwerkverbindungen auf. Ihre Dateien werden nur durch Vorgänge verändert, die
Sie bestätigen. Tags und Index liegen im gewählten Datenordner.

## Lizenz

Siehe [LICENSE.txt](LICENSE.txt) und [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
Der Quellcode liegt in einem privaten Repository.

## Probleme und Wünsche

Eröffnen Sie ein Issue auf dieser Seite. Bitte keine privaten Fotos anhängen und die Logdatei
`logs\bowerfs.log` im Datenordner vor dem Anhängen prüfen.
