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

- https://www.sqlservertutorial.net/getting-started/what-is-sql-server/
- https://learn.microsoft.com/en-us/sql/t-sql/queries/select-transact-sql?view=azuresqldb-current - Official documentation
- https://learn.microsoft.com/en-us/sql/t-sql/language-elements/transact-sql-syntax-conventions-transact-sql?view=azuresqldb-current&tabs=code


## Studies
### Tuesday, November 4, 2025

MS SQL Server uses a proprietary extension to the SQL specification called T-SQL or Transact-SQL.

We're using "Microsoft SQL Azure" for MS SQL Server. This a PAAS.

The official documentation can be found here: https://learn.microsoft.com/en-us/sql/t-sql/queries/select-transact-sql?view=azuresqldb-current
The syntax documentation can be found here: https://learn.microsoft.com/en-us/sql/t-sql/language-elements/transact-sql-syntax-conventions-transact-sql?view=azuresqldb-current&tabs=code

```sql
select * from dbo.ContactStatuses where IdContact = 50394;
DELETE FROM dbo.ContactStatuses where IdContact = 50394;
```