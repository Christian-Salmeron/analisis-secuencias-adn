# Resultados del análisis

Esta carpeta está destinada a almacenar los resultados generados durante los diferentes análisis del proyecto de análisis de secuencias de ADN.

Los resultados se organizarán según su tipo, diferenciando los alineamientos, los árboles filogenéticos y los informes finales.

## Estructura de la carpeta

| Carpeta | Contenido |
|---|---|
| `alignments/` | Alineamientos múltiples de secuencias generados durante el análisis evolutivo. |
| `phylogenetic_trees/` | Árboles filogenéticos reconstruidos a partir de las secuencias analizadas. |
| `reports/` | Informes finales que integran los resultados de los diferentes análisis. |

## Estado actual

El proyecto se encuentra en fase de planificación y organización. Todavía no se han ejecutado análisis ni generado resultados.

Los contenidos descritos a continuación corresponden a salidas previstas y se incorporarán progresivamente durante el desarrollo del programa.

## Resultados previstos

| Resultado | Contenido |
|---|---|
| Análisis básico | Longitud, recuentos de A, T, C y G y porcentaje de contenido GC de cada secuencia. |
| Informe de validación | Registros vacíos, caracteres no permitidos y otras incidencias detectadas. |
| Secuencias complementarias | Secuencias complementarias y reverso-complementarias. |
| Detección de ORF | Posibles marcos abiertos de lectura y sus posiciones en las secuencias. |
| Traducción | Secuencias de aminoácidos obtenidas de las regiones seleccionadas. |
| Búsquedas de similitud | Resultados de BLAST, cuando se definan la herramienta, la base de datos y los parámetros. |
| Alineamientos múltiples | Alineamientos de secuencias homólogas generados mediante herramientas como MAFFT o MUSCLE. |
| Conservación evolutiva | Identificación de posiciones conservadas y variables y frecuencias nucleotídicas por posición. |
| Árboles filogenéticos | Reconstrucciones filogenéticas mediante métodos como Neighbor-Joining o Maximum Likelihood. |
| Resúmenes y gráficos | Tablas estadísticas y representaciones generadas mediante Python y R. |
| Informes finales | Documentos que integren los resultados y las principales conclusiones de los análisis. |

## Formatos previstos

- **CSV:** tablas de características, indicadores de validación, resultados estadísticos y resúmenes.
- **FASTA:** secuencias complementarias, reverso-complementarias y traducciones.
- **TXT:** informes de texto e incidencias.
- **FASTA, ALN o CLUSTAL:** archivos de alineamientos múltiples, según el formato de exportación utilizado.
- **Newick (NWK):** representación de árboles filogenéticos.
- **PNG o PDF:** gráficos, representaciones estadísticas y árboles filogenéticos.
- **TXT o PDF:** informes finales.

Los nombres y la estructura definitiva de los archivos se concretarán durante la implementación.

## Relación con los datos de entrada

Cada resultado conservará el identificador de la secuencia correspondiente para permitir su relación con los archivos de `data/`.

Se mantendrá la distinción entre las secuencias proporcionadas para el análisis, almacenadas en `data/inputs/`, y las secuencias de referencia, almacenadas en `data/references/`.

Los registros excluidos de un análisis deberán figurar en el informe de validación junto con el motivo de exclusión.

Los datos originales se conservarán en `data/` y no se modificarán durante el procesamiento.

## Intercambio entre Python y R

Se prevé que los módulos de Python exporten tablas CSV con las características de las secuencias, los indicadores de validación y los resultados de los análisis.

Los scripts de R utilizarán estas tablas para elaborar resúmenes, análisis estadísticos y representaciones gráficas. Los resultados generados se almacenarán en esta carpeta.

## Reproducibilidad

Para facilitar la trazabilidad y reproducibilidad de los análisis, se documentarán:

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
- [Análisis evolutivo y filogenético](../docs/phylogenetics.md)
- [Plan de pruebas](../test/README.md)
