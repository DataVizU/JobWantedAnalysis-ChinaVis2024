# Job Wanted Analysis for ChinaVis2024
## 项目简介
本项目为[第十一届中国可视化与可视分析大会（ChinaVis 2024）数据可视化竞赛](https://www.chinavis.org/2024/challenge.html)赛道一选题2的参赛作品。项目基于题设要求设计了一个基于机器学习和统计分析的招聘广告大数据可视化系统，该系统采用数据挖掘、聚类分析等技术，处理题目所给的数十万条招聘信息，实现了职位差异度量化评估、多角度职位画像展示、薪酬待遇模式分析、地域招聘活动特征挖掘，以及行业发展动态和新兴职位识别等功能。研究发现，职位差异可通过多角度多维属性有效量化，**薪酬待遇与职位、行业、地域呈现显著相关性，地域招聘活动展现出明显的产业集群特征**。同时，**基于薪酬水平、学历和经验要求能发现急需人才的新兴职位**。

## 数据简介
出题方所提供的数据集包含430,664条详尽的招聘通知，覆盖了169,540种多样化的职位、267,296家不同企业、158个行业类别，并涵盖了371个行政区划。原始数据详见[JobWanted](./data/raw/JobWanted.csv)。

由于原始数据中设置了缺失值、异常值或数据不一致等噪声信息（例如无效的薪酬、缺失的行业类别等），项目将缺失数据补全，并对**薪酬模式**部分进行预处理，剔除异常数据并将格式统一。预处理后数据详见[SalaryFinal](./data/final/SalaryFinal.csv)。根据薪酬的不同模式，项目进一步将招聘通知分为**固定用工招聘通知**和**灵活用工招聘通知**，分别存放于[FixedSalaryFinal](./data/final/FixedSalaryFinal.csv)和[FlexSalaryFinal](./data/final/FlexSalaryFinal.csv)。

我们发现，本数据具有较明显的长尾效应。考虑到出现次数较少的招聘信息不具有可被分析的规律，我们仅选取排序前10%的招聘信息作为分析对象，分割后数据存放于[Top1PercentJobWanted](./data/filtered/Top1PercentJobWanted.csv)。

## 可视化概览
![比赛图片](https://github.com/user-attachments/assets/433f44f3-6c4f-48f8-bc60-6c8d7b5a9958)

## 项目答卷
数据处理、可视设计与结论分析等具体内容详见[📄FinalSheet](./FinalSheet-ChinaVisData2024.pdf)。
