----1---
SELECT t1.id 
FROM (
(SELECT m1.from_user_id id
COUNT (m1.to_user_id)
FROM messages m1
JOIN users u1 ON
m1.to_user_id=u1."id"
WHERE u1.id=1 
 GROUP BY m1.from_user_id
ORDER BY 2 DESC 
LIMIT 1) 
UNION ALL
(SELECT m1.to_user_id id
COUNT (m1.from_user_id)
FROM messages m1
JOIN users u1 ON
m1.from_user_id=u1."id"
WHERE u1.id=1
 GROUP BY m1.to_user_id
 ORDER BY 2 DESC 
LIMIT 1)
ORDER BY 2 DESC
LIMIT 1
) t1
;

---2---
