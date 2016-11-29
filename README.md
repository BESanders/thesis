# Liquid Haskell: Haskell as a Theorem Prover
## Thesis by Niki Vazou (December, 2016)



Code deficiencies and bugs constitute an unavoidable part of software systems.
In safety-critical systems, like aircrafts or medical equipment, 
even a single bug can lead to catastrophic impacts
such as injuries or death.
Formal verification can be used to statically 
track code deficiencies by proving or disproving correctness properties 
of a system. 
However, at its current state formal verification is a cumbersome process
that is rarely used by mainstream developers, mostly because it targets non general purpose languages (e.g., Coq, Agda, Dafny).

We present Liquid Haskell, a _usable_ program verifier that aims to
establish formal verification as an integral part of the development process.
Liquid Haskell _naturally integrates_
the specification of correctness properties
as logical refinements of Haskell's types. 
Moreover, it uses the abstract interpretation framework of liquid types
to _automatically_ check correctness of specifications via SMT solvers
requiring no explicit proofs or complicated annotations.
Finally, the specification language is arbitrary _expressive_,
allowing the user to write general correctness properties about their code, 
thus turning Haskell into a theorem prover. 

Transforming a mature language 
--- with optimized libraries and highly tuned parallelism ---
into a theorem prover enables us to verify a wide variety of properties 
on real world applications.
We used Liquid Haskell to verify shallow invariants of existing Haskell code, 
e.g. memory safety of the optimized string manipulation library `ByteString`.
Moreover, we checked deep, sophisticated properties of parallel Haskell code, 
e.g. program equivalence of a naïve string matcher and its parallelized version. 
Having verified about 20K of Haskell code, we present how Liquid Haskell
serves as a prototype verifier in a future where formal techniques will 
be used to facilitate, instead of hinder, software development. 
