# 常微分方程解法大全：一阶线性方程

[jykyyds：常微分方程解法大全：二阶及高阶微分方程5 赞同 · 0 评论文章![](https://pic3.zhimg.com/equation_ipico.jpg)](https://zhuanlan.zhihu.com/p/500907396)

[jykyyds：常微分方程解法大全：微分方程组18 赞同 · 0 评论文章![](https://pic4.zhimg.com/equation_ipico.jpg)](https://zhuanlan.zhihu.com/p/500910043)

* * *

线性方程
----

### 方程1（线性方程）

$y'+p(x)y=g(x).$

**解法.** $\left(ye^{-\int p(x)\mathrm d x}\right)'=\left(y'+p(x)y\right)e^{-\int p(x)\mathrm d x}=g(x)e^{-\int p(x)\mathrm d x}$

$\implies y=e^{\int p(x)\mathrm d x}\left(C+\int g(x)e^{-\int p(x)\mathrm d x}\mathbb d x\right).$

### 方程2（Bernoulli方程）

$\frac{\mathrm dy}{\mathrm dx}+P(x)y=Q(x)y^n(n\not=0,1).$

**解法.** $\frac{\mathrm dy}{\mathrm dx}+P(x)y=Q(x)y^n\implies y^{-n}\frac{\mathrm dy}{\mathrm dx}+P(x)+y^{1-n}=Q(x)$ ,

令 $z=y^{1-n}$ ，则 $\frac{\mathrm dz}{\mathrm dx}=(1-n)y^{-n}\frac{\mathrm dy}{\mathrm dx}$ ，故 $\frac{\mathrm dz}{\mathrm dx}+(1-n)P(x)z=(1-n)Q(x)$ ，这是一个线性方程，可以使用方程1的解法.

* * *

变量可分离方程
-------

### 方程3（变量可分离方程）

$\frac{\mathrm dy}{\mathrm dx}=\frac{f(x)}{g(y)}.$

**解法.** $\frac{\mathrm dy}{\mathrm dx}=\frac{f(x)}{g(y)}\implies g(y)\mathrm dy=f(x)\mathrm dx\implies\int g(y)\mathrm dy=\int f(x)\mathrm dx.$

### 方程4（齐次方程）.

$\frac{\mathrm dy}{\mathrm dx}=F(\frac yx).$

**解法.** 令 $z=\frac yx$ ，则 $\frac{\mathrm dy}{\mathrm d x}=z+x\frac{\mathrm dz}{\mathrm dx}=F(z)$ ，这是一个变量可分离方程.

### 方程5（可化为齐次方程的方程）

$\frac{\mathrm dy}{\mathrm dx}=f(\frac{ax+by+c}{a_1x+b_1y+c_1}).$

**解法.** 当 $c=c_1=0$ 时，此方程就是齐次方程.

当 $c^2+c_1^2\not=0$ 且 $\Delta=\begin{vmatrix}a&amp;b\\a_1&amp;b_1\end{vmatrix}\not=0$ 时，二元方程组$\begin{cases}ax+by+c=0\\a_1x+b_1y+c_1=0\end{cases}$ 有唯一解 $x=\alpha,y=\beta$ ，令 $x=\xi+\alpha,y=\eta+\beta$ ，方程可化为齐次方程 $\frac{\mathrm d\eta}{\mathrm d\xi}=\frac{a\xi+b\eta}{a_1\xi+b_1\eta}$ .

当 $c^2+c_1^2\not=0$ 且 $\Delta=\begin{vmatrix}a&amp;b\\a_1&amp;b_1\end{vmatrix}=0$ 时，存在实数 $\lambda$ 使得 $a_1=\lambda a,b_1=\lambda b$ 或 $a=\lambda a_1,b=\lambda b_1$ ,不妨设是前者，令 $z=ax+by$ ，则 $\frac{\mathrm dz}{\mathrm dx}=a+b\frac{\mathrm dy}{\mathrm dx}=a+bf(\frac{z+c}{\lambda z+c_1}).$

### 方程6（特殊方程）

$\frac{\mathrm dy}{\mathrm dx}=f(ax+by+c).$

**解法.** 令 $z=ax+by$ ，则 $\frac{\mathrm dz}{\mathrm dx}=a+bf(z+c)$ ，这是一个变量可分离方程.

* * *

全微分方程
-----

### 方程7（全微分方程）

$M(x,y)\mathrm dx+N(x,y)\mathrm dy=0,$

满足 $\frac{\partial M}{\partial y}=\frac{\partial N}{\partial x}$ 或存在 $F(x,y)$ 使得 $\mathrm dF(x,y)=M(x,y)\mathrm dx+N(x,y)\mathrm dy.$

**解法.** 设 $F(x,y)=\int M(x,y)\mathrm dx+\varphi(y)$ ，则

$\mathrm dF(x,y)=M(x,y)\mathrm dx+\frac{\partial}{\partial y}\left(\int M(x,y)\mathrm dx\right)\mathrm dy+\varphi'(y)=M(x,y)\mathrm dx+N(x,y)\mathrm dy,$

解得 $\varphi(y)$ ，带入 $F(x,y)$ 中，则方程的通解为 $F(x,y)=C.$

### f方程8（存在仅依赖于 $x$ 的积分因子的微分方程）

$M(x,y)\mathrm dx+N(x,y)\mathrm dy,$ 满足 $\frac{\frac{\partial N}{\partial y}-\frac{\partial N}{\partial x}}N$ 仅与 $x$ 有关.

**解法.** 积分因子为 $\mu(x)=\exp\left({\int\frac{\frac{\partial N}{\partial y}-\frac{\partial N}{\partial x}}N\mathrm dx}\right),$ 此时方程 $\mu(x)M(x,y)\mathrm dx+\mu(x)N(x,y)\mathrm dy=0$ 是全微分方程.

### 方程9（存在仅依赖于 $y$ 的积分因子的微分方程）

$M(x,y)\mathrm dx+N(x,y)\mathrm dy=0,$ 满足 $\frac{\frac{\partial N}{\partial x}-\frac{\partial M}{\partial y}}M$ 仅与 $y$ 有关.

**解法.** 积分因子为 $\mu(y)=\exp\left(\int\frac{\frac{\partial N}{\partial x}-\frac{\partial M}{\partial y}}M\mathrm dy\right),$ 此时方程 $\mu(y)M(x,y)\mathrm dx+\mu(y)N(x,y)\mathrm dy=0$ 是全微分方程.

**注记.** 以上两种方程的求解公式过于复杂，考试时建议自行推导求解公式，以下给出方程8解法的公式推导：

设 $\mu(x)$ 是微分方程 $M(x,y)\mathrm dx+N(x,y)\mathrm dy=0$ 的积分因子，则

$\frac{\partial(\mu M)}{\partial y}=\frac{\partial(\mu N)}{\partial x}\implies\mu\frac{\partial M}{\partial y}=\mu\frac{\partial N}{\partial x}+\mu'N,$

解 $\mu$ 关于 $x$ 的一阶线性方程可得方程8的求解公式.

### 常用积分因子

方程 $x\mathrm dy-y\mathrm dx=0$ 的常见积分因子为 $\frac1{xy},\frac1{x^2+y^2},\frac1{x^2-y^2}$ ，因为

$x\mathrm dy-y\mathrm dx=xy\mathrm d\left(\log\vert\frac yx\vert\right)=(x^2+y^2)\mathrm d\left(\arctan(1+\frac yx)\right)=(x^2-y^2)\mathrm d\left(\frac12\log\vert\frac{x+y}{x-y}\vert\right),$

当微分方程中出现 $x\mathrm dy-y\mathrm dx$ 时，可以尝试上述三式.

### 方程10（分组求积分因子）

$(x^3y-2y^2)\mathrm dx+x^4\mathrm dy=0.$

**解法.** 首先将方程分组为 $(x^3y\mathrm dx+x^4\mathrm dy)-2y^2\mathrm dx=0,$ 利用积分因子分别求解两组方程的通积分可得

$x^3y\mathrm dx+x^4\mathrm dy=x^3\mathrm d(xy),y^2\mathrm dx=y^2\mathrm dx$ ，从而 $x^3\mathrm d(xy)=2y^2\mathrm dx\implies\frac{\mathrm d(xy)}{(xy)^2}=\frac{2\mathrm dx}{x^5}$ ，

对右侧等式两边同时求积分可得方程的通解.

* * *

变量替换法
-----

本节主要凭借观察，无具体的通用解法.

### 方程11（Riccati方程）

$\frac{\mathrm dy}{\mathrm dx}=P(x)y^2+Q(x)y+R(x).$

**解法.** 若已知方程的一个特解 $y=\phi(x)$ ，令 $y=z+\phi(x)$ 可得

$\frac{\mathrm dy}{\mathrm dx}=\frac{\mathrm dz}{\mathrm dx}+\phi'(x)=P(x)(z+\phi(x))^2+Q(x)(z+\phi(x))+R(x),$

由于 $y=\phi(x)$ 是一个解，带入消去后得 $\frac{\mathrm dz}{\mathrm dx}=(2P(x)\phi(x)+Q(x))z+P(x)z^2$ ，

这是一个Bernoulli方程.

* * *

一阶隐式微分方程
--------

### 方程12（可解出 $y$ 的方程）

$y=f(x,y').$

**解法.** 引进参数 $p=y'$ ，则方程变为 $y=f(x,p)$ ，将上式两边同时对 $x$ 求导，得

$p=y'=\frac{\partial f(x,p)}{\partial x}+\frac{\partial f(x,p)}{\partial p}\cdot\frac{\mathrm dp}{\mathrm dx},$

此时方程转化为关于 $p$ 和 $x$ 的显式微分方程，如果可以求出上述方程的通解 $p=\varphi(x,c),c$ 为常数，则带入可得原方程的通解 $y=f(x,\varphi(x,c)).$

**注记.** 不要直接对 $p$ 求积分得到 $y$ ，以免引入多余的常数项.

### 方程13（可解出 $x$ 的方程）

$x=f(y,y').$

**解法.** 注意到 $y'=\frac{\mathrm dy}{\mathrm dx}=\left(\frac{\mathrm dx}{\mathrm dy}\right)^{-1},$ 只需将 $x$ 看作关于 $y$ 的函数，然后便可视为方程12求解.

### 方程14（Clairaut方程）

$y=xy'+\varphi(y'),$ 其中 $\varphi(z)$ 二阶连续可微且 $\varphi''(z)\not=0.$

**解法.** 令 $y'=p$ 并对 $x$ 求导得 $p=p+x\frac{\mathrm dp}{\mathrm dx}+\varphi'(p)\frac{\mathrm dp}{\mathrm dx}\implies (x+\varphi'(p))\frac{\mathrm dp}{\mathrm dx}=0,$

当 $\frac{\mathrm dp}{\mathrm dx}=0$ 时，有 $p=C$ ，此时通解为 $y=Cx+\varphi(C),$

当 $x+\varphi'(p)=0$ 时，有特解 $x=-\varphi'(p),y=-\varphi'(p)p+\varphi(p).$

**注记.** 有时为了方便起见，可以用 $x=f(p),y=g(p)$ 表示方程的通解，这里的 $p$ 被看作自由变动的常数，而非因变量 $y$ 关于自变量 $x$ 的导函数，这种表示方程实质上是一个参数方程.

### 方程15（不显含 $x$ 或 $y$ 的方程）

$F(y,y')=0$ 或 $F(x,y')=0.$

**解法.** 右侧方程可以使用方程13中的方法转化为左侧方程，因此只讨论不显含 $x$ 的方程的解法.引进参数 $p=y'$ ，则方程变为 $F(y,p)=0$ ，引入参数 $t$ 将上式用参数曲线表示为 $y=\psi(t),p=h(t)$ ，由参数的微分法知， $h(t)=p=y'=\frac{\mathrm dy}{\mathrm dx}=\frac{\psi(t)}{\varphi'(t)},$ 故 $\varphi'(t)=frac{\psi'(t)}{h(t)}\implies \varphi(t)=\int\frac{\psi'(t)}{h(t)}\mathrm dt+C,$

于是方程的通解为 $x=\int\frac{\psi'(t)}{h(t)}\mathrm dt+C,y=\psi(t).$

**注记.** 方程15的解法过于抽象，以下给出一个例子：

$x\sqrt{1+(y')^2}=y'.$

解：令 $y'=\tan t,t\in(-\frac\pi2,\frac\pi2)$ ，则 $x=\sin t$ ，由于 $\mathrm dy=y'\mathrm dx=\tan t\cos t\mathrm dt=\sin t\mathrm dt$ ，故积分可得 $y=\int\sin t\mathrm dt=-\cos t+C,$ 故原方程参数形式的通解为 $x=\sin t,y=-\cos t+C,$ 消去参数 $t$ ，得到通解为 $x^2+(y-C)^2=1.$
> 作者：jykyyds
> 链接：undefined
