---
layout: post
title: 哈密顿系统的辛几何算法(三)
category: notebook
---
## 辛变换

对于 $\phi:\mathbb{R}^{2n} \rightarrow \mathbb{R}^{2n}$，
$\phi(z)=\hat{z}$：
* $\phi$ 叫作辛变换，如果其雅克比矩阵是辛矩阵。即：
[$
\left[ \frac{\partial \hat{z}}{\partial z} \right]^\mathsf{T}J\left[ \frac{\partial \hat{z}}{\partial z} \right]=J
$]
该条件等价于：
[$
d\hat{p}_k \wedge d \hat{q}^k=dp_k \wedge dq^k
$]

## 哈密顿系统的相流是辛变换族

给定 $H$，定义相流 $$\{g^t \mid t\in \mathbb{R}\}$$，满足：
[$
\frac{dg^t(z_0)}{dt}=J^{-1}\nabla H(g^t(z_0))
$]
则：
[$
\left[ \frac{\partial g^t(z)}{\partial z} \right]^\mathsf{T}J\left[ \frac{\partial g^t(z)}{\partial z} \right]=J
$]
证明：$t=0$ 时，显然成立；再证 $$\frac{d}{dt}\left\{ \left[ \frac{\partial g^t(z)}{\partial z} \right]^\mathsf{T}J\left[ \frac{\partial g^t(z)}{\partial z} \right]\right\}=0$$。

## 辛差分格式

对于$\frac{dz}{dt}=K^{-1}(z)\nabla H(z)$，若 $K$ 反对称，非退化，且满足 $Jacobi~ Identiy$：
[$
\frac{\partial K_{ab}}{\partial z_c}+\frac{\partial K_{bc}}{\partial z_a}+\frac{K_{ca}}{\partial z_b}=0
$]
则称其为非正则哈密顿系统，它类似地满足：
[$
\left[ \frac{\partial g^t(z)}{\partial z} \right]^\mathsf{T}K(g^t(z))\left[ \frac{\partial g^t(z)}{\partial z} \right]=K(z)
$]
