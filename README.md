# Sitz Light – Downloads

Sitz Light ist eine Lichtsoftware für mobile DJs: Ein Auto-Director fährt eine
beat-synchrone Lichtshow, du wählst nur Stimmung und Intensität und greifst bei
Bedarf live ein. Bedienung am Rechner, im Browser und am iPad/iPhone.

> **Proprietäre Software. © Markus Sitzmann, alle Rechte vorbehalten.**
> Dieses Repository enthält ausschließlich fertige Installer, Signaturen und
> Versionsinformationen für die automatische Update-Funktion. Es enthält keinen
> Quellcode. Die Nutzung, Weitergabe, Veränderung oder Zerlegung der Software ist
> ohne ausdrückliche schriftliche Erlaubnis nicht gestattet.

## Unterstützte Systeme

| System | Voraussetzung |
|---|---|
| Windows | Windows 10 oder 11, 64 Bit |
| macOS (Apple Silicon) | ab macOS 12 Monterey, M1 oder neuer |
| macOS (Intel) | ab macOS 12 Monterey, z. B. MacBook Pro ab 2015 |
| iPad / iPhone / Browser | als Fernbedienung im selben Netz, Safari ab 15 |

## Download und Installation

Die aktuelle Version findest du unter **[Releases](../../releases/latest)**.
Testversionen sind dort als „Pre-release“ markiert.

- **Windows:** `…-windows-x64.msi` herunterladen und doppelklicken. Erscheint
  „Der Computer wurde durch Windows geschützt“, auf „Weitere Informationen“ →
  „Trotzdem ausführen“ klicken. Beim ersten Start den Netzwerkzugriff erlauben.
- **macOS:** `…-macos-apple-silicon.dmg` bzw. `…-macos-intel.dmg` öffnen und
  „Sitz Light“ in „Programme“ ziehen. Beim ersten Start unter Systemeinstellungen
  → Datenschutz & Sicherheit → „Dennoch öffnen“ klicken.
- **iPad, iPhone, Browser:** keine Installation nötig. Die Adresse bzw. den
  QR-Code zeigt Sitz Light am Rechner unter „System → Webzugriff“.

**Updates:** Sitz Light bietet neue Versionen selbst an, nie während einer laufenden
Show und nie im Gig-Modus. Jedes Update ist signiert und wird vor der Installation geprüft.

## Neu

### Version 0.5.0 (09.10.2026)

- Neu: die Gerätedatenbank mit über 2.200 Lampen bekannter Hersteller. Gerät suchen, Modus wählen, in den Patch übernehmen – ohne Kanäle von Hand einzutippen. Die Fader zeigen jetzt, was jeder Kanal tut (Dimmer, Rot, Pan …).
- Neu: eigene Geräte anlegen, Schritt für Schritt, auch am iPad. Ein ähnliches Gerät lässt sich als Vorlage kopieren; Profile lassen sich exportieren und importieren (auch QLC+-Dateien).
- Mehr Sicherheit: Eingebaute Laser bleiben aus, bis du sie für das einzelne Gerät freigibst. Reset und Automatikprogramme der Lampen werden nie versehentlich ausgelöst.
- Dein bisheriger Patch wird beim Update automatisch übernommen; die alte Datei bleibt als Sicherung erhalten.
- Den Kanal „Test“ gibt es jetzt auf allen Macs. Gibt es eine Testversion nur für Windows, bleibt dein Mac ohne Meldung auf seiner Version.
- Neu: Testmodus für jede Lampe. Kanal für Kanal durch die Wertebereiche fahren und mit der Anleitung vergleichen; Start und Ende immer mit dunklen Lampen.
- Neu: Sitz Light hört auf den Takt. Wählbar sind rkbx_link (Takt und Phrasen aus rekordbox), ein Audio-Eingang (z. B. dein Interface am Mixer) oder Tap. Fällt eine Quelle aus, übernimmt automatisch die nächste, und der Takt läuft weiter.
- Neu: Musikerkennung. Sitz Light zeigt, ob die Musik gerade ruhig ist, groovt, sich aufbaut, droppt oder im Breakdown ist, und warum. Dazu Tief, Mitte, Hoch und der Verlauf der letzten Beats.
- Neu: Test-Show auf den Beat. Helligkeit pulst, Farben wechseln je Takt, die LED-Bar läuft über ihre Segmente. Master und Blackout sind immer erreichbar; Moving Heads bewegen sich erst, wenn du es ausdrücklich einschaltest.
- Neu: Unter Looks stellst du ein, wie das Licht reagiert: nur auf den Takt oder je nach Musikzustand, mit eigener Helligkeit, Puls und Farbwechsel für jeden Zustand.
- Neu: Kanalübersicht unter Geräte → Adressen. Alle 512 Kanäle auf einen Blick, Geräte per Ziehen an eine neue Adresse verschieben; belegte Kanäle werden nie überschrieben.
- Der Audio-Eingang öffnet sich nie von selbst beim Start, nur wenn du ihn wählst. Verweigert das System den Zugriff, sagt Sitz Light, wo du ihn erlaubst.

### Version 0.4.0 (04.10.2026)

- Neue, aufgeräumte Oberfläche: oben die Bereiche Live, Geräte, Looks und Einstellungen, am Handy als große Reiter unten. Auf großen Bildschirmen wird jetzt die ganze Breite genutzt.
- Immer sichtbar oben rechts: Verbindung, Ausgabe AN/AUS, Tempo, „Update verfügbar“ und der Lizenzstatus. Ein Klick führt direkt zur passenden Einstellung.
- Lizenz: Einmal kaufen, für immer nutzen, alle Funktionen und alle künftigen Updates inklusive, kein Abo, kein Ablaufdatum, keine Konten. Die Lizenz wird offline geprüft und unterbricht nie eine laufende Show.
- Ohne Lizenz läuft Sitz Light als Demo: alle Funktionen nutzbar, echte DMX-Ausgabe 10 Minuten je Sitzung, danach blendet das Licht sanft aus. Rechtzeitige Hinweise am Rand, nie mitten im Bild.
- Updates werden schneller gemeldet, als kleiner Hinweis statt als Fenster. Installiert wird weiterhin nur nach Bestätigung am Licht-Rechner, nie während einer Show.
- Neu unter Einstellungen → Über und Leistung: die Neuigkeiten der letzten Versionen.

### Version 0.3.0 (04.10.2026)

- Leertaste = Tap: Das Tempo lässt sich jetzt per Tastatur klopfen, solange Sitz Light vorne ist. „?“ zeigt alle Tastenkürzel, die Belegung lässt sich ändern.
- Die Leistungsanzeige zeigt beim Lichttakt jetzt getrennt die gleichbleibende Verzögerung und die Schwankung.
- Gleichmäßigerer Lichttakt auf dem Mac: Das Licht kommt jetzt ohne die bisherige Verzögerung von rund 5 ms und schwankt kaum noch.
- Neue Taktprüfung unter „Erweitert“ für die Fehlersuche.
- Auf Macs mit Apple-Prozessor gibt es nur noch stabile Versionen.

## Als Nächstes geplant

- **Mehr Tastenkürzel**: Strobe, Blinder, Blackout und Stimmungen auf frei wählbaren Tasten (Tap per Leertaste gibt es schon).
- **Takt noch genauer**: Licht-Verzögerung für alle Taktquellen mit Testblitz einstellen, Art-Net-Nodes im Netz auf Knopfdruck finden.
- **Bühnenplan**: Lampen auf einem Plan anordnen, Moving Heads auf die Tanzfläche einmessen und Bereiche sperren, in die nie geleuchtet wird.
- **Verfolgen**: Moving Heads folgen dem Finger auf dem Bühnenplan, zum Beispiel aufs Brautpaar beim Eröffnungstanz.
- **Effekte und Auto-Director**: Die Show läuft von selbst passend zur Musik. Du wählst nur die Stimmung (Dinner, Eröffnungstanz, Party, Peak) und die Intensität.
- **Live eingreifen**: Farbe festhalten, Look halten, Strobe, Blinder und Blackout auf Knopfdruck.
- **App für iPhone und iPad**: Bedienung als Fernbedienung im lokalen Netz.
- **Später, optional**: 3D-Vorschau der Bühne, um Looks ohne aufgebaute Lampen zu bauen.
