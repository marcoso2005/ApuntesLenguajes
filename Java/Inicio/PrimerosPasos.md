# Primeros pasos en Java
En este documento se explicarán las principales estructuras de Java para realizar pequeños programas.

## Pintar datos por pantalla
Para pintar datos por pantalla lo que realizaremos será indicar por donde lo queremos pintar, que consola y de que forma. En nuestro caso utilizaremos la salida `System` que indica que será la salida por defecto del sistema, `out` para utilizar la salida normal o `err` para mostrar mensajes de error.

```Java
System.out.println("mensajito");
```
Como formas de pitnar disponemos de:
- `print`: pinta un mensaje.
- `println`: pinta un mensaje y añade un salto de linea al final.
- `printf`: pinta mensajes con formato.

Dentro de estos mensajes, podemos implementar diferentes comandos especiales:
- `\n`: introduce un salto de linea.
- `\t`: introduce una tabulacion.
- `\\`: pone una \ como texto.
- `\"`: pone " como texto.
- `\r`: introduce un retorno de carga.
- `\b`: realiza un retroceso (mueve el cursor una posición atras).

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

#### **Operar con variables**
Para crear un variable nueva, indicaremos el tipo de dato seguido del nombre, opcionalmente podemos indicar en este momento el valor del dato con un =.

```Java
int numero = 5;
```

En los tipos numericos podemos incrementar o decrementar los valores de un dato de tipo numerico, podemos usar ++ o --. Si el simbolo se encuentra delante del nombre de la variable `++numero` primero se incrementa y posteriormente se realizan las acciones, mientras que si lo ponemos detras `numero++` primero se realizan las acciones y luego se suma.

Tomando como ejemplo la variable anterior:
```Java
System.out.println(++numero) //Sumaría 1 y luego pintaria el numero 6
System.out.println(numero++) //Pintaría el numero 5 y luego le sumaría uno
```

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
### Switch
Como condiciones en Java tambíen disponemos de otro tipo de condicional llamada `switch`, esta lo que hace es comparar una variable con distintos valores y realiza una seccion de codigo u otro dependiendo de con cual concuerde.
```Java
switch (var) {
    case 1:
        //Codigo si var = 1            
        break;
    case 2:
        //Codigo si var = 2
        break;
    default:
        //Codigo si no se cumple ningun caso
}
```
## Bucles
Un bucle es una sección de codigo que va a repetirse un numero n de veces.

En Java disponemos dos tipos de bucles diferentes:
- `for`
- `while`
  
#### ***For***
La instrucción for se utiliza para crear bules cuando **SI** sabemos el número de iteraciones "vueltas" vamos a dar.

La instruccion esta formada por la palabra for y luego entre parentesis, crearemos una variable de tipo integer; hasta donde va a llegar esta nueva variable; cuanto vamos a incrementar/decrementar la variable en cada vuelta.

```Java
for (int i = 0; i < n; i++) {
    //Codigo a ejecutar en cada iteracion
}
```
#### ***While***
Ademas de la instruccion for, disponemos de la instruccion `while` que se utilizará cuando *NO* sabemos cuantas iteraciones vamos a realizar.
Tenemos dos formas de hacerlo:
La primera comprobaría si la condición se sigue ejecutando y posteriormente (en caso de que se cumpla) se ejecutaría el codigo
```Java
while(n<a){
    //Codigo a ejecutar
}
```
La segunda forma nos asegura que siempre se va a ejecutar minimo una vez el codigo, ya que primero ejecuta y despues comprueba la condición
```Java
do{
    //Codigo a ejecutar
}while(n<a)
```

hola buenos dias