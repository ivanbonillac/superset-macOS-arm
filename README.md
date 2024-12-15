# Apache Superset en macOS ARM Based


## 1. Prerequisitos
### 1.1. Directorios de Trabajo

Dependiendo de donde quieras crear la carpeta. En mi caso la crearé en mi carpeta personal de proyectos `_code-projects`. La ruta para esa carpeta es: `/Users/soporte/Documents/_code-projects` la ruta y nombre para tu carpeta de trabajo puede ser diferente.

Ejecutaremos los siguientes 2 comandos.

```sh
mkdir superset-project  
cd superset-project
```
Luego de ejecutados, estaremos en la ruta `/superset-project` esta ruta será el directorio base de nuestro proyecto. Si ejecutas el siguiente comando en la terminal:
```sh
pwd
```
Debe aparecer `/superset-project` como la ultima direccion del resultado de la consola.


## 1.2. Creación del entorno virtual

Como trabajeremos con un proyecto en Flask (python) lo ideal es crear un entorno virtual para el manejo de las dependencias. Asi que crearemos un entorno virtual para nuestras dependencias de superset. 

```sh
python3.10 -m venv superset-env
```
