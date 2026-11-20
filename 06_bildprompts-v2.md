# Bildprompts für die Kompaktfassung (Version 2)

Diese Datei gehört zu [`05-astrofotografie-vortrag-v2.md`](05-astrofotografie-vortrag-v2.md) (40 Folien). Sie baut auf [`04_bildprompts.md`](04_bildprompts.md) auf und wiederholt dessen Prompts **nicht**, damit es nur eine Stelle gibt, an der ein Prompt gepflegt wird.

## Kurzfassung

| Gruppe | Folien | Was zu tun ist |
|---|---|---|
| **Prompt aus 04 wiederverwenden** | 5, 6, 7, 8, 9, 10, 21, 24, 25, 26, 29, 32, 33 (13 Folien) | Prompt aus `04_bildprompts.md` nehmen, Beschriftung für die Kompaktfassung beachten (Tabelle in Abschnitt 2) |
| **Neu in dieser Datei** | 11, 17, 20, 28, 31, 39 (6 Folien) | Prompts in Abschnitt 3 |
| **Eigene Fotos oder Screenshots, kein KI-Bild** | 1, 4, 12, 13, 14, 15, 16, 18, 19, 22, 23, 30, 34, 35, 36, 37, 38, 40 | Liste in Abschnitt 4 |
| **Ohne Bild** | 2, 3, 27 | Tabelle, Text oder native Formen |

Die Bilder kommen in die Platzhalter `BILD_FolieN_k` der PowerPoint-Datei. **N ist die Foliennummer der Version 2.**

---

## 1. Stil und Werkzeuge

Der bisherige flache „Planetariums-Illustration“-Stil wird durch den gemeinsam festgelegten **technisch-wissenschaftlichen Stil mit dezenter Science-Fiction-Ästhetik** ersetzt. Die Bildsprache orientiert sich an präzisen wissenschaftlichen Lehrgrafiken und hochwertigen optischen Laborvisualisierungen, nicht an Cartoons, japanischen Erklärbildern oder überladenem Cyberpunk. Formate bleiben **4:3 oder 1:1**, wie je Folie angegeben.

**Verbindliche Gestaltungsregeln:**

- **Hintergrund:** tiefes Navy `#0B1020`, höchstens sanfter Verlauf nach `#121A33`; keine hellen Flächen, außer wenn für eine sachliche Darstellung nötig.
- **Konturen und Konstruktion:** präzise, feine cyan-/eisblaue Linien (`#6FB7FF`), dezente geometrische Hilfslinien und Achsen; keine sinnlosen HUD-Elemente.
- **Licht und Akzente:** sparsam eingesetztes Bernstein `#F5A623` für Photonen, Strahlen, Bewegung und Hervorhebungen; Off-White `#F2F4F8` für neutrale Elemente.
- **Materialien:** technisch plausible transparente Glasbauteile, Linsen, Sensoren, dezentes gebürstetes Metall; kontrollierte Lichtreflexe statt starker Lens Flares.
- **Naturfarben:** bei Mond, Sternen, Nebeln und realen Umgebungen erlaubt, aber wissenschaftlich plausibel und nicht überdramatisiert.
- **Komposition:** ein eindeutiger didaktischer Gedanke pro Bild, klare Blickführung, ausreichende Randabstände, ausgewogene Bildfüllung; kein überflüssiger Dekor.
- **Textfrei:** **keine** Buchstaben, Zahlen, Beschriftungen, Formeln, Skalen, Logos, Marken oder Wasserzeichen im generierten Bild. Alle Texte kommen nativ in PowerPoint.
- **Wissenschaftliche Genauigkeit:** Richtung, Anzahl, Proportionen, optische Achsen und Vorher-Nachher-Bezüge anhand der Prüfpunkte kontrollieren. Exakte Spektrallinien, Winkel, Bayer-Muster, Diagrammkurven und Zahlen nativ erstellen.
- **Fotos:** eigene astronomische Aufnahmen und Gerätefotos nicht durch erfundene „echte“ Bilder ersetzen. Generierte Nebel bleiben generisch und eindeutig illustrativ.

**Verbindlicher Stilblock (an jeden KI-Prompt anhängen):**

```text
Style: precise scientific educational illustration with a sophisticated, restrained near-science-fiction optical laboratory aesthetic. Deep midnight navy background (#0B1020), subtle gradient toward #121A33. Crisp thin luminous cyan and ice-blue engineering contours (#6FB7FF), subtle physically meaningful construction guides, warm amber (#F5A623) only for light paths, photons, motion or key highlights, and off-white (#F2F4F8) neutral details. Plausible transparent optical glass, sensor structures and brushed-metal hardware where appropriate. Controlled realistic material shading and restrained soft glow. Clean disciplined geometry, accurate visual relationships, high contrast suitable for projection, balanced composition with clear subject and safe margins. Natural celestial colors only where scientifically relevant. More like a high-quality university physics textbook figure combined with a polished optical engineering visualization than a cartoon. No text, no letters, no numbers, no captions, no formulas, no labels, no logos, no watermark.
```

**Negativblock:**

```text
text, letters, numbers, captions, labels, formulas, equations, axes with numbers, logos, brand marks, watermark, cartoon, anime, flat playful vector art, pastel textbook art, busy cyberpunk, decorative holographic HUD, meaningless grids, excessive lens flare, clutter, malformed hands, extra fingers, invented astronomical photographs
```

**Arbeitsweise:** Englischen Motivprompt mit dem Stilblock kombinieren und das vorgegebene Seitenverhältnis angeben. Vor Freigabe die konkreten Prüfpunkte kontrollieren. Wenn eine physikalisch exakte Darstellung per KI nicht zuverlässig gelingt, **nur den anschaulichen Teil generieren** und präzise Pfeile, Messwerte, Kurven oder Raster in PowerPoint ergänzen.

**Für wiederverwendete Prompts aus `04_bildprompts.md` gilt ausdrücklich:** Deren alter Stilblock und Negativblock werden **nicht** übernommen. Ausschließlich den Motivinhalt wiederverwenden und mit dem hier definierten neuen Stilblock erzeugen. Bereits passende technisch-wissenschaftliche Bilder können unverändert wiederverwendet werden.
---

## 2. Wiederverwendung von Prompts aus `04_bildprompts.md`

Die **Motivbeschreibungen** bleiben erhalten, werden aber immer mit dem **neuen Stilblock aus Abschnitt 1** kombiniert. Der alte Planetariums-/Vektorstil wird nicht übernommen. Die Spalte „Anpassung“ nennt, was sich in der Kompaktfassung ändert.

| Folie (v2) | Thema | Prompt in `04_bildprompts.md` | Anpassung |
|---|---|---|---|
| 5 | Wir fotografieren Vergangenheit | Folie 7 | Beschriftung wie dort: 1,3 Sekunden · 8 Minuten · 1.300 Jahre · 2,5 Millionen Jahre |
| 6 | Seeing: Warum Sterne flimmern | Folie 14 | Beschriftung: ruhige Luft · unruhige Luft |
| 7 | Die Öffnung sammelt das Licht | Folie 19 | Beschriftung: Öffnung · 1× · 4× |
| 8 | Brennweite = Zoom | Folie 16 (Arm und Hand) | Hand prüfen (fünf Finger). Die ineinanderliegenden Himmelsrahmen (24 mm, 200 mm, Teleskop) bauen Sie nativ oder mit eigenem Foto |
| 9 | Der Bildsensor: Pixel sind kleine Eimer | Folie 22 (Eimerraster) und Folie 23 (Sonnenbrillen) | Zwei Bilder: `BILD_Folie9_1` Eimerraster, `BILD_Folie9_2` Sonnenbrillen. Das **Bayer-Muster** bauen Sie nativ |
| 10 | Die Erde dreht sich | Folie 27 (Karussell) | Beschriftung: schnell außen · langsam innen · Himmelspol |
| 21 | Azimutal oder äquatorial | Folie 46 | Beschriftung: AZ · EQ · Himmelspol · Norden. Eigene Fotos des Seestar ersetzen die Illustration, sobald vorhanden |
| 24 | Die Montierung trägt das Bild | Folie 30 | Beschriftung: azimutal · parallaktisch · Himmelspol |
| 25 | Das modulare System, Filter als Sieb | Folie 35 | Nur das Bild vom Sieb verwenden. Beschriftung: Himmelslicht · Filter · Hα · OIII · Stadtlicht |
| 26 | Schmalband mit dem Profi-System | Folie 36 | Zuordnung SII → Rot, Hα → Grün, OIII → Blau nativ beschriften |
| 29 | Standort und Planung | Folie 34 | Beschriftung: dunkler Himmel · Stadthimmel |
| 32 | Stacking | Folie 33 | Für „1, 4, 16, 64 Aufnahmen" besser **ein** sauberes Bild erzeugen und das Rauschen in einem Bildprogramm unterschiedlich stark hinzufügen |
| 33 | Das dunkle Bild | Folie 58 | Beschriftung: linear · gestreckt |

**Wichtig:** Die Foliennummern in der mittleren Spalte beziehen sich auf die **Vertiefungsfassung** (Version 1, 64 Folien). In `04_bildprompts.md` stehen sie in den Überschriften `### Folie N – …`.

---

## 3. Neue Prompts

### Folie 11 – Vier Stufen, vier Ziele  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** eine Treppe mit vier Stufen und dem passenden Gerät und Ziel auf jeder Stufe. Betont wird Wachstum, nicht Rangfolge.

```text
A scientifically precise four-step progression of astronomical observing setups, seen from a slightly elevated side angle, left to right. Exactly four broad equal-width steps, modestly rising rather than suggesting a hierarchy. Step one: generic smartphone on tiny tripod with a small crescent Moon icon above. Step two: generic DSLR with telephoto lens on sturdy tripod with a subtle Milky Way band above. Step three: compact unbranded all-in-one smart telescope on small tripod with a generic red-teal emission nebula above. Step four: classical refractor on a mechanically plausible equatorial mount with polar shaft and counterweight, with a generic spiral galaxy above. Devices are distinct, correctly supported, comparable in visual importance, with clean metal and glass surfaces and fine cyan engineering outlines. Each celestial target floats separately over its matching device; no arrows implying one device is inherently superior. No writing or logos.
```

**Beschriftung in PowerPoint:** 1 bis 4 und die Namen der Stufen aus der Folie.
**Prüfen:** genau vier Stufen, vier unterscheidbare Geräte, Reihenfolge von links nach rechts wie auf der Folie, keine Logos.

### Folie 17 – Der Star-Tracker  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** die Kamera dreht sich mit dem Himmel mit.

```text
Precise technical optical-mechanics illustration of an unbranded DSLR with lens on a compact motorized star-tracker head and tripod under a restrained dark night sky. The tracker polar shaft is clearly tilted upward and its straight dashed extension points exactly at one bright celestial pole star. Faint concentric apparent star-trail arcs centered on that star. Show one thin cyan curved arrow on the sky trail and one amber curved arrow about the tracking shaft, both with the same apparent rotational direction as a teaching schematic. Ensure arrows do not suggest motion around different axes. Brushed metal bearings, minimal cyan construction guides. No labels or numbers; exact rotation arrows may be redrawn natively in PowerPoint.
```

**Beschriftung:** Himmelspol · Polarstern · Star-Tracker.
**Prüfen:** Beide Pfeile laufen in **dieselbe** Richtung: Der Tracker folgt dem Himmel. Die Achse zeigt zum Pol. Wenn die KI hier Fehler macht, in PowerPoint mit Pfeilen nachbauen.

### Folie 20 – Was das Smart-Teleskop automatisch erledigt  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Tippen in der App, das Gerät arbeitet, das Bild wächst.

```text
Balanced scientific-technical illustration of automatic smart telescope imaging. Left: a compact generic unbranded all-in-one smart telescope on a stable small tripod outdoors at night, with its objective pointed toward one original generic faint nebula. A subtle amber incoming light path runs FROM nebula TO objective, not outward. Right: exactly three identical unbranded smartphone screen silhouettes, slightly overlapping but each nebula image visible, displaying the SAME fixed star pattern and nebula composition at successive integration stages: rear very noisy and faint, middle moderately noisy and brighter, front cleaner with better signal-to-noise. No UI writing or fake controls. A fine dotted cyan wireless connection from telescope to phone, and one simple anatomically plausible fingertip touching front screen. Precise glass/metal, restrained glow, scientific clarity.
```

**Beschriftung:** Zielobjekt · Live-Stacking · App.
**Prüfen:** drei Stufen auf den Bildschirmen (grobkörnig bis sauber), Gerät ohne Logo.

### Folie 28 – Eine Aufnahme ist erst der Anfang  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Hälfte Himmel, Hälfte Rechner: viele Bilder werden zu einem.

```text
Scientific technical two-part process illustration with a continuous clear left-to-right flow. Left: DSLR on a tripod under a dark realistic illustrative star field, capturing a sequence of many small identical-framed exposures of the SAME generic nebula, each with different random noise. Middle: a tidy stream of small square image frames converges through a restrained cyan processing pathway, no arbitrary stepping stones. Right: an unbranded laptop on a clean desk displaying ONE final aligned, stacked, high signal-to-noise image of the SAME nebula, recognizable by identical star positions and cloud geometry. Thin amber motion cues and precise cyan optical-laboratory construction lines. No text, numbers, labels or logos.
```

**Beschriftung:** Himmel · Rechner (die sieben Schritte stehen nativ auf der Folie).
**Prüfen:** viele kleine Bilder links, ein großes Ergebnis rechts.

### Folie 31 – Lights, Darks und Flats  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** die drei Bildsorten und das saubere Ergebnis.

```text
Scientific educational four-stage calibration comparison in one horizontal row of four identical-size square image panels. Panel one: a faint generic emission nebula and fixed stars with visible grain and some optical vignetting. Panel two: a nearly black dark exposure with a few subtle hot pixels and fixed-pattern speckles, and a tiny simple closed lens-cap silhouette beside it. Panel three: evenly illuminated neutral gray flat field with gradual darkening toward corners and two faint donut-shaped dust shadows, NO stars or nebula. Panel four: the EXACT SAME nebula and star pattern as panel one, but with reduced fixed-pattern artifacts, corrected vignetting and dust shadows, cleaner background. Thin cyan frames and subtle amber flow arrows between panels; no exaggerated creation of new astronomical detail. This is an illustrative concept, not a mathematically exact calibration pipeline; replace panels with actual captures when available. No writing, labels or numbers.
```

**Beschriftung:** Light · Dark · Flat · Ergebnis.
**Prüfen:** Das Dark ist fast schwarz, das Flat hat dunkle Ecken und Staubringe, das Ergebnis ist sauber. Idealerweise ersetzen Sie die drei Bilder durch Ihre echten Light, Dark und Flat.

### Folie 39 – Euer Startpaket  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** vier Karten für vier Schritte, mit Platz für den QR-Code.

```text
Exactly four visually consistent rounded rectangular technical cards in a single horizontal row on midnight navy, connected by one thin amber path from left to right. Each card contains one clean precision-illustrated cyan/metal icon, in order: generic smartphone on tiny tripod; generic DSLR camera on tripod; compact unbranded smart telescope on tripod; small observatory dome beside a small group of simple anonymous human silhouettes. Balanced polished scientific engineering style, no cartoon faces or fake interface text. Reserve a clearly empty square area in the LOWER RIGHT, separate from the four cards, for a real QR code to be added later; DO NOT generate any QR pattern. Keep cards legible and safe margins, no labels, logos, text or numbers.
```

**Beschriftung:** ohne Extrakosten · mit Kamera · mit Nachführung · Weiterlernen.
**Prüfen:** vier Karten, ein freier Bereich für den QR-Code, kein gezeichneter QR-Code.

---

## 4. Folien mit eigenen Fotos oder Screenshots (kein KI-Bild)

Diese Folien leben von Ihrem echten Material. Ein KI-Bild wäre hier nicht passend.

| Folie | Titel | Was Sie brauchen |
|---|---|---|
| 1 | Der Nachthimmel zum Mitnehmen | eindrucksvolle eigene Astroaufnahme als Hintergrund |
| 4 | Der Himmel heute Abend | Screenshot aus Stellarium für Ort und Zeit, mit eingeblendeten Namen |
| 12 | Das Smartphone | eigene Smartphone-Aufnahmen, Smartphone an Okularhalterung |
| 13 | Andromeda mit dem Smartphone | Ihr Sommerfoto der Andromedagalaxie, Foto des Aufbaus, wenn möglich Original und bearbeitetes Bild |
| 14 | Smartphone: Tipps und Grenzen | Foto Smartphone auf Mini-Stativ, Mond mit Standardbelichtung und mit nach unten korrigierter Belichtung |
| 15 | DSLR, viele Optiken | DSLR in der Mitte, fünf Beispielaufnahmen (Fischauge, Weitwinkel, Normal, Tele, Teleskop) |
| 16 | Orion mit Teleobjektiv | Einzelbild und gestapeltes Ergebnis, Foto des Aufbaus |
| 18 | DSLR: Tipps und Grenzen | eigene Ergebnisse, Live-View-Bildschirm mit vergrößertem Stern |
| 19 | Smart-Teleskop (Seestar S50 Pro) | Fotos transportfertig, aufgebaut, App-Ansicht, Ergebnisbild |
| 22 | Ein Bild wächst mit der Zeit | dasselbe Motiv in sechs Stufen (Einzelbild bis 30 Minuten) |
| 23 | Teleskoptypen | je ein Teleskop und ein Ergebnisbild |
| 30 | Gute und schlechte Einzelbilder | 3 bis 4 eigene Fehlerbilder mit markierter Ursache |
| 34 | Astrosoftware | Screenshots der genannten Programme |
| 35 | Live-Demo AstroWizard | Screenshots der Demo als Notfallplan |
| 36 | Der Bearbeitungsweg | ein Motiv in fünf Stufen |
| 37 | Ist das noch echt? | Beispielbilder: farbnahe Aufnahme, Schmalband, Landschafts-Montage |
| 38 | Vier Wünsche, konkrete Wege | die vier Bilder vom Einstieg (Mond, Milchstraße, Nebel, gesamter Himmel) |
| 40 | Fragen und Demonstration | Foto der vorhandenen Geräte |

Wenn Ihnen für einen Bereich noch ein Foto fehlt, können Sie dort vorübergehend eine Illustration aus `04_bildprompts.md` einsetzen. Kennzeichnen Sie sie dann klar als Illustration.

---

## 5. Zusammenfassung

- **19 KI-Illustrationen** insgesamt: 13 aus Abschnitt 2 und 6 aus Abschnitt 3.
- **18 Folien** brauchen Ihre eigenen Fotos oder Screenshots.
- Bei den Folien 9, 17, 25, 26, 31 und 32 bauen Sie die **genauen Teile** (Bayer-Raster, Pfeilrichtung, Spektrum, Farbzuordnung, Rauschstufen) in PowerPoint oder im Bildprogramm.
- Alle erzeugten Bilder bitte in `THIRD_PARTY_NOTICES.md` unter „KI-generierte Bilder" mit Dienst und Datum eintragen.
