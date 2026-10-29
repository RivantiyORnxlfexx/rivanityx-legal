# Technische Befunde zu RivanityX

Stand: 29. Oktober 2026

## Prüfungsumfang und Einschränkung

Geprüft wurde das im VS-Code-Workspace geöffnete Repository `RivantiyORnxlfexx/rivanityx-legal` sowie dessen versionierter Dateibaum auf dem Branch `main`. Das Repository ist öffentlich. Der Dateibaum enthält ausschließlich `README.md`, `privacy.html` und `terms.html`. Es liegen hier weder Bot-Quellcode noch Datenbankdateien, SQLite-Schemata, Migrationen, Deployment-Dateien, Workflow-Konfigurationen oder Umgebungsvariablen vor.

Daher war keine Prüfung der tatsächlichen Laufzeitverarbeitung des Bots möglich. Die folgenden Betreiberangaben sind nicht durch Code oder Konfiguration verifiziert. Die vorhandenen Rechtstextdateien sind Entwürfe und kein technischer Nachweis.

## Bestätigte Tatsachen aus dem geprüften Repository

- Das GitHub-Konto `RivantiyORnxlfexx` besitzt das öffentliche Repository `rivanityx-legal`; der tatsächliche Repositoryname für ein mögliches Pages-Schema ist damit bekannt.
- Im Repository sind statische HTML-Dateien für Datenschutz und Nutzungsbedingungen vorhanden. Sie enthalten Textvorlagen und Platzhalter.
- Der aktuelle Dateibaum enthält keine HTML-Startseite, CSS-Datei, Bot-Anwendung, Datenbank, Migrationen, Konfiguration, Tests oder GitHub-Actions-/Pages-Workflow.
- Die GitHub-Pages-API meldet für dieses Repository `404 Not Found`. Zum Prüfzeitpunkt ist daher keine veröffentlichte Pages-Site über diese Repository-Konfiguration nachweisbar.
- Der vorhandene Entwurf `terms.html` nennt Moderationsfunktionen und Warnungen/Bans. Diese Aussagen werden durch keinen im Repository verfügbaren Bot-Code belegt. Der Entwurf enthält außerdem einen verbliebenen doppelten Abschnitt „7. Schlussbestimmungen“.
- Die vorhandene `privacy.html` ist eine allgemeine Vorlage und dokumentiert keine konkret verifizierte Verarbeitung.

## Daten und Speicherorte: keine Codebestätigung möglich

| Datenart oder Verarbeitung | Technischer Befund |
| --- | --- |
| SQLite-Tabellen, Spalten und Migrationen | Keine Datenbankdatei, kein Schema und keine Migration im geprüften Repository; Tabellen und Spalten sind unbekannt. |
| Software-Keys | Keine Implementierung verfügbar. Erzeugung, Speicherung, Zuordnung zu Personen, Aktivierung, Validierung, Widerruf und Löschung sind nicht prüfbar. |
| Aktivierungs- und Gerätekennungen | Keine Implementierung verfügbar. Es ist nicht feststellbar, ob Gerätekennungen, IP-Adressen oder andere Identifikatoren verarbeitet werden. |
| Discord-Nutzer-IDs, Server-IDs, Benutzernamen | Kein Bot-Code verfügbar. Die tatsächliche Erhebung, Speicherung und Übermittlung ist nicht prüfbar. |
| Moderationsdaten | Kein Bot-Code verfügbar. Der vorhandene Rechtstext erwähnt Warnungen und Bans, belegt deren Speicherung oder Funktion aber nicht. |
| Technische Protokolle und Analyse | Keine Logging-, Telemetrie- oder Analyseimplementierung im geprüften Dateibaum. Daraus folgt nicht, dass solche Verarbeitung in der Laufzeit oder beim Hosting ausgeschlossen ist. |
| Speicherort und Backups | Kein Hosting- oder Backup-Code und keine Konfiguration verfügbar. Speicherort, Verantwortlichkeiten, Sicherungskopien und deren Löschung sind unbekannt. |
| Export und Löschung | Keine Export- oder Löschbefehle und keine automatischen Aufbewahrungs- oder Löschabläufe im geprüften Repository auffindbar. Eine manuelle Löschung kann daher nicht technisch bestätigt werden. |

## Externe Anbieter und Datenübermittlungen

- Im geprüften Dateibaum sind keine API-Aufrufe, Webhooks, Lizenzserver, HTTP-Clients oder externen Analyse-Dienste implementiert oder konfiguriert.
- Discord ist als Plattform im vorhandenen Nutzungsbedingungen-Entwurf genannt. Mangels Bot-Code lässt sich nicht prüfen, welche Discord-API-Daten der Bot tatsächlich erhält oder welche Inhalte er an Discord übermittelt.
- Aus dem Repository sind keine weiteren externen Empfänger identifizierbar. Der Betreiber hat angegeben, dass weitere externe Dienste genutzt werden, diese aber noch nicht identifiziert sind. Empfänger, Zweck, Datenkategorien, Auftragsverarbeitung und mögliche Drittlandübermittlungen müssen noch ermittelt werden.

## Betreiberangaben, noch nicht technisch bestätigt

Die folgenden Angaben stammen aus der Aufgabenbeschreibung und konnten nicht im Code verifiziert werden:

- Botname: RivanityX.
- Hauptzweck: Software-Keys erstellen und verwalten.
- Datenbank: SQLite.
- Hosting: Cloud; konkreter Hosting-Anbieter unbekannt.
- Moderationssanktionen: manuell.
- Angegebene Speicherdauer: bis zur manuellen Löschung.
- Es bestehen weitere externe Dienste, deren Namen und Funktionen noch unbekannt sind.
- Betreiber: Privatperson; vollständiger Name und erforderliche Betreiberangaben fehlen.
- Zielgruppe: allgemeine Discord-Server.
- Vorgesehener Datenschutzkontakt: `dobberfuhljan@gmail.com`; Bestätigung als veröffentlichbare Kontaktadresse steht noch aus.

Diese Angaben dürfen nicht als durch den Quellcode bestätigte Tatsachen dargestellt werden. Insbesondere belegt die Aussage „bis zur manuellen Löschung“ weder eine implementierte Löschmöglichkeit noch eine tatsächlich festgelegte Aufbewahrungsdauer. Erforderlichkeit, Löschfristen, Backups und mögliche gesetzliche Aufbewahrungspflichten sind zu klären.

## Offene Fragen für den Betreiber

1. Wo befindet sich das Bot-Repository mit vollständigem Quellcode, Datenbankdefinitionen und Migrationshistorie?
2. Welche Key-Felder werden gespeichert, wie werden Keys Personen oder Discord-Konten zugeordnet und welche Aktivierungsdaten (insbesondere IP- oder Gerätekennungen) fallen an?
3. Welche Discord-Ereignisse und Identifikatoren werden verarbeitet? Werden Moderationsentscheidungen oder Sanktionen gespeichert?
4. Welche konkreten Cloud-, Datenbank-, Logging-, Monitoring-, E-Mail-, Lizenz- und sonstigen externen Dienste werden eingesetzt, und welche Daten erhalten sie?
5. Wo werden Bot, SQLite-Datei und Backups gehostet? In welchen Ländern liegen Primärdaten und Sicherungskopien, wer kann darauf zugreifen und wann werden Kopien gelöscht?
6. Welche Funktionen erlauben den Export, Widerruf und die Löschung von Keys oder sonstigen personenbezogenen Daten? Wie werden Sicherungskopien und Protokolle behandelt?
7. Gibt es automatisierte Löschfristen oder werden Daten tatsächlich unbegrenzt bis zu einer manuellen Aktion gespeichert?
8. Welche vollständigen Betreiberangaben und welche Rechtsgrundlagen sind für die beschriebenen Verarbeitungen zutreffend?
9. Darf `dobberfuhljan@gmail.com` als Datenschutzkontakt veröffentlicht werden?
10. Ist GitHub Pages als Hosting-Anbieter für diese statische Informationsseite gewünscht? Falls ja, sind die Pages-Einstellungen derzeit nicht aktiviert.

## Zusammenfassung

Eine codebasierte Datenschutz- oder Funktionsbeschreibung für den Bot ist mit dem aktuell geöffneten Repository nicht belastbar möglich. Die Website kann nur vorläufige, klar markierte Betreiberangaben und Prüfhinweise enthalten, bis das Bot-Repository und die offenen technischen Informationen vorliegen. Es wurden bei der Prüfung keine Secrets, Tokens, Passwörter oder privaten Konfigurationswerte ausgegeben.
