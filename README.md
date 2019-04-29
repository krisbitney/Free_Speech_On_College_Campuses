# Free Speech On College Campuses
This is an independent unsupervised learning project. The goals are to...
1. See if students can be clustered by their positions on free speech
2. Attempt to recover a latent variable representing political correctness, if it exists
3. Assess the relationship between such clusters or latent variables and students' political affiliations

### Results
While students have diverse beliefs about speech, I found no evidence to support the idea that there are discrete"clusters" in which we can categorize students solely based on those views. When it comes to speech, student beliefs vary widely and most students have moderate views overall, as measured by the Stanton Free Speech Index constituent questions asked in the Gallup-Knight Foundation survey study on which this analysis is based. 

I discovered evidence for the latent quality of "political correctness", which accounts for about 23% of the variance in students' beliefs about free speech. 

The "political correctness" factor measures opposition to free speech in favor of protective inclusiveness. It is a measure of the extent to which students favor ideas like promoting an inclusive society, "instituting speech codes" that could restrict "offensive or biased speech" on campus, removing first amendment protection of hate speech, "disinviting [sic] speakers because some students are opposed to the invitation".

I also found evidence for a latent variable we might label "free speech moderation". Students high in "free speech moderation" want their colleges to regulate speech on campus, but support free speech more generally and believe hate speech should be legally protected. 

Finally, I found a latent variable I like to call "free speech extremism". It measures the extent to which a student expresses blanket support for free speech, including the use of speech - e.g. protesting, shouting - to counter unwanted speech.

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
