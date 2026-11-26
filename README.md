# persodyn-qna

Fragen und Antworten zur PerSoDyn-Studie – eine einfache, statische Webseite, gebaut mit [Quarto](https://quarto.org).

Jede Änderung auf dem `main`-Branch wird automatisch über GitHub Actions gebaut und auf GitHub Pages veröffentlicht.

---

## Anleitung für Maren 👋

### Was liegt wo?

| Datei | Wofür? |
|---|---|
| `index.qmd` | **Der Inhalt der Seite.** Hier arbeitest du fast ausschließlich. |
| `_quarto.yml` | Einstellungen (Seitentitel, Design, Inhaltsverzeichnis). Selten nötig. |
| `impressum.qmd`, `datenschutz.qmd` | Rechtliche Pflichtseiten (im Footer verlinkt). |
| `custom.scss`, `fonts/` | Schaltet Google Fonts ab und liefert die Schrift (Source Sans 3, OFL) lokal aus – bitte nicht entfernen (Datenschutz). |
| `persodyn.scss` | Das PerSoDyn-Design (Farben, Schrift, Karte, Überschriften) – übernommen aus dem Studien-Theme im `persodyn`-Repo. |
| `styles.css` | Optische Feinheiten (optional), u. a. die Logos in der Kopfleiste. |
| `images/` | PerSoDyn- und Uni-Münster-Logo, Favicon. |
| `.github/workflows/publish.yml` | Automatische Veröffentlichung. Bitte nicht ändern. |
| `_site/` | Erzeugte Webseite – wird automatisch gebaut, nicht von Hand bearbeiten (ist nicht im Git). |

### Fragen bearbeiten

`index.qmd` ist ganz normales Markdown. Die Struktur:

```markdown
## Themenblock          ← erscheint als Abschnitt im Inhaltsverzeichnis

### Eine Frage?         ← jede Frage ist eine Überschrift mit drei #

Die Antwort als normaler Text darunter.
```

- **Neue Frage:** einfach eine `### Frage?`-Zeile plus Antwort in den passenden Abschnitt kopieren.
- **Neuer Themenblock:** eine `## Thema`-Zeile hinzufügen.
- **Reihenfolge ändern:** Blöcke ausschneiden und verschieben.
- Leerzeilen zwischen Überschrift und Text nicht vergessen.

Nützliche Formatierungen:

```markdown
**fett**, *kursiv*
[Linktext](https://example.org)
[E-Mail](mailto:studie@example.org)

- Aufzählung
- noch ein Punkt

::: {.callout-note}
## Hinweis
Ein hervorgehobener Hinweiskasten. Statt "note" geht auch "tip", "warning" oder "important".
:::
```

Jede Frage bekommt automatisch einen Link-Anker – wenn du mit der Maus über eine Frage fährst, erscheint ein kleines Link-Symbol. So kann man Teilnehmenden direkt den Link zu einer bestimmten Antwort schicken.

### Vorschau auf dem eigenen Rechner (empfohlen)

1. [Quarto installieren](https://quarto.org/docs/get-started/) (einmalig).
2. Im Terminal in diesem Ordner ausführen:

   ```bash
   quarto preview
   ```

3. Es öffnet sich ein Browserfenster. Jedes Mal, wenn du `index.qmd` speicherst, aktualisiert sich die Vorschau automatisch. Beenden mit `Strg+C`.

Alternativ geht das auch in RStudio oder VS Code (mit Quarto-Erweiterung) über den **Render/Preview**-Button.

### Veröffentlichen

Änderungen committen und auf `main` pushen – fertig. Nach ca. 1–2 Minuten ist die neue Version online.
Den Fortschritt siehst du auf GitHub im Reiter **Actions** (grüner Haken = online, rotes X = Fehler, meist ein Tippfehler im Markdown – die Fehlermeldung steht im Log).

Ohne Git geht's auch direkt auf github.com: `index.qmd` öffnen → Stift-Symbol (Edit) → ändern → **Commit changes**.
