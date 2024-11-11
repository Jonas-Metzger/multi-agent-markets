# Multi-Agent Markets

How do you train multi-agent systems to pursue high-level goals?

Challenge: RL+back-propagation through time breaks down as the number of sequential/hierarchical steps increases.

Could the sequential steps be 'decoupled' via a market-based mechanism?

Intuition: allows optimising sub-parts of the problem holding the rest of the problem constant (gradients do that too).

