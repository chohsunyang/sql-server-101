## DATEADD Function

### What does this do?

The DATEADD() function adds a time/date interval to a date and then returns the date.

```sql
DATEADD(interval, number, date)
```

### Senario #1 Know the interval

When you run into certian cases, be careful of what interval you are using.
For example, 1 month and 30 days are two very different concepts. 


```sql
SELECT DATEADD(month, 1, '2022/01/30')
SELECT DATEADD(day, 30, '2022/01/30')
```

| Output                  |
|-------------------------|
| 2022-02-28 00:00:00.000 |
| 2022-03-01 00:00:00.000 |

### Senario #2 Last month
