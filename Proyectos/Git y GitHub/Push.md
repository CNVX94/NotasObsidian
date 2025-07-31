#Github 

	Este comando se encarga de subir nuestra nueva información y/o proyecto con los nuevos cambios.
	El comando no se ejecutara si no hay cambios en el código reciente.

	En resumen, "Tomar nuestro repositorio y subirlo al servidor."

```bash
git push -u origin main
```

	Con este comando estaríamos haciendo que nuestro repositorio que asignamos como "origin" escriba los nuevos datos sobre la rama main.
	Por supuesto esto puede modificarse más adelante...

## Push de Etiquetas (Tags)

	Al manejar etiquetas nosotors podemos designar una especie de versiones según lo consideremos, esto no se subira automaticamente con el push principal y deberá ser agregado uno por uno o con facilidad de todos a la vez:

```bash
git push --tags
```

	Ahora en nuestro repositorio de git podremos observar las versiones señaladas.

![[Pasted image 20250723221016.png]]

> Release Tags [[Etiquetas de producción]]

> Continuamos en [[Pull]]