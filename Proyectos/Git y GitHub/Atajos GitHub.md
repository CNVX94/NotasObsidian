#Github 

	Podemos usar este comando para saber a que dirección estamos realizando nuestras actividades:

```bash
git remote -v
```

	Nos mostrara el "Fetch" de donde es que estamos obteniendo los datos, y el "Push" que es hacía donde estamos orientando los cambios.

	Además observaremos el alias que recibe todo nuestro link marcado en este caso como "Origin".

> Esto fue debido al comando:

```bash
git branch -M main
git push -u origin main
```