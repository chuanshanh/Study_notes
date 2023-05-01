### Week 1

#### 1.1 define

##### 	==Supervised learning（监督学习） X-->Y 映射==

​	分为：**回归**：预测数字，输出有**无限多**可能。 例子：房价预测

​			    **分类**：预测类，输出是**有限**个可能。例子：肿瘤类型判断



#####     ==Unsupervised learning（无监督学习) 只有X,没有Y==

​	分为：**聚类算法（clustering)**：无标签，进行分类/群。  例子：新闻推送，推送相类似的新闻

​				异常检测

​				降维

#### 1.2 Jupyter Notebook

​	使用：打开cmd,输入jupyter notebook ,把对应文件直接拖到黑框，即可打开整个文件夹

#### 1.3 线性回归（Linear Regression Model)

1. 基本概念：

​		训练集-->训练模型-->预测  || x:特征/输入特征/输入变量 || y:目标变量/输出变量 || m: 训练样本数



2. 模型F(x)和代价函数J(w,b)：![image-20230428101935184](C:\Users\24987\AppData\Roaming\Typora\typora-user-images\image-20230428101935184.png)

​		f 是训练模型（model) ，包含w,b两个参数；

​		J是代价函数（cost function)，方差代价函数，用来衡量预测值和实际值间的误差



​		f(x)和J的对应关系直观理解（f仅有参数w)：

<img src="C:\Users\24987\AppData\Roaming\Typora\typora-user-images\image-20230428102613205.png" alt="image-20230428102613205" style="zoom:70%;" />

当f(w,b)时，对应的J(w,b)是一个类似碗状的3d曲面画图，可以用等高线图来理解，中间的最低点就是w,b的最佳取值，即J最小的时候情况。

ps:遇到一个package argument问题，最终更新matplotlib版本到3.7.1解决，感谢群友

![image-20230429090559539](C:\Users\24987\AppData\Roaming\Typora\typora-user-images\image-20230429090559539.png)



==3.梯度下降法（gradient descent algorithm）==

​	作用：寻找最小化的任意函数

​	outline:1.start with some w,b.（=0）；

​				 2.keep changing w,b to reduce J(w,b);

​				 3.Until we settle at or near a mininum(may >1个)

​	不同的起点-----找最大梯度下降的方向----->局部最小值

![image-20230501113331465](C:\Users\24987\AppData\Roaming\Typora\typora-user-images\image-20230501113331465.png)

### 

$$
w=w-\alpha*\frac{\partial}{\partial w}J(w,b)
$$

$$
b=b-\alpha*\frac{\partial}{\partial b}J(w,b)
$$

alpha是学习率（learning rate）即步幅，后跟的偏导函数是方向。

注意：w,b要**同步更新**，用tmp_w,tmp_b存储，最后统一更新。