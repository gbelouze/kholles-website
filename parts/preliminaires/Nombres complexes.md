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

# Nombres complexes


```{exercise}
:label: exo-55
Voir les exercices de Gery Huvent 47, 49, 52, 53, 60, 72, 89 (théorème de Napoléon).
```



```{exercise}
:label: exo-56
Résoudre l'équation $z^3 + (i-2)z^2 +(3-3i)z + 2i-2 = 0$ sachant qu'elle admet une solution réelle.
```

```{solution} exo-56
:class: dropdown
Soit $x$ une telle racine réelle. Soit $P(X) = X^3 + (i-2)X^2 + (3-3i)X + 2i -2$. On a donc $P(x)= \overline{P(x)} = 0$. $x$ étant réel,
l'équation précédente amène
\begin{align*}
-ix^2 + 3ix -2i &= ix^2 - 3ix +2i \\
x^2 - 3x + 2 &= 0 \\
(x-1)(x-2) &=0
\end{align*}
On vérifie rapidement que $P(1) = 0$. On obtient ainsi la factorisation $P(X) = (X-1)(X^2 + (i-1)X + 2 - 2i)$ et
on trouve les racines restantes par une étude classique des polynômes du second degré.
```



```{exercise}
:label: exo-57
Résoudre l'équation $z^n = \overline{z}$.
```

```{solution} exo-57
:class: dropdown
$z=0$ convient. On étudie maintenant les solutions dans $\mathbb{C} \setminus \{0\}$. L'équation est alors équivalente à
$z^{n+1} = |z|^2$.

- si n=1, l'équation est équivalente à $z^2 \in \mathbb{R}^+$ soit $z \in \mathbb{R}$.
- sinon, $|z|=1$ est nécessaire. On trouve les racines $n+1$-ièmes de l'unité.
```



```{exercise}
:label: exo-58
Soit $u$, $v$, $w$ $\in \mathbb{U}$, tels que $u+v+w=0$. Montrer que $u=jv=j^2w$ ou bien
$u=jw=j^2v$.
```

```{solution} exo-58
:class: dropdown
Quitte à multiplier par $\overline{u}$ il suffit de montrer que si $v,w \in \mathbb{U}$ vérifient $1+v+w=0$, alors
$\{v,w \} = \{j,j^2\}$.
En passant à la partie imaginaire dans l'équation précédente, il vient que $v$ et $w$ sont de partie imaginaire opposée et donc
de partie réelle de même modèle module. En passant à la partie réelle dans l'équation il vient alors que leur partie réelle commune
est $-\frac{1}{2}$. Le résultat souhaité est alors immédiat.
```



```{exercise}
:label: exo-59
Soit $N \in \N$. On dit que $N$ est somme de deux carrés s'il existe $a,b \in \N, \; a^2+b^2=N$. Montrer que si $N$ est somme de deux carrés, alors pour tout $p \in \N$, $N^p$ est somme de deux carrés.
```

```{solution} exo-59
:class: dropdown
On montre que l'ensemble des sommes de deux carrés est stable par produit. Cela est immédiat en remarquant que $a^2+b^2 = |a+ib|^2 = z\overline{z}$ avec $z = a+ib$ puis en voyant que
$z_1 \overline{z_1} z_2 \overline{z_2} = z_1z_2 \overline{z_1z_2}$.
```



```{exercise}
:label: exo-60
Soit $z \in \mathbb{U}$ tel que $|1-z|<1$. Montrer que $|1+z^2| \geq 1$.
```


```{solution} exo-60
:class: dropdown
On peut écrire $z=e^{i\theta}$ avec $-\frac{\pi}{3} \leq \theta \leq \frac{\pi}{3}$. Alors $2\theta \in [-\frac{2\pi}{3}, \frac{2\pi}{3}]$ d'où le résultat.
INSERT IMAGE HERE
```





```{exercise}
:label: exo-61
Soit $P= \{ z \in \mathbb{C}, \; \mathfrak{Im}(z) > 0 \}$ et $D= \{ z \in \mathbb{C}, \; |z| < 1\}$.

1. Soit $z \in P$. Montrer que $\frac{z-i}{z+i} \in D$.
1. Soit $z \neq -i$ tel que $\frac{z-i}{z+i} \in D$. Montrer que $z \in P$.
1. Montrer que l'application
\begin{equation*}
    \phi \longmapsto \begin{cases}
     P  \; \rightarrow \; D\\

     z \; \mapsto \frac{z-i}{z+i}
    \end{cases}
\end{equation*}
est une bijection et calculer sa réciproque.

```

```{solution} exo-61
:class: dropdown


1.
    Le résultat est immédiat après écriture de $z=a+ib$ car $\left | \frac{z-i}{z+i} \right | = \frac{a^2+(b-1)^2}{a^2+(b+1)^2}$.
1.
    $a^2+(b-1)^2<a^2+(b+1)^2 \leftrightarrow b>0$.
1.
    $u=\frac{z-i}{z+i} \; \text{et} \; u \neq 1 \; \text{et} \; z \neq -i \leftrightarrow z=i\frac{1+u}{1-u}$
```



```{exercise}
:label: exo-62
Inspiré du 3.20 du poly de Mansuy. Trouver le plus grand $\alpha$ tel que
\begin{equation*}
\forall z \in \mathbb{U} \setminus \{1\}, \; \exists n \in \mathbb{N} \text{ tel que } |z^n -1| \geq \alpha \end{equation*}
Indication : On pourra séparer les cas où $z$ est une racine de l'unité.
Difficulté : ***
```

```{solution} exo-62
:class: dropdown
Avec $z=j$, on a la majoration $\alpha \leq \sqrt{3}$. On montre que $\sqrt{3}$ convient. Soit $z \in \mathbb{U} \setminus \{1\}$, et $\theta \in ]0; 1[$ tel que $2 \pi \theta$ soit son argument.

- si $\theta$ est irrationnel, on peut montrer que $\{ z^n, n \in \mathbb{N} \}$ est dense dans $\mathbb{U}$.
    Pour tout $n \in \N^*$ on note $\theta_n \in ]0; 1[$ tel que $2 \pi \theta$ soit l'argument de $z^n$. Regardons $\gamma = \inf_{n \in \N} \theta_n$.

    Supposons $\gamma > 0$. Soit $n > m \in \N$ tels que $\theta_n < 2\gamma$, $\theta_m < 2\gamma$. Si $\theta_n > \theta_m$, alors $\theta_{n-m}= \theta_n-\theta_m < \gamma$ ce qui est impossible. Ainsi $0 < 1 - \theta_{n-m} < \gamma$. Soit $N = \lfloor \frac{1}{1-\theta_{n-m}} \rfloor$. Il vient en passant deux fois au conjugué $0 < \theta_{N(n-m)} < \alpha$ ce qui est une contradiction.

    Ainsi $\gamma = 0$ et de là $\{ z^n, n \in \mathbb{N} \}$ est soit fini (inf atteint), soit dense dans $\mathbb{U}$ (inf non atteint). Par irrationnalité de
    $\theta$ l'ensemble est dense. En particulier $\sup_{n \in \N} |z^n -1| = 2$ donc il existe $n \in \N$ tel que $|z^n -1| \geq \sqrt{3}$
- sinon, $z$ est une racine de l'unité et est donc générateur de $\mathbb{U}_m$ avec $m \geq 2$ car $z \neq 1$. Avec l'étude précédente de $j$, il suffit de vérifier que
\begin{equation*}
\forall n \geq 2, \; \min \{\mathcal{R}e(z), z \in \mathbb{U}_n \} \leq -\frac{1}{2}
\end{equation*}
Ce résultat est vrai pour $n=2$, et tient nécessairement pour $n \geq 3$ pour assurer $\frac{2\pi}{n} \leq \frac{2\pi}{3}$ où $\frac{2\pi}{3}$ est l'ouverture angulaire de la zone
$\{\mathcal{R}e(z) \leq -\frac{1}{2} , z \in \mathbb{U} \} $.
```



```{exercise}
:label: exo-63
Soit $z_1, \ldots, z_n$ des complexes de modules inférieurs ou égaux à 1.
Montrer qu'il existe $\varepsilon_1, \ldots, \varepsilon_n \in \{ -1, 1\}$ tels que $|\varepsilon_1 z_1 + \ldots + \varepsilon_n z_n | \leq \sqrt{2}$.
```

```{solution} exo-63
:class: dropdown
On raisonne par récurrence. Lorsque $n=2$, on écrit
\begin{align*}
|z_1-z_2|\times|z_1+z_2| &= |z_1^2-z_2^2|\\
&\leq 2
\end{align*}
Pour $n=3$, les complexes $\pm z_1, \pm z_2, \pm z_3$ forment les sommets d'un hexagone (non croisé quitte à permuter les $z_i$). Un des angles au centre est donc inférieur à $\frac{\pi}{3}$. Le demi-côté correspondant est donc de longueure inférieure à $\sin(\pi/6)=1/2$ ce qui fournit $z_i, \varepsilon_j, z_j$ tels que $|z_i + \varepsilon_jz_j| \leq 1$. Cela permet de faire la récurrence.
```




```{exercise}
:label: exo-64
Soit $z_1, \ldots, z_n \in \C$. Montrer que
\begin{equation*}
 \frac{| \sum_{k=1}^n z_k |}{1 + | \sum_{k=1}^n z_k | } \leq \sum_{k=1}^n \frac{|z_k|}{1+|z_k|}
\end{equation*}
```
```{solution} exo-64
:class: dropdown
Croissance de $x \mapsto \frac{x}{1+x}$ et récurrence.
```




```{exercise}
:label: exo-65
Soit $u,v \in \C$ et $z= u + iv$. Trouver une condition nécessaire et suffisante pour que $|z|^2 = u^2 + v^2$.
```
```{solution} exo-65
:class: dropdown
L'identité suivante est toujours vérifiée
\begin{equation*}
 (u+iv)(u-iv) = u^2+v^2
\end{equation*}
La conditon se réécrit donc
\begin{equation*}
(u+iv)(u-iv) = (u+iv)(\bar{u}-i\bar{v})
\end{equation*}
Si $z \neq 0$, cela implique $(u-\bar{u}) = i(v-\bar{v})$. Or le terme de gauche est un réel, et le terme de droite un imaginaire pure. Cela amène ainsi $u,v \in \R$. Bref la condition recherchée est $z=0$ ou $u,v \in \R$.
```





```{exercise}
:label: exo-66
Calculer $\sum_{k=0}^{n-1} (1+w^k)^n$ où $w$ est une racine primitive $n$-ième de l'unité.
```
```{solution} exo-66
:class: dropdown
On écrit pour $w\neq 1$
\begin{align*}
\sum_{k=0}^{n-1} (1+w^k)^n &= 2^n + \sum_{k=1}^{n-1} \sum_{l=0}^n{n \choose l}w^{kl} \\
&=  2^n + 2n -2 + \sum_{l=1}^{n-1}{n \choose l}\frac{w^l-w^{nl}}{1-w^l} \\
&= 2^n + 2n - \sum_{l=0}^n{n \choose l} \\
&= 2n
\end{align*}
```













































































 