# 开始寄语
这个仓库是用来存放我自己调试成功的代码的，也是为了致敬facenet的创始人。
# 操作流程
## 环境配置
* pythontensorflow==1.7  
* scikit-learn  
* opencv-python
* h5py
* matplotlib
* Pillow
* requests
* psutil
* scipy==1.2.1
* pandas
* python == 3.6.x
## facenet库文件的导入
* 在自己电脑对应的Anaconda3\Lib\site-packages目录下，新建facenet文件夹
* 将facenet\src目录下的全部文件复制到上面新建的facenet文件夹内
* 在Anaconda Prompt内输入import facenet，不会报错即可
## 数据及模型操作
* [LFW数据集](http://vis-www.cs.umass.edu/lfw/lfw.tgz)
* 把数据集解压到facenet-master\data下面
* 在data目录新建一个空文件夹，命名为“lfw_160”
* 将待检测所使用的数据集校准为和预训练模型所使用的数据集大小一致（160*160），转换后的数据集存储在lfw_160文件夹内
* 图片预处理——运行人脸对齐程序（src\align\align_dataset_mtcnn.py）
* 如果是下载原版的facenet的话请把/align文件夹里的所有文件全部复制到/src文件夹里
* 输入命令python src\align\align_dataset_mtcnn.py data/lfw data/lfw_160 --image_size 160 --margin 32 --random_order --gpu_memory_fraction 0.25
* 模型下载原版本的模型需要翻墙，如果不想翻墙的朋友，从我的百度云网盘下载[facenet数据集](https://pan.baidu.com/s/1o4ukiddN08aXJgK9wr780Q)
提取码：4hiw
* 在主目录创建model文件夹，并且将四个文件都复制进去
## 执行程序
* 评估预训练模型的准确率，在主目录文件夹下执行代码：
    * python src\validate_on_lfw.py \data\lfw_160 \models\20180408-102900
* 人脸对比,facenet可以输出图片的一维特征向量值，求两个图片特征值的欧氏距离，来判断是不是一个人，运行代码 
    * python src\compare.py \models\20180408-102900 \data\images\1.jpg \data\images\2.jpg  

<img src="1.png" width="60%">
<img src="2.png" width="60%">  

# 结束语
如果对于facenet有什么不会的欢迎发邮件来讨论。1310706904@qq.com。  
虽然是平平无奇的本科生，但是总会发光的。  
感谢facenet的创始人😘# Facenet_Tensorflow
# facenet-tensorflow
