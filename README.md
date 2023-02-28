### Problem Statement
Can you tell whether someone paid their loan in full? Are people working certain jobs more inclined to fully pay off their loan?

### Background
Banks offfer loans to people who appply for them. Wells Fargo Bank in particular offers personal loan from $3,000 to $100,000. 
There are multiple loan plans somone can apply for. Yet there are penalties for late payments. If a payment is only late within
the time alloted by the bank it would be considered in the grace period. There would be no repercussions for paying out the loan
in the grace period. However if the loan is late after the grace period than their will be interest added to the payment fee. 
After being excessively late on a payment than the defaulting can occur which will negatively impact credit score .

### Data 
Data provided by this website: https://www.openintro.org/data/index.php?data=loans_full_schema
Data dictionary also located at this website
loans_full_schema.csv: loans data set 
loans_schema_clean.csv: the cleaned and feature engineered dataset 

### Analysis
All 6 of the binary classification models had accuracy scores over 80%. Though, the most disappointing model was the multininomial 
naive bayes. The model had an accuracy score of 82% and the precison and f1 scores were low at 0.23 for precision and 0.37 for the f1 score.
There were actaully a high number of false negatives as there was 437 false negatives. The other models: Random Forest, KNearest Neigbors, 
Logistic Regression, Adaboost w/Decision Trees, and XG Boost all had accurtacy score of over 90%. The lowest precison score for the remaining 
five models was 0.42 for the Random Forest model. The Logistic Regression, Adaboost w/Decision Trees, and XG Boost all had precision scores over
0.5. The model that scored the best was the XG Boost model. The accuracy score was 99.8% and the roc auc score was 99.9%. The XG boost also had
the lowest number of of false negatives at 12 and false negatives at 15.

### Conclusions
The EDA showed that the top 5 employment titles that fully paid on their loan type were managers, sales, teachers, project manager, and owner respectively.
From this it, it can be gathered that people working mangarial roles tend to fully pay off their loans the most within the limitations of this dataset. There
was not a lot of data for those who were fully paid so it is not realistic to come to the conclusion that this is true in any case. On the other hand,
Since the models all had accuracy score over 80% on the test data and all had auc score of 90% or above than it is safe to say that models were successfuly created
to predict the loan status of paid in full. If more data points were available it would be great to create models to predict which employment roles default more
and then compare it with the paid in full models.
