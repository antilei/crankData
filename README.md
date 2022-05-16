# 民科化程度评测数据集（2022 年第 1 版）

本数据集收录 2022 年 3 月以来百度民科吧部分吧友根据《民科化程度综合评价量表（1.1 版）》对部分民科的民科化程度评测结果。

数据集文件为 `crankData.csv`。

## 数据集解释

数据集共收录 44 条评价数据，每条为 1 行，每行由 30 列的内容构成。

每列的内容及含义如下：

| 列数 | 列名        | 数据类型及格式      | 描述                                     |
|:----|:-----------|:------------------|:-----------------------------------------|
| 1   | 序号        | 正整数（序数）      | 该行评价结果的序号                          |
| 2   | 评价时间     | `YYYY/MM/DD`     | 该行评价结果的评价时间                       |
| 3   | 评价人ID     | `id` + 8 位随机数 | 不同的 ID 代表不同的评价人                   |
| 4   | 民科姓名     | 字符串            | 被评测民科的姓名或网名，已人工排查一人多名的情况 |
| 5   | Q1_双重标准  | 正整数 0~4        | 第 1 个评价问题的得分                       |
| 6   | Q2_批判反问  | 正整数 0~4        | 第 2 个评价问题的得分                       |
| 7   | Q3_转移话题  | 正整数 0~4        | 第 3 个评价问题的得分                       |
| 8   | Q4_首先攻击  | 正整数 0~4        | 第 4 个评价问题的得分                       |
| 9   | Q5_复读装死  | 正整数 0~4        | 第 5 个评价问题的得分                       |
| 10  | Q6_删评拉黑  | 正整数 0~4        | 第 6 个评价问题的得分                       |
| 11  | Q7_钻牛角尖  | 正整数 0~4        | 第 7 个评价问题的得分                       |
| 12  | Q8_死不认错  | 正整数 0~4        | 第 8 个评价问题的得分                       |
| 13  | Q9_围攻纠缠  | 正整数 0~4        | 第 9 个评价问题的得分                       |
| 14  | Q10_目无法纪 | 正整数 0~4        | 第 10 个评价问题的得分                      |
| 15  | Q11_逾越底线 | 正整数 0~4        | 第 11 个评价问题的得分                      |
| 16  | Q12_毒害学生 | 正整数 0~4        | 第 12 个评价问题的得分                      |
| 17  | Q13_低俗辱骂 | 正整数 0~4        | 第 13 个评价问题的得分                      |
| 18  | Q14_骚扰诽谤 | 正整数 0~4        | 第 14 个评价问题的得分                      |
| 19  | Q15_诋毁学者 | 正整数 0~4        | 第 15 个评价问题的得分                      |
| 20  | Q16_抄袭剽窃 | 正整数 0~4        | 第 16 个评价问题的得分                      |
| 21  | Q17_复读装死 | 正整数 0~4        | 第 17 个评价问题的得分                      |
| 22  | Q18_理论空洞 | 正整数 0~4        | 第 18 个评价问题的得分                      |
| 23  | Q19_水平低下 | 正整数 0~4        | 第 19 个评价问题的得分                      |
| 24  | Q20_语言障碍 | 正整数 0~4        | 第 20 个评价问题的得分                      |
| 25  | Q21_逻辑混乱 | 正整数 0~4        | 第 21 个评价问题的得分                      |
| 26  | Q22_自吹自擂 | 正整数 0~4        | 第 22 个评价问题的得分                      |
| 27  | Q23_大喊口号 | 正整数 0~4        | 第 23 个评价问题的得分                      |
| 28  | Q24_认知混乱 | 正整数 0~4        | 第 24 个评价问题的得分                      |
| 29  | Q25_痴心妄想 | 正整数 0~4        | 第 25 个评价问题的得分                      |
| 30  | 总分        | 正整数 0~100      | 上述 25 个问题的总得分                      |

注：

1. 评价人 ID 是基于收到问卷的 IP 赋予的（考虑到隐私问题），不同的 ID 号代表一个不同的 IP 来源，象征着不同的评价人；相同的 IP 视为相同的评价人。
2. “已人工排查一人多名的情况”，是指对于当一个民科的多个名称出现在收集到的数据中时，统一替换为其中一个名称。
3. 第 5 ~ 29 列对应的具体问题见下文。

## 评测问卷内容

评测所用问卷《民科化程度综合评价量表（1.1 版）》由 25 个问题构成，每个问题的最高分为 4 分，最低分为 0 分。这些问题分别对应数据集的第 5 ~ 29 列。

每个问题给出一个描述，评价者需要判断该描述对于被评价民科的符合程度，分为完全符合（4 分）、基本符合（3 分）、有时符合（2 分）、略符合（1 分）和不符合（0 分）五个档次。将每个描述的符合程度对应的分数相加，就得到了该民科的民科化程度总分数。

现将这些问题列举如下：

| 问题序号 | 对应数据集列数 | 对应数据集列名 | 问题描述 |
|:--------|:----|:----|:----|
| 1   | 5   | Q1_双重标准  | 在讨论问题时，该民科常常出现双重标准。                                                        |
| 2   | 6   | Q2_批判反问  | 在讨论问题时，该民科的第一反应往往是批判题目或者反问提问者。                                      |
| 3   | 7   | Q3_转移话题  | 在讨论问题 A 时，该民科经常转移话题到另一个问题 B。                                             |
| 4   | 8   | Q4_首先攻击  | 在讨论问题时，该民科常常首先进行人身攻击。                                                     |
| 5   | 9   | Q5_复读装死  | 在讨论问题时，该民科喜欢复读自己的问题或观点，而对其他人的回复视而不见。                            |
| 6   | 10  | Q6_删评拉黑  | 该民科常常使用删评、拉黑等手段针对反对者。                                                     |
| 7   | 11  | Q7_钻牛角尖  | 该民科分不清不同因素对某现象的影响强弱，或者自己虚构一些影响因素，通过钻牛角尖的方式反驳对方。          |
| 8   | 12  | Q8_死不认错  | 当自己的理论与客观事实出现非专业人员都能发觉的明显矛盾时，该民科仍然不会修改或放弃自己的理论。          |
| 9   | 13  | Q9_围攻纠缠  | 该民科常常纠集大量其他民科，对反对者进行围攻；或者在其他民科的帖子下常常出现，只为攻击经常反对他的人。    |
| 10  | 14  | Q10_目无法纪 | 该民科不具备基本的道德和法律意识。                                                            |
| 11  | 15  | Q11_逾越底线 | 为了维护自己的理论或打击反对者，该民科可以逾越自己已经意识到的道德和法律底线。                       |
| 12  | 16  | Q12_毒害学生 | 该民科常常向在读学生宣传自己的错误理论。                                                       |
| 13  | 17  | Q13_低俗辱骂 | 该民科常常使用低俗的词汇对吧友进行辱骂。                                                       |
| 14  | 18  | Q14_骚扰诽谤 | 该民科对吧友存在性骚扰、诽谤、生命威胁等严重的侵犯人格尊严的行为。                                  |
| 15  | 19  | Q15_诋毁学者 | 该民科常常随意攻击和否定科学家的人格或学术道德。                                                 |
| 16  | 20  | Q16_抄袭剽窃 | 该民科常常抄袭他人的智力成果，并声称为自己的原创。                                               |
| 17  | 21  | Q17_复读装死 | 该民科使用人肉、挂人等方式骚扰吧友。                                                           |
| 18  | 22  | Q18_理论空洞 | 该民科没有系统的理论内容。                                                                   |
| 19  | 23  | Q19_水平低下 | 该民科的理科知识水平在初中以下。                                                              |
| 20  | 24  | Q20_语言障碍 | 该民科在语言理解与表达方面存在一定障碍。                                                       |
| 20  | 25  | Q21_逻辑混乱 | 该民科逻辑混乱，在阐述自己的观点时常犯循环论证、因果不分等逻辑谬误。                                |
| 21  | 26  | Q22_自吹自擂 | 该民科经常使用过度夸大的语言自吹自擂。                                                         |
| 22  | 27  | Q23_大喊口号 | 该民科准备了大量的用于自吹自擂或辱骂攻击反对者的口号，并四处复制粘贴宣传。                           |
| 23  | 28  | Q24_认知混乱 | 该民科看上去已经出现了自我认知的混乱，尽管这可能只是为了炒作。                                     |
| 24  | 29  | Q25_痴心妄想 | 该民科对名利、荣誉、爱情等有严重不切实际的幻想，并成立“粉丝群”“后援会”等组织来构建和维持一个虚幻的形象。 |

## 其他

1. 本数据集目前样本数尚小，且由于问题设计的局限性，主观性可能较大。欢迎大家来[这个贴子](https://tieba.baidu.com/p/7774936121)填写问卷和提出意见建议！
2. 考虑到可读性，数据集使用了中文字符（UTF-8 编码）。如分析环境要求纯英文字符，请自行对数据集进行预处理。
