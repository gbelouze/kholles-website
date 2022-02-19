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

# Matrices

```{exercise}
:label: exo-375
Déterminer le centre de $\M_n(\R)$ (les matrices qui commutent avec tout le monde).
```

```{solution} exo-375
:class: dropdown
Soit $A$ une matrice du centre. Soit $1 \leq i,j \leq n$. $(E_{i,j}A)_{k,l} = \sum_{u=1}^n \delta_{k=i, u=j}A_{u,l} = \delta_{k=i}A_{j,l}$. Ainsi seule la ligne $i$ de $E_{i,j}A$ est non nulle, et est égale à la ligne $j$ de $A$. De même, seule la colonne $j$ de $AE_{i,j}$ est non nulle, et est égale à la $i$-ième colonne de $A$. Ainsi $AE_{i,j}-E_{i,j}A=0$ implique $\forall i \neq j$, $A_{i,j}=0$ et $A_{i,i}=A_{j,j}$. Ainsi les seules matrices possibles sont les $\lambda I_n$, et on vérifie qu'elles conviennent.
```

```{exercise}
:label: exo-377
Soit $E=\Vect(\sin,\cos,\ch,\sh)$. Donner la matrice de l'opérateur de dérivation dans la base canonique $\B = (\sin,\cos,\ch,\sh)$.
```

```{solution} exo-377
:class: dropdown
\begin{equation*}
begin{pmatrix}
0 & 0 & 0 \\
1 &  0 & 0 & 0 \\
0 &  0 & 0 & 1 \\
0 &  0 & 1 & 0 \\
\end{pmatrix}
\end{equation*}
```

```{exercise}
:label: exo-378
Calculer $A^n$ pour
\begin{equation*}
A =
\begin{pmatrix}
1 & 2 & 1 \\
0 & 1 & 2 \\
0 & 0 & 1 \\
\end{pmatrix}
\end{equation*}
```

```{solution} exo-378
:class: dropdown
On écrit $A = I_3 + B$, où 
\begin{equation*}
B=
\begin{pmatrix}
0 & 2 & 1 \\
0 & 0 & 2 \\
0 & 0 & 0 \\
\end{pmatrix}
\end{equation*}
On calcule :

\begin{equation*}
B^2 =
\begin{pmatrix}
0 & 0 & 4 \\
0 & 0 & 0 \\
0 & 0 & 0 \\
\end{pmatrix}
\end{equation*}
De là,
\begin{align*}
A^n &= \sum_{k=0}^n {n \choose k} B^k I_3^{n-k} \\
&= I_3 + nB + \frac{n(n-1)}{2}B^2 \\
&= \begin{pmatrix}
1 & 2n & n(2n-1) \\
0 & 1 & 2n \\
0 & 0 & 1 \\
\end{pmatrix}
\end{align*}
```

```{exercise}
:label: exo-379
Soit
\begin{equation*}
J_n =
\begin{pmatrix}
1 & 1 & \ldots & 1 \\
0 & 1 & \ldots & 1 \\
\vdots & \ddots & \ddots & 1 \\
0 & \ldots & 0 & 1 \\
\end{pmatrix}
\end{equation*}
Calculer l'inverse de $J_n$
```

```{solution} exo-379
:class: dropdown
C'est un cas particulier de
\begin{equation*}
\begin{pmatrix}
1 & a & \ldots & a^{n-1} \\
0 & 1 & \ddots & \vdots \\
\vdots & \ddots & \ddots & a \\
0 & \ldots & 0 & 1 \\
\end{pmatrix}
\end{equation*}
avec $a=1$, et le cas particulier se calcule facilement.
```

```{exercise}
:label: exo-380
Soit 
\begin{equation*}
A_n=
\begin{pmatrix}
1 & a & \ldots & a^{n-1} \\
0 & 1 & \ldots & \vdots \\
\vdots & \ddots & \ddots & a \\
0 & \ldots & 0 & 1 \\
\end{pmatrix}
\end{equation*}
Calculer l'inverse de $A_n$.
```

```{solution} exo-380
:class: dropdown
Notons
\begin{equation*}
A = \begin{pmatrix}
0 & a & \ldots & 0 \\
0 & 0 & \ddots & \vdots \\
\vdots & \ddots & \ddots & a \\
0 & \ldots & 0 & 0 \\
\end{pmatrix} \end{equation*}
Alors $A$ est $n$-nilpotente et $A_n = \sum_{k=0}^{n-1} A^k$. Par analogie avec les sommes géométriques réelles, l'inverse est $I-A$.
```


```{exercise}
:label: exo-381
Montrer l'équivalence
\begin{equation*}
 A \textrm{ antisymétrique } \Leftrightarrow \forall X \in \R^n, \; X^TAX = 0
\end{equation*}
```

```{solution} exo-381
:class: dropdown
On commence par le sens retour. Avec $X = e_i$, on obtient $A_{i,i}=0$. Puis avec $i \neq j$,
\begin{align*}
0 &= (e_i + e_j)^T A (e_i+e_j) \\
&= e_i^TAe_i + e_j^TAe_j + e_i^TAe_j + e_j^TAe_i \\
&= e_i^TAe_j + e_j^TAe_i \\
&= A_{i,j} + A_{j,i} \\
\end{align*}

Pour le sens aller, on a pour tout $i,j$, $e_i^TAe_j = 0$ donc cela reste vrai pour tout $X$.
```

```{exercise}
:label: exo-382
Soit $\phi$ l'endomorphisme de transposition de $\M_n(\C)$. Calculer $det(\phi)$.
```

```{solution} exo-382
:class: dropdown
On peut être malin et dire que dans si $B_1$ est une base des matrices symétriques, $B_2$ des matrices antisymétriques, alors $B = (B_1,B_2)$ est une base de $\M_n(\C)$ dans laquelle $\phi$ est diagonale, avec exactement $|B_2|=\frac{n(n-1)}{2}$ occurrences de $-1$. Sinon on exprime $\phi$ dans la base canonique. C'est un matrice de permutation d'un certain $\sigma \in S_{n^2}$, donc $det(\phi) = \epsilon(\sigma)$. La décomposition de $\sigma$ en produit de cycles à support disjoint est un produit de transpositions. Seuls les $(E_{i,i})$ sont stables par $\sigma$, il y a donc $\frac{n^2-n}{2}$ transpositions, d'où le déterminant $(-1)^{\frac{n(n-1)}{2}}$.
```

```{exercise}
:label: exo-383
Soit $A$ un anneau, $n \in A$ un nilpotent. Montrer que $e_A + n$ est inversible. En déduire que l'ensemble des matrices triangulaires supérieures avec des $1$ sur la diagonale est stable par passage à l'inverse.
```

```{solution} exo-383
:class: dropdown
On s'inspire du développement en série entière de $\frac{1}{1+x}$ : soit $k$ l'ordre de nilpotence de $n$
\begin{equation*}
 (e_A+n)(\sum_{i=0}^{k-1} (-n)^i) = e_A + n^k = e_A
\end{equation*}
```

```{exercise}
:label: exo-384
Soit $\Delta = Diag(a_1, \ldots, a_n) \in \M_n(\R)$. Soit $M \in \M_n(\R)$. Calculer $\Delta M - M\Delta$.
```

```{solution} exo-384
:class: dropdown
\begin{align*}
(\Delta M - M\Delta)_{l,k} &= (a_l-a_k)M_{l,k} \\
\end{align*}
```

```{exercise}
:label: exo-385
Soit $x,\theta \in \R$. Calculer les puissances de la matrice
\begin{equation*}
\begin{pmatrix}
x+\sin(\theta) & \cos(\theta) \\
\cos(\theta) & x - \sin(\theta)
\end{pmatrix}
\end{equation*}
```

```{solution} exo-385
:class: dropdown
On note 
\begin{equation*}
M_{\theta} =
\begin{pmatrix}
\sin(\theta) & \cos(\theta) \\
\cos(\theta) & -\sin(\theta)
\end{pmatrix}
\end{equation*}

Calculons ses puissances :

\begin{equation*}
M_{\theta}^2 =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
\end{equation*}
Ainsi
\begin{align*}
M^m &= (xI_n + M_{\theta})^m \\
&= \sum_{k=0}^m {m \choose k} x^{m-k}M_{\theta}^{k} \\
&= (\sum_{k=0}^m {m \choose 2k} x^{m-2k})I_n + (\sum_{k=0}^{m}{m \choose 2k+1} x^{m-2k-1})M_{\theta}
\end{align*}
On doit pouvoir mettre en forme en regardant $S_1 = \sum_{k=0}^{m}{m \choose 2k} x^{2k}$ et $S_2 = \sum_{k=0}^{m}{m \choose 2k+1} x^{2k+1}$. On a
\begin{equation*}
\begin{cases}
S_1+S_2 &= (1+x)^k \\
S_1-S_2 &= (1-x)^k
\end{cases}
\end{equation*}
D'où $S_1 = \frac{(1+x)^k+(1-x)^k}{2}$ et $S_2 = \frac{(1+x)^k-(1-x)^k}{2}$. En regardant la parité de $m$ cela permet d'écrire une forme un peu plus compacte.
```

```{exercise}
:label: exo-386
Résoudre dans $\M_n(\R)$ l'équation
\begin{equation*}
X+X^T = tr(X)A
\end{equation*}
```

```{solution} exo-386
:class: dropdown
On passe à la trace qui amène l'équation $2tr(X)=tr(X)tr(A)$. Si $tr(X)=0$, on est conduit $X$ antisymétrique et on vérifie que cela fonctionne. Sinon, si $tr(A)\neq 2$, il n'y a pas de solution. Sinon, si $A$ n'est pas symétrique il n'y a pas de solution. Sinon, l'équation se traduit sur les coefficients de $X$ : pour un certain $\lambda \in \R$ (ce sera la trace de $X$), $\forall i,j, \; x_{i,j} + x_{j,i} = \lambda a_{i,j}$. On vérifie que le respect de ces conditions satisfait l'équation générale.
```

```{exercise}
:label: exo-387
Soit $A \in \M_n(\C)$ à diagonale dominante, i.e. $\forall i, \; |a_{i,i}| > \sum_{j \neq i} |a_{i,j}|$. Montrer que $A$ est inversible.
```

```{solution} exo-387
:class: dropdown
Il suffit de montrer que $A$ est injective. Or il vient très naturellement (écrire le système) que $AX=0 \Leftrightarrow X=0$.
```

```{exercise}
:label: exo-388
Déterminer les réels $\lambda$ tels qu'il existe une matrice non nulle $A\in \M_n(\R)$ vérifiant $A^T = \lambda A$.
```

```{solution} exo-388
:class: dropdown
En transposant l'équation on obtient la condition $\lambda^2 = 1$. On vérifie que $\lambda=1$ et $\lambda=-1$ conviennent (matrices symétriques et antisymétriques).
```

```{exercise}
:label: exo-389
Soit $M \in \M_n(\R)$, calculer $JMJ$ où $J$ est la matrice dont tous les cooefficients sont égaux à $1$.
```

```{solution} exo-389
:class: dropdown
\begin{equation*}
(\sum_{i,j} m_{i,j}) J
\end{equation*}

```

```{exercise}
:label: exo-390
Soit $A \in \M_n(\R)$ telle que $A^n=0$ et $A^{n-1}\neq 0$. Soit $u$ l'endomorphisme canoniquement associé à $A$. Montrer qu'il existe $x_0$ tel que $\mathcal{B}(x_0) =(u^{n-1}(x_0), \ldots, u(x_0), x_0)$ soit une base de $\R_n$. Quelle est la matrice de $u$ dans cette base ?
```

```{solution} exo-390
:class: dropdown
$x_0$ tel que $A^{n-1}X_0 \neq 0$ convient et existe par hypothèse.
\begin{equation*}
 mat_{\mathcal{B}(x_0)}(u) =
\begin{pmatrix}
0 & 1 & 0 & \ldots  \\
0 & 0 & \ddots & \ddots  \\
0 & \ldots & 0 & 1  \\
0 & \ldots & \ldots & 0 \\
\end{pmatrix}
\end{equation*}
```



```{exercise}
:label: exo-391
Déterminer le sous-espace de $\M_n(\R)$ engendré par $GL_n(\R)$.
```

```{solution} exo-391
:class: dropdown
Il s'agit de $\M_n(\R)$, en remarquant par exemple que $I_n + E_{i,j}$ est inversible.
```

```{exercise}
:label: exo-392
Soit $M \in \R^n$ matrice définie par
\begin{equation*}
\begin{cases}
M_{i,j} = {j-1 \choose i-1} \; \textrm{si } i \leq j \\
M_{i,j} = 0 \; \textrm{sinon}
\end{cases}
\end{equation*}
Soit $u$ l'endomorphisme de $\R_n[X]$ canoniquement associé. Calculer $u(P)$ pour tout $P$. En déduire que $M$ est inversible et calculer son inverse. Montrer que $M^{-1} = \Delta M \Delta$ pour un certain $\Delta$ diagonale.
```

```{solution} exo-392
:class: dropdown
On calcule $u(X^k)$ pour $k \leq n$.
\begin{equation*}
 u(X^k) = \sum_{i=1}^k {k-1 \choose i-1} X^i = (X+1)^k
\end{equation*}
D'où $u : P(X) \mapsto P(X+1)$. $u$ est donc inversible, d'inverse $u^{-1} : P(X) \mapsto P(X-1)$ et l'inverse de $M$ est définie par
\begin{equation*}
\begin{cases}
M^{-1}_{i,j} = (-1)^{(i-1)(j-1)} {j-1 \choose i-1} \; \textrm{si } i \leq j \\
M^{-1}_{i,j} = 0 \; \textrm{sinon}
\end{cases}
\end{equation*}
On calcule pour
\begin{equation*}
\Delta =
\begin{pmatrix} d_1 & 0 & 0 \\
0 & \vdots & 0 \\
0 & 0 & d_n \\
\end{pmatrix}
\end{equation*}
$(\Delta M \Delta)_{i,j} = d_i d_j M_{i,j}$. Ainsi $d_k = (-1)^{k-1}$ donne la bonne matrice diagonale.
```



```{exercise}
:label: exo-393
Montrer que toute matrice $M$ de $\M_n(\R)$ admet un polynôme annulateur. Montrer que si $A \in \M_n(\R)$ est inversible, alors $A^{-1}$ est un polynôme en $A$.
```

```{solution} exo-393
:class: dropdown
$M^0, M^1, \ldots, M^{n^2}$ est liée. Si $P(A)=0$ on écrit $P=X^k\times Q$ avec $Q \land X=1$. D'où l'existence de $U, V$ tels que $U(X)Q(X)+XV(X)=1$. Or par inversibilité de $A^k$, $Ker(Q(A))=Ker(Q(A)A^k)=\R^n$ donc $Q(A)=0$. De là $AV(A)=I_n$.
```

```{exercise}
:label: exo-394
Montrer que tout hyperplan $H$ de $\M_n(\R)$ ($n \geq 2$) contient une matrice inversible.
```

```{solution} exo-394
:class: dropdown
On écrit $f(A)=\sum_{i,j} \alpha_{i,j}A_{i,j}$ telle que $H=Ker(f)$. S'il existe un coefficient $\alpha_{i,j}$ en dehors de la diagonale, non nul, on prend $M=I+\alpha E_{i,j}$ avec $\alpha$ bien choisi pour que $M\in H$. Sinon on trouve une matrice inversible avec des $0$ sur sa diagonale, elle est dans $H$.
```

```{exercise}
:label: exo-395
Soit $A \in M_n(\R)$ non inversible. Montrer qu'il existe une matrice $B$ telle que $\forall \lambda \in \R^*$, $A+\lambda B$ est inversible.
```

```{solution} exo-395
:class: dropdown
Par équivalence en passant par $J_r$ on se ramène à $A$ triangulaire stricte. $B=I_n$ convient alors.
```

```{exercise}
:label: exo-396
Montrer que toute matrice nilpotente est de trace nulle.
```

```{solution} exo-396
:class: dropdown
On montre par récurrence qu'elle est semblable à une matrice triangulaire supérieure stricte. Le noyau est non trivial donc on peut choisir une base de sorte que la première colonne soit nulle. Puis si $N$ est la matrice de taille $n-1$, en bas à droite, un calcul par bloc montre que $N$ est nilpotente.
```

```{exercise}
:label: exo-397
Soit $A \in \M_n(\R)$. Montrer que pour $r>0$ suffisamment petit, $A+rI$ est inversible.
```

```{solution} exo-397
:class: dropdown
$det(A+rI)$ est un polynôme en $r$, non nul d'après l'exercice des matrices à diagonales dominantes, donc ne s'annule pas sur une voisinage de $0$, $0$ exclu.
```






















































































 