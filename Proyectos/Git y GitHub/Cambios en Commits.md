#Git 

## Diferencias

	Muestra la diferencia entre los archivos a los que se realiza seguimiento contra la versión actual después de modificaciones.

```bash
git diff
```

### Stage

	Permite observar la diferenciación del archivo actual contra el archivo del stage, esto es útil si la comparación lleva tiempo o si el primer comando no muestra ninguna diferencia aunque sepamos que si la tiene.
	
```bash
git diff --stage
```

## Modificación en Commits

	Un commit no será estatico y a veces podremos cometer errores al nombrar el commit o algo por el estilo, la forma más sencilla es:

```bash
git commit --amend -m "Commit Corregido"
```

	Esto funcionara unicamente con nuestro más reciente commit.

## Modificar Commits Anteriores

	Digamos que queremos modificar y hacer que ciertas modificaciones sean parte de un commit anterior, con esto nos moveremos al git anterior pero esto hará que se reconstruya el nuevo commit.

```bash
git reset --soft HEAD^
```

	Con este comadno, aunque conocemos reset para quitar archivos del seguimiento, con este podremos apuntar al ultimo commit antes.
	Este HEAD se puede cambiar por el hash de un commit.
	Esto alterara el git y se deberá tener cuidado ya que podemos perder información no guardada.


## Modificar sin destruir

	Dado que hayamos agregado algo que debería ir antes o que sea preferible agregarlos desde un commit antes, podemos movernos de la siguiente manera:

```bash
git reset --soft HEAD^
git reset --mixed HEAD^
o
git reset --soft hashdelcommit
```

	Recordemos que cada commit tiene un hash, con ese mismo podemos movernos directamente si es que el commit esta mucho antes que nuestro lugar principal.


## Modificar destructivo.

	Con esto haremos realtivamente lo mismo, pero una vez estando dentro del commit donde queremos empezar a reconstruir los cambios, destruiremos todos los cambios hechos en los commits que realizamos a continuación o en los commits posteriores.

```bash
git reset --hard HEAD^
o
git reset --hard hashdelcommit
```

## Recuperar contenido.

	 Suponiendo que de hecho no estabamos mal y ahora nos arrepentimos y lloramos en la esquina del cuarto, hay una solución:

```bash
git reflog
```

	Esta herramienta mostrara los cambios en el tiempo y aquellos commits que hayamos dejado en el tiempo y en orden cronológico.

```bash
git reset --hard hashdelcommitarecuperar
```

	Con esto se recuperará hasta el punto señalado y con lo que tenga agregado el commit.
