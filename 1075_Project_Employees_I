
# Resposta
```sql
SELECT DISTINCT 
    activity_date AS day,
    COUNT(DISTINCT user_id) AS active_users
FROM Activity
WHERE activity_date BETWEEN '2019-07-27'::date - INTERVAL '29' day and '2019-07-27'::date
GROUP BY 1
```

**30-08-25**