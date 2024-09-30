# Dataton 2024


## Descripción del proyecto
Este proyecto tiene como objetivo ubicar las mejores 200 ubicaciones que podría usar la ANTAD para colocar nuevas farmacias afiliadas a la asociación. Para esto, utilizamos datos proporcionados por el INEGI como el Censo de Población y Vivienda 2020 y el DENUE.
Para el procesamiento y visualización de los datos utilizamos los lenguajes de programación R y Python.
##Datos Utilizados
Los datos utilizados para este proyecto provienen de:
- **El Directorio Estadístico Nacional de Unidades Económicas** (obtenido de https://www.inegi.org.mx/app/descarga/?ti=6)
- **El Censo de Población y Vivienda 2020** (obtenido de https://www.inegi.org.mx/programas/ccpv/2020/#Datos_abiertos)
- **La Base Geográfica Digital del INE** (obtenido de https://cartografia.ine.mx/sige8/productosCartograficos/bases)
## Requerimientos

### Python
- **Versión recomendada**: Python 3.6 o superior

#### Librerías requeridas
- `requests` (2.25.1)
- `pandas` (1.3.3)
- `matplotlib` (3.4.3)
- `geopandas` (0.9.0)
- `numpy` (1.21.2)

### R
- **Versión recomendada**: R 4.0.0 o superior

#### Librerías requeridas
- `pacman` (para cargar otras librerías)
- `readr`
- `dplyr`
- `ggplot2`
- `stringr`
- `sf`
- `RColorBrewer`
### Instalación de Librerías

#### Python
Para instalar las librerías de Python, ejecuta:
```bash
    ``pip install requests pandas matplotlib geopandas numpy``
#### R
Para instalar las librerías de R: ejecuta:
if (!requireNamespace("pacman", quietly = TRUE)) {
  install.packages("pacman")
}
pacman::p_load(readr, dplyr, ggplot2, stringr, sf, RColorBrewer)
## Estructura del proyecto
1. **limpieza_datos.ipynb**: Esta Jupyter Notebook realiza la limpieza de los datos iniciales y nos deja con varios dataframes preparados para ejecutar el siguiente archivo.
2. **exports_municipios_farmacias.Rmd**: Este archivo en R Markdown utiliza los datos limpios para obtener los municipios más prometedores para la colocación de las farmacias, además de varias métricas.
