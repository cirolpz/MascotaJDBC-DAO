
# MascotaJDBC-DAO
![Captura de pantalla 2024-12-07 013219](https://github.com/user-attachments/assets/ec7e85a6-7383-48c1-833f-9c2b18f962d5)

Este proyecto lo realicé para aprender JDBC y DAO en el bootcamp EGG.

## Descripción

MascotaJDBC-DAO es una aplicación desarrollada en Java que implementa un sistema de gestión de mascotas utilizando JDBC y el patrón DAO (Data Access Object). El objetivo de este proyecto es proporcionar una comprensión práctica de cómo interactuar con bases de datos mediante JDBC y aplicar el patrón DAO para la separación de la lógica de acceso a datos.

## Características

-   **Gestión de Mascotas**: Permite añadir, actualizar, eliminar y buscar mascotas.
-   **Uso de JDBC**: Interacción directa con la base de datos utilizando JDBC.
-   **Patrón DAO**: Implementación del patrón DAO para la gestión de la persistencia de datos.

## Tecnologías Utilizadas

-   **Java**: Lenguaje de programación principal.
-   **JDBC (Java Database Connectivity)**: Para la conexión y ejecución de consultas en bases de datos.
-   **MySQL**: Base de datos relacional.
-   **Maven**: Herramienta de gestión de proyectos y dependencias.

## Requisitos Previos

-   JDK 11 o superior.
-   Maven 3.6 o superior.
-   Una base de datos MySQL configurada.

## Instalación y Ejecución

1.  Clona el repositorio:
    
    ```bash
    git clone https://github.com/cirolpz/MascotaJDBC-DAO.git
    
    ```
    
2.  Navega al directorio del proyecto:
    
    ```bash
    cd MascotaJDBC-DAO
    
    ```
    
3.  Configura la conexión a la base de datos en el archivo  `application.properties`:
    
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/mascotas_db
    spring.datasource.username=tu_usuario
    spring.datasource.password=tu_contraseña
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
    
    ```
    
4.  Compila y ejecuta la aplicación:
    
    ```bash
    mvn clean install
    mvn spring-boot:run
    
    ```
    

## Uso

### Endpoints

-   `GET /mascotas`: Obtener todas las mascotas.
-   `GET /mascotas/{id}`: Obtener una mascota por ID.
-   `POST /mascotas`: Crear una nueva mascota.
-   `PUT /mascotas/{id}`: Actualizar una mascota existente.
-   `DELETE /mascotas/{id}`: Eliminar una mascota por ID.

### Ejemplo de Peticiones

-   **Crear una nueva mascota**:
    
    ```bash
    curl -X POST http://localhost:8080/mascotas -H "Content-Type: application/json" -d '{"nombre":"Firulais","edad":3}'
    
    ```
    
-   **Obtener todas las mascotas**:
    
    ```bash
    curl -X GET http://localhost:8080/mascotas
    
    ```
    

## Contribuir

1.  Haz un fork del repositorio.
2.  Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3.  Realiza tus cambios y haz commit (`git commit -am 'Añadir nueva funcionalidad'`).
4.  Sube tus cambios a tu rama (`git push origin feature/nueva-funcionalidad`).
5.  Abre un Pull Request.

## Licencia

Este proyecto está licenciado bajo la Licencia MIT.
