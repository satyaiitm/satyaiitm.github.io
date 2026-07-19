## Gradient

$f(x,y,z) \to function$

$\nabla{f} = (f'_x,f'_y,f'_z)$ or $(\frac{\partial f}{\partial x},\frac{\partial f}{\partial y},\frac{\partial f}{\partial z})$   or $(\frac{\partial f}{\partial x_1},\frac{\partial f}{\partial x_2}, ..., \frac{\partial f}{\partial x_n})$ $\to$ Gradient of function $f$

$\nabla{f_{(a,b)}}$ $\to$ Gradient of $f$ at the point $(a,b)$

** limit should exist for all the quardinate or else the gradient will not exitst

## Directional Derivetive

$$
\lim_{h \to 0} \frac{f(\tilde{a} +h \hat{u}) - f(\tilde{a}))}{h} = f_{x_i}(\tilde{a}) = \frac{d }{dx_i}f(\tilde{a})
$$

- at point $\tilde{a}$
- inn the direction of unit vector $u$
- if $\hat{u}$ is the unit vector in the direction or $u$, if it is paralal to axis where $\hat{u} = e_i$

$$
D_{\frac{u}{||u||}} f(\tilde{a}) =\frac{u}{||u||} . \nabla{f(\tilde{a})} = \frac{1}{||u||} < u, \nabla{f(\tilde{a})}>
$$

if $\nabla f$ exists and continous in an open ball around point $(a_1 , a_2, ...,a_n)$ then the directional derivative of the function $f$ at point $(a_1 , a_2, ...,a_n)$ in the direction of a vector $V$, given by the dot product of gradient of function at $(a_1 , a_2, ...,a_n)$ with unit vector in the direction of $V$

$$
\begin {align*}D_u \bullet f(a_1 , a_2, ...,a_n) &= \nabla{f(a_1 , a_2, ...,a_n)} \bullet \frac{u}{||u||} \\ 
&= ||\nabla{f(\tilde{a})}|| . ||\hat {u}|| . cos\theta  \\ 
&= ||\nabla{f(\tilde{a})}|| .  cos\theta  \quad (\because ||\hat {u}|| =1) \end {align*}
$$

- $||\nabla{f(\tilde{a})}|| .  cos\theta$      is maximum if $cos \theta$ is maximum,
 and $cos \theta$ is max at $\theta = 0 ^\circ$ (that means $u$ is in the direction of $\nabla{f(\tilde{a})}$ )
- $||\nabla{f(\tilde{a})}|| .  cos\theta$      is minimum if $cos \theta$ is minimum, 
and $cos \theta$ is min at $\theta = 180 ^\circ$  (that means $u$ is in the opposit direction of $\nabla{f(\tilde{a})}$ )

$\boxed{\underset{\theta = \pi =180 ^\circ}{-1} \le cos \theta \le \underset{\theta = 0}{1}}$


**Maximum value of directional derivative**



$$
\begin{align*}
\nabla f(a,b) \cdot \mathbf{u} 
&= \left[ \nabla f(a,b) \cdot \frac{\nabla f(a,b)}{\|\nabla f(a,b)\|} \right] \\ 
&= \frac{\langle \nabla f(a,b), \nabla f(a,b) \rangle}{\|\nabla f(a,b)\|} \\
&= \frac{\|\nabla f(a,b)\|^2}{\|\nabla f(a,b)\|} \\
&= \|\nabla f(a,b)\|
\end{align*}
$$

$$
\begin{aligned}
\nabla f(a,b) \cdot \mathbf{u} 
&= \nabla f(a,b) \cdot \frac{\nabla f(a,b)}{\|\nabla f(a,b)\|} \\
&= \frac{\langle \nabla f(a,b), \nabla f(a,b) \rangle}{\|\nabla f(a,b)\|} \\
&= \frac{\|\nabla f(a,b)\|^2}{\|\nabla f(a,b)\|} \\
&= \|\nabla f(a,b)\|
\end{aligned}
$$