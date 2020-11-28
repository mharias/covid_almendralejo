# Repositorio de datos de Covid19 de Almendralejo y preparación de gráficas
Repositorio de datos de covid19 de Almendralejo

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub commit](https://img.shields.io/github/last-commit/pcm-dpc/COVID-19)](https://github.com/mharias/covid_almendralejo/commits/master)


Ante la imposibilidad de recopilar de una manera sencilla los datos históricos de casos epidemiológicos de Almendralejo decidí preparar este repositorio, en el que de manera manual, y diariamente, copiamos y pegamos de manera manual los datos publicados bien por el Ayuntamiento de Almendralejo en formato no reusable ([twitter](https://twitter.com/AlcaldiaAlm/status/1329705935992975365?s=20) o [facebook](https://www.facebook.com/ayuntamientodealmendralejo/posts/1091505441303447)) bien  por la Comunidad Autónoma Extremadura desde este [site](https://saludextremadura.ses.es/web/casospositivos).
Los datos se están recopilando en esta [excel](https://github.com/mharias/covid_almendralejo/blob/main/datos/almendralejo.xlsx), se copian de diariamente de este site. Y se hace de forma manual, no he encontrado aun la manera de automatizar esta tarea. Cualquier sugerencia con procedimientos para hacerlo es bienvenida!

El código `python` para realizar la descarga a `pandas` es el siguiente: 
```python
import pandas as pd
path_fuente_datos_github='https://github.com/mharias/covid_almendralejo/blob/main/datos/almendralejo.xlsx?raw=true'
datos = pd.read_excel(path_fuente_datos_github,skiprows=2)
```
En el `pandas` datos ya dispondría de la información de datos positivos y activos ordenados por fechas.
Los datos están disponibles desde 18 de Octubre 2020.

En este [notebook](https://github.com/mharias/covid_almendralejo/blob/main/graficos_almendralejo.ipynb) dispone del código para generar los diferentes gráficos que vemos a continuación:

![alt text](https://github.com/mharias/covid_almendralejo/blob/main/graficos/almendralejo_nuevos_casos.png)

![alt text](https://github.com/mharias/covid_almendralejo/blob/main/graficos/almendralejo_ia14.png)

![alt text](https://github.com/mharias/covid_almendralejo/blob/main/graficos/almendralejo_activos.png)


Si usa estos datos le agradecería que referencie este repositorio #covid_almendralejo. Este repositorio a su vez referencia al origen de datos.

Para cualquier problema puede abrir un [`Issue`](https://github.com/mharias/covid_almendralejo/issues), o mandarme un correo a mharias@me.com, muchas gracias por su colaboración!
