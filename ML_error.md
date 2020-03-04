# Error

**Error comes from…..?**

> 1. bias
> 2. variance

-

**Estimator**

> ![螢幕快照 2019-05-26 下午9.27.34](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午9.27.34.png)
>
> ![螢幕快照 2019-05-27 下午2.07.28](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-27 下午2.07.28.png)
>
> **Bias : $E[f^*] = \bar{f}$ 算出來的位置與真正的$\hat{f}$ 距離差**
>
> **Variance : 每一個 $f^*$ 和 $\bar{f}$ 的距離差**
>
> ------
>
> **如何得到很多的**$f^*$???
>
> -> 不同批training data會獲得不同的$f^*$
>
> -> 用不同的data來找最好的function，就算使用同一個model，找出來最好的function 	$f^*$就是不一樣的 
> ![螢幕快照 2019-05-27 下午5.16.38](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-27 下午5.16.38.png)
>
> ------
>
> **Variance**
>
> 簡單的model受到data的影響較小
>
> ![螢幕快照 2019-05-29 下午5.51.37](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-29 下午5.51.37.png)
>
> ------
>
> **Bias**
>
> $E[f^*] = \bar{f}$ 
>
> $\bar{f}$和真正的靶心$\hat{f}$多接近呢
>
> Bias 越大，平均值與靶心距離較大 
>
> 簡單的model會有比較大的bias，但每一次與真正要找的值比較接近
>
> 複雜的model平均起來會有較小的bias，但每一次與真正要找的直差很多
>
> **原因是因為複雜的model包含的function比較多，function set較大，有較大的機率包含到target function，但搜尋的範圍較大，所以比較不集中**
>
> ![螢幕快照 2019-05-29 下午6.05.14](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-29 下午6.05.14.png)
>
> ![螢幕快照 2019-05-29 下午6.10.35](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-29 下午6.10.35.png)
>
> ------
>
> **如何知道做ML work的時候error是來自bias還是variance?**
>
> * 如果model沒辦法fit你的training example -> error來自於bias (underfitting)
>
>   > 代表target不在function set裡面->重新design model
>
> * 如果model可以fit training data但是在testing data上表現不好 -> error來自於variance(overfitting)
>
>   > * More data (不會影響bias)(可以自己產生XD)
>   > * Regularization
>
> ------
>
> **Model selection**

