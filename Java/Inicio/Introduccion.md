# Introduccion
En este documento se explica que es el lenguaje de programación Java y algunos terminos importantes del mismo.
## ¿Que es java?
Java es un lenguaje de programación de alto nivel y una plataforma informática de software orientada a objetos.
## ¿Que es un objeto?
Un objeto es un componente software que:
- Puede recibir **mensajes** y responder a los mismos.
- Tiene **identidad**.
- Tiene un **estado**.
- Tiene un comportamiento bien **definido**.
## Características de la POO
La POO se basa en el uso de las siguientes capacidades primarias:
- Abstraer.
- Encapsular.
- Modularizar.
- Jerarquizar.
  
También se pueden considerar estas capacidades secundarias:

- Tipo.
- Persistencia.
- Concurrencia.

## Abstracción
### ¿Qué es?
Abstraer es la capacidad que permite distinguir aquellas **características fundamentales** de un objeto que lo hacen diferente del resto, y que proporcionan **límites conceptuales** bien definidos relativos a la perspectiva del que lo visualiza.

Al estudiar algo **ignoramos los detalles**, y tratamos con ideas generales de un **modelo simplificado** de ese algo.

### Claidad de la abstración
Para ayudar a crear abstracciones se puede medir su calidad revisando los siguientes aspectos: 
- **Acoplamiento**: minimizar el grado de asociación entre diferentes abstracciones. Dos abstracciones están acopladas cuando para tener una también hay que tener la otra. 
- **Cohesión**: maximizar el grado de asociación dentro de una abstracción. Hay cohesión cuando los métodos de una abstracción tienen una temática común, trabajan con tipos similares... 
- **Suficiencia** y **completitud**: que tenga las características precisas para permitir un funcionamiento eficiente y completo. No le faltan métodos para cumplir su objetivo. 
- **Primitividad**: las operaciones de una abstracción deben ser lo más básicas posibles. No debe tener operaciones que ya se pueden construir con otras más básicas.

## Encapsulación
### ¿Qué es?
Encapsular es la capacidad que permite **mantener oculta la implementación** de una abstracción para los usuarios de la misma.

El objetivo de encapsular es el de **evitar que un sistema dependa de cómo se ha implementado otro**. Esto **facilita que los clientes no perciban cambios internos** en la implementación de una abstracción.

Otro objetivo de **ocultar una parte de la implementación** frente a un cliente es el de **evitar que el cliente rompa los invariantes**. de la abstracción.

## Jerarquía
### ¿Qué es?
Jerarquizar es una capacidad que permite **ordenar abstracciones**.

La organización de las abstracciones en jerarquías permite **detectar estructuras y comportamientos comunes**, simplificando el desarrollo.

En el esquema de programación orientada a objetos se definen dos formas básicas de jerarquías:
- Jerarquías entre **objetos**.
- Jerarquías entre **clases e interfaces**.
### Tipos
Las jerarquías entre objetos se pueden clasificar en 2 tipos de relaciones:
- Relaciones de **asociación**: establecen relaciones del tipo “tal objeto **contiene** a tal otro objeto”.
- Relaciones de **dependencia** o **uso**: dan lugar a relaciones del tipo “tal objeto **usa** tal otro objeto”
### Polimorfismo
El polimorfismo es un concepto básico de la programación orientada a objetos (POO) que permite tratar a los objetos como instancias de su clase padre. Facilita la flexibilidad y la capacidad de definir métodos de múltiples formas. El polimorfismo se consigue principalmente mediante la sobreescritura y la sobrecarga de métodos.

Es decir permite generar estructuras de almacenamiento de la calse padre, la cual va a almacenar elementos de los hijos independientemente de su clase:
```
Disopngo de la clase coche de la cual heredan mercedes y audi, puedo generar uan variable de tipo coche y alamacenar independientemente una variable de tipo mercedes o audi y utilizar todos los metodos que contenga la clase coche.
```
## Modularidad
### ¿Qué es?
La modularidad es la capacidad que permite dividir un programa en **agrupaciones lógicas** de sentencias llamadas **módulos**.

### Niveles
En Java disponemos de varios niveles de modularidad: 
- Al menor nivel cada módulo se corresponde a un **fichero**. Así, los ficheros se pueden escribir y compilar de manera separada. 
- Las bibliotecas aportan un segundo nivel de modularidad a C++. Mientras, en otros lenguajes, como Java, se ha creado el concepto de **paquete** que permite un número ilimitado de niveles de modularidad aprovechando el concepto de directorio. 
- También suele utilizarse el concepto de **componente** y de programa como módulos que tienen una funcionalidad completa e independiente.

### Ventajas
Las ventajas que ofrece la modularidad son: 
- Facilidad de **mantenimiento, diseño y revisión**. Al dividir el programa se facilita que varias personas puedan desarrollar de manera simultánea e independiente conjuntos disjuntos de módulos. 
- Aumento de la **velocidad de compilación**. Los compiladores suelen compilar por módulos. Esto significa que el cambio de un módulo solo implica la recompilación del módulo y de los que dependan de él, pero no la del total de módulos. 
- Mejora en la **organización y en la reusabilidad**, ya que es más fácil localizar las abstracciones similares si se encuentran agrupadas de una manera lógica.

### Como diseñar modulos
A la hora de diseñar los módulos debe tenerse en cuenta: 
- Maximizar la **coherencia**. Agrupar en un mismo módulo las abstracciones relacionadas lógicamente. 
- Minimizar las **dependencias** entre módulos. Que para compilar un módulo no se necesite compilar muchos otros. 
- Controlar el **tamaño** de los módulos. Módulos pequeños aumentan la desorganización, módulos muy grandes aumentan los tiempos de compilación y reducen su manejabilidad.

## Tipado
Un tipo es una **caracterización precisa asociada a un conjunto de datos**. La asociación del tipo a un dato se conoce como tipado.
El tipado refuerza las decisiones de diseño, impidiendo que se **confundan abstracciones** diferentes y dificultando que puedan utilizarse abstracciones de maneras no previstas.
En lenguajes como Java, **cada abstracción define un tipo**.

### Clasificación
El tipado de un lenguaje se puede clasificar como:
- Débil o fuerte.- Si se puede, o no, cambiar el tipo de un dato.
- Explícito o implícito.- Si hay que declarar el tipo de las variables o no.
- Estático o dinámico.- Si conociendo el tipo de una variable se puede deducir qué código se ejecutará o no.

## Concurrencia
La concurrencia es la capacidad que permite la **ejecución simultánea de varias secuencias** de instrucciones. La concurrencia permite que un programa tenga varios puntos de **ejecución simultáneamente**. 

Clásicamente, los lenguajes de programación no daban soporte a la concurrencia sino que era proporcionada por los **sistemas operativos**. 

En Unix la concurrencia se consigue con la invocación de una función del sistema operativo llamada **fork** que divide la línea de ejecución, creando múltiples líneas de ejecución (también conocidas como hilos o threads).

## Persistencia
La persistencia es la capacidad que **permite que la existencia de los datos trascienda en el tiempo y en el espacio**.

En relación con su tiempo de vida, los datos se pueden catalogar en:
- **Expresiones**, con una vida inferior al de una línea de código.
- **Variables locales**, cuya vida se circunscribe a una función.
- **Variables globales**, que viven mientras se ejecuta un programa.
- Datos que persisten de una **ejecución** a otra.
- Datos que sobreviven a una **versión** de un programa.
- Datos que sobreviven cuando ya **no existen** los programas, sistemas operativos e incluso ordenadores que los crearon. 

Los lenguajes de POO suelen dar soporte a todos usando ficheros y bases de datos.

