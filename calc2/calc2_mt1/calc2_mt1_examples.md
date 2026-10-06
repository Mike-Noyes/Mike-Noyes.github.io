# These are worked example problems that are from the Midterm 2 material.

## Antiderivatives

* Find $\int x^3 dx$.

  **Solution:**  Using the power rule for integration, $\int x^3 dx = \frac{x^4}{4} + C$.

## Substitution

The main thing to remember about substitution is that we need to identify a function and its derivative within the integrand.

* Evaluate $\int 2x e^{x^2} dx$.

   **Solution:** Let $u = x^2$, so $du = 2x dx$. Then the integral becomes

   $$\int e^u du = e^u + C = e^{x^2} + C$$

## Integration by Parts

The important things to remember here are that we are using the product rule in reverse, and we need to choose our $u$ and $dv$ carefully.

* Let $\int x \cos(x) dx$.

   **Solution:** Let $u = x$ and $dv = \cos(x) dx$. Then $du = dx$ and $v = \sin(x)$.

   Using integration by parts:

   $$\int x \cos(x) dx = x \sin(x) - \int \sin(x) dx = x \sin(x) + \cos(x) + C$$

## Navigation

* [Back to the Midterm 1 Page](calc2_mt1.html)
* [Back to the Calc 2 Main Page](../../calc2.html)
* [Back to Home](../../index.html)
