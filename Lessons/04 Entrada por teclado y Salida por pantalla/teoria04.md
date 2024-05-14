## Entrada por teclado y salida por pantalla (I/O)

Java tiene 3 streams (flujos) de entrada y de salida:

1) **Entrada estándard (standard input stream)**. Por defecto se refiere al teclado, aunque se puede redigir a otra fuente de entrada, como por ejemplo, un fichero de texto. Para acceder a este flujo usaremos ```System.in```
2) **Salida estándard (standard output stream)**. Por defecto Java utiliza la pantalla de la consola como salida, pero se puede cambiar, por ejemplo, a un fichero de texto. Para acceder a este flujo usaremos ```System.out```
3) **Salida de error (error output stream)** Este stream se utiliza para mostrar mensajes de error o con información importante. Por defecto, se utiliza la pantalla de la consola, pero también es frecuente redirigirlo haca un fichero .log. Para acceder a este flujo usaremos ```System.err```

La clase ```System``` de API Java nos proporciona acceso a 3 atributos públicos y estáticos llamados ```in``` , ```out``` , ```err``` . Tanto ```System.in``` como ```System.out``` y ```System.error``` son instanciados e inicializados automáticamente por la JVM cuando ésta se enciende, así que no hace falta nada para tenerlos disponibles.