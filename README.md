<p align="center"><img src="logo.png" alt="Sitz Light" width="320"></p>

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

### Version 0.8.0 (24.10.2026)

- **Konfiguration sichern und übertragen:** Unter Einstellungen → „Sichern und übertragen“ speichert Sitz Light die ganze Einrichtung in einer Datei (Patch, eigene Geräte, Shows, Szenen, Farbstimmungen, Takt- und Director-Einstellungen, DMX-Ziele, Tastenkürzel, Gelerntes). Auf einem anderen Rechner wieder einlesen, mit Vorschau und Auswahl. Vorher wird der alte Stand automatisch gesichert. Lizenz und Sicherheitsfreigaben gehen bewusst nicht mit.
- **Vorsorge für die Zukunft:** Sitz Light versteht jetzt eine „Generalfreigabe“. Sollte Sitz Light einmal eingestellt werden, macht diese Datei es für alle dauerhaft frei nutzbar, ohne Lizenz und ohne Internet.

### Version 0.7.1 (12.10.2026)

- Behoben: Die Anzeigen blieben nach dem Einschalten des Audio-Eingangs stehen, und ein Browser auf einem anderen Gerät bekam keine Daten. Jetzt laufen alle Oberflächen weiter, auch wenn einmal ein Wert unerwartet ist.
- Behoben: Beim Wechseln des Audio-Eingangs konnte Sitz Light auf dem Mac abstürzen.
- Der Audio-Eingang heilt sich selbst: Liefert das Interface kurz nichts oder wird es neu eingesteckt, öffnet Sitz Light den Eingang von selbst neu und zeigt „Audio neu gestartet“.
- Ein neues Tempo nach einem Songwechsel wird deutlich schneller übernommen (im Mittel nach etwa 10 statt fast 30 Sekunden).
- Neu: Hinweis „Daten N s alt“, falls die Anzeigen einmal nicht mehr aktuell sind.
- Neu: Einstellungen → Über und Leistung zeigt die Reaktionszeit und die Auslastung der Audio-Analyse; „Diagnosepaket speichern“ lädt Protokolle und Kennwerte als Datei herunter (keine Musik, keine Lizenz, keine Zugangsdaten).

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

## Als Nächstes geplant

- **Liedteile noch genauer**: weniger Drops an falscher Stelle, Intro und Outro besser erkennen.
- **Mehr Szenen je Liedteil**: wiedererkennbare Bewegungen und eine Steigerung im Build-up bis zum Drop.
- **3D-Bühnenplan**: Lampen auf einem Plan platzieren, Moving Heads grafisch einrichten (Zielpunkte, sichere Bereiche, gesperrte Bereiche), mit einfacher 2D-Ansicht als Rückfall.
- **Mehr Ausfallsicherheit**: Programmfenster startet nach einem Fehler neu, ohne dass die Show stoppt.
- **Takt noch genauer**: Licht-Verzögerung für alle Taktquellen mit Testblitz einstellen, Art-Net-Nodes im Netz auf Knopfdruck finden, langsamere Lieder sicherer erkennen.
- **rekordbox-Anbindung** über rkbx_link richtig einbauen und testen (bisher experimentell).
- **Verfolgen**: Moving Heads folgen dem Finger auf dem Bühnenplan, zum Beispiel aufs Brautpaar beim Eröffnungstanz.
- **Auto-Director verfeinern**: Gobos und Prismen, Akzente als eigene Bausteine.
- **Live eingreifen**: eigener MIDI-Controller, Farbe und Szene auf Knopfdruck festhalten.
- **App für iPhone und iPad**: Bedienung als Fernbedienung im lokalen Netz.
- **Hilfe für Einsteiger**: ein Reiter „Hilfe“ mit Schritt-für-Schritt-Anleitung vom ersten Start bis zur ersten Show.
- **Englisch**: Oberfläche und Hilfe auch auf Englisch.
