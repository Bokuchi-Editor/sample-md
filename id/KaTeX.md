# Demo Rendering Matematika KaTeX

## Matematika Inline

Persamaan terkenal Einstein: $E = mc^2$

Rumus kuadrat adalah $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ dan digunakan untuk menyelesaikan $ax^2 + bx + c = 0$.

Identitas Euler: $e^{i\pi} + 1 = 0$

## Matematika Blok (Display)

Integral Gaussian:

$$\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}$$

Ekspansi deret Taylor:

$$f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!}(x - a)^n$$

Persamaan Maxwell:

$$\nabla \cdot \mathbf{E} = \frac{\rho}{\varepsilon_0}$$

$$\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \varepsilon_0 \frac{\partial \mathbf{E}}{\partial t}$$

## Matriks

$$A = \begin{pmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \\ a_{31} & a_{32} & a_{33} \end{pmatrix}$$

## Konten Campuran

Fungsi kepadatan probabilitas dari distribusi normal adalah:

$$f(x) = \frac{1}{\sigma\sqrt{2\pi}} \exp\left(-\frac{(x - \mu)^2}{2\sigma^2}\right)$$

di mana $\mu$ adalah rata-rata dan $\sigma$ adalah simpangan baku.

## Blok Kode (seharusnya TIDAK merender matematika)

```python
# Dollar signs in code should be ignored
price = "$100"
formula = "$x^2 + y^2 = r^2$"
```

Kode inline juga aman: `$not_math$`
