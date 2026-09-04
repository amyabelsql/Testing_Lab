# Running SQL Tests

## Prerequisites

- Access to a SQL Server instance
- A test database
- A SQL execution tool such as `sqlcmd`, SQL Server Management Studio, or Azure Data Studio

## Basic workflow

1. Run any required setup scripts from `sql/setup/`.
2. Run the target validation scripts from `sql/tests/`.
3. Compare the output with the expected result for the test case.
4. Record findings, edge cases, and follow-up actions in the wiki.

## Example

```bash
sqlcmd -S <server> -d <database> -i sql/setup/<script>.sql
sqlcmd -S <server> -d <database> -i sql/tests/<script>.sql
```
