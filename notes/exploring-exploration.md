```markdown
Exploring Exploration
```

| Title    | Exploring Exploration: Comparing Children with RL Agents in Unified Environments |
| -------- | ------------------------------------------------------------ |
| Authors  | [Eliza Kosoy](https://arxiv.org/search/cs?searchtype=author&query=Kosoy%2C+E), [Jasmine Collins](https://arxiv.org/search/cs?searchtype=author&query=Collins%2C+J), [David M. Chan](https://arxiv.org/search/cs?searchtype=author&query=Chan%2C+D+M), [Sandy Huang](https://arxiv.org/search/cs?searchtype=author&query=Huang%2C+S), [Deepak Pathak](https://arxiv.org/search/cs?searchtype=author&query=Pathak%2C+D), [Pulkit Agrawal](https://arxiv.org/search/cs?searchtype=author&query=Agrawal%2C+P), [John Canny](https://arxiv.org/search/cs?searchtype=author&query=Canny%2C+J), [Alison Gopnik](https://arxiv.org/search/cs?searchtype=author&query=Gopnik%2C+A), [Jessica B. Hamrick](https://arxiv.org/search/cs?searchtype=author&query=Hamrick%2C+J+B) |
| Link     | https://arxiv.org/abs/2005.02880                             |
| Keywords | exploration, cognition                                       |



Exploration is a key challenge in artificial intelligence. This paper argues for using children as a baseline to compare exploration of RL agents. They propose the usage of DeepMind Lab for this. 

## Experiment 1

This is a navigational task on a maze like environment. It is divided into three phases - no goal, goal, and goal with shortest path blocked.

- In the no-goal setting, they find that the behaviour of children can be clustered into low explorers, medium explorers and high explorers.
- In the goal setting, they find that the high explorers took the least time to find the goal. Further they find that the behaviour of the children in consistent with an agent that uses DFS. 
  - Consistency : Analysis is restricted to decision points - cells that don't have two neighbouring cells (dead-ends?)
- They don't find any correlation between explorer type and steps taken to reach the goal in the third phase.
- Questions that are not clear:
  - They claim that having a more complete mental model helps in efficient DFS. How does having a complete mental model improve DFS?
  - While they cluster the behaviour using K-Means, they don't provide any graphs or data to indicate the density of the clusters. 

## Experiment 2

The second experiment is designed to study if dense reward signals impact exploration in children. It has the same three phase as the first experiment. The hypothesis is that in case of dense rewards, it would take children shorter time to find the goal in the second phase, when there are local rewards leading to the global reward, while it would taken them longer to get to the global reward, if the path of local rewards is blocked. 

The conclusions are missing from the paper, although they state that lack of exploration doesn't hurt the performance in the third phase.