# Reinforcement Learning

**AI = RL + DL (reinforcement learning+deep learning)**



**Agent**

> Observation = state (從Environment觀察而來，是環境的狀態)
>
> Action = change the environment
>
> Reward = 改變Environment之後給的

**Observation -> Action -> Reward**

沒有足夠的label data - > reinforcement learning

-

**Playing Games**

> **Episode** = Observation s1 -> Action a1 -> Reward r1 -> Observation s2 -> ……. -> Game over
>
> target : maximize reward

-

**Difficulties of reinforcement learning**

> * Reward delay
> * Agent 必須學會去探索沒有做過的行為

-

**Policy-based v.s Value-based**

> Policy-based -> learning an actor
>
> Value-based -> learning a Critic
>
> **-> Asynchronous Advantage Actor-Critic (A3C)**

-

**What is Actor**

> Actor/Policy -> looking for a function
>
> Action = $\pi$(Observation) 
>
> ​	function input = observation
>
> ​	function output = action

-

**Neural network as actor**

> Input = observation of machine (vecrtor / matrix)
>
> Output = action
>
> ![螢幕快照 2019-06-02 上午11.57.41](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-02 上午11.57.41.png)

-

**Goodness of Actor**

> Actor = neural network = $\pi_\theta(s)$ 
>
>  如何判斷一個actor的好壞 -> 讓actor去玩遊戲
>
> Total reward = $R_\theta = \sum^T_{t=1} r_t$
>
> $R_\theta$ 每次都會不一樣，因為遊戲有隨機性，actor本身也有隨機性 -> 目標：希望得到$R_\theta$ 最大的的期望值$\bar{R_\theta}$，越好的actor期望值越大
>
> ------
>
> **如何計算？**
>
> 每一個Episode 會有一連串的序列動作 = $\tau = { {s_1,a_1,r_1,s_2,a_2,r_2,…….s_T,a_T,r_T}}$ 
>
> *  $R(\tau) = \sum^N_{n=1}r_n$ (把所有reward加總起來)(Total reward)
>
> *  $P(\tau|\theta)$ (參數$\theta$對整個序列$\tau$ 整體發生的機率)
> * $\bar{R_\theta} = \sum R(\tau)P(\tau|\theta)$ (整體期望值 = total reward * 發生的機率)

-

**Gradient Asctent**

> * $\theta ^* = \arg{\max_\theta\bar{R_\theta}}$ , $\bar{R_\theta = \sum R(\tau)P(\tau|\theta)}$
>
> * Gradient ascent 
>
>   * Start with $\theta^0$
>   * $\theta^1 = \theta^0+\eta\nabla\bar{R_{\theta^0}}$
>   * $\theta^2 = \theta^1+\eta\nabla\bar{R_{\theta^1}}$
>   * ….
>
>   ![螢幕快照 2019-06-02 下午10.58.15](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-02 下午10.58.15.png)
>
>   ![螢幕快照 2019-06-02 下午11.05.23](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-02 下午11.05.23.png)
>
>   ![螢幕快照 2019-06-02 下午11.06.55](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-02 下午11.06.55.png)
>
>   ![螢幕快照 2019-06-02 下午11.11.09](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-02 下午11.11.09.png)

-

**Policy Gradient**

>  



 









