---
id: "Scholz_1996_Weibull-Plotting"
source_pdf: "../pdf/Scholz_1996_Weibull-Plotting.pdf"
source_filename: "Scholz_1996_Weibull-Plotting.pdf"
format: "academic-paper"
extraction_profile: "text-math-tables-high-fidelity"
extraction_mode: "full-page-ocr"
extraction_quality: "excellent"
extraction_score: 106.0
visual_assets: "disabled"
references_file: "../references/Scholz_1996_Weibull-Plotting.references.md"
---

<!-- p:1 -->

## Plotting on Weibull Paper

#### Fritz Scholz Research and Technology Boeing Information &amp; Support Services

##### August 23, 1996

###### Abstract

This report explains Weibull plotting and its rationale. It shows how the two Weibull parameter estimates are easily read off from the Weibull plot. The use of Weibull plotting is introduced first in the context of complete samples and then extended to two common forms of censoring: type I or multiple censoring and type II censoring. Two blank Weibull plotting templates are provided, one for a two cycle log1o scaee  e s  tssse e o se  e l e e  e ul plot as a diagnostic tool for checking the Weibull assumption underlying the sample is examined critically. For small sample sizes, answers, if obtained via this tool, should be taken with caution, since the variability of such Weibull samples is still substantial.


<!-- p:2 -->


##### 1Introduction

In characterizing the distribution of life lengths or failure times of certain devices one often employs the Weibull distribution. This is mainly due to its weakest link properties, but other reasons are its increasing1 failure rate with device age and the variety of distribution shapes that the Weibull density offers. The increasing failure rate accounts to some extent for fatigue failures.

Weibull plotting is a graphical method for informally checking on the assumption of Weibull distribution model and also for estimating the two Weibull parameters. The method of Weibull plotting is explained and illustrated both for complete samples of failure times as well as for censored samples. In the latter case we consider either type I or multiply censored data or type II censored data. Type I or multiple censoring occurs typically in field data where either the failure times of devices are observed or their last running time is known, r r ts       rs t ts  r multiple censoring instead of type I censoring is motivated by the multiple time points at which some censoring event takes place and prevents the observation of the complete life time. The censoring time points are extraneous events and independent of the actual device failure times, whether these are observed or not. This is in contrast to type II censoring. This occurs mostly under laboratory conditions when all n devices are put on test at the same time and one observes the failure times of the first r devices, with the remaining n − r devices still running successfully. This kind of censoring is useful when one cannot wait until all devices have failed, but wants to guarantee at least so many failures. Here the censoring time is not independent of the failure times, since it coincides with the rth smallest failure time.

It is assumed that the two-parameter Weibull distribution is a reasonable model for describing the variability in the failure time data. If T represents the generic failure time of a device, then the distribution function of T is given by

$$F _ { T } ( t ) = P ( T \leq t ) = 1 - \exp \left ( - \left [ \frac { t } { \alpha } \right ] ^ { \beta } \right ) \quad \text {for } t \geq 0 \, .$$

The parameter α is called the scale parameter or characteristic life. The latter term is motivated by the property FT(α) = 1 − exp(−1) ≈ .632, regardless of the shape parameter β. There are many ways for estimating the parameters α and β from complete or censored data. One of the simplest is through the method of Weibull plotting, which is very popular due to its simplicity, graphical appeal, and its informal check on the Weibull model assumption.

1for Weibull shape parameter β &gt; 1


<!-- p:3 -->


###### 2 Weibull Plotting and its Basis

The basic idea behind Weibull plotting is the relationship between the p-quantiles tp of the Weibull distribution and p for 0 &lt; p &lt; 1. The p-quantile tp is defined by the following property

which leads to

$$p = F _ { T } ( t _ { p } ) = P ( T \leq t _ { p } ) = 1 - \exp \left ( - \left [ \frac { t _ { p } } { \alpha } \right ] ^ { \beta } \right )$$

$$t _ { p } = \alpha \left [ - \log _ { e } \left ( 1 - p \right ) \right ] ^ { 1 / \beta }$$

or taking decimal logs2 on both sides

$$y _ { p } = \log _ { 1 0 } ( t _ { p } ) = \log _ { 1 0 } ( \alpha ) + \frac { 1 } { \beta } \log _ { 1 0 } \left [ - \log _ { e } \left ( 1 - p \right ) \right ] \ .$$

Thus log1o(tp), when plotted against w(p) = log1o [− loge (1 − p)] should follow a straight line pattern with intercept log1o(α) and slope 1/β. Plotting w(p) against yp = log10(tp), as is usually done in a Weibull plot, one should see the following linear relationship

$$w ( p ) = \beta [ \log _ { 1 0 } ( t _ { p } ) - \log _ { 1 0 } ( \alpha ) ]$$

with slope β and abscissa intercept log10(α).

In place of the unknown log1o-quantiles log1o(tp) one uses the corresponding sample quantiles. For a complete sample, T1, . . . , Tn, these are obtained by ordering these Ti from smallest to largest to get T(1) ≤ . .. ≤ T(n) and then associate with pi = i/(n + 1) the pi-quantile estimate or ith sample quantile T(i). These sample quantiles tend to vary around the respective population quantiles tpi. For large sample sample sizes and for pi = i/(n + 1) ≈ p with 0 &lt; p &lt; 1 this variation diminishes (i.e., the sample quantile T(i) converges to tp in a sense not made precise here). For pi close to 0 or 1 the sample quantiles T(i) may (or may not) exhibit high variability even in large samples. Thus one has to be careful in interpreting extreme sample values in Weibull plots.

The idea of Weibull plotting for a complete sample is to plot w(pi) = log10 [− loge (1 − pi)] ag d o  dt r (t o   ot ot nt  (e asoo equation (2), then see a roughly linear pattern.

This plotting is facilitated by Weibull paper with a log1o-transformed abscissa with untransformed labels and a transformed ordinate scale given by w(p) = log1o [− loge (1 − p)]

2The explicit notation log1o and loge is used to distinguish decimal and natural logs.


<!-- p:4 -->


with labels in terms of p. Sometimes this scale is labeled in percent ( i.e., in terms of 100p%). Two blank samples of such Weibull probability paper are given as the first two figures in Appendix A, although they are not labeled as Figure 1 or Figure 2. Figure 1 has two log1o cycles on the abscissa, facilitating plotting of failure times over two orders of magnitudes and Figure 2 has three cycles on the abscissa, facilitating plotting of failure times over three orders of magnitudes.

For each plotting point (log10(T(i)), w(pi)) one locates or interpolates the label value of T(i) on the abscissa and the value pi on the ordinate, i.e., there is no need for the user to perform the transformations log10(T(i)) and w(pi) = log10 [− loge (1 − pi)]. An example of a complete sample plotted on Weibull paper is given in Figure 3 of Appendix A. Figure 3 shows three lines. The dashed line represents the true line corresponding to the Weibull distribution from which the ten values were sampled. The other two lines represent a least squares fit (the formulas for which will be given later) and the other corresponds to maximum likelihood estimates (m.1.e.) of α and β. The process of finding the m.l.e.'s is complicated and usually accomplished through software. Note how susceptible the least squares fit is to the two lower extreme values. This is not surprising since the method of least squares, as applied here, treats all data equally. It does not know that the data come from a Weibull distribution and represent ordered and thus correlated values. The method of maximum likelihood employs the fact that the data come from a Weibull model and knows how to properly weigh the various observations, i.e., stragglers as they show up in Figure 3 will not be given undue influence.

The two blank specimens of Weibull probability paper in Appendix A cover two and three orders of magnitude on the abscissa, namely from 1 to 100 or from 1 to 1000. If the observed life times cover a range from 50 to 4000, one can simply change time units to tens and use the three log1o cycle paper from 5 to 400, which fits. If the ranges are very large, one may have to use Weibull paper covering more orders of magnitude. However, there is a simple transformation device around that difficulty. It is based on the following power transformation property of the Weibull distribution. If T ∼ W(α, β) (i.e., T has a Weibull distribution with parameters α and β), then

$$T ^ { a } \sim \mathcal { W } ( \alpha ^ { a } , \beta / a ) = \mathcal { W } ( \alpha ^ { \prime } , \beta ^ { \prime } ) \ .$$

Thus one can always bring the scale of the failure times up or down into the proper range by an appropriate power transformation.

By eye or by more formal least squares methods one can then fit a line through the po on  o os o  oes ne og  e e o ne  own linear relationship (2) between the quantiles yp and w(p). Here the least squares fit will be quite sensitive to variability in the extreme sample values. Trying allow for that in fitting by eye will be somewhat subjective.


<!-- p:5 -->


Since p = 0.632 yields w(p) = 0 or log10(T) − log10(α) = 0 one can read off an estimate of α from the abscissa scale where the fitted line intercepts the ordinate level 0.632. For this purpose Weibull paper shows a level line at the ordinate 0.632. On the right side scale of the Weibull probability paper one finds the zero value resulting from the transform w(0.632) = 0.

The scale to the left of the ordinate scale runs from zero to ten and is a nomographic device for reading off the estimated shape parameter associated with the line fitted to the plotted data. To obtain it one draws a line parallel to the fitted line going through the solid dot to the right of that shape scale. Appendix A contains several examples illustrating this process.

Some authors suggest to use of pi = (i − .3)/(n + .4) in place of pi to characterize the p for which T(i) is the p-quantile. For large n there is little difference between the two methods and for small n the inherent variability in Weibull samples makes a preference between the two methods somewhat questionable.

### 3 Plotting with Type I Censoring

Under this type of censoring the censoring times and failure times typically intermingle and it is no longer quite so clear for which quantile to consider each failure time as a quantile estimate. There are various schemes of dealing with this problem. The one presented here is the Herd-Johnson method as given in Nelson (1982).

One orders all observations, censored or uncensored, from smallest to largest and one ranks them in reverse order. If T(1) ≤ ... ≤ T(n) are the ordered observations, their corresponding reverse ranks are (r1, . . . , rn) = (n, . . . , 1). For the ith failure one computes recursively the "reliability"

$$R _ { i } = \frac { r _ { ( i ) } } { r _ { ( i ) } + 1 } \ R _ { i - 1 }$$

where R0 = 1 is the reliability or survival probability at time 0. Here the distinction of r(i) and ri is the following. Whereas ri = n − i + 1 represents the reverse rank of the ith ordered obseryation (censored or uncensored), the notation r(i) is the reverse rank associated with the ith ordered failure time. For example, if the first failure time is preceded by two censoring times, then r1 = n, r2 = n − 1, r3 = n − 2 = r(1). The sample calculations in Table 1 should clarify this further.


<!-- p:6 -->


In the above recursive formula for Ri one can view r(i)/(r(i) + 1) as an estimate of the conditional probability of survival at the time of the ith failure, since at the ith failure there are r(i) items, one has just failed and the other r(i) - 1 survived. Thus the proportion of survived items is (r(i) — 1)/r(i). Since this can lead to zero values, which cause problems in probability plotting, one modifies this conditional probability estimate to r(i)/(r(i) + 1). Ri-1 is the estimate of survival prior to ith failure and Ri is the estimate of survival after the ith failure.

As an aside, the proportion (r(i) − 1)/r(i) figures strongly in the definition of the survival function estimate due to Kaplan and Meier (1958). This estimate is defined by

$$R _ { i } ^ { \prime } = \frac { r _ { ( i ) } - 1 } { r _ { ( i ) } } \ R _ { i - 1 } ^ { \prime }$$

with R = 1. Kaplan and Meier show that the step function with steps fi = 1 − Ri at the ¿th failure time is the nonparametric maximum likelihood estimate of the distribution function of failure times without reference to a Weibull model. See Scholz (1980) for a proper definition of maximum likelihood in such wider nonparametric settings.

Returning to the recursion defining Ri, the pi plotting position for the ith failure time is then taken as pi = 1 — Ri. Note that the index i here counts consecutively through the failure times. No points are plotted corresponding to the censored times. If there are no censoring times, this method reduces to the above method of using pi = i/(n + 1) in complete samples and can be viewed as a reason for preferring this method over others.

An example calculation is presented in Table 1, which is taken from Nelson (1982). The corresponding Weibull plot is illustrated in Figure 4 of Appendix A. Note that the time units were viewed in tens since the failure data range is [31.7, 110.0] and a two cycle log1o Weibull paper was used.

From the Weibull plot one can read off the following estimates for α and β, namely α ≈ 125 and β ≈ 1.99. The line was fitted by the method of least squares. To do so one has to work with the transformed failure times Yl¿] = log10(T[ij) and with the corresponding values w(p[i]) = log1o[− loge(1 - p[i])]. The square brackets around the subscripts indicate that the numbering is consecutive along the k failures. In the example of Table 1 this is along 1, 2, . .. , 7, since there are k = 7 failure times. The least squares calculations use the following formulas

$$\widehat { \beta } = \frac { \sum _ { i = 1 } ^ { k } w ( p _ { [ i ] } ) ( Y _ { [ i ] } - \overline { Y } ) } { \sum _ { i = 1 } ^ { k } ( Y _ { [ i ] } - \overline { Y } ) ^ { 2 } } \quad \text {with} \quad \overline { Y } = \frac { 1 } { k } \sum _ { i = 1 } ^ { k } Y _ { [ i ] }$$


<!-- p:7 -->


Table 1: Winding Data &amp; Herd-Johnson Calculations

| Time                                                                         | Reverse Rank r i   | Reliability/Survival Probability - Cond'l r ( i ) / ( r ( i ) +1)   | Reliability/Survival Probability - ×   | Reliability/Survival Probability - Previous R i - 1   | Reliability/Survival Probability - =   | Reliability/Survival Probability - Current R i   | Failure Prob. p i = 1 - R i   |
|------------------------------------------------------------------------------|--------------------|---------------------------------------------------------------------|----------------------------------------|-------------------------------------------------------|----------------------------------------|--------------------------------------------------|-------------------------------|
| 31.7 39.2 57.5 65.0 + 65.8 70.0 75.0 + 75.0 + 87.5 + 88.3 + 94.2 + + 105.8 + | 16 15 14           | (16/17) (15/16)                                                     | × ×                                    | 1.000 0.941                                           | =                                      | 0.941 0.883                                      | .059 .117 .176                |
|                                                                              |                    |                                                                     |                                        |                                                       | =                                      |                                                  |                               |
|                                                                              |                    | (14/15)                                                             | ×                                      | 0.883                                                 | =                                      | 0.824                                            |                               |
|                                                                              | 13                 |                                                                     |                                        |                                                       |                                        |                                                  |                               |
|                                                                              | 12                 | (12/13)                                                             | ×                                      | 0.824                                                 | =                                      | 0.761                                            | .239                          |
|                                                                              | 11                 | (11/12)                                                             | ×                                      | 0.761                                                 | =                                      | 0.697                                            | .303                          |
|                                                                              | 10 9               |                                                                     |                                        |                                                       |                                        |                                                  |                               |
|                                                                              | 8                  |                                                                     |                                        |                                                       |                                        |                                                  |                               |
|                                                                              | 7 6                |                                                                     |                                        |                                                       |                                        |                                                  |                               |
|                                                                              | 5                  |                                                                     |                                        |                                                       |                                        |                                                  |                               |
| 101.7                                                                        | 4                  | (4/5)                                                               | ×                                      | 0.697                                                 | =                                      | 0.557                                            | .443                          |
| 109.2                                                                        | 3                  |                                                                     |                                        |                                                       |                                        |                                                  |                               |
| 110.0                                                                        | 2                  | (2/3)                                                               | ×                                      | 0.557                                                 | =                                      | 0.372                                            | .628                          |
| 130.0 +                                                                      | 1                  |                                                                     |                                        |                                                       |                                        |                                                  |                               |


<!-- p:8 -->


and

$$- \widehat { \beta } \log _ { 1 0 } ( \widehat { \alpha } ) = \overline { w } - \widehat { \beta } \ \overline { Y } \quad \text {with} \quad \overline { w } = \frac { 1 } { k } \sum _ { i = 1 } ^ { k } w ( p _ { [ i ] } ) \ .$$

The estimates from the least squares calculations are  = 123.3 and β = 1.986.

Since the variability is in the Yli] and not in the w(p[i]) one may prefer doing the least squares calculations with abscissa and ordinate reversed, i.e., according to the model (1). In that case one obtains

and

$$\text {one obtainals} \\ \frac { 1 } { \widehat { \beta } } = \frac { \sum _ { i = 1 } ^ { k } ( w ( p _ { [ i ] } ) - \overline { w } ) Y _ { [ i ] } } { \sum _ { i = 1 } ^ { k } ( w ( p _ { [ i ] } ) - \overline { w } ) ^ { 2 } } \quad \text {with} \quad \overline { w } = \frac { 1 } { k } \sum _ { i = 1 } ^ { k } w ( p _ { [ i ] } ) \\ \log _ { 1 0 } ( \widehat { \alpha } ) = \overline { Y } - \overline { w } / \widehat { \beta } \quad \text {with} \quad \overline { Y } = \frac { 1 } { k } \sum _ { i = 1 } ^ { k } Y _ { [ i ] } \, . \\ \intertext { t h e s a m o b s i l s } \widehat { \alpha } \, \text {and} \, \widehat { \beta } \, \text {where used, their values will not be the same}$$

Although the same symbols  and β were used, their values will not be the same under the two least squares approaches. In fact, for this last method the least squares estimates are α = 120.5 and β = 2.055. The resulting fitted line is indicated by the dashed line in Figure 4. Also shown is the line resulting from the maximum likelihood estimates with  = 123.2 and β = 2.376.

### 4 Plotting with Type II Censoring

Here the observed data consist of T(1) ≤ ... ≤ T(r) and all that is known about the other n − r (future) failure times is that they exceed T(r). Since these first r ordered failures are the quantile estimates of tp1, . . . , tpr with pi = i/(n + 1) one can again plot these r points as before on Weibull paper, the only difference being that the n - r censored points are not plotted.

Again one can fit a line by eye or by least squares. However here the low extremes will weigh in more heavily since the upper extremes are missing. As an example, the six lowest values of the complete sample underlying Figure 3 were taken as a type II censored sample and are plotted in Figure 5. As in Figure 3 the true line, the least squares fit line, and the line corresponding to the maximum likelihood estimates are shown. Note that the latter is reasonably close to the true line, whereas the least squares line is led astray substantially.


<!-- p:9 -->


#### 5 Checking the Weibull Model

According to the motivation behind Weibull plotting one expects to see a roughly linear pattern in the plotted points. The examples shown so far may have put a damper on this, but that is mainly due to the small sample sizes in those examples. Some of the examples were artificially generated from Weibull populations. Thus there is no question about their origin. However, the example given by Nelson is supposed to be real data and its pattern on Weibull paper looks remarkably close to linear. This has been observed in other expositions on Weibull plotting as well and it may raise false expectations in the prospective user. When nonlinear patterns are found (in small samples) the user may then be led on false chase for other causes, such as multiple failure modes. There may well be such multiple modes, but small samples are not a good starting point to look for these.

In order to get a sense for the effect of sample size on the variability in linear Weibull 0 =   =   =  ses es   as  ss a  sd and were plotted on an equivalent of Weibull probability paper (without the grid lines, etc.), see Figures 6-8. Also shown on each plot is the true line corresponding to the Weibull distribution from which the sample was drawn. The sample to sample variability at n = 10 is substantial whereas the linearity and proximity to the true line is quite satisfactory at n = 100.

## Appendix A

This appendix contains two blank copies of Weibull probability paper (without page number). The first has a two cycle log1o scale on the abscissa and the second has a three cycle log1o scale. This is followed by several illustrations of Weibull paper with plotted samples.

Figure 3 illustrates the plotting of a complete Weibull sample with three line superimposed: 1) the true line representing the sampled Weibull population, 2) a least squares fitted line (which is strongly influenced by stragglers), and 3) a line corresponding to maximum likelihood estimates of the paramters.

F rs os  ns   e   g tos ste  ota taken from Nelson (1982). Aside from the maximum likelihood fitted line there are two types of least squares lines. In one the ordinate is regressed on the abscissa and in the other the abscissa is regressed on the ordinate.

Figure 5 illustrates the plotting of a type II censored sample by taking the six lowest failure times from the complete sample underlying Figure 3. Again the true line, the least squares fitted line and the maximum likelihood fitted lines are shown.

Figure 6-8 show a collection of eight random samples, each taken from a Weibull popuats e  e e  e e e =  s  ss se ss  e plots for sample sizes n = 30 and n = 100, respectively. On each plot the thick represents the true sampled Weibull population and the thin line is the least squares fitted line.


<!-- p:11 -->


10

### Weibull Probability Paper – 2 Cycle Log

0

0.0

0.2

0.4

0.6

0.8

1.0

1.2

1.4

1.6

1.8

2.0

6666

1.0

666

.995

66

.95

0.5

2

.90

.632

0.0

3

.5

-0.5

4

.1

-1.0

5

.05

-1.5

6

.01

-2.0

7

.005

-2.5

8

.001

-3.0

9

.0005

-3.5

.0001

-4.0

1

2

3

4

5

10

20

30

40

50

100


<!-- p:12 -->


10

### Weibull Probability Paper – 3 Cycle Log

0

0.0

0.2

0.4

0.6

0.8

1.0

1.2

1.4

1.6

1.8

2.0

2.2

2.4

2.6

2.8

3.0

1.0

6666

.999

.995

66

.95

0.5

.90

.632

0.0

3

.5

-0.5

-1.0

5

.05

-1.5

.01

-2.0

.005

-2.5

.001

-3.0

.0005

-3.5

.0001

-4.0

1

2

3

4

5

10

20

30 40 50

100

200

300400 500

1000


<!-- p:13 -->


10

Weibull Probability Paper – 2 Cycle Log

Figure 3

Complete Sample

0.0

0.2

0.4

0.6

0.8

1.0

1.2

1.4

1.6

1.8

2.0

1.0

6666

666

.995

.99

maximum likelihood estimate

least squares estimate

0.5

true line, equation (1)

.90

●

.632

0.0

.5

-0.5

.1

-1.0

.05

-1.5

.01

-2.0

.005

-2.5

.001

-3.0

.0005

-3.5

.0001

-4.0

1

2

3

4

5

10

20

30

40

50

100


<!-- p:14 -->


10

Weibull Probability Paper – 2 Cycle Log

Type I Censored Sample

0.0

0.2

0.4

0.6

0.8

1.0

1.2

1.4

1.6

1.8

2.0

1.0

6666

.999

.993

66

.95

0.5

2

.90

.632

0.0

.5

maximum likelihood estimate

least squares estimate, y vs x

---- least squares estimate, x vs y

-0.5

●

.1

-1.0

.05

-1.5

.01

-2.0

.005

-2.5

.001

-3.0

.0005

-3.5

.0001

-4.0

1

2

3

4

5

10

20

30

40

50

100

Figure 4


<!-- p:15 -->


10

Weibull Probability Paper – 2 Cycle Log

Type II Censored Sample

0.0

0/2

0.4

0.6

0.8

1.0

1.2

1.4

1.6

1.8

2.0

1.0

6666

1999

.995

66

maximum likelihood estimate

.95

least squares estimate

0.5

true line, equation (1)

.90

.632

0.0

.5

-0.5

.1

-1.0

.05

-1.5

.01

-2.0

.005

-2.5

.001

-3.0

.0005

-3.5

.0001

-4.0

1

2

3

4

5

10

20

30

40

50

100

Figure 5


<!-- p:16 -->


Figure 6: Weibull Probability Plots

-0.20.2

02

log10[-In(1-p)]

sample size n = 10

-0.2

-0.6


-1.0


1.0

1.5

2.0

1.0

1.5

2.0

log10(T)

02


-0.2


-0.6


-1.0


1.0

1.5

2.0

1.0

1.5

2.0

0.2

02

-0.2


-0.6


-1.0


1.0

1.5

2.0

1.0

1.5

2.0

02


-0.2


-0.6


-1.0


1.0

1.5

2.0

1.0

1.5

2.0


<!-- p:17 -->


Figure 7: Weibull Probability Plots

0.5


log10[-In(1-p)]

0.0

sample size n = 30

0.0

-0.5


-1.0


-1.5


1.0

1.2

1.4

1.6

1.8

2.0

2.2

1.0

1.2

1.4

1.6

1.8

2.0

2.2

log10(T)

0.5


0.0


-0.5


-1.5 -1.0

-1.0

-1.5

1.0

1.2

1.4

1.6

1.8

2.0

2.2

1.0

1.2

1.4

1.6

1.8

2.0

2.2

0.5

05

0.0


-0.5


-1.0

-1.5-1.0

-1.5

1.0

1.2

1.4

1.6

1.8

2.0

2.2

1.0

1.2

1.4

1.6

1.8

2.0

2.2

0.5


0.0


-0.5

-1.5-1.0-0.5

-1.5 -1.0

1.0

1.2

1.4

1.6

1.8

2.0

2.2

1.0

1.2

1.4

1.6

1.8

2.0

2.2


<!-- p:18 -->


Figure 8: Weibull Probability Plots

0.00.5


log10[-In(1-p)]

sample size n = 100

-1.0


-2.0


0.5

1.0

1.5

2.0

0.5

1.0

1.5

2.0

log10(T)

0.0 0.5


-1.0


-2.0


0.5

1.0

1.5

2.0

0.5

1.0

1.5

2.0

0.00.5

0.0 0.5

-1.0


-2.0


0.5

1.0

1.5

2.0

0.5

1.0

1.5

2.0

0.00.5


-1.0


-2.0


0.5

1.0

1.5

2.0

0.5

1.0

1.5

2.0
