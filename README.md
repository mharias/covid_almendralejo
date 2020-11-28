# Repositorio de datos de Covid19 de Almendralejo y preparación de gráficas
Repositorio de datos de covid19 de Almendralejo

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![GitHub commit](https://img.shields.io/github/last-commit/pcm-dpc/COVID-19)](https://github.com/mharias/covid_almendralejo/commits/master)


He creado este repositorio para recopilar, y poner a disposición de todos, los datos epidemiológicos de Almendralejo publicados por el Ayuntamiento Almendralejo y por la Comunidad Autónoma Extremadura.
Los datos se están recopilando en esta [excel](https://github.com/mharias/covid_almendralejo/blob/main/datos/almendralejo.xlsx), se copian de ediariamente de este site. Y se hace de forma manual, no he encontrado aun la manera de escrapearlo. Cualquier sugerencia con procedimientos para es bienvenida!

El código `python` para realizar la descarga a `pandas` es el siguiente: 
```python
import pandas as pd
path_fuente_datos_github='https://github.com/mharias/covid_almendralejo/blob/main/datos/almendralejo.xlsx?raw=true'
datos = pd.read_excel(path_fuente_datos_github,skiprows=2)
```
En el `pandas`datos ya dispondría de la información de datos positivos y activos ordenados por fechas.
Los datos están disponibles desde 18 de Octubre 2020.

En este [notebook](https://github.com/mharias/covid_almendralejo/blob/main/graficos_almendralejo.ipynb) dispone del código para generar los diferentes gráficos que vemos a continuación:

![alt text](https://github.com/mharias/covid_almendralejo/blob/main/graficos/almendralejo_nuevos_casos.png)

![alt text](https://github.com/mharias/covid_almendralejo/blob/main/graficos/almendralejo_ia14.png)

![alt text](https://github.com/mharias/covid_almendralejo/blob/main/graficos/almendralejo_activos.png)


Si usa estos datos le agradecería que referencie este repositorio. Este repositorio a su vez referencia al origen de datos.

Para cualquier problema puede abrir un `Issue`, o mandarme un correo a mharias@me.com, muchas gracias!
