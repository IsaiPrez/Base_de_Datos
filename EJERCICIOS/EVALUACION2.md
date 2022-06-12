## Práctica 3.
### Introducción a SQL
Objetivo: Demostrar la correcta identificación de los conceptos del lenguaje SQL
Ejercicio:

1. Menciona los comandos DMl: (valor .85)

* Select: Se usa para mostrar datos que hayamos seleccionado.
* Insert: Sirve para ingresar datos a la base de datos.
* Update: Sirve para modificar valores.
* Delete: Encargado para borrar tablas.

2. Menciona 3 tipos de datos que existen: (valor .85)
* Char
* Varchar
* int
* smallint
* bigint
* float

3. ¿Qué diferencia existe entre TRUNCATE y DELETE?(valor .85)

* DELETE borra una serie de filas y TRUNCATE borra todas las filas de una tabal

4. ¿Para qué se utiliza el atributo UNIQUE?(valor .85)

* Permite establecer este atributo a los campos que requieran que no se repitan.

5. ¿Qué diferencia hay entre los tipos de datos VARCHAR y CHAR? (valor .85)

* CHAR es una longitud de caracteres fijas y VARCHAR  es una cadena de longitud variable. Ambas especificadas por el usuario.

6. Defina brevemente el significado de las siglas SQL(valor .85)
 
* Structured Query Language

7. Defina brevemente qué es MySQL WorkBench (valor .85)

* Es un editor visual que se caracteriza por su editor de diagramas.

## Práctica 5.
### Gestores de base de datos

Objetivo: Categorizar los distintos gestores de base de datos que existen y señalar las
ventajas y desventajas

Evaluación: Conoce los tipos de gestores de base de datos 3 puntos.

Domina sus diferencias de los gestores de base de datos mencionados 3 puntos

Ejercicio:

En un mapa conceptual presenta 3 gestores de bases de datos, sus características
principales, las ventajas y desventajas. (valor 6)

![image](https://user-images.githubusercontent.com/101481084/172527553-165a391a-7184-4945-a6e3-6f91d3b41cf1.png)



![image](https://user-images.githubusercontent.com/91554777/170415427-e2b7321b-a97f-43b0-ac24-6e506c307e6b.png)

## Práctica 6.
### Herramienta en línea y ejercicio necesarios para realizar las prácticas

Creación de base de datos.

Objetivo: Demostrar mediante la creación de una base de datos el uso y la aplicación de
las funciones

Ejercicio: Creación de la base de datos (valor 18 puntos)

Tienda de informática

![image](https://user-images.githubusercontent.com/91554777/170415101-717bca19-3644-46a9-8a57-8d5940c5d283.png)




Modelo entidad/relación

![image](https://user-images.githubusercontent.com/101481084/173250480-a115b4c5-4827-4d77-bac0-99784e73aa6f.png)

Base de datos para MySQL

 CREATE DATABASE Tienda; 
USE Tienda;

CREATE TABLE Fabricante ( 
 ID_prov VARCHAR(100) PRIMARY KEY,
 Nom_prov VARCHAR(100) NOT NULL,
 Dir_prov VARCHAR(100), 
 Tel_prov VARCHAR (20), 
 Tipo_prov VARCHAR (50),
 Prod_prov VARCHAR (30)
);
 
 INSERT INTO Fabricante VALUES ("1", "SEAGATE", "Calle 1", "12345", "HARDWARE", "DISCO DURO SATA 3 1 TB" );
 INSERT INTO Fabricante VALUES ("2", "CRUCIAL", "Calle 2", "12341", "HARDWARE", "MEMORIA RAM DDRR4 8 GB" );
 INSERT INTO Fabricante VALUES ("3", "SAMSUNG", "Calle 3", "12342", "HARDWARE", "DISCO SSD 1TB" );
 INSERT INTO Fabricante VALUES ("4", "GIGABYTE", "Calle 4", "12342", "HARDWARE", "GeForce GTX 1880 EXTREME" );
INSERT INTO Fabricante VALUES ("5", "ASUS", "Calle 5", "12343", "HARDWARE", "Monitor 24 LED FULL HD" );
INSERT INTO Fabricante VALUES ("6", "LENOVO", "Calle 6", "12344", "HARDWARE", "Portátil Yoga 520" );
INSERT INTO Fabricante VALUES ("7", "HP", "Calle 7", "12346", "HARDWARE", "Impresora HP Deskjet 3700" );



CREATE TABLE Producto ( 
 ID_prod VARCHAR (100) PRIMARY KEY, 
 Nom_prod VARCHAR (100), 
 Precio_prod FLOAT, 
 ID_prov1 VARCHAR (20), 
 FOREIGN KEY (ID_prov1) REFERENCES Fabricante (ID_prov) );
 
INSERT INTO Producto VALUES ("DD-23", "DISCO DURO SATA 3 1 TB", 86.99, "1");
INSERT INTO Producto VALUES ("MM-34", "MEMORIA RAM DDRR4 8 GB", 120.6, "2");
INSERT INTO Producto VALUES ("DD-98", "DISCO SSD 1TB",150.99, "3");
INSERT INTO Producto VALUES ("MM-98", "GeForce GTX 1080 EXTREME", 185.70, "4");
INSERT INTO Producto VALUES ("MM-23", "GeForce GTX 1050 TI", 755.6, "2");
INSERT INTO Producto VALUES ("MT-12", "MONITOR 24 LED FULL HD", 202.1, "5" );
INSERT INTO Producto VALUES ("MT-08", "MONITOR 27 LED FULL HD", 24.99, "5" );
INSERT INTO Producto VALUES ("LP-19", "PORTATIL YOGA 520", 559.2, "6" );
INSERT INTO Producto VALUES ("LP-11", "PORTATIL IDEAPD 320", 444.2, "6" );
INSERT INTO Producto VALUES ("IM-56", "IMPRESORA HP DESKJET 3720", 59.99, "7" );
INSERT INTO Producto VALUES ("IP-54", "IMPRESORA HP LASERJET PRO M26", 180.3, "7" );

USE Tienda;
--SELECT Nom_prov, Nom_prod FROM Fabricante INNER JOIN Producto ON Fabricante.ID_prov=Producto.ID_prod;






