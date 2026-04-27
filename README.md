# Machine Learning-Assisted Screening of Antioxidant Nanozymes  
# 机器学习辅助抗氧化纳米酶活性预测与筛选

This repository contains the code and datasets used for an undergraduate thesis project on machine learning-assisted prediction and screening of antioxidant nanozymes. The project focuses on nanozymes with superoxide dismutase-like (SOD-like) and catalase-like (CAT-like) activities, aiming to support the discovery of bifunctional antioxidant nanozymes with desirable activity profiles.

本仓库包含本科毕业设计中使用的代码与数据文件，主要用于抗氧化纳米酶的机器学习建模、活性预测和候选材料筛选。研究重点包括超氧化物歧化酶样活性（SOD-like activity）和过氧化氢酶样活性（CAT-like activity），并结合多种酶样活性指标进行综合筛选分析。

---

## Project Overview

Nanozymes are nanomaterials that mimic the catalytic functions of natural enzymes and have broad potential in reactive oxygen species (ROS) scavenging and oxidative stress regulation. Among them, bifunctional antioxidant nanozymes with both SOD-like and CAT-like activities are closer to the natural stepwise ROS elimination process.

In this project, activity data of nanozymes were collected from published literature, including SOD-like, CAT-like, POD-like, and OXD-like activities. Machine learning models were constructed for activity prediction, model evaluation, feature interpretation, and candidate screening.

The main objectives of this project are:

1. To collect and organize nanozyme activity data from published literature.
2. To construct machine learning models for SOD-like and CAT-like activity prediction.
3. To evaluate model performance using grouped cross-validation based on literature sources.
4. To analyze important material features related to nanozyme activity.
5. To conduct joint screening of candidate nanozymes with desirable antioxidant activity profiles.

---

## Repository Structure

```text
.
├─ README.md
├─ requirements.txt
├─ .gitignore
├─ notebooks/
│  ├─ 01_SOD_Nanozyme_Model_Training.ipynb
│  ├─ 02_CAT_Nanozyme_Model_Training.ipynb
│  └─ 03_Screening_and_Analysis.ipynb
└─ data/
   ├─ data-sod.xlsx
   ├─ data-cat.xlsx
   ├─ data-pod.xlsx
   └─ data-oxd.xlsx
```

---

## Files

### Notebooks

#### `01_SOD_Nanozyme_Model_Training.ipynb`

This notebook is used for model training, evaluation, and interpretation of SOD-like nanozyme activity. It includes data preprocessing, feature processing, model construction, cross-validation, performance evaluation, and model interpretation.

#### `02_CAT_Nanozyme_Model_Training.ipynb`

This notebook is used for model training, evaluation, and interpretation of CAT-like nanozyme activity. It includes classification and regression modeling for CAT-related activity indicators, grouped cross-validation, and feature importance analysis.

#### `03_Screening_and_Analysis.ipynb`

This notebook is used for integrated screening and analysis of candidate nanozymes. It combines information from multiple enzyme-like activity datasets and performs joint evaluation of candidate materials.

---

### Data Files

#### `data-sod.xlsx`

Dataset for SOD-like nanozyme activity.

#### `data-cat.xlsx`

Dataset for CAT-like nanozyme activity.

#### `data-pod.xlsx`

Dataset for POD-like nanozyme activity.

#### `data-oxd.xlsx`

Dataset for OXD-like nanozyme activity.

---

## Environment

The code was developed using Python and Jupyter Notebook. The main packages used in this project include:

```text
numpy
pandas
scikit-learn
xgboost
catboost
shap
matplotlib
openpyxl
joblib
jupyter
```

To install the required packages, run:

```bash
pip install -r requirements.txt
```

---

## Usage

Clone this repository:

```bash
git clone https://github.com/your-username/nanozyme-activity-prediction.git
cd nanozyme-activity-prediction
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run the notebooks in the following order:

```text
1. notebooks/01_SOD_Nanozyme_Model_Training.ipynb
2. notebooks/02_CAT_Nanozyme_Model_Training.ipynb
3. notebooks/03_Screening_and_Analysis.ipynb
```

Before running the notebooks, please make sure that all data files are placed in the `data/` folder.

---

## Important Notes

Some paths in the original local notebooks may need to be adjusted before running on another computer. It is recommended to use relative paths such as:

```python
from pathlib import Path

PROJECT_ROOT = Path.cwd()
if PROJECT_ROOT.name == "notebooks":
    PROJECT_ROOT = PROJECT_ROOT.parent

DATA_DIR = PROJECT_ROOT / "data"
RESULTS_DIR = PROJECT_ROOT / "results"

SOD_PATH = DATA_DIR / "data-sod.xlsx"
CAT_PATH = DATA_DIR / "data-cat.xlsx"
POD_PATH = DATA_DIR / "data-pod.xlsx"
OXD_PATH = DATA_DIR / "data-oxd.xlsx"
```

Avoid using local absolute paths such as:

```text
C:\Users\...\Desktop\...
```

because these paths are only valid on the original computer and cannot be used by other users.

---

## Output

The notebooks may generate model evaluation results, figures, feature importance files, SHAP analysis results, and candidate screening results. These output files can be saved in a `results/` folder.

Large intermediate files and trained model files are not necessarily included in this repository.

---

## Thesis Information

This repository supports the undergraduate thesis project:

**机器学习辅助双功能抗氧化纳米酶活性预测与筛选**  
**Machine Learning-Assisted Prediction and Screening of Bifunctional Antioxidant Nanozymes**

---

## Author

Zibin Chu
Beijing University of Chemical Technology  
Bioengineering + Data Science / Big Data Management

---

## License

This repository is intended for academic research and thesis-related demonstration. Please cite or acknowledge this repository if you use the code or data structure for related research.
