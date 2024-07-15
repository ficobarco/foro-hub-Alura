Foro Hub

Descripción: Foro Hub es una aplicación web de foro desarrollada con Spring Boot para gestionar tópicos de discusión, con funcionalidades CRUD y autenticación JWT.

Características:

    CRUD de Tópicos: Crear, leer, actualizar y eliminar tópicos.
    Autenticación JWT
    Validaciones: Con Jakarta Bean Validation.
    Swagger: Documentación automática de la API.

Dependencias Principales:

    Swagger, Lombok, Spring Web, Spring Boot DevTools, Spring Data JPA, Flyway Migration, MySQL Driver, Validation, Spring Security.

Requisitos Previos:

    JDK 17+, Maven 3.8.1+, MySQL 8.0+

Configuración del Proyecto:


Configurar MySQL:

sql

CREATE DATABASE foro_hub;
CREATE USER 'foro_user'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON foro_hub.* TO 'foro_user'@'localhost';
FLUSH PRIVILEGES;

Configurar propiedades en application.properties:

properties

    spring.datasource.url=jdbc:mysql://localhost:3306/foro_hub
    spring.datasource.username=foro_user
    spring.datasource.password=password
    spring.jpa.hibernate.ddl-auto=update
    api.security.secret=tu_secreto_de_jwt



Uso de la API:

Autenticación: Envía una solicitud POST a /login con las credenciales del usuario para obtener un token JWT.

Endpoints Principales:

    POST /topicos: Crear tópico.
    GET /topicos: Listar tópicos.
    PUT /topicos/{id}: Actualizar tópico.
    DELETE /topicos/{id}: Eliminar tópico.
