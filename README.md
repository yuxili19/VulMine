# Uncovering Logit Suppression Vulnerabilities in LLM Safety Alignment

## Introduction

Large language models (LLMs) have revolutionized various
applications, making robust safety alignment essential to prevent harmful
outputs. Current safety alignment techniques, however, harbor inherent
vulnerabilities due to their reliance on logit suppression. In this work,
we identify critical logit-level vulnerabilities by introducing Semantic-
sensitive Alignment and Generation (SSAG), a method designed to sys-
tematically manipulate output-layer logits without altering model pa-
rameters. Experiments on five popular LLMs show that SSAG exposes
harmful responses with a 95% success rate while reducing response time
by 86%. These findings reveal crucial weaknesses in existing alignment
methods, highlighting an urgent need for improved vulnerability detec-
tion and robust safety alignment strategies. The Appendix of our paper are presented [here](Appendix.pdf).

## Installation

To get started, clone this repository and install the required dependencies:

```bash
git clone https://github.com/yuxili19/JailMine.git
cd JailMine
pip install -r requirements.txt
```

## Dataset and Models

The two datasets that we use in our experiment are presented in [VulMine/datasets](https://github.com/yuxili19/VulMine/tree/main/datasets). Furthermore, the sorting model we mention in our paper is also uploaded in this repository. 

## Usage

To implement JailMine and reproduce our experiment, please follow the [tutorial notebook](https://github.com/yuxili19/VulMine/blob/main/Tutorial.ipynb). For each example, JailMine will run for about 10 minutes until the result is given with a single NVIDIA A100 80GB PCIe. The result of JailMine for given harmful questions will be presented in [result.csv](https://github.com/yuxili19/VulMine/blob/main/result.csv).
