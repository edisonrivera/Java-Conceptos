## Input y Output en Java

Aprenderemos a enviar, mostrar y solicitar datos al usuario.

#### Output

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

***

#### Input
Para recoger los datos ingresados por el usuario importaremos una utilidad de Java

``` java
import java.util.Scanner;
``` 

Y para usarlo instanciaremos la clase `Scanner`, es decir, crearemos un **objeto**.

``` java
import java.util.Scanner;

public static void main (String[] args){
	Scanner scanner = new Scanner(System.in);
} 
``` 

Cada dato de entrada se debe leer de una manera diferente, no podemos leer un **número entero** como si fuese un **String**.

``` java
import java.util.Scanner;

public static void main (String[] args){
	Scanner scanner = new Scanner(System.in);
    // Leemos un dato de tipo int
    int numeroUsuario = scanner.nextInt();

    // Leemos un dato de tipo String
    String nombre = scanner.nextLine();

    // Leemos una dato de tipo double
    double decimal = scanner.nextDouble();
} 
``` 