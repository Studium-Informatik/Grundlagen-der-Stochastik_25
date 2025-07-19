### 1. Grundlagen der Wahrscheinlichkeitstheorie

- **Wahrscheinlichkeitsraum (Ω, E, P)**:
    - **Ergebnismenge (Ω)**: Die Menge aller möglichen Ergebnisse eines Zufallsexperiments (z.B. Ω = {0, 1} für Münzwurf).
    - **σ-Algebra (E)**: Eine Menge von Ereignissen (Teilmengen von Ω), für die Wahrscheinlichkeiten definiert werden können. Sie muss bestimmte Eigenschaften erfüllen (z.B. Ω ∈ E, Komplementbildung, abzählbare Vereinigungen).
        - **Borelmengen**: Die kleinste σ-Algebra, die alle offenen Intervalle enthält.
    - **Wahrscheinlichkeitsmaß (P)**: Eine Funktion, die jedem Ereignis in E eine Wahrscheinlichkeit zuordnet.
        - **Eigenschaften des Wahrscheinlichkeitsmaßes (Satz 1.3.2)**: z.B. P(∅)=0, P(Ω)=1, σ-Additivität, Stetigkeit von oben und unten.
        - **Konstruktion von Wahrscheinlichkeitsmaßen**: Für höchstens abzählbar unendliche Mengen Ω durch Zuweisung von Wahrscheinlichkeiten p_ω ≥ 0, sodass deren Summe 1 ergibt.
- **Gleichverteilung / Laplaceraum**: Wenn alle Ergebnisse in einer endlichen Ergebnismenge die gleiche Wahrscheinlichkeit haben. Bei n-fachem Münzwurf ist Pn(A) = |A|/|Ωn|.
- **Kontinuierliche Wahrscheinlichkeitsräume**: Das Konzept, dass einzelne Punkte Wahrscheinlichkeit 0 haben müssen, und Wahrscheinlichkeiten über Intervalle definiert werden (z.B. P([a, b]) = b-a für).

### 2. Diskrete Wahrscheinlichkeitsverteilungen

- **Bernoulli-Verteilung**: Modelliert einen einzelnen Versuch mit zwei Ausgängen (Erfolg/Misserfolg). Parameter ist die Erfolgswahrscheinlichkeit **p**.
    - **Erwartungswert**: **p**.
    - **Varianz**: **p - p²**.
- **Geometrische Verteilung**: Beschreibt die Wahrscheinlichkeit, dass der erste Erfolg in einer Reihe von Bernoulli-Versuchen beim **k-ten Versuch** eintritt. Parameter **q** (Wahrscheinlichkeit für Misserfolg).
    - **Wahrscheinlichkeitsfunktion**: P({k}) = q^(k-1)(1-q).
    - **Informelle Herleitung**: Beispiel Würfeln auf die erste "6".
    - **Erwartungswert**: **1/(1-q)**.
    - **Varianz**: **q/(1-q)²**.
- **Poisson-Verteilung**: Beschreibt die Wahrscheinlichkeit einer bestimmten Anzahl von Ereignissen in einem festen Intervall, wenn diese unabhängig und mit konstanter Rate auftreten. Parameter **λ**.
    - **Wahrscheinlichkeitsfunktion**: P({k}) = (λ^k / k!) * e^(-λ).
    - **Informelle Herleitung**: Als Grenzwert der Binomialverteilung.
    - **Erwartungswert**: **λ**.
- **Binomialverteilung**: Beschreibt die **Anzahl der Erfolge** in **n unabhängigen Bernoulli-Versuchen**. Parameter **n** (Anzahl der Versuche) und **p** (Erfolgswahrscheinlichkeit).
    - **Wahrscheinlichkeitsfunktion**: P(X = k) = (n über k) * p^k * (1-p)^(n-k).
    - **Erwartungswert**: **np**.
    - **Varianz**: **np(1-p)**.
- **Hypergeometrische Verteilung**: Beschreibt die Wahrscheinlichkeit einer Anzahl von Erfolgen in einer Stichprobe, die **ohne Zurücklegen** aus einer endlichen Population gezogen wird, die aus Erfolgen und Misserfolgen besteht.
    - **Formel der Wahrscheinlichkeitsmassenfunktion**: P(X = k) = [(K über k) * (N-K über n-k)] / (N über n).
        - N: Gesamtgröße der Population, K: Anzahl der Erfolge in der Population, n: Größe der Stichprobe, k: Anzahl der Erfolge in der Stichprobe.
    - **Anwendungsbereiche**: Qualitätskontrolle, Kartenspiele, Biologie (Fang-Wiederfang), Urnenmodelle, **Lotto 6 aus 49**.

### 3. Kontinuierliche Wahrscheinlichkeitsverteilungen

- **Wahrscheinlichkeitsdichte (pdf)**: Eine nicht-negative Funktion f(x), deren Integral über den Definitionsbereich 1 ergibt. Die Wahrscheinlichkeit eines Intervalls [c, d] ist das Integral von f(x) über dieses Intervall.
    - **Verteilungsfunktion (cdf)**: F(x) = ∫(-∞,x) dyf(y).
        - **Eigenschaften der Verteilungsfunktion**: F(x) ∈, monoton steigend, lim F(x) = 0 für x→-∞ und lim F(x) = 1 für x→+∞.
- **Gleichverteilung (kontinuierlich)**: Auf einem Intervall [a, b], mit Dichtefunktion **f(x) = 1/(b-a)**.
    - **Konvergenz in Verteilung**: Eine Folge von Gleichverteilungen Xn ~ U(0, 1/n) konvergiert in Verteilung gegen eine **Dirac-Verteilung (Punktmasse bei 0)**.
- **Exponentialverteilung**: Modelliert oft die Zeit bis zum Eintreten eines Ereignisses in einem Poisson-Prozess. Parameter **λ > 0**. Definiert auf **[0, +∞)**.
    - **Dichtefunktion**: **f(x) = λe^(-λx)**.
    - **Erweiterung auf R**: Mittels Indikatorfunktion, wo f(x)=0 für x<0.
- **Normalverteilung (Gaußsche Normalverteilung)**: Die wichtigste kontinuierliche Verteilung. Parameter **µ** (Erwartungswert) und **σ²** (Varianz).
    - **Dichtefunktion**: **f(x) = (1 / √(2πσ²)) * e^(-(x-µ)² / (2σ²))**.
    - **Erwartungswert**: **µ**.
    - **Varianz**: **σ²**.
    - **Standardnormalverteilung**: N(0,1) mit µ=0 und σ²=1.

### 4. Zufallsvariablen, Erwartungswert und Varianz

- **Zufallsvariable (ZV)**: Eine Funktion, die jedem Ergebnis eines Zufallsexperiments einen numerischen Wert zuordnet.
- **Verteilung einer ZV (PX)**: Das von der ZV induzierte Wahrscheinlichkeitsmaß.
- **Erwartungswert (E(X))**: Der "Durchschnittswert" vieler Beobachtungen.
    - **Definition für diskrete ZV**: E(X) = ∑c∈C c * P({X=c}).
    - **Definition für ZV mit Dichte**: E(X) = ∫Ω dx X(x)f(x).
    - **Existenz**: Der Erwartungswert existiert, wenn die Summe/das Integral von |c|P({X=c}) bzw. |X(x)|f(x) konvergiert.
- **Varianz (Var(X) oder V(X))**: Ein Maß für die Streuung der Datenpunkte um den Erwartungswert.
    - **Definition**: V(X) = E((X - E(X))²) = E(X²) - E(X)².
    - **Zusammenhang mit Erwartungswert**: V(X) < ∞ impliziert E(X) < ∞, aber nicht umgekehrt.
    - **Bedeutung**: Eine kleinere Varianz bedeutet, dass die Datenpunkte näher am Erwartungswert liegen.
- **Tschebycheff-Ungleichung (Satz 8.2.2)**: Begrenzt die Wahrscheinlichkeit, dass eine Zufallsvariable um mehr als einen bestimmten Betrag von ihrem Erwartungswert abweicht.
- **Markov-Ungleichung (Satz 8.2.3)**.

### 5. Konvergenzbegriffe und Grenzwerte

- **Gesetz der großen Zahlen**: Empirische Mittelwerte konvergieren gegen den Erwartungswert bei einer großen Anzahl von unabhängigen Beobachtungen.
    - **Schwaches Gesetz der Großen Zahlen (WLLN, Satz 8.2.5)**: Konvergenz in Wahrscheinlichkeit.
    - **Starkes Gesetz der Großen Zahlen (SLLN)**: Der Stichprobenmittelwert konvergiert **fast sicher** gegen den Erwartungswert.
        - Impliziert eine stärkere Form der Konvergenz als das WLLN und erfordert nur die Existenz des ersten Moments.
- **Zentraler Grenzwertsatz (ZGS)**: Die normierte Summe vieler unabhängiger und identisch verteilter (i.i.d.) Zufallsvariablen konvergiert in Verteilung gegen eine **Standardnormalverteilung N(0,1)**, unabhängig von der ursprünglichen Verteilung der Summanden.
- **Satz von De Moivre-Laplace**: Spezialfall des ZGS, die standardisierte Binomialverteilung konvergiert in Verteilung gegen die Standardnormalverteilung.
- **Konvergenzbegriffe von Zufallsvariablen**:
    - **Fast sichere Konvergenz (Xn f.s.→ X)**: Die Zahlenfolge Xn(ω) konvergiert für fast alle ω (bis auf eine Nullmenge) gegen X(ω) (pfadweise Konvergenz). Dies ist die stärkste Form der Konvergenz.
    - **Konvergenz in Wahrscheinlichkeit (Xn i.W.→ X)**: P(|Xn - X| > ϵ) → 0 für n → ∞ für jedes ϵ > 0.
    - **Konvergenz in Verteilung (Xn i.V.→ X)**: Die Verteilungsfunktionen FXn(x) konvergieren gegen FX(x) an allen Stetigkeitspunkten von FX(x). Dies ist die schwächste Form der Konvergenz.
    - **Beziehungen**: Fast sichere Konvergenz impliziert Konvergenz in Wahrscheinlichkeit, die wiederum Konvergenz in Verteilung impliziert. Die Umkehrungen gelten im Allgemeinen nicht.

### 6. Bedingte Wahrscheinlichkeit und Unabhängigkeit

- **Bedingte Wahrscheinlichkeit**: P(A|B) = P(A ∩ B) / P(B) für P(B) > 0. Intuition: Reduktion des Stichprobenraums auf B.
- **Gesetz der totalen Wahrscheinlichkeit**: P(B) = ∑ P(B|Ai)P(Ai) für eine Partition A1, ..., An.
- **Satz von Bayes**: Aktualisiert Wahrscheinlichkeiten basierend auf neuen Informationen.
    - **Formel**: P(A|B) = [P(B|A) * P(A)] / P(B).
    - **Terminologie**: Posteriori-Wahrscheinlichkeit, Likelihood, Prior-Wahrscheinlichkeit, Evidenz.
    - **Anwendungen**: Medizinische Diagnose, Das Ziegenproblem.
- **Unabhängigkeit von Ereignissen**: A und B sind unabhängig, wenn P(A ∩ B) = P(A)P(B). Für eine Folge von Ereignissen (An, n∈N) bedeutet dies, dass P(∩ Aik) = ∏ P(Aik) für beliebige endliche Teilfolgen.
- **Unabhängigkeit von Zufallsvariablen (i.i.d.)**: Wichtig für Grenzwerte und Gesetze der großen Zahlen. Der **Klonsatz (4.5.1)** sichert die Existenz unabhängiger ZV mit vorgegebener Verteilung.

### 7. Einführung in die Statistik

- **Hypothesentest**:
    - **Nullhypothese (H0)**: Die Standardannahme, kein Unterschied oder Zusammenhang.
    - **Arbeitshypothese (H1)**: Die Behauptung, die wir stützen wollen.
- **Fishers exakter Test**: Testet, ob beobachtete Unterschiede in einer 2x2 Kontingenztafel (z.B. in klinischen Studien) signifikant oder zufällig sind.
    - **Kernidee**: Unter H0 sind die Randsummen fix und die Verteilung der Beobachtungen ist hypergeometrisch.
    - **P-Wert**: Die Wahrscheinlichkeit, das beobachtete Ergebnis (oder ein extremeres) unter Annahme der Nullhypothese zu sehen. Ein kleiner p-Wert (<0.05) führt zur Verwerfung von H0.
- **Schätzer**: Eine Funktion der Stichprobendaten, die verwendet wird, um einen unbekannten Populationsparameter zu approximieren (z.B. µ̂ für µ).
    - **Schätzwert**: Das Ergebnis der Anwendung des Schätzers auf eine konkrete Stichprobe.
    - **Güte von Schätzern**:
        - **Erwartungstreue (Unbiasedness)**: E[θ̂] = θ (der Schätzer liegt im Durchschnitt richtig).
        - **Effizienz (Efficiency)**: Kleinere Varianz (weniger Streuung um den wahren Wert).
        - **Konsistenz (Consistency)**: Konvergiert mit wachsender Stichprobengröße zum wahren Parameterwert.
- **Schätzer für den Erwartungswert (µ)**: Der **Stichprobenmittelwert X̄** ist ein erwartungstreuer Schätzer für µ.
- **Schätzer für die Varianz (σ²)**: Die **korrigierte Stichprobenvarianz S² = 1/(n-1) ∑(Xi - X̄)²** ist ein erwartungstreuer Schätzer für σ². Der Nenner (n-1) ist die **Bessel-Korrektur**.