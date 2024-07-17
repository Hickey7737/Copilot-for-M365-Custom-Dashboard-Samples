# Copilot-for-M365-Custom-Dashboard-Samples
Custom Copilot for Microsoft 365 Dashboard samples for Impact and Adoption.

Raw metrics available through Viva Insights provide an opportunity to export Copilot for M365 usage metrics for custom analysis.

In addition to Copilot metrics, you can also export items like collaboration metrics to gauge impact of Copilot on day to day collaboration activities.  You can even include custom fields for line of business KPIs.

Reasons to build your own Copilot Dashboard:

* Report on Copilot usage data older than 28 days

* Report on Copilot usage with daily frequency

* View Copilot adoption and impact for custom cohorts created from a list of HR attributes including slicing Copilot usage data for small groups. E.g. Cost Center, Country, Role, etc.

* Ability to pull in business metrics or key performance indicators and utilize in your analysis.  E.g. sales performance, time to resolution, contract error rate, customer satisfaction rate, etc.

### Prerequisites:
* Copilot for Microsoft 365 licenses 
* Viva Insights License Assigned to Copilot users
* Viva Insights Analyst Role to run person query
* Power BI Pro License and Power BI Desktop
  
### Optionally:
* Viva Insights Admin Role to upload organizational attributes or KPI data
* Organization file to containing custom user attributes for slicers or KPI analysis.  See template here (https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/OrganizationalDataFileEditTemplate.xlsx)
* Viva Insights License Assigned to all tenant users or non Copilot control group to compare cohorts

What's included with this project:
   1. PBIX Power BI template sample report with Adoption and Impact pages
   2. Sample Data file with fake data from custom person query
   3. Instructions via this README

Note:  these samples are provided with no express warranty or guarantee.  The sample Copilot usage data is fabricated and generated with Excel RAND function.  The samples are not designed to be the ultimate Copilot Dashboard but merely examples to learn from.

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/video.jpg)
   
For step-by-step walkthrough on how to utilize analyst workbench for Copilot analysis, see this video - https://www.youtube.com/watch?v=QNyZxOiL6cs

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

4.	In Power BI desktop Ribbon, choose Transform data
5.	Under Query settings in the Right pane ensure the Names is "Query"
6.	Choose the Gear Icon next to Source
7.	Paste the file path from Step 11 Above | Remove "?web=1" from the path | Choose OK

  	![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/data%20source.jpg)
   
7.	If prompted for Authentication on the Access Web content screen | Choose Organizational Account | Sign in | Choose Connect
8.	Choose Close and Apply

At this point you should have the Sample Dashboard deployed with your Copilot for M365 usage data.  Please customize, fork and share your own examples in the comments.

### The Sample dashboard has two tabs:

One tab focused on Adoption:

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/adoption.jpg)

One tab focused on impact:

   ![](https://github.com/Hickey7737/Copilot-for-M365-Custom-Dashboard-Samples/blob/main/impact.jpg)

### Notes for formulas used in the sample dashboard:

#### Copilot Events are a sum of interactions with Copilot across key apps.  

In a study of knowledge workers, users were able to retrieve information across files, emails, and calendars 6 minutes faster with Copilot versus without Copilot. See study #4 in section 2 of this blog post. https://www.microsoft.com/en-us/worklab/work-trend-index/copilots-earliest-users-teach-us-about-generative-ai-at-work

CopilotEvents = SUM (Query[Copilot actions taken in Copilot chat (work)])+SUM(Query[Summarize email thread actions taken using Copilot in Outlook])+SUM(Query[Summarize Word document actions taken using Copilot in Word])+SUM(Query[Summarize presentation actions taken using Copilot in PowerPoint])+SUM(Query[Excel analysis actions taken using Copilot])+Sum(Query[Summarize chat actions taken using Copilot in Teams])+Sum(Query[Email coaching actions taken using Copilot])+SUM(Query[Generate email draft actions taken using Copilot in Outlook])+Sum(Query[Draft Word document actions taken using Copilot])+Sum(Query[Create presentation actions taken using Copilot])+SUM(Query[Rewrite text actions taken using Copilot in Word])+SUM(Query[Create Excel formula actions taken using Copilot])+SUM(Query[Excel formatting actions taken using Copilot])+SUM(Query[Compose chat message actions taken using Copilot in Teams])+Sum(Query[Summarize meeting actions taken using Copilot in Teams])

#### Copilot Assisted Hours multiplies Copilot Events by 6, divides by 60 and adds meeting hours summarized by M365 Copilot in Teams.

Copilot Assisted Hours = (Query[CopilotEvents])*6/60+SUM(Query[Meeting hours summarized by Copilot in Teams])

#### CopilotCostSavingsDollars multiplies Copilot assisted hours by a average hourly rate based on statistics from U.S. Bureau of Labor Statistic.  You can easily change this rate in the formula.  You can also upload individual employee rate information with Viva Insights organization file for more accurate results.

CopilotCostSavingsDollars = (Query[Copilot Assisted Hours]*70)
