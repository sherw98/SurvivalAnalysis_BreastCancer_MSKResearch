# Survival Analysis Project at MSK 2019 Summer

This project was complted in 2019 Summer at Memorial Sloan Kettering under the guidance of Dr. Jaya Satagopan. The final presentation can be found here: https://drive.google.com/file/d/11t1bamY9APsyUwnyksTTG2D1ACbsOBDV/view?usp=sharing 

**************************************************************
Abstract
Background: The prognosis of breast cancer patients with BRCA1/BRCA2 mutations after undergoing breast conservation therapy (BCT) remains inconsistent across different studies. This study aims to analyze the roles of BRCA1/2 mutations and other factors on Ashkenazi Jewish breast cancer patients’ prognosis after they had undergone BCT. 

Method: The data used is from the published study of Robson et al. (1999). This study included 305 Ashkenazi Jewish patients with invasive breast cancer who had underwent BCT at Memorial Sloan Kettering Cancer Center (MSK). Each patient was tested for three specific types of BRCA1/2 mutations which were reported only in Ashkenazi Jewish individuals. An R Shinny app was developed to estimate the probability of surviving up to a certain time using usersupplied values of mutation status, time of diagnosis, and other potential risk factors. 

Results: Among the 305 patients, 28 (9%) were found to have at least one of the three mutations. Mutation carriers were more likely to be diagnosed with breast cancer before the age of 50 (P < 0.001) and were more likely to have at least one lymph node involvement (P = 0.04). Six outcomes were examined, namely ipsilateral recurrence, contralateral recurrence, distant recurrence, breast cancer-specific survival, disease-free survival, and overall survival. The main analysis focused on breast cancer-specific survival. Mutation carriers had lower breast cancerspecific survival probability (10-year Kaplan Meier survival probability = 62.4%) compared to non-mutation carriers (10-year Kaplan Meier survival probability = 86.4%; log-rank test P = 0.01). In a multivariate Cox proportional hazards regression model including mutation status, age of diagnosis, tumor stage, and node involvement, only tumor stage was significantly associated with breast cancer-specific survival (HR = 2.45, 95% CI = 1.23-4.87, P = 0.01). The R Shiny app for estimating breast cancer-specific survival probability is available from the author. 

Conclusions: While BRCA1/2 mutation carriers tended to have lower breast cancer-specific survival probability, mutation status was not the only factor predictive of risk. Tumor stage was a significant factor affecting the prognosis of breast cancer-specific survival among Ashkenazi Jewish breast cancer patients after they had undergone BCT.


**************************************************************
Full App

This is the full app that needs the supplement of data owned by Memorial Sloan Kettering. Therefore, by itself, it does not work. 
However, the example output is shown in the pdfs in this same folder. 

There are four tabs in the app. 

The first tab is "Summary Statistics" that allow one to look at contingency tables by different variables. The default contingency table is viewed by Mutation status. This tab also generates a bar plot by two selected variables. 

The second tab is "Kaplan-Meier Curve" that allows one to select one variable of interest and view the survival probability by different survival conditions such as death due to breast cancer, overall death, ipsilateral recurrence, and 4 other potential outcomes. The x-axis and y-axis can be modified to change the scale of the graph. The number of people at risk at each time period is shown above the x-axis. 

The third tab is "Cox Model" that allows users to customize their model and calculated the corresponded probability estimation by implementing their own risk factors. Among the 7 potential variables, users can select any variables to build a cox regression model. The "Set to Default" button allows them to clear their choices and the model goes back to the default that contains mutation status, age, tumor stage, and the number of nodes. After a cox model is formed or keeping as the default, users can then calculate survival probability after implementing the time from 0 to 200 months and their own conditions of mutation status, age, etc. The output, AIC, and survival probability plot are also shown. 

The fourth tab is "Weibull Regression Model" which has the same feature as the previous tab, just with a different model. 

*******************************************************************

App.R

This app is a simplified version of the Full App. The app is uploaded to the RShiny server: https://sherw98.shinyapps.io/SurvivalProbability/. 
In the model, the independent variables are mutation status, age, tumor stage, and number of nodes, while the dependent variable could be selected by users among the 7 potential outcomes. 
In addition to Cox and Weibull models, the log-normal model was also included.  
