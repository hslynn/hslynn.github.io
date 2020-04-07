---
layout: post
title: 关于GH形式中的约束
category: notebook 
description: Constraint Evolution
---

今天在写毕业论文Generalized Harmonic部分的时候产生的一个想法，记录如下．

GH形式中的约束$\mathcal{C}_a\equiv H_a+\Gamma_a=0$在数值上总不能严格满足，这个偏差称为 *Constraint Violation*，因而需要作 *Constraint Damping* 处理，否则，Constraint Violation会不断增大，文献中将此时的解称为＂非物理的＂(Unphysical). 

我可能是脑子抽筋的一个想法是：
* 能否换一种观点来看这个时候的解？它不是＂非物理的＂，而只是坐标系没有被我们的$H_a$函数所很好地决定住，未必不可用；
* 进而，能否不采用Constraint Damping的办法强制使得坐标系按$H_a$函数所规定的路来走，而是让$H_a$对坐标的限制＂软化＂？

可能有的好处是：
* 免除了Constraint Damping这个操作的不优雅、不确定性；
* 既然Constraint Violation无法消除，导致坐标系的不确定性，进而导致各种误差，那么换用上述办法是否能得到更精确的物理量，比如哈密顿约束，比如黑洞质量，比如引力波？
