#Git 

	"Actualizamndo una rama"

	Si tuvieramos cambios considerables en la rama main y quisieramos conseguir el trabajo desarrollado sin aplicar nuestros cambios directamente podremos movernos hasta el ultimo commit hecho en la rama main (o la que deseemos ocupar) desde nuestra rama seleccionada.

	En este caso se hizo desde la rama secundaria para poder alcanzar los ultimos commits de la rama master.

## Rebase - Comando

```bash
git rebase master
```

Luego podemos ver si todo está bien en la rama master yendo allá.

```bash
git chekout master
```

Y ahora podemos hacer la unión con la segunda rama.
	Se recomienda consultar: [[Unión de Ramas]]

```bash
git merge ramasecundaria
```

Ahora podemos borrar la rama secundaria

```bash
git branch -d ramasecundaria
```

## Rebase - Squash

> En caso de que la virgulilla "~" no aparezca con "ALT+4" o "ALT GR + 4", puedes usar la combinación de ASCII "ALT+1 2 6" en ese orden.

```bash
git rebase -i HEAD~4
```

Esto indicia que:
1. Usaremos el modo "interactivo"
2. Que apuntamos desde "HEAD" el último commit hecho
3. Que queremos realizar modificaciones hacia 4 commit anteriores.

	En el menú seleccionaremos squash para poder unir y/o chocar commit.

```bash
pick 158ba9e # Ejemplo ignorado
pick 7e0d5fd # Ejemplo ignorado 2
pick cae8960 # Actualizamos x archivo
squash 926674b # Actualizamos archivo completado
```

	Squash o s automaticamente chocará ese commit con el commit anterior.

	No se recomienda usar más de un squash ya que esto haría que por ejemplo, los dos commits ahora con Squash choquen con el ejemplo ignorado con cosas que podrían hacer problemas.

	Saldremos con "ESC", dos puntos ":", "w" para guardar cambios, "q" para salir y "!" para realizar los cambios.

```bash
:wq!
```

	Pasaremos a una pantalla distinta donde so queremos podremos cambiar el nombre o simplemente dejarlo como esta, de nuevo saldremos de la forma común.

	Saldremos con "ESC", dos puntos ":", "w" para guardar cambios, "q" para salir y "!" para realizar los cambios.

```bash
:wq!
```

## Rebase - Reword

	Si solo queremos cambiar un nombre de un commit anterior podemos usar "Reword" accediendo de la misma manera que hicimos antes:

```bash
git rebase -i HEAD~4
```

	Luego en el nuevo menú podremos ver:

```bash
pick 158ba9e # Ejemplo ignorado
pick 7e0d5fd # Ejemplo ignorado 2
pick cae8960 # Actualizamos x archivo
pick 926674b # Actualizamos archivo completado
```

	Y ahora debemos hacerlo algo así, cambiamos pick por r:

>No se debe editar directamente desde el menú.

```bash
pick 158ba9e # Ejemplo ignorado
pick 7e0d5fd # Ejemplo ignorado 2
r cae8960 # Actualizamos x archivo
r 926674b # Actualizamos archivo completado
```

	Ahora desde el menú actualizaremos el nombre y lo correspondiente desde el menú interactivo de la consola.

> De nuevo usaremos "a" para editar, "ESC" para salir, ":wq!" para editar, salir y m}aplicar cambios.

## Rebase - Edit


	Empezamos con una demostración sobre en caso de modificar algunos archivos pero ya no deseamos guardar los cambios unicamente de un archivo u otro por agregar, podemos hacerlo de la siguiente manera:

```bash
git checkout -- Archivo.formato
```

	Esto nos devolvera al estado del ultimo commit ignorando los cambios hechos del archivo seleccionado.

	Si nosotros quisieramos hacer el trabajo de una manera distinta, por ejemplo, si hizimos cambios en tres archivos en un solo commit y nosotros ahora queremos separarlos por motivos de trabajo, podemos usar el menú interactivo:

```bash
git rebase -i HEAD~3
```

	Ahora en el menú interactivo seleccionaremos el commit que queremos modificar y cambiaremos "pick" por "edit":

```bash
pick 53d6389 # Ejemplo agregado.
pick a63951e # Ejeplo ignorado.
edit 70db419 # Aquí editamos.
```

	Veremos algo como esto:
	
```bash
PS C:\Users\PC\Desktop\Git\08-demo-rebase> git rebase -i HEAD~3
Stopped at 70db419...  # commits
You can amend the commit now, with

  git commit --amend 

Once you are satisfied with your changes, run

  git rebase --continue
```

	Podemos hacer ammend para cambiar el nombre.

	Ahora estamos en un rebase manual al que tendremos que darle las indicaciónes sobre que queremos hacer.

	Es importante saber que se recomienda hacer unicamente los cambios que necesitamos porque nuestro trabajo ya no está en ninguna rama, si no en un rebase interactivo.

	Usaremos un "reset" para volver al commit anterior y así poder observar los cambios:

```bash
git reset HEAD^
```

	Podemos agregar los archivos que deseamos manualmente con:

```bash
git add nombrearchivos.formato
```

	Y podemos hacer el commit de la manera normal:

```bash
git commit -m "Archivo añadido"
```

	Git aún nos tendra en el "Rebase intercactivo", esto por si aún deseamos hacer alguna modificación, pero esto podría volver la tarea en algo muy laborioso, por ello se recomienda salir primero.

	Ahora, para salir del "Rebase interactivo", se hace de está manera:

```bash
git rebase --continue
```

	Ahora que acabemos de hacer las modificaciónes ya estaremos dentro de nuestra rama "Master" o "Main".

## Abortar

	Si por alguna razón consideramos el cancelar todos nuestros cambios en cualquier momento estando aún dentro del "Rebase Interactivo", podemos utilizar:

```bash
git rebase --abort
```

