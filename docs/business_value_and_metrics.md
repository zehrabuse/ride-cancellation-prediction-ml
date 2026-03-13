## Business Value

If the proposed decision support system performs effectively, it can enable companies to make operational decisions more quickly and efficiently. 
By identifying high-risk cancellation scenarios in advance, the platform can improve customer satisfaction, reduce operational losses, and increase overall profit margins.

A portion of the increased profitability can be reinvested in strategies aimed at further enhancing customer satisfaction, allowing the company to differentiate itself from competitors and strengthen its position in the market.

## Model Success Metrics

Recall is defined as the primary success metric of this project because it directly reflects the model’s ability to identify rides that are likely to be canceled. 
From a business perspective, failing to detect an actual cancellation represents the most critical risk, as it may lead to revenue loss, decreased customer satisfaction, and inaccurate evaluation of operational performance. 

In contrast, incorrectly predicting a non-canceling ride as high risk may introduce additional precautionary actions and minor operational costs, but it does not pose the same level of business impact. 
Therefore, prioritizing recall ensures that high-risk cancellation cases are captured effectively, enabling proactive decision-making, better operational control, and the preservation of overall business value.

### Success Criteria

To establish clear benchmarks for evaluating the model's performance, the following thresholds are defined:

- **Recall ≥ 0.80:** The model is considered successful if it correctly identifies at least 80% of potential cancellation cases. This ensures that most high-risk situations are detected.

- **ROC–AUC ≥ 0.85:** This threshold indicates strong discriminative capability, meaning the model can effectively distinguish between canceled and non-canceled rides.

- **Precision ≥ 0.60:** This ensures that predicted cancellation cases are reasonably reliable and that the model does not generate an excessive number of false alarms.

If these thresholds are met, the model can be considered effective for supporting operational decision-making and reducing the negative business impact associated with ride cancellations.
