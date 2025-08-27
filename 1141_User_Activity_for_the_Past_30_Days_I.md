
# Resposta
```sql
SELECT DISTINCT 
    activity_date AS day,
    COUNT(DISTINCT user_id) AS active_users
FROM Activity
WHERE activity_date BETWEEN '2019-07-27'::date - INTERVAL '29' day and '2019-07-27'::date
GROUP BY 1
```
## NOTAS
A logica eu soube pensar, só não sabia como funcionava direito os tipos de data, usando interval e a keyword DAY, deu certo.


**27-08-25**