Retorna valores únicos, filtrando todos los valores duplicados de una columna especifica.

---
```
SELECT tools 
FROM inventory;
```

## Resultado sin DISTINCT

| tools  |
| ------ |
| Hammer |
| nails  |
| nails  |
| nails  |

---
```
SELECT DISTINCT tools 
FROM inventory;
```

## Resultado CON DISTINCT

| tools  |
| ------ |
| Hammer |
| nails  |
