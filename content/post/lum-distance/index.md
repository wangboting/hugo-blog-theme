---
title: 光度距离与红移

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

{{audio 26655379}}

声明：本文仅作学习笔记使用，转载请注明来源，由于笔者水平有限，如有不当之处，敬请读者指正.

#### 一、光度距离
参数说明:

 -距离 $d$
 
 -视光度 $l$
 
 -绝对光度$L$
 
 -光度 $l=\frac{L}{4 \pi d^{2}}$
 
 考虑宇宙膨胀，将$d$换成物理距离:$d_H=a_0r$。
 
 1. 宇宙膨胀，红移，频率$\nu$减小，光子数目减少，故视光度$l$减少$1+z$倍，
 $$\nu_{0}=\frac{\nu_{1}}{1+z} .$$
 $\nu_0$是光子发出时的频率.$\nu_1$是望远镜接收到的频率.
 
 2. 宇宙膨胀，接收到的光子的能量也降低$1+z$倍.

$$E_{0}=h_{0}\nu_0=h_0 \frac{\nu_{1}}{1+z}=E_{1} \times \frac{1}{1+z} .$$

综上，视光度$l$减少$(1+z)^2$倍。在膨胀时空，视光度 $l$和绝对光度$L$的关系：

$$l=\frac{L}{4 \pi d_{H}^{2}(1+z)^{2}}=\frac{L}{4 \pi a_{0}^{2} r^{2}(1+z)^{2}} .$$
定义光度距离：

$$d_{L}=a_{0} r(1+z)$$

，是一个可观测量，通过标准烛光（造父变星、 Ia型超新星等）的视光度.可通过得到视光距离，加上红移(H(z))的信息，最后可以得到共动距离 
$r$.目前，可以测量：红移，光度距离.

#### 二、宇宙的膨胀速度$H_0$和加速度$q_0$.

速度：$H=\frac{\dot{a}}{a}$

对尺度因子进行泰勒展开：
$$a(t)=1+H_{0}\left(t-t_{0}\right)-\frac{1}{2} q_{0} H_{0}^{2}\left(t-t_{0}\right)+\ldots$$

其中$q(t)=-\frac{\ddot{a} a}{\dot{a}^{2}}=-\frac{\ddot{a}}{a H^{2}}$是加速度。通过拟合观测得到的光度距离$d_{L}$和红移$z$可以确定目前宇宙膨胀速度$H_0$和加速度$q_0$.

目前的观测表明：
$$q(t_0)=-\frac{\ddot{a_0}}{a_0 H_0^{2}}\simeq 0.5\Rightarrow \ddot{a}>0.$$
预示着宇宙存在暗能量. 

 
