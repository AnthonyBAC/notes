Permite crear diferente outputs.

```
SELECT name,
 CASE
  WHEN imdb_rating > 8 THEN 'Fantastic'
  WHEN imdb_rating > 6 THEN 'Poorly Received'
  ELSE 'Avoid at All Costs'
 END AS 'REVIEW'
FROM movies;
```

- **Desglose**
	1. Cada [WHEN] prueba una condición establecida y cada [THEN] muestra un resultado si la condición se cumple.
	2. [ELSE] entrega un resultado si ninguna de las condiciones anteriores funciona
	3. [CASE] siempre debe funcionar con un [END].
	4. En caso de que el end entregue un resultado con nombre extenso, se puede renombrar con un alias utilizando el [AS]