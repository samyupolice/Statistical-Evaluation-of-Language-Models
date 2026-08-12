# A Statistical Approach to Evaluating Language Models: GPT-2 vs DistilGPT2

## Overview

This project presents a statistical approach to evaluating and comparing two transformer-based language models: GPT-2 and DistilGPT2.

The main objective is to investigate whether a smaller distilled model can achieve performance comparable to the original larger model.

Both models are evaluated using the same dataset of factual question-answer pairs. Their generated responses are evaluated for correctness and analysed using multiple statistical techniques.

The project goes beyond basic accuracy by analysing:

- Accuracy
- Variance
- Standard Deviation
- Bootstrap Confidence Intervals
- Hypothesis Testing

This provides a broader understanding of model performance, variability, reliability, and statistical significance.

---

## Project Title

**A Statistical Approach to Evaluating Language Models: A Comparative Study of GPT-2 and DistilGPT2**

---

## Problem Statement

Language models can produce different levels of performance depending on the dataset and inputs used for evaluation.

Traditional model comparison often relies on a single metric such as accuracy. However, differences in accuracy may occur because of dataset variation, sampling, or other experimental factors.

Therefore, evaluating models using additional statistical measures can provide a more reliable understanding of their performance.

This project investigates whether statistical evaluation methods can provide stronger evidence when comparing GPT-2 and DistilGPT2.

---

## Research Question

**Can a smaller distilled model achieve performance comparable to the original larger model?**

To answer this question, GPT-2 and DistilGPT2 are evaluated using the same factual-question dataset and statistical evaluation procedure.

---

## Objectives

The main objectives of this project are:

- Evaluate GPT-2 using a factual question dataset.
- Evaluate DistilGPT2 using the same dataset.
- Compare the accuracy of both language models.
- Analyse the variance of model performance.
- Calculate standard deviation.
- Estimate confidence intervals using bootstrap sampling.
- Perform statistical hypothesis testing.
- Determine whether the observed performance difference is statistically significant.
- Analyse the trade-off between model performance and model size.

---

## Models Used

### GPT-2

GPT-2 is a transformer-based generative language model developed by OpenAI.

It generates coherent and contextually appropriate text based on patterns learned from large-scale internet text.

### DistilGPT2

DistilGPT2 is a smaller version of GPT-2 created using knowledge distillation.

Knowledge distillation involves training a smaller student model to imitate the behaviour of a larger teacher model.

The goal is to reduce model size and computational requirements while attempting to maintain similar language-generation capabilities.

---

## Model Comparison

| Model | Type | Description |
|---|---|---|
| GPT-2 | Transformer Language Model | Original larger model with high capacity |
| DistilGPT2 | Distilled Transformer Model | Smaller compressed version of GPT-2 |

Comparing the two models provides an opportunity to investigate whether model compression can reduce computational requirements without significantly degrading performance.

---

## Dataset

The experiment uses a dataset of factual question-answer pairs.

The questions cover general knowledge topics including:

- Geography
- Science
- History
- Literature

Example questions include:

- What is the capital of France?
- Who wrote the novel 1984?
- What is the largest ocean on Earth?
- Which planet is known as the Red Planet?

The questions were designed to be simple and factual so that the generated responses could be checked for correctness.

Each question was provided to both GPT-2 and DistilGPT2, and the generated responses were collected for analysis.

---

## Experimental Design

Both models are evaluated under the same conditions.

The experiment uses:

- The same factual-question dataset
- The same questions
- The same evaluation process
- The same statistical analysis methods
- The same evaluation criteria

Using the same dataset and evaluation procedure helps provide a consistent comparison between GPT-2 and DistilGPT2.

---

## Experimental Workflow

The complete workflow is:

Dataset Preparation
↓
Load GPT-2
↓
Load DistilGPT2
↓
Generate Responses
↓
Evaluate Response Correctness
↓
Calculate Accuracy
↓
Calculate Variance
↓
Calculate Standard Deviation
↓
Bootstrap Sampling
↓
Confidence Interval Estimation
↓
Hypothesis Testing
↓
Model Comparison

---

## Response Generation

For each factual question:

1. The question is provided to GPT-2.
2. GPT-2 generates a response.
3. The response is evaluated against the expected answer.
4. The same question is provided to DistilGPT2.
5. DistilGPT2 generates a response.
6. The response is evaluated using the same correctness criteria.

The resulting correctness scores are used for the statistical analysis.

---

## Evaluation Metrics

### Accuracy

Accuracy measures the proportion of questions answered correctly by each model.

It is calculated as:

Accuracy = Correct Responses / Total Responses

Accuracy provides the basic performance measure used to compare the two models.

---

### Variance

Variance measures how spread out the model's performance results are around the average.

A higher variance indicates that performance varies more across the evaluated samples.

---

### Standard Deviation

Standard deviation is the square root of variance.

It provides a more interpretable measure of performance variability because it is expressed on the same scale as the evaluation metric.

A lower standard deviation indicates more consistent performance.

---

### Bootstrap Confidence Intervals

Confidence intervals provide an estimated range in which the true model performance is likely to fall.

Bootstrap sampling is used to estimate these intervals.

The bootstrap process repeatedly samples the model scores with replacement and calculates the mean accuracy for each sample.

The resulting distribution is then used to estimate the confidence interval.

The project uses the 2.5th and 97.5th percentiles for the confidence interval.

---

### Hypothesis Testing

Hypothesis testing is used to determine whether the observed performance difference between GPT-2 and DistilGPT2 is statistically significant.

#### Null Hypothesis (H₀)

There is no significant difference between the performance of GPT-2 and DistilGPT2.

#### Alternative Hypothesis (H₁)

There is a significant difference between the performance of GPT-2 and DistilGPT2.

The statistical test calculates a p-value to determine whether the observed difference is likely to have occurred due to random variation.

---

## Implementation Environment

The project was implemented using:

- Python
- Google Colab
- Hugging Face Transformers
- NumPy
- Matplotlib
- SciPy

The Transformers library is used for loading the language models, NumPy is used for numerical calculations, Matplotlib is used for visualization, and SciPy is used for statistical testing.

---

## Statistical Analysis Implementation

The project implements bootstrap sampling by repeatedly drawing samples with replacement.

For each bootstrap sample, the mean accuracy is calculated.

The resulting bootstrap distributions are used to estimate confidence intervals.

The project then performs hypothesis testing using the bootstrap distributions.

The implementation uses an independent t-test to calculate the test statistic and p-value.

The final results table contains:

- Model
- Accuracy
- Variance
- Standard Deviation
- Confidence Interval Lower Bound
- Confidence Interval Upper Bound
- P-value

---

## Results

### Accuracy Comparison

| Model | Accuracy |
|---|---:|
| GPT-2 | 0.12 |
| DistilGPT2 | 0.06 |

GPT-2 achieved higher accuracy than DistilGPT2 on the selected factual-question dataset.

GPT-2 correctly answered approximately 12% of the questions, while DistilGPT2 achieved approximately 6% accuracy.

---

## Variance and Standard Deviation

| Model | Variance | Standard Deviation |
|---|---:|---:|
| GPT-2 | 0.1056 | 0.3249 |
| DistilGPT2 | 0.0564 | 0.2375 |

GPT-2 achieved higher accuracy but also showed slightly higher variance than DistilGPT2.

This indicates that GPT-2 performed better overall, while its performance varied slightly more across the evaluated samples.

DistilGPT2 showed lower variance and standard deviation, indicating more stable performance within the experiment.

---

## Bootstrap Confidence Intervals

| Model | Lower Bound | Upper Bound |
|---|---:|---:|
| GPT-2 | 0.04 | 0.20 |
| DistilGPT2 | 0.00 | 0.14 |

The confidence interval for GPT-2 ranges from 0.04 to 0.20.

The confidence interval for DistilGPT2 ranges from 0.00 to 0.14.

Although the confidence intervals show some overlap, the hypothesis-testing result indicates a statistically significant difference between the models within this experiment.

---

## Hypothesis Testing Results

| Comparison | P-value |
|---|---:|
| GPT-2 vs DistilGPT2 | 0.0000 |

The reported p-value is very small.

Based on the statistical test used in the project, the difference in accuracy between GPT-2 and DistilGPT2 is statistically significant.

This indicates that the observed performance difference is unlikely to be explained by random variation alone within the experimental setup.

---

## Key Findings

The main findings of the project are:

- GPT-2 achieved higher accuracy than DistilGPT2.
- GPT-2 achieved an accuracy of 0.12.
- DistilGPT2 achieved an accuracy of 0.06.
- GPT-2 had higher variance than DistilGPT2.
- GPT-2 had a standard deviation of 0.3249.
- DistilGPT2 had a standard deviation of 0.2375.
- GPT-2 had a bootstrap confidence interval of 0.04–0.20.
- DistilGPT2 had a bootstrap confidence interval of 0.00–0.14.
- The reported hypothesis test produced a p-value of 0.0000.
- The statistical analysis indicates a significant performance difference between the two models.
- GPT-2 performed better on the selected factual-question dataset.
- DistilGPT2 showed lower variability but lower accuracy.

---

## Interpretation of Results

The results indicate that GPT-2 performed better than DistilGPT2 on the selected factual-question dataset.

However, GPT-2 also showed slightly greater variability in performance.

DistilGPT2 showed lower variability but achieved lower accuracy.

The results demonstrate why model comparison should not rely only on a single accuracy value.

Variance and standard deviation provide information about performance stability, while confidence intervals provide information about uncertainty around the estimated performance.

Hypothesis testing provides additional evidence about whether the observed difference between the two models is statistically significant.

---

## Model Size and Computational Efficiency

An important motivation for comparing GPT-2 and DistilGPT2 is the trade-off between model performance and computational efficiency.

Large language models generally require more computational resources, memory, and processing time.

Model distillation attempts to create smaller models that retain as much of the original model's capabilities as possible.

DistilGPT2 represents this approach by providing a smaller version of GPT-2.

The comparison therefore considers not only model performance but also the broader trade-off between model size, computational requirements, and performance.

---

## Visualizations

The project includes visualizations to support the statistical analysis.

The visualizations include:

- Accuracy comparison between GPT-2 and DistilGPT2
- Model accuracy with standard deviation
- Bootstrap distribution of model accuracy
- Confidence distribution of model accuracy

These visualizations provide a clearer representation of model performance and variability.

---

## Technologies Used

- Python
- Google Colab
- Hugging Face Transformers
- GPT-2
- DistilGPT2
- NumPy
- Pandas
- Matplotlib
- SciPy
- Seaborn
- Natural Language Processing
- Statistical Analysis
- Transformer Models

---

## Project Workflow

Factual Question Dataset
↓
Model Selection
↓
Dataset Preparation
↓
Response Generation
↓
Response Evaluation
↓
Accuracy Calculation
↓
Variance Analysis
↓
Standard Deviation Analysis
↓
Bootstrap Sampling
↓
Confidence Interval Estimation
↓
Hypothesis Testing
↓
Results Comparison
↓
Statistical Interpretation

---

## Project Structure

Statistical-Evaluation-of-Language-Models/

├── Dataset/
│
├── Images/
│
├── Models/
│
├── Notebooks/
│   └── Statis_Eval_LM.ipynb
│
├── Reports/
│   └── Statistical Approach to Evaluating LMs.pdf
│
├── README.md
├── requirements.txt
└── .gitignore

---

## How to Run

### Step 1 — Clone the Repository

git clone https://github.com/samyupolice/Statistical-Evaluation-of-Language-Models.git

### Step 2 — Navigate to the Project Directory

cd Statistical-Evaluation-of-Language-Models

### Step 3 — Install Dependencies

pip install -r requirements.txt

### Step 4 — Open the Notebook

Open:

Notebooks/Statis_Eval_LM.ipynb

The notebook can be executed using Jupyter Notebook or Google Colab.

---

## Reproducibility

The experiment follows a consistent evaluation procedure for both language models.

The same factual-question dataset and evaluation process are used for GPT-2 and DistilGPT2.

The notebook contains the implementation for:

- Model loading
- Response generation
- Response evaluation
- Accuracy calculation
- Variance calculation
- Standard deviation calculation
- Bootstrap sampling
- Confidence interval estimation
- Hypothesis testing
- Visualization
- Results generation

This consistent workflow ensures that both models are evaluated under the same experimental conditions.

---

## Limitations

The project has several limitations:

- The evaluation uses a factual question dataset.
- The questions focus primarily on general factual knowledge.
- The dataset is limited in size.
- The evaluation focuses on factual correctness.
- Accuracy does not fully capture the quality of generated language.
- Some responses may contain partially correct information that is difficult to classify using simple correctness criteria.
- The results are specific to the selected dataset and experimental setup.
- The findings should not be interpreted as a universal ranking of GPT-2 and DistilGPT2 across all NLP tasks.
- The experiment evaluates only two language models.

---

## Future Improvements

Future work could include:

- Evaluating larger factual-question datasets.
- Testing additional language models.
- Comparing more distilled and non-distilled models.
- Evaluating models on additional NLP tasks.
- Using established benchmark datasets.
- Comparing inference time.
- Comparing memory requirements.
- Analysing computational efficiency.
- Including semantic similarity metrics.
- Evaluating generated-response quality beyond simple correctness.
- Applying additional statistical tests.
- Increasing the number of bootstrap samples.
- Analysing model performance across different question categories.
- Evaluating larger and more diverse datasets.

---

## Academic Report

A detailed academic report is included in the `Reports/` folder.

The report covers:

- Introduction to language model evaluation
- Statistical approaches to model evaluation
- Accuracy
- Variance
- Standard deviation
- Confidence intervals
- Hypothesis testing
- GPT-2
- DistilGPT2
- Dataset preparation
- Experimental methodology
- Response generation
- Statistical analysis
- Results
- Discussion
- Conclusion
- Future work

---

## Conclusion

This project demonstrates a statistical approach to comparing language models using GPT-2 and DistilGPT2.

GPT-2 achieved higher accuracy than DistilGPT2 on the selected factual-question dataset, with an accuracy of 0.12 compared with 0.06.

The statistical analysis also showed differences in variance, standard deviation, and bootstrap confidence intervals.

The reported hypothesis-testing result produced a p-value of 0.0000, indicating a statistically significant difference between the two models within this experimental setup.

The project demonstrates that statistical evaluation can provide a more comprehensive understanding of language-model performance than relying on accuracy alone.

By combining accuracy, variance, standard deviation, bootstrap confidence intervals, and hypothesis testing, the project provides a structured approach for comparing language models and assessing the reliability of observed performance differences.

---

## Disclaimer

This project was developed for academic and research purposes.

The results are specific to the selected factual-question dataset and experimental methodology and should not be interpreted as a universal comparison of GPT-2 and DistilGPT2 across all language-model tasks.

---

## Author

**Samyuktha Police**

Data Science | Natural Language Processing | Machine Learning | Statistical Analysis
