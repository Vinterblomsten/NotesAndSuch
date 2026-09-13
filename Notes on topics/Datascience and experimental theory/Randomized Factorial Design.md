#Statistics 

Design with two (or more) factors
- Factor $A$ with $p$ levels
- Factor $B$ with $q$ levels

Statistical model
$Y_{ijk}= \mu + \alpha_j+\beta_k+(\alpha\beta)_{jk}+\epsilon_{ijk}$

$\alpha_j$ and $\beta_k$ are **main effects** of the factors while $(\alpha\beta)_{jk}$ are an interaction effect


Subjects are randomly assign one of the $p \times q$ groups
- Members of each group receive "treatment" $a_j b_k$
- Each subject contributes a single measure $Y_{ijk}$

Hypothesis testing can be done by analysis of variance (or rANOVA)

#### **In the Sternberg experiment**
**The Sternberg model:**
![[Screenshot 2025-03-20 at 09.25.01.png]]

**Primary research question:**
- Is memory scanning **serial** and the comparison process **exhaustive**?


- Factor of target included or not included (two levels)
- Factor of target masked or unmasked (two levels) - not included in the model below
- Factor of number of letters (three level - 2, 3, 5)

Statistical model:
$y_{ij}=\mu+\alpha_j+\gamma_k+(\alpha\gamma)_{jk}+\pi_i+\epsilon$

with
- (Fixed) main effect $\alpha_j$
- (Fixed) main effect $\gamma_k$ of set size
- (Fixed) interaction effect  $\alpha\gamma_{jk}$
- (Random) person effect $\pi_i$ (random intercept model)

We don't expect any significant main effects of $\alpha$, no matter whether the comparison process if exhaustive or self-terminating, here we are interested in the interaction effect

The **primary outcome** or dependent variable is the mean RT, while the **secondary outcome** is the accuracy (not very important in this case). 

The linear mixed model in matrix design:
$y_i=X_i\beta+Z_i u_i + \epsilon_i$
 ![[Screenshot 2025-03-20 at 09.42.01.png]]
 
 **A better model** with LMM
$y_{ij}=\mu+\alpha_j+\gamma+(\alpha\gamma)_j+\pi_i+\epsilon$

With
- (Fixed/Discrete) main effect $\alpha_j$
- (**variable**/continuous) covariate $\gamma$
- (Fixed/Discrete) interaction effect $(\alpha\gamma)_j$ ,
- (Random) person effect $\pi_i$ (random intercept model)

In matrix notation for a single observation:
$y_i=X_i\beta+Z_i u_i+\epsilon_i$

Sternberg experiment, test for serial exhaustive memory search (1 factor with 2 levels, 1 covariate, 1 interaction
(Fourth column in the design matrix is merely column 2 times column 3)
![[Screenshot 2025-03-20 at 09.51.15.png]]

**Hypothesis investigation** $I_a$ - Serial vs Parallel
Based on Sternberg’s serial processing model, we predict an effect of set size (regression parameter* 𝜃) on mean reaction time

![[Screenshot 2025-03-20 at 09.54.23.png|300]]

**Hypothesis investigation** $I_b$ - Exhaustion vs Self-termiantion

Based on Sternberg’s serial self-terminating processing model, we predict a trial type × set size interaction effect (regression parameter 𝜃) on mean reaction time.

![[Screenshot 2025-03-20 at 09.57.32.png|300]]


#### Coding in R
![[Screenshot 2025-03-20 at 09.58.28.png]]
