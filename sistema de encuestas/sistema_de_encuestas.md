# Sistema de encuestas

## Listado de entidades

### Encuestas **(ED)**

- encuesta_id **(PK)**
- nombre
- descripcion
- imagen
- fecha
- encuestados

### preguntas **(ED)**

- pregunta_id **(PK)**
- encuesta_id **(FK)**
- pregunta

### respuestas **(ED)**

- respuesta_id **(PK)**
- pregunta_id **(FK)**
- respuesta
- es_correcta

### encuestados **(ED)**

- encuestado_id **(PK)**
- nombre
- apellidos
- edad
- email **(UNIQUE)**

### resultado **(ED)|(EP)**

- resultado_id **(PK)**
- encuesta_id **(FK)**
- encuestado_id **(FK)**
- preguntas
- correctas

## Relaciones

1. Una **encuesta** tiene **preguntas** (_1 - M_).
1. Una **pregunta** obtiene **respuestas** (_1 - M_).
1. Una **encuesta** obtiene **resultados** (_1 - M_).
1. Un **encuestado** tiene **resultados** (_1 - M_).

## Modelo relacional del Sistema de Encuestas

![Sistema de encuestas](./sistema_encuestas.drawio.png)

## Reglas de negocio

Operaciones CRUD (Create, Read, Update, Delete) + Acciones que no se pueden hacer o requerimientos de cada entidad para que su funcionamiento tenga sentido.

### encuestas

1. Crear una encuesta
2. Leer / Consultar una encuesta
3. Actualizar una encuesta
4. Borrar una encuesta

### preguntas

1. Crear una pregunta
2. Leer / Consultar una pregunta
3. Actualizar una pregunta
4. Borrar una pregunta

### respuestas

1. Crear una respuesta
2. Leer / Consultar una respuesta
3. Actualizar una respuesta
4. Borrar una respuesta

### encuestados

1. Crear un encuestado
2. Leer / Consultar un encuestado
3. Actualizar un encuestado
4. Borrar un encuestado
5. Comprobar que el encuestado no esté ya en la BBDD mediante email antes de crearlo.

### resultados

1. Crear un resultado
2. Leer / Consultar un resultados
3. Actualizar un resultados
4. Borrar un resultados
5. Sacar el porcentaje de aciertos que tuvo el encuestado al contestar 