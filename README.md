# Park-Visiting-Survey-Study

Recent studies have found that since the beginning of the COVID-19 pandemic, people around the world have demanded more nature exposure to improve their mental and physical well-being. 
However, these studies didn’t examine whether this increased demand varies across different racial and socioeconomic groups. 
A rich body of literature has shown that racial minority and low-SES communities were underserved in green space resources. This phenomenon was recognized as an environmental justice issue. 
The present study implemented surveys to investigate whether racial minorities and low-SES groups visited local parks less frequently compared to Whites and high-SES groups because of a harder accessibility. 
Contrary to previous findings, the results showed that people reduced their visits to local greenspaces (i.e. parks) during the outbreak, and there was no disproportionate access to local parks across groups.
The frequency of park visits before and during the pandemic had no significant difference with respect to race, education, and income. 
The findings provided evidence that social inequalities in greenspace access have been alleviated. 
In addition, while quarantine has prevented the spread of the virus, it has also limited access to the health benefits of nature.


Data_Analysis.ipynb

The datasets were analyzed by conducting logistic regression analysis. Race (“minority” or “white”) and perceived accessibility (“yes” or “no”) were transformed into binary integer variables (0 or 1). 
The reported frequency of park visits (“Never” = 0, “Daily” =5) before and during the pandemic as well as income (“Below $10K” = 1, “Over $150K” = 5) and educational levels (“High School or Equivalent” = 1, “Doctorate” = 4) were all transformed to numerical variables using ordinal encoding to fit the regression model.
Ordinal encoding was used for these variables because each of them had a natural ordered relationship within it. 
Three regression models were built in the study. To examine whether perceived accessibility to local parks was a mediator that could explain the potential differences in the change of frequency of park visits across groups, we studied the association between race/SES and accessibility (formula='accessibility ~ race + education + income'), and the association between accessibility and change of frequency (formula='difference ~ accessibility'). 
Then, a third regression model was built to study the relationship between race/SES and change of frequency (formula='difference ~ race + education + income + accessibility').

* Robustness Test

  Because it is impossible to go back to the pre-pandemic period and observe how frequently participants visited local parks, the present study relied on self-report responses to make comparisons between the pre-pandemic and during-pandemic frequency of visits. 
  However, it is acknowledged that self-reported responses have their limitations. For instance, the accuracy of participants’ responses depends heavily on their introspective ability. 
  If the ability is compromised for reasons such as aging, it is possible for participants to give inaccurate responses. 
  To account for the uncertainties in the self-reported responses, a bootstrap method was applied to the regression models and simulated data 1000 times for each model to increase the validity of the results.
