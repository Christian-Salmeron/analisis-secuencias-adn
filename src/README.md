# Código fuente en Python

Esta carpeta contiene los módulos previstos para desarrollar el análisis de secuencias de ADN.

## Estado actual

El proyecto se encuentra en fase de planificación y organización. Los archivos contienen descripciones de sus funciones previstas, pero todavía no incluyen una implementación funcional.

## Módulos incluidos

| Archivo | Función prevista |
|---|---|
| `main.py` | Coordinar la lectura, validación, análisis y exportación de resultados según las opciones seleccionadas. |
| `sequence_validation.py` | Comprobar el formato FASTA, detectar registros vacíos y validar los caracteres de las secuencias. |
| `sequence_analysis.py` | Calcular la longitud, los recuentos de nucleótidos y el porcentaje de contenido GC. |
| `sequence_complement.py` | Obtener las secuencias complementarias y reverso-complementarias. |
| `orf_detection.py` | Identificar posibles marcos abiertos de lectura (ORF). |
| `sequence_translation.py` | Traducir las regiones de ADN seleccionadas a secuencias de aminoácidos. |
| `blast_analysis.py` | Realizar búsquedas de similitud mediante BLAST. |
| `multiple_sequence_alignment.py` | Generar alineamientos múltiples de secuencias homólogas mediante herramientas como MAFFT o MUSCLE. |
| `conservation_analysis.py` | Identificar posiciones conservadas y variables y calcular frecuencias nucleotídicas a partir de los alineamientos. |
| `phylogenetic_analysis.py` | Calcular distancias genéticas y reconstruir árboles filogenéticos. |
| `report_generator.py` | Organizar y exportar los resultados y las incidencias de validación. |

## Flujo de trabajo previsto

1. **Entrada:** recibir la ruta de un archivo FASTA y las opciones de análisis.
2. **Lectura y validación:** cargar los registros, conservar sus identificadores y comprobar su formato y contenido.
3. **Análisis básico:** calcular la longitud, la composición nucleotídica y el contenido GC.
4. **Procesamiento adicional:** obtener secuencias complementarias, identificar ORF y traducir las regiones seleccionadas.
5. **Búsqueda de similitud:** comparar las secuencias mediante BLAST frente a una base de datos que se definirá durante la implementación.
6. **Selección y alineamiento:** seleccionar secuencias homólogas y generar un alineamiento múltiple.
7. **Conservación:** identificar posiciones conservadas y variables.
8. **Filogenia:** calcular distancias y reconstruir árboles a partir del alineamiento.
9. **Exportación:** guardar los resultados y las incidencias en `results/`.

Las secuencias proporcionadas por el usuario se almacenarán en `data/inputs/`. Las secuencias de referencia seleccionadas para los análisis se conservarán en `data/references/`, junto con la información de su procedencia.

Los criterios de validación, el tratamiento de caracteres ambiguos, las herramientas externas y sus parámetros se concretarán antes de implementar los módulos.

## Intercambio de resultados con R

Los módulos de Python exportarán los archivos necesarios para los análisis y las visualizaciones de R:

| Formato previsto | Contenido |
|---|---|
| CSV | Características de las secuencias, indicadores de validación y resúmenes de los análisis. |
| FASTA o CLUSTAL | Alineamientos múltiples de secuencias. |
| Newick | Árboles filogenéticos. |

Los scripts de `R/` utilizarán estos archivos para elaborar resúmenes estadísticos, comparaciones y representaciones gráficas.

## Organización de las salidas

| Ruta | Contenido previsto |
|---|---|
| `results/alignments/` | Alineamientos múltiples. |
| `results/phylogenetic_trees/` | Árboles filogenéticos y sus representaciones. |
| `results/reports/` | Informes y resultados integrados. |
| `results/` | Tablas y otros archivos de resultados, según su finalidad. |

Los resultados conservarán los identificadores de las secuencias de entrada. Los registros excluidos deberán figurar en el informe de validación con el motivo correspondiente.

## Pruebas previstas

La carpeta `test/` contiene archivos reservados para comprobar la validación, el análisis básico, los alineamientos, la conservación y la reconstrucción filogenética.

Las pruebas todavía no están implementadas y su alcance actual no cubre todos los módulos.

## Ejecución y dependencias

Actualmente no hay un programa funcional que ejecute este flujo de análisis.

Las dependencias, sus versiones y las instrucciones de instalación y ejecución se incorporarán cuando los módulos estén implementados y verificados.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Datos de entrada](../data/README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Análisis evolutivo y filogenético](../docs/phylogenetics.md)
- [Resultados previstos](../results/README.md)
- [Plan de pruebas](../test/README.md)
