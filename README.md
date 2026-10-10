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

## Empfohlenes Setup

Für das beste Zusammenspiel von Musik und Licht empfehlen wir drei Bausteine:

- **Ein eigener Router (oder Reise-Router) im Rack:** ein stabiles, eigenes Netz für den Licht-Rechner, den Art-Net-Node und das iPad. So bist du unabhängig vom WLAN der Location, das bei vollem Saal oft aussetzt. Den Licht-Rechner und den Node **per Kabel (LAN)** anschließen, das iPad per WLAN. Ein Mac ohne Netzwerkbuchse braucht dafür einen **USB-C-auf-LAN-Adapter**. Feste IP-Adressen für den Node vergeben (z. B. 192.168.2.50) und **nie die Broadcast-Adresse** des Netzes (meist die Endung .255) oder die Netzadresse (.0) verwenden.
- **Ein Audio-Interface für die Musikerkennung:** z. B. ein kleines USB-Interface am Booth- oder Rec-Ausgang des Mixers. Sitz Light erkennt daran Takt, Energie, Build-ups, Drops und Phrasen, auch ohne rekordbox. Den Pegel so einstellen, dass die Pegel-Ampel in Sitz Light grün zeigt. Bei Brummen ein Gerät mit Masse-Trennung (Ground-Lift oder DI-Box) dazwischen.
- **Ein Art-Net-Node** (Ethernet auf DMX) **oder ein galvanisch getrennter USB-DMX-Adapter** mit eigenem Prozessor (Enttec-DMX-USB-Pro-kompatibel). Der Node ist die robustere Wahl: Rechner und Lichtanlage sind elektrisch getrennt, das verhindert Brummen im Ton und schützt die Geräte. Am Node das Universe so einstellen, wie Sitz Light es unter DMX-Ausgabe anzeigt („am Node: Net · Subnet · Universe“).

**Empfohlene Taktquelle ist das Audio-Interface.** Die Anbindung an rekordbox über das Programm **rkbx_link** (eigenes Projekt, nicht Teil von Sitz Light) ist vorerst experimentell und wird später richtig eingebaut: <https://github.com/grufkork/rkbx_link>.

## Neu

### Version 0.6.0 (10.10.2026)

- Neu: Der **Auto-Director** fährt die Show selbst, passend zu Musikzustand, Energie und Phrasen. Eigener Bereich **Director** mit Übersicht (große BPM, Stimmung, Szene, Musikzustand, Phrase), Shows, Szenen, Regeln, Musik & Analyse und Momenten.
- Neu: eigene **Shows** und **Szenen** anlegen, kopieren, umbenennen, löschen und als Datei weitergeben; ein **Show-Assistent** stellt eine Show über sechs Fragen zusammen (Anlass, Farbwechsel, Strobe, Bewegung, Farben – auch die des Brautpaars –, Ruhe beim Essen).
- Neu: **Stimmung** Niedrig, Mittel, Hoch, Eskalation – wie schnell und wild die Show läuft, immer innerhalb der Sicherheitsgrenzen.
- Rund 75 Lichtbilder von ruhig bis schnell, neue Farbstimmungen (z. B. Champagner, Rosé, Sonnenuntergang, Neon). Moving Heads haben je Liedteil eine eigene, wiedererkennbare Bewegung – immer nur im selbst eingetragenen sicheren Bereich und erst nach Freigabe.
- **Takt viel stabiler:** Sitz Light rastet auf den Takt ein und hält ihn in ruhigen Stellen ohne Kick, statt auf das doppelte oder halbe Tempo zu springen. Anzeige „sicher / gehalten / unsicher“. Setzt der Beat aus, bleibt das Licht ruhig und steigt auf der nächsten 1 wieder ein.
- **Phrasen** aus dem Audio stabiler; Phrasen und Musikzustand auch **von Hand** (Knöpfe und Tasten). Sitz Light **lernt aus deinen Eingriffen** und passt die Erkennung schrittweise an deine Musik an; ein **Lernmodus** zeichnet dafür nur Analysewerte auf, keine Musik, nur lokal.
- **Live aufgeräumt:** großer Simulator, BPM, Director an/aus, Stimmung, Momente, Tempo der Effekte, dazu Master, **Blinder**, **Strobe**, **Laser** und **Blackout**. Strobe nur nach Freigabe und höchstens 3 Blitze pro Sekunde (schneller nur nach eigener Freigabe mit Warnhinweis). Laser nur für im Patch freigegebene Geräte, nach einer Rückfrage, gedrückt halten oder als Umschalter; geht bei Blackout, „Alle auf 0“, Verbindungsabbruch und Beenden sofort aus.
- **Ruhe-Look:** läuft keine Musik mehr, blendet das Licht sanft in ein ruhiges, warmes Bild und zurück.
- Pegel-Ampel, ruhigere Analyse-Anzeigen mit Rauschsperre; **Node prüfen** zeigt Name und Universe deines Art-Net-Nodes und erklärt falsche Adressen.
- **Mac:** Sitz Light fragt jetzt selbst nach dem Mikrofon-Zugriff für den Audio-Eingang (vorher kam auf manchen Macs keine Frage).
- Empfohlene Taktquelle ist jetzt der Audio-Eingang; die Anbindung an rekordbox über rkbx_link ist vorerst experimentell.
- Behoben: lange Kanalnamen sprengen die Fader-Karten nicht mehr.

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

## Als Nächstes geplant

- **Phrasen noch besser erkennen**: mit Aufnahmen aus dem Lernmodus an echten Sets nachschärfen.
- **rekordbox-Anbindung** über rkbx_link richtig einbauen und testen (bisher experimentell).
- **Takt noch genauer**: Licht-Verzögerung für alle Taktquellen mit Testblitz einstellen, Art-Net-Nodes im Netz auf Knopfdruck finden.
- **Bühnenplan**: Lampen auf einem Plan anordnen, Moving Heads auf die Tanzfläche einmessen und Bereiche sperren, in die nie geleuchtet wird.
- **Verfolgen**: Moving Heads folgen dem Finger auf dem Bühnenplan, zum Beispiel aufs Brautpaar beim Eröffnungstanz.
- **Auto-Director verfeinern**: Gobos und Prismen, Akzente als eigene Bausteine.
- **Live eingreifen**: eigener MIDI-Controller, Farbe und Szene auf Knopfdruck festhalten.
- **App für iPhone und iPad**: Bedienung als Fernbedienung im lokalen Netz.
- **Mehr Ausfallsicherheit**: Programmfenster startet nach einem Fehler neu, ohne dass die Show stoppt.
- **Später, optional**: 3D-Vorschau der Bühne, um Szenen ohne aufgebaute Lampen zu bauen.
