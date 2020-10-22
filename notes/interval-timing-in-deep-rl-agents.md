| Title    | Interval timing in deep reinforcement learning agents        |
| -------- | ------------------------------------------------------------ |
| Authors  | [Ben Deverett](https://arxiv.org/search/cs?searchtype=author&query=Deverett%2C+B), [Ryan Faulkner](https://arxiv.org/search/cs?searchtype=author&query=Faulkner%2C+R), [Meire Fortunato](https://arxiv.org/search/cs?searchtype=author&query=Fortunato%2C+M), [Greg Wayne](https://arxiv.org/search/cs?searchtype=author&query=Wayne%2C+G), [Joel Z. Leibo](https://arxiv.org/search/cs?searchtype=author&query=Leibo%2C+J+Z) |
| Link     | https://arxiv.org/pdf/1905.13469                             |
| Keywords | interval-timing                                              |



Predicting intervals of time is a fairly trivial task for humans but has not been explored much in artificial agents. This paper studies several components that can be used to achieve the same and compares the results with that seen in humans and primates.

The experiment is setup in Psychlab. The agent is shown two cues separated by a randomly sampled interval. It has to learn the interval and replicate the same by gazing at a certain spot after the sample interval of time passes. The architecture is fairly complex. They use a resnet to learn the representations from images before passing it to a controller network. The output from controller network is fed to a policy and a value network that trains the agent to gaze after the correct interval has passed.

The authors experiment with recurrent network and feed forward network as the controller network. The recurrent network performs accurately almost always and is able to generalize outside the intervals seen during training. The feedforward network has a decent performance, and is unable to generalize well, but the performance curve resembles that of humans and primates.

The authors experiment with various recurrent architectures (LSTM, GRU, Vanilla RNN) and find that all the architectures produce good performance.

The LSTM activations suggest that the neurons act as a timer. The activations start from an initial point when the first cue is presented, and rise uniformly till the cue to stop is shown. After that it declines uniformly to the initial point as the sample duration passes. In case of feedforward networks, the agent makes use of the external environment as a clock. Such a behaviour in the animal world is called stigmergy.

I think the experiment is fairly complicated and perhaps can be replicated to predict intervals using a simpler setup.

