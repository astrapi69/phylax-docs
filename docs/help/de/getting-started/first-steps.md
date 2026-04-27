# Erste Schritte

Diese Anleitung führt dich von "App geöffnet" bis zur ersten gespeicherten Beobachtung. Rechne mit fünf bis zehn Minuten beim ersten Durchlauf.

## 1. Phylax öffnen

Phylax läuft als Progressive Web App (PWA) direkt im Browser, ohne Installation aus einem App Store.

- Adresse: [https://astrapi69.github.io/phylax/](https://astrapi69.github.io/phylax/)
- Empfohlen: aktueller Chrome, Firefox, Safari oder Edge
- Auf dem Smartphone: über "Zum Startbildschirm hinzufügen" wirst du Phylax wie eine native App nutzen können

Die App lädt einmal aus dem Netz und arbeitet danach offline weiter. Daten gehen ab dem ersten Klick nicht mehr nach außen.

## 2. Master-Passwort festlegen

Beim ersten Aufruf siehst du den Onboarding-Bildschirm. Du legst dein **Master-Passwort** fest. Daraus leitet Phylax den Schlüssel ab, mit dem all deine Profil-Daten verschlüsselt werden.

Empfehlungen für ein gutes Master-Passwort:

- Lang ist wichtiger als kompliziert. Eine Passphrase aus mehreren Wörtern, die für dich Sinn ergibt, ist besser als ein kurzes Sonderzeichen-Konstrukt.
- Verwende es nur für Phylax. Recycelte Passwörter aus anderen Diensten sind die häufigste reale Schwachstelle.
- Speichere es in einem Passwort-Manager oder schreibe es an einem sicheren Ort auf.

!!! warning "Master-Passwort: Achillesferse deiner Daten"

    Phylax kennt dein Master-Passwort nicht. Es wird nirgends
    gespeichert, weder auf deinem Gerät noch auf einem Server. Das ist
    der Grund warum deine Daten sicher sind, aber auch warum es keinen
    Reset gibt: Es gibt niemanden der das Passwort wiederherstellen
    könnte.

    Wenn du das Master-Passwort vergisst, sind alle in Phylax
    gespeicherten Daten unwiderruflich verloren. Auch verschlüsselte
    Backups lassen sich ohne das Passwort nicht öffnen.

    **Das ist die wichtigste Sache die du in Phylax richtig machen
    musst.** Investiere bewusst Zeit in eine Strategie die zu dir
    passt.

### Empfohlene Strategien

Wähle mindestens zwei der folgenden Optionen, idealerweise drei. Eine einzige Sicherung ist eine Sicherung die im Ernstfall fehlt.

#### Passwort-Manager (digital, am bequemsten)

Ein Passwort-Manager speichert dein Master-Passwort verschlüsselt und synchronisiert es zwischen deinen Geräten. Optionen:

- **Lokal verschlüsselt:** Bitwarden (kostenlos, Open-Source), KeePass (Datei-basiert, volle Kontrolle), 1Password (kommerziell, sehr ausgereift)
- **Browser-integriert:** Firefox Account, Chrome Passwords, Safari Schlüsselbund. Bequem, aber abhängig von deinem Browser-Konto.

Wenn du Phylax wegen Datensouveränität nutzt, passt ein selbst-gehosteter Bitwarden-Server (Vaultwarden) oder KeePass mit eigener Cloud-Synchronisation am besten dazu.

#### Private Cloud / selbstgehostete Lösung

Wenn du eine eigene Nextcloud, Synology NAS, oder ähnliches betreibst, kannst du das Master-Passwort dort in einem verschlüsselten Notiz-Tool speichern (z.B. Joplin mit Ende-zu-Ende-Verschlüsselung, Standard-Notes, oder verschlüsselte Markdown-Dateien). Vorteil: deine Backup-Strategie für die Cloud schützt automatisch auch das Phylax-Passwort.

#### Physische Notiz

Schreibe das Master-Passwort auf, bewahre es an einem sicheren Ort auf, nicht am Gerät, nicht im Geldbeutel den du täglich dabei hast. Beispiele: Tresor, abschließbare Schublade, bei Vertrauensperson hinterlegt, Bankschließfach. Mehrere Kopien an verschiedenen Orten reduzieren das Verlustrisiko.

#### Recovery-Strategie für den Notfall

Lege fest, wer im Notfall (Krankheit, Tod, Unfall) Zugriff auf dein Master-Passwort bekommen soll. Notiere die Anweisung schriftlich, zusammen mit deinem Testament oder bei einem Vertrauensanwalt.

### Was Backups NICHT lösen

Verschlüsselte Backups schützen vor:

- Geräteverlust (Laptop kaputt, Handy weg)
- Versehentliches Löschen
- Datei-Korruption

Verschlüsselte Backups schützen NICHT vor:

- Vergessenem Master-Passwort, das Backup ist mit demselben Passwort verschlüsselt
- Verlust aller Sicherungs-Strategien gleichzeitig

### Praktischer Vorschlag

Die meisten Phylax-Nutzer fahren gut mit dieser Kombination:

1. Master-Passwort in einem Passwort-Manager (z.B. Bitwarden mit eigener Cloud-Synchronisation)
2. Eine physische Backup-Notiz an einem sicheren Ort
3. Regelmäßige verschlüsselte Phylax-Backups auf einem zweiten Gerät oder in privater Cloud (siehe [Sicherung erstellen und wiederherstellen](../backup/create-and-restore.md))

Diese drei zusammen decken die häufigsten Szenarien ab: Geräteverlust, Passwort-Vergessen, Synchronisations-Probleme.

## 3. Profil anlegen

Nach dem Setzen des Master-Passworts wirst du gefragt, ob du ein neues Profil anlegen oder eine bestehende Sicherung importieren möchtest.

Beim ersten Start: **neues Profil anlegen**.

Du gibst einen Profilnamen ein, optional Geburtsdatum oder Alter und Geschlecht. Mehr braucht es zum Start nicht. Alle weiteren Felder (Gewicht, Diagnosen, Medikamente, Kontextnotizen) lassen sich später jederzeit nachtragen.

## 4. Wo deine Daten leben

Phylax speichert dein Profil verschlüsselt in der lokalen Datenbank deines Browsers (IndexedDB). Das bedeutet:

- Daten bleiben auf deinem Gerät, in deinem Browser-Profil
- Wechsel des Browsers (zum Beispiel von Firefox zu Chrome) heißt: anderes Datenpaket, du musst die Sicherung importieren
- Wechsel des Geräts geht über die `.phylax`-Sicherungsdatei (siehe [Sicherung erstellen und wiederherstellen](../backup/create-and-restore.md))
- Aufräum-Aktionen im Browser ("Cookies und Webseitendaten löschen") können auch Phylax-Daten erfassen, je nach Browser-Einstellung

!!! info "iOS Safari"
    iOS Safari löscht IndexedDB-Daten von Webseiten, die nicht zum Startbildschirm hinzugefügt wurden, nach 7 Tagen Inaktivität. Wenn du Phylax auf iPhone oder iPad nutzt, füge die App zum Startbildschirm hinzu und arbeite mindestens wöchentlich damit, oder lege regelmäßig Sicherungen an.

## 5. Erste Beobachtung anlegen

Eine **Beobachtung** ist die kleinste Einheit in Phylax. Sie hält in einer kleinen, vollständigen Form fest, was du wahrnimmst (Fakt), in welchen Zusammenhang du es einordnest (Muster) und wie du darauf reagierst (Selbstregulation). Diese drei Felder sind Pflicht; zusätzlich vergibst du ein **Thema** zur Gruppierung und einen **Status**.

Beispiel für einen ersten Eintrag:

- **Thema:** Schlaf
- **Beobachtung (Fakt):** Heute morgens 7:30 Uhr Kopfschmerzen rechtsseitig, wach geworden mit Druck.
- **Muster:** Tritt seit zwei Wochen mehrfach auf, immer nach kürzeren Nächten unter sechs Stunden.
- **Selbstregulation:** Ab heute mindestens sieben Stunden Schlaf, in zwei Wochen erneut auswerten.
- **Status:** in Beobachtung

Wechsle in den Bereich "Beobachtungen", lege einen neuen Eintrag an, fülle die Pflichtfelder und speichere. Damit ist dein Profil offiziell gestartet.

Mehr zur Idee hinter Fakt-Muster-Selbstregulation und zu den optionalen Feldern siehst du auf der Seite [Beobachtungen](../daily-use/observations.md).

## 6. Beim nächsten Mal

Wenn du Phylax nach einer Pause wieder öffnest, siehst du den Unlock-Bildschirm. Master-Passwort eingeben, Phylax leitet daraus den Schlüssel ab, entschlüsselt deine Daten und du arbeitest weiter.

Nach längerer Inaktivität (Standard: 5 Minuten) sperrt sich Phylax von selbst und löscht den Schlüssel aus dem Arbeitsspeicher. Das ist Absicht: ein vergessenes Tab im Café soll deine Daten nicht offenlegen.

## Nächste Schritte

- Eine erste Sicherung erstellen, sobald die ersten Einträge stehen: [Sicherung erstellen und wiederherstellen](../backup/create-and-restore.md).
- Mehr über Beobachtungen und ihre drei Typen: [Beobachtungen](../daily-use/observations.md).
- Wenn dich die Idee dahinter interessiert: [Was ist Phylax](what-is-phylax.md) und die Artikel-Serie [Lebende Gesundheit](https://asterios-raptis.medium.com/lebende-gesundheit-die-serie-0193f66df9a3).

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
