
# Resposta
```sql
SELECT p.product_id, 
    COALESCE(ROUND((SUM(p.price*units::numeric)/SUM(u.units)),2),0) AS average_price
FROM Prices p LEFT JOIN UnitsSold u on p.product_id = u.product_id 
AND u.purchase_date BETWEEN p.start_date AND p.end_date 
GROUP BY p.product_id
```
## NOTAS
Coalesce para checar se o valor é nulo e trocar por 0.  

NUMERIC para informar que é decimal  

AND no JOIN para filtrar as datas corretamente (antes eu estava fazendo com where, acontecia depois do join e isso ocasionava em erro)


**26-08-25**