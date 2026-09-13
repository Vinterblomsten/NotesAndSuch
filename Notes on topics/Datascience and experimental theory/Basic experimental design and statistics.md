#Statistics 
**Basic experimental design**
Every cognitive experiment is build upon a hypotesis, that we wish to test.

For example:

"The longer looking time we have of a group of objects, the larger number of objects will we remember"

**Kim's game** - A slide with 20 objects which we look at for 10 (x) seconds at first. In this test, the number of objects we remember is **the dependent variable** of which we measure, and the time we have to look is **the independent variable** which is something that must be entirely under the experimenters control. 

8 objecter husket

###### Statistical models
**Before** every experiment, we must have decided upon a statistical model - never after we have gathered the data.
##### **Different experimental designs**
###### **Completely Randomized Design** (CRD)
between-subjects design
- Randomized clinical trail (RTC)
- different subjects to the experiments with different values of the independent variable

**Statistical model**
$$Y_{ij}=\mu+\alpha_j+\epsilon_{ij} $$
- Subjects are randomly allocated to group a_j,  (j=1..p) og Factor A with $p\geq2$ levels.
- Each Subject I contributes a single measure $Y_{ij}$
- Effects of interest $\alpha_j$
- Hypothesis testing: 
	- t-test, if $p=2$
	- ANOVA (analysis of variance), if $p\geq2$

Pros and cons
- One sample per participant
	- Require many participants
	- If the groups are truly randomly distributed, the groups may be different sizes
- With small sampke sized other factors may skew the results
- CRD works very well when the testing only can be performed once (for example with medical treatment tests) - we avoid carry-over effects 
![[Screenshot 2025-02-06 at 09.16.06.png|400]]
###### **Randomized Block Design** (RBD)


**Statistical model**
- Subjects are blocked into 𝑖 = 1, ... , 𝑛 groups (𝑗-tuples) to stratify a nuisance effect
- Members of each group are then randomly allocated to treatment $a_j$ , (𝑗 = 1, ... , 𝑝), of Factor 𝐴 with 𝑝 ≥ 2
- Each subject contributes a single measure $Y_{ij}$
- Effects of interest: $\alpha_j$
- Hypothesis testing:
	- Paired t-test, if $p=2$
	- rANOVA (Repeated Measures Analysis of Variance), if $p\geq2$
![[Screenshot 2025-02-06 at 09.18.53.png|300]]
###### **Repeated Measure Design (RMD)**
- Each subjects are randomly put into one of two groups:
	- 1. does the baseline-condition assessment first and then the experimental-condition assessment afterwords
	- 2. does the opposite
* This means that we need a smaller population size and that 
* As a rule of thumb, we always use RMD instead of CRD unless there is a reason not to do so
* Matemathically equivalent to RBD, in which on subject forms a "block" and is assigned to all $\alpha_j$
* Requires that you can assume independence of the "treatments/levels of a factor" - that is there should be no learning from treatment to treatment, hence not possible to use the same stimulus set several times.

**Statistical Model**
$$Y_{ij}=\mu+\alpha_j+\pi_i+\epsilon_{ij}$$
- One subject is assigned to all $\alpha_j$, (j=1..p), levels of factor A with $p\geq2$
	- Each subjects is tested under all conditions
	- Each subject i contributes p measures
	- The order of the a_j is typically randomized across the different subjects
- Effects of interest: $\alpha_j$
- Hypothesis testing:
	- Paired t-test, if $p=2$
	- rANOVA (Repeated Measures Analysis of Variance), if $p\geq2$

![[Screenshot 2025-02-06 at 09.30.28.png|300]]
###### **(Completely) Randomized Factorial Design**
- Two or more factors where we test difference of two different independent variables
- full factorial design

**Statistical model**
![[Screenshot 2025-02-06 at 09.52.24.png|400]]
- Design with two or more factors
	- Factor A with p levels
	- Factor B with q levels
- Saubjects are randomally assignmed to one of the p x q groups
- Members of each group recieve tratment $\alpha_j \beta_k$ (j=1..p og k=1..q)
- Each subject contributes a single measure $Y_{ijk}$
- Effects of interest:  $a_{ij}$,$\beta_k$,$\alpha\beta_{jk}$
- Hypothesis testing:
	- ANOVA

**Hierarchical Design**
- Nested factorial design
- When we need to take into account factors, that w e cannot randomize

###### The linear model
- Den simpleste model og dermed den oftest mest brugbare til analyse af de forskellige designs
- Denne må udvides til at indeholde arbitrært mange uafhængige variabler og dertilhørende konstanter
![[Screenshot 2025-02-06 at 09.50.30.png|400]]
- Categorical Predictors
	- A categorical predictor 𝑗 is a discrete predictor that takes one of two values
	![[Screenshot 2025-02-06 at 10.02.00.png|300]]
	- With a single categorical predictor, we can code two groups. In general, we need 𝑝 − 1 predictors to include 𝑝 groups in our design
	- For example when doing an experiment with three groups, where one is a reference group, the model would look as so: $y_i=\beta_0+\beta_1 x_{i1}+\beta_2 x_{i2}+\epsilon_i$
	- Where the values for $x_{i1}=\{ \begin{matrix}   0 & else \\   1 & if group 2   \end{matrix}$ 
	- 