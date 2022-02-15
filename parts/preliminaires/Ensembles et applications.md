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

# Ensembles et applications



```{exercise}
:label: exo-26

1. Soit $A,B$ des parties de $E$. Résoudre pour $X\in E$ l'équation $X \bigcup A = X \bigcap B$.
1. Soit $A,B$ des parties de $E$. Résoudre pour $X\in E$ l'équation $X \bigcup A = \overline{X} \bigcap B$.
```

```{solution} exo-26
:class: dropdown

1.
    On a toujours $A \subset X \bigcup A$ et $X \bigcap B \subset B$. Une condition nécessaire à l'existence de solution est donc $A \subset B$.

    De plus si $X$ est solution, pour avoir l'inclusion du membre de gauche dans celui de droite, il faut $X \subset B$. L'équation se réécrit alors:
    $X \bigcup A = X$, soit $A \subset X$. Ainsi on trouve $\mathcal{S} = \{ A \bigcup Y \; | \; Y \in (B \setminus A)\}$.
2.
    Analyse : soit $X$ solution. $\emptyset = X \bigcap (\overline{X} \bigcap B) = X \bigcap (X \bigcup A) = X$. Synthèse : $\emptyset$ est solution si et seulement si
    $A = B$.

```



```{exercise}
:label: exo-27
Soit $(u_n)_{n \in \mathbb{N}}$ une suite. On dit que $(u_n)$ est de Cauchy si
\begin{equation*}
 \forall \varepsilon > 0, \; \exists N \in \mathbb{N}, \; \forall n,p > N, \; |u_n-u_p|<\varepsilon
\end{equation*}

1.
    Comparer cette définition avec
    \begin{equation*}
     \forall \varepsilon > 0, \; \exists n \in \mathbb{N}, \; \forall p > n, \; |u_n-u_p|<\varepsilon
    \end{equation*}

2.
    Exprimer le caractère borné d'une suite à l'aide de quantificateurs. Montrer qu'une suite de Cauchy est bornée.
3.
    Montrer qu'une suite convergente est de Cauchy.
4.
    Comparer la définition d'une suite de Cauchy avec la suivante
\begin{equation*}
 \forall \varepsilon > 0, \; \exists N \in \mathbb{N}, \; \forall n > N, \; |u_{n+1} - u_n| < \varepsilon
\end{equation*}
```



```{exercise}
:label: exo-28
Soit $x_1, \; \ldots, \, x_p$ des entiers tels que pour tout $k$, $0 \leq x_k \leq k$ et $x_p \neq 0$.
La suite finie $(x_1, \; \ldots, \, x_p)$ s'appelle l'écriture factorielle de l'entier $n = \sum \limits_{k=1}^{p} x_kk!$.

Montrer que cette écriture existe et est unique pour tout entier naturel $n$.
```



```{exercise}
:label: exo-29
Soit $u_n=\sum \limits_{k=1}^n \lfloor \frac{n}{k} \rfloor$. Trouver les entiers $n \in \mathbb{N}$ pour lesquels $u_n$ est pair.
```



```{exercise}
:label: exo-30
Soit $(u_n)_{n \in \mathbb{N}}$ une suite. On définit la $\sigma(u_n)$ comme l'ensemble des valeurs prises une infinité de fois par $(u_n)$.

Exprimer $\sigma(u_n)$ à l'aide de quantificateurs, puis à l'aide d'opérations ensemblistes sur les $U_n = \{ u_i \; | \; i \geq n \}$.
```



```{exercise}
:label: exo-31
Montrer que le raisonnement par récurrence est valide, i.e. $\left ( P(0) \textrm{ et } (P(n) \Rightarrow P(n+1)) \right ) \Rightarrow \forall n, \; P(n)$.
```



```{exercise}
:label: exo-32
Voir énoncé 2.9 du poly de Mansuy. Soit $A$ et $B$ deux parties de E. Considérons
\begin{equation*}
    \phi \longmapsto\begin{cases}
     P(E) \;  \rightarrow \; P(A) \times P(B) \\

     X \; \mapsto (A \bigcap X, B \bigcap X )
    \end{cases}
\end{equation*}

1. Montrer que $\phi$ est injective si, et seulement si, $A \cup B = E$.
1. Trouver une condition nécessaire et suffisante pour que $\phi$ soit surjective.
1. On suppose que $\phi$ est bijective. Calculer $\phi^{-1}$.

Difficulté : *
```

```{solution} exo-32
:class: dropdown

1.
    $(\Rightarrow)$ On raisonne par contraposée en se donnant $x \in E \setminus A \cup B$. Alors $\forall X$, $\phi (X) = \phi(X\cup \{ x \} )$
    d'où la non injectivité.

    $(\Leftarrow)$ Par contraposée encore. Soit $X$ et $Y$ de même image par $\phi$, et par exemple soit $x \in X \setminus Y$. Il est immédiat
    que $x \notin A$ et $x \notin B$.
2.
    La condition est $A \bigcap B = \emptyset $.
3.
    \begin{equation*}
        \phi^{-1} \longmapsto\begin{cases}
         P(A) \times P(B) \;  \rightarrow \; P(E) \\

        (X_1, Y_1) \; \mapsto X_1 \cup Y_1
        \end{cases}
    \end{equation*}

```



```{exercise}
:label: exo-33
Voir énoncé 2.22 du poly de Mansuy. Soit $E= \{ x_1, \; \ldots, \; x_p\}$. Prouver que l'on peut ordonner les éléments de $P(E)$ en respectant
les 4 règles suivantes :

- on commence par $\emptyset$,
- on termine par un singleton,
- chaque élément de $P(E)$ apparaît une et une seule fois,
- chaque terme de la suite est obtenu par l'ajout ou le retrait d'un seul élément au terme précédent.
Difficulté : *
```

```{solution} exo-33
:class: dropdown
On prouve le résultat par récurrence. Soit $\emptyset = a_1, \ldots, a_{2^p} = \{ x_p \}$ une suite de parties convenable associée à $E={x_1, \ldots, x_p}$.

Une suite convenable associée à $E \cup \{ x_{p+1} \}$ est alors
\begin{equation*}
 a_1, \ldots, a_{2^p}, a_{2^p} \cup \{x_{p+1} \}, \ldots, a_1 \cup \{x_{p+1} \} = \{x_{p+1} \}
\end{equation*}

```



```{exercise}
:label: exo-34
Trouver une bijection entre $\mathbb{R}$ et $\mathbb{R}\setminus \mathbb{Z}$. Difficulté : **
```

```{solution} exo-34
:class: dropdown
On note $x_n = \sum \limits_{k=1}^n \frac{1}{2^k}$. On considère alors la bijection
\begin{equation*}
    \phi : \; x \longmapsto\begin{cases}
     m + x_{n+1} \; \text{si } x \text{ est de la forme } x=m+x_n \text{ où } m \in \mathbb{Z} \\

    x \text{ sinon}
    \end{cases}
\end{equation*}
```



```{exercise}
:label: exo-35
Voir énoncé 2.17 du poly de Mansuy. Soit $f$ : $\mathbb{N} \rightarrow \mathbb{N}$ injective et $g$ : $\mathbb{N} \rightarrow \mathbb{N}$ surjective, telles que
\begin{equation*}
 \forall n \in \mathbb{N}, \; f(n) \leq g(n)
\end{equation*}
Montrer que $f=g$.
Difficulté : **
```

```{solution} exo-35
:class: dropdown
Soit par l'absurde $n$ tel que $f(n)<g(n)$. Par surjectivité de $g$ il existe $a_0, \, a_1, \ldots, a_{g(n)}=n$ tels que
$\forall i, \; g(a_i)=i$. Par injectivité de $f$, $Card \{ f(a_i) | i =0, \ldots, g(n) \} = g(n)+1$. Or par hypothèse,
$\{ f(a_i) | i =0, \ldots, g(n) \} \subset [\![0;g(n)-1]\!]$ ce qui amène la contradiction.
```



```{exercise}
:label: exo-36
Soit $E$ un ensemble et $X \subset E$. La fonction indicatrice de $X$ est définie par
\begin{equation*}
    \mathds{1}_X \longmapsto\begin{cases}
     E \;  \rightarrow \; &\{ 0,1 \} \\

     x \; \mapsto &1 \textrm{ si } x \in X \\
     &0 \textrm{ sinon}
    \end{cases}
\end{equation*}

1. Soit $A,B \subset E$. Exprimer $\mathds{1}_{A \bigcup B}, \; \mathds{1}_{A \bigcap B}, \; \mathds{1}_{A \setminus B}$ en fonction de $\mathds{1}_A$ et $\mathds{1}_B$.

2. Soit $A_1$, $A_2$, $\ldots$, $A_n$ des sous-ensembles de $E$. Prouver l'égalité suivante
\begin{equation*}
\mathds{1}_{A_1 \cup A_2 \cup \ldots \cup A_n} = \sum \limits_{k=1}^n (-1)^{k-1} \sum \limits_{1 \leq i_1 \leq \ldots \leq i_k \leq n} \mathds{1}_{A_{i_1}} \ldots \mathds{1}_{A_{i_k}}
\end{equation*}

```

```{solution} exo-36
:class: dropdown

1. $\mathds{1}_{A \bigcap B} = \mathds{1}_A \mathds{1}_B$, $\mathds{1}_{A \setminus B} = \mathds{1}_A (1 - \mathds{1}_B)$ et enfin $\mathds{1}_{A \bigcup B} = \mathds{1}_A + \mathds{1}_B - \mathds{1}_A \mathds{1}_B$.

2. On prouve le résultat par récurrence, l'initialisation ayant été faite à la question précédente. On applique l'hypothèse de récurrence avec $A_n \bigcup A_{n+1}$ au lieu de $A_n$.
\begin{align*}
& \mathds{1}_{A_1 \cup A_2 \cup \ldots \cup A_{n+1}} \\ &= \mathds{1}_{A_n \bigcup A_{n+1}} + \sum \limits_{k=1}^{n-1} (-1)^{k-1} \sum \limits_{1 \leq i_1 \leq \ldots \leq i_k \leq n-1} \mathds{1}_{A_{i_1}} \ldots \mathds{1}_{A_{i_k}} - \mathds{1}_{A_{i_1}} \ldots \mathds{1}_{A_{i_k}}\mathds{1}_{A_n \bigcup A_{n+1}} \\
&= \mathds{1}_{A_n} + \mathds{1}_{A_{n+1}} - \mathds{1}_{A_n} \mathds{1}_{A_{n+1}} + \sum \limits_{k=1}^{n-1} (-1)^{k-1} \sum \limits_{1 \leq i_1 \leq \ldots \leq i_k \leq n-1} \mathds{1}_{A_{i_1}} \ldots \mathds{1}_{A_{i_k}} - \mathds{1}_{A_{i_1}} \ldots \mathds{1}_{A_{i_k}}(\mathds{1}_{A_n} + \mathds{1}_{A_{n+1}} - \mathds{1}_{A_n} \mathds{1}_{A_{n+1}}) \\
&= \sum \limits_{k=1}^{n+1} (-1)^{k-1} \sum \limits_{1 \leq i_1 \leq \ldots \leq i_k \leq n+1} \mathds{1}_{A_{i_1}} \ldots \mathds{1}_{A_{i_k}}
\end{align*}

```



```{exercise}
:label: exo-37
Trouver une bijection entre $\mathbb{N}$ et $\mathbb{N}^2$. Montrer que $\forall n \in \mathbb{N}$, $\mathbb{N}$ et $\mathbb{N}^n$ sont en bijection. Montrer que l'ensemble des suites d'entiers
nulles à partir d'un certain rang est en bijection avec $\mathbb{N}$.
```

```{solution} exo-37
:class: dropdown
$(n,p) \longrightarrow (2n+1)2^p-1$. Le second résultat se montre par récurrence et en utilisant le cas $n=2$. On note alors $\phi_n$ des bijections de $\mathbb{N}$ dans $\mathbb{S}^n$
où $\mathbb{S}^n$ désigne l'ensemble des suites d'entiers nulles à partir du rang $n+1$ exactement. On utilise alors un procédé diagonal : Si on note $\phi_2'$ et $\phi_2''$ les
deux premières composantes de $\phi_2$, alors $n \longrightarrow \phi_{\phi_2'(n)}(\phi_2''(n))$ convient.
```



```{exercise}
:label: exo-38
Existence d'un point fixe pour une fonction $f : \mathcal{P}(E) \rightarrow \mathcal{P}(E)$ croissante.

*Indication : considérer le plus grand $A$ vérifiant $A \subset f(A)$.*
```

```{solution} exo-38
:class: dropdown
Soit $(A_i)_{i \in I}$ l'ensemble des parties de $E$ vérifiant $A_i \subset f(A_i)$. Soit $A = \cup_{i\in I}A_i$. Alors $f(A) = \cup f(A_i)$ donc $A \subset f(A)$. Par croissance de $f$, $f(A) \subset f(f(A))$ donc par maximalité de $A$, $f(A) \subset A$. Bref $A = f(A)$.
```



```{exercise}
:label: exo-39
Soit $E$ un ensemble. Montrer que $E$ est infini ssi toute fonction $f$ de $E$ dans lui-même admet une partie stable non triviale.
```

```{solution} exo-39
:class: dropdown
Si $E$ est fini, considérer $f$ un cycle de support $E$.<br>
Si $E$ est infini, considérons $f : E \rightarrow E$, et choisissons $x \in E$ quelconque. Soit $A = \underset{n \in \N}{\cup} f^{\circ n}(x)$. De toute évidence $A$ est stable par $f$. Si $A$ est fini, $A \neq E$ et $A$ convient. Sinon, $(f^{\circ n}(x))_n$ n'est pas cyclique et en particulier $x \notin \underset{n \geq 1}{\cup} f^{\circ n}(x) = B$. $B$ est stable par $f$ et convient.
```



```{exercise}
:label: exo-40
On dit que $f, g \; : \; X \rightarrow Y$ possèdent un coégalisateur $e : Y \rightarrow Q$ lorsque
1. *Commutativité* $e \circ f = e \circ g$
1. *Maximalité* pour toute fonction $d : Y \rightarrow Q'$ telle que $d \circ f = d \circ g$, il existe une unique fonction $h : Q \rightarrow Q'$ vérifiant $h \circ e = d$.

Montrer que si $e$ existe, alors $e$ est surjective. *Indication : montrer que $\phi$ est surjective si et seulement si pour toute paire de fonction $h_1, h_2$, $h_1 \circ \phi = h_2 \circ \phi \Rightarrow h_1 = h_2$*

Montrer qu'il existe toujours un coégalisateur.
```

```{solution} exo-40
:class: dropdown
La première question se fait avec l'indication et en utilisant le critère *Maximalité*. Pour la deuxième question, on considère la relation binaire $\mathscr{R}$ sur $Y$ définie par
\begin{equation*}
 y_1 \mathscr{R} y_2 \Leftrightarrow \exists x \in X, \; \begin{cases}
y_1 = f(x) \\
y_2 = g(x)
\end{cases}
\end{equation*}
et on s'intéresse aux classes d'équivalences de $\overset{*}{\mathscr{R}}$ la clôture réflexive symétrique transitive de $\mathscr{R}$. Définissons $e : \begin{cases} Y \rightarrow Y / \overset{*}{\mathscr{R}} \\ y \longmapsto \bar{y} \end{cases}$. On montre que $e$ est un coégalisateur. Le seul point délicat est de montrer que $d$ est nécessairement constante sur les classes d'équivalence. Faire un dessin.
```



```{exercise}
:label: exo-41
Montrer qu'on ne peut pas surjecter un ensemble sur ses parties.

*Indication : considérer $P = \{x \; | x \notin f(x) \}$*
```

```{solution} exo-41
:class: dropdown
$P$ a un antécédent par $f$, soit $y$. Si $y \in P$, $y \notin f(y) = P$. Si $y \notin P$, $y \in P$. Bref, absurde.
```



```{exercise} théorème de Bernstein
:label: exo-42
Soit $A,B$ des ensembles tels qu'il existe $f : A \rightarrow B$ injective, $g : B \rightarrow A$ injective. On veut montrer que $A$ et $B$ sont en bijection.

1. Montrer qu'il suffit de trouver une bijection entre $A$ et $g(B)$.
1. Soit $A_0 = A \setminus g(B)$. On définit $A_{n+1} = (g \circ f)(A_n)$. Montrer qu'il suffit de trouver une bijection entre $X = \underset{n \in \N}{\cup}A_n$ et $Y = \underset{n \geq 1}{\cup}A_n$.
1. Conclure

```

```{solution} exo-42
:class: dropdown

1. $B$ et $g(B)$ sont en bijection par injectivité de $g$.
1. Considérons $\sigma : X \rightarrow Y $ qu'on prolonge en $\tilde{\sigma}$ sur $A$ par l'identité. $\tilde{\sigma}$ est injective, et bijective dans $(A\setminus X) \cup Y$. Remarquons que pour tout $n \geq 1$, $A_n \subset g(B)$. Ainsi $A_0 \cup Y = \emptyset$. Dès lors, $(A\setminus X) \cap Y = A \setminus A_0 = g(B)$. Il suit que $\tilde{\sigma}$ est une bijection de $A$ vers $g(B)$, ce qui conclut avec la première question.
1. $\phi = g\circ f$ consititue une bijection de $X$ vers $Y$.

```




































































 