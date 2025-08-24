---
tags:
  - "#波函数"
---


# 📘 概率流密度 \(J(x,t)\)

## 1. 概率守恒
量子力学中，波函数 $\psi(x,t)$ 的模方给出概率密度：
$$
\rho(x,t) = |\psi(x,t)|^2.
$$

概率必须满足守恒律：
$$
\frac{\partial \rho}{\partial t} + \nabla \cdot J = 0,
$$
这就是 **连续性方程**。

---

## 2. 从薛定谔方程推导
薛定谔方程：
$$
i\hbar \frac{\partial \psi}{\partial t} 
= -\frac{\hbar^2}{2m}\nabla^2 \psi + V(x)\psi.
$$

取复共轭：
$$
- i\hbar \frac{\partial \psi^*}{\partial t} 
= -\frac{\hbar^2}{2m}\nabla^2 \psi^* + V(x)\psi^*.
$$

对 $\rho(x,t)=\psi^*(x,t)\psi(x,t)$取时间导数：
$$
\frac{\partial \rho}{\partial t} 
= \psi^* \frac{\partial \psi}{\partial t} + \psi \frac{\partial \psi^*}{\partial t}.
$$

代入薛定谔方程，经过整理，得到：
$$
\frac{\partial \rho}{\partial t} + \nabla \cdot J = 0,
$$
其中概率流密度：
$$
J(x,t) = \frac{\hbar}{2mi}\left(\psi^* \nabla \psi - \psi \nabla \psi^*\right).
$$

---

## 3. 一维形式
在一维时：
$$
J(x,t) = \frac{\hbar}{2mi}\left(\psi^* \frac{\partial \psi}{\partial x} 
- \psi \frac{\partial \psi^*}{\partial x}\right).
$$

等价写法：
$$
J(x,t) = \frac{\hbar}{m}\,\text{Im}\left(\psi^* \frac{\partial \psi}{\partial x}\right).
$$

---

## 4. 物理意义
- $\rho(x,t) = |\psi(x,t)|^2$：概率密度。  
- $J(x,t)$：概率流动的速率。  
- 类比经典力学，它等于 **概率密度 $\rho$** × 平均速度 $\langle v \rangle$。  

---

## 5. 特殊情况
- **平面波** $\psi(x,t) = Ae^{i(kx - \omega t)}$：  
  $$
  J = \frac{\hbar k}{m}|A|^2.
  $$
  粒子以动量 $\hbar k$ 向右流动。  

- **驻波** $\psi(x) = A\sin(kx)$：  
  $$
  J=0.
  $$
  波是来回叠加，概率没有净流动。  

