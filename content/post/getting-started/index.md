---
title: 天文统计学
#subtitle: Welcome 👋 We know that first impressions are important, so we've populated your new site with some initial content to help you get familiar with everything in no time.

# Summary for listings and search engines
#summary: Welcome 👋 We know that first impressions are important, so we've populated your new site with some initial content to help you get familiar with everything in no time.

# Link this post with a project
projects: []

# Date published
#date: '2020-12-13T00:00:00Z'

# Date updated
#lastmod: '2020-12-13T00:00:00Z'

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
#image:
#  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
#  focal_point: ''
#  placement: 2
#  preview_only: false

authors:
  - admin
  - Love Astro

tags:
  - Academic
  - 天文统计

categories:
  - 天文统计
  - 天文
---

### 1. 有两个测量量 $A$ 和 $B$，测量误差分别为 $\sigma_A$ 和 $\sigma_B$，它们的相关系数为 $\rho$，问 $f=3A+2B$ 的误差是多少？
解:根据误差传递公式，可以得到 $f$ 的误差为：
        $$
    \sigma_f = \sqrt{(3\sigma_A)^2 + (2\sigma_B)^2 + 2(3\times 2 \times \rho \sigma_A \sigma_B)}
        $$
        其中 $\rho$ 是相关系数。将其代入上式可以得到：
        $$
        \sigma_f = \sqrt{9\sigma_A^2 + 4\sigma_B^2 + 12\rho \sigma_A \sigma_B}
        $$
        因此，$f=3A+2B$ 的误差是 $\sqrt{9\sigma_A^2 + 4\sigma_B^2 + 12\rho \sigma_A \sigma_B}$。
        
### 2. 已知概率密度$𝑝(𝑥, 𝑦)$，求概率密度$𝑝(ln(\frac{x}{y}), 𝑙𝑛(𝑥 + 𝑦))$。
解: 我们可以使用变量替换法来求解这个问题。令 $u = \ln(\frac{x}{y})$ 和 $v = \ln(x + y)$，则有：

  $$
        \begin{aligned}
        x &= ye^u, \\
        x + y &= e^v.
        \end{aligned}
        $$
        
  根据变量替换法的公式，有：
        
  $$
        p(u, v) = p(x(u,v), y(u,v)) \left| \frac{\partial(x,y)}{\partial(u,v)} \right|
        $$
        
   其中，$\left| \frac{\partial(x,y)}{\partial(u,v)} \right|$ 表示雅可比行列式，计算方法如下：
        
   $$
        \begin{vmatrix}
        \frac{\partial x}{\partial u} & \frac{\partial x}{\partial v} \\
        \frac{\partial y}{\partial u} & \frac{\partial y}{\partial v}
        \end{vmatrix}
        =
        \begin{vmatrix}
        y e^u & 0 \\
        \frac{e^v - 1}{e^u + 1} & \frac{e^v - 1}{e^u + 1}
        \end{vmatrix}
        = \frac{(e^v - 1)y}{e^u + 1}.
        $$
        
   因此，我们可以得到：
        
   $$
        p(u, v) = p(ye^u, e^v - ye^u) \cdot \frac{(e^v - 1)y}{e^u + 1}.
        $$
        
  最后，我们只需要将 $u = \ln(\frac{x}{y})$ 和 $v = \ln(x + y)$ 代入上式即可得到概率密度 $p(\ln(\frac{x}{y}), \ln(x + y))$。
### 3. $X\sim𝑁(𝜇, 𝜎^2)$，$Y\sim𝑁(𝜇, 𝜎^2)$且 $X $和 $Y$ 相互独立, 求$𝑍_1 = 𝛼𝑋 + 𝛽𝑌$和$𝑍_2 =𝛼𝑋 − 𝛽𝑌$的相关系数$(𝛼, 𝛽 ≠ 0)$。
解:根据题意，我们有：

$$
\begin{aligned}
Z_1 &= \alpha X + \beta Y, \\
Z_2 &= \alpha X - \beta Y.
\end{aligned}
$$

因为 $X$ 和 $Y$ 相互独立，所以它们的协方差为零：

$$
\mathrm{Cov}(X,Y) = E[XY] - E[X]E[Y] = \mu^2 - \mu^2 = 0.
$$

于是，我们可以得到 $Z_1$ 和 $Z_2$ 的均值和方差：

$$
\begin{aligned}
E[Z_1] &= E[\alpha X + \beta Y] = \alpha\mu + \beta\mu = (\alpha + \beta)\mu, \\
E[Z_2] &= E[\alpha X - \beta Y] = \alpha\mu - \beta\mu = (\alpha - \beta)\mu, \\
\mathrm{Var}(Z_1) &= \mathrm{Var}(\alpha X + \beta Y) = \alpha^2 \mathrm{Var}(X) + \beta^2 \mathrm{Var}(Y) = \alpha^2\sigma^2 + \beta^2\sigma^2 = (\alpha^2 + \beta^2)\sigma^2, \\
\mathrm{Var}(Z_2) &= \mathrm{Var}(\alpha X - \beta Y) = \alpha^2 \mathrm{Var}(X) + \beta^2 \mathrm{Var}(Y) = \alpha^2\sigma^2 + \beta^2\sigma^2 = (\alpha^2 + \beta^2)\sigma^2.
\end{aligned}
$$

然后，我们来计算 $Z_1$ 和 $Z_2$ 的协方差：

$$
\begin{aligned}
\mathrm{Cov}(Z_1, Z_2) &= E[(Z_1 - E[Z_1])(Z_2 - E[Z_2])] \\
&= E[(\alpha X + \beta Y - (\alpha + \beta)\mu)(\alpha X - \beta Y - (\alpha - \beta)\mu)] \\
&= E[\alpha^2 X^2 - \alpha^2 X(\alpha - \beta)\mu + \alpha\beta XY - \alpha\beta Y(\alpha + \beta)\mu \\
&\quad- \alpha(\alpha - \beta)X\mu + (\alpha - \beta)\alpha\beta\mu^2 + \alpha\beta XY - \beta^2 Y(\alpha - \beta)\mu \\
&\quad- \alpha\beta X(\alpha + \beta)\mu + \beta^2 Y^2 - \beta^2 Y(\alpha + \beta)\mu] \\
&= E[\alpha^2 X^2] - (\alpha + \beta)\mu E[\alpha X] - (\alpha - \beta)\mu E[\alpha X] + (\alpha^2 - \beta^2)\mu^2 \\
&\quad+ E[\alpha\beta XY] - (\alpha + \beta)\mu E[\beta Y] - (\alpha - \beta)\mu E[-\beta Y] \\
&\quad- (\alpha - \beta)\mu E[\alpha X] + (\alpha^2 - \beta^2)\mu^2 + E[\alpha\beta XY] \\
&\quad- (\alpha + \beta)\mu E[\alpha X] - (\alpha - \beta)\mu E[\beta Y] + (\alpha^2 - \beta^2)\mu^2 + E[\beta^2 Y^2] - (\alpha - \beta)\mu E[\beta Y] \\
&= \alpha^2 \mathrm{Var}(X) - \alpha(\alpha + 2\beta)\mu^2 + \alpha\beta E[XY] - \beta(\alpha + 2\beta)\mu^2 + \beta^2\mathrm{Var}(Y) \\
&= \alpha^2\sigma^2 - \beta^2\sigma^2.
\end{aligned}
$$

因此，相关系数为：

$$
\rho = \frac{\mathrm{Cov}(Z_1, Z_2)}{\sqrt{\mathrm{Var}(Z_1)}\sqrt{\mathrm{Var}(Z_2)}} = \frac{\alpha^2 - \beta^2}{\alpha^2 + \beta^2}.
$$

### 4. $𝑦 = {𝑥^{−1}, 𝑥 > 0;0, 𝑥≤0}$是一个概率密度函数吗，为什么?在不显著改变函数在$𝑥 > 0$范围内的主要走向的情况下，如何将它改造成一个概率密度函数，并简单说明改造后的函数为什么是概率密度函数。

解：
    这个函数不是概率密度函数，因为它在$x=0$处不连续，而且对于某些$x$值，它的取值可以大于1。

   要将其改造成概率密度函数，我们需要确保它满足以下两个条件：
    
  1.非负性：对于任何实数$x$，$y(x)>=0$
  2.归一性：$∫𝑦(𝑥)𝑑𝑥=1$
    
   为了满足第一个条件，可以将原函数改写为：
    
   $𝑦 ={0, 𝑥 ≤ 0, 𝑥^{−1}, 𝑥 > 0}$
    
   为了满足第二个条件，我们需要在$x>0$的范围内重新定义该函数。具体来说，我们可以将该函数定义为：
    
   $𝑦 ={𝑘𝑥^{−1}, 𝑥 > 0, 0, 𝑥≤0}$
    
   其中$k$是一个常数，使得$∫𝑦(𝑥)𝑑𝑥=1$。
    
   为了求出$k$的值，我们可以利用归一性条件，得到：
    
   $$∫_{0}^{∞} kx^{-1} dx = 1$$
    
   根据基本积分公式，上述积分结果为：
    
   $$k[ln(x)]_{0}^{∞} = 1$$
    
   由于当$x$趋近于$∞$时，$ln(x)$趋近于正无穷，当$x$趋近于$0$时，$ln(x)$趋近于负无穷，因此上式可以化简为：
    
   $$k(-∞ - ln(0)) = 1$$
    
   由于$ln(0)$趋近于负无穷大，因此上式实际上相当于：
    
   $$k × ∞ = 1$$
    
   由于$∞$乘以任何有限数都等于无穷，因此我们可以得到：
    
   $$k = 1$$
    
   这样，我们就得到了以下概率密度函数：
    
   $$𝑦 ={𝑥^{−1}, 𝑥 > 0, 0, 𝑥≤0}$$
    
   该函数满足概率密度函数的两个条件，并且在$x>0$的范围内具有单调递减的主要走向。因此，它可以被视为一个概率密度函数。
   
   ### 5. 国家天文台刘继峰团队 2019 年在 $3000 $颗 LAMOST 观测的恒星中发现了一颗黑洞双星，问 1)观测到一颗恒星是黑洞双星的概率分布是怎样的?2)刘团队后续又观测了 $12000$ 颗恒星，但是很遗憾没有再找到新的黑洞双星，问此时新观测一颗恒星恰好是黑洞双星的后验概率是多少?
   解：1) 假设观测到一颗恒星是黑洞双星的概率为p，则观测到一颗不是黑洞双星的概率为1-p。根据题目中的信息，3000颗LAMOST观测的恒星中有一颗是黑洞双星，因此我们可以得到以下方程：

   $$ p \times 3000 + (1 - p) \times 3000 = 1$$
    
   解这个方程可得：
    
   $$ p = 1/3000 ≈ 0.00033$$
    
   因此，观测到一颗恒星是黑洞双星的概率大约为$0.00033$。
    
   2) 在刘团队后续观测的$12000$颗恒星中没有再找到新的黑洞双星，因此我们可以将其视为一次伯努利试验。假设事件$A$表示观测到一颗恒星是黑洞双星，事件B表示观测到一颗恒星不是黑洞双星，且在12000次观测中，事件B发生了11999次。根据贝叶斯定理，我们可以计算出在12001次观测中，观测到一颗恒星是黑洞双星的后验概率P(A|B)：
    
   $$P(A|B) = P(B|A) × P(A) / P(B)$$
   
   其中，$P(B|A)$表示在恒星是黑洞双星的情况下，$12001$次观测中有$11999$次不是黑洞双星的概率，即：
    
   $$P(B|A) = (1 - 0.00033)^{11999} ≈ 0.997$$
    
   $P(A)$表示观测到一颗恒星是黑洞双星的先验概率，即$0.00033$。
    
   $P(B)$表示在$12000$次观测中有11999次不是黑洞双星的概率，即：
    
   $$P(B) = (1 - 0.00033)^{11999} × 0.00033 + (1 - (1 - 0.00033)^{11999})\times(1 - 0.00033)
    ≈ 0.99967$$
    
   将上述三个概率代入公式中，可以得到：
    
   $$P(A|B) = P(B|A) × P(A) / P(B)
    ≈ 0.00033 / (1 - 0.00033)^{11999} × 0.997
    ≈ 0.00010$$
    
   因此，在$12001$次观测中，观测到一颗恒星是黑洞双星的后验概率约为$0.00010$。
