# These are worked example problems that are from the Midterm 2 material.

## Functions of Several Variables (14.1)

* Find the domain of $f(x,y) = x\ln(x-y^2)$.

  **Solution:**  Since the natural log function is only defined when its input is greater than 0, we need to find   the values of $x$ and $y$ such that $x-y^2 >0$.  Rewriting this inequality gives $y^2<x$.  Now graph the parabola $y^2=x$ with dotted lines (since it is a strict inequality) and pick a sample point (anything that's not on the dotted line you just drew).  Plug this in to the inequality and see if it's true or not.  If it's true, the region that the sample point is in is your domain.  If the inequality is not true, then the other region is the domain.  For example, the point $(1,0)$ is inside the parabola $y^2=x$.  Plugging these values in we get $0^2<1$ which is a true statement.  That means the region inside the parabola is the domain.

## Limits (14.2)

The main thing to remember about limits of functions of several variables is that there is now an infinite number of paths that can approach the point $(x_0, y_0)$.  This means that it is not enough to evaluate the limit along one, two, or even infinitely many paths.  You would need to evaluate it along **all** possible paths.  This is not easy to do.  It usually involves some kind of geometric argument based on distance to the point, or some more algebraic steps like factoring or trying to use the squeeze theorem.  Because of this, we will mostly show that limits **DON'T** exist by finding two different paths such that the limit evaluated along those paths lead to different values.

* Evaluate $\lim_\{(x,y)\to (0,0)\} \frac\{x^2-y^2\}\{x^2+y^2\}$.

   **Solution:** First, take the path along the x-axis: $y=0$.  Then the limit becomes

   $$\lim_{\(x,0)\to (0,0)\} \frac\{x^2\}\{x^2\} = 1$$

   Now, take the second path along the y-axis: $x=0$.  This limit is

   $$\lim_\{(0,y)\to (0,0)\} \frac\{-y^2\}\{y^2\} = -1$$

   Since these two limits are different, the original limit does not exist.

## Partial Derivatives (14.3)

The important things to remember here are that you are treating one of the variables as a constant and differentiating with respect to the other variable just like you did in Calc 1, using all the rules and techniques that you learned there.  Because of this, differentiating $x^2\sin(y)$ is in practice no different than differentiating $c\sin(y)$ (with respect to $y$) or $cx^2$ (with respect to $x$).

* Let $f(x,y) = xy\sin(\sqrt{x})$.  Find $f_x(x,y), f_y(x,y)$.

   **Solution:** $f_x(x,y) = y\sin(\sqrt\{x\}) + \frac\{xy\cos(\sqrt\{x\})\}\{2\sqrt\{x\}\}$

   Here, we used the product rule and the chain rule from Calc 1.

   $f_y(x,y) = x\sin(\sqrt\{x\})$

There are higher-order partial derivatives, $f_\{xx\}(x,y), f_\{yy\}(x,y), f_\{xy\}(x,y), f_\{yx\}(x,y)$, and so on.  If $f_\{xy\}(x,y)$ and $f_\{yx\}(x,y)$ are continuous on some disk, then on that disk, $f_\{xy\} = f_\{yx\}$.  This is called *Clairaut's Theorem*.

* Let $f(x,y) = x^2y^2 - 2xy$.  Find $f_\{xy\}(x,y)$ and $f_\{yx\}(x,y)$.

   **Solution:** $f_x(x,y) = 2xy^2 - 2y$ and $f_y(x,y) = 2x^2y - 2x$.  Then we have $f_\{xy\}(x,y) = 4xy -2$ and $f_\{yx\}(x,y) = 4xy -2$ and we see that these derivatives are the same.

   We could have assumed this from the beginning by noting that $f(x,y)$ is a polynomial, so all of the derivatives are also polynomials, so the function and all of its derivatives are continuous.  Then we wouldn't have needed to actually compute both mixed-roder partials.

## Tangent Planes (14.4 and 16.6)

There are two main ways to proceed here, depending on whether you're given the surface as the graph of a function $z=f(x,y)$ or if you're given a parametric surface 

$$\vec\{r\}(u,v) = \langle x(u,v), y(u,v), z(u,v) \rangle$$

In the first case, the tangent plane to $z=f(x,y)$ at the point $(x_0, y_0, f(x_0, y_0))$ is given by

$$z = f(x_0, y_0) + f_x(x_0, y_0)(x-x_0) + f_y(x_0, y_0)(y-y_0)$$

In the second case, you are given everything in terms of $u$ and $v$ and you start by converting that into information about $x,y,$ and $z$: $x_0 = x(u_0, v_0), y_0 = y(u_0, v_0),$ and $z_0 = z(u_0, v_0)$.    Then you find the partials of $\vec\{r\}$ with respect to the parameters $u$ and $v$ and evaluate them at $(u_0, v_0)$.  From here, you can form the normal vector by taking the cross product: 

$$ \vec\{n\}(u_0, v_0) = \vec\{r\}\;'_u(u_0, v_0) \times \vec\{r\}\;'_v(u_0, v_0)$$

Once you have this, you use the vector equation for a plane:

$$\vec\{n\}\cdot \langle x-x_0, y-y_0, z-z_0 \rangle = 0$$

Both of these will be worked through below.

* Find the tangent plane to the paraboloid $z=x^2 + 2y^2$ at the point $(1, 1, 3)$.
  
  **Solution:** Start by finding the partial derivatives at the given point:

  $$f_x(1,1) = 2,  f_y(1,1) = 4$$

  Then plug everything in to the tangent plane equation:

  $$z = 3 + 2(x-1) + 4(y-1)$$

  See the Desmos 3D link for a visualization of this:

  * [Tangent Plane to z=f(x,y)](https://www.desmos.com/3d/v49zwldjhu)
  
* Find the tangent plane to $\vec\{r\}(u,v) = \langle u, \cos(u)\cos(v), \cos(u)\sin(v) \rangle$ at the point $P(\frac\{\pi\}\{4\}, \frac\{1\}\{2\}, \frac\{1\}\{2\})$.

  **Solution:** Start by figuring out the values of $u$ and $v$ that map to the point $P$: since the first component of $\vec\{r\}$ is just $u$, this means that $u_0$ must equal the first coordinate of $P$, so we have that $u_0=\frac\{\pi\}\{4\}.  From here, take this value for $u_0$, plug it into the two other components of $\vec\{r\}$, set these equal to the second two coordinates of $P$ and solve for $v_0$.  This gives that $v_0=\frac\{\pi\}\{4\}$.

  Now you need to find the derivatives:

  $$\vec\{r\}_u(u,v) = \langle 1, -\sin(u)\cos(v), -\sin(u)\sin(v)\rangle$$
  
  $$\vec\{r\}_v(u,v) = \langle 0, -\cos(u)\sin(v), \cos(u)\cos(v) \rangle$$

  Now plug in the values for $u_0$ and $v_0$ to get
  
  $$\vec\{r\}_u(\frac\{\pi\}\{4\}, \frac\{\pi\}\{4\}) = \langle 1, -\frac\{1\}\{2\}, -\frac\{1\}\{2\} \rangle$$
  
  $$\vec\{r\}_v(\frac\{\pi\}\{4\}, \frac\{\pi\}\{4\}) = \langle 0, -\frac\{1\}\{2\}, \frac\{1\}\{2\} \rangle$$

  The cross product of these two vectors gives the normal vector to the tangent plane:

  $$\vec\{n\} = \vec\{r\}_u(\frac\{\pi\}\{4\}, \frac\{\pi\}\{4\}) \times \vec\{r\}_v(\frac\{\pi\}\{4\}, \frac\{\pi\}\{4\}) = \langle -\frac\{1\}\{2\}, -\frac\{1\}\{2\}, -\frac\{1\}\{2\} \rangle$$

  Finally, put it all together to get

  $$\langle -\frac\{1\}\{2\}, -\frac\{1\}\{2\}, -\frac\{1\}\{2\} \rangle \cdot \langle x - \frac\{\pi\}\{4\}, y - \frac\{1\}\{2\}, z - \frac\{1\}\{2\} \rangle = 0$$

  If you take the time to expand and simplify a bit, you get

  $$2x+2y+2z = \frac\{\pi\}\{2\}+2$$

  See the Desmos 3D link for a visualization of this:

  * [Tangent Plane to Parametric Surface](https://www.desmos.com/3d/yeix4vk0bc)

## The Chain Rule (14.5)

The thing to do when working through Chain Rule questions is to **DRAW A DIAGRAM!**  It is a very simple and accurate way to record all of the various things that you need.  It is very hard to keep track of all of the various variables involved and the dependencies between them is you don't organize all of that information somehow.  A diagram organizes it all for you.

* Let $z = x^2y + 3xy^4$, where $x = \sin(2t)$ and $y = \cos(t)$. Find $\frac\{dz\}\{dt\}$ when $t = 0$.

**Solution**
According to the multivariable chain rule:
$$\frac\{dz\}\{dt\} = \frac\{\partial z\}\{\partial x\} \frac\{dx\}\{dt\} + \frac\{\partial z\}\{\partial y\} \frac\{dy\}\{dt\}$$

**Step 1: Compute partial derivatives and derivatives**
$$\frac\{\partial z\}\{\partial x\} = 2xy + 3y^4$$
$$\frac\{\partial z\}\{\partial y\} = x^2 + 12xy^3$$

$$\frac\{dx\}\{dt\} = 2\cos(2t)$$
$$\frac\{dy\}\{dt\} = -\sin(t)$$

**Step 2: Evaluate variables at $t = 0$**
* $x(0) = \sin(0) = 0$
* $y(0) = \cos(0) = 1$

Now substitute $x = 0$ and $y = 1$ into the partial derivatives:
$$\frac\{\partial z\}\{\partial x\} = 2(0)(1) + 3(1)^4 = 3$$
$$\frac\{\partial z\}\{\partial y\} = (0)^2 + 12(0)(1)^3 = 0$$

Evaluate the $t$-derivatives at $t = 0$:
$$\frac\{dx\}\{dt\} = 2\cos(0) = 2$$
$$\frac\{dy\}\{dt\} = -\sin(0) = 0$$

**Step 3: Calculate the final rate**
$$\frac\{dz\}\{dt\} = (3)(2) + (0)(0) = 6$$

**Answer:** $6$


## Directional Derivatives and the Gradient (14.6)

The formula if obviously important:

\[D_\{\vec{u}\}f(x_0,y_0) = \nabla f(x_0,y_0)\cdot \vec\{u\}\]

But the main thing that you have to remember when using the formula is that $\vec\{u\}$ needs to be a **unit vector** (that's why we use $\vec\{u\}$ here).  If it's not a unit vector, then you have to normalize it first.

* Find the directional derivative of $f(x, y) = e^{xy} + y^2$ at the point $(2, 0)$ in the direction of the vector $\vec\{v\} = \langle 3, 4\rangle$.

**Solution**

**Step 1: Find the unit direction vector $\vec\{u\}$**
$$\|\vec\{v\}\| = \sqrt{3^2 + 4^2} = 5$$
$$\vec\{u\} = \frac\{\vec\{v\}\}\{\|\vec\{v\}\|\} = \left\langle \frac\{3\}\{5\}, \frac\{4\}\{5\} \right\rangle$$

**Step 2: Find the Gradient Vector $\nabla f(x, y)$**
$$f_x = ye^\{xy\}$$
$$f_y = xe^\{xy\} + 2y$$
$$\nabla f(x, y) = \langle ye^\{xy\}, xe^\{xy\} + 2y \rangle$$

**Step 3: Evaluate Gradient at $(2, 0)$**
$$\nabla f(2, 0) = \langle 0 \cdot e^0, 2 \cdot e^0 + 2(0) \rangle = \langle 0, 2 \rangle$$

**Step 4: Compute the Directional Derivative $D_{\mathbf{u}}f$**
$$D_\{\vec\{u\}\}f(2, 0) = \nabla f(2, 0) \cdot \vec\{u\}$$
$$= \langle 0, 2 \rangle \cdot \left\langle \frac\{3\}\{5\}, \frac\{4\}\{5\} \right\rangle$$
$$= 0\left(\frac\{3\}\{5\}\right) + 2\left(\frac\{4\}\{5\}\right) = \frac\{8\}\{5\}$$

**Answer:** $\frac\{8\}\{5\}$

## Extreme Values (14.7)

The main tool here is the second derivative test.  But since you'll be testing critical points you need to also remember what they are.

A point $(x_0, y_0)$ is a critical point if $f_x(x_0,y_0) = 0$ and $f_y(x_0, y_0) = 0$ (technically speaking, one or both of the partial derivatives could not exist at the point, but this really doesn't happen with the functions we are working with).  So, first, take the first-order partials and find all the critical points.

Now you use the second derivative test.  This is just something that has to be memorized.  Let $D=\f_\{xx\}f_\{yy\}-(f_\{xy\})^2$.  Then there are four things that can happen:

 1) $D>0$ and $f_\{xx\}<0$ and you have a **local max**
 2) $D>0$ and $f_\{xx\}>0$ and you have a **local min**
 3) $D<0$ and you have a **saddle point**
 4) $D=0$ and the test is inconclusive

If you ever can't remember how things work with the first three above, work through $f(x,y)=x^2+y^2$.  This is a paraboloid centered at the origin so the critical point at $(0,0)$ is a min.  $f_x = 2x, f_y=2y, f_\{xx\} = 2, f_\{yy\}=2, f_\{xy\}=0$.  So, $D = 2*2 - 0^2 >0$ and $f_\{xx\}=2>0$.

Also keep in mind that both local maxs and local mins have the same behavior from $D$.  The only thing that changes is the $f_\{xx\}$.  So if you see from the above test that $D>0$ and $f_\{xx\}>0$ gives local min, then you must have $D>0, f_\{xx\}<0$ gives local max (the $D$ inequality is the same).

* Find and classify all local extrema and saddle points of:
$$f(x, y) = x^3 - 3x + y^2$$

**Solution**

**Step 1: Find Critical Points**
Calculate the first partial derivatives and set them to $0$:
$$f_x = 3x^2 - 3 = 0 \implies x^2 = 1 \implies x = \pm 1$$
$$f_y = 2y = 0 \implies y = 0$$

The critical points are $(1, 0)$ and $(-1, 0)$.

**Step 2: Calculate Second Partials and the Discriminant $D$**
$$f_\{xx\} = 6x, \quad f_\{yy\} = 2, \quad f_\{xy\} = 0$$
$$D(x, y) = f_\{xx\}f_\{yy\} - (f_\{xy\})^2 = (6x)(2) - 0^2 = 12x$$

**Step 3: Classify each critical point**
* **For Point $(1, 0)$**:
  $$D(1, 0) = 12(1) = 12 > 0$$
  Since $D > 0$, check $f_\{xx\}(1, 0) = 6(1) = 6 > 0$.
  Therefore, $(1, 0)$ is a **local minimum**.

* **For Point $(-1, 0)$**:
  $$D(-1, 0) = 12(-1) = -12 < 0$$
  Since $D < 0$, $(-1, 0)$ is a **saddle point**.

**Answer:** Local minimum at $(1, 0)$ with value $f(1, 0) = -2$; Saddle point at $(-1, 0)$.

## Lagrange Multipliers (14.8)

Okay, you need to not turn this into a boogeyman.  It is as algorithmic as the second derivative test.  Learn the process, even if you don't fully understand why it works (you should try to understand this, but the process will be enough to get you through most of the things that you'll see on a midterm).  The easiest way to learn the process is to do it a few times yourself.  Work through the example below.

* Find the extreme values of $f(x, y) = xy$ subject to the constraint $x^2 + y^2 = 8$.

**Solution**
Let the constraint function be $g(x, y) = x^2 + y^2 - 8 = 0$.
Using Lagrange multipliers, we solve $\nabla f = \lambda \nabla g$ along with the constraint equation.

Calculate the gradients:
$$\nabla f = \langle y, x \rangle$$
$$\nabla g = \langle 2x, 2y \rangle$$

Set up the system of equations:
1) $y = 2\lambda x$
2) $x = 2\lambda y$
3) $x^2 + y^2 = 8$

If we multiply (1) by $y$ and (2) by $x$:
$$y^2 = 2\lambda xy$$
$$x^2 = 2\lambda xy$$
Thus, $x^2 = y^2$.

Substitute $x^2 = y^2$ into the constraint (3):
$$x^2 + x^2 = 8 \implies 2x^2 = 8 \implies x^2 = 4 \implies x = \pm 2$$

Since $y^2 = x^2$, we also get $y = \pm 2$. This yields four critical points:
$$(2, 2), \quad (2, -2), \quad (-2, 2), \quad (-2, -2)$$

Evaluate $f(x, y) = xy$ at these points:
* $f(2, 2) = 4$ (Maximum value)
* $f(-2, -2) = 4$ (Maximum value)
* $f(2, -2) = -4$ (Minimum value)
* $f(-2, 2) = -4$ (Minimum value)

**Answer:** Maximum value is $4$, minimum value is $-4$.

## Double Integrals over Rectangles (15.1)

These are the nicest integrals that we'll see all semester.  Because you are integrating over a rectangular region, you can change the order of integration without worrying about the bounds changing.  If you have an integrand that is complicated (or impossible) to do in one order, just change the order.  You still will have to do multiple steps to evaluate the integral, but that's to be expected.  There's a huge difference between having to do multiple relatively simple steps that you don't mess up to ultimately get to the correct answer and doing multiple difficult steps that you do mess up and you end up with something that is incorrect.

* Evaluate the double integral:
$$\iint_R (6x^2y - 2x) \, dA$$
where $R = [0, 2] \times [1, 3]$.

**Solution**
By Fubini's Theorem (which is the formal name for this equality between double integrals and iterated integrals), we can set up the double integral as an iterated integral. We will integrate with respect to $y$ first, and then $x$:

$$\iint_R (6x^2y - 2x) \, dA = \int_0^2 \int_1^3 (6x^2y - 2x) \, dy \, dx$$

**Step 1: Inner Integral (with respect to $y$)**
$$\int_1^3 (6x^2y - 2x) \, dy = \left[ 3x^2y^2 - 2xy \right]_\{y=1\}^\{y=3\}$$

Substitute the upper and lower limits:
$$= \left( 3x^2(3)^2 - 2x(3) \right) - \left( 3x^2(1)^2 - 2x(1) \right)$$
$$= (27x^2 - 6x) - (3x^2 - 2x)$$
$$= 24x^2 - 4x$$

**Step 2: Outer Integral (with respect to $x$)**
$$\int_0^2 (24x^2 - 4x) \, dx = \left[ 8x^3 - 2x^2 \right]_0^2$$
$$= \left( 8(2)^3 - 2(2)^2 \right) - (0)$$
$$= (64 - 8) = 56$$

**Answer:** $56$



## Double Integrals over General Regions (15.2)

This is more subtle than integrals over rectangular regions.  Pay attention to the geometry of the region $D$ in the $xy$-plane.  Understand the boundaries (the non-vertical and non-horizontal parts of it) and think about filling this region with either vertical or horizontal lines.  This will give you your bounds.  

Something to keep in mind.  If you're not sure which order to integrate in, just pick one and see what happens.  It will either work and you're done, or it won't work and now you know which order you should use (the other one).  Then use the other order and evaluate the integral.

* Evaluate the double integral:
$$\iint_D xy \, dA$$
where $D$ is the region bounded by $y = x^2$ and $y = 2x$.

**Solution**
First, find the points of intersection to determine the integration limits:
$$x^2 = 2x \implies x^2 - 2x = 0 \implies x(x - 2) = 0$$
So, the curves intersect at $x = 0$ and $x = 2$. In this interval, $2x \ge x^2$, so $y$ ranges from $x^2$ to $2x$.

Setting up the iterated integral as a Type I region:
$$\iint_D xy \, dA = \int_0^2 \int_\{x^2\}^\{2x\} xy \, dy \, dx$$

**Step 1: Inner Integral (with respect to $y$)**
$$\int_\{x^2\}^\{2x\} xy \, dy = \left[ \frac\{1\}\{2\}xy^2 \right]_\{y=x^2\}^\{y=2x\}$$
$$= \frac{1}{2}x(2x)^2 - \frac{1}{2}x(x^2)^2$$
$$= 2x^3 - \frac{1}{2}x^5$$

**Step 2: Outer Integral (with respect to $x$)**
$$\int_0^2 \left( 2x^3 - \frac{1}{2}x^5 \right) \, dx = \left[ \frac\{1\}\{2\}x^4 - \frac\{1\}\{12\}x^6 \right]_0^2$$
$$= \left( \frac\{1\}\{2\}(16) - \frac\{1\}\{12\}(64) \right) - 0$$
$$= 8 - \frac\{16\}\{3\} = \frac\{8\}\{3\}$$

**Answer:** $\frac\{8\}\{3\}$



## Navigation

* [Back to the Midterm 2 Page](calc3_mt2.html)
* [Back to the Calc 3 Main Page](../../calc3.html)
* [Back to Home](../../index.html)
