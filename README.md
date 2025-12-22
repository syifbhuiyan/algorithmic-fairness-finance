Algorithmic Fairness & Information Asymmetry in Digital Finance
Theme: Human-Centered AI / Information Ethics / Fintech Status: Completed Tools: Python, Scikit-Learn, Fairlearn, Pandas

📌 Project Overview
How do alternative data sources in fintech credit scoring introduce unintended bias against specific demographics? This project builds a predictive credit risk model using the Home Credit Default Risk dataset and audits it for algorithmic fairness.

Coming from a background in agri-fintech (WeGro Technologies), I am deeply interested in how information systems can be designed to prevent social inequity. This project utilizes the Fairlearn library to detect and mitigate gender bias in credit decisioning.

🔍 Key Findings
Bias Detected: The baseline model disproportionately penalized male applicants, flagging 90% as "high risk" compared to 14% of females.

Bias Mitigated: Using a ThresholdOptimizer with constraints for Demographic Parity, we successfully equalized the selection rates to ~41% for both groups.

![Fairness Audit Chart](fairness_chart.png)

📂 Repository Structure
fairness_analysis.ipynb: The complete Python code for the model and audit.

research_note.md: A detailed academic note discussing the IS (Information Science) implications of the results.

🚀 How to Run
Open fairness_analysis.ipynb in Google Colab or Jupyter Lab.

Ensure you have a Kaggle API token (kaggle.json) if re-downloading the raw data.

Install dependencies: !pip install fairlearn.
