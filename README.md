
# MechaCar_Statistical_Analysis
AutoRUs newest prototpye the MechaCar has encountered production troubles. Now the protoype production data is need of a review for any insight that can help the manufacturing team overcome the production troubles. The purpose of this analysis is to use R to design a statistical analysis to compare preformance of the MechCar vehicles against performance of vehicles from other manufacturers. 
 
## Road map for this analysis 
- Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
- Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
- Run t-tests to determine if the manufacturing lots are statistically different from the mean population
-Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers.
 
## Results 
## Linear Regression to Predict MPG
###### Prediction Overview
 
![summary(lm(mpg~vehicle_length+vehicle_weight+spoiler_angle+ground_clearance+AWD, data=MechaCar))](https://user-images.githubusercontent.com/107595578/204155111-2e9532c5-b1f8-4000-bfc8-5fc0fb3fddc4.png)
 
- The variables that provided a non-random amount of variance to the mpg values in the dataset are vehicle length and ground clearance. Vechicle length has a p-value of 2.60x10^-12 and ground clearance has a p-value of 5.21x10^-8, (Pr(>F)" column is equavialent to p-value). Since these p-values are smaller than 0.001 percent significance level, we must reject the null hypothesis.  
 
###### p-value
 
![p-value of our linear regression](https://user-images.githubusercontent.com/107595578/204155896-b67c32d8-5ed0-460b-9547-3b168d0b4fc8.png)
 
- The p-value of our linear regression model is 5.35x10^-11, which is smaller than our assumed significance level of 0.005%. Which means we must reject the null hypothesis, that means the slope of our linear model is not zero. The linear model does predicit mpg of MechaCar prototypes effectievely the Multiple R-squared value is 0.7149 with the current dataset, but will most likely fail on future predictions do to the lack of significant in the variables. Meaning that our current dataset is being overfitted. 
 
 
## Summary Statistics on Suspension Coils
###### Total Summary 
 
![total_summary](https://user-images.githubusercontent.com/107595578/204157045-a3082d77-d4b5-48cb-b007-fe49b384c9e3.png)
 
###### Lot Summary 
 
![lot_summary](https://user-images.githubusercontent.com/107595578/204157067-accb6355-b25e-4628-9404-09001b229303.png)
 
- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. While the total summary of the suspension coil's PSI is below the 100 PSI threshold set by the manufacturer with 62.29 PSI variance. When looking at the lot summary, we see that Lot #3 exceeds this threshold with having a 170.28 PSI variance. Lot #1 and Lot #2 don't exceed the 100 PSI threshold. 
 
 
## T-Tests on Suspension Coils
###### T-Test on overall lots 
 
![Overall](https://user-images.githubusercontent.com/107595578/204157552-bccdbf19-5850-4508-a0a1-a51dfb9f0636.png)
 
- After applying the T-test on suspension coils over all lot, our p-value is 0.06028. Our p-value is above our significnce level (result is significant at p < .05) , we do not have enough evidence to reject the null hypothesis. 
 
###### T-Test on Lot#1
 
![Lot1](https://user-images.githubusercontent.com/107595578/204157558-3422bcdb-f5ff-4f43-bd53-132c9d1710ec.png)
 
- After applying the T-test  on suspension on Lot #1, our p-value is 1. Our p-value is above our significnce level (result is significant at p < .05) , we do not have enough evidence to reject the null hypothesis.
 
###### T-Test on Lot#2
 
![Lot2](https://user-images.githubusercontent.com/107595578/204157561-e93779d8-402a-4628-a417-91a62b5cf20c.png)
 
- After applying the T-test  on suspension on Lot #2, our p-value is 0.6072. Our p-value is above our significnce level (result is significant at p < .05) , we do not have enough evidence to reject the null hypothesis.
 
###### T-Test on Lot#3
 
![Lot3](https://user-images.githubusercontent.com/107595578/204157564-51a2da63-88cc-409d-b588-5cc57ea12961.png)
 
- After applying the T-test on suspension on Lot #3 , our p-value is 0.04168. Our p-value is below our significnce level (result is significant at p < .05) , we have enough evidence to reject the null hypothesis. 
 
 
## Study Design: MechaCar vs Competition
In todays world owning a car isn't a necessity as it once was, there are plenty of alternatives to get around these days. For the car manufacturing industry, new car models need to have it all, realiability, low fuel cost, plus all the up todate tech. How to make MechaCar stand out amongst the rest we will need to test the fuel cost, using mpg vs the competition similar model, using a t-test to compare both models.
