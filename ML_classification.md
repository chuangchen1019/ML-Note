# Classification

**X -> function -> class n**



**How to classification**

> 1. 從function set裡面挑一個g(x)
>
> 2. x代入g(x) > 0 -> class 1, else -> class 2
>
> 3. Loss function = $\sum \delta{(\hat{y}^n !=F(x))}$
>
>    ![螢幕快照 2019-06-03 下午11.03.12](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-03 下午11.03.12.png)

-

**Prior&Probability**

> 用vector來表示每個data的特徵值 -> feature
>
> -
>
> **Gaussian Distribution** => input vector x 得到 x  從這個distribution裡面被sample出來的機率
>
> Gaussian Distribution的取決於 
>
> * Mean $\mu$ (控制分佈的最高點)
> * covariance matrix $\sum$ (控制分佈散的程度)
>
> 代入不同的 $\mu$ $\sum$ 會得到不一樣的機率分佈
>
> 假設要找的x不在這個機率分佈裡面，我們可以取得這機率分佈的$\mu$ $\sum$ 然後帶入gaussian distribution算出整體分佈 -> 算出x在這個gaussian distribution被sample出來的機率
>
> -
>
> **How to find $\mu \sum$ ?**
>
> -> **Maximum Likelihood**
>
> * 任何一個gaussian都可以sample出一樣分佈的點，只是這個機率不一樣(對於每個不同的gaussian) -> Different Likelihood
>
> * 當我們取得$\mu \sum$ 就可以算出gaussian取出這些點的機率 
> * $L(\mu,\sum) = f_{\mu,\sum}(x^1) f_{\mu,\sum}(x^2)….$
> * 找到最大Liklihood的那個gaussian的那一組參數 = $(\mu^*,\sum^*)$

-

**Modifying Model**

> 強迫每個class都用同樣的covariance matrix
>
> ![螢幕快照 2019-06-04 下午3.42.48](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-04 下午3.42.48.png)
>
> 用共同的covariance matrix的時候$\sum$ 要加權平均
>
> —> linear model 
>
> -
>
> ![螢幕快照 2019-06-04 下午3.47.54](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-04 下午3.47.54.png)

-

**Probability Distribution**

> 要選哪個機率模型？ -> 人可以自己決定(不一樣要用gaussian)
>
> Ex. Binary feature -> Bernoulli distributions, all dimensions are independent -> Naive Bayes Classifier

-

Posterior Probability

> ![螢幕快照 2019-06-04 下午3.54.55](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-04 下午3.54.55.png)
>
> 











