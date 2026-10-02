# These are worked example problems that are from the Midterm 2 material.

## Functions of Several Variables (14.1)

* Find the domain of $f(x,y) = x\ln(x-y^2)$.

  **Solution:**  Since the natural log function is only defined when its input is greater than 0, we need to find   the values of $x$ and $y$ such that $x-y^2 >0$.  Rewriting this inequality gives $x>y^2$.

## Limits (14.2)

The main thing to remember about limits of functions of several variables is that there is now an infinite number of paths that can approach the point $(x_0, y_0)$.  This means that it is not enough to check one or two (or even finitely many) paths to show that a limit exists.  But, it is enough to check two paths to show that the limit doesn't exist.  If you can find two paths that lead to two different limits, then the limit does not exist.

* Evaluate $\lim_{(x,y)\to (0,0)} \frac{x^2-y^2}{x^2+y^2}$.

   **Solution:** First, take the path along the x-axis: $y=0$.  Then the limit becomes

   $$\lim_{(x,0)\to (0,0)} \frac{x^2}{x^2} = 1$$

   Now, take the second path along the y-axis: $x=0$.  This limit is

   $$\lim_{(0,y)\to (0,0)} \frac{-y^2}{y^2} = -1$$

   Since these two limits are different, the original limit does not exist.

## Partial Derivatives (14.3)

The important things to remember here are that you are treating one of the variables as a constant and differentiating with respect to the other variable just like you did in Calc 1, using all the rules and tools that you have.

* Let $f(x,y) = xy\sin(\sqrt{x})$.  Find $f_x(x,y), f_y(x,y)$.

   **Solution:** $f_x(x,y) = y\sin(\sqrt{x}) + \frac{xy\cos(\sqrt{x})}{2\sqrt{x}}$

   Here, we used the product rule and the chain rule from Calc 1.

   $f_y(x,y) = x\sin(\sqrt{x})$

There are higher-order partial derivatives, $f_{xx}(x,y), f_{yy}(x,y), f_{xy}(x,y), f_{yx}(x,y)$, and so on.  If $f_{xy}(x,y)$ and $f_{yx}(x,y)$ are continuous on some disk, then on that disk, $f_{xy}(x,y) = f_{yx}(x,y)$.  This is called *Clairaut's Theorem* and it is usually stated as "mixed second-order partials commute."

* Let $f(x,y) = x^2y^2 - 2xy$.  Find $f_{xy}(x,y)$ and $f_{yx}(x,y)$.

   **Solution:** $f_x(x,y) = 2xy^2 - 2y$ and $f_y(x,y) = 2x^2y - 2x$.  Then we have $f_{xy}(x,y) = 4xy -2$ and $f_{yx}(x,y) = 4xy -2$ and we see that these derivatives are the same.

   We could have assumed this from the beginning by noting that $f(x,y)$ is a polynomial, so all of the derivatives are also polynomials, so the function and all of its derivatives are continuous everywhere.

## Tangent Planes (14.4 and 16.6)

There are two main ways to proceed here, depending on whether you're given the surface as the graph of a function $z=f(x,y)$ or if you're given a parametric surface 

$$\vec{r}(u,v) = \langle x(u,v), y(u,v), z(u,v) \rangle$$

In the first case, the tangent plane to $z=f(x,y)$ at the point $(x_0, y_0, f(x_0, y_0))$ is given by

$$z = f(x_0, y_0) + f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y-y_0)$$

In the second case, you are given everything in terms of $u$ and $v$ and you start by converting that into information about $x,y,$ and $z$: $x_0 = x(u_0, v_0), y_0 = y(u_0, v_0),$ and $z_0 = z(u_0, v_0)$.  You then need to find the normal vector to the tangent plane using the partial derivatives of the parameterization:

$$ \vec{n}(u_0, v_0) = \vec{r}\;'_u(u_0, v_0) \times \vec{r}\;'_v(u_0, v_0)$$

Once you have this, you use the vector equation for a plane:

$$\vec{n}(\cdot \langle x-x_0, y-y_0, z-z_0 \rangle = 0$$

Both of these will be worked through below.

* Find the tangent plane to the paraboloid $z=x^2 + 2y^2$ at the point $(1, 1, 3)$.
  
  **Solution:** Start by finding the partial derivatives at the given point:

  $$f_x(1,1) = 2,  f_y(1,1) = 4$$

  Then plug everything in to the tangent plane equation:

  $$z = 3 + 2(x-1) + 4(y-1)$$

  See the Desmos 3D link for a visualization of this:

  [Tangent Plane to z=f(x,y)](https://www.desmos.com/3d/v49zwldjhu)
  
* Find the tangent plane to $\vec{r}(u,v) = \langle u, \cos(u)\cos(v), \cos(u)\sin(v) \rangle$ at the point $P(\frac{\pi}{4}, \frac{1}{2}, \frac{1}{2})$.

  **Solution:** Start by figuring out the values of $u$ and $v$ that map to the point $P$: since the first component of $\vec{r}$ is just $u$, this means that $u_0$ must equal the first coordinate of $P$.  This gives $u_0 = \frac{\pi}{4}$.  Plug this in to the other two components of $\vec{r}$ to get that $\frac{\sqrt{2}\cos(v)}{2} = \frac{1}{2}$ and the same for the third component.  A little trig work gives that $v_0=\frac{\pi}{4}$ as well.

  Now you need to find the derivatives:

  $$\vec{r}_u(u,v) = \langle 1, -\sin(u)\cos(v), -\sin(u)\sin(v)\rangle$$
  $$\vec{r}_v(u,v) = \langle 0, -\cos(u)\sin(v), \cos(u)\cos(v) \rangle$$

  Now plug in the values for $u_0$ and $v_0$ to get
  
  $$\vec{r}_u(\frac{\pi}{4}, \frac{\pi}{4}) = \langle 1, -\frac{1}{2}, -\frac{1}{2} \rangle$$
  $$\vec{r}_v(\frac{\pi}{4}, \frac{\pi}{4}) = \langle 0, -\frac{1}{2}, \frac{1}{2} \rangle$$

  The cross product of these two vectors gives the normal vector to the tangent plane:

  $$\vec{n} = \vec{r}_u(\frac{\pi}{4}, \frac{\pi}{4}) \times \vec{r}_v(\frac{\pi}{4}, \frac{\pi}{4}) = \langle -\frac{1}{2}, -\frac{1}{2}, -\frac{1}{2} \rangle$$

  Finally, put it all together to get

  $$\langle -\frac{1}{2}, -\frac{1}{2}, -\frac{1}{2} \rangle \cdot \langle x - \frac{\pi}{4}, y - \frac{1}{2}, z - \frac{1}{2} \rangle = 0$$

## The Chain Rule (14.5)

## Directional Derivatives and the Gradient (14.6)

## Extreme Values (14.7)

## Lagrange Multipliers (14.8)

## Double Integrals over Rectangles (15.1)

## Double Integrals over General Regions (15.2)

## Double Integrals in Polar Coordinates (15.3)


## Navigation

* [Back to the Midterm 2 Page](calc3_mt2.html)
* [Back to the Calc 3 Main Page](../../calc3.html)
* [Back to Home](../../index.html)
