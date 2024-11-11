# Multi-Agent Markets

How do you train multi-agent systems to pursue high-level goals?

Challenge: RL+back-propagation through time breaks down as the number of sequential/hierarchical steps increases.

Could the sequential steps be 'decoupled' via a market-based mechanism?

Intuition: allows optimising sub-parts of the problem holding the rest of the problem constant (gradients do that too).

Question: What is the formal relationship between prices and gradients? How do you achieve organic 'decoupling'?

Random Ideas:

- `competition' may yield more informative gradients than RL -- discrete choice vs reward-weighted policy gradients
- training separate weights vs training separate prompts seems to be different ways of doing it. But promps can be viewed as parameters after all.


Towards a formalism:

- define an end-user as a tool-using/subagent-using LLM, but that LLM has to `pay' for each subagent-use, which is charged in proportion to the number of tokens generated to produce the result
- do some form of discrete search over search procedures (akin to [Archon](https://arxiv.org/abs/2409.15254)) for the `tools' or sub-routines
- the tool-using super-agent can decide between delegation and self-generation, but the RL objective is risk-aware that self-generation may be less optimal

What are the right benchmarks to tackle?
- does any exist that could benefit from it?
- how does openAI swarm work? What is it tested on?
