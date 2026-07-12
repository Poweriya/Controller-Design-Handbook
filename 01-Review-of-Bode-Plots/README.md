# Review of Bode plots


## Introduction
### What is bode plot:
A Bode plot is a plot of the magnitude and phase of a transfer function or other complex-valued quantity, vs. frequency. Magnitude in decibels, and phase in degrees, are plotted vs. frequency, using semilogarithmic axes. The magnitude plot is effectively a log-log plot, since the magnitude is expressed in decibels and the frequency axis is logarithmic.

The magnitude in decibels (dB) is calculated using the following formula:

$$
\|G\|_{\mathrm{dB}} = 20\log_{10}\left(\|G\|\right)
$$

If $$G=(\frac{f}{f_0})^n$$, the magnitude in decibels (dB) is given by:

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

---

## References

[Fundamentals of Power Electronics](https://fmipa.umri.ac.id/wp-content/uploads/2016/03/R._Erickson_Fundamentals_of_Power_Electronics_pBookZZ.org_.pdf)
