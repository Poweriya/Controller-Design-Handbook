

## Introduction
### What is bode plot:
A Bode plot is a plot of the magnitude and phase of a transfer function or other complex-valued quantity, vs. frequency. Magnitude in decibels, and phase in degrees, are plotted vs. frequency, using semilogarithmic axes. The magnitude plot is effectively a log-log plot, since the magnitude is expressed in decibels and the frequency axis is logarithmic.

The magnitude in decibels (dB) is calculated using the following formula:

$$
\|G\|_{\mathrm{dB}} = 20\log_{10}\left(\|G\|\right)
$$

If $G=(\frac{f}{f_0})^n$, the magnitude in decibels (dB) is given by:

$$
\
|G|_{\mathrm{dB}}
=20\log_{10}\left|\left(\frac{f}{f_0}\right)^n\right|
=20n\log_{10}\left(\frac{f}{f_0}\right)
\
$$

<p align="center">
  <img src="../images/Image1.png" alt="Image1" width="500">
</p>

##
### Single Pole Response
Consider the RC circuit below. As illustrated, the circuit consists of a series RC branch connected to a voltage source. The transfer function is determined by the voltage divider formula shown below:

<p align="center">
  <img src="../images/RC.png" alt="Image1" width="300">
</p>

$$
H(s) = \frac{V_2(s)}{V_1(s)} = \frac{\frac{1}{sC}}{R + \frac{1}{sC}} = \frac{1}{sRC + 1}
$$

Then we have:

$$
H(s) = \frac{1}{1 + \frac{s}{\omega_0}} \quad \text{where} \quad \omega_0 = \frac{1}{RC}
$$

Since $R$ and $C$ are real positive quantities, $\omega_0$ is also real and positive. The denominator of ebove Eq contains a root at $s = -\omega_0$, and hence $G(s)$ contains a real pole in the left half of the complex plane [1].  

To find the magnitude and phase of the transfer function, we let $s = j\omega$, where $j$ is the square root of $-1$. We then find the magnitude and phase of the resulting complex-valued function. With $s = j\omega$, equation becomes[1]: 

$$
G(j\omega) = \frac{1}{\left(1 + j \frac{\omega}{\omega_0}\right)} = \frac{1 - j \frac{\omega}{\omega_0}}{1 + \left(\frac{\omega}{\omega_0}\right)^2}
$$

$$
\|G(j\omega)\| = \sqrt{\left[\text{Re}\left(G(j\omega)\right)\right]^2 + \left[\text{Im}\left(G(j\omega)\right)\right]^2} = \frac{1}{\sqrt{1 + \left(\frac{\omega}{\omega_0}\right)^2}}
$$

$$
\|G(j\omega)\|_{\text{dB}} = -20 \log_{10} \left(\sqrt{1 + \left(\frac{\omega}{\omega_0}\right)^2}\right) \text{ dB}
$$

The best practice for drawing the magnitude Bode plot of $G$ is to determine the asymptotic behavior for large and small frequencies.

$$
\omega \ll \omega_0 \text{ and } f \ll f_0 \rightarrow \left(\frac{\omega}{\omega_0}\right) \ll 1 \rightarrow \|G(j\omega)\| \approx 1 \text{ or } 0\text{dB}
$$

$$
\omega \gg \omega_0 \text{ and } f \gg f_0 \rightarrow \left(\frac{\omega}{\omega_0}\right) \gg 1 \rightarrow \|G(j\omega)\| \approx \frac{1}{\sqrt{\left(\frac{\omega}{\omega_0}\right)^2}} = \left(\frac{f}{f_0}\right)^{-1}
$$

Then the magnitude asymptotes is:

<p align="center">
  <img src="../images/Picture2.png" alt="Image1" width="500">
</p>

For evaluating exact magnitude we can use magnitude calculation in some point which are simple.

$$
\text{at } f = f_0 : \begin{cases} 
|G(j\omega_0)| = \frac{1}{\sqrt{1 + \left(\frac{\omega_0}{\omega_0}\right)^2}} = \frac{1}{\sqrt{2}} \\
\|G(j\omega_0)\|_{\text{dB}} = -20 \log_{10} \left(\sqrt{1 + \left(\frac{\omega_0}{\omega_0}\right)^2}\right) \approx -3 \text{ dB} 
\end{cases}
$$

at $f = 0.5f_0$ and $f = 2f_0$ : Similar arguments show that the exact curve lies 1dB below the asymptotes.

<p align="center">
  <img src="../images/Picture3.png" alt="Image1" width="500">
</p>

The phase of $G(j\omega_0)$ is:

$$
\angle G(j\omega) = \tan^{-1} \left( \frac{\text{Im} \{ G(j\omega) \}}{\text{Re} \{ G(j\omega) \}} \right)
$$

if: 

$$
G(j\omega) = \frac{1}{\left(1 + j \frac{\omega}{\omega_0}\right)} = \frac{1 - j \frac{\omega}{\omega_0}}{1 + \left(\frac{\omega}{\omega_0}\right)^2}
$$

Then: 

$$
\angle G(j\omega) = -\tan^{-1} \left( \frac{\omega}{\omega_0} \right)
$$

We can estimate the phase of $G(j\omega)$ for very small and large frequencies, as well as at $\omega_0$. The result is illustrated in below:

<p align="center">
  <img src="../images/Picture4.png" alt="Image1" width="500">
</p>

According to $\angle G(j\omega)$ equation, at corner frequency $(f=f_0)$, the phase is $-45^\circ$. For drawing a more accurated graph we need a third asymptote to approximate the phase. A simpler choice could be:

$$
f_a = \frac{f_0}{10}
$$
$$
f_b = 10f_0
$$

At the break frequencies,the actual phase deviates from the asymptotes by $\tan^{-1}(0.1) \approx 5.7^\circ$

Based on the explanation above, the Bode plot for a real pole (a left-half-plane or negative pole) is illustrated in the picture below:

<p align="center">
  <img src="../images/Picture5.png" alt="Image1" width="500">
</p>

Using the same approach, the magnitude and phase Bode plots for a real zero are shown below:

### Real Zero (Left half-plane zero)

<p align="center">
  <img src="../images/Picture6.png" alt="Image1" width="500">
</p>

### Right half-plane zero

<p align="center">
  <img src="../images/Picture7.png" alt="Image1" width="500">
</p>

### Inverted pole

<p align="center">
  <img src="../images/Picture8.png" alt="Image1" width="500">
</p>

### Inverted zero

<p align="center">
  <img src="../images/Picture9.png" alt="Image1" width="500">
</p>

## Review of combination
The Bode diagram of a transfer function containing several pole, zero, and gain terms, can be constructed by simple addition. At any given frequency, the magnitude (in decibels) of the composite transfer function is equal to the sum of the decibel magnitudes of the individual terms. Likewise, at a given frequency the phase of the composite transfer function is equal to the sum of the phases of the individual terms.

Suppose that we have constructed the Bode diagrams of two complex-values functions of frequency:

$$
G_3(\omega)=G_1(\omega)\,G_2(\omega)
$$

And: 

$$
G_1(\omega)=R_1(\omega)e^{j\theta_1(\omega)}
$$

$$
G_2(\omega)=R_2(\omega)e^{j\theta_2(\omega)}
$$

$$
G_3(\omega)=R_3(\omega)e^{j\theta_3(\omega)}
$$

If

$$
G_3(\omega)=G_1(\omega)\,G_2(\omega)
$$

Then:

$$
G_3(\omega)=R_1(\omega)e^{j\theta_1(\omega)}
R_2(\omega)e^{j\theta_2(\omega)}
$$

$$
G_3(\omega)=
\left(R_1(\omega)R_2(\omega)\right)
e^{j\left(\theta_1(\omega)+\theta_2(\omega)\right)}
$$

$$
\left|R_3(\omega)\right|_{\mathrm{dB}}=\left|R_1(\omega)\right|_{\mathrm{dB}}+\left|R_2(\omega)\right|_{\mathrm{dB}}
$$

---

## References

[1] [Fundamentals of Power Electronics](https://fmipa.umri.ac.id/wp-content/uploads/2016/03/R._Erickson_Fundamentals_of_Power_Electronics_pBookZZ.org_.pdf)
