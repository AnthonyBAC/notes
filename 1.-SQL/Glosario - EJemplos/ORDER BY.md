Util para mostrar una lista de datos en el orden que nosotros queramos.

```
SELECT *
FROM movies
ORDER BY name;
```

[ORDER BY] es la clausula que indica que debe ordenar el resultado dependiendo de una columna elegida en este caso la columna [name]

---
1. **También se puede ordenar de manera descendente.**
	```
	SELECT *
	FROM movies
	WHERE imdb_rating > 8
	ORDER BY year DESC;
	```
	
[DESC] se ocupara ordenar las cosas de manera descendente.
[ASC] se ocupara para ordenar las cosas de manera ascendente.