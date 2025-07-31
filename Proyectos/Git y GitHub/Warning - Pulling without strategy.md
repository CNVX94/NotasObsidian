#Git #Github 

	En versiones anteriores, este warning avisa sobre algunas cosas que GitHub toma a consideración para poder trabajar correctamente.

	Es raro que aparezca, pero igualmente podremos configurarlo o modificarlo a gusto.

```bash
git config --global pull.ff only
```

	Esto permitira que al no tener un "Fast-Forward" al unir una rama, entremos autoamticamente en modo de conflicto para poder realizar los cambios pertinentes y no estar construyendo una aplicación que al final del día no compile...

>Observar notas de [[Unión de Ramas]]

	Podremos observar los cambios asignados con:

```bash
git config --global -e
```

	Notaremos lo sieguiente en el menú:

![[Pasted image 20250723230510.png]]

> Seguimos en [[Clonar un Repositorio]]