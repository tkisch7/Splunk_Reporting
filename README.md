<h1>Advanced Hunting APTs with Splunk</h1>

<h2>Description</h2>
Creating reports and dashboards is a great way to automate searches and create a user interface that displays some important information. Organizations may want to schedule searches on a schedule to reduce the load on the search head and to make searches without user interjection. Dashboards can help create visualizations to provide the end user with quick information about the data that is present. Also, dashboards can be useful when providing data to stakeholders as they can provide a great overview of the logs.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Splunk</b> 
- <b>SPL</b>
- <b>Splunk Reports</b>
- <b>Splunk Dashboards</b>

<h2>Environments Used </h2>

- <b>Linux Virtual Machine</b>

<h2>Lab Walk-through</h2>

<p align="center">
1. First, we want to understand the data that we are working with. With a quick search of all the indexes, we can see the source types available. We have three hosts; Network-server, web-server, vpn_server. : <br/>
<img src="https://imgur.com/TCtCH8x.png" height="80%" width="80%" alt="Splunk Reporting"/>
<br />
<br />
2. We want to create a report for the number of times a user logged in to the vpn network during a given time frame. For this dataset we would just use the ‘all time’ as the window since we have a small number of events.:  <br/>
<img src="https://imgur.com/umJILdL.png" height="80%" width="80%" alt="Splunk Reporting"/>
<br />
<br />
3. After creating the search we want, we can save the report by clicking “save as” and creating a title and description.: <br/>
<img src="https://imgur.com/nDEni3W.png" height="80%" width="80%" alt="Splunk Reporting"/>
<br />
<br />
4. After saving the report you can view the report by selecting view and it will take you to the report you created. You can also see your new report in the reports tab.:  <br/>
<img src="https://imgur.com/6EXeDx2.png" height="80%" width="80%" alt="Splunk Reporting"/>
 <br />
<br />
5. When looking at the reports tab you can see who created the report and the sharing access. We can see our report set to private, so if we want to change this, we can click the edit option to allow this report to be used by other users.:  <br/>
<img src="https://imgur.com/46NLEdH.png" height="80%" width="80%" alt="Splunk Reporting"/><br />
<br />
6. We can follow the previous steps and create a new report with the count of connections by port number from our network server logs. :  <br/>
<img src="https://imgur.com/rPbzOFK.png" height="80%" width="80%" alt="Splunk Reporting"/><br />
<br />
7. To create a new dashboard, we need to head over to the dashboard tab and select “Create New Dashboard”. Here we can create the title, write a description, set permissions, and select how we want to build our dashboard. Sticking with the theme of VPN users, we created a dashboard with the following settings.:  <br/>
<img src="https://imgur.com/Lyn7iWZ.png" height="80%" width="80%" alt="Splunk Reporting"/><br />
<br />
8. Creating a Dashboard prompts you to first add a panel to start the creation process. Clicking on the add panel button will bring a tab that shows the options new, new from report, clone, and add prebuilt. Since we have a report created for VPN log-ins by user, we can just use that report. We can change the view we want to a chart and make our table a visual graph.:  <br/>
<img src="https://imgur.com/23ma72V.png" height="80%" width="80%" alt="Splunk Reporting"/>
 <br />
<br />
9. Following the previous steps, we can create a new report and dashboard for  a count of web-server status codes .:  <br/>
<img src="https://imgur.com/6RFKnyk.png" height="80%" width="80%" alt="Splunk Reporting"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
