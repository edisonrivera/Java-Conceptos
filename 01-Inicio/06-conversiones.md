## Conversiones

Se dividen en dos tipos **implícitas** y **explícitas**.


+ `Implicitas`: No necesitan declaración de sintaxis extra.

Ejemplo:

``` java
    public static void main(String[] args) {
        int numero = 451;
        float flotante = numero;
        System.out.println("Numero (int): " + numero);
        System.out.println("Flotante (float): " + flotante);
    }  
```

Output:
```
Numero (int): 451
Flotante (float): 451.0
```

---

+ `Explícitas`: Necesitan una declaración de sintaxis.

Ejemplo:

``` java
public static void main(String[] args) {
    int numero = 127;
    byte numeroByte = (byte) numero;
    System.out.println("Numero (int): " + numero);
    System.out.println("Byte (byte): " + numeroByte);
} 
```

Output:

```
Numero (int): 127
Byte (byte): 127
```