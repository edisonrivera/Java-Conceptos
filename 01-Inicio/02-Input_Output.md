## Input y Output en Java

Aprenderemos a enviar, mostrar y solicitar datos al usuario.

#### Input

Existen tres tipos de formas de poder mostrar datos por pantalla:

``` java
System.out.println();
System.out.print();
System.out.printf();
```

1. `System.out.println()`: Realiza un salto de línea `(\n)` de forma automática.

``` java
System.out.println("Hola mundo");
System.out.println("Siguiente Línea");
``` 

**Output**:
```
Hola mundo
Siguiente Línea
```
---

2. `System.out.print()`: No realiza el salto de línea.
``` java
System.out.print("Hola,");
System.out.print("Mundo");
``` 

**Output**:
``` 
Hola,Mundo
``` 

---

3. `System.out.printf()`: Permite modificar de mejor manera la salida de datos.

``` java
boolean band = true;
char simbolo = '@';
String nombre = "Estela";
int numero = -324;
double decimal = 14444.324324;

    /*
    %s -> String.
    %d -> int.
    %b -> boolean.
    %c -> char.
    %f -> double.
    */

System.out.printf("%b", band);
System.out.printf("%c", simbolo);
System.out.printf("Hola %10s", nombre); //%[numero]s or %-[numero]s
System.out.printf("%010d", numero); // Reemplaza los espacios puestos por 0
System.out.printf("%.2f", decimal); //%.[numero de decimales]f
System.out.printf("%,f", decimal);
System.out.printf("%+f", decimal); //Añade en símbolo
``` 