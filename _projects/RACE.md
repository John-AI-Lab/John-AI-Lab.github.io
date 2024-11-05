---
title: RACE Dataset

description: |
  Large-scale reading comprehension dataset designed to evaluate machine understanding of text

layout: project
last-updated: 2017-04-15
---

The **RACE (ReAding Comprehension from Examinations)** dataset is a large-scale reading comprehension dataset designed to evaluate machine understanding of text. It comprises over 28,000 passages and nearly 100,000 questions, collected from English examinations in China intended for middle and high school students.

## Dataset Structure

RACE is divided into two subsets:

- **RACE-M**: Targeted at middle school students.
- **RACE-H**: Targeted at high school students.

Each subset contains passages followed by multiple-choice questions, with four options per question. The dataset is available in Parquet format for efficient data handling. ([huggingface.co](https://huggingface.co/datasets/ehovy/race/tree/main))

{:center: style="text-align: center"}
![image](/img/race/race.png){: width="70%"}
{:center}

## Key Features

- **Diverse Topics**: Passages cover a wide range of subjects, providing a comprehensive assessment of reading comprehension abilities.
- **Multiple Difficulty Levels**: The division into middle and high school levels allows for evaluation across different complexity tiers.
- **Standardized Format**: Consistent structure facilitates straightforward integration into various machine learning models.

## Accessing the Dataset

The RACE dataset is hosted on [Hugging Face Datasets](https://huggingface.co/datasets/ehovy/race) and can be accessed using the `datasets` library:

```python
from datasets import load_dataset

dataset = load_dataset('ehovy/race', 'all')
```

This command loads the entire dataset. To load specific subsets, replace 'all' with 'high' or 'middle'.

## Citation

If you use the RACE dataset in your research, please cite the following paper: [RACE: Large-scale ReAding Comprehension Dataset From Examinations](https://arxiv.org/abs/1704.04683)

```bibtex
@inproceedings{lai-etal-2017-race,
  title = "{RACE}: Large-scale {R}e{A}ding Comprehension Dataset From Examinations",
  author = "Lai, Guokun  and Xie, Qizhe  and Liu, Hanxiao  and Yang, Yiming  and Hovy, Eduard",
  booktitle = "Proceedings of the 2017 Conference on Empirical Methods in Natural Language Processing",
  month = sep,
  year = "2017",
  address = "Copenhagen, Denmark",
  publisher = "Association for Computational Linguistics",
  url = "https://aclanthology.org/D17-1082",
  doi = "10.18653/v1/D17-1082",
  pages = "785--794",
}
```
