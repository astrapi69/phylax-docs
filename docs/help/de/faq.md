# FAQ

Häufige Fragen zu Phylax. Wenn deine Frage hier nicht steht, wirf einen Blick auf [Erste Schritte](getting-started/first-steps.md), [Beobachtungen](daily-use/observations.md) oder den [Hintergrund](background.md).

## Was passiert, wenn ich mein Master-Passwort vergesse?

Es gibt keinen Reset und keinen Recovery-Pfad. Phylax kennt dein Master-Passwort nicht und speichert es nirgendwo. Wenn du es vergisst, sind alle in Phylax gespeicherten Daten unzugänglich. Auch verschlüsselte Sicherungen lassen sich ohne das Passwort nicht öffnen. Diese Eigenschaft macht Phylax sicher gegen Cloud-Diebstahl, sie macht aber das Passwort selbst zur kritischen Stelle. Lege deshalb von Anfang an eine Strategie an: siehe [Erste Schritte: Master-Passwort](getting-started/first-steps.md#2-master-passwort-festlegen).

## Werden meine Daten irgendwo hochgeladen?

Nein. Phylax hat keinen eigenen Server. Alle Daten leben verschlüsselt in deinem Browser (IndexedDB). Es gibt keine Telemetrie, keine Analytics, keine Werbe-Tracker. Die einzige Ausnahme: wenn du den optionalen KI-Assistenten verwendest, gehen deine Anfragen direkt vom Browser an den von dir gewählten Anbieter (OpenAI oder Anthropic) mit deinem eigenen API-Schlüssel. Phylax fungiert dort nur als Vermittler ohne Zwischenspeicher.

## Funktioniert Phylax offline?

Ja. Phylax ist eine Progressive Web App, die nach dem ersten Laden offline weiterarbeitet. Alle Bearbeitungen, Eintragungen und Anzeigen funktionieren ohne Internetverbindung. Eine Verbindung brauchst du nur, wenn der KI-Assistent verwendet wird oder wenn die App ein Update aus dem Netz lädt.

## Kann ich Phylax auf mehreren Geräten nutzen?

Ja, aber ohne automatischen Sync. Jeder Browser auf jedem Gerät hat seinen eigenen verschlüsselten Datenspeicher. Wenn du Phylax auf mehreren Geräten nutzen willst, exportierst du auf Gerät A eine `.phylax`-Sicherung und importierst sie auf Gerät B. Bei späteren Bearbeitungen auf B bleibt A im alten Stand, bis du erneut eine Sicherung übertragen wirst. Mehr dazu in [Sicherung erstellen und wiederherstellen](backup/create-and-restore.md).

## Wie lange bleiben meine Daten im Browser?

Solange du sie nicht löschst und der Browser sie nicht räumt. Browser können IndexedDB-Daten unter Speicherdruck oder bei langer Inaktivität entfernen, vor allem auf Mobilgeräten. Phylax fordert beim ersten Setzen des Master-Passworts persistente Speicherung an (`navigator.storage.persist()`); wenn der Browser das gewährt, sind deine Daten gegen automatische Räumung geschützt. Trotzdem: regelmäßige Sicherungen sind nicht optional.

## Was passiert, wenn iOS Safari die IndexedDB nach 7 Tagen Inaktivität leert?

iOS Safari räumt IndexedDB-Daten von Webseiten, die nicht zum Startbildschirm hinzugefügt wurden, nach 7 Tagen ohne Nutzung. Wenn das passiert, sind die Daten in diesem Browser weg. Zwei Schutzmaßnahmen: Phylax über "Zum Startbildschirm hinzufügen" als App installieren (dann gilt die Räumung nicht) und mindestens wöchentlich Sicherungen erstellen, die du auf einem zweiten Speicherort liegen hast.

## Stellt Phylax Diagnosen oder gibt Therapieempfehlungen?

Nein, nie. Phylax ist eine Doku- und Strukturierungsplattform, kein Medizinprodukt. Wenn du einen erhöhten Laborwert einträgst, sagt Phylax dir nicht, was er bedeutet. Auch der KI-Assistent strukturiert nur, er interpretiert nicht. Diagnosen, Therapieentscheidungen und medizinische Bewertungen bleiben bei deiner Ärztin oder deinem Arzt.

## Welche Daten kann Phylax aus Befunden importieren?

Mit dem KI-Assistenten und deinem eigenen API-Schlüssel kannst du PDFs (Arztbriefe, Laborberichte, ePA-Dokumente) hochladen, und der Assistent extrahiert daraus Beobachtungen, Laborwerte und ähnliches in strukturierter Form. Du siehst eine Vorschau und entscheidest, was tatsächlich ins Profil übernommen wird. Aktuell ist der ePA-Import-Pfad ausgebaut (siehe [ePA-Import](data/epa-import.md)); weitere Quellen werden in späteren Iterationen folgen.

## Wie sicher ist die Verschlüsselung?

Phylax verwendet AES-256-GCM für die Verschlüsselung der Daten und PBKDF2 mit SHA-256 (1.200.000 Iterationen) für die Ableitung des Schlüssels aus deinem Master-Passwort. Der Schlüssel selbst lebt nur im Arbeitsspeicher des Browsers, nie persistent. Bedrohungs-Modell und Architektur-Entscheidungen sind im Quellcode-Repo dokumentiert: [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax).

## Kann ich Phylax mit jemand anderem teilen?

Ein Profil pro Browser, ein Master-Passwort pro Profil. Multi-Profile (mehrere Personen oder Stellvertreter-Pflege auf einem Gerät) ist als Phase 8 geplant, aktuell aber noch nicht verfügbar. Was du heute schon kannst: ein Stellvertreterprofil für eine andere Person pflegen (siehe [Basisdaten](daily-use/profile-base-data.md)).

## Was tun, wenn ein Backup nicht importierbar ist?

Drei häufige Ursachen:

- **Falsches Master-Passwort.** Sicherungen sind mit dem Passwort verschlüsselt, das zum Zeitpunkt der Erstellung galt. Wenn du es seither geändert hast, brauchst du das alte zum Importieren.
- **Beschädigte Datei.** `.phylax`-Dateien dürfen nicht geändert oder umbenannt werden, sonst schlägt die Validierung fehl. Wenn die Datei einen Cloud-Sync durchlaufen hat, kann sie beschädigt sein; importiere lieber das Original aus dem Backup-Speicher.
- **Falsches Format.** Phylax-Sicherungen haben die Endung `.phylax`. Markdown-Sicherungen werden über den Profil-Import-Pfad eingelesen, nicht über den Backup-Import.

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
