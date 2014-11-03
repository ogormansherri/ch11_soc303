---
title       : Chapter 10 
subtitle    : One Way ANOVA
author      : Sherri Verdugo, M.S.
job         : Instructor, CSUF
framework   : deckjs        
highlighter : deck.js  
theme       : swiss
hitheme     : solarized_light      
widgets     : [mathjax, quiz, bootstrap]  
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Chapter 10 One Way ANOVA

### Sherri Verdugo, M.S.

### Instructor, CSUF

---

## Prologue & Introduction

The Analysis of Variance (ANOVA) can be used for more than one group. We are not limited to just one group. ANOVA is a powerful tool. 

### ANOVA is the statistical cousin to the t test.

* A technique for comparing sample means.
* Can be used for more than two means.
* Friendly to experimental testing. 
* Several sample means are being compared at once. 
* Overview of the process.
* Can be used to evaluate statistical tests.

---

## How Analysis of Variance is Used

Design for non experimental application with two variables:
     
     * One is interval level of measurement (usually the dependent)
     * Grouped data of any level of measurement. 
     * ANOVA is non-directional...meaning only non-directional hypothesis apply.
     

--- 

## Example of ANOVA Concept Introduction

### Abortion stance by rural and urban settings

Example of a non-experimental setting

Rural Group 1    | Urban Group 2
-----------------|--------------
160              | 100
130              | 110
150              | 130
140              | 120
$\Sigma X_1=580$ | $\Sigma X_2 =460$
$\bar{X}_1=145$  | $\bar{X}_2=115$

* Means differ
* Hypothesis: $H_0: \mu_1=\mu_2$ and $H_A: \mu_1 \neq \mu_2$
* ANOVA is NON-DIRECTIONAL
* Calculate the $F$ ratio (named Fisher, the original development)
* Compare the $F$ to $F_{critical}$ at $\alpha=0.5$

---

## Analysis of Variance in Experimental Settings

### Example 1: random groups

Experiments are the backbone of science. ANOVA is the most common used statistical technique. Participants or subjects are the people being studied in an experiment. 

* __Scenario__: Using a random sampling assignment of 30 subjects are assigned to one of three groups. Each group has 10 subjects. Because of the random assignment, any difference in mean satisfaction scores among the three groups will be the result of the time frame for the course (day, night, and Saturday) rather than any other factors. 

* Hypothesis for variable selection:

$H_0:\mu_{day}=\mu_{night}=\mu_{saturday}$

$H_A1:\mu_{day} \neq \mu_{night}$, $H_A2:\mu_{day} \neq \mu_{saturday}$, $\mu_{night} \neq \mu_{saturday}$

* Question: are the means different from each other to conclude they are not related to sampling error.

---

## ANOVA example 1 continued: DATA

Day   | Night  | Saturday
------|--------|----------
5     | 5      | 5 
5     | 4      | 5
5     | 4      | 5
5     | 3      | 4
4     | 3      | 4
4     | 2      | 4
4     | 2      | 3
4     | 2      | 3
3     | 1      | 3
2     | 0      | 2

* Sums for each group: $\Sigma X_D=41$, $\Sigma X_N=26$, and $\Sigma X_S = 38$
* Means for each group: $\overline{D}=\frac{41}{10}=4.1$, $\overline{N}=\frac{26}{10}=2.6$, and $\overline{S}=\frac{38}{10}=3.8$
* Question: the means are different...are they different enough to claim that they did not come from sampling error???

---

## F: an intuitive friendly approach

### Case 1: Day versus Night

Day               | Night
------------------|------
5                 | 5 
5                 | 5
5                 | 5
3                 | 3
3                 | 3
3                 | 3
$\Sigma x_D =24$  |$\Sigma x_D =24$
$\bar{x}_D=24/6=4$|$\bar{x}_D=24/6=4$

* The Grand Mean = $\Sigma G_M=\frac{48}{12}=4.00$
* We can use the F statistic here.

---

## F: an intuitive friendly approach

### Case 2: Day versus Night New Scores

Day                  | Night
---------------------|------
5                    | 5 
5                    | 5
5                    | 3
5                    | 3
3                    | 3
3                    | 3
$\Sigma x_D =26$     |$\Sigma x_D =22$
$\bar{x}_D=26/6=4.33$|$\bar{x}_D=22/6=3.67$

* The Grand Mean = $\Sigma G_M=\frac{48}{12}=4.00$
* F = 1.248
* The classes now differ a bit because of the satisfaction rating.

---

## F: an intuitive friendly approach

### Case 3: Day versus Night New Scores

Day                  | Night
---------------------|------
5                    | 5 
5                    | 3
5                    | 3
5                    | 3
5                    | 3
3                    | 3
$\Sigma x_D =28$     |$\Sigma x_D =20$
$\bar{x}_D=28/6=4.67$|$\bar{x}_D=20/6=3.33$

* The Grand Mean = $\Sigma G_M=\frac{48}{12}=4.00$
* F = 7.994
* The classes now differ a bit because of the satisfaction rating.

---

## F: an intuitive friendly approach

### Case 4: Day versus Night New Scores

Day                  | Night
---------------------|------
5                    | 3 
5                    | 3
5                    | 3
5                    | 3
5                    | 3
5                    | 3
$\Sigma x_D =30$     |$\Sigma x_D =18$
$\bar{x}_D=30/6=5.00$|$\bar{x}_D=18/6=3.00$

* The Grand Mean = $\Sigma G_M=\frac{48}{12}=4.00$
* F = mathematically undefined...it is getting larger though and approaching infinity as a limit.

---

## ANOVA Terminology: Getting to know ANOVA

Some new concepts are needed to deal with the calculations.

* Variance Estimate  = $\hat{\sigma}=\frac{\Sigma(x-\bar{x})^2}{n-1}$
* **Sum of Squares:** The sum of the squared deviations of the values of x from the mean.
* **Mean Square:** The mean squared deviation of a score (a value of x) from the mean of all scores. $MS=\frac{SS}{df}$
* **Total Sum of Squares:** The total of the squared deviations of scores about the grand mean. $SS_{TOTAL} = \Sigma x^2-\frac{(\Sigma x)^2}{n}$
* **Between-Groups Sums of Squares [page 328]:** $SS_{Between}=\frac{(\Sigma X_{cat.1})^2}{n_{cat.1}} + \frac{(\Sigma X_{cat.2})^2}{n_{cat.2}}+ ... + \frac{(\Sigma X_{last.cat})^2}{n_{last.cat}} - \frac{(\Sigma X_{total})^2}{n_{total}}$

---

## ANOVA Terminology: Getting to know ANOVA, continued

* **Between-Groups Sums of Squares:** The portion of the total sum of squares that can be accounted for by the variations of the category means about the grand mean. $SS_{Between}=\frac{(\Sigma X_{cat.1})^2}{n_{cat.1}} + \frac{(\Sigma X_{cat.2})^2}{n_{cat.2}}+ ... + \frac{(\Sigma X_{last.cat})^2}{n_{last.cat}} - \frac{(\Sigma X_{total})^2}{n_{total}}$
* **Within-Groups Sums of Squares (a.k.a. Error Sum of Squares) [page 328]:** The portion of the total sum of squares left unexplained by the variations of the category means about the grand mean. $SS_{Within}=SS_{Total}-SS_{Between}$

---

## ANOVA Terminology: Getting to know ANOVA, continued

### Summary Recap for Sum of Squares

* $SS_B$ = the portion of $SS_T$ accounted for by the categories of the independent variable.
* $SS_T$ = the portion of $SS_T$ not accounted for by the categories of the independent variable.
* Additive: $SS_T = SS_B + SS_W$
* We use both $SS_T$ and $SS_B$ to form two separate population variance estimates, these result in the between groups mean squares and between groups degrees of freedom.

---

## ANOVA Terminology: Getting to know ANOVA, continued

### Summary Recap for Mean Squares

* **Between-Groups Mean Square:** A variance estimate based on the between-groups sum of squares. $MS_{BETWEEN}=\frac{SS_B}{df_B}=\frac{SS_B}{num.categories - 1}$
* **Degrees of Freedom, between-groups Mean Squares:** $df_{between} = num.categories -1$
* **Within-Groups Mean Squares:** A population variance estimate based on what the categories of the independent variable do not explain --the variation of scores within the groups: $MS_{Within} = \frac{SS_{Within}}{df_{Within}} = \frac{SS_{Within}}{(n_{Total}-1)-(num.categories - 1)}$ 
* **Degrees of Freedom, Within-Groups Mean: That portion of the total degrees of freedom not accounted for by the number of groups studied. $df_W=(n_{Total}-1) - (num.categories - 1)$

---

## ANOVA Terminology: Getting to know ANOVA, continued

### Summary Recap for Mean Squares

$df_W=df_{total}-df{between}=(n-1)-(num.categories)-1$

So what is $MS_W$? 

* $MS_{Within} = \frac{SS_{Within}}{df_{Within}} = \frac{SS_{Within}}{(n_{Total}-1)-(num.categories - 1)}$
* The degrees of freedom are additive: 
     * $df_{total}=df_B+df_W$

---

## Key Concepts

* **One-Way Analysis of Variance (ANOVA) [page 318]:** A technique for comparing sample means that can be used to compare more than two means.  Analysis of variance with one dependent variable and one independent variable.
* **F/The F Ratio: [page 319]**: The statistic generated by the analysis of variance procedure.
* **Participants or Subjects in an Experiment [page 320]:** The people being studied in an experiment.
* **Grand Mean [page 323]:** The mean of all scores.
* **Sum of Squares [page 327]:** The sum of the squared deviations of the values of x from the mean.
* **Mean Square [page 327]:** The mean squared deviation of a score (a value of x) from the mean of all scores. $MS=\frac{SS}{df}$
* **Total Sum of Squares [page 328]:** The total of the squared deviations of scores about the grand mean. $SS_{TOTAL} = \Sigma x^2-\frac{(\Sigma x)^2}{n}$
* **Between-Groups Sums of Squares [page 328]:** The portion of the total sum of squares that can be accounted for by the variations of the category means about the grand mean. $SS_{Between}=\frac{(\Sigma X_{cat.1})^2}{n_{cat.1}} + \frac{(\Sigma X_{cat.2})^2}{n_{cat.2}}+ ... + \frac{(\Sigma X_{last.cat})^2}{n_{last.cat}} - \frac{(\Sigma X_{total})^2}{n_{total}}$
* **Within-Groups Sums of Squares (a.k.a. Error Sum of Squares) [page 328]:** The portion of the total sum of squares left unexplained by the variations of the category means about the grand mean. $SS_{Within}=SS_{Total}-SS_{Between}$
* **Between-Groups Mean Square [page 329]:** A variance estimate based on the between-groups sum of squares. $MS_{BETWEEN}=\frac{SS_B}{df_B}=\frac{SS_B}{num.categories - 1}$
* **Degrees of Freedom, between-groups Mean Squares [page 329]:** $df_{between} = num.categories -1$
* **Within-Groups Mean Squares [page 329]:** A population variance estimate based on what the categories of the independent variable do not explain --the variation of scores within the groups: $MS_{Within} = \frac{SS_{Within}}{df_{Within}} = \frac{SS_{Within}}{(n_{Total}-1)-(num.categories - 1)}$ 
* **Degrees of Freedom, Within-Groups Mean [page329]: That portion of the total degrees of freedom not accounted for by the number of groups studied. $df_W=(n_{Total}-1) - (num.categories - 1)$
* ANOVA source table
* Robustness (of a test of significance)
* Post hoc procedures/ post hoc test of multiple comparisons: [page 318]
          * A follow on procedure that is used once a null hypothesis has been rejected.
* Scheffe's test
* Scheffe's critical value
* Model SS
* Model MS
* Error SS
* Two-way analysis of variance/ two way ANOVA
* Interaction Effects

---

## Equations of Interest

* Grand Mean = $\frac{\Sigma X}{N}$ it is the mean of all scores divided by N.
* Variance Estimate  = $\hat{\sigma}=\frac{\Sigma(x-\bar{x})^2}{n-1}$

---

## Equations of Interest, Continued

* Analysis of Variance Components:
     * $SS_{Total}=\Sigma x^2_{Total}-\frac{(\Sigma x_{Total})^2}{n_{Total}}$
     * $SS_{Between}=\frac{(\Sigma X_{cat.1})^2}{n_{cat.1}} + \frac{(\Sigma X_{cat.2})^2}{n_{cat.2}}+ ... + \frac{(\Sigma X_{last.cat})^2}{n_{last.cat}} - \frac{(\Sigma X_{total})^2}{n_{total}}$
     * $SS_{Within}=SS_{Total}-SS_{Between}$
     * $MS_{Between} = \frac{SS_{Between}}{df_{Between}} = \frac{SS_{Between}}{num.categories - 1}$
     * $MS_{Within} = \frac{SS_{Within}}{df_{Within}} = \frac{SS_{Within}}{(n_{Total}-1)-(num.categories - 1)}$
     * $F=\frac{MS_{Between}}{MS_Within}$
     * $df=num.categories - 1$
     * $df_W=(n_{Total}-1) - (num.categories - 1)$


---

## Equations of Interest, Continued

* Scheffe's Test: For any two categories, $i$ and $j$, the following formula generates Scheffe's critical value.

     * $(\bar{X}_i - \bar{X}_j) = \pm \sqrt{(df_n)(F_{critical})(MS_W)(\frac{1}{n_i} + \frac{1}{n_j})}$
     
