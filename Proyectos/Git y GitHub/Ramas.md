#Git 

	Podemos observar a través de los comandos:

```bash
git branch
git status
```

	 Al iniciar el Commit nos encontraremos trabajando en "Master", la cual es la rama principal del flujo de trabajo, o donde se encuentra la rama original del proyecto. 

	 Una rama puede verse como un proyecto paralelo que puede desarrollarse de diferente manera o con ideas distintas.

	"Se aconseja no hacer muchos cambios en la rama master y desarrollar siempre en diferentes ramas".

## Cambiar nombres de ramas

	No siempre o a veces será necesario y se aconseja hacer esto en tiempos recientes, cambiaremos de nombre la rama "Master" a "Main" con el siguiente comando:

```bash
git branch -m master main
```

## Cambio global

```bash
git config --global init.defaultBranch main
```

	Esto hace que cada nuevo repositorio empiece con el nombre de la rama como "main" en lugar de "master". Al menos lo mantendra para cada rama principal, no para las extra.


## Crear una Rama

	Por fin aqui creamos una rama nueva:

```bash
git branch nombrerama
```

### Movernos a una rama

```bash
git checkout nombrerama
```

## Eliminar Rama

```bash
git branch -d nombrerama
```

## Eliminar una Rama de manera forzada

	Git avisara si hay cambios que no hayamos considerado o agregado en la rama que nosotros creamos, podemos considerarlo o forzar la eliminación si así nosotros lo deseamos.

```bash
git branch -d nombrerama -f
```

## Atajo para Crear una Rama y Movernos

	Existe este atajo para crear una rama y movernos automaticamente a ella sin necesidad de hacer todos los pasos de creación:

```bash
git chekout -b nombrerama
```

Seguimos en [[Unión de Ramas]]

## Actualizar una Rama

	Para este caso en particular dejamos un nodo aparte.

[[Rebase]]