# Hintergrund

Diese Seite ist eine Brücke. Phylax steht auf einer Idee ("Lebende Gesundheit"), einer Architektur (Browser-only, verschlüsselt) und einer offenen Roadmap. Wer mehr wissen will, findet die Substanz an drei Orten.

## Die Idee: Lebende Gesundheit

Phylax setzt das Konzept der Lebenden Gesundheit um, eine vierteilige Artikel-Serie von Asterios Raptis. Der Kern: Gesundheit ist ein vom Menschen geführter Prozess, kein vom System verwalteter Zustand.

- [Lebende Gesundheit, Übersicht und alle Teile](https://asterios-raptis.medium.com/lebende-gesundheit-die-serie-0193f66df9a3)

Die vier Teile decken ab:

1. Gesundheit als nutzergeführter Prozess
2. Selbstanwendung: Beobachten, Mustern erkennen, Selbstregulation
3. Stellvertreterprofile (älterer Verwandter, abhängiges Kind)
4. KI als Strukturierungspartner, nicht als Diagnostiker

## Die Architektur

Phylax ist eine reine Browser-Anwendung. Kein Backend, kein Cloud-Sync, keine Telemetrie.

- **Datenhaltung:** IndexedDB im Browser, vollständig verschlüsselt mit AES-256-GCM.
- **Schlüsselableitung:** PBKDF2 mit SHA-256, 1.200.000 Iterationen, aus deinem Master-Passwort.
- **Schlüssel-Lebensdauer:** Nur im Arbeitsspeicher, nie persistent. Auto-Lock nach 5 Minuten Inaktivität (konfigurierbar) leert den Schlüssel.
- **Tech-Stack:** React 18, TypeScript, Dexie.js (IndexedDB-Wrapper), Web Crypto API, Tailwind CSS, vite-plugin-pwa.

Architektur-Entscheidungen sind als ADRs (Architecture Decision Records) im Repo dokumentiert.

## Bedrohungsmodell in einem Satz

Phylax schützt vor: gestohlenem Gerät bei gesperrter App, neugierigen Mitlesenden, Cloud-Diebstahl (kein Cloud-Speicher), Telemetrie-Lecks (keine Telemetrie).

Phylax schützt nicht vor: Keyloggern auf dem Gerät, kompromittiertem Betriebssystem, schwachem Master-Passwort, körperlichem Zwang, Browser-Exploits.

## Warum kein Backend

Datensouveränität. Sobald Daten irgendwo gespeichert werden, das nicht dein Gerät ist, sind sie potenziell für andere zugänglich (Datenbank-Lecks, Anbieter-Zugriff, Pflicht zur Herausgabe). Phylax umgeht das, indem es kein Backend hat.

Das hat Kosten: kein automatischer Geräte-Sync, kein Cross-Device-Login, keine zentrale Recovery. Diese Kosten sind beabsichtigt und vom Konzept her unauflösbar.

## Quellcode und Roadmap

Phylax ist Open Source.

- Repository: [github.com/astrapi69/phylax](https://github.com/astrapi69/phylax)
- Lizenz: MIT
- Aktueller Stand und Phasen-Plan: [ROADMAP.md](https://github.com/astrapi69/phylax/blob/main/docs/ROADMAP.md)
- Konzept-Dokument: [CONCEPT.md](https://github.com/astrapi69/phylax/blob/main/docs/CONCEPT.md)
- Architektur-Entscheidungen: [docs/decisions/](https://github.com/astrapi69/phylax/tree/main/docs/decisions)

## Diese Dokumentation

Die Dokumentation, die du gerade liest, lebt in einem eigenen Repository:

- [github.com/astrapi69/phylax-docs](https://github.com/astrapi69/phylax-docs)

Korrekturen, fehlende Topics oder Übersetzungs-Wünsche werden dort als Issues oder Pull Requests aufgenommen.

Stand: 2026-04-27 (Iteration 1, erste Inhalte)
