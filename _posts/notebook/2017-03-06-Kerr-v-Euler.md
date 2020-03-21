---
layout: post
title: Kerr Geodesic v. Euler 2-body (or Vinti)
category: notebook 
---
给出如下的Kerr调和坐标的$2PN$展开：
$$
\begin{align}
~~~~~~g_{00}\approx&-1+\frac{2M}{R}-\frac{2M^2}{R^2}+\frac{2M^3}{R^3}+\frac{Ma^2}{R^3};\\ 
      g_{01}\approx&\frac{2M(M+\sqrt{M^2-a^2})}{R^2}\cdot\frac{X}{R}-\frac{2Ma}{R^2}\cdot\frac{Y}{R}\\ &-\frac{4M^2(M+\sqrt{M^2-a^2})}{R^3}\cdot\frac{X}{R}+\frac{2M^2a}{R^3}\cdot\frac{Y}{R};\\
      g_{02}\approx&\frac{2M(M+\sqrt{M^2-a^2})}{R^2}\cdot\frac{Y}{R}+\frac{2Ma}{R^2}\cdot\frac{X}{R}\\ &-\frac{4M^2(M+\sqrt{M^2-a^2})}{R^3}\cdot\frac{Y}{R}-\frac{2M^2a}{R^3}\cdot\frac{X}{R};\\
      g_{03}\approx&\frac{2M(M+\sqrt{M^2-a^2})}{R^2}\cdot\frac{Z}{R}-\frac{4M^2(M+\sqrt{M^2-a^2})}{R^3}\cdot\frac{Z}{R};\\
      g_{ij}\approx&\left(1+\frac{2M}{R}+\frac{M^2}{R^2}\right)\delta_{ij}+\frac{M^2}{R^2}\cdot\frac{X_iX_j}{R^2};\\
      r=&\sqrt{X^2+Y^2+Z^2};\\
      X=&\sqrt{R^2+a^2}\sin\sigma\cos\phi;\\
	  Y=&\sqrt{R^2+a^2}\sin\sigma\sin\phi;\\
	  Z=&R\cos\theta
\end{align}
$$

取$g_{00}=-1+\frac{2M}{R}=-1+\frac{2M}{\sqrt{r^2-a^2\sin^2\theta}}$，$g_{\mu j}=\delta_{\mu j}$貌似就可以得到欧拉两体（或者Vinti？）问题了，因为在此时空下运动的检验粒子的拉氏量：<br/>
$$
\begin{align}
~~~~~~\mathcal{L}=&1-\frac{d\tau}{dt}\\
	     		 =&1-\sqrt{-\left(\frac{d\tau}{dt} \right)^2}\\
			     =&1-\sqrt{1-\frac{2M}{R}-\dot{X}^2-\dot{Y}^2-\dot{Z}^2}\\
				 =&1-\left[1-\frac{M}{R}-\frac{1}{2}\left(\dot{X}^2+\dot{Y}^2+\dot{Z}^2\right)\right]\\
				 =&\frac{1}{2}\left(\dot{X}^2+\dot{Y}^2+\dot{Z}^2\right)+\frac{M}{R}\\
				 =&\frac{1}{2}\frac{R^2+b^2\cos^2\sigma}{R^2+b^2}\dot{R}^2 + \frac{1}{2}(R^2+b^2\cos^2\sigma)\dot{\sigma}^2\\
				  & + \frac{1}{2}(R^2+b^2)\sin^2\sigma\dot{\phi}^2 + \frac{M}{R}
\end{align}
$$

若不先作 $PN$ 近似，而是直接使用原始的调和坐标，则会得到最后的势能项为：
[$
\frac{M(R+M)}{(R+M)^2+a^2\cos^2\sigma}
$]

而 Vinti 问题的 $Lagrangian$ 是:\\
$$
\begin{align}
~~~~~~\mathcal{L}^*=& \frac{1}{2}\frac{R^2+b^2\cos^2\sigma}{R^2+b^2}\dot{R}^2 + \frac{1}{2}(R^2+b^2\cos^2\sigma)\dot{\sigma}^2\\
		& + \frac{1}{2}(R^2+b^2)\sin^2\sigma\dot{\phi}^2 + \frac{M R}{R^2+b^2\cos^2\sigma}
\end{align}
$$

要建立二者之间的联系，问题在于：
* 由于只考虑到牛顿阶，这里的分母有极大的自由，比如你可以向其中添加含有$a$、$M$的项。
这样来说，似乎可以认为势能项是一样的；但是，到底是在何种意义上我们说，Kerr 的测地线与 Vinti 问题有联系呢？
如果作这样的 $1PN$ 处理，自然应该同时将其它项展开到相应的阶数，而不能仅限于势能项。
