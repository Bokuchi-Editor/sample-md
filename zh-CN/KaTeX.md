# KaTeX 数学公式渲染演示

## 行内公式

爱因斯坦的著名方程：$E = mc^2$

一元二次方程求根公式为 $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$，它用于求解 $ax^2 + bx + c = 0$。

欧拉恒等式：$e^{i\pi} + 1 = 0$

## 块级公式

高斯积分：

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

泰勒级数展开：

$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n$$

麦克斯韦方程组：

$$\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0}$$

$$\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}$$

## 矩阵

$$A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$$

## 混合内容

正态分布的概率密度函数为：

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)$$

其中 $\mu$ 为均值，$\sigma$ 为标准差。

## 代码块（不应渲染数学公式）

```python
# Dollar signs in code should be ignored
price = "$100"
formula = "$x^2 + y^2 = r^2$"
```

行内代码同样安全：`$not_math$`
