## Excepciones

Nos sirven para controlar de mejor manera errores que se pueden presentar en el flujo del programa, ya sea por un mal uso de parte del usuario o un error en la codificación.

Esquema de una excepcion:

``` java
try{
    // Operaciones a "intentar"
} catch ("Tipo de excepcion") {
    // Mensajes de error
} finally {
    // Este mensaje se muestra siempre
}
```

+ Bloque **try**: Ejecutará las operaciones que queremos "intentar".
+ Bloque **catch**: Nos informará acerca del error.
+ Bloque **finally**: Se ejecutará independiente de la operación anterior.

---

Tipo de errores más comunes:
+ `ArithmeticExpection`: Errores sobre operaciones matemáticas.
+ `InputMismatchException`: Errores sobre tipos de datos no permitidos.
+ `Exception`: Captura todo tipo de errores.

---

1. `ArithmeticExpection`

``` java
public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    try{
        System.out.print("Dividendo: ");
        int x = scanner.nextInt();
        
        System.out.print("Divisor: ");
        int y = scanner.nextInt();

        int resultado = x/y;
        System.out.println("El resultado es : " + resultado);
            
    } catch (ArithmeticException e) {
        System.out.println("Math ERROR ");
    } finally {
        System.out.println("Este fue todo el proceso");
        scanner.close(); 
    }
}
```

Output:

```
Dividendo: 4
Divisor: 0
Math ERROR 
Este fue todo el proceso
```

---

2. `InputMismatchException`:

``` java
public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    
    try{
        System.out.print("Dividendo: ");
        int x = scanner.nextInt();
        
        System.out.print("Divisor: ");
        int y = scanner.nextInt();

        int resultado = x/y;
        System.out.println("El resultado es : " + resultado);
            
    } catch (InputMismatchException e){
        System.out.println("Ingresar datos válidos");
    } finally {
        System.out.println("Este fue todo el proceso");
        scanner.close(); 
    }
}
```

Output:

```
Dividendo: 4
Divisor: ñ
Ingresar datos válidos
Este fue todo el proceso
```

---

3. `Exception`:

``` java
public static void main(String[] args) {
    Scanner scanner = new Scanner(System.in);

    try{
        System.out.print("Dividendo: ");
        int x = scanner.nextInt();
        
        System.out.print("Divisor: ");
        int y = scanner.nextInt();

        int resultado = x/y;
        System.out.println("El resultado es : " + resultado);
            
    } catch (Exception e){
        System.out.println("Error: " + e);
    } finally {
        System.out.println("Este fue todo el proceso");
        scanner.close(); 
    }
}
```


Output:

```
Dividendo: f
Error: java.util.InputMismatchException
Este fue todo el proceso
```