
# Resposta
```sql
SELECT teacher_id, COUNT(DISTINCT subject_id) as cnt
FROM Teacher
GROUP BY 1
```
## NOTAS
Codigo muito simples, mas sem a pratica recente de sql, na primeira tentativa coloquei COUNT DISTINCT(subject_id), erro bobo se sintaxe.

