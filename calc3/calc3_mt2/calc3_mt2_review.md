# These are some review problems that will help you prepare for Midterm 2.

If you click on **Solution** a worked solution will appear.  Only do this after you have attempted the question yourself.

## Functions of Several Variables (14.1)

* Find the domain of $f(x,y) = \sqrt{16 - x^2 - y^2}$.

  <details>
  <summary><strong>Solution</strong></summary>

  For the square root to be defined, we need $16 - x^2 - y^2 \geq 0$, which gives us $x^2 + y^2 \leq 16$.

  The domain is the disk of radius 4 centered at the origin, including the boundary circle.

  </details>

* Find the range of $f(x,y) = x^2 + y^2 + 1$.

  <details>
  <summary><strong>Solution</strong></summary>

  Since $x^2 + y^2 \geq 0$ for all real $x$ and $y$, we have $f(x,y) = x^2 + y^2 + 1 \geq 1$.

  The minimum value is 1 (achieved at $(0,0)$), and there is no maximum.

  The range is $[1, \infty)$.

  </details>

## Limits (14.2)

* Show that $\lim_{(x,y)\to (0,0)} \frac{xy}{x^2 + y^2}$ does not exist.

  <details>
  <summary><strong>Solution</strong></summary>

  Along the path $y = x$:
  $$\lim_{(x,x)\to (0,0)} \frac{x \cdot x}{x^2 + x^2} = \lim_{x \to 0} \frac{x^2}{2x^2} = \frac{1}{2}$$

  Along the path $y = 0$:
  $$\lim_{(x,0)\to (0,0)} \frac{x \cdot 0}{x^2 + 0} = 0$$

  Since we get different limits along different paths, the limit does not exist.

  </details>

## Partial Derivatives (14.3)

* Find $f_x$ and $f_y$ for $f(x,y) = e^{x^2y}$.

  <details>
  <summary><strong>Solution</strong></summary>

  $$f_x(x,y) = e^{x^2y} \cdot 2xy = 2xye^{x^2y}$$

  $$f_y(x,y) = e^{x^2y} \cdot x^2 = x^2e^{x^2y}$$

  </details>

* Find $f_{xx}$ and $f_{yy}$ for $f(x,y) = \sin(xy)$.

  <details>
  <summary><strong>Solution</strong></summary>

  First, find the first partial derivatives:
  
  $$f_x(x,y) = y\cos(xy)$$
  
  $$f_y(x,y) = x\cos(xy)$$

  Then the second partial derivatives:
  
  $$f_{xx}(x,y) = -y^2\sin(xy)$$
  
  $$f_{yy}(x,y) = -x^2\sin(xy)$$

  </details>

## Tangent Planes (14.4)

* Find the equation of the tangent plane to $z = x^2 - y^2$ at the point $(2, 1, 3)$.

  <details>
  <summary><strong>Solution</strong></summary>

  First, verify the point is on the surface: $2^2 - 1^2 = 4 - 1 = 3$.

  Find the partial derivatives:
  
  First, find $f_x$: $f_x(x,y) = 2x$, so $f_x(2,1) = 4$.
  
  Second, find $f_y$: $f_y(x,y) = -2y$, so $f_y(2,1) = -2$.

  The general tangent plane equation is:

  $$z = f(x_0, y_0) + f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y - y_0)$$

  so plugging in the values from our question gives
  
  $$z = 3 + 4(x-2) - 2(y-1)$$

  which can be simplified to
  
  $$z = 4x - 2y - 3$$

  </details>
  
## Chain Rule (14.5)

*

  <details>
  <summary><strong>Solution</strong></summary>


  </details>

## Directional Derivatives (14.6)

*

  <details>
  <summary><strong>Solution</strong></summary>


  </details>

## Extreme Values (14.7)

*

  <details>
  <summary><strong>Solution</strong></summary>


  </details>

## Lagrange Multipliers (14.8)

*

  <details>
  <summary><strong>Solution</strong></summary>


  </details>

## Double Integrals of Rectangular Regions (15.1)

* Evaluate the double integral:
$$\iint_R (4x^3 + 9x^2y^2) \, dA$$
where $R = [0, 1] \times [0, 2]$.

  <details>
  <summary><strong>Solution</strong></summary>

  By Fubini's Theorem, we set up the double integral as an iterated integral. We will integrate with respect to $y$ first, and then $x$:

  $$\iint_R (4x^3 + 9x^2y^2) \, dA = \int_{0}^{1} \int_{0}^{2} (4x^3 + 9x^2y^2) \, dy \, dx$$

  **Step 1: Inner Integral (with respect to $y$)**
  $$\int_{0}^{2} (4x^3 + 9x^2y^2) \, dy = \left[ 4x^3y + 3x^2y^3 \right]_{y=0}^{y=2}$$

  Substitute the limits:
  $$= \left( 4x^3(2) + 3x^2(2)^3 \right) - (0)$$
  $$= 8x^3 + 24x^2$$

  **Step 2: Outer Integral (with respect to $x$)**
  $$\int_{0}^{1} (8x^3 + 24x^2) \, dx = \left[ 2x^4 + 8x^3 \right]_0^1$$
  $$= \left( 2(1)^4 + 8(1)^3 \right) - (0) = 10$$

  **Answer:** $10$

  </details>

## Double Integrals over Non-Rectangular Regions (15.2)

*

  <details>
  <summary><strong>Solution</strong></summary>


  </details>
  

## Navigation

* [Back to the Midterm 2 Page](calc3_mt2.html)
* [Back to the Calc 3 Main Page](../../calc3.html)
* [Back to Home](../../index.html)
