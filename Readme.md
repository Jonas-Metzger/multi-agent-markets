# Multi-Agent Markets

How do you train multi-agent systems to pursue high-level goals?

Challenge: RL+back-propagation through time breaks down as the number of sequential/hierarchical steps increases.

Could the sequential steps be 'decoupled' via a market-based mechanism?

Intuition: allows optimising sub-parts of the problem holding the rest of the problem constant (gradients do that too).

Question: What is the formal relationship between prices and gradients? How do you achieve organic 'decoupling'?

Random Ideas:

- `competition' may yield more informative gradients than RL -- discrete choice vs reward-weighted policy gradients
- training separate weights vs training separate prompts seems to be different ways of doing it. But promps can be viewed as parameters after all.


