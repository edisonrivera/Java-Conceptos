### Variables 

``` java
    public static void main(String[] args) {
        int valorEntero = 15; 
        boolean band = true;
        String nombre = "Estela";
        byte x = 127; // Hasta 127 o -127
        float flotante = 1.01f;
        double doble = 14.5454545;
        char simbolo = '@';

        System.out.print("Entero: " + valorEntero + "\n" + 
        "Bool: " + band + "\n" + "String: " + nombre + "\n" +
        "Byte: " + x + "\n" + "Float: " + flotante + "\n" + 
        "Double:" + doble + "\n" + "Char: " + simbolo + "\n");
    }
```

**Output:**

```
Entero: 15
Bool: true
String: Estela
Byte: 127
Float: 1.01
Double:14.5454545
Char: @
```

---

### Clase Wrapper

Crea un **contenedor** (espacio en memoria), para el tipo de variables vistas en la parte superior **variables primitivas**.

Ventajas de usar **Clases Wrapper**:
1. Mejora el rendimiento del programa.
2. Proporciona métodos útiles.

Ejemplo:

``` java
 public static void main (String[] args){
             
        Boolean band = false;
        Character simbolo = '@';
        Integer numero = 45;
        Double decimal = 46.5;
        String nombre = "Estela";

        System.out.println(band.compareTo(false)); // 0 -> true; -1 -> false
        System.out.println(simbolo.charValue());
        System.out.println(numero.toString()); // int -> String
        System.out.println(decimal.hashCode()); 
        System.out.println(nombre.length()); // longitud
    }
```
+ Una clase Wrapper siempre comienza con una mayúscula.
+ Proporciona métodos útiles que los datos primitivos no poseen.

Output:
``` 
0
@
45
1078411264
6
``` 


Existen 2 conceptos más `Autoboxing` y `Unboxing`.
+ **AutoBoxing**: Conversión automática de un tipo de **dato primitivo** a un **objeto**.

Ejemplo:

``` java
    public static void main(String[] args) {
        int primitivo = 500;
        Integer wrapper = primitivo;
        System.out.println("Primitivo: " + primitivo);
        System.out.println("Objeto: " + wrapper);
    }
```

Output:

```
Primitivo: 500
Objeto: 500
```

+ **Unboxing**: Conversión de un **objeto** a un **dato primitivo**

``` java
    public static void main(String[] args) {
        List<Integer> numeros = new ArrayList<Integer>();
        numeros.add(25);
        int numeroPrimitivo = numeros.get(0);
        System.out.println("Numero Objeto: " + numeros.get(0));
        System.out.println("Numero Primitivo: " + numeroPrimitivo);
    }
```

Output:

```
Numero Objeto: 25
Numero Primitivo: 25
```