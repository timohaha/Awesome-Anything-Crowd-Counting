# Awesome Biological Counting

> 用计算机视觉 / 机器学习方法统计图像或视频中**生物个体数量**的论文、数据集与代码合集。
> 收录对象包含人，但不限于人：鸟类、鱼群、昆虫、海洋哺乳动物、红外相机兽类、细胞与微生物等。
>
> 与人群计数（Crowd Counting）合集的区别：本仓库以**方法（Method）**为主轴组织，而非按年份罗列。

<!--
仓库英文名（目录名 / GitHub repo name）可在发布前自行修改，例如：
Awesome-Biological-Counting / Awesome-Vision-Counting / Awesome-Animal-Counting。
修改后同步更新本标题与下方所有相对链接即可。
-->

## Contents

- [News](#news)
- [Datasets](#datasets)
- [Metrics](#metrics)
- [Papers (by Method)](#papers-by-method)
- [By Subject (cross-index)](#by-subject-cross-index)
- [Contributing](#contributing)
- [Related](#related)

## News

<!-- 按时间倒序记录新数据集 / 新综述 / 重要更新，格式：- [YYYY.MM] 事件描述（链接，可选） -->

- （暂无）

## Datasets

> 单独收录计数任务常用数据集。标注类型区分：Point（点）/ Box（框）/ Image-level（仅图级总数）。

| Dataset | Subject 对象 | Scene 场景 | Scale 规模 | Annotation 标注 | Split 划分 | Link |
| --- | --- | --- | --- | --- | --- | --- |
| WorldExpo'10 | People | 多场景监控（108 场景） | 3980 标注图像 / 1132 视频序列 / 108 场景 | Point | 103 场景训练 / 5 场景测试 | 待补充 |
| Mall | People | 商场室内监控 | 2000 帧 | Point | 800 训练 / 1200 测试 | 待补充 |
| Shanghai Tech Part A | People | 密集人群街头 | 300 训练 / 182 测试图像，241,677 标注，平均 501 人 | Point | 300 训练 / 182 测试 | 待补充 |
| Shanghai Tech Part B | People | 稀疏街头 | 原文未详述图像数（稀疏街道场景） | Point | 原文未详述 | 待补充 |
| UCF-QNRF | People | 稀疏 + 密集混合 | 1,251,642 标注，单图最多 12,865 标注 | Point | 原文未详述 | 待补充 |
| UCSD | People | 室外监控 | 2000 帧，238×158，11–46 人 | Point | 800 训练 / 1200 测试 | 待补充 |
| UCF_CC_50 | People | 密集人群静态图 | 50 张灰度图，94–4543 人 | Point | 5 折交叉验证 | 待补充 |
|Beijing BRT| People | 北京快速公交站台监控 (含光照变化) | 1,280张图像 (640×360), 单图1~64人 | 头部中心点 (Point) | Train / Val / Test (按时间顺序划分) | 待补充 |
| Bacterial cell dataset | 细菌细胞 | 显微镜 | 5 个子集（不同训练样本数） | Point | 按子集划分 | 待补充 |
| Synthetic cells（合成荧光显微镜细胞） | Cells | 荧光显微镜 | 200 张，171±64 细胞 | Region-level（弱监督） | 100 训练 / 100 测试 | 待补充 |
| Pedestrian（室外监控行人） | People | 室外监控视频 | 2000 张，29±9 人 | Region-level（弱监督） | 5 帧稀疏标注训练，其余评测 | 待补充 |
| Malaria（疟疾血涂片红细胞） | Cells | 显微镜血涂片 | 78 张，90±84 红细胞 | Region-level（弱监督） | 5 图训练 / 其余测试 | 待补充 |
| TRONCOS | 车辆 (Vehicle) | 高速公路及城市交通拥堵监控 | 1,244张图像, 46,796辆车 | 车辆中心点 (Point) + ROI | 官方提供 Train / Val / Test (常用5折) | 待补充 |

## Metrics

- 计数回归指标（三大主干通用，最常用）：MAE（Mean Absolute Error，平均绝对误差）； MSE（Mean Squared Error，均方误差）/ RMSE（均方根误差）； MDE / 平均偏差（Mean Deviation Error）
- 检测 / 定位计数指标：Precision / Recall / F1； AP（Average Precision，点定位平均精度）
- 视频时序计数指标：MOTA（Multiple Object Tracking Accuracy）
- 空间分布评估指标（针对密集/车辆计数场景）：GAME (Grid Average Mean Absolute Error, 网格平均绝对误差)

## Papers (by Method)

> 分类采用**三大技术主干 + 两个横切范式**。一篇论文只归入最主要的一类，避免重复收录。

### 三大技术主干（公认范式）

| [Density Map（密度图回归）](src/Density_Map.md) | [Detection-based（检测后计数）](src/Detection_based.md) | [Direct Regression（直接全局回归）](src/Direct_Regression.md) |
| --- | --- | --- |

### 两个横切范式（按监督 / 样本条件，正交叠加在主干之上）

| [Weakly / Semi / Self-supervised（弱/半/自监督）](src/Weak_Semi_Self_Supervised.md) | [Few-shot / Zero-shot（少样本/零样本）](src/Few_Zero_Shot.md) |
| --- | --- |

> **暂不单列、先作标签并入最近主干**（攒够约 10 篇再拆成独立文件）：Video/Tracking 视频时序、Domain Adaptation 域自适应/泛化、Prompt/Open-world 提示式/开放世界、Classical ML 传统非深度方法。归类裁决规则见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## By Subject (cross-index)

> 第二索引：按收录对象反查，便于按物种/场景检索。各主干文件内也按对象分小节。

- People（人 / 人群）：[FSSA](#fssa),[CS-SLR](#cs-slr),[CrowdNet](#crowdnet),[DeepCount](#deepcount)、[Stacked-Pool](#stacked-pool)、[FCNCC](#fcncc)、[MCNN](#mcnn);
- Birds（鸟类）：（待补充）
- Fish（鱼群）：（待补充）
- Insects（昆虫：蜂、蚁等）：（待补充）
- Marine mammals（海洋哺乳动物）：（待补充）
- Camera-trap mammals（红外相机兽类）：（待补充）
- Cells & Microorganisms（细胞 / 微生物 / 浮游生物）：[DE-VOC](de-voc),[GP](#GP);
- Other（其他）：[M-SFANet](#m-sfanet)、[Hydra-Cnn](#hydra-cnn);


## Contributing

欢迎补充，收录标准、分类裁决与条目格式见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## Related

- [gjy3035/Awesome-Crowd-Counting](https://github.com/gjy3035/Awesome-Crowd-Counting)：人群计数方向，按年份组织（本仓库的参考对象）。
