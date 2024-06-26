# Projecto Final

## Milestone 01

### Contexto

Un cliente nos ha encomendado desarollar una aplicación web tipo marketplace. Esta aplicación está dividida en cinco hitos:

1. Diseño y Prototipo
1. Desarrollo Frontend
1. Desarrollo Backend
1. Integración y Despliegue
1. Presentación del Proyecto

#### Requerimientos de este hito

* Diseño de UI.
* Definición de navegación entre vistas.
* Listado de dependencias a usar.
* Modelo entidad-relación para la base de datos.
* Contrato de datos de la API.

### Diseño Interfaz

![Vista 1](/vistas/Home.png)
![Vista 2](/vistas/Login.png)
![Vista 3](/vistas/Registro.png)
![Vista 4](</vistas/Mis compras.png>)
![Vista 5](/vistas/Productos.png)
![Vista 6](</vistas/Detalle Productos.png>)
![Vista 7](/vistas/Carrito.png)
![Vista 8](/vistas/Perfil.png)
![Vista 9](/vistas/Favorito.png)
![Vista 10](</vistas/Productos publicados.png>)
![Vista 11](</vistas/Publicación producto.png>)

### Navegación entre Vistas

![Navegación](</vistas/Navegación entre vistas.png>)

### Dependencias

#### Frontend

* React (Framework de JavaScript)
* Vite (Herramienta creación de proyectos)
* Ant Design 5 (Framework CSS)
* Bootstrap (Framework CSS)
* React Router (Navegación en React)
* Axios (Peticiones HTTP)
* Formik (Formularios en React)

#### Backend

* Node.js (Entorno de ejecución de Javascript)
* Express.js (Framework JS)
* PostgreSQL (Base de datos)
* JWT (Autentificación)
* CORS (Middleware)
* Dotenv (Para variables de entorno)
* Jest (Framework de Pruebas)
* `swagger-ui` (documentación API)
* `swagger-jsdoc` (documentación API)

### Modelo Base de Datos

Se consideran las siguientes tablas:
* `usuarios`: Representa a usuarios y vendedores.
* `productos`: Representa el pool de productos disponible en el marketplace.
* `publicaciones`: Representa las publicaciones de venta realizadas sobre alguno de los productos disponibles en el marketplace.
* `transacciones`: Representa las compras realizadas por un cliente.

El siguiente diagrama muestra las relaciones y las columnas de cada tabla:
![ddbb-erd](./tbl_relationships.svg)

Se tienen las siguientes relaciones:
* `usuarios`: relación 1:N con tabla `publicaciones`, e.g., un vendedor puede publicar múltiples productos.
* `usuarios`: relación 1:N con tabla `transacciones`, e.g., un comprador puede comprar múltiples veces.
* `categorias`: relación 1:N con tabla `productos`, e.g., una categoría puede albergar varios productos.
* `producto`: relación 1:N con tabla `publicaciones`, e.g., un producto puede estar listado en una o más publicaciones.

### Contrato de datos de API

* `/usuario`
  * `GET`: devuelve información del usuario. Require estar previamente autenticado.
  * `POST`: crea un nuevo usuario. No requiere autenticación.
  * `PUT`: actualiza los datos de un usuario. Requiere autenticación.
* `/productos`
  * `GET`: devuelve una lista paginada de los productos disponibles.
  * `POST`: crea un nuevo producto. Requiere autenticación.
* `/productos/{id}`
  * `GET`: devuelve información de un producto. No require autenticación.
  * `PUT`: actualiza un producto. Require autenticación.
* `/publicaciones`
  * `GET`: devuelve una lista paginada de las publicaciones disponibles
  * `POST`: crea una nueva publicación. Requiere autenticación.
* `/publicaciones/{id}`
  * `GET`: devuelve información de una publicación. No require autenticación.
  * `PUT`: actualiza una publicación. Requiere autenticación.

### Autores

* [Julio Carvajal](https://github.com/jcartronics)
* [Nicolás González](https://github.com/NicolasGonzales-96)
* [Roberto Martínez](https://github.com/RobertoMartinezGuzman)
* [Patricio Parada](https://github.com/pelafustan)

### Agradecimientos

* Café negro.
* Té verde (cuando lele pansha).
* [Desafío Latam](https://desafiolatam.com/)
