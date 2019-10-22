Advanced Statistics Module 9 T-Test for Indpendent Samples
================

The data below is from a study whose research hypothesis was: “There will be a difference between boys and girls in the number of times they raise their hand in class.” For the purposes of this study, boys were coded as 2 on gender; girls were coded as 1 and boys were marked 0.

``` r
x=c(9,8,3,8,10)
y=c(3,1,2,6,4,3,6)
```

``` r
ttestx = t.test(x)
samplemeanx = round(ttestx$estimate,2)

ttesty = t.test(y)
samplemeany = round(ttesty$estimate,2)

dfx = length(x)-1
dfy = length(y)-1

tscorex = 2*(1-ttestx$p.value)
tscorey = 2*(1-ttesty$p.value)
```

\#1. Find your two sample means.

The sample mean of data (x) is 7.6, while the sample mean of data (y) is 3.57

\#2. Find the degrees of freedom(s).

The degree of freedom for data (x) is 4 and the degree of freedom for y is 6.

\#3. Find t-test statistic score (s).

The t-statistic score for data (x) is 6.2898048 and the t-statistic for data (y) is 4.9669963.

\#4. Find the P value (s).

The p-value for data (x) is 0.003264 and the p-value for data (y) is 0.0025344.

\#5. Assume an alpha of .05 was chosen, Would this result have been statistically significant?

Yes, with an alpha of .05, the results are significant because the p-value for data (x) is 0.0032, while the p-value for data (y) is 0.0025. Since both of these values are below 0.05, we can reject the null hypothesis and conclude that gender does in fact play a role in the number of times a student raises their hand.

\#6. What critical value would your obtained t-test value have to exceed to be significant at the .01 level (assume a two-tailed test)?

For data set (x), the critical value would be 2(1-pvalue), which would be 1.9934721, and data set (y) would be 1.9949311.
