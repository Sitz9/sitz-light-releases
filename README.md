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

### Version 0.12.0 (31.10.2026)

- **iPad und Handy koppeln**: Nur gekoppelte Geräte dürfen Sitz Light bedienen. Am Licht-Rechner unter Einstellungen → Fernbedienung „Neues Gerät koppeln“ wählen, dann am iPad die PIN eingeben oder den QR-Code abfotografieren. Für jedes Gerät wählst du „Bedienen“ (nur Live) oder „Einrichten“ (alles). Nach dem Update müssen iPad und Handy einmal neu gekoppelt werden.
- **Live-Tab nach deinen Wünschen**: Mit „Anordnen“ ordnest du die Bausteine (Director, Simulator, Takt, Genre, Stimmung, Phrase, Pulsieren, Farbstimmung, Momente, Launchpad, Mover) frei an, getrennt für Rechner, iPad und Handy. Genre, Stimmung, Phrase, Pulsieren und Farbstimmung gibt es als große Knöpfe oder als Auswahlliste. Blackout bleibt immer unten in der Leiste.
- **Launchpad**: große Felder für Blinder, Strobe und Laser zum Halten oder Einrasten. Eingerastet laufen Blinder und Strobe höchstens die eingestellte Zeit (Standard 10 s, höchstens 30 s) mit Countdown. Dazu Farbknöpfe (Blau, Lila, Pink, Grün, Gelb, Rot, Weiß, frei einstellbar), die alle Lampen weich umfärben.
- **Mover von Hand**: Moving Heads mit dem Finger oder den Pfeiltasten ausrichten, immer im sicheren Bereich, Positionen speichern, mit einem Knopf zurück an den Director.
- **Hintergrund**: Grau, Schwarz, Carbon oder ein eigenes Foto (wird automatisch abgedunkelt, damit alles lesbar bleibt).
- **Lernen aus Eingriffen** ist jetzt ein Schalter und ab Werk aus.
- Auswahllisten im Director lesbar, djsitz.com in der Kopfzeile, sicherer Start, wenn Sitz Light schon läuft.

### Version 0.11.1 (31.10.2026)

- **Ruhigerer Build-up**: Vor dem Drop baut das Licht die Spannung jetzt über Helligkeit, kräftiger werdende Farben und schneller werdende Moving Heads auf, statt über schnelles Geflacker. Eine Szene steigert sich bis zum Drop, statt alle paar Takte zu wechseln. Lichtblitze gibst du weiterhin selbst per Strobe-Knopf dazu.
- **Segmente zusammenfassen**: Bei Geräten mit mehreren Segmenten (z. B. LED-Bars) stellst du unter Geräte → Patch ein, wie viele Segmente zusammen leuchten. Standard: höchstens vier Blöcke je Gerät, das wirkt ruhiger.
- **Szenen-Vorschau**: Läuft die Show, zeigt das Licht eine neu hinzugefügte Szene nicht mehr von selbst. Mit ▶ fragt Sitz Light vorher, ob die laufende Show kurz unterbrochen werden soll.

### Version 0.11.0 (31.10.2026)

- **Genre**: Wähle im Live-Tab das Genre, das du gerade spielst (House, Dance & Pop, Party-Action, Classics, Hip-Hop / R&B, Latin, Schlager, Chill / Lounge, Hochzeit: Dinner / Sekt, Hochzeit: Eröffnungstanz). Das Licht übernimmt den Charakter der Musik: wie viel sich bewegt, wie oft Szenen wechseln, ob es pulsiert. Der Wechsel kommt sanft zur nächsten Phrase. Tasten Umschalt+1 bis Umschalt+9. Eigene Genres lassen sich unter Director → Genres anlegen.
- Die Show bleibt der Rahmen: Ein Genre macht das Licht nie heller, schneller oder wilder, als die Show erlaubt. Lichtblitze gibt es weiterhin nur per Strobe-Knopf.
- **Mover-Show**: Die Moving Heads rocken jetzt richtig ab, mit großen, abwechslungsreichen Bewegungen im Takt und einer neuen Bewegung je Phrase, immer im sicheren Bereich.
- **Wenig Energie = ruhiges Licht**: Wird die Musik sehr ruhig, blinkt nichts mehr, das Licht wechselt höchstens langsam die Farbe.
- **Farben im Live-Tab** wählbar, kleine „i“-Erklärungen überall im Director, ruhigere Gliederung, nichts bricht mehr um.
- **Lauflichter** lassen sich abschalten oder mit Start- und Endgerät festlegen.
- **Szenen-Vorschau**: Beim Zusammenstellen einer Show zeigt das Licht jede Szene kurz im Takt, auch ohne Musik.
- **20 neue Szenen**, vor allem ruhige und fließende für Build-up und Drop, dazu „Frequenz-Höhen“: Lampen unten folgen dem Bass, oben den Höhen (Höhe je Lampe im Patch einstellbar).
- **Akzentfarbe** jetzt Gelb wie das Logo, unter Einstellungen → Bedienung frei wählbar.
- Die Zurück-Taste der Maus (und Zurück am iPad) springt nur noch zwischen den Seiten und verlässt Sitz Light nie.
- In der Demo steht, wo es die Lizenz gibt: djsitz.com.

## Als Nächstes geplant

- **Liedteile noch genauer**: weniger Drops an falscher Stelle, Intro und Outro besser erkennen.
- **Lernen überarbeiten**: Korrekturen von Hand wirken noch gezielter auf die Erkennung der Liedteile.
- **3D-Bühnenplan**: Lampen auf einem Plan platzieren, Moving Heads grafisch einrichten (Zielpunkte, sichere Bereiche, gesperrte Bereiche), mit einfacher 2D-Ansicht als Rückfall.
- **Mehr Ausfallsicherheit**: Programmfenster startet nach einem Fehler neu, ohne dass die Show stoppt; Sicherung der Show vor dem Gig.
- **Takt noch genauer**: Art-Net-Nodes im Netz auf Knopfdruck finden, langsamere Lieder sicherer erkennen.
- **rekordbox-Anbindung** über rkbx_link richtig einbauen und testen (bisher experimentell).
- **Verfolgen**: Moving Heads folgen dem Finger auf dem Bühnenplan, zum Beispiel aufs Brautpaar beim Eröffnungstanz.
- **Auto-Director verfeinern**: Gobos und Prismen, Akzente als eigene Bausteine.
- **Live eingreifen**: eigener MIDI-Controller.
- **App für iPhone und iPad**: Bedienung als Fernbedienung im lokalen Netz.
- **Hilfe für Einsteiger**: ein Reiter „Hilfe“ mit Schritt-für-Schritt-Anleitung vom ersten Start bis zur ersten Show.
- **Englisch**: Oberfläche und Hilfe auch auf Englisch.
