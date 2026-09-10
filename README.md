# datenportal-dokumentation

Einziges Thoth-Biblios-Projekt für die Datenportal-Dokumentation.

Dieses Repo enthält ausser dem Glossar **keine eigentliche Dokumentation**, sondern die Site-
Konfiguration, die mehrere Dokumentationsquellen zu einer gemeinsamen Website
zusammenführt.

Die gebaute Seite wird via Forgejo Action auf Codeberg Pages und via GitHub Action auf GitHub Pages deployed:

- Codeberg Pages: https://edigonzales.codeberg.page/datenportal-dokumentation/
- GitHub Pages: https://edigonzales.github.io/datenportal-dokumentation/

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
java -jar ../thoth/thoth-biblios/build/libs/thoth-biblios-0.0.1-SNAPSHOT-all.jar serve --config biblios.yml --port 8091 \
--use-local-working-tree

```

```bash
java -jar /Users/stefan/sources/thoth/thoth-biblios/build/libs/thoth-biblios-0.0.1-SNAPSHOT-all.jar serve \
--config ./biblios.yml \
--port 8091 \
--use-local-working-tree
```




Für lokale Dummy-Repos:

```bash
./scripts/generate-local-config.sh
java -jar /pfad/zu/thoth-biblios-<version>-all.jar build --config biblios.local.yml
```


Mögliche Hintergrundfarben für Cards:

| Zielgruppe | Hintergrund | Wirkung | Kontrast Text / Link |
|---|---|---|---|
| Benutzer | `#E8F1FF` | ruhig, vertrauenswürdig, blau | 13.3:1 / 4.76:1 |
| Administration | `#FFF4E6` | aufmerksam, organisatorisch, amber | 13.9:1 / 4.99:1 |
| Entwickler | `#F1ECFF` | technisch, eigenständig, violett | 13.1:1 / 4.69:1 |
