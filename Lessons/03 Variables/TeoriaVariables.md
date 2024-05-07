# Variables en Java

## Introducción

En esta lección, exploraremos las variables en Java, que son esenciales para almacenar datos en nuestros programas. Antes de profundizar en las variables, definamos qué son las palabras clave en Java.

### Palabras Clave en Java

Una palabra clave es una palabra reservada en Java que tiene un significado específico definido por el lenguaje de programación. Estas palabras no se pueden usar como identificadores, como nombres de variables, nombres de métodos u otros identificadores. Son sensibles a mayúsculas y minúsculas, lo que significa que `int`, `Int` y `INT` se consideran diferentes.

Ejemplos de palabras clave en Java incluyen:
- **Tipos de Datos Primitivos:** `int`, `double`, `char`, `boolean`
- **Declaraciones de Control:** `if`, `else`, `while`
- **Modificadores:** `public`, `private`, `final`
- **Otros:** `this`, `super`, `null`

Cada palabra clave cumple un propósito específico en Java, desde definir tipos de datos hasta controlar el flujo del programa.

## Comprensión de las Variables

### ¿Qué son las Variables?

Las variables son ubicaciones de almacenamiento nombradas en la memoria, donde los programadores pueden almacenar, modificar y recuperar datos. Se definen con un tipo de dato específico, que dicta el tipo de datos que la variable puede contener y las operaciones que se pueden realizar sobre ella.

#### Almacenamiento de Variables en Memoria

En Java, entender cómo se almacenan las variables en la memoria es crucial para gestionar eficientemente los recursos y optimizar el rendimiento del programa.

##### Stack y Heap en Java

Java utiliza principalmente dos áreas de memoria para almacenar datos durante la ejecución del programa: el Stack y el Heap.

- **Stack:** Esta área de memoria almacena variables primitivas y las referencias a objetos. Las variables almacenadas en el stack son temporales y se eliminan una vez que se completa la ejecución del bloque de código o la función donde se declaran.

- **Heap:** Aquí es donde se almacenan todos los objetos creados, así como las instancias de clases. A diferencia del stack, el heap no libera automáticamente los objetos una vez que la función termina, lo cual está manejado por el Garbage Collector de Java, que es un proceso que automatiza la gestión de la memoria eliminando objetos que ya no son accesibles.

##### Variables Primitivas vs. Referencias a Objetos

- **Variables Primitivas:** Cuando declaras una variable primitiva, Java almacena el valor directamente en la memoria del stack. Por ejemplo:

  ```java
  int numero = 30;  // Almacenado directamente en el stack.

#### Ejemplo de Declaración y Asignación de Variables

Para declarar y asignar una variable entera llamada `edad`, puedes usar el siguiente código Java:

```java
int edad;       // Declaración
edad = 25;      // Asignación
```

# Tipos de Datos en Java

Java soporta varios tipos de datos primitivos que incluyen:

- **Enteros:** `int`, `long`
- **Números de punto flotante:** `float`, `double`
- **Caracteres:** `char`
- **Booleanos:** `boolean`

Elegir el tipo de dato correcto es crucial, ya que impacta el rendimiento y la precisión de tu programa. Por ejemplo, usar un tipo de dato entero para representar un valor decimal puede resultar en pérdida de precisión.

## Tipos de Datos Objeto

Además de los tipos de datos primitivos, Java también soporta tipos de datos objeto, que son variables que hacen referencia a objetos. Los objetos son estructuras de datos complejas que contienen datos (atributos) y comportamiento (métodos).

## Trabajando con Variables en JShell

JShell, el entorno de programación interactivo de Java, te permite definir, modificar y visualizar variables fácilmente.

### Definiendo Variables en JShell

Para definir una variable entera llamada `edad` con un valor de 25 en JShell, usarías:

```java
int edad = 25;
```

### Usando Variables
Una vez que una variable está definida, puedes usarla refiriéndote a su nombre. Por ejemplo, para imprimir el valor de edad:

```java
System.out.println(edad);  // Muestra: 25
```

### Modificando Variables
Puedes cambiar el valor de una variable en cualquier momento usando el operador de asignación (=):

```java
edad = 30;  // Ahora, edad es 30
System.out.println(edad);  // Muestra: 30
```

## Ejercicio Práctico
Aplica lo aprendido. Intenta cambiar el valor de una variable entera miEdad de 30 a 65 y luego imprime el nuevo valor usando JShell.

```java
int miEdad = 30;         // Declara y asigna `miEdad`
miEdad = 65;             // Modifica `miEdad`
System.out.println(miEdad);  // Imprime el valor de `miEdad`
```