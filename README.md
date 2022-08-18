# yl
Visual cognitive engineering assignment
# Unet for Weizmann Horse Database

## 数据准备

1. 数据集： [Weizmann Horse Database | Kaggle](https://www.kaggle.com/datasets/ztaihong/weizmann-horse-database/metadata).
2. 该数据集包含327幅马的图像和掩蔽图像。
3. 训练时，需要改变数据集的所在路径。
4. 训练验证集按0.85：0.15的比例随机划分

```
weizmann_horse_db
├──── horse(327 images)
│    ├──── horse001.png
│    ├──── horse002.png
│    └──── ...
├──── mask(327images)
│    ├──── horse001.png
│    ├──── horse002.png
│    └──...
```

## 训练

运行以下命令进行训练:

```
python train.py
```



## 测试

测试集结果：MIoU： **0.919**  ,Boundary IoU： 0.731。

测试时，注释掉train.py的main函数，可直接使用训练好的模型文件进行测试。模型文件位于相应的文件夹中。

对应的命令：python train.py

