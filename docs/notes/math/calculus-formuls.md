
# Differentiation Formulas

## Definition

$$
f'(x)=\lim_{h\to0}\frac{f(x+h)-f(x)}{h}
$$

---

# Basic Derivatives

| Function | Derivative |
|----------|------------|
| $c$ | $0$ |
| $x$ | $1$ |
| $x^n$ | $nx^{n-1}$ |
| $\sqrt{x}$ | $\frac{1}{2\sqrt{x}}$ |
| $\frac{1}{x}$ | $-\frac{1}{x^2}$ |
| $\frac{1}{x^n}$ | $-nx^{-(n+1)}$ |
| $x^{1/n}$ | $\frac{1}{n}x^{\frac1n-1}$ |

---

# Exponential Functions

- $\frac{d}{dx}(e^x)=e^x$
- $\frac{d}{dx}(a^x)=a^x\ln a$
- $\frac{d}{dx}(e^{f(x)})=e^{f(x)}f'(x)$
- $\frac{d}{dx}(a^{f(x)})=a^{f(x)}\ln(a)\,f'(x)$


---

# Logarithmic Functions

- $\frac{d}{dx}(\ln x)=\frac1x$

- $\frac{d}{dx}(\log_a x)=\frac1{x\ln a}$

- $\frac{d}{dx}(\ln(f(x)))=\frac{f'(x)}{f(x)}$

---

# Trigonometric Functions

- $\frac{d}{dx}(\sin x)=\cos x$

- $\frac{d}{dx}(\cos x)=-\sin x$

- $\frac{d}{dx}(\tan x)=\sec^2x$

- $\frac{d}{dx}(\cot x)=-\csc^2x$

- $\frac{d}{dx}(\sec x)=\sec x\tan x$

- $\frac{d}{dx}(\csc x)=-\csc x\cot x$

---

# Inverse Trigonometric Functions

- $\frac{d}{dx}(\sin^{-1}x)=\frac1{\sqrt{1-x^2}}$

- $\frac{d}{dx}(\cos^{-1}x)=\frac{-1}{\sqrt{1-x^2}}$

- $\frac{d}{dx}(\tan^{-1}x)=\frac1{1+x^2}$

- $\frac{d}{dx}(\cot^{-1}x)=\frac{-1}{1+x^2}$

- $\frac{d}{dx}(\sec^{-1}x)=\frac1{|x|\sqrt{x^2-1}}$

- $\frac{d}{dx}(\csc^{-1}x)=\frac{-1}{|x|\sqrt{x^2-1}}$

---

# Hyperbolic Functions

- $\frac{d}{dx}(\sinh x)=\cosh x$
- $\frac{d}{dx}(\cosh x)=\sinh x$
- $\frac{d}{dx}(\tanh x)=\operatorname{sech}^2x$
- $\frac{d}{dx}(\coth x)=-\operatorname{csch}^2x$
- $\frac{d}{dx}(\operatorname{sech}x)-\operatorname{sech}x\tanh x$
- $\frac{d}{dx}(\operatorname{csch}x)-\operatorname{csch}x\coth x$

---

# Algebra of Derivatives

## Sum Rule

$\frac{d}{dx}(u+v)=u'+v'$

---

## Difference Rule

$\frac{d}{dx}(u-v)=u'-v'$

---

## Constant Multiple Rule

$\frac{d}{dx}(cu)=cu'$

---

## Product Rule

$\frac{d}{dx}(uv)=u'v+uv'$

---

## Quotient Rule

$\frac{d}{dx}\left(\frac uv\right) = \frac{u'v-uv'}{v^2}$

---

## Chain Rule

$\frac{d}{dx}f(g(x))=f'(g(x))\,g'(x)$

or

$\frac{dy}{dx}=\frac{dy}{du}\cdot\frac{du}{dx}$

---

# Implicit Differentiation

Given

$$
F(x,y)=0
$$

Differentiate both sides with respect to $x$.

---

# Parametric Differentiation

If

$$
x=f(t),\qquad
y=g(t)
$$

then

$$
\frac{dy}{dx}
=
\frac{\frac{dy}{dt}}
{\frac{dx}{dt}}
$$

---

# Logarithmic Differentiation

If

$$
y=f(x)
$$

take logarithm

$$
\ln y=\ln(f(x))
$$

Differentiate:

$$
\frac{y'}{y}
=
\frac{d}{dx}\left(\ln(f(x))\right)
$$

---

# Higher-Order Derivatives

Second derivative

$$
\frac{d^2y}{dx^2}
$$

Third derivative

$$
\frac{d^3y}{dx^3}
$$

nth derivative

$$
\frac{d^ny}{dx^n}
$$

---

# Useful Identities

If

$$
y=x^x
$$

then

$$
\frac{dy}{dx}
=
x^x(1+\ln x)
$$

---

If

$$
y=u^v
$$

then

$$
\frac{dy}{dx}
=
u^v
\left(
v'\ln u
+
v\frac{u'}u
\right)
$$

---

# Gradient (Multivariable)

For

$$
f(x,y)
$$

$$
\nabla f
=
\left[
\frac{\partial f}{\partial x},
\frac{\partial f}{\partial y}
\right]^T
$$

For

$$
f(x_1,x_2,\ldots,x_n)
$$

$$
\nabla f
=
\begin{bmatrix}
\frac{\partial f}{\partial x_1}\\
\frac{\partial f}{\partial x_2}\\
\vdots\\
\frac{\partial f}{\partial x_n}
\end{bmatrix}
$$

---

# Jacobian

For

$$
F(x)=
\begin{bmatrix}
f_1\\
f_2\\
\vdots\\
f_m
\end{bmatrix}
$$

$$
J=
\left[
\frac{\partial f_i}{\partial x_j}
\right]
$$

---

# Hessian

For

$$
f(x)
$$

$$
H=
\left[
\frac{\partial^2f}
{\partial x_i\partial x_j}
\right]
$$






# Integrals







- $\int uv \  dx = u \int v \ dx - \int (u'\int v \ dx)dx \rightarrow choose \ u (ILATE)$
- $∫a \ dx=ax+C$
- $∫x^ndx=\frac{x^{n+1}}{n+1}+C( n≠−1)$
- $∫(ax+b)^ndx=\frac{(ax+b)^{n+1}}{a(n+1)}+C(for \ n≠−1)$
- $∫\frac1xdx=ln⁡|x|+C$
- $∫e^{x}dx=e^{x}+C$
- $∫e^{ax}dx=\frac1ae^{ax}+C$
- $∫a^xdx=\frac{a^x}{\ln⁡a}+C$
- $∫\ln⁡x dx=x \ln⁡x−x+C$

### Integrals with a singularity

$∫\frac1xdx=ln⁡|x|+C$

$\int \frac1xdx=ln⁡|x|+ \begin{cases}A & x>0; \\B& x<0\end{cases}$

### Rational functions

- $∫a \ dx=ax+C$
    
    The following function has a non-integrable singularity at 0 for *n* ≤ −1:
    
- $∫x^ndx=\frac{x^{n+1}}{n+1}+C( n≠−1)$ Cavalieri's quadrature formula)
- $∫(ax+b)^ndx=\frac{(ax+b)^{n+1}}{a(n+1)}+C(for \ n≠−1)$
- $∫\frac1xdx=ln⁡|x|+C$
- $∫\frac1xdx=\begin {cases} ln⁡|x|+C^− &x<0 \\ ln⁡|x|+C^+ &x>0\end{cases}$
- $∫\frac {c}{ax+b}dx=\frac ca \ln⁡|ax+b|+C$

### Exponential functions

- $∫e^{ax}dx=\frac1ae^{ax}+C$
- $∫f^′(x)e^{f(x)}dx=e^{f(x)}+C$
- $∫a^xdx=\frac{a^x}{\ln⁡a}+C$
- $∫e^x(f(x)+f^′(x))dx=e^xf(x)+C$
- $∫e^x(f(x)−(−1)^n \frac {d^nf(x)}{dx^n})dx=e^x∑_{k=1}^{n}(−1)^{k−1} \frac{d^{k−1}f(x)}{dx^{k−1}}+C$ (if n  is a positive integer)
- $∫e^{−x}(f(x)− \frac{d^nf(x)}{dx^n})dx=−e^{−x}∑_{k=1}^{n} \frac{d^{k−1}f(x)}{dx^{k−1}}+C$ (if n  is a positive integer)