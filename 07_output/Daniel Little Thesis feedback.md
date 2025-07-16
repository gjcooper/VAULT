# Report 1

Evaluation of Gavin Cooper’s PhD [[Thesis]]: _Cognitive models of decision strategies in consumer preference_
Let me start by applauding the candidate for producing a high quality thesis that clearly meets all of the requirements of the PhD. The work contained herein is advanced and examines the question of consumer decision strategies from three perspectives: non-parametric analysis, parametric model, and psychological representations.
The thesis demonstrates a detailed and expert understanding of the three primary areas of focus. This is no small achievement given the wealth of technical development in each of these areas along with the advanced state of the decision making field. A real highlight of the thesis is the deconstruction of various decision strategies into their component properties. This is an important contribution of the thesis and aids in both Chapter 2 and Chapter 3 in using the relevant properties of the strategy to identify that strategy in data.
Chapter 2 is published and has been peer-reviewed. I don't have much to add here except to point out that this is a highly novel and interesting application of Systems Factorial Technology. It forms an important extension of that methodology to the consumer decision making case.
Chapter 3 explores how well decision strategies can be identified from data. Again, the overview of decision strategies, how they operate in terms of processing and accept/reject decisions, and the mapping of decision processes onto decision classes is important and useful. I liked the way that the choice task simulates the models with people and then tests how well the model can recover the strategy. The simulation with mixed strategies showing an accurate recovery of strategy is really nice (Fig 3.6).
Chapter 4 examined how well a model of distance (varying both attribute weights and underlying distance metric) could capture consumer decisions in unary and binary tasks. The objectives are clearly stated and defined. The experimental investigations are thorough and compelling.
Overall, I would be happy to see this thesis passed without any further changes. I have first listed some very minor typos that can be fixed up prior to submission of the final thesis. Below that I have listed some thoughts that might help with further development of this work.

## Small typos for amending:

- [x] p. 64 "asses" --> "assess"
- [x] p. 68 "ana" --> "an"
- [x] p. 94 "There are three notable difference" --> "differences"
- [x] p. 96 "r = 1" --> Should be r = 2 here.

## Comments:
- [ ] p. 63 - This section sets out a rationale for using parametric models instead of SFT. There are a set of limitations that are provided, which are undoubtedly true, but I think we now have a little more information that permits additional nuance. (You don't need to change anything here, this is just for your information).
    - For one, the SFT predictions as they pertain to error responses have been extended for both the SIC (Little et al., 2022) and Capacity (Townsend & Altieri, 2012). The SIC work is probably the most relevant demonstrating that the use of the AND task SIC is unaffected by any level of error provided that stochastic dominance holds. (The OR task is more complex).\
    - Second, certainly there is some benefit to fitting a parametric model because it fits both correct and error RTs simultaneously, but that depends on the relationship between correct and error RTs. For instance, some RT models cannot predict slow errors - but are fine if error RTs equal correct RTs. (I realise that the general preference and tendency is to use a full model which can predict fast and slow errors but there are additional complications - e.g., variable non-decision time that are typically ignored when depending on the leading edge of the distribution).\
    - Third, SFT does depend on meeting some assumptions regarding stochastic dominance, but those are really an expression of how well the experiment worked to manipulate RT. Yes, you can apply a parametric model when stochastic dominance failed but really it's a failure of the experiment, not the analysis. So applying a parametric model to an experiment where stochastic dominance doesn't hold might not yield very good inferences either. Garbage in, garbage out as the saying goes.
- [x] p. 91 - I didn't get a good sense of what abstract and concrete mindset meant in this context. It would be useful to define these terms with examples early on in this chapter.
- [ ] p. 95 - The relationship between 4.1C and the Minkowski metric is a little opaque to me because the curvature in the graph depends on some reference point (presumably the origin in the graph - but it isn't clear why the origin is the reference point until the experiment is introduced later. For example, in categorisation models, the reference is the item you're trying to categorise). Another way to conceptualise the curvature is that from a given reference, you can construct an isosimilarity contour (i.e., at which distances are other stimuli perceived as equally similar to the reference). This is diamond shape for city block distance and circular for Euclidean (see Shepard, 1961).
- [ ] p. 95 - "Most applications of the Minkowski distance as applied in categorisation have fixed the r-value at either 1 or 2 depending on the assumed independence of the features (Reed,1972; Nosofsky,1986; Smith,2014)."

    > The reason for this is because distance metrics have been found to provide good approximations to similarity data from separable and integral dimensions; other metrics (e.g., r > 2 dominance metrics) have also been explored.

- [x] p. 96 - "Simple two way interactions between options correspond...to a Euclidean metric."

    > I don't follow how this is the case. If participants perceive a compound cue representing an interaction between attributes, then distance could still be city-block.


## Minor Comments:
- [x] p. 6 - "the most efficient way of searching would be in an attribute-wise fashion"...

    > "efficient" with respect to what optimising goal? (The same question arises at the top of page 7).

- [x] p. 17 - "...it is silent about the processes consumers use to gather and integrate the information into their choices beyond assuming the choice is a sum of component utilities."

    > this is perhaps too strong as clearly some DCE's can be constructed which do provide info about the process
- [ ] p. 18 - "also leads to selecting attribute levels that may not represent levels seen in “real life”, reducing ecological validity."

    > Does this suggest that in many "real-life" choices the specific underlying model doesn't matter but the class of models might?

- [ ] p. 19 - "The participant is then generally instructed to reveal the required information by using the computer mouse to either click on or hover over each piece of information."

    > This inserts a search process into the decision making process - but arguably the search process is already present

- [x] p. 19 - "In real-life settings, the presented information is rarely obscured and revealed one attribute level at a time."

    > Really? If I want information about a supermarket item, aside from the name and price, I have to pick it up and examine it

- [ ] p. 20 - "One alternative to these methods that either obscure information ([[Mouselab]]) or require participants to request information specifically ([[Active Information Search]]) could be to present choices arrange in a DCE display without restrictions"

    > This is just an alternative type of display, present sometimes in the real world (e.g., on a website) but often not since only so many items can fit on one page).

- [x] p. 20 - "...offer an improvement over Mouselab and Active Information"

    > I don't think it's an improvement; it's just different

- [x] p. 20 - "Eye tracking is the closest external measure we have for determining the underlying processing of attribute information, with the most ecological validity for tapping into the decision process. "

    > I disagree. It is a measure like any other that has certain contexts in which it is more or less applicable. In an eye-tracking experiments, items and attributes, for instance, can't be overlapped as they often are in real life.

- [ ] p. 65 - "...competing options will share attributes such as price and quality but differ in the levels associated with each attribute."

    > There's another issue which is that options are often presented with non-comparable features. E.g., one hotel might provide you a nightly rate another might provide you with a weekly rate, a third might provide a nightly rate based on the use of some loyalty card which provide additional

- [x] p. 92 - What is a preference for large assortment sizes? What's the context?
- [x] p. 93 - "One early concept of a psychological space is understanding similarity judgements."

    > I don't follow what this means

- [x] p. 93 - "...techniques of multidimensional scaling"

    > There are more primary references that should likely form the basis of the citations here.