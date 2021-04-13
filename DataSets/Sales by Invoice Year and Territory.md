# Sales by Invoice Year and Territory

## Introduction

These instructions walk you through the creation of the Sales by Invoice Year and Territory dataset.

## Build the Query

In the **Measures** area, expand **Sales**. Click on **Sales Total Including Tax** and drag it into the query area.

Expand the **Sales Invoice Date** branch.

Drag the **Year** column and drop it to the left of the Sales Total Including Tax.

Finally expand the **City** branch. Drag **Sales Territory** in between Year and Sales Total Including Tax.

Click the **Click to execute the query** link to ensure the query runs without issues.

![Sales by Invoice Year and Territory Successful Query](images/sales-by-invoice-year-and-territory-01.png)

## Save the query

Use the File menu, the pick Save.

In the **Look in** area of the dialog, make sure it is set to your report server. If not use the folder icon to the right in order to locate your server.

Name the file **Sales by Invoice Year.rsd** then click Save.

![Sales by Invoice Year and Territory Save Dialog](images/sales-by-invoice-year-and-territory-02.png)

## Conclusion

Close the Report Builder window.

Use the Refresh button on your browser to refresh the Report Portal page. You should now see your new dataset.
