Small-signal ac equations of the buck-boost converter, derived as below:

<p align="center">
  <img src="../images/Picture15.png" alt="Image1" width="300">
</p>

$$
L \frac{d\hat{i}(t)}{dt} = D\hat{v}_g(t) + D'\hat{v}(t) + (V_g - V)\hat{d}(t)
$$

$$
C \frac{d\hat{v}(t)}{dt} = -D'\hat{i}(t) - \frac{\hat{v}(t)}{R} + I\hat{d}(t)
$$

$$
\hat{i}_g(t) = D\hat{i}(t) + I\hat{d}(t)
$$

The converter contains two inputs, $\hat{d}(s)$ and $\hat{v}_{g}(d)$, hence, the ac output voltage variations can be expressed as the 
superposition of terms arising from the two inputs:

$$
\hat{v}(s) = G_{vd}(s) \hat{d}(s) + G_{vg}(s) \hat{v}_g(s)
$$

The control-to-output and line-to-output transfer functions can be defined as:

$$
G_{vd}(s) = \left. \frac{\hat{v}(s)}{\hat{d}(s)} \right|_{\hat{v}_g(s) = 0} \quad \text{and} \quad G_{vg}(s) = \left. \frac{\hat{v}(s)}{\hat{v}_g(s)} \right|_{\hat{d}(s) = 0}
$$
