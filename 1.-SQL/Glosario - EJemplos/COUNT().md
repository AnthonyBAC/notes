Función que toma como argumento el nombre de una columna y cuenta los valores de las lineas non-empty de la columna indicada.

---
```
SELECT COUNT(*)
FROM fake_apps
WHERE price = 0
```

En este ejemplo, estamos contando la cantidad de fake_apps que hay, luego agregándole una clausula [[WHERE]] se comienzan a contar todas las apps que tienen un valor de 0.
