#Git 
## Stash

	 Boveda segura de cambios que puede alojar todo el trabajo desde el último commit que no han impactado, es decir, salvar un desarrollo pendiente para recuperarlo más adelante, esto guadara todo el direcotrio, incluyendo archivos nuevos agregados y modificaciónes.

	Se considera para casos específicos donde tengamos que resolver algo antes.

Crear el stash:

```bash
git stash
```

Crear el stash con un nombre específico:

```bash
git stash save "Nombre"
```

Consultar cambios de un stash:

```bash
git stash show "stash@{n}"
```

Verificar los cambios de todos los stash:

```bash
git stash list --stat
```
Recuperar el stash y el trabajo generado.

```bash
git stash pop
```

Borrar el stash (Todos los borra sin preguntar, se puede recuperar con el hash con reflow).

```bash
git stash clear
```

Borrar un stash en específico:

```bash
git stash drop "stash@{n}"
```

Recuperar un stash en especifico.

```bash
git stash apply nombrestash@{n}
```

> Nota: Al parecer el powershell, la consola mal interpreta los corchetes "{}" ya que son de función especial, por lo que se recomienda realizarlo de la siguiente manera en PoweShell:

```bash
git stash apply n 
-- Donde n es numero
-- o
git stash apply "stash@{n}"
```
### Conflictos en Stash

	 Se recomienda nunca alojar mucho trabajo o más de un stash sin nombre, una buena práctica siempre es mejor cuadno se usan ramas o menos de dos stash.
## Rebase

	 Continuamos en:

[[Rebase]]