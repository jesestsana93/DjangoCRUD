Modificar el archivo settings.py de acuerdo al SMBD con el que se vaya a trabajar
Para Postgresql:
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'nombre',
        'USER': 'postgres',
        'PASSWORD': 'contraseña',
        'HOST':'localhost',
        'PORT':5432,
    }
} 

Para MySQL:
Installar pip install cymysql
pip install django-cymysql

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'refugio',
        'USER': 'root',
        'PASSWORD': 'UNAMsaje93',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}

LANGUAGE_CODE = 'en-mx'

INSTALLED_APPS = [
    'apps.agregar',
    'apps.las',
    'apps.que',
    'apps.se',
    'apps.usen',
]
https://medium.com/@a01207543/django-conecta-tu-proyecto-con-la-base-de-datos-mysql-2d329c73192a

Para importar el cliente en todo el proyecto, lo que haremos será abrir el documento MyProject/MyProject/__init__.py y escribir los siguiente:
import pymysql
pymysql.install_as_MySQLdb()
