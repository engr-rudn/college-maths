---
title: Sentential Logic
questions:
- "What basic?"
- "How can ?"
- "How do ?"
- "Can I ?"
objectives:
- "???"
- "???"
---
# How to prove it - Ch 1: Sentential Logic

Built: 2018.03.02
Updated: 2018.03.02

1.1 Deductive Reasoning and Logical Connectives
1.2 Truth Tables
1.3 Variables and Sets
1.4 Operations on Sets
1.5 The Conditional and Biconditional Connectives

## 1.1 Deductive Reasoning and Logical Connectives

Proofs are central to mathematics. Deductive reasoning is foundation on how proofs are created.

**Definitions**
- **premise**: a statement that we assume as true 
- **conclusion**: the result we arrive at based on premises
- **valid**: an argument is **valid** if all **premises** cannot be true without **conclusion** being true as well

The form below allows us to focus on the logic of the argument/proof, as opposed to the content and definitions of the argument/proof.

$$
\begin{aligned}
P &\text{ or } Q \\\
  &\text{not } Q \\\
  &\text{therefore } P \\\
\end{aligned}
$$
Key words in arguments/proofs
$$
\begin{array}{c|c}
\text{symbol} & \text{word}\\\
\hline
\wedge & \text{and} \\\
\vee & \text{or} \\\
\neg & \text{not}
\end{array}
$$
- **disjunction**: $$P \vee Q$$ is the disjunction of $$P \text{ and } Q$$
- **conjunction**: $$P \wedge Q$$ is the conjunction of $$P \text{ and } Q$$
- **formula**: a grammatical expression using symbols

The logical "words" are not always restricted to "and", "or" and "not" - there can be other words that join statements together.

Logical "words" can exist in mathematical statements as well - $$3 <= \pi$$, "3 is either less than or equal to pi"


## 1.2 Truth Tables

#### Truth Tables
- **truth value** value we assign to a statement, i.e. *true* or *false*
- **truth tables** a tabular form to evaluate the **truth value** of a **formula**

Example
$$
\begin{array}{c|c|c}
P & Q & P \vee Q\\\
\hline
\mathrm{T} & \mathrm{T} & \mathrm{T} \\\
\mathrm{T} & \mathrm{F} & \mathrm{T} \\\
\mathrm{F} & \mathrm{T} & \mathrm{T} \\\
\mathrm{F} & \mathrm{F} & \mathrm{F} \\\
\end{array}
$$
- **inclusive**: includes possibility of both statements being true
- **exclusive**: excludes the possibility of both statements being true

Mathematics, "or" is **inclusive**

- **main connective**: the symbol which ultimately determines **truth value** for a **formula** when evaluating with a **truth table**


#### Valid argument
A **valid argument** is one in which where all premises are true, the conclusion is also true.
$$
\begin{aligned}
P & \vee Q \\\
& \neg Q \\\
\hline
& \therefore P
\end{aligned}
$$

$$
\begin{array}{c|c|c|c|c}
P & Q & P \vee Q & \neg Q & P\\\
\hline
\mathrm{T} & \mathrm{T} & \mathrm{T} & \mathrm{F} & \mathrm{T}\\\
\mathbf{T} & \mathbf{F} & \mathbf{T} & \mathbf{T} & \mathbf{T}\\\
\mathrm{F} & \mathrm{T} & \mathrm{T} & \mathrm{F} & \mathrm{F}\\\
\mathrm{F} & \mathrm{F} & \mathrm{F} & \mathrm{T} & \mathrm{F}\\\
\end{array}
$$
This is a **valid argument** because where all premises are true (second row in bold) the conclusion is true

#### Equivalent Formulas
**formulas** are **equivalent** when the **truth values** are the same for the same values of the statements. $$L \vee S \text{ and } (\neg S \wedge L) \vee S$$ are equivalent

Need to know equivalences that come up often

**DeMorgan's laws**
$$
\begin{aligned}
\neg(P \wedge Q) &\text{ is equivalent to } \neg P \vee \neg Q \\\
\neg(P \vee Q) &\text{ is equivalent to } \neg P \wedge \neg Q \\\
\end{aligned}

**Commutative laws**
\begin{aligned}
P \wedge Q &\text{ is equivalent to } Q \wedge P \\\
P \vee Q &\text{ is equivalent to } Q \vee P \\\
\end{aligned}
$$

**Associative laws**
$$
\begin{aligned}
P \wedge (Q \wedge R) &\text{ is equivalent to } (P \wedge Q) \wedge R \\\
P \vee (Q \vee R) &\text{ is equivalent to } (P \vee Q) \vee R \\\
\end{aligned}
$$

**Idempotent laws**
$$
\begin{aligned}
P \wedge P &\text{ is equivalent to } P \\\
P \vee P &\text{ is equivalent to } P  \\\
\end{aligned}
$$

**Distributive laws**
$$
\begin{aligned}
P \wedge (Q \vee R) &\text{ is equivalent to } (P \wedge Q) \vee (P \wedge R) \\\
P \vee (Q \wedge R) &\text{ is equivalent to } (P \vee Q) \wedge (P \vee R) \\\
\end{aligned}
$$

**Absoprtion laws**
$$
\begin{aligned}
P \vee (P \wedge Q) &\text{ is equivalent to } P \\\
P \wedge (P \vee Q) &\text{ is equivalent to } P\\\
\end{aligned}
$$

**Double Negation law**
$$
\begin{aligned}
\neg \neg P &\text{ is equivalent to } P \\\
\end{aligned}
$$

#### Tautalogies and Contradictions
- **tautalogy** a formula that is always true - $$\top$$
- **contradiction** a formula that is always false - $$\perp$$

These can help simplify more complex formulas

**Tautology laws**
$$
\begin{aligned}
P \wedge \top &\text{ is equivalent to } P \\\
P \vee \top &\text{ is a } \top \\\
\neg \top &\text{ is a } \perp \\\
\end{aligned}
$$

**Contradiction laws**
$$
\begin{aligned}
P \wedge \perp &\text{ is a } \perp \\\
P \vee \perp &\text{ is equivalent to } P \\\
\neg \perp &\text{ is a } \top \\\
\end{aligned}
$$

## 1.3 Variables and Sets
## 1.4 Operations on Sets
## 1.5 The Conditional and Biconditional Connectives