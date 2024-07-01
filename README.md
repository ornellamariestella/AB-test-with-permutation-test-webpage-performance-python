> [!TIP]
> Read this first. 

# Comparing performance of two webpage designs: A/B Test with Permutation Test :mag:

In this case study, *the Product and Design teams* of a company have collaborated to restyle **an e-commerce webpage**, aiming to increase the conversion rate. 

The new version includes one major component change from the old one. I have **designed an A/B test** to compare performance between old and new pages, and assessed the statistical significance of our results using a **Permutation test**.

In real-world scenario, the design of the A/B test is shared with the Development team, which sets up the experiment and then shares results back. In this case, the output is a .csv file retrieved from Kaggle and loaded into VS code for data analysis.

## Design of the experiment :pencil2:

- **Baseline conversion rate** taken from GA4: 11.5%
- **Minimum detectable effect** decided by stakeholders: 1% increase
- [**Sample size**](https://www.evanmiller.org/ab-testing/sample-size.html#!11.5;80;5;1;0): minimum of 16154 per group (control and treatment)

The test is set to 50% of traffic diverted to the newly designed page, and 50% to the old (assigned randomly).

## Findings

### A/B test
- The **minimum sample size** per group (16154) for our set **minimum detectable effect** (%1 increase) has been reached.
- Both control and treatment groups have approximately the same sample size, indicating that our **50% traffic split worked**, despite having found a few inconsistencies that were quickly dropped.
- When looking at conversions, **the treatment group seems to have performed better than the control group**, suggesting that the new webpage performs better than the old page.

But is this result **statistically significant**? 

### Permutation test
- With an alpha level of 5%, **we accept the null hypothesis** (H0) and conclude that the observed result of our A/B test is **not statistically significant**.

*H0: treatment's conversion rate <= control's conversion rate // H1: treatment's conversion rate > control's conversion rate*

Thank you for checking out this case study! :star2: