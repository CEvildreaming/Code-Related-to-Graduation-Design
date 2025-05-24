“This project encompasses all my graduation project code.Once you secure the Retinal OCT-C8 dataset that I used, you can fully replicate the experiments in the paper.”
“这个项目包含了我的所有毕业设计代码内容，找到和我一样的Retinal OCT-C8数据集之后可以完整复刻论文内容实验”
Model里面的代码是五种基本的模型。其中EfiicientNet和Swin Transformer有多种变体，可以再model_dict里面查看初始化名称； Train脚本是进行模型对比的时候训练的基本脚本。基本参数可以调。 F1脚本是计算如F1分数，Precision和recall的，同时支持宏和加权两种，看数据集实验，本实验基于Retinal OCT-C8数据集，加权分数等于宏分数。 其他如Adam.py和AdamW.py或者其他是消融试验的变量训练器。是基于Train.py修改得来。具体看论文控制变量表格 本论文数据集在https://www.kaggle.com/datasets/obulisainaren/retinal-oct-c8下载。

由于实验环境是租的AutoDL云GPU，整体代码的运行相关逻辑需要修改指定地址。比如Train训练Resnet的时候，具体模型地址和数据集地址需要依据环境决定，另外需要注意的是，F1pro.py是评估脚本。指定数据集需要数据集的test也就是测试集。否则计算不准确。

图像分类系统代码是system.py,可以直接运行，注意不能在虚拟环境，最好在本地环境，不然运行可能报错
