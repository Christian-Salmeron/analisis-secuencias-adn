# Metodología del análisis de secuencias de ADN

## Propósito

Este documento describe el flujo metodológico propuesto para analizar secuencias de ADN en formato FASTA. Las funciones se incorporarán y validarán durante el desarrollo del proyecto.

## Datos de entrada

El archivo FASTA contiene una o más secuencias. Cada registro comienza con una línea de encabezado que inicia con `>` y continúa con la secuencia de nucleótidos.

El archivo `data/example.fasta` contiene secuencias artificiales para probar el formato. No representan organismos ni proceden de una base de datos biológica. El archivo `data/metadata.csv` relaciona cada identificador FASTA con información descriptiva.

## Flujo de análisis previsto

1. **Lectura:** cargar cada registro FASTA y conservar su identificador.
2. **Validación:** comprobar que el archivo tenga encabezados y secuencias no vacías. La política para caracteres ambiguos se definirá antes de implementar el análisis.
3. **Análisis básico:** calcular la longitud, la frecuencia de A, T, C y G, y el contenido GC por secuencia.
4. **Procesamiento adicional:** calcular la secuencia complementaria y reverso-complementaria; identificar posibles marcos abiertos de lectura y traducir las regiones seleccionadas.
5. **Comparación:** realizar búsquedas de similitud mediante BLAST cuando se definan la herramienta, la base de datos y sus parámetros.
6. **Resumen y visualización:** organizar los resultados en tablas que puedan utilizarse en Python y R, y generar gráficos estadísticos cuando corresponda.

## Cálculo del contenido GC

El contenido GC se calculará como:

`GC (%) = (número de G + número de C) / longitud analizada × 100`

El tratamiento de caracteres ambiguos deberá quedar documentado cuando se implemente la función para evitar resultados inconsistentes.

## Reproducibilidad y alcance

Cada resultado deberá conservar el identificador de la secuencia analizada. Cuando se incorporen herramientas externas, también se documentarán sus versiones, parámetros y bases de datos utilizadas.

La estructura descrita representa el flujo previsto del proyecto; no implica que todas las funciones estén implementadas actualmente.
