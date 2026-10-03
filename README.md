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

### Version 0.2.0 (Testphase ab 03.10.2026)

- Sitz Light hat jetzt ein eigenes Programmfenster und einen Installer für Windows und macOS (Apple Silicon und Intel, ab macOS 12).
- Automatische Updates: Neue Versionen werden angeboten und erst nach deiner Bestätigung installiert, nie während die Lampen angesteuert werden. Ein Gig-Modus sperrt Updates ganz, und zur vorherigen Version kannst du jederzeit zurückwechseln.
- Beim Beenden mit eingeschalteter Ausgabe fragt Sitz Light nach und schaltet vorher alle Lampen aus.
- Beim Beenden (auch über ⌘Q, das Dock oder beim Abmelden) gehen die Lampen zuverlässig aus, und Sitz Light räumt sich vollständig auf.
- Gleichmäßigerer Lichttakt auf Notebooks im Akkubetrieb; die Leistungsanzeige zeigt jetzt auch Akku oder Netzteil.
- Der Mac-Installer zeigt, wohin Sitz Light gezogen werden muss.
- Startet Sitz Light einmal nicht, zeigt es jetzt verständlich, woran es liegt, und öffnet auf Knopfdruck die Log-Datei.
- Bei allen Rückfragen ist die sichere Antwort vorausgewählt („Abbrechen“, „Später“): Ein versehentliches Enter schaltet nichts ein oder aus.
- Neue Leistungsanzeige: Sie zeigt, ob Sitz Light auf deinem Rechner entspannt läuft.
- Die DMX-Ausgabe unter Windows läuft jetzt gleichmäßig im Takt.

## Als Nächstes geplant

- **Gerätedatenbank**: Tausende Lampen bekannter Hersteller zum Auswählen, ohne Kanäle von Hand einzutippen. Fehlende Geräte lassen sich in wenigen Minuten selbst anlegen und direkt an der Lampe prüfen.
- **Takt aus rekordbox**: Das Licht folgt automatisch Tempo, Takt und Songaufbau, auch wenn Sitz Light auf einem eigenen Rechner läuft.
- **Bühnenplan**: Lampen auf einem Plan anordnen, Moving Heads auf die Tanzfläche einmessen und Bereiche sperren, in die nie geleuchtet wird.
- **Verfolgen**: Moving Heads folgen dem Finger auf dem Bühnenplan, zum Beispiel aufs Brautpaar beim Eröffnungstanz.
- **Effekte und Auto-Director**: Die Show läuft von selbst passend zur Musik. Du wählst nur die Stimmung (Dinner, Eröffnungstanz, Party, Peak) und die Intensität.
- **Live eingreifen**: Farbe festhalten, Look halten, Strobe, Blinder und Blackout auf Knopfdruck.
- **App für iPhone und iPad**: Bedienung als Fernbedienung im lokalen Netz.
- **Später, optional**: 3D-Vorschau der Bühne, um Looks ohne aufgebaute Lampen zu bauen.
