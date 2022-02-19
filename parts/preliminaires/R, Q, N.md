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

# R, Q, N



```{exercise}
:label: exo-77
Montrer qu'une union dénombrable d'ensemble dénombrable est dénombrable.
```



```{exercise}
:label: exo-78
Soit $\sigma: \N \rightarrow \N$ une bijection. Montrer que l'ensemble des $n$ tels que $\sigma(n) \geq n$ est infini.
```

```{solution} exo-78
:class: dropdown
On va montrer que l'ensemble des $\{ \sigma \; | \; \exists n \sigma = \sigma(n) \textrm{ and } \sigma(n) \geq n \} $ n'est pas majoré, cela conclura par bijectivité de $\sigma$. Soit $N \in \N$, et considérons l'ensemble $\sigma([\![1, N]\!]$.

- Si $\sigma([\![1, N]\!] = [\![1, N]\!]$ alors $\sigma(N+1) \geq N+1$.
- Sinon $\exists k \leq N$ tel que $\sigma(k) > N$ i.e. $\sigma(k) \geq N+1$.
```




```{exercise}
:label: exo-79
Soit $\sigma$ une bijection de $\N^*$ dans $\N^*$ telle que $(\frac{\sigma(n)}{n})$ converge. Que dire de la limite ? Trouver un exemple où $(\frac{\sigma(n)}{n})$ ne converge pas.
```

```{solution} exo-79
:class: dropdown
On va montrer que la limite est $1$. Soit $l$ la limite

1. Si $l<1$, soit $\varepsilon > 0$ suffisamment petit, il existe $N$ tel que $\forall n \geq N$, $\frac{\sigma(n)}{n} < 1-\varepsilon$. Soit $M = \max{\sigma(1), \ldots, \sigma(N)}$, et $K(M) = \lfloor \frac{M}{1-\varepsilon} \rfloor$. Quitte à prendre $M$ encore plus grand, $K \geq M+1$.

```



```{exercise}
:label: exo-80

1. Trouver une injection de $\R$ vers $\P(\N)$.
1. Trouver une injection de $\P(\N)$ vers $\R$.

```

```{solution} exo-80
:class: dropdown


1.
    On définit l'image de $x$ par $\phi$ de la manière suivante : si le développement de $x$ est
    $ x=0,a_1a_2\ldots
    $
    on pose
    \begin{equation*}
     \phi(x) = \{ 1a_{\frac{n(n+1)}{2}}\ldots a_{\frac{(n+1)(n+2)}{2}-1} \; | \; n \in \N^* \}
    \end{equation*}
    Meilleure solution : prendre la réciproque de la question 2, en binaire.
2. 
    On définit l'image de $A \in \P(\N)$ par $\psi$ de la manière suivante:
    \begin{equation*}
     \psi(x) = \sum_{n=1}^{+\infty} \mathds{1}_{n \in A} 10^{-n}
    \<end>equation*</end>
```



````{exercise}
:label: exo-81

1. 
    Soit $n \in \N^*$ et $a_1, \ldots, a_n$ des éléments de $[\![0,9]\!]$ non tous égaux à $9$. On note $x$ le réel dont le développement décimal est $0,a_1\ldots a_na_1\ldots a_na_1\ldots a_n\ldots$. Justifier l'existence et trouver $p,q \in \N$ tels que $x= \frac{p}{q}$.
2. 
    Réciproquement, montrer que si $x$ est rationnel, alors son développement décimal est périodique à partir d'un certain rang.
    ```{admonition} Indication
    :class: tip
    On admettra que si $u$ et $v$ sont premiers entre eux, alors il existe $n$ tels que $u^n = 1 \mod{v}$.
    ```
````

```{solution} exo-81
:class: dropdown

1.
    On note 
    \begin{equation*}
    a = \sum_{m=1}^{n}a_m10^{n-m}
    \end{equation*}

    Alors
    \begin{align*}
    x &= \sum_{k=1}^{+\infty}a10^{-nk} \\
    &= a\frac{10^{-n}}{1 - 10^{-n}} \\
    &= \frac{a}{10^n-1} \\
    \end{align*}
2.
    Soit $x = \frac{p}{q}$ avec $p \land q = 1$. Écrivons $q = 2^\alpha 5^\beta q'$ avec $q'\land 2 = q' \land 5 = 1$. Quitte à multiplier le numérateur par une puissance appropriée de $2$ ou de $5$, on se restreint à l'étude de la forme suivante $x = 10^{-m} \frac{p'}{q'}$ où $p' \land q' = 1$ et $q' \land 10 = 1$.

    Ensuite $10$ est inversible dans $(\Z/q'\Z, *)$ ce qui fournit $n$ tel que $10^n = 1 \mod{q'}$. En effet il existe $i<j$ tels que $10^i = 10^j \mod{q'}$ et on multiplie par $10^{-i}$.  Finalement on peut écrire
    \begin{equation*}
     x = 10^{-m}\frac{p''}{10^n-1}
    \end{equation*}

    dont le développement décimal est périodique à partir d'un certain rang.
```



```{exercise}
:label: exo-82
Soit $k \in \N$. On définit $(a_n)_{n \in N}$ la suite telle que $a_n$ est le chiffre des unités du coefficient binomial ${n\choose k}$. On note $x$ le réel défini par la donné de son développement décimal propre
\begin{equation*}
 x = 0,a_1a_2a_3\ldots
\end{equation*}

    1. Montrer que pour tout $n \in \N$, il existe un entier $q$ tel que
    \begin{equation*}
     {n+10k!\choose k} = {n\choose k} + 10q
    \end{equation*}

    1. En déduire que $x \in \Q$

```



```{exercise}
:label: exo-83
Soit $A$ une partie non vide bornée de $\R$. Déterminer $\underset{x,y \in A}{\sup} |x-y|$.
```

```{solution} exo-83
:class: dropdown
$\underset{x,y \in A}{\sup} |x-y| \leq \sup A - \inf A $ par définition. Soit $\varepsilon > 0$, et $x, y \in A$ tels que $ \sup A < x + \varepsilon $ et $ \inf A > y - \varepsilon$. Alors $\underset{x,y \in A}{\sup} |x-y| \geq \sup A - \inf A + 2 \varepsilon$.
```



```{exercise}
:label: exo-84
Résoudre dans $\R$ l'équation $x E(x) = x^2 - E(x)^2$ où $E(\cdot)$ désigne la fonction partie entière.
```

```{solution} exo-84
:class: dropdown
Posons $n = E(x)$ et $\alpha = x - E(x) \in [0,1]$. On doit résoudre
\begin{equation*}
n(n+\alpha) = n^2 + 2n\alpha + \alpha^2 - n^2
\end{equation*}
soit
\begin{equation*}
\alpha^2 + n\alpha - n^2 = 0
\end{equation*}
Si $\alpha = 0$, cela impose $n = 0$ et on vérifie que $x=0$ convient. Sinon $\alpha = \frac{n(\sqrt{5}-1)}{2}$. Or $2 \leq \sqrt{5} \leq 3$, nécessairement $n=1$ et $x = \frac{1+\sqrt{5}}{2}$ convient.
```




```{exercise}
:label: exo-85
Soit $G \subset \R$ sous-groupe de $\R$ pour l'addition. Montrer que $G$ est dense dans $\R$ ou bien $G$ est isomorphe à $a\Z$ pour un certain $a$ à expliciter.
```

```{solution} exo-85
:class: dropdown
On note $G^+ = G \cap \R_+^*$. Considérons $a = \inf G^+$.
- **Si $a > 0$**  : s'il existe $x,y \in G^+$ tels que $a\leq x < y < 2a$, alors $y-x \in G$ (car $G$ est un groupe) et $y-x > 0$ donc $y-x \in G^+$. Mais $y-x < a$, c'est impossible. Ainsi $a$ est atteint, i.e. $a \in G^{+}$. Puis, comme $G$ est un groupe, $a\Z \subset G$. On va montrer qu'en fait $a\Z = G$. Supposons donc par l'absurde qu'il existe $g\in G$, $g \notin a\Z$ c'est-à-dire qu'on peut trouver $k\in \Z$ tel que $ka < g < (k+1)a$. Alors $\gamma = (k+1)a - g \in G$ et $\gamma > 0$ donc $\gamma \in G^+$ et $\gamma < a$. C'est une contradiction.
- **Si $a= 0$** : on va montrer que $G^+$ est dense dans $\R_+$. Soit alors $x \in \R_+$ et $\varepsilon>0$. D'abord $a$ n'est pas atteint donc on peut trouver $g\in G$ tel que $0 < g < \varepsilon$. Prenons $n \in \N$ tel que $ng \leq x < (n+1)g$ (i.e. $n = \lfloor \frac{x}{g} \rfloor$). Alors $ng \in G$ et $|x-ng| < \varepsilon$. Cela conclut pour la densité de $G^+$ dans $\R_+$. Ensuite tout simplement $-G_+ \subset G$ et $-G_+$ est dense dans $\R_-$. Finalement, $G$ est dense dans $\R$.
```




```{exercise}
:label: exo-86
Soit $A$ une partie de $\R$. Déterminer $\sup \{ \alpha x | x \in A\}$ en fonction de $\alpha$.
```

```{solution} exo-86
:class: dropdown
Si $\alpha > 0$, il s'agit de $\alpha \sup A$, si $\alpha = 0$ c'est évident et si $\alpha < 0$, il s'agit de $\alpha \inf A$.
```



```{exercise}
:label: exo-87
Déterminer le sup et l'inf de l'ensemble suivant
\begin{equation*}
 A = \{ \frac{mn}{(m+n)^2} \; | \; m,n \in \N\setminus\{0\} \}
\end{equation*}
```

```{solution} exo-87
:class: dropdown
Commençons par noter que pour tout $m,n$, $\frac{mn}{(m+n)^2} > 0$ donc $\inf A \geq 0$. Puis par exemple $\underset{n \rightarrow + \infty}{\frac{1 \cdot n}{(1+n)^2}} = 0$ donc $\inf A \leq 0$, et finalement $\inf A = 0$.

Ensuite on écrit pour $m,n \in \N\setminus\{0\}$
\begin{equation*}
 \frac{mn}{(m+n)^2} = \frac{1}{\frac{m}{n} + \frac{n}{m} + 2}
\end{equation*}
La fonction $x + \frac{1}{x}$ est minorée par $2$ sur $\R+$, il suit que pour tout $m,n$, $\frac{mn}{(m+n)^2} \leq \frac{1}{2+2} = \frac{1}{4}$, et cette borne est atteinte pour $m,n=1$. Il suit $\sup A = \frac{1}{4}$.
```



```{exercise}
:label: exo-88
Soit $a,b,c$ des réels de $[0,1]$. Montrer qu'au moins une des quantités suivantes est plus petite que $\frac{1}{4}$ : $a(1-b), \; b(1-c), \; c(1-a)$.
```

```{solution} exo-88
:class: dropdown
$a(1-b)b(1-c)c(1-a) = a(1-a) b(1-b) c(1-c) \leq \frac{1}{4^3}$ d'où la conclusion.
```



```{exercise}
:label: exo-89
Déterminer
\begin{equation*}
 \inf \{ (x_1+ \ldots+ x_n)(\frac{1}{x_1} + \ldots + \frac{1}{x_n}) \; | \; x_1, \ldots, x_n \in \R_+^*\}
\end{equation*}
```

```{solution} exo-89
:class: dropdown
Notons $A_n = \{ (x_1+ \ldots+ x_n)(\frac{1}{x_1} + \ldots + \frac{1}{x_n}) \; | \; x_1, \ldots, x_n \in \R_+^*\}$.

Avec Cauchy-Schwarz, on a immédiatement que $\inf(A_n) \geq n^2$ et le cas $x_1=x_2=\ldots=x_n=1$ permet de conclure que $\inf(A_n) = n^2$.

Supposons qu'on ne connaisse pas Cauchy-Schwarz et retrouvons ce résultat par récurrence sur $n$.
**Pour $n=2$** On développe
\begin{align*}
(x_1 + x_2)\cdot(\frac{1}{x_1} + \frac{1}{x_2}) &= 2 + \frac{x_2}{x_1} + \frac{x_1}{x_2} \\
&\geq 2 + 2 \quad \textrm{par étude de la fonction $x \mapsto x + \frac{1}{x}$}
\end{align*}
et avec le cas $x_1 = x_2 = 1$, on trouve $\inf A_2 = 4$. Ce cas nous donne l'idée d'évaluer $x_1=x_2=\ldots=x_n=1$, et on essaye donc de prouver que $\inf A_n = n^2$.
**Hérédité** On regarde
\begin{align*}
(x_1+ \ldots+ x_n + x_{n+1})(\frac{1}{x_1} + \ldots + \frac{1}{x_n} + \frac{1}{x_{n+1}}) &= (x_1+ \ldots+ x_n)(\frac{1}{x_1} + \ldots + \frac{1}{x_n}) + 1 + \sum_{i=1}^n\frac{x_i}{x_{n+1}} + \frac{x_{n+1}}{x_i} \\
&\geq \inf A_n + 2n + 1 = (n+1)^2
\end{align*}
```



```{exercise}
:label: exo-90

1. Montrer pour $n\in \N$ que $\sqrt{n} \in \Q \Leftrightarrow \sqrt{n} \in \N$
1. Soit $a,b \in \N$ qui ne sont pas des carrés parfaits. Montrer que $\sqrt{a}+\sqrt{b}$ est irrationnel.

```

```{solution} exo-90
:class: dropdown

1. Le sens retour est évident. Soit $n$ qui n'est pas un carré parfait. Il s'agit de montrer que $\sqrt{n}$ est irrationnel, supposons par l'absurde qu'il ne l'est pas et on écrit $n = \frac{p^2}{q^2}$, soit $nq^2 = p^2$. Par identification des exposants dans la décomposition en facteur premier des deux termes, tous les exposants de la décomposition de $n$ en facteur premier sont pairs, $n$ est donc un carré parfait, ce qui est une contradiction.
1. On note $x = \sqrt{a}+\sqrt{b}$ et $y = \sqrt{a}-\sqrt{b}$. On a $xy \in \Q$ donc $x$ et $y$ sont soit tous deux rationnels, soit tous deux irrationnels. Mais $x+y \notin \Q$, ils sont donc irrationnels.

```



```{exercise}
:label: exo-91
Un nombre univers est un nombre tel que toute séquence finie de chiffres apparaît dans son développement décimal.

    1. Exhiber un nombre univers.
    1. Montrer que l'ensemble des nombres univers est dense dans $\R$.

À titre informatif, sachez qu'on peut montrer que *l'ensemble des nombres univers est indénombrable*.
```

```{solution} exo-91
:class: dropdown

1. $\alpha=  0.012345678910111213141516\ldots$
1. Soit $a<b\in\R$. On montre qu'il existe un nombre univers dans $]a,b[$. Soit $k$ tel que $a + 2\times10^{-k}<b$. $10^{-k}\lfloor 10^ka\rfloor = 10^{-k-1}\alpha$ convient.

Montrons que l'ensemble des nombres univers est indénombrable. Pour cela, notons $\alpha = 0.a_0b_0a_1b_1a_2\ldots$ où $a_n$ est l'écriture en base 10 de $2n$, et $b_n$ de $2n+1$. Remarquons que $a_ib_i \neq b_ia_i$ pour tout $i$ (par exemple car il n'ont pas la même valeur modulo $2$). À $(u_n) \in \{0,1\}^{\N}$ on associe $f(u_n) = 0.c_0c_1c_2\ldots$ où
\begin{equation*}
\begin{cases}
c_i = a_ib_i \qquad \textrm{si $u_i = 1$}\\
c_i = b_ia_i \qquad \textrm{sinon}
\end{cases}
\end{equation*}
Il suffit de remarquer pour conclure que $f$ est une fonction injective de $\{0,1\}^{\N}$ vers $\mathcal{U}$ l'ensemble des nombres univers.
```



```{exercise} nombre incommensurable
:label: exo-92

1. Soit $x \in \R$ un irrationnel. On note $D(\cdot)$ la fonction partie fractionnaire. Montrer que $\{D(nx) \; | \; n\in \N \}$ est dense dans $[0,1]$.
1. On dit que $x$ et $y$ sont incommensurables si leur rapport est irrationnel. Soit $x,y$ incommensurables. Si $z$ est un réel, on note $z \mod{y} = y D(z/y) \in [0, y[$. Montrer que l'ensemble $\{nx \mod y \; | \; n \in \N \}$ est dense dans $[0,y[$. En déduire que $\{ \cos(n) | n \in \N \}$ est dense dans $[0,1]$. *Indication : on admet l'irrationnalité de $\pi$*

```

````{solution} exo-92
:class: dropdown

1. Soit $A = \{D(nx) \; | \; n\in \N \}$. Commençons par remarquer que par irrationnalité de $x$, $D(nx)>0$ pour tout $n$. Il s'agit donc montrer que la borne inférieure de $A$ est $0$.

**$A$ n'admet pas de minimum** Soit $\delta = D(nx)$. Si $\delta$ est rationnel, égal à $p/q$, alors $D(nqx)=0$ ce qui est impossible. Ainsi $\delta$ est irrationnel. Considérons alors $k = \lfloor \frac{1}{\delta} \rfloor$. Par irrationalité de $\delta$, $k\delta < 1$ et $(k+1)\delta > 1$. Notons $\eta = 1-k\delta > 0$. On a $D(nkx) = k\delta$ et $D(n(k+1)x) = 1 + (\delta - \eta) - 1 = \delta - \eta < \delta$. Cela prouve que $A$ n'admet pas de minimum.
**L'infinimum de $A$ est $0$** Notons $a = \inf A$, et supposons par l'absurde $a>0$. Soit $\varepsilon > 0$ tel que $\varepsilon < a$. Puisque $a$ n'est pas atteint, on peut trouver $n<m$ tels que $a < D(mx) < D(nx) < a + \varepsilon$. On pose $\delta = D(nx) - D(mx) < \varepsilon$

```{prf:lemma}
:nonumber:
Soit $a,b \in \N$. Alors 
\begin{equation*}

D(ax) + D(bx) =
\begin{cases}
D((a+b)x)\\
\textrm{ou} \\
1+D((a+b)x)
\end{cases}
\end{equation*}
```
```{prf:proof}
On écrit $ax = n_a + D(ax)$, $bx = n_b + D(bx)$. Il vient $(a+b)x = n_{a+b} + D((a+b)x) =  n_a + n_b + D(ax) + D(bx)$. Or $0 < D(ax) + D(bx) < 2$ et de là le résultat.
```
````

D'après le lemme on a donc $D(nx) + D((m-n)x) = 1 + D(mx)$, soit $D((m-n)x) = 1 - \delta$. En particulier, $\delta$ est irrationnel. Informellement, ajouter $(m-n)x$ revient à retirer $\delta$ de la partie fractionnaire. En considérant les multiples de $(m-n)$, pn peut ainsi atteindre $1-\delta$, $1-2\delta$, $1-3\delta$, etc. On peut retirer $\delta$ jusqu'à trouver une partie fractionnaire plus petite que $a$. Rendons cet argument formel.

Soit $k = \lfloor \frac{1}{\delta} \rfloor$. Par irrationnalité de $x$, $k\delta < 1$ et $(k+1)\delta > 1$. Notons $\eta = 1-k\delta > 0$ et remarquons que $\eta < \delta < \varepsilon < a$. On écrit
\begin{align*}
k(m-n)x &= k (\lfloor mx \rfloor - \lfloor nx \rfloor) + k(D(mx) - D(nx)) \\
&= k (\lfloor mx \rfloor - \lfloor nx \rfloor) - k\delta \\
&= k (\lfloor mx \rfloor - \lfloor nx \rfloor) -1 + \eta\\
\end{align*}
Ainsi $D(k(m-n)x) = \eta < a$, ce qui est impossible !

2. Par la question $1$, $\{D(n\frac{x}{y}) \; | \; n\in \N \}$ est dense dans $[0,1]$ donc  $\{yD(n\frac{x}{y}) \; | \; n\in \N \}$ est dense dans $[0,y]$. Ensuite $\pi$ est irrationnel donc $\frac{1}{2\pi}$ également, donc $1$ et $2\pi$ sont incommensurables, donc $\{ n \mod{2\pi}\}$ est dense dans $[0,2\pi]$ et cela conclut.

```



```{exercise}
:label: exo-93
Soit $\mathcal{S}$ une famille finie de segment de $\R$, telle que $\forall I,J \in \mathcal{S}, \; I \cap J\neq \emptyset$. Montrer que $\underset{I \in \mathcal{S}}{\bigcap} I \neq \emptyset$. Et si la famille est infinie ?
```

```{solution} exo-93
:class: dropdown
On note $I_1 = [a_1, b_1], I_2 = [a_2, b_2], \ldots, I_n = [a_n, b_n]$ les segments de $\mathcal{S}$. Notons $a = \max a_i = a_{\gamma}$ et $b = \min b_i = b_{\delta}$. Puisque $I_{\gamma}$ et $I_{\delta}$ sont d'intersection non vide, il vient $a \leq b$. On montre alors facilement que $[a,b] \subset\underset{I \in \mathcal{S}}{\bigcap} I \neq \emptyset$. Si la famille est infinie, on remplace $\min$ et $\max$ par $\inf$ et $\sup$ mais les inégalités subsistent.
```



````{exercise}
:label: exo-94
PROOF UNCOMPLETE

Soit $\alpha, \beta \in \R$. On pose $A = \{E(n\alpha) \; | \; n \in \N \}$ et $B = \{E(n\beta) \; | \; n \in \N \}$. Montrer que $A$ et $B$ forment une partition de $\N^*$ si et seulement si $\alpha$ et $\beta$ sont irrationnels et vérifient $\frac{1}{\alpha} + \frac{1}{\beta} = 1$.

```{admonition} Indication
:class: tip
Introduire la fonction de densité d'une partie $P$ de $\N$ $d(P) = \lim Card(P\cap[\![1;n]\!])/n$*.
```
````

```{solution} exo-94
:class: dropdown
Pour le sens retour, on suppose qu'il existe $k = E(na) = E(mb)$. Alors $k < na, mb < k+1$ (les inégalités étant strictes par irrationnalité). On peut alors écrire
\begin{align*}
k &= \frac{k}{a} + \frac{k}{b} \\
&< n+m <\frac{k+1}{a} + \frac{k+1}{b} = k+1
\end{align*}
Ce qui induit une contradiction.

Poiur le sens direct, on remarque que la densité de $A$ est $\frac{1}{a}$, que la densité de $B$ est $\frac{1}{b}$ et que la densité se somme pour l'union disjointe.
```



```{exercise}
:label: exo-95
Montrer que $\R$ et $\R^2$ sont équipotents. En déduire que $\R^a$ et $\R^b$ sont équipotents, pour $a,b \in \N^*$.
```

```{solution} exo-95
:class: dropdown
$\R \cong \{0,1\}^\N$. Il suffit de montrer que $\N \cong \Z$. C'est facile. Cela donne
\begin{equation*}
f : \begin{cases}
\{0,1\}^\N \times  \{0,1\}^\N \rightarrow  \{0,1\}^\N \\
(a_1, a_2, \ldots),(b_1, b_2, \ldots) \mapsto (a_1, b_1, a_2, b_2, \dots)
\end{cases}
\end{equation*}
Ensuite par récurrence $\R \cong \R^n$.
```




```{exercise}
:label: exo-96
Trouver une injection de $\sigma : \R \rightarrow \mathcal{P}(\N)$ telle que $\sigma(x)$ soit infinie pour tout réel $x$, et telle que $\sigma(x)\cap\sigma(y)$ soit finie pour tout $x\neq y$
```
```{solution} exo-96
:class: dropdown
On cherche tout d'abord $\sigma : ]0,1[ \rightarrow \mathcal{P}(\N)$. À un réel d'écriture binaire $0,a_1a_2a_3\ldots$ on associe $\{ \sum a_i2^i \; | \; \forall i \in \N, \; a_i=0\}$. On vérifie que $\sigma$ vérifie les hypothèses voulues. Ensuite il ne reste plus qu'à composer à droite par (par exemple) $1/2(1+\arctan)$ qui envoie injectivement $\R$ sur $]0,1[$.
```















































































 