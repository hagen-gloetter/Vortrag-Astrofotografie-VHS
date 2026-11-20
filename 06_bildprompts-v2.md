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

Der Stil ist unverändert: **Planetariums-Illustration**, dunkles Nachtblau, Bernstein und Eisblau, flacher Vektorstil, ein Motiv pro Bild, **kein Text im Bild**. Alle Regeln (Qualitätsprüfung, Hinweise je Werkzeug, Negativblock) stehen in `04_bildprompts.md`, Abschnitte 1 und 2. Formate: 4:3 oder 1:1.

**Stilblock (an jeden neuen Prompt anhängen):**

```text
Style: flat vector infographic illustration in a planetarium style. Deep midnight navy background (#0B1020) with a subtle gradient to #121A33. Clean geometric shapes, soft glow, limited palette of warm amber (#F5A623), ice blue (#6FB7FF) and off-white (#F2F4F8). A few tiny scattered stars as texture. Single clear subject, generous empty space, high contrast for projector display, friendly educational look. No text, no letters, no numbers, no logos, no watermark.
```

**Negativblock:**

```text
text, letters, numbers, captions, labels, logos, watermark, photo-realistic, cluttered background, extra fingers, distorted hands
```

---

## 2. Wiederverwendung von Prompts aus `04_bildprompts.md`

Die Prompts bleiben unverändert. Die Spalte „Anpassung" nennt, was sich in der Kompaktfassung ändert.

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
A gently rising staircase of four wide steps of equal width, seen from the side, left to right. On the first step a smartphone standing on a tiny tripod. On the second step a DSLR camera with a long lens on a tripod. On the third step a compact all-in-one smart telescope on a small tripod. On the fourth step a classic telescope on an equatorial mount. Above each device floats a small glowing target in the night sky: a crescent moon above the phone, a band of the Milky Way above the camera, a glowing nebula above the smart telescope, and a spiral galaxy above the classic telescope. All devices are generic and have no brand marks.
```

**Beschriftung in PowerPoint:** 1 bis 4 und die Namen der Stufen aus der Folie.
**Prüfen:** genau vier Stufen, vier unterscheidbare Geräte, Reihenfolge von links nach rechts wie auf der Folie, keine Logos.

### Folie 17 – Der Star-Tracker  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** die Kamera dreht sich mit dem Himmel mit.

```text
A small camera with a lens mounted on a compact motorized tracking head on a tripod, pointing up at the night sky. The tracking head's rotation axis is tilted upward and aimed at a single bright pole star. Faint concentric star trails circle around the pole star in the sky. Two curved arrows show the rotation: a blue curved arrow around the pole star showing how the sky appears to turn, and an amber curved arrow around the tracker's axis, both running in the same direction. Minimal geometric shapes, no brand details.
```

**Beschriftung:** Himmelspol · Polarstern · Star-Tracker.
**Prüfen:** Beide Pfeile laufen in **dieselbe** Richtung: Der Tracker folgt dem Himmel. Die Achse zeigt zum Pol. Wenn die KI hier Fehler macht, in PowerPoint mit Pfeilen nachbauen.

### Folie 20 – Was das Smart-Teleskop automatisch erledigt  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Tippen in der App, das Gerät arbeitet, das Bild wächst.

```text
Left: a compact all-in-one smart telescope on a small tripod outdoors at night, pointing at a glowing nebula in the sky. A thin amber beam of light runs from the nebula into its lens. Right: three overlapping copies of a smartphone screen showing the same nebula at three stages, from very grainy and faint in the back to clean and bright in front, suggesting that the picture grows over time. A dotted wireless signal arc connects the telescope and the phone. A fingertip taps the front screen. No brand marks.
```

**Beschriftung:** Zielobjekt · Live-Stacking · App.
**Prüfen:** drei Stufen auf den Bildschirmen (grobkörnig bis sauber), Gerät ohne Logo.

### Folie 28 – Eine Aufnahme ist erst der Anfang  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** Hälfte Himmel, Hälfte Rechner: viele Bilder werden zu einem.

```text
Split composition with a soft diagonal path from left to right. Left half: a camera on a tripod under a starry night sky, capturing a cascade of many small square photos that fall like cards. Right half: a cozy desk with a laptop where the stack of small photos merges into one single large glowing nebula picture on the screen. Between both halves a path of small stepping stones suggests the steps of the process. Calm, friendly mood.
```

**Beschriftung:** Himmel · Rechner (die sieben Schritte stehen nativ auf der Folie).
**Prüfen:** viele kleine Bilder links, ein großes Ergebnis rechts.

### Folie 31 – Lights, Darks und Flats  ·  4:3  ·  🔧 KI + nativ

**Bild soll zeigen:** die drei Bildsorten und das saubere Ergebnis.

```text
Three framed square photos side by side, followed by an arrow pointing to a fourth, clean picture. First frame: a star field with a faint glowing nebula and a bit of grainy noise. Second frame: an almost black image with a few tiny bright speckles, a small lens cap icon in the corner. Third frame: an evenly lit grey-white surface that is darker in the corners and shows several faint ring-shaped dust shadows. The fourth frame at the end of the arrow: the same star field and nebula as in the first frame, now clean, sharp and evenly lit.
```

**Beschriftung:** Light · Dark · Flat · Ergebnis.
**Prüfen:** Das Dark ist fast schwarz, das Flat hat dunkle Ecken und Staubringe, das Ergebnis ist sauber. Idealerweise ersetzen Sie die drei Bilder durch Ihre echten Light, Dark und Flat.

### Folie 39 – Euer Startpaket  ·  4:3  ·  ✅ KI-Bild

**Bild soll zeigen:** vier Karten für vier Schritte, mit Platz für den QR-Code.

```text
Four rounded cards in a row, each showing one simple icon on a navy background: a smartphone on a tiny tripod, a DSLR camera on a tripod, a compact smart telescope on a tripod, and a small observatory dome with a group of friendly people silhouettes next to it. The cards are connected by a thin amber line from left to right. Leave an empty square space in the lower right corner for adding a QR code later. Do not draw a QR code.
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
