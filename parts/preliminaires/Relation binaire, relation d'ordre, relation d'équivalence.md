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

# Relation binaire, relation d'ordre, relation d'équivalence


```{exercise}
:label: exo-43

1. Montrer l'inégalité de Cauchy-Schwarz $(\sum x_iy_i)^2 \leq (\sum x_i^2)(\sum y_i^2)$.
1. Soit $E$ un ensemble de cardinal $n$, $\mathscr{R}$ une relation d'équivalence sur $E$ ayant $k$ classes d'équivalence et $G = {(x, y) \in E^2 \; | \; x\mathscr{R}y}$ le graphe d'équivalence de $\mathscr{R}$ supposé de cardinal $p$. Montrer que $n^2 \leq kp$.
```

```{solution} exo-43
:class: dropdown

1.
    \begin{align*}
    (\sum x_iy_i)^2  &= \sum x_i^2y_i^2 + 2\sum_{i<j} (x_iy_i)(x_jy_j) \\
    (\sum x_i^2)(\sum y_i^2) &= \sum x_i^2y_i^2 + \sum_{i<j} x_i^2y_j^2 + x_j^2y_i^2 \\
    &= (\sum x_iy_i)^2 + \sum_{i<j} x_i^2y_j^2 - 2(x_iy_ix_jy_j) + x_j^2y_i^2 \\
    &= (\sum x_iy_i)^2 + \sum_{i<j} (x_iy_j-x_jy_i)^2 \\
    &\geq (\sum x_iy_i)^2
    \end{align*}
2.
    On a $n = |c_1| + \ldots + |c_k|$ et $p = |c_1|^2 + \ldots + |c_k|^2$. On applique Cauchy-Schwarz avec $x_i = |c_i|$ et $y_i = 1$.
```



```{exercise}
:label: exo-44
Soit $E$ un ensemble et $A$ une partie de $E$. On définit une relation $\mathscr{R}$ sur $\mathcal{P}(E)$ par
\begin{equation*}
 x \mathscr{R} y \Leftrightarrow X \cup A = Y \cup A
\end{equation*}

1. Montrer que $\mathscr{R}$ est une relation d'équivalence.
1. Décrire la classe d'équivalence de $X \in \mathcal{P}(E)$.


```

```{solution} exo-44
:class: dropdown

1. Évident
1. Soit pour $X \subset E$, $\tilde{X} = X \setminus A$. On montre que $\tilde{X}$ est un représentant de la classe d'équivalence pour $X$, et que $X \mathscr{R} Y$ si et seulement si $\tilde{X} = \tilde{Y}$. Dès lors
\begin{equation*}
 \bar{X} = \{ (X \setminus A) \cup B \; | \; B \subset A\}
\end{equation*}

```



```{exercise}
:label: exo-45
Soit $\mathscr{R}$ une relation binaire sur $X$. Montrer qu'il existe une unique relation d'équivalence $\overset{*}{\mathscr{R}}$ vérifiant
1. *coherence* $x \mathscr{R} y \Rightarrow x \overset{*}{\mathscr{R}} y$
1. si une relation d'équivalence $\sim$ vérife *coherence*, alors les classes d'équivalence de $\sim$ contiennent les classes d'équivalence de $\mathscr{R}$.

Cette relation d'équivalence s'appelle la clôture réflexive, symétrique, transitive de $\mathscr{R}$.
```



```{exercise}
:label: exo-47
Soit $\preccurlyeq$ la relation binaire définie sur le demi-plan $E = \{(a,b) \in \R^2 \; | \; a \leq b \}$ par
\begin{equation*}
 (a,b) \preccurlyeq (a',b') \Leftrightarrow (a,b)=(a',b') \textrm{ ou } b \leq a'
\end{equation*}

1. Montrer que $\preccurlyeq$ est une relation d'ordre sur $E$.
1. S'agit-il d'une relation d'ordre totale ?

```

```{solution} exo-47
:class: dropdown

1. On applique la définition.
1. $(1,2)$ et $(1,3)$ ne sont pas comparables.

```



```{exercise} Ordre lexicographique
:label: exo-48
Sur $E = \N^2$, on définit la relation binaire $\preccurlyeq$ par
\begin{equation*}
 (x,y) \preccurlyeq (x',y') \Leftrightarrow x < x' \textrm{ ou } (x=x' \textrm{ et } y \leq y')
\end{equation*}

1. Vérifier que $\preccurlyeq$ est une relation d'ordre sur $E$.
1. S'agit-il d'une relation d'ordre totale ? S'agit-il d'un bon ordre ?

```

```{solution} exo-48
:class: dropdown

1. Vérifier la définition.
1. Oui et oui. Il suffit de vérifier que toute partie non vide possède un minimum, ce qui est facile en ne considérant que les éléments dont la première coordonnée est minimale.

```



```{admonition} Relation bien fondée
:class: margin
Une relation binaire $\rightarrow$ est bien fondée s'il n'existe pas de suite infinie $x_n \rightarrow x_{n+1}$.
```
```{exercise} lemme de Newman
:label: exo-49
Soit $E$ un ensemble et $\rightarrow$ une relation sur $E$. On note $\overset{*}{\rightarrow}$ la clôture réflexive, transitive de $\rightarrow$. On dit que $\rightarrow$

- est **confluente** si
\begin{equation*}
 \forall x, y, z \in E, \; z \overset{*}{\leftarrow} x \overset{*}{\rightarrow} y \Rightarrow ( \exists v \in E, \; y \overset{*}{\rightarrow} v \textrm{ et } z \overset{*}{\rightarrow} v)
\end{equation*}
- est **localement confluente** si
\begin{equation*}
 \forall x, y, z \in E, \; z \leftarrow x \rightarrow y \Rightarrow ( \exists v \in E, \; y \overset{*}{\rightarrow} v \textrm{ et } z \overset{*}{\rightarrow} v)
\end{equation*}

On veut montrer que si $\rightarrow$ est bien fondée, alors $\rightarrow$ est localement confulente si et seulement si $\rightarrow$ est confluente.

Soit $P(x)$ la propriété
\begin{equation*}
 \forall y, z \in E, \; z \overset{*}{\leftarrow} x \overset{*}{\rightarrow} y \Rightarrow ( \exists v \in E, \; y \overset{*}{\rightarrow} v \textrm{ et } z \overset{*}{\rightarrow} v)
\end{equation*}

1. Montrer la propriété en supposant que tous les successeurs de $x$ vérifient $P$. *Indication : utiliser deux fois l'hypothèse d'induction*.
1. Conclure par l'absurde.
```



```{exercise} Ordre alphabétique
:label: exo-50
On se donne $\prec$ un ordre stricte sur un alphabet $\mathcal{A}$.
On définit l'ordre lexicographique sur les mots de $\mathcal{A}$ par
\begin{equation*}
 u \leq_{lex} v \Leftrightarrow \begin{cases}
u \textrm{ est préfixe de } v \\
\textrm{ou}\\
\exists w, s, t \in \mathcal{A}^*, \; a,b \in \mathcal{A}, \; a \prec b \textrm{ et } u = was, \; v = wbt
\end{cases}
\end{equation*}
On définit l'ordre militaire sur les mots de $\mathcal{A}$ par
\begin{equation*}
 u \leq_{mil} v \Leftrightarrow \begin{cases}
|u| < |v| \\
\textrm{ou}\\
|u| = |v| \textrm{ et } u \leq_{lex} v
\end{cases}
\end{equation*}
Montrer que l'ordre militaire est bien fondé, mais que l'ordre lexicographique ne l'est pas.
```

````{solution} exo-50
:class: dropdown
**L'ordre lexicographique n'est pas bien fondé**
Il suffit de trouver un contre-exemple. Par exemple, $u_n = a^nb$ est strictement décroissante pour l'odre lexicographique.

**L'ordre militaire est bien fondé**
Supposons par l'absurde qu'on puisse trouver $(u_n)$ une suite strictement décroissante pour l'ordre militaire. Remarquons que la suite $|u_n|$ est une suite d'entiers décroissante, donc constante à partir d'un certain rang, mettons $N$. Cela fournit donc une suite $(v_n)$ telle que $v_{n+1} <_{lex} v_n$ pour tout $n$ et $|v_n|$ est constante. On va montrer la propriété suivante, par récurrence sur la taille de $w_n$
```{prf:lemma}
:nonumber:
Soit $w_n$ une suite de taille constante et décroissante pour $\leq_{lex}$. Alors $w_n$ est stationnaire (i.e. constante à partir d'un certain rang)
```
Alors $v_n$ constituera une contradiction.

L'initialisation où $w_n$ est juste une lettre est immédiate parce que $\mathcal{A}$ est fini, et donc $\prec$ est un bon ordre. Soit maintenant donc $v_n$ de taille constante $p+1$. Considérons $w_n$ les $p$ premières lettres de $v_n$, et $z_n$ la dernière lettre, i.e. $v_n = w_nz_n$. Alors $w_n$ et $z_n$ sont décroissantes pour $\leq_{lex}$, donc par hypothèse de récurrence stationnaire, donc $v_n$ l'est également.
````



```{exercise}
:label: exo-51
On suppose que la relation "être l'ami de" est réflexive et symétrique, et que le nombre de personnes est fini. Montrer qu'il existe deux personnes ayant autant d'amis.
```

```{solution} exo-51
:class: dropdown
Par l'absurde, la fonction nombre d'amis est une bijection avec $[\,| 1, n |\,]$ où $n$ est le nombre de personnes. En particulier, il existe une personne amie qu'avec elle-même, et une avec tout le monde. Cela entre en contradiction avec la symétrie.
```



```{exercise}
:label: exo-52
On suppose que la relation "avoir serré la main" est irréflexive et symétrique, et que l'ensemble des personnes est fini. Montrer que le nombre de personnes ayant serré un nombre impair de mains est pair.
```

```{solution} exo-52
:class: dropdown
On regarde $p = |{(x,y) \; | \; \textrm{$x$ et $y$ se sont serrés la main}}|$. Notons $\Delta$ la relation "a serré la main de". Par symétrie et irréflexivité, $p$ est pair. En effet, en notant $x_1, \ldots, x_n$ les personnes, on peut écrire
\begin{align*} p &= \sum_{1\leq i,j \leq n, \; x_i \Delta x_j} 1 \\
&= \sum_{1\leq i,j \leq n, \; i \neq j, \; x_i \Delta x_j} 1 \qquad &\textrm{(irréfléxivité)}\\
&= \sum_{1\leq i<j \leq n, \; x_i \Delta x_j} 2 \qquad &\textrm{(symétrie)}\\
&= 0 \mod{2}
\end{align*}
Or $p = \sum_i |\{ \textrm{mains serrées par $x_i$}\}|$. Notons $I$ la partie de $1, \ldots, n$ correspondant aux personnes ayant serré un nombre impair de mains, et $J$ son complémentaire. On a
\begin{align*}
p &= \sum_{i=1}^n |\{y \; | \; x_i\Delta y\}| \\
&= \sum_{i \in I} 1 + \sum_{i \in J} 0 \mod{2} \\
&= |I| \mod{2}
\end{align*}
```



```{exercise}
:label: exo-53
Soit $(E, \preccurlyeq)$ un ensemble ordonné tel que toute partie non vide admet un plus petit élément et un plus grand élément. Montrer que $E$ est fini.
```

```{solution} exo-53
:class: dropdown
Si $E$ est infini, on peut prendre son plus grand élément, puis le plus grand des restant, etc. ce qui construit une suite infinie strictement décroissante.
```



```{exercise}
:label: exo-54
Soit $E$ un ensemble ordonné par une relation $\leq$. On considère un tableau à $n$ lignes et $p$ colonnes d'éléments de $E$. Comparer
\begin{equation*}
 \underset{1 \leq j \leq p}{\max} \left ( \underset{1 \leq i \leq n}{\min} a_{i,j} \right )
\end{equation*}
et
\begin{equation*}
 \underset{1 \leq i \leq n}{\min} \left ( \underset{1 \leq j \leq p}{\max} a_{i,j} \right )
\end{equation*}
Donner un cas de non égalité.
```

```{solution} exo-54
:class: dropdown
Le plus petit des géants est plus grand que le plus grand des nains.
```







































































 