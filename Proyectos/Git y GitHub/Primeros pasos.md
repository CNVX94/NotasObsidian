#Git

	Comenzamos por usar el bash por defecto de git.

1. Versión

```bash
git --version
```

	Nos permite observar la versión actual de Git con la que trabajamos y además permite saber si está instalada o no la herramienta.

2.  Abreviaturas
   
```bash
git - v
```

	Al usar una abreviatura en lugar de la palabra completa se utiliza unicamente un signo de menos "-" para poder realizar el comando correctamente, en este caso se relaiza la misma tarea pero sin la palabra completa.

3.  Configuración de Usuario.
   
```bash
git config --global user.name "Usuario"
git config --global user.email "ejemplo@mail.com"
```

	Git nos solicita una validación y una entidad confirmada debido a que en el registro existira quien y los cambios hechos en cada commit, por ello se pide sinceridad y registro personal o de la empresa para poder realizar el trabajo correspondiente.

4. Visualizar Configuración.
   
```bash
git config --global -e
```

	 Abrira un menú en el que podremos modificar nuestros datos con la tecla "a", podremos continuar y guardar cambios con la tecla "Esc", una vez visualicemos dos puntos ":", luego con "w" para hacer el cambio, "q" para simplemente salir o "!" para hacer todo y salir.

5. Directorio.

```bash
	$ cd /c/Users/PC/Desktop/Git/01-bases
```

	Podemos arrastrar a la ventana de git bash el directorio sobre el que queremos trabajar, de otra manera tendrá que ser indicada con la dirección de raíz donde está localizado nuestro proyecto.

6.  Inicializar Repositorio.

```bash
	git init
```

	Una vez registrados y en la carpeta del proyecto podremos inicializar el repositorio con "git init", simplemente hará su trabajo y podrémos observarlo a continuación.

7.  Estatus.
   
```bash
	git status
```

	Ya creado el repositorio, ahora podremos observar los archivos que estan presentes en la carpeta que no estén bajo señal de ser controlados por el repositorio, lo cual nos permite 

8. Agregar
   
```bash
	git add index.html
	git add .
```

	Este comando permite añadir los archivos que queremos esten bajo el control de versiones, podemos agregar uno por uno o todos al mismo tiempo, asi como también eliminarlos con:

9. Remover.
   
```bash
	git reset "NombreArchivo"
	git status
```

	 Con esto podremos observar los cambios correspondientes al archivo que hayamos decidido no conservar en el control del repositorio.

10. Commit.

```bash
	git commit -m "First Commit"
```

	Una vez finalizada la selección de archivos, ahora podremos crear nuestro primer commit en donde agregaremos nuestro mensaje "-m" y el texto que tendra para el control de versiones, en este caso "First Commit".

11. Observar Historial.

```bash
	git log
```

	Con esto podremos observar quien, cuando y que mensaje dejo en los cambios realizados, así como el titulo del mensaje.

Seguimos en [[Reconstruir]].