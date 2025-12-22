Title: Algorithmic Fairness in Digital Finance: A Case Study on Demographic Parity

Abstract This study audits a Logistic Regression model trained on the Home Credit Default Risk dataset to identify and mitigate gender-based algorithmic bias. Drawing on principles of "Fairness, Accountability, and Transparency" (FAccT), we explore how automated credit scoring can inadvertently introduce information asymmetry and penalize specific demographics.

1. Introduction In modern FinTech, credit scoring algorithms are often treated as objective arbiters of risk. However, information systems trained on historical data frequently encode systemic biases. This project investigates a "black box" risk model to determine if it satisfies Demographic Parity—the ethical standard that a model’s positive decisions (e.g., granting a loan) should be independent of sensitive attributes like gender.

2. Methodology

Data Source: Home Credit Default Risk (Kaggle).

Features: Age, Gender, Total Income.

Sensitive Attribute: Gender (Male/Female).

Audit Tool: Fairlearn (Microsoft/Azure) and scikit-learn.

Mitigation Strategy: Post-processing with ThresholdOptimizer to enforce Demographic Parity constraints.

3. The Bias Audit (Pre-Mitigation) The initial model, optimized purely for weighted accuracy, exhibited severe bias:

Selection Rate Disparity: The model predicted "High Risk" for 90.5% of Male applicants, compared to only 14.0% of Female applicants.

Accuracy Asymmetry: While the model was 82% accurate for women, it dropped to 18% for men. This suggests the model learned to "game" the loss function by blanket-labeling men as defaulters—a classic case of algorithmic discrimination.

4. Mitigation & Results We applied a ThresholdOptimizer to recalibrate the decision boundary.

Result: The selection rate gap was closed. Both groups now have a "High Risk" prediction rate of approximately 41.6%.

Trade-off: As expected in Information Science theory, fairness comes at a cost to pure predictive accuracy. However, the system is now equitable, treating individuals based on their financial history rather than their demographic group.

5. Conclusion & IS Implications For platforms like WeGro or other agri-fintech services, deploying un-audited models can lead to the systematic financial exclusion of specific demographic groups. This study demonstrates that "fairness" must be an architectural requirement of the information system, not an afterthought.
