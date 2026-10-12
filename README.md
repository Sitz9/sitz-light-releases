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

### Version 0.7.0 (12.10.2026)

- **Takt läuft nicht mehr davon:** Das Tempo bleibt immer im eingestellten Bereich und ändert sich nur noch in kleinen Schritten. Rastet es einmal falsch ein, merkt Sitz Light das selbst und fängt sich kontrolliert neu. Abgestimmt an rund 50 echten Songs von House über Schlager bis Hypertechno; doppeltes oder halbes Tempo kommt kaum noch vor, auch nicht in Breakdowns.
- **Tap hat immer Vorrang:** Ein Tipp setzt sofort die „1“, ab dem zweiten zählt dein Tempo. Die Audio-Analyse richtet sich danach aus und übernimmt erst wieder, wenn sie 8 Takte lang zustimmt, ohne Sprung. Mit **T** gibst du den Takt wieder frei. Die Anzeige zeigt, wer gerade führt und ob der Takt sicher, gehalten oder unsicher ist.
- **Lichter bleiben nicht mehr stehen:** Kurze Lücken im Beat oder ein unsicherer Takt am Songanfang halten das Licht nicht mehr an; dann gibt es nur keine harten Blitze auf Verdacht.
- **Fehler merken:** Läuft der Takt einmal daneben, hält Sitz Light kurz die Analysewerte fest (nur Zahlen, keine Musik, nur auf deinem Rechner); per Knopf auch jederzeit von Hand.
- **Live neu geordnet:** großer Simulator (Klick auf eine Lampe zeigt ihre Regler daneben), großer Auto-Director mit Show, Szene, Stimmung und Phrasen, unten Master, Blinder, Strobe, Laser und Blackout mit ihren Tasten. Am Handy kompakt.
- **Neuer Reiter „Freigaben“:** alle Sicherheitsfreigaben auf einen Blick (DMX-Ausgabe, Lichtblitze, Mover-Bewegung, sichere Bereiche, Laser) mit Ampel.
- **Geräte übersichtlicher:** Fader nach Gerät mit Suche und Pegelbalken; in der Gerätedatenbank ein Filter nach **Hersteller**.
- **Mehr Bewegung:** In den Shows Party und Club bewegen sich die Moving Heads bei Stimmung Hoch und Eskalation größer und schneller, immer innerhalb ihres sicheren Bereichs. **22 neue Szenen** (jetzt 98).
- **Deine Daten bleiben erhalten:** Einstellungen, eigene Shows, Szenen, Farben und Gelerntes liegen außerhalb des Programms und werden bei Updates übernommen; vor jeder Umstellung entsteht automatisch eine Sicherung.

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

## Als Nächstes geplant

- **Takt und Phrasen noch besser erkennen**: mit dem Prüfstand an echter Musik und Aufnahmen aus dem Lernmodus nachschärfen, besonders den schnellen, richtigen Einstieg in DJ-Intros.
- **rekordbox-Anbindung** über rkbx_link richtig einbauen und testen (bisher experimentell).
- **Takt noch genauer**: Licht-Verzögerung für alle Taktquellen mit Testblitz einstellen, Art-Net-Nodes im Netz auf Knopfdruck finden.
- **Bühnenplan**: Lampen auf einem Plan anordnen, Moving Heads auf die Tanzfläche einmessen und Bereiche sperren, in die nie geleuchtet wird.
- **Verfolgen**: Moving Heads folgen dem Finger auf dem Bühnenplan, zum Beispiel aufs Brautpaar beim Eröffnungstanz.
- **Auto-Director verfeinern**: Gobos und Prismen, Akzente als eigene Bausteine.
- **Live eingreifen**: eigener MIDI-Controller, Farbe und Szene auf Knopfdruck festhalten.
- **App für iPhone und iPad**: Bedienung als Fernbedienung im lokalen Netz.
- **Hilfe für Einsteiger**: ein Reiter „Hilfe“ mit Schritt-für-Schritt-Anleitung vom ersten Start bis zur ersten Show.
- **Englisch**: Oberfläche und Hilfe auch auf Englisch.
- **Mehr Ausfallsicherheit**: Programmfenster startet nach einem Fehler neu, ohne dass die Show stoppt.
- **Später, optional**: 3D-Vorschau der Bühne, um Szenen ohne aufgebaute Lampen zu bauen.
