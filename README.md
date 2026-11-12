# Análisis de secuencias de ADN

Proyecto académico colaborativo de la asignatura Introducción a la Programación Científica del Máster Universitario en Bioinformática de UNIR.

El proyecto propone desarrollar herramientas en Python y R para analizar secuencias de ADN. La actividad actual se centra en crear, organizar y documentar el repositorio y utilizar Git y GitHub para el control de versiones y la colaboración.

## Estado actual

El proyecto se encuentra en fase de planificación y organización.

Actualmente se dispone de:

- Una estructura de carpetas para código, datos, documentación, pruebas y resultados.
- Dos secuencias artificiales de ejemplo y sus metadatos.
- Archivos Python y R con descripciones de sus funciones previstas.
- Documentación del flujo de análisis y de las pruebas previstas.
- Un historial de cambios y contribuciones mediante commits y pull requests.

Los módulos de análisis y las pruebas automatizadas están pendientes de implementación. Todavía no hay un programa funcional ejecutable ni resultados de análisis generados.

## Objetivos

- Organizar un proyecto de bioinformática de forma clara y coherente.
- Utilizar Git y GitHub para registrar, revisar e integrar cambios.
- Facilitar la colaboración entre los integrantes del equipo.
- Documentar los datos, los módulos y el flujo de trabajo previsto.
- Planificar herramientas para validar, analizar y comparar secuencias de ADN.

## Estructura del repositorio

| Ruta | Contenido |
|---|---|
| `src/` | Módulos previstos de Python y documentación del código. |
| `R/` | Scripts previstos para resúmenes estadísticos, comparación y visualización. |
| `data/` | Secuencias artificiales de ejemplo, metadatos y documentación de entrada. |
| `docs/` | Metodología prevista del análisis. |
| `results/` | Documentación de las salidas previstas y ubicación futura de los resultados. |
| `test/` | Documentación de las pruebas previstas. |
| `README.md` | Presentación general del proyecto. |
| `CHANGELOG.md` | Historial de versiones y cambios del proyecto. |
| `requirements.txt` | Archivo reservado para las dependencias de Python. |
| `.gitignore` | Reglas para excluir archivos temporales y otros archivos innecesarios del control de versiones. |
| `LICENSE` | Licencia MIT. |

## Módulos previstos de Python

| Archivo | Función prevista |
|---|---|
| `src/main.py` | Coordinar el flujo del programa y los análisis seleccionados. |
| `src/sequence_validation.py` | Validar el formato FASTA y el contenido de las secuencias. |
| `src/sequence_analysis.py` | Calcular longitud, composición nucleotídica y contenido GC. |
| `src/sequence_complement.py` | Obtener secuencias complementarias y reverso-complementarias. |
| `src/orf_detection.py` | Identificar posibles marcos abiertos de lectura (ORF). |
| `src/sequence_translation.py` | Traducir las regiones seleccionadas a secuencias de aminoácidos. |
| `src/blast_analysis.py` | Realizar búsquedas de similitud mediante BLAST. |
| `src/report_generator.py` | Organizar y exportar resultados e incidencias. |

Consulta la [documentación de los módulos de Python](src/README.md).

## Scripts previstos de R

| Archivo | Función prevista |
|---|---|
| `R/gc_statistics.R` | Elaborar resúmenes estadísticos del contenido GC. |
| `R/sequence_comparison.R` | Comparar características entre secuencias y, cuando existan metadatos apropiados, entre grupos o especies. |
| `R/sequence_quality.R` | Resumir indicadores de calidad básica, como bases ambiguas, registros vacíos o posibles duplicados. |
| `R/visualization.R` | Generar gráficos de las características analizadas. |
| `R/report_analysis.R` | Elaborar informes estadísticos a partir de los resultados de Python. |

El control de calidad previsto no incluye puntuaciones Phred, ya que los archivos FASTA no contienen puntuaciones de calidad de lectura.

## Flujo de trabajo previsto

1. Leer los registros de un archivo FASTA y conservar sus identificadores.
2. Validar su formato y los caracteres de las secuencias.
3. Calcular la longitud, la composición nucleotídica y el contenido GC.
4. Ejecutar los análisis adicionales seleccionados: secuencias complementarias, detección de ORF, traducción o búsquedas mediante BLAST.
5. Exportar tablas de resultados e incidencias.
6. Utilizar las tablas en R para elaborar resúmenes, comparaciones y gráficos.

Los registros excluidos de un análisis deberán conservarse en el informe de validación junto con el motivo de exclusión.

Las políticas para caracteres ambiguos y los parámetros de los análisis adicionales se concretarán antes de su implementación.

Consulta la [metodología prevista](docs/metodologia.md).

## Datos de ejemplo

La carpeta `data/` contiene:

- [`example.fasta`](data/example.fasta): dos secuencias artificiales de ADN.
- [`metadata.csv`](data/metadata.csv): información descriptiva asociada a sus identificadores.

Estas secuencias tienen una finalidad educativa. No representan organismos reales ni proceden de una base de datos biológica.

Consulta la [documentación de los datos](data/README.md).

## Resultados previstos

Las salidas previstas incluyen:

- Tablas de longitud, composición nucleotídica y contenido GC.
- Informes de validación.
- Secuencias complementarias y reverso-complementarias.
- Posibles ORF y traducciones de las regiones seleccionadas.
- Resultados de búsquedas de similitud.
- Resúmenes estadísticos y gráficos.

Se almacenarán en `results/` y conservarán los identificadores de las secuencias de entrada.

Actualmente no se han generado resultados. Consulta la [documentación de las salidas previstas](results/README.md).

## Cómo obtener el proyecto

### Clonar con Git

Es necesario disponer de Git para utilizar esta opción.

```bash
git clone https://github.com/Christian-Salmeron/analisis-secuencias-adn.git
cd analisis-secuencias-adn
```

### Descargar como ZIP

1. Abrir el repositorio en GitHub.
2. Seleccionar **Code → Download ZIP**.
3. Descomprimir el archivo.

La descarga ZIP contiene los archivos del proyecto, pero no conserva el historial de Git.

## Uso actual y dependencias

Actualmente se puede consultar la documentación, explorar los datos de ejemplo y revisar la planificación de los módulos.

Los archivos Python y R contienen descripciones de funcionalidades previstas. Ejecutarlos no realiza los análisis descritos.

`requirements.txt` está reservado para las futuras dependencias de Python; actualmente no declara paquetes. Las dependencias y sus versiones, junto con las instrucciones de instalación y ejecución, se añadirán durante la implementación.

## Pruebas previstas

La carpeta `test/` contiene el plan inicial de pruebas. Se prevé utilizar `pytest` para comprobar aspectos como:

- Lectura y validación de registros FASTA.
- Detección de caracteres no permitidos.
- Cálculo de longitud, composición nucleotídica y contenido GC.
- Obtención de secuencias complementarias y reverso-complementarias.
- Detección de ORF y traducción.
- Generación de informes.

Las pruebas automatizadas todavía no están implementadas ni ejecutadas.

Consulta el [plan de pruebas](test/README.md).

## Colaboración y control de versiones

El historial del repositorio recoge las contribuciones del equipo y la integración de cambios mediante pull requests.

Para nuevas contribuciones, se propone:

1. Crear una rama para el cambio.
2. Modificar los archivos correspondientes.
3. Registrar los cambios con un mensaje de commit que explique la acción realizada.
4. Publicar la rama y abrir una pull request.
5. Revisar e integrar los cambios en `main`.

Los títulos y las descripciones de los commits deben reflejar el trabajo realizado y distinguir la documentación de la implementación de funcionalidades.

## Próximos pasos

- Concretar las políticas de validación y los formatos de intercambio.
- Implementar los módulos de Python.
- Desarrollar los scripts de R.
- Definir y documentar las dependencias.
- Incorporar y ejecutar pruebas automatizadas.
- Añadir ejemplos reproducibles de ejecución.
- Documentar los resultados y mantener actualizada la información del proyecto.

## Documentación

- [Módulos de Python](src/README.md)
- [Datos de entrada](data/README.md)
- [Metodología prevista](docs/metodologia.md)
- [Resultados previstos](results/README.md)
- [Plan de pruebas](test/README.md)
- [Historial de cambios](CHANGELOG.md)

## Equipo

- Nicole María Arias Espinoza.
- Inmaculada Martínez Olmo.
- Marta Ruiz Alcázar.
- Christian Salmerón Conde.

Las contribuciones pueden consultarse en el historial de commits y en las pull requests del repositorio.

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para conocer sus condiciones.
