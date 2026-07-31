# Basic Probability

1. **Experiment**: Process or phenomenon that we wish to study statistically.
Example: Tossing a fair coin.
2. **Outcome**: Result of the experiment.
Example: head is an outcome on tossing a fair coin.
3. **Sample space**: A sample space is a set that contains all outcomes of an experiment.
    - Sample space is a set, typically denoted S of an experiment.
    - example: Toss a coin: $S = \{ heads, tails \}$
4. **Event**: An event is a subset of the sample space.
- Toss a coin: S = { heads, tails }
    - Events: empty set, {heads}, {tails}, { heads, tails }
    - 4 events
- An event is said to have “occurred” if the actual outcome of the experiment belongs to the event.
- One event can be contained in another, i.e. A ⊆ B
- Complement of an event A, denoted AC = { outcomes in S not in A } = (S \ A).
- Since events are subsets, one can do complements, unions, intersections.
5. **Disjoint events**: Two events with an empty intersection are said to be disjoint events.
    - Throw a die: even number, odd number are disjoint.
    - Multiple events: E1, E2, E3, .... are disjoint if, for any i 6 = j , Ei ∩ Ej = empty set.
6. **De Morgan’s laws**: For any two events A and B,
$(A ∪ B)C = AC ∩ BC$ and $(A ∩ B)C = AC ∪ BC$ .
7. **Probability**: “Probability” is a unction P that assigns to each event a real number between 0 and 1 and satisfies the following two axioms:
(i) P (S) = 1 (probability of the entire sample space equals 1).
(ii) If E1, E2, E3, ... are disjoint events ( Could be infinitely many),
$P (E_1 ∪ E_2 ∪ E_3 ∪ ...) = P (E_1) + P (E_2) + P (E_3) + ...$
    - Probability function Assigns a value that represents chance of ccurrence of the event.
    - Higher value of the probability of an event means higher chance of occurring that event.
    - 0 means event cannot occur and 1 means event always occurs.
8. Probability of the empty set (denoted φ) equals 0. that is
P (φ) = 0
9. Let EC be the complement of Event E. Then,
P (EC ) = 1 − P (E)
10. If event E is the subset of event F , that is E ⊆ F , then
P (F ) = P (E) + P (F \ E)
⇒ P (E) ≤ P (F )
11. If E and F are events, then
P (E) = P (E ∩ F ) + P (E \ F )
P (F ) = P (E ∩ F ) + P (F \ E)
12. If E and F are events, then
P (E ∪ F ) = P (E) + P (F ) − P (E ∩ F )
13. **Equally likely events**: assign the same probability to each outcome.
14. If sample space S contains the equally likely outcomes, then
    - $P (\text{one outcome}) = \cfrac{ 1}{\text{Number of outcomes in S}}$
    - $P (event) = \cfrac{\text{Number of outcomes in event}}{\text{Number of outcomes in S}}$
15. **Conditional probability space**: Consider a probability space (S, E, P ), where S
represents the sample space, E represents the collection of events, and P represents
the probability function.
• Let B be an event in S with P (B) > 0. Now, conditional probability space given B is defined as
For any event A in the original probability space (P, S, E), the conditional prob-
ability of A given B is P (A ∩ B)
P (B) .
• It is denoted by P (A | B). And
$P (A ∩ B) = P (B)P (A | B)$
16. **Law of total probability**:
• If the events B and Bc partitioned the sample space S such that P (B1), P (B2) 6 = 0,
then for any event A of S,
$P (A) = P (A | B)P (B) + P (A | B^c)P (B^c).$
• In general, if we have k events B1, B2, · · · , Bk that partition S, then for any event
A in S,
$P (A) = \displaystyle∑_{i=1}^k
P (B_i ∩ A) =
∑_{i=1}^k
P (A | B_i)P (B_i).$
17. **Bayes’ theorem**: Let A and B are two events such that $P (A) > 0, P (B) > 0$.

 $P (A ∩ B) = P (B)P (A | B) = P (A)P (B | A)\\
⇒ P (B | A) = \cfrac{P (B)P (A | B)}{P(A)}$

In general, if the events $B_1, B_2, · · · , B_k$ partition S such that $P (B_i) \ne 0$ for $i = 1, 2, · · · , k,$ then for any event A in S such that $P (A) \ne 0$,

$\displaystyle P (B_r | A) = \displaystyle \cfrac {P (B_r)P (A | B_r)}{ \displaystyle \sum ^k_{i=1}
P (B_i)P (A | B_i)}$

for $r = 1, 2, · · · , k.$
18. **Independence of two events**: Two events A and B are independent iff
$P (A ∩ B) = P (A)P (B)$
• A and B independent $⇒ P (A | B) = P (A)$ and $(B | A) = P (B)$ for $P (A), P (B) >0$
• Disjoint events are never independent.
• A and B independent ⇒ A and Bc are independent.
• A and B independent ⇒ Ac and Bc are independent.
19. **Mutual independence of three events**: Events A, B, and C are mutually independent if
(a) $P (A ∩ B) = P (A)P (B)$
(b) $P (A ∩ C) = P (A)P (C)$
(c) $P (A ∩ B) = P (A)P (B)$
(d) $P (A ∩ B ∩ C) = P (A)P (B)P (C)$
20. **Mutual independence of multiple events**: Events A1, A2, · · · ,n are mutually independent if, $\forall \ i_1, i_2, · · · , i_k,$
$P (A_{i_1} ∩ A_{i_2} ∩ · · · A_{i_k} ∩) = P (A_{i_1} )P (A_{i_2} ) · · · P (A_{i_k} )$
n events are mutually independent ⇒ any subset with or without complementing are independent as well.
21. Occurrence of event A in a sample space is considered as success.
22. Non - occurrence of event A in a sample space is considered as failure.
23. **Repeated independent trials**:
    1. **Bernoulli trials**
        - Single Bernoulli trial:
        – Sample space is {success, failure} with P(success) = p.
        – We can also write the sample space S as {0, 1}, where 0 denotes the
        failure and 1 denotes the success with P (1) = p, P (0) = 1 − p.
        This kind of distribution is denoted by Bernoulli(p).
        - Repeated Bernoulli trials:
        – Repeat a Bernoulli trial multiple times independently.
        – For each of the trial, the outcome will be either 0 or 1.
    2. **Binomial distribution**: Perform n independent Bernoulli(p) trials.
        - It models the number of success in n independent Bernoulli trials.
        - Denoted by B(n, p).
        - Sample space is {0, 1, · · · , n}.
        - Probability distribution is given by
        $P (B(n, p) = k) = ^nC_kp^k(1 − p)^{n−k}$
        where n represents the total number trials and k represent the number of success in n trials.
        - $P (B = 0) + P (B = 1) + · · · + P (B = n) = 1 \\
        ⇒ (1 − p)^n + ^nC_2p^2(1 − p)n−2 + · · · + p^n = 1.$
    3. **Geometric distribution**: It models the number of failures the first success.
        - Outcomes: Number of trials needed for first success and is denoted by G(p).
        - Sample space: {1, 2, 3, 4, · · · }
        - $P (G = k) = P$ (first $k − 1$ trials result in 0 and $k \th$ trial result in 1.) = $(1 − p)^{k−1}p.$
        - Identity: $P (G ≤ k) = 1 − (1 − p)^k.$

## Probability distributions

1. **Uniform random variable:** $X ∼ Uniform(T )$, where $T$ is some finite set.
    - Range: Finite set T
    - PMF: $f_X (t) = \frac{1}{|T |}$ for all $t ∈ T$
2. **Bernoulli random variable:** $X ∼ Bernoulli(p)$, where 0 ≤ p ≤ 1.
• Range: {0, 1}
• PMF: $f_X (0) = 1 − p, f_X (1) = p$
3. **Binomial random variable:** $X ∼ Binomial(n, p)$, where n: positive integer, 0 ≤ p ≤ 1.
• Range: {0, 1, 2, . . . ., n}
• PMF: $fX (k) = ^nC_k p^k(1 − p)^{n−k}$
4. **Geometric random variable:** $X ∼ Geometric(p)$, where 0 < p ≤ 1.
• Range: {1, 2, . . . ., n}
• PMF: $f_X (k) = (1 − p)^{k−1}p$
5. **Negative Binomial random variable:** $X ∼ Negative \ Binomial(r, p)$, where r: posi-
tive integer, 0 < p ≤ 1.
• Range: {r, r + 1, r + 2, . . . .}
• PMF: $f_X (k) = ^{k−1}C_{r−1}(1 − p)^{k−r}p^r$
6. **Poisson random variable:** $X ∼ Poisson(λ)$, where λ > 0.
• Range: {0, 1, 2, 3, . . . .}
• PMF: $f_X (k) = \frac { e^{−λ}λ^k}{k!}$
7. **Hypergeometric random variable:** $X ∼ HyperGeo(N, r, m)$, where N, r, m: positive
integers
• Range: $\{max(0, m − (N − r)), . . . , min(r, m)\}$
• PMF: $f_X (k) = \cfrac {^rC_k^{N −r}C_{m−k}}{ ^N C_m}$


### table for discrete random variables


| Distribution | PMF $f_X(k)$ | CDF $F_X(x)$ | $E[X]$ | $\text{Var}(X)$ |
| :--- | :--- | :--- | :---: | :---: |
| **Uniform**$(A)$<br>$A = \{a, a+1, \dots, b\}$ | $\frac{1}{n}, \text{ for } k \in A$<br>$n = b - a + 1$ | $\begin{cases} 0 & x < a \\\ \frac{\lfloor x \rfloor - a + 1}{n} & a \le x < b \\\ 1 & x \ge b \end{cases}$ | $\frac{a+b}{2}$ | $\frac{n^2 - 1}{12}$ |
| **Bernoulli**$(p)$ | $\begin{cases} p & k = 1 \\\ 1-p & k = 0 \end{cases}$ | $\begin{cases} 0 & x < 0 \\\ 1-p & 0 \le x < 1 \\\ 1 & x \ge 1 \end{cases}$ | $p$ | $p(1-p)$ |
| **Binomial**$(n,p)$ | $\binom{n}{k} p^k (1-p)^{n-k}$<br>$\text{for } k = 0, 1, \dots, n$ | $\begin{cases} 0 & x < 0 \\\ \sum_{i=0}^{\lfloor x \rfloor} \binom{n}{i} p^i (1-p)^{n-i} & 0 \le x < n \\\ 1 & x \ge n \end{cases}$ | $np$ | $np(1-p)$ |
| **Geometric**$(p)$ | $(1-p)^{k-1}p$<br>$\text{for } k = 1, 2, \dots$ | $\begin{cases} 0 & x < 1 \\\ 1 - (1-p)^{\lfloor x \rfloor} & x \ge 1 \end{cases}$ | $\frac{1}{p}$ | $\frac{1-p}{p^2}$ |
| **Poisson**$(\lambda)$ | $\frac{e^{-\lambda}\lambda^k}{k!}$<br>$\text{for } k = 0, 1, \dots$ | $\begin{cases} 0 & x < 0 \\\ e^{-\lambda}\sum_{i=0}^{\lfloor x \rfloor} \frac{\lambda^i}{i!} & x \ge 0 \end{cases}$ | $\lambda$ | $\lambda$ |






### table for continous random variables




| Distribution | PDF $f_X(x)$ | CDF $F_X(x)$ | $E[X]$ | $\text{Var}(X)$ |
| :--- | :--- | :--- | :---: | :---: |
| **Uniform**$[a,b]$ | $\frac{1}{b - a}, \text{ for } a \le x \le b$ | $\begin{cases} 0 & x \le a \\\ \frac{x-a}{b-a} & a < x < b \\\ 1 & x \ge b \end{cases}$ | $\frac{a+b}{2}$ | $\frac{(b-a)^2}{12}$ |
| **Exp**$(\lambda)$ | $\lambda e^{-\lambda x}, \text{ for } x > 0$ | $\begin{cases} 0 & x \le 0 \\\ 1 - e^{-\lambda x} & x > 0 \end{cases}$ | $\frac{1}{\lambda}$ | $\frac{1}{\lambda^2}$ |
| **Normal**$(\mu, \sigma^2)$ | $\frac{1}{\sigma\sqrt{2\pi}} \exp\left( \frac{-(x-\mu)^2}{2\sigma^2} \right), -\infty < x < \infty$ | No closed form | $\mu$ | $\sigma^2$ |
| **Gamma**$(\alpha, \beta)$ | $\frac{\beta^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\beta x}, \text{ for } x > 0$ | No simple form | $\frac{\alpha}{\beta}$ | $\frac{\alpha}{\beta^2}$ |
| **Beta**$(\alpha, \beta)$ | $\frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} x^{\alpha-1} (1-x)^{\beta-1}, \text{ for } 0 < x < 1$ | No simple form | $\frac{\alpha}{\alpha+\beta}$ | $\frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}$ |










# Probability Inequalities & Limit Theorems Cheat Sheet

### 1. Markov's Inequality
Let $X$ be a discrete random variable taking non-negative values with a finite mean $\mu$. Then:
$$P(X \ge c) \le \frac{\mu}{c}$$

### 2. Chebyshev's Inequality
Let $X$ be a discrete random variable with a finite mean $\mu$ and a finite variance $\sigma^2$. Then:
$$P(|X - \mu| \ge k\sigma) \le \frac{1}{k^2}$$

### 3. Weak Law of Large Numbers (WLLN)
Let $X_1, X_2, \dots, X_n \sim \text{iid } X$ with $E[X] = \mu$ and $\text{Var}(X) = \sigma^2$.  
Define the sample mean as $\overline{X} = \frac{X_1 + X_2 + \dots + X_n}{n}$. Then:
$$P(|\overline{X} - \mu| > \delta) \le \frac{\sigma^2}{n\delta^2}$$

### 4. Using CLT to Approximate Probability
Let $X_1, X_2, \dots, X_n \sim \text{iid } X$ with $E[X] = \mu$ and $\text{Var}(X) = \sigma^2$.  
Define the sum as $Y = X_1 + X_2 + \dots + X_n$. Then:
$$\frac{Y - n\mu}{\sqrt{n}\sigma} \approx \text{Normal}(0, 1)$$

### 5. Bias of an estimator
$$\text{Bias}(\hat{\theta}, \theta) = E[\hat{\theta}] - \theta$$

### 6. Method of moments
Sample moments: $M_k(X_1, X_2, \dots, X_n) = \frac{1}{n}\sum_{i=1}^{n} X_i^k$

**Procedure:** For one parameter $\theta$
- Sample moment: $m_1$
- Distribution moment: $E(X) = f(\theta)$
- Solve for $\theta$ from $f(\theta) = m_1$ in terms of $m_1$.
- $\hat{\theta}$: replace $m_1$ by $M_1$ in the above solution.

### 7. Likelihood of i.i.d. samples
Likelihood of a sampling $x_1, x_2, \dots, x_n$, denoted:
$$L(x_1, \dots, x_n) = \prod_{i=1}^{n} f_X(x_i; \theta_1, \theta_2, \dots)$$

### 8. Maximum likelihood (ML) estimation
$$\theta_1^*, \theta_2^*, \dots = \arg\max_{\theta_1, \theta_2, \dots} \prod_{i=1}^{n} f_X(x_i; \theta_1, \theta_2, \dots)$$

### 9. Bayesian estimation
Let $X_1, \dots, X_n \sim \text{i.i.d. } X$, parameter $\Theta$.
- Prior distribution of $\Theta$: $\Theta \sim f_{\Theta}(\theta)$.
- Samples, $S$: $(X_1 = x_1, \dots, X_n = x_n)$
- Posterior: $\Theta \mid (X_1 = x_1, \dots, X_n = x_n)$
- Bayes' rule: $\text{Posterior} \propto \text{Prior} \times \text {Likelihood}$
- Posterior density $\propto f_{\Theta}(\theta) \times P(X_1 = x_1, \dots, X_n = x_n \mid \Theta = \theta)$

### 10. Normal samples with unknown mean and known variance
$X_1, \dots, X_n \sim \text{i.i.d. Normal}(M, \sigma^2)$.  
Prior $M \sim \text{Normal}(\mu_0, \sigma_0^2)$.  
$$\text{Posterior mean: } \hat{\mu} = \overline{X}\left(\frac{n\sigma_0^2}{n\sigma_0^2 + \sigma^2}\right) + \mu_0\left(\frac{\sigma^2}{n\sigma_0^2 + \sigma^2}\right)$$


