# Sets
> _english notes by me from [L. Battaia - _"Matematica di base"_](https://github.com/farenheith27/ImScared/blob/f543d590f32e5e3ec875af4564e655ea22982fc2/StudyMaterials_PDF/Matematica%20di%20Base%20-%20L.%20Battaia.pdf)_
## 0 Notation
**N -> Natural Numbers Set**
- Starts from 1

**Z -> Whole Numbers Set**
- Include negative numbers and 0
- 0 is neither positive or negative

**Q -> Rational Numbers Set**
- Can be expressed as a fraction of integer numbers

**R -> Real Numbers Set**
- Include every rational and irrational numbers

**MORE: Irrational Numbers**
- Cannot be expressed as a fraction of integer numbers

## 1.1 Propositional Logic
> Examples <br>
> _"Snow is white"_ -> Universally TRUE <br>
> _"Earth is a star"_ -> Universally FALSE <br>
> _"Rome is a nice city"_ -> TRUE for some, FALSE for others <br>
> _"Tomorrow will rain"_ -> Cannot neither be TRUE nor FALSE <br>

Propositions can be:
- TRUE or FALSE
- TRUE and FALSE
- NOT TRUE or NOT FALSE

### 1.1.1 Definitions
Definition of PROPOSITION: 
1. Every statement who can be TRUE of FALSE
Definition of CONNECTIVE:
1. Words that unite more PROPOSITIONS
   > and
   > or
   > ...
3. Words that work on PROPOSITIONS
   > if then
   > not
   > ...

### 1.1.2 Connectives
> P = Proposition <br>

- **not**
  > P is FALSE, not P is TRUE 
- **et**
  > P is TRUE, D is TRUE, P et D is TRUE <br>
  > P is FALSE, D is TRUE, P et D is FALSE <br>
  > P is TRUE, D is FALSE, P et D is FALSE <br>
  > P is FALSE, D is FALSE, P et D is FALSE <br>
- **vel**
  > P is TRUE, D is TRUE, P vel D is TRUE <br>
  > P is FALSE, D is TRUE, P vel D is TRUE <br>
  > P is TRUE, D is FALSE, P vel D is TRUE <br>
  > P is FALSE, D is FALSE, P vel D is FALSE <br>
- **implies =>**
  > P is TRUE, D is TRUE, P => D is TRUE <br>
  > P is FALSE, D is TRUE, P => D is TRUE <br>
  > P is TRUE, D is FALSE, P => D is FALSE <br>
  > P is FALSE, D is FALSE, P => D is TRUE <br>
> [!note]
> Google Gemini helped me with that
> <br> It's easier to read **implicates** as an agreement between two sides
> <br>
> <br> _If condition P is satisfied, then I'll satisfy promise Q_
> <br>
> <br> The table can be written as:
> <br> _You did P, then I did Q - You did your job so I did mine - We both kept our promises - proposition is TRUE_
> <br> _You did P, then I didn't Q - You did your job but I didn't mine - I broke my promise while I had to kept it - proposition is FALSE_
> <br> _You didn't P, then I did Q - You didn't your job but I did mine - You broke your promise so I'm not obliged to keep mine but I did anyway - proposition is TRUE_
> <br> _You didn't P, then I did Q - You didn't your job so I didn't mine - You broke your promise so I'm not obliged to keep mine and I broke it too - proposition is TRUE_
> <br>
> <br> Basically, _if P is FALSE proposition is always TRUE_, _if P is TRUE Q must be TRUE_
- **if and only if <=> (aka "iff")**
  > P is TRUE, D is TRUE, P <=> D is TRUE <br>
  > P is FALSE, D is TRUE, P <=> D is FALSE <br>
  > P is TRUE, D is FALSE, P <=> D is FALSE <br>
  > P is FALSE, D is FALSE, P <=> D is TRUE <br>
> [!note]
> Google Gemini helped me with that
> <br> It's easier to read **if and only if** as "="
> <br> That's it, nothing more
> <br>
> <br> Basically, _P <=> Q_ can be read as _is true that P = Q?_

If we want to prove a theoreme, the _"implies"_ connective is very important. We can summarize the demonstration like:
> P is TRUE _(hypotheses)_
> Q is undefined _(theses)_
> P => Q is TRUE _(proof of theorem)_

It is possible to build more complex propositions by operating propositions with common math operators. Something like:
> \[(P et D) vel (P et not D)]

#### 1.1.2.1 De Morgan laws
1. not(P vel D) = (not P) et (not D)
2. not(P et D) = (not P) vel (not D)

## 1.2 Predicates
Logic is about determine if a proposition is TRUE or FALSE.

_x < 2_ cannot be a Proposition because _x_ is a variable.

Substituting _x_ with a value inside a Set of determinated values gives a Proposition.

That means _x < 2_ is a Dependent Proposition, with **x** as a Variable and **P(x)** as a Predicate.

> _x_ variable
> _P(x)_ predicate
> _x0_ specific value from a Set
> _P(x0)_ proposition

### 1.2.1 Quantifiers
Used in predicates operations
- **exist**
  > existential
- **for all**
  > universal
- **exist!**
  > there is one and only one

> [!important]
> When using more quantifiers, their order matters <br>
> <br>
> _P(x,y) = "x is a student who can solve y"_ <br>
> can be written as: <br>
> **for every** _y_ **exist** _x_ **such that** _P(x,y)_ <br>
> and reads: <br>
> _"Whatever the problem y is, there's a student x who can solve it"_ <br>
> <br>
> while: <br>
> **exist** _x_ **for every** _y_ **such that** _P(x,y)_ <br>
> reads: <br>
> _"There's a student x who can solve every problem y"_ <br>

> [!note]
> I used Google Gemini to understand better this piece, because my brain simply does not accept it as it is 
> <br>There's something like a skill issue here, I'm not capable of understand why this works like that
> <br>I was used to think at math expression as something readable in both direction, I'm learning that logic expression can be read only _"from right to left"_
> <br>
> <br> P(x,y) it's more like "what is y depend from what is x"
> <br> I'll try to expand the sentence to better understand it when reading again this madness
> <br>
> <br> 1. We can choose whatever problem from Y, and we'll ever find a studend from X who is capable to solve it. The choosen student can vary depending on which Y we choose, but we'll ever be capable of finding one X
> <br>
> <br> 2. We choose whatever student from X. The choosen student can solve 1 problem, maybe another student can solve 2, another one can solve more. But there's **at least one** mf who goes "hold my beer" and solve every damn problem we have in Y

#### De Morgan laws for quantifiers
With quantifiers, **exist** and **for every** can be intended as negation of the other<br>
I'll write down an example for myself then ask Gemini because my brain already hurts too much:
- not(**exist** x **such that** P(x)) = **for all** x **such that** not P(x)
- not(**for all** x **such that** P(x)) = **exist** x **such that** not P(x)
> Apparently was just bad written on my math book, nothing esotheric there

## 1.2 Other basic symbols
- **summation**
  > _i_ is called **index** (it can be written with different letters ofc)
  > <br> _a(i)_ is the **expression**
  > <br> The range is defined by _i=m_ **bottom limit** and _n_ **upper limit**
  > <br> _m_, _n_ and _i_ are **natural numbers**
  > <br> Whole numbers can be expressed with _-i_
  > <br> It's nonsense to sum rational or real numbers between _m_ and _n_ because they're infinite
  > <br> **Sum of every copy of _a(i)_, while _i_ vary from _m_ to _n_**
- **product notation** (or **Pi notation**)
  > _i_ is called **index** (it can be written with different letters ofc)
  > <br> _a(i)_ is the **expression**
  > <br> The range is defined by _i=m_ **bottom limit** and _n_ **upper limit**
  > <br> _m_, _n_ and _i_ are **natural numbers**
  > <br> Whole numbers can be expressed with _-i_
  > <br> It's nonsense to multiplicate rational or real numbers between _m_ and _n_ because they're infinite
  > <br> **Multiplication of every copy of _a(i)_, while _i_ vary from _m_ to _n_**

## 1.4 Axiom, Theorems _(Th.)_, Proofs
We'll go with basic understanding of what they mean <br>
### Primitives - Undefined terms
Words that cannot be defined without other words, because they're meaning have no explication outside a vicious circle of words
> <br> **Example** _(translated from a research on an Italian Dictionary)_
> <br> **Point**: primitive element of geometry, with no _dimensions_
> <br> **Dimension*+: relative _extent_ of something
> <br> **Extent**: _space_, surface
> <br> **Space**: _extent_ of...

We have to take them as they are, so the name.
### Axioms
Propositions which are _introducted without demonstration_, related to properties of Primitives. <br>
They're useful to comprehend what exactly the Primitives are. <br>
Its important to verify that different Axioms does not go in conflict between eachother.

### Th.
Propositions which are _deducted by demonstrations_ from Axioms or other Theorems. <br>
They're defined by logical implication as we've already seen: _P => Q_ <br>
In Th. there are:
- **Statement:** the proposition we have to demonstrate
  - **Hypotheses:** starting point
  - **Theses:** ending point to be demonstrated
- **Proof:** all the reasoning and logic deductions, related on axioms or other theorems, we use to get from hypotheses to theses
  - It's important to note that proofs **must be** replicable at the same conditions
 
### Necessary conditions _(nc)_, Sufficient conditions _(sc)_, Necessary and Sufficient conditions _(nsc)_
- **Necessary**
  > A is nc for B
  > <br>
  > <br> If B is TRUE, A must be TRUE
  > <br> If A is FALSE, B must be FALSE
  > <br> _B => A_
- **Sufficient**
  > A is sc for B
  > <br>
  > <br> If A is TRUE, B must be TRUE
  > <br> If B is FALSE, A must be FALSE
  > <br> _A => B_
- **Necessary and Sufficient**
  > A is nsc for B
  > <br>
  > <br> If B is TRUE, A must be TRUE
  > <br> If A is FALSE, B must be FALSE
  > <br> _A <=> B_

### Proof by contradiction
In our logic, theses can only be TRUE or FALSE, so if it is not FALSE then it must be TRUE. <br>
In proofs by contradiction, we take the theses as FALSE and we go backwards until we get _FALSE thesis = TRUE hypotheses_. <br>
This result in a contradiction, that can be read as: _theses must be TRUE because for certain it's not FALSE_.

### Lemmas
Some proofs are so complex they require an high number of intermediate logical implication. <br>
**Lemmas** are subsidiary theorems used to proof a bigger theorem.

### Corollary
Th. immediatly demonstrated by the proof of another th., can be more important than the first th. proved.

### Definitions _(Def.)_
Used to introduce new concepts after the Primitives, by explaining it with known words. <br>
They're different from Primitives because they use Primitives or proved Th. to define the concept, while Primitives are taken as they are without defining them more. <br>
That's a simplification of the term.

## 1.5 Sets
