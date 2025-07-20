# Inhaltsverzeichnis  
- [Grundlagen der Wahrscheinlichkeitstheorie](#grundlagen-der-wahrscheinlichkeitstheorie)  
  - [Wahrscheinlichkeitsraum](#wahrscheinlichkeitsraum)  
      - [Ergebnismenge $\Omega$](#ergebnismenge-omega)  
      - [$\sigma$-Algebra $\mathcal{E}$](#sigma-algebra-mathcale)  
          - [Borelmenge](#borelmenge)  
      - [Wahrscheinlichkeitsmaß $\mathbb{P}$](#wahrscheinlichkeitsmaß-mathbbp)  
      - [Diskreter Wahrscheinlichkeitsraum](#diskreter-wahrscheinlichkeitsraum)  
          - [Def](#def)  
          - [Bsp](#bsp)  
  - [Gleichverteilung / Laplaceraum](#gleichverteilung--laplaceraum)  
  - [Kontinuierliche Wahrscheinlichkeitsräume](#kontinuierliche-wahrscheinlichkeitsräume)  
      - [Beispiel 1: Zufallszahl zwischen 0 und 1](#beispiel-1-zufallszahl-zwischen-0-und-1)  
      - [Beispiel 2: Normalverteilung (Glockenkurve)](#beispiel-2-normalverteilung-glockenkurve)  
  
- [Diskrete Wahrscheinlichkeitsverteilungen](#diskrete-wahrscheinlichkeitsverteilungen)  
  - [Bernoulli-Verteilung](#bernoulli-verteilung)  
      - [Taschenrechner](#taschenrechner)  
  - [Stetige Gleichverteilung](#stetige-gleichverteilung)  
  - [Poisson-Verteilung](#poisson-verteilung)  
      - [Taschenrechner](#taschenrechner-1)  
  - [Binomialverteilung](#binomialverteilung)  
      - [Taschenrechner](#taschenrechner-2)  
  - [Hypergeometrische Verteilung](#hypergeometrische-verteilung)  
  
- [Kontinuierliche Wahrscheinlichkeitsverteilungen](#kontinuierliche-wahrscheinlichkeitsverteilungen)  
  - [Gleichverteilung (kontinuierlich)](#gleichverteilung-kontinuierlich)  
  - [Exponentialverteilung](#exponentialverteilung)  
  - [Normalverteilung (Gauß-Verteilung)](#normalverteilung-gauß-verteilung)  
  
- [Zufallsvariablen, Erwartungswert und Varianz](#zufallsvariablen-erwartungswert-und-varianz)  
  - [Zufallsvariable (ZV)](#zufallsvariable-zv)  
  - [Verteilung einer ZV](#verteilung-einer-zv)  
  - [Erwartungswert $\mathbb{E}(X)$](#erwartungswert-mathbbex)  
      - [Definitionen](#definitionen)  
      - [Existenzbedingung](#existenzbedingung)  
  - [Varianz $\text{Var}(X)$](#varianz-textvarx)  
  - [Wichtige Ungleichungen](#wichtige-ungleichungen)  
      - [Tschebyscheff-Ungleichung](#tschebyscheff-ungleichung-satz-822)  
      - [Markov-Ungleichung](#markov-ungleichung-satz-823)  
  
- [Bedingte Wahrscheinlichkeit und Unabhängigkeit](#bedingte-wahrscheinlichkeit-und-unabhängigkeit)  
  - [Bedingte Wahrscheinlichkeit](#bedingte-wahrscheinlichkeit)  
  - [Gesetz der totalen Wahrscheinlichkeit](#gesetz-der-totalen-wahrscheinlichkeit)  
  - [Satz von Bayes (Bayes-Theorem)](#satz-von-bayes-bayes-theorem)  
      - [Begriffe](#begriffe)  
      - [Anwendungen](#anwendungen)  
  - [Unabhängigkeit von Ereignissen](#unabhängigkeit-von-ereignissen)  
  - [Unabhängigkeit von Zufallsvariablen](#unabhängigkeit-von-zufallsvariablen)  
  - [Klonsatz (Satz 4.5.1)](#klonsatz-satz-451)  
  
- [Einführung in die Statistik](#einführung-in-die-statistik)  
  - [Hypothesentest](#hypothesentest)  
  - [Fishers exakter Test](#fishers-exakter-test)  
  - [Schätzer](#schätzer)  
  - [Gütekriterien von Schätzern](#gütekriterien-von-schätzern)  
  - [Wichtige Schätzer](#wichtige-schätzer)  
  - [Zusatzbegriffe](#zusatzbegriffe)  
  
# Zusammenfassung Wahrscheinlichkeitstheorie und Statistik  
  
## Grundlagen der Wahrscheinlichkeitstheorie  
  
---  
  
### Wahrscheinlichkeitsraum  
  
Beschrieben mit $(\Omega, \mathcal{E}, \mathbb{P})$  
  
#### Ergebnismenge $\Omega$  
  
Die Menge aller möglichen Ergebinsse eines Zufallsexperiments.  
Bsp: $\Omega=\{ 0,1 \}$ für Münzwurf, $\Omega=\{ 1,2,3,4,5,6 \}$ für Würfelwurf  
  
#### $\sigma$-Algebra $\mathcal{E}$  
  
Eine Menge von Ereignissen $\mathcal{E}$ Teilmenge von $\Omega$, mit den Eigenschaften:  
  
1. $\Omega, \emptyset \in \mathcal{E}$  
2. $\forall E\in \mathcal{E}\implies (\Omega \setminus E)\in\mathcal{E}$  
3. $\forall E_{n}\in \mathcal{E} \implies \bigcup^{\infty}_{n=1}E_{n}\in\mathcal{E}$  
  
##### Borelmenge  
  
???  
  
#### Wahrscheinlichkeitsmaß $\mathbb{P}$  
  
ordnet jedem Ereignis in E eine Wahrscheinlichkeit zu.  
  
Sei $\mathcal{E}$ eine $\sigma$-Algebra auf $\Omega$. Eine Abbildung $\mathbb{P}: \mathcal{E}\to [0,1]$.  
Eigenschaften eines Wahrscheinlichkeitsmaßes $\mathbb{P}$:  
  
1. **Normiertheit:**  
  
   $$   \mathbb{P}(\Omega) = 1 \quad \text{und} \quad \mathbb{P}(\emptyset) = 0  
   $$  
  
2. **Additivität (σ-Additivität bei abzählbar unendlich vielen Mengen):**  
   Für paarweise disjunkte Ereignisse $E_1, E_2, E_3, \dots \in \mathcal{E}$ gilt:  
  
   $$  
   E_i \cap E_j = \emptyset \quad \text{für } i \neq j \quad \Rightarrow \quad \mathbb{P}\left( \bigcup_{k=1}^\infty E_k \right) = \sum_{k=1}^\infty \mathbb{P}(E_k)  
   $$  
  
   **Beispiel (fairer Würfel):**  
  
   $$   \mathbb{P}(\{2\}) = \frac{1}{6}, \quad \mathbb{P}(\{2, 4\}) = \mathbb{P}(\{2\}) + \mathbb{P}(\{4\}) = \frac{1}{6} + \frac{1}{6} = \frac{1}{3}  
   $$  
  
#### diskreter Wahrscheinlichkeitsraum  
  
Ein Wahrscheinlichkeitsraum $(\Omega, \mathcal{P}(\Omega), \mathbb{P})$ besteht aus drei Dingen:  
  
1. $\Omega\neq \emptyset$ (Menge der Elementarereignisse) aber ENDLICH oder ABZÄHLBAR UNENLICH  
2. $\sigma$-Algebra $\mathcal{P(\Omega)}$ (Potenzmenge von $\Omega$)  
3. Wahrscheinlichkeitsmaß $\mathbb{P}:\mathcal{P}(\Omega)\to[0,1]$  
  
##### Def  
  
$$  
\displaylines{  
\tilde{p}_{\omega} \geq 0, \quad 0 < \sum_{\omega \in \Omega} \tilde{p}_{\omega} < + \infty \\ \\  
  
\implies p_{\omega}:= \frac{\tilde{p}_{\omega}}{\sum_{\omega \in \Omega} \tilde{p}_{\omega}}  
}  
$$  
  
##### Bsp  
  
Sei $\Omega = \mathbb{N}$, und $\tilde{p}_{n}=\frac{1}{n^2}$. Dann gilt:  
  
- $\tilde{p}_{n}\geq0$  
- $\sum^{\infty}_{n=1} \frac{1}{n^2}= \frac{\pi^{2}}{6}<\infty$  
  
Also erfüllt $\tilde{p}_n$​ die Bedingung  
$$  
0 < \sum_{n=1}^{\infty} \tilde{p}_n < \infty  
$$  
  
Dann kann man $p_n := \frac{\tilde{p}_n}{\sum \tilde{p}_n}$ definieren und erhält eine gültige **diskrete  
Wahrscheinlichkeitsverteilung**.  
  
---  
  
### Gleichverteilung / Laplaceraum  
  
Wenn alle Ergebnisse in einer endlichen Ergebnismenge die gleiche Wahrscheinlichkeit haben. Bei $n$-fachem Münzwurf  
ist $\mathbb{P}_{n}(A) = \frac{\lvert A \rvert}{\lvert \Omega_{n} \rvert}$  
  
---  
  
### Kontinuierliche Wahrscheinlichkeitsräume  
  
Ein **kontinuierlicher Wahrscheinlichkeitsraum** wird verwendet, wenn das Ergebnis eines Zufallsexperiments **nicht als  
einzelne Zahl, sondern als ein Punkt auf einer Zahlengeraden** (oder Fläche, Raum usw.) beschrieben wird.  
  
#### Beispiel 1: Zufallszahl zwischen 0 und 1  
  
wahl einer zufälligen Zahl zwischen 0 und 1, z. B. mit einem Dartwurf auf eine Skala von 0 bis 1.  
  
- $\Omega=[0,1]$  
- Die Wahrscheinlichkeitsverteilung ist **gleichmäßig**  
- Die **Wahrscheinlichkeitsdichtefunktion** (PDF) ist:  
  $$  
  f(x) = \begin{cases}  
  1, & \text{für } x \in [0,1] \\  
  0, & \text{sonst}  
  \end{cases}  
  $$  
- Die Wahrscheinlichkeit, dass $X$ in einem bestimmten Intervall liegt (z. B. zwischen 0,2 und 0,5), ist:  
  $$  
  P(0{,}2 \leq X \leq 0{,}5) = \int_{0{,}2}^{0{,}5} f(x)\,dx = \int_{0{,}2}^{0{,}5} 1 \, dx = 0{,}3  
  $$  
  
#### Beispiel 2: Normalverteilung (Glockenkurve)  
  
Körpergröße von Menschen. Die Werte liegen auf einem Kontinuum und sind **normalverteilt**.  
  
- $\Omega=\mathbb{R}$  
- Die Wahrscheinlichkeitsdichtefunktion:  
  $$  
  f(x) = \frac{1}{\sigma \sqrt{2\pi}} \, e^{-\frac{(x - \mu)^2}{2\sigma^2}}  
  $$  
- Beispiel: Größe ~ $N(170, 10^2)$, Mittelwert 170 cm, Standardabweichung 10 cm  
- zwischen 160 cm und 180 cm größe:  
  $$  
  P(160 \leq X \leq 180) = \int_{160}^{180} f(x)\,dx  
  $$  
  
## Diskrete Wahrscheinlichkeitsverteilungen  
  
---  
  
### Bernoulli-Verteilung  
  
* Zwei Ausgänge (0 oder 1)  
* **Parameter:** $p \in [0,1]$ (Wahrscheinlichkeit für Erfolg)  
* **Verwendung:** Modellierung eines einzelnen Versuchs mit zwei möglichen Ausgängen (z. B. Münzwurf)  
* **Wahrscheinlichkeit:**  
  $$  P(X = 1) = p,\quad P(X = 0) = 1 - p  
  $$  
* **Erwartungswert:** $\mathbb{E}[X] = p$  
* **Varianz:** $\text{Var}(X) = p(1 - p)$  
  **Beispiel:** Kopf (1) oder Zahl (0) beim Münzwurf mit $p = 0{,}5$  
  
#### Taschenrechner  
  
Binomial PD – $\mathbb{P}(X=k)$  
Binomial CD – $\mathbb{P}(X\leq k)$  
  
- $x=k$  
- $n$ = Anzahl der Versuche  
- $p$ = Trefferwahrscheinlichkeit  
  
---  
  
### Stetige Gleichverteilung  
  
Gleichverteilungen über Intervall  
  
* **Form:** Konstante Dichte auf \[a, b]  
* **Parameter:** $a, b \in \mathbb{R},\ a < b$  
* **Dichtefunktion:**  
  $$  f(x) = \frac{1}{b - a},\quad x \in [a, b]  
  $$  
  Beispiel $a=2,b=5\quad f(x)= \frac{1}{5-2}=\frac{1}{3}$ für $x \in [2,5]$  
  
---  
  
### Poisson-Verteilung  
  
* **Form:** Rechtssteilig, für kleine $\lambda$ stark rechtsschief  
* **Parameter:** $\lambda \geq 0$ (mittlere Ereignisrate)  
* **Verwendung:** Anzahl von Ereignissen in einem festen Intervall bei konstanter Rate  
* **Wahrscheinlichkeit:**  
  
$$  
P(X = k) = \frac{\lambda^k}{k!} e^{-\lambda},\quad k \in \mathbb{N}_0  
$$  
  
* **Erwartungswert:** $\mathbb{E}[X] = \lambda$  
* **Varianz:** $\text{Var}(X) = \lambda$  
  **Beispiel:** Anzahl Anrufe pro Stunde in einem Callcenter  
  
#### Taschenrechner  
  
Poisson PD – $\mathbb{P}(X=k)$  
Poisson CD – $\mathbb{P}(X\leq k)$  
  
- $x=k$  
- $\mu$ = $\lambda$ = Erwartungswert/Mittelwert  
  
---  
  
### Binomialverteilung  
  
* **Parameter:** $n \in \mathbb{N},\ p \in [0,1]$  
* **Verwendung:** Anzahl Erfolge in $n$ unabhängigen Bernoulli-Versuchen  
* **Wahrscheinlichkeit:**  
  $$  P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}  
  $$  
* **Erwartungswert:** $\mathbb{E}[X] = np$  
* **Varianz:** $\text{Var}(X) = np(1 - p)$  
  **Beispiel:** Anzahl richtiger Antworten bei Zufallsraten in einem Multiple-Choice-Test  
  
#### Taschenrechner  
  
Poisson PD – $\mathbb{P}(X=k)$  
Poisson CD – $\mathbb{P}(X\leq k)$  
  
- $x=k$  
- $N$ = Versuche  
- $p$ = Trefferwahrscheinlichkeit  
  
---  
  
### Hypergeometrische Verteilung  
  
* **Form:** Abhängig von Ziehung ohne Zurücklegen  
* **Parameter:**  
    * $N$: Gesamtanzahl  
    * $K$: Anzahl Erfolge in Population  
    * $n$: Stichprobengröße  
* **Verwendung:** Wahrscheinlichkeiten ohne Zurücklegen, z. B. bei Qualitätskontrolle oder Kartenspielen  
* **Wahrscheinlichkeit:**  
  $$  P(X = k) = \frac{\binom{K}{k} \binom{N - K}{n - k}}{\binom{N}{n}}  
  $$  
  **Beispiel:** Wahrscheinlichkeit von 2 roten Karten beim Ziehen von 5 Karten aus einem Deck mit 26 roten Karten  
  
## Kontinuierliche Wahrscheinlichkeitsverteilungen  
  
---  
  
### Gleichverteilung (kontinuierlich)  
  
**Definition:** Jeder Wert im Intervall \[a, b] ist gleich wahrscheinlich.  
**Parameter:** $a < b$  
  
* **PDF (Wahrscheinlichkeitsdichte):**  $$  
  f(x) = \begin{cases}  
  \frac{1}{b - a} & \text{für } x \in [a, b] \\  
  0 & \text{sonst}  
  \end{cases}  
  $$  
* **CDF (Verteilungsfunktion):**  
  
  $$  F(x) = \begin{cases}  
  0 & \text{für } x < a \\  
  \frac{x - a}{b - a} & \text{für } x \in [a, b] \\  
  1 & \text{für } x > b  
  \end{cases}  
  $$  
  
---  
  
### Exponentialverteilung  
  
**Definition:** Modelliert Wartezeiten bis zum nächsten Ereignis in einem Poisson-Prozess.  
**Parameter:** $\lambda > 0$  
**Definiert auf:** $[0, \infty)$  
  
* **PDF:**  
  $$  f(x) = \begin{cases}  
  \lambda e^{-\lambda x} & \text{für } x \geq 0 \\  
  0 & \text{sonst}  
  \end{cases}  
  $$  
  
* **CDF:**  
  
  $$  F(x) = \begin{cases}  
  1 - e^{-\lambda x} & \text{für } x \geq 0 \\  
  0 & \text{sonst}  
  \end{cases}  
  $$  
  
* **Erwartungswert:** $\mathbb{E}[X] = \frac{1}{\lambda}$  
* **Varianz:** $\text{Var}(X) = \frac{1}{\lambda^2}$  
  
---  
  
### Normalverteilung (Gauß-Verteilung)  
  
**Definition:** Die zentrale Verteilung in Statistik und Wahrscheinlichkeit.  
**Parameter:**  
  
* $\mu$ (Mittelwert)  
* $\sigma^2$ (Varianz)  
* **PDF:**  $$  
  f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)  
  $$  
  
* **CDF:** Keine geschlossene Form; wird numerisch berechnet oder über Standardnormalverteilung (z-Werte) tabelliert.  
  
* **Standardnormalverteilung:**  
  Spezialfall mit $\mu = 0$, $\sigma^2 = 1$  
  
## Zufallsvariablen, Erwartungswert und Varianz  
  
---  
  
### Zufallsvariable (ZV)  
  
Eine **Funktion**, die jedem Ergebnis eines Zufallsexperiments einen **numerischen Wert** zuordnet:  
$$  
X: \Omega \rightarrow \mathbb{R}  
$$  
  
---  
  
### Verteilung einer ZV  
  
Bezeichnet das **induzierte Wahrscheinlichkeitsmaß** auf $\mathbb{R}$, abgeleitet aus dem zugrunde liegenden Maßraum.  
$$  
P_X(B) = P(X^{-1}(B)) \quad \text{für } B \subseteq \mathbb{R}  
$$  
  
---  
  
### Erwartungswert $\mathbb{E}(X)$  
  
Beschreibt den **mittleren Wert** einer Zufallsvariablen bei vielen Wiederholungen.  
  
#### Definitionen:  
  
* **Diskrete ZV:**  
  $$  \mathbb{E}(X) = \sum_{c \in \mathcal{C}} c \cdot P(X = c)  
  $$  
* **Stetige ZV mit Dichte $f(x)$:**  
  $$  \mathbb{E}(X) = \int_{\Omega} X(x) f(x)\,dx  
  $$  
  
#### Existenzbedingung:  
  
$$  
\text{Erwartungswert existiert } \Leftrightarrow \sum |c| P(X = c) \text{ bzw. } \int |X(x)|f(x) dx < \infty  
$$  
  
---  
  
### Varianz $\text{Var}(X)$  
  
Misst die **Streuung** der Werte von $X$ um den Erwartungswert.  
$$  
\text{Var}(X) = \mathbb{E}[(X - \mathbb{E}(X))^2] = \mathbb{E}(X^2) - (\mathbb{E}(X))^2  
$$  
  
* **Interpretation:** Kleine Varianz → Werte liegen nah bei $\mathbb{E}(X)$  
* **Beziehung zur Existenz:**  
  
  $$  \text{Var}(X) < \infty \Rightarrow \mathbb{E}(X) < \infty, \quad \text{aber nicht umgekehrt}  
  $$  
  
---  
  
### Wichtige Ungleichungen  
  
#### Tschebyscheff-Ungleichung (Satz 8.2.2):  
  
Für eine ZV $X$ mit endlichem Erwartungswert $\mu$ und Varianz $\sigma^2$:  
$$  
P(|X - \mu| \geq \epsilon) \leq \frac{\sigma^2}{\epsilon^2} \quad \text{für alle } \epsilon > 0  
$$  
  
Nützlich zur **Abschätzung der Ausreißerwahrscheinlichkeit**.  
  
#### Markov-Ungleichung (Satz 8.2.3):  
  
Für nichtnegative ZV $X \geq 0$ mit $\mathbb{E}(X) < \infty$:  
$$  
P(X \geq a) \leq \frac{\mathbb{E}(X)}{a} \quad \text{für alle } a > 0  
$$  
  
Allgemeiner als Tschebyscheff, benötigt nur Nichtnegativität.  
  
## Bedingte Wahrscheinlichkeit und Unabhängigkeit  
  
---  
  
### Bedingte Wahrscheinlichkeit  
  
**Definition:**  
  
$$  
P(A \mid B) = \frac{P(A \cap B)}{P(B)} \quad \text{für } P(B) > 0  
$$  
  
**Intuition:**  
Der Stichprobenraum wird auf $B$ eingeschränkt ("B ist bekannt").  
  
---  
  
### Gesetz der totalen Wahrscheinlichkeit  
  
Wenn $A_1, ..., A_n$ eine **Partition** des Ereignisraums ist (d.h. paarweise disjunkt und $\bigcup A_i = \Omega$), dann  
gilt:  
  
$$  
P(B) = \sum_{i=1}^n P(B \mid A_i) \cdot P(A_i)  
$$  
  
Anwendung: Wenn die Wahrscheinlichkeiten $P(B \mid A_i)$ bekannt sind, aber $P(B)$ unbekannt.  
  
---  
  
### Satz von Bayes (Bayes-Theorem)  
  
**Formel:**  
$$  
P(A \mid B) = \frac{P(B \mid A) \cdot P(A)}{P(B)} \quad \text{für } P(B) > 0  
$$  
  
#### **Begriffe:**  
  
* **Prior:** $P(A)$ — ursprüngliche Einschätzung der Wahrscheinlichkeit von $A$  
* **Likelihood:** $P(B \mid A)$ — Wahrscheinlichkeit der Beobachtung $B$ gegeben $A$  
* **Evidenz:** $P(B)$ — Gesamtwahrscheinlichkeit des beobachteten Ereignisses  
* **Posterior:** $P(A \mid B)$ — aktualisierte Wahrscheinlichkeit von $A$ nach Beobachtung von $B$  
  
#### Anwendungen:  
  
* Medizinische Tests  
* Maschinelles Lernen  
* **Ziegenproblem** (Monty Hall)  
  
---  
  
### Unabhängigkeit von Ereignissen  
  
**Zwei Ereignisse $A$ und $B$ sind unabhängig, wenn:**  
$$  
P(A \cap B) = P(A) \cdot P(B)  
$$  
  
**Für mehrere Ereignisse $A_1, ..., A_n$:**  
$$  
P\left( \bigcap_{k=1}^{n} A_{i_k} \right) = \prod_{k=1}^{n} P(A_{i_k}) \quad \text{für alle Teilmengen}  
$$  
  
---  
  
### Unabhängigkeit von Zufallsvariablen  
  
**Definition:** ZV $X, Y$ sind unabhängig, wenn für alle messbaren Mengen $A, B$:  
$$  
P(X \in A, Y \in B) = P(X \in A) \cdot P(Y \in B)  
$$  
  
**i.i.d. = unabhängig und identisch verteilt**  
  
Wichtige Voraussetzung für:  
  
* **Gesetz der großen Zahlen**  
* **Zentraler Grenzwertsatz**  
  
---  
  
### Klonsatz (Satz 4.5.1)  
  
**Aussage:** Es existieren **unabhängige Zufallsvariablen**, die alle **dieselbe Verteilung** haben wie eine gegebene  
Zufallsvariable.  
  
## Einführung in die Statistik  
  
---  
  
### Hypothesentest  
  
* **Nullhypothese $H_0$:**  
  "Status quo" – es gibt **keinen Unterschied** oder Effekt.  
  Beispiel: Kein Zusammenhang zwischen Behandlung und Heilung.  
  
* **Alternativhypothese $H_1$:**  
  Das, was man **zeigen möchte** – z. B. ein Unterschied oder Zusammenhang.  
  
---  
  
### Fishers exakter Test  
  
**Anwendung:**  
2×2-Kontingenztafeln, z. B. in klinischen Studien (Behandlung vs. Kontrolle).  
**Voraussetzung:** Kleine Stichproben, fixe Randsummen.  
  
* **Kernidee:**  
  Unter $H_0$ folgt die Zellenbesetzung einer **hypergeometrischen Verteilung**.  
  
* **P-Wert:**  
  $$  p = P(\text{Beobachtung oder extremer} \mid H_0)  
  $$  
  
  → Gibt die Wahrscheinlichkeit an, dass ein so (oder noch) extremeres Ergebnis unter $H_0$ auftritt.  
  
  **Wenn** $p < \alpha$ (z. B. 0,05), **dann verwerfe $H_0$**.  
  
---  
  
### Schätzer  
  
Ein **Schätzer $\hat{\theta}$** ist eine Funktion der Stichprobendaten zur **Approximation eines unbekannten  
Populationsparameters** $\theta$.  
  
* **Schätzwert:**  
  Der konkrete Wert, den man für eine Stichprobe erhält.  
  
---  
  
### Gütekriterien von Schätzern  
  
| Kriterium           | Bedeutung                                                                  |  
|---------------------|----------------------------------------------------------------------------|  
| **Erwartungstreue** | $\mathbb{E}[\hat{\theta}] = \theta$ – Im Mittel korrekt.                   |  
| **Effizienz**       | Geringe Varianz unter allen erwartungstreuen Schätzern.                    |  
| **Konsistenz**      | $\hat{\theta}_n \to \theta$ für $n \to \infty$ (stochastische Konvergenz). |  
  
---  
  
### Wichtige Schätzer  
  
* **Für den Erwartungswert $\mu$:**  
  $$  \bar{X} = \frac{1}{n} \sum_{i=1}^n X_i  
  $$  
  
  → Erwartungstreuer Schätzer für $\mu$  
  
* **Für die Varianz $\sigma^2$:**  
  $$  S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i - \bar{X})^2  
  $$  
  
  → Erwartungstreu durch **Bessel-Korrektur** (statt $n$, wird $n-1$ verwendet)  
  
---  
  
### Zusatzbegriffe  
  
* **Signifikanzniveau $\alpha$:**  
  Grenze für den p-Wert, z. B. 0,05 → 5 % Irrtumswahrscheinlichkeit bei Ablehnung von $H_0$  
  
* **Teststärke (Power):**  
  Wahrscheinlichkeit, dass ein Test $H_0$ **korrekt verwirft**, wenn $H_1$ stimmt