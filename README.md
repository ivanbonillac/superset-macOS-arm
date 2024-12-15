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

Como trabajeremos con un proyecto en Flask (python) lo ideal es crear un [entorno virtual](https://docs.python.org/es/3/tutorial/venv.html#introduction) para el manejo de las dependencias aisladas. . Asi que crearemos un entorno virtual para nuestras dependencias de superset. Es importante que sepas que el superset requiere una version especifica python: `python 3.10` Verifica que esa version de python este instalada en tu macOS, para que cuando crees el entorno virtual puedas especificarlo como detalla el siguiente comando. 

```sh
python3.10 -m venv superset-env
```
## 1.3. Activacion del entorno virtual
Una vez creado el entorno vitual, ejecutaremos el siguiente comando que activara el entorno virtual.

```sh
source superset-env/bin/activate
```
Ahora verás en tu linea de comando que comienza con `(superset-env)`. Quiere decir que estarás dentro del entorno y podemos ejecutar ciertos comandos como pip o python directamente sin el python3.

#### Verificando version de `python` instalada en el entorno
Ejecutaremos: 
```sh
python --version
```
El resultado debería ser: `Python 3.10.16` en mi caso por que tengo instalada esa version. En tu caso puede ser diferente dependiendo de la version de python instalada.

#### Comando para desactivar el entorno
Cunado requieras cerrar el entorno ejecutaremos: 
```sh
deactivate
```
La terminal deberia verse ahora sin `(superset-env)`.

## 1.4. Actualizando `pip`
Como utilizamos python, tenemos que usar un manejador de paquetes. Para python el manejador de paquetes es pip, este viene instalado en el entorno virtual por defecto. Para verificar realizamos el siguiente comando en nuestro entorno virtual activo. Este nos debe arrojar la version del pip instalada en ese momento.
```sh
pip --version
```


Para actualizar el pip ejecutaremos:
```sh
pip install --upgrade pip
```

## 2. Instalando Superset desde `pip`
