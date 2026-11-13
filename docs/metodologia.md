# Metodología prevista

## Estado actual

Este documento describe el flujo propuesto para analizar secuencias de ADN. Los módulos todavía no están implementados y no se han generado resultados.

## Datos de entrada

Los datos se organizarán de la siguiente forma:

| Ruta | Contenido |
|---|---|
| `data/example.fasta` | Dos secuencias artificiales de ejemplo. |
| `data/metadata.csv` | Metadatos asociados a las secuencias de ejemplo. |
| `data/inputs/` | Secuencias proporcionadas por el usuario. |
| `data/references/` | Secuencias de referencia y documentación de su procedencia. |

Las secuencias artificiales servirán para ilustrar el formato de entrada y preparar pruebas. No permitirán extraer conclusiones sobre organismos reales.

Cada registro FASTA tendrá una cabecera que comience con `>`, seguida de su secuencia. Se utilizará como identificador el texto anterior al primer espacio de la cabecera.

## Flujo de análisis previsto

1. **Lectura:** cargar los registros FASTA y conservar sus identificadores.
2. **Validación:** comprobar cabeceras, secuencias vacías, identificadores repetidos y caracteres permitidos.
3. **Análisis básico:** calcular longitud, recuentos de nucleótidos y contenido GC.
4. **Procesamiento adicional:** obtener secuencias complementarias y reverso-complementarias, detectar ORF y traducir las regiones seleccionadas.
5. **Búsqueda de similitud:** comparar las secuencias mediante BLAST frente a una base de datos de referencia.
6. **Selección de secuencias:** seleccionar secuencias homólogas y documentar sus identificadores y procedencia.
7. **Alineamiento múltiple:** alinear las secuencias seleccionadas mediante herramientas como MAFFT o MUSCLE.
8. **Conservación:** identificar posiciones conservadas y variables a partir del alineamiento.
9. **Filogenia:** calcular distancias y reconstruir árboles a partir de alineamientos adecuados.
10. **Análisis estadístico y visualización:** elaborar resúmenes, comparaciones y gráficos mediante Python y R.
11. **Generación de informes:** integrar resultados, parámetros e incidencias.

Los análisis adicionales dependerán de las opciones seleccionadas y de que los datos sean adecuados para cada procedimiento.

## Validación y contenido GC

Antes de implementar los módulos se definirán las políticas para caracteres ambiguos, registros inválidos e identificadores repetidos.

El contenido GC se calculará como:

`GC (%) = (número de G + número de C) / número de posiciones consideradas × 100`

Se documentará qué posiciones forman parte del denominador y cómo se tratan las bases ambiguas. Las secuencias vacías no se utilizarán para este cálculo.

Los registros excluidos se conservarán en el informe de validación junto con el motivo de exclusión.

## Intercambio entre Python y R

| Formato previsto | Contenido |
|---|---|
| CSV | Características de las secuencias, indicadores de validación y resúmenes. |
| FASTA o CLUSTAL | Alineamientos múltiples. |
| Newick | Árboles filogenéticos. |

Python realizará el procesamiento y exportará los archivos necesarios. R los utilizará para elaborar resúmenes estadísticos y representaciones gráficas.

## Salidas previstas

Los resultados se almacenarán en `results/`:

- `alignments/`: alineamientos múltiples.
- `phylogenetic_trees/`: árboles y sus representaciones.
- `reports/`: informes y resultados integrados.
- La raíz de `results/`: tablas y otros archivos, según su finalidad.

Los datos originales de `data/` no se modificarán durante el procesamiento.

## Reproducibilidad

Cuando se implemente el proyecto, cada análisis documentará:

- Archivos de entrada e identificadores.
- Versión del código o commit.
- Herramientas y dependencias utilizadas.
- Parámetros y opciones seleccionadas.
- Bases de datos y sus versiones o fechas de consulta.
- Fecha de ejecución.
- Incidencias y criterios de exclusión.

## Documentación relacionada

- [Presentación general](../README.md)
- [Datos de entrada](../data/README.md)
- [Módulos de Python](../src/README.md)
- [Análisis filogenético previsto](phylogenetics.md)
- [Resultados previstos](../results/README.md)
- [Plan de pruebas](../test/README.md)
