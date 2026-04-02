# KaTeX 數學公式渲染展示

## 行內數學公式

愛因斯坦的著名方程式：$E = mc^2$

一元二次方程式的求解公式為 $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$，用於求解 $ax^2 + bx + c = 0$。

尤拉恆等式：$e^{i\pi} + 1 = 0$

## 區塊數學公式

高斯積分：

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

泰勒級數展開：

$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n$$

馬克士威方程式：

$$\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0}$$

$$\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}$$

## 矩陣

$$A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$$

## 混合內容

常態分佈的機率密度函數為：

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)$$

其中 $\mu$ 是平均值，$\sigma$ 是標準差。

## 程式碼區塊（不應渲染數學公式）

```python
# 程式碼中的錢字符號應被忽略
price = "$100"
formula = "$x^2 + y^2 = r^2$"
```

行內程式碼也不受影響：`$not_math$`
