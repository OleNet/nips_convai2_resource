# Resources for NIPS 2018 Competition The Conversational Intelligence Challenge 2 (ConvAI2)  

## ParlAI

安装FAIR实验室的工具[ParlAI](https://github.com/facebookresearch/ParlAI#installing-parlai)


## Dataset  

Official train dataset download [link](https://s3.amazonaws.com/fair-data/parlai/convai2/convai2.tar.gz)

Or

中国用户下载amazonaws的资源比较慢，这里有一个百度云盘[convai2.tar.gz](https://pan.baidu.com/s/1Akz9PpbNvlvVMtp9NxXBDA)的镜像, 

下载的convai2.tar.gz 放在如下路径:ParlAI/data/ConvAI2/convai2.tar.gz,  注意不需要解压。

程序自动处理后，ParlAI/data/ConvAI2/目录中会包含如下文件：

|id|  `ls ParlAI/data/ConvAI2/`        |
|--|-----------------------------------|
|1| train_both_original_no_cands.txt  |
|2| train_both_original.txt           |
|3| train_both_revised_no_cands.txt   |
|| ... ...                           |
|27| valid_self_revised_no_cands.txt   |
|28| valid_self_revised.txt            |

文件名也代表了数据的组织方式
按照是否含有self/other 的 persona(画像)组织
| both | none | other | self | 说明            |
|------|------|-------|------|---------------|
| O    | X    | X     | X    | 两者的persona都有  |
| X    | O    | X     | X    | 两者的persona都没有 |
| X    | X    | O     | X    | 只有对方的persona  |
| X    | X    | X     | O    | 只有自己的persona  |

按照修正前/后的persona组织

| original | revise | 说明              |
|----------|--------|-----------------|
| O        | X      | 原始的persona产出的数据 |
| X        | O      | 修正的persona产出的数据 |

按照有无候选组织

| no_cands | 说明  |
|----------|-----|
| O        | 无候选 |



## Baseline models

因为ParlAI的baseline模块依赖了很多预训练资源，存在aws上不方便中国用户下载，所以为了方便，把这些与训练的资源已经在[百度云](https://pan.baidu.com/s/1PwsbFJo0FIvEhmiu4T4AIw)上。

下载之后, 在ParlAI/data/（没有的话创建一个即可）文件夹下解压model.tar.gz，`tar zxvf model.tar.gz`.

## Run Example 

run一个baseline脚本，测试是否上述数据准备成功：

`cd ParlAI; python projects/convai2/baselines/kvmemnn/eval_f1.py`

## Papers 

[A Persona-Based Neural Conversation Model](https://arxiv.org/abs/1603.06155)  
[A Neural Conversational Model](https://arxiv.org/abs/1506.05869)  
[A Diversity-Promoting Objective Function for Neural Conversation Models](https://arxiv.org/abs/1510.03055)  
[Personalizing Dialogue Agents: I have a dog, do you have pets too?](https://arxiv.org/abs/1801.07243)  
