# NOVA Netzwerk – Version 1.2

## Veröffentlichung auf GitHub Pages

**Alle Dateien aus diesem Paket** ins Wurzelverzeichnis des GitHub-Repositories `Mxrkus21/nova-website` hochladen (nicht nur `index.html`):

- `index.html`
- `projekte.html`
- `styles.css`
- `script.js`
- `projects.js`
- `favicon.svg`

Bereits vorhandene rechtlich geprüfte `impressum.html` und `datenschutz.html` beibehalten. Fehlende Seiten vor Veröffentlichung erstellen.

### Warum das Design auf GitHub Pages anders aussah

Die Seite lädt das Design aus `styles.css`. Wenn nur `index.html` hochgeladen wurde oder `styles.css` im falschen Verzeichnis liegt, fehlt das Styling. Lade alle Dateien gemeinsam hoch. `?v=12` in den Referenzen umgeht zudem alte CSS/JS-Versionen im Browsercache.

### Projektanzeige

`projekte.html` lädt **offene GitHub Issues** aus `Mxrkus21/nova-website` über die öffentliche GitHub REST API. Es sind keine API-Schlüssel und kein Server nötig. Issues müssen für das Repository aktiviert sein.

- Die Ansicht ist ausschließlich lesend.
- Klick auf eine Projektkarte öffnet die Diskussion auf GitHub.
- Ohne offene Issues wird ein ehrlicher Leerzustand gezeigt.
- GitHub-API-Limits oder Ausfälle werden abgefangen und mit einem Link zu GitHub quittiert.
- Pull Requests werden herausgefiltert.
- Die ersten 100 offenen Issues werden geladen; bei mehr Projekten ist später Paginierung erforderlich.
- Für die öffentlichen Projektbeiträge gelten GitHubs Nutzungs- und Datenschutzbedingungen.

### Prüfen

1. Auf GitHub kontrollieren, dass `styles.css` neben `index.html` liegt.
2. Nach Deployment die Seite mit Strg+F5 neu laden.
3. `/nova-website/projekte.html` öffnen.
4. GitHub Issues aktivieren und ein echtes Test-Issue erstellen, dann prüfen, ob es erscheint.
5. Impressum und Datenschutz prüfen.
