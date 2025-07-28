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










