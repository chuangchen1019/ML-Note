# Gradient Descent

**Stochastic Gradient Descent**

> **Gradient Descent** = $\theta^i = \theta ^{i-1} - \eta \nabla {L(\theta^{i-1})}$
>
> **Stochastic Gradient Descent**
>
> * 只考慮一個example的loss值
>
>   $L^n = (\hat{y}^n-(b+\sum{w_ix^n_i}))^2$
>
> * 原本的Gradient descent是看所有的loss才update一次參數，而stochastic gradient descent是看一個example的loss就update 一次參數。 

-

**Feature Scaling**

> ![螢幕快照 2019-06-03 下午7.51.49](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-03 下午7.51.49.png)
>
> 把資料調整成相似的分佈 -> 希望不同的feature他們的scaling相同 
>
> w1,w2對y是有差不多的影響力 -> 好處：可以適用同一個 learning rate (不需要各自設計不同的learning rate)
>
> ------
>
> ![螢幕快照 2019-06-03 下午8.14.20](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-03 下午8.14.20.png) 

-

**Gradient Descent Theory**

> **Taylor Series**

