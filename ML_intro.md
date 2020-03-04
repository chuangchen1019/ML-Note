# Machine Learning Intro

https://www.youtube.com/watch?v=CXgbekl66jc&list=PLJV_el3uVTsPy9oCRY30oBPNLCo89yu49&index=1

**What is Artificial Intelligence**

> Artificial lntelligence -> 人工智慧 -> 是人類要達成的目標
>
> Machine Learning -> 機器學習 -> 達成人工智慧的一種手段
>
> Deep Learning ->  深度學習 -> 機器學習的一種方法

-

**本能&人類設定好的本能**

> **Hand-crafted rules** (設定規則，機器執行，不會自己思考) -> hand-crafted AI
>
> 1. 非常僵化 (Hard to consider all possibilities)
> 2. 永遠無法超越創造者

-

**What is Machine Learning**

> 寫程式讓機器具有學習的能力
>
> -> **Looking for a Function (from data)**
>
> F(input) = response

-

**Framework**

> 1. **Function Set** (裡面有成千上萬的function) = Model
>
>     **Supervised Learning** -> 給machine input和正確的output讓他學習
>
> 2. **Training Data** (餵給function) -> 找出 Goodness of function f
>
> ![螢幕快照 2019-05-25 下午1.10.31](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-25 下午1.10.31.png)
>
> * 光找出好的function是不夠的
>
> 3. **Goodness of function f ** ——> Pick the "Best" Function f*(用好的演算法挑)
>
> ![螢幕快照 2019-05-25 下午1.13.19](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-25 下午1.13.19.png)
>
> <span style = "color:red">Step : </span>
>
> ​	<span style = "color:red">1. Define function set</span>
>
> ​	<span style="color:red">2. Find Goodness of function</span>
>
> ​	<span style="color:red">3. Pick the best function f* </span>

------

**Learning Map**

![螢幕快照 2019-05-25 下午1.23.27](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-25 下午1.23.27.png)

------

**Regression**

> Machine找出來的function的輸出是一個數值(scalar)
>
> (The output of the target function f is scalar)
>
> Ex : pm2.5預測未來某天的pm2.5**數值**

-

**Classification**

> 1. Binary Classification
>
>    > f(input) =<span style="color:red"> Yes or No </span>(Ex:判斷是否是垃圾郵件)
>
> 2. Multi-class Classification
>
>    > f(input) = <span style="color:red">class1, class2, ….. classN</span> (Ex:輸入一則新聞，輸出是哪一個分類)

-

**Model**

> 選不同的Function set = 選不同的Model
>
> 1. Linear Model
>
> 2. Non-linear Model
>
>    > **Deep Learning**
>    >
>    > * Image Recognition (圖片辨識)
>    >
>    >   input image -> Function(Hierarchical Structure) -> pixel和圖片的關係
>    >
>    >   可以描述pixel跟class的關係
>    >
>    >   ![螢幕快照 2019-05-25 下午1.50.49](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-25 下午1.50.49.png)
>    >
>    > * ------
>    >
>    >   Playing GO (下棋)
>    >
>    >   Input 棋盤狀況 -> Function -> Next move(下一步應該落子的位置)
>    >
>    >   **可以想成一個19x19的類別選擇問題(19x19 classes)**
>    >
>    >   ![螢幕快照 2019-05-25 下午1.52.34](/Users/ghjyjjj/Desktop/ML_pic/螢幕快照 2019-05-25 下午1.52.34.png)
>
>    **Supervised Learning -> 大量的training data -> <span style = "color:red">大量的Output (通常稱為 label)</span> -> 大量的effort (人工弄出來)**
>
>    

-

**How to reduce 需要的 Label ?**

> 1. Semi-supervised Learning
>
>    > ex : 擁有少量的貓和狗的labeled data,擁有大量的貓和狗的unlabeled data
>    >
>    > 這些沒有labeled的data在semi-supervised learning的環境下對學習有幫助
>
> 2. Transfer Learning
>
>    > ex: 擁有少量的貓狗labeled data,擁有大量的labeled/unlabeled data(都沒有關係不相干的圖片)
>
> 3. Unsupervised Learning
>
>    > ex: 給機器看大量的文章
>    >
>    > 完全沒有label的情況下機器能夠學到什麼樣的程度，可不可以了解詞彙的意思
>
> 4. Stucture Learning
>
>    > 輸出結構化的、複雜的物件
>
> 5. Reinforcement Learning
>
>    > Supervised Learning -> 會告訴機器正確答案
>    >
>    > Reinforcement Learning -> 只告訴機器做完的結果是好是壞(Critics)(較符合人在現實中的學習環境，較intelligence)