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

#### 1. 有两个测量量 $A$ 和 $B$，测量误差分别为 $\sigma_A$ 和 $\sigma_B$，它们的相关系数为 $\rho$，问 $f=3A+2B$ 的误差是多少？

解:根据误差传递公式，可以得到 $f$ 的误差为：
        
$$       
    \sigma_f = \sqrt{(3\sigma_A)^2 + (2\sigma_B)^2 + 2(3\times 2 \times \rho \sigma_A \sigma_B)}
$$ 
    
其中 $\rho$ 是相关系数。将其代入上式可以得到：
    
 $$
        \sigma_f = \sqrt{9\sigma_A^2 + 4\sigma_B^2 + 12\rho \sigma_A \sigma_B}
        $$
    
因此，$f=3A+2B$ 的误差是 $\sqrt{9\sigma_A^2 + 4\sigma_B^2 + 12\rho \sigma_A \sigma_B}$。

#### 2. 已知概率密度$𝑝(𝑥, 𝑦)$，求概率密度$𝑝(ln(\frac{x}{y}), 𝑙𝑛(𝑥 + 𝑦))$。

解: 我们可以使用变量替换法来求解这个问题。令 $u = \ln(\frac{x}{y})$ 和 $v = \ln(x + y)$，则有：
{{< math >}}

$$
        \begin{aligned}
        x &= ye^u, \\
        x + y &= e^v.
        \end{aligned}
        $$
        
{{< /math >}}        
根据变量替换法的公式，有：

{{< math >}}
  
$$
        p(u, v) = p(x(u,v), y(u,v)) \left| \frac{\partial(x,y)}{\partial(u,v)} \right|
        $$

{{< /math >}} 
 其中，$\left| \frac{\partial(x,y)}{\partial(u,v)} \right|$ 表示雅可比行列式，计算方法如下：

{{< math >}}

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
{{< /math >}}         
因此，我们可以得到：
{{< math >}}

$$
        p(u, v) = p(ye^u, e^v - ye^u) \cdot \frac{(e^v - 1)y}{e^u + 1}.
        $$
        
{{< /math >}}        
 最后，我们只需要将 $u = \ln(\frac{x}{y})$ 和 $v = \ln(x + y)$ 代入上式即可得到概率密度 $p(\ln(\frac{x}{y}), \ln(x + y))$。
 
#### 3. $X\sim𝑁(𝜇, 𝜎^2)$，$Y\sim𝑁(𝜇, 𝜎^2)$且 $X $和 $Y$ 相互独立, 求$𝑍_1 = 𝛼𝑋 + 𝛽𝑌$和$𝑍_2 =𝛼𝑋 − 𝛽𝑌$的相关系数$(𝛼, 𝛽 ≠ 0)$。

解:根据题意，我们有：

$$
Z_1 = \alpha X + \beta Y, 
$$
$$
Z_2 = \alpha X - \beta Y.
$$

因为 $X$ 和 $Y$ 相互独立，所以它们的协方差为零：

$$
\mathrm{Cov}(X,Y) = E[XY] - E[X]E[Y] = \mu^2 - \mu^2 = 0.
$$

于是，我们可以得到 $Z_1$ 和 $Z_2$ 的均值和方差：

{{< math >}}

$$
\begin{split}
E[Z_1] &= E[\alpha X + \beta Y] \\
&= \alpha\mu + \beta\mu \\
&= (\alpha + \beta)\mu,
\end{split}
$$

{{< /math >}}

{{< math >}}

$$
\begin{split}
E[Z_2] &= E[\alpha X - \beta Y] \\
&= \alpha\mu - \beta\mu \\
&= (\alpha - \beta)\mu,
\end{split}
$$

{{< /math >}}

{{< math >}}

$$
\begin{split}
\mathrm{Var}(Z_1) &= \mathrm{Var}(\alpha X + \beta Y) \\
&= \alpha^2 \mathrm{Var}(X) + \beta^2 \mathrm{Var}(Y) \\
&= \alpha^2\sigma^2 + \beta^2\sigma^2 \\
&= (\alpha^2 + \beta^2)\sigma^2,
\end{split}
$$

{{< /math >}}

{{< math >}}

$$
\begin{split}
\mathrm{Var}(Z_2) &= \mathrm{Var}(\alpha X - \beta Y) \\
&= \alpha^2 \mathrm{Var}(X) + \beta^2 \mathrm{Var}(Y) \\
&= \alpha^2\sigma^2 + \beta^2\sigma^2 \\
&= (\alpha^2 + \beta^2)\sigma^2.
\end{split}
$$

{{< /math >}}

