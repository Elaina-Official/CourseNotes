# Discrete Mathematics

## Logic and Proof

### Propositions Logic

#### Negation Operator (Not)

- Let $p$ be a proposition
-  Negation of $p$ is the statement  “It is not the case that $p$”
- Notation: $\lnot p,\sim p, \overline{p}$

####  Conjunction Operator (AND)

- Let $p$ and $q$ be propositions
- Conjunction of $p$ and $q$ is “$p$ and $q$” 
- Notation: $p\land q$

#### Disjunction Operator (OR)

- Let $p$ and $q$ be propositions
- Disjunction of $p$ and $q$ is “$p$ or $q$”
- Notation: $p\lor q$

####  Exclusive OR Operator (XOR)

- Let $p$ and $q$ be propositions
- Notation: $p\oplus q,p\neq q, p+q$

#### Conditional Statement (Imply)

- Let $p$ and $q$ be propositions
- Conditional statement is “if $p$, then $q$”
- Notation: $p\rightarrow q$
- $p$ is called the hypothesis (or antecedent or premise)
- $q$ is called the conclusion (or consequence)

####  Biconditional Statement (Equivalent)

- Let $p$ and $q$ be propositions
- Biconditional statement is “$p$ if and only if $q$” (iff)
- Notation: $p\leftrightarrow q, p=q, p\equiv q$
- Also called bi-implications, equivalence
- Equivalent to $(p\rightarrow q)\land(q\rightarrow p)$

####  Proposition Logic Table

| Formal Name             | Nickname   | Symbol            |
| ----------------------- | ---------- | ----------------- |
| Negation Operator       | NOT        | $\lnot$           |
| Conjunction Operator    | AND        | $\land$           |
| Disjunction Operator    | OR         | $\lor$            |
| Exclusive-OR Operator   | XOR        | $\oplus$          |
| Conditional Statement   | Imply      | $\rightarrow$     |
| Biconditional Statement | Equivalent | $\leftrightarrow$ |

#### Truth Table 

| $p$  | $q$  | $\lnot p$ | $p\land q$ | $p\lor q$ | $p\oplus q$ | $p\rightarrow q$ | $p\leftrightarrow q$ |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| T    | T    | F         | T          | T         | F           | T                | T                    |
| T    | F    | F         | F          | T         | T           | F                | F                    |
| F    | T    | T         | F          | T         | T           | T                | F                    |
| F    | F    | T         | F          | F         | F           | T                | T                   |

#### Precedence of Logical Operator

| Precedence | Symbol             | Nickname   |
| :---: | :---: | :---: |
| 1          | $\lnot$            | NOT        |
| 2          | $\land$            | AND        |
| 3          | $\lor\quad \oplus$ | OR    XOR  |
| 4          | $\rightarrow$      | Imply      |
| 5          | $\leftrightarrow$  | Equivalent |

Types of Proposition

- Tautology: A compound proposition which is always true
- Contradiction: A compound proposition which is always false
- Contingency: A compound proposition which is neither a tautology nor  a contradiction

### Propositional  Equivalences

Definition: Two propositions $P$ and $Q$ are logically  equivalent if $P\leftrightarrow Q$ is a tautology. 

Notation: $P\Leftrightarrow Q\text{ or }P\equiv Q$

#### Important Equivalences 1

- Identify Laws

  $p\land T\equiv p$

  $p\lor F\equiv p$

- Domination Laws

  $p\lor T\equiv T$

  $p\land F\equiv F$

- Idempotent Laws

  $p\lor p\equiv p$

  $p\land p\equiv p$

- Double Negation Law

  $\lnot(\lnot p)\equiv p$

- Negation Laws

  $p\lor \lnot p\equiv T$

  $p\land \lnot p\equiv F$

- Commutative Laws

  $p\lor q\equiv q\lor p$

  $p\land q\equiv q\land p$

- Associative Laws

  $p\land(q\land r) \equiv (p\land q)\land r$

  $p\lor(q\lor r) \equiv (p\lor q)\lor r$

- Distributive Laws

  $p\lor(q\land r) \equiv (p\lor q)\land(p\or r)$

  $p\land(q\lor r) \equiv (p\land q)\lor(p\land r)$

- Absorption Laws

  $p\lor(p\land q)\equiv p$

  $p\land(p\lor q)\equiv p$

- De Morgan's Laws

  $\lnot(p\lor q)\equiv \lnot p\land \lnot q$

  $\lnot(p\land q)\equiv \lnot p\lor \lnot q$

#### Important Equivalences 2

- $P \rightarrow Q \equiv \lnot P \lor Q$
- $P \rightarrow Q \equiv \lnot Q \rightarrow \lnot P$
- $P \lor Q \equiv \lnot P \rightarrow Q$
- $P \land Q \equiv \lnot (P \rightarrow \lnot Q)$
- $\lnot (P \rightarrow Q) \equiv P \land \lnot Q$
- $(P \rightarrow Q) \land (P \rightarrow R) \equiv P \rightarrow (Q \land R)$
- $(P \rightarrow R) \land (Q \rightarrow R) \equiv (P \lor Q) \rightarrow R$
- $(P \rightarrow Q) \lor (P \rightarrow R) \equiv P \rightarrow (Q \lor R)$
- $(P \rightarrow R) \lor (Q \rightarrow R) \equiv (P \land Q) \rightarrow R$

### Predicates and Quantifiers

#### Predicates

Predicate logic is an extension of propositional logic that permits concisely reasoning about whole classes of entities.  Predicate(proposition function) is a function of proposition, and the truth value of proposition function can only be determined when the values of variables are known. 

#### Quantifiers

Quantification expresses the extent to which a predicate is true over a range of elements. The area of logic that deals with predicates and quantifiers is called the Predicate Calculus. 

Three types of quantification will be focused:

- Universal Quantification: all, none, etc.

  - Definition: Universal quantification of $P(x)$ is the statement “$P(x)$ is true for all values of $x$ in the domain”. 
  - Notation: $\forall xP(x)$
  - Truth value
    - True when $P(x)$ is true for all $x$
    - False otherwise

- Existential Quantification: some few, many, etc.

  - Definition: Existential quantification of $P(x)$ is the proposition “There exists an element $x$ in the domain such that $P(x)$ is true”. 
  - Notation: $\exist xP(x)$
  - Truth value
    - False when $P(x)$ is false for all x
    - True otherwise

- Unique Quantification: exactly one, etc. 

  Unique Quantification can be expressed by using Universal Quantification and Existential Quantification. 

#### Precedence and Scope of Quantifiers

$\forall$ and $\exist$ have higher precedence than all logical operators from proposition calculus. 

The part of a logical expression to which a quantifier is applied is called the scope of this quantifier. 

#### Logical Equivalences Involving Quantifiers

For Universal Quantifiers, 

$\forall x \ (P(x) \land Q(x)) \equiv \forall x \ P(x) \land \forall x \ Q(x)$

$\forall x \ P(x) \lor \forall x \ Q(x) \rightarrow \forall x \ (P(x) \lor Q(x))$

For Existential Quantifiers, 

$\exists x \ (P(x) \land Q(x)) \rightarrow \exists x \ P(x) \land \exists x \ Q(x)$ 

$\exists x \ (P(x) \lor Q(x)) \equiv \exists x \ P(x) \lor \exists x \ Q(x)$

For any $A$($A$ does not consist  of free variable $x$), we have 

$\forall x \ (A \land P(x)) \equiv A \land \forall x \ P(x)$

$\forall x \ (A \lor P(x)) \equiv A \lor \forall x \ P(x)$

$\exists x \ (A \land P(x)) \equiv A \land \exists x \ P(x)$

$\exists x \ (A \lor P(x)) \equiv A \lor \exists x \ P(x)$

$\forall x \ P(x) \rightarrow A \equiv \exists x \ (P(x) \rightarrow A)$

$A \rightarrow \forall x \ P(x) \equiv \forall x \ (A \rightarrow P(x))$

$\exists x \ P(x) \rightarrow A \equiv \forall x \ (P(x) \rightarrow A)$

$A \rightarrow \exists x \ P(x) \equiv \exists x \ (A \rightarrow P(x))$

The De Morgan's Law for Quantifiers is

$\lnot \exist xP(x)\equiv \forall x\lnot P(x)$

#### Translation

### Nested Quantifiers

Two quantifiers are nested if one is within the scope of the other. 

If quantifiers are same type, the order is not a matter. If quantifiers are different types, read from left to right. 

### Rules of Inference

#### Rules of Inference

Argument in propositional logic is a sequence of propositions. A argument form is like this:
$$
\begin{array}{r}
p \\
p\rightarrow q \\
\hline
\therefore q
\end{array}
$$
The upper is called Premise/Hypothesis, and the lower is called Conclusion. 

- Premises / Hypothesis: All except the final proposition
- Conclusion: The final proposition

**Rules of Inference ($\rightarrow $)**

| Formal Name | Symbol |
| ---- | ---- |
|   Modus Ponens   | $((p \rightarrow q) \land p) \rightarrow q$ |
| Modus Tollens | $((\neg q) \land (p \rightarrow q)) \rightarrow \neg p$ |
| Hypothetical Syllogism | $((p \rightarrow q) \land (q \rightarrow r)) \rightarrow (p \rightarrow r)$ |
| Disjunctive Syllogism | $((p \lor q) \land \neg p) \rightarrow q$ |
| Addition | $p \rightarrow (p \lor q)$ |
| Simplification | $(p \land q) \rightarrow p$ |
| Conjunction | $(p \land q) \rightarrow (p \land q)$ |
| Resolution | $((p \lor q) \land (\neg p \lor r)) \rightarrow (q \lor r)$ |

**Proof of Theorems: Equivalence**

Since we know that $p\leftrightarrow q\equiv(p\rightarrow q)\land(q\rightarrow p)$.To prove equivalence, we can show $p\rightarrow q$ and $q\rightarrow p$ are both true. 

#### Rules of Inference for Quantifiers

- Universal Instantiation
  $$
  \begin{array}{r}
  \forall xP(x) \\
  \hline
  \therefore P(a)
  \end{array}
  $$

- Existential Instantiation
  $$
  \begin{array}{r}
  \exist xP(x) \\
  \hline
  \therefore P(c) \text{ for some element }c
  \end{array}
  $$

- Universal Generalization
  $$
  \begin{array}{r}
  P(b)\text{ for an arbitraty }b \\
  \hline
  \therefore \forall xP(x)
  \end{array}
  $$

- Existential Generalization
  $$
  \begin{array}{r}
  P(d)\text{ for some element }d \\
  \hline
  \therefore \exist xP(x)
  \end{array}
  $$



### Introduction to Proofs

These are formal proofs, which are very clear and precise, always extremely lone and hard to follow. 

- Proposition
- Operator
- Predicates
- Quantifier
- Truth Table
- Rules of Equivalence
- Rules of Inference

We also have some informal proofs. There will be more than one rule of inference may be used in each step, and steps may be skipped. 

- Direct Proof
- Indirect Proof
-  Proof by Contraposition
- Proof of Theorems: Equivalence
- Proof by Contradiction
- Proof by Cases
- Existence Proof
- Uniqueness Proof

## Relation

### Set and Functions

### Relations and Properties

### Equivalence and Partial Orderings



## Counting 

## Graph

g

Partition 

一个集合的分区必须满足以下条件：

1. **非空**：每个子集都不能是空集。
2. **互不相交**：任意两个子集之间没有公共元素。
3. **覆盖全集**：所有子集的并集等于原集合。

欧拉通路（回路） vs 哈密顿通路（回路）

经过所有边（的回路） vs 经过所有点（的回路）

### 图论中符号 $C_n$、$W_n$、$K_n$ 的含义

---

#### 1. $C_n$：n-阶循环图（Cycle Graph）
- **定义**：$C_n$ 表示具有 $n$ 个顶点的**循环图**，顶点按顺序连接形成一个闭合的环，每个顶点与前后两个顶点相连。
- **顶点数**：$n$
- **边数**：$n$
- **条件**：$n \geq 3$（至少 3 个顶点才能形成一个环）
- **示例**：  
   - $C_3$：三角形  
   - $C_4$：正方形  
   - $C_5$：五边形  

---

#### 2. $W_n$：n-阶车轮图（Wheel Graph）
- **定义**：$W_n$ 表示具有 $n$ 个顶点的**车轮图**，它由一个中心顶点和 $C_{n-1}$ 的循环图组成。
- **结构**：
   - $C_{n-1}$：包含 $n-1$ 个顶点的循环图。  
   - **中心顶点**：与 $C_{n-1}$ 上所有顶点相连。
- **顶点数**：$n$
- **边数**：
$$ 2(n-1) $$
- **条件**：$n \geq 4$（至少 4 个顶点才能形成车轮图）
- **示例**：  
   - $W_4$：三角形加中心顶点  
   - $W_5$：正方形加中心顶点  

---

#### 3. $K_n$：n-阶完全图（Complete Graph）
- **定义**：$K_n$ 表示具有 $n$ 个顶点的**完全图**，在该图中，每一对不同的顶点之间都存在一条边。
- **特点**：所有顶点两两相连。
- **顶点数**：$n$
- **边数**：
$$ \frac{n(n-1)}{2} $$
- **示例**：  
   - $K_1$：只有 1 个顶点，没有边  
   - $K_2$：两个顶点之间有一条边  
   - $K_3$：三角形，每个顶点都相连  
   - $K_4$：四个顶点，两两相连，形成完全连接结构  

---

### 总结表格

| 符号  | 名称               | 顶点数 | 边数               | 结构描述                 |
| ----- | ------------------ | ------ | ------------------ | ------------------------ |
| $C_n$ | 循环图（Cycle）    | $n$    | $n$                | 顶点按顺序闭合形成一个环 |
| $W_n$ | 车轮图（Wheel）    | $n$    | $2(n-1)$           | $C_{n-1}$ 加中心顶点     |
| $K_n$ | 完全图（Complete） | $n$    | $\frac{n(n-1)}{2}$ | 所有顶点两两相连         |
