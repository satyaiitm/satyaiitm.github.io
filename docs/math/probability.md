# Basic Probability

1. **Experiment**: Process or phenomenon that we wish to study statistically.
Example: Tossing a fair coin.
2. **Outcome**: Result of the experiment.
Example: head is an outcome on tossing a fair coin.
3. **Sample space**: A sample space is a set that contains all outcomes of an experiment.
• Sample space is a set, typically denoted S of an experiment.
• example: Toss a coin: $S = \{ heads, tails \}$
4. **Event**: An event is a subset of the sample space.
• Toss a coin: S = { heads, tails }
– Events: empty set, {heads}, {tails}, { heads, tails }
– 4 events
• An event is said to have “occurred” if the actual outcome of the experiment belongs to the event.
• One event can be contained in another, i.e. A ⊆ B
• Complement of an event A, denoted AC = { outcomes in S not in A } = (S \ A).
• Since events are subsets, one can do complements, unions, intersections.
5. **Disjoint events**: Two events with an empty intersection are said to be disjoint events.
• Throw a die: even number, odd number are disjoint.
• Multiple events: E1, E2, E3, .... are disjoint if, for any i 6 = j , Ei ∩ Ej = empty set.
6. **De Morgan’s laws**: For any two events A and B,
$(A ∪ B)C = AC ∩ BC$ and $(A ∩ B)C = AC ∪ BC$ .
7. **Probability**: “Probability” is a unction P that assigns to each event a real number
between 0 and 1 and satisfies the following two axioms:
(i) P (S) = 1 (probability of the entire sample space equals 1).
(ii) If E1, E2, E3, ... are disjoint events ( Could be infinitely many),
$P (E_1 ∪ E_2 ∪ E_3 ∪ ...) = P (E_1) + P (E_2) + P (E_3) + ...$
• Probability function Assigns a value that represents chance of occurrence of the
event.
• Higher value of the probability of an event means higher chance of occurring that
event.
• 0 means event cannot occur and 1 means event always occurs.
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
• Let B be an event in S with P (B) > 0. Now, conditional probability space given
B is defined as
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
$$

\begin{array}{|l|l|l|c|c|}
\hline
\text{Distribution} & \text{PMF } (f_X(k)) & \text{CDF } (F_X(x)) & E[X] & \text{Var}(X) \\ \hline
\begin{array}{l} \text{Uniform}(A) \\ A = \{a, a+1, \dots, b\} \end{array} & 
\begin{array}{l} \frac{1}{n}, \;\; x = k \\ n = b - a + 1 \\ k = a, a+1, \dots, b \end{array} & 
\begin{cases} 0 & x < 0 \\ \frac{k-a+1}{n} & k \le x < k+1 \\ & k = a, a+1, \dots, b-1, b \\ 1 & x \ge n \end{cases} & 
\frac{a+b}{2} & \frac{n^2 - 1}{12} \\ \hline

\text{Bernoulli}(p) & 
\begin{cases} p & x = 1 \\ 1-p & x = 0 \end{cases} & 
\begin{cases} 0 & x < 0 \\ 1-p & 0 \le x < 1 \\ 1 & x \ge 1 \end{cases} & 
p & p(1-p) \\ \hline

\text{Binomial}(n,p) & 
\begin{array}{l} {}^nC_k p^k (1-p)^{n-k}, \\ k = 0, 1, \dots, n \end{array} & 
\begin{cases} 0 & x < 0 \\ \sum_{i=0}^k {}^nC_i p^i (1-p)^{n-i} & k \le x < k+1 \\ & k = 0, 1, \dots, n \\ 1 & x \ge n \end{cases} & 
np & np(1-p) \\ \hline

\text{Geometric}(p) & 
\begin{array}{l} (1-p)^{k-1}p, \\ k = 1, \dots, \infty \end{array} & 
\begin{cases} 0 & x < 0 \\ 1 - (1-p)^k & k \le x < k+1 \\ & k = 1, \dots, \infty \end{cases} & 
\frac{1}{p} & \frac{1-p}{p^2} \\ \hline

\text{Poisson}(\lambda) & 
\begin{array}{l} \frac{e^{-\lambda}\lambda^k}{k!}, \\ k = 0,1, \dots, \infty \end{array} & 
\begin{cases} 0 & x < 0 \\ e^{-\lambda}\sum_{i=0}^k \frac{\lambda^i}{i!} & k \le x < k+1 \\ & k = 0, 1, \dots, \infty \end{cases} & 
\lambda & \lambda \\ \hline
\end{array}
$$

### table for continous random variables

$$
\begin{array}{|l|l|l|c|c|}
\hline
\text{Distribution} & \text{PDF } (f_X(k)) & \text{CDF } (F_X(x)) & E[X] & \text{Var}(X) \\ \hline

\text{Uniform}[a,b] & 
\frac{1}{b - a}, \;\; a \le x \le b & 
\begin{cases} 0 & x \le a \\ \frac{x-a}{b-a} & a < x < b \\ 1 & x \ge b \end{cases} & 
\frac{a+b}{2} & \frac{(b-a)^2}{12} \\ \hline

\text{Exp}(\lambda) & 
\lambda e^{-\lambda x}, \;\; x > 0 & 
\begin{cases} 0 & x \le 0 \\ 1 - e^{-\lambda x} & x > 0 \end{cases} & 
\frac{1}{\lambda} & \frac{1}{\lambda^2} \\ \hline

\text{Normal}(\mu, \sigma^2) & 
\begin{array}{l} \frac{1}{\sigma\sqrt{2\pi}} \exp\left( \frac{-(x-\mu)^2}{2\sigma^2} \right), \\ -\infty < x < \infty \end{array} & 
\text{No closed form} & 
\mu & \sigma^2 \\ \hline

\text{Gamma}(\alpha, \beta) & 
\frac{\beta^\alpha}{\Gamma(\alpha)} x^{\alpha-1} e^{-\beta x}, \;\; x > 0 & & 
\frac{\alpha}{\beta} & \frac{\alpha}{\beta^2} \\ \hline

\text{Beta}(\alpha, \beta) & 
\begin{array}{l} \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)} x^{\alpha-1} (1-x)^{\beta-1} \\ 0 < x < 1 \end{array} & & 
\frac{\alpha}{\alpha+\beta} & \frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)} \\ \hline
\end{array}

$$