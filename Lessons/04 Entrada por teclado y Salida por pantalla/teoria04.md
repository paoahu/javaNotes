## 4. Entrada por teclado y salida por pantalla (I/O)

Java tiene 3 streams (flujos) de entrada y de salida:

1) **Entrada estándard (standard input stream)**. Por defecto se refiere al teclado, aunque se puede redigir a otra fuente de entrada, como por ejemplo, un fichero de texto. Para acceder a este flujo usaremos ```System.in```
2) **Salida estándard (standard output stream)**. Por defecto Java utiliza la pantalla de la consola como salida, pero se puede cambiar, por ejemplo, a un fichero de texto. Para acceder a este flujo usaremos ```System.out```
3) **Salida de error (error output stream)** Este stream se utiliza para mostrar mensajes de error o con información importante. Por defecto, se utiliza la pantalla de la consola, pero también es frecuente redirigirlo haca un fichero .log. Para acceder a este flujo usaremos ```System.err```

La clase ```System``` de API Java nos proporciona acceso a 3 atributos públicos y estáticos llamados ```in``` , ```out``` , ```err``` . Tanto ```System.in``` como ```System.out``` y ```System.error``` son instanciados e inicializados automáticamente por la JVM cuando ésta se enciende, así que no hace falta nada para tenerlos disponibles.

### 4.1 MÉTODOS DE SALIDA
La clase ```System``` de API Java nos proporciona acceso a un atributo público y estático llamado ```out``` de tipo ```PrintStream``` (otra clase de API de Java). Este atributo, que es una referencia a un objeto de la clase ```PrintStream```, nos permite acceder a los métodos públicos de esta clase, la cual se encarga de escribir datos en el flujo de salida que se indique. Entre ellos, destacana: ```print``` ```println``` ```printf```

**Métodos print y println**

Estos dos métodos son los más frecuentes. La diferencia entre ellos es que ```println``` imprime el contenido que se le pasa y añade un salto de línea (\n)

```
System.out.print(5);
System.out.println(8); // es equivalente a print(8 + "\n");
System.out.print(5);
```
El código anterior imprimiría:

```
58
5
```
**Método printf**
Los métodos anteriores no permiten especificar un formato para controlar aspectos como, por ejemplo, el número de decimales que es necesario mostrar para un valor de tipo ```double```. El método ```printf``` recibe, como mínimo, una cadena de texto que indica el texto juntamente con el formato que es necesario mostrar. 

```
System.out.printf("Hola! %d %2.d", 53, 89.7); //Hola! 53 89.70 -> añade un 0 para que 87.9 tenga 2 decimales
System.out.printf("Hola! %03.d", 53); //Hola! 053 -> añade un 0 para que 53 tenga 3 dígitos
```

La manera de indicar en el texto de salida dónde queremos usar un fomrato especial es mediante el uso de un comodín que tiene un formato determinado % [flags][ancho]codigoConversion. Tanto los flags como el ancho son dos valores opcionales. Los flags sirven para indicar aspectos de la alienación del texto y el elemento que hay qe añadir como padding (relleno), entre otros. Por su parte, el ancho es un valor que indica cuanto espacio tiene que ocupar el elemento como mínimo. Para acabar, el código de conversión sirve para indicar el tipo de valor:

- ```d``` para entero
- ```f``` para float o double
- ```c``` para char
- ```i``` para String

```
System.out.printf("%s|%6d|%.2f", "eps", 53, 89.7); //eps|    53|89.7 -> el número 53 ocupa un ancho de 6 caracteres
System.out.printf("Hola|%-4d|", 53); //Hola|53  |" -> 53 ocupa 4 posiciones y está alineado a la izquierda (se indica con un -)
```

Respecto al salto de línea, este método funciona exactamente igual que print, no avanza el cursor en la línea siguiente. Así que si queremos hacer el salto, tenemos que añadir \n al final del texto.

### 4.2 MÉTODOS DE ENTRADA
Como ya hemos comentado, por defecto, el flujo de entrada proviene del teclado. En JDK 5 se introdujo una clase llamada ```Scanner``` que facilita la lectura con el formato del teclado. De esta manera, con ```Scanner``` podremos controlar, de manera sencilla, si queremos leer un ```int``` , un ```double``` , etc.

```
Scanner in = new Scanner(System.in); //Objeto Scanner que lee de teclado
int number = in.nextIn(); // espera recibir un int, en caso contrario lanza una excepción
double decimal = in.nextDouble(); //espera recibir un double, en caso contrario lanza una excepción
String word = in.next(); //lee un texto hasta llegar al primer espacio
String text = in.nextLine(); //lee un texto hasta llegar al primer salto de línea (incluye espacios en blanco)
in.Close(); //Cerramos el flujo (stream)