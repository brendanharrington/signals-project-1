# Theoretical Analysis

## Task 1: Rover System Dynamics

### Governing Equation
Applying Newton's second law, the differential equation describing the rover's motion is:

$$M_1 \ddot{x}_1(t) = f_{motor}(t) - \mu M_1 g \dot{x}_1(t)$$

Given parameters:
- Mass of rover $M_1 = 300\,kg$
- Friction coefficient $ \mu = 0.2\,s/m $
- Lunar gravity $ g = 1.62\,m/s^2 $

The equation simplifies to:

$$
300\,\ddot{x}_1(t) + 97.2\,\dot{x}_1(t) = f_{motor}(t)
$$

### Transfer Function
Taking Laplace transforms (assuming zero initial conditions):

$$
300s^2X_1(s) + 97.2sX_1(s) = F_{motor}(s)
$$

Thus, the transfer function $ \frac{X_1(s)}{F_{motor}(s)} $ is:

$$
\frac{X_1(s)}{F_{motor}(s)} = \frac{1}{300s^2 + 97.2s}
$$

## Task 2: Response to Rectangular Pulse Input
The rectangular pulse input is given by:

$$
f_{motor}(t) = A\left[u(t)-u(t-10)\right]
$$

Laplace transform of the input is:

$$
F_{motor}(s) = A \frac{1 - e^{-10s}}{s}
$$

Thus, the rover's position in the s-domain is:

$$
X_1(s) = \frac{A(1 - e^{-10s})}{s(300s^2 + 97.2s)}
$$

## Task 3: Final Position using Final Value Theorem
Using the Final Value Theorem:

$$
x(\infty) = \lim_{s \to 0}sX_1(s) = \lim_{s \to 0}\frac{A(1 - e^{-10s})}{300s^2 + 97.2s}
$$

Evaluate this limit:

$$
x(\infty) = \frac{A \cdot 10}{97.2}
$$

To reach exactly 100 m:

$$
100 = \frac{10A}{97.2} \quad \rightarrow \quad A = 972\,N
$$

Thus, an input force amplitude $ A = 972\,N $ is required for the rover to stop precisely at 100 m.

