# Appendix

## 本章数学符号总结

| 符号或代码名称         | 含义            | 正文中的写法或说明                                 |
| --------------- | ------------- | ----------------------------------------- |
| `accumEvidence` | 累积证据序列        | 保存一个试次中各帧的累积证据，用于绘制证据积累轨迹。                |
| `accuracy`      | 正确率           | 多个试次中，正确反应所占的比例。                          |
| `b`             | 决策边界间距        | 6.4 中下边界为 0，上边界为 `b`；初始证据为 `b × z`。       |
| `B`             | 对称决策阈值        | 6.2—6.3 中，上下决策边界分别表示为 `+B` 和 `−B`。        |
| `bounds`        | 参数取值范围        | 参数拟合时，限定各个待估计参数的取值范围。                     |
| `coh`           | 刺激一致性         | 表示当前试次中运动方向一致的程度；数据文件中的对应列名为 `coherence`。 |
| `correct`       | 当前试次的正确性      | `1` 表示反应正确，`0`表示反应错误。                     |
| `D`             | 观测数据集         | 由多个试次的数据组成，每个试次包含刺激一致性、反应时间和正确性等信息。       |
| `data.shape`    | 数据矩阵的维度       | 表示数据的行数和列数；示例数据的维度为 `(300, 3)`。           |
| `ddmpdf()`      | 单试次概率密度函数     | 根据模型参数和试次信息，计算反应时间与选择结果的联合概率密度。           |
| `evidence`      | 当前累积证据        | 模拟过程中当前时刻的证据值；6.4 中初始值为 `b × z`。          |
| `f`             | 单个点朝目标方向运动的概率 | 用于生成点的运动方向，与刺激一致性有关。                      |
| `i`             | 当前帧序号         | 记录证据积累进行到第几帧。                             |
| `k`             | 漂移系数          | 表示刺激一致性与漂移率之间的比例关系。                       |
| `LL`            | 对数似然          | 衡量一组模型参数对观测数据的支持程度。                       |
| `meanACC`       | 平均正确率         | 多个模拟试次的平均正确率。                             |
| `meanRT`        | 平均反应时间        | 多个模拟试次的平均反应时间。                            |
| `n_dot`         | 每帧的点数         | 模拟随机点运动时，每一帧中呈现的点的数量。                     |
| `N_correct`     | 朝正确方向运动的点数    | 用于统计支持正确方向的运动信息。                          |
| `N_wrong`       | 朝错误方向运动的点数    | 用于统计支持错误方向的运动信息。                          |
| `NLL`           | 负对数似然         | 对数似然的相反数；模型拟合通过最小化负对数似然来估计参数。             |
| `norm.rvs()`    | 正态分布随机抽样函数    | 其中 `loc` 表示均值，`scale`表示标准差，`size`表示抽样数量。  |
| `pdf()`         | 概率密度函数        | 根据模型参数和试次信息计算概率密度。                        |
| `res.x`         | 拟合得到的参数向量     | 保存优化过程得到的各个模型参数估计值。                       |
| `rt`            | 当前试次的反应时间     | 反应时间在数据文件中的列名为 `RT`。                      |
| `T`             | 时间或模拟时长       | 表示模拟中的时间长度，具体取值由所在代码段定义。                  |
| `t_nd`          | 非决策时间         | 刺激编码、反应执行等非证据积累过程所需的时间；代码中也写作 `ndt`。      |
| `v`             | 漂移率           | 表示证据积累的平均方向和速度；6.4 的代码中使用 `v = k × coh`。  |
| `x0`            | 初始参数向量        | 参数优化开始时使用的一组初始值。                          |
| `z`             | 相对起始位置        | 表示证据积累的起点在上下边界之间的相对位置；初始证据为 `b × z`。      |
| `θ`             | 模型参数向量        | 包含拟合所需的一组参数，如漂移系数、决策边界、起始位置和非决策时间。        |
| `μ`             | 证据增量的均值       | 正态分布的均值，用于描述证据增量的平均水平。                    |
| `σ`             | 证据增量的标准差      | 正态分布的标准差，用于描述证据增量的波动程度。                   |

## 本章参考文献

1. Gold, J. I. & Shadlen, M. N. Neural computations that underlie decisions about sensory stimuli. _Trends in Cognitive Sciences_ **5**, 10–16 (2001).
2. Ratcliff, R. A theory of memory retrieval. _Psychological Review_ **85**, 59–108 (1978).
3. Gold, J. I. & Shadlen, M. N. The neural basis of decision making. _Annual Review of Neuroscience_ **30**, 535–574 (2007).
4. Sun, Y., Lin, Y. & Han, S. Inhibition and updating share common resources: Bayesian evidence from signal detection theory and drift diffusion model. _Psychological Research_ **89**, 128 (2025).
5. Ratcliff, R. & Tuerlinckx, F. Estimating parameters of the diffusion model: Approaches to dealing with contaminant reaction times and parameter variability. _Psychonomic Bulletin & Review_ **9**, 438–481 (2002).
6. Kruschke, J. K. & Liddell, T. M. Bayesian data analysis for newcomers. _Psychonomic Bulletin & Review_ **25**, 155–177 (2018).
7. Vandekerckhove, J., Tuerlinckx, F. & Lee, M. D. Hierarchical diffusion models for two-choice response times. _Psychological Methods_ **16**, 44–62 (2011).
8. Shinn, M., Lam, N. H. & Murray, J. D. A flexible framework for simulating and fitting generalized drift-diffusion models. _eLife_ **9**, e56938 (2020).
9. White, C. N., Ratcliff, R., Vasey, M. W. & McKoon, G. Using diffusion models to understand clinical disorders. _Journal of Mathematical Psychology_ **54**, 39–52 (2010).
10. Lawlor, V. M. et al. Dissecting the impact of depression on decision-making. _Psychological Medicine_ **50**, 1613–1622 (2020).
11. Ozturk, S. et al. Knowledge of threat biases perceptual decision making in anxiety: Evidence from signal detection theory and drift diffusion modeling. _Biological Psychiatry: Global Open Science_ **4**, 145–154 (2024).
12. Dillon, D. G., Lazarov, A., Dolan, S., Bar-Haim, Y., Pizzagalli, D. A. & Schneier, F. R. Fast evidence accumulation in social anxiety disorder enhances decision making in a probabilistic reward task. _Emotion_ **22**, 1–18 (2022).
13. Smucny, J., Hanks, T. D., Lesh, T. A. & Carter, C. S. Altered associations between task performance and dorsolateral prefrontal cortex activation during cognitive control in schizophrenia. _Biological Psychiatry: Cognitive Neuroscience and Neuroimaging_ **8**, 1050–1057 (2023).
14. Shen, C., Calvin, O. L., Rawls, E., Redish, A. D. & Sponheim, S. R. Clarifying cognitive control deficits in psychosis via drift diffusion modeling and attractor dynamics. _Schizophrenia Bulletin_ **50**, 1357–1370 (2024).
15. Chen, Y., Liu, Y., Wang, Z., Yang, T. & Fan, Q. Accumulation of evidence during decision making in OCD patients. _Frontiers in Psychiatry_ **13**, 980905 (2022).
16. Grennan, G., Zhao, Y. & Fang, A. Applying a drift diffusion model to test the effect of oxytocin on attentional biases in body dysmorphic disorder. _Journal of Obsessive-Compulsive and Related Disorders_ **39**, 100841 (2023).
17. Pirrone, A., Dickinson, A., Gomez, R., Stafford, T. & Milne, E. Understanding perceptual judgment in autism spectrum disorder using the drift diffusion model. _Neuropsychology_ **31**, 173–180 (2017).
18. Sripada, C. & Weigard, A. Impaired evidence accumulation as a transdiagnostic vulnerability factor in psychopathology. _Frontiers in Psychiatry_ **12**, 627179 (2021).
19. Hutcherson, C. A., Bushong, B. & Rangel, A. A neurocomputational model of altruistic choice and its implications. _Neuron_ **87**, 451–462 (2015).
20. Krajbich, I., Bartling, B., Hare, T. & Fehr, E. Rethinking fast and slow based on a critique of reaction-time reverse inference. _Nature Communications_ **6**, 7455 (2015).
21. Chen, F. & Krajbich, I. Biased sequential sampling underlies the effects of time pressure and delay in social decision making. _Nature Communications_ **9**, 3557 (2018).
22. Son, J.-Y., Bhandari, A. & FeldmanHall, O. Crowdsourcing punishment: Individuals reference group preferences to inform their own punitive decisions. _Scientific Reports_ **9**, 11625 (2019).
23. Yu, H., Siegel, J. Z., Clithero, J. A. & Crockett, M. J. How peer influence shapes value computation in moral decision-making. _Cognition_ **211**, 104641 (2021).
24. Ghaffari, M. & Fiedler, S. The power of attention: Using eye gaze to predict other-regarding and moral choices. _Psychological Science_ **29**, 1878–1889 (2018).
25. Smith, S. M. & Krajbich, I. Gaze amplifies value in decision making. _Psychological Science_ **30**, 116–128 (2019).
