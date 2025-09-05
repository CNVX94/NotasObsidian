#Linux  #Python

VENV (Virtual Environment)

## 1. ¿Qué es?

Se puede considerar un entorno o una pequeña maquina donde instalaremos herramientas y/o dependencias y librerías que necesitemos específicamente para algunos proyectos, 

>Ubuntu no permite instalar algunas aplicaciones que puedan requerir instalaciones  o elementos que puedan interferir con las librerías que ya tenga el sistema.

## 2. ¿Cómo crear uno?

### 2.1 Asegurarnos de tener instalado python (también es util para determinar alguna versión especifica de python)

```bash
sudo apt update
sudo apt install python3-venv
```

### 2.2 En la carpeta del proyecto crear el entorno:

```bash
python3 -m venv venv /// <-Nombre del entorno
```

### 2.3 Activar el entorno virtual

Ejecutar en terminal:

```bash
source venv/bin/activate
///venv se refiere al nombre
///Es importante estar en la carpeta anterior de donde tenemos localizado el venv
```

