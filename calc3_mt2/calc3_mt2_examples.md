# These are worked example problems that are from the Midterm 2 material.

## Functions of Several Variables (14.1)

1. Find the domain of $f(x,y) = x\ln(x-y^2)$.

  **Solution:**  Since the natural log function is only defined when its input is greater than 0, we need to find   the values of $x$ and $y$ such that $x-y^2 >0$.  Rewriting this inequality gives $x>y^2$.

## Limits (14.2)

The main thing to remember about limits of functions of several variables is that there is now an infinite number of paths that can approach the point $(x_0, y_0)$.  This means that it is not enough to check one or two (or even finitely many) paths to show that a limit exists.  But, it is enough to check two paths to show that the limit doesn't exist.  If you can find two paths that lead to two different limits, then the limit does not exist.

1. Evaluate $\lim_{(x,y)\to (0,0)} \frac{x^2-y^2}{x^2+y^2}$.

   **Solution:** First, take the path along the x-axis: $y=0$.  Then the limit becomes

   $$\lim_{(x,0)\to (0,0)} \frac{x^2}{x^2} = 1$$

   Now, take the second path along the y-axis: $x=0$.  This limit is

   $$\lim_{(0,y)\to (0,0)} \frac{-y^2}{y^2} = -1$$

   Since these two limits are different, the original limit does not exist.

## Partial Derivatives (14.3)

The important things to remember here are that you are treating one of the variables as a constant and differentiating with respect to the other variable just like you did in Calc 1, using all the rules and tools that you have.

1. Let $f(x,y) = xy\sin(\sqrt{x})$.  Find $f_x(x,y), f_y(x,y)$.

   **Solution:** $f_x(x,y) = y\sin(\sqrt{x}) + \frac{xy\cos(\sqrt{x})}{2\sqrt{x}}$

   Here, we used the product rule and the chain rule from Calc 1.

   $f_y(x,y) = x\sin(\sqrt{x})$

There are higher-order partial derivatives, $f_{xx}(x,y), f_{yy}(x,y), f_{xy}(x,y), f_{yx}(x,y)$, and so on.  If $f_{xy}(x,y)$ and $f_{yx}(x,y)$ are continuous on some disk, then on that disk, $f_{xy}(x,y) = f_{yx}(x,y)$.  This is called *Clairaut's Theorem* and it is usually stated as "mixed second-order partials commute."

2. Let $f(x,y) = x^2y^2 - 2xy$.  Find $f_{xy}(x,y)$ and $f_{yx}(x,y)$.

   **Solution:** $f_x(x,y) = 2xy^2 - 2y$ and $f_y(x,y) = 2x^2y - 2x$.  Then we have $f_{xy}(x,y) = 4xy -2$ and $f_{yx}(x,y) = 4xy -2$ and we see that these derivatives are the same.

   We could have assumed this from the beginning by noting that $f(x,y)$ is a polynomial, so all of the derivatives are also polynomials, so the function and all of its derivatives are continuous everywhere.

## Tangent Planes (14.4 and 16.6)

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
