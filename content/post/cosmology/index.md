---
title: 字宙的年龄和尺度

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
  - Cosmology

categories:
  - Academic
  - Cosmology
---

声明：本文仅作学习笔记使用，转载请注明来源，由于笔者水平有限，如有不当之处，敬请读者指正.

#### 一、粗略地计算

对尺度因子的一阶展开：
$$a(t) \simeq a\left(t_{0}\right)+\frac{d a\left(t_{0}\right)}{d t}\left(t-t_{0}\right)=1+H_{0}\left(t-t_{0}\right)$$

设宇宙初始时：$a(t) =0$.宇宙的年龄可以作以下的粗略计算： $t-t_{B B}=H_{0}^{-1} \simeq 1.4 \times 10^{10}years=140$亿年，$t_{BB}$表示大爆炸的初始时间（Big Bang）.

#### 二、宇宙年龄的计算方法
$$t_{0}-t_{B B}=\int_{t_{BB}}^{t_{0}} d t=\int_{0}^{a_{0}} \frac{d a}{\dot{a}}=\int_{0}^{a_{0}} \frac{d a}{a H}=\int_{0}^{\infty} \frac{d z}{(1+z) H(z)}.$$

1️. 取决于不同时刻的 $H$的演化;

2. 哈勃参数的演化取决于主导宇宙演化的物质.

#### 三、可观测宇宙的大小

从宇宙初始时，光能传播的最大共动距离：

$$r_{\max }=\int_{0}^{r_{\max} } d r=c \int_{t_{B B}}^{t} \frac{d t^{\prime}}{a\left(t^{\prime}\right)}.$$

相应的物理距离:

$$dH(t)=a(t)\times r_{m a x}=c a(t) \int_{t_{B B}}^{t} \frac{d t^{\prime}}{a\left(t^{\prime}\right)} \neq c\left(t-t_{B B}\right).$$

${a\left(t^{\prime}\right)} $不是常数，宇宙是膨胀的.

#### 四、共形时间

共形时间：不含尺度因子${a\left(t\right)} $的部分.$d \eta=\frac{d t}{a(t)}.$与光传播的最大共动距离的关系：

$$r_{\max }=\int_{0}^{r_{\max }} d r=c \int_{\eta_{\beta B}}^{\eta} d \eta=c\left(\eta-\eta_{B B }\right).$$

弗里德曼-罗伯逊-沃尔克度规(FRW):（物理时间）
$$d s^{2}=-c^{2} d t^{2}+a^{2}(t)\left[d r^{2}+r^{2}\left(d \theta^{2}+\sin ^{2} \theta d \varphi^{2}\right)\right]$$

共形时间：

$$d s^{2}=a^{2}(t)\left[-c^{2} d \eta^{2}+d r^{2}+r^{2}\left(d \theta^{2}+\sin ^{2} \theta d \varphi^{2}\right)\right].$$

（类闵可夫斯基空间）.将动态时空化为静止时空.

粒子视界：$r_{p h}=c\left(\eta-\eta_{B B}\right)$（看回去，可观测宇宙的大小）（共动距离）(ph=Particle \quad horizon).宇宙事件视界：该粒子可影响的区域.（看以后，可影响的宇宙大小）(ceh=Cosmic \quad event\quad horizon)，$r_{c e h}=c\left(\eta_{\text {end }}-\eta\right)$，P可以影响 
Q但是不能影响 R.
![image](https://github.com/wangboting/hugo-blog-theme/assets/71454203/a0885be0-fdb3-4d59-a95e-e38deae57a2c)
