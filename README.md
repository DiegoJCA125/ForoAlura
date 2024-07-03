# 	:toolbox: Proyecto Foro Alura (BackEnd)

Foro Hub es un Web API  creada en Java Spring, que se basa en REST, corresponde a un requisito para la formación de `BacKend` de #OracleOne y #Alura.

<h2>Base de datos</h2>

Este API se conecta a una base de datos MySQL, la cual contiene una serie de tablas, se detallan a continuación: 

 Tabla course: Contiene los cursos que se imparten en el foro.
 Tabla status: Contiene el estado de los tópicos (Activo, Inactivo)
 Tabla profile: Contiene los diferentes tipos de perfiles de los usuarios (Administrator, Experto, Junior)
 Tabla user: Contiene los usuarios que crean tópicos, respuestas a esos tópicos.
 Tabla topic: Es la parte fundamental del challenge, crea el foro o la consulta que tiene un usuario en el sistema.
 Tabla responses: Contiene las respuestas a cada de los tópicos del sistema.

El modelo de base de datos se observa de la siguiente manera:

<h2>Métodos del Web API</h2>

La función principal de este Web API es crear una tópico(consulta del foro) para uno de los cursos y que otros usuarios puedan ayudarle mediante respuestas.

El mismo permite consultar, crear, modificar y eliminar tópicos, respuestas. Y permite consultar, crear y modificar usuarios.

A continuación se adjuntan diversas imágenes del proyecto:

- Entorno de desarrollo en ejecución. 
- Métodos del Web API, documentación mediante `Swagger UI`.
- 
<h2>Autenticación</h2>

- Para utilizar los métodos del Web API es necesario autenticarse, se utiliza JWT para realizarlo, lo debe de realizar en el método `POST` de la ruta `/login`
- Una vez generado el token deberá de utilizarse en la sección Authorize (Swagger UI).
- Una vez verificado el token podra consumir los métodos de `GET`, `POST`, `PUT`, `DELETE`.

<h2>:hammer_and_pick: Métodos más utilizados del Web API</h2>
- Este es un ejemplo del método `GET` de la ruta /topics, que retorna todos los tópicos y las respuestas que le han brindado al mismo.
- En la siguiente imágen se observa el método `POST` para crear un nuevo tópico.
- Se observa el método `POST` para crear una respuesta al tópico creado anteriormente.
- Acá se observa como la consulta al tópico y la respuesta registrada.
------------------------

<h2>Tecnologías Utilizadas</h2>
- Lombok
- JDK 17.
- Maven.
- Validation
- Spring Web
- Spring Boot.
- Swagger UI. 
- MySQL.
- Spring Data JPA.
- Flyway Migration
- Spring Security - Auth0 para la creación de JWT.
