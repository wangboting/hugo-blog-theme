---
title: 第一章 概率论基础

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
  - 统计学
  - 概率论

categories:
  - 统计学
  - 概率论
---

### 一、概率基础知识

定义：（概率）设  $\mathrm{E}$  是随机实验,  $\mathrm{S}$  是它的样本空间, 对于  $\mathrm{E}$  中的每一事 件  $\mathrm{A}$  赋予一个实数, 记为  $P(A)$ , 称为事件  $\mathrm{A}$  的概率，如果集合函数  $P\left({ }^{\circ}\right)$  满足:

1 非负性：对任意  $\mathrm{A}$ , 有  $P(A) \geq 0$ ;

2 规范性：对于必然事件  $\mathrm{S}, P(S)=1$ ;

3 可列可加性：设  $A_{1}, A_{2}, \ldots$  是两两互不相容的事件, 即  $A_{i} A_{j}=\phi$, $i \neq j$ ,  $i, j=1,2, \ldots$ , 则有  $P\left(A_{1} \bigcup A_{2} \bigcup \ldots\right)=P\left(A_{1}\right)+P\left(A_{2}\right)+\ldots$ 

概率的性质:

性质 1:  $P(\phi)=0$ .

性质 2: (有限可加性) 若 $ A_{1}, A_{2}, \ldots, A_{n} $ 两两互不相容, 即 $ A_{i} A_{j}=\phi$ , 当 $ i \neq j $ 时, 则有

$$P\left(A_{1} \bigcup A_{2} \bigcup \ldots \bigcup A_{n}\right)=P\left(A_{1}\right)+P\left(A_{2}\right)+\ldots P\left(A_{n}\right)$$ .

性质 3: 若  $A \subseteq B$ , 则
$$
P(B-A)=P(B)-P(A) ,
P(B) \geq P(A)
$$

定义： 设  $A$  和  $B$  是两个随机事件, 且  $P(A)>0$ , 称

$$P(B \mid A)=\frac{P(A B)}{P(A)}$$

为在事件 $ A $ 发生的条件下事件$  B  $发生的条件概率。
乘法定理： 设  $P(A)>0 $, 则

$P(A B)=P(B \mid A) P(A)$

定义： 设  $S $ 为实验 $ E $ 的样本空间,  $B_{1}, B_{2}, \ldots, B_{n}$  为 $ S$  上的一组随机 事件, 若

i)  $B_{i} B_{j}=\phi, i \neq j, i, j=1,2, \ldots, n $

ii)  $B_{1} \bigcup B_{2} \bigcup \ldots \bigcup B_{n}=S $

则称   $B_{1}, B_{2}, \ldots, B_{n} $  为样本空间   $S $  上的一个划分。

定理：设实验   $E $  上的样本空间为  $ S, A  $ 为  $ E  $ 的事件,   $B_{1}, B_{2}, \ldots, B_{n} $  是   $S   $上的一个划分, 且  $ P\left(B_{i}\right)>0,(i=1,2, \ldots, n) $ , 则
{{< math >}}
$$
\begin{split}
P(A) = & P(A \mid B_1) P(B_1) + \\
       & P(A \mid B_2) P(B_2) + \\
       & \ldots + \\
       & P(A \mid B_n) P(B_n)
\end{split}
$$
{{< /math >}}

这个公式被称为全概率公式。

定义： 设  $ A $  和  $ B   $是两个随机事件, 若满足  $ P(A B)=P(A) P(B)  $ 则称   $A  $ 和   $B  $ 相互独立。

定理：若  $ A $  和  $ B  $ 是两个随机事件, 且有   $P(A)>0  $, 若   $A $  和   $B  $ 相互独 立, 则  $ P(B \mid A)=P(B)  $ 成立, 反之亦然。

定理：若随机事件  $ A $  和  $ B $相互独立，则下列各对随机事件也相互独立：   $A  $ 和  $ \bar{B}, \bar{A}   $和  $ B, \bar{A}  和  \bar{B}  $ 。
如果有三个随机事件   $A, B, C $ , 它们相互独立，当且仅当
{{< math >}}
$$
\begin{split}
P(A B)=P(A) P(B), \\
P(A C)=P(A) P(C), \\
P(B C)=P(B) P(C), \\
P(A B C)=P(A) P(B) P(C) .
\end{split}
$$
{{< /math >}}
定理：设实验  $E $ 的样本空间为 $ S, A $ 为  $E$  的随机事件,$  B_{1}, B_{2}, \ldots, B_{n}$  是  $S$  上的一个划分, 且 $ P(A)>0, P\left(B_{i}\right)>0,(i=1,2, \ldots, n)$ , 则

$$P\left(B_{i} \mid A\right)=\frac{P\left(A \mid B_{i}\right) P\left(B_{i}\right)}{\sum_{j=1}^{n} P\left(A \mid B_{j}\right) P\left(B_{j}\right)}$$

这称为贝叶斯公式。
对于两个随机事件  $A $ 和  $B$ , 贝叶斯公式也可以写成
$$
\begin{array}{l}
P(B \mid A)=\frac{P(A \mid B) P(B)}{P(A \mid \bar{B}) P(\bar{B})+P(A \mid B) P(B)} \\
=\quad \frac{P(A \mid B) P(B)}{P(A)} \\
\end{array}
$$

上面公式等号左面称为后验概率（posterior probability），等号右边 分子上第一项称为似然概率 (likelihood) ，第二项称为先验概率 (prior probability), 而分母上的项称为证据 (evidence), 即

$$\overbrace{P(B \mid A)}^{\text {posterior }}=\frac{\overbrace{P(A \mid B)}^{\text {likelihood }} \overbrace{P(B)}^{\text {prior }}}{\underbrace{P(A)}_{\text {evidence }}}$$
