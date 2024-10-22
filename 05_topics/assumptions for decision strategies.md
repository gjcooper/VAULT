# Assumptions for Decision Strategies

## Ordered by SFT paper categorisation

| Name                                                     | SFT[^4]  | Attrs          | Screening | Pairwise | Aspiration | Accept     | Reject     |
| -------------------------------------------------------- | -------- | -------------- | --------- | -------- | ---------- | ---------- | ---------- |
| [[Equal Weight Heuristic\|EQW]]                          | Co       | Integrated     | No[^1]    | No       | No[^3]     |            |            |
| [[Weighted Additive Rule\|WADD]]                         | Co       | Integrated     | No[^1]    | No       | No[^3]     |            |            |
| [[Additive Difference Strategy\|ADD]]                    | Co       | Integrated     | No        | Yes      | No         |            |            |
| [[Majority of Confirming Dimensions Heuristic\|MCD]]     | Co       | Integrated[^2] | No        | Yes      | No         |            |            |
| [[Frequency of Good and-or Bad Features Heuristic\|FRQ]] | Co       | Integrated     | No[^1]    | No       | Yes        |            |            |
| [[Compatibility Test\|COM]]                              | ST (S/P) | Independant    | Yes       | No       | Yes        | EITHER[^5] | EITHER[^5] |
| [[Conjunctive Strategy\|CONJ]]                           | ST (S/P) | Independant    | Yes       | No       | Yes        | AND        | OR         |
| [[Satisficing Heuristic\|SAT]]                           | ST (S/P) | Independant    | Partial   | No       | Yes        | AND        | OR         |
| [[Satisficing-plus Heuristic\|SAT+]]                     | ST (S/P) | Independant    | Partial   | No       | Yes        | OR         | OR         |
| [[Disjunctive Strategy\|DIS]]                            | Ex (S/P) | Independant    | Yes       | No       | Yes        | OR         | AND        |
| [[Dominance strategy\|DOM]]                              | Ex (S/P) | Independant    | No        | No       | No         | AND[^6]    | AND[^6]    |
| [[Simple Majority Decision rule\|MAJ]]                   | Ex (S/P) | Independant    | No        | No       | No         | OR[^6]     | OR[^6]     |
| [[Elimination by Aspect Strategy\|EBA]]                  | ST (S)   | Independant    | Yes       | No       | Yes        | AND[^7]    | OR         |
| [[Lexicographic Heuristic\|LEX]]                         | ST (S)   | Independant    | Yes       | No       | No         | OR[^8]     | OR[^8]     |
| [[Minimum Difference Lexicographic Rule\|MDLR]]          | ST (S)   | Independant    | Yes       | No       | No         | OR[^9]     | OR[^9]     |

## Ordered by Pfeiffer book Appendix A table order

| Name                                                     | SFT[^4]  | Attrs          | Screening | Pairwise | Aspiration | Accept     | Reject     |
| -------------------------------------------------------- | -------- | -------------- | --------- | -------- | ---------- | ---------- | ---------- |
| [[Additive Difference Strategy\|ADD]]                    | Co       | Integrated     | No        | Yes      | No         |            |            |
| [[Compatibility Test\|COM]]                              | ST (S/P) | Independant    | Yes       | No       | Yes        | EITHER[^5] | EITHER[^5] |
| [[Conjunctive Strategy\|CONJ]]                           | ST (S/P) | Independant    | Yes       | No       | Yes        | AND        | OR         |
| [[Disjunctive Strategy\|DIS]]                            | Ex (S/P) | Independant    | Yes       | No       | Yes        | OR         | AND        |
| [[Dominance strategy\|DOM]]                              | Ex (S/P) | Independant    | No        | No       | No         | AND[^6]    | AND[^6]    |
| [[Elimination by Aspect Strategy\|EBA]]                  | ST (S)   | Independant    | Yes       | No       | Yes        | AND[^7]    | OR         |
| [[Equal Weight Heuristic\|EQW]]                          | Co       | Integrated     | No[^1]    | No       | No[^3]     |            |            |
| [[Frequency of Good and-or Bad Features Heuristic\|FRQ]] | Co       | Integrated     | No[^1]    | No       | Yes        |            |            |
| [[Simple Majority Decision rule\|MAJ]]                   | Ex (S/P) | Independant    | No        | No       | No         | OR[^6]     | OR[^6]     |
| [[Majority of Confirming Dimensions Heuristic\|MCD]]     | Co       | Integrated[^2] | No        | Yes      | No         |            |            |
| [[Minimum Difference Lexicographic Rule\|MDLR]]          | ST (S)   | Independant    | Yes *     | No       | No         | OR[^9]     | OR[^9]     |
| [[Lexicographic Heuristic\|LEX]]                         | ST (S)   | Independant    | Yes *     | No       | No         | OR[^8]     | OR[^8]     |
| [[Satisficing Heuristic\|SAT]]                           | ST (S/P) | Independant    | Partial   | No       | Yes        | AND        | OR         |
| [[Satisficing-plus Heuristic\|SAT+]]                     | ST (S/P) | Independant    | Partial   | No       | Yes        | OR         | OR         |
| [[Weighted Additive Rule\|WADD]]                         | Co       | Integrated     | No[^1]    | No       | No[^3]     |            |            |

_There are some noteable differences between Pfeiffer's work and mine, these are marked with as asterisk (*)_

## Notes

[^1]: Not traditionally thought of as screening, but if paired with no-choice options could be reconsidered to be such
[^2]: The integration here is much simpler, rather than some kind of weighted sum, or utility difference (such as in [[Additive Difference Strategy|ADD]]), the difference between two alternatives in each pairwise comparison is the difference in the number of "winning" attributes.
[^3]: These utility based methods do not traditionally consider an aspiration level, however with the introduction of a "No Choice" option in a more traditional choice task you could consider as aspiration level like the amount of utility needed to move away from the default of no choice.
[^4]: Co = Coactive, ST = Self-terminating, S/P = Serial or Parallel, Ex = Exhaustive
[^5]: Depending on the choice of $k$ for the model this could veer closer to or further away from the AND/OR to OR/AND combination rules of the [[Conjunctive Strategy|CONJ]] and [[Disjunctive Strategy|DIS]] heuristics
[^6]: All attribute levels need to be assessed, however the raw levels are compared directly.
[^7]: If only one option is left after screening (via rejection) then not all attributes have to be processed.
[^8]: Weight attributes by importance, work on attribute levels directly. If multiple options remain after looking at attribute N, move to attribute N+1
[^9]: The same as above [^8] however there is a threshold of minimum useful difference. That is if an attribute such as price for one option is $100 and another option is $101, the difference is too small to have an influence on the final choice.