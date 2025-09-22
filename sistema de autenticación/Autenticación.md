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