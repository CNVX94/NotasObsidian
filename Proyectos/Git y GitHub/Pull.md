#Github 

	Basicamente "Obtener los cambios de nuestro repositorio."

```bash
git pull
o
git pull -u origin main
```

	Por defecto es recomendado automatizar que por defecto nuestro pull sea hacía la origin, pero si queremos absorber una rama, también puede hacerse.


## Subir Cambios Locales a Remoto

	Simplemente usando el mismo comando una vez hayamos hecho cambios y realizado nuestro nuevo commit, podemos hacer:

```bash
git pull
```

	Debemos contemplar que tendremos fallos si hay cambios nuevos desde el repositorio en liena y desde nuestro repositorio local, por ejemplo, haciendo cambios en la misma linea, por ello el pull estará fallando.

	Tenemos la siguiente herramienta que viene gracias a modificaciones en las configuraciones.

```bash
git config pull.rebase true
o
git config --global pull.rebase true
```

	Esto agrega la capacidad de visualizar en el editor de código las diferencias que estan bloqueando la posibilidad de hacer el pull que necesitamos para actualizar nuestro proyecto.
	
	La segunda línea nos permite guardar el cambio de manera global.
	
	Es importante recordar que una vez ocurra el error, estaremos en un caso similar en las notas de "Reabase", esto nos pone en un Rebase Interactivo donde habremos de hacer los cambios correspondientes a cosnideración para guardar la correción en un nuevo "commit" y después salir con el comando:

> Consultar [[Rebase]]

```bash
  git commit -m "Error solucionado"
  git rebase --continue
  git push
```

	Finalmente consultamos con un push que nuestro trabajo ahora esta correcto.

> Seguimos en: [[Warning - Pulling without strategy]]