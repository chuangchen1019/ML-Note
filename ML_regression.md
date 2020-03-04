# Regression

https://www.youtube.com/watch?v=fegAeph9UaA&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=3

**What can "Regression" do?**

* Stock market forcast (股票指數的預測)
* Self-driving Car 
* Recommendation

------

**Model**

> **Linear Model : **
>
> > 如果可以把要找的function寫成  $y = b + \sum W_i X_i$ 的形式 
> >
> > $X_i$ = input x 的 attribute = <span style="color:#4c5d78">**feature**</span>
> >
> > $W_i$ = weight
> >
> > b = bias 

-

**Goodness of Function**

> * **$y = b + w . X_cp$**
>
> Training data : $(x^1,\hat{y}^1)$,$(x^2,\hat{y}^2)$…..$(x^n,\hat{y}^n)$ (皆為正確觀察到的值)
>
> **Def Loss function L: $L(f) = L(w,b) = \sum_{n=1}^ {10}(\hat{y}^n - (b + w . x_{cp}^n))^2$**
>
> > Input : function
> >
> > Output : function不好的程度, 衡量參數的好壞
> >
> > 公式 ：真正的數值-預測的數值 再取平方
> >
> > Loss function output 越大代表function越差

-

**Gradient Descent**

> Loss function $L(w)$ 是可微分的 -> $w^* = \arg \min L(w)$ (找出一個最佳的w讓loss function 最小)
>
> 1. 選取初始的點 $w_0$ (initial value)
>
> 2. Compute $\frac{dL}{dw}|_{w=w^0}$ (在$w^0$這個位置參數$w$對loss function微分 -> 找切線斜率)
>
> 3. 算出來的value如果是負的 -> 代表w正向還存在更小的loss
>
>    以此類推。
>
>    ![螢幕快照 2019-05-26 下午4.51.21](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午4.51.21.png)
>
> 4. step要移動多少？
>
>    Step size = $-\eta\frac{dL}{dw}|_{w=w^0}$  
>
>    $\eta$ = learning rate (learning rate設越大，step size更新的幅度就會變大)
>
>    下一步的位置 $w^1 = w^0 - \eta\frac{dL}{dw}|_{w=w^0} $
>
> 5. Compute $\frac{dL}{dw}|_{w=w^1}$ (在$w^1$時候的位置的微分)
>
> ------
>
> **2 parameters????**
>
> $w^*, b^* = \arg \min_{w,b} L(w,b)$ (有w跟b兩個參數的情況)
>
> 1. Pick initial value $w^0,b^0$
>
> 2. Compute $\frac {\delta L}{\delta w}|_{w=w^0, b=b^0}$ $\frac {\delta L}{\delta b}|_{w=w^0, b=b^0}$ (算出在這兩個位置的偏微分)
>
> 3. 同理 
>
>    > $w^1 = w^0 - \eta\frac{\delta L}{\delta w}|_{w=w^0,b=b^0} $
>    >
>    >  $b^1 = b^0 - \eta\frac{\delta L}{\delta b}|_{w=w^0,b=b^0} $
>
> 4. 繼續gradient descent下去
>
> ![螢幕快照 2019-05-26 下午8.09.52](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午8.09.52.png)
>
> **What is "Gradient !???"**
>
> **Gradient = $\nabla [\frac{ \delta L}{\delta w},\frac{ \delta L}{\delta b} ]$ **
>
> ![螢幕快照 2019-05-26 下午8.16.55](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午8.16.55.png)
>
> <span style="color:red">偏微分會找到法線方向</span>
>
> ------
>
> **Formulation**
>
> ![螢幕快照 2019-05-26 下午8.21.37](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午8.21.37.png)
>
>  
>
> ------
>
> **Model Selection**
>
> 使用training data / test data 判斷model好壞
>
> ![螢幕快照 2019-05-26 下午8.35.28](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午8.35.28.png)
>
> 目標：error rate越低越好
>
> > <span style="color:red">**在training data上做的越來越好，也有可能testing data做的越來越糟，越複雜的model不一定永遠都會在testing data上有更好的表現 -------> overfitting**</span>
> >
> > ![螢幕快照 2019-05-26 下午8.40.47](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午8.40.47.png)
>
> ------
>
> **Redesign the model**
>
> **Regularization** —>(改善loss function)
> $$
> L = \sum(\hat{y}^n-(b+\sum w_ix_i))^2 + \lambda \sum (w_i)^2
> $$
>
> * we preffer smooth function(對於input的變化比較不敏感)
>
>   -> 被雜訊干擾的時候會受影響較小
>
> * $\lambda$值越大 -> 找到的function越平滑 (增加考慮w原本的值，考慮error的部分就減少，training data上得到的error就會變大)
>
>   ![螢幕快照 2019-05-26 下午9.11.06](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-26 下午9.11.06.png)
>
>   
>
> * <span style="color:red">bias (b) 和function的平滑程度沒有關係(只是平移)</span>















