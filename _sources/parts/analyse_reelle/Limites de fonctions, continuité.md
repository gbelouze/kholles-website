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

# Limites de fonctions, continuité


```{exercise}
:label: exo-154
La fonction $x \longmapsto \lfloor x \rfloor + \lfloor -x \rfloor$ admet-elle une limite en $+ \infty$ ?
```

```{solution} exo-154
:class: dropdown
$\forall x \in \mathbb{N}, \; f(x) = 0$ et $f(x+\frac{1}{2}) = -1$ donc $f$ n'admet pas de telle limite.
```



```{exercise}
:label: exo-155
A-t-on $f$ continue sur un segment et jamais identiquement nulle sur un sous-intervalle de ce segment de $\Rightarrow$ $f$ s'annule un nombre fini de fois.
```

```{solution} exo-155
:class: dropdown
Non avec $x\sin(\frac{1}{x})$
```



```{exercise}
:label: exo-156
Soit $f$, $g$ deux fonctions continues de $[0,1]$ dans $\R$ telles que
\begin{equation*}
 \sup f = \sup g
\end{equation*}
Montrer que le graphe de $f$ et le graphe de $g$ se coupent.
```

```{solution} exo-156
:class: dropdown
Par continuité, le sup est atteint. On écrit $s = \sup f = \sup g = f(a) = f(b)$. On a alors $(f-g)(a) \geq 0$ et $(f-g)(b) \leq 0$ donc $f-g$ s'annule.
```



```{exercise}
:label: exo-157

1. Soit $f \; : \; \mathbb{R}^*_+ \longrightarrow  \mathbb{R}$ continue telle que, pour tout $x>0$, la suite $(f(nx))_n$ est croissante. Montrer que $f$ est croissante.
1. Et si on abandonne l'hypothèse de la continuité de $f$ ?

```

```{solution} exo-157
:class: dropdown

1.
    Raisonnons par l'absurde en se donnant $a<b$ tels que $f(a)>f(b)$. Par continuité de $f$, il existe $\varepsilon>0$ tel que $\varepsilon < b-a$ et $\forall x \in [b-\varepsilon, b+\varepsilon], f(a)>f(x)$. Choisissons $N \in \mathbb{N}$ suffisamment grand de sorte que $\frac{a}{N} < 2 \varepsilon$. Alors la suite $(n\frac{a}{N})_n$ contient $a$ et rencontre $[b-\varepsilon, b+\varepsilon]$ donc la suite $(f(n\frac{a}{N}))_n$ n'est pas croissante, ce qui contredit les hypothèses de départ.
2.
    Considérons la fonction $f \; : \; x \longmapsto \mathds{1}_{\mathbb{Q}} $. Pour tout $x$ réel, pour tout $n \in \mathbb{N}^*$, $nx \in \mathbb{Q} \; \longleftrightarrow \; x \in \mathbb{Q}$ donc $\forall x, \, (f(nx))_n$ est constante donc croissante.
```



```{exercise}
:label: exo-158
Trouver les fonctions $f : \R \rightarrow \R$ continues en $1$ vérifiant $\forall x \in \R, \; f(x^2) = f(x)$.
```

```{solution} exo-158
:class: dropdown
On a immédiatement $\forall n \in \N, \; f(x) = f(x^{2^{-n}})$. Or pour $x \neq 0$, $x^{2^{-n}}  \underset{n \rightarrow +\infty}{ \rightarrow} 1$ donc $\forall x \neq 1$, $f(x) = f(1)$. Par continuité en 1. On vérifie immédiatement que les fonctions constantes sur $\R^*$ conviennent.
```



```{exercise}
:label: exo-159
Montrer que deux fonctions d'un intervalle ouvert, croissantes et dont la somme est continue sont continues.
```

```{solution} exo-159
:class: dropdown
Soit $]a,b[$ l'intervalle de définition de $f$ et $g$ et soit $x \in ]a,b[$. On justifie facilement que $\underset{x^-}{\lim} f + \underset{x^-}{\lim} g = \underset{x^-}{\lim} (f+g) = (f+g)(x)$ par continuité de $f+g$. Or $\underset{x^-}{\lim} f \leq f(x)$ et
$\underset{x^-}{\lim} g \leq g(x)$ donc ces deux inégalités sont des égalités. Ceci étant vrai pour tout $x$ et étant facilement montré de la même façon pour la limite en $x^+$, $f$ et $g$ sont continues.
```



```{exercise}
:label: exo-160
Soit $f \; : \; \mathbb{R} \longrightarrow \mathbb{R}$ $T$-périodique et continue. Montrer qu'il existe $a \in \mathbb{R}$ tel que $f(\mathbb{R}) = f([a,a+\frac{T}{2}])$.
```

```{solution} exo-160
:class: dropdown
Soit $a,b \in [0,T]$ tels que $f$ atteigne son minimum et son maximum respectivement en $a$ et $b$. Quitte à remplacer $f$ par $-f$ on peut supposer $a<b$. Si $b-a\leq \frac{T}{2}$, $a$ convient. Sinon $b$ convient.
```



```{exercise}
:label: exo-161
Voir exercice 8.31 du poly de Mansuy. Soit $f \; \: \; \mathbb{R}_+ \longrightarrow \mathbb{R}$ continue et surjective. Montrer que $f^{-1}(\{0\})$ est infini.
Difficulté : */**
```

```{solution} exo-161
:class: dropdown
Montrons que cet ensemble n'est pas majoré. Soit $A>0$, par continuité de $f$, $f[0,A]$ est borné, mettons par $M$. $f$ étant surjective, $M+1$ admet un antécédent, soit $x$, et $-M-1$ admet un antécédent, soit $y$. Nécessairement $x>A$ et $y>A$. Mais par continuité de $f$ et d'après le théorème des valeurs intermédiaires, il existe $z$ entre $x$ et $y$ tel que $f(z)=0$. Cela conclut.
```



```{exercise}
:label: exo-162
Voir exercice 8.28 du poly de Mansuy. Soit $f$ et $g$ deux fonctions continues sur $[0,1]$ telles que
\begin{equation*}
\forall x \in [0,1], \qquad 0 < f(x) <g(x).
\end{equation*}
Montrer qu'il existe $D>C>1$ tels que
\begin{equation*}
\forall x \in [0,1], \qquad Cf(x) < g(x)<Df(x).
\end{equation*}
Difficulté : **
```
```{solution} exo-162
:class: dropdown
On regarde la fonction $\frac{g}{f}$ définie et continue sur le segment $[0,1]$, donc bornée. Notons $m$ son minimum, atteint en $a$ et $M$ son maximum. Par hypothèse, $\frac{g}{f}(a) > 1$ donc $m>1$. $\frac{1+m}{2}$ convient comme valeur de $C$. $M+1$ convient comme valeur de $D$.
```





```{exercise}
:label: exo-163
Voir exercice 8.26 du poly de Mansuy. Déterminer les fonctions $f \; : \; \mathbb{R} \longrightarrow \mathbb{R}$ continues telles que $f(\mathbb{Q}) \subset \mathbb{R} \setminus \mathbb{Q}$ et $f(\mathbb{R} \setminus \mathbb{Q}) \subset \mathbb{Q}$.
Difficulté : *** (nécessite les notions de dénombrabilité)
```

```{solution} exo-163
:class: dropdown
Montrons par l'absurde qu'il n'en existe pas en considérant $f$ convenable. Si $f(\mathbb{Q})$ contient deux éléments distincts, soit $a<b$, alors par continuité de $f$, $[a,b] \subset f(\mathbb{R})$ donc $[a,b] \setminus \mathbb{Q} \subset f(\mathbb{Q})$. Or $[a,b] \setminus \mathbb{Q}$ est indénombrable tandis que $ f(\mathbb{Q})$ est dénombrable. Non! Ainsi $f(\mathbb{Q})={a}$. Mais par densité de $\mathbb{Q}$ dans $\mathbb{R}$ et par continuité de $f$, $f$ est alors constante égale à $a$, ce qui contredit les hypothèses de départ.
```



```{exercise}
:label: exo-164
Soit $f : \R \rightarrow \R$ une fonction continue périodique. Montrer que $f$ est uniformément continue.
```

```{solution} exo-164
:class: dropdown
Notons $T$ la période de $f$. $f$ est uniformément continue sur $[0, 2T]$. Soit $\varepsilon > 0$ et $\alpha < \frac{T}{2}$ de l'uniforme continuité associé à $\varepsilon$ :
\begin{equation*}

\forall x, y \in [0, 2T], |x-y| < \alpha \Rightarrow |f(x)-f(y)|<\varepsilon
\end{equation*}
Soit $x<y$ $\in \R$ tels que  $|x-y| < \alpha$. On écrit la "division euclidienne" $x = nT + b$ où $n \in \N$ et $b < T$, et de même $y = mT + c$. On a $n \leq m \leq m+1$. Il vient $|f(x)-f(y)| = |f(b)-f((m-n)T+c)| < \varepsilon$ car $|b-((m-n)T + c)| = |x-y| < \alpha$ et $0 \leq (m-n)T+c \leq T+c < 2T$.
```





```{exercise}
:label: exo-165
Soit $f$ et $g$ continues de $[0,1]$ dans $[0,1]$ qui commutent. Montrer qu'il existe $x$ tel que $f(x)=g(x)$
```

```{solution} exo-165
:class: dropdown
Par l'absurde $f<g$. Soit $l$ un point fixe de $f$. Il vient $f(g(l))=g(f(l))=g(l)$ donc l'ensemble des points fixes de $f$ est stable par $g$. Considérons $s = \sup \{ l \; | \; f(l)=l\}$, qui existe car cet ensemble est non vide (résultat classique). Par continuité de $f$ on a $f(s)=s$. Puis $g(s) \leq s$ par maximalité de $s$. De là $g(s) \leq s = f(s) < g(s)$. Absurde !
```



```{exercise}
:label: exo-166
Soit $f : \R \rightarrow \R$ croissante et $D$ l'ensemble des points en lesquels $f$ n'est pas continue. Montrer que $D$ est au plus dénombrable.
```

```{solution} exo-166
:class: dropdown
Soit $x \in D$. On a donc $f(x^+)-f(x^-)>0$. On peut donc trouver un rationnel $r_x \in ]f(x^-)-f(x^+)$. On définit ainsi une application injective (car strictement croissante) de $D$ dans $\Q$. Il suit que $D$ est au plus dénombrable.
```



```{exercise}
:label: exo-167
Soit $f$ une fonction de $\mathbb{C}$ dans $ \R$, continue en $0$ et en $1$, telle que $f(1)=1$ et $f(z_1z_2)=f(z_1)f(z_2)$.
1. Montrer que $f$ est strictement positive sur $\C^*$
1. Montrer qu'il un existe un réel $\alpha \geq 0$ tel que $f(x)=x^{\alpha}$ pour $x > 0$.
1. Montrer que $f(e^{it})=1$ pour tout réel $t$.
1. Conclure.

```

```{solution} exo-167
:class: dropdown
1. La positivité est évidente. Soit $z \neq 0$. Supposons par l'absurde $f(z)=0$. Alors pour tout $n \in \N$, on a $f(z^{1/2^n})=0$, donc par continuité en $1$, $f(1)=0$, ce qui est absurde.
1. Soit $g = f_{\R_+^*}$, continue, strictement positive et multiplicative. On peut donc correctement définir $h = \ln(g)$ qui est continue et vérifie $h(ab)=h(a)+h(b)$. Le raisonnement suivant est alors classique : $\forall x>0$, $\forall n \in \N$, $h(x^n) = nh(x)$, puis $h(x^{p/q}) = \frac{p}{q}h(x)$. Par continuité de $h$ et densité des rationnels, cela s'étend à : pour tout $y>0$ $h(x^y) = yh(x)$ et ainsi $h = h(e)\ln$ !
1. Les racines $n$-ièmes de l'unité vérifient $f(z)^n=1$ donc $f(z)=1$. Par densité des racines de l'unité et continuité de $f$, c'est vrai pour tout complexe du cercle unité.
1. $f$ est donc de la forme $\rho e^{it} \mapsto \rho^\alpha$.

```


```{exercise}
:label: exo-168
Soit $f  : \R \rightarrow \R$ uniformément continue et telle que $(f(n))_{n \in \N}$ diverge vers $+\infty$. Montrer que 
\begin{equation*}
f \underset{x \rightarrow +\infty}{\rightarrow} +\infty
\end{equation*}
```

```{solution} exo-168
:class: dropdown
Soit $\delta$ de l'uniforme continuité associé à 1. Soit $M$ tel que $M\delta > 1$. Il vient $\forall n \in \N, \forall n \leq x < n+1$,
\begin{equation*}
 f(x) \geq f(n)-M
\end{equation*}
D'où le résultat.
```

```{exercise}
:label: exo-169
Soit $E,F$ deux espaces vectoriels normés et $f : E \rightarrow F$. On note $Gr(f) = \{(x,y) \in E \times F \; | \; f(x) = y \}$.

1. Montrer que si $f$ est continue, alors $Gr(f)$ est fermé dans $E \times F$.
1. Montrer la réciproque lorsque $f(E)$ est inclus dans un compact de $F$.
1. Trouver un contre-exemple si $f(E)$ n'est pas inclus dans un compact.

```

```{solution} exo-169
:class: dropdown

1. Soit $(x_n, y_n)$ une suite de $Gr(f)$ qui converge vers $(x,y) \in E\times F$. Alors $x_n \rightarrow x$ donc par contuinité de $f$, $y_n = f(x_n) \rightarrow f(x)$, puis par unicité de la limité, $y=f(x)$ et finalement $(x,y) \in Gr(f)$.
1. Soit $x_n$ une suite de $E$ qui converge vers $x\in E$. On pose $y_n = f(x_n)$. Soit $y$ une valeur d'adhérence de $y_n$, associée à une extractrice $\phi$. Alors $(x_{\phi(n)}, y_{\phi(n)})$ est une suite d e$Gr(f)$ qui converge vers $(x,y)$. $Gr(f)$ étant fermé, on a $(x,y) \in Gr(f)$ i.e. $y=f(x)$. Ainsi $y_n$ admet au plus une seule valeur d'adhérence. $f(E)$ étant compacte, $y_n$ en admet au moins une. Finalement $y_n$ admet une et une seule valeur d'adhérence donc converge, vers $f(x)$.
1. Dans $\R$, 
\begin{equation*}
x \mapsto \begin{cases} \frac{1}{x} \quad \textrm{si $x \neq 0$} \\ $0$ \quad \textrm{sinon} \end{cases}
\end{equation*}
 fournit un contre exemple.

```

```{exercise}
:label: exo-170
Soit $f : \R \rightarrow \R$ uniformément continue, bornée, et $g : \R \rightarrow \R$ continue. Montrer que $g \circ f$ est uniformément continue
```

```{solution} exo-170
:class: dropdown
Soit $\varepsilon > 0$. $f(\R)$ est borné inclus dans un segment, mettons $S$. Par Heine, $g$ est uniformément continue sur $S$. Soit $\gamma$ de l'uniforme continuité de $g_{|S}$ associé à $\varepsilon$. Soit $\delta$ de l'uniforme continuité de $f$ associé $\gamma$. Alors
\begin{equation*}
 |x-y| \leq \delta \Rightarrow |f(x) - f(y)| \leq \gamma \Rightarrow |g(f(x)) - g(f(y))| \leq \varepsilon
\end{equation*}
ce qui conclut.
```

```{exercise} {$f([a,b]) \subset g([a,b])$}
:label: exo-171
Soit $f,g : [a,b] \rightarrow \R$ continues. On suppose $\forall x \in [a,b], \exists y \in [a,b], f(x) = g(y)$. Montrer qu'il existe $x\in [a,b]$ tel que $f(x) = g(x)$
```

```{solution} exo-171
:class: dropdown
Par l'absurde $f < g$. $f$ étant continue, il existe $x$ tel que $f(x) = \inf f$. Puis il existe donc $y$ tel que $g(y) = \inf f$. Alors $f(y) < \inf f$ ce qui est impossible.
```

```{exercise} {Cordes de longueur $\frac{1}{n}$}
:label: exo-172
Soit $f : [0,1] \rightarrow \R$ continue telle que $f(0) = f(1) = 0$.

1. Montrer qu'il existe $x \in [0,\frac{1}{2}]$ tel que $f(x) = f(x + \frac{1}{2}$.
1. Pour $n \geq 2$, montrer qu'il existe $x \in [0,1- \frac{1}{n}]$ tel que $f(x) = f(x + \frac{1}{n}$.
1. Trouver une fonction $f$ telle que $\forall x \in [0,1- \frac{2}{5}]$, $f(x) \neq f(x + \frac{2}{5})$.
1. Sans corection ! Montrer qu'il existe $a > 0$, tel que : $\forall b \in ]0,a]$, $\exists x \in [0, 1-b]$ tel que $f(x) = f(x+b)$.

```

```{solution} exo-172
:class: dropdown

1. Soit $g = f(\cdot) - f (\frac{1}{2} + \cdot)$. On a $g(0) + g(\frac{1}{2}) = 0$ donc $g$ touche $0$.
1. Soit $g = f(\cdot) - f (\frac{1}{n} + \cdot)$. On a $g(0) + g(\frac{1}{n}) + \ldots + g(1 - \frac{1}{n}) = 0$ donc $g$ touche $0$.
1. Soit $\phi$ une fonction périodique de plus petite période $T = \frac{2}{5}$, par exemple $\phi(x) = \sin^2(\frac{2\pi x}{5})$. On va ajouter la bonne pente à $\phi$ pour avoir l'égalité en $0$ et $1$ : $f(x) = \phi(x) - x\phi(1)$. Alors écrivons
\begin{align*}
f(x) = f(x+T) &\Leftrightarrow T\phi(1) = 0 \\
&\Leftrightarrow \phi(1) = 0 \\
&\Leftrightarrow \frac{1}{T} \in N
\end{align*}
Ainsi avec n'importe quelle période autre que $\frac{1}{n}$, on peut trouver des contre-exemples (et en l'occurence avec $T = \frac{2}{5}$).

```

```{exercise}
:label: exo-173
Soit $E$ un espace de Banach (espace vectoriel normé complet), et $f : E \rightarrow E$ une fonction $k$-lipschitzienne avec $k < 1$. On choisit $u_0 \in E$ quelconque, et on définit $u_{n+1} = f(u_n)$.

1. Montrer que $u$ converge vers une limite $l$.
1. Montrer que $l$ est le seul point fixe de $f$.

```

```{solution} exo-173
:class: dropdown
1. Par récurrence $||u_{n+1} - u_{n}|| \leq k^n ||u_1 - u_0||$. Donc $u$ est de Cauchy, donc converge.
1. Pour l'unicité, soit $l'$ tel que $f(l') = l'$. Alors $||l'-l|| = ||f(l') - f(l)|| \leq k ||l' -l||$ donc $||l' - l || = 0$. Pour le fait que $l$ est un point fixe, $f$ est lipschitzienne donc continue, donc $f(u_n) \rightarrow f(l)$. Mais $f(u_n) \rightarrow l$ donc $l = f(l)$.
```

```{exercise}
:label: exo-174
Soit $C$ un compact convexe d'un espace vectoriel normé $E$. Soit $f : C \rightarrow C$ 1-lipschitzienne. Montrer que $f$ admet un point fixe. On pourra introduire $f_n : x \mapsto \frac{1}{n}a + (1-\frac{1}{n})f(x)$ pour un $a \in C$ fixé.
```

```{solution} exo-174
:class: dropdown
$f_n$ est bien définie de $C$ dans $C$ car $C$ est convexe, et est $1-\frac{1}{n}$ lipschitzienne, donc admet un point fixe $l_n$. La suite $l_n$ est à valeur dans le compact $C$ donc admet une valeur d'adhérence $l$, associée à une extractrice $\phi$. On remarque que la suite $f_{\phi(n)}(l) = \frac{1}{\phi(n)}a + (1- \frac{1}{\phi(n)})f(l)$ converge vers $f(l)$. Puis
\begin{align*}
||f(l) - l || &\leq ||f(l) - f_{\phi(n)}(l)|| + ||f_{\phi(n)}(l) - f_{\phi(n)}(l_{\phi(n)})|| + ||f_{\phi(n)}(l_{\phi(n)}) - l_{\phi(n)}|| + ||l_{\phi(n)} - l|| \\
&\leq ||f(l) - f_{\phi(n)}(l)||  + (1-\frac{1}{\phi(n)})||l_{\phi(n)} - l|| +  0 +||l_{\phi(n)} - l|| \longrightarrow 0
\end{align*}
D'où $f(l) = l$.
```

```{exercise}
:label: exo-175
Site de Michel Quercia.
Evn :

1. 87. Prendre $k_i \in K_i$ tels que $f(k_i) = x$, remarquer quepour chaque $K_i$ on peut extraire une sous-suite convergente dans $K_i$ et faire l'habituelle composée de dénombrables extractrices.
1. 95
1. 98 avec de Banach (complet) plutôt que de dimension finie, puis 101
1. 102
1. 109. Penser au fait que $||f(\cdot)||$ est continue. Pour la réciproque penser à la caractérisation des applications linéaires continues.
1. Montrer que la norme est continue. Solution : elle est 1-lipschitzienne.

Continu :

1. 30
1. 21
1. 23
1. 17
1. 16

```
































































 