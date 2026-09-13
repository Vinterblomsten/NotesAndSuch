#Statistics 

**Multiple comparisons problem**
When doing multiple statistical tests, there is a much higher chance of one of the test to get a significant result by chance
![[Screenshot 2025-04-10 at 09.25.12.png]]

The null-hypothesis significance testing (NHST) approach is closely connected to decision theory
![[Screenshot 2025-04-10 at 09.25.51.png|300]]
- Type I error (false positive)
- Type II error (false negative,next time)

**Type I error**
When rejecting $H_0$ incorrectly
- The error rate is controlled by the significance level $\alpha$

**Family wise error (FWE)**
When running multiple tests with significance $\alpha$ the overall probability of getting at least one type I error increases
- To maintain the error probability $\alpha$ on a family level we need adjustments
![[Pasted image 20250410093251.png|400]]

**Fischers least significant difference test (LSD-test)**
When we compare the results of **three** groups, Fisher’s LSD test protects the $\alpha$ on family level
- The LSD test **requires** the ANOVA 𝐹-test to be significant
- In the LSD test, the error variance for two groups is estimated by the pooled variance of all three groups:
$$
t=\frac{\bar{X_1}-\bar{X_2}}{\sqrt{s^2_p (\frac{1}{n_1}+\frac{1}{n_2})}}=\frac{\bar{X_1}-\bar{X_2}}{\sqrt{MSE(\frac{1}{n_1}+\frac{1}{n_2})}}
$$
**Bonferroni correction**
The Bonferroni correction is a simple correction, applicable across most contexts
- When running $c$ tests, the $\alpha$ level of each test is corrected to:
$$
\alpha=\frac{\alpha_{FWE}}{c}
$$
- This correction is often overly conservative and comes with a loss of power
- Should be avoided if other correction can be applied

**Holm's sequentially rejective test**
Has a much higher test power that Bonferroni, but is more complicated
- Begins by sorting the test statistics into a decreasing series
- The tests are then run one by one from the highest test statistic, where each test is run with the $\alpha$ level:
$$
1-(1-\alpha_{FW})^{1/c-i}
$$
- Where $c$ is the total number of tests and $i$ is the step in the testing sequence