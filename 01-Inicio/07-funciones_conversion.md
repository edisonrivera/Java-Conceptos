## Funciones de conversión

Existen diferentes formas de realizar conversiones de datos a primitivos u objetos. Las dos principales son `valueOf()` y `parse()`.

+ `valueOf()`: Este método devuelve un **objeto**.
+ `parse()`: Este método devuelve un **primitivo**.
+ `toString()`: Transforma objetos a cadenas de texto.

Ejemplo:

``` java
public static void main(String[] args) {
    String numero = "45";
    Integer edad = 20;
    Integer numeroInt = Integer.valueOf(numero);
    int primitivoInt = Integer.parseInt(numero);

    System.out.println("Cadena de texto: " + number.toString());
    System.out.println("numeroInt (Objeto): " + numeroInt);
    System.out.println("primitivo (Primitivo): " + primitivoInt);
}
```

Output:

``` 
Cadena de texto: 20
numeroInt (Objeto): 45
numeroPrimitivo (primitivo): 45
```