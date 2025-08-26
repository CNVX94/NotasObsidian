  #Java  #Programacion

1. Una vez que en consola obtenemos algo como esto:
```c
PS C:\Users\PC> java --version
java 24.0.1 2025-04-15
Java(TM) SE Runtime Environment (build 24.0.1+9-30)
Java HotSpot(TM) 64-Bit Server VM (build 24.0.1+9-30, mixed mode, sharing)
```

Podemos entonces proceder a realizar nuestro primer archivo .java.

2. Realizar una carpeta para el proyecto, añadir el archivo "HolaMundo.java".
3. El código es básico, debe de verse algo así.


```java
public class holamundo {

    public static void main(String[] args) {

        System.out.println("¡Hola, mundo!");

    }

}
```

4. Una vez guardado, debemos de escribir en la terminal:


```bash
PS C:\Users\PC\Documents\TryJava> javac holamundo.java 
PS C:\Users\PC\Documents\TryJava> java holamundo.java  
¡Hola, mundo!
```

5. Como puedes observar, una clase ha sido creada, esto es para facilitar el trabajo a java y pueda compilar rápidamente el código posteriormente, además de que así se asegura de saber que está haciendo correctamente el trabajo.
6. Para observar el código, siempre y cuando estés realizando de manera correcta el llamado a un texto o un procedimiento, entonces ejecuta el archivo ".java" con "java archivo.java" en lugar de con "javac" recordando que este es primero para compilar y crear la clase.