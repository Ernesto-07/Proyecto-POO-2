# Proyecto-POO-2
Proyecto de funcionamiento de taller automotriz.
Proyecto de uso de clases y objetos. En este proyecto de la materia de programacion orientada a objetos seleccione un problema a resolver que involucre diferentes clases y objetos. El problema es que en un taller mecánico se manejan diferentes tipos de información que puede llegar a ser desordenada, como los vehículos que llegan, los mecánicos que trabajan ahí y los servicios que se realizan. Siempre se escribe todo eso en una libreta, lo cual es desordenado. El proyecto busca representar esa información de una forma facil usando programación orientada a objetos.

# Contexto:
Este proyecto es sobre un taller mecánico. La idea es tener clases básicas que representen cosas del taller: un vehículo, un mecánico y un servicio. Cada clase guarda información sencilla y puede mostrarla en pantalla.

# Codigo y su funcionalidad 
El programa contiene:

una persona que va a heredar a mecanico y cliente, y aqui es donde se aplica el polimorfismo y clases abstractas, usando virtual en la funcion de describir()=0,

un mecánico con su nombre, apellido, edad, experiencia,

un cliente con su nombre, apellido, edad, años de uso,

un vehículo con marca y modelo,

un servicio con su tipo y costo,

y un taller que se conectara por composicion a servicio y vehiculo, y por agregacion hacia persona.

Después, muestra esos datos en consola y también imprime mensajes como la descripción del vehículo, del mecánico y el costo del servicio.

# Menu desplegado 
El menu tiene 6 opciones a considerar:

0. Opcion de salir del programa al haber pasado por las demas opciones, o si el usuario quiere salir en cualquier momento.

1. Opcion de agregar el vehiculo

2. Opcion de agregar el servicio que se le dara al vehiculo

3. Opcion de mostrar lo que lleva por ahora el taller (los vehiculos con sus respectivos servicios)

4. Opcion de agregar al cliente con su nombre, apellido, edad, etc.

5. Opcion de agregar al mecanico que dara el servicio.

# UML 
[UML](./UML2..png)


# UML y su relacion al problema 
Se sube un archivo png con la imagen del UML que disene, que involucre un numero de clases que el profesor pide. 
En este UML de clases se observa como inclui herencia, usando protected en los atributos. Tambien se incluye composicion dentro de este diagrama, lo que lo hace un diagrama completo. Se incluye agregacion tambien entre taller y persona, agregando personas al taller.
En el uml en la parte izquierda, se observa como de persona se hereda a mecanico y a cliente, los cuales daran su informacion mas adelante. Esto para resolver el problema del orden en que llegan los clientes y que mecanico hara el trabajo. En la parte derecha vemos como de taller se compone servicio y vehiculo, que sirve para los registros de los autos que llegan y los servicios que se aplicaran. 

# Uso de .clear y .fail
Use cin.fail y cin.clear para que cuando se ingrese un valor menor a 0 en los casos donde se pide un numero entero, se imprima que se ingrese un valor entero mayor a 0 y se vuelve a mostrar el menu para darle al usuario la opcion de volverlo a escribir. El .fail me va a funcionar para revisar si la entrada fallo y el .clear funciona para limpiar al cin, que va a seguir recibiendo datos despues de ser limpiado. En resumen, el .fail me va a decir si hubo un error (en este caso que el entero sea menor a 0) y el .clear es para borrar el dato que se habia guardado en el cin, y que pueda seguir recibiendo datos. El continue; es como decir que vuelva al inicio del ciclo ootra vez y no siga con las lineas de codigo de abajo. Esto lo hice para que haya menos casos donde el codigo pueda tronar.

# Uso de destructores
Ya que creamos objetos con new y les reservamos un espacio en el heap, y los destructores son para liberar la memoria que reservamos en este. 

Destructor de clase taller: use un ciclo for que recorre el arreglo y se para cuando llegue al numero de personas (clietes o mecanicos) que se registro, al recorrer esta arreglo, por cada elemento que pasa, usa el delete para borrar la memoria del heap.

Destructor Persona: A este se la anadio el virtual debido a sus clases hijas y por el polimorfismo. Es un destructor vacio que usa el virtual para que el destructor no solo busque en la clase tipo  Persona, sino tambien en cliente y mecanico. Si no se hiciera esto el destructor nomas borraria los atributos que le pertenecen a persona, y dejaria los extra que tienen cliente y mecanico en el heap, por lo que no se limpiaria bien. Se deja vacio el destructor porque c++ sabe como borrarlos por si solo, en taller si use delete porque use un apuntador.

# Consideraciones

Corre en consola.

Está hecho en C++ normal.

1. Entrar a carpeta donde se encuentre el "mainpoo.cpp" y donde se encuentren los demas .h

2. Compilar con: "g++ mainpoo.cpp -o taller". Esto genera el archivo ejecutable

3.  Ejecute el siguiente comando: taller

# Cosas que harian que el proyecto deje de funcionar 
Al usuario poner un dato diferente al pedido en las opciones del menu lo sacara inmediatamente del programa.

1. Si el usuario escribe un tipo de dato no esperado (por ejemplo en edad o costo), simplemente sacara al usuario del programa.

# Correcciones

Se hace correcciones al diagrama de clases, al igual que se anaden complementos, que pertenece a la sub-competencia de Evalúa los componentes que integran una problemática SICT0301A, el diagrama de clases puedes ser observado desde este repositorio.

Se implementa de manera correcta el polimorfismo de manera clara y limpia,  que pertenece a la sub-competencia de Implementa acciones científicas SICT0303A.

Sigo estándares en todo mi código fuente: estilo, sangrías, comentarios, nombres, etc..., que pertenece a la sub-competencia de SICT0303A. Se agregaron comentarios en todo el codigo que especifican y explican los parametros y lo que se regresa. Tambien se cuido lo de limite de caracteres y las sangrias.

Cumplo con estándares en mi repositorio: tiene un readme claro que explica el proyecto (para que sirve, para que no sirve y como se usa), no tiene archivos basura o versiones pasadas, que pertenece a la sub-competencia de SICT0303A. Se modifico el ReadMe para ser mucho mas claro y dejar en claro el contexto del proyecto y su funcionalidad, al igual de que como funciona y que hacer y no hacer.
