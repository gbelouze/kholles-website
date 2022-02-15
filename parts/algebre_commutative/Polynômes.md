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

# Polynômes

```{exercise}
:label: exo-292
Montrer que les fonctions trigonométriques ne sont pas des polynômes
```

```{solution} exo-292
:class: dropdown
On dérive pour $\cos$ et $\sin$, et on regarde l'équation $\tan^2 = 1 + \tan'$ pour $\tan$.
```

```{exercise}
:label: exo-293
Montrer que le polynôme $\sum_{k=0}^{2n} \frac{X^k}{k!}$ n'admet pas de racine réelle.
```

```{solution} exo-293
:class: dropdown
$P$ tend vers $+\infty$ en $\pm \infty$ donc $P$ atteint son $\inf$, mettons en $a$. On a aussi $P = P' + \frac{X^2n}{(2n)!}$ d'où $P(a) = \frac{a^{2n}}{(2n!)}$ qui est strictement positif, sauf si $a=0$, cas que l'on peut rejeter à la main. Remarque : l'idée de dériver est naturelle par analogie avec l'exponentielle.
```

```{exercise}
:label: exo-294
Soit $P$ un polynôme de $\C[X]$. Déterminer $P(\C)$
```

```{solution} exo-294
:class: dropdown
Si $deg(P) > 0$, le polynôme $P - z$ admet une racine complexe pour tout $z \in \C$ donc $P(\C) = \C$. Sinon, $P(\C) = P(0)$.
```


```{exercise}
:label: exo-295
Résoudre dans $\C[X]$ l'équation $P(X^2)=P(X)P(X+1)$.
```

```{solution} exo-295
:class: dropdown
On procède par analyse synthèse. On a $r$ racine implique $r^2$ racine et $(r-1)^2$ racine. On suppose $P$ non nul. Cela amène à trouver les $E$ ensembles finis stables par $x \mapsto x^2$ et par $x \mapsto (x-1)^2$. Soit un tel $E$. On a $\forall z \in E, \; |z| \in \{0,1\}$. Puis en regardant $|z-1|^2$ pour $z\neq 0, z \neq 1$, on montre que $E \subset \{ 0, 1, -j, -\bar{j} \}$. La stabilité par carré impose $E \subset \{ 0, 1\}$. À partir de là la synthèse est facile et on trouve $0, 1, X^n(X-1)^n$ pour $n \in \N$.
```

```{exercise} Gauss-Lucas
:label: exo-296
Montrer que les racines de la dérivée d'un polynôme sont comprises dans l'enveloppe convexe des racines de ce polynôme. Conséquence : Soit $P$ polynôme dont un des coefficients est nuls. Montrer que $0$ appartient à l'enveloppe convexe des racines de $P$.
```

```{solution} exo-296
:class: dropdown
On dérive $\log(P)$. Pour la conséquence, $0$ est racine de la dérivée $k-ième$ dont les racines sont incluses dans l'enveloppe convexe de $P$ par Gauss-Lucas itéré.
```

```{exercise} Régionnement
:label: exo-297
Soit $P = X^n + a_{n-1}X^{n-1} + \ldots + a_0$. Montrer que
\begin{equation*}
 \max \{ |z|, \; z \in Z(P) \} \leq 1 + \underset{0 \leq i \leq n-1 }{\max} |a_i|
\end{equation*}
Conséquence :
Soit $(P_k) \in \C_n[X]$ une suite de polynômes unitaires à coefficients bornés par $M$. Montrer qu'il existe une extractrice $\phi$ telle que $Z(P_{\phi(k)})$ converge.
```

```{solution} exo-297
:class: dropdown
On pose $\mu = \underset{0 \leq i \leq n-1 }{\max} |a_i|$. Soit $z \in Z(P)$. On a $|z|^n \leq \sum_{k=0}^{n-1} |a_k||z_k| \leq \mu \frac{|z|^n-1}{|z|-1}$ si $|z| \neq 1$. Supposons $|z| > 1$ Il vient
\begin{equation*}
 |z|^n(|z|-1) \leq \mu (|z|^n-1) \leq \mu|z|^n
\end{equation*}
Et de là le résultat. La conséquence est immédiate.
```

```{exercise}
:label: exo-298
Soit $P \in \Q[X]$ tel que $1+\sqrt{2}$ soit une racine de $P$. Calculer $P(1-\sqrt{2})$.
```

```{solution} exo-298
:class: dropdown
On regarde le polynôme minimal de l'idéal des polynôme qui s'annulent en $1+\sqrt{2}$.
```

```{exercise}
:label: exo-299
Soit $F$ une partie fermée de $\C$ et $P_k = X^n + a_{n-1,k}X^{n-1} + \ldots + a_{0,k}$ une suite de polynôme tels que
\begin{equation*}
\begin{cases}
    a_{l,k} \rightarrow a_l\\
    Z(P_k) \subset F
\end{cases}
\end{equation*}
On note $P = \sum_{l=0}^na_lX^l$. Montrer que $Z(P) \subset F$.
```

```{solution} exo-299
:class: dropdown
Soit $a \in \C \setminus F$. On a pour tout $k$,
\begin{equation*}
 |P_k(a)| = \prod_{j=1}^n |a-z_{j,k}| \geq d(a, F)^n > 0
\end{equation*}
À la limite, $|P(a)| \geq d(a, F)^n > 0$.
```

```{exercise}
:label: exo-300
Montrer que tout polynôme positif sur $\R$ est somme de deux carrés.
```

```{solution} exo-300
:class: dropdown
D'abord on remarque que l'ensemble des polynômes sommes de deux carrés est stable par produit (cf exercice de complexes). Puis si $P = X^2 + 2aX +b$ est irréductible, on a $a^2-b < 0$. De là $P = (X+a)^2+(\sqrt{b-a^2})^2$. Puis si $P$ admet $x$ pour racine, $P \sim_{x} \lambda(X-x)^{\alpha}$. Il vient $\lambda > 0$ et $\alpha$ pair. Cela conclut.
```

```{exercise}
:label: exo-301
Déterminer les polynômes $P$ tels que $P'$ divise $P$.
```

```{solution} exo-301
:class: dropdown
Ok avec d'Alembert Gauss. Sinon on explicite la relation $P=QP'$ de divisibilité et on dérive $k$ fois pour $k$ plus petit que $n$ et on évalue en la racine de $Q$. Ou encore avec les fractions rationnelles et en regardant $\frac{P'}{P}$, $P$ a une seule racine.
```

```{exercise}
:label: exo-302
Soit P un polynôme tel que les restes de la division euclidienne de $P$ par $(X - 1)$ , $(X - 2)$ et $(X - 3)$ soient $3$, $7$ et $13$ respectivement. Déterminer le reste de la division euclidienne de $P$ par $(X-1)(X-2)(X-3)$ .
```

```{solution} exo-302
:class: dropdown
Ce reste $R$ est de degré au plus $2$ et coïncide avec l'interpolateur de Lagrange associé à $(1,3), (2,7), (3,13)$ en $3$ points, donc ces deux polynômes sont égaux.
```

```{exercise}
:label: exo-303
Soit $P \in \C[X]$, on suppose que pour tout $x \in \R$, $P(x) \in \R$. Montrer que $P \in \R[X]$.
```

```{solution} exo-303
:class: dropdown
Par exemple avec un polynôme interpolateur de Lagrange sur $deg(P)+1$ points réels. Ou sinon avec le polynôme $\bar{P}$
```


```{exercise}
:label: exo-304
Déterminer $m>0$ tel que le polynôme $X^4-(3m+2)X^2+m^2$ ait ses racines en progression arithmétique.
```

```{solution} exo-304
:class: dropdown
$P$ est pair donc ses racines sont réparties autour de $0$. Ainsi il existe $a>0$ tel que $-3a, -a, a, 3a$ sont les racines de $P$. Ainsi $P=(X^2-9a^2)(X^2-a^2) = X^4 - 10a^2 +9a^4$. On a donc
\begin{equation*}
\begin{cases}
10a^2 &= 3m+2 \\
9a^4 &= m^2
\end{cases}
\end{equation*}
De là $m = 3a^2$ puis $a=\sqrt{2}$, ce qui correspond à $m=6$.
```


```{exercise}
:label: exo-305
Résoudre l'équation $4P=(X-1)P'+P''$.
```

```{solution} exo-305
:class: dropdown
Soi t$n$ le degré de $P$. On écrit $P = a_nX^n+Q$ avec $deg(Q<n)$. En réinjectant dans l'équation on a
\begin{equation*}
4a_nX^n-na_nX^n+R=0
\end{equation*}
avec $deg(R)<n$, d'où $n=4$. Ensuite après dérivations successives de l'équation et évaluation en $1$, on obtient $4P(1)=P''(1)$, $3P'(1)=P^{(3)}(1)$, $2P''(1)=P^{(4)}(1)$ et $P^{(3)}(1)=P^{(5)}(1)=0$, d'où $P'(1)=0$. On effectue un développement de Taylor en $1$ pour obtenir
\begin{equation*}
 P(X) = P(1) \left (1 +2(X-1)^2+\frac{1}{3}(X-1)^4 \right )
\end{equation*}
On vérifie que tous les polynômes de cette forme conviennent.
```

```{exercise}
:label: exo-306
Soit $P \in \R[X]$ unitaire. Montrer que $P$ est scindé dans $\R[X]$ si et seulement si
\begin{equation*}
 \forall z \in \C, \; |P(z)| \geq |\Im(z)|^{deg(P)}
\end{equation*}
```

```{solution} exo-306
:class: dropdown
$(\Rightarrow) \;$ On écrit $P = \prod(X-a_i)$, avec $a_i \in \R$. On évalue en $z = x+iy$ :
\begin{align*}
|P(z)| &= \prod |(x-a_i) + iy| \\
&\geq \prod |y| =  |\Im(z)|^{deg(P)}
\end{align*}
$(\Leftarrow) \;$ Si $P$ admet une racine non réelle, on a une contradiction en évaluant en cette racine. On conclut avec D'Alembert-Gauss.
```


```{exercise}
:label: exo-307
Soit $P$ un polynôme de degré $n$ tel que $\forall k \in \{ 0, 1, \ldots, n\}, \; P(k)=\frac{k}{k+1}$. Calculer $P(n+1)$.
```

```{solution} exo-307
:class: dropdown
On regarde $Q = (X+1)P-X$, de degré $n+1$ et nul en $0,1,\ldots, n$. Il vient $Q = a\prod_{i=0}^n(X-i)$. Mais $Q(-1)=1$ donc $a=\frac{(-1)^{n+1}}{(n+1)!}$. De là $P(n+1) = \frac{n+1+Q(n+1)}{n+2} = \frac{n+1+(-1)^{n+1}}{n+2}$
```

```{exercise}
:label: exo-308
Déterminer les $P$ tels que
\begin{equation*}
 P(\cos(t)) + P(\sin(t))=1
\end{equation*}
```

```{solution} exo-308
:class: dropdown
En remplaçant $t$ par $-t$, il vient que $P(X)$ et $(P-X)$ coïncident sur une infinité de valeurs, donc $P$ est pair. Ainsi $P$ s'écrit comme un polynômr en $X^2$, notons le $Q$, qui vérifie
\begin{equation*}
 Q(\cos^2(t)) + Q(\sin^2(t))=1
\end{equation*}
donc $Q(X)+Q(1-X)=1$. Ainsi, $R=Q(X+\frac{1}{2})-\frac{1}{2}$ est impair (penser au centre de symétrie du graphe de $Q$). On peut donc écrire $R=XU(X^2)$.

Réciproquement ça marche (mais il reste un peu de calcul).
```



```{exercise}
:label: exo-309
Soit $f$ une fonction localement polynomiale, i.e. $\forall x \in \R$, $\exists \varepsilon > 0, P_x \in \R[X]$, $f = P_x$ sur $]x-\varepsilon, x+\varepsilon[$. Montrer que $f$ est un polynôme.
```

```{solution} exo-309
:class: dropdown
Si elle ne l'est pas, soit $s = \inf \{ x > 0 \; | \; f(x) \neq \P_0(x)\}$. Par hypothèse, $s > 0$. Or $P_s$ et $P_0$ coïncident sur un intervalle, donc $P_s = P_0$, donc $s$ n'est pas l'infinimum.
Remarque : avec le théorème de Baire, l'hypothèse plus faible $\forall x, \exists n, f^{(n)}(x) = 0$ suffit.
```












































































 