# Ventas

## Listado de entidades

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono **(UQ)**
- email **(UQ)**
- direccion
- cp
- ciudad
- pais **(FK)**

### productos **(ED|EC)**

- producto_id **(PK)**
- nombre
- descripcion
- foto
- precio
- cantidad_stock

### ventas

- venta_id **(PK)**
- cliente_id **(FK)**
- fecha
- importe

### articulos_x_venta **(ED)**
<!-- Esto es una entidad pivote: relaciona información de dos o más tablas. En esta entidad habrá más de una llave foránea. -->

- articulo_id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad_vendidos

<!-- Pedir aclaración a CHATGPT. esta entidad está algo confusa. -->


### pais **(EC)**

- pais_id **(PK)**
- nombre
- dominio **(UQ)**


<!-- Cuando marcas un atributo como UNIQUE en una base de datos, lo que haces es garantizar que su valor no se repita en ningún registro de la tabla. Es una forma de aplicar integridad de datos automática desde el propio motor de base de datos. -->

## Relaciones

1. Un **cliente** vive **pais** (1:M)
2. Un **cliente** genera **venta** (1:M)
3. Un **articulo** pertence **venta** (1:M)
Un **articulo** es un **producto** (1:M)

## Diagramas

### Modelo relacional de la base de datos

![Modelo relacional](/Modelado%20relacional%20sistema_de_Ventas.png)

## Reglas de negocio

<!-- Reglas de negocio para cada entidad, es decir, operaciones CRUD necesarias para cada entidad -->

### clientes
1. Crear/añadir un cliente
2. Leer un cliente en particular
3. Leer todos los clientes
3. Actualizar un cliente
4. Borrar un cliente

### productos
1. Crear/añadir un producto
2. Leer un producto en particular
3. Leer todos los productos
3. Actualizar un producto
4. Borrar un producto
5. Cada vez que haya una venta, la cantidad de productos vendida debe ser restada del stock.

### ventas
1. Crear/añadir una venta
2. Leer una venta en particular
3. Leer todas las ventas
3. Actualizar una venta
4. Borrar una venta
5. Cada vez que haya una venta, la cantidad de productos vendida debe ser restada del stock.

### articulos_x_venta

1. Crear/añadir un articulo
2. Leer un articulo en particular
3. Leer todos los artículos
3. Actualizar un articulo
4. Borrar un articulo
5. Leer todos los artículos de una venta
5. Leer todos los artículos de un producto
5. Leer todos los artículos de un cliente

### pais
1. Crear/añadir un pais
2. Leer un pais en particular
3. Leer todos los países
3. Actualizar un pais
4. Borrar un pais