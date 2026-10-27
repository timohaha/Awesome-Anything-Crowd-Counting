# Direct Regression（直接全局回归）

> **定义**：跳过位置建模，由图像特征直接回归一个全局计数值（标量），不产出密度图 / 点 / 框。
>
> **收录边界（已并入的相邻变体，不单列）**：
> - 计数分类（把数量分箱做分类，而非回归连续值）并入此类；
> - 传统 / 非深度方法（手工特征 + 线性 / 核回归 / 森林等，无神经网络）放在对应物种小节并标注 `(classical)`。
>
> 回归密度图再积分的，归入 [Density_Map](Density_Map.md)；先检测再数框的，归入 [Detection_based](Detection_based.md)。

## 条目格式

```markdown
- <a name="缩写"></a>**[缩写]** 论文标题（**会议/期刊 年份**）[[论文](论文链接)][[代码](代码链接，无则省略)]![GitHub stars](http://img.shields.io/github/stars/作者/仓库.svg?logo=github&label=Stars)
```

## 论文列表

### People（人 / 人群）
- <a name="CS-SLR"></a>[**CS-SLR**] Cost-sensitive sparse linear regression for crowd counting with imbalanced training data(**ICME,2016**)[[paper]](https://ieeexplore.ieee.org/document/7552905)
- <a name="DeepCount"></a>**[DeepCount]** Deep Density-aware Count Regressor（**ECAI,2020**）[[paper]](https://arxiv.org/abs/1908.03314)[[code]](https://github.com/GeorgeChenZJ/deepcount)![GitHub stars](http://img.shields.io/github/stars/GeorgeChenZJ/deepcount.svg?logo=github&label=Stars)


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
- （待补充）
