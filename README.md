# [datos.gob.ar](http://datos.gob.ar/)

CORRGIR

Repositorio de la extensión del Portal [datos.gob.ar](http://datos.gob.ar/) de la República Argentina para [CKAN](http://ckan.org/). Este proyecto se encarga de modificaciones al ruteo de la aplicación web, cambios visuales a la interfaz, y customización del portal, entre otros. Este repositorio *no* constituye el proyecto entero. El repositorio central del proyecto del Portal datos.gob.ar es [portal_datos.gob.ar](https://github.com/datosgobar/portal_datos.gob.ar)

- [Instalación](#instalaci%C3%B3n)
- [Desarrollo](#desarrollo)
- [Estructura de archivos](#estructura-de-archivos)
- [Uso del theme](#uso-del-theme) --> HACER
- [Créditos](#cr%C3%A9ditos)
- [Consultas sobre Andino](#consultas-sobre-andino)

## Instalación

HACER

## Desarrollo

Como alternativa a la instalación dockerizada existe la posibilidad de tener una instalación contenida en un `virtualenv` del sistema. Esto se puede obtener siguiendo las instrucciones de [esta guia](http://docs.ckan.org/en/ckan-2.5.2/maintaining/installing/install-from-source.html). Una vez instalado el paquete a nivel sistema, es posible linkear el proceso principal a un debbuger de python (por ej pycharm). Este metodo no es recomendado para hacer modificaciones que impacten en el manejo del servidor por parte del wsgi de apache o nginx. Para dicho caso, es necesario tener una instalación de la aplicación dockerizada y acceder al contenedor del theme para realizar el desarrollo necesario.

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
