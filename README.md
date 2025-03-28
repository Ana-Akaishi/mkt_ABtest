![cover](https://images.pexels.com/photos/2119758/pexels-photo-2119758.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2)

# Marketing Campaign A/B Testing
For this project, I'll analyse marketing campaign effectiveness with **A/B Testing**. This is an statistical approach to analyze if there's difference after applying the treatment, or in this case, after marketing promotions.

I'll use the [public database](https://www.kaggle.com/datasets/chebotinaa/fast-food-marketing-campaign-ab-test) available on Kaggle. Here, I'll test 3 different promotions on a fast food restaurant. Let's assume the dataset is a pilot, and the marketing team wants the DS to analyze which campaign was effective and they should invest.

Since this project don't have business problem or case to solve, I'm gonna run the usual exploratory data analysis (EDA) to understand the company and then focus in avarage ticker/[avarage order value (AOV)](https://businessplan-templates.com/blogs/metrics/fast-food). For the fast food industry, AOV is one of the most importante KPIs, since the main idea of the business is to sell as many units as possible and dilute their costs.

## Dataset
Usually, A/B tests are made between a control group and the treatment (A and B). But for this case, marketing ran 3 promotions at the same time, and wants to know which one is better. So instead of comparing performaces with business as usual, I'll be comparing 3 treatments.
- **Since I don't have the control group/benchmark to compare other promotions, I'm choosing to use PROMOTION 2 as my benchmark**

The dataset isn't big, so I'll approach it as a the final sample. I won't need to run the ideal sample size for this project.

Before running any statistical test, it's important to **check for normality**. This will guide me towards which statistical test run.

## Project Steps
First, I'll analyze the dataset and how the variables behave around each promotion. After that, I'll run the AB Test and provide the results.

00_EDA

01_AB_Test

## EDA Summary

This fast food company has 137 stores, devided between Small (15), Medium (80) and Large (42) stores. The company has been in the market for 28 years, and just opened some big stores (76 new units) that are the top sellers in the network ($4,464 thousand). Marketing team ran a promotion/campaign across the stores, and measures week over week.

Promotion 1 has the lowest volume of sales (43 WoW), but delivered the best financial performance (avg $57 thousands). It means customers bought morte items per transaction, this result happened mainly in medium and large units.

Promotion 2 has a good volume of sales (47 WoW), same as Promotion 3, but had the lowest avarage revenue ($47 thousands). This could be interpretated as customers buying cheap items from the menu. 
- Since I'm treating PROMOTION 2 as my **benchmark**, this is in line with the expected fast food client behavior (looking for quick as cheaper meals)
- If PROMOTION 2 was a real marketing strategy, I would suggest to for more data on customer demoghraphics and location to stablish a profile. This way marketing team could be develop targeted promotions to increase our target KPI

Promotion 3 performed well in sales volume (47 WoW) and financial performance ($55 thousands).

Also, when analyzed stores size, large and medium unites tend to perform better in terms of sale and revenue. It would be interesting if we had the cost of each unit to see if it's worth to keep **small stores** or not.

## A/B Test Summary
In this project, I ran an A/B Test to evaluate the effectiveness of 3 marketing campaigns for a fast food company. Based on the statistical analysis, promotion 1 and 2 are statistical different from each other. Promotion 3 on the other hand, is  different from promotion 2 but similar to promotio 1.

Insights BASED ONLY ON THE AVAILABLE INFORMATION:
- Based on EDA analysis, the company should chose to move with Promotions 1 OR 3, depending on **the KEY METRIC THE COMPANY VALUES**:
    - Chose Promotion 1 if **our target KPI is increse the AOV**. Promotion 1 increases the AOV by 2.75% ($10.77)
    - Chose Promotion 3 if **our target KPI is increase Total revenue**. Promotion 3 increases TOTAL REVENUE by 12.33% ($1,510.59)
- My recommendation is to move with Promotion 1, despite the lower volume in sales, Promotion 1 has the highest avarage revenue
- Drop promotion 2, despite have a higher sales volume, it has the lowest revenue