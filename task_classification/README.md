# task classification
## 2D特征训练
### 1. generally: 在纹理中找瑕疵。基于高斯混合模型（GMM）分类器的纹理检查模型，适用于图像金字塔，可以分析纹理的多个频率范围。
### 2. 要求：训练样本必须完美无瑕疵
### 3. 整体步骤：
1. 创建模型```create_texture_inspection_model```或读取模型```read_texture_inspection_model```
2. 添加训练样本```add_texture_inspection_model_image```
3. 查看样本```get_texture_inspection_model_image```
4. 训练模型```train_texture_inspection_model```

### 4. 原理： 每层金字塔都会训练一个GMM模型，并确定该层的'novelty_threshold'（区分有无瑕疵的阈值）。