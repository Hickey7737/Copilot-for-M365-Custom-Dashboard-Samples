# Copilot-for-M365-Custom-Dashboard-Samples
Custom Copilot M365 Dashboard samples for Impact and Adoption

Raw metrics available through Viva Insights Analyst Workbench provide an opportunity to export Copilot for M365 usage data for custom dashboards or analysis.  

In addition to Copilot metrics, you can also export things like Collaborating metrics to gauge impact of Copilot on regular collaboration activities.  You can even include custom fields for line of business KPIs like sales close rate to gauge impact of Copilot on real world business indicators.


Some reasons to build your own Copilot Dashboard:

-Ability to report on Copilot usage data older than 28 days

-Ability to view adoption and impact metrics for custom cohorts created from a list of HR attributes including slicing Copilot usage data for groups smaller than 10 (min 5)

-Ability to pull in custom organizational data – for example sales performance or geography – to identify business impact correlations

-Ability to customize the definition of active Copilot users and explore usage intensity

-Include business KPIs to truly gauge impact on real world business functions.

For step-by-step walkthrough on how to utilize analyst workbench for Copilot analysis, see this video - https://www.youtube.com/watch?v=QNyZxOiL6cs

Part I - Viva Insights Analyst Workbench Custom Person Query​

1. Navigate to Viva Insights Analyst Workbench at https://analysis.insights.viva.office.com/analyst/analysis​
2. Choose Create analysis | Custom query | Person Query | Set up analysis

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/createanalysis.jpg)
   
4. Choose Time Period - Up to 1 Year.  ​
5. Optionally Auto-refresh to refresh weekly when Insights processes data (Sunday 12AM).  ​Pro Tip: If you place the results in a durable location, the PBI report will refresh automatically​
6. Choose more settings:  Group by | Daily or Weekly.  This is the frequency of metrics deliverd in the query.  Daily will give you daily usage stats and weekly stats rooled up by week.​

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/queryoptions.jpg)
   
8. Select metrics by clicking Add Metrics:  Add Microsoft 365 Copilot Metrics (required) and Collaboration activity metrics (optional) to measure Copilot impact on collaboration
9. Choose Add to query

![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/queryoptions.jpg)
    
11. Select which employees you want to include in the query.  By default, query will include all Employees Active in M365.  Add additional conditions to narrow query scope.
12. Select which employee attributes you want to include in the query.  Employee attributes come from upload of Org data file in Viva Insights.  Employee attributes can help slice custom dashboards.  E.g. I want to see Copilot Adoption and Impact for Countries, Cost Centers or any other organizational attribute
13. Choose Run Query.  Query will take approximately between 10-60 minutes









​
