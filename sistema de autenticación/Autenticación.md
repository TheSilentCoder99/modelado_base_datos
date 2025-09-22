## Listado de entidades

### usuarios (ED)
- usuario_id **(PK)**
- nombre_usuario **(UQ)**
- contrasenia
- correo_electronico **(UQ)**
- nombre
- apellido
- foto_perfil
- activo
- fecha_creacion
- fecha_actualizacion

### roles **(EC)**

- rol_id **(PK)**
- nombre
- descripcion
- duracion

### permisos **(EC)**
- permiso_id **(PK)**
- nombre
- descripcion
- duracion

### roles_x_usuario **(EP)**
- rol_x_usuario_id **(PK)**
- usuario_id **(FK)**
- rol_id **(FK)**

### permisos_x_roles **(EP)**
- permiso_x_rol_id **(PK)**
- permiso_id **(FK)**
- rol_id **(FK)**

## Relaciones

1. Un **rol** otorga **permisos** (M - M)
1. Un **usuario** tiene **rol/es** (M - M)

<!-- ¿Por qué la relación usuario<=>permiso no es necesaria? 

En los sistemas de autenticación/autorización se suele usar el modelo RBAC (Role-Based Access Control).

Relaciones típicas en RBAC:

Rol ↔ Permiso:

Relación muchos a muchos (M–M).

Un rol puede otorgar muchos permisos, y un permiso puede estar en muchos roles.
✅ Esta es fundamental, no sobra.

Usuario ↔ Rol:

Relación muchos a muchos (M–M).

Un usuario puede tener varios roles, y un rol puede asignarse a varios usuarios.
✅ También es fundamental.

Usuario ↔ Permiso (directa):

Aquí depende del diseño:

En RBAC puro, NO se modela directamente usuario–permiso, porque los permisos se heredan siempre vía roles.

En sistemas más flexibles (a veces llamados RBAC extendido o ABAC híbrido), sí puede existir una relación directa de usuario–permiso para excepciones o permisos especiales.
Es decir, los permisos de un usuario se obtienen consultando los roles que tiene.
  -->
