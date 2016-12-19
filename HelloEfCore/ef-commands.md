# DotNet EF Commands

Reference: https://docs.microsoft.com/en-us/ef/core/miscellaneous/cli/dotnet

## Scaffold DbContext from Existing Database

- Using SQL Express and SQL Server Management Studio
- Create NorthwindSlim database
- Download http://bit.ly/NorthwindSlim
- Run sql script to create database objects and data

```
dotnet ef dbcontext scaffold "Server=(local)\sqlexpress;Database=NorthwindSlim;Trusted_Connection=True;" Microsoft.EntityFrameworkCore.SqlServer -o Models -f
```
 