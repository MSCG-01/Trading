# Trading

Minimale Grundlage für ein mögliches späteres Trading-Projekt. Dieses Repository enthält derzeit **keinen Trading-Algorithmus, keine Broker-Anbindung und keine Orderausführung**. Eine Strategie, Programmiersprache und Broker-Schnittstelle sind noch nicht festgelegt.

## Geplanter Arbeitsablauf

1. Anforderungen und Risiken einer Strategie schriftlich festhalten.
2. Daten und Annahmen prüfen; Regeln für Tests und Auswertung definieren.
3. Erst danach Code in kleinen, überprüfbaren Schritten entwickeln und mit Testdaten bzw. einem Paper-Konto prüfen.
4. Eine mögliche Live-Anbindung gesondert freigeben, mit festen Risikolimits, Überwachung und einer Möglichkeit zum sofortigen Stoppen.

Diese Liste ist eine Entwicklungsreihenfolge, keine Handelsfreigabe. Nichts in diesem Repository darf derzeit Orders platzieren.

## Lokale Konfiguration

`.env.example` zeigt nur mögliche Namen für spätere lokale Einstellungen. Falls eine Integration diese Werte tatsächlich benötigt, kann lokal eine `.env` erstellt werden. Die Beispielwerte sind leer; Zugangsdaten gehören niemals in dieses öffentliche Repository. Für produktive Zugänge einen geeigneten Secret Manager verwenden.

## Umgang mit Broker- und API-Schlüsseln

- Nur die minimal nötigen Rechte vergeben; Auszahlungen und Transfers für Trading-Schlüssel deaktivieren, wenn der Anbieter das erlaubt.
- Zuerst ausschließlich getrennte Test- oder Paper-Zugänge verwenden. Live-Zugänge erst nach eigener Prüfung und ausdrücklicher Freigabe einrichten.
- Schlüssel weder in Quellcode noch in Commits, Issues, Pull Requests, Screenshots, Chats oder Logs ablegen. Auch `.env` und lokale Exportdateien nicht hochladen.
- `.gitignore` schützt nur vor versehentlichem Hinzufügen neuer Dateien. Vor jedem Commit mit `git status` und `git diff --cached` prüfen, was veröffentlicht wird.
- Bei einem versehentlich veröffentlichten Schlüssel sofort beim Anbieter widerrufen oder rotieren; das Löschen aus dem letzten Commit allein reicht nicht, weil Git-Historie erhalten bleibt.

**Status:** Grundstruktur ohne Strategieentscheidung und ohne ausführbaren Handel.
