# Sicherung erstellen und wiederherstellen

Sicherungen sind in Phylax keine optionale Hygiene, sondern die einzige reale Schutzschicht zwischen dir und einem Geräteverlust. Phylax synchronisiert nicht in die Cloud. Wenn dein Gerät kaputtgeht, gestohlen wird oder der Browser die IndexedDB-Daten räumt, sind ohne Sicherung alle Beobachtungen, Laborwerte, Supplemente, offenen Punkte und Profil-Versionen weg. Diese Seite zeigt, wie du das verhinderst.

## Zwei Sicherungs-Wege

Phylax bietet zwei verschiedene Sicherungsformate, die beide ihre Berechtigung haben.

### Verschlüsselte `.phylax`-Sicherung

Die Standard-Sicherung. Eine `.phylax`-Datei ist:

- vollständig (enthält alle Daten deines Profils)
- verschlüsselt mit deinem Master-Passwort (AES-256-GCM)
- nur mit demselben Master-Passwort wieder lesbar
- als binäre Datei nicht für Menschen lesbar
- in keinem anderen Programm öffenbar

Das ist der Weg, wenn du dein Profil sichern oder zwischen Geräten transportieren willst, ohne die Klartext-Daten irgendwo abzulegen.

### Markdown-Export

Die zweite Sicherung. Eine Markdown-Datei ist:

- vollständig in Klartext lesbar
- nicht verschlüsselt
- in jedem Texteditor öffenbar
- direkt importierbar zurück in Phylax (siehe [Profil importieren](../data/profile-import.md))

Das ist der Weg, wenn du dein Profil außerhalb von Phylax archivieren willst (z.B. in einem privaten Notiz-System), oder wenn du den Inhalt ausdrucken willst, oder wenn du ihn jemandem geben willst.

!!! warning "Markdown-Sicherungen sind unverschlüsselt"
    Eine Markdown-Sicherung enthält all deine Gesundheitsdaten im Klartext. Behandele die Datei genauso wie ein medizinisches Dossier: sicherer Speicherort, kein E-Mail-Anhang an Unbekannte, kein Cloud-Speicher ohne eigene Verschlüsselung.

## Sicherung erstellen

In den **Einstellungen** der App gibt es einen Bereich für Sicherungen. Klick auf **Sicherung erstellen** öffnet ein kleines Formular, in dem du das Format wählst (`.phylax` oder Markdown). Phylax bündelt deine Daten und der Browser bietet die Datei zum Download an.

Die Datei landet im Download-Ordner deines Browsers. Verschiebe sie umgehend an einen sicheren Speicherort (siehe unten); im Download-Ordner ist sie weder organisiert noch gegen Versehen geschützt.

## Wann du eine Sicherung erstellen solltest

- **Nach größeren Bearbeitungen.** Eine neue Diagnose, ein neuer Laborbefund mit zwanzig Werten, eine Umstellung der Supplement-Liste. Diese Aufwände willst du nicht zweimal machen, falls etwas schiefgeht.
- **Vor Browser-Aufräumaktionen.** Wenn du ohnehin "Cookies und Webseitendaten löschen" planst, sichere vorher.
- **Periodisch, unabhängig vom Anlass.** Ein wöchentlicher oder monatlicher Termin in deinem Kalender mit "Phylax sichern" reicht. Frequenz richtet sich nach deiner Eintragungs-Aktivität.
- **Vor Geräte- oder Browser-Wechsel.** Phylax-Daten leben pro Browser; ohne Sicherung fängst du auf einem neuen Gerät bei null an.

## Wo du Sicherungen ablegen solltest

Eine Sicherung im Download-Ordner deines aktuellen Geräts schützt dich nicht gegen den Verlust dieses Geräts. Mehrere Speicherorte reduzieren das Verlustrisiko.

- **Zweites Gerät:** Externe Festplatte, USB-Stick, zweiter Computer.
- **Private Cloud:** Eigene Nextcloud, Synology NAS, oder vergleichbares mit Verschlüsselung.
- **Verschlüsseltes Drive:** Bitlocker-Laufwerk, FileVault-USB, VeraCrypt-Container.
- **Public Cloud (nur `.phylax`):** Da `.phylax`-Dateien bereits mit deinem Master-Passwort verschlüsselt sind, kannst du sie auch in eine Public Cloud (Dropbox, Google Drive, etc.) legen. Die Datei wäre dort verschlüsselt; das Risiko ist die Stärke deines Master-Passworts. Markdown-Sicherungen gehören dort nicht hin.

Drei verschiedene Orte sind besser als ein perfekter. Eine alte Sicherung an einem zweiten Ort ist mehr wert als die neueste Sicherung am selben Ort wie das Original.

## Sicherung wiederherstellen

Phylax bietet zwei Wiederherstellungs-Wege, je nachdem in welchem Zustand die App ist.

### Vor dem Login (Welcome-Bildschirm)

Wenn die App leer ist (frisch installiert, oder nach einem Reset), erscheint im Onboarding-Bildschirm die Option **Sicherung importieren**. Hier wählst du eine `.phylax`-Datei aus, gibst das Master-Passwort ein, mit dem sie verschlüsselt wurde, und Phylax stellt das Profil wieder her.

Dieser Weg ist die Standard-Migration auf ein neues Gerät: App öffnen, Sicherung importieren, fertig.

### Nach dem Login (Einstellungen)

Wenn du in einer entsperrten Phylax-Sitzung bist und eine ältere Sicherung importieren willst (z.B. nach einem versehentlichen Lösch-Vorgang), öffnest du die Einstellungen, Bereich Sicherungen, **Sicherung importieren**.

!!! warning "Wiederherstellung überschreibt"
    Eine Wiederherstellung ersetzt den aktuellen Profilstand vollständig durch den Stand der Sicherung. Wenn du seit der Sicherung Eintragungen gemacht hast, sind diese danach weg. Bei Unsicherheit: erst eine aktuelle Sicherung erstellen, dann wiederherstellen, sodass du im Notfall zur aktuellen Version zurück kannst.

Beide Wege erfordern das Master-Passwort, mit dem die Sicherung erstellt wurde. Das ist nicht zwangsläufig dein aktuelles Master-Passwort: wenn du dein Master-Passwort nach Erstellung der Sicherung geändert hast, brauchst du das alte zum Importieren.

## Was Sicherungen NICHT lösen

Verschlüsselte Sicherungen schützen dich vor:

- Verlust oder Defekt des Geräts
- Versehentliches Löschen einer Beobachtung oder eines Profils
- Browser-Aufräumaktionen, die IndexedDB-Daten entfernen
- iOS Safari, das Daten nach 7 Tagen Inaktivität auslagert

Verschlüsselte Sicherungen schützen dich NICHT vor:

- **Vergessenem Master-Passwort.** Die Sicherung ist mit demselben Passwort verschlüsselt wie deine Live-Daten. Wenn du das Passwort vergisst, ist die Sicherung genauso unzugänglich wie die Datenbank. Siehe [Erste Schritte: Master-Passwort](../getting-started/first-steps.md#2-master-passwort-festlegen).
- **Verlust aller Sicherungs-Strategien gleichzeitig.** Wenn das Gerät kaputtgeht, der Backup-USB im selben Beutel war und du keine Cloud-Kopie hast, ist alles weg. Mehrere Orte. Immer.

## Praktische Empfehlung

Eine erprobte Kombination für die meisten Phylax-Nutzer:

1. **Wöchentlicher Termin** im Kalender: `.phylax`-Sicherung erstellen und in private Cloud kopieren.
2. **Quartalsweise** zusätzlich auf USB-Stick oder externe Festplatte.
3. **Vor Reisen oder Geräte-Wechsel** ad-hoc-Sicherung.

Plus: Master-Passwort an mindestens zwei Orten gespeichert (Passwort-Manager und physische Notiz). Siehe [Erste Schritte: Empfohlene Strategien](../getting-started/first-steps.md#empfohlene-strategien).

## Weiterlesen

- Master-Passwort sicher aufbewahren: [Erste Schritte](../getting-started/first-steps.md#2-master-passwort-festlegen).
- Was ist im `.phylax`-Format: Architektur-Hintergrund unter [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax).
- Profil aus Markdown importieren: [Profil importieren](../data/profile-import.md).

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
