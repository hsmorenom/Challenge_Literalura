Sistema de Gestión de Libros y Autores
Este es un sistema para gestionar libros y autores. Permite realizar diferentes consultas sobre los libros y autores registrados en la base de datos. La aplicación está construida en Java utilizando Spring Boot y Hibernate para la gestión de la persistencia en la base de datos.

Requisitos
Java 21 o superior
PostgreSQL (u otra base de datos compatible con JPA)
Maven (para gestionar las dependencias)
Funcionalidades
El sistema permite realizar las siguientes acciones a través de un menú interactivo en consola:

Buscar un libro por título: Permite buscar un libro por su título en la base de datos. El sistema devolverá información como el autor, idioma y el número de descargas del libro.

Listar libros registrados: Muestra una lista de todos los libros registrados en la base de datos, incluyendo su título, autor, idioma y número de descargas.

Listar autores registrados: Muestra una lista de todos los autores registrados en la base de datos, mostrando su nombre y fecha de nacimiento (y si está disponible, la fecha de fallecimiento).

Listar autores vivos en un año: Muestra una lista de autores que estaban vivos en un año determinado. El sistema verificará la fecha de nacimiento y fallecimiento de los autores.

Listar libros por idioma: Muestra una lista de libros que están registrados en un idioma específico. Los idiomas disponibles son español (es), inglés (en), francés (fr) y portugués (pt).

Salir: Cierra la aplicación.

Instalación
1. Clonar el repositorio
bash
Copiar código
git clone https://github.com/usuario/repositorio.git
2. Configurar la base de datos
Asegúrate de tener una base de datos PostgreSQL configurada. Puedes usar una base de datos existente o crear una nueva para este proyecto. Luego, configura los detalles de la base de datos en el archivo application.properties de la carpeta src/main/resources:

properties
Copiar código
spring.datasource.url=jdbc:postgresql://localhost:5432/nombre_de_tu_base_de_datos
spring.datasource.username=tu_usuario
spring.datasource.password=tu_contraseña
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect
3. Ejecutar la aplicación
Asegúrate de que las dependencias estén instaladas. Si estás usando Maven, puedes ejecutar el siguiente comando para instalar todas las dependencias necesarias:

bash
Copiar código
mvn clean install
Para ejecutar la aplicación:

bash
Copiar código
mvn spring-boot:run
4. Acceder a la aplicación
La aplicación se ejecutará en el terminal y presentará el siguiente menú:

less
Copiar código
Escoge una opción:
1 - Buscar un libro por título
2 - Listar libros registrados
3 - Listar autores registrados
4 - Listar autores vivos en un año
5 - Listar libros por idioma
0 - Salir
Estructura del Proyecto
com.desafiochallenge.model: Contiene las clases Libro y Autor, que representan las entidades de la base de datos.
com.desafiochallenge.repository: Contiene los repositorios de JPA para interactuar con la base de datos.
com.desafiochallenge.service: Contiene los servicios que implementan la lógica de negocio, como la búsqueda de libros, la lista de autores y libros, y la verificación de autores vivos.
com.desafiochallenge.principal: Contiene la clase principal (Principal) con la lógica del menú interactivo.
Contribución
Si deseas contribuir a este proyecto, por favor realiza un fork del repositorio y envía tus cambios a través de un pull request. Asegúrate de seguir las buenas prácticas de codificación y de documentar adecuadamente tus cambios.
