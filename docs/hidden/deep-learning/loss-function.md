Below are the main loss functions typically used in deep learning, with formula, derivative, and common use cases. (All derivatives are w.r.t. the model’s scalar output for a single sample; vector cases generalize component‑wise.)

---

## 1. Mean Squared Error (MSE)

**Formula (single sample)**

$\mathcal{L}_{\text{MSE}} = (y - \hat{y})^2$

**Derivative**

$\cfrac{\partial \mathcal{L}_{\text{MSE}}}{\partial \hat{y}} = -2 (y - \hat{y}) = 2(\hat{y} - y)$

**Use cases**

- Regression (predicting continuous values).
- Reconstruction loss in autoencoders / VAEs (for continuous pixels or features).

---

## 2. Mean Absolute Error (MAE / L1)

**Formula**

$\mathcal{L}_{\text{MAE}} = |y - \hat{y}|$

**Derivative** (subgradient)

$\frac{\partial \mathcal{L}_{\text{MAE}}}{\partial \hat{y}} =$
$\begin{cases}1 & \hat{y} > y \\-1 & \hat{y} < y \\\text{undefined (any value in }[-1,1]\text{)} & \hat{y} = y\end{cases}$

**Use cases**

- Regression when robustness to outliers is important.
- Sometimes for image reconstruction to encourage sharpness.

---

## 3. Binary Cross‑Entropy (BCE)

Assume a sigmoid output $p = \sigma(z)$, target $y \in \{0,1\}$

**Formula (in terms of probability ppp)**

$\mathcal{L}_{\text{BCE}} = -\left(y \log p + (1 - y)\log(1 - p)\right)$

**Derivative w.r.t. zzz (pre‑sigmoid logit)**

Using $p = \sigma(z)$ and chain rule,

$\frac{\partial \mathcal{L}_{\text{BCE}}}{\partial z} = p - y$

**Use cases**

- Binary classification (single output neuron with sigmoid).
- Multi‑label classification (one sigmoid per class, then BCE per class).

---

## 4. Categorical Cross‑Entropy (Multi‑class)

Softmax outputs $\hat{p}_k = \frac{e^{z_k}}{\sum_j e^{z_j}}$, one‑hot target y.

**Formula**

$\mathcal{L} = -\sum_{k} y_k \log \hat{p}_k$

For a single class label ccc, this becomes $-\log \hat{p}_c$.

**Derivative w.r.t. logits $z_k$**

$\frac{\partial \mathcal{L}}{\partial z_k} = \hat{p}_k - y_k$

**Use cases**

- Multi‑class classification (image classes, token classes).
- Pixel‑wise classification in segmentation (per‑pixel softmax).

---

## 5. Focal Loss (for imbalanced classification)

Let ptp_tpt be the predicted probability of the true class (for binary, $p_t = p$ if $y=1$, else $1−p$).

**Formula (binary case)**

$\mathcal{L}_{\text{focal}} = - (1 - p_t)^\gamma \log(p_t)$

with focusing parameter $\gamma > 0$

**Derivative (w.r.t. ptp_tpt)**

$\frac{\partial \mathcal{L}_{\text{focal}}}{\partial p_t} = - (1 - p_t)^\gamma \frac{1}{p_t}  + \gamma (1 - p_t)^{\gamma - 1} \log(p_t)$

(For implementation, autodiff is usually used.)

**Use cases**

- Object detection (e.g., RetinaNet) with heavy class imbalance.
- Any task where easy negatives dominate the loss.

---

## 6. Hinge Loss (margin‑based)

For scores sss, labels $y \in \{-1, +1\}$.

**Formula**

$\mathcal{L}_{\text{hinge}} = \max(0, 1 - y s)$

**Derivative w.r.t. s**

$\cfrac{\partial \mathcal{L}_{\text{hinge}}}{\partial s} = \begin{cases} - y & \text{if } 1 - y s > 0 \\ 0 & \text{otherwise} \end{cases}$

**Use cases**

- SVM‑style classification.
- Sometimes used in GAN discriminators (hinge GAN).

---

## 7. Huber Loss (Smooth L1)

For error $e = y - \hat{y}$ and parameter $\delta > 0$.

**Formula**

$\mathcal{L}_{\text{Huber}} =\begin{cases}\frac{1}{2} e^2 & |e| \le \delta \\\delta (|e| - \frac{1}{2}\delta) & |e| > \delta\end{cases}$

**Derivative w.r.t. $\hat{y}$**

$\cfrac{\partial \mathcal{L}_{\text{Huber}}}{\partial \hat{y}} = \begin{cases}- e & |e| \le \delta \\- \delta \, \text{sign}(e) & |e| > \delta \end{cases}$

**Use cases**

- Regression where both robustness (L1‑like) and smooth gradients (L2‑like) are needed.
- Bounding box regression in detection (Smooth L1).

---

## 8. Kullback–Leibler (KL) Divergence

For discrete distributions P and Q over classes:

**Formula**

$D_{\text{KL}}(P \parallel Q) = \sum_{k} P_k \log\frac{P_k}{Q_k}$

**Derivative w.r.t. QkQ_kQk**

$\frac{\partial D_{\text{KL}}}{\partial Q_k} = - \frac{P_k}{Q_k}$

(Practically, derivatives are taken w.r.t. logits of Q via chain rule.)

**Use cases**

- VAEs: KL between approximate posterior and prior in the latent space.
- Distillation / comparing output distributions (teacher–student).

---

## 9. VAE Loss (Reconstruction + KL)

For a VAE with latent posterior $q_\phi(z|x)$ and prior $p(z)$.

**Formula (for one sample)**

$\mathcal{L}_{\text{VAE}} = \underbrace{\mathbb{E}_{q_\phi(z|x)}[-\log p_\theta(x|z)]}_{\text{reconstruction loss}} + \underbrace{D_{\text{KL}}(q_\phi(z|x) \parallel p(z))}_{\text{regularizer}}$

- Reconstruction loss is often MSE or BCE.
- KL has closed form for Gaussian qqq and standard normal ppp.

**Derivative**

- Computed via reparameterization trick and autodiff; no simple scalar formula.

**Use cases**

- Generative models with continuous latent variables (VAE, β\betaβ-VAE).
- Representation learning with disentanglement (through KL weighting).

---

## 10. GAN Losses (Original Minimax)

For discriminator D(x) and generator G(z).

**Discriminator loss**

$\mathcal{L}_D = -\mathbb{E}_{x \sim p_{\text{data}}}[\log D(x)] - \mathbb{E}_{z \sim p(z)}[\log (1 - D(G(z)))]$

**Generator loss (non‑saturating)**

$\mathcal{L}_G = -\mathbb{E}_{z \sim p(z)}[\log D(G(z))]$

**Derivatives**

- W.r.t. discriminator / generator outputs: same BCE derivative forms $p−y$.
- Backpropagated through the networks via chain rule.

**Use cases**

- Image generation, style transfer, super‑resolution.
- Many variants (WGAN, WGAN‑GP, hinge GAN) modify these terms but remain adversarial.

---

## 11. Diffusion Model Noise‑Prediction Loss (DDPM)

Training objective: predict Gaussian noise ϵ\epsilonϵ added at timestep ttt.

**Formula**

$\mathcal{L}_{\text{DDPM}} = \mathbb{E}_{x, t, \epsilon} \left[ \|\epsilon - \epsilon_\theta(x_t, t)\|_2^2 \right]$

**Derivative w.r.t. ϵθ\epsilon_\thetaϵθ**

$\frac{\partial \mathcal{L}}{\partial \epsilon_\theta} = 2(\epsilon_\theta(x_t, t) - \epsilon)$

**Use cases**

- Denoising Diffusion Probabilistic Models (DDPM) and DDIM.
- Modern high‑quality image, audio, and video generative models.

---

## 12. Contrastive / InfoNCE Loss (simplified)

For a positive pair (e.g., image–text) among many negatives; similarities sis_isi.

**Formula (for one anchor)**

$\mathcal{L} = -\log \frac{\exp(s_{\text{pos}} / \tau)}{\sum_{j} \exp(s_j / \tau)}$

where τ\tauτ is a temperature.

**Derivative w.r.t. similarity sks_ksk**

$\frac{\partial \mathcal{L}}{\partial s_k} = \begin{cases} \frac{1}{\tau}\left( \text{softmax}_k - 1 \right) & k = \text{pos} \\  \frac{1}{\tau}\,\text{softmax}_k & k \ne \text{pos} \end{cases}$

**Use cases**

- CLIP‑style image–text alignment.
- Self‑supervised learning (SimCLR, MoCo, etc.).

---

If you tell which area you want to focus on (classification, VAEs, GANs, diffusion, contrastive), a shorter subset with more numeric examples can be given for that specific group.