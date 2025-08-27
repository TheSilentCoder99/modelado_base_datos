# Maratones

## Listado de Entidades

### carreras (ED)

- carrera_id **(PK)**
- nombre_de_carrera
- tipo_de_carrera **(FK)**
- fecha
- tiempo
- mejor_tiempo   
- altitud
- lugar
- pais **(FK)**
- foto

### tipo de carrera (EC)

- tipo_de_carrera_id **(PK)**
- descripcion
- distancia

### países (EC)

- pais_id **(PK)**
- nombre_pais

## Relaciones

1. Una **carrera** _pertenece_ a un **tipo de carrera**. [_1 a 1_]
1. Una **carrera** se _corre_ en un **país**. [_1 a 1_]

## Diagramas

### Modelo Entidad - Relación

![Práctica1.png](./Práctica1.png)

### Modelo Relacional de la BBDD

![Diagrama1](./Diagrama1.png)

## Reglas de Negocio

### carreras

1. Crear el registro de una de carrera.
2. Leer el registro de una carrera dada una condición en particular.
2. Leer todos los registros de la entidad carreras.
2. Actualizar los datos de una carrera dada una condición en particular.
3. Eliminar los datos de una carrera dada una condición en particular.

### tipos_de_carrera

1. Crear el registro de un tipo de carrera.
2. Leer el registro de un tipo de carrera dada una condición en particular.
2. Leer todos los registros de la entidad tipo de carreras.
2. Actualizar los datos de un tipo de carrera dada una condición en particular.
3. Eliminar los datos de un tipo de carrera dada una condición en particular.

### países

1. Crear el registro de un pais.
2. Leer el registro de un país dada una condición en particular.
2. Leer todos los registros de la entidad paises.
2. Actualizar los datos de país dada una condición en particular.
3. Eliminar los datos de un país dada una condición en particular.
