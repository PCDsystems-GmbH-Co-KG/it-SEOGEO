# SEO-Regelwerk für Webseiten (konsolidiert)

Zweck: Arbeitsgrundlage für Claude beim Erstellen und Prüfen von Webseitentexten.
Quellen: 11 Einzeldateien aus `regeln/SEO/` (Yoast-Checks, Löwen-Text SEO, Meta-Description-Leitfaden).
Gegengeprüft und ergänzt mit dem Skill `seo-audit` (coreyhaines31/marketingskills). Ergänzungen sind mit **[Skill]** markiert.
Sprache der Texte: Deutsch.

---

## 1. Schnellreferenz: Alle Grenzwerte

| Bereich | Regel | Wert |
|---|---|---|
| SEO-Titel | Länge | 15 bis 60 Zeichen, Ziel ca. 50 bis 60 (Pixelbreite prüfen) |
| SEO-Titel | Keyword | so weit vorne wie möglich |
| Meta-Description | Länge | max. ca. 155 bis 160 Zeichen, besser max. 1000 px |
| Meta-Description | Pflichtteile | Hauptkeyword, Suchintention, CTA |
| H1 | Anzahl pro Seite | genau 1 |
| Textabschnitt unter einer Überschrift | max. Wörter | 300 |
| Absatz | max. Wörter | 150 |
| Satz | gilt als lang ab | mehr als 20 Wörter |
| Lange Sätze | Anteil am Text | max. 25 % |
| Passiv | Anteil der Sätze | max. 10 % |
| Bindewörter | Anteil der Sätze | mindestens 30 % |
| Satzanfänge | gleiches Wort | max. 2 Sätze in Folge (ab 3 Warnung) |

---

## 2. Rangordnung der Arbeitsschritte

1. Fokus-Keyphrase festlegen (Abschnitt 3).
2. SEO-Titel schreiben (Abschnitt 4).
3. Meta-Description schreiben (Abschnitt 5).
4. Text strukturieren mit Überschriften (Abschnitt 6).
5. Text lesbar schreiben (Abschnitt 7).
6. Checkliste durchgehen (Abschnitt 9).

---

## 3. Keyword-Strategie

### 3.1 Fokus-Keyphrase
Der Suchbegriff, für den eine Seite ranken soll. Jede Seite bekommt genau eine.

Auswahl in drei Schritten:
1. **Begriff finden, nach dem Menschen suchen.** Long-Tail-Keyphrasen bevorzugen. Weniger Konkurrenz, mehr Conversions.
2. **Suchvolumen prüfen.** Mit Tools (z. B. Semrush in Yoast) Potenzial vergleichen.
3. **Keyphrase googeln.** Suchintention prüfen. Zeigt Google Videos, Produktseiten oder Blogbeiträge? Den Inhalt daran ausrichten.

Beispiele:
- Kurz: „Content Optimierung" (viel Volumen, viel Konkurrenz)
- Long-Tail: „Effektive Keyword-Recherche-Tools für kleine Unternehmen" (weniger Volumen, zielgenauer)

Nicht jede Seite braucht eine Fokus-Keyphrase. Beispiel: Kontaktseite. Nur Seiten optimieren, die dauerhaft organischen Traffic bringen sollen.

### 3.2 Synonyme
Wörter mit gleicher Bedeutung wie die Keyphrase (Hund = Vierbeiner).
- Vermeiden Keyword-Stuffing und machen den Text lesbarer.
- Google versteht Synonyme. Rankings für Synonym-Suchen sind möglich.
- Einsetzen in Überschriften, Meta-Description und Fließtext.

### 3.3 Verwandte Keywords (nicht verwechseln mit Synonymen)
Vertiefen das Thema, bedeuten aber etwas anderes (Hund → Hundefutter, Hundeleine, Gassi gehen). Sie geben Kontext und decken das Thema breit ab.

---

## 4. SEO-Titel (Title-Tag)

Der Titel ist ein Rankingfaktor und entscheidet über den Klick. Er bildet mit der Meta-Description das Snippet. Wegen Zero-Click-Searches (Antwort direkt bei Google oder KI) zählt ein überzeugender Titel mehr denn je.

**Grundregeln**
- Klar und prägnant, fasst das Thema exakt zusammen.
- Keyword möglichst am Anfang.
- 15 bis 60 Zeichen. Manche Quellen raten zu max. 40 Zeichen für optimale Keyword-Platzierung.
- Muss genau das versprechen, was der Nutzer sucht.

**9 Hebel für mehr Klicks**
1. Fragen stellen („Was ist SEO?").
2. Zeichenlimit voll nutzen, aber nicht überschreiten (Snippet-Tool).
3. Keyword auch in der URL.
4. Power-Wörter („mühelos", „am besten").
5. Emotionen wecken.
6. Aktualität: aktuelles Jahr nennen (z. B. 2026).
7. Neugier wecken.
8. Bildungsinhalte betonen (Anleitung, Guide, Schritt für Schritt).
9. Von Google-Ads-Texten lernen.

**2 Headline-Formeln**
- Formel 1: *Wie du [Wunsch], auch wenn / ohne [Einwand].*
  Beispiel: Mehr Reichweite für deinen Blog gewinnen: Wie du deine Leserschaft aufbaust, auch ohne teure Werbekampagnen.
- Formel 2: *Mit [Methode] erreichst du [Ziel], damit du [Wunsch].*
  Beispiel: Mit maßgeschneiderten SEO-Texten landest du auf Seite 1.

---

**[Skill] Ergänzungen zum Titel**
- Vor dem Schreiben die Ergebnisseite zur Ziel-Suchanfrage ansehen: Format, erwartete Wörter (best, kostenlos, Jahr, Zahl) und die Lücke, die kein Titel füllt.
- Aufbau: `[Hauptbegriff] + [Grund zum Klicken] + [Marke, nur wenn sie zieht]`. Unbekannte Marke nach hinten.
- Google kürzt nach Pixeln. Die wichtigsten Wörter in die ersten 50 Zeichen.
- Jeder Titel ist einmalig. Titel, H1, URL-Slug und Meta-Description beschreiben dasselbe Thema.
- Google schreibt Titel um, wenn sie zu lang, keyword-überladen, generisch oder nicht zur H1 passend sind. Dann Titel straffen und an H1 angleichen.
- „Kostenlos", Jahreszahl oder Zahl nur, wenn die Seite es einlöst. Slug nicht wegen Jahr oder Zahl ändern.
- Schwache CTR bei Top-5-Platz: nur Titel und Description ändern, Ausgangswert notieren, 3 bis 4 Wochen warten.

| Seitentyp | Muster |
|---|---|
| Produkt / Leistung | `[Kategorie] für [Zielgruppe] \| [Marke]` |
| Preise | `[Marke] Preise: Pakete und Kosten` |
| Vergleich | `[A] vs. [B]: [entscheidender Unterschied]` |
| Bestenliste | `[Zahl] beste [Dinge] für [Zielgruppe] ([Jahr])` |
| Anleitung | `So geht [Aufgabe]` oder `[Aufgabe] ohne [Hindernis]` |
| Definition | `Was ist [Begriff]? [Kurzer Nutzen]` |
| Leitfaden | `[Thema]: Der Leitfaden für [Zielgruppe]` |
| Problemlösung | `[Problem] beheben: [Lösung]` |

---

## 5. Meta-Description

Kurze Zusammenfassung im HTML-Head, meist unter dem Titel in den SERPs sichtbar.

**Rankingfaktor?** Nein, nur indirekt. Sie wirkt wie ein Werbetext und steigert die Klickrate (CTR). Hohe CTR kann langfristig bessere Rankings bringen.

**Warum selbst schreiben?**
- Google baut bei Long-Tail-Anfragen oft eigene Auszüge (über 60 % der Fälle).
- Beim Hauptkeyword nutzt Google meist die eigene Beschreibung.
- Facebook, LinkedIn & Co. nutzen sie beim Teilen, wenn keine Social-Tags gesetzt sind.

**5 Regeln**
1. **Länge:** ca. 155 bis 160 Zeichen, sicherer max. 1000 Pixel (breite Buchstaben brauchen mehr Platz). Mit SERP-Snippet-Generator prüfen.
2. **Hauptkeyword einbauen.** Kein Ranking-Boost, aber Fettdruck in den SERPs.
3. **Suchintention treffen.** Mit einer Frage zum Problem starten, Seite als Lösung anbieten.
4. **Call-to-Action am Ende** („Jetzt entdecken!", „Hier mehr erfahren", „Gleich lesen").
5. **Neugier** durch bewussten Abbruch („...") kurz vor dem Limit.

**[Skill] Ergänzung:** Jede Seite braucht eine einmalige Description. Doppelte oder automatisch erzeugte Texte vermeiden. Klarer Nutzen statt Füllsatz.

**Sonderfall:** `data-nosnippet` markiert Textteile, die Google nicht als Snippet nutzen soll. Vorsichtig einsetzen.

---

## 6. Struktur: Überschriften

| Tag | Funktion |
|---|---|
| H1 | Haupttitel, nur einmal pro Seite |
| H2 | Hauptabschnitte (Kapitel) |
| H3 bis H6 | weitere Untergliederung innerhalb eines H2 |

**Warum:** Nutzer scannen Texte. Überschriften sind Wegweiser. Suchmaschinen erkennen daran Struktur und Hauptthemen.

**Regeln**
- Unter einer Überschrift max. **300 Wörter** am Stück.
- Überschriften aussagekräftig formulieren. Der Leser soll wissen, worum es geht.
- Fokus-Keyphrase oder Synonyme in einigen (nicht allen) H2/H3 verwenden.
- Hierarchie einhalten: H1 → H2 → H3 → H2. Nicht von H2 auf H4 springen.
- **[Skill]** H1 enthält das Hauptkeyword und passt zum Titel. Überschriften nie nur fürs Styling nutzen. Jede Seite hat eine H1.

---

## 7. Lesbarkeit (Yoast-Checks)

Gutes Lesen hält Nutzer länger auf der Seite und senkt die Absprungrate. Das ist ein positives Signal für Google.

### 7.1 Absatzlänge
- Max. **150 Wörter** pro Absatz.
- Ein Absatz = ein Gedanke. Idealerweise baut er um einen Kernsatz auf (meist der erste).
- Lange Absätze am Themenwechsel teilen. Aufzählungen in Bullet-Listen umwandeln.
- Ziel: keine Textwüsten, gute Scannbarkeit, besonders am Smartphone.

### 7.2 Satzlänge
- Lang = mehr als **20 Wörter**. Davon max. **25 %** der Sätze.
- Kürzen: aus einem Satz zwei machen, Füllwörter streichen (eigentlich, sozusagen, natürlich), Schachtelsätze vermeiden, laut vorlesen.
- Pro Satz ein Kerngedanke.

### 7.3 Passiv
- Max. **10 %** der Sätze im Passiv.
- Passiv ist schwerer zu lesen, wirkt distanziert und lässt offen, wer handelt.
- Methode: Akteur finden und zum Subjekt machen.
  - Schlecht: Das neue Feature wurde von unserem Team entwickelt.
  - Besser: Unser Team hat das neue Feature entwickelt.
- Gelegentliches Passiv ist in Ordnung, wenn der Handelnde unwichtig oder unbekannt ist.

### 7.4 Bindewörter (Transition Words)
- Mindestens **30 %** der Sätze enthalten ein Bindewort.
- Sie verbessern den Textfluss und machen Beziehungen zwischen Gedanken klar.

| Funktion | Beispiele |
|---|---|
| Aufzählung, Ergänzung | und, außerdem, zudem, darüber hinaus, erstens, zweitens |
| Ursache, Wirkung | weil, deshalb, da, aus diesem Grund, folglich |
| Gegensatz, Einschränkung | aber, jedoch, obwohl, andererseits, trotzdem |
| Zeit | während, danach, vorher, gleichzeitig, schließlich |
| Zusammenfassung | zusammenfassend, kurz gesagt, abschließend |

### 7.5 Aufeinanderfolgende Sätze
- Warnung ab **3 Sätzen in Folge** mit demselben Anfangswort.
- Negativbeispiel: „Wir bieten ... Wir haben ... Wir freuen uns ..."
- Lösung: Bindewort an den Anfang, Satz umstellen, kurze Sätze verbinden, Subjekt wechseln (Leser oder Nutzen statt „Wir").

### 7.6 Wort-Komplexität
- Seltene, sehr lange oder fachsprachliche Wörter vermeiden. Sie erhöhen die Absprungrate und schließen Leser aus.
- Schreiben wie man spricht. Fachjargon nur bei echtem Bedarf, dann erklären.
- Einfacher: „umsetzen" oder „einbauen" statt „implementieren".

---

## 8. Hinweise zu Widersprüchen und Fallen

- **Titellänge:** Die Quelle nennt 15 bis 60 Zeichen, der Skill 50 bis 60. Kein echter Widerspruch: 60 ist die Obergrenze. Google kürzt nach Pixelbreite, nicht nach Zeichen. Titel im Snippet-Tool prüfen. Bei Zweifel eher kürzer.
- **Meta-Description-Länge:** Zeichen (155 bis 160) und Pixel (1000) sind zwei Näherungen. Die Pixelmessung gilt als genauer.
- **Titel als Rankingfaktor, Meta-Description nicht:** Das ist ein echter Unterschied. Die Description nur für die Klickrate optimieren.
- **Neugier-Tricks:** Formulierungen wie „Nr. 6 wird dich schockieren" sind Clickbait. Nur nutzen, wenn der Inhalt hält, was der Titel verspricht. Sonst steigt die Absprungrate.
- **Cliffhanger in der Description:** Google schreibt Snippets oft selbst um. Wirkung nicht garantiert.
- **Yoast-Werte sind Richtwerte,** keine Google-Regeln. Sie sichern Lesbarkeit, ersetzen aber keinen guten Inhalt.
- **Jahreszahl im Titel:** Nur setzen, wenn der Inhalt wirklich aktuell ist, und jährlich pflegen.
- **Satzanfänge:** Yoast warnt ab 3 gleichen. Praktisch also maximal 2 in Folge.

---

## 9. Checkliste pro Seite

**Keyword**
- [ ] Fokus-Keyphrase festgelegt, Suchintention per Google-Suche geprüft
- [ ] Synonyme und verwandte Keywords gesammelt

**Snippet**
- [ ] Titel 15 bis 60 Zeichen, Keyword vorne, Pixelbreite geprüft
- [ ] Titel verspricht, was die Seite liefert
- [ ] Keyword auch in der URL
- [ ] Meta-Description max. ca. 155 Zeichen / 1000 px
- [ ] Keyword, Frage oder Nutzen, CTA in der Description

**Struktur**
- [ ] Genau eine H1
- [ ] H2/H3 logisch gestaffelt, keine übersprungenen Ebenen
- [ ] Keyphrase oder Synonym in einigen Überschriften
- [ ] Nie mehr als 300 Wörter ohne Überschrift
- [ ] Hauptkeyword in den ersten 100 Wörtern, Alt-Texte gesetzt, interne Links vorhanden

**Lesbarkeit**
- [ ] Absätze max. 150 Wörter, ein Gedanke je Absatz
- [ ] Höchstens 25 % Sätze über 20 Wörter
- [ ] Höchstens 10 % Passiv
- [ ] Mindestens 30 % Sätze mit Bindewort
- [ ] Keine 3 Sätze in Folge mit gleichem Anfangswort
- [ ] Keine unnötig komplexen Wörter

---

## 10. [Skill] Weitere On-Page-Regeln, die in den Quelldateien fehlen

**Inhalt**
- Hauptkeyword in den ersten 100 Wörtern.
- Die Suchanfrage in den ersten zwei Sätzen beantworten, dann vertiefen.
- Suchintention treffen und besser sein als die Top-Ergebnisse. Verwandte Keywords natürlich einbauen.
- Dünne oder doppelte Inhalte vermeiden.
- **Kannibalisierung:** Zwei Seiten für dieselbe Suchanfrage bremsen sich. Eine Seite als Besitzer wählen, Brauchbares zusammenführen, andere per 301 umleiten.

**URL**
- Lesbar, beschreibend, klein geschrieben, mit Bindestrichen. Keine unnötigen Parameter. Keyword wenn natürlich möglich.

**Bilder**
- Sprechende Dateinamen, Alt-Text auf allen Bildern (beschreibt das Bild), komprimiert, moderne Formate (WebP), Lazy Loading, responsive Bilder.

**Interne Links**
- Wichtige Seiten gut verlinken, beschreibende Ankertexte, keine kaputten Links, keine verwaisten Seiten, wichtige Seiten innerhalb von 3 Klicks von der Startseite.

**E-E-A-T (Vertrauen)**
- Erfahrung zeigen, Autor mit Qualifikation nennen, Aussagen belegen, Kontakt, Impressum und Datenschutz sichtbar, HTTPS.

---

## 11. [Skill] Technische Grundlagen (Kurzcheck)

Reihenfolge der Prüfung: 1. Crawling und Indexierung, 2. Technik und Tempo, 3. On-Page, 4. Inhaltsqualität, 5. Autorität und Links.

| Bereich | Prüfen |
|---|---|
| Crawling | robots.txt blockiert nichts Wichtiges, Sitemap-Verweis vorhanden |
| Sitemap | nur kanonische, indexierbare URLs, in Search Console eingereicht |
| Indexierung | kein versehentliches `noindex`, Canonicals zeigen richtig, keine Redirect-Ketten, keine Soft-404 |
| Canonical | Selbst-Canonical auf einmaligen Seiten, einheitlich https, www und Slash |
| Core Web Vitals | LCP unter 2,5 s, INP unter 200 ms, CLS unter 0,1 |
| Mobil | responsiv, Viewport gesetzt, kein horizontales Scrollen, gleicher Inhalt wie Desktop |
| Sicherheit | durchgehend HTTPS, gültiges Zertifikat, kein Mixed Content |
| Schema | nur mit gerendertem Browser oder Rich Results Test prüfen. Abruf per curl übersieht per JavaScript eingefügtes JSON-LD (z. B. von Yoast) |

Mehrsprachige Seiten: hreflang mit Selbstverweis und Rückverweis, gültige Codes (`en-GB`, nie `en-UK`), `x-default`, Canonical pro Sprache auf sich selbst, nie sprachübergreifend.

---

## 12. [Skill] Neue Seite veröffentlichen: Startcheck

- [ ] Interne Links von mindestens 3 passenden Seiten, beschreibende Ankertexte
- [ ] Einmaliger Titel und einmalige Description passend zur Suchanfrage
- [ ] Eine H1, passend zum Titel
- [ ] Selbst-Canonical gesetzt
- [ ] In der XML-Sitemap
- [ ] Strukturierte Daten, wo passend
- [ ] Hauptinhalt im HTML, nicht nur per JavaScript
- [ ] Indexierbar (kein `noindex`, nicht in robots.txt gesperrt)
- [ ] Danach einmal Indexierung in Search Console anfragen

## 13. [Skill] Bestehende Seiten verbessern (Platz 8 bis 20)

1. In der Search Console Seite und Suchanfrage der letzten 28 Tage prüfen.
2. Gruppen: Platz 8 bis 20 (Inhalt und Links), Platz 1 bis 5 mit schwacher CTR (nur Titel und Description), Platz 4 bis 7 bei wichtigen Anfragen.
3. Die drei Ergebnisse darüber ansehen. Grund nennen: Intention, fehlender Abschnitt, Aktualität, Format oder Links.
4. Kleinste Änderung wählen: fehlenden Abschnitt ergänzen, interne Links setzen, Veraltetes aktualisieren.
5. Ausgangswerte notieren, 3 bis 4 Wochen warten. Bringen zwei Runden nichts, liegt es an Intention oder Autorität, nicht am Text.

---

## 14. Quellenverzeichnis

| Datei | Thema |
|---|---|
| fokus_keyphrase_erklaerung.md | Fokus-Keyphrase (Yoast) |
| fokus_synonyme_erklaerung.md | Synonyme, verwandte Keywords (Yoast) |
| perfekter_seo_titel.md | SEO-Titel (Löwen-Text SEO) |
| SEO Meta-Description.md | Meta-Description |
| zwischen_berschriften_erklaerung.md | Überschriften (Yoast) |
| absatzlaenge_erklaerung.md | Absatzlänge (Yoast) |
| satzlaenge_erklaerung.md | Satzlänge (Yoast) |
| passivitaet_passiv_erklaerung.md | Passiv (Yoast) |
| bindewoerter_erklaerung.md | Bindewörter (Yoast) |
| aufeinanderfolgende_saetze_erklaerung.md | Satzanfänge (Yoast) |
| wort_komplexitaet_erklaerung.md | Wort-Komplexität (Yoast) |
| Skill `seo-audit` (SKILL.md, title-tags.md, rankings-push.md) | Gegenprüfung und Ergänzungen **[Skill]** |
