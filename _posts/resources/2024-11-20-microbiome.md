---
layout: post
title: Microbiome basics
category: resources
image: https://media.licdn.com/dms/image/D5612AQENbGxsBiiBXA/article-cover_image-shrink_720_1280/0/1682668294084?e=2147483647&v=beta&t=o8W3gA2iYv0oL-ZQzqAU9UKn2ft21lSRa_ngd53hDzo
---
<!-- https://t4.ftcdn.net/jpg/08/13/85/15/360_F_813851569_Pm4OMS0rtCi4D3Y4Vgt76SI87MLUATNk.jpg -->
<!--  https://sbvu.ac.in/wp-content/uploads/2023/11/microbes-bacteria-7.jpg -->
<!-- since it is a post, they have always to start with a date!!!  -->


Microbiome analysis counts several aspects, yet it always comes down at some basic concepts! 
Here, I will try to cover a thing or two and gather some links that describe them more thoroughly.
To save some (of my) time, I will use a lot of copy-paste () always referring the initial resource 

**TABLE OF CONTENTS**
- [Microbiome data idiosyncrasy](#microbiome-data-idiosyncrasy)
  - [Covariate Adjustment](#covariate-adjustment)
- [Microbiome diversity](#microbiome-diversity)
  - [Diversity within a community](#diversity-within-a-community)
  - [Diversity between communities](#diversity-between-communities)
- [Feature Identification](#feature-identification)
  - [Differential Abundance Analysis](#differential-abundance-analysis)
  - [Mediation analysis](#mediation-analysis)
  - [Feature Identification Adjusting for Confounding](#feature-identification-adjusting-for-confounding)
- [Microbial phenomena that can drive you nuts!](#microbial-phenomena-that-can-drive-you-nuts)
  - [A strain dips to very low abundance in a microbial community and then recovers to thrive](#a-strain-dips-to-very-low-abundance-in-a-microbial-community-and-then-recovers-to-thrive)
  - [](#)
- [Literature](#literature)

---

## Microbiome data idiosyncrasy 


{:.quote-box}
> Although microbiome data has some of the attributes of compositional data, it is **not perfectly compositional**. 
>Classic compositional data vectors represent portions of a whole. The total sum of the components is not meaningful, and only the relative difference between components matters [36]. 
> For truly compositional data, the vectors (2, 1) and (2000, 1000) represent the same information: only that the first and second components are present in the ratio 2 : 1. 
>For microbiome data, **the size of the counts also contains information about the reliability of the ratio**. 
>Larger counts are more likely to closely match the true ratio in the sample [44].




### Covariate Adjustment

**Regression analysis**, potentially with **penalization for variable selection**, has been used to analyze an outcome of interest modeled as a function of microbiome features.


![covariate_challenge](https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-3-030-73351-3_7/MediaObjects/493285_1_En_7_Fig4_HTML.png)




## Microbiome diversity


### Diversity within a community 

**α-diversity** 

https://docs.onecodex.com/en/articles/4136553-alpha-diversity

Shannon Entropy (\(H'\))

$$
H' = - \sum_{i=1}^S p_i \ln(p_i)
$$

where:

- $$p_i$$ is the proportional abundance of species \(i\),
- $$S$$ is the total number of species.

The effective number of species based on Shannon entropy is:

$$
\text{Effective Number of Species} = e^{H'}
$$

---


### Diversity between communities 

**β-diversity** 



## Feature Identification

This sections is paraphrasing in a summary of the *[Liu et al.](https://doi.org/10.1007/978-3-030-73351-3_7) (2021)* chapter in the [Statistical Analysis of Microbiome Data](https://doi.org/10.1007/978-3-030-73351-3) book.

Questions to be addressed:

*  which microbiome features are impacted by treatments or environmental conditions? $$ \rightarrow $$ identify features whose abundances change across treatments or conditions differential $$ \rightarrow $$ **abundance analysis**
*  which microbiome features mediate treatment effects on an outcome? $$ \rightarrow $$ identify taxa affected by treatments and that because of their change the outcome of the treatment is influenced $$ \rightarrow $$ **mediation analysis**
*  which microbiome features have an effect on an outcome, adjusting for confounders  $$ \rightarrow $$ identify microbiome features with an effect on an outcome with no particular treatments of interest, but with potential complex confounding arising from relationships between microbes, host, and environment $$ \rightarrow $$ [**Feature Identification Adjusting for Confounding**](#feature-identification-adjusting-for-confounding)



### Differential Abundance Analysis 


 the null hypothesis of a differential abundance test is that treatments do not affect the mean abundance level. 

Differential abundance analysis (solid lines) selects microbiome features whose abundance levels change across treatments or conditions. It only examines the relationship between treatments/conditions and microbiome features, but not the relationships involving other outcomes

![DA](https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-3-030-73351-3_7/MediaObjects/493285_1_En_7_Fig2_HTML.png)



### Mediation analysis 

high dimensionality and sparsity of microbiome data.

In case of a *treatment - microbiome - outcome* study, one needs to avoid differential abundance analysis as the relationships you are looking for are out of scope for DA! 

Mediation analysis examines the **indirect effects of treatment on the outcome** through the microbiome. 
To determine whether a feature has a mediation effect, a method must **consider both the effect of the treatment on the feature and the effect of the feature on the outcome**.

![mediation](https://media.springernature.com/lw685/springer-static/image/chp%3A10.1007%2F978-3-030-73351-3_7/MediaObjects/493285_1_En_7_Fig3_HTML.png?as=webp)



### Feature Identification Adjusting for Confounding

asd




## Microbial phenomena that can drive you nuts! 


### A strain dips to very low abundance in a microbial community and then recovers to thrive

This is quite common and reflects the complex interplay of ecological, evolutionary, and environmental factors. 
[In this page](/insights/persistence.html) you can find some of the ways a strain might manage to survive during these low-abundance periods without going completely extinct.



### 


## Literature 

Datta, Somnath, and Subharup Guha, eds. [Statistical Analysis of Microbiome Data](https://link.springer.com/book/10.1007/978-3-030-73351-3). Springer International Publishing, 2021. 



<!-- As dilution rate would decrease, growth rates of A. muciniphila and Ruminococcaceae increase, while B. vulgatus and E. coli would decrease  -->
<!-- fast-growing species in all cultures were Escherichia coli and several species of Bacteroides, Dorea, and Lachnoclostridium -->

