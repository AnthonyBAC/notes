Valores desconocidos de datos.
- No se pueden verificar datos NULL con los operadores comunes como '=' o '!='
- Se puede utilizar IS NULL o IS NOT NULL

---
```
SELECT name
FROM movies 
WHERE imdb_rating IS NOT NULL;
```

Buscando nombres de la tabla movies que contengan imdb_rating, osea que no tenga datos null.

---
```
SELECT name
FROM movies 
WHERE imdb_rating IS NULL;
```

Buscando nombres de la tabla movies que NO contengan [imdb_rating], osea que los datos de [imdb_rating] sean nulos.