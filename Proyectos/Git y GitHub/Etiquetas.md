#Git 

	Se pueden considerar como una referencia a un commit específico y a todo el estado del proyecto en ese momento específico. 
	Se utilizan para marcar versiones o release de nuestro código.

## Visualizar Etiquetas

```bash
git tag
o
git show v0.1.0
```

	Podemos visualizar todas y una por separado a detalle.
## Crear etiqueta

```bash
git tag nombretag
```

## Eliminar etiqueta

```bash
git tag -d nombretag
```


## Versión Anotada

```bash
git tag -a v1.0.0 -m "Version 1.0.0 lista"
```

	Esto ayuda a indicar un punto de maduración del proyecto, puede señalar también que aquí puede verse afectado el código a modificaciónes.

## Anotar en Commit Anterior

	 Si quisieramos señalar en algun commit anterior qalguna etiqueta debe ser con el hash del commit en cuestión.

```bash
git tag -a v0.1.0 ba644c0 -m "Version Alpha de la app"
```

> Release Tags [[Etiquetas de producción]]