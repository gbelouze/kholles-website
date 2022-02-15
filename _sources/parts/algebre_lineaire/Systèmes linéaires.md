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

# Systèmes linéaires

```{exercise}
:label: exo-398
Discuter de l'existence et de l'unicité d'un polygône à $n$ côté où les milieux de chaque côté sont fixés.
```

```{solution} exo-398
:class: dropdown
Le système est équivalent à l'existence d'affixe $z_1, \ldots, z_n$ tels que $\forall i$, $z_i + z_{i+1} = 2a_i$. Ceka donne un système à résoudre. On trouve que si $n$ est impair il y a toujours une unique solution, et que si $n$ est pairon a la condition de compatibilité $\sum (-1)^k a_k = 0$ et lorsqu'elle est remplie il y a une infinité de solutions.
```

```{exercise}
:label: exo-399
Soit $A\in \M_n(\R)$. Montrer que $A$ est de rang $r$ si et seulement si $A$ est équivalente à $J_r$. En déduire que $A$ et $A^t$ ont même rang.
```

```{solution} exo-399
:class: dropdown
Corollaire du pivot de Gauss : équivalence à un certain $J_s$, puis même dimension de l'image : $r=s$.
```

```{exercise}
:label: exo-400
Soit $A \in \M_{n,p}(\R)$ de rang $r$, $V \in GL_p(\R)$ telle que $AV$ soit échelonnée en colonnes. Montrer que

1. $C_1(AV), \ldots, C_r(AV)$ est une base de $Im(A)$.
1. $C_{r+1}(V), \ldots, C_p(V)$ est une base de $Ker(A)$.

```

```{solution} exo-400
:class: dropdown

1. La famille est libre car $AV$ est échelonnée en colonne, elle est composée de vecteurs de $Im(A)$ donc libre et bonne dimension, donc base.
1. $AC_k(V)=C_k(AV)$ donc c'est une famillede $Ker(A)$, libre car $V$ est inversible, et de bon cardinal. C'est une base.

```

```{exercise}
:label: exo-401
Soit $A \in \M_n(\R)$ de rang $r$ et $U \in GL_n(\R)$ telle que $UA$ est échelonnée en lignes. Montrer que

1. $X\in Ker(A)$ si et seulement si
 \begin{equation*}
 L_1(UA)X=0, \ldots, L_r(UA)X=0 \end{equation*}

1. $Y \in Im(A)$ si et seulement si
\begin{equation*}

L_{r+1}(U)Y=0, \ldots, L_n(U)Y=0
\end{equation*}

```

```{solution} exo-401
:class: dropdown

1. $X \in Ker(A) \Leftrightarrow UAX = 0 \Leftrightarrow \forall i, \; L_i(UA)X = 0 \Leftrightarrow \forall i \leq r, \; L_i(UA)X=0$
1. On écrit $Y=AX$. Alors $UY=UAX$ donc $\forall i > r, L_i(UY)=0$. D'où $Im(A) \subset \bigcap \limits_{i=r+1}^n Ker(L_i(U))$. Or $L_{r+1}(U), \ldots, L_n(U)$ est libre donc $dim(\bigcap \limits_{i=r+1}^n Ker(L_i(U))) = n-(n-r)=r=rg(A)$. D'où l'égalité.

```

```{exercise}
:label: exo-402
Trouver une base du noyau et de l'image de $A=\begin{pmatrix} 1&0&2&1&2 \\ 0&1&1&3&3\\ 1&1&2&2&1 \end{pmatrix} $
```











































































 