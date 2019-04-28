# Free_Speech_On_College_Campuses
This is an independent unsupervised learning project. The goals are to...
1. See if students can be clustered by their positions on free speech
2. Attempt to recover a latent variable representing political correctness
3. Assess the relationship between such clusters or latent variables and students' political affiliations

### Results
I found that students cannot be segmented into distinct groups based on their free speech beliefs, as measured by the Stanton Free Speech Index constituent questions asked in the Gallup-Knight Foundation survey study on which this analysis is based. 

I found marginal support for a variable that could be described as "political correctness". The variable explains about 23% of the differences in speech beliefs. The variable serves as a measure of opposition to free speech, and is primarily dominated by favor for promoting an inclusive society, "instituting speech codes" that would restrict "biased speech", removing first amendment protection of hate speech, and "disinviting [sic] speakers because some students are opposed to the invitation".

There is a statistically significant relationship between the Stanton Free Speech Index and political ideology/party affiliation among college students that persists after accounting for factors socioeconomic status, college region, college sector, gender, religion and race. Conservative students tend to have more support for free speech than do moderate students, while liberal students tend to have stronger preference for protective speech policies than moderate students. And while Democrat students are less likely than Independent students to support free speech, Republic students support free speech to about the same degree as Independent students. Despite those differences, the distributions of free speech index scores retain substantial overlap when stratified by ideology or political party leanings.

### Data Source
Data for this project comes from a joint survey study by Gallup and the Knight Foundation. The study surveyed more than 3,000 students on college campuses.

Gallup/Knight Foundation (2018). Free Expression on Campus: What College Students Think
about First Amendment Issues. Gallup America Inc. Retrieved from: https://heterodoxacademy.org/gallup-knight-foundation-study/

### Procedure
I completed the following tasks the "StudentFreeSpeech.ipynb" Jupyter notebook:
1. Explored data
2. Assessed missing values
    * Converted missing values to NaN
    * Assessed missing values by dataframe column
    * Assessed missing values by dataframe row
    * Imputed missing values
3. Selected, re-encoded, and cleaned features
4. Created a data preprocessing pipeline
5. Standardized features
6. Reduced dimensionaly of feature space
    * Transformed feature space using principal components analysis (PCA)
    * Interpreted principal components using principal directions in original feature space
    * Quantitatively assessed impact of "curse of dimensionality"
7. Clustered customer data using four methods:
    * KMeans
    * Gaussian Mixture
    * Density-Based Spatial Clustering of Applications with Noise (DBSCAN)
    * Hierarchichal/Agglomerative
8. Varied clustering algorithm hyperparameters and juxtaposed methods' internal performance
9. Estimated paramters of OLS regressions

Cluster model performance was evaluated using Silhouette score and Calinski-Harabaz score.
                  
### Required libraries                       
This project uses Numpy, Pandas, Pyplot, Seaborn, Sklearn, Statsmodels, and Jupyter.
