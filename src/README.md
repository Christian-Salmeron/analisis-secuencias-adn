# Código fuente en Python

Esta carpeta contiene los módulos destinados a desarrollar las funcionalidades de análisis de secuencias de ADN mediante Python.

## Estado actual

El proyecto se encuentra en fase de planificación y desarrollo. Los módulos describen las funcionalidades previstas para el programa, cuya implementación y validación se realizarán progresivamente.

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
| `multiple_sequence_alignment.py` | Generar alineamientos múltiples de secuencias homólogas (MSA) mediante herramientas como MAFFT o MUSCLE. |
| `conservation_analysis.py` | Analizar la conservación evolutiva a partir de los alineamientos, identificando posiciones conservadas, variables y frecuencias nucleotídicas. |
| `phylogenetic_analysis.py` | Calcular distancias genéticas y reconstruir árboles filogenéticos mediante métodos como Neighbor-Joining o Maximum Likelihood. |
| `report_generator.py` | Organizar y exportar los resultados de los análisis y las incidencias de validación. |

## Flujo de trabajo previsto

1. **Entrada de datos:** recibir las rutas de los archivos FASTA almacenados en `data/inputs/` y las opciones de análisis.
2. **Lectura:** cargar los registros y conservar sus identificadores.
3. **Validación:** comprobar el formato y el contenido de las secuencias.
4. **Análisis básico:** calcular la longitud, la composición nucleotídica y el contenido GC de las secuencias válidas.
5. **Procesamiento molecular:** obtener secuencias complementarias y reverso-complementarias, identificar ORF y realizar traducciones.
6. **Identificación y comparación:** realizar búsquedas de similitud mediante BLAST utilizando las secuencias de referencia de `data/references/`.
7. **Alineamiento múltiple:** alinear las secuencias homólogas seleccionadas.
8. **Conservación evolutiva:** identificar posiciones conservadas y variables en los alineamientos.
9. **Análisis filogenético:** calcular distancias genéticas y reconstruir árboles filogenéticos.
10. **Generación de resultados:** exportar tablas, alineamientos, árboles, gráficos e informes a la carpeta `results/`.

Las políticas para caracteres ambiguos, registros inválidos e identificadores repetidos se concretarán antes de implementar los módulos.

## Intercambio de resultados con R

Se prevé generar tablas CSV con un registro por secuencia, incluyendo su identificador, longitud, composición nucleotídica, contenido GC e indicadores de validación.

Los scripts de la carpeta `R/` utilizarán estas tablas para realizar resúmenes estadísticos, comparaciones y representaciones gráficas.

Los resultados de los análisis evolutivos también podrán utilizarse para generar visualizaciones de conservación y árboles filogenéticos mediante las herramientas disponibles en R.

El módulo `blast_analysis.py` estará destinado a realizar búsquedas de similitud frente a bases de datos de referencia, mientras que `R/sequence_comparison.R` permitirá comparar las características calculadas de las secuencias.

## Organización de los resultados

Los resultados generados por los módulos de Python se almacenarán en `results/`, siguiendo esta estructura:

| Carpeta | Contenido |
|---|---|
| `results/alignments/` | Alineamientos múltiples de secuencias. |
| `results/phylogenetic_trees/` | Árboles filogenéticos reconstruidos. |
| `results/reports/` | Informes finales y resultados integrados. |

Las tablas, estadísticas y otros archivos de salida podrán almacenarse directamente en `results/` o integrarse en los informes correspondientes.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Datos de entrada](../data/README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Análisis evolutivo y filogenético](../docs/phylogenetics.md)
- [Resultados del análisis](../results/README.md)
- [Plan de pruebas](../test/README.md)

## Ejecución

Actualmente no hay un programa funcional ejecutable. Las instrucciones de instalación y ejecución se añadirán cuando los módulos estén implementados y verificados.
