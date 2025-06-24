### **Used car assessor: What drives the price of a car?**  

This notebook contains data analysis and modeling to determine which features make some cars more expensive, or others less expensive. This information will help used car dealers to make better pricing decisions for their cars. 

# **Business understanding**

Using the vehicles dataset, I did some analysis to determine which factors drive the price of a used car. I performed exploratory data analysis and built a Machine Learning model to find the key drivers of a used car's price.

# **Data Understanding**

In this section I explored the vehicles dataset to understand the following aspects:

* **Data types:** how many variables are there? What data types? Are there only numeric variables or also categorigal ones?  
* **data quality:** How many missing values are there? How many variables have a single value for all rows?
*  **Correlations:** Which variables are correlated with each other or with price?
* **Data distributions:** What is the distribution of the variables? Which of them are skewed?
* **Outliers:** Are there aany outliers in the dataset? If so, how do we handle them?

1. Used car prices are skewed, with the majority of cars priced below $40,000

2. Car prices vary by manufacturer: Ferrari, Aston-Martin and Tesla cars have median prices between $50,000 - $90,000. In contrast, Saturn and Mercury cars have median prices close to $5,000. 

3. Car prices also vary by the car's drive: 4WD cars have the highest median price vs FWD with the lowest

4. Car size also determines its price: Full-size cars are the most expensive while sub-copmact are the cheapest.

5. Car price also varies with its color: white cars have the highest price, followed by orange. Puple cars have the lowest median price.

6. There is a small but negative correlation between car price and odometer reading. This shows cars with high mileage are cheaper than those with low mileage, which stands to reason.

7. Car prices also vary by state: a few states such as Arkinsaw and Delaware have the highest median prices, while Oklahoma has the lowest median price. 

# Most important drivers of price

An ML model I built shows the two most important drivers of car prices are its model and manufacturer. A distant third, fourth and fifth are the region, state and odometer reading. Here's the list of variables ranked by their importance: 

              **Importance
model          16.882493
manufacturer   16.086451**
region          0.092990
state           0.060056
odometer        0.054873
fuel            0.033331
type            0.020044
size            0.016154
transmission    0.011845
year            0.009747
age             0.009747
drive           0.005296
cylinders       0.005142
title_status    0.003791
condition       0.002819
paint_color     0.002477

# A closer look at key drivers

Let's take a closer look at how a car's model and manufacturer impacts its price.  

1. Buick as a manufacturer has the highest positive impact on price. 

2. Beyond that, specific car models drive high prices. The most important models that drive higher prices are Mercedes Sprinter, Ford F150 Longbed, Dodge challenger srt demon, Corvette LT3 and BMW 850i. These are very expensive car models that have the highest positive coefficients in the model. Here's the top 10 features that drive higher car prices: 

onehot__manufacturer_buick            348712.782649
onehot__model_benz sprinter           122853.555401
onehot__model_f150 longbed            117984.350485
onehot__model_challenger srt demon    111676.441420
onehot__model_corvette lt3             93036.259048
onehot__model_850i                     84715.631791
onehot__model_astro cargo              82309.884167
onehot__model_210                      78309.715839
onehot__model_galaxie                  78172.576893
onehot__model_911 turbo s              76869.471489  

3. In contrast certain specific car models lead to lower prices. This includes specific Buick models e.g. Encore, Lacrosse and Regal Premium. These models have the highest negative coefficients, meaning they lead to the lowest prices.  Here's a list of the 10 highest negative features:

onehot__model_encore convenience        -366270.220476
onehot__model_regal premium             -366344.930083
onehot__model_encore essence, awd       -366919.833221
onehot__model_verano leather group      -366942.630030
onehot__model_encore essence awd        -367106.274546
onehot__model_lacrosse premium          -367219.904137
onehot__model_lacrosse cxl 4dr sedan    -368257.529876
onehot__model_encore leather            -368337.614924
onehot__model_encore gx                 -369726.715872
onehot__model_encore leather sport      -370516.814988

More details are in this Jupyter Notebook. 