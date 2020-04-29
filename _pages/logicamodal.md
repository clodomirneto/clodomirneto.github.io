---
layout: archive
title: "Lógica Modal"
permalink: /logicamodal/
author_profile: true
---

<br />

Fix the propositional language $\mathcal{ML}$ whose primitive symbols (alphabet) are:

* the sentence letters: $\alpha, \beta, \ldots$;
* the constant symbol: $\bot$ (falsehood);
* the connectives: $\to$ (material implication), $\Box$ (necessity);
* the punctuation marks: ( and ).

The formulas of $\mathcal{ML}$ (or $\mathcal{ML}$-formulas) are defined inductively:

* a sentence letter is a modal sentence;
* $\bot$ is a modal sentence;
*  if $A$ and $B$ are modal sentences, so is $(A \to B)$;
* if $A$ is a modal sentence, so is $\Box A$.

Various other symbols are introduced by abbreviations:

| - | - | - |
| Df $\top$ | $\top = \bot \to \bot$ | $\top$ (truth-hood) |
| Df $\neg$ | $\neg A = A \to \bot$  | $\neg$ (negation) |
| Df $\vee$ | $A \vee B = \neg A \to B$ | $\vee$ (disjunction) |
| Df $\wedge$ | $A \wedge B = \neg (A \to \neg B)$ | $\wedge$ (conjunction) |
| Df $\leftrightarrow$ | $A \leftrightarrow B = (A \to B) \wedge (B \to A)$ | $\leftrightarrow$ (material bi-implication) |
| Df $\Diamond$ | $\Diamond A = \neg \Box \neg A$ | $\Diamond$ (possibility) |

If a formula $A$ is of the form ($\neg B$) or ($B \odot C$), for $\odot \in \{ \wedge, \vee, \to, \leftrightarrow \}$, then $\neg$, or respectively, $\odot$ is called the main connective of $A$. The formula $B$ is said to be the antecedent of the implication ($B \to C$) and $C$ its consequent.

We understand by a modal logic any set of formulas in the present language, containing all classical tautologies (CT) and closed under tautological consequence (TC) and Uniform Substitution (US). If $S$ is a modal logic, we will write $\vdash_{S} A$ in place of $A \in S$. 

We consider here a Hilbert-type calculus ($\mathcal{H}$) for Classical Logic. This system consists of several axioms and one rule of inference.

Axiom 1 (H1): $A \to (B \to A)$.

Axiom 2 (H2): $(A \to (B \to C)) \to ((A \to B) \to (A \to C))$.

Axiom 3 (H3): $\bot \to A$.

Axiom 4 (H4): $((A \to \bot) \to \bot) \to A$.

Inference rule (MP): If $\vdash_{S} A$ and $\vdash_{S} A \to B$, then $\vdash_{S} B$.

A proof is then defined as a finite sequence of sentences such that each member either belongs to $\mathcal{H}$ or is derived from earlier members of the sequence by MP, CT, TC and US.

**Example 1.** $\vdash_{S} A \to A$.

| - | - | - |
| 1 | $\vdash_{S} A \to (B \to A)$ | H1 |
| 2 | $\vdash_{S} A \to ((A \to A) \to A)$ | US, 1 |
| 3 | $\vdash_{S} (A \to (B \to C)) \to ((A \to B) \to (A \to C))$ | H3 |
| 4 | $\vdash_{S} (A \to ((A \to A) \to A)) \to ((A \to (A \to A)) \to (A \to A))$ | US, 3 |
| 5 | $\vdash_{S} (A \to (A \to A)) \to (A \to A)$ | MP, 2, 4 |
| 6 | $\vdash_{S} A \to (A \to A)$ | US, 1 |
| 7 | $\vdash_{S} A \to A$ | MP, 5, 6 |

A normal modal logic is a set of formulas containing every formula falling under one or other of the schemata: (K): $&#10522; \Box (A \to B) \to (\Box A \to \Box B)$ and closed under MP, CT, TC, US and the rule of necessitation (RN): if $&#10522; A$ then $&#10522; \Box A$. As the appearance of $&#10522;$ here betrays, we are thinking of the above specification of a normal modal logic as an axiomatization of the smallest such logic, which is called $K$ (after Kripke).

**Theorem 1.** Every normal system of modal logic has the following theorems.

1. $\mathrm{N}$: $&#10522; \Box \top$;
2. $\mathrm{RM}$: if $&#10522; A \to B$ then $&#10522; \Box A \to \Box B$;
3. $\mathrm{M}$: $&#10522; \Box (A \wedge B) \to (\Box A \wedge \Box B)$;
4. $\mathrm{C}$: $&#10522; (\Box A \wedge \Box B) \to \Box (A \wedge B)$;
5. $\mathrm{R}$: $&#10522; \Box (A \wedge B) \leftrightarrow (\Box A \wedge \Box B)$;
6. $\mathrm{RR}$: If $&#10522; (A \wedge B) \to C$ then $&#10522; (\Box A \wedge \Box B) \to \Box C$;
7. $\mathrm{RE}$: if $&#10522; A \leftrightarrow B$ then $&#10522; \Box A \leftrightarrow \Box B$;
8. $\mathrm{RK}$: if $&#10522; (A_{1} \wedge \ldots \wedge A_{n}) \to B$ then $&#10522; (\Box A_{1} \wedge \ldots \wedge \Box A_{n}) \to \Box B$.

*Proof.* Let $S$ be a normal system of modal logic. Thus,

1. $\mathrm{N}$: $&#10522; \Box \top$.

| - | - | - |
| 1 | $&#10522; \bot \to A$ | H3 |
| 2 | $&#10522; \bot \to \bot$ | US, 1 |
| 3 | $&#10522; \top$ | Df $\top$, 2 |
| 4 | $&#10522; \Box \top$ | RN, 3 |

2. $\mathrm{RM}$: if $&#10522; A \to B$ then $&#10522; \Box A \to \Box B$.