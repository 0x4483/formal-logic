## Formal Logic 

1. Sentential Logic 
2. Predicate Logic


### 1. Sentential Logic

Formal Logic has two essential components: sentential logic and predicate logic. We will first examine sentential logic below. 

#### 1.1 Syntax and Semantics 

To discuss the syntax of the formal logic, one must first understand the basic components that make up the formal logic. The most basic building block of any logical expression is called an __atom__. An atom that must be represented by capital letters can either take on __TRUE__ or __FALSE__. However, without __connectives__ (negation, &, ^, ->) and __symbols__( "(", ")", ",") these atoms cannot be formed into expressions. However, expressions are just finite sequence of atoms connected by the connectives. In order to have meaningful discussion of logic, a set of grammatic rules are required to form __formula__. The grammatic rules are recursively defined. Basically, a formula must take on several defined form: (F1 & F2), (F1 ^ F2), (F1 -> F2) or F1 is an atom (the base case). When we see a logical formula, we can break the formula down using a parse tree method where the leaf is the atomic truth variable and the branch are the connectives that glue these atoms together.  

The semantics of the formal logic focuses intensely on the truth value assignments. The most common way to investigate the truth value of a formula is to use a truth table in determining its sub-formula's truth values (taking advantage of a parse tree method). A formula can be a __tautology__ if and only if whenever the premises is true and the conclusion is also true. An argument is valid if and only if its conditional analogue is a tautology. Basically, tautology describes the formal formulae, whereas validity describes arguments with premises and conclusion in a metamethmatics sense. 

#### 1.2 Proof Techniques 

To best illustrate the proof techniques we employ in formal logic, we can give one easy example to illustrate. Suppose that we havea finite conjunctions of literal where literal is either an atomic formula or the negation of an atomic formula. We want to show that if such conjunction is both a tauotology then there is sential letter C and not C that are in the conjunction. We want prove by __extracting__ the postive subformula or the goal. In other words, we assume there is a finite conjunction of literal such that it is tautological, and our current goal is to show that C and not C are in the conjuntion. We then apply __refutation__ technique to assume that C and not C are not in the conjunction. Since our conjunction of literals may or may not contain negated forms. Therefore, we construct our truth assignment function sigma such that we assign FALSE to all literal that do not contain negation and truth to the literal that do contain negated form. Hence, C or not C are both FALSE. Tracing up the sparse tree, we obtain FALSE at the root. Contradicting with our assumption that the formula is tautological. Therefore, by refutation, we conclude the claim to be true; thereby, ending our proof. 

### Predicate Logic

Claim: For all finite sets Γ of formulae and for all formulae T, T is a logical consequence of Γ if and only if there is no counterexample to Γ, T. (Γ is the set of premises T1, … , ψn of the argument with the conclusion T.)

Now, we are transiting to predicate logic. Predicate Logic extends the library from sentential logic to include constant (a, b, d ... t) and variables(u, v, w, x, y, z) and predicate letters (for n > 0, A^n, B^n) and sentential capitalized letters(A, B, ...). Therefore, predicate logic becomes more interesting. In addition, we introduced universal and extensial quantifiers. For the semantics part of the predicate logic, we rely on the interpretation to decide the truth value. I is the interpreation of a predicate logic formulae. It is like a truth function that takes a n-place predicate letters. For examle, L(x, y) can be interpreted as `<x, y>`. 

__Claim__: For all finite sets Γ of formulae and for all formulae T, T is a logical consequence of Γ if and only if there is no counterexample to Γ, T. (Γ is the set of premises T1, … , ψn of the argument with the conclusion T.)

__Proof__: We recognize that this requires us to discuss in the predicate logic's domain. Since we know there is no counter example to Γ (we cannot found an interpretation such that premises of Γ Ai to be true and B the conclusion of Γ to be false). Therefore, we conclude that whenever the premises of Γ Ai is true, B the conclusion is also true on interpretation. Hence, by definition, T is a logical consequence of Γ. Similarly, we can prove the other direction with respect to interpretation in the domain of predicate logic discussion. 

__Claim__:  For all formulae A and B, A is logically equivalent to B if and only if the biconditional (A <-> B) is a logical truth (tautology). 

__Proof__:  We won't go into details of this proof but the general strategy of solving it. First, different from the mathematcis we are used to, the point of the proof is to understand how to interpret biconditional and logical equivalence in term of predicate logic. The essential idea relies, again, in the definition of each terms with respect to interpretation. To say A is logically equivalent to B, we meant that `I(A) = I(B)`. Remember the proof is straight forward as long as we remember that the interpretation I is just a truth assignment function that either take on atomic letter or n-place tuples. 














