```{math}
    \newcommand \sh {\textrm{sh}}
    \newcommand \ch {\textrm{ch}}
    \renewcommand \th {\textrm{th}}
    \newcommand \R {\mathbb{R}}
    \newcommand \C {\mathbb{C}}
    \newcommand \K {\mathbb{K}}
    \newcommand \Q {\mathbb{Q}}
    \newcommand \N {\mathbb{N}}
    \newcommand \Z {\mathbb{Z}}
    \newcommand \M {\mathcal{M}}
    \renewcommand \L {\mathcal{L}}
    \newcommand \B {\mathcal{B}}
    \newcommand \Vect {\textrm{Vect}}
    \renewcommand \S {\mathcal{S}}
    \renewcommand \P {\mathcal{P}}
```

# Fractions rationnelles

Un résultat important : si $P$ est à racines simples (notons les $(x_i)$), $Q \land P = 1$ et $deg(Q) < deg(P)$, alors
\begin{equation*}
\frac{Q}{P} = \sum_{x_k} \frac{Q(x_k)}{P'(x_k)}\frac{1}{X-x_k}
\end{equation*}

```{exercise}
:label: exo-310
Décomposer en éléments simples les fractions rationnelles suivantes.

1. $F_1=\frac{1}{X^n-1}$ dans $\C[X]$
1. $F_2 = \frac{n!}{(X-1)(X-2)\ldots(X-n)}$ dans $\R[X]$.
1. $F_3 = \frac{1}{X^{2n}+1}$ dans $\C[X]$ puis $\R[X]$
1. $F_4 = \frac{X+1}{X^8(X+2)}$
1. $F_5 = \frac{X^2}{(X^2-1)^2}$

```

```{solution} exo-310
:class: dropdown

1. Notons $w_1, \ldots, w_n$ les racines $n$-ième de l'unité. On a donc $ F_1 = \sum \frac{a_k}{X-w_k} $. On écrit
\begin{align*}
a_k &= \frac{1}{\prod_{i \neq k} (w_k - w_i)}\\
&= \frac{1}{w_k^{n-1}}  \frac{1}{\prod_{i \neq k} (1 - w_i/w_k)}\\
&= w_k^{1-n} \left ( \prod_{w_i \neq 1} (1 - w_i) \right ) ^{-1}\\
&= w_k^{1-n}n^{-1}\\
&= \frac{w_k}{n}
\end{align*}
D'où
\begin{equation*}
 F_1 = \frac{1}{n} \sum \frac{w_k}{X-w_k}
\end{equation*}

2. On a donc $F_2 = \sum_{k=1}^n \frac{a_k}{X-k}$
Et on évalue :
\begin{align*}
a_k &= \frac{n!}{(k-1)!\times (-1)^{n-k}(n-k)!} \\
&= (-1)^{n-k} n {n-1 \choose k-1}
\end{align*}
d'où
\begin{equation*}
 F_2 = n (-1)^n \sum_{k=1}^n (-1)^k\frac{{n-1 \choose k-1}}{X-k}
\end{equation*}
3. Notons $w = e^{\frac{i\pi}{2n}}$, un pôle de $F_3$. Notons $w_0, \ldots, w_{2n-1}$ les racines $2n$-ièmes de l'unité. Il vients que les $\nu_k = ww_k = e^{i\pi \frac{2k+1}{2n}}$ sont les pôles de $F_3$ dans $\C$, puis
\begin{equation*}
 F_3 = -\frac{1}{2n}\sum_{k=0}^{2n-1} \frac{\nu_k}{X-\nu_k}
\end{equation*}
est la DES dans $\C$ de $F_3$. Puis en associant $\nu_{k}$ et $\nu_{2n-1-k}$ on trouve la DES dans $\R$ : $F_3 = \frac{1}{2n} \sum_{k=1}^n \frac{a_kX+b_k}{X^2-2\cos{\frac{2k+1}{2n}\pi}+1}$ où
$ a_kX + b_k = (X-\nu_k)\nu_{2n-1-k} + (X-\nu_{2n-1-k})\nu_k
$ d'où $a_k = 2\cos{\frac{2k+1}{2n}\pi}$ et $b_k = -2$ soit
\begin{equation*}
F_3 = \frac{1}{n} \sum_{k=1}^n \frac{-\cos{\frac{2k+1}{2n}\pi}X+1}{X^2-2\cos{\frac{2k+1}{2n}\pi}+1}
\end{equation*}
4. On effectue un DL en $0$ de $\frac{x+1}{x+2}$ :
\begin{align*}
\frac{x+1}{x+2} &\underset{0}{=} \frac{1}{2}(x+1)(\sum_{k=0}^8 (-1)^k(\frac{x}{2})^k + o(x^8)) \\
&\underset{0}{=} \frac{1}{2} - \sum_{k=1}^8(-1)^k(\frac{x}{2})^k \\
\end{align*}
On en déduit un $DL$ de $F_4$ puis on identifie les termes de la DES et du DL.
5. On écrit
\begin{equation*}
 F_5 = \frac{a}{X-1}+\frac{b}{(X-1)^2}+\frac{c}{X+1}+\frac{d}{(X+1)^2}
\end{equation*}
Mais $F_5$ est paire, cela amène en remplaçant $X$ par $-X$ :
\begin{equation*}
\begin{cases}
a &= -c \\
b &= d
\end{cases}
\end{equation*}
On évalue en $0$ pour obtenir l'équation supplémentaire $a=b$, puis en $1$ pour obtenir $b=\frac{1}{4}$. Cela fournit la DES.

```


```{exercise}
:label: exo-311
Calculer la dérivée $n$-ième de
\begin{equation*}
 F = \frac{1}{X^2+1}
\end{equation*}
```

```{solution} exo-311
:class: dropdown
On décompose
\begin{equation*}
 F = \frac{-i}{2(X-i)} + \frac{i}{2(X+i)}
\end{equation*}
Puis la dérivé $n$-ième de $\frac{1}{X+a}$ est $\frac{(-1)^nn!}{(X+a)^{n+1}}$. De là
\begin{align*}
F^{(n)} &= \frac{in!}{2}(-1)^{n}\left (\frac{1}{(X+i)^{n+1}} - \frac{1}{(X-i)^{n+1}} \right )
\end{align*}
On peut simplifier en remarquant que les coefficient de cette dérivée doivent être réels, et donc on peut prendre la partie imaginaire du gros machin.
```


```{exercise}
:label: exo-312
Soit $P,Q$ non nuls, premiers entre eux. Montrer que $F=\frac{P}{Q}$ est paire si et seulement si $P$ et $Q$ sont pairs. Établir un résultat équivalent pour $F$ impaire.
```

```{solution} exo-312
:class: dropdown
$P$ divise $P(X)Q(-X)=P(-X)Q(X)$ donc par Gauss divise $P(-X)$. De même $P(-X)$ divise $Q(X)$. Ainsi $P(X)=\lambda P(-X)$. L'analyse des coefficients amène $\lambda = (-1)^{n}$. Pareil pour $Q$. Ainsi $P$ et $Q$ sont tous deux pairs ou tous deux impairs. Le cas impair est exclu car alors $0$ est racine à la fois de $P$ et $Q$.

Le résultat à établir ensuite est $F$ impaire si et seulement si $P$ pair, $Q$ impair, ou bien $P$ impair, $Q$ pair.
```


```{exercise}
:label: exo-313
Soit $x_1,, \ldots, x_n$ des complexes distincts et 
\begin{equation*}
P = \prod_{i=1}^n (X-x_i)
\end{equation*}
Calculer
\begin{equation*}
 S=\sum_{i=1}^n \frac{P''(x_i)}{P'(x_i)}
\end{equation*}
```

```{solution} exo-313
:class: dropdown
On regarde la fraction rationnelle $F = \frac{P''}{P}$. Sa DES est donnée par
\begin{equation*}
 F = \sum_{i=1}^n \frac{P''(x_k)}{P'(x_k)}\frac{1}{X-x_k}
\end{equation*}
De là $xF(x) \underset{x \rightarrow +\infty}{\longrightarrow} S$. Or $XP''(X)$ est de degré strictement inférieur à celui de $P$ donc $XF \underset{+\infty}{\longrightarrow} 0$. De là $S=0$.
```

```{exercise}
:label: exo-314
Soit $P \in \R[X]$ unitaire de degré $n$, et $Q = \prod_{k=0}^n (X-k)$. Calculer $S = \sum_{k=0}^n \frac{P(k)}{\prod_{i \neq k}(k-i)}$ et en déduire l'existence d'un $k \in [\![0,n]\!] $ tel que $|P(k)| \geq \frac{n!}{2^n}$.
```

```{solution} exo-314
:class: dropdown
DES de $\frac{P}{Q}$ pour en déduire $S = \underset{x\rightarrow +\infty}{\lim}\frac{xP}{Q} = 1$. Puis si aucun $k$ ne vérifie l'inégalité, $S < \frac{1}{2^n}\sum \frac{n!}{k!(n-k)!} = 1$.
```


```{exercise} théorème de Gauss-Lucas]
:label: exo-315

1. Soit $P \in \C[X]$ non constant. Montrer que les racines de $P'$ appartiennent à l'enveloppe convexe des racines de $P$.
1. Soit $P \in \C[X]$ non constant, et soit $H$ un demi-plan de $\C$ tels que $0 \in P'(H)$. Montrer que $P(H) = \C$.
1. Retrouver le thèorème de D'Alembert-Gauss.

```

```{solution} exo-315
:class: dropdown

1. On considère la fraction rationnelle $\frac{P'}{P}$, de DES $\sum \frac{\alpha_k}{X-x_k}$, où les $x_k$ sont les racines de $P$ et $\alpha_k$ leur multiplicité. Soit $x$ une racine de $P'$ qui n'est pas aussi une racine de $P$. On écrit
\begin{align*}
0 &= \sum_k \frac{\alpha_k}{x-x_k} \\
0 &= \sum_k \overline{(x - x_k)}\frac{\alpha_k}{|x-x_k|^2}\\
0 &= \sum_k (x - x_k)\frac{\alpha_k}{|x-x_k|^2}\\
x &= \sum_k \frac{\lambda_k}{\sum_i \lambda_i} x_k
\end{align*}
où les $\lambda_k = \frac{1}{|x-x_k|^2}$ sont compris entre $0$ et $1$.

2. Soit $z\in \C$. On considère $P_z = P-z$. $P_z$ vérifie les mêmes hypothèses que $P$. Si $P_z$ ne s'annule pas sur $H$, alors l'enveloppe convexe des racines de $P_z$ est incluse dans $\C \setminus H$ et donc les racines de $P'_z$ le sont aussi. Cela étant exclu par hypothèse, $P_z$ s'annule sur $H$, donc $P$ atteint $z$ sur $H$. Cela conclut.
3. Récurrence sur le degré. Le cas d'initialisation se fait à la main (et est, au passage, trivial).

```












































































 