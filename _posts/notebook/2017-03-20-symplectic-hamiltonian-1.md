---
layout: post
title: 哈密顿系统的辛几何算法(一)
description: ODE复习
category: notebook 
---
前言：本学期（17 年春）上了如题的这门课，加深一下对经典力学及辛几何的理解。而且，部分内容我也有可能在科研中用得上。
## 复习一点常微分
给出如下的 ODE:
[$
\frac{dx}{dt}=f(x)
$]
* 右端不含t，则称其为自洽的。易证：
 若 $\varphi(t)$是解，则 $x=\varphi_{*}=\varphi(t+c)$ 也是解。
* 每个解 $\varphi(t)$ 代表一条轨线，如果两条轨线相交，如 $\varphi(t_1)=\psi(t_2)$，则必重合：
[$
\varphi_*(t)\mid_{t=t_2}=\varphi(t+t_1-t_2)\mid_{t=t_2}=\psi(t)\mid_{t=t_2}
$]
由解的唯一性定理，知 $$\varphi_*(t)=\psi(t)$$。
* 周期性质：一列周期 $$\{c_i\}\rightarrow c_0$$，则 $c_0$ 也是周期。
进而，所有周期的集合 $F$ 是闭的，非空。
	* 假如 $F$ 中没有最小正数，则 $F$ 包含全体实数，即 $\varphi(t)=a$。
	* 假如 $F$ 中最小正数为 $T$，则 $$F=\{mT \mid m \in \mathbb{Z}\}$$。

将以 $(0, \xi)$ 为初值的解记为 $$\varphi(t, \xi)$$，则 $$\varphi\left(t,\varphi\left(s,\xi\right)\right)=
\varphi\left(t+s, \xi\right)$$。 <br/> 
若系统非自治，即：
[$
\frac{dx}{dt}=f\left(x,t\right)
$]
则 $g^{r+s}\neq g^rg^s $，当且仅当 $f$ 不依赖于 $t$ 时等号成立。
