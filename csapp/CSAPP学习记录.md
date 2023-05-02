### CSAPP学习记录

#### Lab0:实验环境配置成功:)

实验操作流程：

1.打开虚拟机

2.进入实验文件，打开终端，输入 vim bits.c 即可看到实验资料，在这里进行写代码

3.另打开一个终端进行编译，输入make clean;make;./btest;  即可看到得分情况。输入./ dlc bits.c;./ dlc -e bits.c即可查看操作符使用情况。

4.注意：在编译前要进行保存（为什么需要这样目前还不清楚），即按Esc后输入“：w”。输入“：wq”是保存后退出。

下载Lab:

​	终端输入：wget http://csapp.cs.cmu.edu/3e/datalab-handout.tar 

​	再解压：tar xvf datalab-handout.tar，进入文件即可进行操作