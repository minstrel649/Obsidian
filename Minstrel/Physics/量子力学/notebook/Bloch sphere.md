 # 1. Bloch 球的定义

任意单量子比特态（忽略整体相位）可以写作：

$$
|\psi\rangle = \cos\frac{\theta}{2}\,|0\rangle 
+ e^{i\phi}\sin\frac{\theta}{2}\,|1\rangle,
$$

其中 $$\theta \in [0,\pi],\ \phi \in [0,2\pi)$$。

这对应到单位球面上的一个点：

$$
\vec{r} = (\sin\theta\cos\phi,\ \sin\theta\sin\phi,\ \cos\theta).
$$

这个单位球体就是 **Bloch 球**，其北极是 $$|0\rangle = |\uparrow\rangle$$，  
南极是 $$|1\rangle = |\downarrow\rangle$$。

---

# 2. 泡利矩阵和 Bloch 球旋转

一个单比特 Hamiltonian 可以写作：

$$
H = -\frac{\hbar\Omega}{2}\,\vec{n}\cdot\vec{\sigma},
$$

其中 $$\vec{n}$$ 是某个单位矢量，$$\vec{\sigma}=(X,Y,Z)$$。

演化算符是：

$$
U(t) = e^{-iHt/\hbar} 
= e^{i\frac{\Omega t}{2}\,\vec{n}\cdot\vec{\sigma}},
$$

它表示 **Bloch 球绕 $$\vec{n}$$ 轴旋转角度 $$\Omega t$$**。

---

# 3. 例子：$$H=-\mu B Y$$

写成标准形式：

$$
H = -\hbar \Omega Y, \quad \Omega = \mu B/\hbar.
$$

于是：

$$
U(t) = e^{i\Omega t Y}.
$$

这就是 Bloch 球 **绕 $$y$$ 轴旋转角度 $$2\Omega t$$** 的演化。

---

# 4. 直观理解

- 初态：$$|\uparrow\rangle$$ = 北极。  
- Hamiltonian：绕 $$y$$ 轴旋转。  
- 在时间 $$\delta t$$，态从北极开始往 Bloch 球的经线方向“旋转”一些角度。  
- 测量 $$Z$$ 就是在检查它投影到 $$Z$$ 方向（即北极/南极）的概率。  

✅ 结论：  
Bloch 球是描述单比特态的几何图像。  
在本题中，Hamiltonian $-\mu B Y$对应于 Bloch 球上绕 $y$ 轴匀速旋转。  
所以概率随时间是正弦、余弦变化，你算到的 $$\cos^2(\Omega\delta t)$$、$$\sin^2(\Omega\delta t)$$ 正是这个几何旋转的体现。

---

# 5. σ 的含义

在量子力学、量子信息里，$$\sigma$$ 通常指的是 **Pauli 矩阵**：

$$
\sigma_x = X = 
\begin{pmatrix}
0 & 1 \\ 
1 & 0
\end{pmatrix}, \quad
\sigma_y = Y =
\begin{pmatrix}
0 & -i \\ 
i & 0
\end{pmatrix}, \quad
\sigma_z = Z =
\begin{pmatrix}
1 & 0 \\ 
0 & -1
\end{pmatrix}.
$$

---

## 作用在基态上的效果

$$
\sigma_x|0\rangle = |1\rangle, \quad \sigma_x|1\rangle = |0\rangle
$$

→ 翻转 $$|0\rangle,|1\rangle$$，所以叫“比特翻转”。  

$$
\sigma_y|0\rangle = i|1\rangle, \quad \sigma_y|1\rangle = -i|0\rangle
$$

→ 也是翻转，但带相位因子。  

$$
\sigma_z|0\rangle = |0\rangle, \quad \sigma_z|1\rangle = -|1\rangle
$$

→ 不翻转，只给 $$|1\rangle$$ 加一个相位 −1。  

---

## 和 Bloch 球的关系

单比特态可以写作：

$$
\rho = \frac{1}{2}(I + \vec{r}\cdot \vec{\sigma}), 
\quad \vec{r} = (x,y,z).
$$

其中 $$\vec{\sigma} = (\sigma_x,\sigma_y,\sigma_z)$$。  

于是 Bloch 球上的坐标 $$(x,y,z)$$ 就是态的期望值：

$$
x = \langle\sigma_x\rangle, \quad
y = \langle\sigma_y\rangle, \quad
z = \langle\sigma_z\rangle.
$$
