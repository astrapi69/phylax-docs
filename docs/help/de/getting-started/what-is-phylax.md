# Was ist Phylax

Phylax ist eine persönliche, datensouveräne Gesundheitsplattform, die im Browser läuft. Du erstellst und pflegst dein medizinisches Profil als lebendes Dokument: Beobachtungen, Laborwerte, Supplemente, offene Punkte und Profil-Versionen wachsen über Jahre mit dir mit, verschlüsselt mit deinem Master-Passwort, ausschließlich auf deinem Gerät.

## Die Grundidee

Klassische Gesundheits-Apps verwalten dich. Phylax nicht. Phylax versteht Gesundheit als einen vom Menschen geführten Prozess: du beobachtest, du erkennst Muster, du regulierst dich selbst, und du dokumentierst, was wirklich passiert ist. Ärztinnen, Befunde und Therapien sind Teil davon, aber sie sind nicht die Quelle der Wahrheit über deinen Körper, du bist es.

Diese Idee heißt "Lebende Gesundheit". Phylax ist die App-gewordene Form davon.

## Warum gibt es Phylax

Wer chronisch krank ist, wer eine ältere Person betreut, wer einen langwierigen Klärungsprozess durchläuft, kennt das Problem: Befunde liegen verstreut, Eigenbeobachtungen werden vergessen, beim nächsten Arzttermin fehlt der rote Faden. Klassische Apps lösen das nicht, weil sie auf Tracking abzielen ("Schritte heute"), nicht auf Verstehen ("Welches Muster zeigt sich seit drei Monaten").

Phylax ist der Versuch, einen Werkzeugkasten zu bauen, der Verstehen unterstützt, ohne dafür deine Daten in fremde Hände zu legen.

## Für wen ist Phylax

- Menschen mit chronischen oder ungeklärten Beschwerden, die einen Faden über Jahre festhalten wollen
- Angehörige, die ein Profil stellvertretend pflegen (Elternteil, Kind)
- Menschen, die KI als Strukturierungspartner einsetzen wollen, ohne ihre Gesundheitsdaten an eine Cloud zu übergeben
- Alle, die Software wollen, die ihnen gehört und nicht andersherum

## Was Phylax anders macht

Apple Health, Google Fit und Tracker-Apps speichern deine Daten in der Cloud des Herstellers. Phylax nicht. Es gibt keinen Phylax-Server. Deine Daten verlassen deinen Browser nicht, außer du exportierst sie aktiv. Es gibt keine Telemetrie, keine Analytics, keinen Werbe-Tracker. Phylax ist Open Source, der Quellcode liegt offen auf GitHub.

KI ist optional und Bring-Your-Own-Key: wenn du sie nutzen willst, gibst du deinen eigenen API-Schlüssel von OpenAI oder Anthropic ein. Phylax fungiert nur als Vermittler, deine Anfragen gehen direkt vom Browser an den von dir gewählten Anbieter.

## Was Phylax NICHT ist

- **Kein Medizinprodukt.** Phylax stellt keine Diagnosen und gibt keine Therapieempfehlungen.
- **Kein Cloud-Sync.** Daten bleiben pro Gerät. Wechsel zwischen Geräten geht über die `.phylax`-Sicherung, nicht über automatischen Sync.
- **Kein Arzt-Portal.** Phylax ist für dich, nicht für deine Ärztin. Sie bekommt einen Ausdruck oder PDF-Export, falls du das möchtest.
- **Keine Auto-Interpretation.** Wenn du einen Laborwert eingibst, sagt Phylax dir nicht, was er bedeutet. Diese Aufgabe bleibt bei deiner Ärztin.

## Weiterlesen

- [Erste Schritte](first-steps.md) führt dich von "App geöffnet" bis zum ersten Profil.
- Die Idee dahinter beschreibt die Artikel-Serie "Lebende Gesundheit": [Übersicht und alle Teile](https://asterios-raptis.medium.com/lebende-gesundheit-die-serie-0193f66df9a3).
- Phylax ist Open Source: [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax).

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
