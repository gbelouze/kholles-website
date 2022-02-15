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

# Séries numériques

```{exercise}
:label: exo-143
Soit $(u_n)$ telle que $u_{n+1} = o(u_n)$. Montrer que $\sum_{k \geq n} u_k \sim u_n$.
```

```{solution} exo-143
:class: dropdown
On se place à $n$ suffisamment grand pour que $|u_{n+1}| \leq \varepsilon |u_n|$. Alors $\sum_{k \geq n+1} |u_k| \leq \frac{\varepsilon}{1-\varepsilon} |u_n|$ et de là $\sum_{k \geq n+1} u_k = o(u_n)$. Le résultat suit naturellement.
```


```{exercise}
:label: exo-144
Soit $(u_n)$ une suite de réels positifs et \begin{equation*}
 v_n = \frac{u_n}{1+u_n} \end{equation*}

Montrer que les séries de terme général $u_n$ et $v_n$ sont de même nature.
```

```{solution} exo-144
:class: dropdown
On a $0 \leq v_n \leq u_n$ donc $\sum u_b$ converge $ \Rightarrow \sum v_n$ converge.
On suppose que $v_n$ converge. Alors $v_n \rightarrow 0$ donc $u_n \rightarrow 0$ et $ v_n = u_n (1 + o(1)) = u_n + o(u_n)$. Supposons par l'absurde que $u_n$ diverge, alors $\sum o(u_n) = o(\sum u_n)$ donc $\sum v_n \sim \sum u_n$ diverge. Non!
```


```{exercise}
:label: exo-145
Soit $(u_n)$ une suite réelle telle que la série de terme général $(u_n)$ diverge. Montrer qu'il existe $(v_n)$ telle que $v_n = o(u_n)$ et telle que la série de terme général $(v_n)$ diverge.
```

```{solution} exo-145
:class: dropdown
Raisonner sur les sommes partielles (par exemple prendre $V_n = \ln(U_n)$).
```


```{exercise}
:label: exo-146
Montrer qu'il existe $(u_n) \in \R^{\N}$ telle que pour tout $\lambda \in \overline{\R}$, il existe $\phi$ un réordonnement de $\N$ (bijection de $\N$ dans $\N$) tel que  $\sum \limits_{n=1}^{+ \infty} u_{\phi(n)} = \lambda$.
```

```{solution} exo-146
:class: dropdown
Prendre $u_n = \frac{(-1)^n}{n}$.
```


```{exercise}
:label: exo-147
Soit $ \sum u_n$ une série réelle convergente mais pas absolument convergente. Montrer que pour tout $\lambda \in \bar{\R}$, il existe $\sigma$ une bijection de $\N$ dans $\N$ telle que $\sum_{\sigma(n)} \rightarrow \lambda$.
```

```{exercise}
:label: exo-148
Soit $\sigma$ une permutation de $\N$ dans $\N$. Montrer que la série de terme général $(\frac{\sigma(n)}{n^2})$ diverge.
```

```{solution} exo-148
:class: dropdown
$S_{2n}-S_n$ est minoré par $\frac{1}{8}$ (majorer grossièrement $\frac{1}{k^2}$) donc le critère de Cauchy n'est pas vérifié.
```


```{exercise}
:label: exo-149
Soit $(u_n)$ une suite réelle positive telle que la série de terme général $u_n$ diverge. Soit $\alpha > 0$. Étudier la nature de la série $\frac{u_n}{U_n^{\alpha}}$.
```

```{solution} exo-149
:class: dropdown

```


```{exercise}
:label: exo-150

1. Soit $u_n$ une suite décroissante vers $0$ telle que $\sum u_n$ converge. Montrer que $u_n = o(\frac{1}{n})$.
1. Exhiber une suite réelle positive $u_n$ telle que la série de terme général $u_n$ converge mais telle que $nu_n$ ne tende pas vers $0$

```

```{solution} exo-150
:class: dropdown
On a $0 < (2n)u_{2n} \leq 2 \sum_{k = n+1}^{2n} u_k = 2(S_{2n}-S_n) \rightarrow 0$. De là $2nu_{2n} \rightarrow 0$ et il vient facilement $u_n = o(u_n)$.
Puis prendre $u_n = \frac{1}{n}$ si $n$ est un carré, $0$ sinon.
```



```{exercise}
:label: exo-151
Soit $\frac{p_n}{q_n}$ convergeant vers un irrationnel. Montrer que $p_n \rightarrow +\infty$ et $q_n \rightarrow +\infty$.
```

```{exercise}
:label: exo-152
Soit $(z_n)$ une suite de complexe de partie réelle positive, et telle que les séries de terme général $z_n$ et $z_n^2$ (respectivement) convergent. Montrer que $\sum |z_n|^2$ converge. Et si on abandonne l'hypothèse partie réelle positive ?
```


```{exercise}
:label: exo-153

1. Équivalent de $\ln(n!)$.
1. Déterminer $\lim_{a\to+\infty}\sum_{n=1}^{+\infty}\frac{a}{n^2+a^2}$.
1. Série de Bertrand un cran plus loin $\frac{1}{n \ln(n) \ln(\ln(n))^{\alpha}}$
1. $u_n$ et $v_n$ tg de séries réelles convergentes, $w_n$ telle que $u_n \leq w_n \leq v_n$. Montrer que $w_n$ tg d'une série convergente (regarder d'abord $w_n - u_n$).
1. Condition sur $a$, $b$ et $c$ pour que la série de terme général $u_n = a\sqrt{n} + b \sqrt{n-1} + c\sqrt{n-2}$ converge. Calculer sa limite dans ce cas.
1. (voir Marc Sage) Soit $\phi : \N \rightarrow \N$ injective, et $\mu_n$ le ppcm de $\phi(1)$, $\phi(2)$, \ldots $\phi(n)$. Montrer que la série de terme général $\frac{1}{\mu_n}$ converge.
1. Soit $z_n$ une suite de complexe espacés d'au moins 1 deux à deux. Trouver $\alpha$ tel que la série de terme général $\frac{1}{n^\alpha z_n}$ converge absolument.
1. Avec les sommes de Riemann : calculer la limite de la série de terme général $(-1)^n\frac{\ln(n)}{n}$
1. Soit $f : \R^*_+ \rightarrow \R^*_+$ de classe $C^1$ et telle que $\frac{f'}{f}$ tende vers $-\infty$ en $+\infty$. Montrer ue la série de terme général $f(n)$ converge et calculer un équivalent de $R_n$ le reste.
1. En utilisant Taylor-Lagrange sur $x \mapsto \ln(1+x)$, calculer la limite de la série de terme général $\frac{(-1)^n}{n}$ (c'est $\ln(2)$). Retrouver le même résultat en remarquant que $\frac{1}{k} = \int_0^1 t^{k-1}dt$.
1. Calculer $\sum_{0}^{+\infty}kx^k$

```































































 