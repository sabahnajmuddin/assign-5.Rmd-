---
title: "Week 5 Assignment"
output: html_document
date: "2025-02-08"
---

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```

## Part 1: Sources of Bias

### 1. What are some potential sources of bias in the underlying data?

- **Historical Bias**: Occurs when data reflects past societal inequalities, leading to unfair model outcomes even if the data is accurate (Suresh & Guttag, 2021).
- **Representation Bias**: Arises when the training dataset does not adequately represent certain populations, leading to poor model generalization (Suresh & Guttag, 2021).
- **Measurement Bias**: Occurs when features or labels used in modeling are imperfect proxies for real-world constructs. For example, using credit scores to measure "creditworthiness" can lead to disparities (Suresh & Guttag, 2021).
- **Evaluation Bias**: Appears when the test data does not represent the real-world population, causing misleading performance assessments (Suresh & Guttag, 2021).

### 2. How might biases be introduced in the data science pipeline?

Biases can emerge at multiple stages:
- **Data Generation**: Historical bias from existing inequalities.
- **Population Definition & Sampling**: Representation bias from over/underrepresentation.
- **Feature Selection & Data Collection**: Measurement bias from flawed proxies.
- **Model Training**: Learning bias from the inherent patterns in training data.
- **Evaluation**: Evaluation bias from misrepresentative benchmarks.
- **Deployment**: Deployment bias when biased models impact real-world decisions (Suresh & Guttag, 2021).

### 3. What are the risks to fairness in downstream applications and deployment?

- **Discriminatory Loan Denials**: Certain groups may be unfairly denied loans due to biased historical data (Hardt et al., 2016).
- **Disparate Interest Rates**: Models may suggest higher interest rates for marginalized groups (Dwork et al., 2012).
- **Regulatory and Ethical Risks**: Biased decision-making could lead to legal and reputational challenges (Kim, 2018).

Ensuring fairness in ML requires continuous monitoring and bias mitigation strategies.

## Part 2: Bias Metrics

### 1. False Positive in Loan Approval

A **false positive** occurs when a borrower who would have repaid the loan is incorrectly classified as high-risk and denied the loan. This leads to:
- Loss of legitimate customers.
- Economic exclusion for individuals misclassified as high-risk.
- Reduced revenue for banks (Unit21, n.d.).

### 2. False Negative in Loan Approval

A **false negative** happens when a high-risk borrower is incorrectly classified as low-risk and granted a loan. Consequences include:
- Increased loan defaults and financial losses.
- Higher operational costs for banks in debt recovery.
- Potential regulatory scrutiny for poor lending practices (SEON, n.d.).

### 3. Confusion Matrix Metrics for Fairness

To ensure equity in loan approval:
- **False Positive Rate (FPR)**: Helps prevent unfair denials across demographic groups.
- **False Negative Rate (FNR)**: Ensures risky borrowers are not disproportionately approved.
- **Disparate Impact Ratio**: Measures approval rate disparities across different groups.

## References

- Suresh, H., & Guttag, J. (2021). A framework for understanding sources of harm throughout the machine learning life cycle. *Proceedings of the ACM on Human-Computer Interaction*.
- Hardt, M., Price, E., & Srebro, N. (2016). Equality of opportunity in supervised learning. *Advances in Neural Information Processing Systems*.
- Dwork, C., Hardt, M., Pitassi, T., Reingold, O., & Zemel, R. (2012). Fairness through awareness. *Proceedings of the 3rd Innovations in Theoretical Computer Science Conference*.
- Kim, P. T. (2018). Data-driven discrimination at work. *William & Mary Law Review*.
- Unit21. (n.d.). False positives in fraud detection. Retrieved from https://www.unit21.ai/fraud-aml-dictionary/false-positives
- SEON. (n.d.). False negatives in fraud prevention. Retrieved from https://seon.io/resources/dictionary/false-negatives/
