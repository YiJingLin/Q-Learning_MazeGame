# Q-Learning practice

## 1. go straight : 
> Dec 23-24, 2017


## 2. maze (list version) : 
> Dec 26, 2017
1. Because of fail state with negative reward, change condition in choose_action policy. There are three conditions :
	1. Choose randomly when random number break the epsilon value, or
	2. Choose randomly from zero-rewards, where there contain negative reward and max reward is zero, or
	3. Choose biggest reward. (In this condition, positive reward is guaranteed)
2. Speed of convergence is quite slow where negative reward and multi-direction blocks exist. By add punishment to Bumpping the wall, shortest path to target have been finded at early round (about 5 episodes), Instead of 15 episodes in basic case.
