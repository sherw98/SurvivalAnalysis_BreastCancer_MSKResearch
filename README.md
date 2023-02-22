# Survival Analysis Project at Memorial Sloan Kettering Cancer Center (2019 Summer)

## Presentation

This project was completed in 2019 Summer at Memorial Sloan Kettering under the guidance of Dr. Jaya Satagopan. The final presentation is in *presentation.pdf*, and can also be found here: https://drive.google.com/file/d/11t1bamY9APsyUwnyksTTG2D1ACbsOBDV/view?usp=sharing 

**************************************************************
## Project Abstract

### Background: 

The prognosis of breast cancer patients with BRCA1/BRCA2 mutations after undergoing breast conservation therapy (BCT) remains inconsistent across different studies. This study aims to analyze the roles of BRCA1/2 mutations and other factors on Ashkenazi Jewish breast cancer patients’ prognosis after they had undergone BCT. 

### Method: 

The data used is from the published study of Robson et al. (1999). This study included 305 Ashkenazi Jewish patients with invasive breast cancer who had underwent BCT at Memorial Sloan Kettering Cancer Center (MSK). Each patient was tested for three specific types of BRCA1/2 mutations which were reported only in Ashkenazi Jewish individuals. An R Shinny app was developed to estimate the probability of surviving up to a certain time using usersupplied values of mutation status, time of diagnosis, and other potential risk factors. 

### Results: 

Among the 305 patients, 28 (9%) were found to have at least one of the three mutations. Mutation carriers were more likely to be diagnosed with breast cancer before the age of 50 (P < 0.001) and were more likely to have at least one lymph node involvement (P = 0.04). Six outcomes were examined, namely ipsilateral recurrence, contralateral recurrence, distant recurrence, breast cancer-specific survival, disease-free survival, and overall survival. The main analysis focused on breast cancer-specific survival. Mutation carriers had lower breast cancerspecific survival probability (10-year Kaplan Meier survival probability = 62.4%) compared to non-mutation carriers (10-year Kaplan Meier survival probability = 86.4%; log-rank test P = 0.01). In a multivariate Cox proportional hazards regression model including mutation status, age of diagnosis, tumor stage, and node involvement, only tumor stage was significantly associated with breast cancer-specific survival (HR = 2.45, 95% CI = 1.23-4.87, P = 0.01). 

The *RShiny app* for estimating breast cancer-specific survival probability is available from the author. 

The combined final results can be seen in *results.pdf*

### Conclusions: 

While BRCA1/2 mutation carriers tended to have lower breast cancer-specific survival probability, mutation status was not the only factor predictive of risk. Tumor stage was a significant factor affecting the prognosis of breast cancer-specific survival among Ashkenazi Jewish breast cancer patients after they had undergone BCT.


**************************************************************
## RShiny App

An RShiny app was built to output KM curves and interactively predict patient prognosis using different regressino models. Please see details in the RShiny_App folder. 

*******************************************************************

## Simplified RShiny App

This app is a simplified version of the Full App. It is not built on the original patient data. The app is uploaded to the RShiny server: https://sherw98.shinyapps.io/SurvivalProbability/. 
In the model, the independent variables are mutation status, age, tumor stage, and number of nodes, while the dependent variable could be selected by users among the 7 potential outcomes. 
In addition to Cox and Weibull models, the log-normal model was also included.  
