# Distributions list:
- Bernoulli: used for modeling binary outcomes such as coin flips
- Binomial: used for modeling the number of successes in a fixed number of Bernoulli trials
- Poisson: used for modeling the number of events in a fixed interval of time or space
- Exponential: used for modeling the time until an event occurs
- Normal: used for modeling continuous data that is symmetric and unimodal
- Uniform: used for modeling continuous data that is symmetric and unimodal
- Geometrical: used for modeling the number of Bernoulli trials until the first success

... 

### Example 2:
X and Y are Poisson independent random variables with parameters λ1 and λ2, respectively. Calculate the expected value of X given X + Y = n.

_Expectation: weighted sum of the possible values of X, where the weights are the probabilities of the values._

`E[X|X+Y=n] = Σx * P(X=x|X+Y=n)`

### Solution 2:

#### Formula for the possion distribution
$P\{X = k\} = e^{-\lambda} \cdot \frac{\lambda^k}{k!}$

#### Probability of X given X + Y = n
$P\{X = k|X + Y = n\} = \frac{P\{X = k, Y = n - k\}}{P\{X + Y = n\}} = \frac{P\{X = k, Y = n - k\}}{P\{Y = n - k\}} = $

#### Using the formula for the possion distribution
$e^{-\lambda_1} \cdot \frac{\lambda_1^k}{k!} \cdot e^{-\lambda_2} \cdot \frac{\lambda_2^{n-k}}{(n-k)!} e^{-\lambda_2} \cdot \frac{\lambda_2^{n-k}}{(n-k)!} = 
e^{-\lambda_1} \cdot \frac{\lambda_1^k}{k!}$

$=(\frac{n}{k}) * (\frac{\lambda_1}{\lambda_1 + \lambda_2}) ^ k * (\frac{\lambda_2}{\lambda_1 + \lambda_2}) ^ {n-k}$


### Example 3:
Suppose the joint density of X and Y is given by: $f(x, y) = 
6xy*(2-x-y)$ for $0 < x < y < 1$ and $0$ elsewhere. Find the marginal density of X and Y.

Compute the conditional of $X$ given that $Y = y$, and y $\in$ (0, 1).

### Solution 3:

$f_{XY} = \frac{f_{XY}(x, y)}{f_Y(y)}$

$f_Y(y) = \int_1^0 6xy * (2-x-y) dx$
$ = 6\int_1^0 (2xy - x^2y -  xy^2)dx$
$ = 6[xy^2 - \frac{x^2y^2}{2} - \frac{xy^3}{3}]_1^0$

$f_Y(y) = 
\begin{cases} 
6y - 2y^2 - 3y^3 & \text{if } y \in (0, 1) \\
0 & \text{elsewhere}
\end{cases}
$

$f(x|y) = \frac{f_{XY}(x, y)}{f_Y(y)} = \frac{6xy*(2-x-y)}{4y-3y^2} = \frac{6xy*(2-x-y)}{y(4-3y)}$

$E[X|Y] = \int_1^0 x * \frac{6x*(2-x-y)}{y(4-3y)} dx$


### Example 4:
Assuming that the miner is all times equally likely to choose any of the doors, what is the Expected length of time until the mined reaches safety?

### Solution 4:
$X$: Time until the miner reaches safety.
$Y$: The door the miner chooses.

$E[X] = E[X|Y = 1] * p(Y = 1) + E[X|Y = 2] * p(Y = 2) + E[X|Y = 3] * p(Y = 3) = \frac{1}{3} * [E[X|Y = 1] + E[X|Y = 2] + E[X|Y = 3]]$

From the picture, we can see that:

$E[X|Y = 1] = 2 Hours$
$E[X|Y = 2] = 3 Hours + E[X]$
$E[X|Y = 3] = 5 Hour + E[X]$

We plug these values into the equation and solve for $E[X]$.

$E[X] = \frac{1}{3} * [2 + 3 + 5 + E[X] + E[X]] = \frac{1}{3} * [10 + 2E[X]] = \frac{10}{3} + \frac{2}{3}E[X] = 10 Hours$

# In class exercises:

Ex2 - Q1): Define a random variable for the experiment of flipping a fair coin 3 times. Describe the sample space and assign a numerical value to each outcome.

Ex2 - Q1 - Sol): 
$X = \{HHH, HHT, HTH, HTT, THH, THT, TTH, TTT\}$
$X = \{1, 2, 3, 4, 5, 6, 7, 8\}$

Ex2 - Q2): For the random variable X representing the sum of numbers obtained when rolling two six-sided dice, calcualte $P[X = 7]$ and $P[X > 4]$

