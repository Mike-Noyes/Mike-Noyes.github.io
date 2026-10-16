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

* Let $z = x^2 - xy + y^2$, where $x = e^{2t}$ and $y = \ln(t + 1)$. Find $\frac{dz}{dt}$ when $t = 0$.

  <details>
  <summary><strong>Solution</strong></summary>

  By the chain rule:
  $$\frac{dz}{dt} = \frac{\partial z}{\partial x} \frac{dx}{dt} + \frac{\partial z}{\partial y} \frac{dy}{dt}$$

  So you need all these derivatives:
  $$\frac{\partial z}{\partial x} = 2x - y, \quad \frac{\partial z}{\partial y} = -x + 2y$$
  $$\frac{dx}{dt} = 2e^{2t}, \quad \frac{dy}{dt} = \frac{1}{t+1}$$

  Now, evaluate variables at $t = 0$: <br>
  $x(0) = e^0 = 1$ <br>
  $y(0) = \ln(1) = 0$

  Substitute these coordinates into the derivatives:
  $$\frac{\partial z}{\partial x} = 2(1) - 0 = 2$$
  $$\frac{\partial z}{\partial y} = -1 + 2(0) = -1$$
  $$\frac{dx}{dt} = 2e^0 = 2$$
  $$\frac{dy}{dt} = \frac{1}{1} = 1$$

  Plug everything in to calculate the final rate:
  $$\frac{dz}{dt} = (2)(2) + (-1)(1) = 4 - 1 = 3$$


  </details>

## Directional Derivatives (14.6)

* Find the directional derivative of $f(x, y) = x^2y^3 - 4y$ at the point $(2, 1)$ in the direction of the vector $\vec{v} = \langle 12, - 5 \rangle$.

  <details>
  <summary><strong>Solution</strong></summary>

  First, find the unit direction vector $\vec{u}$:
  $$\|\mathbf{v}\| = \sqrt{12^2 + (-5)^2} = \sqrt{144 + 25} = 13$$
  $$\vec{u} = \left\langle \frac{12}{13}, -\frac{5}{13} \right\rangle$$

  Next, find the Gradient Vector $\nabla f(x, y)$:
  $$f_x = 2xy^3$$
  $$f_y = 3x^2y^2 - 4$$
  $$\nabla f(x, y) = \langle 2xy^3, 3x^2y^2 - 4 \rangle$$

  Evaluate Gradient at $(2, 1)$:
  $$\nabla f(2, 1) = \langle 2(2)(1)^3, 3(2)^2(1)^2 - 4 \rangle = \langle 4, 8 \rangle$$

  Plug everything in to compute the Directional Derivative $D_{\vec{u}}f$:
  $$D_{\vec{u}}f(2, 1) = \nabla f(2, 1) \cdot \vec{u} = 4\left(\frac{12}{13}\right) + 8\left(-\frac{5}{13}\right)$$
  $$= \frac{48 - 40}{13} = \frac{8}{13}$$


  </details>

## Extreme Values (14.7)

* Find and classify all local extrema and saddle points of:
  $$f(x, y) = x^2 + 4xy + 5y^2 - 4x - 6y$$

  <details>
  <summary><strong>Solution</strong></summary>

  First, find critical points by calculating the first partials and setting to $0$:
  $$f_x = 2x + 4y - 4 = 0 \implies x + 2y = 2$$
  $$f_y = 4x + 10y - 6 = 0 \implies 2x + 5y = 3$$

  At this stage, you need to solve this system of equations:
  
  Multiply the first equation by $2$: $2x + 4y = 4$.
  Subtracting this from the second equation: $(2x + 5y) - (2x + 4y) = 3 - 4 \implies y = -1$.
  Substitute $y = -1$ back into $x + 2y = 2 \implies x - 2 = 2 \implies x = 4$.

  The critical point is $(4, -1)$.

  Now you need to calculate the second-order partials and find $D$:
  $$f_{xx} = 2, \quad f_{yy} = 10, \quad f_{xy} = 4$$
  $$D = f_{xx}f_{yy} - (f_{xy})^2 = (2)(10) - (4)^2 = 20 - 16 = 4$$

  Finally, classify the critical point:
  * At Point $(4, -1)$:
    $$D = 4 > 0$$
    Since $D > 0$, check $f_{xx} = 2 > 0$.
    Therefore, $(4, -1)$ is a **local minimum**.


  </details>

## Lagrange Multipliers (14.8)

* Find the extreme values of $f(x, y) = 2x + 3y$ subject to the constraint $x^2 + y^2 = 13$.

  <details>
  <summary><strong>Solution</strong></summary>

  Let $g(x, y) = x^2 + y^2 - 13 = 0$.
  Using Lagrange multipliers, we solve $\nabla f = \lambda \nabla g$:
  $$\nabla f = \langle 2, 3 \rangle$$
  $$\nabla g = \langle 2x, 2y \rangle$$

  Set up the system of equations:
  1) $2 = 2\lambda x \implies \lambda x = 1$
  2) $3 = 2\lambda y \implies 2\lambda y = 3$
  3) $x^2 + y^2 = 13$

  From (1) and (2), since $\lambda \ne 0$, we have $x = \frac{1}{\lambda}$ and $y = \frac{3}{2\lambda}$.
  Substitute these into (3):
  $$\left(\frac{1}{\lambda}\right)^2 + \left(\frac{3}{2\lambda}\right)^2 = 13 \implies \frac{1}{\lambda^2} + \frac{9}{4\lambda^2} = 13$$
  $$\frac{13}{4\lambda^2} = 13 \implies 4\lambda^2 = 1 \implies \lambda = \pm \frac{1}{2}$$

  * If $\lambda = \frac{1}{2}$: $x = 2$, $y = 3$. Point: $(2, 3)$
  * If $\lambda = -\frac{1}{2}$: $x = -2$, $y = -3$. Point: $(-2, -3)$

  Evaluate $f(x, y)$:
  * $f(2, 3) = 2(2) + 3(3) = 13$ (Maximum value)
  * $f(-2, -3) = 2(-2) + 3(-3) = -13$ (Minimum value)

  **Answer:** Maximum value is $13$, minimum value is $-13$.

  </details>

## Double Integrals of Rectangular Regions (15.1)

* Evaluate the double integral:
$$\iint_R (4x^3 + 9x^2y^2) \, dA$$
where $R = [0, 1] \times [0, 2]$.

  <details>
  <summary><strong>Solution</strong></summary>

  By Fubini's Theorem, we set up the double integral as an iterated integral. We will integrate with respect to $y$ first, and then $x$:

  $$\iint_R (4x^3 + 9x^2y^2) \, dA = \int_{0}^{1} \int_{0}^{2} (4x^3 + 9x^2y^2) \, dy \, dx$$

  First, you need to evaluate the inner integral (with respect to $y$):
  $$\int_{0}^{2} (4x^3 + 9x^2y^2) \, dy = \left[ 4x^3y + 3x^2y^3 \right]_{y=0}^{y=2}$$

  Substitute the limits:
  $$= \left( 4x^3(2) + 3x^2(2)^3 \right) - (0)$$
  $$= 8x^3 + 24x^2$$

  Now you need to evaluate the outer integral (with respect to $x$):
  $$\int_{0}^{1} (8x^3 + 24x^2) \, dx = \left[ 2x^4 + 8x^3 \right]_0^1$$
  $$= \left( 2(1)^4 + 8(1)^3 \right) - (0) = 10$$


  </details>

## Double Integrals over Non-Rectangular Regions (15.2)

* Evaluate the double integral:
$$\iint_D \frac{\sin(y)}{y} \, dA$$
where $D$ is the triangular region with vertices at $(0,0), (0,1), (1,1)$.

  <details>
  <summary><strong>Solution</strong></summary>

  The heart of this problem is picking the right order of integration.

  Looking at the integrand, there isn't a clear way to integrate this directly with respect to $y$ since this function doesn't have an elementary antiderivative (with respect to $y$).

  This means that you need to integrate with respect to $x$ first.

  Sketch the region $D$ in the $xy$-plane.  This is a triangle bounded on the right by the line $y=x$.  Since you're integrating in the order $dxdy$, you need to write this line as a function of $y$: $x=y$.

  Setting up the iterated integral in the order $dxdy$ gives:
  $$\iint_D \frac{\sin(y)}{y} \, dA = \int_{0}^{1} \int_{0}^{y} \frac{\sin(y)}{y} \, dx \, dy$$

  First, evaluate the inner integral (with respect to $x$):
  $$\int_{0}^{y} \frac{\sin(y)}{y} \, dx = \left[ x\frac{\sin(y)}{y} \right]_{x=0}^{x=y}$$
  $$= y\frac{\sin(y)}{y} - 0$$
  $$= \sin(y)$$

  Now evaluate the outer integral (with respect to $y$):
  $$\int_{0}^{1} \sin(y)\, dy = \left[ -\cos(y) \right]_0^1$$
  $$= -\cos(1)--\cos(0)$$
  $$= \cos(0)-\cos(1)$$
  $$= 1 - \cos(1)$$


  </details>
  

## Navigation

* [Back to the Midterm 2 Page](calc3_mt2.html)
* [Back to the Calc 3 Main Page](../../calc3.html)
* [Back to Home](../../index.html)
