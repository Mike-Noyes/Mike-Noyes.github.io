# These are some review problems that will help you prepare for Midterm 2.

If you click on **Solution** a worked solution will appear.  Only do this after you have attempted the question yourself.

## Antiderivatives

* Find $\int (3x^2 + 2x) dx$.

  <details>
  <summary><strong>Solution</strong></summary>

  Using the power rule for each term:

  $$\int (3x^2 + 2x) dx = x^3 + x^2 + C$$

  </details>

* Find $\int \frac{1}{x} dx$ for $x > 0$.

  <details>
  <summary><strong>Solution</strong></summary>

  The antiderivative of $\frac{1}{x}$ is the natural logarithm:

  $$\int \frac{1}{x} dx = \ln(x) + C$$

  </details>

## Substitution

* Evaluate $\int (2x + 1)^5 dx$.

  <details>
  <summary><strong>Solution</strong></summary>

  Let $u = 2x + 1$, so $du = 2dx$ or $dx = \frac{du}{2}$:

  $$\int (2x + 1)^5 dx = \int u^5 \frac{du}{2} = \frac{1}{2} \cdot \frac{u^6}{6} + C = \frac{(2x + 1)^6}{12} + C$$

  </details>

## Integration by Parts

* Find $\int x e^x dx$.

  <details>
  <summary><strong>Solution</strong></summary>

  Let $u = x$ and $dv = e^x dx$. Then $du = dx$ and $v = e^x$:

  $$\int x e^x dx = x e^x - \int e^x dx = x e^x - e^x + C = e^x(x - 1) + C$$

  </details>

## Navigation

* [Back to the Midterm 2 Page](calc2_mt2.html)
* [Back to the Calc 2 Main Page](../../calc2.html)
* [Back to Home](../../index.html)
