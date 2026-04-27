# Basisdaten

Die Basisdaten sind das stabile Fundament deines Profils: Name, Geburtsdatum, Geschlecht, bekannte Diagnosen, aktuelle Medikamente, relevante Einschränkungen. Sie ändern sich seltener als Beobachtungen oder offene Punkte und bilden den Rahmen, in dem alles andere Sinn ergibt. Wer das Profil drei Jahre lang pflegt, hat hier den Anker.

## Welche Felder gehören dazu

Die Basisdaten umfassen aktuell:

- **Name:** Wie das Profil heißen soll. Bei einem eigenen Profil dein Name oder ein Kürzel; bei einem Stellvertreterprofil der Name der betreuten Person.
- **Geburtsdatum:** ISO-Datum. Wenn vorhanden, ist es immer die bessere Quelle als das Alter.
- **Alter:** Reine Zahl. Nur sinnvoll, wenn das Geburtsdatum unbekannt oder bewusst nicht gespeichert wird.
- **Geschlecht:** Frei eintragbarer Text, kein geschlossenes Auswahlfeld. Beispiele: "weiblich", "männlich", "divers", "nicht angegeben".
- **Bekannte Diagnosen:** Liste, eine Diagnose pro Zeile. Beispiele: "Hashimoto-Thyreoiditis", "Migräne mit Aura", "Pollenallergie".
- **Aktuelle Medikamente:** Liste, dauerhaft eingenommene Medikamente. Diese überschneidet sich teilweise mit dem Supplement-Bereich; die Trennung ist Konvention: hier landet, was Verordnung ist und woran du nicht selbst regelmäßig schraubst, im Supplement-Bereich landet alles, was du in eigener Regie steuerst.
- **Relevante Einschränkungen:** Liste, dauerhafte Einschränkungen, die für medizinische Entscheidungen wichtig sind. Beispiele: "Laktoseintoleranz", "Penicillin-Unverträglichkeit", "Kontrastmittel-Risiko".

## Geburtsdatum oder Alter

Wenn beides vorhanden ist, gewinnt das Geburtsdatum. Phylax leitet das Alter daraus ab, wo es benötigt wird, und du musst es nicht jährlich von Hand pflegen.

Das Alter-Feld ist trotzdem da, für drei Fälle:

- Bei Stellvertreterprofilen, wenn das Geburtsdatum nicht bekannt ist (z.B. älterer Verwandter mit Demenz, Geburtsurkunde nicht greifbar).
- Wenn du aus Datenschutzgründen das genaue Geburtsdatum nicht eintragen willst.
- Bei einem Profil-Import, in dem nur das Alter steht.

Sobald du ein Geburtsdatum nachpflegst, wird das vorher gepflegte Alter überschrieben, weil das Geburtsdatum die genauere Quelle ist.

## Profil bearbeiten

In der Profilansicht gibt es im Bereich "Basisdaten" einen Knopf **Profil bearbeiten**. Klick öffnet ein Formular mit allen oben genannten Feldern.

1. Felder anpassen.
2. Optional **Grund der Änderung** eintragen. Beispiel: "Neue Allergie nach Heuschnupfen-Saison aufgenommen", "Diagnose Hashimoto vom 14.03. ergänzt".
3. Speichern.

Beim Speichern erzeugt Phylax automatisch einen neuen Profil-Versions-Eintrag.

## Profil-Versionen

Jede Bearbeitung der Basisdaten erhöht die Profilversion und erzeugt einen Eintrag im Versionsverlauf. Das ist kein Hintergrund-Detail, sondern ein wichtiges Feature:

- Du kannst nachvollziehen, wann du was geändert hast.
- Bei medizinisch relevanten Änderungen (neue Diagnose, neue Allergie, abgesetztes Medikament) ist der Versions-Eintrag dein Audit-Log.
- Der **Grund der Änderung** macht aus dem Eintrag eine sprechende Notiz, statt eines anonymen Zeitstempels.

Die Versions-Historie selbst lebt im Bereich "Verlauf" der Profilansicht (siehe dort, wenn dieser Bereich in einer späteren Iteration eigene Doku bekommt). Aktuell ist sie eine Liste mit Datum, Versions-Nummer und Änderungsgrund.

## Was nicht in den Basisdaten ist

Das Profil hat über die Basisdaten hinaus weitere Felder, die in Phase 2 noch nicht über das gleiche Bearbeitungsformular zugänglich sind:

- **Größe und Gewicht:** Aktuell aus dem Import übernehmbar, eigenes Bearbeitungsformular folgt.
- **Hausarzt:** Name und Kontaktdaten, eigenes Formular geplant.
- **Gewichtsverlauf:** Mehrere Werte über Zeit, eigene Bearbeitung folgt.
- **Kontextnotizen:** Frei formulierter Hintergrundtext, eigenes Formular folgt.
- **Externe Referenzen und Warnsignale:** Werden im Verlauf der Phase 2 mit eigenen Bearbeitungen versehen.

Wenn diese Felder beim Profil-Import vorhanden waren, bleiben sie unangetastet, wenn du die Basisdaten bearbeitest. Phylax überschreibt sie nicht versehentlich.

## Eigenes Profil und Stellvertreterprofil

Phylax kennt zwei Profil-Typen:

- **Eigenes Profil (`self`):** Du selbst bist die dokumentierte Person.
- **Stellvertreterprofil (`proxy`):** Du pflegst das Profil für jemand anderen, z.B. ein Kind oder einen älteren Verwandten. Im Feld **Stellvertretend für** kannst du eintragen, für wen.

Der Profiltyp ist nicht im Standard-Bearbeitungsformular der Basisdaten; er wird beim Anlegen eines Profils gesetzt und ändert sich selten. Multi-Profile pro Browser kommen in einer späteren Phase, aktuell sind ein bis zwei Profile praktikabel.

## Weiterlesen

- Wie du Bearbeitungen über mehrere Geräte hinweg synchron hältst: [Sicherung erstellen und wiederherstellen](../backup/create-and-restore.md).
- Wenn du ein bestehendes Profil aus Markdown importieren willst: [Profil importieren](../data/profile-import.md).
- [Beobachtungen](observations.md), [Laborwerte](lab-values.md), [Supplemente](supplements.md), [Offene Punkte](open-points.md) leben oberhalb der Basisdaten und nutzen sie als Rahmen.

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
