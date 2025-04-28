```
SELECT
to_char(NUMRUN_CLI, '09g999g999') || '-' || DVRUN_CLI "RUN CLIENTE"
,PNOMBRE_CLI ||' '|| SNOMBRE_CLI ||' '|| APMATERNO_CLI ||' '|| APPATERNO_CLI "NOMBRE COMPLETO CLIENTE"
,TO_CHAR(FECHA_NAC_CLI,'DD/MM/YYYY') "Fecha Nacimiento"
FROM CLIENTE
WHERE to_char(FECHA_NAC_CLI,'DD/MM') = to_char((TO_DATE('&Dato')+1),'DD/MM')
ORDER BY APPATERNO_CLI;
```
---
## Ejercicio Desglosado

# 1.

```
SELECT
to_char(NUMRUN_CLI, '09g999g999') || '-' || DVRUN_CLI "RUN CLIENTE"
,PNOMBRE_CLI ||' '|| SNOMBRE_CLI ||' '|| APMATERNO_CLI ||' '|| APPATERNO_CLI "NOMBRE COMPLETO CLIENTE"
,TO_CHAR(FECHA_NAC_CLI,'DD/MM/YYYY') "Fecha Nacimiento"
FROM CLIENTE
```
---
Esta sección llama a buscar la tablas [cliente] con sus siguientes columnas.

[NUMRUN_CLI Y DVRUN_CLI] = Convierte los dos datos a [character] y los concatena también definiendo el formato del rut [09g999g999].

[PNOMBRE_CLI, SNOMBRE_CLI, APMATERNO_CLI, APPATERNO_CLI] = Concatena los nombres y apellidos completos del cliente, agregando les un espacio entre cada palabras 

[FECHA_NAC_CLI] = Se convierte la fecha a character definiendo su formato [DD/MM/YYYY]

---
# 2.

```
WHERE to_char(FECHA_NAC_CLI,'DDMM') = to_char((TO_DATE('&Dato')+1),'DDMM')
ORDER BY APPATERNO_CLI;
```

La cláusula [WHERE] se utiliza para filtrar las filas de la tabla `CLIENTE`. Dentro de esta cláusula, se realiza una comparación entre dos cadenas de texto:

 - La primera cadena se obtiene de la columna `FECHA_NAC_CLI` (fecha de nacimiento del cliente) y se convierte a formato 'DDMM' (día y mes) usando `TO_CHAR`.
 - La segunda cadena se obtiene de la fecha ingresada por el usuario (`&Dato`). Primero, esta entrada se convierte a un valor de fecha usando `TO_DATE`, luego se le suma un día, y finalmente se convierte a formato 'DDMM' usando `TO_CHAR`.

Solo las filas donde ambas cadenas 'DDMM' coinciden pasan el filtro, es decir, solo se seleccionan los clientes cuya fecha de nacimiento (día y mes) coincida con el día y mes de la fecha ingresada por el usuario más un día.

---

