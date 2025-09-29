# REST server Bibliteca

Descripción:

Quiero crear un REST server para una biblioteca que permita gestionar libros, autores, géneros y todo ello pueda ser asignado a un usuario, el cual podrá reservar dicho libro.

Cada libro estará asociado a un autor, un género y un usuario que lo registró (admin). Entidades como género o editorial se irán añadiendo para darle más contenido a la base.

Los libros tendrán un stock predeterminado de 1, por lo que no se podra reservar el mismo libro por dos usuarios a la vez.

# FUNCIONALIDAD RESERVA Y NOTIFICACIÓN DE DISPONIBILIDAD

Las reservas se podrán hacer para un máximo de 20 días, el usurario podrá elegir la cantidad de 1-20 y la cantidad máxima de libros serán de 1 por el momento.

Si un libro se encuentra en estado "reservado", los usuarios podrán pedir que sean notificados cuando el libro vuelva a estar "disponible".

# RESERVAS DE SALA PARA FIRMA DE LIBROS O AUDIENCIAS

Un autor podrá reservar por horas (max 4h), una sala de la librería que será adecuada para el tipo de evento. Todo esto se podrá hacer desde un menú de reservas especial al que solo podrán acceder los roles ADMIN y AUTOR. Dicha reserva tendrá que ser confirmada por un ADMIN, al cual le llegará una notificación de la reserva.

En dicho menú podrá solicitar el tipo de evento... firma de libros, lectura, etc... para que el admin pueda checkear y preparar dicha sala para el evento. 

Los usuarios podrán recibir emails de aviso con información del evento (autor, libro, firma o lectura) para acudir si lo desean reservando una plaza (máx 50 usuarios).

# COMPOSICIÓN DE ENTIDADES

El sistema incluirá CRUD para todas las entidades, autenticación JWT, con roles y permisos, búsqueda de información y subida de imágenes de libros, autores y usuarios a una bd no-sql. La idea es empezar con lo básico (libros y usuarios) y luego ampliar funcionalidades.

# LIBRO
- id
- nombre
- autor
- registrado por (adminUser)

# USUARIO
- nombre
- email
- contraseña
- rol
- fechaRegistro

# AUTOR
- nombre
- género
- biografía

## ROLES
- ADMIN
- USER
- AUTHOR


