
Hao Chen
https://stan-haochen.github.io

BlendMask CVPR20

Instance Segmentation

    + COCO 80 classes
        + AP平均精度
        + 泛化能力好，不太容易过拟合
        - 标注不准确
        - AP指标对分割不精准

    + Cityscapes 8 classes   
        - 类别不均衡

    + Open Images and LVIS

Mask R-CNN ➡️ Faster R-CNN + FCN

Why NOT R-CNN

    + FPN/Rol下采样丢失细节
        - 增加polling分辨率代价太大：更大的感受野，更难更慢训练

全卷积方法：

    + 自底向上，每个像素预测
        - SOLO
        - 没有实例高级信息
        - 不难适应复杂场景
    + 自顶向下，每个实例预测
        - DeepMask
        - InstanceFCN
        - TensorMask
        - 缺乏细节信息
        - 背景无用计算
    + Proposal-Based
        - top（bbox） 和 bottom（segmentation）
        - MaskLab
        - YOLACT
        - Blender 

SOLO：

    - segementing objects by locations

Blender
    
    - spatial+channel assembing

BlendMask
   
    - top：bbox and  attention tensor
    - 框架：
        - top
        - bottom：semetic，position
        - blender


