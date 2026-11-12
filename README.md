
# 🧬 Análisis de Secuencias de ADN

### Proyecto de Bioinformática | Python & R

Proyecto orientado al desarrollo de una herramienta bioinformática para el **análisis automatizado de secuencias de ADN**, combinando Python para el procesamiento de secuencias biológicas y R para el análisis estadístico y la visualización de resultados.

La aplicación permitirá a los usuarios introducir secuencias de ADN, caracterizar su composición nucleotídica, identificar posibles regiones codificantes, traducirlas a aminoácidos y compararlas con secuencias disponibles en bases de datos biológicas.

Además, el proyecto incorporará análisis evolutivos y filogenéticos para investigar la conservación de secuencias, las relaciones genéticas y los patrones evolutivos entre secuencias y organismos relacionados.

> **Estado del proyecto:** en fase de planificación y organización. Los módulos y funcionalidades descritos representan la estructura prevista de la aplicación y todavía no se consideran implementados.

---

## 🎯 Objetivos

### Objetivo general

Diseñar una herramienta bioinformática modular para el análisis de secuencias de ADN que facilite su caracterización molecular y la interpretación de los resultados.

### Objetivos específicos

- Validar secuencias de ADN introducidas por el usuario.
- Calcular la longitud y composición nucleotídica.
- Determinar el porcentaje de contenido GC.
- Obtener secuencias complementarias y reverso-complementarias.
- Identificar posibles marcos abiertos de lectura (ORF).
- Traducir regiones codificantes a secuencias de aminoácidos.
- Comparar secuencias con bases de datos mediante BLAST.
- Recuperar información biológica y funcional asociada a los genes y proteínas identificados.
- Investigar la conservación evolutiva y la variabilidad genética mediante el alineamiento múltiple de secuencias.
- Reconstruir e interpretar árboles filogenéticos para explorar las relaciones evolutivas.
- Realizar análisis estadísticos mediante R.
- Generar gráficos e informes de resultados.
- Aplicar Git y GitHub para el control de versiones y el trabajo colaborativo.

---

## 🔬 Funcionalidades previstas

| Funcionalidad | Descripción | Lenguaje |
|---|---|---|
| Validación de secuencias | Comprobación de nucleótidos válidos y formatos de entrada. | Python |
| Análisis nucleotídico | Cálculo de longitud y frecuencia de A, T, C y G. | Python |
| Contenido GC | Cálculo del porcentaje de guaninas y citosinas. | Python |
| Secuencias complementarias | Obtención de la complementaria y reverso-complementaria. | Python |
| Detección de ORF | Identificación de posibles marcos abiertos de lectura. | Python |
| Traducción a proteínas | Conversión de regiones codificantes a aminoácidos. | Python |
| Comparación con BLAST | Búsqueda de similitudes con secuencias biológicas conocidas. | Python |
| Identificación de secuencias homólogas |  Identificación de secuencias relacionadas y recuperación de información sobre los organismos de origen. | Python |
| Anotación funcional | Obtención de información sobre genes, proteínas, dominios y funciones biológicas asociadas. | Python |
| Alineamiento múltiple de secuencias (MSA) | Alineamiento de secuencias homólogas para identificar posiciones conservadas y variables. | Python |
| Análisis de conservación evolutiva | Evaluación de la conservación y variabilidad nucleotídica a lo largo de las secuencias alineadas. | Python y R  
| Reconstrucción de árboles filogenéticos | Construcción de árboles filogenéticos mediante métodos basados en distancias evolutivas o máxima verosimilitud. | Python
| Análisis de distancias genéticas | Cálculo y comparación de distancias evolutivas entre secuencias. | Python y R
| Evaluación del soporte filogenético | Estimación de la robustez de las ramas de los árboles mediante análisis bootstrap. | Python
| Interpretación filogenética | Identificación de grupos de secuencias relacionadas y estudio de sus relaciones evolutivas. | R
| Análisis estadístico | Estudio de la distribución y variabilidad de los resultados. | R |
| Comparación de secuencias | Comparación estadística de características entre secuencias. | R |
| Visualización | Elaboración de histogramas, diagramas de cajas y otros gráficos, así como visualización de patrones de conservación y árboles filogenéticos. | R |
| Generación de informes | Organización y presentación de los resultados obtenidos. | Python y R |

---

## 📂 Estructura del repositorio

```text
analisis-secuencias-adn/
│
├── data/                         # Datos de entrada
│   ├── example.fasta             # Secuencia de ADN de ejemplo
│   ├── reference.fasta           # Secuencias de referencia
│   └── metadata.csv              # Metadatos de las secuencias
│
├── src/                          # Código fuente Python
│   ├── main.py
│   ├── sequence_validation.py
│   ├── sequence_analysis.py
│   ├── sequence_complement.py
│   ├── orf_detection.py
│   ├── sequence_translation.py
│   ├── blast_analysis.py
│   ├── report_generator.py
│   ├── multiple_sequence_alignment.py  
│   ├── conservation_analysis.py        
│   └── phylogenetic_analysis.py        
│
├── R/                            # Scripts de análisis estadístico
│   ├── gc_statistics.R
│   ├── sequence_comparison.R
│   ├── visualization.R
│   ├── report_analysis.R
│   ├── sequence_quality.R
│   ├── conservation_analysis.R 
│   └── phylogenetic_tree.R     
│
├── test/                        # Pruebas del programa
│   ├── test_sequence_validation.py
│   ├── test_sequence_analysis.py
│   ├── test_multiple_sequence_alignment.py # NUEVO
│   ├── test_conservation_analysis.py       # NUEVO
│   └── test_phylogenetic_analysis.py
│
├── results/                      # Resultados de los análisis
│   ├── alignments/               # Alineamientos generados
│   ├── phylogenetic_trees/       # Árboles filogenéticos
│   └── reports/                  # Informes finales
│
├── docs/                         # Documentación técnica
│   ├── methodology.md            # Metodología del análisis
│   └── phylogenetics.md          # Metodología filogenética
│
├── .gitignore                    # Archivos excluidos de Git
├── LICENSE                       # Licencia del proyecto
├── README.md                     # Documentación principal
├── CHANGELOG.md                  # Registro de cambios
└── requirements.txt              # Dependencias de Python
```

**Nota:** esta estructura representa la organización prevista del proyecto. Algunos archivos de datos y componentes pueden estar pendientes de incorporación.

---

## 🚀 Instalación y ejecución

### Requisitos previos

Para utilizar el proyecto, será necesario disponer de las siguientes herramientas:

- **Python 3:** para ejecutar los módulos de análisis desarrollados en Python.
- **R:** para ejecutar los scripts de análisis estadístico y control de calidad.
- **Git:** para clonar el repositorio y gestionar las versiones del proyecto.

### Instalación

1. Clonar el repositorio de GitHub:

   ```bash
   git clone https://github.com/Christian-Salmeron/analisis-secuencias-adn.git
   ```

2. Acceder al directorio del proyecto:

   ```bash
   cd analisis-secuencias-adn
   ```

3. Instalar las dependencias necesarias para ejecutar los módulos y scripts, una vez estén definidas en el proyecto.

### Ejecución

El proyecto se encuentra actualmente en fase de desarrollo. Las instrucciones específicas para ejecutar cada módulo y funcionalidad se incorporarán a medida que se complete su implementación.

Los módulos de Python se encuentran en la carpeta `src/`, mientras que los scripts de R están organizados en la carpeta `R/`.

---

## 🐍 Módulos Python

Los archivos de la carpeta `src/` están destinados a implementar las funcionalidades principales de la aplicación.

| Archivo | Función prevista |
|---|---|
| `main.py` | Punto de entrada del programa y coordinación de los análisis. |
| `sequence_validation.py` | Validación de las secuencias según criterios de formato y contenido. |
| `sequence_analysis.py` | Cálculo de longitud, composición nucleotídica y contenido GC. |
| `sequence_complement.py` | Obtención de secuencias complementarias y reverso-complementarias. |
| `orf_detection.py` | Identificación de posibles marcos abiertos de lectura. |
| `sequence_translation.py` | Traducción de regiones codificantes a aminoácidos. |
| `blast_analysis.py` | Comparación de secuencias mediante BLAST. |
| `report_generator.py` | Generación de informes con los resultados bioinformáticos. |

Esta organización modular facilitará el desarrollo independiente de las funcionalidades y su posterior integración.

---

## 📊 Scripts R

Los scripts de la carpeta `R/` estarán orientados al procesamiento estadístico y a la visualización de los resultados procedentes de los análisis bioinformáticos.

| Archivo | Función prevista |
|---|---|
| `gc_statistics.R` | Análisis estadístico del contenido GC de diferentes secuencias. |
| `sequence_comparison.R` | Comparación de características de secuencias entre organismos o grupos. |
| `visualization.R` | Generación de gráficos e histogramas para representar los resultados. |
| `report_analysis.R` | Elaboración de informes estadísticos. |
| `sequence_quality.R` | Evaluación y resumen de parámetros de calidad de las secuencias. |

Se prevé utilizar archivos CSV como formato de intercambio de resultados entre Python y R.

---

## 🧪 Pruebas y validación

La carpeta `tests/` estará destinada a verificar el correcto funcionamiento de los módulos del programa.

Se contempla desarrollar pruebas automatizadas utilizando **pytest**.

### Pruebas previstas

- Validación de secuencias correctas e incorrectas.
- Comprobación de la longitud y el recuento de nucleótidos.
- Verificación del cálculo del contenido GC.
- Comprobación de secuencias complementarias y reverso-complementarias.
- Evaluación de la detección de ORF.
- Verificación de la traducción a aminoácidos.
- Comprobación de los formatos de salida e informes.

Las pruebas se implementarán una vez desarrolladas las funcionalidades correspondientes.

La planificación detallada se encuentra en `tests/README.md`.

---

## 🔄 Flujo de trabajo previsto

El funcionamiento de la aplicación se organizará en ocho etapas:

1. **Entrada de datos:** el usuario proporcionará una o varias secuencias de ADN, directamente o mediante archivos FASTA.
2. **Validación:** Python comprobará el formato y los nucleótidos de las secuencias.
3. **Análisis básico:** se calcularán longitud, composición nucleotídica y contenido GC.
4. **Procesamiento molecular:** se obtendrán las secuencias complementarias y se identificarán posibles ORF.
5. **Traducción:** las regiones codificantes seleccionadas podrán traducirse a aminoácidos.
6. **Comparación:** se realizarán búsquedas de similitud mediante BLAST.
7. **Análisis estadístico:** R procesará los resultados y generará representaciones gráficas.
8. **Generación de informes:** los resultados se organizarán en archivos y documentos para facilitar su interpretación.

---

## 🛠️ Tecnologías y herramientas previstas

### Lenguajes

- **Python 3:** procesamiento y análisis bioinformático.
- **R:** análisis estadístico y visualización.

### Bibliotecas y herramientas

| Herramienta | Aplicación prevista |
|---|---|
| Biopython | Lectura, manipulación y análisis de secuencias. |
| NCBI BLAST | Comparación de secuencias con bases de datos biológicas. |
| Biostrings | Manipulación de secuencias biológicas en R. |
| ggplot2 | Visualización estadística de resultados. |
| pytest | Pruebas automatizadas de Python. |
| Git | Control de versiones. |
| GitHub | Alojamiento y colaboración. |

### Gestión de dependencias

El archivo `requirements.txt` está destinado a recoger las dependencias necesarias para el entorno Python.

Las bibliotecas utilizadas en R se gestionarán por separado.

Las versiones definitivas se establecerán cuando se implementen y validen los módulos.

---

## 📁 Gestión de datos y resultados

### Carpeta `data/`

Almacenará las secuencias de ADN y sus metadatos.

Los formatos previstos incluyen:

- **FASTA (.fasta):** almacenamiento de secuencias biológicas.
- **CSV (.csv):** almacenamiento de metadatos asociados.

### Carpeta `results/`

Almacenará los resultados generados durante los análisis.

Los archivos previstos incluyen:

- Tablas CSV con características de las secuencias.
- Resultados de identificación de ORF.
- Resultados de comparaciones mediante BLAST.
- Gráficos generados con R.
- Informes finales.

### Carpeta `docs/`

Contendrá documentación técnica y metodológica complementaria, como descripciones de algoritmos, diagramas del flujo de trabajo y procedimientos de análisis.

---

## 📝 Historial de cambios

El archivo `CHANGELOG.md` está destinado a registrar las modificaciones y mejoras más relevantes del proyecto.

Permitirá documentar:

- Incorporación de nuevos módulos.
- Modificaciones de la estructura.
- Ampliación de funcionalidades.
- Actualizaciones de documentación.
- Correcciones y mejoras futuras.

Este registro complementará el historial de commits proporcionado por Git.

---

## 🤝 Control de versiones y colaboración

El proyecto utiliza **Git y GitHub** para facilitar el trabajo colaborativo entre los cuatro integrantes del equipo.

### Procedimiento de colaboración

1. **Repositorio principal:** centraliza la estructura y documentación del proyecto.
2. **Fork:** cada integrante puede crear una copia del repositorio en su cuenta.
3. **Commits:** los cambios se registran mediante confirmaciones con mensajes descriptivos.
4. **Pull Requests:** las modificaciones se proponen para su revisión e incorporación.
5. **Code Review:** los integrantes pueden revisar y comentar las contribuciones.
6. **Merge:** los cambios aprobados se integran en la rama principal.
7. **Sincronización:** los forks pueden actualizarse para incorporar cambios del repositorio original.

Este procedimiento permitirá conservar un historial de las modificaciones y facilitará la coordinación entre los integrantes del grupo.

---

## 🚧 Estado actual del proyecto

**Fase de planificación y organización del repositorio.**

Actualmente se ha planteado la arquitectura del proyecto y se han creado archivos correspondientes a los módulos Python y scripts R previstos.

También se ha preparado la estructura destinada al almacenamiento de datos, documentación, resultados y pruebas.

**Las funcionalidades del programa todavía no están implementadas ni validadas.** El repositorio constituye una propuesta inicial para un futuro desarrollo bioinformático.

---

## 🎓 Contexto académico

Este proyecto se desarrolla como parte de la actividad grupal **«GitHub: Crear un repositorio GitHub. Control de versiones»**, correspondiente a la asignatura **Introducción a la Programación Científica**, del Máster Universitario en Bioinformática de la **Universidad Internacional de La Rioja (UNIR)**.

La finalidad principal de esta actividad es adquirir experiencia práctica en:

- Creación y configuración de repositorios GitHub.
- Organización de proyectos de programación científica.
- Gestión de archivos y directorios.
- Registro y seguimiento de cambios.
- Trabajo colaborativo mediante forks y pull requests.
- Elaboración de documentación técnica.

---

## 📄 Licencia

Este proyecto se distribuye bajo la **licencia MIT**, cuyas condiciones pueden consultarse en el archivo `LICENSE`.
