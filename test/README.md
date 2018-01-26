<a id='en'></a>
# [Q-Learning practice](#en)

## 1. go straight : 
> Dec 23-24, 2017


## 2. maze (list version) : 
> Dec 26, 2017

- Because of **fail state (with negative reward)** , I change the IF-ELSE statement in *choose_action* policy. There are three statement :
	1. Choose randomly when random number break the epsilon value, or
	2. **Choose randomly from zero-rewards, where there contain negative reward and max reward is zero**, or
	3. Choose biggest reward. (In this condition, positive reward is guaranteed)
	- With sec. statement, **"Avoidance of negative action"** can be considered when choosing a action.
- Speed of convergence is quite slow where negative reward and multi-direction blocks exist. By **adding punishment to Bumpping the wall**, shortest path (to target) have been found at early round (about 5 episodes), instead of 15 episodes in basic case.
	- When bumpping the wall, get -1 as reward.

## 3. GUI (using **Tkinter**) :
> Jan 19, 2018

- Design GUIs for training vision. One of them is to show Q-Table info, and the another is to show agent status on map.

<a id='zh-TW'></a>
# [Q-Learning 練習](#zh-TW)

## 1. 走直線
> Dec 23-24, 2017

## 2. 迷宮 (list版本) :
> Dec 26, 2017

- 因為存在**失敗狀態(reward為負)**，我修改了在 *choose_action* 策略中的 IF_ELSE 判斷式，其中存在三個判斷式：
	1. 如果隨機值大於 epsilon，則隨機取action, 或者
	2. **若該state存在reward為負且最大reward=0，則從reward=0的action中隨機選一個**, 或者
	3. 選最大的reward,(這個狀況下不會有負的reward被選到)

## 3. GUI (使用**Tkinter**) :
> Jan 19, 2018

- 設計呈現用的GUI，預期目標：雙視窗，分別呈現Q-Table資訊以及agent於地圖上的狀態

## 4. QLearning & Sarsa module :
> Jan 26, 2018

- 將兩個相近的 algorithm 寫成 module，順便練習**繼承(Inheritance**
