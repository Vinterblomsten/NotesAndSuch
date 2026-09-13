#Statistics 
###### rANOVA
- The Repeated Measures Analysis of Variance respresents a decomposition og sources of variation into separate factors
- In addition to the standard ANOVA, the within-group, or residual variance (SSR), is divided further into variation between blocks (participants) and variation within blocks (residual variation)

Statistical model ($i$ : group/person, $j$ : block???):
$$
Y_{ij}=\mu+\alpha_j+\pi_i+\epsilon_{ij}
$$
With *random* effect:
$$ \pi_j \sim N(0,\sigma_\pi^2) $$
Sample estimators:


Variance:
- Total variance (SST): $SST=\sum\sum(Y_{ij}-\bar{Y})^2$
- Between-Groups, or explained variance (SSE): $SSE=n_j\sum(\bar{Y}_j-\bar{Y})^2$
- Between block variance: $SSBL=p_i\sum(\bar{Y}_i-\bar{Y})^2$
- Residual variance: $SSR=\sum\sum(Y_{ij}-\bar{Y}_i-\bar{Y_j}+\bar{Y})^2$

Hypothesis test:
$$\mu_1=\mu_2=...=\mu_p=\mu$$
$$\alpha_1=\alpha_2=...=\alpha_p=\alpha$$
- Test statistic:
$$ F_{(obs)}=\frac{SSE/df_1}{SSR/df_2} $$
$$F_{(obs)}\sim F(df_1, df_2)$$
$$df_1=k-1$$
$$df_2=N-k$$
$k$: number of groups, $N$: total number of messures 
- P-value:
$$p=P(F_{(obs)}>F)$$
