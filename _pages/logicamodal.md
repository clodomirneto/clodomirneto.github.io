---
layout: archive
title: "Lógica Modal"
permalink: /logicamodal/
author_profile: true
---

<br />

* **Lógica**. É o estudo da legitimidade de argumentos.

* **Argumento**. É uma sequência de proposições na qual uma das proposições é a conclusão e as demais são as premissas.

* **Proposição**. Sentença declarativa na qual podemos atribuir um valor lógico.

* **Leis do Pensamento**
1. Princípio da identidade: Se uma proposição é verdadeira, então esta proposição é verdadeira.
2. Princípio da não-contradição: Uma proposição não pode ser verdadeira e falsa ao mesmo tempo.
3. Princípio do terceiro excluído: Toda proposição ou é verdadeira ou é falsa, nunca existindo um terceiro caso.

* **Lógica Formal**. Investiga as estruturas das proposições e do raciocínio dedutivo, ignorando o conteúdo das proposições que venham a ser consideradas, para concentrar-se apenas em sua forma.

* **Alfabeto**. Dado um conjunto numerável $P$, o alfabeto proposicional sobre $P$ designa-se $Alf_{P}$ e é constituído por:
1. Símbolos Proposicionais: $A$, $B$, $C$, $\ldots$;
2. Símbolo $\bot$ (absurdo, contradição, falso);
3. Conectivos Proposicionais: $\neg$ (negação), $\wedge$, (conjunção), $\vee$ (disjunção), implicação ($\to$), bi-implicação ($\leftrightarrow$);
4. Símbolos de Pontuação: $($ , $)$.

* **Linguagem**. A linguagem proposicional induzida por $Alf_{P}$ designa-se $L_{P}$ e é o conjunto definido por:
1. $p \in L_{P}$, qualquer que seja $p \in P$;
2. $\bot \in L_{P}$;
3. $(\neg \phi) \in L_{P}$, $(\phi \wedge \psi) \in L_{P}$, $(\phi \vee \psi) \in L_{P}$, $(\phi \to \psi) \in L_{P}$, $(\phi \leftrightarrow \psi) \in L_{P}$, quaisquer que sejam $\phi, \, \psi \in L_{P}$.

$\quad$ Os elementos de $L_{P}$ são as fórmulas da linguagem proposicional induzida por $Alf_{P}$, também chamada de fórmula bem formada (fbf).

* **Dedução Natural**

*1.* Absurso ($\bot E$): Se uma derivação chega a uma contradição, então pode-se deduzir a validade de qualquer proposição.

<center>
$\dfrac{\bot}{\phi} \bot E$
</center>

*2.* Absurdo clássico (PBC): Exibida uma derivação de uma contradição a partir de uma hipótese $\neg \phi$, descarta-se a hipótese e infere-se $\phi$.

<center>
$
\begin{array}{c}
\hspace{-1.5cm} [\neg \phi]^{\alpha} \\
\hspace{-2cm} \vdots \\
\dfrac{\bot}{\phi} PBC, \alpha
\end{array}
$
</center>

*3.* Introdução da negação ($\neg$I): Exibida uma derivação de uma contradição a partir de uma hipótese $\phi$, descarta-se a hipótese e infere-se $\neg \phi$.

<center>
$
\begin{array}{c}
\hspace{-1cm} [\phi]^{\alpha} \\
\hspace{-1.4cm} \vdots \\
\dfrac{\bot}{\neg \phi} \neg I, \alpha
\end{array}
$
</center>

*4.* Eliminação da negação ($\neg$E): De quaisquer fbfs $\neg \phi$ e $\phi$, infere-se $\bot$.

<center>
$\dfrac{\neg \phi \qquad \phi}{\bot} \neg E$
</center>

*5.* Introdução da conjunção ($\wedge$I): De quaisquer fbfs $\phi$ e $\psi$, infere-se a conjunção $\phi \wedge \psi$.

<center>
$\dfrac{\phi \qquad \psi}{\phi \wedge \psi} \wedge I$
</center>

*6.* Eliminação da conjunção ($\wedge$E): De uma conjunção infere-se cada um de seus conjunctos.

<center>
$
\begin{array}{cc}
\dfrac{\phi \wedge \psi}{\phi} \wedge E_{1} \qquad & \dfrac{\phi \wedge \psi}{\psi} \wedge E_{2}
\end{array}
$
</center>

*7.* Introdução da disjunção ($\vee$I): De uma fbf $\phi$, infere-se a disjunção de $\phi$ com qualquer fbf.

<center>
$
\begin{array}{cc}
\dfrac{\phi}{\phi \vee \psi} \vee E_{1} \qquad & \dfrac{\psi}{\phi \vee \psi} \vee E_{2}
\end{array}
$
</center>

*8.* Eliminação da disjunção ($\vee$E): De fbfs $\phi \vee \psi$, $\phi \to \theta$ e $\psi \to \theta$, infere-se $\theta$.

<center>
$
\begin{array}{c}
\hspace{0.5cm} [\phi]^{\alpha} \hspace{0.5cm} [\psi]^{\beta} \\
\hspace{0.3cm}\vdots \hspace{1.4cm} \vdots \\
\dfrac{\phi \vee \psi \qquad \theta \qquad \theta}{\theta} \vee E, \alpha, \beta
\end{array}
$
</center>

*9.* Introdução da implicação ($\to$I): Exibida uma derivação de uma fbf $\psi$ a partir de uma hipótese $\phi$, descarta-se a hipótese e infere-se $\phi \to \psi$.

<center>
$
\begin{array}{c}
\hspace{-1.5cm} [\phi]^{\alpha} \\
\hspace{-1.8cm} \vdots \\
\dfrac{\psi}{\phi \to \psi} \to I, \alpha
\end{array}
$
</center>

*10.* Eliminação da implicação ($\to$E): De fbfs $\phi \to \psi$ e $\phi$, infere-se $\psi$.

<center>
$\dfrac{\phi \to \psi \qquad \phi}{\psi} \to E$
</center>

*11.* Introdução da bi-implicação ($\leftrightarrow$I): De fbfs $\phi \to \psi$ e $\psi \to \phi$, infere-se $\phi \leftrightarrow \psi$.

<center>
$\dfrac{\phi \to \psi \qquad \psi \to \phi}{\phi \leftrightarrow \psi} \leftrightarrow I$
</center>

*12.* Eliminação da bi-implicação ($\leftrightarrow$E): De uma fbf $\phi \leftrightarrow \psi$, infere-se $\phi \to \psi$ e $\psi \to \phi$.

<center>
$
\begin{array}{cc}
\dfrac{\phi \leftrightarrow \psi}{\phi \to \psi} \leftrightarrow E_{1} \qquad & \dfrac{\phi \leftrightarrow \psi}{\psi \to \phi} \leftrightarrow E_{2}
\end{array}
$
</center>

* **Derivações**

*1.* Absorção (ABS): $A \to B \vdash A \to (A \wedge B)$

| 1 | $A \to B$ | P |
| 2 | $A$ | $H(\to)$ |
| 3 | $B$ | $\to E, 1, 2$ |
| 4 | $A \wedge B$  | $\wedge I, 2, 3$ |
| 5 | $A \to (A \wedge B)$  | $\to I, 2-4$ |

```coq
Section PropositionalLogic.
Variables A B : Prop.
Hypothesis P1 : A -> B.
Theorem abs : A -> (A /\ B).
Proof.
intro Ha.
split.
- exact Ha.
-
apply P1.
exact Ha.
Qed.
End PropositionalLogic.
```

*2.* Silogismo Hipotético (SH): $A \to B, B \to C \vdash A \to C$

```coq
Section PropositionalLogic.
Variables A B C: Prop.
Hypothesis P1 : A -> B.
Hypothesis P2 : B -> C.
Theorem sh : A -> C.
Proof.
intro Ha.
apply P2.
apply P1.
exact Ha.
Qed.
End PropositionalLogic.
```

*3.* Silogismo Disjuntivo (SD): $A \vee B, \neg A \vdash B$

```coq
Section PropositionalLogic.
Variables A B : Prop.
Hypothesis P1 : A \/ B.
Hypothesis P2 : ~A.
Theorem sd : B.
Proof.
destruct P1 as [Ha | Hb].
contradiction.
exact Hb.
Qed.
End PropositionalLogic.
```

*4.* Modus Tollens (MT): $A \to B, \neg B \vdash \neg A$

```coq
Section PropositionalLogic.
Variables A B : Prop.
Hypothesis P1 : A -> B.
Hypothesis P2 : ~B.
Theorem mt : ~A.
Proof.
unfold not.
intro Ha.
unfold not in P2.
apply P2.
apply P1.
exact Ha.
Qed.
End PropositionalLogic.
```

*5.* Dilema Construtivo (DC): $A \vee B, A \to C, B \to D \vdash C \vee D$

```coq
Section PropositionalLogic.
Variables A B C D : Prop.
Hypothesis P1 : A \/ B.
Hypothesis P2 : A -> C.
Hypothesis P3 : B -> D.
Theorem dc : C \/ D.
Proof.
destruct P1 as [Ha | Hb].
left.
apply P2.
exact Ha.
right.
apply P3.
exact Hb.
Qed.
End PropositionalLogic.
```

*6.* Dilema Destrutivo (DD): $\neg C \vee \neg D, A \to C, B \to D \vdash \neg A \vee \neg B$

```coq
Section PropositionalLogic.
Variables A B C D : Prop.
Hypothesis P1 : ~C \/ ~D.
Hypothesis P2 : A -> C.
Hypothesis P3 : B -> D.
Theorem dd : ~A \/ ~B.
Proof.
destruct P1 as [Hnc | Hnd].
left.
unfold not.
intro Ha.
unfold not in Hnc.
apply Hnc.
apply P2.
exact Ha.
right.
unfold not.
unfold not in Hnd.
intro Hb.
apply Hnd.
apply P3.
exact Hb.
Qed.
End PropositionalLogic.
```

*7.* Transposição (TRANS): $\vdash (A \to B) \leftrightarrow (\neg B \to \neg A)$

*8.* Implicação Material (IM): $\vdash (A \to B) \leftrightarrow (\neg A \vee B)$

*9.* Exportação (EXP): $\vdash ((A \wedge B) \to C) \leftrightarrow (A \to (B \to C))$

```coq
Section PropositionalLogic.
Variables P Q R : Prop.
Theorem exp : ((P /\ Q) -> R) <-> (P -> (Q -> R)).
Proof.
unfold iff.
split.
-
intro Hpqr.
intro Hp.
intro Hq.
apply Hpqr.
split.
*
exact Hp.
*
exact Hq.
-
intro Hpqr.
intro Hpq.
apply Hpqr.
destruct Hpq as [Hp Hq].
exact Hp.
destruct Hpq as [Hp Hq].
exact Hq.
Qed.
End PropositionalLogic.
```

*10.* Tautologia (TAUT): $\vdash A \leftrightarrow (A \wedge A)$

```coq
Section PropositionalLogic.
Variables A : Prop.
Theorem taut_and : A <-> (A /\ A).
Proof.
unfold iff.
split.
-
intro Ha.
split.
*
exact Ha.
*
exact Ha.
-
intro Haa.
destruct Haa as [Ha Ha1].
exact Ha.
Qed.
End PropositionalLogic.
```

*11.* Tautologia (TAUT): $\vdash A \leftrightarrow (A \vee A)$

```coq
Section PropositionalLogic.
Variables A : Prop.
Theorem taut_or : A <-> (A \/ A).
Proof.
unfold iff.
split.
-
intro Ha.
left.
exact Ha.
-
intro Haa.
destruct Haa as [Ha | Ha1].
exact Ha.
exact Ha1.
Qed.
End PropositionalLogic.
```

*12.* Comutação (COM): $\vdash (A \wedge B) \leftrightarrow (B \wedge A)$

```coq
Section PropositionalLogic.
Variables A B : Prop.
Theorem com_and : (A /\ B) <-> (B /\ A).
Proof.
unfold iff.
split.
-
intro Hab.
split.
*
destruct Hab as [Ha Hb].
exact Hb.
*
destruct Hab as [Ha Hb].
exact Ha.
-
intro Hba.
split.
+
destruct Hba as [Hb Ha].
exact Ha.
+
destruct Hba as [Hb Ha].
exact Hb.
Qed.
End PropositionalLogic.
```

*13.* Comutação (COM): $\vdash (A \vee B) \leftrightarrow (B \vee A)$

```coq
Section PropositionalLogic.
Variables A B : Prop.
Theorem com_or : (A \/ B) <-> (B \/ A).
Proof.
unfold iff.
split.
-
intro Hab.
destruct Hab as [Ha | Hb].
right.
exact Ha.
left.
exact Hb.
-
intro Hba.
destruct Hba as [Hb | Ha].
right.
exact Hb.
left.
exact Ha.
Qed.
End PropositionalLogic.
```

*14.* Lei de De Morgan (DM): $\vdash \neg (A \wedge B) \leftrightarrow (\neg A \vee \neg B)$

*15.* Lei de De Morgan (DM): $\vdash \neg (A \vee B) \leftrightarrow (\neg A \wedge \neg B)$

*16.* Associação (ASSOC): $\vdash (A \wedge (B \wedge C)) \leftrightarrow ((A \wedge B) \wedge C)$

```coq
Section PropositionalLogic.
Variables A B C : Prop.
Theorem assoc_and : (A /\ (B /\ C)) <-> ((A /\ B) /\ C).
Proof.
unfold iff.
split.
-
intro Habc.
split.
*
destruct Habc as [Ha Hbc].
split.
+
exact Ha.
+
destruct Hbc as [Hb Hc].
exact Hb.
*
destruct Habc as [Ha Hbc].
destruct Hbc as [Hb Hc].
exact Hc.
-
intro Habc.
split.
*
destruct Habc as [Hab Hc].
destruct Hab as [Ha Hb].
exact Ha.
*
split.
+
destruct Habc as [Hab Hc].
destruct Hab as [Ha Hb].
exact Hb.
+
destruct Habc as [Hab Hc].
exact Hc.
Qed.
End PropositionalLogic.
```

*17.* Associação (ASSOC): $\vdash (A \vee (B \vee C)) \leftrightarrow ((A \vee B) \vee C)$

```coq
Section PropositionalLogic.
Variables A B C : Prop.
Theorem assoc_or : (A \/ (B \/ C)) <-> ((A \/ B) \/ C).
Proof.
unfold iff.
split.
-
intro Habc.
destruct Habc as [Ha | [Hb | Hc]].
left.
left.
exact Ha.
left.
right.
exact Hb.
right.
exact Hc.
-
intro Habc.
destruct Habc as [[Ha | Hb] | Hc].
left.
exact Ha.
right.
left.
exact Hb.
right.
right.
exact Hc.
Qed.
End PropositionalLogic.
```

*18.* Distribuição (DIST): $\vdash (A \wedge (B \vee C)) \leftrightarrow ((A \wedge B) \vee (A \wedge C))$

```coq
Section PropositionalLogic.
Variables A B C : Prop.
Theorem dist_and : (A /\ (B \/ C)) <-> ((A /\ B) \/ (A /\ C)).
Proof.
unfold iff.
split.
-
intro Habc.
destruct Habc as [Ha Hbc].
destruct Hbc as [Hb | Hc].
left.
split.
*
exact Ha.
*
exact Hb.
*
right.
split.
+
exact Ha.
+
exact Hc.
-
intro Habc.
destruct Habc as [Hab | Hac].
split.
*
destruct Hab as [Ha Hb].
exact Ha.
*
left.
destruct Hab as [Ha Hb].
exact Hb.
*
split.
+
destruct Hac as [Ha Hc].
exact Ha.
+
right.
destruct Hac as [Ha Hc].
exact Hc.
Qed.
End PropositionalLogic.
```

*19.* Distribuição (DIST): $\vdash (A \vee (B \wedge C)) \leftrightarrow ((A \vee B) \wedge (A \vee C))$

```coq
Section PropositionalLogic.
Variables A B C : Prop.
Theorem dist_or : (A \/ (B /\ C)) <-> ((A \/ B) /\ (A \/ C)).
Proof.
unfold iff.
split.
-
intro Habc.
destruct Habc as [Ha | [Hb Hc]].
split.
*
left.
exact Ha.
*
left.
exact Ha.
*
split.
+
right.
exact Hb.
+
right.
exact Hc.
-
intro Habc.
destruct Habc as [Hab Hac].
destruct Hab as [Ha | Hb].
left.
exact Ha.
destruct Hac as [Ha | Hc].
left.
exact Ha.
right.
split.
exact Hb.
exact Hc.
Qed.
End PropositionalLogic.
```