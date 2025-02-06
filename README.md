# conectaCorp

## Backend

El backend se ha realizado con Node.js + Express.js.

### Endpoints

1. Usuarios

    POST /api/users

    Descripción: Crea un nuevo usuario en la base de datos.

    Parametros:
    - username (requerido): Nombre de usuario.
    - password (requerido): Contrasena.
    - email (requerido): Correo electronico.

2. Salas

    GET /api/rooms

    Descripción: Recupera el listado de salas disponibles. 

    POST /api/rooms

    Descripción: Crea una nueva sala en la base de datos.

    Parametros:
    - name (requerido): Nombre de la sala.

    POST /api/rooms/:id/username

    Descripción: Invita a un usuario a una sala.

    Parametros:
    - id (requerido): ID de la sala.
    - username (requerido): Nombre de usuario.

3. Mensajes

    GET /api/messages

    Descripción: Recupera el historial de mensajes de una sala, con posibilidad de paginación.

    Parametros:
    - room (requerido): Nombre de la sala.
    - page (opcional): Página de la paginación.
    - limit (opcional): Cantidad de mensajes por paquete.

    POST /api/messages

    Descripción: Guarda un nuevo mensaje en la base de datos.