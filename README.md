## Formal Logic 

1. Sentential Logic 
2. Predicate Logic


### Sentential Logic

Formal Logic has two essential components: sentential logic and predicate logic. We will first examine sentential logic below. 

#### Syntax and Semantics 

To discuss the syntax of the formal logic, one must first understand the basic components that make up the formal logic. The most basic building block of any logical expression is called an __atom__. An atom that must be represented by capital letters can either take on __TRUE__ or __FALSE__. However, without __connectives__ (negation, &, ^, ->) and __symbols__( "(", ")", ",") these atoms cannot be formed into expressions. However, expressions are just finite sequence of atoms connected by the connectives. In order to have meaningful discussion of logic, a set of grammatic rules are required to form __formula__. The grammatic rules are recursively defined. Basically, a formula must take on several defined form: (F1 & F2), (F1 ^ F2), (F1 -> F2) or F1 is an atom (the base case). When we see a logical formula, we can break the formula down using a parse tree method where the leaf is the atomic truth variable and the branch are the connectives that glue these atoms together.  

The semantics of the formal logic focuses intensely on the truth value assignments. The most common way to investigate the truth value of a formula is to use a truth table in determining its sub-formula's truth values (taking advantage of a parse tree method). A formula can be a __tautology__ if and only if whenever the premises is true and the conclusion is also true. An argument is valid if and only if its conditional analogue is a tautology. Basically, tautology describes the formal formulae, whereas validity describes arguments with premises and conclusion in a metamethmatics sense. 
