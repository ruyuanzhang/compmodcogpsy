# Appendix

## 本章数学符号总结

6.4 经典漂移扩散模型

| 符号或正文名称            | 物理意义                      | 正文中的写法或说明                                                                 |
| ------------------ | ------------------------- | ------------------------------------------------------------------------- |
| θ                  | 漂移扩散模型的参数向量               | 当前参数组合；拟合时包含漂移系数、决策边界、起始偏差和非决策时间                                          |
| k                  | 漂移系数                      | 刺激一致性百分比与漂移率之间的比例系数                                                       |
| coh                | 刺激一致性                     | 当前试次中朝同一方向运动的点的比例；数据列名为 `coherence`                                       |
| `coherence`        | 数据文件中的刺激一致性列名             | 与表中的刺激符号 `coh` 同义                                                         |
| μ                  | 每帧证据增量的均值，即漂移率            | 正态分布的均值；正文用 `DriftRate` 表示，定义为 `k × coh`                                  |
| σ                  | 每帧证据增量的标准差                | 正态分布的标准差；代码中作为 `scale` 参数                                                 |
| B                  | 决策边界间距                    | 拟合参数表和绘图代码中写作 `B`；模拟代码前面写作 `b`                                            |
| a                  | 起始偏差参数                    | 表示起始位置在决策边界间距中的相对比例，0 < a < 1                                             |
| ndt                | 非决策时间                     | 漂移扩散模型的拟合参数之一                                                             |
| rt                 | 当前试次的反应时间                 | `ddmpdf()` 的输入；数据表列名写作 `RT`，建议正文统一写作 `rt`                                 |
| correct            | 当前试次的正确性                  | 1 表示正确，0 表示错误                                                             |
| θ 下的单试次联合概率密度      | 给定参数时，该试次反应时间和选择结果的联合概率密度 | 正文由 `ddmpdf()` 调用 `pdf()` 计算；选择下边界时，正文说明为 1 减去上边界对应的密度                    |
| LL                 | 对数似然                      | 衡量参数 θ 对观测数据的支持程度                                                         |
| NLL                | 负对数似然                     | 最大似然估计通过最小化 NLL 来拟合参数                                                     |
| D                  | 观测数据集                     | 示例文件 `exampledata.txt` 读入 `data` 后得到；300 行代表 300 个试次，3 列依次为刺激一致性、反应时间和正确性 |
| 正态分布               | 单帧证据波动的概率分布               | 代码从正态分布采样；其均值为 μ，标准差为 σ                                                   |
| `DriftRate`        | 漂移率                       | 代码中由 `k × coh` 计算；大小写应保持一致，正文循环代码另出现 `driftRate`                          |
| `b`                | 模拟代码中的决策边界变量              | 与后文绘图用的 `B` 指同一边界，建议统一成 `B`                                               |
| `z`                | 模拟代码中的起始偏差比例              | 初始证据写为 `evidence = b × z`；与拟合参数 `a` 表示同一相对起始位置，建议统一成 `a`                  |
| `evidence`         | 当前累积证据                    | 模拟中每一步更新的证据值；初始值设为边界与起始偏差比例的乘积                                            |
| `accumEvidence`    | 各帧累积证据的序列                 | 用于保存并绘制整个试次的证据轨迹                                                          |
| `i`                | 当前帧序号                     | 用于记录证据积累进行到第几帧                                                            |
| `data.shape`       | 数据矩阵的行数和列数                | 输出 `(300, 3)`；不是模型参数                                                      |
| `x0`               | 优化器的初始参数向量                | `minimize()` 中的 `(1, 2, 0.5, 0.2)`；                                       |
| `bounds`           | 优化器中各参数的取值范围              | 依次限制漂移系数、决策边界、起始偏差和非决策时间                                                  |
| `res.x`            | 优化得到的参数向量                 | `res.x[0]` 至 `res.x[3]` 分别对应四个拟合参数                                        |
| `pdf()`            | 概率密度函数                    | 根据模型参数和当前试次信息计算概率密度                                                       |
| `ddmpdf()`         | 本节使用的单试次概率密度函数            | 根据当前试次的刺激、反应时间、正确性及模型参数计算联合概率密度                                           |
| `norm.rvs()`       | 从正态分布抽取随机数的函数             | `loc` 对应均值 μ，`scale` 对应标准差 σ，`size` 指定抽样数量                                |
| `np.abs(evidence)` | 累积证据绝对值                   | 用来判断累积证据是否达到决策边界                                                          |
| `np.arange(i+1)`   | 帧序号数组                     | 用作绘图横轴                                                                    |
| `RT`               | 数据文件中的反应时间列名              | 与表中的反应时间符号 `rt` 同义；建议统一符号，保留 `RT` 仅作数据列名说明                                |

## 参考文献

6.4 经典漂移扩散模型

1\.   Ratcliff, R. A theory of memory retrieval. Psychol. Rev. 85, 59–108 (1978).

2\.   Gold, J. I. & Shadlen, M. N. The Neural Basis of Decision Making. Annu. Rev. Neurosci. 30, 535–574 (2007).

3\.   Sun, Y., Lin, Y. & Han, S. Inhibition and updating share common resources: Bayesian evidence from signal detection theory and drift diffusion model. Psychological Research 89, 128 (2025).

4\.   Ratcliff, R. & Tuerlinckx, F. Estimating parameters of the diffusion model: Approaches to dealing with contaminant reaction times and parameter variability. Psychon. B. Rev. 9, 438–481 (2002).

5\.   Kruschke, J. K. & Liddell, T. M. Bayesian data analysis for newcomers. Psychon. B. Rev. 25, 155–177 (2018).

6\.   Vandekerckhove, J., Tuerlinckx, F. & Lee, M. D. Hierarchical diffusion models for two-choice response times. Psychol. Methods 16, 44–62 (2011).

7\.   Shinn, M., Lam, N. H. & Murray, J. D. A flexible framework for simulating and fitting generalized drift-diffusion models. eLife 9, e56938 (2020).
