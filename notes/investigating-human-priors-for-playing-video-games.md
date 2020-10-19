> Investigating Human Priors for Playing Video Games

| Title    | Investigating Human Priors for Playing Video Games           |
| -------- | ------------------------------------------------------------ |
| Authors  | Rachit Dubey, Pulkit Agrawal, Deepak Pathak, Thomas L. Griffiths, Alexei A. Efros |
| Link     | https://arxiv.org/pdf/1802.10217.pdf                         |
| Keywords | cognition, prior                                             |

A lot of RL work is done using video games as the platform. It is a well known fact that humans bring a lot of prior knowledge while playing video games. In this paper, the authors conduct several ablation studies to understand the relative importance of some of these priors. The following are the observations made in the paper:

- **Semantic prior** : Knowledge of semantics helps humans infer the latent reward structure of the game. For example, if a game has a key and a door, a human would first visit the key and then the door. In the absence of semantics, humans were unable to infer the reward structure and hence explored more.
- **Visible distinction**: Distinct objects even without semantics help drive efficient exploration in humans. The idea that visibly distinct objects are interesting is a critical prior and can act as sub-goals for exploration.
- **Affordances as prior**: Affordance turned out to be as important as semantic information. 
-  **Things that look similar behave similarly**: Visual similarity turned out to be the second most important prior used by humans during gameplay.
- **Prior knowledge about object interactions**: This surprisingly led to increased exploration, apart from more time required and more deaths.



### Results

- When these visual priors were removed from the game, the time taken to solve the game rose from 2 to 20 mins, while average number of deaths rose from 4 to 40. *Physics and motor priors were not removed*.
- Exploration was close to random.
- Most participants noted that they could solve the game only by memorizing it. 
- They propose a taxonomy of object priors based on the results showing how important the prior was and based on work in developmental psychology suggesting at what stage in life do humans acquire such priors.
- They also try to train a RL agent to solve a simpler version of these games. But since this is a sparse reward setup (similar to Montezuma's Revenge), A3C and BFS could not solve the game. Curiosity backed exploration strategy worked.

Priors need not be always helpful. If the rewards are not visible in any level, it is highly unlikely that a human would capture those rewards. While adding priors to RL agents seem to be an interesting line of work, we would need to ensure that it doesn't hamper exploration in these settings.