### ¿Qué es una Clase en Java?

Es una plantilla que define la forma de un **objeto**, aquí se especifican datos, es decir, `atributos` y `métodos`.

![](../images/01-POO-clase.PNG)


1. **Atributos**: Son las características de una clase.
2. **Métodos**: Son las acciones que la clase puede hacer.

``` java
public class Perro {

    // Atributos de la clase Perro
    String nombre = "Elias";
    String raza = "Shiba Inu";
    double alturaCm = 70.5;


    // Método de la clase Perro
    public void comer(){
        System.out.print("El perro puede comer");
    }

    public void dormir(){
        System.out.print("El perro duerme");
    }

    public void ladrar(){
        System.out.print("El perro ladra");
    }

}
```



### ¿Qué es un Objeto en Java?

Este es una **`instancia`** de una clase, es decir, tiene su realidad física, posee sus `atributos` y `métodos`.

``` java
Perro perro = new Perro();

```