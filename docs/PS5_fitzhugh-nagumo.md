# Project 5: FitzHugh-Nagumo and excitability
Jun Allard

## Background, model, and Part I

The phenomenon of excitability exists in many biological systems,
including in the electrophysiology of neurons. The FitzHugh-Nagumo
equations

$$\begin{aligned}
\frac{dv}{dt} &= v - \frac{1}{3} v^3 - w \\
\frac{dw}{dt} &= \epsilon \left( v + a - bw\right)
\end{aligned}$$

describe neuron electrophysiology where, roughly speaking, $v$ is the
electrical potential (voltage) across the cell’s membrane, and $w$ is
the activity of ion pumps. The parameters $\epsilon$, $a$ and $b$
represent properties of the ion pumps. The model has been
nondimensionalized. Both $v$ and $w$ can be negative or positive.

1.  Confirm that for $\epsilon=0.08$, $a=0.5$, $b=0.2$, the system is
    oscillatory.
2.  Confirm that for $\epsilon=0.08$, $a=1.0$, $b=0.2$, the system has
    the following property: if you choose initial conditions
    $v(0)=-1.5$, $w(0)=-0.5$, the system evolves directly towards a
    stable steady state, but if you choose initial conditions
    $v(0)=0.0$, $w(0)=-0.5$, the system moves away from the steady state
    before eventually converging towards it. This behavior is called
    *excitability*. At these parameters, what is the steady state value
    of $v$ and $w$?

## Part II: Current injection

Assume the neuron is at rest (at its steady state), and another cell
injects a current into it. The current is injected between $t=40$ and
$t=47$, and has a strength of $I_0=1.0$. In the model, this means

$$\begin{aligned}
\frac{dv}{dt} &= v - \frac{1}{3} v^3 - w + I(t)\\
\frac{dw}{dt} &= \epsilon \left( v + a - bw\right)
\end{aligned}$$

where

$$I(t) = \begin{cases}
I_0 & \qquad t_\mathrm{start} < t < t_\mathrm{stop}\\
0 & \qquad \text{otherwise}
\end{cases}$$

or, in Matlab,

``` matlab
I0 = 1.0;
tStart = 40;
tStop = 47;
I = @(t) I0*(t>tStart).*(t<tStop);
```

3.  At the excitable parameters from above ($a=1.0$), simulate the
    system with initial conditions at the steady state (or very close),
    and simulate a 7-second injection starting at $t=40$ as above.

## Part III: Ring of ten cells

Neurons are connected in a neural network. Suppose there are ten cells,
each with membrane potential and ion pump activity obeying the
FitzHugh-Nagumo equations for $v_i(t)$ and $w_i(t)$ where
$i=1 \ldots 10$ indexes the cells. The cells are electrically connected
so that

$$\begin{aligned}
\frac{dv_i}{dt} &= v_i - \frac{1}{3} v_i^3 - w_i + I_i(t) + D\left( v_{i-1} - 2 v_i + v_{i+1}\right)\\
\frac{dw_i}{dt} &= \epsilon \left( v_i + a - bw_i\right)
\end{aligned}$$

where $D=0.9$ is a new parameter that describes the electrical
connectivity of the neighboring cells. The ion pumps are not connected
between cells, so the $w$ equation is unchanged. For simplicity, let’s
assume the cells are connected in a ring, so that

$$\frac{dv_1}{dt} = v_1 - \frac{1}{3} v_1^3 - w_1 + I_1(t) + D\left( v_{10} - 2 v_1 + v_{2}\right)$$

and similarly for the tenth cell,

$$\frac{dv_{10}}{dt} = v_{10} - \frac{1}{3} v_{10}^3 - w_{10} + I_{10}(t) + D\left( v_{9} - 2 v_{10} + v_{1}\right).$$

4.  Write code to simulate these ten cells. There will be 20 equations,
    $v$ and $w$ for each cell.

    1.  Assume there is no injection current. We expect all ten cells to
        settle at the same steady state. Make two plots. First, plot a
        time series of the membrane potential of all ten cells as a
        function of time. Second, make a movie of the voltage in all ten
        cells, where the horizontal axis is the cell number.

        ``` matlab
        % movie
        for nt=1:numel(T)
            figure(5); clf; hold on; box on;
            plot(X(nt,1:10));
            set(gca,'ylim', [-2.5,2.5])
            xlabel('Cell');
            ylabel('Voltage')
            drawnow;
        end
        ```

    2.  Now assume that the fourth cell (and only the fourth cell)
        receives an injection current $I(t)$ as above, between $t=40$
        and $t=47$. Make a time series with all ten cells. Make a movie
        with the voltage for all cells.[^1]

        Hint: You do not need to make it generalize to different numbers
        of cells. In other words, don’t try to make it work for an
        arbitrary number of cells and then set the number of cells
        to 10. Just make it work for 10 cells. (Unless you want to make
        it generalized.)

[^1]: This type of behavior is called an *excitable traveling wave
    pulse*. These are unlike the harmonic pulses familiar from sound
    waves, vibrations, and light. For example, when two excitable pulses
    collide, they annihilate.
