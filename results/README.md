# Resultados del análisis

Esta carpeta está destinada a almacenar los resultados que genere el programa de análisis de secuencias de ADN.

## Estado actual

El proyecto se encuentra en fase de planificación. Todavía no se han ejecutado análisis ni generado resultados.

Los contenidos descritos a continuación son salidas previstas.

## Resultados previstos

| Resultado | Contenido |
|---|---|
| Análisis básico | Longitud, recuentos de A, T, C y G y porcentaje de contenido GC de cada secuencia. |
| Informe de validación | Registros vacíos, caracteres no permitidos y otras incidencias detectadas. |
| Secuencias complementarias | Secuencias complementarias y reverso-complementarias. |
| Detección de ORF | Posibles marcos abiertos de lectura y sus posiciones en las secuencias. |
| Traducción | Secuencias de aminoácidos obtenidas de las regiones seleccionadas. |
| Búsquedas de similitud | Resultados de BLAST, cuando se definan la herramienta, la base de datos y los parámetros. |
| Resúmenes y gráficos | Tablas estadísticas y representaciones generadas mediante R. |

## Formatos previstos

- **CSV:** tablas de características, indicadores de validación y resúmenes.
- **FASTA:** secuencias complementarias, reverso-complementarias y traducciones.
- **TXT:** informes de texto e incidencias.
- **PNG o PDF:** gráficos.

Los nombres y la estructura definitiva de los archivos se concretarán durante la implementación.

## Relación con los datos de entrada

Cada resultado conservará el identificador de la secuencia correspondiente para permitir su relación con los archivos de `data/`.

Los registros excluidos de un análisis deberán figurar en el informe de validación junto con el motivo de exclusión.

Los datos originales se conservarán en `data/`.

## Intercambio entre Python y R

Se prevé que los módulos de Python exporten tablas CSV con las características de las secuencias y los indicadores de validación.

Los scripts de R utilizarán estas tablas para elaborar resúmenes y gráficos, que también se almacenarán en esta carpeta.

## Reproducibilidad

Cuando se implementen los análisis, se documentarán:

- Los archivos de entrada utilizados.
- La versión del código o el commit correspondiente.
- Las versiones de las herramientas y dependencias.
- Los parámetros de ejecución.
- Las bases de datos y sus versiones, cuando corresponda.
- La fecha de ejecución.

Cualquier ejemplo de salida elaborado manualmente deberá identificarse como ilustrativo y distinguirse de los resultados generados por el programa.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Datos de entrada](../data/README.md)
- [Módulos de Python](../src/README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Plan de pruebas](../test/README.md)
