> [!question]+ 题目2
>
>Suppose $a\in\mathbf F$, $v\in V$, and $av=0$. Prove that $a=0$ or $v=0$.

> [!success]- 证明
>
> 分为两种情况。
>
> **情况一：$a=0$**
>
> 此时结论已经成立。
>
> **情况二：$a\neq0$**
>
> 因为 $\mathbf F$ 是数域，所以非零标量 $a$ 存在乘法逆元 [[Section 1A#multiplicative inverse|multiplicative inverse]]
$a^{-1}$，且
>
> $$
> a^{-1}a=1.
> $$
>
> 因为 $av=0$，所以
>
> $$
> \begin{aligned}
> v
> &=1v\\
> &=(a^{-1}a)v\\
> &=a^{-1}(av)\\
> &=a^{-1}0\\
> &=0.
> \end{aligned}
> $$
>
> 因此，当 $a\neq0$ 时，必有 $v=0$。综上，
>
> $$
> \boxed{av=0\implies a=0\ \text{或}\ v=0.}
> $$

> [!question]+ Question3
>
>Suppose $v,w\in V$. Explain why there exists a unique $x\in V$ Such that $v+3x=w$.

> [!success]+ Solution
>
> Let $x=\dfrac13(w-v)$. We will show that $x$ is the unique solution.
> 
>Since $-v\in V$, the definition of addition in [[Section 1B### 1.19 definition: addition, scalar multiplication|1.19]] gives $w+(-v)\in V$. Since $\dfrac13\in\mathbf F$, the definition of scalar multiplication in [[Section 1B### 1.19 definition: addition, scalar multiplication|1.19]] then gives $x=\dfrac13(w+(-v))\in V$.
> **Existence**
>
> By the properties of a vector space and the definition of vector subtraction,
>
> $$
> \begin{aligned}
> v+3x
> &=v+3\left(\frac13(w-v)\right)\\
> &=v+\left(3\cdot\frac13\right)(w-v)
> &&\text{(1)}\\
> &=v+(w-v)
> &&\text{(2)}\\
> &=v+\bigl(w+(-v)\bigr)
> &&\text{(3)}\\
> &=\bigl(v+(-v)\bigr)+w
> &&\text{(4)}\\
> &=0+w
> &&\text{(5)}\\
> &=w.
> &&\text{(6)}
> \end{aligned}
> $$
>
> Thus $x$ is a solution.
>
> (1) [[Section 1B#associativity|associativity of scalar multiplication]].
>
> (2) [[Section 1A#multiplicative inverse|complex multiplicative inverse]] and [[Section 1B#multiplicative identity|the multiplicative identity property]].
>
> (3) [[Section 1B#vector-subtraction|definition of vector subtraction]].
>
> (4) [[Section 1B#commutativity|commutativity of addition]] and [[Section 1B#associativity|associativity of addition]].
>
> (5) [[Section 1B#additive inverse|the additive inverse property]].
>
> (6) [[Section 1B#commutativity|commutativity of addition]] and [[Section 1B#additive identity|the additive identity property]].
>
> **Uniqueness**
>
> Let $y\in V$ be any solution, so that
>
> $$
> v+3y=w.
> $$
>
> Adding $-v$ to both sides gives
>
> $$
> (-v)+(v+3y)=(-v)+w.
> $$
>
> Using associativity and commutativity of addition, the additive inverse and identity properties, and the definition of subtraction, we obtain
>
> $$
> 3y=w-v.
> $$
>
> Hence
>
> $$
> \begin{aligned}
> y
> &=1y\\
> &=\left(\frac13\cdot3\right)y\\
> &=\frac13(3y)\\
> &=\frac13(w-v)\\
> &=x.
> \end{aligned}
> $$
>
> Here we use  [[Section 1B#multiplicative identity|the multiplicative identity property]], [[Section 1A#multiplicative inverse|complex multiplicative inverse]], and  [[Section 1B#associativity|associativity of scalar multiplication]].
>
> Therefore every solution equals $x$, so the solution is unique.

> [!question]+ Question5
>
>Show that in the definition of a vector space[[Section 1B#1.20 Definition Vector Space|1.20]], the additive inverse
>condition can be replaced with the condition that $0v=0$ for all $v \in V$. Here the 0 on the
>left side is the number 0, and the 0 on the right side is the additive identity of $V$. 

> [!success]- Solution
>
> We keep all the other conditions in [[Section 1B#1.20 Definition Vector Space|1.20]] unchanged and prove both implications.
>
> **From the original condition to the new condition**
>
> Assume that every element of $V$ has an additive inverse.
>
> Let $v\in V$. By the distributive property,
>
> $$
> \begin{aligned}
> 0v
> &=(0+0)v\\
> &=0v+0v.
> \end{aligned}
> $$
>
> Let $z\in V$ be the additive inverse of $0v$, so that $z+0v=0$. Adding $z$ to both sides and using associativity gives
>
> $$
> \begin{aligned}
> z+0v&=z+(0v+0v),\\
> 0&=(z+0v)+0v,\\
> 0&=0+0v,\\
> 0&=0v.
> \end{aligned}
> $$
>
> Thus $0v=0$ for every $v\in V$.
>
> **From the new condition to the original condition**
>
> Assume that $0v=0$ for every $v\in V$.
>
> Let $v\in V$ and define $w=(-1)v$. By the definition of scalar multiplication, $w\in V$.
>
> Using the multiplicative identity property, the distributive property, and the assumed condition, we obtain
>
> $$
> \begin{aligned}
> v+w
> &=v+(-1)v\\
> &=1v+(-1)v\\
> &=\bigl(1+(-1)\bigr)v\\
> &=0v\\
> &=0.
> \end{aligned}
> $$
>
> Hence $w$ is an additive inverse of $v$. Since $v$ was arbitrary, every element of $V$ has an additive inverse.
>
> Therefore the additive inverse condition can be replaced by the condition that $0v=0$ for every $v\in V$.

> [!question]+ Question 6
>
> Let $\infty$ and $-\infty$ denote two distinct objects, neither of which is in $\mathbf R$. Define an addition and scalar multiplication on $\mathbf R\cup\{\infty,-\infty\}$ as you could guess from the notation. Specifically, the sum and product of two real numbers is as usual, and for $t\in\mathbf R$ define
>
> $$
> t\infty=
> \begin{cases}
> -\infty & \text{if }t<0,\\
> 0 & \text{if }t=0,\\
> \infty & \text{if }t>0,
> \end{cases}
> \qquad
> t(-\infty)=
> \begin{cases}
> \infty & \text{if }t<0,\\
> 0 & \text{if }t=0,\\
> -\infty & \text{if }t>0,
> \end{cases}
> $$
>
> and
>
> $$
> \begin{aligned}
> t+\infty
> &=\infty+t=\infty+\infty=\infty,\\
> t+(-\infty)
> &=(-\infty)+t=(-\infty)+(-\infty)=-\infty,\\
> \infty+(-\infty)
> &=(-\infty)+\infty=0.
> \end{aligned}
> $$
>
> With these operations of addition and scalar multiplication, is $\mathbf R\cup\{\infty,-\infty\}$ a vector space over $\mathbf R$? Explain.

> [!success]- Solution
>
> No. Addition is not associative.
>
> Indeed, by the given definitions,
>
> $$
> \begin{aligned}
> (\infty+(-\infty))+1
> &=0+1=1,\\
> \infty+((-\infty)+1)
> &=\infty+(-\infty)=0.
> \end{aligned}
> $$
>
> Since $1\neq0$, the associativity requirement in 1.20 fails. Therefore $\mathbf R\cup\{\infty,-\infty\}$, with the given operations, is not a vector space over $\mathbf R$.

> [!question]+ Question 7
>
> Suppose $S$ is a nonempty set. Let $V^S$ denote the set of functions from $S$ to $V$. Define a natural addition and scalar multiplication on $V^S$, and show that $V^S$ is a vector space with these definitions.

> [!success]+ Solution
>
> ### Operations
>
> For $f,g\in V^S$, define their *sum* $f+g$ by
>
> $$
> (f+g)(x)=f(x)+g(x)
> $$
>
> for every $x\in S$.
>
> For $\lambda\in\mathbf F$ and $f\in V^S$, define the *product* $\lambda f$ by
>
> $$
> (\lambda f)(x)=\lambda f(x)
> $$
>
> for every $x\in S$.
>
> The operations on the right-hand sides are those in $V$. Since their values belong to $V$, these formulas define functions from $S$ to $V$. Thus $f+g,\lambda f\in V^S$.
>
> We now verify the properties in 1.20.
>
> ---
> ### 1. Commutativity
>
> Let $f,g\in V^S$. For every $x\in S$, we have
>
> $$
> \begin{aligned}
> (f+g)(x)
> &=f(x)+g(x)\\
> &=g(x)+f(x)\\
> &=(g+f)(x).
> \end{aligned}
> $$
>
> The second equality follows from commutativity of addition in $V$. The other equalities follow from the definition of addition on $V^S$.
>
> Thus $f+g=g+f$, because the two functions agree at every element of $S$.
> 
> ---
> ### 2.Associativity
>
> Let $f,g,h\in V^S$ and $a,b\in \mathbf F$. $\forall x\in S$, we have
> 
>**Additon**
> $$
> \begin{aligned}
> ((f+g)+h)(x)
> &=(f+g)(x)+h(x)\\
> &=(f(x)+g(x))+h(x)\\
> &=f(x)+(g(x)+h(x))\\
> &=f(x)+(g+h)(x)\\
> &=(f+(g+h))(x).
> \end{aligned}
> $$
> The third equality follows from associativity of addition in $V$, since $f(x),g(x),h(x)\in V$. The other equalities follow from the definition of addition on $V^S$.
> 
> ---
>
>### 3.Scalar Multiplication
> $$
> \begin{aligned}
> ((ab)f)(x)
> &=(ab)f(x)\\
> &=a(bf(x))\\
> &=a((bf)(x))\\
> &=(a(bf))(x)\\
> \end{aligned}
> $$
> The second equality follows from associativity of scalar multiplication in $V$, since $f(x)\in V$. The other equalities follow from the definition of scalar multiplication in $V^S$.
>
> Since both identities hold at every $x\in S$, we obtain $(f+g)+h=f+(g+h)$ and $(ab)f=a(bf)$.
> ### additive identity
>
> Define $z:S\to V$ by $z(x)=0_V$ for every $x\in S$, where $0_V$ is the additive identity of $V$. Then $z\in V^S$.
>
> For any $f\in V^S$ and every $x\in S$, we have
>
> $$
> (f+z)(x)=f(x)+z(x)=f(x)+0_V=f(x).
> $$
>
> The last equality follows from the additive identity property in $V$.
>
> Thus $f+z=f$, because the two functions agree at every element of $S$. Therefore $z$ is an additive identity of $V^S$.
> 
> ### additive inverse
>
> Let $f\in V^S$.  Define $g:S\to V$ by $g(x)=-f(x)$ for every $x\in S$. Since  $f(x)\in V$, its additive inverse $-f(x)$ belongs to $V$. Thus $g\in V^S$.
> 
> For every $x\in S$, we have
>
> $$
> (f+g)(x)=f(x)+g(x)=f(x)+(-f(x))=0_V=z(x).
> $$
>
> The penultimate equality follows from the additive inverse property in $V$.
>
> Thus $f+g=z$, because the two functions agree at every element of $S$. Therefore $g$ is an additive inverse of $f$.
> ### multiplicative identity
> Let  $f\in V^S$. For every $x\in S$, we have 
> $$
> (1f)(x) = 1f(x) = f(x).
> $$ 
> The first equality follows from the definition of scalar multiplication on $V^S$, and the second follows from the multiplicative identity property in $V$. 
> 
> Thus $1f = f$, because the two functions agree at every element of $S$.
> ### distributive properties
> Let $f,g\in V^S$ and $a,b\in \mathbf F$. For every $x\in S$, we have 
> $$\begin{aligned}
> (a(f+g))(x)
> &=a(f(x)+g(x))\\
> &=af(x)+ag(x)\\
> &=(af)(x)+(ag)(x)\\
> &=(af+ag)(x)
> \end{aligned}$$
>  
> $$\begin{aligned}
> ((a+b)f)(x)
> &=(a+b)f(x)\\
> &=af(x)+bf(x)\\
> &=(af)(x)+(bf)(x)\\
> &=(af+bf)(x)
> \end{aligned}$$
> In each calculation, the second equality follows from a distributive property in $V$. The other equalities follow from the definitions of addition and scalar multiplication on $V^S$.
>
> Since these equalities hold for every $x\in S$, we obtain $a(f+g)=af+ag$ and $(a+b)f=af+bf$.
> ##### Therefore, with the addition and scalar multiplication defined above, $V^S$ is a vector space over $\mathbf F$.

































