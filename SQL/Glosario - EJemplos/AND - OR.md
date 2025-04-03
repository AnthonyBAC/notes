1. **AND**
	- Muestra la linea si todas las condiciones son true
---
2. **OR**
	- Muestra la linea si cualquiera de las dos condiciones es true
---
```
SELECT *
FROM movies
WHERE year > 2014 -- primer condicion
   OR genre = 'action'; -- segunda condicion
```

Con [OR] cualquier de las dos condiciones si es correcta, entregara un resultado.