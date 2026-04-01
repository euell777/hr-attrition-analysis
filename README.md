# HR Employee Attrition Analysis
# HR员工离职分析

## 项目概述 | Project Overview

基于 IBM HR Analytics 数据集（1470名员工，35个特征），分析员工离职的关键影响因素，并构建预测模型。

## 数据集 | Dataset

- **来源**: [IBM HR Analytics Employee Attrition & Performance (Kaggle)](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)
- **规模**: 1470 rows × 35 columns
- **目标变量**: Attrition（离职：Yes/No）
- **整体离职率**: 16.1%

## 核心发现 | Key Findings

### 离职关键因素（按影响力排序）

| 促进离职 | 抑制离职 |
|---------|---------|
| 加班（OverTime）| 总工龄长 |
| 频繁出差 | 环境满意度高 |
| 销售代表/实验室技术员岗位 | 工作满意度高 |
| 长期未晋升 | 年龄较大 |
| 跳槽次数多 | 跟现任经理时间长 |
| 通勤距离远 | 工作生活平衡好 |
| 单身状态 | — |

### 模型表现

| 模型 | Accuracy | AUC | 离职 Recall |
|------|----------|-----|------------|
| 逻辑回归 | 86% | 0.808 | 34% |
| 随机森林 | 83% | 0.745 | 6% |

> 逻辑回归在此场景下表现优于随机森林，AUC 0.808。

## 技术栈 | Tech Stack

- **语言**: Python 3
- **数据处理**: pandas, numpy
- **可视化**: matplotlib, seaborn
- **建模**: scikit-learn（Logistic Regression, Random Forest）

## 项目结构 | Project Structure
```
hr-attrition-analysis/
    ├── data/                           # 数据集
    │   └── WA_Fn-UseC_-HR-Employee-Attrition.csv
    ├── notebooks/                      # 分析笔记本
    │   ├── 01_data_exploration.ipynb   # 数据探索与可视化
    │   └── 02_feature_engineering.ipynb # 特征工程与建模
    ├── .gitignore
    ├── LICENSE
    └── README.md
```
## 运行方式 | How to Run
```bash
git clone https://github.com/euell777/hr-attrition-analysis.git
cd hr-attrition-analysis
pip install pandas numpy matplotlib seaborn scikit-learn
jupyter lab
```

## License

MIT License
