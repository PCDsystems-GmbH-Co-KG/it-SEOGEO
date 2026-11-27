# Projekt SEO-OPT

Ziel: Aus einer Webseite oder einem Dokument (Word, TXT, PDF) entsteht der fertige, SEO-optimierte Text für eine B2B-Webseite plus alle Yoast-Daten.

Sprache: immer Deutsch. Schreibstil: kurze Sätze, aktive Sprache, keine Füllwörter, keine Gedankenstriche, kein Jargon.

## Ablauf (immer in dieser Reihenfolge)

1. **Quelle erfragen.** Frage zuerst nach einer Webseite (URL) oder einem Dokument (Word, TXT, PDF mit Pfad). Frage zusätzlich nach:
   - Ziel-Domain und gewünschtem Slug (für die Canonical-URL)
   - Zielgruppe und Region, falls nicht aus der Quelle klar
   - Gewünschtem Handlungsaufruf (z. B. Kontaktformular, Beratungstermin)
   Ohne Quelle nicht weitermachen.
2. **Quelle auslesen.** Webseite: abrufen und alle Fakten sammeln. Dokument: vollständig lesen (Word und PDF über die passenden Skills). Nur belegte Fakten verwenden.
3. **Text schreiben.** Erstelle zuerst den gesamten Text für die Webseite. Ziel: Das Produkt oder die Dienstleistung verkauft sich bei B2B-Kunden gut, der Interessent wird neugierig und nimmt Kontakt auf.
   - Aufbau: Hero mit H1 und erstem CTA, Problem, Nutzen, Beweis (Zahlen, Referenzen), FAQ, finaler CTA.
   - Nutzen vor Funktionen. Konkrete Zahlen. Klare Handlungsaufrufe.
4. **SEO-Regeln anwenden.** Lies `C:\Users\s.lambertz\.claude\regeln\SEO\SEO_Regeln_Komplett.md` vollständig und wende alle Regeln auf den Text und auf die Yoast-Daten an. Das ist die einzige Quelle der Regeln, es gibt keine Kopie im Projekt. Prüfe danach Punkt für Punkt gegen die Checkliste (Abschnitt 9 der Regeln) und korrigiere Abweichungen. Wichtige Grenzwerte: SEO-Titel 15 bis 60 Zeichen mit Keyword vorne, Meta-Beschreibung max. ca. 155 Zeichen mit Keyword und Handlungsaufruf, genau eine H1, max. 300 Wörter unter einer Überschrift, Absätze max. 150 Wörter, max. 25 % lange Sätze, max. 10 % Passiv, mind. 30 % Sätze mit Bindewort, keine 3 Sätze in Folge mit gleichem Anfangswort. Fehlt die Datei, stoppe und frage nach.
5. **Zwei Dateien erzeugen** im Ordner `ausgabe/<Projektname>/` (pro Auftrag ein eigener Unterordner, nichts überschreiben):
   - `TEXT.md`: der fertige Text mit Überschriftenstruktur (H1, H2, H3), bereit zum Einfügen in die Seite.
   - `YOAST.md`: diese sieben Felder, jeweils mit Zeichenanzahl:
     1. Fokus-Keyphrase
     2. Keyphrase-Synonyme
     3. SEO-Titel
     4. Meta-Beschreibung
     5. Titel für Social-Media
     6. Beschreibung für Social-Media
     7. Canonical-URL

## Qualitätsregeln

- Keine erfundenen Fakten, Kunden, Zitate oder Zahlen. Herstellerangaben als solche kennzeichnen.
- Texte eigenständig formulieren. Nichts wörtlich von der Quelle kopieren (Duplicate Content).
- Bei Unsicherheit nachfragen oder recherchieren, nicht raten.
- Am Ende kurz berichten: was erstellt wurde, wo die Dateien liegen, was der Nutzer prüfen muss.

## Ordner

- `regeln/`: nur ein Hinweis. Die Regeln liegen zentral unter `C:\Daten\CLAUDEPROJEKTE\SEO-OPT\SEO_Regeln_Komplett.md`.
- `ausgabe/`: Ergebnisse pro Auftrag.


# Blog-Design PCDsystems (Elementor, Beiträge)

Zweck: Arbeitsgrundlage für Claude beim Anlegen neuer Blog-Beiträge auf pcd-systems.de.
Muster: https://www.pcd-systems.de/dora-verordnung-mittelstand-anforderungen/ (Beitrag-ID 7277)
Referenz-Ergebnis: Schatten-KI-Beitrag (ID 7415)
Ergänzend gilt: `C:\Users\s.lambertz\.claude\regeln\SEO\SEO_Regeln_Komplett.md`

---

## 1. Ablauf

1. Text lesen (meist .txt im Downloads-Ordner), SEO-Regeln lesen.
2. Beitrag anlegen: `elementor-create-page` mit `post_type: "post"` und Titel (= H1, SEO-Titel).
3. Inhalt in EINEM Durchgang mit `elementor-build-composition` bauen (V4-Widgets).
4. Beitragsbild setzen: `elementor-update-page-settings` mit `{"post_featured_image": {"id": <Mediathek-ID>, "url": "<URL>"}}`.
   Bild vorher mit `elementor-list-assets` (Suche nach Dateiname) finden.
5. Änderungen später mit `elementor-manage-elements` und den IDs aus der `resolved_xml` des Build-Calls.
   Nie IDs aus einem älteren `get-page-structure` nach einem Build verwenden (überschreibt sonst).
6. Entwurf bleiben lassen. Nicht veröffentlichen ohne ausdrückliches Ja.
7. Dem Nutzer immer den Vorschau-Link nennen: `https://www.pcd-systems.de/?p=<ID>&preview_id=<ID>&preview=true`

## 2. Was die Seitenvorlage selbst liefert (NICHT im Body bauen)

Header, Footer, H1 (= Beitragstitel), Beitragsbild oben, Datum, Suche und "Verwandte Beiträge" kommen aus dem Single-Template.
Der Body enthält nur den Artikeltext. Das Muster hat kein Inhaltsverzeichnis und keine Autorenbox.

## 3. Was Elementor-Tools NICHT können (manuell im WordPress-Backend, dem Nutzer als Tabelle melden)

- Yoast: Fokus-Keyphrase, SEO-Titel, Meta-Description
- Slug (Keyword enthalten, klein, Bindestriche)
- Kategorien (DORA-Beitrag nutzt 17, 11, 43)
- Alt-Text des Beitragsbilds (in der Mediathek)
- Veröffentlichen, Sitemap, Indexierung anfragen

## 4. Aufbau des Beitragskörpers (Reihenfolge)

1. Root: ein `e-flexbox`, Spalte, Gap 20px, Padding 10px, Breite 100%.
2. Einstieg als **H2** (der Body hat keine H1), danach Absätze.
3. Weitere H2-Abschnitte, bei Bedarf H3 darunter. Keine Ebenen überspringen.
4. Fazit als H2 oder H3.
5. Trenner (4px, #163B67).
6. CTA "Für Unternehmen": H3 + Absatz + Button "JETZT KONTAKT AUFNEHMEN" -> https://www.pcd-systems.de/kontakt/
7. Unterer Container: Trenner + Hinweis "Mit Unterstützung von KI erstellt" (kursiv, 10px).

Entfernt auf Wunsch des Nutzers (nicht wieder einbauen, außer er fragt):
- CTA "Für IT-Talente" mit Jobs-Button
- Block "Weiterführende Links"

## 5. Design-Werte (an der Musterseite gemessen)

Schrift: Poppins (erbt vom Theme, nicht setzen). Textfarbe überall `#163B67`.

| Element | Desktop | Tablet | Mobil | Zeilenhöhe | Sonstiges |
|---|---|---|---|---|---|
| Fließtext, Listen | 22px | 22px | 20px | 27px (Mobil 24px) | Gewicht 400 |
| H2 | 44.2px | 29px | 25px | 53px / 35px / 30px | Gewicht 700, Letter-Spacing -2px |
| H3 | 33.16px | 24px | 21px | 40px / 29px / 25px | Gewicht 700, Letter-Spacing -1px |
| Button | 25px | 25px | 25px | 37.5px | Gewicht 600, Padding 12px 24px |
| KI-Hinweis | 10px | 10px | 10px | 27px | kursiv |

Breakpoints im Style-String: `@media(--tablet)` und `@media(--mobile)`.
Hinweis: Die Musterseite zeigt mobil für den KI-Hinweis 20px. Vermutlich Fehler, wir nutzen 10px.

Button:
- Hintergrund `#0099CE`, Schrift weiß `#FFFFFF`
- Radius `15px 0px 15px 15px`
- Links ausgerichtet (`align-self:flex-start`), kein Unterstrich
- **Hover UND Focus: Hintergrund `#163B67`, Schrift `#FFFFFF`.** Schriftfarbe immer explizit setzen, sonst überschreibt das Theme.

Trenner: `e-div-block` mit `padding:0; border-top:4px solid #163B67; width:100%`.

## 6. Technische Regeln für build-composition

- Fließtext: `e-paragraph` mit `tag: "span"` und `display:block` im Style (sonst bricht `<ul>` im `<p>`).
- Listen: `<ul>`/`<ol>` direkt im `paragraph`-String eines `e-paragraph`. Erlaubte Tags: b, strong, em, u, ul, ol, li, a, br, span, sup, sub.
- Fettdruck für Schlüsselbegriffe wie im Muster (`<strong>`), Listenpunkte mit `<b>Stichwort:</b>`.
- Überschriften: `e-heading` mit `tag` h2/h3.
- Buttons: `e-button` mit `text` und `link: {destination, isTargetBlank:false}`.
- Elementnamen (`configuration-id`) lesbar auf Deutsch, z. B. "H2 Risiken". Sie erscheinen im Navigator.
- Abstände nur über Gap des Roots. Keine Margins an Absätzen.
- Mobile-Werte direkt im Style-String mitgeben, nicht in Nachbearbeitung.
- Textinhalte: Umlaute normal schreiben, `&` als `&amp;`.
- Keine Gedankenstriche im Text (Nutzerregel).

## 7. SEO-Kurzfassung für Beiträge

- Genau eine Fokus-Keyphrase, im SEO-Titel (vorne), in der Meta-Description, im Slug, in den ersten 100 Wörtern und in einigen H2/H3.
- SEO-Titel max. 60 Zeichen. Meta-Description max. ca. 155 Zeichen mit Keyword, Nutzen und CTA.
- Sätze max. 20 Wörter (höchstens 25 % länger), Passiv unter 10 %, mind. 30 % Sätze mit Bindewort, keine 3 gleichen Satzanfänge in Folge, Absätze max. 150 Wörter, max. 300 Wörter unter einer Überschrift.
- Mindestens 3 interne Links mit beschreibendem Ankertext. Externe Quellen mit `target="_blank"`.
- Fakten und Zahlen aus dem Text des Nutzers nie verändern. Nur Stil straffen.

## 8. Bekannte interne Links

| Thema | URL |
|---|---|
| Kontakt | https://www.pcd-systems.de/kontakt/ |
| Jobs | https://www.pcd-systems.de/jobs/ |
| IT-Beratung | https://www.pcd-systems.de/it-beratung/ |
| IT-Betreuung | https://www.pcd-systems.de/it-betreuung/ |
| IT-Sicherheit | https://www.pcd-systems.de/it-sicherheit/ |
| IT-Sicherheitsprüfung | https://www.pcd-systems.de/itq-sicherheitspruefung/ |
| IT-Infrastrukturanalyse | https://www.pcd-systems.de/it-infrastrukturanalyse/ |
| KI-Kompetenz-Schulung | https://www.pcd-systems.de/ki-kompetenz-schulung/ |
| Microsoft 365 | https://www.pcd-systems.de/microsoft-365/ |
| Awareness-Schulung | https://www.pcd-systems.de/mitarbeiter-sensibilisierung/ |
| Passwortmanager | https://www.pcd-systems.de/passwortmanager/ |
| Beitrag EU AI Act für KMU | https://www.pcd-systems.de/eu-ai-act-kmu/ |
| Beitrag DORA | https://www.pcd-systems.de/dora-verordnung-mittelstand-anforderungen/ |
| Beitrag Cyber-Deception | https://www.pcd-systems.de/cyber-deception/ |
| Beitrag IT-Due-Diligence | https://www.pcd-systems.de/it-due-diligence-firmenuebernahme-risiken/ |
| Beitrag 10 häufigste IT-Probleme | https://www.pcd-systems.de/die-10-haeufigsten-it-probleme-bei-unternehmen/ |

Weitere Seiten bei Bedarf mit `elementor-list-posts` (Parameter `search`) suchen.

## 9. Messen der Musterseite (falls Werte neu geprüft werden)

Im Browser-Pane die Musterseite öffnen, Viewport mit `resize_window` auf 1440 / 768 / 375 setzen und per JavaScript `getComputedStyle` auslesen.
Ohne gesetzten Viewport liefert die Seite falsche Werte (Breite 0).
Selektoren im Muster: H2 `.elementor-element-abc8273 h2`, H3 `.elementor-element-2fa0bef h3`, Text `.elementor-element-e86388f p`, Button `.elementor-element-128d32e a`, KI-Hinweis `.elementor-element-56af904 em`.
Nach der Messung Viewport mit `preset: "desktop"` zurücksetzen.

## 10. Hinweise zur Zusammenarbeit

- Immer Deutsch, direkt und sachlich, kurze Sätze.
- Texte erfinden nur, wenn nötig (z. B. CTA), und das dem Nutzer ausdrücklich melden.
- Der Nutzer korrigiert Design gern per Aufzählung. Jeden Punkt einzeln abarbeiten und einzeln bestätigen.

## 11. Landingpages (Seiten, nicht Beiträge): Pflichtregeln gegen Layoutfehler

Gilt für Seiten mit eigenem Hero-Bereich, z. B. Uniqkey (Seite 7370). Vorlage für Farben, Buttons und Breite: `C:\Daten\CLAUDEPROJEKTE\WordpressPCD\DESIGN.md`.

### 11.1 Header überdeckt auf dem Handy den Hero (Fehler vom 2026-10-11)

- **Ursache:** Auf dem Handy (unter 768px) liegt der PCD-Header fest (`position:fixed`, Höhe 92px) über dem Seiteninhalt. Ein Hero mit wenig Abstand oben verschwindet darunter. Die H1 ist dann halb verdeckt.
- **Auf dem Desktop** (Header ca. 101px) ist der Header statisch und überlagert nichts.
- **Regel:** Der erste Container (Hero) bekommt mobil oben mindestens **136px** Abstand (92px Header plus ca. 44px Luft). Desktop oben 72px. Kein höherer Desktop-Wert, sonst entsteht eine große Lücke.
- **Style-String für den Hero (wörtlich übernehmen):**
  `display:flex; justify-content:center; padding:72px 20px 64px; background-image:linear-gradient(#043C7F 0%, #001E31 100%); @media(--mobile){padding-top:136px; padding-bottom:48px; padding-left:16px; padding-right:16px;}`
- **Mobil nur mit Einzelwerten** (`padding-top` usw.) schreiben, nicht mit der Kurzform `padding:136px 16px 48px`. Die Kurzform wurde im Test beim Speichern auf den alten Wert (40px) zurückgesetzt.

### 11.2 Nach jeder Layoutänderung prüfen

1. Vorschau-Link erzeugen (`elementor-create-preview-link`) und im Browser-Pane öffnen.
2. Viewport mit `resize_window` auf **375x812** (Mobil) und **1440x900** (Desktop) setzen, Seite neu laden.
3. Per JavaScript messen: `h1.top - header.bottom` muss **größer als 0** sein (Ziel mobil ca. 38px). Wert prüfen, nicht schätzen.
4. Bei Mobil zusätzlich: `document.documentElement.scrollWidth` gleich Viewportbreite (kein seitliches Scrollen), erster Button im Sichtbereich.
5. Danach Viewport mit `preset: "desktop"` zurücksetzen.
6. Bei Zweifel gespeicherte Werte mit `elementor-get-page-structure` (`include_content: true`) lesen. Das zeigt den Stand in der Datenbank.
7. Die öffentliche Seite kann durch WP Rocket zwischengespeichert sein. Mit Parameter testen (`?v=2`) und dem Nutzer sagen, dass er den Cache leeren oder neu laden soll.

### 11.3 Weitere bekannte Fallen

- **Doppelte H1:** Das Theme zeigt den Seitentitel als H1. Immer `elementor-update-page-settings` mit `{"hide_title": "yes"}` setzen. Die Seite hat dann genau eine H1 im Hero.
- **Verlauf:** `radial-gradient` wird vom Server verworfen. `linear-gradient` nutzen.
- **Hover-Farben:** Bei jedem Button Hover und Focus mit Schrift- UND Hintergrundfarbe setzen, sonst erscheint die Theme-Linkfarbe (dunkles Violett auf dunklem Button).
- **Listen:** `<ul>`/`<ol>` in einem `e-paragraph` erscheinen mit 14px (Theme-Regel), nicht mit der Absatzgröße. Stattdessen Zeilen mit `<br>` und Emoji (✅, 1️⃣) nutzen.
- **Sprungmarken (Anker):** Die Widgets haben kein ID-Feld. Keine Links wie `#vorteile` setzen.
- **Gleichzeitiger Editor:** Ist die Seite im Elementor-Editor offen, kann ein Speichern dort meine Änderungen überschreiben. Vor Änderungen den Nutzer bitten, den Editor zu schließen, und nach Änderungen den Stand lesen.
- **Mobile-Wert prüfen:** Nach `style_apply_mode: "replace"` den Mobil-Wert nachlesen. Er kann zurückspringen.
- **Karten mit Hover-Bewegung:** `transition: transform 300ms, box-shadow 300ms; &:hover{transform: translateY(-8px); box-shadow:0px 12px 24px rgba(0,0,0,0.3);}`
- **FAQ:** `e-accordion` mit `faq_schema: true`, Fragen ohne Emojis (sonst landen sie im Google-Schema).
- **Veröffentlicht?** Die Seite 7370 ist öffentlich erreichbar. Änderungen per Tool wirken dort sofort. Bei Entwürfen und Live-Seiten gilt: vor größeren Umbauten den Nutzer fragen.
