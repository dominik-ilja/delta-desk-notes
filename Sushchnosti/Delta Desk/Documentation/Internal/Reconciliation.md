---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# Reconciliation

There are multiple clients that we perform reconciliation for:

- Carrick Lane
- Visdom

We'll separate the reconciliation processes for both of these clients. There's two pieces of software that we'll need:

- **SQL Server Management Studio** - Used to connect to the database
- **Remote Desktop Connection** - Used to connect to the virtual machine

## Carrick Lane

1. Connect to database through **SQL Server Management Studio**. The URI is "[carricklane.database.windows.net](http://carricklane.database.windows.net)". The credentials are kept within 1Password.
2. Right click on `Databases > CarrickLane` and select "New Query". Luke recommends running the following query to see if there are trades. Luke also told me that Josh recommends highlighting the section that we wish to query:

```sql
Select *
FROM ClientTrade
WHERE DateTrade = '2025-09-11'
```

1. Connect to the virtual machine through the **Remote Desktop Connection** application. The computer name is "[vpc.absoftwareventures.com](http://vpc.absoftwareventures.com)". You'll need to have credentials from 1Password as well.
2. In the virtual machine, we'll need to go to the "Schwab Data Delivery" application. We cannot directly retrieve files from Schwab with FTP. This is the reason for the application. In the application, you'll press the green "Download all new files" button. This will transfer the files through FTP. This button can be pressed as many times as you want. If the files were already pulled, then it'll give you a popup of something like "No files to download" or something similar. This allows the jobs that run in the morning to operate on the files.
3. Once the files are uploaded, we can then query the database and prepare the results to be sent. - I don't think this is the correct order.

> SQL Scripts are stored at C:\Users\DominikKulak\Documents\SQL Server Management Studio 21

In the morning, are the "Import" lines are run, and at night the "Send" lines are run.

## Visdom

_We're currently undergoing some changes on how the process for Visdom works._

The reconciliation process for Visdom looks a little different from Carrick Lane. We essentially only do the first half of the process. We'll transfer the files through FTP with the "Schwab Data Delivery" application. The "Schwab Data Delivery" app can only be used for a single client. - FACT CHECK THIS. Currently, Luke has the app on his local computer. Josh is wanting to convert this to run on a virtual machine. After pulling the files, a script is run (what is this script) that uploads the data into Visdom's database. Once this is done, our job is complete.

## Miscellaneous

- Carrick Lane currently has around 699 clients.
- Luke has reported that at times the query against FIDO can be slow. Taking upwards to 30 minutes.
- LINQPad #Question

At what point am I hitting this button - Andrew

- What is a strike? #Question
- What is a roll? #Question
- What is a strategy? - I see "XDP" #Question
- What is a client? - I see "XDPPRGU6" which is probably just an ID #Question
- ESMX Destination - What does ESMX stand for? #Question
- What is allocation? #Question
- What is a position? #Question
- What is an option? #Question
- What is a trade ticket? #Question 