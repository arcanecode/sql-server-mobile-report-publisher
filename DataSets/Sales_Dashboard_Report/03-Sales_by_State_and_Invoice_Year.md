# Sales Details

## Introduction

In this file, you'll see how to create the dataset needed for the detailed sales data grid, located on the right side of the dashboard.

![Sales Details](../images/sales-dashboard-demo-simple-data-grid.png)

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

Expand the **Measures** branch, then the **Sales** branch.

Drag the **Sales Total Including Tax** to the designer area.

Next, expand the **City** dimension, and drag the **State Province** to the designer to the left of the Sales Total Including Tax.

Finally, expand the **Sales Invoice Date** branch. Drag the **Year Label** column and drop it between the two columns already in the designer.

Click the **Click to execute the query** link to ensure the query runs without issues.

![Sales by State and Invoice Year](../images/sales-by-state-invoice-year-01.png)

## Sort Order

Now we have a minor issue. The data is not organized into any meaningful order. While the user will have the ability to change the sorting in the simple data grid, it would be nice if it came sorted already to meet the need of our user.

They have said sorting by year first, then state, makes the most sense. We can accomplish this with a little DAX magic.

In the designer, click the Design Mode button.

![](./images/../../images/employee-list-03.png)

This will switch your to the DAX editor. Don't worry if you don't know DAX, what we'll do is very simple.

By default you'll see the query that the report designer created.

```
EVALUATE SUMMARIZECOLUMNS('City'[State Province], 'Sale Invoice Date'[Year Label], "Sales Total Including Tax", [Sales Total Including Tax])
```

All we have to do is add an ORDER BY clause to the end, and list the columns to sort by.

Note we can append it to the end of the existing line, or hit ENTER and come to a new line to improve readability.

```
EVALUATE SUMMARIZECOLUMNS('City'[State Province], 'Sale Invoice Date'[Year Label], "Sales Total Including Tax", [Sales Total Including Tax]) 
ORDER BY 'Sale Invoice Date'[Year Label], 'City'[State Province]
```

You can use the execute query link, or click the big red exclamation mark, to run the new query. Once you verified it works you can save it.

## Save the query

Use the File menu, the pick Save.

In the **Look in** area of the dialog, make sure it is set to your report server. If not use the folder icon to the right in order to locate your server.

Name the file **Sales by State and Invoice Year.rsd** then click Save.

![Sales by State and Invoice Year Save as](../images/sales-by-state-invoice-year-02.png)

## Conclusion

Close the Report Builder window.

Use the Refresh button on your browser to refresh the Report Portal page. You should now see your new dataset.
