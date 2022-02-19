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

# Convergence des suites numériques


```{exercise}
:label: exo-103
Voir énoncé 6.6 du poly de Mansuy. Soit $(u_n)$ et $(v_n)$ deux suites réelles de majorants $l$ et $l'$ respectivement, telles que $u_n+v_n \rightarrow l+l'$.
Que dire de $u_n$ ?
Difficulté : *
```

```{solution} exo-103
:class: dropdown
On montre que $u_n \rightarrow l$.
Soit $\varepsilon > 0$ et $N$ tel que $\forall n \geq N$, $|l+l' - (u_n +v_n)| < \varepsilon$. $l$ et $l'$ étant des majorants respectifs de $u_n$ et $v_n$ on a
$|l-u_n| \leq |l-u_n| + |l'-v_n| = |l+l' - (u_n +v_n)| < \varepsilon$ d'où le résultat souhaité.
```




```{exercise}
:label: exo-104
Voir énoncé 6.3 du poly de Mansuy. Soit $(u_n)$ une suite réelle convergente vers $l$. Est-ce que $(\lfloor u_n \rfloor)$ est convergente ? Et si $l \notin \Z$ ?

Difficulté : *
```

```{solution} exo-104
:class: dropdown
Un contre-exemple est fourni par $\frac{(-1)^n}{n}$.
```



```{exercise}
:label: exo-105
Voir énoncé 6.14 du poly de Mansuy. Soit $(u_n)_n$ et $(v_n)_n$ deux suites équivalentes de limite $+\mathcal{1}$. Montrer que
\begin{equation*}
 \ln (u_n) \sim \ln (v_n) \end{equation*}

Difficulté : *
```

```{solution} exo-105
:class: dropdown
$\ln (u_n)-\ln (v_n) = \ln(\frac{u_n}{v_n}) \longrightarrow 0$. Or $\ln(u_n) \longrightarrow +\mathcal{1}$ . L'équivalence est alors immédiate.
```



```{exercise}
:label: exo-106
Voir énoncé 6.8 du poly de Mansuy. Étudier par inégalité la convergence de la suite définie par $u_n = n^2\sum \limits_{k=1}^{n}\frac{1}{k+n^3}$.
Difficulté : *
```

```{solution} exo-106
:class: dropdown
D'une part $v_n \leq n^2\sum \limits_{k=1}^{n}\frac{1}{n^3} = 1$ et d'autre part $v_n \geq n^2\sum \limits_{k=1}^{n}\frac{1}{n^3+n} = \frac{n^2}{1+n^2} \rightarrow 1$.
Par encadrement, $v_n \rightarrow 1$.
```



```{exercise}
:label: exo-107
Voir énoncé 6.15 du poly de Mansuy. Soit $(u_n)_n$ telle que $u_n \sim \frac{1}{n}$ et
\begin{equation*}
 \forall n \geq 1, \; \; u_n \leq \frac{1}{n} + \frac{2}{n^2} \end{equation*}

A-t-on $u_n = \frac{1}{n} + O(\frac{1}{n^2})$ ? Et si on ajoute la condition $u_n \geq \frac{1}{n}$ ?
Difficulté : *
```

```{solution} exo-107
:class: dropdown
$u_n = \frac{1}{n} - \frac{1}{n \ln(n)}$ fournit un contre-exemple à la première égalité. En ajoutant l'inégalité supplémentaire, $u_n = \frac{1}{n} + O(\frac{1}{n^2})$
devient vrai puisque $|u_n - \frac{1}{n^2}| \leq \frac{2}{n^2}$.
```



```{exercise}
:label: exo-108
Voir énoncé 6.4 du poly de Mansuy. Soit $a>0$, étudier la convergence de la suite $u_n=(\lfloor a^n \rfloor^{\frac{1}{n}})_n$.
Difficulté = */**
```

```{solution} exo-108
:class: dropdown

- Si a<1, $u_n$ est stationnaire à 0.
- Si a=1, $u_n$ est constante égale à 1.
- si a>1, on regarde l'inégalité $a \leq u_n \leq (a^n +1)^{\frac{1}{n}} = e^{\frac{1}{n} \ln(a^n+1)}$. Or l'inégalité des accroissements finis s'écrit
pour $\ln$ sur $[1 \; , \; +\mathcal{1}[$, $\ln(a^n+1) \leq n\ln(a) +1$. De là vient la convergence du membre de droite vers $a$, puis par encadrement celle
de $u_n$ vers $a$.
```



```{exercise}
:label: exo-109
Voir énoncé 6.5 du poly de Mansuy. Soit $\alpha = 2 + \sqrt{3}$ et $\beta = 2 -\sqrt{3}$.

1. Montrer que pour tout $n\in \mathbb{N}$, $u_n=\alpha^n + \beta^n \in \mathbb{N}$.
1. Étudier la convergence de $(\alpha^n - \lfloor \alpha^n \rfloor)_n$.

Difficulté : **
```

```{solution} exo-109
:class: dropdown

1.
    On écrit le binôme de Newton
    \begin{align*}
    \alpha^n + \beta^n &= \sum \limits _{k=0}^n {n \choose k} 2^{n-k} \sqrt{3}^k (1 + (-1)^k) \\
    &=  \sum \limits _{k=0, \; \text{k paire}}^n {n \choose k} 2^{n-k+1} 3^{\frac{k}{2}} \in \mathbb{N}\\
    \end{align*}
2.
    On a $0 < \beta < 1$ donc $\forall n$, $\lfloor \alpha^n \rfloor = u_n -1$. Il vient
    \begin{equation*}
     \alpha^n - \lfloor \alpha^n \rfloor = 1 - \beta^n \rightarrow 1
    \end{equation*}

    Cela conclut.
```



```{exercise}
:label: exo-110
Voir énoncé 6.7 du poly de Mansuy. Soit $(u_n)_n$ et$(v_n)_n$ deux suites telles que $u_n^2+v_n^2+u_nv_n \rightarrow 0$. Que dire de $u_n$ et $v_n$ ?
Indication : pour faciliter l'exercice, on pourra plutôt demander de montrer que leur limite est 0.
Difficulté : **
```

```{solution} exo-110
:class: dropdown
$(u_n+v_n)^2 - u_nv_n \longrightarrow 0$ donc $\forall \varepsilon > 0$, $\exists N \in\mathbb{N}$, $\forall n \geq N$, $u_nv_n > -\varepsilon$. On peut imposer de plus
$\forall n \geq N$, $|u_n^2+v_n^2 + u_nv_n| < \varepsilon$, ce qui amène $0 \leq u_n^2+v_n^2 < 2\varepsilon$ (l'inégalité se voit bien par l'absurde).
Finalement on trouve que $u_n^2 + v_n^2 \longrightarrow 0$ ce qui conduit au résultat souhaité.
```



```{exercise}
:label: exo-111
Voir énoncé 6.21 du poly de Mansuy.

1. Montrer que pour tout $n\in \mathbb{N}^*$, l'équation $e^x = n-x$ admet une unique solution positive que l'on notera $x_n$.
1. Déterminer deux termes du développement asymptotique de $x_n$.

Difficulté : **
```

```{solution} exo-111
:class: dropdown

1. On étudie la fonction $f_n(x) = e^x - n + x$ de dérivée strictement positive sur $\mathbb{R}_+$ donc strictement croissante sur cet intervalle. De plus
$f(0) \leq 0$ et $f(n) > 0$ d'où le résultat.

2.
$x_n = n - e^{x_n} \geq 0$ donc $\forall n, \; x_n \leq \ln (n)$. Ainsi $e^{x_n} \sim n$ donc (voir exercice 6.14 du poly de Mansuy) \begin{equation*}
 x_n \sim \ln (n)\end{equation*}

On écrit $\alpha_n = \ln(n) - x_n \geq 0$. On a donc $\alpha_n = o(\ln (n))$. En repartant de l'égalité de définition de $x_n$ on obtient alors
$e^{\ln(n)-\alpha_n} = n-\ln(n) + \alpha_n $ ce qui amène $\ln(n)-\alpha_n = \ln (n - \ln (n) + \alpha_n)$ puis $\alpha_n = -\ln (1 - \frac{\ln (n)-\alpha_n}{n}) \sim -\ln (1 - \frac{\ln (n)}{n}) $.
On utilise alors l'équivalent $\ln (1+x) \underset{x\rightarrow 0}{\sim} x$ qui se retrouve par exemple avec le théorème des accroissements finis. Bref,
\begin{equation*}
 u_n = \ln (n) - \ln(\ln(n)) + o( \ln(\ln(n)))\end{equation*}



```




```{exercise}
:label: exo-112
Voir énoncé 6.36 du poly de Mansuy. Soit $\phi \; : \; \mathbb{N} \rightarrow \mathbb{Q}$ bijective. Déterminer les valeurs d'adhérence de la suite $(\phi(n))_n$.
Difficulté : **
```


```{solution} exo-112
:class: dropdown
On montre que l'ensemble des valeurs d'adhérence de $\phi_n$ est $\mathbb{R}$. Pour cela on se donne $q \in \mathbb{Q}$. Pour tout $\varepsilon > 0$, l'ensemble
$\{ r \in \mathbb{Q}, \; |q-r| < \varepsilon \}$ est infini, donc $\{ \phi^{-1}(r), \; r \in \mathbb{Q}, \; |q-r| < \varepsilon \}$ n'est pas borné et ainsi $\forall N, \; \exists n > N, \; |q-\phi(n)| < \varepsilon $. Cela assure donc que $q$ est une valeur
d'adhérence de la suite. Par densité de $\mathbb{Q}$ dans $\mathbb{R}$, le résultat cherché est alors acquis.
```


```{exercise}
:label: exo-113
Montrer qu'une suite bornée converge si et seulement si elle admet exactement une valeur d'adhérence.
```

```{solution} exo-113
:class: dropdown
Le sens direct est évident. Pour le sens retour, si $(u_n)$ ne converge pas vers l'unique valeur d'adhérence $a$, alors on peut se munir d'une extractrice $\phi$ tel que $d(a, (u_{\phi(n)})) > \varepsilon$ pour un certain $\varepsilon$ suffisamment petit. Alors $(u_{\phi(n)})$ est bornée, donc admet une valeur d'adhérence, qui nécessairement n'est pas $a$. Cela fournit une seconde valeur d'adhérence à $(u_n)$ ce qui est une contradiction.
```


````{exercise}
:label: exo-114
Soit $(u_n)_n$ une suite bornée telle que $u_n + \frac{1}{2}u_{2n} \rightarrow 1$. Que dire de $u_n$ ?
```{admonition} Indication
:class: tip
On pourra demander de montrer qu'une suite bornée converge si et seulement si elle admet exactement une valeur d'adhérence.
```
Et si on abandonne l'hypothèse $(u_n)$ bornée ?
````

```{solution} exo-114
:class: dropdown
La relation assure que si $a$ est une valeur d'adhérence de $(u_n)$, alors $2-2a$ l'est également, et $f(a) = -2+4a$ l'est donc également (en recomposant).
Supposons par l'absurde qu'il existe $a \neq \frac{2}{3}$ une valeur d'adhérence de $(u_n)$. Alors $4a - 2 - \frac{2}{3} = 4 \times (a-\frac{2}{3})$
donc la suite $f^{on}(a)$ diverge, ce qui contredit l'hypothèse de bornitude. Ainsi $(u_n)_n$ est bornée et n'admet qu'une seule valeur d'adhérence, donc converge et il est immédiat que $\frac{2}{3}$ est la limite.

Si on abandonne l'hypothèse bornée, on va trouver un contre-exemple explicite en posant
\begin{align*}
u_n =
\begin{cases}
\frac{1}{3}(2 + (-2)^k) \quad &\textrm{si $n = 2^k$}\\
\frac{2}{3} \quad &\textrm{sinon}
\end{cases}
\end{align*}
qui n'est pas bornée donc ne converge pas, et qui vérifie $u_n + \frac{1}{2}u_{2n} = 1$.
```


```{exercise}
:label: exo-115
Soit $(a_n)$ une suite de $\R_+^*$ qui converge vers $0$. Montrer que les ensembles $X^+ = \{ n \in \N \; | \; \forall m \geq n, \; a_m \leq a_n \}$ et $X^- = \{ n \in \N \; | \; \forall m \leq n, \; a_m \geq a_n \}$ sont infinis.
```

```{solution} exo-115
:class: dropdown
On montre que $X^+$ n'est pas majoré. Soit donc $N \in \N$. On a $a_{N+1} > 0$, posons $\varepsilon = a_{N+1}/2 < a_{N+1}$. Par convergence vers $0$, il existe $M$ tel que $\forall m \geq M$, $u_m < \varepsilon$. Soit $M_0$ le plus petit de ces tels $M$. Nécessairement $M_0 > N+1$, donc $M_0 - 1 > N$ , et $M_0 - 1$ appartient à $X^+$, ce qui conclut.

On montre encore plus facilement que $X^-$ n'est pas majoré. Soit $N \in \N$, et $m = \underset{1 \leq n \leq N}{u_n} > 0$. Il existe $k$ tel que $u_k < m$. Soit $k_0$ le plus petit de ces tels $k$. Nécessairement $k_0 \geq N + 1$ et $k_0 - 1 \in X^-$.
```


```{exercise}
:label: exo-116
Montrer Bolzano-Weierstrauss dans $\R^d$ pour $|| \cdot ||_{\infty}$
```

```{solution} exo-116
:class: dropdown
Chaque composante est bornée, on peut faire $d$ extractions.
```

```{exercise}
:label: exo-117
Montrer que $||\cdot ||_1$, $|| \cdot ||_2$ et $|| \cdot ||_{\infty}$ sont équivalentes.
```

```{solution} exo-117
:class: dropdown

```



```{exercise}
:label: exo-118
Soit $z_1, \ldots, z_p$ des complexes de module 1. Montrer que $p$ est une valeur d'adhérence de $s_n = (z_1^n + \ldots + z_p^n)_n$. On pourra admettre le cas $p=1$.
```

```{solution} exo-118
:class: dropdown
Par récurrence sur $p$. L'initialisation est évidente. On factorise par $z_p^n$. Notons $y_i=\frac{z_i}{z_n}$. Soit donc $\phi$ une extractrice telle que $(y_1^{\phi(n)} + \ldots + y_{p-1}^{\phi(n)})_n \rightarrow p-1$. De plus $s_{\phi(n)}$ est dans un fermé borné de dimension finie donc admet une valeur d'adhérence, et nécessairement celle-ci est de module $p$, notons la donc $pe^{i\theta}$. Idée générale : il existe un $N$ tel que $e^{i\theta}$ est très proche de $1$. De plus, être proche de
$pe^{i\theta}$ force chacun des $n\theta_i$ à être proche de $\theta$. De là, on peut rendre $\max_i (N|\theta-\theta_i|)$ arbitrairement petit, ce amène que $s$ est proche de $pe^{iN\theta}$ donc de $p$.
```



```{exercise}
:label: exo-119
Soit $z_1, \ldots, z_p$ des complexes de module supérieur ou égal à 1 tels que $z_1^n+ \ldots + z_p^n$ converge. Montrer que $z_1 = \ldots = z_p = 1$.
Inidication : Utiliser l'exercice précédent.
```

```{solution} exo-119
:class: dropdown
On se ramène au cas de complexes de module 1 en factorisant par le complexe de plus grand module. D'après l'exercise précédent $p$ est une valeur d'adhérence de $(z_1^n + \ldots + z_p^n)_n$ donc la limite de cette suite est $p$. On peut alors par exemple regarder la partie réelle des $z_i^n$ qui est majorée par 1. Il vient qu'elle tend vers 1 pour tout $i$ puis que $z_i=1$ pour tout $i$.
```




```{exercise}
:label: exo-120
Soit $\sigma$ une bijection de $\N^*$ dans $\N^*$ telle que $(\frac{\sigma(n)}{n})$ converge. Que dire de la limite ?
```

```{solution} exo-120
:class: dropdown
On montre $l=1$. Si $l<1$ en choisissant $l<l'<1$ on exhibe une contradiction avec l'injectivité. Si $l>1$ on exhibe une contradiction avec la surjectivité.
```



```{exercise}
:label: adherence_condition
Soit $u_n \in \R^{\N}$, et $a \in \R$ tel que $\forall \varepsilon > 0$, l'ensemble $\B(a, \varepsilon) \cap (u_n)$ est infini. Montrer que $a$ est une valeur d'adhérence de $u$.
```

```{solution} adherence_condition
:class: dropdown
Pour tout $n$ on peut donc se munir d'une extractrice $\phi_n$ telle que $d((u_{\phi_n}), a) \leq \frac{1}{n}$. On définit alors notre extractice $\psi$ par
\begin{equation*}
 \psi(n) = \phi_n \circ \phi_{n-1} \circ \ldots \circ \phi_1 (n)
\end{equation*}
Et on peut vérifier que $|u_{\psi}(n) - a| \leq \frac{1}{n}$
```



```{exercise}
:label: exo-122
Soit $u_n$ telle que $u_{n+1}-u_n \rightarrow 0$. Montrer que l'ensemble des valeurs d'adhérence de $(u_n)$ est un intervalle.
```

```{solution} exo-122
:class: dropdown
Soit $a<b$ deux valeurs d'adhérence de la suite, $c \in ]a, b[$ et $\varepsilon > 0$. Soit $N$ tel que $u$ fait des pas de moins de $\varepsilon$ après $N$.

Soit $A \in \R$ tel que $A \geq N$ et soit $A < n < m$ tels que $|u_n - a| < \varepsilon$ et $|u_m - b| < \varepsilon$. Soit $M = \max{k < m \; | \; u_k < c}$. On a $n \leq M \leq m$ (quitte à prendre $\varepsilon$ suffisamment petit, $M \geq n$), et de plus $u_M \leq c \leq u_{M+1}$ donc $|u_M - c| \leq |u_M - u_{M+1}| \leq \varepsilon$.

Remarquons que $M \geq A$, donc il existe une infinité de rangs tels que $u$ est proche de $c$ : $c$ est une valeur d'adhérence (par exemple avec l'exercice {ref}`adherence_condition`).
```





```{exercise}
:label: exo-123
Exhiber une suite dont l'ensemble des valeurs d'adhérence est $\R$.
```

```{solution} exo-123
:class: dropdown
Par exemple notons $u$ la suite qui à $n = \overline{a_1a_2\ldots a_k}^{10}$ (écrit en base $10$) associe $u_n = 0,a_1a_2a_3\ldots$. Alors $0.1$ est une valeur d'adhérence, et $1$ est une valeur d'adhérence, et $u_{n+1} - u_n \rightarrow 0$, donc tout élément de $[0.1, 1]$ est une valeur d'adhérence de $u$.

Ensuite on dilate continument. D'abord $v_n = f(u_n)$ où $f(x) = -1 + 2\frac{1-x}{0.9}$, et tout élément de $[-1, 1]$ est une valeur d'adhérence de $v_n$, puis $w_n = \th (v_n)$

Sinon n'importe quelle bijection de $\N$ vers $\Q$.
```



```{exercise}
:label: exo-124
Soit $(u_n) \in \C^{\N}$ et $(l_k)$ une suite de valeur d'adhérence de $(u_n)$ qui tend vers $l$. Montrer que $l$ est une valeur d'adhérence de $(u_n)$.
```

```{solution} exo-124
:class: dropdown
On note $\phi_k$ une extractrice associée à $l_k$, que l'on choisit de sorte que $d(l_k, (u_{\phi_k})) \leq \frac{1}{k}$. Il suffit de considérer l'extractrice $\psi : k \mapsto \phi_k \circ \ldots \circ \phi_1 (k)$.
```



````{exercise}
:label: exo-125
Soit $u_n = \sum \limits_{k=0}^n\frac{1}{k!}$ et $v_n = u_n + \frac{1}{nn!}$. Montrer que $(u_n)$ et $(v_n)$ convergent vers la même limite, notée $e$. Montrer que $e \notin \Q$.
```{admonition} Indication
:class: tip
Montrer que $(u_n)$ et $(v_n)$ sont adjacentes.
```
````



```{exercise}
:label: exo-126
Nature de la série de terme général $\sin(\pi(2+\sqrt{3})^n)$.
```

```{solution} exo-126
:class: dropdown
Soit $\alpha = 2+\sqrt{3}$ et $\beta = 2-\sqrt{3}$. On a pour tout $n$, $\alpha^n+\beta^n \in \N$. De là $|\sin(\pi\alpha^n)| = \sin(\pi\beta^n) \sim \pi\beta^n$ d'où la convergence de la série.
```




```{exercise}
:label: exo-127
Soit $(w_n)$ une suite à valeurs dans $[0,1]$ telle que pour tout $n$, 
\begin{equation*}
w_{n+1}(1-w_n) > \frac{1}{4}
\end{equation*}
Nature et limite de $(w_n)$.
```

```{solution} exo-127
:class: dropdown
On montre que la suite est croissante en utilisant que $\forall x, \; x(1-x) \leq \frac{1}{4}$. Nécessairement elle converge et la limite $l$ doit vérifier $l(1-l) \geq \frac{1}{4}$ et de là $l=\frac{1}{2}$.
```



```{exercise}
:label: exo-128
Soit $(u_n)$ une suite à valeurs dans $\R$ vérifiant $u_0 \neq 0$ et pour tout $n$, 
\begin{equation*}
u_{n+1} \leq 2- \frac{1}{u_n}
\end{equation*}
Nature et limite de $(u_n)$.
```

```{solution} exo-128
:class: dropdown
Remarquons que $\forall x>0, \; 2-\frac{1}{x} \leq x$ avec égalité si et seulement si $x=1$. La suite est donc décroissante. Donc converge. Donc inégalité à la limite. Donc la limite est $1$.
```



```{exercise}
:label: exo-129
Soit $p_n, q_n$ deux suites d'entiers naturels, telles que $\frac{p_n}{q_n}\rightarrow x \notin \Q$. Montrer que $q_n \rightarrow +\infty$.
```

```{solution} exo-129
:class: dropdown
La distance de $x$ à $\frac{\N}{q_n}$ est minorée par $\varepsilon_n > 0$.

Sinon on peut aussi extraire par l'absurde une valeur d'adhérence que $(q_n)$ et en déduire que $p_{\phi(n)}$ converge puis que $x$ est rationnel.
```

















































































 