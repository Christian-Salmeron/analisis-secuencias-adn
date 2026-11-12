# Datos de entrada

Esta carpeta contiene los datos de ejemplo del proyecto de análisis de secuencias de ADN.

## Archivos incluidos

| Archivo | Contenido |
|---|---|
| `example.fasta` | Dos secuencias artificiales de ADN para ilustrar el formato de entrada. |
| `metadata.csv` | Información descriptiva asociada a cada secuencia. |
| `README.md` | Documentación de los datos y su uso previsto. |

## Origen y finalidad

Las secuencias son artificiales y se utilizan con fines educativos y para planificar las pruebas del programa.

No representan organismos reales ni proceden de una base de datos biológica. No permiten extraer conclusiones biológicas sobre especies o muestras.

## Formato FASTA

Cada registro de `example.fasta` incluye:

- Una cabecera que comienza con `>`.
- Un identificador de secuencia seguido de una descripción.
- La secuencia de nucleótidos en las líneas siguientes.

Los identificadores utilizados son:

- `seq_sintetica_001`
- `seq_sintetica_002`

Se prevé utilizar como identificador el texto de la cabecera anterior al primer espacio. Este identificador permitirá relacionar cada secuencia con sus metadatos y resultados.

## Metadatos

El archivo `metadata.csv` contiene las siguientes columnas:

| Columna | Descripción |
|---|---|
| `sequence_id` | Identificador que coincide con el del registro FASTA. |
| `source` | Origen de la secuencia; en los ejemplos actuales, sintética. |
| `organism` | Organismo de procedencia; en los ejemplos actuales, «No aplica». |
| `sequence_type` | Tipo de secuencia; en este proyecto, ADN. |
| `notes` | Información adicional sobre la finalidad de la secuencia. |

## Validación prevista

Durante la implementación se comprobará:

- Que cada registro FASTA tenga una cabecera y una secuencia no vacía.
- Que los identificadores sean únicos.
- Que los identificadores del FASTA y de los metadatos coincidan.
- Que los caracteres de las secuencias cumplan la política de validación.

La política para bases ambiguas, como `N`, se definirá antes de implementar los análisis.

## Incorporación de nuevos datos

Los nuevos conjuntos de datos deberán documentar su origen, identificadores, formato y condiciones de uso.

Cuando procedan de una base de datos pública, se registrarán también sus números de acceso y la fecha de descarga.

Los resultados de los análisis se almacenarán en la carpeta `results/`.

## Estado actual

Los archivos de ejemplo están disponibles. Su lectura, validación y análisis automatizados están pendientes de implementación.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Módulos de Python](../src/README.md)
- [Plan de pruebas](../test/README.md)
