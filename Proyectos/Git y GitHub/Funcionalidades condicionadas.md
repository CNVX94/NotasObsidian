#Git 

## .gitkeep
	Git generalmente no se hará a la tarea de detectar o considerar directorios vacíos, es por ello que tenemos esta herramienta:

	.gitkeep

	Sera un archivo dentro de la carpeta con la que podremos inidcar a Git que es un direcotrio o espacio que debe ser considerado para los siguientes commits.

	Podremos añadirlo con:
	
```bash
git add uploads/*.gitkeep
```

## reset --hard

	A veces si hacemos cambios, pero nos arrepentimos de borrar, alterar algo, este comando nos volvera a una especie de checkout donde el proyecto estaba en cierto punto, en muchos sentidos son similares pero se deja a consideración.

```bash
git reset --hard
```

