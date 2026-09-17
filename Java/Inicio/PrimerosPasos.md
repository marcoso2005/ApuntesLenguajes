# Primeros pasos en Java
En este documento se explicarán las principales estructuras de Java para realizar pequeños programas.
## Tipos de datos
En los lenguajes de programación disponemos de varios tipos de datos que son los que se utilizan para crear las diferentes variables de nuestros programas.

En Java estos se clasifican en dos tipos diferentes:
- Primitivos.
- Referenciados.

### Tipos primitivos
Los tipos primitivos son aquellos que guardan un valor simple directamente en **memoria** es decir **NO** son objetos.

Estos son:
- Enteros
  - byte (1 byte)
  - short (2 bytes)
  - **integer** (4 bytes)
  - long (8 bytes)
- Decimales
  - float (4 bytes)
  - **double** (8 bytes)
- Caracteres
  - **char** (2 bytes)
- Booleano
  - **boolean** (1 bit)

### Tipos estructurados
Almacenan referencias u objetos en memoria. En este caso tendríamos todos los objetos que creemos nosotros mas adelante. Un ejemplo de este tipo de datos es **String**.


## Condiciones
Una condición es una regla o expresión lógica que se evalúa como verdadera (**true**) o falsa (**false**).

En Java disponemos principalmente de dos estructuras para realizar condicionales:
- `if`
- `switch`

### IF
La condición if sirve para evaluar una expresíon como verdadera o falsa, en caso de ser verdadera, se realizará una accion.
```Java
if(condicion){
    //Codigo
}
```
En caso de que no se cumpla la condición queramos que se realize un codigo diferente, podemos utilizar else.

Esta seccion del codigo se ejecutará cuando no se cumplan las condiciones del if.
```Java
if(condicion){
    //Codigo si condicion verdadera
}else{
    //Codigo si condicion falsa
}
```
Además podemos realizar varios if seguidos antes de realizar el else, esto se llama else if.
```Java
if(condicion1){
    //Codigo si condicion1 verdadera
}else if(condicion2){
    //Codigo si condicion2 Verdadera
}else{
    //Codigo si condicion falsa
}
```
#### ***Concatenar condiciones***
Dentro de la condición de un if podemos concatenar varias intruciones mediante AND (**&**) y or (**|**).

En el caso del and, para que se cumpla la condicion deben cumplirse **ambas condiciones**.

Mientras que en el caso del or, solo es necesario que se cumpla **una condición**.

```Java
if(condicion1 && condicion2){
    //Codigo si se cumplen la condicion1 Y la condicion2
}else if (condicion1 || condicion2){
    //Codigo si se cumple condicion1 O condicion2
}else if((condicion1 && condicion2) | condicion3){
    //Codigo si se cumple la condicion1 Y la condicion2 O si se cumple la condicion3
}else{
    //Codigo si no se cumple ninguna condicion
}
```