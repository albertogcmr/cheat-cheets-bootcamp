## Installation

```
$ sudo apt-get install python3-venv
```

Forma alternativa: 

```
$ pip3 install virtualenv
```

## Create virtual environment

https://realpython.com/python-virtual-environments-a-primer/

Create a new virtual environment inside the directory. 

```
$ python3 -m venv env
$ source env/bin/activate
(env) $
```

Now you can work. 

```
(env) $ code main.py
```

Para desactivar el entorno virtual

```
(env) $ deactivate
$
```

NOTA: En este ejemplo generemos los ficheros del entorno virtual en la carpeta `env` de la carpeta actual. Lo ideal es crear estos entornos en una carpeta **ajena** al proyecto actual. Lo que sí debería estar incluido es el fichero requirements.txt

## Requirements

El siguiente comando crea un fichero llamado `requirements.txt` que lista las dependencias que necesita el entorno virtual que has creado.

```
(env) $ pip freeze > requirements.txt
``` 

En caso de que clones un proyecto que incluye un archivo de este tipo, para instalar las dependencias que necesitas usa el siguiente comando. 

```
(env) $ pip install -r requirements.txt
```