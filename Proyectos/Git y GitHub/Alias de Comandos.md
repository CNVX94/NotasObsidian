#Git 

	Podemos ayudarnos para visualizar de diferente manera algunos comandos para que nos muestren l oque necesitamos o un poco de menos visualización a diferentes textos que arroja la consola.

## Short

```bash
git status --short
```

	En este comando nos mostrara los archivos con su abreviación de aquello a lo que se este realizando o no el seguimiento correspondiente.

## Crear Alias

	Comandos de git largos resumidos de forma corta asignados por nuestra mano.

```bash
git config --global alias.s status --short
o
git config --global alias.s "status --short"
```

	Podemos observar que estamos realizando la configuración de manera global para nuestra area de trabajo, estamos indicando que caracter de alias queremos y a continuación el comando a resumnir, finalmente la indicación de que con esto lo acortaremos.

	La primer instrucción no agregará la extensón de short, aquellas consideraciones deberan agregarse entre comillas para que el sistema entienda directamente a que comando se está realizando el alias, de otra manera se deberá mododificar desde:

```bash
git config --global -e
```

## Algunos Alias

	Proveeído por el curso:

Log:

```bash
git config --global alias.lg "log --graph --abbrev-commit --decorate --format=format:'%C(bold blue)%h%C(reset) - %C(bold green)(%ar)%C(reset) %C(white)%s%C(reset) %C(dim white)- %an%C(reset)%C(bold yellow)%d%C(reset)' --all"
```

Status:

```bash
git config --global alias.s "status --short"
```

Alternativa a Status:

```bash
git config --global alias.s "status -sb"
```