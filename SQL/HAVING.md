Se utiliza para filtrar resultados después de agrupar, es decir se aplica sobre los grupos creados por [[GROUP BY]], se usa con funciones de agregación.

---

```
SELECT producto, SUM(cantidad) AS total_vendido
FROM ventas
GROUP BY producto
HAVING SUM(cantidad) > 10;
```

En este caso se buscan los productos que vendieron mas de 10 unidades. 

> Si se ocupara [WHERE] en este caso, buscaría por filas individuales cual es el que tiene una cantidad vendida mayor a 10, pero no es lo que queremos