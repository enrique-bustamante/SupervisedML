# SupervisedML


precicion
recall
balance accuray score
recommend the model if any to use
justify recommendation

## Analysis

### Native Random Oversampling

When utilizing random oversampling, the precision for finding low-risk loan
applicants is 100% but high risk is 1%. The recall is better for detecting
high-risk applicants at 51% while the recall rate for low-risk applicants is 63%.

The F1 score for low-risk applicants is 0.77 while it is only 0.02 for
high-risk applicants. This means the model is better at predicting low-risk
applicants but not very good at detecting high-risk applicants, resulting in
loans potentially being given out to high-risk applicants.

The balanced accuracy score for this model is 57.11%.

### SMOTE

When the same data was analyzed utilizing SMOTE, the precision for finding
low-risk and high-risk loan applicants didn't differ from the random
oversampling method. The recall for SMOTE was 67% for low-risk, 47% for
high-risk, making it better for identifying low-risk applicants but worse at
identifying high-risk applicants.

The F1 score for low-risk applicants is 0.80 and 0.02 for low and high-risk
applicants, respectively. This means the model is better at predicting low-risk
applicants but not very good at detecting high-risk applicants, resulting in
loans potentially being given out to high-risk applicants.

The balanced accuracy score for this model is 56.72%.

### Undersampling

When the same data was analyzed utilizing Clustered Centroids, the precision
for low and high-risk applicants was 99% and 1%, respectively. The recall for
low-risk was 94%, but dropped to 13% for high-risk applicants.

The F1 score for low-risk applicants is 0.77 and 0.02 for high-risk
applicants. This means the model is better at predicting low-risk applicants
but not very good at detecting high-risk applicants, resulting in loans
potentially being given out to high-risk applicants.

The balanced accuracy score for this model is 53.38%.

### Combination Sampling

Running the data through a combination of over and undersampling, specifically
SMOTE-ENN, the precision for low and high-risk applicants was 100% and 1%,
respectively. The recall improved for detecting high-risk applicants at 62%.
Low-risk applicant recall was 53%.

The F1 score for low and high-risk applicants were 0.69 and 0.02,
respectively. This means the model is better at predicting low-risk
applicants but not very good at detecting high-risk applicants, resulting in
loans potentially being given out to high-risk applicants.

The balanced accuracy score fro this model is 57.87%.


## Recommendations

If we had to choose one of these four models, I would choose the combination
sampling, due to having the highest recall. It also had the best balanced
accuracy score out of all of the models. I would rather use a more reliable
model that is better at detecting high-risk applicants.

The Easy Ensemble Adaboost method had much better performance compared to the
prior four models discussed. The precision and recall for high-risk applicants
was 9% and 92%, respectively. The balanced accuracy score was also higher at 93.17%.
