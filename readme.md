# Mi Repertorio - Aplicación Musical CRUD

Este proyecto es una implementación básica de un blog donde los usuarios pueden crear publicaciones (posts) y otros usuarios pueden interactuar con ellas mediante el sistema de "likes". El proyecto utiliza Node.js con Express para el backend, PostgreSQL para la base de datos, y HTML/CSS/JavaScript para el frontend.

### Características:

- Creación de Publicaciones: Los usuarios pueden crear nuevas publicaciones ingresando información como el usuario que hace la publicación, la URL de la imagen, y una descripción.
- Visualización de Publicaciones: Todas las publicaciones creadas están disponibles para visualizar.
- Sistema de "Likes": Los usuarios pueden "likear" publicaciones existentes, incrementando así el contador de "likes".


### Prerrequisitos

Para poder ejecutar la API, se deben cumplir los siguientes prerrequisitos:

- Node.js 
- PostgreSQL .
- Tener instalado un cliente de PostgreSQL, como por ejemplo pgAdmin.


### Instalación

Para instalar la API, se deben seguir los siguientes pasos:

1. Clonar el repositorio
```bash
git clone https://github.com/danilojpalma/like_me.git
```
2. Acceder al directorio del repositorio.
```bash
cd mi_repertorio
```
3. Instalar las dependencias del proyecto.
```bash
npm install
```
4. Crear la base de datos en PostgreSQL.

Para crear la base de datos, se debe ejecutar el siguiente comando en el cliente de PostgreSQL:
```sql
CREATE DATABASE repertorio ;
CREATE TABLE canciones (id SERIAL, titulo VARCHAR(50), artista 
VARCHAR(50), tono VARCHAR(10))
```
5. Configurar la conexión a la base de datos.

Debes crear un archivo en la carpeta raiz con el nombre `.env`, en donde se deben configurar las variables de entorno segun tu configuración en tu cliente de PostgreSQL.
```javascript

DB_HOST = localhost
DB_USER = postgres
DB_PASSWORD = contraseña
DB_DATABASE = repertorio

```
### Uso:

Ejecute el servidor con

```bash
npm run dev
```

Abra su navegador web y navegue hasta http://localhost:3000.

### Agregar una nueva canción:

- Ingrese el título, artista y tono de la canción en los campos de entrada respectivos.
- Haga clic en el botón "Agregar".
- Ver todas las canciones:

La tabla de canciones mostrará la lista de canciones en su repertorio.

### Editar una canción:

- Haga clic en el botón "Editar" para la canción que desea modificar.
- Actualice los detalles de la canción en los campos de entrada.
- Haga clic en el botón "Editar" nuevamente (actualizará la canción con los nuevos detalles).


### Eliminar una canción:

Haga clic en el botón "Eliminar" para la canción que desea eliminar.
Confirme la eliminación en el cuadro de diálogo de alerta.

## Código fuente

El código fuente de la API se encuentra en el siguiente repositorio de GitHub:

[https://github.com/danilojpalma/mi_repertorio.git](https://github.com/danilojpalma/mi_repertorio.git)

En el repositorio, se pueden encontrar los archivos de configuración de la base de datos (`db.js`) y las consultas a la base de datos (`queries.js`).

## Licencia

Este proyecto se encuentra bajo la licencia MIT. Para más información, consultar el archivo `LICENSE.md`.