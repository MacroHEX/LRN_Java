# Aprendiendo Java

Curso de practica de Java, aquí voy a poner mis notas

## Tabla de Contenidos

- [Aprendiendo Java](#aprendiendo-java)
  - [Tabla de Contenidos](#tabla-de-contenidos)
  - [¿Qué es Java?](#qué-es-java)
  - [Prerrequisitos](#prerrequisitos)
  - [Variables](#variables)
    - [Declaración de Variables](#declaración-de-variables)
  - [Referencias](#referencias)
  - [Cadenas](#cadenas)
    - [Métodos Útiles de las Cadenas](#métodos-útiles-de-las-cadenas)
  - [Secuencias de Escape](#secuencias-de-escape)
  - [Arreglos](#arreglos)
    - [La Clase Array](#la-clase-array)
    - [Arreglos Multi-dimensionales](#arreglos-multi-dimensionales)
  - [Constantes](#constantes)
  - [Expresiones Aritméticas](#expresiones-aritméticas)
  - [Operadores de Incremento y Decremento](#operadores-de-incremento-y-decremento)
  - [Casteo](#casteo)
  - [Dando Formato a Números](#dando-formato-a-números)
  - [Recibiendo Datos](#recibiendo-datos)
  - [Flujo de Control](#flujo-de-control)
    - [Operadores de Comparación](#operadores-de-comparación)
    - [Operadores Lógicos](#operadores-lógicos)
  - [Condicional If](#condicional-if)
  - [Operadores Ternarios](#operadores-ternarios)
  - [Switch Case](#switch-case)
  - [Ciclos](#ciclos)
    - [Ciclos For](#ciclos-for)
    - [Ciclos While](#ciclos-while)
    - [Ciclos Do..While](#ciclos-dowhile)
    - [Ciclos For-each](#ciclos-for-each)
  - [Comandos](#comandos)

## ¿Qué es Java?

Java es uno de los lenguajes de programación más populares en el mundo. Con Java puedes realizar varias aplicaciones tanto como de escritorio, web, móviles y sistemas distribuidos.

## Prerrequisitos

Necesitaremos del [Java Development Kit](https://www.oracle.com/java/technologies/downloads/) **(JDK)** para realizar aplicaciones con Java.

## Variables

|    Tipo    |       Bits    |  Rango | Valor por Defecto |
|:----------:|:-------------:|:------:|:-----------------:|
| boolean | 1 | false-true | false |
| char | 16 | \u0000 - \uFFFF | \u0000|
| byte | 8 | -128 - 127 | 0 |
| short | 16 | -32768 - 32767 | 0 |
| int | 32 | -2147483648 - 2147483647 | 0 |
| long | 64 | -9223372036854775808 - 9223372036854775807 | 0 |
| float |32 | ±3.40282347E+38 - ±1.40239846E-45 | 0.0 |
| double | 64 | ±1.79769313486231570E+308 - ±4.94065645841246544E-324 | 0.0 |

### Declaración de Variables

```java

byte edad = 26;
long contadorVistas = 3_123_456L;
float precio = 10.99F;
char letra = 'A';
boolean ejecutando = true;

```

- En java utilizamos ; (punto y coma) al final de cada línea.

- Utilizamos caracteres simples entre comillas simples 'A' y cadenas con comillas dobles "Hola Mundo".

- El tipo entero por defecto es el int. Para representar un valor del tipo long, debemos añadir la letra L al final.

- El tipo flotante por defecto es el double. Para representar un valor del tipo float, debemos añadir la letra F al final.

```java

// Utilizamos dobles barras para realizar comentarios

```

## Referencias

Java cuenta con 8 primitivos, todo lo demás son referencias, estos no almacenan el objeto en la memoria. Almacenan la referencia (o la dirección) del objeto en memoria.

Para utilizar las referencias necesitamos utilizar el operador new. La memoria es liberada aútomaticamente cuando ya no es utilizada.

```java

Date ahora = new Date();

```

## Cadenas

Las cadenas pertecen al tipo por referencia pero no necesitamos utilizar el operador new para asignarles memoria. Podemos declararlo como un primitivo.

```java

String nombre = "Martin";

```

### Métodos Útiles de las Cadenas

La clase String en Java nos provee de varios métodos útiles:

- starsWith("a")
- endsWith("a")
- length()
- indexOf("a")
- replace("a", "b")
- toUpperCase()
- toLowerCase()
  
Las cadenas son inmutables, lo que significa que una vez inicializadas su valor no puede ser alterado. Todos los métodos que modifican a la cadena (como toUpperCase) retornan un nuevo objeto cadena. El original se mantiene inalterado.

## Secuencias de Escape

- \\
- \"
- \n (salto de linea)
- \t (tab)

## Arreglos

Utilizamos los arreglos para almacenar una lista de objetos. Podemos almacenar cualquier tipo de objeto en un arreglo (primitivo o por referencia). Todos los objetos (también llamados elementos) en un arreglo son del mismo tipo.

```java

// Creando e inicializamos un arreglo de 3 elementos
int[] numeros = new int[3];
numeros[0] = 10;
numeros[1] = 20;
numeros[2] = 30;

// Acortado
int[] numeros = { 10, 20, 30 };

```

Los arreglos en Java tienen un tamaño fijo. No se puede añadir ni remover elementos una vez inicializamos el arreglo.

### La Clase Array

Esta clase nos provee con varios métodos útiles para trabajar con los arreglos.

```java

int[] numeros = { 4, 5, 7 };
Arrays.sort(numeros);
String resultado = Arrays.toString(numeros);
System.out.println(resultado);

```

### Arreglos Multi-dimensionales

```java

// Creamos un arreglo 2x3 (dos filas, tres columnas)
int[2][3] matriz = new int[2][3];
matriz[0][0] = 10;

// Acortado
int[2][3] matriz = {
                        {1, 2, 3},
                        {4, 5, 6}
                   };

```

## Constantes

Constantes (también llamadas variables finales) cuentan con un valor fijo. Una vez lo asignamos, no podemos cambiarlo.

```java

final float RATIO_INTERES = 0.04;

```

Por convención, utilizamos LETRAS MAYÚSCULAS para nombrar las constantes. Varias palabras pueden ser separadas con un guión bajo.

## Expresiones Aritméticas

```java

int x = 10 + 3;
int x = 10 - 3;
int x = 10 - 3;
int x = 10 / 3; // retorna un entero
float x = (float)10 / (float)3; // retorna un flotante
int x = 10 % 3; // modulo (resto de la división)

```

## Operadores de Incremento y Decremento

```java

int x = 1;
x++; // Equivalente a x = x + 1;
x--; // Equivalente a x = x - 1;

x += 5; // Equivalente a x = x + 5;

```

## Casteo

En Java disponemos de dos tipos de casteos:

- **Implicito:** que ocurre automaticamente cuando almacenamos un valor en otro tipo mayor o más preciso.
- **Explicito:** lo hacemos manualmente.

```java

// El casteo implicito ocurre cuando intentamos almacenar un valor short
//(2 bytes) en uno int (4 bytes).
short x = 1;
int y = x;

// Casteo explicito

int x = 1;
short y = (short) x;

```

Para convertir una cadena a número, utilizamos uno de los siguientes métodos:

- Byte.parseByte("1);
- Short.parseShort(“1”);
- Integer.parseInt(“1”);
- Long.parseLong(“1”);
- Float.parseFloat(“1.1”);
- Double.parseDouble(“1.1”);

## Dando Formato a Números

```java

NumberFormat moneda = NumberFormat.getCurrencyInstance();
String resultado = moneda.format("123456"); // $123,456

NumberFormat porcentaje = NumberFormat.getPercentInstance();
String resultado = percent("0.04"); // 4%

```

## Recibiendo Datos

```java

Scanner scanner = new Scanner(System.in);
double numero = scanner.nextDouble();
byte numero2 = scanner.nextByte();
String nombre = scanner.next();
Sring linea = scanner.nextLine();

```

## Flujo de Control

### Operadores de Comparación

- x == y // operador de igualdad
- x != y // operador de desigualdad
- x > y
- x >= y
- x < y
- x <= y

### Operadores Lógicos

- x && y // AND
- x || y // OR
- !x // NOT

```java

bool ganaBien = true;
bool tieneBuenCredito = false;
bool tieneAntecedentes = false;

boos esElegible = (ganaBien || tieneBuenCredito) && !esElegible;

```

## Condicional If

Esta es la estructura básica del condicional if. Si vamos a realizar varias acciones debemos utilizar llaves { }.

if (condicion1)
     accion1
else if (condicion2)
     accion2
else if (condicion3)
     accion3
else
     accion4

## Operadores Ternarios

```java

String nombreClase = (gana > 100_000) ? "Primera" : "Economica";

```

Este codigo es una versión acortada del siguiente:

```java

if (gana > 100_000)
     nombreClase = "Primera";
else
     nombreClase = "Economica";

```

## Switch Case

Utilizamos el switch case para ejecutar diferentes partes de un código dependiendo del valor de la variable.

```java

switch (x){
     case 1:
          ...
          break;
     case 2:
          ...
          break;
     case 3:
          ...
          break;
     default:
          ...
}

```

Al final de cada **case** añadimos la línea break para saltar al siguiente bloque.

## Ciclos

### Ciclos For

Los ciclos **for** son utiles cuando conocemos la cantidad de veces que algo va a ser repetido. Declaramos una varaible para contar y en cada iteración la aumentamos hasta que alcancemos a la cantidad de veces que queremos ejecutar el mismo código.

```java

for (int i = 0; i < 5; i++) {
     //codigo
     }

```

### Ciclos While

Los ciclos **while** son utiles cuando no conocemos la cantidad de veces que algo va a ser repetido. Puede ser dependiente de un valor (que el usuario ingresa).

```java

while (unaCondicion){
     ...
     if (unaCondicion)
          break;
}

```

Utilizamos el comando **break** para salir del ciclo.

### Ciclos Do..While

Los ciclos **Do...While** son similares a los **While** pero estos son ejecutados al menos una vez. Al contrario un ciclo while puede no ejecutarse si su condición inicial es falsa.

```java

do {
     ...
} while (unaCondicion);

```

### Ciclos For-each

Los ciclos **ForEach** son utiles para iterar sobre un arreglo o colección.

```java

int[] numeros = {1 , 2, 3, 4, 5};
for (int i numero : numeros)
     ...

```

## Comandos

```java

// Genera el metodo main
psvm -> private static void main (String[] args) {}

// Genera la impresión a pantalla
sout -> System.out.println();
        
```
