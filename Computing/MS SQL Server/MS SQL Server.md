---
aliases:
cssclasses:
tags:
Related: []
Sources: []
Type: Documentation
---
# MS SQL Server

SQL Server is a relational database management system (RDBMS) developed and marketed by Microsoft.

It consists of two main components:

- Database engine - Performs queries and handles database operations
- SQLOS - SQL Server Operating System

Some tools involved are:

- SQL Server Management Studio

## Notes

The square brackets in queries is for delimiting the parts of your query:

```sql
SELECT TOP (1000) [IdUser]
      ,[IdDepartment]
      ,[FirstName]
      ,[LastName]
      ,[EmailAddress]
      ,[DefaultPage]
      ,[DefaultIdWorkflow]
      ,[IsDeleted]
      ,[DateDeleted]
      ,[DeletedBy]
      ,[DateCreated]
      ,[CreatedBy]
      ,[DateUpdated]
      ,[UpdatedBy]
      ,[PhoneNumber]
      ,[CalendlyLink]
      ,[BluerockExtension]
      ,[IdChatServUser]
      ,[IsDefaultForNotification]
  FROM [dbo].[Users]
```

The language doesn't require semicolons at the end of lines except for some special cases like:

- Before Common Table Expressions
- Before `MERGE` statements



## References

https://www.sqlservertutorial.net/getting-started/what-is-sql-server/