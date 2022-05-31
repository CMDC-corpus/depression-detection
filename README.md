# 毕设交接

代码中包含大论文中的所有实现，包括自编码器网络和下游网络，DDFN网络，引入了多任务学习机制的DDFN网络，还有本文所用的所有基线模型，所有模型的代码都在models.py文件中，对于具体模型的定义在文件中都有注释

## 数据库下载

https://drive.google.com/drive/folders/1BnpE-xfQmRbQPWW4wxc_llMPkI2GZ2cy


## 代码使用细节

### 环境配置

<ul>
    <li>Pytorch</li>
    <li>Numpy</li>
    <li>Scipy</li>
    <li>Sklearn</li>
    <li>Pickle</li>
</ul>

### 数据预处理

在跑程序之前需要将数据打成pkl文件，pkl文件的格式如下

    
    {
    "train": {
        "text": [],          # text feature
        "audio": [],         # audio feature
        "vision": [],        # video feature
        "labels": []         # the phq score of each participant
        },
    "valid": {***},          # same as "train"
    "test": {***},           # same as "train"
    }
    
pkl文件需要命名成mosei_senti_data.pkl.

### 怎样运行

整个系统的接口文件是main.py，运行流程如下



    python main.py
