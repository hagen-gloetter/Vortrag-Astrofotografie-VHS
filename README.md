# Astrofotografie – Physik und Technik des Nachthimmels

![Inhalt: CC BY 4.0](https://img.shields.io/badge/Inhalt-CC%20BY%204.0-lightgrey)
![Code: MIT](https://img.shields.io/badge/Code-MIT-green)
![Sprache: Deutsch](https://img.shields.io/badge/Sprache-Deutsch-blue)

**Ein VHS-Vortrag über Astrofotografie: vom Photon zum Bild – und welches Werkzeug dazu passt.**

Dieses Repository enthält das vollständige Vortragsskript, die Anleitung zum Erzeugen der PowerPoint-Folien und Prompts für erklärende Bilder. Der Vortrag richtet sich an interessierte Laien ohne Vorkenntnisse in Physik oder Fotografie.

> **Leitidee:** Es gibt nicht das beste Gerät. Es gibt nur ein geeignetes Werkzeug für ein bestimmtes Ziel. Die Physik des Lichts zeigt, welches.

---

## Worum geht es?

Der Vortrag folgt dem **Weg des Lichts** und stellt erst am Ende die Geräte vor:

**Objekt → Atmosphäre → Optik → Sensor → Himmelsbewegung → Rauschen und Stacking → Filter → Werkzeuge → Aufnahme → Bearbeitung**

Jedes Gerät, vom Smartphone über die DSLR und das Smart-Teleskop bis zum klassischen Teleskop, ist eine bestimmte Kombination derselben physikalischen Bausteine. Wer diese Bausteine versteht, kann jedes System selbst einordnen.

| | |
|---|---|
| **Format** | VHS-Vortrag mit anschließenden Fragen und Live-Demonstration |
| **Dauer** | ca. 90–110 Minuten |
| **Umfang** | 64 Folien in 12 Kapiteln, dazu 12 Reservefolien |
| **Niveau** | VHS-Kurs: erst ein Alltagsbild, dann der Fachbegriff, wenige Formeln mit Rechenbeispiel |
| **Sprache** | Deutsch |

### Gliederung

1. Einstieg: Was möchten wir fotografieren?
2. Licht und Objekte: Was strahlt uns an?
3. Die Atmosphäre: Was passiert unterwegs?
4. Die Optik: Wie sammeln wir das Licht?
5. Der Sensor: Wie wird Licht gezählt?
6. Die Erddrehung: Wie lange dürfen wir belichten?
7. Das Signal: Wie wird das Bild sauber?
8. Himmelshintergrund und Filter
9. Die Werkzeuge: Welches Gerät passt?
10. Der vollständige Aufnahme-Workflow
11. Vom Rohbild zum fertigen Ergebnis
12. Abschluss

### Beispiele für Alltagsbilder im Vortrag

- Pixel sind **Eimer im Regen**, Photonen die Regentropfen
- Der Sternenhimmel dreht sich wie ein **Karussell**
- Ein Gas leuchtet wie eine **Neonröhre**
- Flächenhelligkeit ist **Butter auf dem Brot**
- Ein Schmalbandfilter ist **eine Stimme im lauten Raum**

---

## Inhalt des Repositories

| Datei | Zweck |
|---|---|
| [`02-astrofotografie-vortrag.md`](02-astrofotografie-vortrag.md) | **Das Vortragsskript.** Pro Folie: Folieninhalt, Visualisierung, Kernaussage, Sprechtext, Übergang |
| [`01_prompt.md`](01_prompt.md) | Prompt, mit dem ein KI-System aus dem Skript die PowerPoint-Datei erzeugt |
| [`04_bildprompts.md`](04_bildprompts.md) | Bildprompts und Stilvorgaben für 28 erklärende Schaubilder und Alltagsbilder |
| [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md) | Hinweise zu Fremdinhalten und Marken |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | So kann man Korrekturen und Verbesserungen beitragen |
| [`CHANGELOG.md`](CHANGELOG.md) | Änderungsverlauf |
| [`CITATION.cff`](CITATION.cff) | Zitierhinweis |
| [`LICENSE`](LICENSE) | MIT-Lizenz für Skripte und Quellcode |
| [`LICENSE-CONTENT.md`](LICENSE-CONTENT.md) | CC BY 4.0 für Texte, Folien und Prompts |

### Aufbau einer Folie im Skript

```text
## Folie N – Titel
### Folieninhalt      sichtbarer Text auf der Folie (inkl. Merkzeilen)
### Visualisierung    gewünschtes Bild oder Schaubild
### Kernaussage       zentrale Botschaft
### Sprechtext        ausformulierter Vortragstext
### Interaktion       Frage ans Publikum (nur an einzelnen Folien)
### Übergang          Verbindung zur nächsten Folie
```

Am Ende vieler Folien stehen zwei Merkzeilen:

- **Physik dahinter:** der physikalische Grund in einem Satz
- **Für Ihr Foto:** die praktische Konsequenz in einem Satz

---

## So wird aus dem Skript eine Präsentation

1. **PowerPoint erzeugen:** Geben Sie [`01_prompt.md`](01_prompt.md) zusammen mit [`02-astrofotografie-vortrag.md`](02-astrofotografie-vortrag.md) an ein KI-System mit Dateierzeugung und Codeausführung (zum Beispiel ChatGPT mit Code Interpreter oder einen Coding-Agenten). Das System erzeugt `astrofotografie-vortrag.pptx` und ein wiederholbares Skript `build_pptx.py`. Das Ergebnis sind 88 Folien: 64 Hauptfolien, 11 Kapiteltrenner, 1 Anhangtrenner und 12 Reservefolien. Der Sprechtext landet in den Referentennotizen.
2. **Eigene Bilder einsetzen:** Die meisten Visualisierungen sind **eigene Aufnahmen**. Die erzeugte Datei enthält dafür benannte Platzhalter (`BILD_FolieN_k`), die Sie in PowerPoint ersetzen.
3. **Erklärende Schaubilder:** Mit den Prompts aus [`04_bildprompts.md`](04_bildprompts.md) lassen sich passende Illustrationen im einheitlichen Stil „Planetarium" erzeugen. Genaue Teile wie Spektrallinien oder das Bayer-Raster werden nativ in PowerPoint gebaut.

---

## Quellen und Grundlagen

- Angaben zum Smart-Teleskop (Öffnung, Brennweite, Gesichtsfeld, Filter, EQ-Modus) stammen aus der Herstellerangabe zum Seestar S50 Pro. Die Anleitung selbst ist urheberrechtlich geschützt und **nicht Teil dieses Repositories** (siehe [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md)).
- Die physikalischen Aussagen wurden sorgfältig geprüft, ersetzen aber keine Fachbegutachtung. Fehler melden Sie bitte als Issue (siehe [`CONTRIBUTING.md`](CONTRIBUTING.md)).

---

## Lizenz

Das Repository verwendet zwei Lizenzen:

| Was | Lizenz |
|---|---|
| Texte, Vortragsskript, Folien und Prompts | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.de), siehe [`LICENSE-CONTENT.md`](LICENSE-CONTENT.md) |
| Skripte und Quellcode (zum Beispiel `build_pptx.py`) | [MIT](LICENSE) |
| Fremdbilder und Fremdinhalte | jeweilige Ursprungslizenz, dokumentiert in [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md) |

Sie dürfen den Vortrag halten, anpassen und weitergeben, auch in eigenen Kursen und gegen Honorar. Bitte nennen Sie die Quelle und weisen Sie auf Änderungen hin. Eigene Fotos des Autors sind **nicht** automatisch freigegeben (siehe [`LICENSE-CONTENT.md`](LICENSE-CONTENT.md)).

## Autor

Hagen Glötter, [GitHub](https://github.com/hagen-gloetter)

## Mitmachen

Fehler im Skript, unklare Erklärungen oder Verbesserungsvorschläge sind willkommen. Lesen Sie dazu [`CONTRIBUTING.md`](CONTRIBUTING.md).
