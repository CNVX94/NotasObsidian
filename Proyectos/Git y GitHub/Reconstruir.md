#Git 

1. Leer "[[Primeros pasos]]" para información de la creación del repositorio y otras instrucciones.
2. Usar la [[Ayuda]] si te sientes perdido.

## Checkout

A través de este comando:

 "Regresar y reconstruir todo el proyecto a como estaba antes."

```bash
git checkout -- .
```

Podremos retronar al ultimo y más actual commit, por lo que es por esto que es importante observar con:

```bash
git log
```

Para saber exactamente a que retornariamos.

Es una herramienta muy útil para recuperar datos después de un cambio o eliminación de un documento.

Podremos observar una "U - Untrack " en cada archivo al que no se le este realizando seguimiento, dado que actualicemos o creemos algún archivo debe considerarse para agregar en el siguiente commit.

Se recomienda evitar archivos de compilación o generación del sistema, también a archivos que contengan "Api Key" o cualquier información sensible de acceso al sistema.  

Seguir en [[Ramas]].