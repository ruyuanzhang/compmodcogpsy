---
description: Appendix
---

# Appendix

## 本章参考文献

1. Tversky, A., & Kahneman, D. (1979). Prospect theory: An analysis of decision under risk. In _Handbook of the fundamentals of financial decision making: Part I_ (pp. 99-127).
2. Tversky, A., & Kahneman, D. (1992). Advances in prospect theory: Cumulative representation of uncertainty. Journal of Risk and Uncertainty, 5(4), 297-323. https://doi.org/10.1007/BF00122574
3. Prelec, D. (1998). The probability weighting function. Econometrica, 497-527. https://doi.org/doi.org/10.2307/2998573
4. Goldstein, W. M., & Einhorn, H. J. (1987). Expression theory and the preference reversal phenomena. _Psychological review_, _94_(2), 236.  https://doi.org/1987-20947-001
5. Zhang, H., & Maloney, L. T. (2012). Ubiquitous log odds: a common representation of probability and frequency distortion in perception, action, and cognition. Front Neurosci, 6, 1. https://doi.org/10.3389/fnins.2012.00001
6. Peterson, J. C., Bourgin, D. D., Agrawal, M., Reichman, D., & Griffiths, T. L. (2021). Using large-scale experiments and machine learning to discover theories of human decision-making. Science, 372(6547), 1209. https://doi.org/10.1126/science.abe2629
7. Wallsten, T. S., Pleskac, T. J., & Lejuez, C. W. (2005). Modeling behavior in a clinically diagnostic sequential risk-taking task. Psychological review, 112(4), 862-880. https://doi.org/10.1037/0033-295X.112.4.862
8. Figner, B., Mackinlay, R. J., Wilkening, F., & Weber, E. U. (2009). Affective and deliberative processes in risky choice: age differences in risk taking in the Columbia Card Task. Journal of Experimental Psychology: Learning, Memory, and Cognition, 35(3), 709. https://doi.org/10.1037/a0014983
9. Frey, R., Pedroni, A., Mata, R., Rieskamp, J., & Hertwig, R. (2017). Risk preference shares the psychometric structure of major psychological traits. Science Advances, 3(10), e1701381. https://doi.org/10.1126/sciadv.1701381
10. Zilker, V., & Pachur, T. (2023). Attribute attention and option attention in risky choice. Cognition, 236, 105441. https://doi.org/10.1016/j.cognition.2023.105441
11. Pachur, T., Schulte-Mecklenbeck, M., Murphy, R. O., & Hertwig, R. (2018). Prospect theory reflects selective allocation of attention. Journal of Experimental Psychology: General, 147(2), 147-169. https://doi.org/10.1037/xge0000406
12. Krefeld-Schwalb, A., Pachur, T., & Scheibehenne, B. (2022). Structural parameter interdependencies in computational models of cognition. Psychological review, 129(2), 313-339. https://doi.org/10.1037/rev0000285
13. Barretto-Garcia, M., de Hollander, G., Grueschow, M., Polania, R., Woodford, M., & Ruff, C. C. (2023). Individual risk attitudes arise from noise in neurocognitive magnitude representations. Nature Human Behaviour, 7(9), 1551-1567. https://doi.org/10.1038/s41562-023-01643-4
14. Zhang, H., Ren, X., & Maloney, L. T. (2020). The bounded rationality of probability distortion. Proceedings of National Academy of Sciences, 117(36), 22024-22034. https://doi.org/10.1073/pnas.1922401117
15. Zhu, J.-Q., Xie, H., Arumugam, D., Wilson, R., & Griffiths, T. L. (2026). Using reinforcement learning to train large language models to explain human decisions. International Conference on Learning Representations.



## 逆温参数名字的来源

逆温参数这个名称来自统计物理学中的玻尔兹曼分布。玻尔兹曼分布把一个系统处于状态 i 的概率写为：

$$
P(i) ∝ exp[−E(i)/(kT)]
$$

其中 $$E(i)$$是该状态的能量，T 是温度。温度较高时，不同状态的概率变得相近，系统更容易随机地进入高能量状态；温度较低时，概率则集中于能量最低的状态。如果把主观价值理解为负的能量，即 $$V(i) = −E(i)$$，并把常数 k 合并到参数中，就可以得到：

$$
P(i) ∝ exp[θV(i)]
$$

其中 $$θ$$ 与 $$1/T$$ 成正比。因此，较大的 $$\theta$$对应较低的温度和更加确定的选择，较小的 $$\theta$$对应较高的温度和更加随机的选择。这就是选择敏感参数被称为“逆温参数”的原因。



