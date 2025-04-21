Combina todas las filas de una con todas las de otra tabla

```
SELECT *
FROM colores
CROSS JOIN tallas;
```

Si `colores` tiene 3 filas y `tallas` tiene 4, el resultado tendrá **3 × 4 = 12 filas**.
### Se utiliza **cuando**************
- Necesitas generar **todas las combinaciones posibles** entre dos conjuntos de datos.
- Por ejemplo, generar todas las combinaciones de productos con tamaños y colores.