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

!!! warning "Phylax kann dein Master-Passwort nicht zurücksetzen"
    Phylax kennt dein Passwort nicht. Es liegt nirgendwo gespeichert, weder bei dir auf dem Gerät noch auf einem Server. Wenn du es vergisst, sind die verschlüsselten Daten unzugänglich. Es gibt eine Reset-Funktion, die löscht aber alles und startet bei null. Genau diese Eigenschaft macht Phylax sicher gegen Cloud-Diebstahl, sie macht aber auch das Passwort selbst zur kritischen Stelle.

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

Eine **Beobachtung** ist die kleinste Einheit in Phylax. Drei Typen stehen zur Verfügung: Fakt, Muster, Selbstregulation. Beim ersten Mal reicht ein Fakt: zum Beispiel "Heute morgens 7:30 Uhr Kopfschmerzen rechtsseitig, wach geworden mit Druck".

Wechsle in den Bereich "Beobachtungen", lege einen neuen Eintrag an, wähle Typ "Fakt", schreibe deinen Text und speichere. Damit ist dein Profil offiziell gestartet.

## 6. Beim nächsten Mal

Wenn du Phylax nach einer Pause wieder öffnest, siehst du den Unlock-Bildschirm. Master-Passwort eingeben, Phylax leitet daraus den Schlüssel ab, entschlüsselt deine Daten und du arbeitest weiter.

Nach längerer Inaktivität (Standard: 5 Minuten) sperrt sich Phylax von selbst und löscht den Schlüssel aus dem Arbeitsspeicher. Das ist Absicht: ein vergessenes Tab im Café soll deine Daten nicht offenlegen.

## Nächste Schritte

- Eine erste Sicherung erstellen, sobald die ersten Einträge stehen: [Sicherung erstellen und wiederherstellen](../backup/create-and-restore.md).
- Mehr über Beobachtungen und ihre drei Typen: [Beobachtungen](../daily-use/observations.md).
- Wenn dich die Idee dahinter interessiert: [Was ist Phylax](what-is-phylax.md) und die Artikel-Serie [Lebende Gesundheit](https://asterios-raptis.medium.com/lebende-gesundheit-die-serie-0193f66df9a3).

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
