# Free Speech On College Campuses
This is an independent unsupervised learning project. The goal is to answer three questions:
1. Is there a distinct faction of anti-speech extremists on college campuses, as media reports have suggested?
2. Would I find support for an underlying concept of “political correctness” among the beliefs students expressed?
3. How do beliefs about free expression relate to political affiliation?

### Results
While students have diverse beliefs about speech, I found no evidence of discrete"clusters" in which we can categorize students solely based on those views. There is not a clear faction of students who oppose free speech. When it comes to speech, student beliefs vary widely and most students have moderate views overall, as measured by the Stanton Free Speech Index (FSI) constituent questions asked in the Gallup-Knight Foundation survey study on which this analysis is based. The distribution of the FSI is unimodal.

I discovered evidence for the latent quality of "political correctness", which accounts for about 23% of the variance in students' beliefs about free speech. 

The "political correctness" factor measures preference for protective inclusiveness in lieu of free expression. It is a measure of the extent to which students believe the value of promoting an inclusive society is more important than freedom of express. Students high in this metric favor "instituting speech codes" that could restrict "offensive or biased speech" on campus, removing first amendment protection of hate speech, and "disinviting [sic] speakers because some students are opposed to the invitation".

I found additional evidence for a quality we might label "free speech moderation". Students high in this metric support free speech in general - they believe hate speech should be legally protected, for example - but also want some regulation of speech on campus.

The statistical process also uncovered a third variable I like to call "free speech extremism". It measures the extent to which a student expresses blanket support for free speech, including the use of speech to counter unwanted speakers - e.g. by protesting, shouting.

There is a statistically significant relationship between the Stanton Free Speech Index and political ideology/party affiliation among college students that persists after accounting for factors socioeconomic status, college region, college sector, gender, religion and race. Conservative students tend to have more support for free speech than do moderate students, while liberal students tend to have stronger preference for protective speech policies than moderate students. And while Democrat students are less likely than Independent students to support free speech, Republic students support free speech to about the same degree as Independent students. Despite those differences, the distributions of free speech index scores retain substantial overlap when stratified by ideology or political party leanings.

Interestingly, the trait "political correctness" is a better predictor of a college student's political ideology than socioeconomic status, religion, age, gender, race, college sector, or college geographical region.

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
5. Reduced dimensionaly of feature space
    * Transformed feature space using principal components analysis (PCA)
    * Interpreted principal components using principal directions in original feature space
    * Quantitatively assessed impact of "curse of dimensionality"
6. Clustered customer data using four methods:
    * KMeans
    * Gaussian Mixture
    * Density-Based Spatial Clustering of Applications with Noise (DBSCAN)
    * Hierarchichal/Agglomerative
7. Varied clustering algorithm hyperparameters and juxtaposed methods' internal performance
8. Estimated variable relationships using OLS

Cluster model performance was evaluated using Silhouette score and Calinski-Harabaz score.
                  
### Required libraries                       
This project uses Numpy, Pandas, Pyplot, Seaborn, Sklearn, Statsmodels, and Jupyter.
