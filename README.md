# [data.buenosaires.gob.ar](https://data.buenosaires.gob.ar/)

CORRGIR

Repositorio de la extensión del Portal [data.buenosaires.gob.ar](http://data.buenosaires.gob.ar/) de la Ciudad de Buenos Aires para [CKAN](http://ckan.org/). Este proyecto se encarga de modificaciones al ruteo de la aplicación web, cambios visuales a la interfaz, y customización del portal, entre otros. Este repositorio *no* constituye el proyecto entero.

- [Instalación](#instalaci%C3%B3n)
- [Desarrollo](#desarrollo)
- [Estructura de archivos](#estructura-de-archivos)
- [Uso del theme](#uso-del-theme) --> HACER
- [Créditos](#cr%C3%A9ditos)
- [Consultas sobre Andino](#consultas-sobre-andino)

## Instalación

Correr dentro del entorno virtual de python(venv) para instalaciones hechas con Docker:

    -pip install -e "git+https://github.com/gasti10/ckanext-gobar-theme.git#egg=ckanext-gobar_theme"

### Estructura de archivos

```
- ckanext
    - gobar_theme
        - asset
            - js
                - archivos de js a ser importados por los distintos templates html
            - styles
                - archivos css generados desde sus versiones de scss
        - public
            - assets estáticos y públicos como imagenes y fuentes
        - templates
            - archivos de jinja renderizados por los controladores
        - actions.py # lógica de modelos de ckan, sobreescribe y/o extiende la lógica de ckan
        - controller.py # controladores para la home y la api, sobreescriben y/o extienden la lógica de ckan
        - helpers.py # metodos auxiliares para renderizado de templates
        - package_controller.py # controlador de lógica de datasets y recursos, sobreescribe y/o extiende la lógica de ckan
        - plugin.py # archivo que registra el repositorio como extensión de ckan y declara acciones, helpers y ruteo
```

## Créditos

Este proyecto está basado en [CKAN](https://github.com/ckan/ckan) y en la [guia para crear extensiones](http://docs.ckan.org/en/latest/extensions/tutorial.html).
