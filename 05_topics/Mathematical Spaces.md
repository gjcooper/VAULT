This second chapter of [[Michael Betancourt]]'s book on [[Probability]] extends the initial terminology of finite sets into more general mathematical spaces. That is countably and uncountably infinite sets.

With this introduction of mathematical spaces, the same terminology of sets applies, but now these set become more practical with the introduction of **structure** on the set or space.

These structures can be grouped into the follow categories:
- Ordering structures.
    - A _strict_ (or _complete_ or _total_) ordering defines a strict sequential arrangement on the set (such that $x_1 < x_2$ and $x_2 < x_3$ then $x_1 < x_3$). This ordering operation is **transitive**.
    - A _partial_ ordering defines a less strict ordering where two distinct elements can occupy the same place in the order. That is we have an operation $\leq$ defined.
- Algebraic structures.
    - A single (generic) binary operator $\cdot$ defined on the space can be:
        - **commutative** $\rightarrow$ $x_1 \cdot x_2 = x_2 \cdot x_1$
        - **associative** $\rightarrow$ $(x_1 \cdot x_2) \cdot x_3 = x_1 \cdot (x_2 \cdot x_3)$
        - **unital** $\rightarrow$ there is a _unit element_ (or _identity element_) $x_{Id}$ such that $x \cdot x_{Id} = x_{Id} \cdot x = x$
        - There may also be a $x_{Null}$ defined that leads to $x \cdot x_{Null} = x_{Null} \cdot x = x_{Null}$. This **null element** (_absorbing_ or _zero_ element)
    -  The _addition_ $+$ and _multiplication_ operations are two commonly defined operations on mathematical spaces, however they do no necessarily follow their conventional properties.
    - An _arithmetic_ is an algebraic structure with a binary operation that _distributes_ over another, as in $x_3 \cdot (x_1 + x_2) = (x_3 \cdot x_1) + (x_3 \cdot x_2)$
    - A _linear algebra_ has a _scalar multiplication_ operator that takes one input element from the space and a real number $\alpha$ that distributes over a associative, commutative, and unital binary operator ($+$). A set with these operators is also known as a vector space (with elements from the set termed **vectors**)
- Metric structures introduce a notion of **distance** between individual elements. A distance metric should be $\gt 0$ for all distinct elements, should satisfy the _triangle inequality_ and a set with such a distance function defined is known as a **metric space**
- Topological structures allow us to think about mathematical spaces in another way. My understanding is more limited here, but we can think of **open balls** (all elements with a certain distance of an element $x$) a **boundary** (all elements exactly a certain distance $r$ from another element $x$) and a closed ball (The union of the open ball and it's boundary for $r$). Topological structures only get more confusing from here with open and closed sets and **topologies** (a collection of subsets that contains the empty set, the full set and is closed under arbitrary unions and finite intersections). A set with a defined topology is known as a topological space.

## Prototypical spaces

Some mathematical spaces are so useful, and part of that usefulness comes from the abundance of structures they are imbued with. Several such are:
- Power sets have partial ordering via inclusion, union and intersection operators add boolean algebraic structure and more
- The integers are the prototypical discrete space.
- The real line is the prototypical continuous space

# Defined relationships on spaces

A **function** is a mapping between and input set and an output set. If $f(x_1) = f(x_2) \iff x_1 = x_2$ then $f$ is **injective**. Non-injective functions are known as _many-to-one_ functions. If every element of $Y$ is the output of evaluating $f$ on some input value from $X$ they $f$ is **surjective** and if $f$ is injective and surjective it is known as **bijective**.

If we have a bijective function with means we can define an **inverse function** $f^{-1}$ that maps the output from $f(x)$ back to $x$.

The way a function acts on the structure within a set is a separate consideration, and terms such as _pushforward_ and _pullback_ relate to the ways a function effects a structure. This can lead to _structure-preserving transformations_ and in the special case of a structure-preserving transformation on a bijection we get an **isomorphism**.

Additionaly if a transformation preserves the order on the elements of a set then that are _monotonically increasing  functions_..

Algebra preserving functions are **homomorphisms**, metric preserving functions are **isometries** and topology preserving functions are **homeomorphisms**.