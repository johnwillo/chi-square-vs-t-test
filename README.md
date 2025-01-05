# Test of chi-square vs t test type I error rates on binomial data.

When comparing two independent samples a common recommendation is to use a t test for continuous data and a chi-square test on binomial data. In fact I have made this recommendation myself. Recently, however, when researching the use of a non-inferiority test applied to binomial data, I came upon a paper by D'Agostino et al. [-@dagostinoAppropriatenessCommonProcedures1988], which recommended the use of *either* the Pearson chi-square test (without the Yates' correction for continuity) *or* an independent-sample t test for testing the equality of two independent binomial populations.

This was surprising to me so I applied both a chi-square test and a t-test to two data frames. The first data frame (mydata1) consists of 400 frequency quadrats, 200 of which were randomly located in a treatment area and 200 in a reference area. In each quadrat a target plant species was recorded either as present (1) or absent (0). The proportion of quadrats containing the plant was 0.54 in the reference area and 0.45 in the treatment area. The second data frame (mydata2) has the same number of frequency quadrats in both areas but frequencies (proportions of quadrats containing the plant) are much lower, only 0.04 for the reference area and 0.025 for the treatment area.

As shown below, a t test performed on the 0's and 1's gives essentially the same p value as a chi-square test on the same data.

Load needed packages and the two data frames and look at the first 6 rows of each data frame.
