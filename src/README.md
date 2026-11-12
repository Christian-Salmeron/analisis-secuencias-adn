# Código fuente en Python

Esta carpeta contiene los archivos previstos para desarrollar el análisis de secuencias de ADN en Python.

## Estado actual

El proyecto se encuentra en fase de planificación. Los archivos contienen comentarios que describen su función prevista; todavía no implementan los análisis.

## Módulos previstos

| Archivo | Función prevista |
|---|---|
| `main.py` | Coordinar la lectura, validación, análisis y generación de resultados según las opciones seleccionadas. |
| `sequence_validation.py` | Comprobar el formato FASTA, detectar registros vacíos y validar los caracteres de las secuencias. |
| `sequence_analysis.py` | Calcular la longitud, los recuentos de A, T, C y G y el porcentaje de contenido GC. |
| `sequence_complement.py` | Obtener las secuencias complementarias y reverso-complementarias. |
| `orf_detection.py` | Identificar posibles marcos abiertos de lectura (ORF). |
| `sequence_translation.py` | Traducir las regiones de ADN seleccionadas a secuencias de aminoácidos. |
| `blast_analysis.py` | Realizar búsquedas de similitud mediante BLAST, una vez definidos la herramienta, la base de datos y los parámetros. |
| `report_generator.py` | Organizar y exportar los resultados y las incidencias de validación. |

## Flujo de trabajo previsto

1. Recibir la ruta de un archivo FASTA y las opciones de análisis.
2. Leer los registros y conservar sus identificadores.
3. Validar el formato y el contenido de las secuencias.
4. Calcular las características básicas de las secuencias válidas.
5. Ejecutar los análisis adicionales seleccionados.
6. Exportar los resultados y las incidencias a la carpeta `results/`.

Las políticas para caracteres ambiguos, registros inválidos e identificadores repetidos se concretarán antes de implementar los módulos.

## Intercambio de resultados con R

Se prevé generar tablas CSV con un registro por secuencia, incluyendo su identificador, longitud, composición nucleotídica, contenido GC e indicadores de validación.

Los scripts de la carpeta `R/` utilizarán estas tablas para realizar resúmenes estadísticos y gráficos.

El módulo `blast_analysis.py` realizará búsquedas de similitud frente a una base de datos. El archivo `R/sequence_comparison.R` estará destinado a comparar las características calculadas de las secuencias.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Plan de pruebas](../test/README.md)

## Ejecución

Actualmente no hay un programa funcional ejecutable. Las instrucciones de instalación y ejecución se añadirán cuando los módulos estén implementados y verificados.
