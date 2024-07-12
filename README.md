# Copilot-for-M365-Custom-Dashboard-Samples
Custom Copilot for Microsoft 365 Dashboard samples for Impact and Adoption.

Raw metrics available through Viva Insights provide an opportunity to export Copilot for M365 usage data for custom dashboards or analysis.

In addition to Copilot metrics, you can also export things like collaboration metrics to gauge impact of Copilot on regular collaboration activities.  You can even include custom fields for line of business KPIs like sales close rate to gauge impact of Copilot on real world business indicators.

Reasons you may want to build your own Copilot Dashboard:

-Report on Copilot usage data older than 28 days

-View adoption and impact metrics for custom cohorts created from a list of HR attributes including slicing Copilot usage data for groups smaller than 10 (min 5). E.g Cost Center, Country, Role, etc.

-Ability to pull in organizational Key Performance Indicators.  E.g. sales performance, time to resolution, contract error rate, customer satisfaction rate, etc.

-Ability to customize the definition of active Copilot users and explore usage intensity

For step-by-step walkthrough on how to utilize analyst workbench for Copilot analysis, see this video - https://www.youtube.com/watch?v=QNyZxOiL6cs

Note:  these samples are provided with no express warranty or guarantee.  The sample Copilot usage data is fabricated and generated with Excel RAND function.

## Step I - Viva Insights Analyst Workbench Custom Person Query 

1. Navigate to Viva Insights Analyst Workbench at https://analysis.insights.viva.office.com/analyst/analysis
2. Choose Create analysis | Custom query | Person Query | Set up analysis

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/createanalysis.jpg)
   
3. Choose Time Period.  Viva Insights stores up to 13 months of Copilot and collaboration data.  
4. Optionally choose Auto-refresh to refresh weekly when Viva Insights processes data (Sundays at 12AM).  Pro Tip: If you place the results in a durable location, the Power BI report can refresh automatically
5. Choose more settings:  Group by | Daily or Weekly.  This is the frequency of metrics delivered in the query.  Daily will give you daily usage stats and weekly nets you stats rolled up by week.

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/queryoptions.jpg)
   
6. Select metrics by clicking Add Metrics:  Add Microsoft 365 Copilot Metrics (required) and Collaboration activity metrics (optional) to measure Copilot impact on collaboration
7. Choose Add to query

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/select%20metrics.jpg)
    
8. Select which employees you want to include in the query.  By default, queries will include all Employees Active in M365.  Add additional conditions to narrow query scope.

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/select%20emps.jpg)

9. Select which employee attributes you want to include in the query.  Employee attributes come from uploading of Org data file in Viva Insights.  Employee attributes can help analysis or to slice your custom dashboards.  E.g. I want to see Copilot Adoption and Impact for Countries, Cost Centers or I want to see the impact of close rates for Sales professionals enabled with Copilot.

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/emp%20attribs.jpg)

10. Choose Run Query.  Query will take approximately between 10-60 minutes
11. Save the output CSV file to a durable location on SharePoint or OneDrive.  Take note of the path: In Excel | Choose File | Info | Copy Path 

## Part II - Download Power BI Template and connect to data file generated in Step I

1. Download Custom Copilot Dashboard Examples.pbix and open in Power BI Desktop App.  https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/Custom%20Copilot%20Dashboard%20Examples.pbix
2. Note: You will get a notice that "There are pending changes in your queries that haven't been applied".  Choose X to close this message and play with the sample data.

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/Apply%20changes.jpg)

3.	In Power BI desktop Ribbon, choose Transform data
4.	Under Query settings in the Right pane ensure the Names is "Query"
5.	Choose the Gear Icon next to Source
6.	Paste the file path from Step 11 Above | Remove "?web=1" from the path | Choose OK

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/data%20source.jpg)
   
7.	If prompted for Authentication on the Access Web content screen | Choose Organizational Account | Sign in | Choose Connect
8.	Choose Close and Apply







​
