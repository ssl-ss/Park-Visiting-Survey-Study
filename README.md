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




References:

1. Ugolini, F., Massetti, L., Calaza-Martínez, P., Cariñanos, P., Dobbs, C., Ostoic, S. K., Marin, A. M., Pearlmutter, D., Saaroni, H., Šaulienė, I., Simoneti, M., Verlič, A., Vuletić, D., & Sanesi, G. (2020). Effects of the COVID-19 pandemic on the use and perceptions of urban green space: An international exploratory study. Urban forestry & urban greening, 56, 126888. https://doi.org/10.1016/j.ufug.2020.126888
2.Pouso, S., Borja, Á., Fleming, L. E., Gómez-Baggethun, E., White, M. P., & Uyarra, M. C. (2021). Contact with blue-green spaces during the COVID-19 pandemic lockdown beneficial for mental health. The Science of the total environment, 756, 143984. https://doi.org/10.1016/j.scitotenv.2020.143984
3. Soga, M., Evans, M. J., Tsuchiya, K., and Fukano, Y.. (2021). A room with a green view: the importance of nearby nature for mental health during the COVID‐19 pandemic. Ecological Applications 31( 2):e02248. 10.1002/eap.2248
4. Poortinga, W., Bird, N., Hallingberg, B., Phillips, R., & Williams, D. (2021). The role of perceived public and private green space in subjective health and wellbeing during and after the first peak of the COVID-19 outbreak. Landscape and Urban Planning, 211, 104092. https://doi.org/10.1016/j.landurbplan.2021.104092
5. Grima, Nelson & Corcoran, Will & Hill-James, Corinne & Langton, Benjamin & Sommer, Haley & Fisher, Brendan. (2020). The importance of urban natural areas and urban ecosystem services during the COVID-19 pandemic. 27. Wen, M., Zhang, X., Harris, C. D., Holt, J. B., & Croft, J. B. (2013). Spatial Disparities in the Distribution of Parks and Green Spaces in the USA. Annals of Behavioral Medicine, 45(S1), 18–27. https://doi.org/10.1007/s12160-012-9426-x
6. Dai, D. (2011). Racial/ethnic and socioeconomic disparities in urban green space accessibility: Where to intervene? Landscape and Urban Planning, 102(4), 234–244. https://doi.org/10.1016/j.landurbplan.2011.05.002
7. Martin, C. A., Warren, P. S., & Kinzig, A. P. (2004). Neighborhood socioeconomic status is a useful predictor of perennial landscape vegetation in residential neighborhoods and embedded small parks of Phoenix, AZ. Landscape and Urban Planning, 69(4), 355–368. https://doi.org/10.1016/j.landurbplan.2003.10.034
