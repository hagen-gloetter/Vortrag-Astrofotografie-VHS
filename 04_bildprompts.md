# Bildprompts für die Vortragsfolien

Diese Datei enthält fertige Prompts für KI-Bildwerkzeuge (ChatGPT, Midjourney, Firefly, Gemini u. a.). Die Prompts sind auf Englisch, weil die Ergebnisse dort besser werden. Erklärungen sind auf Deutsch.

**Umfang:** 28 Folien mit erklärenden Schaubildern und Alltagsbildern. Echte Himmelsfotos (Milchstraße, Nebel, Mond, Sternspuren, Geräte, Fehlerbilder, Bearbeitungsstufen) bleiben **Ihre eigenen Aufnahmen**.

**Bildformat:** 4:3 oder 1:1 als Bild neben dem Text. Die Bilder kommen in die Platzhalter `BILD_FolieN_k` der PowerPoint-Datei.

---

## 1. Empfohlener Stil: „Planetariums-Illustration"

| Merkmal | Festlegung |
|---|---|
| Look | flacher Vektor-Infografikstil, klare geometrische Formen, dezentes Leuchten |
| Hintergrund | tiefes Nachtblau `#0B1020`, leichter Verlauf nach `#121A33` |
| Akzente | Bernstein `#F5A623` (Licht, Wichtiges), Eisblau `#6FB7FF` (Sekundäres), Off-White `#F2F4F8` |
| Komposition | ein klares Motiv, viel freie Fläche, ein Gedanke pro Bild |
| Text im Bild | **keiner**. KI-Bilder erzeugen fehlerhafte Buchstaben. Beschriftung kommt in PowerPoint |
| Alltagsbilder | freundlich, einfach, ohne Cartoon-Gesichter |
| Natürliche Farben | nur dort erlaubt, wo sie zum Inhalt gehören (Nebel, Abendsonne, Stadtlicht, Mond) |

**Warum dieser Stil:** Er passt zu den dunklen Folien, ist beamerfreundlich (hoher Kontrast), wirkt einheitlich über alle Folien und hebt sich klar von Ihren echten Fotos ab. So sehen Zuschauer sofort: Foto = echtes Ergebnis, Illustration = Erklärung.

### Stilblock (an jeden Prompt anhängen)

```text
Style: flat vector infographic illustration in a planetarium style. Deep midnight navy background (#0B1020) with a subtle gradient to #121A33. Clean geometric shapes, soft glow, limited palette of warm amber (#F5A623), ice blue (#6FB7FF) and off-white (#F2F4F8). A few tiny scattered stars as texture. Single clear subject, generous empty space, high contrast for projector display, friendly educational look. No text, no letters, no numbers, no logos, no watermark.
```

### Negativblock (wenn das Werkzeug ihn unterstützt)

```text
text, letters, numbers, captions, labels, logos, watermark, photo-realistic, cluttered background, extra fingers, distorted hands
```

### Hinweise je Werkzeug

- **ChatGPT / Gemini / Firefly:** Prompt und Stilblock zusammen einfügen. Format dazuschreiben: „Aspect ratio 4:3" oder „square 1:1". Negativblock als letzten Satz mit „Avoid: …".
- **Midjourney:** Prompt und Stilblock einfügen und am Ende `--ar 4:3 --no text, letters, numbers, watermark` (oder `--ar 1:1`) anhängen.
- Erzeugen Sie immer **mehrere Varianten** und wählen Sie die klarste. Bei Schaubildern entscheidet Klarheit, nicht Schönheit.

---

## 2. Qualitätsregeln für erklärende Bilder

KI-Bilder sind bei Physik oft **fast richtig, aber falsch**. Prüfen Sie jedes Bild gegen die Prüfpunkte unter dem Prompt. Zusätzlich:

1. **Kein Text im Bild.** Beschriftungen setzen Sie in PowerPoint.
2. **Genaue Teile bauen Sie nativ in PowerPoint:** Rasterzahlen (Bayer-Muster), Spektrallinien an der richtigen Wellenlänge, Winkel, Kurven, Tabellen. Diese Folien sind unten mit **„KI + nativ"** markiert. Das KI-Bild liefert dort nur Stimmung oder Alltagsbild.
3. **Keine Markennamen und Logos.** Geräte werden als „kompaktes Smart-Teleskop" beschrieben, nicht als Seestar oder ZWO.
4. **Keine bekannten Fotos nachbauen.** Besonders bei Nebeln keine erkennbaren Hubble-Bilder kopieren („generic nebula").
5. **Hände und Finger** (Folie 16) werden oft falsch. Wenn es nicht klappt, als einfache Silhouette zeichnen lassen oder in PowerPoint mit Formen bauen.

**Kennzeichnung je Folie:**

- ✅ **KI-Bild:** funktioniert gut als Illustration
- 🔧 **KI + nativ:** KI liefert das Alltagsbild, genaue Teile ergänzen Sie in PowerPoint

---

## 3. Prompts nach Folien

### Folie 4 – Wir folgen dem Weg des Lichts  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** die Reise des Lichts vom Stern bis zum Rechner, als fünf Stationen.

```text
A winding horizontal path of light in five clearly separated stations, all drawn at the same size: a small bright star at the start, then a thin glowing layer of atmosphere shown as a soft blue band, then a simple telescope lens, then a square camera sensor chip with a tiny pixel grid, then a laptop screen showing a bright star field. A thin amber beam of light connects all five stations in order from left to right. Calm composition, even spacing, plenty of empty space above and below.
```

**Beschriftung in PowerPoint:** Objekt · Luft · Optik · Sensor · Rechner (Nummern 1–8 wie auf der Folie).
**Prüfen:** genau fünf Stationen, Lichtweg läuft eindeutig von links nach rechts, keine Buchstaben.

### Folie 5 – Auge und Kamera  ·  1:1  ·  ✅ KI-Bild

**Bild soll zeigen:** Auge = Schnappschuss, Kamera = Eimer, der sich füllt.

```text
Split composition. Left half: a stylized human eye with a single quick bright flash symbol beside it, suggesting an instant snapshot. Right half: a row of three identical buckets standing in gentle rain at night, the first nearly empty, the second half full, the third almost full of glowing amber water, showing water collecting over time. A thin vertical divider between both halves. Starry night background.
```

**Beschriftung:** Auge · Kamera (und „Zeit →").
**Prüfen:** drei Eimer mit steigendem Füllstand, Auge nur klein und einfach.

### Folie 7 – Wir fotografieren Vergangenheit  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** ein Lichtstrahl, der als Brief unterwegs ist, vom Mond über die Sonne und den Orionnebel bis zur Andromedagalaxie.

```text
A long diagonal amber beam of light travelling from the upper right corner to the lower left corner. Along the beam, in order from far to near: a distant spiral galaxy, a glowing pink and blue nebula, a small yellow sun, a grey moon, and a small blue Earth at the end. The spacing between the objects becomes smaller and smaller towards the Earth, suggesting enormous distances far away and short distances close by. A tiny vintage envelope icon rides on the light beam, like a letter in transit.
```

**Beschriftung:** 1,3 Sekunden · 8 Minuten · 1.300 Jahre · 2,5 Millionen Jahre (als Pfeile, nur Zahlen aus der Folie).
**Prüfen:** Reihenfolge Erde, Mond, Sonne, Nebel, Galaxie. Abstände nicht maßstäblich, aber wachsend.

### Folie 8 – Wie hell ist hell?  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** das Butterbrot-Bild: dieselbe Menge Licht (Butter), einmal konzentriert, einmal dünn verteilt.

```text
Two slices of bread side by side. Left: a very small slice, the size of a postage stamp, covered with a thick glowing amber layer of butter. Right: a very large slice, covered with the same amount of butter spread extremely thin so it looks pale and faint. Both on a dark navy table. Playful but simple and clean.
```

**Beschriftung:** hell und klein · schwach und groß (Flächenhelligkeit).
**Prüfen:** rechte Scheibe deutlich größer, Butter dünn, aber sichtbar.

### Folie 9 – Licht hat Farben  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Wellenlänge bestimmt die Farbe. Blau = kurze Welle, Rot = lange Welle.

```text
Two horizontal waves stacked above a rainbow band. The upper wave is blue with short, tight wavelengths. The lower wave is red with long, stretched wavelengths. Beneath them a smooth rainbow spectrum band running from blue on the left to red on the right. On the far left, a white light beam enters a glass prism and splits into the rainbow.
```

**Beschriftung:** 450 nm · 550 nm · 650 nm (nativ ergänzen), „Prisma".
**Prüfen:** Blau hat die **kürzere** Welle, Rot die längere, Reihenfolge im Spektrum Blau bis Rot. Für exakte nm-Skala besser das native Spektrumband aus PowerPoint verwenden.

### Folie 10 – Die Farbe verrät die Temperatur  ·  1:1  ·  ✅ KI-Bild

**Bild soll zeigen:** glühendes Metall und Sterne: heißer = weißer und blauer.

```text
Left: a bar of glowing metal heated at one end, colour gradient from dark red through orange to yellowish-white. Right: a vertical column of three round stars of the same size: top a blue-white star, middle a yellow-white star, bottom an orange-red star, like a thermometer where the hot star is at the top. Soft glow around each star. A thin arrow pointing upward along the stars, hot at the top.
```

**Beschriftung:** über 10.000 °C · 5.500 °C · unter 4.000 °C.
**Prüfen:** blau oben (heiß), orange-rot unten (kühl), Eisen endet nicht blau.

### Folie 11 – Vom Gas zum Stern und zurück  ·  1:1  ·  ✅ KI-Bild

**Bild soll zeigen:** der Kreislauf der Sternentstehung in vier Stationen.

```text
A circular loop with four stations connected by curved arrows, clockwise. Top: a dark dusty gas cloud with faint silhouettes. Right: the cloud collapsing into a small glowing core. Bottom: a bright blue young star lighting up a glowing pink-red nebula around it. Left: an old star ending as an expanding soft ring of gas, which feeds back into the dark cloud at the top. Nebula colours may use natural magenta-red and teal as an exception to the palette.
```

**Beschriftung:** 1 bis 4 wie auf der Folie.
**Prüfen:** Kreislauf ist geschlossen, Pfeilrichtung stimmt mit der Nummerierung 1 bis 4 überein.

### Folie 13 – Jedes Gas hat seine eigene Farbe  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Neonröhre als Alltagsbild für leuchtendes Gas.

```text
A glowing orange-red neon tube bent into a simple loop, mounted on a dark wall, with a soft glow around it. Next to it, three small glass tubes of gas, each glowing in a different single colour: deep red, blue-green, and dark red. Small sparks of light inside each tube. No text.
```

**Beschriftung:** Hα 656 nm · OIII 501 nm · SII 672 nm.
**Prüfen:** Die **drei Spektrallinien** (656, 501, 672 nm) bauen Sie nativ, nicht per KI.

### Folie 14 – Seeing: Warum Sterne flimmern  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Luftpakete verschiedener Temperatur biegen das Licht.

```text
Lower part: a hot road at dusk with visible heat shimmer wobbling the horizon. Upper part: a night sky where a single bright star sends a thin amber light ray down through translucent blobs of warm (amber tinted) and cool (blue tinted) air. The ray bends in a zigzag as it passes through each blob. Next to it, the same star shown twice: once sharp and once blurred and wobbly.
```

**Beschriftung:** ruhige Luft · unruhige Luft.
**Prüfen:** Lichtstrahl knickt an den Luftpaketen, scharfer und unscharfer Stern sichtbar.

### Folie 15 – Tief am Horizont ist die Luft dick  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Dicke Luftschicht bei flachem Blick.

```text
A large curved Earth limb at the bottom of the image with a thin blue atmosphere shell around it, drawn clearly exaggerated in thickness. A small observer figure stands on the surface. Three rays of light from far-away stars reach the observer: one coming straight from above (short path through the air), one from medium height, and one from near the horizon (long path through the air). The near-horizon ray turns reddish. In the far corner a red setting sun on the horizon.
```

**Beschriftung:** 90° · 30° · 10° (1-fach · 2-fach · 6-fach nativ ergänzen).
**Prüfen:** Je flacher der Strahl, desto länger der Weg durch die Lufthülle. Winkelverhältnisse stimmen nur annähernd, daher bei Bedarf nativ nachzeichnen.

### Folie 16 – Wie groß ist ein Himmelsobjekt?  ·  1:1  ·  ✅ KI-Bild (Hände prüfen!)

**Bild soll zeigen:** der ausgestreckte Arm als Winkelmaß.

```text
A simple flat silhouette of an outstretched arm and hand seen from the side, held up against a night sky. A small full moon is visible just next to the little finger and appears only half as wide as the finger. Subtle markers show the width of the little finger, the thumb and the fist. Minimal, clean shapes, no realistic skin details, five fingers only.
```

**Beschriftung:** 1° · 2° · 10° · Mond 0,5°.
**Prüfen:** fünf Finger, Mond halb so breit wie der kleine Finger.

### Folie 18 – Der Mond auf dem Sensor  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Pixel als Mosaiksteine.

```text
Three identical round moons side by side, each made from square mosaic tiles. The first moon is built from very few large coarse tiles, almost unrecognizable. The second is built from medium tiles, craters faintly visible. The third is built from many tiny tiles, showing clear craters. All three have the same overall size. Grey and white tones for the moons, thin gaps between tiles.
```

**Beschriftung:** 50 mm · 400 mm · 1.000 mm.
**Prüfen:** gleiche Mondgröße, nur die Kachelzahl wächst.

### Folie 19 – Die Öffnung sammelt das Licht  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** doppelter Durchmesser = vierfache Menge.

```text
Two open buckets standing side by side in gentle rain under a night sky. The right bucket is exactly twice as wide as the left one. Next to each bucket, a small stack of water droplet icons shows the amount collected: one droplet group beside the small bucket and four droplet groups beside the wide bucket. Even rain, simple shapes.
```

**Beschriftung:** Öffnung · 1× · 4×.
**Prüfen:** rechter Eimer genau doppelt so breit, vier Tropfengruppen gegen eine.

### Folie 20 – Keine Optik ist perfekt  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Beugung: Wellen, die sich hinter einer Öffnung ausbreiten, und ein Stern als Scheibchen mit Ringen.

```text
Left: top view of water waves arriving at a narrow harbour entrance and spreading out in circular ripples behind it. Right: a single star shown as a small bright disc surrounded by faint thin concentric rings, like an airy pattern, glowing amber. A subtle arrow connects both pictures.
```

**Beschriftung:** Beugung.
**Prüfen:** die Wellen laufen hinter der Öffnung **auseinander**, Stern mit zarten Ringen.

### Folie 22 – Pixel sind kleine Eimer für Licht  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Sensor als Eimerraster, Füllstand = Helligkeit.

```text
A grid of many small identical square buckets seen from a slight angle, standing in even rain. Each bucket has a different water level, glowing amber. The water levels together form a faint shape of a bright star cluster in the centre of the grid: fuller buckets in the middle, emptier buckets at the edges. Raindrops fall evenly from above.
```

**Beschriftung:** Photonen · Pixel · Messwert.
**Prüfen:** Eimer in regelmäßigem Raster, Mitte voller als der Rand.

### Folie 23 – Wie der Sensor Farbe sieht  ·  1:1  ·  🔧 KI + nativ

**Bild soll zeigen:** Schachbrett aus Mini-Sonnenbrillen als Bild für Farbfilter.

```text
A square chessboard-like grid of tiny sunglasses lenses, each lens a single colour: red, green or blue. Behind the grid, a bright white beam of light shines through. Each lens lets only its own colour pass through. Playful and clean.
```

**Beschriftung:** keine, das **Bayer-Muster (2 × Grün, 1 × Rot, 1 × Blau)** bauen Sie nativ als 4 × 4 Raster.
**Prüfen:** KI trifft das Bayer-Muster fast nie richtig. Verwenden Sie das KI-Bild nur als Stimmungsbild.

### Folie 24 – Nicht jedes Photon wird gezählt  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Regentropfen, die teils im Eimer landen, teils abprallen.

```text
A single bucket in rain, close-up. Most raindrops fall into the bucket and join the water, but a few drops bounce off the rim and a few splash outside. Each drop is a small glowing amber dot. Simple, clear, plenty of empty space around the bucket.
```

**Beschriftung:** Quanteneffizienz.
**Prüfen:** Mehrheit landet im Eimer, wenige prallen ab.

### Folie 27 – Der Himmel steht nicht still  ·  1:1  ·  ✅ KI-Bild

**Bild soll zeigen:** Karussell als Bild für Erddrehung.

```text
Top view of a carousel at night with small horses seated near the rim. Motion arcs behind the horses at the rim are long and sweeping, while arcs near the centre pole are short. Behind the carousel, faint concentric star trails in the sky circle around the same centre point, like a night sky rotating around the pole star.
```

**Beschriftung:** schnell außen · langsam innen · Himmelspol.
**Prüfen:** äußere Spuren länger als innere, gemeinsames Zentrum.

### Folie 29 – Warum sich das Bildfeld dreht  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Dasselbe Sternfeld dreht sich um das Zielobjekt.

```text
The same star field shown as three overlapping rectangular frames, all centred on the same small glowing nebula. Each frame is rotated a little more than the previous one around the nebula: 0 degrees, 15 degrees, 30 degrees. Stars inside each frame rotate with it. The frames are semi-transparent amber outlines. The nebula stays fixed in the centre.
```

**Beschriftung:** 0 · 10 · 30 Minuten (wie auf der Folie).
**Prüfen:** gemeinsamer Mittelpunkt, Rahmen gleich groß. Bei Fehlern in PowerPoint mit drei gedrehten Rechtecken nachbauen.

### Folie 30 – Die Montierung trägt das Bild  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Die beiden Montierungsarten und ihre Achsen.

```text
Two simple technical-style illustrations of telescope mounts side by side. Left: a mount with one vertical axis and one horizontal axis, shown with two thin amber arrows (up-down and left-right). Right: a mount whose main axis is tilted and points up toward a bright star in the sky, shown with one curved amber arrow around that tilted axis. Minimal geometric shapes, no brand details.
```

**Beschriftung:** azimutal · parallaktisch · Himmelspol.
**Prüfen:** rechte Hauptachse zeigt zum hellen Stern (Himmelspol). Der Neigungswinkel entspricht dem Breitengrad. Bei Bedarf nativ.

### Folie 31 – Woher kommt das Rauschen?  ·  1:1  ·  ✅ KI-Bild

**Bild soll zeigen:** gleichmäßiger Regen füllt Gefäße nie exakt gleich.

```text
Four identical glass jars standing in a row in steady rain. The water levels are nearly the same but slightly different in each jar: one a little lower, one a little higher. Raindrops fall at random positions. Glowing amber water, dark navy background.
```

**Beschriftung:** 98 · 104 · 95 · 103 (Tropfen, wie im Sprechtext).
**Prüfen:** vier gleiche Gläser, leichte Unterschiede im Füllstand.

### Folie 32 – Das Signal muss lauter sein als das Rauschen  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Gespräch in einer lauten Kneipe.

```text
A busy, noisy cafe scene drawn as a flat illustration with silhouettes. Two people talk at a small table. Between them a thin, faint amber sound wave of the quiet voice. Around them a chaotic cloud of jagged blue sound waves from the crowd. In a second smaller scene on the right, the speaker talks louder: the amber wave is large and clearly rises above the blue noise.
```

**Beschriftung:** Signal · Rauschen.
**Prüfen:** Signal amber, Rauschen blau, rechts deutlich größer.

### Folie 33 – Warum Stacking funktioniert  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Viele verrauschte Bilder verschmelzen zu einem sauberen.

```text
A stack of many semi-transparent square photo frames layered like cards, each showing the same star field with grainy random noise. At the top of the stack, one frame is clean and sharp and glows, the noise averaged away. Subtle arrows pointing from the stack up to the clean frame. Dark background.
```

**Beschriftung:** 1 · 4 · 16 · 64 (nativ ergänzen).
**Prüfen:** Für den Vergleich „1, 4, 16, 64 Aufnahmen" besser **ein** sauberes Bild erzeugen und das Rauschen in einem Bildprogramm unterschiedlich stark hinzufügen. So stimmt die Abstufung.

### Folie 34 – Der Himmel ist nicht überall gleich dunkel  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** dunkler Landhimmel gegen aufgehellten Stadthimmel.

```text
A single landscape split smoothly from left to right. Left: a dark countryside horizon with a rich starry sky and the Milky Way clearly visible. Right: a city skyline silhouette with an orange glow dome over it, where only a few bright stars remain visible. A soft gradient transition in the middle. Natural orange city glow is an exception to the palette.
```

**Beschriftung:** Bortle 2 · Bortle 5 · Bortle 8–9.
**Prüfen:** links viele Sterne, rechts nur wenige, weicher Übergang.

### Folie 35 – Wie ein Sieb für Licht  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Filter als Sieb, nur wenige Farben kommen durch.

```text
A broad rainbow beam of light entering a fine sieve or coffee filter from the left. After the sieve only two thin separate beams continue: one deep red and one blue-green. A few stray orange-yellow rays from a street lamp icon are stopped and fall away at the sieve. Simple, clean, easy to read.
```

**Beschriftung:** Himmelslicht · Filter · Hα · OIII · Stadtlicht.
**Prüfen:** nur zwei dünne Strahlen kommen durch. Den echten Durchlassbereich zeichnen Sie nativ als Spektrum.

### Folie 36 – Echte Messdaten, erfundene Farben  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** Drei Schwarz-Weiß-Bilder werden zu einem Farbbild kombiniert.

```text
Three grayscale panels of the same generic emission nebula in a row at the top, each slightly different in structure. Below them, the same three panels tinted red, green and blue respectively, merging with arrows into one colourful combined nebula image at the bottom. Do not copy any famous nebula photograph. Natural nebula colours are an exception to the palette.
```

**Beschriftung:** SII → Rot · Hα → Grün · OIII → Blau (nativ, richtige Zuordnung).
**Prüfen:** Zuordnung in der Grafik stimmt mit der Folie überein. Die Zuordnung wird nativ beschriftet, nicht im Bild.

### Folie 58 – Das lineare Bild  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** dunkel wirkendes Bild, in dem schwache Information steckt, nach dem Strecken sichtbar.

```text
Two panels side by side. Left: an almost completely black image of a star field where only faint hints of a nebula are visible. Right: the same scene brightened, showing a clearly visible glowing nebula and many stars. A subtle curved arrow between them suggests stretching the brightness. Dark navy frame.
```

**Beschriftung:** linear · gestreckt.
**Prüfen:** beide Hälften zeigen dieselbe Szene, rechts deutlich heller.

### Folie 46 – Azimutal oder äquatorial: zwei Betriebsarten  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** dasselbe Gerät in zwei Aufbauten, ohne Marke.

```text
Two identical compact all-in-one smart telescopes on tripods, shown side by side, with no brand marks or logos. Left: the telescope stands upright on a flat tripod head, a thin vertical axis line and a horizontal axis line are drawn in amber. Right: the telescope sits on a tilted wedge, its main axis angled up toward the pole star shown as a bright star in the sky. A small north arrow on the ground under the right tripod.
```

**Beschriftung:** AZ · EQ · Himmelspol · Norden.
**Prüfen:** rechts zeigt die geneigte Achse zum Polarstern. Ihre echten Fotos des Geräts ersetzen die Illustration, sobald Sie sie haben.

---

## 4. Zusammenfassung

| Art | Folien |
|---|---|
| ✅ KI-Bild | 5, 7, 8, 10, 11, 14, 16, 18, 19, 20, 22, 24, 27, 31, 32, 34, 58 |
| 🔧 KI + nativ | 4, 9, 13, 15, 23, 29, 30, 33, 35, 36, 46 |

Für die 🔧-Folien gilt: Das KI-Bild setzt die Stimmung, die **genauen Elemente** (Spektrallinien, Wellenlängen, Bayer-Raster, Winkel, Zuordnungen, Zahlen) bauen Sie in PowerPoint nativ. Dazu passt der Katalog der nativen Schaubilder in [01_prompt.md](./01_prompt.md).
