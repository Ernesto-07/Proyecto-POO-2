# Proyecto-POO-2
Proyecto de funcionamiento de taller automotriz.
Proyecto de uso de clases y objetos. En este proyecto de la materia de programacion orientada a objetos seleccione un problema a resolver que involucre diferentes clases y objetos. El problema es que en un taller mecánico se manejan diferentes tipos de información que puede llegar a ser desordenada, como los vehículos que llegan, los mecánicos que trabajan ahí y los servicios que se realizan. Siempre se escribe todo eso en una libreta, lo cual es desordenado. El proyecto busca representar esa información de una forma facil usando programación orientada a objetos.

# Contexto:
Este proyecto es sobre un taller mecánico. La idea es tener clases básicas que representen cosas del taller: un vehículo, un mecánico y un servicio. Cada clase guarda información sencilla y puede mostrarla en pantalla.

# Codigo y su funcionalidad 
El programa crea:

una persona que va a heredar a mecanico y cliente,

un mecánico con su nombre, apellido, edad, experiencia,

un cliente con su nombre, apellido, edad, años de uso,

un vehículo con marca y modelo,

un servicio con su tipo y costo,

y un taller que se conectara por composicion a servicio y vehiculo.

Después, muestra esos datos en consola y también imprime mensajes como la descripción del vehículo, una bienvenida del mecánico y el costo del servicio.

# Menu desplegado 
El menu tiene 6 opciones a considerar:

Opcion de salir del programa al haber pasado por las demas opciones, o si el usuario quiere salir en cualquier momento.
Opcion de agregar el vehiculo
Opcion de agregar el servicio que se le dara al vehiculo
Opcion de mostrar lo que lleva por ahora el taller (los vehiculos con sus respectivos servicios)
Opcion de agregar al cliente con su nombre, apellido, edad, etc.
Opcion de agregar al mecanico que dara el servicio.

# UML y su relacion al problema 
Se sube un archivo png con la imagen del UML que disene, que involucre un numero de clases que el profesor pide. 
En este UML de clases se observa como inclui herencia, usando protected en los atributos. Tambien se incluye composicion dentro de este diagrama, lo que lo hace un diagrama completo. Se podria incluir facilmente agregacion tambien pero sera una modificacion que se hara despues.
En el uml en la parte izquierda, se observa como de persona se hereda a mecanico y a cliente, los cuales daran su informacion mas adelante. Esto para resolver el problema del orden en que llegan los clientes y que mecanico hara el trabajo. En la parte derecha vemos como de taller se compone servicio y vehiculo, que sirve para los registros de los autos que llegan y los 
servicios que se aplicaran. 

# Cosas que harian que el proyecto deje de funcionar 
Por ahora, simplemente que el UML tenga informacion incompleta o insuficiente, o mover cosas que no se deberian de cambiar. 
Mas adelante en el codigo, cosas que podrian hacer tronar este proyecto son cosas como: Al usuario poner un dato diferente al pedido en las opciones del menu lo sacara inmediatamente del programa.

Si el usuario escribe un tipo de dato no esperado, simplemente sacara al usuario del programa.
