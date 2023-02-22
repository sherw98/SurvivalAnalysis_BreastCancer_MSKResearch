This folder contains the complete RShiny app built to visualize and calculate patient prognosis. 

This full app needs the supplement of data owned by Memorial Sloan Kettering. Therefore, by itself, it does not work. However, the example output is shown in the pdfs in this same folder.

There are four tabs in the app.

The first tab is "Summary Statistics" that allow one to look at contingency tables by different variables. The default contingency table is viewed by Mutation status. This tab also generates a bar plot by two selected variables.

The second tab is "Kaplan-Meier Curve" that allows one to select one variable of interest and view the survival probability by different survival conditions such as death due to breast cancer, overall death, ipsilateral recurrence, and 4 other potential outcomes. The x-axis and y-axis can be modified to change the scale of the graph. The number of people at risk at each time period is shown above the x-axis.

The third tab is "Cox Model" that allows users to customize their model and calculated the corresponded probability estimation by implementing their own risk factors. Among the 7 potential variables, users can select any variables to build a cox regression model. The "Set to Default" button allows them to clear their choices and the model goes back to the default that contains mutation status, age, tumor stage, and the number of nodes. After a cox model is formed or keeping as the default, users can then calculate survival probability after implementing the time from 0 to 200 months and their own conditions of mutation status, age, etc. The output, AIC, and survival probability plot are also shown.

The fourth tab is "Weibull Regression Model" which has the same feature as the previous tab, just with a different model.

