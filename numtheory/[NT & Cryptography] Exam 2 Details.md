# [NT & Cryptography] Exam 2 Details

### Lecture 6

**Theorem (Euclid):** Suppose $p$ is a prime number and $a,b \in \mathbb{N}$. If $p \mid ab$, then $p \mid a$ or $p \mid b$. 

### Lecture 7

**Fundamental Theorem of Arithmetic:** Every integer $n > 1$ can be UNIQUELY factored as the product of primes.

**Corollary:** Any positive integer $n > 1$ can be written uniquely in a canonical form:
$$
n = p_1^{k_1} p_2^{k_2} \cdots p_t^{k_t}
$$
where for all $i$:

- $p_i$ is prime
- $p_1 < p_2 < \cdots < p_t$
- $k_i$ are positive integers

**Theorem (Euclid):** There are infinitely many primes.

**Definition:** The integers $a,b$ are congruent mod $n$ if $n \mid (a-b)$. We write this $a \equiv b \text{ mod }n$.

----

### Lecture 8

**Theorem:** Let $a,b \in \mathbb{Z}$. We say that $a \equiv b \text{ mod }n \iff$ $a$ & $b$ have the same non-negative remainder when divided by $n$.

**Theorem:** If $a \equiv b \text{ mod }n$ and $b \equiv c \text{ mod }n$, then $a \equiv c \text{ mod }n$.

**Corollary:** If $a \equiv b \text{ mod }n$ and $c \equiv d \text{ mod }n$, then $a + c \equiv b + d \text{ mod }n$

**Corollary:** If $a \equiv b \text{ mod }n$ and $c \equiv d \text{ mod }n$, then $ac \equiv bd \text{ mod }n$ 

**Corollary:** If $a \equiv b \text{ mod }n$ then $a + c \equiv b + c \text{ mod }n$ and $ac \equiv bc \text{ mod }n$

**Corollary:** If $a \equiv b \text{ mod }n$, then $a^k \equiv b^k \text{ mod }n$ for any positive integer $k$. 

----

### Lecture 10

**Theorem:** If $ca \equiv cb \text{ mod }n$, then $a \equiv b \text{ mod } \left(\frac{n}{d}\right)$ where $d = \text{gcd}(c,n)$. 

**Theorem:** If $ca \equiv cb \text{ mod }n$ and $\text{gcd}(c,n) = 1$ then $a \equiv b \text{ mod }n$ 

**Definition:** A subset $R \subset \mathbb{Z}$ of size $n$ is a complete set of residues $\text{ mod }n$ if, for every $a,b \in R$, $a \not \equiv b \text{ mod }n$ . 

**Lemma:** If $R$ is a complete set of residues $\text{mod }n$ and $a \in \mathbb{Z}$ with $\text{gcd}(a,n) = 1$, then $aR = \{ar \;:\; r \in R\}$ is also a complete set of residues $\text{ mod }n$.

**Definition (Solvability):** The equation $ax \equiv b \text{ mod }n$ has a solution $\iff \text{gcd}(a,n) \mid b$. 

**Lemma:** If $\text{gcd}(a,n) = 1$, then $ax \equiv b \text{ mod }n$ has a unique solution $\text{ mod }n$. 

----

### Lecture 12

**Lemma:** When $\text{gcd}(a,n) \mid b$, the number of solutions to $ax \equiv b \text{ mod }n$ is $\text{gcd}(a,n)$.

**Chinese Remainder Theorem:** Let $n_1, n_2, \dots, n_t$ be positive integers such that $\text{gcd}(n_i, n_j) = 1$ for all $i \neq j$. Then
$$
\begin{align*}
	x &\equiv a_1 \text{ mod }n_1\\
  x &\equiv a_2 \text{ mod }n_2\\
  &\;\;\;\;\;\;\;\;\vdots\\
  x &\equiv a_t \text{ mod }n_t 
\end{align*}
$$
has a simultaneous solution which is unique $\text{mod } n_1n_2\cdots n_t$ .

---

### Lecture 13

**Theorem (Fermat):** Suppose $p$ is prime and $p \nmid a$. Then,
$$
a^{p-1} \equiv 1 \text{ mod }p
$$
**Corollary:** If $p$ is prime, then for every $a$,
$$
a^p = a \text{ mod }p
$$

---

### Lecture 14

**Theorem (Wilson):** If $p$ is prime, then $(p-1)! \equiv -1 \text{ mod }p$.

----

### Lecture 15

**Converse of Wilson's Theorem:** If $(n-1)! \equiv 1 \text{ mod }n$, then $n$ is prime.

**Theorem:** Let $p$ be an odd prime. The congruence $x^2 + 1 \equiv 0 \text{ mod }p$ has a solution if and only if $p \equiv 1 \text{ mod }4$. 

---

### Homework

**Theorem:** The congruences $x \equiv a \text{ mod }n$ and $x \equiv b \text{ mod }m$ admit a simultaneous solution if and only if $\text{gcd}(n,m) \mid (a-b)$. 

**Solving Congruence Relation Systems:** 

If you have a system like in the CRT where respective $n_i$ are comprime. Then, define some

- $N = n_1n_2\cdots n_t$ 
- $N_i = \frac{N}{n_i}$ 
- Find modular inverse $m_i$ such that $m_i \cdot N_i \equiv 1 \text{ mod }n_i$

  
$$
x = \sum_{i=0}^t a_iN_im_i \text{ mod } N
$$
**Theorem:** If you have the following system
$$
\begin{align*}
	x &\equiv a \text{ mod } n_1\\
	x &\equiv a \text{ mod } n_2\\
	&\;\;\;\;\;\;\;\;\vdots\\
	x &\equiv a \text{ mod } n_t
\end{align*}
$$
We can simplify this system into the following.
$$
x \equiv a \text{ mod } \text{lcm}(n_1, n_2, \dots, n_t)
$$