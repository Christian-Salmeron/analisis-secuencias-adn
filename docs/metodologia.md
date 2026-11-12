# Metodología del análisis de secuencias de ADN

## Propósito

Este documento describe el flujo metodológico propuesto para analizar secuencias de ADN en formato FASTA. Las funciones se incorporarán y validarán durante el desarrollo del proyecto.

## Datos de entrada

Los datos se organizarán en la carpeta `data/`, diferenciando tres tipos de recursos:

- **`data/example.fasta`:** contiene secuencias artificiales utilizadas para ilustrar el formato FASTA y planificar las pruebas del programa.
- **`data/inputs/`:** almacenará las secuencias proporcionadas por el usuario que se someterán a análisis.
- **`data/references/`:** contendrá secuencias de referencia procedentes de bases de datos biológicas públicas u otros recursos documentados.

El archivo `data/metadata.csv` contiene información descriptiva asociada a las secuencias de ejemplo. Para los nuevos conjuntos de datos se documentarán, cuando corresponda, los identificadores, el organismo de procedencia, los números de acceso y la fuente de obtención.

Cada registro FASTA comienza con una línea de encabezado que inicia con >, seguida de la secuencia de nucleótidos. Se utilizará el identificador situado antes del primer espacio de la cabecera para relacionar cada secuencia con sus metadatos y resultados.

## Flujo de análisis previsto

1. **Lectura:** cargar cada registro FASTA y conservar su identificador.
2. **Validación:** comprobar que el archivo tenga encabezados y secuencias no vacías. La política para caracteres ambiguos se definirá antes de implementar el análisis.
3. **Análisis básico:** calcular la longitud, la frecuencia de A, T, C y G, y el contenido GC por secuencia.
4. **Procesamiento adicional:** calcular la secuencia complementaria y reverso-complementaria; identificar posibles marcos abiertos de lectura y traducir las regiones seleccionadas.
5. **Comparación:** realizar búsquedas de similitud mediante BLAST cuando se definan la herramienta, la base de datos y sus parámetros.
6. **Análisis de conservación evolutiva:** evaluar el grado de conservación de las posiciones nucleotídicas a partir de los alineamientos múltiples.
7. **Reconstrucción e interpretación filogenética:** estimar las relaciones evolutivas entre las secuencias mediante la reconstrucción de árboles filogenéticos.
8. **Análisis estadístico y visualización:** organizar los resultados en tablas y representaciones gráficas mediante Python y R.
9. **Generación de informes:** integración de los resultados obtenidos en informes que permitan consultar y comparar los análisis realizados.

## Cálculo del contenido GC

El contenido GC se calculará como:

`GC (%) = (número de G + número de C) / longitud analizada × 100`

El tratamiento de caracteres ambiguos deberá quedar documentado cuando se implemente la función para evitar resultados inconsistentes.

## Reproducibilidad y alcance

Cada resultado deberá conservar el identificador de la secuencia analizada. Cuando se incorporen herramientas externas, también se documentarán sus versiones, parámetros y bases de datos utilizadas.

La estructura descrita representa el flujo previsto del proyecto; no implica que todas las funciones estén implementadas actualmente.
