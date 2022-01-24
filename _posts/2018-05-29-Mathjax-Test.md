---
layout: post
title: Mathjax Test Post
---
Dual curve pricing

[Andersen and Piterbarg (2010)](#1).

[Ametrano and Marco Bianchetti (2013)](#2).

OIS discounting is used in conjunction with Libor rates for pricing in the dual-curve setup. If we consider a fixed tenor structure

\begin{align}
0=T_0<T_1<\ldots<T_M,
\label{eq:tau}\end{align}

where in Eq. \eqref{eq:tau} the intervals $\tau_i=T_{i}-T_{i-1}$, $i=0,\ldots,M$ is the year fraction between the accrual dates $T_i$ and $T_{i-1}$ depending on day count convention, then Libor and OIS zero-coupon bonds (discount factors) can be obtained from the continuously-compounded forward Libor and forward OIS curves in the following manner. Let $f(t,T_{i},T_{i-1})$ be the continuously-compounded forward rate and let $P(t,T_0)=1$ and $P(t,T_1)=\exp(-f(t,T_1)\cdot\tau_1)$ then

$$
P(t,T_n) = P(t,T_{n-1})\exp\left(-f(t,T_n)\cdot\tau_n\right),\hspace{.25pc}n=2,\ldots M.
$$

Let $P(t,T_n)$ and $P_{OIS}(t,T_n)$ be the Libor and OIS discount factors respectively for a given $t$ and $T_n$, then define the simply-compounded Libor and OIS forward rate as

$$
L(t,T_{n-1},T_{n}) = L_n(t) = \frac{1}{\tau_n}\left(\frac{P(t,T_{n-1})}{P(t,T_{n})}-1\right),
$$

and

$$
F(t,T_{n-1},T_{n}) = F_n(t) = \frac{1}{\tau_n}\left(\frac{P_{OIS}(t,T_{n-1})}{P_{OIS}(t,T_{n})}-1\right).
$$

## References
<a id="1">[1]</a>
Leif B.G. Andersen and Vladimir V. Piterbarg. _Interest Rate Modelling, Volume I: Foundations and Vanilla Models_. Atlantic Financial Press, 1st edition, 2010a.

<a id="2">[2]</a>
Ferdinando M. Ametrano and Marco Bianchetti, Everything You Always Wanted to Know About Multiple Interest Rate Curve Bootstrapping but Were Afraid to Ask (April 2, 2013). Available at SSRN: [https://ssrn.com/abstract=2219548](https://ssrn.com/abstract=2219548)
