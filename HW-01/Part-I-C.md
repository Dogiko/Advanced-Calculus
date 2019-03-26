## Use mathematical induction to prove the following statements.

### (a) Let $0<a_1<\dots<a_n$, $n$ is a positive integer, and let $e_i = \pm 1$ for $i=1,2,\dots,n$.

### Prove that $\sum_{i=1}^n e_ia_n$ assumes at least $\frac{n(n+1)}{2}$ distinct value as the $e_i$ range over $2^n$ possible combination of signs.

### (b) Prove that $2!4!\dots (2n)! \geq ((n+1)!)^n$

### (c) Prove that for each integer $n$ there exists a positive integer $k$ so that $(\sqrt{2}-1)^n = \sqrt{k}-\sqrt{k-1}$

### (d) Let $a_i \geq 1$ for $i=1,\dots ,n$. Prove that

### $$2^{n-1}(a_1 a_2 \dots a_n + 1) \geq (1+a_1) \dots (1+a_n)$$



---

### (a) Let $0<a_1<\dots<a_n$, $n$ is a positive integer, and let $e_i = \pm 1$ for $i=1,2,\dots,n$.

### Prove that $\sum_{i=1}^n e_i a_i$ assumes at least $\frac{n(n+1)}{2}$ distinct value as the $e_i$ range over $2^n$ possible combination of signs.



---

For $n=1$, $|\{\pm a_1\}| = 2 \geq \frac{1(1+1)}{2}$ be true

Suppose $n=k$ be true, $|\sum_{i=1}^{k} e_i a_i| \geq \frac{k(k+1)}{2}$

When $n=k+1 $, $\{\sum_{i=1}^{k+1} e_i a_i\} \supseteq A \cup \{y_j\}_{j=1}^k$, where

$$\begin{array}\\
A    & = & \{(\sum_{i=1}^{k} e_i a_i) - a_{k+1}\}\\
y_j  & = & (\underset{1\leq i \leq k+1, i\neq j}{\sum{}}a_i) - a_j
\end{array}
$$

we have $|A| = |\sum_{i=1}^{k} e_i a_i| \geq \frac{k(k+1)}{2}$

$\{y_j\}$ strictly decreasing since $\{a_i\}$ strictly increasing, hance $|\{y_j\}|=k$

$\{y_j\}$ and $A$ are disjoint since
$$\begin{array}\\
y_k & = & (\underset{1 \leq i \leq k-1}{\sum{}}a_i)+(a_{k+1}-a_k)\\
    & > & (\underset{1 \leq i \leq k-1}{\sum{}}a_i)+(a_k - a_{k+1})\\
    & = & \max{(A)}
\end{array}
$$

That is, we have $|\sum_{i=1}^{k+1} e_i a_i | \geq |A| + |\{y_j\}| \geq \frac{k(k+1)}{2} + k = \frac{(k+2)(k+1)}{2}$



---

### (b) Prove that $2!4!\dots (2n)! \geq ((n+1)!)^n$

---

For $n=1$, $2!= ((1+1)!)^2$ be true

Suppose $n=k$ be true, $\underset{1\leq i \leq k}\Pi{2i} \geq ((k+1)!)^k$

When $n=k+1 $, to prove this inequality, we argue $\frac{\text{LHS}}{\text{RHS}} \geq 1$

$$\begin{array}\\
\frac{\underset{1\leq i \leq k+1}\Pi{2i}}{((k+2)!)^{(k+1)} } & \geq & \frac{((2k+2)!)((k+1)!)^k}{((k+2)!)^{(k+1)} } \\
                                                             &  =   & \frac{((2k+2)!)((k+1)!)^k}{((k+1)!)^{k} (k+2)^k
                                                                                                 ((k+2)!)} \\
                                                             &  =   & \frac{((2k+2)!)}{ (k+2)^k ((k+2)!)} \\
                                                             &  =   & \frac{(k+2+1)(k+2+2)\dots (k+2+k)}{(k+2)^k}\\
                                                             &  >   & 1\\
\end{array}
$$



---

### (c) Prove that for each integer $n$ there exists a positive integer $k$ so that $(\sqrt{2}-1)^n = \sqrt{k}-\sqrt{k-1}$

---

#### Claim $(\sqrt{2}-1)^n = (-1)^{n}\alpha_n\sqrt{2} + (-1)^{n-1}\beta_n some $ for $\alpha_n, \beta_n$ be integers

When $n=1, \alpha=\beta=1$ be true

Suppose that $n=l$ be true. That is, $(\sqrt{2}-1)^l = (-1)^{l}\alpha_l\sqrt{2} + (-1)^{l-1}\beta_l$

When $n=l+1$,
$$\begin{array}\\
(\sqrt{2}-1)^{l+1} & = & ((-1)^{l}\alpha_l\sqrt{2} + (-1)^{l-1}\beta_l)*(\sqrt{2}-1)\\
                   & = & ((-1)^{l+1}(\alpha_l+\beta_l)\sqrt{2} + (-1)^{l-1}(2\alpha_l+\beta_l))\\
\alpha_{l+1}       & = & \alpha_l + \beta_l \\
\beta_{l+1}        & = & 2\alpha_l + \beta_l \\
\end{array}
$$

#### Main statement

When $n=1, k_1=2$ be true.

Suppose that $n=l$ be true. That is, $(\sqrt{2}-1)^l = \sqrt{k_l}-\sqrt{k_l - 1}$

By the claim above
$$
k_l = 
\begin{cases}
2\alpha_l^2\text{, for $l$ even}\\
\beta_l^2\text{, for $l$ odd}\\
\end{cases}
$$

$$
2\alpha_l^2 - \beta_l^2 = (-1)^l
$$


When $n=l+1$,

$$\begin{array}\\
2\alpha_{l+1}^2 - \beta_{l+1}^2 & = & (2\alpha_l^2 + 4\alpha_l\beta_l + 2\beta_l^2)
                                        - (4\alpha_l^2 + 4\alpha_l\beta_l + \beta_l^2)\\
                                & = & -(2\alpha_l^2 - \beta_l^2)\\
                                & = & (-1)^{l+1}
\end{array}
$$

and then set

$$
k_{l+1} = 
\begin{cases}
2\alpha_{l+1}^2\text{, for $l+1$ even}\\
\beta_{l+1}^2\text{, for $l+1$ odd}\\
\end{cases}
$$

we got $(\sqrt{2}-1)^{l+1} = \sqrt{k_{l+1}}-\sqrt{k_{l+1} - 1}$



---
### (d) Let $a_i \geq 1$ for $i=1,\dots ,n$. Prove that

### $$2^{n-1}(a_1 a_2  \dots a_n + 1) \geq (1+a_1) \dots (1+a_n)$$
---

For $n=1$, $(1+a_1) = (1+a_1)$ be true

Suppose $n=k$ be true, $2^{k-1}(a_1 a_2 \dots a_k + 1) \geq (1+a_1) \dots (1+a_k)$

set
$$\begin{array}\\
b_i & = & a_1 a_2 \dots a_i\\
c_i & = & (1+a_1) \dots (1+a_i)
\end{array}
$$

get

$$ 2^{k-1}(b_{k} + 1) \geq c_{k} $$


When $n=k+1$,

$$\begin{array}\\
\text{LHS} - \text{RHS} &  =  & 2^{k}(b_{k+1} + 1) - c_{k+1}\\
                        &  =  & 2^{k}(b_{k}a_{k+1} + 1) - c_{k}(1+a_{k+1})\\
                        & \geq& 2^{k}(b_{k}a_{k+1} + 1) - 2^{k-1}(b_{k} + 1)(a_{k+1} + 1)
                                 &\text{,  by the truth when $n=k$ , note minus symbol}\\
                        & \geq& p\Big((2b_{k}a_{k+1} + 2) - (b_{k}a_{k+1} + b_k + a_{k+1} + 1) \Big)
                                 &\text{, set } p =  2^{k-1}\\
                        &  =  & p(b_{k}a_{k+1} - b_k - a_{k+1} + 1)\\
                        &  =  & p(b_{k} - 1)(a_{k+1} - 1)\\
                        & \geq& 0
\end{array}
$$


