# ab_codecademy
A/B Test for two "Ready" Premium Feature ads

This project uses two data sets, the first contains information on users who saw the original ad. The second file contains information on users who saw the new version of the banner ad.

The python code is a full exploratory analysis and statistical analysis of the data. The data sets are both relatively clean, however it is always advisable to check the extents and values for all the columns.

A major issue that stands out when exploring the data is the two populations were not properly randomized in the study design. A/B testing should randomize the populations who view each ad to eliminate confounding variables so that the only difference is which ad the user saw.

Ultimately a down stepping, multivariate, logistic regression analysis showed colinearity between the number of exercises users had completed and the ad they were shown. This is an issue and means that we cannot factor out the influence of user experience in the click through rate. By running the test with both the group and number of exercises then stepping down and then with just number of exercises, variables that were originally insignificant were then highly significant. This suggests colinearity.

In order to compensate for this, an attempt was made to filter out the original users so that they matched the new ad users. This drops the observations from over 10k to under 400. When we compare these two groups, there is a difference in CTR however the p-value is not small enough to reject the null hypothesis: there is no difference in click through rate between the ad versions.

Going forward, we have two options: 
1 Do nothing, as the test was inconclusive 
2 Keep the current ad and re-run the statistical analysis if the funds and time allow and ensure users are properly randomized.
3 Adopt the new ad with caution as there is SOME evidence it may have a higher CTR and no eveidence it underperfors but continue to monitor results.
