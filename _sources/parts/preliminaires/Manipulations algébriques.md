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

# Manipulations algébriques


```{exercise}
:label: exo-67
Voir énoncé 4.2 du poly de Mansuy. Calculer par télescopage $S=\sum \limits_{k=0}^n \frac{k}{(k+1)!}$.
Difficulté : *
```

```{solution} exo-67
:class: dropdown
\begin{align*}
S &= \sum \limits_{k=0}^n \frac{1}{k!} - \frac{1}{(k+1)!} \\
&= 1 - \frac{1}{(n+1)!}  \text{ (télescopage)} \\
\end{align*}
```



```{exercise}
:label: exo-68
Voir énoncé 4.2 du poly de Mansuy. Calculer par télescopage $S=\sum \limits_{k=0}^n \frac{1}{\sqrt{k+1} + \sqrt{k}}$.
Difficulté : *
```

```{solution} exo-68
:class: dropdown
\begin{align*}
S &= \sum \limits_{k=0}^n \frac{\sqrt{k+1}-\sqrt{k}}{(\sqrt{k+1}+\sqrt{k})(\sqrt{k+1}-\sqrt{k})} \\
&= \sqrt{n+1}  \text{ (télescopage)} \\
\end{align*}
```



```{exercise}
:label: exo-69
Voir énoncé 4.3 du poly de Mansuy, première somme. Calculer $S_1 = \sum \limits_{k=0, k \equiv 0[3]}^n {n\choose k}$.
Difficulté : **
```

```{solution} exo-69
:class: dropdown
On note
\begin{align*}
S_1 &= \sum \limits_{k=0, k \equiv 0[3]}^n {n\choose k} \\
S_2 &= \sum \limits_{k=0, k \equiv 1[3]}^n {n\choose k} j \\
S_3 &= \sum \limits_{k=0, k \equiv 2[3]}^n {n\choose k} j^2 \\
\end{align*}
On a alors
\begin{align*}
S_1+S_2+S_3 &= (1+j)^n = -j^{2n} \\
S_1+jS_2+j^2S_3 &= (1+j^2)^n = -j^n \\
S_1+j^2S_2+jS_3 &= 2^n \\
\end{align*}
D'où en sommant les trois égalités $S_1 = \frac{1}{3}(2^n-j^n-j^{2n})$.
```



```{exercise}
:label: exo-70
Voir énoncé 4.3 du poly de Mansuy, deuxième somme. Calculer $S_1 = \sum \limits_{k=0}^n {n\choose 2k}(-1)^k $.
Difficulté : **
```

```{solution} exo-70
:class: dropdown
On note
\begin{align*}
S_1 &= \sum \limits_{k=0}^n {n\choose 2k}(-1)^k \\
S_2 &= i\sum \limits_{k=0}^n {n\choose 2k+1} (-1)^k  \\
\end{align*}
On a alors
\begin{align*}
S_1+S_2 &= (1+i)^n \\
S_1-S_2 &= (1-i)^n  \\
\end{align*}
D'où en sommant les deux égalités $S_1 = \frac{1}{2}((1-i)^n+(1+i)^n)$.
```



```{exercise}
:label: exo-71
Voir énoncé 4.3 du poly de Mansuy, troisième somme. Calculer $S_1(t) = \sum \limits_{k=0}^n {2n+1\choose 2k+1}t^{2k+1}$.
Difficulté : **
```

```{solution} exo-71
:class: dropdown
On note
\begin{align*}
S_1(t) &= \sum \limits_{k=0}^n {2n+1\choose 2k+1}t^{2k+1} \\
S_2(t) &= \sum \limits_{k=0}^n {2n+1\choose 2k}t^{2k} \\
\end{align*}
On a alors
\begin{align*}
S_1(t)+S_2(t) &= (1+t)^{2n+1} \\
S_2(t)-S_1(t) &= (1-t)^{2n+1}  \\
\end{align*}
D'où en sommant les deux égalités $S_1(t) = \frac{1}{2}((1+t)^{2n+1}-(1-t)^{2n+1})$.
```



```{exercise}
:label: exo-72
Voir énoncé 4.11 du poly de Mansuy. Soit $x_1, \; \ldots, \, x_p$ des entiers tels que pour tout $k$, $0 \leq x_k \leq k$ et $x_p \neq 0$.
La suite finnie $(x_1, \; \ldots, \, x_p)$ s'appelle l'écriture factorielle de l'entier $n = \sum \limits_{k=1}^{p} x_kk!$.
Montrer que cette écriture existe et est unique pour tout entier naturel $n$.
Difficulté : **
```


```{solution} exo-72
:class: dropdown
On montre l'unicité en premier lieu. Pour cela on se donne par l'absurde $x_1, \, \ldots, \, x_p, y_1, \, \ldots, \,y_p$ tels que $y_p-x_p \geq 1$
et $\sum \limits_{k=1}^p (y_k-x_k)k! = 0$. De là $p! \leq \sum \limits_{k=1}^{p-1} k \times k! < p!$, la dernière inégalité étant
immédiate par récurrence. Cela fournit la contradiction et prouve l'unicité de la décomposition. Il suffit alors de remarquer que
$[\![0,p!-1]\!]$ et $\{(x_1, \, \ldots, \, x_{p-1}), \; 0 \leq x_k \leq k\}$ ont même cardinal pour conclure.
```



```{exercise}
:label: exo-73
Voir énoncé 4.8 du poly de Mansuy. Calculer pour tout $\theta \in \mathbb{R}$, la somme $S_1 = \sum \limits_{k=0}^n {n \choose k} \cos(k \theta)$.
Difficulté : **
```

```{solution} exo-73
:class: dropdown
L'astuce consiste à considérer la deuxième somme $S_2 = \sum \limits_{k=0}^n {n\choose k}i\sin(k\theta)$.
On a alors $S_1 = \mathfrak{Re}(S_1 + S_2) = \mathfrak{Re}((1+e{i\theta})^n)$.
```




```{exercise}
:label: exo-74
Voir énoncé 4.10 du poly de Mansuy. Simplifier $(1-2z+z^2) \sum \limits_{k=1}^n kz^k$.
Difficulté : **
```

```{solution} exo-74
:class: dropdown
On regarde le polynôme $Q(X)=\sum \limits_{k=0}^nX^k = \frac{X^{n+1}-1}{X-1}$ sur $\mathbb{R} \setminus \{1\}$ de dérivée
$Q'(X)=\sum \limits_{k=1}^nkX^{k-1} = \frac{nX^{n+1}-(n+1)X^n +1}{(X-1)^2}$. Ainsi le polynôme de l'énoncé et
$nX^{n+2}-(n+1)X^{n+1} +X$ coïncident sur un ensemble infini donc sur $\mathbb{C}$.
```



```{exercise}
:label: exo-75
Soit $E$ un ensemble de cardinal $n$. Calculer $S = \sum \limits_{A,B \subset E} |A \bigcap B|$. Difficulté :  **
```

```{solution} exo-75
:class: dropdown
\begin{align*}
S &= \sum \limits_{A,B \subset E} \sum \limits_{x \in E} \mathds{1}_{x \in A \bigcap B} \\
&= \sum \limits_{x \in E} \sum \limits_{A,B \subset E} \mathds{1}_{x \in A \bigcap B} \\
&= \sum \limits_{x \in E} | \{A,B \in E \setminus \{x\} \} | \\
&= \sum \limits_{x \in E} 4^{n-1} \\
&= n4^{n-1} \\
\end{align*}
```




```{exercise}
:label: exo-76
Soit $p \in \N^*$. Calculer $S = \sum \limits_{k=0, k \equiv 0[p]}^n {n\choose k}$
```














































































 