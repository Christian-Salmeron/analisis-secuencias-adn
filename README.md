# Análisis de secuencias de ADN

Proyecto académico colaborativo de la asignatura Introducción a la Programación Científica del Máster Universitario en Bioinformática de UNIR.

El proyecto propone desarrollar una herramienta con Python y R para validar y caracterizar secuencias de ADN, buscar secuencias similares y estudiar su conservación y sus relaciones filogenéticas.

La actividad actual se centra en organizar y documentar el repositorio y utilizar Git y GitHub para el control de versiones y la colaboración.

## Estado actual

El proyecto está en fase de planificación y organización.

Actualmente incluye:

- Una estructura de carpetas para código, datos, documentación, pruebas y resultados.
- Dos secuencias artificiales de ejemplo y sus metadatos.
- Archivos Python y R con descripciones de sus funciones previstas.
- Documentación del flujo de trabajo.
- Un plan inicial de pruebas.
- Un historial de cambios.

Los módulos y las pruebas automatizadas todavía no están implementados. No hay un programa funcional que ejecute los análisis ni resultados generados.

## Objetivos

- Organizar y documentar un proyecto de bioinformática.
- Registrar, revisar e integrar cambios mediante Git y GitHub.
- Facilitar la colaboración del equipo.
- Validar secuencias y calcular sus características básicas.
- Identificar posibles regiones codificantes y traducirlas.
- Buscar secuencias similares mediante BLAST.
- Alinear secuencias homólogas y analizar su conservación.
- Reconstruir e interpretar árboles filogenéticos.
- Generar gráficos e informes mediante Python y R.

## Estructura del repositorio

| Ruta | Contenido |
|---|---|
| `src/` | Módulos previstos de Python y su documentación. |
| `R/` | Scripts previstos de análisis estadístico y visualización. |
| `data/` | Secuencias de ejemplo, metadatos y carpetas de entrada y referencia. |
| `docs/` | Metodología y planificación del análisis filogenético. |
| `results/` | Organización y documentación de las salidas previstas. |
| `test/` | Archivos y documentación del plan inicial de pruebas. |
| `README.md` | Presentación general del proyecto. |
| `CHANGELOG.md` | Historial de cambios. |
| `requirements.txt` | Archivo reservado para dependencias de Python. |
| `.gitignore` | Reglas de exclusión del control de versiones. |
| `LICENSE` | Licencia MIT. |

## Módulos previstos de Python

Los siguientes archivos se encuentran en `src/`:

| Archivo | Función prevista |
|---|---|
| `main.py` | Coordinar el flujo del programa. |
| `sequence_validation.py` | Validar registros FASTA y caracteres de las secuencias. |
| `sequence_analysis.py` | Calcular longitud, composición nucleotídica y contenido GC. |
| `sequence_complement.py` | Obtener secuencias complementarias y reverso-complementarias. |
| `orf_detection.py` | Detectar posibles marcos abiertos de lectura. |
| `sequence_translation.py` | Traducir regiones de ADN a aminoácidos. |
| `blast_analysis.py` | Realizar búsquedas de similitud mediante BLAST. |
| `multiple_sequence_alignment.py` | Generar alineamientos múltiples. |
| `conservation_analysis.py` | Identificar posiciones conservadas y variables. |
| `phylogenetic_analysis.py` | Coordinar el cálculo de distancias y la reconstrucción filogenética. |
| `report_generator.py` | Organizar y exportar resultados e incidencias. |

Consulta la [documentación de Python](src/README.md).

## Scripts previstos de R

Los siguientes archivos se encuentran en `R/`:

| Archivo | Función prevista |
|---|---|
| `gc_statistics.R` | Elaborar resúmenes del contenido GC. |
| `sequence_comparison.R` | Comparar características de secuencias y, cuando existan metadatos adecuados, de grupos. |
| `sequence_quality.R` | Resumir bases ambiguas, registros vacíos y posibles duplicados. |
| `conservation_analysis.R` | Representar la conservación y la variabilidad. |
| `phylogenetic_tree.R` | Representar y anotar árboles filogenéticos. |
| `visualization.R` | Generar gráficos de las características analizadas. |
| `report_analysis.R` | Elaborar informes estadísticos. |

El control de calidad previsto no incluye puntuaciones Phred, porque los archivos FASTA no contienen puntuaciones de calidad de lectura.

## Flujo de trabajo previsto

1. Leer los registros FASTA y conservar sus identificadores.
2. Validar el formato y el contenido de las secuencias.
3. Calcular longitud, composición nucleotídica y contenido GC.
4. Ejecutar los análisis adicionales seleccionados: secuencias complementarias, detección de ORF, traducción o BLAST.
5. Seleccionar secuencias homólogas y generar alineamientos múltiples.
6. Analizar posiciones conservadas y variables.
7. Reconstruir árboles filogenéticos cuando los datos sean adecuados.
8. Exportar resultados e incidencias.
9. Elaborar resúmenes y gráficos con R.
10. Integrar los resultados en informes.

Los registros excluidos deberán conservarse en el informe de validación junto con el motivo de exclusión.

Los criterios de validación, las herramientas y sus parámetros se concretarán durante la implementación.

Consulta la [metodología prevista](docs/metodologia.md) y el [análisis filogenético previsto](docs/phylogenetics.md).

## Datos

| Ruta | Contenido |
|---|---|
| [`data/example.fasta`](data/example.fasta) | Dos secuencias artificiales de ADN. |
| [`data/metadata.csv`](data/metadata.csv) | Metadatos asociados a los ejemplos. |
| [`data/inputs/`](data/inputs/) | Carpeta reservada para secuencias del usuario. |
| [`data/references/`](data/references/) | Carpeta reservada para secuencias de referencia. |

Las secuencias de ejemplo tienen finalidad educativa. No representan organismos reales ni permiten extraer conclusiones biológicas sobre especies.

Los datos originales se conservarán sin modificaciones durante el procesamiento.

Consulta la [documentación de los datos](data/README.md).

## Resultados e intercambio con R

Se prevé exportar:

- **CSV:** tablas de características, validación y resúmenes.
- **FASTA:** secuencias complementarias, reverso-complementarias y traducciones.
- **FASTA o CLUSTAL:** alineamientos múltiples.
- **Newick:** árboles filogenéticos.
- **PNG o PDF:** representaciones gráficas.
- **TXT o PDF:** informes.

Los archivos se organizarán de la siguiente forma:

| Ruta | Contenido previsto |
|---|---|
| `results/alignments/` | Alineamientos múltiples. |
| `results/phylogenetic_trees/` | Árboles filogenéticos y sus representaciones. |
| `results/reports/` | Informes y resultados integrados. |
| `results/` | Tablas y otros archivos de resultados, según su finalidad. |

Python exportará los archivos necesarios y R los utilizará para elaborar resúmenes y visualizaciones. Los resultados conservarán los identificadores de las secuencias correspondientes.

Actualmente no se han generado resultados.

Consulta la [documentación de resultados](results/README.md).

## Obtener el proyecto

### Con Git

Es necesario tener Git instalado.

```bash
git clone https://github.com/Christian-Salmeron/analisis-secuencias-adn.git
cd analisis-secuencias-adn
```

### Como ZIP

1. Abrir el repositorio en GitHub.
2. Seleccionar **Code → Download ZIP**.
3. Descomprimir el archivo.

La descarga ZIP no conserva el historial de Git.

## Uso actual y dependencias

Actualmente se puede consultar la documentación, explorar los datos de ejemplo y revisar la planificación de los módulos.

Los archivos Python y R describen funcionalidades previstas. No ejecutan los análisis documentados.

`requirements.txt` todavía no declara paquetes. Las dependencias, sus versiones y las instrucciones de ejecución se añadirán durante la implementación.

Entre las herramientas consideradas se encuentran BLAST, MAFFT o MUSCLE, IQ-TREE o FastTree y paquetes de R como `ape`, `ggtree` y `ggplot2`. Su selección definitiva queda pendiente.

## Pruebas previstas

La carpeta `test/` contiene estos archivos:

- `test_sequence_validation.py`
- `test_sequence_analysis.py`
- `test_multiple_sequence_alignment.py`
- `test_conservation_analysis.py`
- `test_phylogenetic_analysis.py`

Describen las comprobaciones previstas. Todavía no contienen pruebas automatizadas funcionales ni cubren todos los módulos.

Se prevé utilizar `pytest` durante la implementación.

Consulta el [plan de pruebas](test/README.md).

## Colaboración y control de versiones

Para contribuir:

1. Crear una rama para el cambio.
2. Modificar los archivos correspondientes.
3. Registrar los cambios mediante un commit descriptivo.
4. Publicar la rama y abrir una pull request.
5. Revisar e integrar los cambios en `main`.

Los mensajes de commit y las pull requests deberán distinguir entre documentación, planificación e implementación.

El historial de cambios se documenta en [CHANGELOG.md](CHANGELOG.md).

## Próximos pasos

- Definir criterios de validación y formatos de intercambio.
- Implementar los módulos de Python.
- Desarrollar los scripts de R.
- Seleccionar herramientas externas y documentar sus parámetros.
- Incorporar dependencias e instrucciones de ejecución.
- Implementar y ejecutar pruebas.
- Añadir ejemplos reproducibles y resultados documentados.

## Documentación

- [Módulos de Python](src/README.md)
- [Datos de entrada](data/README.md)
- [Metodología prevista](docs/metodologia.md)
- [Análisis filogenético previsto](docs/phylogenetics.md)
- [Resultados previstos](results/README.md)
- [Plan de pruebas](test/README.md)
- [Historial de cambios](CHANGELOG.md)

## Equipo

- Nicole María Arias Espinoza.
- Inmaculada Martínez Olmo.
- Marta Ruiz Alcázar.
- Christian Salmerón Conde.

Las contribuciones pueden consultarse en los commits y las pull requests.

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta [LICENSE](LICENSE).
