# Variables y Expresiones en Java

## Introducción

En esta lección, continuaremos explorando el uso de variables en Java, enfocándonos especialmente en cómo almacenamos datos en ellas y cómo podemos utilizarlas para manejar expresiones matemáticas complejas.

## Trabajando con Expresiones Matemáticas

Las expresiones matemáticas en Java permiten realizar cálculos y almacenar los resultados en variables. Veamos un ejemplo práctico que ilustra cómo se puede almacenar el resultado de una expresión en una variable.

### Ejemplo de Expresión Literal

Consideremos la siguiente expresión:

```java
int literalVariable = (20 / 2) + (10 + 2);
```

En esta expresión, utilizamos operadores de división (/) y suma (+). En Java, el operador de división devuelve un resultado de punto flotante incluso si ambos operandos son enteros, a menos que se utilice de manera que el contexto requiera un entero. Las paréntesis en la expresión se utilizan para especificar el orden en el que deben realizarse las operaciones. Por lo tanto, la expresión se evalúa de la siguiente manera:

1. Lo que hay en el interior de los paréntesis se evalúan primero. 
2. Dentro de los paréntesis, las multiplicaciones y diisiones se calculan primero. Situviéramos un paréntesis de esta maner (2*3+4/2), primero tendríamos que calcular 2 * 3 y 4/2 y luego hacer la suma. Por lo que en este ejemplo, como sólo tenemos 1 operación dentro de cada paréntesis, el orden es hacer dicha operación.
2. Si después de calcular los paréntesis, no hay divisiones / multiplicaciones, se tiende a calcular de izquierda a derecha, aunque dadas las propiedades de la suma, el orden no altera el resultado. 

El resultado será 22 que se asignará a ```literalVariable```

## Uso de JShell para Probar la Expresión
Podemos usar JShell para definir la variable y ver el resultado:


```int literalVariable = (20 / 2) + (10 + 2);
System.out.println(literalVariable);  // Esto imprimirá: 22
```

## Operaciones con Variables
Ahora, vamos a crear una nueva variable y realizar operaciones adicionales con ella.

### Creación y Uso de Variables Adicionales

```int secondVariable = 50;
int sum = literalVariable + secondVariable;  // Sumamos `literalVariable` y `secondVariable`
System.out.println(sum);  // Esto imprimirá: 72
```

### Modificación de Variables
Supongamos que queremos modificar el valor de secondVariable multiplicándolo por tres:

```secondVariable = secondVariable * 3;  // Multiplicamos el valor por 3
sum = sum + secondVariable;  // Añadimos el nuevo valor de `secondVariable` a `sum`
System.out.println(sum);  // Esto imprimirá: 222
```