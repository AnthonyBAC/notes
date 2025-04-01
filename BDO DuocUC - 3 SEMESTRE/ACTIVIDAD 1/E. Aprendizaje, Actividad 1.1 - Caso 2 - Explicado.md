```
SELECT
NUMRUN_EMP || ' ' || DVRUN_EMP "RUN EMPLEADO"
,PNOMBRE_EMP || ' ' || SNOMBRE_EMP || ' ' || APPATERNO_EMP || ' ' || APMATERNO_EMP "NOMBRE COMPLETO EMPLEADO"
,SUELDO_BASE || '$'
,TRUNC(SUELDO_BASE/100000) AS "PORCENTAJE MOVILIZACION"
,ROUND(SUELDO_BASE * (TRUNC(SUELDO_BASE/100000) * 0.01),0) AS "VALOR_MOVILIZACION"
FROM EMPLEADO
ORDER BY 4 DESC;
```
---
## Ejercicio Desglosado

# 1.

```
SELECT
NUMRUN_EMP || ' ' || DVRUN_EMP "RUN EMPLEADO"
,PNOMBRE_EMP || ' ' || SNOMBRE_EMP || ' ' || APPATERNO_EMP || ' ' || APMATERNO_EMP "NOMBRE COMPLETO EMPLEADO"
,SUELDO_BASE || '$'
,TRUNC(SUELDO_BASE/100000) AS "PORCENTAJE MOVILIZACION"
,ROUND(SUELDO_BASE * (TRUNC(SUELDO_BASE/100000) * 0.01),0) AS "VALOR_MOVILIZACION"
FROM EMPLEADO
```
---
### Primera sección, llama a buscar columnas de la tabla [EMPLEADO]:

 1. **[NUMRUN_EMP Y DVRUN_EMP]** 
	 - Se concatenan con un espacio entre ellas.
	 
2. **[PNOMBRE_EMP, SNOMBRE_EMP, APPATERNO_EMP, APMATERNO]**  
	- Concatenacion de nombres y apellidos completos del empleado.
	
3. **[SUELDO_BASE]**
	- Se concatena junto al char de dinero [$].
	
4. **[COLUMNA 4]**
	- Se utiliza [TRUNC] para quitar decimal al resultado de [SUELDO_BASE/100000] , esto se utiliza para entregar un 1% por cada 100mil de sueldo,  se utilza [AS] para dar un nombre a la columna.
	
5. [COLUMNA 5] = **Paso a Paso**

	1. **"Primero se hace el mismo procedimiento de la columna 4"**:
    
    - Esto se refiere a que se toma el valor del `SUELDO_BASE` y se divide por 100,000.
    - Este resultado nos indica cuántos bloques de 100,000 unidades monetarias contiene el sueldo base.
    
	2. **"utilizando TRUNC para quitar el decimal al resultado"**:
    
    - La función `TRUNC` se aplica al resultado de la división anterior.
    - `TRUNC` elimina cualquier parte decimal del resultado, dejando solo la parte entera.
    - Esto es importante porque solo queremos contar los bloques completos de 100,000.
    
	3. **"Se multiplica por 0.01 para sacar el porcentaje"**:
    
    - El resultado de `TRUNC` se multiplica por 0.01.
    - 0.01 representa el 1%. Por lo tanto, esta multiplicación calcula el porcentaje del sueldo base que se debe aumentar.
    
	4. **"Luego poder multiplicarlo nuevamente por el [SUELDO_BASE]"**:
    
    - El porcentaje calculado en el paso anterior se multiplica por el `SUELDO_BASE`.
    - Esto calcula el valor del aumento en unidades monetarias.
    
	5. **"Se utiliza función [ROUND] para redondear el resultado"**:
    
    - La función `ROUND` se aplica al resultado de la multiplicación anterior.
    - `ROUND` redondea el resultado al entero más cercano, eliminando cualquier decimal.
    
	6. **"también se utiliza [AS] para entregar un alias a la columna"**:
    
    - La palabra clave `AS` se utiliza para asignar un nombre (alias) a la columna resultante.
    - Esto hace que el resultado de la consulta sea más fácil de leer y entender.

---
# 2.

```
ORDER BY 4 DESC;
```

1. **`ORDER BY`**:
    - Esta cláusula se utiliza en SQL para ordenar los resultados de una consulta `SELECT`.
    - Indica que queremos organizar las filas devueltas por la consulta.
    
2. **`4`**:
    - Este número hace referencia a la cuarta columna en el conjunto de resultados de la consulta `SELECT`.
    - En lugar de especificar el nombre de una columna, estamos utilizando su posición numérica.
    - Es importante tener en cuenta que el conteo de las columnas comienza desde 1.
    
3. **`DESC`**:
    - Esta palabra clave indica que queremos ordenar los resultados en orden descendente.
    - Esto significa que los valores más altos aparecerán primero, seguidos de los valores más bajos.
    - Si omitiéramos `DESC`, los resultados se ordenarían en orden ascendente (de menor a mayor) de forma predeterminada.
    
---


