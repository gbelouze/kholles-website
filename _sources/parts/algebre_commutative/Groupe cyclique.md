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

# Groupe cyclique

```{exercise}
:label: exo-235
Montrer que le groupe alterné $\mathcal{A}_n$ est engendré par les 3-cycles de $\S_n$.
```

```{solution} exo-235
:class: dropdown
On observe que $(a_1 \; a_2 \; a_3) \circ (a_2 \; a_3 \; a_4) = (a_1 \; a_2) \circ (a_3 \; a_4)$. Puis $(a_1 \; a_2) \circ (a_2 \; a_3) = (a_1 \; a_2 \; a_3)$.  Notons $\mathcal{B}_n$ le groupe engendré par les trois cycles. Alors pour tout $b \in \mathcal{B}_n$, $\varepsilon(b) = 1$ donc $\mathcal{B}_n \subset \mathcal{A}_n$. Si $a \in \mathcal{A}_n$, on décompose $a$ comme produit de transpositions. En évaluant la signature de $a$, il vient qu'il y a un nombre pair de ces transpositions, on peut donc les regrouper deux par deux. D'après l'observation initiale, $a$ se décompose en produit de 3-cycles. Cela conclut.
```


```{exercise}
:label: exo-236
Trouver tous les morphismes de groupe de $(\S_n,\circ)$ dans $(\C^*, \times)$.

*Variante* trouver tous les morphismes de groupe de $(\S_n,\circ)$ dans $G$ un groupe commutatif (ça marche pareil).
```

```{solution} exo-236
:class: dropdown
Soit $\mu$ un tel morphisme. Alors pour toute transposition $(i \; j)$, $\mu^2(i \; j) = 1$ donc l'image des transpositions par $\mu$ est dans $\{-1,1\}$ et puisque les transpositions engendrent le groupe symétrique, $\mu$ est un morphisme dans $(\{-1,1\}, \times)$. S'il vaut $1$ sur les transpositions, il est trivial. Sinon par exemple $f(1 \; 2) = -1$. Alors pour tout $i \in [\![3,n]\!]$, on a $f(1 \; 2 \; i)^3 = f(Id)=1=f((1 \; i) \circ (1 \; 2))^3 = -1 \times f(1 \; i)^3$ donc $f(1 \; i) = -1$ puis avec le même raisonnement, pour tout $j$, $f(i \; j) = -1$. Ainsi $\mu$ et le morphisme signature $\varepsilon$ coïncident sur une partie qui engendre le groupe, donc sont égaux. Finalement les deux seuls morphismes de $(\S_n,\circ)$ dans $(\C^*, \times)$ sont l'identité et la signature.
```

```{exercise}
:label: exo-237
Soit $n \in \N^*$. Calculer le nombre moyen de points fixes des permutations de $\S_n$.
```

```{solution} exo-237
:class: dropdown
Soit $m$ ce nombre. On écrit
\begin{align*}
m &= \frac{1}{n!} \sum_{\sigma \in \S_n} \sum_{i=1}^n \mathds{1}_{i=\sigma(i)} \\
&= \frac{1}{n!} \sum_{i=1}^n \sum_{\sigma \in \S_n} \mathds{1}_{i=\sigma(i)} \\
&= \frac{1}{n!} \sum_{i=1}^n (n-1)! \\
&= 1 \\
\end{align*}
```


```{exercise}
:label: exo-238
Montrer que les permutations de $\S_n$ qui commutent avec $\sigma = (1 \; 2 \; \ldots \; n)$ sont les puissances de $\sigma$.
```

```{solution} exo-238
:class: dropdown
Soit $\tau$ qui commute avec $\sigma$. On a $(\tau(1) \; \tau(2) \; \ldots \; \tau(n)) = \tau \circ \sigma \circ \tau^{-1} = (1 \; 2 \; \ldots \; n) $. Soit $i = \tau^{-1}(1)$. On a donc pour tout $k \in [\![ 0,n-1 ]\!]$, $\tau(i+k) = 1+k$, donc $\tau = \sigma^{i-1}$.
```


```{exercise}
:label: exo-239
Pour $\sigma \in \S_n$, on définit l'orbite d'un élément $i \in [\![1,n]\!]$ comme étant
\begin{equation*}
 \{ \sigma^k(i) \; | \; k \in \N \}
\end{equation*}
On note $o(\sigma)$ le nombre d'orbites distinctes de $\sigma$. Exprimer $\varepsilon(\sigma)$ en fonction de $o(\sigma)$
.
```

```{solution} exo-239
:class: dropdown
On décompose en cycles à supports disjoints. On trouve $\varepsilon(\sigma) = (-1)^{n-o(\sigma)}$.
```


```{exercise}
:label: exo-240
Pour chacune des décompositions suivantes, calculer leur puissance 2018.
\begin{align*}
\sigma_1 &=
\begin{pmatrix}
1 & 2 & 3 & 4 & 5  & 6 & 7 & 8 & 9 & 10 \\
6 & 1 & 3 & 9 & 10 & 8 & 5 & 2 & 4 & 7 \\
\end{pmatrix}
\\
\sigma_2 &=
\begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6 & 7  & 8 & 9 & 10 \\
8 & 6 & 3 & 4 & 7 & 2 & 10 & 1 & 9 & 5 \\
\end{pmatrix}
\\
\sigma_3 &=
\begin{pmatrix}
1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 \\
2 & 8 & 3 & 9 & 5 & 1 & 7 & 6 & 4 & 10 \\
\end{pmatrix}
\\
\end{align*}
```

```{solution} exo-240
:class: dropdown
Simple décomposition en cycles à supports dijoints.
```


```{exercise}
:label: exo-241
Soit $\sigma = (i_1 \; i_2 \; \ldots \; i_p)$ un cycle de $\S_n$ et $\tau \in \S_n$. Exprimer $ \tau \circ \sigma \circ \tau^{-1}$.
```

```{solution} exo-241
:class: dropdown
Il s'agit de $(\tau(i_1), \tau(i_2), \ldots, \tau(i_p))$.
```

```{exercise}
:label: exo-242
Montrer que $\S_n$ est engendré par $(1 \; 2)$ et $(1\; 2 \; \ldots \; n )$.
```

```{solution} exo-242
:class: dropdown
Notons $\sigma = (1 \; 2)$ et $\tau = (1\; 2 \; \ldots \; n )$. Les $\tau^n \circ \sigma \circ \tau^{-n}$ génèrent les $(i,i+1)$. Puis on génère $(1,i+1) = (i, i+1) (1,i) (i, i+1)$. Enfin on génère $(i,j) = (1,j) (1,i) (1,j)$, donc toutes les transpositions, donc le groupe.
```








































































 