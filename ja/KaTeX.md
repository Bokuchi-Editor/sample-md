# KaTeX 数式レンダリングデモ

## インライン数式

アインシュタインの有名な方程式: $E = mc^2$

二次方程式の解の公式は $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ で、$ax^2 + bx + c = 0$ を解くことができます。

オイラーの等式: $e^{i\pi} + 1 = 0$

## ディスプレイ数式（ブロック）

ガウス積分:

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

テイラー級数展開:

$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n$$

マクスウェル方程式:

$$\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0}$$

$$\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}$$

## 行列

$$A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$$

## 数式と文章の混在

正規分布の確率密度関数は次のように表されます:

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)$$

ここで $\mu$ は平均、$\sigma$ は標準偏差を表します。

## コードブロック（数式がレンダリングされないことの確認）

```python
# コードブロック内のドル記号は無視されるべき
price = "$100"
formula = "$x^2 + y^2 = r^2$"
```

インラインコードも同様: `$not_math$`
