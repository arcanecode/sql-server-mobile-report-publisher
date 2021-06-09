# State Employee Sales Data

## Introduction

These instructions walk you through the creation of the State Employee Sales dataset. The dataset is used to populate all of the controls on the report, except for the Employee and State list.

![State Employee Sales Dashboard](./../images/sales-by-state-employee-dashboard-demo.png)

## Launch the Dataset Designer

In the SQL Server Reporting Services Portal, click the New menu, then Dataset.

Your browser might prompt you that it is trying to open Microsoft Report Builder. If so click Open or OK.

You may be prompted that the report requires a connection to the report server, and warns you the connection may not be secure. This is typically the case when you have SQL Server installed on your local development box, and you can safely click Yes.

If you are in a corporate environment, you should check with your system administrator first.

The Report Builder now appears, with the dialog asking you to select a dataset. If you've run Report Builder before, the WWI Tabular dataset may already appear in the list. if so, you can click it then click Create.

If not, click on the _Browse other data sources_ link. The _Look in_ bar should default to the server you launched Report Builder from, for example _http://acdev2/ReportServer_. If not you can use the icon to the right of the _Look in_ bar to navigate to a server.

The dataset should appear in the list. If you are following the suggestions in these documents it would be named _WWI Tabular_. Click on it, then click _Open_.

It should now appear in the initial dialog. Now you can click _Create_.

You are now ready to build the query.

## Build the Query

Expand the **Measures** branch, then expand **Sales**. Click on **Sales Total Including Tax** and drag it into the query area.

Expand the **City** dimension, then drag the **State Province** onto the query designer.

Go to the **Employee** dimension, then drag its **Employee** attribute onto the designer.

Next, expand the **Sales Invoice Date**. Drag the following fields onto the query designer.

* Year
* Beginning of Quarter Label Short
* Beginning of Month Label Short
* Sales Total Including Tax
* Beginning of Month

Click the **Click to execute the query** link to ensure the query runs without issues.

![State Employee Sales Dialog](../images/state_employee_sales_01.png)

## Save the query

Use the File menu, the pick Save.

In the **Look in** area of the dialog, make sure it is set to your report server. If not use the folder icon to the right in order to locate your server.

Name the file **State Employee Sales.rsd** then click Save.

![State Employee Sales Save Dialog](../images/state_employee_sales_02.png)

## Conclusion

Close the Report Builder window.

Use the Refresh button on your browser to refresh the Report Portal page. You should now see your new dataset.
