#Git 

	Las ramas una vez creadas pueden ser utiles o deshechables para el proyecto, por lo que es útil saber los diferentes casos que podemos tener dependiendo nuestra situación de trabajo:

## Fast-Forward

	Este tipo de unión en ramas es útil siempre y cuando se haya estado desarrollando en la rama y no exista conflicto con la rama principal, por ejemplo, que alguien paralelo a nuestros ultimos commits en la rama master haya desarrollado algunas funciónes de manera distinta mientras nosotors desarrollabamos en la rama master.
	O también siempre y cuando nosotros hayamos solo hecho midificaciones en la rama y no en el main.

	Este comando debe hacerse desde la rama que espera los cambios, es decir, en la rama "Main" si queremos agregar el contenido de la rama que hemos avanzado.

	De otra manera, nosotros traeriamos los cambios hechos en "Main" a nuestra rama, lo cual puede ser util después pero en la mayoría de casos no exactamente.

```bash
git merge nombrerama
```

	El caso "Fast-Forward" es cuando se ha logrado sin mayor inconveniente y git ha logrado mezclar las ramas.

## Unión Automática

	Exponiendo el caso anterior, en caso de tener cambios en la rama main, y desarrollo en la branch, si queremos hacer una unión de cualquier lado, git nos dará un aviso de los cambios que se están llevando a cabo y nos pedira que de preferencia especifiquemos en el commit la razón de esta mezcla, en el sub menu debemos agregar ese cambio y salir con ":wq!"

## Conflictos

	Si en el caso anterior las modificaciónes han sido en la misma linea o Git considera que se esta sobreponiendo y no sabe cual de los archivos conservar, tendremos un conflicto donde deberemos actuar.
	Visual Studio nos ayudara mostrando la diferencia y razon de conflicto en los archivos, Git solo nos indicará dónde está localizado, deberemos de realizar la comparación y hacer loc}s cambios consideración de sustituir, eliminar o añadir dependiendo de lo que busquemos hacer.
	Una vez haya quedado como esperamos sea lo correcto, a continuación solo deberemos salvar y añadir al stage los cambios, también simplemente hacer un commit recortado que ya lo hace automaticamente, con esto ya tendremos la unión completa con los archivos que hayan sido aceptados a la primera y con nuestra nueva solución.

## Actualizar Ramas

	 Continuamos en:

[[Rebase]]