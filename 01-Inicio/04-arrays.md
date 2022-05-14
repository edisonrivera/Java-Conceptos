### Listas

1. Pueden ser solo de un solo tipo de datos.
2. Pueden tener una tamaño definido o ir creciendo dinámicamente.

``` java
    public static void main (String[] args){

        String tiposDeComida[] = {"Frita", "Al vapor", "Saludable"};
        System.out.println("Tipos de Comida");

        for (int i=0; i < tiposDeComida.length; i++){
            System.out.println(i + ".-> " + tiposDeComida[i]);
        }

        // Arrays "quemadas"
        String[] marcaAutos = new String[3];
        marcaAutos[0] = "Mazda";
        marcaAutos[1] = "Toyota";
        marcaAutos[2] = "Mercedes Benz";  
    }
```

---

### Arrays

1. Son mucho más fáciles de manipular.
2. Cuentan con métodos útiles.
3. Crecen dinámicamente.

Algunos de los métodos más útiles son:

+ `add([elemento])` -> añadir elementos al array.
+ `size()` -> Longitud del array.
+ `get([index])` -> Conseguimos el elemento de dicha posición. 
+ `set([index], [nuevo elemento])` -> Reemplaza un elemento.
+ `remove([index])` -> Elimina un elemento.
+ `clear()` -> Limpia el arrayList.

Para usar un array debemos importar una utilidad

``` java
import java.util.ArrayList;
```
> Esto nos permitirá usar arrays sin ningún incoveniente.

Ejemplo:
``` java

    public static void main (String[] args){
        ArrayList<String> food = new ArrayList<String>();   
        food.add("Pizza");       
        food.add("Hamburguer");  
        food.add("Hot-Dog");      

        for (int i = 0; i < food.size(); i++){
            System.out.println(i + ".-> " + food.get(i));
        }
        System.out.println(food);

    }
```

Output:

``` 
0.-> Pizza
1.-> Hamburguer
2.-> Hot-Dog
[Pizza, Hamburguer, Hot-Dog]
```

---

### Arrays Bidimensionales

Para esto al sintaxis se puede volver un poco compleja, pero nada imposible.

``` java
ArrayList<ArrayList<String>> arrayBidimensional = new ArrayList<ArrayList<String>>();
```

Ejemplo:
``` java
public static void main (String[] args){
    ArrayList<ArrayList<String>> variateList = new ArrayList<ArrayList<String>>();
        
    ArrayList<String> foodList = new ArrayList<String>();   
    foodList.add("Pizza");       
    foodList.add("Hamburguer");   
    foodList.add("Hot-Dog");

    ArrayList<String> autosList = new ArrayList<String>();   
    autosList.add("Mazda");       
    autosList.add("Toyota");   
    autosList.add("Honda");

    variateList.add(foodList);
    variateList.add(autosList);

    for (int i = 0; i<variateList.size();i++){
        System.out.println("Lista N." +  i + " -> " + variateList.get(i));
    }
}
``` 

Output:
```
Lista N.0 -> [Pizza, Hamburguer, Hot-Dog]
Lista N.1 -> [Mazda, Toyota, Honda]
```

Para poder acceder a un elemento específico de un array bidimensional lo haremos de la siguiente forma:

Supongamos que tenemos este array bidimensional:
```
[["Pizza","Hamburguer","Hot-Dog"],
 ["Mazda","Toyota","Honda"]]
```

Ahora, nosotros queremos acceder al elemento **"Toyota"**


En términos de código se haría así:
``` java
System.out.println(variateList.get(1).get(1))
```

+ El primer **get** se usar para especificar una lista dentro del array bidimensinal y el segundo **get** especifica el elemento dentro de la lista anterior.

Es decir, en el ejemplo nosotros accedemos primero a la segunda lista con `get(1)` y posterior a eso accedemos al elemento "Toyota" con `get(1)`.

Output:
```
Toyota
```