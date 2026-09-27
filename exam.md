30th & 5th

Quantitative Research – Take-Home Assessment

Pure Lambda Calculus · Research Questions

Duration: 24 hours · Difficulty: Hard · Focus: Untyped & Typed λ-Calculus, Semantics, Proofs



NOTICE: This is a fictional practice assessment created for educational purposes. “30th & 5th” is not a real firm. The problems are original research-style questions intended to approximate the depth expected in a demanding quant research take-home centered on the foundations of the λ-calculus.



Instructions

You have 24 hours from the moment you begin. Submit:





A written solutions document (Markdown or PDF) containing all proofs, constructions, and arguments.



Optional but encouraged: an accompanying OCaml (or Haskell) implementation of any algorithms, reduction machines, or type checkers you design. Code is secondary to mathematical insight.

Guidelines:





Prefer rigorous proofs over informal sketches. When citing standard theorems (Church-Rosser, strong normalization of STLC, etc.), state precisely what you are invoking and fill in the key inductive steps for your chosen syntax.



You may consult standard references (Barendregt, Hindley–Seldin, Pierce, Girard, etc.). All solutions must be your own work.



Partial solutions that demonstrate deep understanding are valued more than complete but superficial answers.



Clearly state any additional assumptions you introduce.



Problem 1 — Confluence, Standardization, and Böhm Trees

Consider the pure untyped λ-calculus with β-reduction.

(a) Church-Rosser via complete developments.
Sketch (or fully formalize) Takahashi’s proof of the Church-Rosser theorem using complete developments. In particular, define the parallel reduction relation ⇒ and prove that if M ⇒ N and M ⇒ P then there exists Q such that N ⇒ Q and P ⇒ Q. Show how this yields confluence of →β.

(b) Standardization theorem.
State the Standardization Theorem. Prove that every β-reduction sequence can be rearranged into a standard reduction sequence (leftmost-outermost). Explain why this implies that a term has a normal form if and only if the leftmost reduction strategy terminates on it.

(c) Böhm trees and solvability.
Define the Böhm tree of a term. Characterize the solvable terms in terms of their Böhm trees. Prove that a term is solvable if and only if it has a head normal form. Give an example of an unsolvable term whose Böhm tree is infinite (and non-trivial).

(d) Observational equivalence.
Define contextual (observational) equivalence ≅obs. Prove that two terms with identical Böhm trees are observationally equivalent. Is the converse true? Justify.



Problem 2 — Typed Calculi, Strong Normalization, and Inhabitation

(a) Simply-typed λ-calculus (STLC).
Prove strong normalization of STLC by the Tait–Girard method of reducibility candidates (or by the saturated sets method). Explicitly construct the interpretation of function types and verify the key closure properties.

(b) Type inhabitation.
Decide the following inhabitation problems in STLC (with a single base type o). For each, either give a closed inhabitant or prove none exists:





((A → B) → A) → A (Peirce)



(A → B) → ((B → C) → (A → C))



((A → A) → B) → B

Relate your answers to the distinction between intuitionistic and classical propositional logic via the Curry–Howard correspondence.

(c) System F.
Recall the polymorphic identity Λα. λx:α. x. Show that System F can encode Church numerals and that the predecessor function is definable (unlike in pure untyped λ-calculus under most reasonable encodings). Sketch why strong normalization still holds for System F (Girard’s candidates or an outline of the proof).

(d) Undecidability.
Prove that type inhabitation for System F is undecidable. (You may reduce from the halting problem or from semi-unification / second-order unification.)



Problem 3 — Models and Denotational Semantics

(a) Term model and open term model.
Construct the open term model of the untyped λ-calculus. Show that it validates β-equality but not η-equality in general. What additional quotient yields the η-model?

(b) Scott’s D∞ model (outline).
Describe the inverse-limit construction of Scott’s D∞ model. Explain why every element is the limit of its finite projections and how application is defined continuously. Why does this model contain a fixed-point combinator?

(c) Graph models / Plotkin’s Pω.
Sketch the construction of Plotkin’s graph model Pω. Show that it is a λ-model. Compare its theory (the set of equations it validates) with that of D∞.

(d) Full abstraction.
What does it mean for a model to be fully abstract with respect to observational equivalence? Is D∞ fully abstract for the pure untyped λ-calculus? Briefly discuss the status of full abstraction for PCF (Plotkin’s language) and the role of sequentiality.



Problem 4 — Advanced Topics & Research-Style Questions

Choose two of the following four topics and develop a substantial answer (proofs, constructions, or precise arguments). Depth is preferred over coverage.

(A) Intersection Types.
Present the intersection type system of Coppo–Dezani (or a modern variant). Prove that a term is strongly normalizing if and only if it is typable in the intersection type system (you may outline the harder direction). How does this refine the simple-type discipline?

(B) Linear λ-Calculus & Resource Awareness.
Define the linear λ-calculus (or a simple fragment of intuitionistic linear logic with !). Show how it controls resource usage. Give an example of a term that is typable in ordinary STLC but not in the linear system, and explain the computational significance.

(C) Parametricity.
State Reynolds’ Abstraction Theorem for System F (or a simplified version). Derive at least two free theorems (e.g., for the type ∀α. α → α and for ∀α. (α → α) → α → α). Discuss how parametricity constrains the behavior of polymorphic functions.

(D) Higher-Order Abstract Syntax & Binding.
Compare three approaches to representing binding structure: (i) de Bruijn indices, (ii) nominal sets / atoms, (iii) higher-order abstract syntax (HOAS). Discuss the advantages and disadvantages of each for metatheoretic reasoning (e.g., proving substitution lemmas or adequacy of encodings). Sketch how one would prove the substitution lemma in the nominal setting.



Problem 5 — Open-Ended Research Question

Formulate and partially answer one original research-style question that arises naturally from the preceding material. Examples of acceptable directions (you may invent your own):





Complexity of normalization for restricted classes of terms (e.g., terms of bounded order or terms typable with intersection types of bounded rank).



Relationships between Böhm-tree equivalence and other notions of observational equivalence in the presence of constants or non-deterministic choice.



Constructive content of classical proofs via λμ-calculus or continuations, and whether a particular classical principle has a “reasonable” computational interpretation.



Quantitative semantics (e.g., relational models, probabilistic λ-calculi) and how they refine classical models.

Your answer should contain:





A precise statement of the question.



Relevant background definitions.



At least one non-trivial partial result, construction, or counter-example.



A short discussion of why the question is interesting and what a complete solution might look like.



Evaluation Criteria





Mathematical rigor — correctness of definitions, proofs, and constructions.



Depth of understanding — ability to connect syntactic, semantic, and logical perspectives.



Clarity of exposition — precise language, well-structured arguments.



Originality — especially in Problem 4 choices and Problem 5.



Insight — recognition of subtle points, limitations of standard results, or interesting special cases.



— End of Assessment —

Good luck. Prefer depth over breadth.
