# North Carolina State Center Birth Statistics Case Study

**Introduction**

For this study, a random sample of 800 subjects from the North Carolina birth registry of 120,300 records will be analyzed using programming language R.

**Objectives**

The goals of this analysis involve using probability to investigate the correlation between smoking during pregnancy and the occurrence of premature births. Additionally, using the same dataset, another objective is to calculate probabilities for the data (mother’s age in years) as normally distributed throughout the dataset.

**Data Description of Variables**

![Screenshot 2024-01-26 124234](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/063f5ccc-4c22-4742-978d-db53154d80f5)

**Note:** MAGE is a discrete quantitative variable. PREMIE and SMOKE are qualitative categorical values with numerical values (1 OR 0).

**Data**

File name: LDS_C02_NCBIRTH800

For analysis: **ncbs800** - Variables include mage, premie, and smoke only.

**Results and Discussion**

**Q1** Using all 800 observations create a table that cross-tabulates the counts of mothers in the classifications of whether the baby was premature or not (PREMIE) and whether the mother admitted to smoking during pregnancy (SMOKE) or not.

**Note:** The table generated includes 798 values, with two missing values from the total 800.

![Screenshot 2024-01-26 124431](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/3dcb6235-a18a-4ab6-8a0f-d3dfcebad768)

**Variables premie and smoke and frequency**

![Screenshot 2024-01-26 124508](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/659a63b9-2d12-40f7-a399-3770d9e316a8)

**a)	Find the probability that a mother in this sample admitted to smoking.** 

The variable smoke uses numerical value **0** to indicate mothers that _did not_ smoke during pregnancy and numerical value **1** to indicate mothers that _did_ smoke during pregnancy. 114 is the total number of mothers that smoked in the sample size of 800, with two missing values. To find the probability of mothers that admitted to smoking, 114 is divided by 798 = 0.14285 or **14.285%**

**b)	Find the probability that a mother in this sample had a premature baby.**

The variable premie uses numerical value **0** to indicate an infant that _was not_ born premature and numerical value **1** to indicate an infant that _was_ born premature. Looking down at the column premie and across row with 1, 93 is the number of premature births. Divided by the sample size of 798 is 0.11654 or **11.654%**

**c)	Find the probability that a mother in the sample had a premature baby given that the mother admitted to smoking.**

For mothers that had premature births AND admitted to smoking, the number is 15 out of 798 or 0.01879%. The total count of mothers that smoke is 114. Divided by 798 = 0.14285. Following the conditional probability formula of: 
P(A | E) = P(Premature | Smoked) = P(Premature AND Smoked) / P(Smoked)
0.01879/0.14285 = 0.13153658 or **13.153%**

**d)	Find the probability that a mother in the sample had a premature baby given that the mother did not admit to smoking.**

Using the same formula P(A | E) = P(Premature AND did not smoke) / P(Did not smoke)
(78/798) = 0.09774 ; (684/798) = 0.85714
0.09774 / 0.85714 = 0.114030 or **11.403%**

**e)	Find the probability that a mother in the sample had a premature baby or that the mother did not admit to smoking.**

**Note:** 2 values are missing so total = 798

Had a premature baby | P(premie) = # premature / total number
	93/798 = .11654135 = (11.6541353%)
 
Did not smoke | P(smoke) = # did not smoke / total number
	684/798 = 0.85714286 = (85.7142857%)
 
Premature AND did not smoke | P(premie and smoke) = # premie and not smoked/ total number
	78/798 = .09774436 (9.774361%)
 
P(premature or did not smoke) = # of premature + # of did not smoke – # premature and did not smoke / total number
	93 + 684 – 78 / 798 = 699/798 = .87593985 or **87.593%**

**Q2** using all 800 observations of the NCBIRTH800 data answer the following questions:

**a)** Assuming that mothers age (MAGE) is approximately normally distributed with a mean of 26.91 and a standard deviation of 6.11, answer the following questions regarding mothers age:

**_i._ What is the probability that Age is less than 20 years**

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/2bdb2cb4-819a-42d5-8c19-50b981380d42)

o	The graph depicts a normal curve with a mean of 26.91, standard deviation of 6.11 and shaded area equal to 0.1290417. The probability that a mother’s age is less than 20 years old is **12.904%**, along the x-axis and curve approximates 68% of the total area.

**_ii._ What is the probability that Age is more than 36 years**

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/555edb5a-354f-478a-858a-aeda82443086)

o	The graph depicts a normal curve with a mean of 26.91, standard deviation of 6.11 and shaded area equal to 0.0684. The probability that a mother’s age is more than 36 years old is **6.84%**, along the x-axis and curve approximates 68% of the total area.

**_iii_. What is the probability that Age is between 20 years and 33 years**

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/c40d2a9b-1bb2-40a7-92ac-435694da921c)

o	The graph depicts a normal curve with a mean of 26.91, standard deviation of 6.11 and shaded area equal to 0.7115097. The probability that a mothers age is between 20 years and 33 years old is **71.1509%**

**b)** Assuming that mothers age (MAGE) is approximately normally distributed with a mean of 26.91 and a standard deviation of 6.11, answer the following questions regarding mother’s age: 

**_i_. Generate a Boxplot, a Histogram and a distribution plot for mother’s age.**

**_Boxplot_**

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/18d52e7e-a6e7-4fdf-965f-79557b0fe0cf)

![Screenshot 2024-01-26 125214](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/a5b48307-124d-419c-ba5a-a99a292086af)

o	There was a total of 800 observations, with two missing values making it 798. The mean age was 26.91, close to the median of 26 years old. Variability as measured by the standard deviation for this sample was 6.11 years. The range for the median quartile (IQR) of observations was 10 years. The IQR of the variable mage is Q3 (32) – Q1 (22) = 10. Lower extreme = 15; upper extreme = 42; Range = 27
o	It can be observed from the boxplot that 25% of the distribution is under 22 years of age. 50% of the distribution is up to 26 years of age and 75% of the distribution is under 32 years of age.

**_Histogram_**

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/b90e67b7-44f0-4b68-9f0c-ae8f7e747c00)

o	Mage is represented as a discrete random variable. The median of this dataset is 26 years. The histogram reflects that 71.15097% of the distribution falls between the ages of 20 to 33 years old. The probability that a mother’s age is less than 20 years is 12.90417% and is observed by low frequency on the left (gradual increase with age). The probability that a mother’s age is over 36 years old is 6.84% and is observed by lowering frequency on the right. Greater spread among data indicates greater variability.

**_Distribution Plot_**

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/83c64561-7568-4c6d-b3d7-17c34667e1c8)

o	In a normal distribution, 68% of data falls within the standard deviation of the mean. The mean falls in between 20.8 and 33.02.

**_ii_. What is the 68.26% range (lower bound and upper bound) for mother’s age?**

Mean = 26.91 ; SD = 6.11 ; Shaded area = 0.3173/2 is 0.15865 on both sides.

![image](https://github.com/efejzic/Bayesian_Birth_Statistics/assets/119814593/bdbad8de-f127-449b-b232-406554a1f3b1)

o	The x axis is the bounded area between 1 standard deviation from the mean in the right and left direction. The upper bound and lower bound create 68.26% of the normal distribution for mage. The normal curve, or probability density function (PDF), is associated with continuous random variable mage.
1 Deviation to the left; Lower bound = mean – standard deviation
**20.80** = 26.91 – 6.11
1 Deviation to the right; Upper bound = mean + standard deviation
**33.02** = 26.91 + 6.11

**Conclusion** 

The objectives of this unit were to demonstrate an understanding of the concept and properties of probability and data distribution. This dataset was analyzed to investigate the correlation between smoking during pregnancy and the occurrence of premature births.  Out of 800 records (with two missing values), the probability that a mother in the sample admitted to smoking was 14.285%, 114 smokers out of 798, while the probability that a mother had a premature baby was 11.654%, 93 out of 798 births. Only 15 out of 798, 1.879%, of mothers had a premature baby and admitted to smoking. Additionally, the data shows us that more premature babies were born to mothers who did not smoke compared to mothers who did (78 births compared to 15, respectively). There is a body of research that suggests a correlation between substance use, including alcohol and nicotine, during pregnancy and the incidence of premature births. The probability that a mother in the sample had a premature baby and potentially lied about smoking is 87.5939%, an interesting observation that could serve as an explanation for the high rate of premature births for “non-smokers”. When it comes to the variable mage, or mother’s age, the probability that a mother’s age is between 20 years and 33 years old is 71.15097%. Another risk factor for premature births is young age (under 20) and advanced maternal age (over 35). The probability that a mother’s age is more than 36 years old is 6.84%, a smaller percentage than the probability that a mother’s age is less than 20 years old is 12.904%. Additional analysis would be needed to compare premature birthrates between young and older mothers.



