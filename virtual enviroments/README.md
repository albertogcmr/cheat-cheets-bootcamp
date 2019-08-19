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

## Requirements

```
(env) $ pip freeze >> requirements.txt
```

Este comando crea un fichero llamado `requirements.txt` que lista las dependencias que necesita el entorno virtual que has creado. 

Si heredas un proyecto que incluye un archivo de este tipo para instalar las dependencias que necesitas usa el siguiente comando. 

```
(env) $ pip install -r requirements.txt
```