## MYSQL


**Exercise 8.1**
- Instalar paquete mariadb
![Captura1.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/mysql/Captura1.png)

**Parte 1. By executing SELECT User, Host FROM mysql.user; find out the number of entries in the user table in the mysql database.**
![Captura2.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/mysql/Captura2.png)
![Captura3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/mysql/Captura3.png)
![Captura4.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/mysql/Captura4.png)


**Parte 2. What are the commands to create and delete a table, and to select data from a table? What about inserting data into a table?**
- Crear una tabla:

CREATE TABLE nombre_tabla (
    columna1 tipo_dato CONSTRAINTS,
    columna2 tipo_dato CONSTRAINTS
);

- Eliminar una tabla:

DROP TABLE nombre_tabla;

- Seleccionar datos de una tabla:

SELECT * FROM nombre_tabla;

- Insertar datos en una tabla:

INSERT INTO nombre_tabla (columna1, columna2) VALUES ('valor1', 'valor2');




**Parte 3.**
![Parte3.png](https://github.com/Rardati/Despliegue/blob/main/Slackware/mysql/Parte3.png)







**Exercise 8.2 Optional exercises**

**Parte 1**


**Parte 2**






Este es el codigo insertado en index.php
<?php
// 1. Conectar a la base de datos
$servername = "localhost"; // El servidor donde está la base de datos
$username = "adminsec";    // El nombre de usuario de MySQL
$password = "tu_contraseña"; // La contraseña del usuario 'adminsec'
$dbname = "nselab";        // El nombre de la base de datos

// Crear conexión
$conn = new mysqli($servername, $username, $password, $dbname);

// Comprobar la conexión
if ($conn->connect_error) {
    die("Conexión fallida: " . $conn->connect_error);
}

// 2. Ejecutar la consulta SQL para obtener los datos de la tabla users
$sql = "SELECT studentid, firstname, lastname FROM users"; // La consulta para seleccionar datos
$result = $conn->query($sql);

// 3. Mostrar los datos en una tabla HTML
if ($result->num_rows > 0) {
    // Si hay resultados, mostrar cada fila
    echo "<table border='1'>
            <tr>
                <th>Student ID</th>
                <th>First Name</th>
                <th>Last Name</th>
            </tr>";

    // Recorrer cada fila y mostrar los valores
    while($row = $result->fetch_assoc()) {
        echo "<tr>
                <td>" . $row["studentid"] . "</td>
                <td>" . $row["firstname"] . "</td>
                <td>" . $row["lastname"] . "</td>
              </tr>";
    }

    echo "</table>"; // Cerrar la tabla
} else {
    echo "0 resultados"; // Si no hay resultados
}

// 4. Cerrar la conexión
$conn->close();
?> 


