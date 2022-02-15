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

# Réduction

```{exercise}
:label: exo-403
Montrer que pour tout permutation $\sigma \in \Sigma_n$, la matrice de permutation $P_{\sigma}$ est diagonalisable.
```

```{solution} exo-403
:class: dropdown
Elle vaut l'identité élevée à une certaine puissance.
```


```{exercise}
:label: exo-404
Soit $M$ la matrice de Zoro inversée ($Z$ symétrique, avec des $1$ sur la diagonale). Calculer les puissances de $M$. Montrer que $M$ est semblable à $Id-e_{1,1}+e_{n,n}$ (matrice diagonale).
```

```{solution} exo-404
:class: dropdown
On regarde le rang de $M, M-Id, M-2Id$.
```

```{exercise}
:label: exo-405
Soit $u$ un endomorphisme tel que $u^2$ est diagonalisable. Montrer que $u$ est diagonalisable si et seulement si $Ker(u)=Ker(u^2)$.
```

```{solution} exo-405
:class: dropdown
Sens retour. On exhibe $P=X\prod(X-a_i)$ scindé à racines simples et annulateur de $u^2$. On pose $Q =X^2 \prod(X-\sqrt{a_i})(X+\sqrt{a_i})$ et $Q^* = \frac{Q}{X}$. On regarde $E=Ker(P(u^2)) = Ker(Q(u)) = \oplus_{i} Ker(u^2-a_iI)+Ker(u^2)=Ker(u)\oplus_{i} Ker(u-\sqrt{a_i}I) + Ker(u+\sqrt{a_i}I)$. Donc $Q^*(u)=0$ et $Q^*$ est scindé à racines simples : $u$ est diagonalisable.

Sens aller. On possède une base de vecteurs propres de $u$, donc stables par $u^2$.
```

```{exercise}
:label: exo-406
Montrer que la famille des $e^{\lambda x}$ est libre. Même question pour $\cos(\lambda x)$, $\lambda>0$.
```

```{solution} exo-406
:class: dropdown
Les voir comme des vecteurs propres.
```



















































































 