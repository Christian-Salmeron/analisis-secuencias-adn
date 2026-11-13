# Análisis evolutivo y filogenético previsto

## Estado actual y alcance

Este documento describe los procedimientos previstos para estudiar la conservación y las relaciones evolutivas entre secuencias homólogas de ADN.

Los procedimientos todavía no están implementados ni se han ejecutado. Las herramientas mencionadas son alternativas que se concretarán durante el desarrollo.

Las secuencias artificiales de ejemplo no se utilizarán para extraer conclusiones evolutivas sobre organismos reales.

## Selección de secuencias

Se prevé utilizar BLAST para buscar secuencias similares en bases de datos biológicas.

La selección de posibles secuencias homólogas considerará:

- Identidad y cobertura del alineamiento.
- E-value.
- Longitud y región comparada.
- Anotación y procedencia de cada secuencia.
- Ausencia de duplicados innecesarios.

Una coincidencia de BLAST servirá como evidencia para seleccionar candidatos; se comprobará que las secuencias correspondan a regiones comparables antes de reconstruir un árbol.

Las referencias seleccionadas se almacenarán en `data/references/`, documentando sus accesiones, organismos y fuentes.

## Alineamiento múltiple

Se prevé generar alineamientos mediante MAFFT o MUSCLE.

El alineamiento permitirá identificar:

- Posiciones conservadas.
- Sustituciones de nucleótidos.
- Huecos compatibles con inserciones o deleciones.
- Regiones de alineamiento incierto.

Antes del análisis filogenético se revisará la calidad del alineamiento. Cualquier exclusión de posiciones o secuencias deberá quedar documentada.

## Conservación

El módulo de conservación utilizará el alineamiento para calcular frecuencias nucleotídicas e identificar posiciones conservadas y variables.

Durante la implementación se definirán:

- La medida de conservación.
- Los umbrales utilizados.
- El tratamiento de huecos y bases ambiguas.
- Los criterios para considerar una posición válida.

## Reconstrucción filogenética

Se contemplan dos alternativas:

| Método | Procedimiento previsto |
|---|---|
| Neighbor-Joining | Reconstrucción a partir de una matriz de distancias genéticas. |
| Máxima verosimilitud | Reconstrucción mediante un modelo de evolución molecular. |

Para Neighbor-Joining se podrá utilizar el paquete `ape` de R. Para máxima verosimilitud se valorará el uso de IQ-TREE o FastTree.

La herramienta, el modelo y los parámetros definitivos se documentarán cuando se implemente el análisis.

## Soporte de las ramas

Se prevé evaluar el soporte mediante procedimientos adecuados al método seleccionado, como bootstrap.

Se registrarán el procedimiento y sus parámetros. Los valores de soporte se interpretarán como medidas de estabilidad o respaldo de las agrupaciones, sin presentarlos como una certeza absoluta.

## Interpretación

La interpretación considerará:

- Agrupaciones y clados.
- Longitudes de las ramas, cuando corresponda.
- Valores de soporte.
- Calidad y extensión del alineamiento.
- Limitaciones de las secuencias seleccionadas.

No se interpretará un árbol como enraizado salvo que se haya definido y justificado el procedimiento de enraizamiento.

## Exportación y visualización

| Archivo previsto | Contenido |
|---|---|
| FASTA o CLUSTAL | Alineamiento múltiple. |
| CSV | Medidas de conservación, distancias y resúmenes. |
| Newick | Árbol filogenético. |
| PNG o PDF | Representaciones gráficas. |

Los alineamientos se guardarán en `results/alignments/`, los árboles en `results/phylogenetic_trees/` y los informes en `results/reports/`.

Se prevé utilizar herramientas de R como `ape`, `ggtree` y `ggplot2` para la representación e interpretación de resultados.

## Reproducibilidad

Cada análisis registrará las secuencias utilizadas, las herramientas y versiones, los parámetros, el modelo evolutivo, el procedimiento de soporte y cualquier modificación del alineamiento.

## Documentación relacionada

- [Presentación general](../README.md)
- [Metodología prevista](metodologia.md)
- [Módulos de Python](../src/README.md)
- [Resultados previstos](../results/README.md)
