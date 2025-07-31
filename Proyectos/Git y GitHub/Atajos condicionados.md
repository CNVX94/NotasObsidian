#Git 

	No siempre es necesario hacer todo el trabajo manualmente, claro que es recomendado pero hay algunis atajos que sirven bajo algunas circunstancias.

	Es importante considerarlos una vez hayamos finalizado el curso.
## Actualizar sin añadir

	Mientras hagamos seguimiento de manera correcta y trabajemos en los mismos archivos, si queremos hacer un commit actualizado con nuestros mismos archivos podemos hacerlo directamente con:

```bash
git commit -am "Actualizacion"
```

	Nos va a permitir realizar la actualización de nuestros archivos a los que les este dando seguimiento al repositorio, pero no agregará ni hará nada con los nuevos o diferentes archivos que hayamos agregado en el flujo de trabajo.

## Archivos específicos

	Suponiendo que solo quiera agregar un conjunto de archivos del mismo tipo, considerando que es prefireble que cada tipo de archivos una vez modificados se hagan en un commit aparte, podremos usar el siguiente atajo:

```bash
git add *.formatoarchivo
```

	Debemos considerar que cada archivo sera buscado desde el root y no serán considerados los archivos en carpetas, y es por ello que debemos tenerlo en cuenta.

```bash
git add carpeta/*.formatoarchivo
```

## Añadir Directorios

	Siempre y cuando consideremos actualizar o añadir al stage una gran cantidad de archivos que no solamente con añadir por extensón, por ejemplo, que contenga diferentes terminaciones o carpetas, podemos añadir el directorio completo de la siguiente manera:

```bash
git add carpeta/
```

## Muestro reducido

	Utilizando log veremos mucha información seccionada, podemos recortar la visualización con el siguiente comando:
	
```bash
git log --oneline
```

	A su vez puede recortarse con un alias como viene paso a paso en:	
[[Alias de Comandos]]

