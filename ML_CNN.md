# CNN

CNN -> 為了簡化model

**CNN -> Image**

> **subsampling**
>
> ex. 把奇數行偶數列拿掉之類的 -> 縮小圖片但不影響判斷 -> 可以減少參數
>
> -
>
> CNN progress
>
> convolution -> max pooling -> convolution -> max pooling -> … -> flatten
>
> -
>
> 1. Convolution : 找出部分的patterns(圖片中具意義的特徵)、不同位置的pattern
> 2. Max pooling : 做subsampling 

-

**Convolution**

> 有很多個filter (= matrix)，裡面裝training出來的參數
>
> 使用filter蓋在image上做內積
>
> 透過stride移動filter
>
> ![螢幕快照 2019-06-07 下午7.04.54](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 下午7.04.54.png)
>
> 一個filter做完會將6x6 matrix變成4x4 matrix 
>
> 所有的4x4 matrix疊合起來 -> **feature map**
>
> (如果要找的feature大小不同，CNN也沒辦法自動處理這件事)
>
> ------
>
> ![螢幕快照 2019-06-07 下午7.18.48](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 下午7.18.48.png)
>
> 會sharing weight (減少需要的parameters)

-

**Max pooling**

> ![螢幕快照 2019-06-07 下午7.27.42](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-06-07 下午7.27.42.png)
>
> 4x4 matrix 2x2一組分四組 挑四個element裡面的最大值
>
> -> output 2x2 matrix

-

**Flatten**

> 把得到的feature map拉直-> 丟到fully connected feeforward network -> end

-

Deep dream / Deep style

 -

**Why CNN?**

> 看你的image特性來決定要不要用CNN
>
> CNN處理image特別有效
>
> 圍棋的特性跟image很像



