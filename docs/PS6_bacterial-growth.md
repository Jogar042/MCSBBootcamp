# Project 6: Bacterial growth and parameter fitting
Jun Allard

## Model simulation

Given the parameters of a model, we can use ODE solvers to predict the
behavior of a model, $x(t)$.

Given data, can we find which model parameters are the best fit?

1.  Write code to simulate the following model

    <span id="eq-generalized-logistic">$$\frac{dN}{dt} = \lambda N \left( 1 - \left(N/\theta\right)^\alpha\right) \qquad(1)$$</span>

    where the user (you) specifies the parameter values $\lambda=1$,
    $\theta=10^3$, $\alpha=2$, and the initial condition $N(0)=200$.
    Plot a time series of $N_\mathrm{sim}(t)$.

## Data analysis

2.  Write code that loads bacterial growth experimental data into two
    arrays: one for the amount of bacteria $N_\mathrm{exp}(t_i)$ and the
    other for the measurement time points $t_i$. Plot the time series
    $N_\mathrm{exp}(t_i)$.
3.  Plot the solution $N(t)$ and the experimental data
    $N_\mathrm{exp}(t)$ on the same axes. Set $N(0)$ to match the
    experimental data exactly. Manually explore different parameter
    values of $\lambda,\theta,\alpha$ to see which values best fit the
    data.

## Parameter learning

4.  Write code that computes the sum of squared error (SSE), which is

    $$\mathrm{SSE} = \sum_i \left( N_\mathrm{sim}(t_i) - N_\mathrm{exp}(t_i)\right)^2$$

    Hint: The Matlab solver `ode45` can take a time vector as an input
    argument. If the time vector has more than two elements, it will
    return the solution only at those elements. This is useful if you
    only need the solution at certain times $t_i$.

5.  Using the code from the previous part, create a *function* that
    takes parameters and returns the SSE. Hint: A function can be
    defined in a separate m-file.

6.  Use an automated minimization algorithm like Matlab’s `fminsearch`
    to find the parameters that minimize the sum of squared error. These
    parameters are the “best fit” or “maximum likelihood” parameters
    $\hat\lambda,\hat\theta,\hat\alpha$. Plot, on the same axes, the
    experimental and best-fit model time series, $N_\mathrm{exp}(t)$ and
    $N_\mathrm{sim}(t)$.

## Model learning

7.  Now repeat the above, but use the model with $\alpha=1$. Did the fit
    improve, or worsen?

8.  Now repeat the above, but with

    $$\frac{dN}{dt} = \lambda N.$$

    Note this is numerically the same as
    <a href="#eq-generalized-logistic" class="quarto-xref">Equation 1</a>
    with $\theta \gg N$. Did the fit improve, or worsen?
