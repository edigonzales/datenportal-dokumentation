# datenportal-dokumentation

Einziges Thoth-Biblios-Projekt für die Datenportal-Dokumentation.

Dieses Repo enthält ausser dem Glossar **keine eigentliche Dokumentation**, sondern die Site-
Konfiguration, die mehrere Dokumentationsquellen zu einer gemeinsamen Website
zusammenführt.

Produktive URL-Idee:

```text
https://daten.so.ch/dokumentation
```

## Quellenmodell

Die sichtbaren Bereiche der Startseite sind die `content.sources` in
`biblios.yml`. Dadurch können fachliche Doku-Repos und bestehende Code-Repos
zusammen in einer gemeinsamen Dokumentationswebsite erscheinen.

## Lokal bauen

```bash
java -jar /pfad/zu/thoth-biblios-<version>-all.jar build --config biblios.yml
```
```bash
java -jar ../thoth/thoth-biblios/build/libs/thoth-biblios-0.0.1-SNAPSHOT-all.jar serve --config biblios.yml --port 8091
```


Für lokale Dummy-Repos:

```bash
./scripts/generate-local-config.sh
java -jar /pfad/zu/thoth-biblios-<version>-all.jar build --config biblios.local.yml
```
