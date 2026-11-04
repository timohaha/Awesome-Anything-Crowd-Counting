# Density Map（密度图回归）

> **定义**：将每个目标中心点用高斯核扩散成密度图，训练模型回归整图密度图，再对密度图积分得到个体总数。这是计数的主流范式，也是密度估计方向最相关的主干。
>
> **收录边界（已并入的相邻变体，不单列）**：
> - 点监督 / 中心点定位热图计数（不显式建完整密度图，但同属位置密度建模）；
> - 以密度图为输出的 Transformer / 序列方法（按输出归此，不按网络结构单列）；
> - 传统 / 非深度密度估计（LLE、核方法等，无神经网络），放在对应物种小节并标注 `(classical)`。
>
> 输出单个总数、不建模位置的，归入 [Direct_Regression](Direct_Regression.md)。

## 条目格式

```markdown
- <a name="缩写"></a>**[缩写]** 论文标题（**会议/期刊 年份**）[[论文](论文链接)][[代码](代码链接，无则省略)]![GitHub stars](http://img.shields.io/github/stars/作者/仓库.svg?logo=github&label=Stars)
```

## 论文列表

### People（人 / 人群）
- <a name="Stacked-Pool"></a>[**Stacked-Pool**]Stacked Pooling For Boosting Scale Invariance Of Crowd Counting(**ICASSP,2020**)[[paper]](https://siyuhuang.github.io/papers/ICASSP-2020-STACKED%20POOLING%20FOR%20BOOSTING%20SCALE%20INVARIANCE%20OF%20CROWD%20COUNTING.pdf)[[arxiv]](https://arxiv.org/abs/1808.07456)[[code]](https://github.com/siyuhuang/crowdcount-stackpool)
- <a name="FCNCC"></a>[**FCNCC**]Fully Convolutional Crowd Counting On Highly Congested Scenes(**VISAPP,2017**)[[paper]](https://arxiv.org/abs/1612.00220)
- <a name="CrowdNet"></a>[**CrowdNet**]CrowdNet: A Deep Convolutional Network for Dense Crowd Counting(**ACMMM,2016**)[[paper]](https://arxiv.org/abs/1608.06197)[[code]](https://github.com/davideverona/deep-crowd-counting_crowdnet)![GitHub stars](https://img.shields.io/github/stars/davideverona/deep-crowd-counting_crowdnet.svg?logo=github&label=Stars)
- <a name="MSCNN"></a>[**MSCNN**]Multi-scale Convolution Neural Networks for Crowd Counting(**ICIP,2016**)[[paper]](https://arxiv.org/abs/1702.02359)[[code]](https://github.com/Ling-Bao/mscnn)
- <a name="MCNN"></a>[**MCNN**] Single-Image Crowd Counting via Multi-Column Convolutional Neural Network(**CVPR,2016**)[[paper]](https://www.semanticscholar.org/paper/Single-Image-Crowd-Counting-via-Multi-Column-Neural-Zhang-Zhou/2dc3b3eff8ded8914c8b536d05ee713ff0cdf3cd?p2df)




### Birds（鸟类）
- （待补充）

### Fish（鱼群）
- （待补充）

### Insects（昆虫：蜂、蚁等）
- （待补充）

### Marine mammals（海洋哺乳动物）
- （待补充）

### Camera-trap mammals（红外相机兽类）
- （待补充）

### Cells & Microorganisms（细胞 / 微生物 / 浮游生物）
- <a name="DE-VOC"></a>[**DE-VOC**]Fast visual object counting via example-based density estimation(**ICIP,2016**)[[paper]](https://web.pkusz.edu.cn/adsp/files/2015/10/Fast-Visual-Object-Counting-via-Example-based-Density-Estimation.pdf)

### Others(其他)
- <a name="M-SFANet"></a>[**M-SFANet**]Encoder-Decoder Based Convolutional Neural Networks with Multi-Scale-Aware Modules for Crowd Counting（**ICPR,2020**）[[paper]](https://arxiv.org/abs/2003.05586)[[code]](https://github.com/Pongpisit-Thanasutives/Variations-of-SFANet-for-Crowd-Counting)
- <a name="Hydra-CNN"></a>[**Hydra-CNN**]Towards perspective-free object counting with deep learning (**ECCV,2016**)[[paper]](http://agamenon.tsc.uah.es/Investigacion/gram/publications/eccv2016-onoro.pdf) [[code]](https://github.com/gramuah/ccnn)
