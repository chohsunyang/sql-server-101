## DATEADD Function

### What does this do?

The DATEADD() function adds a time/date interval to a date and then returns the date.

```sql
DATEADD(interval, number, date)
```

### Senario #1

At the begining of each month, you need to run a report that captures the sales figure for last month. But you need to exclude that data for this month.

```sql
SELECT YEAR(DATEADD(month, - 1, GETDATE())) - 1
SELECT YEAR(DATEADD(month, - 1, GETDATE())) 
SELECT DATEADD(month, - 1, GETDATE())
SELECT DATEADD(month, 0, GETDATE())
SELECT GETDATE()
```

| Output                  |
|-------------------------|
| 2021                    |
| 2022                    |
| 2022-10-09 22:13:58.510 |
| 2022-11-09 22:13:58.510 |
| 2022-11-09 22:13:58.510 |
