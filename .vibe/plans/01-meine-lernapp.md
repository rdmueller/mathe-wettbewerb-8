---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: { accessible: 5, checks-pass: 2 }
---

# Plan: meine-lernapp, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-23. Explore, Plan, Code, Commit.*

## Goal

<!-- 1–2 sentences: what learners do, what they learn. -->

Achtklässlerinnen und Achtklässler am Gymnasium in Hessen bereiten sich auf die 1. Runde des Mathematik-Wettbewerbs
vor: Sie schätzen pro Thema ein, wie fit sie sind, wiederholen die Regel kurz und rechnen viele Aufgaben ohne
Taschenrechner – alle 8 Pflichtthemen und die 4 Wahlaufgaben W1–W4.

## Key decisions

<!-- One line each: decision and reason. Archetype first. Your own choice without the creator: mark "(guess)". -->

- Archetyp `explainer`: Kapitel pro Thema der Checkliste, kurze Wiederholung plus viele Aufgaben mit neuen Zahlen und
  typischen Fehlern, Selbsteinschätzung pro Kapitel passt zur Checkliste. `quiz` scheidet aus (keine neuen Zahlen,
  keine Erklärseiten), `interactive` auch (kein Spiel, kein Trainer mit Timer nötig).
- App zum Teilen mit `@lernapps/tooling`, nicht `@lernapps/practice`: der Wettbewerb betrifft alle 8. Klassen in Hessen. (guess)
- Kein `scope`: keine `open-task`, und die App folgt nicht dem Material der Erstellerin/des Erstellers, sondern nur seiner
  Themenliste; dafür `tutor.rules` in `src/app.yaml`: ohne Taschenrechner rechnen, Wettbewerbsniveau Klasse 8. (guess)

## Notes

<!-- Strand or subject, competencies by chapter (ids), didactic approach, scope, sources and licences, open questions. -->

**Lernlandkarte Mathematik** (https://lernapps.net/apps/map/mathematik.json, Lehrplan he-gymnasium). Die Checkliste
der Erstellerin/des Erstellers deckt diese Kompetenzen ab (Richtstufe 7-8, dazu Wiederholung aus 5-6):

1. Zuordnungen: `zuordnungen`, `proportionale-zuordnungen`, `antiproportionale-zuordnungen`, `koordinatensystem` (5-6)
2. Prozentrechnung: `prozent-grundbegriffe` (5-6), `prozent-prozentwert`, `prozent-prozentsatz`, `prozent-grundwert`
   – schon geübt in der App `mathe-arithmetik`
3. Fläche, Umfang, Volumen: `flaeche-umfang-quadrat-rechteck` (5-6), `flaeche-umfang-dreieck-viereck`,
   `volumen-oberflaeche-quader-wuerfel` (5-6), `formeln-umstellen`
4. Terme: `terme-variable`, `terme-umformen`, `rationale-zahlen-rechnen`
5. Wahrscheinlichkeit: `zufallserscheinungen` (Ergebnisraum), `zufall-laplace`, `zufall-baumdiagramm`,
   `zufall-pfadregel-1`, `zufall-pfadregel-2` – schon geübt in der App `mathe-stochastik`
6. Symmetrie und Abbildungen: `symmetrie` (5-6), `bewegungen-figuren` (5-6)
7. Winkel an Geradenkreuzungen: `winkelsaetze`
8. Bruchrechnung: `brueche-addieren-subtrahieren`, `brueche-multiplizieren-dividieren`, `dezimalbrueche-rechnen`,
   `grundrechenarten-rechengesetze` (alle 5-6)
9. W2 Dreieckskonstruktionen: `dreieckskonstruktion`, `kongruenz`, `linien-im-dreieck` (Höhe, Winkelhalbierende),
   `winkelsaetze`
10. W1 Terme und Gleichungen: `klammern-binome` (nur Klammern auflösen), `terme-umformen`, `lineare-gleichungen`,
    `ungleichungen`

Nicht auf der Karte: Satz vom Nullprodukt, Lösungsmenge mit Grundmenge ℤ (W1), Konstruktion mit Seitenhalbierender
(W2). Das wird später als Vorschlag an `lernapps/apps` gemeldet.

**So üben die Lernenden** (Skill `lernapps-exercise-patterns`, Mathematik):

- Rechnen (Prozent, Fläche/Volumen, Terme, Brüche, Gleichungen, Laplace, Pfadregeln, Winkel): `generated`-Aufgaben,
  jedes Mal neue Zahlen, typische Fehler mit eigener Rückmeldung (z. B. Formel falsch umgestellt, Vorzeichen,
  Ungleichungszeichen nicht gedreht).
- Erkennen und Zuordnen (proportional/antiproportional, Graph Gerade/Hyperbel, Symmetrie, Winkelarten,
  Kongruenzsatz SSS/SWS/WSW/SsW): `single-choice`, `matching`, `true-false` mit Begründung (z. B. ob „je mehr, desto
  mehr“ schon proportional bedeutet).
- Ablesen (Koordinatensystem, Tabelle, Baumdiagramm): Abbildung als SVG, gefragt ist ein Wert.
- Vorgehen (Lösungsweg „gegeben/gesucht, Formel, Rechnung, Antwort“, Konstruktionsschritte): `ordering`.
- Konstruieren mit Zirkel und Geodreieck geht nur im Heft: die App übt Planfigur, Strategie, Kongruenzsatz und
  fehlende Winkel; Konstruieren selbst nicht.
- Die Checkliste selbst wird zur Selbsteinschätzung pro Kapitel („Bin ich fit?“).

### Recherche

**Strang: keiner (`strand: none`).** Mathematik hat `explainerFocus: strand`; die Themen des Wettbewerbs reichen über
fünf Stränge (Arithmetik, Größen und Messen, Algebra, Geometrie, Stochastik). Die App steht deshalb nicht auf der
Lernlandkarte, wird aber gelistet. Antwort „B“ der Erstellerin/des Erstellers.

**Der Wettbewerb** (https://mathematik-wettbewerb.de/pages/index.xml, „Mathematik-Wettbewerb des Landes Hessen“,
verified; Informationen zur 1. Runde 2026/2027:
https://mathematik-wettbewerb.de/pages/downloads/mw_1r_informationen.pdf, verified):

- Pflicht für alle 8. Klassen in Hessen, als Klassenarbeit; Gruppe A = Gymnasium.
- 8 Pflichtaufgaben je 3 BE, dazu 2 von 4 Wahlaufgaben je 12 BE, zusammen 48 BE.
- **Kein Taschenrechner, keine Formelsammlung.** Daher: Aufgaben der App mit Zahlen, die im Kopf oder schriftlich
  gehen; Formeln muss man auswendig können.
- Wahlaufgaben der letzten Jahre: W1 Gleichungen/Ungleichungen mit G = ℤ, W2 Dreieckskonstruktionen, W3 Prozent-
  Sachaufgaben mit mehreren Schritten, W4 zweistufige Zufallsversuche. Die Checkliste nennt nur W1 und W2.
- Aufgaben der Runde 1 mit Lösungen: Archiv https://mathematik-wettbewerb.de/pages/aufgloes.xml (verified), z. B.
  2023/24, 2024/25, 2025/26. Keine Lizenz angegeben: nur als Orientierung für Art und Schwierigkeit, nichts kopieren.

**Lehrplan:** „Bildungsstandards und Inhaltsfelder – Das neue Kerncurriculum für Hessen, Sekundarstufe I –
Gymnasium, Mathematik“, Hessisches Kultusministerium, 2011,
https://kultus.hessen.de/sites/kultus.hessen.de/files/2021-07/kerncurriculum_mathematik_gymnasium.pdf (verified),
Kap. 7.2 (S. 24) und Übersicht Jahrgangsstufe 7/8 (S. 26–29). Die Reihenfolge der Kapitel folgt der Checkliste.

### Kompetenzen nach Kapiteln (eine Seite je Kompetenz)

In Klammern die ähnlichste Kompetenz der Lernlandkarte, nur zur Orientierung.

**Start:** So gehst du an eine Aufgabe heran (Aufgabe ganz lesen, Thema bestimmen, Plan, dann rechnen) – Startseite,
keine eigene Kompetenz.

1. Zuordnungen
   1. Ich kann Zuordnungen in Tabellen darstellen und Punkte im Koordinatensystem eintragen und ablesen.
      (`zuordnungen`, `koordinatensystem`)
   2. Ich kann proportionale Zuordnungen erkennen und Tabellen mit dem Faktor ergänzen. (`proportionale-zuordnungen`)
   3. Ich kann antiproportionale Zuordnungen erkennen und von proportionalen unterscheiden.
      (`antiproportionale-zuordnungen`)
   4. Ich kann am Graphen erkennen, ob eine Zuordnung proportional (Gerade durch den Ursprung) oder antiproportional
      (Hyperbel) ist.
2. Prozentrechnung
   1. Ich kann den Prozentwert mit G · p % = P berechnen. (`prozent-prozentwert`)
   2. Ich kann die Formel umstellen und den Prozentsatz oder den Grundwert berechnen. (`prozent-prozentsatz`,
      `prozent-grundwert`)
   3. Ich kann Sachaufgaben zur Prozentrechnung mit gegeben/gesucht, Formel, Rechnung und Antwort lösen.
      (`prozent-sachaufgaben`)
3. Flächeninhalt, Umfang und Volumen
   1. Ich kann Flächeninhalt und Umfang von Quadrat und Rechteck berechnen. (`flaeche-umfang-quadrat-rechteck`)
   2. Ich kann Flächeninhalt und Umfang von Dreiecken berechnen und zu jeder Seite die Höhe einzeichnen, auch außen.
      (`flaeche-umfang-dreieck-viereck`)
   3. Ich kann Flächeninhalt und Umfang von Parallelogramm und Trapez berechnen. (`flaeche-umfang-dreieck-viereck`)
   4. Ich kann das Volumen von Quader und Würfel berechnen. (`volumen-oberflaeche-quader-wuerfel`)
   5. Ich kann Netze von Quader und Würfel erkennen und ihre Oberfläche berechnen. (`netze-schraegbilder-modelle`,
      `volumen-oberflaeche-quader-wuerfel`)
   6. Ich kann eine Flächen- oder Volumenformel nach einer Größe umstellen, z. B. nach der Höhe. (`formeln-umstellen`)
4. Terme
   1. Ich kann zu einem Text oder einer Rechenvorschrift einen Term aufstellen. (`terme-variable`)
   2. Ich kann den Wert eines Terms berechnen, wenn ich eine Zahl für x einsetze. (`terme-variable`)
   3. Ich kann gleichartige Glieder zusammenfassen. (`terme-umformen`)
   4. Ich kann Produkte wie 3x · (−2y) berechnen und dabei zuerst das Vorzeichen bestimmen.
      (`rationale-zahlen-rechnen`, `terme-umformen`)
5. Wahrscheinlichkeit
   1. Ich kann den Ergebnisraum aufschreiben und die Laplace-Wahrscheinlichkeit als „günstige : alle“ berechnen.
      (`zufallserscheinungen`, `zufall-laplace`)
   2. Ich kann ein Baumdiagramm mit allen Wahrscheinlichkeiten zeichnen. (`zufall-baumdiagramm`)
   3. Ich kann mit den Pfadregeln (multiplizieren entlang eines Pfades, addieren über Pfade) Wahrscheinlichkeiten
      berechnen. (`zufall-pfadregel-1`, `zufall-pfadregel-2`)
6. Symmetrie und Abbildungen
   1. Ich kann Achsen- und Punktsymmetrie erkennen und Symmetrieachsen finden. (`symmetrie`)
   2. Ich kann Figuren an einer Achse spiegeln und um einen Punkt drehen. (`bewegungen-figuren`)
7. Winkel
   1. Ich kann fehlende Winkel mit der Winkelsumme im Dreieck (180°) und im Viereck (360°) berechnen. (`winkelsaetze`)
   2. Ich kann Neben-, Scheitel-, Stufen- und Wechselwinkel an Geradenkreuzungen berechnen. (`winkelsaetze`)
8. Bruchrechnung
   1. Ich kann Brüche und Dezimalbrüche addieren und subtrahieren. (`brueche-addieren-subtrahieren`,
      `dezimalbrueche-rechnen`)
   2. Ich kann Brüche und Dezimalbrüche multiplizieren und dividieren. (`brueche-multiplizieren-dividieren`,
      `dezimalbrueche-rechnen`)
   3. Ich kann Klammern und Punkt vor Strich beachten, wenn ich mit Brüchen rechne. (`grundrechenarten-rechengesetze`)
9. Wahlaufgabe W2: Dreieckskonstruktionen
   1. Ich kann eine Planfigur zeichnen und Ecken, Seiten und Winkel richtig bezeichnen (A → B → C gegen den
      Uhrzeigersinn, a gegenüber von A, α bei A).
   2. Ich kann an den gegebenen Stücken erkennen, welcher Kongruenzsatz passt (SSS, SWS, WSW, SsW) und ob das Dreieck
      eindeutig ist. (`kongruenz`)
   3. Ich kann die Schritte einer Konstruktion in die richtige Reihenfolge bringen, auch mit Höhe, Seitenhalbierender
      oder Winkelhalbierender. (`dreieckskonstruktion`, `linien-im-dreieck`)
   4. Ich kann einen fehlenden Winkel berechnen und eine fertige Konstruktion durch Nachmessen prüfen.
      (`winkelsaetze`)
10. Wahlaufgabe W1: Terme und Gleichungen
    1. Ich kann Klammern auflösen, auch Minusklammern, und zwei Klammern ausmultiplizieren. (`klammern-binome`)
    2. Ich kann eine Gleichung lösen: zusammenfassen, sortieren, durch den Faktor vor x teilen – auch wenn x² auf
       beiden Seiten wegfällt oder Dezimalzahlen vorkommen. (`lineare-gleichungen`)
    3. Ich kann eine Ungleichung lösen und das Zeichen drehen, wenn ich mit einer negativen Zahl multipliziere oder
       durch sie teile. (`ungleichungen`)
    4. Ich kann eine Gleichung wie (5x + 5) · (x − 5) = 0 mit dem Satz vom Nullprodukt lösen. (nicht auf der Karte)
    5. Ich kann die Lösungsmenge aufzählend angeben, die Grundmenge ℤ beachten und die Probe machen. (nicht auf der
       Karte)

11. Wahlaufgabe W3: Prozent-Sachaufgaben mit mehreren Schritten
    1. Ich kann den neuen Wert nach einer prozentualen Zunahme oder Abnahme mit dem Faktor berechnen (vermehrter und
       verminderter Grundwert). (`prozent-veraenderung`)
    2. Ich kann angeben, um wie viel Prozent ein Wert größer oder kleiner ist als ein anderer. (`prozent-vergleich`)
    3. Ich kann mehrere prozentuale Änderungen nacheinander berechnen und Prozente von Prozentpunkten unterscheiden.
       (`prozent-von-prozenten`)
12. Wahlaufgabe W4: Zweistufige Zufallsversuche
    1. Ich kann beim Ziehen mit und ohne Zurücklegen die Wahrscheinlichkeiten der zweiten Stufe anpassen.
       (`zufall-ohne-zuruecklegen`)
    2. Ich kann Ereignisse wie „genau einmal“ oder „mindestens einmal“ den passenden Pfaden zuordnen.
       (`zufall-ereignis-uebersetzen`)
    3. Ich kann eine Wahrscheinlichkeit über das Gegenereignis mit 1 − P(E) berechnen. (`zufall-gegenereignis`)

Zusammen: 12 Kapitel, 42 Seiten, dazu Startseite und Selbsteinschätzung.

### Seiten und Kapitel

Kapitel = Ordner, Seite = eine Kompetenz von oben, in dieser Reihenfolge (wie die Checkliste). Ohne Strang tragen die
Seiten keine Karten-Ids; die Ordnung folgt der Checkliste und dem Aufbau innerhalb jedes Kapitels.

| Kapitel (Ordner) | Seiten | Voraussetzungen, die die App nicht übt |
|---|---|---|
| `zuordnungen` | `tabelle-koordinaten`, `proportional`, `antiproportional`, `graphen` | Multiplizieren und Dividieren im Kopf |
| `prozent` | `prozentwert`, `prozentsatz-grundwert`, `sachaufgaben` | Prozent als Hundertstel (`prozent-grundbegriffe`): kurz auf `prozentwert` wiederholt; Brüche kürzen: Link zu Kapitel `brueche` |
| `flaechen` | `quadrat-rechteck`, `dreieck`, `parallelogramm-trapez`, `quader-wuerfel`, `netz-oberflaeche`, `formeln-umstellen` | Einheiten von Länge, Fläche, Volumen umrechnen (`einheiten-flaeche-volumen`): Wiederholungsseite „Das brauchst du hier“ am Kapitelanfang |
| `terme` | `aufstellen`, `werte-berechnen`, `zusammenfassen`, `produkte` | Rechnen mit negativen Zahlen (`rationale-zahlen-rechnen`): auf `produkte` geübt; vorher nur Plus-Zahlen |
| `wahrscheinlichkeit` | `laplace`, `baumdiagramm`, `pfadregeln` | Brüche multiplizieren und addieren: Link zu Kapitel `brueche` |
| `symmetrie` | `symmetrie-erkennen`, `spiegeln-drehen` | Geodreieck: senkrecht und Abstand (`parallel-senkrecht-abstand`): im Text erinnert |
| `winkel` | `winkelsumme`, `geradenkreuzungen` | Winkel messen (`winkel-messen`), parallele Geraden: im Text erinnert |
| `brueche` | `plus-minus`, `mal-geteilt`, `rechenregeln` | Bruch kürzen und erweitern (`brueche-kuerzen-erweitern`): Wiederholungsseite am Kapitelanfang |
| `w2-konstruktionen` | `planfigur`, `kongruenzsaetze`, `konstruktion-schritte`, `winkel-pruefen` | Grundkonstruktionen mit Zirkel (Mittelsenkrechte, Winkelhalbierende, Parallele): Wiederholungsseite am Kapitelanfang |
| `w1-gleichungen` | `klammern`, `gleichungen`, `ungleichungen`, `nullprodukt`, `loesungsmenge` | ganze Zahlen ℤ, Terme zusammenfassen: Link zu Kapitel `terme` |
| `w3-prozent` | `zu-abnahme`, `vergleich`, `mehrere-aenderungen` | baut auf Kapitel `prozent` auf: Link |
| `w4-zufall` | `ohne-zuruecklegen`, `ereignisse-pfade`, `gegenereignis` | baut auf Kapitel `wahrscheinlichkeit` auf: Link |

Brüche (Kapitel 8) kommen erst nach Prozent und Wahrscheinlichkeit, weil die Checkliste es so ordnet; die Seiten dort
verlinken auf das Kapitel `brueche`. (guess)

### Didaktik: Weg zur Kompetenz und Fehler, die die Rückmeldung erkennt

„(Quelle)“ = Fehler aus einer geöffneten Quelle, sonst aus Erfahrung (guess).

- 1.1 Tabelle aus einer Sachsituation selbst füllen, dann Punkte eintragen. Fehler: x- und y-Wert vertauscht.
- 1.2 Faktor aus zwei Wertepaaren selbst finden (x · 2 → y · 2). Fehler: „je mehr, desto mehr“ für proportional
  gehalten; Differenz statt Faktor fortgesetzt.
- 1.3 Produkt x · y in der Tabelle ausrechnen und entdecken, dass es gleich bleibt. Fehler: „je mehr, desto weniger“
  für antiproportional gehalten; proportional gerechnet (Dreisatz falsch herum).
- 1.4 Punkte einer Tabelle selbst einzeichnen, Form benennen. Fehler: jede Gerade für proportional gehalten, auch
  ohne Ursprung.
- 2.1 Am Hunderterfeld 1 % ablesen, dann G · p % = P. Fehler: p statt p % gerechnet (mal 20 statt mal 0,2);
  Grundwert und Prozentwert vertauscht (Quelle: IQB „20 Prozent“).
- 2.2 Die Formel selbst umstellen, eine Umformung pro Schritt. Fehler: P : G vergessen mal 100; geteilt statt mal.
- 2.3 Lösungsschritte ordnen, dann rechnen. Fehler: falscher Grundwert bei „teurer als“; Prozent vom neuen statt
  vom alten Preis; einfach subtrahiert (Quelle: IQB).
- 3.1 Fläche durch Kästchen zählen, dann a · b. Fehler: Umfang und Fläche verwechselt; Einheit cm statt cm².
- 3.2 Dreieck als halbes Rechteck bzw. Parallelogramm herleiten; zu jeder Seite die Höhe wählen. Fehler: schräge
  Seite statt Höhe; durch 2 vergessen; Höhe außen nicht erkannt.
- 3.3 Parallelogramm zum Rechteck umlegen, Trapez aus zwei Dreiecken. Fehler: Schrägseite statt Höhe; beim Trapez
  nicht (a + c) : 2.
- 3.4 Würfelchen schichten: Grundfläche · Höhe. Fehler: Oberfläche statt Volumen; Einheit cm² statt cm³.
- 3.5 Netz aus dem Quader „aufklappen“, gleiche Flächen paarweise färben, dann O = 2ab + 2ac + 2bc. Fehler: nur 3
  statt 6 Flächen gezählt; Netz mit überlappenden Flächen für richtig gehalten.
- 3.6 Formel wie eine Gleichung umstellen. Fehler: falsche Umkehroperation (mal statt geteilt), beim Dreieck das
  „: 2“ vergessen.
- 4.1 Rechenvorschrift Schritt für Schritt in Zeichen übersetzen. Fehler: Klammer vergessen („das Doppelte der Summe“).
- 4.2 Wertetabelle durch Einsetzen füllen. Fehler: 3x mit x = 4 als 34 gelesen; Punkt vor Strich missachtet.
- 4.3 Gleichartige Glieder sortieren, dann zusammenfassen. Fehler: 4n + 6n + 3 = 13n; 3ab + 5ab = 8a²b²
  (Quelle: TEDS-IME).
- 4.4 Erst Vorzeichen, dann Zahlen, dann Variablen. Fehler: minus mal minus = minus; Zahlen addiert statt
  multipliziert.
- 5.1 Ergebnisraum selbst aufzählen, günstige markieren. Fehler: Augensummen zweier Würfel als gleich wahrscheinlich
  angenommen (Quelle: Equiprobability Bias).
- 5.2 Baum aus dem Zufallsversuch aufbauen; Äste an einem Knoten ergeben 1. Fehler: ohne Zurücklegen die
  Wahrscheinlichkeiten nicht angepasst; Äste ergeben nicht 1.
- 5.3 Pfad im Baum verfolgen. Fehler: entlang des Pfades addiert statt multipliziert; Pfade multipliziert statt
  addiert.
- 6.1 Figur gedanklich falten bzw. um 180° drehen. Fehler: Punkt- mit Achsensymmetrie verwechselt (Quelle: serlo);
  nur senkrechte Achse gesucht.
- 6.2 Punkt für Punkt spiegeln (senkrecht, gleicher Abstand). Fehler: Abstand nicht senkrecht gemessen; falsche
  Drehrichtung.
- 7.1 Aus drei Winkeln eines zerschnittenen Dreiecks 180° legen. Fehler: 360° beim Dreieck; Viereck mit 180°.
- 7.2 Winkelpaare an der Kreuzung selbst färben, Gleichheit begründen. Fehler: Stufenwinkel ohne parallele Geraden
  genutzt (Quelle: serlo); Neben- mit Scheitelwinkel verwechselt.
- 8.1 Hauptnenner selbst bilden. Fehler: Zähler plus Zähler, Nenner plus Nenner (Quelle: IQB „Apfelsaftschorle“).
- 8.2 Mal: Zähler mal Zähler; geteilt: mit dem Kehrwert. Fehler: beim Teilen den falschen Bruch umgedreht; Komma
  falsch gesetzt.
- 8.3 Rechenreihenfolge markieren, dann rechnen. Fehler: von links nach rechts statt Punkt vor Strich.
- 9.1 Planfigur aus den gegebenen Stücken skizzieren und beschriften. Fehler: im Uhrzeigersinn beschriftet; a an A
  statt gegenüber.
- 9.2 Stücke markieren und mit den Sätzen vergleichen. Fehler: SsW mit sSW verwechselt; WWW für eindeutig gehalten
  (Quelle: serlo „Konstruierbare Dreiecke“).
- 9.3 Schritte einer Konstruktion ordnen und begründen. Fehler: Höhe, Seitenhalbierende und Winkelhalbierende
  verwechselt.
- 9.4 Fehlenden Winkel mit 180° berechnen, mit dem gemessenen vergleichen. Fehler: 360° statt 180°.
- 10.1 Jedes Glied mit jedem multiplizieren (Rechteckmodell). Fehler: Minusklammer nur beim ersten Glied
  aufgelöst; nur die ersten und letzten Glieder multipliziert.
- 10.2 Gleichung als Waage: auf beiden Seiten dasselbe tun. Fehler: x² nicht auf beiden Seiten gestrichen; beim
  Sortieren Vorzeichen vergessen.
- 10.3 Mit einem Zahlenbeispiel sehen, warum sich das Zeichen dreht. Fehler: Zeichen nicht gedreht (Quelle: serlo).
- 10.4 Ein Produkt ist 0, wenn ein Faktor 0 ist: beide Faktoren gleich 0 setzen. Fehler: ausmultipliziert statt
  Nullprodukt; nur eine Lösung angegeben.
- 11.1 Am Hunderterfeld sehen: +20 % heißt 120 % = Faktor 1,2. Fehler: nur die Änderung statt des neuen Werts
  angegeben; Prozentsatz addiert statt Betrag.
- 11.2 Unterschied durch den Vergleichswert teilen. Fehler: durch den falschen Wert geteilt (Grundwert
  verwechselt).
- 11.3 Zwei Faktoren hintereinander multiplizieren. Fehler: +20 % und −20 % heben sich auf; Prozentpunkte als
  Prozent gerechnet (Quelle: serlo „Aufgaben zu Prozent und Prozentpunkten“).
- 12.1 Urne vor und nach dem ersten Zug zeichnen. Fehler: beim zweiten Zug den alten Nenner behalten.
- 12.2 Alle Pfade aufschreiben, passende markieren. Fehler: bei „genau einmal“ nur einen der zwei Pfade gezählt.
- 12.3 Gegenereignis „keinmal“ finden, 1 − P rechnen. Fehler: Gegenereignis von „mindestens einmal“ als „höchstens
  einmal“ gewählt.
- 10.5 Lösung prüfen: liegt sie in ℤ? Probe einsetzen. Fehler: Lösung außerhalb von G angegeben, L = ∅ nicht erkannt
  (Quelle: serlo).

### Umfang

- **Drin:** alle Themen der Checkliste: Pflichtthemen 1–8, Wahlthemen W1 und W2; dazu auf Wunsch W3, W4 und Netz und
  Oberfläche des Quaders; Startseite mit dem Vorgehen „Für
  jede Aufgabe“; Selbsteinschätzung pro Kapitel und für die ganze App.
- **Draußen, mit Grund:**
  - Konstruieren mit Zirkel und Geodreieck: geht nur im Heft; die App übt Planfigur, Kongruenzsatz, Schritte, Prüfen.
  - Ein Probewettbewerb mit Zeit und Punkten: der Archetyp hat keinen Timer.
- **Zahlenbereich:** wie im Wettbewerb ohne Taschenrechner: ganze Zahlen meist von −20 bis 20, Längen 1–20 cm
  (ganzzahlig oder ,5), Prozentsätze in Schritten von 5 % (dazu 1 %, 12,5 %, 33⅓ % nur als Bruch), Brüche mit
  Nennern bis 12, Wahrscheinlichkeiten mit Würfeln, Münzen, Glücksrädern bis 8 Feldern, Urnen bis 10 Kugeln. Ergebnisse
  so gewählt, dass sie im Kopf oder schriftlich aufgehen.
- **Sprache:** nur Deutsch, einfache Sprache, „du“.
- **Keine Daten von Lernenden:** die Checkliste der Erstellerin/des Erstellers bleibt lokal, nur die abgeleiteten
  Kompetenzen kommen in die App.

### Quellen (alle selbst geöffnet; Fakten übernommen, keine Sätze)

serlo.org (CC BY-SA 4.0), Wikipedia (CC BY-SA 4.0), je „verified“:

- 1: https://de.serlo.org/mathe/1771/direkte-proportionalitaet „Direkte Proportionalität“;
  https://de.serlo.org/mathe/196516/direkte-und-indirekte-proportionalitaet „Direkte und indirekte
  Proportionalität“; https://de.wikipedia.org/wiki/Kartesisches_Koordinatensystem „Kartesisches Koordinatensystem“
- 2: https://de.serlo.org/mathe/36750/einfuehrung-in-grundwert-prozentwert-und-prozentsatz „Einführung in Grundwert,
  Prozentwert und Prozentsatz“
- 3: https://de.serlo.org/mathe/1697/rechteck „Rechteck“; https://de.serlo.org/mathe/36520/flaechenformeln-ebener-figuren
  „Flächenformeln ebener Figuren“; https://de.wikipedia.org/wiki/H%C3%B6he_%28Geometrie%29 „Höhe (Geometrie)“;
  https://de.serlo.org/mathe/131901/rauminhalt-von-wuerfel-und-quader „Rauminhalt von Würfel und Quader“;
  https://de.serlo.org/mathe/1847/aequivalenzumformungen „Äquivalenzumformungen“
- 4: https://de.serlo.org/mathe/117669/belegung-von-variablen „Belegung von Variablen“;
  https://de.serlo.org/mathe/135559/zusammenfassen-von-termen „Zusammenfassen von Termen“;
  https://de.serlo.org/mathe/62045/rechnen-mit-ganzen-zahlen „Rechnen mit ganzen Zahlen“; Terme aufstellen: keine
  passende Quelle gefunden
- 5: https://de.serlo.org/mathe/1755/laplace-experiment „Laplace-Experiment“; https://de.serlo.org/mathe/1501/ergebnismenge
  „Ergebnismenge“; https://de.serlo.org/mathe/156048/mehrstufige-zufallsexperimente „Mehrstufige Zufallsexperimente“;
  https://de.serlo.org/mathe/189811/pfadregeln „Pfadregeln“
- 6: https://de.serlo.org/mathe/35620/achsensymmetrie; https://de.serlo.org/mathe/35721/punktsymmetrie;
  https://de.serlo.org/mathe/1925/kongruenz „Kongruenz“
- 7: https://de.serlo.org/mathe/1707/winkel „Winkel“; Winkelsumme: unchecked
- 8: https://de.serlo.org/mathe/50493/rechnen-mit-bruechen-ueberblick „Rechnen mit Brüchen – Überblick“;
  https://de.serlo.org/mathe/19482/dezimalbrueche; https://de.serlo.org/mathe/111923/umgang-mit-klammern „Umgang mit
  Klammern“
- 9: https://de.serlo.org/mathe/1957/dreiecke-konstruieren; https://de.serlo.org/mathe/78680/konstruierbare-dreiecke
  „Konstruierbare Dreiecke“; https://de.serlo.org/mathe/1913/seitenhalbierende;
  https://de.wikipedia.org/wiki/Winkelhalbierende
- 10: https://de.serlo.org/mathe/1677/distributivgesetz; https://de.serlo.org/mathe/1995/ungleichungen-loesen;
  https://de.serlo.org/mathe/221122/loesung-von-quadratischen-gleichungen (Abschnitt „Satz vom Nullprodukt“);
  https://de.serlo.org/mathe/154971/loesungsmenge-einer-gleichung; https://de.wikipedia.org/wiki/Lineare_Gleichung
- 3 (Netz, Oberfläche): https://de.serlo.org/mathe/1699/quader „Quader“; https://de.serlo.org/mathe/35621/koerpernetze
  „Körpernetze“
- 11: https://de.serlo.org/mathe/37829/zusammenfassung „Einführung in den verminderten und vermehrten Grundwert“;
  https://de.serlo.org/mathe/174192/aufgaben-zu-prozent-und-prozentpunkten „Aufgaben zu Prozent und Prozentpunkten“
- 12: https://de.serlo.org/mathe/156048/mehrstufige-zufallsexperimente „Mehrstufige Zufallsexperimente“;
  https://de.serlo.org/mathe/25615/aufgaben-zum-thema-ereignisse „Aufgaben zum Thema Ereignisse“ (Aufgabenseite);
  Gegenereignis: keine eigene Erklärseite gefunden, unchecked
- Typische Fehler: IQB, VERA-8 Didaktische Kommentierung „20 Prozent“ und „Apfelsaftschorle“ (verified); TEDS-IME
  Fortbildung, Uni Hamburg, Sitzung 4 (Terme, verified); „The Equiprobability Bias …“, PMC4310748 (verified).
- Nicht erreichbar: schule-bw.de (abgeschaltet), HU Berlin Didaktik (HTTP 410).

## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [x] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [x] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [x] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [x] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [x] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [x] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [x] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [x] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [x] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [x] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [x] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [x] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [x] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [x] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.
      Creator: gleich mit rein (W3, W4, Netz/Oberfläche); dann: ja

### Answers

<!-- The interview: per topic the creator's answer, in their words. Keep the topics. -->

- Goal: what learners do in the app, what they learn.
  - Creator: „es geht um die Vorbereitung zum Mathewettbewerb […] Anbei die Checkliste der Themen“ (Checkliste „Bin ich fit für den Mathe-Wettbewerb?“, Klasse 8, Runde 1: Pflichtthemen 1–8, Wahlthemen W1 Terme und Gleichungen, W2 Dreieckskonstruktionen).
- Learners: subject, school year, prior knowledge.
  - Creator: „Mathewettbewerb, Gymnasium, Stufe 8, Hessen“.
- Model and focus: an app of the catalog (https://lernapps.net/apps/llms.txt) as model; what matters most (exercises,
  visualisations, game feel).
  - Creator: „alles drei“ (Übungsaufgaben, Erklärungen mit Bildern, Selbsteinschätzung). Kein Vorbild genannt.
- Hurdles: misconceptions and mistakes of the learners; the creator's examples and experiments.
  - Creator: „keine ahnung“. Typische Fehler leite ich aus der Checkliste (z. B. „je mehr, desto mehr“ mit proportional verwechselt, Höhen außerhalb, Vorzeichen, x² fällt weg, Ungleichungszeichen drehen) und aus der Recherche ab. (guess)
- Content: who writes it (creator, you, from sources); own material (worksheets, tests).
  - Creator: „ich habe nichts“ (auf meine Frage: selbst schreiben nach Checkliste und alten Wettbewerbsaufgaben?). Ich schreibe die Inhalte nach Checkliste und Quellen.
- Amount: how much content in the first version; what comes later.
  - Creator: „B“ = gleich alles: Pflichtthemen 1–8, W1 und W2, eine App ohne festen Strang der Lernlandkarte (`strand: none`), mit Selbsteinschätzung.
  - Nach der Recherche, auf meine Frage nach W3, W4 und Netz/Oberfläche: „gleich mit rein“.
- Languages: German only, or German and English. Never English only.
  - Creator: „deutsch“.
- Look and feel: calm like a worksheet, or like a game (colours, praise, effects); dark mode.
  - fixed by the archetype (explainer: Aussehen der Laufzeit, ruhig wie ein Arbeitsblatt, Dark Mode nach Gerät).
- Terms: the creator's words for the main things in the app, used everywhere.
  - Abgedeckt durch die Checkliste (Goal): ihre Wörter gelten, z. B. Zuordnung, Grundwert/Prozentwert/Prozentsatz, Planfigur, Pfadregeln, Ergebnisraum, Lösungsmenge.
- Finding the app: what teachers and parents would search for.
  - Creator: „ja“ (auf meinen Vorschlag „Mathewettbewerb Hessen Klasse 8 üben“).

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [x] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [x] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [x] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [x] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [x] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [x] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [x] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.
      Creator: ja

### Content method

<!-- One line each: the patterns and where; the figures and how they are made; the data files; each component, what it
checks and what it cannot; how a later agent adds a chapter. It becomes the content guide in Code. -->
<!-- An explainer: per figure, model and component its learning action in two to four sentences
(`explainer-representation-explained`); per page its prerequisites the app does not practise, and which get a recap
page, which a link. -->

**Inhalte auf den Archetyp abgebildet** (Skill `lernapps-explainer-design`, „Map the content“)

- `strand: none` (Mathematik ist `explainerFocus: strand`, die App reicht über fünf Stränge). Seiten tragen keine
  `competencies`; die Kompetenz steht als „Ich kann …“ im Seitenziel. Keine `recap`-Seiten mit Karten-Ids (nur mit
  Strang erlaubt); stattdessen ein Abschnitt „Das brauchst du hier“ am Anfang der ersten Seite eines Kapitels. (guess)
- 12 Kapitel = Ordner, 42 Seiten = je eine Kompetenz, Reihenfolge wie unter „Seiten und Kapitel“.
- Abschnitte mit festen Ids auf allen Seiten: `start` (Einstiegsaufgabe), `regel` (Herleitung, Abbildung, Formel),
  `beispiel` (Box mit Rechenweg), `merke` (typischer Fehler, nur wo nötig), `uebung` (mindestens 4 Aufgaben, von
  leicht zu schwer). Titel passend zur Seite.
- Voraussetzungen, die die App nicht übt: im Abschnitt „Das brauchst du hier“ der ersten Kapitelseite, kurz und ohne
  Aufgabe (Einheiten bei `flaechen`, Kürzen/Erweitern bei `brueche`, Grundkonstruktionen bei `w2-konstruktionen`);
  sonst ein Link im Text auf das Kapitel der App (Brüche ← Prozent, Wahrscheinlichkeit; Terme ← W1; Prozent ← W3;
  Wahrscheinlichkeit ← W4).
- Startseite: Was der Wettbewerb ist (8 Pflicht-, 2 von 4 Wahlaufgaben, ohne Taschenrechner), Vorgehen „Aufgabe ganz
  lesen – Thema bestimmen – Plan – rechnen – Antwortsatz“, Link zur Selbsteinschätzung.
- Selbsteinschätzung in jedem Kapitel (`selfAssessment`), 2 Aufgaben je Seite, bevorzugt `generated`.
- Keine Geschichte: die Lernenden sind 13–14, die Seiten tragen sich durch Alltagssituationen in den Aufgaben
  (Preise, Spiele, Sport, Bastelarbeiten). (guess)
- Sprache: nur Deutsch, „du“. Daten in `src/data/`: `zufallsversuche.yaml` (Würfel, Münze, Glücksräder, Urnen mit
  Anzahl der Ergebnisse), `figuren.yaml` (Buchstaben und Zeichen mit Achsen- und Punktsymmetrie),
  `kongruenzsaetze.yaml` (gegebene Stücke → Satz, eindeutig ja/nein).

**Muster** (Skill `lernapps-exercise-patterns`, Mathematik)

| Muster | Für | Form | Beispiel |
|---|---|---|---|
| Rechenaufgabe mit Fehlerdiagnose | Prozent, Flächen, Volumen, Oberfläche, Termwert, Winkel, Laplace, Pfadregeln, W3 | `generated`, Zahlen ohne Taschenrechner lösbar, 2–3 `mistakes`, `hint`, `steps` | „Ein Dreieck hat g = {{g}} cm und h = {{h}} cm. Flächeninhalt?“ Fehler `g * h`: „Du hast vergessen, durch 2 zu teilen.“ |
| Bruch als Auswahl | Bruchrechnung, Wahrscheinlichkeiten als Bruch | `generated` mit `compare: { choice }`: richtiger Bruch und Brüche aus den typischen Fehlern; zusätzlich `number` als Dezimalbruch, wo er abbricht | 2/3 + 1/4 → Auswahl 11/12, 3/7, 3/12 |
| Term als Auswahl | Terme aufstellen, zusammenfassen, Produkte, Klammern | `single-choice` bzw. `generated` mit `choice`; Zahl vor x als `number` | 3x · (−2y) → −6xy, 6xy, x − 2y |
| Erkennen mit Begründung | proportional/antiproportional, Graph, Symmetrie, Winkelpaare, Kongruenzsatz | `true-false`, `single-choice`, `matching`; jede Option mit `info` | „Je mehr Zeit, desto mehr Wasser – ist das proportional?“ |
| Ablesen | Koordinatensystem, Tabelle, Baumdiagramm, Netz | `image` (SVG) als `material`, dann `number` oder `single-choice` | Punkt im KS ablesen: x-Wert? |
| Schritte ordnen | Lösungsweg Prozent, Gleichung lösen, Konstruktionsschritte | `ordering` | Konstruktion SWS: 4 Schritte ordnen |
| Lösung einer Gleichung | Gleichungen, Ungleichungen, Nullprodukt, Lösungsmenge | `generated` mit `number` (x = …); Ungleichung: Zahl und Zeichen als `choice` (x < 3, x > 3, …); Lösungsmenge: `multiple-choice` | (x+4)(x−3) = 0 → beide Lösungen per `multiple-choice` |

- Abbildungen: eigene SVGs in `src/images/` (Dreiecke mit Höhen innen und außen, Parallelogramm/Trapez umgelegt,
  Quader und Netze, Koordinatensysteme mit Ursprungsgerade und Hyperbel, Baumdiagramme von oben nach unten,
  Geradenkreuzungen mit farbigen Winkelpaaren, Planfiguren, Urnen vorher/nachher), `hundred-grid` für Prozent,
  `formula` für Formeln. Gleiche Farben in der ganzen App: gegeben blau, gesucht orange, Höhe gestrichelt.
- Je Abbildung: Bildunterschrift sagt, worauf man achtet; `alt` sagt, was zu sehen ist; nie die Lösung.
- Komponenten: keine. Brüche und Terme kann man nicht frei eintippen (die Eingabe kennt nur Zahlen); stattdessen
  Auswahl aus typischen Fehlern. Bedarf als Issue an `lernapps/app-templates` („Eingabe von Brüchen und Termen“).
- Grenzen: Die App prüft keine Zeichnung und keine Konstruktion, keinen frei geschriebenen Lösungsweg; kein Timer.
- Ein späteres Kapitel (z. B. W3 neu, Zinsen): Ordner anlegen, Seiten nach demselben Abschnittsschema, Muster aus
  dieser Tabelle, Selbsteinschätzung im `chapter.yaml` ergänzen.

**Seiten: Einstieg · Wechsel · Belohnung** (Geschichte: keine)

- zuordnungen/tabelle-koordinaten: Einkaufszettel → Tabelle füllen · Tabelle, Punkte, Ablesen · „Du liest Graphen wie eine Karte.“
- zuordnungen/proportional: Zwei Wertepaare, Faktor finden · Tabelle, Merke „je mehr, desto mehr“, Auswahl · eigene Tabelle ergänzt.
- zuordnungen/antiproportional: Pizza teilen: Personen und Stücke · Produkt x · y entdecken, Vergleich · Unterschied begründet.
- zuordnungen/graphen: Punkte einzeichnen, Form raten · SVG Gerade/Hyperbel, Zuordnen · Kapitelrückblick.
- prozent/prozentwert: Hunderterfeld: 1 % sehen · Formel, Beispiel, Rechnen · Rabatt selbst ausgerechnet.
- prozent/prozentsatz-grundwert: Welche Größe fehlt? · Formel umstellen, Rechnen · alle drei Größen beherrscht.
- prozent/sachaufgaben: Schritte ordnen · Sachaufgabe, Antwortsatz · Kapitelrückblick.
- flaechen/quadrat-rechteck: Kästchen zählen · Formel, Fläche/Umfang unterscheiden · Zimmerboden berechnet.
- flaechen/dreieck: Rechteck halbieren · SVG Höhen innen/außen, Rechnen · jede Höhe gefunden. **Musterseite.**
- flaechen/parallelogramm-trapez: Parallelogramm zerschneiden und umlegen · SVG, Rechnen · zwei Formeln hergeleitet.
- flaechen/quader-wuerfel: Würfelchen schichten · Formel, Rechnen · Aquarium gefüllt.
- flaechen/netz-oberflaeche: Netz oder kein Netz? · Netz färben, O berechnen · Geschenkpapier berechnet.
- flaechen/formeln-umstellen: Höhe gesucht · Umstellen wie Gleichung, Ordnen · Kapitelrückblick.
- terme/aufstellen: Rechenvorschrift in Zeichen · Auswahl, Ordnen · „Du übersetzt Text in Mathe.“
- terme/werte-berechnen: Wertetabelle füllen · Einsetzen, Merke 3x ≠ 34 · Tabelle komplett.
- terme/zusammenfassen: Obstkorb-Falle (Merke) · Sortieren, Auswahl · lange Terme gekürzt.
- terme/produkte: Vorzeichen zuerst · Regeltabelle, Rechnen · Kapitelrückblick.
- wahrscheinlichkeit/laplace: Ergebnisraum eines Würfels aufschreiben · günstige markieren, Bruch wählen · faire Spiele erkannt.
- wahrscheinlichkeit/baumdiagramm: Münze zweimal werfen · Baum lesen, Äste ergeben 1 · eigener Baum.
- wahrscheinlichkeit/pfadregeln: Pfad verfolgen · multiplizieren/addieren, Rechnen · Kapitelrückblick.
- symmetrie/symmetrie-erkennen: Buchstaben falten · Achse/Punkt zuordnen · Alphabet sortiert.
- symmetrie/spiegeln-drehen: Punkt spiegeln, Koordinaten · SVG, Ablesen · Kapitelrückblick.
- winkel/winkelsumme: Drei Ecken aneinanderlegen · Rechnen Dreieck/Viereck · jeden fehlenden Winkel gefunden.
- winkel/geradenkreuzungen: Winkelpaare färben · Zuordnen, Rechnen · Kapitelrückblick.
- brueche/plus-minus: Pizzastücke addieren · Hauptnenner, Merke Zähler+Zähler · Rezept umgerechnet.
- brueche/mal-geteilt: Hälfte von einem Drittel · Kehrwert, Rechnen · Dezimal ↔ Bruch.
- brueche/rechenregeln: Reihenfolge markieren · Ordnen, Rechnen · Kapitelrückblick.
- w2-konstruktionen/planfigur: Fehler in einer Planfigur finden · Beschriften, Zuordnen · Planfigur sitzt.
- w2-konstruktionen/kongruenzsaetze: Welche Stücke sind gegeben? · Satz zuordnen, eindeutig? · alle vier Sätze.
- w2-konstruktionen/konstruktion-schritte: Erster Schritt? · Ordnen mit Höhe/Seiten-/Winkelhalbierender · Strategie fertig.
- w2-konstruktionen/winkel-pruefen: Fehlender Winkel · Rechnen, Prüfen · Kapitelrückblick.
- w1-gleichungen/klammern: Rechteck aus Klammern · ausmultiplizieren, Auswahl · Minusklammer gemeistert.
- w1-gleichungen/gleichungen: Waage · Schritte ordnen, x berechnen · x² streichen erkannt.
- w1-gleichungen/ungleichungen: Zahlenbeispiel −2 < 3 · Zeichen drehen, Auswahl · Regel begründet.
- w1-gleichungen/nullprodukt: „Was mal was ist 0?“ · beide Faktoren = 0, Auswahl · zwei Lösungen gefunden.
- w1-gleichungen/loesungsmenge: Liegt 2,5 in ℤ? · L angeben, Probe · Kapitelrückblick.
- w3-prozent/zu-abnahme: +20 % am Hunderterfeld · Faktor, Rechnen · Preisschild berechnet.
- w3-prozent/vergleich: Wer ist teurer, um wie viel %? · Grundwert wählen, Rechnen · Vergleich begründet.
- w3-prozent/mehrere-aenderungen: +20 %, dann −20 % · Faktoren multiplizieren, Prozentpunkte · Kapitelrückblick.
- w4-zufall/ohne-zuruecklegen: Urne vorher/nachher · Nenner anpassen, Baum · Ziehung durchgerechnet.
- w4-zufall/ereignisse-pfade: „genau einmal“ markieren · Pfade zuordnen, Rechnen · Ereignisse übersetzt.
- w4-zufall/gegenereignis: „mindestens einmal“ ist mühsam · 1 − P, Rechnen · Kapitelrückblick.

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [x] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [x] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [x] Load skill `lernapps-explainer`.
- [x] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [x] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
- [x] Musterseite flaechen/dreieck: Einstieg Rechteck halbieren, SVG mit Höhen innen und außen, Formel, Beispielbox, Merke schräge Seite, Übung mit generated (A, u, Höhe außen) und Fehlerdiagnose; zeigt das Abschnittsschema und die Farbregeln für alle Seiten
<!-- tasks: pattern (1 added): the one page or screen that is the pattern for the others -->
- [x] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
      Creator: ja
- [x] Startseite: Wettbewerb in drei Sätzen (8 Pflicht-, 2 von 4 Wahlaufgaben, ohne Taschenrechner), Vorgehen für jede Aufgabe, Link zur Selbsteinschätzung
- [x] Kapitel zuordnungen: 4 Seiten (tabelle-koordinaten, proportional, antiproportional, graphen) mit SVG-Koordinatensystemen, Selbsteinschätzung
- [x] Kapitel prozent: 3 Seiten (prozentwert, prozentsatz-grundwert, sachaufgaben) mit Hunderterfeld, generated mit Fehlerdiagnose, Selbsteinschätzung
- [x] Kapitel flaechen, übrige 5 Seiten (quadrat-rechteck, parallelogramm-trapez, quader-wuerfel, netz-oberflaeche, formeln-umstellen) nach der Musterseite, Abschnitt Einheiten, Selbsteinschätzung
- [ ] Kapitel terme: 4 Seiten (aufstellen, werte-berechnen, zusammenfassen, produkte), Terme als Auswahl, Selbsteinschätzung
- [ ] Kapitel wahrscheinlichkeit: 3 Seiten (laplace, baumdiagramm, pfadregeln) mit Daten zufallsversuche.yaml und SVG-Bäumen, Selbsteinschätzung
- [ ] Kapitel symmetrie: 2 Seiten (symmetrie-erkennen, spiegeln-drehen) mit Daten figuren.yaml, Selbsteinschätzung
- [ ] Kapitel winkel: 2 Seiten (winkelsumme, geradenkreuzungen) mit SVG-Winkelpaaren, Selbsteinschätzung
- [ ] Kapitel brueche: 3 Seiten (plus-minus, mal-geteilt, rechenregeln), Brüche als Auswahl, Abschnitt Kürzen/Erweitern, Selbsteinschätzung
- [ ] Kapitel w2-konstruktionen: 4 Seiten (planfigur, kongruenzsaetze, konstruktion-schritte, winkel-pruefen) mit Planfiguren als SVG, Daten kongruenzsaetze.yaml, Abschnitt Grundkonstruktionen, Selbsteinschätzung
- [ ] Kapitel w1-gleichungen: 5 Seiten (klammern, gleichungen, ungleichungen, nullprodukt, loesungsmenge), Selbsteinschätzung
- [ ] Kapitel w3-prozent: 3 Seiten (zu-abnahme, vergleich, mehrere-aenderungen), Selbsteinschätzung
- [ ] Kapitel w4-zufall: 3 Seiten (ohne-zuruecklegen, ereignisse-pfade, gegenereignis) mit Urnen-SVGs, Selbsteinschätzung
<!-- tasks: pages (13 added): the other pages or screens, after the pattern -->
- [ ] Update the content guide so that it describes the app as built (`app-content-matches`).
- [ ] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [ ] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [ ] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
