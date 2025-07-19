## 1. Grundlagen der Wahrscheinlichkeitstheorie
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
TODO

"Die kleinste σ-Algebra, die alle offenen Intervalle enthält."



#### Wahrscheinlichkeitsmaß $\mathbb{P}$
ordnet jedem Ereignis in E eine Wahrscheinlichkeit zu.

Sei $\mathcal{E}$ eine $\sigma$-Algebra auf $\Omega$. Eine Abbildung $\mathbb{P}: \mathcal{E}\to [0,1]$ heißt Wahrscheinlichkeitsmaß, wenn:
1. $\mathbb{P}(\Omega)=1$, $\mathbb{P}(\emptyset)=0$
2. $\forall E_{i}, E_{j} \in \mathcal{E} \quad E_{i}\cap E_{j}=\emptyset, i\neq j \implies$$$
\mathbb{P}(E_{1}\cup E_{2}\cup\dots)=\mathbb{P}(E_{1})+\mathbb{P}(E_{2})+\dots
$$
z.B. fairer Würfel $\mathbb{P}(\{ 2 \})=\frac{1}{6}$ oder $\mathbb{P}(\{ 2,4 \})=\frac{1}{6}+\frac{1}{6}=\frac{1}{3}$


### Gleichverteilung / Laplaceraum
Wenn alle Ergebnisse in einer endlichen Ergebnismenge die gleiche Wahrscheinlichkeit haben. Bei $n$-fachem Münzwurf ist $\mathbb{P}_{n}(A) = \frac{\lvert A \rvert}{\lvert \Omega_{n} \rvert}$

### Kontinuierliche Wahrscheinlichkeitsräume
Ein **kontinuierlicher Wahrscheinlichkeitsraum** wird verwendet, wenn das Ergebnis eines Zufallsexperiments **nicht als einzelne Zahl, sondern als ein Punkt auf einer Zahlengeraden** (oder Fläche, Raum usw.) beschrieben wird.

#### Beispiel 1: Zufallszahl zwischen 0 und 1
wahl einer zufälligen Zahl zwischen 0 und 1, z. B. mit einem Dartwurf auf eine Skala von 0 bis 1.

- $\Omega=[0,1]$
- Die Wahrscheinlichkeitsverteilung ist **gleichmäßig**
- Die **Wahrscheinlichkeitsdichtefunktion** (PDF) ist:
  $$
   f(x) = \begin{cases}
   1, & \text{für } x \in [0,1] \\
   0, & \text{sonst}
   \end{cases}
   $$
- Die Wahrscheinlichkeit, dass $X$ in einem bestimmten Intervall liegt (z. B. zwischen 0,2 und 0,5), ist:
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
- Beispiel: Größe ~ $N(170, 10^2)$, Mittelwert 170 cm, Standardabweichung 10 cm
- zwischen 160 cm und 180 cm größe:
  $$
   P(160 \leq X \leq 180) = \int_{160}^{180} f(x)\,dx
   $$
