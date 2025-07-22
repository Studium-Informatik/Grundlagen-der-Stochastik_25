# 1
## 1
Für $A \subseteq \Omega$:
$$
\mathbb{P}(A)=\sum^{\omega}_{\omega \in A} \mathbb{P}(\{ \omega \})
$$

$n$-facher Münzwurf:
$\Omega_{n}=\{ 0,1 \}^n$. mit $A \subseteq \Omega_{n}$
$$
P_{n}(A)= \frac{\lvert A\rvert}{\lvert \Omega_{n} \rvert } 
$$

Gesetz der großen Zahlen:
informelle Beschreibung: bei n-maligem Münzwurf im Schnitt die Hälfte der Würfe KOPF und die andere Hälfte ZAHL ergibt

Normalverteilung von Gauß:
$$
f(x)=\frac{1}{\sigma \sqrt{ 2\pi }}e^{\frac{-(x-\mu)^2}{2\sigma^2}}
$$

## 2
### $\sigma$ Algebra
Ein Mengensystem $\mathcal{E}$ auf der Menge $\Omega$ heißt $\sigma$-Algebra, wenn:
1. $\Omega, \emptyset \in \mathcal{E}$ 
2. $\forall E\in \mathcal{E}\implies (\Omega \setminus E)\in\mathcal{E}$
3. $\forall E_{n}\in \mathcal{E} \implies \bigcup^{\infty}_{n=1}E_{n}\in\mathcal{E}$

z.B. Würfel $\Omega=\{ 1,2,3,4,5,6 \}$

### Wahrscheinlichkeitsraum
Ein Wahrscheinlichkeitsraum $(\Omega, \mathcal{E}, \mathbb{P})$ besteht aus drei Dingen: 
1. $\Omega\neq \emptyset$ (Menge der Elementarereignisse)
2. $\sigma$-Algebra $\mathcal{E}$ auf $\Omega$
3. Wahrscheinlichkeitsmaß $\mathbb{P}:\mathcal{E}\to[0,1]$


z.B. Kombinationen der Würfelergebnisse $\mathcal{E}=\{ \emptyset, \{ 1 \}, \{ 2,4 \}, \{ 1,2,3,4,5,6 \},\dots \}$

### Wahrscheinlichkeitsmaß
Sei $\mathcal{E}$ eine $\sigma$-Algebra auf $\Omega$. Eine Abbildung $\mathbb{P}: \mathcal{E}\to [0,1]$ heißt Wahrscheinlichkeitsmaß, wenn:
1. $\mathbb{P}(\Omega)=1$
2. $\forall E_{i}, E_{j} \in \mathcal{E}. E_{i}\cap E_{j}=\emptyset, i\neq j \implies$
   $$
\mathbb{P}(E_{1}\cup E_{2}\cup\dots)=\mathbb{P}(E_{1})+\mathbb{P}(E_{2})+\dots
$$

z.B. fairer Würfel $\mathbb{P}(\{ 2 \})=\frac{1}{6}$ oder $\mathbb{P}(\{ 2,4 \})=\frac{1}{6}+\frac{1}{6}=\frac{1}{3}$

# 2
## 1
Satz 1.3.2. Sei $(Q, \mathcal{E}, P)$ ein Wahrscheinlichkeitsraum. Dann gilt:
$\mathbb{P}(\emptyset) = 0$.
$E \cap F = \emptyset \implies \mathbb{P}(E \cup F) = \mathbb{P}(E) + \mathbb{P}(F)$.

Seien $E, F$ Ereignisse:
$E \subseteq F \implies \mathbb{P}(E) < \mathbb{P}(F)$.
$\mathbb{P}(E \cup F) = \mathbb{P}(E) + \mathbb{P}(F) - \mathbb{P}(E\cap F)$. Insbesondere ist $\mathbb{P}(E\cup F) < \mathbb{P}(E) + \mathbb{P}(F)$. 

$$
\mathbb{P}\left(\bigcup^{\infty}_{n=1}E_{n}\right)\leq \sum^{\infty}_{n=1}\mathbb{P}(E_{n})
$$

## 3 <mark style="background: #FF5582A6;">Borelmengen</mark>
### Eigenschaften
- Jede offene Menge ist eine Borelsche Menge.
- Jede abgeschlossene Menge ist ebenfalls eine Borelsche Menge.
- Borelmengen sind abgeschlossen unter:
    - abzählbaren Vereinigungen
    - abzählbaren Durchschnitten
    - Komplementbildung

# 3
## 1 diskreter Wahrscheinlichkeitsraum
Ein Wahrscheinlichkeitsraum $(\Omega, \mathcal{P}(\Omega), \mathbb{P})$ besteht aus drei Dingen: 
1. $\Omega\neq \emptyset$ (Menge der Elementarereignisse) aber ENDLICH oder ABZÄHLBAR UNENLICH
2. $\sigma$-Algebra $\mathcal{P(\Omega)}$ (Potenzmenge von $\Omega$)
3. Wahrscheinlichkeitsmaß $\mathbb{P}:\mathcal{P}(\Omega)\to[0,1]$

### Def
$$
\displaylines{
\tilde{p}_{\omega} \geq 0, \quad 0 < \sum_{\omega \in \Omega} \tilde{p}_{\omega} < + \infty \\ \\

\implies p_{\omega}:= \frac{\tilde{p}_{\omega}}{\sum_{\omega \in \Omega} \tilde{p}_{\omega}}
}
$$

### Bsp
Sei $\Omega = \mathbb{N}$, und $\tilde{p}_{n}=\frac{1}{n^2}$. Dann gilt:
- $\tilde{p}_{n}\geq0$
- $\sum^{\infty}_{n=1} \frac{1}{n^2}= \frac{\pi^{2}}{6}<\infty$

Also erfüllt $\tilde{p}_n$​ die Bedingung
$$
0 < \sum_{n=1}^{\infty} \tilde{p}_n < \infty
$$

Dann kann man $p_n := \frac{\tilde{p}_n}{\sum \tilde{p}_n}$ definieren und erhält eine gültige **diskrete Wahrscheinlichkeitsverteilung**.

# Verteilungen
## Bernoulli-Verteilung

* **Typ:** Diskret
* **Form:** Zwei Ausgänge (0 oder 1)
* **Parameter:** $p \in [0,1]$ (Wahrscheinlichkeit für Erfolg)
* **Verwendung:** Modellierung eines einzelnen Versuchs mit zwei möglichen Ausgängen (z. B. Münzwurf)
* **Wahrscheinlichkeit:**

$$
P(X = 1) = p,\quad P(X = 0) = 1 - p
$$

* **Erwartungswert:** $\mathbb{E}[X] = p$
* **Varianz:** $\text{Var}(X) = p(1 - p)$
**Beispiel:** Kopf (1) oder Zahl (0) beim Münzwurf mit $p = 0{,}5$

## Gleichverteilung

### Diskrete Gleichverteilung

* **Typ:** Diskret
* **Form:** Alle Ausgänge gleich wahrscheinlich
* **Parameter:** $n$ (Anzahl möglicher Ausgänge)
* **Verwendung:** Modellierung fairer Zufallsprozesse (z. B. Würfeln)
* **Wahrscheinlichkeit:**

$$
P(X = k) = \frac{1}{n},\quad k \in \{1, \dots, n\}
$$

* **Erwartungswert:** $\mathbb{E}[X] = \frac{n + 1}{2}$
* **Varianz:** $\text{Var}(X) = \frac{n^2 - 1}{12}$
**Beispiel:** Ergebnis eines fairen Würfels (1–6)

### Stetige Gleichverteilung

* **Typ:** Stetig
* **Form:** Konstante Dichte auf \[a, b]
* **Parameter:** $a, b \in \mathbb{R},\ a < b$
* **Verwendung:** Modellierung von Gleichverteilungen über Intervalle
* **Dichtefunktion:**

$$
f(x) = \frac{1}{b - a},\quad x \in [a, b]
$$

**Beispiel:** Gleichverteilung auf $[0, 1/n]$, konvergiert gegen Dirac-Maß bei 0

## Geometrische Verteilung

* **Typ:** Diskret
* **Form:** Abnehmende Wahrscheinlichkeiten
* **Parameter:** $q = 1 - p \in [0,1)$
* **Verwendung:** Anzahl der Versuche bis zum ersten Erfolg
* **Wahrscheinlichkeit:**

$$
P(X = k) = q^{k-1}(1 - q),\quad k \in \mathbb{N}
$$

* **Erwartungswert:** $\frac{1}{1 - q}$
* **Varianz:** $\frac{q}{(1 - q)^2}$
**Beispiel:** Erste 6 beim Würfeln ($q = \frac{5}{6}$)

## Poisson-Verteilung
* **Typ:** Diskret
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

## Exponentialverteilung

* **Typ:** Stetig
* **Form:** Abnehmend, Gedächtnislosigkeit
* **Parameter:** $\lambda > 0$ (Rate)
* **Verwendung:** Zeit bis zum nächsten Ereignis bei Poisson-Prozess
* **Dichtefunktion:**

$$
f(x) = \lambda e^{-\lambda x},\quad x \geq 0
$$

* **Verteilungsfunktion:**

$$
F(x) = 1 - e^{-\lambda x}
$$

* **Erwartungswert:** $\mathbb{E}[X] = \frac{1}{\lambda}$
* **Varianz:** $\text{Var}(X) = \frac{1}{\lambda^2}$
**Beispiel:** Zeit bis zum nächsten Kunden in einer Warteschlange

## Normalverteilung

* **Typ:** Stetig
* **Form:** Glockenkurve, symmetrisch
* **Parameter:** $\mu \in \mathbb{R}, \sigma^2 > 0$
* **Verwendung:** Häufige Modellverteilung in Statistik und Naturwissenschaften
* **Dichtefunktion:**

$$
f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} \, e^{-\frac{(x - \mu)^2}{2\sigma^2}}
$$

* **Erwartungswert:** $\mathbb{E}[X] = \mu$
* **Varianz:** $\text{Var}(X) = \sigma^2$
**Beispiel:** Körpergrößen, Messfehler

## Binomialverteilung

* **Typ:** Diskret
* **Form:** Symmetrisch bei $p = 0{,}5$, sonst schief
* **Parameter:** $n \in \mathbb{N},\ p \in [0,1]$
* **Verwendung:** Anzahl Erfolge in $n$ unabhängigen Bernoulli-Versuchen
* **Wahrscheinlichkeit:**

$$
P(X = k) = \binom{n}{k} p^k (1 - p)^{n - k}
$$

* **Erwartungswert:** $\mathbb{E}[X] = np$
* **Varianz:** $\text{Var}(X) = np(1 - p)$
**Beispiel:** Anzahl richtiger Antworten bei Zufallsraten in einem Multiple-Choice-Test

## Dirac-Verteilung (Punktmasse)

* **Typ:** Stetig (aber "singulär")
* **Form:** Punktmasse auf einem Wert
* **Parameter:** $x_0 \in \mathbb{R}$ (Ort der Masse)
* **Verwendung:** Grenzverteilung, theoretisches Modell
* **Dichte (formal):**

  $$
  \delta_{x_0}(x) = \begin{cases}
  \infty & \text{für } x = x_0 \\
  0 & \text{sonst}
  \end{cases},\quad \text{mit } \int_{-\infty}^{\infty} \delta_{x_0}(x)\,dx = 1
  $$

**Beispiel:** Grenzverteilung von $X_n \sim U(0, 1/n)$ konvergiert gegen $\delta_0$

## Hypergeometrische Verteilung

* **Typ:** Diskret
* **Form:** Abhängig von Ziehung ohne Zurücklegen
* **Parameter:**

  * $N$: Gesamtanzahl
  * $K$: Anzahl Erfolge in Population
  * $n$: Stichprobengröße
* **Verwendung:** Wahrscheinlichkeiten ohne Zurücklegen, z. B. bei Qualitätskontrolle oder Kartenspielen
* **Wahrscheinlichkeit:**

  $$
  P(X = k) = \frac{\binom{K}{k} \binom{N - K}{n - k}}{\binom{N}{n}}
  $$

**Beispiel:** Wahrscheinlichkeit von 2 roten Karten beim Ziehen von 5 Karten aus einem Deck mit 26 roten Karten