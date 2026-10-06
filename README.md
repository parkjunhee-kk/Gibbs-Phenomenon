# The Gibbs Phenomenon

**Dirichlet Kernel Analysis of Fourier Partial Sums near a Jump Discontinuity**

Junhee Park, Hanreul Kang

📄 **[Full report (PDF)](Gibbs_Phenomenon.pdf)**

<p align="center"><img src="gibbs_figure.png" width="800"></p>

## Overview

When a function has a jump discontinuity, its Fourier partial sums overshoot near the jump, and this overshoot **does not vanish** as the number of terms $N \to \infty$. This report explains why, using the Dirichlet kernel, and derives the universal overshoot constant

$$
\left(\frac{1}{\pi}\mathrm{Si}(\pi) - \frac{1}{2}\right)\Delta \approx 0.08949\,\Delta,
\qquad \mathrm{Si}(u) = \int_0^u \frac{\sin t}{t}\,dt,
$$

where $\Delta$ is the size of the jump.

## Main Results

**1. Dirichlet kernel and convolution.** The partial sums can be written as

$$
S_N f(x) = \frac{1}{2\pi}\int_{-\pi}^{\pi} f(x-t)\,D_N(t)\,dt,
\qquad
D_N(t) = \frac{\sin\left((N+\tfrac12)t\right)}{\sin(t/2)}.
$$

**2. Dirichlet's theorem.** If $f$ is $2\pi$-periodic, piecewise continuous, and has one-sided limits and one-sided derivatives at every point, then

$$
\lim_{N\to\infty} S_N f(x) = \frac{f(x+) + f(x-)}{2}.
$$

The proof uses the Riemann–Lebesgue lemma, which is also proved in full.

**3. Gibbs constant.** For the square wave ($\Delta = 2$), with $N = 2M-1$ and the first peak located at $x_M = \pi/(2M)$,

$$
\lim_{M\to\infty} S_{2M-1} f\!\left(\frac{u}{2M}\right) = \frac{2}{\pi}\,\mathrm{Si}(u),
\qquad
\lim_{M\to\infty} S_{2M-1} f(x_M) = \frac{2}{\pi}\,\mathrm{Si}(\pi) \approx 1.17898.
$$

The peak moves toward the jump but its height stays fixed, so the convergence is **not uniform**.

## Numerical Verification

| $N$ | overshoot / $\Delta$ |
|---:|---:|
| 1 | 0.136620 |
| 5 | 0.094178 |
| 15 | 0.090142 |
| 99 | 0.089507 |
| 999 | 0.089490 |
| $\infty$ | **0.089490** |

## Contents of the Report

1. Introduction
2. Fourier series on $[-\pi, \pi]$ and the statement of Dirichlet's theorem
3. The Dirichlet kernel: complex form, closed form, sine representation, convolution, integral identity
4. Proof of Dirichlet's theorem (including the Riemann–Lebesgue lemma)
5. The Gibbs phenomenon: square-wave analysis, Gibbs constant, numerical verification, universality
6. Conclusion

## References

- J. W. Gibbs, Fourier's series, *Nature* **59** (1899), 606.
- E. Hewitt and R. E. Hewitt, The Gibbs–Wilbraham phenomenon: an episode in Fourier analysis, *Archive for History of Exact Sciences* **21** (1979), 129–160.
- E. M. Stein and R. Shakarchi, *Fourier Analysis: An Introduction*, Princeton University Press, 2003.
