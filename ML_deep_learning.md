# Deep Learning

 **Fully Connect Feedforward Network**

> 兩個layer之間的neuron都全連接 -> fullyy connected 
>
> input是由後往前傳 -> feedforward ![螢幕快照 2019-06-07 上午11.09.01](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 上午11.09.01.png)
>
> 一個neural network就是一個function
>
> 知道全部的weight / bias我們就可以得到vector output出來的值(另一個vector)
>
> -
>
> 建構network function(決定network之間的連接) = **define a function set**
>
> ![螢幕快照 2019-06-07 上午11.17.06](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 上午11.17.06.png)
>
> ------
>
> **Deep = Many hidden layers**
>
> (要幾層才算deep有不同的定義)
>
> ------
>
> **Matrix Operation**
>
> ![螢幕快照 2019-06-07 上午11.40.43](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 上午11.40.43.png)
>
> 矩陣運算 -> GPU 加速 (比CPU快)
>
> ------
>
> **Output Layer**
>
> Hidden Layers = feature engineering
>
>   Layer = **Multi-class Classifier** (Softmax)
>
> ------
>
> **Goodness of function**
>
> ![螢幕快照 2019-06-07 下午1.10.25](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 下午1.10.25.png)
>
> output和target計算cross entropy -> 越小用好
>
> ------
>
> 怎麼更新參數 -> Gradient descent
>
> backpropagation為計算偏微分一個比較好的方式 -> 有很多套件可以做

-

**Backpropagation**

> 就是Gradient descent只是比較有效率
>
> **Backward Pass**
>
> 建一個反向的NN
>
> ![螢幕快照 2019-06-07 下午6.13.25](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 下午6.13.25.png)

