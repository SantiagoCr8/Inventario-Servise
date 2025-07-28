# Producto-Service

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)  
![License](https://img.shields.io/badge/license-MIT-blue)

## Descripción
Es un microservio que ayuda a la gestion de productos

## Prerequisitos
¿Qué necesitas instalado en tu máquina?
```bash
- Java 17
- Maven 3.8+
- PostgreSQL 17
```
## Base de datos
El microservicio utiliza PostgreSQL 17 y se debe hacer la siguiete configuracion a la base de datos
```bash
username: postgres
password: admin
port: 5432
database: postgres
```
si quiere cambiar la base de datos lo puede hacer en application.properties

## Instalacion
Crea una carpeta donde se va ha guardar el proyecto y habre un cmd dentro de la ruta

Copia los siguietes comandos en el cmd y ejecutelos
```bash
git clone https://github.com/SantiagoCr8/Producto-Servise.git
cd Producto-Servise
mvn clean package -DskipTests
```
## Ejecucion
Cuando termine de ejecutar verifica que el servicio de Producto-Servise este funcionando y despues ejecute el siguiente comando para correr el servicio
```bash
java -jar target/producto-service-0.0.1-SNAPSHOT.jar --spring.profiles.active=local
```

## Funcionamento

El servicio corre el puerto 8081 y se crearon 3 enpoint para el microservicio

### Buscar Producto
Se encarga de traer el stock de un productio especifico

puedes ingresar con la siguiete URL http://localhost:8081/productos/{id} y cambias el {id} por el id del producto que quieres buscar

### Crear producto
El enpoit se encarga de crear nuevos productos

puedes ingresar con la siguiete URL http://localhost:8081/productos y se debe enviar un json con los siguientes atributos
```bash
    {
    "nombre": "Leche",
    "precio": 1000.00,
    "descripcion": "Leche"
}
```

## Test
El microservio ya tiene pruebas unitarias y pruebas de integracion
## Excepciones 
EL microservicio ya cuenta con un manejo de excepciones y son manejadas con condigos HTTP
## Documentacion Microservicio
Con las siguiente URI se puede ingresar a la documentacion de los enpoint /doc/swagger-ui/swagger-ui/index.html

<img width="1465" height="675" alt="image" src="https://github.com/user-attachments/assets/0ca098b9-a85c-4dfd-bc75-26356b1d71e4" />

Ejemplo:

http://localhost:8081/doc/swagger-ui/swagger-ui/index.html











