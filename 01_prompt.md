# Prompt: PowerPoint-Präsentation aus dem Vortragsskript erzeugen

> **Verwendung:** Diesen Prompt zusammen mit der Datei `02-astrofotografie-vortrag.md` an ein KI-System mit Dateierzeugung und Codeausführung geben (z. B. Claude mit Dateierstellung, ChatGPT mit Code Interpreter, Copilot-Agent mit Python). Die Markdown-Datei ist die **einzige inhaltliche Quelle**.
>
> Alles unterhalb der Linie ist der eigentliche Prompt.

---

## Rolle

Du bist ein erfahrener Präsentationsdesigner und Python-Entwickler. Du erzeugst aus einem strukturierten Markdown-Vortragsskript eine vollständige, professionell gestaltete PowerPoint-Datei (`.pptx`) für einen deutschsprachigen VHS-Vortrag über Physik und Technik der Astrofotografie. Das Publikum besteht aus interessierten Laien ohne Vorkenntnisse. Die Präsentation wird in einem abgedunkelten Raum per Beamer gezeigt. Deshalb gilt: wenig Text, ein Gedanke pro Folie, klare Bilder und einfache Schaubilder.

## Aufgabe

Lies die angehängte Datei `02-astrofotografie-vortrag.md` vollständig und erzeuge daraus die Datei **`astrofotografie-vortrag.pptx`** (16:9, 13,333 × 7,5 Zoll).

Verwende Python mit `python-pptx` (oder `pptxgenjs`, falls verfügbar und besser geeignet). Schreibe ein wiederholbares Generatorskript `build_pptx.py`, das die Markdown-Datei **parst** und nicht Folieninhalte von Hand einträgt. So lässt sich die Präsentation nach Änderungen am Skript neu erzeugen.

## Struktur der Quelldatei

Die Quelle ist so aufgebaut:

- `# Kapitel N – …` → Kapitel (12 Stück). Der Text nach dem Gedankenstrich ist der Kapiteltitel, ein Teil nach dem Doppelpunkt ist die Leitfrage des Kapitels.
- `## Folie N – …` → eine Folie (64 Stück)
- `## Reservefolie A–L – …` → Anhangfolien (12 Stück, nur Kurzbeschreibung)
- Innerhalb jeder Folie die Abschnitte:
  - `### Folieninhalt` → **sichtbarer Folientext**
  - `### Visualisierung` → Beschreibung des gewünschten Bildes oder Schaubilds (fehlt bei einzelnen Folien)
  - `### Kernaussage` → zentrale Botschaft
  - `### Sprechtext` → ausformulierter Vortragstext
  - `### Interaktion` → Hinweis zur Publikumsbeteiligung (nur an einigen Folien, z. B. 2, 10, 14, 16)
  - `### Übergang` → Überleitung zur nächsten Folie (fehlt bei der letzten Folie)
- Am Ende vieler Folieninhalte stehen ein oder zwei **Merkzeilen** im Format `**Physik dahinter:** …` und `**Für Ihr Foto:** …`. Sie sind sichtbarer Folientext und werden besonders gestaltet (siehe Design).
- Der Abschnitt `Hinweise zur Verwendung` (mit den Unterabschnitten Roter Faden, Niveau, Zeitplanung), die `Empfohlene Repository-Struktur` und der `Lizenzhinweis` am Ende sind **keine Folien**. Übernimm sie nicht. Der Dateikopf (Titel, Untertitel, Leitidee) wird nur auf der Titelfolie verwendet, soweit er dort im Folieninhalt steht.

Beachte:

- Innerhalb von `### Folieninhalt` kommen Markdown-Überschriften der Ebenen `#` und `##` vor. Sie gehören zum Folieninhalt und beenden den Abschnitt nicht. Ein Abschnitt endet erst beim nächsten `###`-Abschnitt oder bei `---`.
- Als Folientitel gilt die erste `#`-Überschrift im Folieninhalt, nicht die Überschrift `## Folie N – …`.
- **Ausnahme:** Hat ein Folieninhalt keine `#`-Überschrift (Folie 51 besteht nur aus einer Tabelle), verwende den Titel aus `## Folie N – …` als sichtbaren Folientitel.
- Tabellen können leere Zellen enthalten (Folie 25). Lass diese Zellen leer.

## Folienaufbau

Erzeuge in dieser Reihenfolge:

1. **Titelfolie** = Folie 1 (Vollbild-Platzhalter, großer Titel).
2. Vor den Folien jedes weiteren Kapitels (Kapitel 2–12) eine **Kapiteltrennfolie** (Kapitelnummer groß, Kapiteltitel, Leitfrage, sonst leer). Kapitel 1 bekommt keine Trennfolie, da Folie 1 direkt beginnt.
3. Die **Folien 2–64** in Originalreihenfolge, jeweils genau eine Folie. Die Kapiteltrennfolie steht vor der ersten Folie ihres Kapitels.
4. Eine **Trennfolie „Reserve- und Vertiefungsfolien"**.
5. Die **Reservefolien A–L**, jeweils eine Folie mit Titel und Kurztext.

Erwartete Gesamtzahl: 64 + 11 Kapiteltrennfolien + 1 Anhangtrennfolie + 12 Reservefolien = **88 Folien**. Prüfe die Zahl am Ende. Leite Zahlen im Skript aus der Quelle ab und schreibe sie nicht fest in den Code. Weicht die Quelle später ab, passt sich das Ergebnis an.

## Inhaltsregeln (sehr wichtig)

1. **Nichts erfinden.** Alle sichtbaren Texte stammen wörtlich aus `### Folieninhalt`. Ändere weder Formulierungen noch Zahlen, Fachbegriffe oder Reihenfolge. Ergänze keine Fakten, Zitate, Bilder oder Quellenangaben.
2. **Nichts Sichtbares verlieren.** Jede Aufzählung, Tabelle, Nummerierung, Fettung, Merkzeile und jeder Merksatz im Folieninhalt muss erscheinen. Das Zeichen `*kursiv*` (z. B. Fußnote auf Folie 17, Erklärzeilen auf Folie 62) wird kursiv und in gedämpfter Farbe gesetzt. Die Zeichen `≈`, `√`, `°`, `″`, `µ`, `Hα`, `−` und `÷` müssen in der gewählten Schrift korrekt dargestellt werden. Prüfe das im gerenderten Ergebnis.
3. **Sprechtext gehört in die Notizen.** Schreibe in die Referentennotizen jeder Folie in dieser Reihenfolge:
   - `KERNAUSSAGE:` + Text
   - `SPRECHTEXT:` + vollständiger Text (Absätze erhalten, Merksätze eingeschlossen)
   - `INTERAKTION:` + Text (nur wenn vorhanden)
   - `ÜBERGANG:` + Text
   - `VISUALISIERUNG:` + Beschreibung aus der Quelle (als Hilfe beim Einfügen der echten Bilder)

   Kernaussage, Sprechtext, Interaktion und Übergang erscheinen **nie** auf der Folie selbst.
4. **Reservefolien:** Titel und Beschreibungstext aus der Quelle sichtbar auf der Folie (die Aufzählung bei Reservefolie G ebenfalls). Keine Notizen nötig, außer die Folie hat selbst Text dafür.
5. Textlänge: Wenn Text für die Folie zu lang wird, verkleinere die Schrift maximal bis 20 pt. Kürze nie den Inhalt. Teile in diesem Fall die Inhalte in zwei Spalten oder auf zwei Folien auf (Folie dann mit „(1/2)" und „(2/2)" im Titel) und melde dies im Abschlussbericht. Beachte, dass einige Folien Tabelle, Aufzählung, Merkzeile und Bild gleichzeitig enthalten (z. B. Folien 8, 15, 18, 32, 34). Plane dort das Layout bewusst, zum Beispiel Tabelle links und Bild rechts, Merkzeile als Band unten.
6. **Rechenbeispiele und Formeln** (z. B. Folie 18: Bogensekunden pro Pixel, Folie 28: 500 ÷ Brennweite, Folie 33: √Anzahl) werden als eigene, groß gesetzte Formelzeile hervorgehoben (Bernstein, mindestens 28 pt), nicht als Fließtext. Verwende keine Formelobjekte, sondern normalen Text mit Unicode-Zeichen.

## Umgang mit Bildern

Es gibt **keine Bilddateien**. Alle Visualisierungen sind eigene Fotos der Referentin oder des Referenten, die später manuell eingesetzt werden.

- Erzeuge für jede Visualisierung einen **Bildplatzhalter**: Rechteck mit dunkler Füllung (etwas heller als der Folienhintergrund), gestrichelter Rahmen in der Akzentfarbe, dezentes Kamerasymbol oder „BILD" als Wasserzeichen und darunter in kleiner Schrift (14 pt) eine **Kurzbeschreibung** aus dem `### Visualisierung`-Abschnitt, z. B. `Eigenes Bild: dasselbe Motiv in vier Entwicklungsstufen`.
- Wenn die Visualisierung mehrere Bilder beschreibt (z. B. „vier Aufnahmen nebeneinander", „sechs Stufen", „drei Zwischenbilder"), erzeuge **genau so viele Platzhalter** in einem passenden Raster und beschrifte jeden einzeln, soweit die Quelle die Inhalte nennt (z. B. Folie 3: Mond, Milchstraße, Nebel, All-Sky/Sternspuren; Folie 33: 1, 4, 16, 64 Aufnahmen; Folie 18: drei Monde bei 50, 400 und 1.000 mm).
- Platzhalter müssen sich in PowerPoint **einfach ersetzen** lassen. Lege daher jeden Platzhalter als eigenes, benanntes Shape an (`BILD_Folie12_1`, `BILD_Folie12_2`, …) und setze einen Alternativtext. Alternativ nutze echte Bildplatzhalter (Picture Placeholder) im Layout, wenn das mit der Bibliothek zuverlässig geht.
- Folie 1 und Folie 64: Der Hintergrundplatzhalter füllt die gesamte Folie, der Text liegt auf einer halbtransparenten dunklen Fläche, damit er lesbar bleibt.
- **Schaubilder baust du selbst** aus nativen, editierbaren PowerPoint-Formen (keine Bitmaps), wenn die Visualisierung als „natives Schaubild" oder rein schematisch beschrieben ist. Die Physikfolien leben von diesen Schaubildern. Beschrifte sie nur mit Begriffen und Zahlen aus dem Folieninhalt oder aus dem `### Visualisierung`-Abschnitt. Kurven und Skizzen sind **schematisch** und werden mit „Schema" gekennzeichnet. Erfinde keine Messwerte.
  - Folie 4: Reise Stern → Atmosphäre → Linse/Spiegel → Sensor → Rechner (Pfeile), darunter die acht nummerierten Stationen
  - Folie 8: Helligkeitsleiter von der Sonne bis zur Sichtbarkeitsgrenze
  - Folie 9: Wellenlinie (oben kurz, unten lang) und Spektrumband von 400 bis 700 nm mit Blau, Grün, Rot
  - Folie 11: Kreislaufschaubild Wolke → Sternentstehung → junger Stern → Nebel → Sternende → Wolke
  - Folie 13: Spektrum mit drei hellen Linien bei 501 nm (OIII), 656 nm (Hα), 672 nm (SII)
  - Folie 15: Erde mit dünner Lufthülle und drei Lichtwegen (90°, 30°, 10°)
  - Folie 19: zwei Eimer im Regen, der zweite doppelt so breit
  - Folie 22: Raster aus Eimern mit unterschiedlichen Füllständen
  - Folie 23: 4 × 4-Pixelraster im Bayer-Muster (Rot, Grün, Blau) neben einem Mono-Raster
  - Folie 24: schematische QE-Kurve über die Wellenlänge mit markierten Bereichen für Blau, Grün, Rot und Hα
  - Folie 29 und 30: schematische Darstellung azimutaler und parallaktischer Montierung mit Himmelspol
  - Folie 35: Spektrum mit Durchlassbereichen eines Breitband- und eines Schmalbandfilters
  - Folie 36: Zuordnung SII → Rot, Hα → Grün, OIII → Blau
  - Folie 46: Drehachsen im AZ-Modus (senkrecht) und im EQ-Modus (zum Himmelspol geneigt)
  - Folie 47: Prozesskette mit acht Schritten (aus dem Folieninhalt)
  
  Wenn ein Schaubild zusätzlich eigene Fotos verlangt, ergänze Bildplatzhalter daneben.
- Verwende **keine Stockfotos, keine KI-generierten Himmelsbilder und kein Clipart.**

## Tabellen

Markdown-Tabellen (Folien 8, 15, 18, 25, 32, 34, 38, 46, 51, 55) werden zu **echten PowerPoint-Tabellen**: Kopfzeile in der Akzentfarbe, Zeilen abwechselnd leicht abgesetzt, Text mindestens 20 pt, linke Spalte fett. Bei Folie 38 (vier Spalten), Folie 46 und Folie 51 (je drei Spalten) darf die Tabelle die ganze Folienbreite nutzen.

## Design

Ziel: ruhig, hochwertig, nachtfreundlich, wie ein Planetariumsvortrag. Dunkles Design mit hohem Kontrast für Beamer.

**Farben**
- Hintergrund: tiefes Nachtblau `#0B1020` (alternativ ein sehr subtiler Verlauf nach `#121A33`)
- Haupttext: `#F2F4F8`
- Akzent 1 (Titel-Linie, Aufzählungszeichen, Tabellenkopf): warmes Bernstein `#F5A623`
- Akzent 2 (Sekundär, Pfeile, Rahmen): Eisblau `#6FB7FF`
- Gedämpfter Text (Beschriftungen): `#9AA4B8`
- Keine Rottöne außer für Warnungen (Reservefolie G, Sonnenfotografie): dort `#FF5A5A` als Akzent.

**Schrift**
- Überschriften: `Calibri Light` oder `Segoe UI Semibold` (nur Schriften verwenden, die auf Windows und macOS vorhanden sind, Fallback `Arial`)
- Fließtext: `Calibri` oder `Segoe UI`
- Größen: Titel 40 pt, Untertitel 28 pt, Aufzählungen 26–28 pt, Tabellen und Beschriftungen mindestens 18 pt. **Nichts unter 18 pt** außer Bildunterschriften der Platzhalter (14 pt).
- Linksbündig, maximal 6 Aufzählungspunkte pro Folie sichtbar gedacht, großzügiger Weißraum.

**Layout**
- Eigenes **Folienmaster** mit sauberen Layouts anlegen: Titelfolie, Kapiteltrenner, Titel + Aufzählung, Titel + Bild, Titel + 2 Spalten, Titel + Tabelle, Titel + Prozesskette, Nur Titel. Verwende diese Layouts, nicht lose Textfelder auf leeren Folien. Dadurch bleiben Gliederungsansicht und Barrierefreiheit nutzbar.
- Titel oben links, dünne Bernsteinlinie darunter, Fußzeile mit Folienzahl rechts unten und links dem Text „Astrofotografie · VHS-Vortrag" in gedämpfter Farbe. Titelfolie und Kapiteltrenner ohne Fußzeile.
- Satzspiegel: Rand mindestens 0,6 Zoll.
- **Merkzeilen** (`**Physik dahinter:**` und `**Für Ihr Foto:**`) erscheinen als abgesetztes Band am unteren Folienrand über die volle Satzspiegelbreite, **nie** mitten im Aufzählungstext:
  - „Physik dahinter": Band in dunklem Eisblau-Ton, linker Balken und Label in Eisblau `#6FB7FF`, Text weiß
  - „Für Ihr Foto": Band in dunklem Bernstein-Ton, linker Balken und Label in Bernstein `#F5A623`, Text weiß
  - Stehen beide auf einer Folie, stapeln sie sich (Physik oben, Foto unten)
  - Das Label (z. B. „Physik dahinter") steht fett vor dem Text. Mindestens 20 pt.
- Layoutwahl pro Folie nach Inhalt:
  - Text + ein Bild → Text links (ca. 45 %), Bildplatzhalter rechts
  - Bildvergleich (3–6 Bilder) → Raster, Text als kurze Zeile darüber oder darunter
  - Tabelle + Bild (z. B. Folie 18) → Tabelle links, Bild rechts
  - Nur Text → Aufzählung links, großzügig, ggf. mit großem dezentem Symbol
  - Zitate in Anführungszeichen (Folie 2, 61) → große, gut lesbare Zitatzeilen
  - Schaubild-Folien (siehe Umgang mit Bildern) → Schaubild als Hauptfläche, Text kompakt daneben oder darunter
- Kapiteltrenner: große Kapitelnummer in Bernstein, Kapiteltitel in Weiß, Leitfrage (Teil nach dem Doppelpunkt) in Eisblau darunter, kleine Sternpunkte als dezentes dekoratives Muster (native Formen, sparsam).

**Betonungen**
- `**fett**` aus dem Markdown wird fett. Merksätze und die jeweils wichtigste Aussage einer Folie (falls im Folieninhalt fett gesetzt, z. B. Folie 3) in Bernstein hervorgehoben.
- Aufzählungen mit kleinem Bernstein-Punkt, nummerierte Listen (Folien 4, 11, 22, 33, 63) mit Nummern in Bernstein.

## Besondere Folien

- **Folie 2** (Warum sind Sie heute hier?): Die vier Aussagen sollen **nacheinander** per Einblend-Animation (Fade/Erscheinen, bei Klick) erscheinen. Wenn sich Animationen in deiner Bibliothek nicht zuverlässig setzen lassen, ergänze die Animations-XML direkt oder erzeuge als Ersatz vier aufeinander aufbauende Folien und melde das im Abschlussbericht. Bei der ersten Variante bleibt die Zahl 88 bestehen.
- **Folie 4** (Wir folgen dem Weg des Lichts): Roadmap. Die acht Stationen als nummerierte Reihe mit dem Schaubild „Stern → Atmosphäre → Linse/Spiegel → Sensor → Rechner". Dieses Motiv darf auf den Kapiteltrennfolien als kleine Fortschrittsleiste wiederkehren, wobei die aktuelle Station hervorgehoben ist. Ordne die Kapitel den Stationen zu: Kapitel 2 = Objekt, 3 = Luft, 4 = Optik, 5 = Sensor, 6 = Erddrehung, 7 und 8 = Signal, 9 = Werkzeuge, 10 und 11 = Aufnahme und Bearbeitung.
- **Folien 8, 15, 18, 32, 34:** Tabelle plus Aufzählung plus Merkzeile. Tabelle zentral, übrige Zeilen kompakt, Merkzeile unten. Bei Folie 18 steht die Formel `Bogensekunden pro Pixel ≈ 206 × Pixelgröße (µm) ÷ Brennweite (mm)` als große Formelzeile.
- **Folie 30** hat die Titel-Überschrift „Präzision statt bloßer Tragfähigkeit" und zwei Spalten (`## Azimutale Montierung`, `## Parallaktische Montierung`) mit Bildplatzhalter für das schematische Bild beider Montierungen.
- **Folie 36:** Die Hubble-Palette (SII → Rot · Hα → Grün · OIII → Blau) als Farbzuordnungsgrafik, zusätzlich drei Schwarz-Weiß-Platzhalter und ein Farbplatzhalter.
- **Folie 46** (Azimutal oder äquatorial): Dreispaltige Vergleichstabelle, daneben zwei Bildplatzhalter (AZ-Aufbau, EQ-Aufbau) und das Schaubild der Drehachsen.
- **Folie 51:** nur Tabelle, Titel aus `## Folie 51 – …` (siehe Struktur).
- **Folie 62:** vier Blöcke (Wunsch als Zitat, darunter das empfohlene System, darunter kursiv die Begründung). Layout 2 × 2.
- **Folie 63:** sieben nummerierte Aussagen, jede in einer Zeile mit großer Bernstein-Ziffer. Keine Visualisierung nötig.
- **Folie 64:** Aufzählung der Geräte und die Zeile „Fragen und Demonstration" als große, hervorgehobene Schlusszeile.
- **Reservefolie G** (Sonnenfotografie): Warnfarbe Rot als Akzent, Sicherheitsliste gut lesbar.
- Folien mit Merksatz (z. B. Folie 3) zeigen den Merksatz nur dann, wenn er auch im Folieninhalt steht. Steht er nur im Sprechtext, gehört er in die Notizen.

## Qualitätssicherung (Pflicht)

Führe nach der Erzeugung selbst folgende Prüfungen durch und korrigiere Fehler, bevor du das Ergebnis meldest:

1. **Anzahl:** Die Datei enthält 88 Folien. Jede der 64 Hauptfolien und 12 Reservefolien ist vorhanden, in der richtigen Reihenfolge. 11 Kapiteltrennfolien und 1 Anhangtrennfolie sind eingefügt.
2. **Text-Abgleich:** Vergleiche automatisch den sichtbaren Text jeder Folie mit dem Abschnitt `### Folieninhalt` der Quelle (Wörter müssen übereinstimmen, Markdown-Zeichen ausgenommen). Es dürfen keine Wörter fehlen oder hinzukommen. Das schließt alle Merkzeilen ein: 24 × „Physik dahinter" und 28 × „Für Ihr Foto" müssen als Bänder vorhanden sein. Zähle sie nach.
3. **Notizen:** Jede der 64 Hauptfolien hat Notizen mit Kernaussage, Sprechtext und Übergang (Ausnahme: die letzte Folie hat keinen Übergang). Der Notizentext stimmt mit der Quelle überein. Folien mit Interaktion haben zusätzlich den Eintrag `INTERAKTION:`.
4. **Überlauf:** Kein Text ragt über Folienrand oder Shape hinaus, keine Überlappungen. Rendere die Datei zu Bildern (z. B. mit LibreOffice: `soffice --headless --convert-to pdf`, danach `pdftoppm -png -r 50`) und sieh dir mindestens die Folien 1, 4, 9, 13, 18, 23, 32, 34, 38, 46, 51, 62, 63 und 64 sowie eine Kapiteltrennfolie und eine Reservefolie visuell an. Das sind die dichtesten Folien. Korrigiere Auffälligkeiten.
5. **Kontrast und Lesbarkeit:** Keine Schrift unter 18 pt (Ausnahme: Platzhalterbeschriftung), Kontrast zwischen Text und Hintergrund mindestens 7:1. Sonderzeichen (`≈ √ ° ″ µ Hα −`) werden korrekt dargestellt.
6. **Platzhalter:** Jedes in der Quelle verlangte Bild hat einen benannten, ersetzbaren Platzhalter. Zähle sie und nenne die Gesamtzahl. Schaubilder sind native Formen, keine Bilder.
7. **Datei öffnet sich** fehlerfrei (z. B. erneutes Laden mit `python-pptx`).

## Ausgabe

Liefere:

1. `astrofotografie-vortrag.pptx`
2. `build_pptx.py` (Generatorskript, lauffähig, mit kurzen Kommentaren nur dort, wo nötig)
3. Einen **kurzen Abschlussbericht** (maximal 15 Zeilen) mit: Folienanzahl, Anzahl der Bildplatzhalter, Anzahl der nativen Schaubilder, Folien, die du wegen Textmenge aufgeteilt oder anders gelöst hast, verwendete Schriften, bekannte Einschränkungen (z. B. Animation Folie 2), und eine Liste der Folien, bei denen du eine Gestaltungsentscheidung treffen musstest.

Stelle keine Rückfragen, sondern triff vernünftige Entscheidungen und dokumentiere sie im Abschlussbericht. Beginne direkt mit der Umsetzung.
