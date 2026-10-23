# WindSMP Join-Logs

Aufnahmen vom **23.10.2026** mit AFKLocal **0.14.2-diagnostics (Build 24)**.

| Edition | Accountname | Serveradresse | Empfangene Fehlermeldung |
| --- | --- | --- | --- |
| **Java** | **Shadowpigi** | `windsmp.net:25565` | `Unable to connect to spawn-1: multiplayer.disconnect.configuration_error` |
| **Bedrock** | **Pigi8983** | `windsmp.net:19132` | `Unable to connect to spawn-2: Unerwarteter Fehler während der Konfiguration` |

## Dateien

- [Reine Join-Logs](WindSMP-Nur-Join-2026-10-23.txt): je ein aufgezeichneter Verbindungsversuch, vom Verbindungsstart bis zum Server-Disconnect; 44 Java- und 14 Bedrock-Paketmetadaten.
- [Seit wann die Verbindungen scheitern](Seit-wann-ausgefallen.txt): letzte bestätigte erfolgreiche Kontrolle am 17.10.2026; der aktuelle Fehler ist am 18.10.2026 bereits dokumentiert. Der genaue erste Ausfallzeitpunkt ist nicht gespeichert.

## Beobachteter Abbruch

- **Java / Shadowpigi:** empfangenes `disconnect`-Paket `0x02` in der Konfigurationsphase nach Registry-Daten und Tags; noch kein Weltbeitritt.
- **Bedrock / Pigi8983:** empfangenes `disconnect`-Paket `0x05` nach `resource_pack_stack` und gesendeter Client-Antwort; noch kein `start_game`.

Beide Abbruchpakete wurden erfolgreich gelesen. Die Paketfolge zeigt die Abbruchstelle und die Servermeldung; sie belegt nicht den internen Auslöser auf dem Server. Ein als `written` protokolliertes Paket belegt den lokalen Schreibvorgang, keine erfolgreiche Verarbeitung durch den Server.

Die Original-Logzeitstempel sind **UTC (+00:00)**; am Aufnahmetag entspricht Europe/Berlin **UTC+2**. Die Zeitstempel vor den gesammelten `packet-trace`-Zeilen sind deren Ausgabezeit; `milliseconds` bezeichnet den relativen Zeitpunkt innerhalb der Sitzung.

Enthalten sind ausschließlich Verbindungsdiagnosen und historische Beobachtungen. Keine Zugangstokens, Passwörter, Paketnutzdaten oder privaten Chats.

