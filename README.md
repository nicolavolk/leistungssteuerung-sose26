# Leistungssteuerung: Methoden der Datenanalyse
Interaktive HTML-Lerntools für Methoden der Datenanalyse – Modul 13: Leistungssteuerung - SoSe 26 - Volk
---
# Lernunterlage: Methoden der Datenanalyse in der Leistungssteuerung

**UE 4 · Modul 13 Leistungssteuerung · SoSe 2026**  
Nicola R. Volk, M.Sc. | Ruhr-Universität Bochum

## Überblick: Fünf interaktive Analysemodule

Diese Lernunterlage begleitet die fünf interaktiven HTML-Module der UE 4. Jedes Modul behandelt ein eigenständiges Analyseinstrument, das in der evidenzbasierten Leistungssteuerung zentral ist — zusammen bilden sie eine methodische Kette, die vom Einzelwert-Vergleich mit einer Normgruppe bis zur Beurteilung praktischer Bedeutsamkeit führt. Modul E ist der Sonderfall für Projekte mit nur einer Versuchsperson (N = 1).

```
Modul A               Modul B               Modul C               Modul D          Modul E (N=1)
z-Transformation  →   Pre-Post-Analyse  →   Messfehler & MDC  →   Effektgröße  →   Einzelfall-Analyse
─────────────────     ─────────────────     ─────────────────     ─────────────     ─────────────────
Wo steht ein Athlet   Wie verändert sich    Ist eine Veränderung   Wie groß ist     Was lässt sich
im Vergleich zur      eine Gruppe vom Pre-  größer als der         der Unterschied  über eine Person
Normgruppe?           zum Post-Test?        Messfehler?            praktisch?       methodisch sagen?
```

**Lernziel der UE:** Du kannst sportliche Messwerte normieren, individuelle Trainingsreaktionen klassifizieren, Messfehler-Grenzen berechnen und Effektgrößen interpretieren — und weißt, wie diese Methoden im Rahmen der Leistungssteuerung zusammenwirken. Für Einzelfall-Studien (N = 1) stehen mit Modul E die Methoden MDC₉₅, SWC und Δz zur Verfügung.

---

**Einstiegspunkt:** [`00_Lernunterlage.html`](00_Lernunterlage.html) — strukturierte Lernunterlage mit Aufgaben zu jedem Modul.

---

## Nutzung

Alle Dateien herunterladen (oder im Browser öffnen via GitHub Pages) — die Tools laufen vollständig im Browser, ohne Installation oder Internet-Verbindung.

```
00_Lernunterlage.html   ← Hier starten
01_Z-Score.html
02_Pre-Post.html
03_Messfehler.html
04_Effektgroesse.html
05_Einzelfall.html
```

> Alle Dateien müssen im **selben Ordner** liegen, damit die Links zwischen den Tools funktionieren.

---

## Methodische Kette

```
Modul A          Modul B           Modul C            Modul D        Modul E (N=1)
z-Transformation → Pre-Post-Analyse → Messfehler & MDC → Effektgröße → Einzelfall-Analyse
```

Gemeinsame Konzepte: **SWC** (Smallest Worthwhile Change = 0,2 × SD) verbindet Modul B, C und E. **MDC₉₅** aus Modul C ist die methodische Grundlage für Modul E.

---

## Modul A — z-Transformation & Normierung

**Datei:** `01_Z-Score.html`

### Konzept

Die z-Transformation überführt einen Rohwert _x_ in eine standardisierte Einheit, die angibt, wie weit der Wert vom Mittelwert der Normgruppe entfernt ist — gemessen in Standardabweichungen:

$$z = \frac{x - M}{SD}$$

**Beispiel:** Ein Athlet springt 45 cm im CMJ. Die Normgruppe (gleiches Alter, gleiches Geschlecht) hat M = 40 cm, SD = 5 cm.  
→ z = (45 − 40) / 5 = **+1,00**  
→ Der Athlet liegt **eine Standardabweichung über dem Durchschnitt** seiner Normgruppe — das entspricht dem **84. Perzentil**.

Das Perzentil gibt an, welchen Prozentsatz der Normgruppe der Athlet übertrifft.

### Schaltflächen und Eingabefelder

| Element                                | Beschreibung                                                                                                                                                                                                                                                                                            |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Frei eingeben / DTB-Normwerte**      | Umschalter zwischen zwei Eingabemodi. "Frei eingeben" erlaubt beliebige M und SD; "DTB-Normwerte" lädt reale Normdaten des DTB-Performance-Tests (Volk et al.) für die gewählte Gruppe automatisch.                                                                                                     |
| **Geschlecht**                         | (nur DTB-Modus) Wählt die Normgruppe nach Geschlecht (männlich/weiblich). Beeinflusst M und SD aller Testvariablen.                                                                                                                                                                                     |
| **Altersgruppe**                       | (nur DTB-Modus) Wählt die Altersgruppe in Halbjahresschritten (< 10 Jahre bis ≥ 18 Jahre). Normwerte verändern sich mit dem Alter.                                                                                                                                                                      |
| **Testvariable**                       | (nur DTB-Modus) Auswahl der Leistungsvariable (z. B. CMJ, 10m Sprint, F₀). Der Badge "↑ höher = besser" bzw. "↓ niedriger = besser" zeigt die Bewertungsrichtung — wichtig bei Sprintzeiten, wo ein kleiner Wert besser ist.                                                                            |
| **Mittelwert (M)**                     | Mittelwert der Referenzpopulation. Im DTB-Modus gesperrt (grau hinterlegt), da automatisch befüllt.                                                                                                                                                                                                     |
| **Std.-Abweichung (SD)**               | Streuung der Referenzpopulation. Bestimmt, wie "breit" die Normalverteilung im Diagramm erscheint. Je kleiner die SD, desto homogener die Gruppe.                                                                                                                                                       |
| **Rohwert-Slider**                     | Schiebt den eigenen Messwert _x_ entlang der Verteilung. Die Ergebniskarten und das Diagramm aktualisieren sich in Echtzeit.                                                                                                                                                                            |
| **Rohwert-Eingabe**                    | Direkteingabe des Messwertes. Ist mit dem Slider synchronisiert.                                                                                                                                                                                                                                        |
| **Simulation: Normgruppe verschieben** | Verschiebt den Normgruppenmittelwert um bis zu ±3 SD, ohne den eigenen Wert zu verändern. Demonstriert, wie sehr das z-Score-Ergebnis von der gewählten Referenzgruppe abhängt. Dies ist didaktisch zentral: Derselbe Rohwert kann "gut" oder "schlecht" wirken, je nachdem, gegen wen verglichen wird. |

### Anzeigekarten (rechts oben)

| Karte          | Bedeutung                                                                                                                          |
| -------------- | ---------------------------------------------------------------------------------------------------------------------------------- |
| **z-Wert**     | Standardisierter Wert. Positiv = über dem Durchschnitt, negativ = darunter.                                                        |
| **Perzentil**  | Prozentualer Rang in der Normgruppe. z = +1 ≈ 84. Perzentil; z = −1 ≈ 16. Perzentil.                                               |
| **Einordnung** | Verbale Kategorisierung: Weit unter Ø (z < −2), Unter Ø (−2 bis −1), Durchschnittlich (±1), Über Ø (1 bis 2), Weit über Ø (z > 2). |

### Farbzonen im Diagramm

Die Normalverteilung ist in fünf Zonen eingefärbt (hellblau = unter Durchschnitt, dunkelblau = über Durchschnitt). Der rote Punkt markiert den eigenen Wert. Die schattierte Fläche links des Punktes entspricht dem Perzentil.

> **Achtung bei Sprintzeiten:** Bei invertierten Metriken (5m, 10m, 20m) wird das z-Score invertiert dargestellt: Ein schneller (niedriger) Wert erhält ein positives z-Score und ein hohes Perzentil.

### Lernaufgaben Modul A

1. Stelle M = 40, SD = 5, Rohwert = 40 ein. Was ist das z-Score? Was sagt das über den Athleten?
2. Erhöhe die SD auf 10 bei gleichem Rohwert. Was passiert mit dem z-Score und warum?
3. Wechsle in den DTB-Modus. Wähle "männlich, 14 Jahre, CMJ". Wo liegt ein CMJ von 35 cm?
4. Verschiebbe den Normgruppen-Slider auf +2 SD. Was passiert mit dem Percentil? Was bedeutet das für die Auswahl der Referenzgruppe?

---

## Modul B — Pre-Post Visualizer

**Datei:** `02_Pre-Post.html`

### Konzept

Im Trainingsalltag messen wir Athleten vor und nach einer Intervention (Pre-Test, Post-Test). Die zentrale Frage lautet: **Hat sich jemand tatsächlich verbessert — und wenn ja, wer?**

Zur Klassifikation nutzt das Modul den **SWC** (_Smallest Worthwhile Change_), den kleinsten praktisch bedeutsamen Unterschied:

$$SWC = 0{,}2 \times SD_{Pre}$$

Dies entspricht der Definition eines "kleinen Effekts" nach Cohen (d = 0,2). Verändert sich ein Athlet um mehr als den SWC, gilt die Änderung als **praktisch bedeutsam**.

Zusätzlich wird der **Cohen's d_z** berechnet — eine Effektgröße für Wiederholungsmessungen:

$$d_z = \frac{\bar\Delta}{SD_\Delta}$$

### Schaltflächen und Eingabefelder

| Element                             | Beschreibung                                                                                                                                                                                                 |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Simulation / Manuelle Eingabe**   | Umschalter zwischen Modi. Im Simulationsmodus werden Daten zufällig erzeugt; im manuellen Modus können eigene Werte tabellarisch eingegeben werden.                                                          |
| **N Athleten (Slider)**             | Stichprobengröße 4–20. Mehr Athleten erhöhen die Stabilität der Kennwerte.                                                                                                                                   |
| **Mittelwert Pre**                  | Ausgangsniveau der Gruppe (z. B. 40 cm CMJ).                                                                                                                                                                 |
| **SD Pre**                          | Streuung beim Pre-Test. Beeinflusst direkt den SWC (SWC = 0,2 × SD).                                                                                                                                         |
| **Mittl. Δ (Effekt)**               | Der durchschnittliche wahre Trainingseffekt in der Stichprobe.                                                                                                                                               |
| **Streuung der ind. Veränderungen** | Streuung der individuellen Veränderungen. Hohe Werte = heterogene Trainingsreaktionen.                                                                                                                       |
| **🔀 Neu**                          | Erzeugt eine neue Zufallsstichprobe mit denselben Parametern. Wichtig: Veranschaulicht Stichprobenvariabilität — dieselben "wahren" Parameter können sehr unterschiedliche beobachtete Stichproben erzeugen. |
| **+ Athlet / − Athlet**             | (manueller Modus) Zeilen in der Datentabelle hinzufügen oder entfernen.                                                                                                                                      |
| **Pre-/Post-Felder in Tabelle**     | (manueller Modus) Direkte Eingabe der Messwerte. Das Δ und der Responder-Status (↑ ↓ →) werden sofort berechnet.                                                                                             |

### Diagrammtypen (Tabs)

| Tab                | Was wird gezeigt                                                                                                                                                                                                           |
| ------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spaghetti-Plot** | Jede Linie verbindet Pre- und Post-Wert eines Athleten. Farbkodierung: Grün = Responder (Δ > SWC), Grau = kein klarer Effekt, Rot = negativer Responder. Die gestrichelte blaue Linie zeigt den Gruppenmittelwert.         |
| **Waterfall**      | Balken nach individuellem Δ sortiert (aufsteigend). Zeigt auf einen Blick, wie die Veränderungen verteilt sind und welche Athleten die SWC-Schwelle überschreiten. Die orangefarbenen gestrichelten Linien markieren ±SWC. |
| **Beeswarm**       | Einzelpunkte als "Schwarm" angeordnet, mit Mittelwert und SD-Balken. Erlaubt den Vergleich der Verteilungsform zwischen Pre und Post.                                                                                      |

### Anzeigekarten (rechts oben)

| Karte           | Bedeutung                              |
| --------------- | -------------------------------------- |
| **M Pre**       | Mittelwert beim Pre-Test               |
| **M Post**      | Mittelwert beim Post-Test              |
| **Ø Δ%**        | Prozentualer Gruppeneffekt             |
| **Cohen's d_z** | Effektgröße für Wiederholungsmessungen |
| **Responder**   | Anzahl Athleten mit Δ > SWC            |
| **Non-Resp.**   | Anzahl Athleten mit Δ < −SWC           |

### Lernaufgaben Modul B

1. Setze Mittl. Δ = 0 und SD der Δs = 3. Wie viele "Responder" entstehen rein durch Zufall? Klicke mehrfach "Neu" und beobachte die Schwankung.
2. Erhöhe die SD Pre von 5 auf 10 bei gleichem Δ = 3. Was passiert mit dem SWC und der Responder-Zahl?
3. Wechsle alle drei Diagrammtypen durch. Welcher Plot hilft dir am besten, heterogene Trainingsreaktionen zu erkennen?
4. Gib im manuellen Modus selbst 8 Athleten ein (4 verbessern sich deutlich, 4 kaum). Beschreibe die Verteilung mit Zahlen.

---

## Modul C — Messfehler, SEM & MDC

**Datei:** `03_Messfehler.html`

### Konzept

Jedes Messinstrument macht Fehler. Bevor wir eine Veränderung im Athleten interpretieren, müssen wir wissen: **Ist diese Veränderung größer als das Rauschen des Tests selbst?**

**Berechnungskette:**

1. **ICC** (Intraklassenkorrelation): Maß für die Reliabilität — wie konsistent produziert der Test dasselbe Ergebnis bei derselben Person? Wertebereich 0–1.

2. **SEM** (Standard Error of Measurement — Standardmessfehler):
   $$SEM = SD_{Baseline} \times \sqrt{1 - ICC}$$

3. **MDC₉₅** (Minimal Detectable Change — Minimale echte Änderung):
   $$MDC_{95} = SEM \times 1{,}96 \times \sqrt{2}$$

Der Faktor 1,96 entspricht dem 95%-Konfidenzintervall; √2 berücksichtigt, dass zwei Messzeitpunkte (Pre und Post) je einen eigenen Messfehler haben.

**Kritischer Vergleich:** Der MDC wird dem SWC (0,2 × SD) gegenübergestellt. Wenn MDC > SWC, dann übertönt der Messfehler den kleinsten praktisch bedeutsamen Effekt — der Test ist für individuelle Aussagen zu ungenau.

### Schaltflächen und Eingabefelder

| Element                | Beschreibung                                                                                                                                                                                                                  |
| ---------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **ICC-Slider**         | Kernparameter. Bewegt ICC von 0,50 (schlecht) bis 0,995 (exzellent). Der angezeigte ICC-Wert aktualisiert alle Berechnungen sofort. Schwellenwerte: ≥ 0,95 = exzellent; ≥ 0,90 = gut; ≥ 0,75 = akzeptabel; < 0,75 = schlecht. |
| **SD Baseline**        | Streuung der Gruppe beim Pre-Test. Beeinflusst SEM, MDC und SWC. Größere SD → größerer MDC.                                                                                                                                   |
| **Mittelwert**         | Durchschnittswert der Gruppe (wird für den CV% benötigt).                                                                                                                                                                     |
| **N Athleten**         | Stichprobengröße für die Simulation (4–30).                                                                                                                                                                                   |
| **Wahrer Effekt (Δ)**  | Gibt an, welche echte Veränderung im simulierten Datensatz vorliegt. Kann auf 0 gesetzt werden, um "Rauschen ohne Effekt" zu simulieren.                                                                                      |
| **🔀 Neue Stichprobe** | Generiert neue Zufallsathletendaten mit denselben Parametern. Wichtig: Zeigt, wie zufällig ein bestimmter Befund (z. B. "6 von 12 über MDC") wirklich ist.                                                                    |

### Diagrammtypen (Tabs)

| Tab                       | Was wird gezeigt                                                                                                                                                                                                                                                                                        |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Entscheidungsdiagramm** | Jeder Athlet als Punkt entlang der Δ-Achse. Die grau schraffierte Zone markiert ±MDC — Punkte innerhalb dieser Zone gelten als "nicht eindeutig". Farbkodierung wie in Modul B. Die orangefarbene gestrichelte Linie zeigt die SWC-Referenz.                                                            |
| **Verteilungen**          | Zwei Normalverteilungen: Die graue zeigt, wie Messwert-Unterschiede allein durch Messfehler entstehen (Δ_wahr = 0). Die blaue zeigt, wie die Verteilung bei einem echten Effekt verschoben ist. Die Fläche rechts von +MDC unter der blauen Kurve entspricht der "Detektionsrate" (statistische Power). |
| **ICC-Sensitivität**      | Kurve: Wie verändert sich der MDC bei verschiedenen ICC-Werten? Der orangefarbene Punkt markiert den aktuell eingestellten ICC. Der rote Bereich links zeigt, wo MDC > SWC gilt.                                                                                                                        |

### Die Formelkette (linkes Panel, unten)

Die Schritte ICC → SEM → MDC₉₅ sind als "Kette" dargestellt. Der aktive Schritt (MDC₉₅) ist hervorgehoben. Dies soll die Abhängigkeit der Kennzahlen voneinander verdeutlichen.

### Anzeigekarten (rechts oben)

| Karte        | Bedeutung                                                                                            |
| ------------ | ---------------------------------------------------------------------------------------------------- |
| **SEM**      | Standardmessfehler in Messeinheiten.                                                                 |
| **MDC₉₅**    | Minimale echte Änderung (95%-Sicherheit). Rot hinterlegt, wenn MDC > SWC.                            |
| **CV%**      | Variationskoeffizient = SEM / M × 100. Ermöglicht den Vergleich über Tests mit verschiedenen Skalen. |
| **Über MDC** | Anzahl Athleten, bei denen Δ > MDC gilt.                                                             |

### Lernaufgaben Modul C

1. Setze ICC = 0,90, SD = 5. Berechne SEM und MDC₉₅ per Hand und überprüfe das Ergebnis.
2. Reduziere den ICC auf 0,70. Was passiert mit MDC und dem Verhältnis zu SWC?
3. Öffne den Tab "ICC-Sensitivität". Ab welchem ICC-Wert gilt MDC > SWC (roter Bereich)? Was folgt daraus für die Tauglichkeit des Tests?
4. Setze "Wahrer Effekt" auf 0, klicke 5× "Neue Stichprobe". Wie viele Athleten landen jedes Mal fälschlicherweise über der MDC-Grenze (falsch-positiv)?

---

## Modul D — Effektgröße: Cohen's d & Hedges' g

**Datei:** `04_Effektgroesse.html`

### Konzept

Um zwei Gruppen (z. B. Trainings- vs. Kontrollgruppe) oder zwei Zeitpunkte zu vergleichen, reicht es nicht, nur zu fragen: "Gibt es einen Unterschied?" — sondern: **Wie groß ist dieser Unterschied praktisch?**

**Cohen's d** standardisiert den Mittelwertunterschied mit der gepoolten Standardabweichung:

$$d = \frac{M_B - M_A}{SD_{pooled}} \qquad SD_{pooled} = \sqrt{\frac{SD_A^2 + SD_B^2}{2}}$$

**Hedges' g** korrigiert d für kleine Stichproben:

$$g = d \times J(df) \qquad J = 1 - \frac{3}{4 \cdot df - 1} \qquad df = n_A + n_B - 2$$

Bei kleinen Stichproben (n < 20) überschätzt d den wahren Effekt leicht — g ist dann die genauere Angabe.

**Konventionen nach Cohen (1988):**

|         | d       |                               | Bezeichnung | Intuition |
| ------- | ------- | ----------------------------- | ----------- | --------- |
| < 0,2   | Trivial | Kaum wahrnehmbar              |
| 0,2–0,5 | Klein   | Sichtbar, aber gering         |
| 0,5–0,8 | Mittel  | Praktisch bedeutsam           |
| ≥ 0,8   | Groß    | Deutlich wahrnehmbarer Effekt |

### Schaltflächen und Eingabefelder

| Element                                       | Beschreibung                                                                                                                                      |
| --------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Simulation / Manuell**                      | Im Simulationsmodus wird d direkt per Slider eingestellt; im manuellen Modus werden M, SD und n beider Gruppen eingegeben.                        |
| **Zwei Gruppen / Pre–Post**                   | Wechselt die Beschriftungen (Gruppe A/B vs. Pre/Post). Ändert keine Berechnung, aber die Visualisierung und die CLES-Beschreibung.                |
| **Cohen's d (Slider)**                        | (nur Simulation) Stellt die Effektgröße von −3 bis +3 ein. Die Verteilungen im Diagramm verschieben sich live.                                    |
| **SD der Gruppen — Gleich / Unterschiedlich** | Bei "Gleich" wird eine SD = 1 angenommen; bei "Unterschiedlich" können SD_A und SD_B getrennt eingegeben werden, was die gepoolte SD beeinflusst. |
| **Stichprobengröße n**                        | Beeinflusst die Hedges'-g-Korrektur — größere Stichproben nähern g an d an.                                                                       |

### Anzeigekarten (rechts oben)

| Karte             | Bedeutung                                                                                                                                                                                     |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Cohen's d**     | Standardisierte Effektgröße; Interpretation lt. Konventionen rechts unten.                                                                                                                    |
| **Überlappung**   | Anteil der Fläche, den beide Verteilungen teilen. Je kleiner, desto unterschiedlicher die Gruppen. Bei d = 0: 100% Überlappung; bei d = 2: ca. 30% Überlappung.                               |
| **CLES**          | _Common Language Effect Size_: Wahrscheinlichkeit, dass eine zufällig gewählte Person aus Gruppe B besser abschneidet als eine aus Gruppe A. Intuitiv verständlichster Effektgrößen-Ausdruck. |
| **NNT-Intuition** | "X von 100 zeigen klaren Vorteil" — entspricht der CLES in Prozentzahlen.                                                                                                                     |

### Das Diagramm

Zwei überlappende Normalverteilungen: Gruppe A/Pre in Blau, Gruppe B/Post in Orange. Der schraffierte Bereich zeigt die Überlappungszone. Der Doppelpfeil oben mit d-Wert zeigt den Abstand der Mittelwerte. Je weiter die Glocken auseinanderrücken, desto kleiner die Überlappung, desto größer der Effekt.

### Lernaufgaben Modul D

1. Stelle d = 0,2, dann d = 0,5, dann d = 0,8 ein. Beschreibe verbal, was du im Diagramm siehst. Wie verändert sich die Überlappung?
2. Setze d = 0,5 und n = 5. Dann n = 50. Wie verändert sich Hedges' g? Warum ist die Korrektur bei kleinen Stichproben wichtig?
3. Bei welchem d-Wert liegt die CLES bei 50%? Was bedeutet das inhaltlich?
4. Wechsle in den manuellen Modus und gib realistische Daten ein (z. B. Trainingsgruppe: M = 44 cm, SD = 5, n = 12; Kontrollgruppe: M = 40 cm, SD = 5, n = 12). Berechne d per Hand und vergleiche mit der Anzeige.

---

## Modul E — Einzelfall-Analyse (N = 1)

**Datei:** `05_Einzelfall.html`

### Konzept

Wenn nur eine Person getestet, trainiert und erneut getestet wird (N = 1), entfällt Gruppenstatistik. Deskriptive Beschreibung (Δ in Rohwerten, Prozentwert) reicht allein nicht aus — ohne Referenz ist unklar, ob eine beobachtete Veränderung real oder durch Messfehler erklärbar ist. Drei bekannte Konzepte aus den Modulen A, B und C werden kombiniert:

| Methode   | Frage                                | Formel          |
| --------- | ------------------------------------ | --------------- |
| **MDC₉₅** | Ist Δ größer als das Messrauschen?   | SEM × 1,96 × √2 |
| **SWC**   | Ist Δ praktisch bedeutsam?           | 0,2 × SD_norm   |
| **Δz**    | Hat sich die Normposition verändert? | z_post − z_pre  |
| **RCI**   | Standardisierter Einzelfall-z-Wert   | Δ / SEM_diff    |

Dabei gilt: SEM = SD × √(1 − ICC) und SEM_diff = SEM × √2.

**3-Stufen-Ampel (Kernlogik):**

1. **Rot** — |Δ| < MDC₉₅: Im Messrauschen, keine sichere Interpretation möglich.
2. **Gelb** — |Δ| ≥ MDC₉₅, aber |Δ| < SWC: Echte, aber triviale Veränderung.
3. **Grün** — |Δ| ≥ MDC₉₅ **und** |Δ| ≥ SWC: Echte, praktisch bedeutsame Veränderung.

Der **RCI** (Reliable Change Index, Jacobson & Truax, 1991) ist mathematisch äquivalent zur MDC₉₅-Entscheidung, drückt das Ergebnis aber als standardisierten z-Wert aus: |RCI| ≥ 1,96 entspricht einer reliablen Veränderung mit 95 % Sicherheit.

### Parameter-Quellen für N=1

- **ICC**: Aus der Literatur (z. B. Hopkins et al. 2009; testspezifische Metaanalysen)
  - CMJ: ICC ≈ 0,95 · Sprintzeit: ICC ≈ 0,97 · Maximalkraft: ICC ≈ 0,90–0,95
- **SD**: Aus Normtabellen der Referenzgruppe (Alter, Geschlecht, Sportart)

### Schaltflächen und Eingabefelder

| Element               | Beschreibung                                                                           |
| --------------------- | -------------------------------------------------------------------------------------- |
| **Pre-/Post-Wert**    | Messwerte der Einzelperson vor und nach der Intervention                               |
| **Einheit**           | Optional (z. B. cm, s, W/kg) — nur für Anzeige                                         |
| **Richtung**          | "↑ höher = besser" für Sprung-/Kraftvariablen; "↓ niedriger = besser" für Sprintzeiten |
| **Mittelwert M / SD** | Kennwerte der Referenzgruppe (aus Normtabellen oder Literatur)                         |
| **ICC-Slider**        | Reliabilität des Tests (0,70–0,99). Beeinflusst SEM, MDC und RCI — nicht aber SWC      |

### Anzeigekarten

| Karte     | Bedeutung                                               |
| --------- | ------------------------------------------------------- | --- | ------- |
| **Δ**     | Rohwert-Differenz (Post − Pre) mit Prozentwert          |
| **MDC₉₅** | Minimale echte Änderung; grün wenn                      | Δ   | darüber |
| **SWC**   | Kleinste praktisch bedeutsame Änderung (0,2 × SD)       |
| **RCI**   | Standardisierter Einzelfall-Effekt; grün wenn           | RCI | ≥ 1,96  |
| **Δz**    | Veränderung der z-Score-Position (mit Perzentil-Angabe) |
| **SEM**   | Standardmessfehler (aus ICC und SD)                     |

### Das Diagramm

Die Normalverteilung der Referenzgruppe mit Pre- und Post-Position als markierte Punkte. Der grau schraffierte Bereich zeigt die MDC-Zone um die Pre-Position; die orangenen gestrichelten Linien markieren die SWC-Grenzen. Ein farbiger Pfeil (grün = Verbesserung, rot = Verschlechterung) verbindet Pre und Post.

### Lernaufgaben Modul E

1. Pre = 38 cm, Post = 41 cm, SD = 5, ICC = 0,95. Berechne MDC₉₅ per Hand (SEM = 5 × √(1−0,95) ≈ 1,12 cm; MDC = 1,12 × 1,96 × √2 ≈ 3,10 cm). Welche Ampelfarbe ergibt sich?
2. Gleiche Werte, aber ICC = 0,75. Was ändert sich am MDC? Ändert sich der SWC? Warum nicht?
3. Setze Pre = Post (Δ = 0). Welche Farbe zeigt die Ampel? Was sagt der RCI?
4. 10m-Sprintzeit: Pre = 1,82 s, Post = 1,79 s, ICC = 0,97, SD_norm = 0,08 s. Mit "niedriger = besser": Ist die Veränderung praktisch bedeutsam?

---

## Verbindung der fünf Module: Die methodische Kette

Die fünf Module bilden zusammen eine typische Analysekette in der Leistungssteuerung:

```
SCHRITT 1: Einzelathlet einordnen (Modul A)
  → z-Transformation zeigt, wo ein Athlet im Vergleich zur Altersgruppe steht.
  → Grundlage für individuelle Stärken-Schwächen-Profile.

SCHRITT 2: Gruppenveränderung nach Intervention sichten (Modul B)
  → Pre-Post-Analyse zeigt, welche Athleten auf ein Training reagieren (Responder).
  → SWC definiert die Minimalschwelle für praktische Bedeutsamkeit.

SCHRITT 3: Echte Änderung vs. Messfehler trennen (Modul C)
  → MDC₉₅ stellt klar: Ist das beobachtete Δ größer als das Messrauschen?
  → Ohne Kenntnis des MDC können Veränderungen falsch interpretiert werden.

SCHRITT 4: Praktische Bedeutsamkeit quantifizieren (Modul D)
  → Cohen's d / Hedges' g erlaubt den Vergleich mit Literaturwerten.
  → CLES macht den Effekt für alle Beteiligten kommunizierbar.

SONDERFALL N=1: Einzelfall-Analyse (Modul E)
  → Δ mit MDC₉₅ vergleichen: Ist die Veränderung reliabel?
  → Δ mit SWC vergleichen: Ist sie praktisch bedeutsam?
  → Δz berechnen: Hat sich die Normposition verändert?
```

**Wichtige Querverbindungen:**

- Der **SWC** (0,2 × SD) erscheint in Modul B, C _und_ E — derselbe Schwellenwert, drei Kontexte.
- Der **MDC** aus Modul C sollte kleiner als der SWC sein, damit ein Test für individuelle Trainingssteuerung geeignet ist — Kernbedingung auch in Modul E.
- **Cohen's d = 0,2** entspricht exakt der Definition des SWC. Damit ist der SWC nichts anderes als der Effekt, den ein "kleines d" erzeugen würde.
- Die **z-Transformation** (Modul A) und die **Effektgröße d** (Modul D) basieren beide auf Standardabweichungen. Modul E nutzt z-Scores aus Modul A zur Kontextualisierung der Einzelfall-Veränderung.
- Der **RCI** (Modul E) ist mathematisch identisch mit der MDC₉₅-Entscheidung aus Modul C, nur als standardisierter Wert ausgedrückt.

---

## Häufige Missverständnisse

**"Ein z-Score von +2 bedeutet, der Athlet ist sehr gut."**  
Nur relativ zur Normgruppe. Wenn die Normgruppe schlecht ist, kann z = +2 trotzdem einen absolut schwachen Wert bedeuten. Modul A zeigt das mit dem Simulations-Slider.

**"Wenn sich der Mittelwert verbessert, haben sich alle verbessert."**  
Nein. Modul B zeigt, dass hinter einem Gruppen-Δ oft stark heterogene individuelle Reaktionen stecken: Manche verbessern sich deutlich, andere kaum oder sogar negativ.

**"Ein Δ von 3 cm im CMJ ist eine echte Verbesserung."**  
Nicht unbedingt. Modul C und E zeigen: Wenn der MDC für diesen Test z. B. 4 cm beträgt, liegt das Δ innerhalb des Messfehlers — wir können keine sichere Aussage treffen.

**"Ein kleines d ist nicht relevant."**  
Kommt auf den Kontext an. Im Leistungssport kann d = 0,2 für Sprintselektion entscheidend sein. Cohen's Konventionen sind Daumenregeln, keine absoluten Grenzen.

**"Bei N = 1 kann man gar nichts aussagen."**  
Falsch. Modul E zeigt: Mit MDC₉₅, SWC und Δz lassen sich valide, methodisch begründete Aussagen über eine Einzelperson machen — vorausgesetzt, ICC und SD der Referenzgruppe sind bekannt.

---

## Literaturhinweise

- Cohen, J. (1988). _Statistical Power Analysis for the Behavioral Sciences_ (2. Aufl.). Erlbaum.
- Impellizzeri, F. M., et al. (2018). Internal and External Training Load: 15 Years On. _International Journal of Sports Physiology and Performance_, 14(2), 270–273.
- Hopkins, W. G., et al. (2009). Progressive Statistics for Studies in Sports Medicine and Exercise Science. _Medicine & Science in Sports & Exercise_, 41(1), 3–13.
- Jacobson, N. S., & Truax, P. (1991). Clinical significance: A statistical approach to defining meaningful change in psychotherapy research. _Journal of Consulting and Clinical Psychology_, 59(1), 12–19. — Quelle für den Reliable Change Index (RCI) in Modul E.
- Volk, N. R., et al. (in Vorbereitung). DTB Performance Test Normative Data.

---

_Erstellt für Modul 13 Leistungssteuerung, SoSe 2026 · RUB · Nicola R. Volk_
