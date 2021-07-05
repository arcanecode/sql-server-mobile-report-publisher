# Demo Files

## What's Here

This folder contains copies of all the demo files used in this course.

The RSD files are the datasets. The RDL is the paginated report that is used in the drillthrough example.

The RSMOBILE files are the dashboards themselves. The two that end in demo are the ones I created to show the finished results. The other two are the ones that were generated during the course.

The WWI-SSAS-Tabular.abf file is the backup of the SSAS Tabular database.

## How To Use

First, you need to create a _Data Source_ that the datasets will need.

Go to the Report Portal, and use the New menu. Pick Data Source. Name the data source **WWI Tabular**.

For the connection type, pick **Microsoft SQL Server Analysis Services**.

For the connection string, you can use something like:

```
Data Source=localhost;Initial Catalog=WWI-SSAS-Tabular
```

This assumes you are using a development box where everything is running on. Otherwise use the name of your server instead of localhost.

Now you can use the Upload menu in the Report Portal to upload all of the sample files. Assuming you have restored the WWI-SSAS-Tabular.abf file to your SSAS Server, you should be able to run your reports.

---

## Author Information

### Author

Robert C. Cain | [@ArcaneCode](https://twitter.com/arcanecode) | arcanecode@gmail.com

### Websites

About Me: [http://arcanecode.me](http://arcanecode.me)

Blog: [http://arcanecode.com](http://arcanecode.com)

Github: [http://arcanerepo.com](http://arcanerepo.com)

LinkedIn: [http://arcanecode.in](http://arcanecode.in)

### Copyright Notice

This document is Copyright (c) 2021 Robert C. Cain. All rights reserved.

The code samples herein is for demonstration purposes. No warranty or guarantee is implied or expressly granted.

This document may not be reproduced in whole or in part without the express written consent of the author and/or Pluralsight. Information within can be used within your own projects.
