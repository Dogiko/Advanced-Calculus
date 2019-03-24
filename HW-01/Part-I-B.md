## The following are a set of problems related to sets and functions.

### (a) Let $\Omega$ be a nonempty set. For $A, B \subset \Omega$, define there "symmetric difference" as $A \circ B =(A-B)\cup(B-A)$. Prove that for subset $A,B,C \subset \Omega,$

### $$\text{(1) } A \circ (B \circ C) = (A \circ B) \circ C$$

### $$\text{(2) } A \cap (B \circ C) = (A \cap B) \circ (A \cap C)$$

### Also, (3) prove that $A = \emptyset \iff B = B \circ A \text{ for all } B \subset \Omega$.

### Finally, (4) can the equality $A \cup (B \circ C) = (A \cup B) \circ (A \cup C)$ be ture?

---

### (b) Let $f : A \rightarrow B$ be a function. $\{ C_\alpha \}_{\alpha \in I}$ is a familly of subsets of $B$ indexed by the set $I$. Prove that

### $$\text{(1) } f^{-1}(\cup_{\alpha \in I}C_\alpha) = \cup_{\alpha \in I} f^{-1}(C_\alpha)$$

### $$\text{(2) } f^{-1}(\cap_{\alpha \in I}C_\alpha) = \cap_{\alpha \in I} f^{-1}(C_\alpha)$$

### Moreover, prove that (3) $f^{-1}(B-C) = A - f^{-1}(C) \text{ for any subset } B \subset C$.

---

### (c) Same $f$ as in (b), but now $\{ C_\alpha \}$ is a family of subsets of $A$. Prove that

### $$\text{(1) } f(\cup_{\alpha}C_\alpha) = \cup_{\alpha \in I} f(C_\alpha)$$

### $$\text{(2) } f(\cap_{\alpha}C_\alpha) \subset \cap_{\alpha \in I} f(C_\alpha)$$

### Show by an example that the above subset relation for intersection is in general not equal.

### However, prove that if $f$ is one-to-one, it become equality.

---


### (d) Let $f: A \rightarrow B$ be a function. Prove that $f$ is one-to-one iff one of the following statements is true:

### (1)  $f^{-1}(f(C))=C$, for all $C \subset A$

### (2)  $f(C\cap D)=f(C)\cap f(D)$, for all $C, D \subset A$

### (3)  For all $C, D \subset A$, $f(C) \cap f(D) = \emptyset$ iff $C \cap D = \emptyset$

### (4)  $f(C - D)=f(C)-f(D)$, for all $D \subset C \subset A$

### Moreover, prove that $f$ is onto iff $f(f^{-1}(E))=E$ for all $E \subset B$





---


### (a) Let $\Omega$ be a nonempty set. For $A, B \subset \Omega$, define there "symmetric difference" as $A\circ B =(A-B)\cup(B-A)$. Prove that for subset $A,B,C \subset \Omega,$

### $$\text{(1) } A \circ (B \circ C) = (A \circ B) \circ C$$

### $$\text{(2) } A \cap (B \circ C) = (A \cap B) \circ (A \cap C)$$

### Also, (3) prove that $A = \emptyset \iff B = B \circ A \text{ for all } B\subset \Omega$.

### Finally, (4) can the equality $A \cup (B \circ C) = (A \cup B) \circ (A \cup C)$ be ture?

---

(1)

First, we have this equality, $\forall A,B,C,D \subset \Omega$

$$\begin{array}\\
(A \cup B) \cap (C \cup D) & = & ((A \cup B) \cap C) \cup ((A \cup B) \cap D) \\
& = & (A \cap C) \cup (B \cap C) \cup (A \cap D) \cup (B \cap D) & \cdots \cdots \cdots \text{(1)}
\end{array}
$$

Return to what we want,

$$\begin{array}\\
A \circ (B \circ C) & = & A \circ ((B - C) \cup (C - B))\\
                    & = & (A - ((B - C) \cup (C - B))) \cup (((B - C) \cup (C - B))-A) \\
                    & = & ((A-(B-C)) \cap (A-(C-B))) \cup (((B-C)-A) \cup ((C - B)-A))\\
                    & = & ((A \cap (B' \cup C)) \cap (A \cap (C' \cup B))) \cup (B \cap C' \cap A') \cup (C \cap B' \cap A')\\
                    \\
                    & = & (((A \cap B') \cup (A \cap C)) \cap ((A \cap C') \cup (A \cap B))) \\
                    &   & \cup (B \cap C' \cap A') \\
                    &   & \cup (C \cap B' \cap A')\\
                    \\
                    & = & \cup (A \cap B \cap C) \\
                    &   & \cup (A \cap B' \cap C') \\
                    &   & \cup (B \cap C' \cap A') \\
                    &   & \cup (C \cap A' \cap B') \text{ , apply (1)} \\
                    \\
                    & = & C \circ (A \circ B) \text{ , since this foumula is symmetric for } A,B,C \\
                    & = & (A \circ B) \circ C
\end{array}
$$

$ $

(2)

$$
\begin{array}\\
LHS & = & A \cap (B \circ C) \\
    & = & A \cap ((B \cap C') \cup (C \cap B')) \\
    & = & (A \cap B \cap C') \cup (A \cap C \cap B') \\
    \\
RHS & = & ((A \cap B) - (A \cap C)) \cup ((A \cap C) - (A \cap B)) \\
    & = & ((A \cap B \cap (A' \cup C')) \cup ((A \cap C \cap (A' \cup B')) \\
    & = & (A \cap B \cap C') \cup (A \cap C \cap B') \text{ ,since } A \cap A' = \emptyset\\
    & = & LHS
\end{array}
$$

$ $

(3)

If $A = \emptyset$

$$
B \circ A = (B - \emptyset) \cup (\emptyset - B) = B \cup \emptyset = B
$$

$ $

Otherwise, for $A \neq \emptyset$, pick $x \in A$,

if $x \in B$ we have $x \notin B - A \text{ and } x \notin A-B$,

that is $x \notin A \circ B$

$\implies B \neq A \circ B$

if $x \notin B$, we have $x \in (A-B) \subset A \circ B$ 

$\implies B \neq A \circ B$

$ $

(4)

This equlity is false, for $A \neq \emptyset$, pick $x \in A$ 

$x \in A \subset \text{LHS}$

but, $x \notin $RHS because that

$$
\begin{array}\\
         & x \in A \cup B & \text{ and } & x \in A \cup C \\
\implies & x \notin ((A \cup B) - (A \cup C)) & \text{ and } & x \notin ((A \cup C) - (A \cup B))\\
\implies & x \notin \text{RHS}
\end{array}
$$



---

### (b) Let $f : A \rightarrow B$ be a function. $\{ C_\alpha \}_{\alpha \in I}$ is a familly of subsets of $B$ indexed by the set $I$. Prove that

### $$\text{(1) } f^{-1}(\cup_{\alpha \in I}C_\alpha) = \cup_{\alpha \in I} f^{-1}(C_\alpha)$$

### $$\text{(2) } f^{-1}(\cap_{\alpha \in I}C_\alpha) = \cap_{\alpha \in I} f^{-1}(C_\alpha)$$

### Moreover, prove that (3) $f^{-1}(B-C) = A - f^{-1}(C) \text{ for any subset } B \subset C$.

---

(1)

" $\subseteq$ "

given $x \in $LHS, there exists $y \in \cup_{\alpha \in I}C_\alpha$ such that $f(x) = y$

$\implies y \in C_\alpha \text{ for some } \alpha \in I$

$\implies x \in f^{-1}(C_\alpha) \text{ for some } \alpha \in I$

$\implies x \in $RHS

$ $

" $\supseteq$ "

given $x \in $RHS, there exists $y \in C_\alpha \text{ for some } \alpha \in I$ such that $f(x) = y$

$\implies y \in \cup_{\alpha \in I}C_\alpha$

$\implies x \in$LHS

$ $

(2)

" $\subseteq$ "

Given $x \in $LHS, there exists $y \in \cap_{\alpha \in I}C_\alpha$ such that $f(x) = y$

$\implies y \in C_\alpha \text{ for all } \alpha \in I$

$\implies x \in f^{-1}(C_\alpha) \text{ for all } \alpha \in I$

$\implies x \in $RHS

$ $

" $\supseteq$ "

Given $x \in $RHS, there exists $y \in C_\alpha \text{ for all } \alpha \in I$ such that $f(x) = y$

$\implies y \in \cap_{\alpha \in I}C_\alpha$

$\implies x \in$LHS

$ $

(3)

" $\supseteq$ "

For all $x \in $RHS, $ f(x) = y \in B$,

but $y \notin C$ since $x \notin f^{-1}(C)$

$\implies y \in B - C$

$\implies x \in $LHS

$ $

" $\subseteq$ "

Suppose not,

there exists $x \in A, x \in $LHS but $x \notin$RHS

$x \notin$RHS $\implies x \in f^{-1}(C), \text{ that is } f(x) \in C$

$x \in $LHS $\implies f(x) \in B-C $

so, we have $f(x) \in (B-C) \cap C = \emptyset$, contradiction



---

### (c) Same $f$ as in (b), but now $\{ C_\alpha \}$ is a family of subsets of $A$. Prove that

### $$\text{(1) } f(\cup_{\alpha}C_\alpha) = \cup_{\alpha \in I} f(C_\alpha)$$

### $$\text{(2) } f(\cap_{\alpha}C_\alpha) \subset \cap_{\alpha \in I} f(C_\alpha)$$

### Show by an example that the above subset relation for intersection is in general not equal.

### However, prove that if $f$ is one-to-one, it become equality.

---

(1)

" $\subseteq$ "

Given $y \in$ LHS, there exists $x \in \cup_{\alpha}C_{\alpha}$ such that f(x) = y

$x \in C_{\alpha}$ for some $\alpha \in I$

that is $y \in$ RHS

" $\supseteq$ "

Given $y \in$ LHS, i.e. $y \in f(C_{\alpha})$ for some $\alpha \in I$

there exists $x \in C_{\alpha}$, such that f(x) = y

$x \in \cup_{\alpha}C_{\alpha}$

that is $y \in$ RHS

(2)

Given $y \in$ LHS, there exists $x \in \cap_{\alpha}C_{\alpha}$ such that f(x) = y

$x \in C_{\alpha}$ for all $\alpha$

so $y \in f(C_{\alpha})$ for all $\alpha$

that is, $y \in \cap_{\alpha} f(C_{\alpha}) = $RHS

"equality is general false"

Define $f:\mathbb{R} \rightarrow \mathbb{R}$ as $f(x) = x^2$

$f([-2,-1] \cap [1,2]) = f(\emptyset) = \emptyset \neq [1,4]\cap [1,4] = f([-2,-1]) \cap f([1,2])$

when $f$ is one-to-one

Given $y \in$ RHS,  for each $\alpha$, there exists $x_\alpha \in C_{\alpha}$ such that $f(x_\alpha)=y$

all $x_\alpha = f^{-1}(y)$ since $f$ is one-to-one

$f^{-1}(y) \in \cap_{\alpha} C_{\alpha}$

so $y \in$RHS



---

### (d) Let $f: A \rightarrow B$ be a function. Prove that $f$ is one-to-one iff one of the following statements is true:

### (1)  $f^{-1}(f(C))=C$, for all $C \subset A$

### (2)  $f(C\cap D)=f(C)\cap f(D)$, for all $C, D \subset A$

### (3)  For all $C, D \subset A$, $f(C) \cap f(D) = \emptyset$ iff $C \cap D = \emptyset$

### (4)  $f(C - D)=f(C)-f(D)$, for all $D \subset C \subset A$

### Moreover, prove that $f$ is onto iff $f(f^{-1}(E))=E$ for all $E \subset B$


---

" one-to-one $\implies$ (1) "

Given $x \in $ RHS, $y:=f(x) \in f(C)$

$\implies x \in f^{-1}(f(C))$

Given $x \in $ LHS, there exists $y \in f(C)$ such that $y = f(x)$

$y \in f(C) \implies $ there exists $x' \in C$, $f(x')=y$

since $f$ is one-to-one, $x=x'\in C$

" (1) $\implies$ one-to-one "

Given $x \in A$, suppose that $x' \in A$, such that $f(x)=f(x')=y$

$\{x\} = f^{-1}(f(\{x\})) = f^{-1}(\{y\}) = \{x, x'\}$

$\implies x = x'$

" one-to-one $\implies$ (2) "

Given $y \in $LHS, there exists $x \in C \cap D$, such that $y=f(x)$

$\implies y \in f(C)$ and $y \in f(D)$, that is, $y \in $ RHS

Given $y \in $ RHS, there exists $x \in C$, $x' \in D$, $f(x)=f(x')=y$

Since $f$ is one-to-one, $x=x' \in C\cap D \implies y=f(x) \in $LHS

" (2)$\implies$ (3) "

$C \cap D = \emptyset \iff f(C\cap D) = \emptyset$

and we have $f(C\cap D)=f(C)\cap f(D)$

" (3)$\implies$ one-to-one "

Suppose not, there exists $x, x' \in A$, $x \neq x'$ such that $f(x)=f(x')=y$

Set $C=\{x\}$, $D=\{x'\}$, $C \cap D = \emptyset$ but $f(C)\cap f(D) = \{y\} \neq \emptyset$, contradiction

" (3) $\implies$ (4)"

$(C-D)\cap D = \emptyset$, so $f(C-D)\cap f(D) = \emptyset$

and we have $f(C) = f((C-D)\cup D)= f(C-D) \cup f(D)$

$\implies f(C)-f(D)=f(C-D)$

" (4)$\implies$ one-to-one "

Suppose not, there exists $x, x' \in A$, $x \neq x'$ such that $f(x)=f(x')=y$

Set $C = \{x, x'\}$, $D=\{x'\}$, than $f(C-D)=\{y\} \neq \emptyset$

but $f(C)-f(D) = \{y\} - \{y\}=\emptyset$, contradiction

"onto iff $f(f^{-1}(E))=E$"

Suppose $f$ is onto, for all $y \in E$, there exists $x \in A$ such that $f(x)=y \in E$

that is $x \in f^{-1}(E)$

$\implies y \in f(f^{-1}(E))$

conversely, for all $y \in E$

$f(f^{-1}(\{y\}))=\{y\}$

$\implies f^{-1}(\{y\}) \neq \emptyset$

$\implies$ there exists $x \in A$ such that $f(x)=y$