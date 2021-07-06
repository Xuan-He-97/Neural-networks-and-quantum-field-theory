# Neural-networks-and-quantum-field-theory

Many neural networks are thought to admit GP (Gaussian Process) limits, where an EFT approach is valid to solve the NGP problem. 

Previous study shows that any architecture that is a composition of multilayer perceptrons, recurrent
neural networks, skip connections, convolutions or graph convolutions, pooling, batch or layer normalization, and/or attention admits GP limit.

## Asymptotic Neural Networks

Asymptotic neural networks is related to Gaussian process. The essential idea is to regard a neural network as a function in the function space, 

<img src="https://render.githubusercontent.com/render/math?math=f_{\theta, N}: \mathbb{R}^{d_{\text {in }}} \rightarrow \mathbb{R}^{d_{\text {out }}}">, 

with distribution <img src="https://render.githubusercontent.com/render/math?math=p(f) \sim \exp \left[-\frac{1}{2} \int d^{d_{\text {in }}} x d^{d_{\text {in }}} x^{\prime} f(x) \Xi\left(x, x^{\prime}\right) f\left(x^{\prime}\right)\right]">. 

As an Gaussian process the neural network satisfies: <img src="https://render.githubusercontent.com/render/math?math=\{f(x_1), ..., f(x_k)\} \sim \mathcal{N}(\mu, \Xi^{-1})">. An assumption in this project is that the functions always have zero mean.

Knowing the function space distribution, the correlation function can be written in terms of it. 

<img src="https://render.githubusercontent.com/render/math?math=G^{(n)}(x_1, ..., x_n) = \int df f_1 ... f_n p(f) = \frac{\int df f_1 ... f_n e^{- S}}{Z}">

In free field theory, the field configuration is drawn from a Gaussian process. It is natural to connect asymptotic neural networks to free field theory, where the correlation (n-pt) function could be computed via Wick contraction:

<img src="https://render.githubusercontent.com/render/math?math=G_{GP}^{(n)}(x_1, ..., x_n) = \sum_{p\in \textrm{Wick}(x_1, ..., x_n)} K(a_1, b_1)...K(a_{n/2}, b_{n/2})">.

Neural networks fall into asymptotic limit when the width N goes to infinite. In infinite width limit, the n-pt function could be estimated by Feynman diagrams.

## NGP Neural Networks

Off its infinite width limit, the neural network does not correspond to Gaussian process anymore. Nevertheless, NGP (non-Gaussian) is used to describe its function space distribution. Instead of free field theory, effective field theory gives NGP likelihoods and thus describes neural networks with finite width.

Log-likelihood of the function space can be obtained by perturbation theory,

<img src="https://render.githubusercontent.com/render/math?math=G^{(n)}(x_1, ..., x_n) = \frac{\int df f(x_1)...f(x_n) \left[ 1 - \int d^{d_{in}}x g_k f(x)^k + O(g_k^2) \right] e^{-S_{GP}} / Z_{GP, 0}}{\int df \left[ 1 - \int d^{d_{in}}x g_k f(x)^k + O(g_k^2) \right] e^{-S_{GP}} / Z_{GP, 0}}">

and Feynman rules.

The coupling constants is determined via scaling theory and symmetry. 

<img src="https://render.githubusercontent.com/render/math?math=\lambda \sim N^{-1}, \kappa \sim N^{-2}">, 

and, 

<img src="https://render.githubusercontent.com/render/math?math=[\lambda] = -d_{in} - 4,  [\kappa] = -d_{in} - 6">

## Experiments

In this project, I tested the falling off from NGP to GP limit by varying network width N and the relation between GP deviation and N in the NGP part.

Then I draw relationship between the coupling constants and the width. The 4-pt correction is also plotted to show its effect of reducing the deviation.

Last, the coupling constants is also determined by the cutoff via RG equation. The plot of them is also drawn to verigy the RG equation.
