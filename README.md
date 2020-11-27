# ada-2020-project-milestone-p3-p3_padamalgame


## Project proposal
### 1. Title:
Analyzing the temporal attributes of civil wars
### 2. Abstract:
The takeaways from the original paper are that algorithmic approaches offer a higher predictive power of civil war onset than traditional techniques, an asset used to corroborate some previous causal conclusions, and to question others. We propose to further exploit the derived algorithmic model in order to analyze some temporal aspects of these conflicts. Namely, we will study the evolution of the best predictors across the years. Also, we will tackle the arguably as-important issue of the duration of these conflicts, to gain an insight into the enablers of peace. To do so we will use additional data, and leverage the same algorithmic approach to predict duration. Finally, we will use another model, namely artificial neural networks, to study if predictive accuracy can be enhanced further. In the same spirit of the paper, permutation importance will then be used to strengthen or emit new hypotheses on our causal analysis.
### 3. Research questions:
- Do the best predictors of civil war onset evolve throughout the years and if so, what does this allude to ?
- Can the duration of the conflict be predicted and if so, what enablers of peace can be hypothesised ?
- Are artificial neural networks even better predictors, and do they corroborate or question the previous analysis ?
### 4. Proposed datasets:
- **CWD**: Civil War Dataset, the dataset already used by the paper. We will use this dataset for analysis of the evolution of civil war predictors over the years. This dataset was already previously used.
- **Civil War End-Date Dataset**: This dataset contains information about the duration and end dates of intrastate conflicts. Since the conflicts are defined in this dataset with slightly different conditions, there will be some data wrangling to do. https://www.prio.org/Data/Armed-Conflict/Onset-and-Duration-of-Intrastate-Conflict/
### 5. Methods
- **Data collection**: To be able to join the 2 datasets, we will have to analyze and select the intrastate conflicts from the Civil War End-Date Dataset corresponding to events in the CWD dataset. We will have no data wrangling to do with this second dataset.
- **Temporal change of best predictors for civil war**: We will analyze the evolution of predictors for civil war over the years by grouping the events in bins of ten years periods (using the mean decrease in Gini score). We will then analyze if there is a significant change of predictors over the years. We will also do clustering on the features of the events, to see if we can find some temporal dependencies and on which periods.
- **Analysis of civil war duration**: Following a similar approach to that of the paper, we will fit a Random Forest regressor to predict the duration of a conflict. Evaluating the predictive performance of the model (coefficient of determination) will first give us an insight as to how well the features of the CWD dataset can encapsulate the complex factors determining the duration of a conflict. We will then analyze the mean decrease in Gini score to get a better understanding of the important variables.
- **Comparison with Artificial Neural Networks**: The whole analysis conducted above will then be replicated using ANNs instead (similar to the logistic regression and random forest comparison from the paper). To efficiently do so without rewriting the whole pipeline, our code will be modularized. To analyze the best predictors, we will use permutation importance. To better understand how the ANN performs those predictive tasks, we will perform t-SNE on the activations.
### 6. Proposed timeline
- **Week 1**: We will prepare the work, e.g wrangle the data, and work on the first question. A modularized code pipeline will also be set up in order to efficiently perform the different analyses for both the Random Forest and the ANN.
- **Week 2**: We will do the core of the work, analyzing the data and answering question 2. Based on the results we will find, the analysis will be pushed further. The third question will follow up thanks to a well structured code.
- **Week 3**: This week can be a margin for any encountered issues with data analysis. Otherwise, we will prepare the datastory, publish the graph and discuss our results.

### 7. Organization within the team
- **Week 1**: Nicolas will deal with the data wrangling, Matthieu will set up the code pipeline and Yves will work on question 1.
- **Week 2**: Nicolas and Yves will focus on the research of question 2. Nicolas will fit the model and Yves will be in charge of analysing the data to find the best predictors. Matthieu will handle the clustering part and possible extensions.
- **Week 3**: Matthieu will implement an interactive visualisation, Yves will do the plots and figures, and Nicolas will write the datastory. Everyone will be in charge of the redaction and discussion of the results.
