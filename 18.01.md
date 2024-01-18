## Task - 1

```sql
SELECT * FROM person, pizzeria
ORDER BY person.id, pizzeria.id;
```
![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/86264c9b-3b80-430a-86db-315164eb87ea)

## Task - 2

```sql

SELECT action_date, p.name FROM
(
	SELECT order_date AS action_date, person_id FROM person_order
	INTERSECT ALL
	SELECT visit_date,person_id FROM person_visits
) as tab
JOIN person p ON tab.person_id = p.id
```
![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/f99a4ca5-b847-412b-ba0b-e6b00eb1dbc9)
