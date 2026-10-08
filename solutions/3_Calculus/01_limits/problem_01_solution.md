To evaluate the limit 

$$
\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7},
$$

we can factor out the highest power of $n$ in the denominator ($n^2$) from both the numerator and the denominator:

$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} = \lim_{n\to\infty}\frac{n^2\left(4 - \frac{3}{n} + \frac{1}{n^2}\right)}{n^2\left(2 + \frac{5}{n} - \frac{7}{n^2}\right)}$$

Canceling $n^2$ from the top and bottom gives:

$$= \lim_{n\to\infty}\frac{4 - \frac{3}{n} + \frac{1}{n^2}}{2 + \frac{5}{n} - \frac{7}{n^2}}$$

As $n$ approaches infinity ($n \to \infty$), all terms with $n$ in the denominator approach zero:
* $\frac{3}{n} \to 0$
* $\frac{1}{n^2} \to 0$
* $\frac{5}{n} \to 0$
* $\frac{7}{n^2} \to 0$

Substituting these limits in leaves us with:

$$= \frac{4 - 0 + 0}{2 + 0 - 0} = \frac{4}{2} = 2$$

## Why the Highest-Degree Terms Determine the Result

For very large values of $n$, the terms with the highest power of $n$ ($n^2$ in this case) grow much faster than the lower-degree terms ($n$ and constants). 

As $n$ becomes extremely large, the lower-degree terms become infinitesimally small compared to $n^2$ and have a negligible effect on the overall ratio. In essence, as $n \to \infty$, the expression behaves virtually identically to just the ratio of its leading terms:

$$\lim_{n\to\infty}\frac{4n^2-3n+1}{2n^2+5n-7} \approx \lim_{n\to\infty}\frac{4n^2}{2n^2} = \frac{4}{2} = 2$$

This rule applies generally to rational functions as $n \to \infty$: if the degrees of the numerator and denominator polynomials are equal, the limit is simply the ratio of their leading coefficients.
