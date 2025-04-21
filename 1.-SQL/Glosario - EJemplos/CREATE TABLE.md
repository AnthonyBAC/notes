Definir estructura de una nueva tabla dentro de una base de datos.

- Permite especificar el nombre de la tabla y las columnas que contendrá.
- Define el tipo de datos que cada columna puede almacenar.
- Establece restricciones sobre los datos, como claves primarias, foráneas, valores único.

# Ejemplo

```
CREATE TABLE clientes (
    id INT PRIMARY KEY,
    nombre VARCHAR(255),
    email VARCHAR(255) UNIQUE,
    fecha_registro DATE
);
```

