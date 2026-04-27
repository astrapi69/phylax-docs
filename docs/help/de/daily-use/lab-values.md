# Laborwerte

Laborwerte in Phylax bilden ab, wie Befunde in der Realität ankommen: ein Laborbefund pro Termin, mit vielen Einzelwerten innerhalb. Diese zweistufige Struktur (Bericht plus Werte) hält die Daten so, wie sie auch im PDF stehen, und macht spätere Auswertung über mehrere Berichte hinweg überhaupt erst möglich.

## Bericht und Werte

Wenn du Laborwerte in Phylax eintragen willst, legst du zuerst einen **Laborbefund** an. Der Befund trägt die rahmensetzenden Informationen:

- **Datum (Pflicht):** Wann wurde der Befund erstellt. Sortierung der Berichte folgt diesem Datum.
- **Labor (optional):** Welches Labor hat den Befund erstellt.
- **Arzt (optional):** Welche Ärztin hat ihn angeordnet.
- **Bericht-Nr. (optional):** Falls auf dem PDF eine eindeutige Nummer steht.
- **Kontext (optional):** Was war der Anlass. Beispiel: "Routine-Check Hausarzt", "Nachkontrolle Schilddrüse nach drei Monaten Einnahme".

Innerhalb dieses Berichts legst du dann die einzelnen **Laborwerte** an. Pro Wert:

- **Kategorie (Pflicht):** Frei vergebene Gruppierung, z.B. "Blutbild", "Nierenwerte", "Schilddrüse", "Vitamine".
- **Parameter (Pflicht):** Was wurde gemessen, z.B. "Hämoglobin", "TSH", "Vitamin D".
- **Ergebnis (Pflicht):** Der gemessene Wert, z.B. "13.7", "1:40", "<5", "positiv". Frei als Text, weil Befunde unterschiedlich formatiert sind.
- **Einheit (optional):** z.B. "g/dl", "ng/ml", "mg/l".
- **Referenzbereich (optional):** Wie das Labor den Bereich angibt, z.B. "13.5-17.5", "1:40", "<10".
- **Bewertung (optional):** Eine Einordnung. Übliche Werte: "normal", "erhöht", "erniedrigt", "kritisch". Phylax schlägt diese vier vor, du kannst aber frei eintragen, was zum Befund passt.

## Warum diese Trennung

Ein Befund kommt selten allein. Wer einen Bluttest macht, bekommt zwanzig oder fünfzig Werte zurück, die alle vom selben Datum, Labor und Anlass stammen. Würde Phylax jeden Wert einzeln behandeln, müsstest du Datum und Labor zwanzigmal eintragen. Mit Bericht und Werten getrennt füllst du den Rahmen einmal und kannst dich auf die Werte konzentrieren.

Die Trennung erlaubt es zukünftig auch, Trends über mehrere Berichte hinweg zu zeigen, sobald diese Auswertungen geschrieben sind.

## Bericht und Werte anlegen

Im Bereich "Laborwerte" der Profilansicht.

1. **Neuer Befund** klicken.
2. Datum eintragen, optional Labor, Arzt, Bericht-Nr., Kontext.
3. Speichern. Du landest in der Bericht-Detailansicht.
4. Im Bericht: **Wert hinzufügen** klicken.
5. Kategorie wählen oder neu eintragen, dann Parameter, Ergebnis, Einheit, Referenzbereich, Bewertung.
6. Speichern. Wert erscheint sofort, gruppiert nach Kategorie.
7. Schritte 4 bis 6 wiederholen für alle Werte des Berichts.

Auf dem Smartphone empfiehlt es sich, den Bericht in Ruhe abzutippen und auf das Auto-Lock zu achten: nach fünf Minuten Inaktivität sperrt Phylax sich von selbst. Lange Pausen während der Eingabe lösen einen Lock aus, ungesicherte Eingaben gehen dann verloren.

## Bewertungs-Werte

Phylax schlägt vier Begriffe für die Bewertung vor:

- **normal:** Im Referenzbereich.
- **erhöht:** Oberhalb des Referenzbereichs.
- **erniedrigt:** Unterhalb des Referenzbereichs.
- **kritisch:** Stark außerhalb des Bereichs, sofortige Beachtung erforderlich.

Diese sind nur Vorschläge, weil Phylax keine medizinische Einschätzung trifft. Wenn ein Befund eine andere Sprache nutzt (z.B. "im Normbereich", "auffällig"), kannst du das frei übernehmen.

## Bearbeiten und Löschen

Werte und Berichte können nachträglich angepasst werden, wenn beim Eintragen ein Tippfehler unterläuft oder das Labor eine Korrektur schickt.

Beim Löschen eines Berichts werden alle zugeordneten Werte mitgelöscht. Phylax fragt vorher nach. Einzelne Werte lassen sich getrennt löschen, ohne den Bericht anzutasten.

## Phylax interpretiert nicht

Wichtig: Phylax sagt dir nicht, was ein Wert bedeutet. Wenn dein TSH leicht erhöht ist, hörst du das von Phylax nicht. Diese Aufgabe liegt bei deiner Ärztin. Phylax dokumentiert, sortiert und macht die Werte über Jahre wiederfindbar; die Bewertung kommt von einer Person mit medizinischer Ausbildung.

Auch beim ePA-Import strukturiert die KI nur, sie interpretiert nicht. Der Wert "TSH 4.8" wird übernommen, samt Referenzbereich aus dem PDF; die Frage, ob 4.8 für dich relevant ist, bleibt beim Arztgespräch.

## Weiterlesen

- Befunde aus PDF-Dokumenten automatisch übernehmen: [ePA-Import](../data/epa-import.md).
- Wie Beobachtungen und Laborwerte zusammenhängen (Querverweise): [Beobachtungen](observations.md).
- Sicherung deiner Befunde: [Sicherung erstellen und wiederherstellen](../backup/create-and-restore.md).

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
