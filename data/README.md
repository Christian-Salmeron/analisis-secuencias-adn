# Datos de entrada

Esta carpeta contiene los datos necesarios para el análisis de secuencias de ADN, organizados según su finalidad: datos de ejemplo, secuencias de entrada y secuencias de referencia.

## Archivos incluidos

| Archivo | Contenido |
|---|---|
| `example.fasta` | Dos secuencias artificiales de ADN para ilustrar el formato de entrada. |
| `metadata.csv` | Información descriptiva asociada a cada secuencia. |
| `inputs/` | Secuencias de ADN proporcionadas para el análisis. |
| `references/` | Secuencias de referencia utilizadas para búsquedas de similitud, alineamientos y análisis evolutivos. |
| `README.md` | Documentación de los datos y su uso previsto. |

## Datos de ejemplo 

Los archivos `example.fasta` y `metadata.csv` contienen dos secuencias artificiales que se utilizarán con fines educativos y para planificar las pruebas del programa.

Estas secuencias no representan organismos reales ni proceden de una base de datos biológica, por lo que no permiten extraer conclusiones biológicas sobre especies o muestras.


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

## Datos de entrada

La carpeta `inputs/` almacenará las secuencias de ADN proporcionadas por el usuario para realizar los diferentes análisis del proyecto.

Se podrán incorporar archivos en formato FASTA que deberán cumplir los criterios de formato y contenido establecidos por el programa.

Estas secuencias constituirán los datos principales sobre los que se realizarán los análisis de composición nucleotídica, identificación de regiones codificantes, traducción, búsquedas de similitud y análisis evolutivos.

## Secuencias de referencia

La carpeta `references/` contendrá secuencias de referencia procedentes de bases de datos biológicas públicas o de otros recursos documentados.

Se utilizarán para:

- Comparar las secuencias de entrada mediante búsquedas de similitud.
- Identificar secuencias homólogas.
- Realizar alineamientos múltiples de secuencias (MSA).
- Analizar la conservación evolutiva.
- Reconstruir e interpretar árboles filogenéticos.
- Cuando se incorporen secuencias de referencia, se documentarán su organismo de procedencia, número de acceso, base de datos de origen y fecha de descarga, siempre que esta información esté disponible.


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

Se mantendrá una separación entre las secuencias proporcionadas para el análisis (`inputs/`) y las secuencias utilizadas como referencia (`references/`).

Los resultados de los análisis se almacenarán en la carpeta `results/`.

## Estado actual

Los archivos de ejemplo están disponibles. Las carpetas `inputs/` y `references/` se utilizarán para organizar los futuros conjuntos de datos. La lectura, validación y análisis automatizados están pendientes de implementación.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Módulos de Python](../src/README.md)
- [Plan de pruebas](../test/README.md)
