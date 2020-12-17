# Ending civil wars 
### On the prediction of interstate conflicts

This project is an extension of the work performed in the paper [Comparing Random Forest with Logistic Regression for Predicting Class-Imbalanced Civil War Onset Data](https://www.jstor.org/stable/24573207?seq=1) by David Muchlinski, David Siroky, Jingrui He and Matthew Kocher. The data analysis can be found in the notebook `p4_extension.ipynb`.

## Rendered notebook:
[**Click here**](https://nbviewer.jupyter.org/github/epfl-ada/ada-2020-project-milestone-p3-p3_padamalgame/blob/main/p4_extension.ipynb) to view the notebook rendered (map plots are not displayed). To view the rendered notebook with all plots, please download `p4_extension.html`. 

## Data story:
[**Click here**](https://mlecauchois.github.io/cwonset/) to view the datastory.

## Abstract:
The takeaways from the original paper are that algorithmic approaches offer a higher predictive power of civil war onset than traditional techniques, an asset used to corroborate some previous causal conclusions, and to question others. We propose to further exploit the derived algorithmic model in order to analyze some temporal aspects of these conflicts. Namely, we will study the evolution of the best predictors across the years. Also, we will tackle the arguably as-important issue of the ending of these conflicts, to gain an insight into the enablers of peace. To do so we will manipulate the data, and leverage the same algorithmic approach to predict ending. Finally, we will use another model, namely artificial neural networks, to study if predictive accuracy can be enhanced further. In the same spirit of the paper, permutation importance will then be used to strengthen or emit new hypotheses on our causal analysis.

## Research questions:
- Do the best predictors of civil war onset evolve throughout the years and if so, what does this allude to ?
- Can the duration of the conflict be predicted and if so, what enablers of peace can be hypothesised ?
- Are artificial neural networks even better predictors, and do they corroborate or question the previous analysis ?

## Dataset:
- **CWD**: Civil War Dataset, the dataset already used by the paper. We will use this dataset for the analysis of the evolution of civil war predictors over the years. This dataset was already previously used. All replication materials from the original paper can be found [here](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/KRKWK8).

## Methods:
- **Temporal change of best predictors for civil war**: We will analyze the evolution of predictors for civil war over the years by grouping the events in bins of 15 years periods (using the permutation importance). We will then analyze if there is a significant change of predictors over the years. We will also do clustering on the features of the events, to see if we can find some temporal dependencies and on which periods.
- **Analysis of civil war ending**: Following a similar approach to that of the paper, we will fit a Random Forest regressor to predict the ending of a conflict. Evaluating the predictive performance of the model will first give us an insight as to how well the features of the CWD dataset can encapsulate the complex factors determining the ending of a conflict. We will then analyze the permutation importance to get a better understanding of the important variables.
- **Comparison with Artificial Neural Networks**: The whole analysis conducted above will then be replicated using ANNs instead (similar to the logistic regression and random forest comparison from the paper). To efficiently do so without rewriting the whole pipeline, our code will be modularized. To analyze the best predictors, we will use permutation importance. To better understand how the ANN performs those predictive tasks, we will perform t-SNE on the activations.

## Timeline:
- **Week 1**: We prepared the work, e.g wrangle the data, and work on the first question. A modularized code pipeline is also set up in order to efficiently perform the different analyses for both the Random Forest and the ANN. Initial data exploration analysis.
- **Week 2**: Complementary work on the first research question (ROC curves, permutation importance, embedding analysis) and analysis of different clustering approaches for the problem. Second research question is also tackled (ROC curves, permutation importance, embedding analysis) and some work is done in order to generate interactive plots. 
- **Week 3**: Setup of the datastory website, continued work on the plots and larger hyperparamater search.

## Contribution:
- **Nicolas**:
- **Matthieu**: 
- **Yves**:

