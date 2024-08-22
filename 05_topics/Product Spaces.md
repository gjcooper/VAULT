# Product Spaces

From Chapter [three](https://betanalpha.github.io/assets/chapters_html/product_spaces.html)

## Product Sets

A product set $X_1 \times X_2$ is the set of all possible combinations of elements from sets $X_1$ and $X_2$. This is easily generalisable to non-finite sets, as well as to product between more than 2 sets. An ordered collection of component variables $x = (x_1, ..., x_i, ..., x_I)$ is often known as an **n-tuple** and the product set can sometimes be known as a **multivariate** set as the individual elements are specified by multiple variables. _Product subsets_ can be specified as the product of subsets of the component sets, although most set operations are not compatible with the component structure of a product set. One except is the intersection of product subsets, which can always be derived from the intersection of the component subsets (sometimes called _rectangular subsets_). Additionally it is important to note that _most_ subsets of a product set are **not** product subsets

## Product structure

Strict ordering of component sets typically leads to ambiguous ordering or partial ordering on the product set. For product algebras, an operation on the product set can be defined if each component set has that operation. What's more if each component set operation has the same property (i.e. is commutative for example) then the matching operation on the product set will also have that property (will also be commutative). Product metrics also inherit the properties of the metrics from the component sets. Product topologies don't follow this same pattern though, as some topologies, specifically for the case of unions of open product subsets.

## Prototypical product spaces

Most are made up of combinations of the prototypical spaces from [[Mathematical Spaces]], however there are a couple of note. A _replicated product space_ is formed by usinfg multiple copies of the same space together, although notation can be difficult, so when explictly using one it is best to be precise when introducing it. **Multivariate Real Numbers** are a replicarted product space over the real number line and are used a lot.

## Decomposing product spaces

Dealing with every element at once from a product space can be overwhelming, so sometime we may want to decompose them. The intuition here to say for $\mathbb{R}^2$ is to take a value on one axis and then extend it across the other (think of a line from the plane). Similarly for $\mathbb{R}^3$ we could think of a plane from the volume.

## Transforming product spaces

Although a transformation can be applied to the product space as a whole, it can be more interesting to look at transformations that harmonise with the compoenent sets making up a product space. For instance, component-preserving functions transform each component independently of the others. A component-preseving map will transform a rectangular grid into a rectangular grid, whereas a map that is not component preserving will rotate, skew or warp the grid.
Projection functions are the functional equivalent to the useful interpretation of product spaces introduced in the Decomposing product spaces section. That is they map an element from the product space down into a marginal subset (one or more component sets).
Partial evaluation is the definition of a new function based on the evaluation of a full function (that operates on the fully specified element from a product space) upon a element with a missing component. Think of this like partial functions in computer programming.