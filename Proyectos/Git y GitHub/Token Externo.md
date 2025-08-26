#Github 

	Ahora que consultemos un proyecto en una computadora externa, o en donde sea que intentemos desarrollar nuestro proyecto en un area externa requeriremos ahora de una "Contraseña" para poder hacer "Push"

	Esa "Contraseña" en cuestión tenemos que generarla exclusivamente desde nuestro perfil como un "Personal Token", para ello tendremos que entrar:

1. Iniciar Sesión en GitHub.
2. Ir a nuestra foto de perfil.
3. Entrar a configuración o settings.
4. Bajar hasta casi el final de las opciones y entrar a "Configuración de Desarrollador" o "Developer Settings".
5. Entrar en "Personal Access Tokens".
6. Seleccionaremos "Fine-grained tokens" o "tokens (classic)" dependiendo nuestra necesidad.
7. Lo generaremos de preferencia con un lapso de tiempo considerable, si trabajaras desde una PC propia puedes hacerlo ilimitado.
8. Guarda la Key generada.

	Cabe aclarar que esto será únicamente para nosotros como el propietario del repositorio original, cualquier otra cuenta externa deberemos agregarla en colaboradores y todas sus intentos de "push" los veremos en "Pull Requests".}

	Ahora podemos configurar de manera permanente la clave para no tener que estarla escribiendo cada que intentemos hacer pull:

1. Agregar esto en terminal.
```bash
git config --global credential.helper store
```

2. Podemos proceder a hacer push y a agregar la contraseña que sera guardada en la configuración.   