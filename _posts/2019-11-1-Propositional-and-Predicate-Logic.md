---
title: Models of Computation Part1 - Basic Propositional and Predicate Logic
tags: exam ComputerTheory
---

## Propositional Logic
#### Difference between Syntax and Semantics:
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-10-28 at 10.04.19 pm.png]
### Syntax 语法
[{{site.baseurl}}/assets/mocpart1/CEF30D4F-D7C6-4D0B-B864-08623928F8D3.png]

#### Bind tightness
Assuming ¬ binds tighter than ^ and ∨
These bind tighter than ⊕, which binds tighter than ⇒ and ⇔.
¬高於∧，∧高於∨，∨高於⊕， ⊕高于→ 和⇔
This allows use to write without ambiguity
((P ∧ (¬Q)) ⇒ (P ∨ (P ⇔ Q))) 
**as** P ∧ ¬Q ⇒ P ∨ (P ⇔ Q)
[{{site.baseurl}}/assets/mocpart1/A887FE49-E7D7-4907-B75B-88589EEB05EA.png]

### Semantics 语义
A proposition is false or true
A  truth assignment maps each propositional letter to t or f
We can give the semantics of the connectives via ::truth tables::

### Truth Table
Assigning meaning to all propositional formulas, as we let A and B stands for the values of arbitrary (compound) propositions 断言
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-06 at 9.34.34 am.png]

### Conjunction and Disjunction
- Conjunction: P ∧ Q
- Disjunciton: P ∨ Q

### Implication 
P ⇒ Q means “if P then Q“, “P only if Q” or “Q whenever P”
可通过P推导出Q
P ⇒ Q equals to ¬P ∨ B
### XOR
[{{site.baseurl}}/assets/mocpart1/bear_sketch@2x.png]

### Nor and Nand
We can also define ↓ or ‘nor’, ↑ or ‘nand’. “Nand” is sometimes called Sheffer’s stroke
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-06 at 9.41.32 am.png]

## Logic Concepts
### Validity and Satisfiability 
- A propositional formula is **valid** if no truth assignment makes it false. 
	- Otherwise it is **non-valid**
- It is **unsatisfiable** if no truth assignment makes it true. 
	- Otherwise it is **satisfiable**.
- A valid propositional formula is a **tautology** 赘述
- An unsatisfiable propositional formula is a **contradiction** 矛盾

#### Valid means Vacuous 空洞的 显而易见
Logically, “Valid” means vacuous. For example, A ⇒ A is a vacuous statement, and valid. 
Eg. *“If Trump is sane then Trump is sane”* tells us nothing about whether Trump is sane—the statement is true whatever the case may be. You don’t even have to know who Trump is, or what it means to be sane, in order to agree: ::The statement is **inherently** true.::

#### Example: Contradiction
P ∧ Q ∧ (¬Q ⇔ (¬P ∨ Q))  is unsatisfiable.
Other than complete the truth table, P and Q are conjuncts of the formula, so if a truth assignment maps either to f, the formula evaluates to f.
And if P and Q are both mapped to t, the third conjunct becomes (¬t ⇔ (¬t ∨ t)), which again evaluates to f. 

#### Substitution Preserves Validity + Unsatisfiability
Validity is preserved by substitution of propositional letters by formulas.
(¬P ∧ Q) ⇒ (P ⇒ R)  is valid, and hence (¬(A ∨ B) ∧ (B ⇔ C)) ⇒ ((A ∨ B) ⇒ (B ⇔ C)) is valid.
**Note: A formula is unsatisfiable iff its negation is valid** 
	- 这句是个废话 如果一个公式不可被满足，只有当他的反义句是valid的，也就是都是True
It follows that substitution also preserves unsatisfiability

### Models, Logical Consequence, and Equivalence
Theta: θ
Phi /ph:ae/: Φ
Psi /sai:/: Ψ

#### Model
Let θ be a truth assignment and Φ be a propositional formula. If θ makes Φ true then θ is a model of Φ
#### Logical consequence 
Ψ is a ~logical consequence~ of Φ iff every model of Φ is a model of Ψ as well.
write as Φ |= Ψ
#### Equivalence
If Φ |= Ψ and Ψ |= Φ both hold, that is, Φ and Ψ have exactly the same models, then Φ and Ψ are (logically) equivalent.
In this case we write Φ ≡ Ψ

#### Example 
[{{site.baseurl}}/assets/mocpart1/6870024A-7E1E-4C1D-B97C-2224886DE46C.png]

#### Substitution Preserves Logical Equivalence
If Φ ≡ Ψ and Φ′ and Ψ′ are the results of replacing each occurrence of letter P (in both) with formula ε, then Φ′ ≡ Ψ′ .
#### Interchange of Equivalents
Replacing equals by equals will lead to equals. If
	- Φ is a sub-formula of ε,
	- Φ ≡ Ψ, and
	- ε′ is the result of replacing Φ in ε by Ψ,
Then ε ≡ ε′. 
- Interchange of equivalents preserves not only logical equivalence. It also preserves:
	- logical consequence, 
	- validity
	- unsatisfiability. 
Unlike substitution, it even preserves satisfiability

## Rules (Equivalences)
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-06 at 5.01.35 pm.png]
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-06 at 5.01.47 pm.png]
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-06 at 5.02.01 pm.png]

### Example Quiz: Which of these claims hold?
- P ⇒ Q ≡ (Q ⇔ (P ∨ Q)) 
[{{site.baseurl}}/assets/mocpart1/D152DC08-1E2A-439C-9CEA-07A50709553E.png]

* (P ⇒ Q) ∧ (P ⇒ R) ≡ P ⇒ (Q ∧ R) 
[{{site.baseurl}}/assets/mocpart1/5923DED8-369F-486A-BCAB-348A0ECD0AA5.png]

## Mechanised Reasoning
### Normal Forms for Propositional Logic
A literal is P or ¬P where P is a propositional letter. 

*note: Every propositional formula can be expressed in CNF, as well as in DNF.*
#### CNF (Conjunctive Normal Form) ∧
A formula is in ~conjunctive normal form (CNF)~ if it is a conjunction of disjunctions of literals (a conjunction of “clauses”).
		- (A ∨ ¬B) ∧ (B ∨ C ∨ D) ∧ A
#### DNF (Disjunctive Normal Form) ∨
It is in ~disjunctive normal form (DNF)~ if it is a disjunction of conjunctions of literals. 
		- (¬A ∧ ¬B) ∨ (¬B ∧ C) ∨ (A ∧ ¬D)

### Converting a formula between CNF and DNF
#### General steps:
1. Eliminate all occurrences of ⊕, using
	- A⊕B ≡ (A ∨ B) ∧ (¬A ∨ ¬B)
2. Eliminate all occurrences of ⇔, using
	- A ⇔ B ≡ (A ⇒ B) ∧ (B ⇒ A).
3. Eliminate all occurrences of ⇒ using A ⇒ B ≡ ¬A ∨ B.
4. Use *De Morgan’s Laws* to push ¬ inward over ∧ and ∨.
5. Eliminate double negations using ¬¬A ≡ A.
6. Use the distributive laws to get the required form.
#### Example: to CNF
	(¬P ∧ (¬Q ⇒ R)) ⇔ S 
2 ≡ ((¬P ∧ (¬Q ⇒ R)) ⇒ S) ∧ (S ⇒ (¬P ∧ (¬Q ⇒ R))) 
3 ≡ (¬(¬P ∧ (¬Q ⇒ R)) ∨ S) ∧ (¬S ∨ (¬P ∧ (¬Q ⇒ R))) 
3 ≡ (¬(¬P ∧ (¬¬Q ∨ R)) ∨ S) ∧ (¬S ∨ (¬P ∧ (¬¬Q ∨ R)))
4 ≡ ((¬¬P ∨ (¬¬¬Q ∧ ¬R)) ∨ S) ∧ (¬S ∨ (¬P ∧ (¬¬Q ∨ R)))
5 ≡ ((P ∨ (¬Q ∧ ¬R)) ∨ S) ∧ (¬S ∨ (¬P ∧ (Q ∨ R)))
6 ≡ (((P ∨ ¬Q) ∧ (P ∨ ¬R)) ∨ S) ∧ ((¬S ∨ ¬P) ∧ (¬S ∨ (Q ∨ R)))
6 ≡ (P ∨ ¬Q ∨ S) ∧ (P ∨ ¬R ∨ S) ∧ (¬S ∨ ¬P) ∧ (¬S ∨ Q ∨ R)

The result is in RCNF, but doen’t means it’s in unique form. 
### RCNF (Reduced CNF)
A CNF formula is in reduced CNF (RCNF) if, for each of its clauses, no propositional letter occurs twice.
- E.g. 
(A ∨ ¬B ∨ ¬A) ∧ (¬C ∨ ¬B) ∧ (C ∨ ¬A ∨ C ∨ B) Becomes (¬C ∨ ¬B) ∧ (C ∨ ¬A ∨ B)

### Canonical Forms: Xor Normal Form
If a normal form ~leads to a unique representation for every Boolean function~, we call it **canonical** 
 canonical form (“Xor normal form”) presents the function in a sum-of-products form, using exclusive or and conjunction.
For example, the formula (A ⇒ B) ∧ (B ⊕ C) is written as 
	- ABC ⊕ AC ⊕ B ⊕ C
This form is **unique**, up to reordering of conjuncts and summands. Or, representing the summands as sets:
	- {{A, B, C}, {A, C}, {B}, {C}}
	
### Canonical Forms: ROBDDs
::Binary decision diagrams (BDDs) give another canonical form::
::(A ⇒ B) ∧ (B ⊕ C)  can be represented by the graph:::
::If A then [follow solid arc] else [follow dashed arc] If A then B then::
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-13 at 5.52.47 pm.png]

#### Validity and Satisfiability with ROBDDs
This graph representation becomes canonical when we enforce maximal sharing of subgraphs (and agree on an ordering of variables like A, B, C).
The resulting graph is then an **ROBDD** - a reduced, ordered BDD.
These have been very popular and useful for hardware verification etc.
Clearly a propositional formula is valid iff its ROBDD is the single-leaf graph **t**. It is unsatisfiable iff its ROBDD is **f**


### Clausal Form
Knowledge bases are often presented in CNF, as a ~set (conjunction) of clauses.~ A clauses is a set (disjunction) of literals.
Abstracting from the order of literals and clauses, we can think of a formula in CNF as given in **clausal form**,  we may write:
- (P ∨ ¬Q ∨ S) ∧ (P ∨ ¬R ∨ S) ∧ (¬S ∨ ¬P) ∧ (¬S ∨ Q ∨ R)
As 
- {{P, S, ¬Q}, {P, S, ¬R}, {¬P, ¬S}, {Q, R, ¬S}}
- No distinction between these.

#### Empty Clauses
Clause {A,B} represents A ∨ B, and clause {A} represents A.
The natural reading of the term `clause ∅` is **false**
because **f** is neutral element for ∨, and we could have written A ∨ B as **f** ∨ A ∨ B, and A as **f** ∨ A.
Hence we agree that the ::empty clause ∅ represents ⊥.::
#### Empty Formulas
The formula {C1, C2}, with clauses C1 and C2, represents C1 ∧ C2. 
The formula {C} represents C. 
The natural reading of the (CNF) formula ∅: it is true
because **t** is neutral element for ∧, and we could have written C1 ∧ C2 as **t** ∧ C1 ∧ C2, and C as **t** ∧ C. 
Hence we agree that the ::empty formula ∅ represents ⊤.::
### Summary
For clausal form representation (CNF) we then have:
	- The set ∅ of clauses is **valid**. 
	- Any set {∅, . . .} of clauses is **unsatisfiable**.
An empty set of clauses is valid, because it is trivial to satisfy all of the set’s clauses—there is nothing to do.
But a (non-empty) set that contains an empty clause cannot be satisfied, because nothing satisfies that empty clause.
**In particular, note that {∅} != ∅.** ({∅} means false, ∅ means true)

### Resolvent
Consider the two clauses ¬P ∨ A and P ∨ B
	- If P is true, they reduce to A and t
	- If P is false, they reduce to t and B
There are no other possible values for P, so: if ¬P ∨ A and P ∨ B are both true, then either A is true or B is true (or both). That is, the clause A v B is a logical consequence of the two original clauses. We call A v B their **resolvent**
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-13 at 6.23.58 pm.png]

#### Propositional resolution 
[{{site.baseurl}}/assets/mocpart1/B69DE916-F88B-49CA-9484-DE4E047EEC1B.png]

#### Refuting a set of Clauses (Refuting Proof of Unsatisfiability)
Resolution suggests a way of verifying that a CNF formula is unsatisfiable
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-13 at 6.41.14 pm.png]
If, through a number of resolution steps, we can derive the empty clause ⊥, then the original set of clauses were unsatisfiable.

##### Example1: refutation
[{{site.baseurl}}/assets/mocpart1/2F037132-7A97-46EB-8E9C-2467B90AC191.png]
##### Example2: refutation
[{{site.baseurl}}/assets/mocpart1/0AA7CEF3-3EBF-41D4-8494-14D7C2BBDE7F.png]
Not possible to derive unsatisfiable ⊥ here.

#### Deductions and Refutations
A **resolution deduction** of clause C from a set S of clauses is a finite sequence C1, C2 .. Cn of clauses such that Cn=C and for each I, 1<=i<=n, Ci is either a member of S or a resolvent of Cj and Ck, for some j, k <i
A **resolution refutation** of a set S of clauses is a resolution deduction of ⊥(unsatisfiable) from D

### Resolution principle 
The idea of Propositional Resolution is simple. Suppose we have the clause {*p*,*q*}. In other words, we know that*p*is true or*q*is true. Suppose we also have the clause {¬*q*,*r*}. In other words, we know that*q*is false or*r*is true. One clause contains*q*, and the other contains ¬*q*. If*q*is false, then by the first clause*p*must be true. If*q*is true, then, by the second clause,*r*must be true. Since*q*must be either true or false, then it must be the case that either*p*is true or*r*is true. So we should be able to derive the clause {*p*,*r*}.
The case we just discussed is an example. If we have the clause {*p*,*q*} and we also have the clause {¬*q*,*r*}, then we can derive the clause {*p*,*r*} in a single step.
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-19 at 3.14.18 am.png]

### Using refutation (Show validity)
To show that Φ is valid, first put ¬Φ in RCNF, yielding a set S of clauses.
Then refute S, that is, deduce ⊥ from S.
- Consider: (P ⇒ R) ∨ (R ⇒ (P ∧ Q))
- Negating yields: ¬((¬P ∨ R) ∨ (¬R ∨ (P ∧ Q)))
- Pushing negation then yields: P ∧ ¬R ∧ R ∧ (¬P ∨ ¬Q)
From this we can derive ⊥ in a single resolution step.
[{{site.baseurl}}/assets/mocpart1/768AAAE0-ACEE-41AC-8979-AF094FB51773.png]
Because (not R and R) will allways be False in any case
Therefore we can derive unsatisfibility for this formula in a single resolution step

2. Suppose we express a circuit design as a formula Φ in RCNF.
Suppose we wish to show that the design satisfies some property Ψ, that is, show Φ |= Ψ.
We can exploit this fact: 
- **Φ |= Ψ iff Φ ∧ ¬Ψ is unsatisfiable**
Hence a strategy is:
	- Negate Ψ and bring it into RCNF; 
	- add those clauses to the set Φ; and 
	- find a refutation of the resulting set of clauses.


## Predicate Logic
### Definitions
- predicate logic allows to
	-  finitely express statements that deal with infinite collections of objects (integers, for example); 
		- 有限的表达去处理无限的对象集合
	- express relations, capturing transitive verbs and relative pronouns.
		- 表达关系捕捉过度的动词相关的代词
To enable this, predicate logic uses **variables** that are assumed to range over collections of individuals, such as integers, graphs, people, or whatever, as well as **quantifiers**.
Propositional letters become generalised to **predicates**, that is functions that map tuples of individuals to false or true.
#### Example: Expressing Relations
Tom found Rover and returned him to Anne:
	Found(tom, rover) ∧ Gave(tom, rover, anne)
Tom found a dog and gave **it** to Anne:
	∃x (Dog(x) ∧ Found(tom, x) ∧ Gave(tom, x, anne))
Jill inhabits the house **that** Jack built:
	∃x (House(x) ∧ Inhabits(Jill, x) ∧ BuilderOf (jack, x))

### Quantification and Vocabulary

#### Quantification
Existential quantification, ∃, is generalised ∨. 
Universal quantification, ∀, is generalised ∧.
Quantifier examples:
“Every human is mortal” -> ∀x (Human(x) ⇒ Mortal(x))
“Some cat is mortal” -> ∃x (Cat(x) ∧ Mortal(x))- The alphabet of a first-order language 
**Note: Very common to use ⇒ with ∀ and ∧ with ∃.**
*Example:*
L(bob, Eva) -> Bob loves Eva
- ∀x L(x, Eva) -> Everyone loves Eva (incl. Eva)
- ∀x (¬I(x, Eva) ⇒ L(x, Eva)) -> Eva is loved by everyone else
- ∃x (¬I(x, bob) ∧ L(x, bob)) -> Someone other than Bob loves Bob
- ∀x (∃y L(x, y )) -> Everybody loves somebody
- ∃y (∀x L(x, y )) -> Someone is loved by everybody
- ∃x (∀y L(x, y )) -> Someone loves everybody
#### Vocabulary:
	- Variables (x,y,z,u,v,w)
	- function symbols (f,g,h … )
	- constants (Abosch,c, … , 0,1, tom)
	- predicate symbols (P,Q,R,A,B , … , <, =)
	- connectives
	- quantifiers
	- parentheses
	- (sometimes: **f, t**)
Each function symbol comes with an **arity**: a number that says how many arguments the function takes. Each predicate symbol similarly comes with an arity.

### Terminology
A term is a variable or a constant or a construction f(t1…tn)
	- Where n > 0 , f is a function symbol of arity n, and each ti is a term.
An **atomic formula** is a construction P(t1….tn) where n>=0 and P is a predicate symbol of arty n, and each ti is a term.
	Term ←→ Individual, object
	Atom ←→ Assertion (false or true)
A **literal** is an atomic formula or its negation.
#### Case Matters
A predicate starts with an upper case letter, nothing else does
	- father(ron) is a term, it denotes some object: the father of Ron
	- Father(ron) is a formula, it denotes a truth value: whether Ron is a father

### Syntax
Very much the same as the propostional logic
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-16 at 5.42.37 pm.png]

### Bound and Free variable
A variable which is in the scope of a quantifier (binding that variable) is bound. 
If it is not bound then it is free. 
A variable may occur both free and bound in a formula — witness y in 
		- ∀z (P(x, y , z) ∧ ∀y (P(f (x), z, y )))
It is possible for scopes to have “holes”:
		- ∀x∃y (x < y ∧ ∃x (y < x))
		- The last occurrence of x is bound by the closest quantifier, so the scope of ∀x is not all of ∃y (. . .).
#### Bound variable renaming and capture
The bound variable of a quantified formula is just a placeholder — its exact name is inessential.
	- ∃x∀y (x< y) means the same as ∃x∀ z (x<z)
If a variable occurs bound in a certain expression then the meaning of that expression does not change when all bound occurrences of that variable are replaced by another one.
However, to avoid **variable capture**, we cannot change the variable bound by ∀y to a variable in an enclosing scope:
	- ∃x∀y (x< =y) means the same as ∃x∀ x (x<=x)
### Questions
[{{site.baseurl}}/assets/mocpart1/DB384E05-ED95-4E7D-9B32-9E0DC18F67C6.png]

## Predicate Logic: Syntax
### The Meaning of a predicate logic formula
Is this closed formula true or false?
∀x, z (x < z ⇒ ∃y (x < y ∧ y < z))
It depends on what ‘<’ stands for, and the ~domain D~ of interest, that is, what sort of things x, y, and z denote.
- It is **false** if D=**Z** and < is the usual “smaller than“
- It is **true** if D = **Z** and < is “smaller than or equal”
- It is **true** if D = **R** and < is the usual “smaller than”
- It is **true** if D = {0}. 
- In some cases, the meaning of a formula is independent of what its predicate names denote, and of what sort of things the variables range over.
- Eg.
	- ∀x P(x) ∨ ∃y (¬P(y )) is inherently true, no matter what domain is, no matter what(it is **valid**).
	- Similarly, ∀x P(x) ∧ (¬P(a)) is false no matter what a and P stand for (the formula is **unsatisfiable**).
	- 
### Interpretations/Structures
An interpretation consists of 
	- A non-empty set D (the domain, or universe)
	- An assignment, to each n-ary predicate symbol P, of an n-place function **p**: D^n -> {**f**, **t**}
	- An assignment, to each n-ary function symbol g, of an n-place function **g:** D^n -> D;
	- An assignment to each constant ~a~ of some fixed element of D
#### Free variables and Valuations
formulas that may have free variables, for example:
			- ∃x P(f(y),x) 
We need to consider two things:
	- A **valuation** is a function σ : var → D for free variables;
	- An interpretation as just discussed
Connectives are always given their usual meaning
#### Terms and Valuations
Given an interpretation I, we get a valuation function from terms automatically, by natural extension:
			- σ(a) = d
			- σ(g(t1, . . . ,tn)) = g(σ(t1), . . . , σ(tn))
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-10-30 at 8.01.17 pm.png]

### Truth of a Formula
The truth of a closed formula should depend only on the given interpretation. Our only interest in formulas with free variable is that we want to define the truth of a formula compositionally
[{{site.baseurl}}/assets/mocpart1/DF5EB287-D4B9-4C83-B93A-6E7E50A5D61B.png]

### Making a Formula True
[{{site.baseurl}}/assets/mocpart1/554CDC2D-3A3A-47F1-B0E7-FEB844073112.png]

### models and Validity of Formulas 
[{{site.baseurl}}/assets/mocpart1/Screen Shot 2019-08-23 at 9.27.09 pm.png]

### SummarisingL Satisfiability and Validity
A closed, wff is 
	- **Satisfiable** iff I |= F for some interpretation I;
	- **valid** iff I |= F for every interpretation I;
	- **unsatisfiable** iff I |!= F for every interpretation I;
	- **non-valid** iff I |!= F for some interpretation I.
As in the propositional case, we have
	- F is valid iff ¬F is unsatisfiable; 
	- F is non-valid iff ¬F is satisfiable.
#### Example: Non-Validity
[{{site.baseurl}}/assets/mocpart1/69B59D6B-C9B2-45CF-952C-3597D9AE443F.png]

#### Example: Validity
[{{site.baseurl}}/assets/mocpart1/89D76CB2-1812-4686-965E-FD5AEDA0B424.png]

## Rules: Quantifiers
[{{site.baseurl}}/assets/mocpart1/6C965FA6-B542-4449-8912-E86922B0E503.png]
[{{site.baseurl}}/assets/mocpart1/5D3488DC-2802-41FD-A133-D697B40D999A.png]


## Predicate Logic: Clausal Form
### Resolution for Predicate Logic
As for propositional logic, it assumes clasual form, that is, having a formula presented in conjunctive normal form, without any quantifiers.
Again, it consists on generating logical consequences, trying to derive an empty clause, there by proving the original formula unsatisfiable.
Existential quantifiers are eliminated in a process called **Skolemization**

### Skolemization (Eliminating Existential Quantifiers)
Consider the formula F = ∃x∀y P(x,y) under some interpretation I 
F is satisfiable iff some valuation σ makes ∀y P(x,y) true. Say that σ(x) = d0, makes ∀y P(x,y) true.
Now consider a fresh constant a, and the formula ∀y P(a,y)
This formula is satisfiable iff F is. If I satisfies F then we simply add to I the mapping of a to d0 — this extended interpretation satisfies ∀y P(a,y)
This formula is satisfiable iff F is. If I satisfies F then we simply add to I the mapping of a to d0 — this extended interpretation satisfies ∀y P(a,y) 
If ∀y P(x,y) is unsatisfiable, there is no valuation that will make ∀y P(x,y) true. Hence no interpretation will make ∀y P(a,y) true.

We call a as a Skolem constant

#### Skolem Constants and functions
Now consider the formula G = ∀y∃x P(x,y), We cannot conclude that ∀y P(a,y) is satisfiable iff G is. 
Since ∃x is within the scope of ∀y, the value of x for which P(x,y) holds may differ, given different values of y. The value of x is a function of the value of y. Replacing x by a constant will not do. 
But then we can generate the formula ∀y P(f(y),y), choosing a fresh function symbol f . 
We call f(y) as Skolem function

#### Example: Skolemization
[{{site.baseurl}}/assets/mocpart1/C7EA3079-5637-4D7B-96F3-4C27D6C1D51F.png]

### General Steps: Transform to Cluster form
[{{site.baseurl}}/assets/mocpart1/CF6C38A8-5AA8-4EBE-95D2-ADDAF62F9227.png]

#### Note: Skolemization Justification
Note that Skolemization of a formula does not produce a logically equivalent formula. 
For example, ∀x∃y P(x,y) turns into ∀x P(x,f(x)). 
If we interpret these in the domain Z of integers, interpreting f as the “successor” function (+1), and P as >, then the original formula is satisfied, but the second is not. 

However, Skolemization does **produce an equisatisfiable formula**—one that is satisfiable iff the original was—and this is all we care about for the purposes of resolution proofs. 


#### Example
[{{site.baseurl}}/assets/mocpart1/3B9C7213-5606-408B-930E-A0F25F923D07.png]
[{{site.baseurl}}/assets/mocpart1/1CB26040-77D6-4EF3-9164-1B2CA2FE7DB4.png]
[{{site.baseurl}}/assets/mocpart1/35764DC5-FB24-423E-B00D-40418DBE8851.png]
[{{site.baseurl}}/assets/mocpart1/BF40BCC1-D067-4CD7-92F8-F1EC3145909E.png]
[{{site.baseurl}}/assets/mocpart1/B72B5C59-0280-4E29-B2A3-0B60323F46F7.png]
[{{site.baseurl}}/assets/mocpart1/040EDBA9-AB8B-419A-93BB-CD6693E605B5.png]

### Resolution for Predicate Logic
Simple cases seem easy enough, for example, from 
		- ¬B(x) ∨ M(x) and ¬M(c) 
we would like to conclude ¬B(c), note all variables in the formula above are universally quantified

In particular, we could instantiate ¬B(x) ∨ M(x) to ¬B(c) ∨ M(c), then we will be resolving the two clauses on M(c) and its negation, just as happened in the propositional case. The resolvent then comes out as ¬B(c) as we hope


## Predicate Logic: Unification and Resolution
### Substitutions
A substitution is a finite set of replacements of variables by terms, that is, a set θ of the form {x1 -> t1,x2 ->  t2,…,xn -> tn}, where the xi are variables and the ti are terms. 
We can also think of θ as a function from terms to terms, or from atomic formulas to atomic formulas. θ(F) is the result of simultaneously replacing each occurrence of xi in F by ti . 
[{{site.baseurl}}/assets/mocpart1/195CF7DA-293E-48FB-9A81-C98B1DBB1C61.png]

### Unifier
A unifier of two terms *s* and *t* is a substitution θ such that `θ(s) = θ(t)`
The terms s and t are **unifiable** iff there exists a unifier for s and t.

A most general unifier (mgu) for s and t is a substitution θ such that
	- θ is a unifier for s and t, and 
	- **Every other unifier σ of s and t can be expressed as τ ◦ θ for some substitution τ.** 
	- (The composition τ ◦ θ is the substitution we get by first using θ, and then using τ on the result produced by θ.) 
**Theorem**. If s and t are unifiable, they have a most general unifier. 

#### Examples:
[{{site.baseurl}}/assets/mocpart1/F4A3F71E-1090-4F5D-89E5-FB2E0552907A.png]
[{{site.baseurl}}/assets/mocpart1/D429C524-E818-48D2-81E3-77D9C5886509.png]

### A Unificaiton Algorithm
In the following, let x be a variable, let F and G be function or predicate names, and let s and t be arbitrary terms. 
- **Input**: Two terms s and t.
- **Output**: If they are unifiable: a most general unifier for s and t; otherwise ‘failure’.
- **Algorithm**: Start with the set of equations {s = t}.  (This is a singleton set: it has one element.)

As long as some equation in the set has one of the six forms listed on 
#### Solving Term Equations
[{{site.baseurl}}/assets/mocpart1/D0DD4E22-3ABA-4AFE-91A1-EF5EC77C97A2.png]
##### Example 1
[{{site.baseurl}}/assets/mocpart1/8E0B111D-D1C3-476C-AAE0-451FEA57EAE0.png]
##### Example 2
[{{site.baseurl}}/assets/mocpart1/873BAB8C-E312-42E1-9EA5-9559E9408065.png]
##### example 3
[{{site.baseurl}}/assets/mocpart1/52F5C884-6C42-462F-B7B0-7F271A2FFD63.png]

#### Term Equations as Substitutions 
The process of solving term equations always halts. 
When it halts without reporting ‘failure’, the term equation system is left in a normal form: On the left-hand sides we have variables only, and they are all different. Moreover, these variables occur nowhere in the right-hand sides. 
If the normal form is {x1 = t1,…,xn = tn}, then {x1 􏰀→t1,…,xn 􏰀→tn} is a most general unifier for the input terms s and t. If the result is ‘failure’, no unifier exists.

### Resolvents
[{{site.baseurl}}/assets/mocpart1/C01BF93B-EC51-4F26-9D56-13DBBB27035F.png]

#### Refutation
##### Example:Tadpoles in Clausal Form
[{{site.baseurl}}/assets/mocpart1/3927A4BB-E1A6-47A2-9328-9C68468BDEE9.png]

#### A Refutation
[{{site.baseurl}}/assets/mocpart1/841B13FD-063F-4F7F-907D-326EA45BCFE6.png]
[{{site.baseurl}}/assets/mocpart1/8039B82B-E6F2-4295-AB57-2AEDBEF98F81.png]

After several steps, we generates empty caluse, so input set unsatisfiable.
[{{site.baseurl}}/assets/mocpart1/9DBCD199-8F28-4EA9-9B10-33BAE0C5D3CE.png]

#### Factoring
In addition to resolution, there is one more valid rewriting of clauses, called factoring.
Let C be a clause and let A1, A2 ∈ C. If A1 and A2 are unifiable with mug θ, add the clause θ (C).
[{{site.baseurl}}/assets/mocpart1/76A6F8C1-1631-4ABA-A463-9A04FDC226E1.png]
Factoring is sometimes crucial:
[{{site.baseurl}}/assets/mocpart1/4144D5AF-99D8-42F0-96C9-672573A8A75D.png]
#### How to Use Clauses
A resolution step uses two clauses (or two “copies” of the same clause). A factoring step uses one clause. 
**A given clause can be used many times in a refutation, taking part in many different resolution/factoring steps.**
Hence we should really rename all variables in a clauses every time we use the clause, using fresh variable names. Sometimes this renaming is essential for correctness, especially when resolution uses two “copies” of the same clause.
*Recall: each clauses is implicitly universally quantified*

#### The Resolution Method
[{{site.baseurl}}/assets/mocpart1/B81BFCCD-AAD1-44CF-BF9F-18D023001868.png]

#### The Power of Resolution
**Theorem**: C is unsatisfiable iff the resolution method can add ⊥ after a finite number of steps. 

We say that resolution is **sound** and **complete**. 健全且完整
**It gives us a proof procedure for unsatisfiability (and validity).** 
*Note: however, that resolution does not give a **decision procedure** for unsatisfiability (or validity) of first-order predicate logic formulas.* 
Indeed, these are **undecidable** (or more precisely, semi-decidable) **properties**. 

#### Proof Search
[{{site.baseurl}}/assets/mocpart1/DCB2B3F2-BFA9-4A05-801B-2BCF83FE2FCF.png]
#### Horn Clauses and Prolog
A Horn clause is a clause with at most one positive literal 
All seven clauses used in the tadpole example were Horn. 
A clause such as {¬T(z),¬D(y),¬E(y,z),M(z)} can also be thought of as (T(z)∧D(y)∧E(y,z))⇒M(z)
In the logic programming language Prolog, the clause is written 
```
miserable(Z) :  - tadpole(Z), 
					 deepwaterfish(Y), 
					 eats(Y,Z). 
```
- For logic programs, the restriction to Horn clauses simplifies the search problem, but it does not remove it. 
- For propositional Horn clauses, satisfiability can be decided in linear time. (For arbitrary propositional CNF it is NP-complete.) 