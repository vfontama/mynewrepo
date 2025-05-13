## Assignment 5.1: Will the Customer Accept the Coupon?

This report summarizes exploratory data analysis performed on the coupons dataset provided for this assignment. The goal was to determine which customers should be targeted with the coupons and which should not. 

# Univariate analysis
I performed univariate analysis to find coupon acceptance rates for specific variables. From this analys I found the following insights:

1. Acceptance rates vary by age: Under 21 age group has the highest acceptance rate by age, followed by age 26 and 21
![alt text](image.png) 

2. Customers accept coupons at a higher rate when the temperature is high e.g. at 80 degrees Farenheit.

3. Customers without children are more likely to accept coupons than those with kids

4. Those driving within 25 minutes of a business are actually less likely to accept coupons

5. Customers with income under $62,500 are more likely to accept the coupon. The exception is those over $100K.

6. Healthcare, Production occupations and contruction workers are more likely to accept coupons than the rest.

# Analysis of Bar visitors

1. Acceptance rates for Bar coupons is much less than overall coupon acceptance rates. Overall 56.8% of coupons were accepted. However, only 41.1% of bar coupons were accepted!

2. There is a linear relationship between frequency of bar visits and coupon acceptance rates. Those who visit bars more frequently are more likely to accept coupons.

3. Those who visited bars less frequently were LESS likely accept coupons than the rest. In fact, those who visited bars less than once or never are significantly less likely to accept coupons. We shouldn't target them.

4. There is some interaction between age and frequency of bar visits: Adults over 25 who visit bars more than once a month have much higher accptance rates than the rest!

5. Acceptance rate depends not only on the frequency of Bar visits but also on athe passenger type. Those driving with friends are most likely to accept the coupon, while those driving alone are less likely to accept it.

6. Those who visit the bar more frequently are more likely to accept the coupon, especially if their passengers are not kids and they themselves are not farmers, fishermen or forestry workers.

# Analysis of those who got coupons from cheap restaurants

1. These customers had much higher acceptance rates than overall population. Overall 56.8% of coupons were accepted. However, over 70.1% of cheap restaurant coupons were accepted!

2. Acceptance rates vry by frequency of restaurant visits: those who visit cheap restaurants are more likely to accept coupons!

3. Customers who go to cheap restaurants over 4 times a month, and whose income is less than 50k are more likely to accept coupons.

Based on this analysis we should target the following cohorts of customers with coupons:
1. Young people below 21

2. Healthcare, Production occupations and contruction workers 

3. Customers who visit bars 4 or more times a month: offer them bar vouchers

4. Customers who visit a bar more than once and who are driving with friends

7. Customers who visited the bar 3 or more times a month and are under 30


Do not target:
1. Customers who visit bars less than once a month: don't target them with bar vouchers

2. Customers who visit cheap restaurants 4 or more times a month and earn under $50K per year. 

3. Those driving with kids. 