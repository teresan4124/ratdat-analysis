# ratdat-analysis
Analyzed rodent body weight data to examine sexual dimorphism and seasonal trends. Conducted data cleaning, normality and variance checks, t-tests, Kruskal–Wallis tests, and visualized distributions by sex and month. Provides reproducible R code for statistical analysis and plotting.

Rodent Body Weight Analysis – Portal Project

Introduction
Long-term ecological studies are essential for understanding how ecosystems change and adapt over time. The Portal Project, established in 1977 in the Chihuahuan Desert of Arizona, provides over four decades of rodent, plant, and ant community data. These data have contributed to over 100 scientific publications and allow investigation of competition, community dynamics, and ecosystem responses to environmental change. The dataset is publicly available and can be accessed in R using the ratdat package.
Rodents play central roles in desert ecology through seed predation and granivory, making their traits and population dynamics important to study. This project focuses on sexual dimorphism in rodent body size and temporal changes in species distributions. Identifying species with sexual dimorphism can reveal selective pressures, while examining monthly trends helps understand seasonal or sampling variation.

Research questions:
Do rodent species differ in body weight between sexes?
How do species distributions change over time?

Hypotheses:
Some rodent species will show sexual dimorphism, with males expected to weigh more than females.
Species proportions will remain constant across months.

Materials and Methods
Study Site and Data Collection
Location: Portal Project, Chihuahuan Desert, Arizona (31.937769, −109.08029)
24 experimental plots (50 × 50 m), monthly rodent sampling using Sherman live traps at 49 permanent stakes per plot
Measurements: species, sex, weight, hind foot length, reproductive condition; PIT tagging since 1991
Dataset available on Zenodo: https://doi.org/10.5281/zenodo.1215988
Data Processing and Variables
Response variable: body weight
Predictors: sex, month
Species with insufficient observations were excluded
Weight distributions and variance tested using Shapiro-Wilk and Levene’s tests

Statistical Analyses
Sexual dimorphism: Two-sample t-tests (Welch or pooled variance depending on assumptions); nonparametric alternatives if assumptions violated
Species distributions over time: Kruskal-Wallis rank-sum tests for non-normal distributions

Analysis and Results

Sexual Dimorphism:
Peromyscus fulvescens: Welch t-test showed significant sexual dimorphism, t(60.63) = 2.98, p = 0.004, females heavier (M = 13.68 g) than males (M = 12.44 g)

Peromyscus leucopus: No significant difference, t(33) = 0.45, p = 0.66, females (M = 19.31 g) vs males (M = 18.68 g)

Neotoma ochrognathus: No significant difference, t(39) = -0.05, p = 0.96, females (M = 55.32 g) vs males (M = 55.70 g)

Temporal Trends:
P. fulvescens: Marginally non-significant monthly variation, χ²(10) = 17.50, p = 0.064

P. leucopus: No significant monthly variation, χ²(9) = 8.64, p = 0.47

N. ochrognathus: No significant monthly variation, χ²(11) = 5.89, p = 0.88

Conclusion:
Sexual dimorphism in body weight is evident only in P. fulvescens. No species showed significant monthly variation in weight, suggesting minimal seasonal effects or consistent sampling over time.
