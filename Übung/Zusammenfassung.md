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

## 2
