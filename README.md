# Road-Accidents-DA

Data Analytics project for the (OMSV) studies center (Buenos Aires - Argentina).

This project seeks to carry out an exploratory analysis of the data provided by the traffic accident study center in Buenos Aires - Argentina. Below is the structure of the content of this readme:

- [Road-Accidents-DA](#road-accidents-da)
  - [Datasets](#datasets)
    - [Descriptive Metadata](#descriptive-metadata)
      - [Quantitative Variables](#quantitative-variables)
      - [Qualitative Variables](#qualitative-variables)
    - [Null Values Management](#null-values-management)
  - [EDA Structuration](#eda-structuration)

## Datasets

For this project a dataset with 2 related tables were used. The dataset is a XLSX file with the following Sheet structure:

* Homicidios.xlsx
  * Hechos
  * Victimas
  * Diccionario Hechos
  * Diccionario Victimas
  * Glosario

The 'Hechos' and 'Victimas' sheets contains the main information about 696 road accidents occurred from 2016 to 2021. The remaining sheets contain information about the descriptive metadata and a glossary of relevant words. In the following section the dataset descriptive metadata will be showed in detail.

### Descriptive Metadata

Please query the following table for the dataset descriptive metadata:

| VARIABLE      | DESCRIPCION                                            | DTYPE            | CLASE         | CATEGORIA   |
|---------------|-------------------------------------------------------|------------------|---------------|-------------|
| ID            | Identificador unico del siniestro                    | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| N_VICTIMAS    | Cantidad de víctimas                                  | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| FECHA         | Fecha en formato dd/mm/aaaa                            | [&lt;class 'str'&gt;] | Categorica | Ordinal     |
| AAAA          | Año                                                   | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| MM            | Mes                                                   | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| DD            | Día del mes                                           | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| HORA          | Hora del siniestro                                    | [&lt;class 'str'&gt;] | Categorica | Ordinal     |
| HH            | Franja horaria entera                                 | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| LUGAR         | Dirección del hecho                                   | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| TIPO_CALLE    | Tipo de arteria. Para intersecciones se clasifica... | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| CALLE         | Nombre de la arteria donde se produjo el hecho        | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| ALTURA        | Altura de la arteria donde se produjo el hecho        | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| CRUCE         | Cruce en caso de que sea una encrucijada              | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| DIRECCION     | Direccion en formato normalizado usig                | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| COMUNA        | Comuna de la ciudad (1 a 15)                          | [&lt;class 'int'&gt;] | Categorica | Nominal     |
| XY_(CABA)     | Geocodificación plana                                 | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| POS_X         | Longitud con separador punto. wgs84                  | [&lt;class 'str'&gt;] | Cuantitativa | Continua    |
| POS_Y         | Latitud con separador punto. wgs84                   | [&lt;class 'str'&gt;] | Cuantitativa | Continua    |
| PARTICIPANTES | Conjunción de víctima y acusado                      | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| VICTIMA       | Vehículo del fallecido, o bien peatón/a.              | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| ACUSADO       | Vehículo del acusado/a del hecho, sin implicar...    | [&lt;class 'str'&gt;] | Categorica | Nominal     |

#### Quantitative Variables

Please query the following table for the dataset Quantitative Variables:

| VARIABLE      | DESCRIPCION                                            | DTYPE            | CLASE         | CATEGORIA   |
|---------------|-------------------------------------------------------|------------------|---------------|-------------|
| N_VICTIMAS    | Cantidad de víctimas                                  | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| AAAA          | Año                                                   | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| MM            | Mes                                                   | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| DD            | Día del mes                                           | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| HH            | Franja horaria entera                                 | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| ALTURA        | Altura de la arteria donde se produjo el hecho        | [&lt;class 'int'&gt;] | Cuantitativa | Discreta    |
| POS_X         | Longitud con separador punto. wgs84                  | [&lt;class 'str'&gt;] | Cuantitativa | Continua    |
| POS_Y         | Latitud con separador punto. wgs84                   | [&lt;class 'str'&gt;] | Cuantitativa | Continua    |

#### Qualitative Variables

Please query the following table for the dataset Qualitative Variables:

| VARIABLE      | DESCRIPCION                                            | DTYPE            | CLASE         | CATEGORIA   |
|---------------|-------------------------------------------------------|------------------|---------------|-------------|
| ID            | Identificador unico del siniestro                    | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| FECHA         | Fecha en formato dd/mm/aaaa                            | [&lt;class 'str'&gt;] | Categorica | Ordinal     |
| HORA          | Hora del siniestro                                    | [&lt;class 'str'&gt;] | Categorica | Ordinal     |
| LUGAR         | Dirección del hecho                                   | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| TIPO_CALLE    | Tipo de arteria. Para intersecciones se clasif...     | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| CALLE         | Nombre de la arteria donde se produjo el hecho        | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| CRUCE         | Cruce en caso de que sea una encrucijada              | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| DIRECCION     | Direccion en formato normalizado usig                | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| COMUNA        | Comuna de la ciudad (1 a 15)                          | [&lt;class 'int'&gt;] | Categorica | Nominal     |
| XY_(CABA)     | Geocodificación plana                                 | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| PARTICIPANTES | Conjunción de víctima y acusado                      | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| VICTIMA       | Vehículo del fallecido, o bien peatón/a.              | [&lt;class 'str'&gt;] | Categorica | Nominal     |
| ACUSADO       | Vehículo del acusado/a del hecho, sin implicar...    | [&lt;class 'str'&gt;] | Categorica | Nominal     |

### Null Values Management

The Dataset tagged every null value by default with the 'SD' tag, which means 'Sin Dato'. Nevertheless, some columns had still empty values that needed to be managed. In the following table null values state for each dataset column are showed prior to the null values treatment:

| Column        | No_Null_% | No_Null_Qty | Null_% | Null_Qty |
|---------------|-----------|-------------|--------|----------|
| ID            | 100.00    | 696         | 0.00   | 0        |
| N_VICTIMAS    | 100.00    | 696         | 0.00   | 0        |
| FECHA         | 100.00    | 696         | 0.00   | 0        |
| AAAA          | 100.00    | 696         | 0.00   | 0        |
| MM            | 100.00    | 696         | 0.00   | 0        |
| DD            | 100.00    | 696         | 0.00   | 0        |
| HORA          | 100.00    | 696         | 0.00   | 0        |
| HH            | 100.00    | 696         | 0.00   | 0        |
| LUGAR         | 100.00    | 696         | 0.00   | 0        |
| TIPO_CALLE    | 100.00    | 696         | 0.00   | 0        |
| CALLE         | 99.86     | 695         | 0.14   | 1        |
| ALTURA        | 18.53     | 129         | 81.47  | 567      |
| CRUCE         | 75.43     | 525         | 24.57  | 171      |
| DIRECCION     | 98.85     | 688         | 1.15   | 8        |
| COMUNA        | 100.00    | 696         | 0.00   | 0        |
| XY_(CABA)     | 100.00    | 696         | 0.00   | 0        |
| POS_X         | 100.00    | 696         | 0.00   | 0        |
| POS_Y         | 100.00    | 696         | 0.00   | 0        |
| PARTICIPANTES | 100.00    | 696         | 0.00   | 0        |
| VICTIMA       | 100.00    | 696         | 0.00   | 0        |
| ACUSADO       | 100.00    | 696         | 0.00   | 0        |

For the EDA process, Null values were imputed with the 'SD' tag. However, considering the small quantity of null values in **CALLE** and **DIRECCION** columns, this records will be removed for the dashboard construction.

Due to the high amount of null values in the **ALTURA** column, this column will be removed for the dashboard construction.

The **CRUCE** column was imputed with the 'SD' tag.

## EDA Structuration

![road acc map](src/road_accidents_map.png)