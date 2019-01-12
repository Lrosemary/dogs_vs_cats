# 代码运行前请阅读以下内容
1. 建议用python3.5及以上的环境，另外模型可视化需要安装pydot-ng, graphviz, pydog包, 本地还需要安装Grahviz并将它的bin目录添加到系统环境变量中 (*这一步我暂时还没解决，即使参考了别人分享的[解决办法](https://blog.csdn.net/u011311291/article/details/80298563)，可以暂时跳过*）。  
[https://graphviz.gitlab.io/download/ ](https://graphviz.gitlab.io/download/)

2. 下载该仓库中的data目录  
  
3. 因为执行效率的缘故，解压和图像分类存放中分批拷贝全量数据集中的两处代码已经注释掉，建议在本地执行。  

4. 代码中的*_batch_size （如copy_batch_size）变量都可以根据硬件变化调整。  

5. Kaggle上下载数据集并在data目录下逐层解压 (*Jupyter Notebook中不知道为什么解压超级慢，本地用PyCharm跑代码解压很快的，所以这一步建议在本地用winrar之类的解压，代码中已注释掉*) [https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition/data](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition/data)  
  
  
**解压**之后的**目录结构**如下：  
\-- data    
\-----dogs_vs_cats.ipynb # 代码notebook    
\-----model_info.png  # notebook中的一张插图  
\-----All.zip  # 从kaggle上下载得到    
\-----train.zip # 从All.zip解压得到   
\-----test.zip # 从All.zip中解压得到  
\-----sample_submission.csv # 从All.zip中解压得到    
\-----train # 从train.zip解压得到     
\-----test # 从test.zip中解压得到  
**说明**：如果重新跑代码目录结构就恢复到这个样子，后面新建的目录都手动删除掉（不手动删除会遇到一次错误，再次执行也可以继续，但本地删除效率更高）。


**图像分类存放**之后的**目录结构**：  
\-- data    
\-----dogs_vs_cats.ipynb # 代码notebook    
\-----model_info.png  # notebook中的一张插图  
\-----All.zip  # 从kaggle上下载得到    
\-----train.zip # 从All.zip解压得到   
\-----test.zip # 从All.zip中解压得到  
\-----sample_submission.csv # 从All.zip中解压得到    
\-----train.zip # 从train.zip解压得到     
\-----test.zip # 从test.zip中解压得  
###### （下面是较解压之后的新增部分）  
\-----train2  
\-----------cats  # 本地将train目录中前12500张猫的图片拷贝到这个目录下，注意是拷贝，不是剪切  
\-----------dogs  # 本地将train目录中后12500张狗的图片拷贝到这个目录下，注意是拷贝，不是剪切    
\-----test2  
\-----------test  # 本地将test目录中全部图片拷贝到这个目录下，注意是拷贝，不是剪切  
**说明**：目录执行代码会创建（因为预处理的需要分类存放），但代码中拷贝文件太慢了，所以手动在本地拷贝，代码中已经注释掉。
