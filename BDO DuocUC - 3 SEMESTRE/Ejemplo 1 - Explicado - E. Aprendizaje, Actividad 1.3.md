---

---
```
SELECT RE.NOMBRE_REGION
,PR.NOMBRE_PROVINCIA
,NOMBRE_COMUNA
,COUNT(C.NRO_CLIENTE) 
FROM CLIENTE C
RIGHT JOIN COMUNA CO ON CO.COD_REGION = C.COD_REGION AND CO.COD_PROVINCIA = C.COD_PROVINCIA AND C.COD_COMUNA = CO.COD_COMUNA
RIGHT JOIN REGION RE ON RE.COD_REGION = CO.COD_rEGION
RIGHT JOIN PROVINCIA PR ON PR.COD_REGION = CO.COD_rEGION AND pr.cod_provincia = co.cod_provincia
GROUP BY RE.NOMBRE_rEGION,PR.NOMBRE_PROVINCIA
,NOMBRE_COMUNA
ORDER BY 4 DESC;
```
---
## Ejercicio Desglosado

# 1.

```
SELECT RE.NOMBRE_REGION
      ,PR.NOMBRE_PROVINCIA
      ,NOMBRE_COMUNA
      ,COUNT(C.NRO_CLIENTE)
      FROM CLIENTE C
```
---

[RE.NOMBRE_REGION] = Selecciona nombre region, tabla [REGION]
[PR.NOMBRE_PROVINCIA] = Selecciona nombre provincia, tabla [PROVINCIA]
[NOMBRE_COMUNA] = Nombre comuna, tabla [COMUNA]

---


[COUNT(C.NRO_CLIENTE)] = Cuenta el numero de clientes en cada grupo,  [C.NRO_CLIENTE] hace referencia a la columna, [NRO_CLIENTE] de la tabla, [CLIENTE]

---

[FROM CLIENTE C] = Tabla principal donde se obtendrán datos, asignándole alias C

---
# 2.

```
RIGHT JOIN COMUNA CO 
  ON CO.COD_REGION = C.COD_REGION 
  AND CO.COD_PROVINCIA = C.COD_PROVINCIA 
  AND C.COD_COMUNA = CO.COD_COMUNA
```

[[RIGHT JOIN]] [COMUNA CO]  = Extrae filas de la tabla de la derecha[COMUNA CO] y filas coincidentes de la tabla izquierda.[CLIENTE C]

---

[[ON]] = Especifica la condiciona de union entre tablas, Define como deben coincidir las filas entre las dos tablas.

[[AND]] =  Agrega condiciones a la union.

---

[CO.COD_REGION = C.COD_REGION] = Columna [COD_REGION] de la tabla [COMUNA] debe coincidir con la columna [COD_REGION] de la tabla [CLIENTE]

[CO.COD_PROVINCIA = C.COD_PROVINCIA] = Columna [COD_PROVINCIA] tabla [COMUNA] debe coincidir con la columna [COD_PROVINCIA] de la tabla [CLIENTE]

[C.COD_COMUNA = CO.COD_COMUNA] = Columna [COD_COMUNA] tabla [CLIENTE] debe coincidir con columna [COD_COMUNA] tabla [COMUNA]

---
# 3.

```
RIGHT JOIN REGION RE 
  ON RE.COD_REGION = CO.COD_REGION
```

[RIGHT JOIN REGION RE] = Incluye todos los registros de la tabla de la derecha [REGION ALIAS RE] inclusive si no hay coincidencia en la tabla izquierda [COMUNA]

[ON RE.COD_REGION = CO.COD_REGION] = Union entre la columna, [COD_REGION]  tabla [REGION] y columna [COD_REGION] tabla [COMUNA].

---
# 4.

```
RIGHT JOIN PROVINCIA PR 
  ON PR.COD_REGION = CO.COD_REGION 
  AND PR.COD_PROVINCIA = CO.COD_PROVINCIA
```

[RIGHT JOIN PROVINCIA PR] = Incluye todos los registros de la tabla de la derecha [PROVINCIA ALIAS PR] inclusive si no hay coincidencia en la tabla izquierda [COMUNA].

[ON PR.COD_REGION = CO.COD_REGION AND PR.COD_PROVINCIA = CO.COD_PROVINCIA] = Union entre la columna [COD_REGION Y COD_PROVINCIA] de la tabla [PROVINCIA] Y [COD_REGION Y COD_PROVINCIA] de la tabla [COMUNA]

---
# 5.

```
GROUP BY RE.NOMBRE_rEGION, PR.NOMBRE_PROVINCIA, NOMBRE_COMUNA
```

Este agrupa los resultados, por [REGION], [PROVINCIA] y [COMUNA] 

*Esto es necesario, porque estamos utilizando [COUNT(C.NRO_CLIENTE)], [GROUP BY] asegura que los datos se dividan en grupos según las tres columnas*

---
# 6.

```
ORDER BY 4 DESC;
```

[ORDER BY] ordena los resultados según la [4] columna, siendo este el conteo de los clientes [COUNT(C.NRO_CLIENTE)].

[DESC] ordena los resultados de manera descendente.