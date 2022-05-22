---
layout: post
title: Lab 5 First Draft
subtitle: By Tuhin Ghosh
tags: [lab]
comments: true
---

#  An Analysis of Private College Endowments
##  By: Tuhin Ghosh

## Background

The United States higher education system is one of the best globally, with renowned institutions like Harvard University and the Massachusetts Institute of Technology providing top-notch education to its students. Such institutions house faculty who are leaders in their respective fields, state-of-the-art resources, and boundless opportunities for undergraduate, graduate, and Ph.D. students alike. To garner such a repertoire of tools, colleges have established endowments to provide a steady income stream to institutions. Apart from this stability, endowments enable colleges to increase spending on students, financial aid, diminishing the negative impact of low economic well-being on students’ education. Moreover, endowments allow colleges to make long-term plans with the security of the necessary funds.

However, the value of a university’s endowments is far from being spread evenly. In 2019, the top 20 institutions with the largest endowments made up 50% of the total value of the endowments of the 786 institutions surveyed (National Association of College and University Business Officers (NACUBO), and Teachers Insurance and Annuity Association (TIAA) survey, 2019). 

Looking back, the values of these endowments have increased significantly over the past decade with Harvard breaking $40 billion in the Fiscal Year of 2020, starting at $27.4 billion in 2010(NACUBO and TIAA Survey).  

Understanding the drivers behind the increase and general value of endowments is imperative to demystify college endowments’ nature in the United States. These endowments play such a significant role in improving the students’ experience, providing funds for planning, and demonstrating the propensity of an institution’s alumni base to donate. What is driving this skewed distribution? What separates the predictors of higher-end institutions from lower-end ones? What separates private institutions’ endowments from other types of institutions’ endowments? 

As mentioned before, endowments have various uses in United States post-secondary institutions, such as reducing costs for students or security in long-term projects (ACE, 2021). In terms of the makeup of the endowment itself, a large part of it consists of donations. Sometimes, donations are restricted by the donor to be spent in a certain way, such as in research, athletics, or the endowment. There is still a significant portion, however, of this fund that is unrestricted. When a donation is given to the endowment, it is assumed that the institution will not spend the principal but rather any income made off it will be. Therefore, many institutions utilize a spending rate equal to the investment return from the endowment (Hansmann, 1990). 
With the restrictions imposed on many endowments in many states, it is accurate to think of an endowment as a hedge fund of sorts. The donor “buys shares” through their donation, and only the gain can be utilized (Ehrenberg, 2009). Due to the endowment being used as an investment tool for most institutions, there is a copious amount of research on the appropriate market tactics and spending rates for endowments. It can be surmised that the investment strategies often follow a robust diversification model while keeping a firm equity basis. They also tend to hold less cash on hand and, as mentioned, only spend a percentage of the total return (Goetzman, Griswold, and Tseng, 2010). Ang, Ayala, and Goetzman (2014) found that nearly ⅓ of institutions’ endowments are placed in private equity and hedge funds. Larger endowments also tend to invest more into alternative equities as they have a more experienced investment team backing them (Lord, 2014)


## The Data 

### Sources 
The variables used in this analysis were mainly those that described any institution’s various facets. There was a particular emphasis on selecting variables representative of areas where an institution spends its endowment. The institutions chosen were all private universities or colleges with endowment values above $1 billion in the FY 2019, according to NACUBO/TIAA Survey. The endowment values from each fiscal year from 2019-2010 were extracted from this survey; their 2018 Carnegie Classification was also taken from this survey. Finally, the Historically Black College or University Indicator(2019) was taken as well. 

A number of other variables from 2 other databases were taken for this analysis as well. The Council for Advancement and Support of Education manages the Voluntary Support of Education Survey, which houses data on the fundraising of U.S. colleges since the mid-1900s. From that database, data was procured on variables such as Total Alumni Giving in dollars, # of Alumni Donors, Alumni Participation(%), Alumni Support per Alumni of Record, Total Parent giving in $, Alumni Support as a % of Total Support, Full-Time # of enrolled students, Expenditures, and Largest Gift from a Living Individual. This source represented a majority of the variables in the data used for this analysis.
The values for age were procured from the U.S. News profile of each institution, and each value was for the age of the institution as of June of that year. 

The final data source is from the National Center for Education Statistics (NCES), the federal organization tasked with collecting data on U.S. education. They maintain the Integrated Postsecondary Education Data System from which a large number of variables were extracted. These variables include SAT Score, Percent admitted, Graduation rate, Average amount of federal, state, local, or institutional grant aid awarded, Percent of undergraduates awarded any financial aid, Average Tuition for Full-Time Undergraduates, and Investment Return. 

### Preliminary Analysis
Once the data was cleaned up and the necessary institutions were removed due to a lack of all significant data, there were 55 private institutions remaining. 40 of those were research institutions offered up to a Doctoral degree as signified by their Carnegie Classification of 4. 2 institutions have a Carnegie Classification of 3; they offered up to a Master’s degree. Finally, 13 colleges have a classification of 2, offering only a Baccalaureate degree.

Moreover, every single college was a non-HBCU, signifying an apparent trend that colleges with larger endowments tend not to be HBCUs. While examining the entire 2019 NACUBO/TIAA survey, one can observe that out of the 786 institutions, only 14 were HBCUs. For reference, there are currently more than 100 HBCUs in the United States (HBCU First, 2021).

Let's take a look at endowment trends over the past 10 years. From the following graph,

we can see that endowment values have been steadily rising over the past decade. From the endowments in the dataset, we find a mean of 5.6 billion dollars with a max at 40 billion dollars and a minimum of 1 billion in 2019.

There are many relevenat factors that play a large role in these institutions which may have an effect on endowment values. Let us look at the correlations of these variables with endowment values to get a proper idea of which ones have a larger impact. 

## Analysis

We'll look at a range of variables and try to narrow down which factors have the largest impact and why they are at the top.

### Age

From this graph:

This scatterplot has pretty minimal trends. There is not much reason to believe that there is any sort of relationship between the two. Logically, age’s impact could be explained through the accumulation of donations and endowment value over time. If, for example, the total amount of endowment increase is 30% greater at one institution, but the age of the other institution is twice as large, age will dictate which endowment is larger. With age, the net amount of donations increases as well since the alumni base grows each year. 
Looking at the correlation(0.554), we have confirmation that the linear relationship between the two is not very strong, so perhaps age does not play a large role here. 

### Expenditures

This graph looks a little more promising: 

More expenditures may have meant a larger negative impact, but this may not be the case. One could presume that more expenditures would cut into an endowment, decreasing its value and showing a negative correlation. This impact might be positive. This phenomenon is likely due to wealthier institutions having the resources to incur more expenditures. There are also numerous other sources that an institution can use to fund expenditures such as federal aid (minimally present at private institutions), tuition, or the sale of goods or services (Thomas, 2021). As such, expenditures may not be cutting into endowments at higher institutions but are instead indicative of an institution’s resources. 

However, the correlation only sits at about 0.57 most likely due to the wide range of data. Perhaps a different model could fit the data better. 

