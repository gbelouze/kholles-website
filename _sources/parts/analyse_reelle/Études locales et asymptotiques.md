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

# Études locales et asymptotiques

```{exercise}
:label: exo-202
Déterminer les $\lambda \in \R$ tels que $\sin(\lambda x) \underset{+\infty}{=} o(\sin(x))$
```

```{solution} exo-202
:class: dropdown
Si $\lambda \neq 0$, $\sin(\lambda x)^{-1}(\{1\})$ est non majoré, donc on nie le petit $o$ avec $\varepsilon = \frac{1}{2}$.
```

```{exercise}
:label: exo-203
Soit $a, b >0$. Déterminer un équivalent de $\ln(\ln(ax + b)) - \ln(\ln(x))$ en $+\infty$.
```

```{solution} exo-203
:class: dropdown
\begin{align*}
\ln(\ln(ax+b)) &= \ln(\ln(ax)+\ln(1+\frac{b}{ax})) \\
&= \ln(\ln(ax))+\ln(1+\frac{\frac{b}{ax}-\frac{b^2}{2(ax)^2}}{\ln(a)+\ln(x)}) \\
&= \ln(\ln(x))+\ln(1+\frac{\ln(a)}{\ln(x)})+o()
\end{align*}
```


```{exercise}
:label: exo-204
Posons $f_0 : x \mapsto 1-x$ et pour tout $n\in \N$,
\begin{equation*}
f_{n+1} = \frac{1}{2-f_n}
\end{equation*}
Déterminer le DL en 0 à l'ordre $m \in \N$ de $f_n$.
```

```{solution} exo-204
:class: dropdown
On remarque que $f_n$ est une homographie. On écrit donc
\begin{equation*}
 f_n =\frac{a_n x -b_n}{c_n x -d_n}
\end{equation*}
ce qui conduit à deux systèmes de deux relations de récurrence mutuellement récursives. On résoud pour trouver $a_n = n-1$, $c_n = n$ et $b_n = d_n = -1$. De là le développement à l'ordre $m$
\begin{equation*}
 f_n(x) \underset{0}{=} 1 + \sum_{k=1}^m (-1)^kn^{k-1}x^k + o(x^m)
\end{equation*}
```

```{exercise}
:label: exo-205
Soit $\alpha > 0$. Trouver une condition nécessaire et suffisante sur $\alpha$ pour que
\begin{equation*}
 e^{(x+1)^{\alpha}} \underset{+\infty}{\sim} e^{x^{\alpha}}
\end{equation*}
```

```{solution} exo-205
:class: dropdown
\begin{align*}
e^{(x+1)^{\alpha}} &= e^{x^{\alpha}(1+\frac{\alpha}{x}+o(\frac{1}{x}))} \\
&= e^{x^{\alpha}} e^{\frac{\alpha}{x^{1-\alpha}}+o(\frac{1}{x^{1-\alpha}})}
\end{align*}
D'où la condition $\alpha < 1$.
```

```{exercise}
:label: exo-206
Trouver $a, b \in \R$ tels que
\begin{equation*}
 a\sin(x)+b\tan(x) \underset{0}{=} x + o(x^5)
\end{equation*}
```

```{solution} exo-206
:class: dropdown
\begin{align*}
\sin(x) &\underset{0}{=} x - \frac{x^3}{3} + o(x^4) \\
\tan(x) &\underset{0}{=} x + \frac{x^3}{3} + o(x^4) \\
&\Leftrightarrow
\begin{cases}
a+b &= 1 \\
-a+2b &= 0 \\
\end{cases} \\
&\Leftrightarrow
\begin{cases}
a &= \frac{2}{3} \\
b &= \frac{1}{3} \\
\end{cases} \\
\end{align*}
```


```{exercise}
:label: exo-207
Déterminer le DL à l'ordre $8$ en $0$ de
\begin{equation*}
 (\cos(x) -1)(\sh(x)-x) - (\ch(x)-1)(\sin(x)-x)
\end{equation*}
```

```{solution} exo-207
:class: dropdown
\begin{align*}
(\cos(x) -1)(\sh(x)-x) &= (-\frac{x^2}{2} + \frac{x^4}{4!} + o(x^5))(\frac{x^3}{3!} + \frac{x^5}{5!}+o(x^6)) \\
(\ch(x)-1)(\sin(x)-x) &= (\frac{x^2}{2} + \frac{x^4}{4!} + o(x^5))(\frac{x^3}{3!} - \frac{x^5}{5!}+o(x^6)) \\
(\cos(x) -1)(\sh(x)-x) - (\ch(x)-1)(\sin(x)-x) &= -\frac{x^5}{6} + o(x^8) \\
\end{align*}
```

```{exercise}
:label: exo-208
Trouver la limite en $+\infty$ de
\begin{equation*}
 \left (  \frac{\ln(x+1)}{\ln(x)} \right )^{x\ln(x)}
\end{equation*}
```

```{solution} exo-208
:class: dropdown
\begin{align*}
\ln(\ln(x+1))-\ln(\ln(x)) &= \ln(\ln(x) + \frac{1}{x}  + o(\frac{1}{x})) - \ln(\ln(x)) \\
&= \ln(1 + \frac{1}{x\ln(x)} + o(\frac{1}{x\ln(x)})) \\
&= \frac{1}{x\ln(x)} + o(\frac{1}{x\ln(x)}) \\
\left (  \frac{\ln(x+1)}{\ln(x)} \right )^{x\ln(x)} &= e^{x\ln(x)(\frac{1}{x\ln(x)} + o(\frac{1}{x\ln(x)}))} \\
&= e^{1+o(1)} \\
\underset{+\infty}{\longrightarrow} e
\end{align*}
```

```{exercise}
:label: exo-209
Déterminer le DL à l'ordre $5$ en $0$ de
\begin{equation*}
 \int_0^x \frac{\sin(t)}{t}dt
\end{equation*}
```

```{solution} exo-209
:class: dropdown
$x - \frac{x^3}{18}+\frac{x^5}{4\times 5!} + o(x^5)$
```



```{exercise}
:label: exo-210
Déterminer le DL à l'ordre $5$ en $0$ de
\begin{equation*}
 (\cos(x))^2
\end{equation*}
```

```{solution} exo-210
:class: dropdown
$1 - x^2 + \frac{x^4}{3} + o(x^5)$
```

```{exercise}
:label: exo-211
Déterminer le DL à l'ordre $3$ en $0$ de
\begin{equation*}
 \frac{\ln(1+x)}{\sin(x)}
\end{equation*}
```

```{solution} exo-211
:class: dropdown
$1-\frac{x}{2}+\frac{x^2}{2}-\frac{x^3}{3} + o(x^3)$
```

```{exercise}
:label: exo-212
Trouver une relation de récurrence sur les coefficients du DL de
\begin{equation*}
 f : x \mapsto e^{\arctan(x)}
\end{equation*}
```

```{solution} exo-212
:class: dropdown
On dérive une fois $f$ pour trouver la relation $f'(x) = (1+x^2)f(x)$. Cette relation se réécrit comme une relation de récurrence sur les coefficients :
\begin{equation*}
 (k+2)a_{k+2} = a_{k+1} + ka_k
\end{equation*}
en utilisant l'unicité du développement limité.
```

```{exercise}
:label: exo-213
Soit $f : x \mapsto x e^{x^2}$. Montrer que $f$ est bijective de $\R$ dans $\R$. Déterminer un développement limité à l'ordre 6 en $0$ de $f^{-1}$.
```

```{solution} exo-213
:class: dropdown
La bijectivité est évidente. Remarquons que la fonction $f$ est impaire. Ainsi $-f^{-1}(f(x))= -x = f^{-1}(f(-x)) = f^{-1}(-f(x))$ donc par surjectivité de $f$ on a pour tout $t \in \R$, $-f^{-1}(t) = f^{-1}(-t)$, bref $f^{-1}$ est impaire et son développement limité en 0 s'écrit donc
\begin{equation*}
 f^{-1}(x) \underset{0}{=} a_1 x + a_3 x^3 + a_5 x^5 + o(x^6)
\end{equation*}
On injecte alors le DL de $f$ et on identifie au DL de l'identité pour finalement trouver
\begin{equation*}
 f^{-1}(x) \underset{0}{=} x - x^3 - \frac{7}{2} x^5 + o(x^6)
\end{equation*}
```

```{exercise}
:label: exo-214
Montrer que $x + \ln(x) = n$ admet une unique solution $x_n$ dans $\R$ et donner un développement asymptotique à trois termes de $x_n$.
```

```{solution} exo-214
:class: dropdown
Existence et unicité sont évidentes. On remarque que $x_n \leq n$ et que $x_n \rightarrow +\infty$. Ensuite il s'agit de développement et de réinjections successives dans l'équation $x_n = n - \ln(x_n)$ pour trouver
\begin{equation*}
 x_n = n -\ln(n) + \frac{\ln(n)}{n} + o(\frac{\ln(n)}{n})
\end{equation*}
```


```{exercise}
:label: exo-215
À l'aide d'une étude asymptotique de $x \mapsto \sqrt{x^4 + x^3 + 1}$, montrer que $\{ (x, y) \in \Z \; | \; y^2 = x^4 + x^3 + 1 \}$ est fini.
```

```{solution} exo-215
:class: dropdown
On obtient le développpement $\sqrt{x^4 + x^3 + 1} \underset{+\infty}{=} x^2 + \frac{x}{2} - \frac{1}{8} + \frac{1}{72x} + o(\frac{1}{x})$. De là pour $n$ assez grand, $| \frac{1}{72n} + o(\frac{1}{n}) | < \frac{1}{8}$. De là l'ensemble est majoré et dans $\Z^2$ donc fini.
```


```{exercise}
:label: exo-216
Montrer pour $n \in \N$ que l'équation
\begin{equation*}
 P_n(x) = x^n + \ldots + x^2 + x -1 = 0
\end{equation*}
admet une unique solution réelle positive $u_n$. Trouver un développement asymptotique à deux dermes de $u_n$.
```

```{solution} exo-216
:class: dropdown
L'unicité vient par stricte croissance sur $\R^+$. L'existence suit du TVI, de la valeur en $0$ et de la valeur en $1$ de $P_n$. Ensuite $x_n$ est strictement décroissante car à $x > 0$ fixé, $(P_n(x))_n$ strictement croissante. Ainsi $x_n$ converge, mettons vers $l \in [0, 1[$. On a donc d'une part $\forall n \in \N, \; P_n(l) < 0$ i.e. $ 1-l^n< 2(1-l)$ donc $ 1 \leq 2(1-l)$ et d'autre part pour tout $\lambda > l$ il existe un rang tel que $P_n(\lambda) > 0$ d'où $\frac{1}{1-\lambda} > 2$. Bref nécessairement $ 1 = 2(1-l)$ puis $l = \frac{1}{2}$.
Par ailleurs on peut toujours écrire $u_n^{n+1}-2u_n +1= 0$. On étudie $\varepsilon_n = u_n - \frac{1}{2}$. On a
\begin{equation*}
 u_n^{n+1}-2\varepsilon_n = 0
\end{equation*}
d'où pour tout $\alpha > 0$, $\varepsilon_n = o((\frac{1}{2}+\alpha)^n)$. En particulier $n\varepsilon_n = o(1)$. On écrit alors
\begin{align*}
2\varepsilon_n &= (\frac{1}{2} + \varepsilon_n)^{n+1} \\
&= e^{(n+1)(\ln(\frac{1}{2}) + \ln(1+2\varepsilon_n)))} \\
&= \frac{1}{2^{n+1}}e^{2(n+1)\varepsilon_n + o(n\varepsilon_n)} \\
&= \frac{1}{2^{n+1}}(1+o(1))
\end{align*}
Et finalement $u_n = \frac{1}{2} + \frac{1}{2^{n+2}} + o(\frac{1}{2^n})$.
```


```{exercise}
:label: exo-217
Trouver $a, b \in \R$ tels que $\cos(x)-\frac{1-ax^2}{1-bx^2} = o(x^n)$ avec $n$ maximal.
```

```{solution} exo-217
:class: dropdown
On trouve $a=-\frac{5}{12}, b =\frac{1}{12}$.
On écrit le DL ce $\cos$ :
\begin{equation*}
 cos(x) = 1 -\frac{1}{2}x^2 + \frac{1}{4!}x^4 - \frac{1}{6!}x^6 + o(x^6)
\end{equation*}
Puis celui de $\frac{1-ax^2}{1-bx^2}$ (après calculs):
\begin{equation*}
 \frac{1-ax^2}{1-bx^2} = 1 + (a-b)x^2 - b(a-b)x^4 + b^2(a-b)x^6 + o(x^6)
\end{equation*}
On a alors
\begin{equation*}
 \cos(x)-\frac{1-ax^2}{1-bx^2} = o(x^n) = (-\frac{1}{2} - (a-b))x^2 + (\frac{1}{24} + b(a-b)) x^4 + (-\frac{1}{720}-b^2(a-b))x^6 + o(x^6)
\end{equation*}
Ce qui conduit aux valeurs annoncées.
```


```{exercise}
:label: exo-218
Soit $f \in \C^2(\R)$ telle que $\forall x, y \in \R^2$,
\begin{equation*}
 f(x-y)f(x+y) \leq f(x^2)
\end{equation*}
Montrer que $\forall x \in \R$,
\begin{equation*}
f(x)f''(x) \leq f'(x)^2
\end{equation*}
```

```{solution} exo-218
:class: dropdown
On applique Taylor-Lagrange à l'ordre 2 sur $f(x-y)$ et $f(x+y)$, puis on multiplie les égalités pour obtenir
\begin{equation*}
 f(x-y)f(x+y)-f(x^2) = y^2(f(x)f''(x) - f'(x)^2) + o(y^2)
\end{equation*}
Puis pour $y$ suffisamment petit, $f(x-y)f(x+y)-f(x^2)$ est du même signe que $f(x)f''(x) - f'(x)^2$.
```

```{exercise}
:label: exo-219
Déterminer
\begin{equation*}
 \inf \{ \sup_{[0,1]} |f''| \; | \; f \in \C^2([0,1], \R), \;f(0)=0, \; f(1)=1, \; f'(0)=f'(1) = 0\}
\end{equation*}
```

```{solution} exo-219
:class: dropdown
Soit $\alpha$ la réponse. Soit $f$ dans l'ensemble décrit. On peut écrire $f(1/2) = f(1-1/2) = f(0+1/2)$. On écrit les deux égalités de Taylor-Lagrange correspondantes
\begin{align*}
f(1/2) &= 1 + \frac{f''(c_1)}{8} \quad &c_1 \in ]1/2, 1[ \\
f(1/2) &=  \frac{f''(c_2)}{8} \quad&c_2 \in ]0, 1/2[ \\
\end{align*}
Selon la position de $f(1/2)$ par rapport à $1/2$, cela apporte $\alpha \geq 4$. Pour l'égalité, on prend l'exemple de $x \mapsto 2x^2$ entre $0$ et $\frac{1}{2}$, et $1-2(x-1)^2$ entre $1/2$ et $1$  (on obtient cet exemple en intégrant deux fois $4$ sur $[0,1/2]$ et $-4$ sur $[1/2, 1]$).

```





































































 