```
SELECT columnas 
FROM tabla_izquierda tz 
JOIN tabla_derecha td ON tz.columna = td.columna;
```

- Desglose
	- Primero se seleccionan las columnas principales de la [tabla_izquierda]
	- Utilizas join para llamar a la nueva tabla [tabla_derecha] 
	- [ON] para llamar la columna de la tabla principal que coincide con la tabla derecha [tabla_izquierda.columna]
	- Despues del igual [=] Se llama la columna de la tabla derecha que coincide con la de la [tabla_izquierda]
	- REDORDAR [TZ Y TD] son solamente un alias para las tablas, para poder llamarlas cuando necesites una columna, el alias lo eliges TU

```
SELECT CLIENTE
FROM CLIENTES C // **C ES EL ALIAS QUE TU LE DAS A LA TABLA**
JOIN MOVIMIENTOS MI (MI ES UN ALIAS) ON C.NRO_CLIENTE = MI.NRO_CLIENTE
```

- En este caso.
	- La columna coincidente es [NRO_CLIENTE] se encuentra en ambas tablas [MOVIMIENTOS] y [CLIENTES]