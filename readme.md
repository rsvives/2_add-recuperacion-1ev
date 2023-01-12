# Acceso a datos: Recuperación 1ª Ev

## Contenidos
1. Ficheros
   1. De texto
   2. De acceso aleatorio
2. Bases de datos relacionales:
    1. Sentencias parametrizadas
    2. Transacciones


## Instrucciones

- Leer todo el contenido de este fichero detenidamente antes de empezar.
- Cada ejercicio puntúa diferente y está compuesto por una serie de apartados que van puntuando.
  Es altamente recomendable detectar qué ejercicios se pueden hacer de manera más sencilla y rápida para aprovechar el
  tiempo de la mejor manera posible.
- Todos los métodos tendrán que contemplar las excepciones necesarias.
- ⚠️ Se recuerda que, para los ejercicios de bases de datos, es necesario instalar el driver de MySQL.

## Enunciados

### Ejercicio 1: ficheros (5 puntos) 

El fichero `temperaturas.txt` en la carpeta "archivos" contiene un conjunto de temperaturas, cada una de ellas en una línea diferente.
Crear los siguientes métodos y llamarlos desde el main:

#### - leerTemperaturas(File) [2pts]:
Método que recibe el fichero `temperaturas.txt` y devuelve un ArrayList con las temperaturas que contiene en su interior. 

#### - aumentarTemperaturas(ArrayList<Integer>, numero) [2pts]:
Método que recibe un ArrayList y un número y crea un fichero llamado `nuevas_temperaturas.txt` con las temperaturas contenidas en el ArrayList, sumándoles el número recibido por parámetros.

#### - temperaturasAccesoAleatorio(ArrayList<Integer>) [1pts]:
Método que recibe un ArrayList, lo itera, y por cada elemento del ArrayList, crea un registro de una determinada longitud
en un fichero de acceso aleatorio. Dicho fichero se ha de crear en el propio método y se ha de llamar `temperaturas-raf.txt`. 
El tamaño del registro (stingBuffer) ha de ser de 30.


### Ejercicio 2: bases de datos
Se va a utilizar un servidor de bases de datos en local, por lo que habrá que arrancar servidor MySQL del XAMPP.
>⚠️ Es importante incluir el driver de MySQL en este proyecto para poder testear y ejecutar dicha conexión correctamente.

#### - crearConexión [1pts]
Crear un método que permita crear una conexión con una base de datos cuyos datos se facilitan a continuación.
El método ha de retornar un objeto de tipo Connection, con la conexión a la base de datos.
**No es necesario** que reciba los parámetros de la conexión como argumentos.

- Host: localhost
- Puerto: el que indica el XAMPP
- Nombre base de datos: add_recuperacion_1ev (crearla a mano con el Heidi / PHPMyAdmin)
- Usuario: root
- Contraseña: (vacío)

#### - crearTabla() [1pts]

Crear una tabla de películas desde Java con los siguientes datos:
- id
- titulo
- año
- director
- genero

#### - insertarRegistros() [1,5pts]
Método que sirve para insertar 3 registros de películas. 
La inserción se tiene que hacer de cada registro por separado, pero todos englobados en una transacción. 

#### - consultaPreparada() [1,5pt]
Método que muestra por pantalla aquellas películas que se hicieron a partir del año 2000. 
La consulta se tiene que realizar mediante una sentencia preparada