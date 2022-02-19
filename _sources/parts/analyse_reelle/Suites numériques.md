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

# Suites numériques


```{exercise}
:label: exo-97
Soit $\alpha \in \mathbb{R}$ et $(u_n)_n$ la suite définie par :
\begin{equation*}
 \forall n \in \mathbb{N}, \; \; u_{n+2} - 2 \cos(\alpha )u_{n+1} + u_n = 0
\end{equation*}
Donner l'expression de $u_n$ en fonction de $n$.
```

```{solution} exo-97
:class: dropdown
Classiquement on regarde le polynôme $P(x)=X^2-2 \cos ( \alpha ) X + 1 = (X-e^{i\alpha})(X-e^{-i\alpha})$. Il vient $u_n = A e^{in\alpha} + B e^{-in\alpha}$ où $A$ et $B$ vérifient
$A+B=u_0$ et $A e^{i\alpha} + B e^{-i\alpha} = u_1$ ce qui fournit sans difficulté les valeurs de $A$ et $B$.
```



```{exercise}
:label: exo-99
Soit $(u_n)_n$ une suite définie par $u_0=1$ et
\begin{equation*}
 \forall n \in \mathbb{N}, \; u_{n+1} = (\prod \limits_{k=0}^n u_k) +2 
\end{equation*}

Déterminer l'expression, pour $n \geq 1$, de $u_n$ en fonction de $n$.
```

```{solution} exo-99
:class: dropdown
Soit $n\geq1$. On réécrit la relation de récurrence $u_{n+1} = u_n(\prod \limits_{k=0}^{n-1} u_k) + 2 = (u_n-2)u_n +2$.
On introduit alors $v_n =u_n-1$ qui vérifie la relation de récurrence $v_{n+1}=v_n^2$. Cela amène $\forall n \geq 1, \; u_n = 2^{2^{n-1}}+1$.
```



```{exercise}
:label: exo-100
Voir énoncé 5.8 du poly de Mansuy.
```

```{solution} exo-100
:class: dropdown
La suite $v_n = u_n+1$ vérifie la relation de récurrence $v_{n+1} = 2v_n + 3^n$. La suite $(3_n)_{n\in \mathbb{N}}$ vérifie la même relation de récurrence.
Ainsi $w_n = v_n - 3^n$ vérifie $w_{n+1} = 2w_n$. On trouve alors facilement une expression de $u_n$.
```



```{exercise}
:label: exo-101
Considérons la suite $(u_n)_{n\geq1}$, dont les valeurs sont successivement 1, 2, 2, 3, 3, 3, 4, 4, 4, 4, 5, $\ldots$. Donner
une expression explicite de $u_n$ en fonction de $n$.
```

```{solution} exo-101
:class: dropdown
La formule $\sum \limits_{k=1}^n k = \frac{n(n+1)}{2}$ amène que $\forall p \in ] \frac{n(n-1)}{2}, \; \frac{n(n+1)}{2}], \; u_p = n$.
La limite a lieu lorsque $2p = n(n+1)$ soit $n=\frac{-1+\sqrt{1+8p}}{2}$. Ainsi $u_n = \lceil \frac{-1+\sqrt{1+8n}}{2} \rceil$.
```




```{exercise}
:label: exo-102
Soit $u_n=\sum \limits_{k=1}^n \lfloor \frac{n}{k} \rfloor$. Trouver les entiers $n \in \mathbb{N}$ pour lesquels $u_n$ est pair.
```


```{solution} exo-102
:class: dropdown
On se propose d'établir une relation de récurrence sur $u_n$. On regarde
\begin{equation*}
 u_{n+1} - u_n = 1 +  \sum \limits_{k=1}^n [\frac{n+1}{k}] - [\frac{n}{k}] = Card \{ d, d | n+1 \}
\end{equation*}
Il s'agit donc de déterminer la parité du nombre de diviseurs de $n$. On se convainc facilement en associant deux par deux les diviseurs que ce nombre est toujours
pairs à moins que $n$ ne soit un carré. Ainsi les $n$ convenables, sachant que 1 ne l'est pas, sont $4, \; 5, \; \ldots, \; 8, \; 16, \; \ldots, \; 24, \; \ldots$. Autrement dit,
$\mathbb{S} = \{ n, \; \exists p \in \mathbb{N}, \; (2p)^2 \leq n < (2p+1)^2 \}$.
```















































































 