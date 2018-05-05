# Resources for NIPS 2018 Competition The Conversational Intelligence Challenge 2 (ConvAI2)  

## ParlAI

安装FAIR实验室的工具[ParlAI](https://github.com/facebookresearch/ParlAI#installing-parlai)


## Dataset  

Official train dataset [download link](https://s3.amazonaws.com/fair-data/parlai/convai2/convai2.tar.gz)

中国用户下载amazonaws的资源比较慢，这里有一个百度云盘convai2.tar.gz的镜像, [link](https://pan.baidu.com/s/1Akz9PpbNvlvVMtp9NxXBDA)

下载的convai2.tar.gz 放在如下路径ParlAI/data/ConvAI2/convai2.tar.gz


## Baseline models

Models by ParlAI team are baselines. Models of those are separately put in directory `ParlAI/data/models/convai2/`, for example, the kvmemnn model is put in `ParlAI/data/models/convai2/kvmemnn/kvmemnn.tgz`.

因为ParlAI的baseline模块依赖了很多预训练资源，存在aws上不方便中国用户下载，所以为了方便，把这些与训练的资源已经在[百度云](https://pan.baidu.com/s/1PwsbFJo0FIvEhmiu4T4AIw)上。
下载之后创建目录在ParlAI目录创建data/文件夹，解压下载的model.tar.gz， `tar zxvf model.tar.gz`.


## Papers 

[A Persona-Based Neural Conversation Model](https://arxiv.org/abs/1603.06155)  
[A Neural Conversational Model](https://arxiv.org/abs/1506.05869)  
[A Diversity-Promoting Objective Function for Neural Conversation Models](https://arxiv.org/abs/1510.03055)  
[Personalizing Dialogue Agents: I have a dog, do you have pets too?](https://arxiv.org/abs/1801.07243)  
