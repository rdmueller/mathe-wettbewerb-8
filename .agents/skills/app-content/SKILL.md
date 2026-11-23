---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

Explainer zur Vorbereitung auf die 1. Runde des Mathematik-Wettbewerbs des Landes Hessen, Klasse 8, Gruppe A
(Gymnasium). `strand: none` (die Themen reichen über fünf Stränge der Lernlandkarte Mathematik). Nur Deutsch.

## Curriculum

- Hessen, Gymnasium, Jahrgang 8 (Wiederholung von Stoff aus 5–7).
- Wettbewerb: https://mathematik-wettbewerb.de/pages/index.xml; Informationen zur 1. Runde 2026/2027:
  https://mathematik-wettbewerb.de/pages/downloads/mw_1r_informationen.pdf – 8 Pflichtaufgaben je 3 BE, 2 von 4
  Wahlaufgaben je 12 BE, **ohne Taschenrechner und Formelsammlung**.
- Orientierung: „Bildungsstandards und Inhaltsfelder – Das neue Kerncurriculum für Hessen, Sekundarstufe I –
  Gymnasium, Mathematik“, Hessisches Kultusministerium, 2011,
  https://kultus.hessen.de/sites/kultus.hessen.de/files/2021-07/kerncurriculum_mathematik_gymnasium.pdf, Kap. 7.2
  (S. 24) und Übersicht Jg. 7/8 (S. 26–29).
- Themen und Reihenfolge folgen der Checkliste der Erstellerin/des Erstellers (Pflichtthemen 1–8, W1, W2), ergänzt um
  W3 und W4 aus den Wahlaufgaben der letzten Jahre. Die Checkliste selbst bleibt lokal.

## Competencies

Ordner `src/<kapitel>/`, Seite `src/<kapitel>/<seite>.yaml`. Übungs-Ids: `<seite>-<kurzname>`, z. B.
`dreieck-flaeche`. In Klammern die ähnlichste Kompetenz der Lernlandkarte (nur Orientierung, nicht im YAML).

- `zuordnungen`: `tabelle-koordinaten` Ich kann Zuordnungen in Tabellen darstellen und Punkte im Koordinatensystem
  eintragen und ablesen (`zuordnungen`, `koordinatensystem`) · `proportional` Ich kann proportionale Zuordnungen
  erkennen und Tabellen mit dem Faktor ergänzen · `antiproportional` Ich kann antiproportionale Zuordnungen erkennen und
  von proportionalen unterscheiden · `graphen` Ich kann am Graphen erkennen, ob eine Zuordnung proportional (Gerade
  durch den Ursprung) oder antiproportional (Hyperbel) ist.
- `prozent`: `prozentwert` Ich kann den Prozentwert mit G · p % = P berechnen · `prozentsatz-grundwert` Ich kann die
  Formel umstellen und den Prozentsatz oder den Grundwert berechnen · `sachaufgaben` Ich kann Sachaufgaben mit
  gegeben/gesucht, Formel, Rechnung und Antwort lösen.
- `flaechen`: `quadrat-rechteck` Ich kann Flächeninhalt und Umfang von Quadrat und Rechteck berechnen · `dreieck` Ich
  kann Flächeninhalt und Umfang von Dreiecken berechnen und zu jeder Seite die Höhe einzeichnen, auch außen ·
  `parallelogramm-trapez` Ich kann Flächeninhalt und Umfang von Parallelogramm und Trapez berechnen · `quader-wuerfel`
  Ich kann das Volumen von Quader und Würfel berechnen · `netz-oberflaeche` Ich kann Netze von Quader und Würfel
  erkennen und ihre Oberfläche berechnen · `formeln-umstellen` Ich kann eine Flächen- oder Volumenformel nach einer
  Größe umstellen.
- `terme`: `aufstellen` Ich kann zu einem Text oder einer Rechenvorschrift einen Term aufstellen · `werte-berechnen`
  Ich kann den Wert eines Terms berechnen, wenn ich eine Zahl für x einsetze · `zusammenfassen` Ich kann gleichartige
  Glieder zusammenfassen · `produkte` Ich kann Produkte wie 3x · (−2y) berechnen und dabei zuerst das Vorzeichen
  bestimmen.
- `wahrscheinlichkeit`: `laplace` Ich kann den Ergebnisraum aufschreiben und die Laplace-Wahrscheinlichkeit berechnen ·
  `baumdiagramm` Ich kann ein Baumdiagramm mit allen Wahrscheinlichkeiten zeichnen · `pfadregeln` Ich kann mit den
  Pfadregeln Wahrscheinlichkeiten berechnen.
- `symmetrie`: `symmetrie-erkennen` Ich kann Achsen- und Punktsymmetrie erkennen und Symmetrieachsen finden ·
  `spiegeln-drehen` Ich kann Figuren an einer Achse spiegeln und um einen Punkt drehen.
- `winkel`: `winkelsumme` Ich kann fehlende Winkel mit der Winkelsumme im Dreieck und im Viereck berechnen ·
  `geradenkreuzungen` Ich kann Neben-, Scheitel-, Stufen- und Wechselwinkel berechnen.
- `brueche`: `plus-minus` Ich kann Brüche und Dezimalbrüche addieren und subtrahieren · `mal-geteilt` Ich kann Brüche
  und Dezimalbrüche multiplizieren und dividieren · `rechenregeln` Ich kann Klammern und Punkt vor Strich beachten.
- `w2-konstruktionen`: `planfigur` Ich kann eine Planfigur zeichnen und richtig bezeichnen · `kongruenzsaetze` Ich
  kann erkennen, welcher Kongruenzsatz passt und ob das Dreieck eindeutig ist · `konstruktion-schritte` Ich kann die
  Schritte einer Konstruktion ordnen, auch mit Höhe, Seiten- oder Winkelhalbierender · `winkel-pruefen` Ich kann einen
  fehlenden Winkel berechnen und eine Konstruktion durch Nachmessen prüfen.
- `w1-gleichungen`: `klammern` Ich kann Klammern auflösen und zwei Klammern ausmultiplizieren · `gleichungen` Ich kann
  eine Gleichung lösen, auch wenn x² wegfällt oder Dezimalzahlen vorkommen · `ungleichungen` Ich kann eine Ungleichung
  lösen und das Zeichen drehen · `nullprodukt` Ich kann eine Gleichung mit dem Satz vom Nullprodukt lösen ·
  `loesungsmenge` Ich kann die Lösungsmenge angeben, G = ℤ beachten und die Probe machen.
- `w3-prozent`: `zu-abnahme` Ich kann den neuen Wert nach einer Zu- oder Abnahme mit dem Faktor berechnen ·
  `vergleich` Ich kann angeben, um wie viel Prozent ein Wert größer oder kleiner ist · `mehrere-aenderungen` Ich kann
  mehrere Änderungen nacheinander berechnen und Prozente von Prozentpunkten unterscheiden.
- `w4-zufall`: `ohne-zuruecklegen` Ich kann beim Ziehen ohne Zurücklegen die Wahrscheinlichkeiten anpassen ·
  `ereignisse-pfade` Ich kann „genau einmal“ und „mindestens einmal“ den Pfaden zuordnen · `gegenereignis` Ich kann
  eine Wahrscheinlichkeit über das Gegenereignis berechnen.

**Übungen je Seite** (Stand wie gebaut; `*` = `generated`):

- `zuordnungen/tabelle-koordinaten`: `tabelle-koordinaten-start`, `tabelle-koordinaten-welcher`, `tabelle-koordinaten-ablesen`, `tabelle-koordinaten-achse`, `tabelle-koordinaten-taxi*`, `tabelle-koordinaten-rechteck*`
- `zuordnungen/proportional`: `proportional-start`, `proportional-alter`, `proportional-tabelle`, `proportional-preis*`, `proportional-welche`, `proportional-rezept*`
- `zuordnungen/antiproportional`: `antiproportional-start`, `antiproportional-geld`, `antiproportional-tabelle`, `antiproportional-zuordnen`, `antiproportional-helfer*`, `antiproportional-vorrat*`
- `zuordnungen/graphen`: `graphen-start`, `graphen-zuordnen`, `graphen-gerade*`, `graphen-hyperbel*`, `graphen-gleichung`, `graphen-punkt`
- `prozent/prozentwert`: `prozentwert-start`, `prozentwert-grundwert`, `prozentwert-anteile`, `prozentwert-verein*`, `prozentwert-rabatt*`, `prozentwert-tauschen`, `prozentwert-schulweg`
- `prozent/prozentsatz-grundwert`: `prozentsatz-grundwert-start`, `prozentsatz-grundwert-gesucht`, `prozentsatz-grundwert-umfrage*`, `prozentsatz-grundwert-sparen*`, `prozentsatz-grundwert-rechnung`, `prozentsatz-grundwert-test`
- `prozent/sachaufgaben`: `sachaufgaben-start`, `sachaufgaben-was-fehlt`, `sachaufgaben-teurer-als`, `sachaufgaben-teurer*`, `sachaufgaben-vorher*`, `sachaufgaben-wahl`
- `flaechen/quadrat-rechteck`: `quadrat-rechteck-start`, `quadrat-rechteck-einheit`, `quadrat-rechteck-flaeche*`, `quadrat-rechteck-umfang*`, `quadrat-rechteck-quadrat*`, `quadrat-rechteck-gleicher-umfang`, `quadrat-rechteck-garten`
- `flaechen/dreieck`: `dreieck-start`, `dreieck-welche-hoehe`, `dreieck-drei-hoehen`, `dreieck-flaeche*`, `dreieck-hoehe-aussen*`, `dreieck-umfang*`, `dreieck-rest*`, `dreieck-rueckwaerts*`
- `flaechen/parallelogramm-trapez`: `parallelogramm-trapez-start`, `parallelogramm-trapez-ablesen`, `parallelogramm-trapez-parallelogramm*`, `parallelogramm-trapez-trapez*`, `parallelogramm-trapez-umfang*`, `parallelogramm-trapez-hoehe`
- `flaechen/quader-wuerfel`: `quader-wuerfel-start`, `quader-wuerfel-einheit`, `quader-wuerfel-volumen*`, `quader-wuerfel-wuerfel*`, `quader-wuerfel-liter*`, `quader-wuerfel-bauen`
- `flaechen/netz-oberflaeche`: `netz-oberflaeche-start`, `netz-oberflaeche-sechs-quadrate`, `netz-oberflaeche-quader*`, `netz-oberflaeche-wuerfel*`, `netz-oberflaeche-ohne-deckel*`, `netz-oberflaeche-rueckwaerts`
- `flaechen/formeln-umstellen`: `formeln-umstellen-start`, `formeln-umstellen-schritte`, `formeln-umstellen-rechteck*`, `formeln-umstellen-dreieck*`, `formeln-umstellen-quader*`, `formeln-umstellen-trapez`, `formeln-umstellen-wuerfel`
- `terme/aufstellen`: `aufstellen-start`, `aufstellen-dreifache-summe`, `aufstellen-woerter`, `aufstellen-schritte`, `aufstellen-umfang*`, `aufstellen-popcorn*`, `aufstellen-figur`
- `terme/werte-berechnen`: `werte-berechnen-start`, `werte-berechnen-52`, `werte-berechnen-einsetzen*`, `werte-berechnen-klammer*`, `werte-berechnen-rueckwaerts`, `werte-berechnen-tarife`
- `terme/zusammenfassen`: `zusammenfassen-start`, `zusammenfassen-gleichartig`, `zusammenfassen-koeffizient*`, `zusammenfassen-xy`, `zusammenfassen-sortieren*`, `zusammenfassen-minus`, `zusammenfassen-l-figur`
- `terme/produkte`: `produkte-start`, `produkte-term`, `produkte-vier-faktoren`, `produkte-koeffizient*`, `produkte-minus-minus*`, `produkte-quadrat`, `produkte-figur`
- `wahrscheinlichkeit/laplace`: `laplace-start`, `laplace-urne`, `laplace-ueben*`, `laplace-augensumme`, `laplace-anzahl*`, `laplace-vergleich`
- `wahrscheinlichkeit/baumdiagramm`: `baumdiagramm-start`, `baumdiagramm-ablesen`, `baumdiagramm-ergaenzen*`, `baumdiagramm-summe`, `baumdiagramm-pfade*`, `baumdiagramm-gluecksrad`
- `wahrscheinlichkeit/pfadregeln`: `pfadregeln-start`, `pfadregeln-rechnung`, `pfadregeln-pfad*`, `pfadregeln-gleiche-farbe*`, `pfadregeln-muenze-wuerfel`, `pfadregeln-oder`, `pfadregeln-rueckwaerts`
- `symmetrie/symmetrie-erkennen`: `symmetrie-erkennen-start`, `symmetrie-erkennen-nur-punkt`, `symmetrie-erkennen-art*`, `symmetrie-erkennen-achsen*`, `symmetrie-erkennen-vierecke`, `symmetrie-erkennen-quadrat`, `symmetrie-erkennen-woerter`
- `symmetrie/spiegeln-drehen`: `spiegeln-drehen-start`, `spiegeln-drehen-schraeg`, `spiegeln-drehen-achse*`, `spiegeln-drehen-halbe*`, `spiegeln-drehen-viertel*`, `spiegeln-drehen-zwei-achsen`, `spiegeln-drehen-richtung`
- `winkel/winkelsumme`: `winkelsumme-start`, `winkelsumme-dreieck*`, `winkelsumme-viereck*`, `winkelsumme-zwei-stumpfe`, `winkelsumme-basiswinkel*`, `winkelsumme-doppelt`, `winkelsumme-viereck-teile`
- `winkel/geradenkreuzungen`: `geradenkreuzungen-start`, `geradenkreuzungen-paare`, `geradenkreuzungen-nebenwinkel*`, `geradenkreuzungen-zwei-schritte*`, `geradenkreuzungen-nicht-parallel`, `geradenkreuzungen-halbierende`, `geradenkreuzungen-scheitel`
- `brueche/plus-minus`: `plus-minus-start`, `plus-minus-addieren*`, `plus-minus-subtrahieren*`, `plus-minus-dezimal*`, `plus-minus-luecke`, `plus-minus-gemischt`, `plus-minus-taschengeld`
- `brueche/mal-geteilt`: `mal-geteilt-start`, `mal-geteilt-mal*`, `mal-geteilt-geteilt*`, `mal-geteilt-komma*`, `mal-geteilt-stuecke*`, `mal-geteilt-dezimal`, `mal-geteilt-band`
- `brueche/rechenregeln`: `rechenregeln-start`, `rechenregeln-schritte`, `rechenregeln-punkt-vor-strich*`, `rechenregeln-klammer*`, `rechenregeln-links-rechts`, `rechenregeln-wettbewerb`
- `w2-konstruktionen/planfigur`: `planfigur-start`, `planfigur-fehler`, `planfigur-richtung`, `planfigur-zuordnen`, `planfigur-gegenueber*`, `planfigur-winkel-b*`, `planfigur-wettbewerb`
- `w2-konstruktionen/kongruenzsaetze`: `kongruenzsaetze-start`, `kongruenzsaetze-satz*`, `kongruenzsaetze-eindeutig*`, `kongruenzsaetze-ssw-richtig`, `kongruenzsaetze-welche`, `kongruenzsaetze-begruendung`
- `w2-konstruktionen/konstruktion-schritte`: `konstruktion-schritte-start`, `konstruktion-schritte-zuerst*`, `konstruktion-schritte-sws`, `konstruktion-schritte-ssw`, `konstruktion-schritte-linien`, `konstruktion-schritte-seitenhalbierende`, `konstruktion-schritte-winkelhalbierende`, `konstruktion-schritte-flaeche*`
- `w2-konstruktionen/winkel-pruefen`: `winkel-pruefen-start`, `winkel-pruefen-wsw*`, `winkel-pruefen-laengste`, `winkel-pruefen-messen`, `winkel-pruefen-hoehe*`, `winkel-pruefen-wettbewerb`
- `w1-gleichungen/klammern`: `klammern-start`, `klammern-minus`, `klammern-zahl*`, `klammern-zwei*`, `klammern-zwei-minus*`, `klammern-term`, `klammern-wettbewerb`
- `w1-gleichungen/gleichungen`: `gleichungen-start`, `gleichungen-schritte`, `gleichungen-einfach*`, `gleichungen-beide-seiten*`, `gleichungen-dezimal*`, `gleichungen-x-quadrat*`, `gleichungen-wettbewerb`
- `w1-gleichungen/ungleichungen`: `ungleichungen-start`, `ungleichungen-wann`, `ungleichungen-teilen*`, `ungleichungen-zwei-seiten*`, `ungleichungen-gleich`, `ungleichungen-wettbewerb`
- `w1-gleichungen/nullprodukt`: `nullprodukt-start`, `nullprodukt-loesungen`, `nullprodukt-x-faktor`, `nullprodukt-kleinere*`, `nullprodukt-groessere*`, `nullprodukt-nur-null`, `nullprodukt-wettbewerb`
- `w1-gleichungen/loesungsmenge`: `loesungsmenge-start`, `loesungsmenge-leer`, `loesungsmenge-bereich`, `loesungsmenge-anzahl*`, `loesungsmenge-kleinste*`, `loesungsmenge-wettbewerb`
- `w3-prozent/zu-abnahme`: `zu-abnahme-start`, `zu-abnahme-faktor`, `zu-abnahme-faktoren`, `zu-abnahme-zunahme*`, `zu-abnahme-abnahme*`, `zu-abnahme-rueckwaerts*`, `zu-abnahme-werbung`
- `w3-prozent/vergleich`: `vergleich-start`, `vergleich-teilen`, `vergleich-mehr*`, `vergleich-weniger*`, `vergleich-wer-hat-recht`, `vergleich-ticket`
- `w3-prozent/mehrere-aenderungen`: `mehrere-aenderungen-start`, `mehrere-aenderungen-rechnung`, `mehrere-aenderungen-reihenfolge`, `mehrere-aenderungen-preis*`, `mehrere-aenderungen-insgesamt*`, `mehrere-aenderungen-punkte`, `mehrere-aenderungen-wahl`
- `w4-zufall/ohne-zuruecklegen`: `ohne-zuruecklegen-start`, `ohne-zuruecklegen-ast`, `ohne-zuruecklegen-zweimal-rot*`, `ohne-zuruecklegen-lose*`, `ohne-zuruecklegen-gummibaerchen`, `ohne-zuruecklegen-rueckwaerts`
- `w4-zufall/ereignisse-pfade`: `ereignisse-pfade-start`, `ereignisse-pfade-zuordnen`, `ereignisse-pfade-hoechstens`, `ereignisse-pfade-genau*`, `ereignisse-pfade-hoechstens-rot*`, `ereignisse-pfade-gluecksrad`, `ereignisse-pfade-auslosen`
- `w4-zufall/gegenereignis`: `gegenereignis-start`, `gegenereignis-zuordnen`, `gegenereignis-gluecksrad`, `gegenereignis-urne*`, `gegenereignis-gluecksrad-prozent*`, `gegenereignis-gerade`, `gegenereignis-rueckwaerts`

## Content structure

- Startseite (`src/app.yaml`, `intro`): der Wettbewerb in drei Sätzen; Vorgehen für jede Aufgabe (ganz lesen – Thema
  bestimmen – Plan – rechnen – Antwortsatz); Hinweis auf die Selbsteinschätzung.
- Jede Seite, Abschnitte in dieser Reihenfolge, Ids fest, Titel passend zur Seite:
  1. `start` – eine leichte Aufgabe vor jeder Erklärung (Titel z. B. „Probier zuerst“).
  2. `regel` – Herleitung mit Abbildung und `formula`; die Lernenden leiten ab, nicht nur ablesen.
  3. `beispiel` – eine Box mit Rechenweg, eigene Zahlen.
  4. `merke` – nur wenn es einen typischen Fehler gibt: Box „Merke“.
  5. `uebung` – mindestens 4 Aufgaben, leicht → schwer, mindestens eine `generated`; letzter Satz: was als Nächstes kommt.
- Die erste Seite eines Kapitels beginnt (vor `start`) mit Abschnitt `brauchst` „Das brauchst du hier“, wenn das Kapitel
  Vorwissen braucht, das die App nicht übt (Einheiten bei `flaechen`, Kürzen/Erweitern bei `brueche`,
  Grundkonstruktionen bei `w2-konstruktionen`): kurz, ohne Aufgabe.
- Seitenbeginn: ein Satz „Ziel: Ich kann …“ und wie die Seite an die vorige anknüpft.
- Höchstens 350 Wörter Text und 350 in Aufgaben je Seite; Abbildung, Tabelle oder Aufgabe in den ersten 4 Blöcken.
- Selbsteinschätzung in jedem `chapter.yaml` (`selfAssessment`), 2 Aufgaben je Seite, bevorzugt `generated`.
- Kapitel 9–12 heißen „Wahlaufgabe W2 …“, „W1 …“, „W3 …“, „W4 …“ wie im Wettbewerb; Reihenfolge wie die Checkliste.
- Aufgaben- und Rückmeldungstext je Seite oft 350–450 Wörter (Hinweis `explainer-text-load`, akzeptiert: viele
  Übungen sind der Zweck der App); Lesetext unter 350.
- Keine Geschichte; Aufgaben in Alltagssituationen (Preise, Spiele, Sport, Basteln, Garten).

## Terminology

- Wörter der Checkliste: Zuordnung, proportional/antiproportional, Grundwert G, Prozentwert P, Prozentsatz p %,
  Grundseite g, Höhe h, Planfigur, Kongruenzsatz SSS/SWS/WSW/SsW, Ergebnisraum, Laplace-Wahrscheinlichkeit,
  Baumdiagramm, Pfadregeln, Gegenereignis, Lösungsmenge L, Grundmenge G = ℤ (bei W1 G heißt Grundmenge, bei Prozent G
  heißt Grundwert: im Text immer ausschreiben).
- Schreibweise: Malpunkt „·“, Geteilt „:“, Dezimalkomma, Einheit mit Leerzeichen („12 cm²“), Winkel griechisch
  α, β, γ, δ; Dreieck ABC gegen den Uhrzeigersinn, Seite a gegenüber A.
- Wahrscheinlichkeit als gekürzter Bruch, wo nicht anders gefragt.
- Anrede: „du“, einfache Sprache, kurze Sätze; keine Kindersprache (13–14 Jahre).

## Exercise patterns

| Muster | Form | Was variiert | Beispiel |
|---|---|---|---|
| Rechenaufgabe mit Fehlerdiagnose | `generated`, `compare: { number: … }`, 2–3 `mistakes`, `hint`, `steps` | Zahlen ohne Taschenrechner lösbar (`where`) | `flaechen/dreieck.yaml`, `dreieck-flaeche`: Fehler `g * h` → „durch 2 teilen vergessen“ |
| Bruch als Auswahl | `generated` mit `compare: { choice }`: richtiger Bruch und Brüche aus typischen Fehlern | Zähler, Nenner | 2/3 + 1/4 → 11/12, 3/7, 3/12 |
| Term als Auswahl | `single-choice` oder `generated` mit `choice`; Zahl vor x als `number` | Koeffizienten | 3x · (−2y) → −6xy, 6xy, x − 2y |
| Erkennen mit Begründung | `true-false`, `single-choice`, `matching`, jede Option mit `info` | Situation | „Je mehr Zeit, desto mehr Wasser – proportional?“ |
| Ablesen | `image` als `material`, dann `number`/`single-choice` | Bild | Punkt im Koordinatensystem |
| Schritte ordnen | `ordering` | Schritte | Konstruktion SWS |
| Lösung einer Gleichung | `generated` `number` (x = …); Ungleichung als `choice`; Lösungsmenge `multiple-choice` | Koeffizienten | (x + 4)(x − 3) = 0 |

- Zahlenbereich: ganze Zahlen meist −20 … 20, Längen 1–20 cm (ganz oder ,5), Prozentsätze in 5er-Schritten (dazu 1 %,
  12,5 %), Nenner bis 12, Würfel/Münzen/Glücksräder bis 8 Felder, Urnen bis 10 Kugeln.
- Daten (je Datei ein Kommentar oben erklärt die Felder):
  - `src/data/zufallsversuche.yaml` – Würfel, Glücksräder, Urnen mit einem Ereignis; richtiger Bruch und drei falsche
    als Text (`wahrscheinlichkeit/laplace`).
  - `src/data/bruchaufgaben.yaml` – Bruchaufgaben (Zahlen a, b, c, d, Ergebnis und drei typische Fehler als gekürzter
    Text, Lösungsschritte) für `brueche/plus-minus` und `brueche/mal-geteilt`.
  - `src/data/figuren.yaml` – Großbuchstaben mit Achsen und Punktsymmetrie (ohne O, X, K, Ziffern: schriftabhängig).
  - `src/data/kongruenzsaetze.yaml` – gegebene Stücke → Kongruenzsatz, eindeutig ja/nein (sSW mit zwei Dreiecken
    nachgeprüft).
  - `src/data/urnen.yaml` – Urnen bis 10 Kugeln für `w4-zufall` (Brüche mit Python geprüft).
- Brüche aus Datensätzen werden als Text gespeichert und als Auswahl gezeigt; LaTeX in einem Datenfeld erscheint roh –
  den Bruch im Aufgabentext aus den Zahlen bauen.
- Keine Komponenten: Brüche und Terme werden ausgewählt, nicht getippt (die Eingabe kennt nur Zahlen).
- **Antwortpositionen:** Die Laufzeit mischt die Optionen nicht. In `single-choice`/`multiple-choice` steht die
  richtige Option an wechselnden Stellen (natürliche Reihenfolgen wie „Strecke 1, 2, 3“ oder aufsteigende Zahlen
  bleiben). In `generated` mit `choice` wird `r: { int: [0, N-1] }` gezogen und die Liste rotiert:
  `choice: "[[e.p, e.f1, e.f2, e.f3], [e.f1, e.p, e.f2, e.f3], [e.f1, e.f2, e.p, e.f3], [e.f1, e.f2, e.f3, e.p]][r]"`.
- Jede Seite hat mindestens eine Aufgabe auf Wettbewerbsniveau (Id oft `<seite>-wettbewerb`).

## Figures

- Eigene SVGs in `src/images/<kapitel>-<name>.svg`, von Hand geschrieben, Lizenz CC BY 4.0 wie der Inhalt.
- Farben überall gleich: gegeben blau `#2563eb`, gesucht orange `#ea580c`, Hilfslinie/Höhe gestrichelt; Text in
  `currentColor`-freundlichen Kontrasten, weißer Hintergrund mit Rand, damit Dark Mode lesbar bleibt.
- Dreiecke mit der Grundseite unten; Bäume von oben nach unten, an jedem Ast die Wahrscheinlichkeit; Koordinatensysteme
  mit Achsenbeschriftung und Einheit.
- Breite höchstens 360 px; `alt` sagt, was zu sehen ist; Bildunterschrift sagt, worauf man achtet; nie die Lösung im
  Bild. Für Prozent zusätzlich `figure` `hundred-grid`.

## Sources

- Zweitquellen je Seite (geöffnet, Fakten übernommen, keine Sätze): serlo.org (CC BY-SA 4.0) und Wikipedia; die
  vollständige Liste steht in `.vibe/plans/01-meine-lernapp.md`, „Quellen“. Jede Seite verlinkt ihre Quelle in
  `links` der Aufgaben.
- Typische Fehler: IQB VERA-8 Didaktische Kommentierungen „20 Prozent“ und „Apfelsaftschorle“; TEDS-IME Fortbildung
  Uni Hamburg (Terme); „The Equiprobability Bias …“ (PMC4310748); serlo „Konstruierbare Dreiecke“, „Ungleichungen
  lösen“, „Lösungsmenge einer Gleichung“.
- Alte Wettbewerbsaufgaben (Archiv mathematik-wettbewerb.de) nur als Orientierung; keine Lizenz, nichts kopiert.
- Die Checkliste der Erstellerin/des Erstellers bleibt lokal und wird nie committet.

## Adding a chapter or round

1. Kompetenzen als „Ich kann …“ unter „Competencies“ ergänzen.
2. Ordner `src/<kapitel>/` mit `chapter.yaml` (Titel, `summary`, `pages`, `selfAssessment`), Kapitel in
   `src/app.yaml` unter `chapters` eintragen.
3. Je Kompetenz eine Seite nach „Content structure“, Aufgaben nach „Exercise patterns“, Abbildungen nach „Figures“.
4. `npx vp build`, `npx --no -- lernapps screenshots`, Bilder ansehen; `npx --no -- lernapps check`.
5. Diese Datei aktualisieren und mit dem Inhalt committen.

## Rules learned from mistakes

- Optionen nicht immer richtig zuerst – die Laufzeit mischt nicht (46 von 57 Fragen hatten die Lösung oben).
- Jeden Fachbegriff beim ersten Auftreten erklären („stumpf“, „Umfang“) – Lernenden-Test der Musterseite.
- Keine Aufgabe, deren Bild die Lösung zeigt (Höhe in einem Dreieck mit waagerechter Seite war „senkrecht nach unten“
  ablesbar) – schräge Lage wählen.
- Kein Tipp, der verrät, welche Angabe man ignorieren soll; keine kindlichen Tipps („Fahre mit dem Finger …“).
- Lange Formeln auf mehrere `formula`-Blöcke verteilen (bei 360 px sonst `accessible`-Fehler).
- Kein geschütztes Leerzeichen in Überschriften (bricht einen e2e-Test).
- `generated` hat kein `links`-Feld; Texte mit „: “ in Anführungszeichen.
