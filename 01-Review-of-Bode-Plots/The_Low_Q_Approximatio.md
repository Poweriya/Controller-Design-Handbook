In practice, second-order transfer functions with two real poles can often be analyzed by treating them as two independent first-order systems. This approach greatly simplifies the construction of the Bode plot because the overall frequency response is obtained by combining the individual responses of each pole. Although the exact mathematical expressions for the corner frequencies may appear complicated, simple approximations are usually sufficient when the poles are well separated. These approximations not only reduce computational effort but also provide better physical insight into how the circuit parameters influence the system behavior. Consequently, engineers commonly rely on these simplified relationships during controller design and frequency-response analysis.

For quality factors less than or equal to 0.5, the denominator of the second-order transfer function has two real roots. Applying the quadratic formula yields the two corner frequencies, which can be used to represent the transfer function as two first-order poles. These expressions are valid only when the damping ratio is sufficiently low to produce distinct real poles.

For $Q\leq0.5$, the real roots of the denominator polynomial are

$$
\omega_1=
\frac{\omega_0}{Q}
\left(
\frac{1-\sqrt{1-4Q^2}}{2}
\right)
$$

$$
\omega_2=
\frac{\omega_0}{Q}
\left(
\frac{1+\sqrt{1-4Q^2}}{2}
\right)
$$

The corner frequency $\omega_2$ can be expressed:

$$
\omega_2=\frac{\omega_0}{Q} F(Q)
$$

Where $F_Q$ is:

$$
F(Q)=\frac{1}{2}\left(1+\sqrt{1-4Q^2}\right)
$$

Note that, when $Q \ll 0.5$, then $4Q^2 \ll 1$ and $F(Q)$ is approximately equal to 1. We then obtain

$$
\omega_2 \approx \frac{\omega_0}{Q} \quad \text{for } Q \ll \frac{1}{2}
$$

To derive a similar approximation for $\omega_1$, we can multiply and divide by $F(Q)$. Upon simplification of the numerator, we obtain

$$
\omega_1 = \frac{Q \omega_0}{F(Q)}
$$

Again, $F(Q)$ tends to 1 for small $Q$. Hence, $\omega_1\$ can be approximated as

$$
\omega_1 \approx Q \omega_0 \quad \text{for } Q \ll \frac{1}{2}
$$

For $Q < 0.5$, the two poles at $\omega_0$ split into real poles. One real pole occurs at corner frequency $\omega_1 < \omega_0$, while the other occurs at corner frequency $\omega_2 > \omega_0$. The corner frequencies can be easily approximated.

For the filter circuit, the parameters $Q$ and $\omega_0$ are defined accordingly. For the case when $Q \ll 0.5$, the following analytical expressions for the corner frequencies can be derived:
