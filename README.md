## Formal Logic 

1. Sentential Logic
2. Predicate Logic
3. A Glimpse of Elementary Theory of Numbers
4. Set Theory Functions


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

###  A Glimpse of Elementary Theory of Numbers

__Theorem__: Every number greater than 1 can be written as the product of powers of distinct primes. Assume for contradiction that there exists a least number x0 that cannot be represented in that form. If x0 is prime, we reach contradiction immediately. If x0 is not a prime, then there exists a prime number smaller than x0 such that x0 = pr. Since x0 is the least such non-representation, r can be represented, with product of pr, we know that x0 can be represented in such form, which contradicts with our orginal assumption. 

However, our goal is to prove the uniqueness of prime factorization. Therefore, we can assume that a natural number can be represented in two different ways. If we order the product of primes in increasing order then we know if pi divides qi, then pi = qi by corollary 9. Therefore, we know the base must all be equal. Now, if we can show the exponents are also equal we are done. We can do so by assume they are not equal, then we can divide both sides to reduce the exponents term to a smaller value. However, then for that pi, it exists on one side but not the other. Therefore, we shows a prime that divides one side of an equality but not the other. This cannot happen and hence we derived a contradiction, which allowing us to conclude the claim. 

### Set Theory Functions 

1. theorem 2.2: for any given sets a, b, c, d. If order pair [a, b] = [c, d] then a = c and b = d. 
2. lemma 2.4: given sets a and b, there is a set y of all and only those ordered pairs having their first elemet in a and their second element in b. 

We introduced the concept of ordered pairs because they allow us to define cartesian products using sets. The first lemma tell us that if two sets are equal, the elements inside are equal. If two sets of different size are equal, then the larger once must be able to reduce to a smaller set. Therefore, there are similar elements in the sets, and if two sets of size 2 share the same element, the other one must also be the same. Theorem states that if two ordered pairs are equal than the elements are equal correspondingly. The proof follows the definition of ordered pairs. `<a, b> := {x in <a, b> <-> x = {a}  or x = {a, b}}`. The trick relis on taking an instance of x which is {a}. Then the left handside becomes easy to prove to be TRUE. THen we have `{a} in {{c}. {c, d}}`. Then we know `{a}` must be either of the two. If its the first element, than we know a is c, otherwise we can use the second compoenent of the lemma to reduce the size and conclude that a = c in either case. Therefore, a is always c. As for proving b = d, we can use the third compoenent of the lemma to achieve our goal. Hence, we have showed the uniqueness of ordered pairs. 

Before introducting the definition of Cartesian product, we first show that its exists. That is given sets a and b, there is a set y of all and only those ordered pairs having their first elemet in a and their second element in b. The proof of this invokes the definition of power-sets. We basically shows that z1 and z2 are elements of the powerset. By showing so, the proof follows immediately. Becasuse z1 is an element of a to begin with and z2 is also an element of b to begin with. 

`Cartesian Product: (\all x)(x \in axb <-> (\exists y \in a)(\exists z \in b)(x = <y, z>)`

n-tuples can easily be represented by ordered pairs. In addition, a total relation is simply one that everything int he domain is mapped to some value in the codomain, and singled value states that every x is mapped to a unique y. Partial ordering is reflexive, antisymmetric and transitive. Notice here antisymmetric implies that if f(x) = y and f(y) = x, then x = y. The classic example is subset: if x subset y and y subset x then x equals to y. 

Then, we proved that subset is a partial ordering set. The proof follows from the basic property of set theory with the only difference being that we invoke the domain to be the P(a). To grow a partially ordering set into an ordering set, we just need to show that the partial ordering set is linear, which means that all x and y in a, either r(x, y) or r(y, x). For example, on natural number, >= is a linear relation since every number is either >=  or <=. 

Partition is the next big topic in the set theory. A partition of a set a is a subset of P(a) such that (U pi = a) for all x, y in pi. Partition and Equivalence Class is intricate relationship with one another. Therefore, we divide our attention to proving the equality of the two.

`Claim: Let a be a set and r be an equivalence relation on a. Then the set of r-equivalence class Pr = {[x]r | x in a } is a partition of a.`

The proof the this relies on the know clearly what the definition of a partition is. We need to prove two things. First, we need to show that Union of pi on r equals to a. In addition, if two equivalence classes are not equal then their shared set is empty. To show the first part, since we know that U pi subsets a which is given. Hence, all we need to show is that a susbsets U pi. Let x in a, we show x in U pi because r(x,x) since equivalence relation. Therefore, we are done with the first part. Next, we show the contrapositive is true. Namely, we show that if their joined set is not empty, then they must be equal. We use properties of r (equivalence relations) to demonstrate that x subsets y and similarly y subsets x. Hence [x] = [y]. 
















