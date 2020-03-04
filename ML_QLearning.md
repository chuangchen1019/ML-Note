# Q_Learning

**Q-function**

> $Q^\pi(s,a)$
>
> 強制agent在s的時候做a這個action -> 都用actor$\pi$繼續玩下去之後得到的reward期望值![螢幕快照 2019-06-09 上午9.20.20](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-09 上午9.20.20.png)
>
> ------
>
> **Q_learning progress**
>
> 1. $\pi$ 與環境互動
> 2. Learning $Q^\pi(s,a)$
> 3. 找到更好的actor $\pi'$
>
> ------
>
> **Better?**
>
> $V^{\pi'}(s) \geq V^{\pi}(s)$ : 在所有的state s中，$\pi'$ 的表現會比 $\pi$ 好
>
> $\pi'(s) = \arg{\max{Q^\pi(s,a)}}$ (透過learning $Q^\pi$ 找到一組參數更新$\pi$使得所有state能在更新後的$\pi'$有更好的表現)
>
> ------
>
> **Target Network**
>
> ![螢幕快照 2019-06-09 上午9.58.39](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-09 上午9.58.39.png)
>
>  固定Target network然後不斷的更新$Q^\pi$ 更新一陣子之後再把target network的$Q^\pi$更新成現在的$Q^\pi$ 
>
> ------
>
> **Exploration**
>
> 機器學習到做某action會得到positive的reward，之後就不會去做其他的action，所以必須explore。
>
> How to fix that ?
>
> * **Epsilon Greedy** : $1-\epsilon $ 的機率會完全依照Q function的值，其他的機率會依照random ($\epsilon $會隨著時間遞減)
> * **Boltzmann Exploration** 
>
> ------
>
> **Replay Buffer**
>
> 把與環境互動的資料都放到reply buffer裡面
>
> 裡面的exp可能來自不同的policy -> 因為還沒到buffer的上限值就更新參數所以會得到不同的exp

-

**Double DQN**

> Q value is usually over-estimated
>
> Double DQN會更接近實際的值，learn出來的policy會比較強
>
> ------
>
> Double DQN 有兩個 Q network
>
> 一個 Q network 決定哪一個action的Q value最大
>
> 另一個 Q network 算整體的Q value
>
> -
>
> **可以避免over-estimate的問題**
>
> * 拿原本的Q network選action(內層)
> * 拿target network做外層的Q network -> 執行運算![螢幕快照 2019-06-09 上午10.45.19](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-09 上午10.45.19.png)

-

**Dueling DQN**

> **唯一不同的事情：改network的架構**
>
> ![螢幕快照 2019-06-09 上午10.54.27](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-09 上午10.54.27.png)
>
>  