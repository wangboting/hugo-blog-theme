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
#### 1. 有两个测量量 {{< math >}}$A$  {{< /math >}}  和  {{< /math >}}  {{< math >}}$B$ {{< /math >}}  ，测量误差分别为 {{< math >}}$\sigma_A$  {{< /math >}}  和 {{< math >}}$\sigma_B$，它们的相关系数为 {{< math >}}$\rho$ {{< /math >}}  ，问 {{< math >}}$f=3A+2B$ {{< /math >}}   的误差是多少？
解:根据误差传递公式，可以得到 $f$ 的误差为：
{{< math >}}        
  $$
    \sigma_f = \sqrt{(3\sigma_A)^2 + (2\sigma_B)^2 + 2(3\times 2 \times \rho \sigma_A \sigma_B)}
$$
 {{< /math >}}   
  其中 $\rho$ 是相关系数。将其代入上式可以得到：
  {{< math >}}  
  $$
        \sigma_f = \sqrt{9\sigma_A^2 + 4\sigma_B^2 + 12\rho \sigma_A \sigma_B}
        $$
   {{< /math >}}    
   因此，{{< math >}}$f=3A+2B${{< /math >}} 的误差是 {{< math >}}$\sqrt{9\sigma_A^2 + 4\sigma_B^2 + 12\rho \sigma_A \sigma_B}$ {{< /math >}}  。
#### 2. 已知概率密度{{< math >}}$𝑝(𝑥, 𝑦)$ {{< /math >}}  ，求概率密度{{< math >}}$𝑝(ln(\frac{x}{y}), 𝑙𝑛(𝑥 + 𝑦))$ {{< /math >}}  。
解: 我们可以使用变量替换法来求解这个问题。令 {{< math >}}$u = \ln(\frac{x}{y})$ 和 {{< math >}}$v = \ln(x + y)$ {{< /math >}}  ，则有：
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
其中，{{< math >}}$\left| \frac{\partial(x,y)}{\partial(u,v)} \right|$ {{< /math >}}   表示雅可比行列式，计算方法如下：
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
   最后，我们只需要将 {{< math >}}$u = \ln(\frac{x}{y})$ {{< /math >}}   和 {{< math >}}$v = \ln(x + y)$ {{< /math >}}   代入上式即可得到概率密度 {{< math >}}$p(\ln(\frac{x}{y}), \ln(x + y))$ {{< /math >}}  。

