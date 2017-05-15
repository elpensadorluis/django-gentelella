# [Plantilla Original Gentelella Admin](https://github.com/puikinsh/gentelella)
este es un fork del proyecto: https://github.com/GiriB/django-gentelella traducido al español y con proyecto de utilizar el framework vue.js para hacerlo reactivo.

## Pasos
[Optional] [Configurar VirtualEnv y VirtualEnvWrapper]
- Buscar en los repositorios de su distribución Linux los paquetes python-virtualenv python-virtualenvwrapper e instalarlos segun como esten en los repositorios
#### [Debian]:
```
apt-get update
apt-cache search python virtualenv virtualenvwrapper
apt-get install virtualenv virtualenvwrapper
```
#### [Arch]
```
pacman -Syyu
pacman -Ss python virtualenv virtualenvwrapper
pacman -S python-virtualenv python-virtualenvwrapper
```
Crear Un directorio en nuestro HOME
```
mkdir $HOME/.virtualenvs
```
Modificar el archivo .Bashrc de nuestro sistema con su editor de preferencia:
```
vim ~/.bashrc
```
Agregar al final dos variables para instanciar workon y asignarle la carpeta que hemos creado y el link al script de virtualenvwrapper:
```
...
export WORKON_HOME=~/.virtualenvs
source /usr/bin/virtualenvwrapper.sh
```
Recordar que se debe ubicar el script virtualenvwrapper.sh en el lugar donde se instala y asignarle esa dirección a la variable source. La forma más practica de buscarlo en linux desde consola es la siguieten:
```
cd /
su
find -name virtualenvwrapper.sh
```
Ahora nos toca activar nuestro Entorno virtual, pero primero debemos crear nuestro primer virtualenv, lo cual es muy sencillo gracias a VirtualEnvWrapper: (Recomiendo buscar las versiones de python instaladas en el sistema primero y elegir la que necesitamos en el entorno virtual)
```
ls /usr/bin/ | grep python
mkvirtualenv -p /usr/bin/python3.7 mi_env
workon mi_env
```
Para desactivar el entorno utilizar el comando:
```
(mi_env)$ deactivate
```

Para saber más comandos ejecutar desde consola:
```
man virtualenv
```
##### Opten el Código:
```
    git clone https://github.com/elpensadorluis/django-gentelella.git
    cd django-gentelella
```

##### Instala los requerimientos:
```
    pip install -r requirements.txt
```

##### Ejecuta el Código
```
    cd gentelella
    python manage.py runserver 
```
##### Abre un navegador web y busca tu proyecto en:
http://localhost:8000/
