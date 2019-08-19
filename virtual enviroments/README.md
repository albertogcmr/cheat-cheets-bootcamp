## Create virtual environment

https://realpython.com/python-virtual-environments-a-primer/

Create a new virtual environment inside the directory

```
$ python3 -m venv env
$ source env/bin/activate
(env) $
```

Para desactivar el entorno virtual

```
(env) $ deactivate
$
```

NOTA: En este ejemplo generemos los ficheros del entorno virtual en la carpeta `env` de la carpeta actual. Lo ideal es crear estos entornos en una carpeta **ajena** al proyecto actual. Lo que sí debería estar incluido es el fichero requirements.txt

## Requirements

```
(env) $ pip freeze >> requirements.txt
```

Este comando crea un fichero llamado `requirements.txt` que lista las dependencias que necesita el entorno virtual que has creado. 

Si heredas un proyecto que incluye un archivo de este tipo para instalar las dependencias que necesitas usa el siguiente comando. 

```
(env) $ pip install -r requirements.txt
```