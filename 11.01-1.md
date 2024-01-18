1
SELECT name, age
FROM person WHERE address= 'Novosibirsk'

![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/7213a894-f541-43ba-b715-5de8721504e4)


2
SELECT name, age
FROM person WHERE address= 'Novosibirsk' AND gender = 'female'
ORDER BY name

 ![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/c0441a35-bdb0-46dc-941a-76a13e986856)

3 
SELECT * FROM pizzeria
WHERE rating BETWEEN 3.5 AND 5
ORDER BY rating DESC

 ![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/2a4463c1-d6d4-492f-a08a-78201cda19a1)

4
SELECT DISTINCT  person_id FROM person_visits
WHERE pizzeria_id = 2 OR visit_date BETWEEN '2022-01-01' AND '2022-01-05'
ORDER BY person_id DESC
    
 ![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/9c0db71c-2ce5-4be8-90e3-ce292ce01a5c)


5
SELECT name FROM person
WHERE id IN (SELECT person_id FROM person_order
                    WHERE menu_id = 1)
 
![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/8daa0be8-1043-4678-8fbd-7f9378021c05)


6
SELECT EXISTS(SELECT name FROM person WHERE name = 'Anna')
![image](https://github.com/VikaBogomolova/vvvvvvvvvvvvvvv/assets/112609467/68c61b45-d0a1-4ebf-a16f-a94652346cd7)

