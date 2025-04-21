**Une resultados de dos consultas `SELECT`** en una sola tabla, siempre y cuando tengan **la misma cantidad de columnas y tipos compatibles**.

```
SELECT nombre FROM clientes
UNION
SELECT nombre FROM proveedores;
```

- Une los `nombre` de ambas tablas en **una sola lista**.
- Elimina duplicados por defecto. Si quieres incluir duplicados, usas `UNION ALL`.
### Se utiliza cuando
- Quieres combinar resultados similares de dos tablas distintas.