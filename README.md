# B2---Trabajo Consulta 2 Conexión base de datos relacional
## 1. ¿Qué es JDBC y cuáles son sus componentes?
Java Database Connectivity (JDBC) es una interfase de acceso a bases de datos
estándar SQL que proporciona un acceso uniforme a una gran variedad de bases
de datos relacionales. JDBC también proporciona una base común para la
construcción de herramientas y utilidades de alto nivel. 
Con la API JDBC, es posible enviar sentencias SQL a prácticamente cualquier sistema de base de datos sin necesidad de escribir programas específicos para cada uno. Es decir, no es necesario desarrollar un programa distinto para acceder a bases de datos como Sybase, Oracle o Informix.
### Componentes:
#### 1. Driver JDBC (Controlador JDBC)
Es el puente entre la aplicación Java y la base de datos. JDBC define diferentes tipos de controladores para conectar con distintos sistemas de gestión de bases de datos (DBMS).
Tipos de controladores JDBC:
- Tipo 1: JDBC-ODBC Bridge (obsoleto).
- Tipo 2: Controlador nativo-API.
- Tipo 3: Controlador nativo-protocolo (el más utilizado).
#### 2. Connection
- Gestiona la conexión con la base de datos.
- Se obtiene a través del DriverManager y permite iniciar transacciones, establecer configuraciones y cerrar la conexión.
#### 3. Statement
- Permite ejecutar consultas SQL estáticas sin parámetros.
- Se usa para ejecutar comandos SQL simples como SELECT, INSERT, UPDATE, etc.
#### 4. PreparedStatement (Declaración preparada)
- Similar a Statement, pero permite consultas parametrizadas para evitar inyecciones SQL y mejorar el rendimiento en consultas repetitivas.
#### 5. ResultSet 
- Contiene los resultados devueltos por una consulta SQL.
- Se puede recorrer para obtener los datos de la base de datos.
#### 6. DriverManager
- Es el gestor de controladores JDBC, encargado de establecer la conexión con la base de datos según la URL de conexión proporcionada.
- Gestiona múltiples controladores y selecciona el adecuado en función de la URL.
#### 7.  SQLException
- Maneja los errores que pueden ocurrir durante la ejecución de operaciones de base de datos.
## 2. Librerias en Scala que permiten conectarse a una Base de Datos


![image](https://github.com/user-attachments/assets/f9072372-d604-4bec-a862-fbcb92643c7b)

### Conclusión:

- Si prefieres un enfoque similar a trabajar con colecciones de Scala y quieres una API más sencilla, Slick es una buena opción.
- Si buscas mayor control, un enfoque funcional puro y seguridad en transacciones, Doobie es más adecuado.

## 3. ¿Cómo establecer una conexión a una Base de Datos Relacional?
### 1. Creamos la Base de Datos en MySQL.

![image](https://github.com/user-attachments/assets/8260bc47-281b-4ba1-925c-8894885a7828)

### 2. Importamos la dependecia a nuestro proyecto de Scala con el sbt.

![image](https://github.com/user-attachments/assets/2a06c9a6-1179-4e29-8ae5-2bb3155e617b)

### 3. Luego creamos un archivo en Scala para conectar la base de datos.

![image](https://github.com/user-attachments/assets/87e89234-10e5-4b83-a638-1bf08620ed83)

### 4. Probamos la conexión con la base de datos realizando la consulta de los datos de la tabla creada previamente.

![image](https://github.com/user-attachments/assets/71fd3c2b-b63f-44bc-8164-a278504ee1c9)




