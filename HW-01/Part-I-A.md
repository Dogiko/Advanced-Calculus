## The following are some problems relating to simple logical deduction.

### (a) If $A$ is elected, then $B$ will resign. If $C$ is elected, then $B$ will not resign. However, if $A$ is elected, then $C$ will not be elected. Therefore $B$ will resign. Is the argument valid.

### (b) Let $P$, $Q$ and $R$ are three statements. What kind of the connectives should you put in the following question (?) position so that the composite statement becomes a valid conclusion?
$$((P\implies \neg Q)\wedge (R \implies Q)) \implies P?R$$

### (c) Let $f : A \implies B$ be a function. use the logical symbols (the quantifiers connectives, etc) to express that (1) $f$ is one-to-one (2) $f$ is onto, and (3) $f$ is one-to-one and onto. More over, write down their negtive statements.

---

---

### (a) If $A$ is elected, then $B$ will resign. If $C$ is elected, then $B$ will not resign. However, if $A$ is elected, then $C$ will not be elected. Therefore $B$ will resign. Is the argument valid.

---

No, this argument is not valid.

Set $P$ : $C$ is elected, $Q$ : $B$ will resign.

We have $P \implies \neg Q$, but we can't get any infomation from $\neg P$.

In this case, $B$ must resign if $A$ is elected.

---

### (b) Let $P$, $Q$ and $R$ are three statements. What kind of the connectives should you put in the following question (?) position so that the composite statement becomes a valid conclusion?
$$((P\implies \neg Q)\wedge (R \implies Q)) \implies P?R$$

---

Since $(R \implies Q) \Longleftrightarrow (\neg Q \implies \neg R)$

We can get $P\implies \neg Q \implies \neg R$,

that is $P \implies \neg R$

---

### (c) Let $f : A \rightarrow B$ be a function. use the logical symbols (the quantifiers connectives, etc) to express that (1) $f$ is one-to-one (2) $f$ is onto, and (3) $f$ is one-to-one and onto. More over, write down their negtive statements.

---

(1) 

$f \text{ is one-to-one } \iff (\forall x, y \in A,  (x\neq y \wedge f(x) \neq f(y)))$

$f \text{ is not one-to-one } \iff (\exists x, y \in A,  (x\neq y \wedge f(x) = f(y)))$

---

(2)

$f \text{ is onto } \iff (\forall u \in B, (\exists x\in A, f(x) = u))$

$f \text{ is not onto } \iff (\exists u \in B,  (\forall x\in A, f(x) \neq u))$

---

(3)

$f \text{ is one-to-one and onto } \iff (\forall x, y \in A,  (x\neq y \wedge f(x) \neq f(y))) \wedge (\forall u \in B, (\exists x\in A, f(x) = u))$

$f \text{ is not (one-to-one and onto) } \iff  (\exists x, y \in A,  (x\neq y \wedge f(x) = f(y))) \vee (\exists u \in B,  (\forall x\in A, f(x) \neq u))$