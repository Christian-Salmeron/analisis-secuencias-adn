# Análisis Evolutivo y Filogenético

## 1. Introducción

Este documento describe la metodología utilizada para realizar análisis evolutivos y filogenéticos de secuencias de ADN, desde la identificación de secuencias homólogas hasta la reconstrucción e interpretación de árboles filogenéticos.

## 2. Obtención de secuencias homólogas

Las secuencias homólogas se identifican mediante la comparación de la secuencia de entrada con bases de datos biológicas públicas utilizando **BLAST**.

Los principales criterios de selección son:
- Porcentaje de identidad.
- Cobertura de la secuencia.
- Valor E-value.
- Similitud entre secuencias.

## 3. Alineamiento múltiple de secuencias (MSA)

Se realiza un alineamiento múltiple de las secuencias homólogas mediante herramientas como **MAFFT** o **MUSCLE**, con el objetivo de identificar:
- Posiciones conservadas.
- Regiones variables.
- Inserciones y deleciones (gaps).

## 4. Análisis de conservación evolutiva

Se evalúa el grado de conservación nucleotídica a partir del alineamiento, incluyendo:
- Identificación de posiciones conservadas y variables.
- Cálculo de frecuencias nucleotídicas.
- Estimación de los niveles de conservación por posición.

## 5. Reconstrucción de árboles filogenéticos

Se reconstruyen árboles filogenéticos para estudiar las relaciones evolutivas entre las secuencias mediante diferentes métodos:
- **Neighbor-Joining (NJ):** basado en distancias genéticas.
- **Máxima verosimilitud (ML):** basado en modelos de evolución molecular.

Se pueden utilizar herramientas como **IQ-TREE** o **FastTree**.

## 6. Evaluación del soporte de las ramas

La fiabilidad de las agrupaciones del árbol se evalúa mediante métodos de soporte como el **Bootstrap**, que permite estimar la estabilidad de las relaciones filogenéticas mediante remuestreo de las posiciones del alineamiento.

## 7. Interpretación filogenética

Se analizan los árboles obtenidos para identificar:
- Secuencias evolutivamente relacionadas.
- Agrupaciones y clados.
- Distancias genéticas.
- Patrones de divergencia evolutiva.
- Valores de soporte de las ramas.

## 8. Visualización y presentación de resultados

Los resultados se representan mediante herramientas como **ape**, **ggtree** y **ggplot2** en R.

El informe final incluirá:
- Secuencias analizadas y bases de datos utilizadas.
- Alineamiento múltiple.
- Resultados del análisis de conservación.
- Árbol filogenético reconstruido.
- Métodos y parámetros empleados.
- Interpretación de los principales resultados.

## 9. Herramientas principales

| Herramienta | Aplicación |
|---|---|
| BLAST | Identificación de secuencias homólogas |
| MAFFT / MUSCLE | Alineamiento múltiple |
| IQ-TREE / FastTree | Reconstrucción filogenética |
| ape / ggtree / ggplot2 | Análisis y visualización de árboles |

