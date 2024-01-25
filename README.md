## Task - 1

```sql
SELECT name, id FROM pizzeria
WHERE NOT EXISTS(SELECT * FROM person_visits 
WHERE id=pizzeria.id)
```
![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/efdf5df1-a6c1-42eb-8941-9c43549b79cf)
