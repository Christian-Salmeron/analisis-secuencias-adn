
# 🧬 Análisis de Secuencias de ADN

### Proyecto de Bioinformática | Python

Este proyecto tiene como objetivo desarrollar una herramienta bioinformática en **Python** para el análisis automatizado de secuencias de ADN.

La aplicación permitirá introducir una secuencia de nucleótidos y realizar diferentes operaciones, desde el análisis de su composición hasta la identificación de posibles regiones codificantes y su comparación con secuencias biológicas conocidas.

---

## 🎯 Objetivos del proyecto

- Desarrollar una herramienta para el análisis automatizado de secuencias de ADN.
- Validar las secuencias introducidas por el usuario.
- Analizar la composición nucleotídica y calcular el contenido GC.
- Obtener secuencias complementarias y reverso-complementarias.
- Identificar posibles marcos abiertos de lectura (ORF).
- Traducir secuencias codificantes a aminoácidos.
- Comparar secuencias mediante herramientas bioinformáticas.
- Generar informes con los resultados obtenidos.
- Utilizar **Git y GitHub** para gestionar versiones y facilitar el trabajo colaborativo.

---

## 🔬 Funcionalidades previstas

| Funcionalidad | Descripción |
|---|---|
| Validación de secuencias | Comprobar que la secuencia introducida contiene nucleótidos válidos. |
| Análisis de composición | Calcular la longitud y contar los nucleótidos A, T, C y G. |
| Contenido GC | Determinar el porcentaje de guaninas y citosinas. |
| Secuencia complementaria | Obtener la secuencia complementaria y reverso-complementaria. |
| Identificación de ORF | Detectar posibles marcos abiertos de lectura. |
| Traducción a proteínas | Traducir posibles regiones codificantes a aminoácidos. |
| Comparación de secuencias | Buscar similitudes con secuencias de bases de datos mediante BLAST. |
| Generación de informes | Organizar y presentar los resultados obtenidos. |

---

## 📂 Estructura del repositorio

```text
analisis-secuencias-adn/
│
├── data/                       # Secuencias de ADN de entrada
│
├── src/                        # Código fuente del programa
│   ├── main.py
│   ├── sequence_validation.py
│   ├── sequence_analysis.py
│   ├── sequence_complement.py
│   ├── orf_detection.py
│   ├── sequence_translation.py
│   ├── blast_analysis.py
│   └── report_generator.py
│
├── tests/                      # Pruebas del programa (previstas)
├── results/                    # Resultados de los análisis
├── docs/                       # Documentación técnica
│
├── .gitignore                  # Archivos excluidos de Git
├── LICENSE                     # Licencia del proyecto
└── README.md                   # Documentación principal
```

Las carpetas `tests/` y `docs/` representan componentes previstos de la organización y pueden incorporarse o adaptarse según las necesidades del proyecto.

---

## 🧩 Organización del código fuente

El código fuente del proyecto se organiza en diferentes módulos Python dentro de la carpeta `src/`.

Cada módulo tendrá una responsabilidad específica, facilitando la organización, el mantenimiento y la futura ampliación del programa.

| Módulo | Función prevista |
|---|---|
| `main.py` | Programa principal que recibirá la secuencia de ADN y coordinará los análisis. |
| `sequence_validation.py` | Validará las secuencias introducidas y comprobará que contienen nucleótidos permitidos. |
| `sequence_analysis.py` | Calculará la longitud, la composición nucleotídica y el porcentaje GC. |
| `sequence_complement.py` | Generará las secuencias complementarias y reverso-complementarias. |
| `orf_detection.py` | Detectará posibles marcos abiertos de lectura (ORF). |
| `sequence_translation.py` | Traducirá las regiones codificantes a secuencias de aminoácidos. |
| `blast_analysis.py` | Permitirá comparar secuencias con bases de datos biológicas mediante BLAST. |
| `report_generator.py` | Generará informes con los resultados de los análisis. |

### Funcionamiento previsto

El programa seguirá un flujo de trabajo organizado:

1. **Entrada:** el usuario proporcionará una secuencia de ADN.
2. **Validación:** se comprobará que la secuencia tenga un formato válido.
3. **Análisis:** se calcularán sus principales características moleculares.
4. **Procesamiento:** se obtendrán secuencias complementarias, posibles ORF y traducciones a proteínas.
5. **Comparación:** se buscarán similitudes con secuencias conocidas mediante BLAST.
6. **Resultados:** se generará un informe con la información obtenida.

---

## 🛠️ Tecnologías previstas

- **Python 3:** lenguaje de programación principal.
- **Biopython:** biblioteca para el procesamiento y análisis de secuencias biológicas.
- **NCBI BLAST:** herramienta para comparar secuencias con bases de datos biológicas.
- **Git:** sistema de control de versiones.
- **GitHub:** plataforma para alojar y compartir el repositorio.

---

## 🚧 Estado del proyecto

**En fase de planificación y organización.**

Se ha definido la estructura del repositorio y se han incorporado los archivos correspondientes a los módulos previstos del programa.

Las funcionalidades bioinformáticas descritas todavía no están implementadas.

El desarrollo futuro contemplaría la programación de los módulos, su integración y la realización de pruebas para comprobar el correcto funcionamiento de la aplicación.

---

## 🤝 Control de versiones y colaboración

El proyecto utiliza **Git y GitHub** para organizar y gestionar su desarrollo colaborativo.

El flujo de trabajo contempla:

1. Creación de un repositorio principal compartido.
2. Realización de forks para trabajar sobre copias individuales.
3. Incorporación de cambios mediante commits descriptivos.
4. Propuesta de modificaciones mediante Pull Requests.
5. Revisión y fusión de los cambios en el repositorio principal.

Este procedimiento permite mantener un historial de modificaciones y facilita la colaboración entre los integrantes del equipo.

---

## 🎓 Contexto académico

Proyecto elaborado como parte de la actividad grupal **«GitHub: Crear un repositorio GitHub. Control de versiones»**, correspondiente a la asignatura **Introducción a la Programación Científica** del Máster Universitario en Bioinformática de la **Universidad Internacional de La Rioja (UNIR)**.

El objetivo principal de la actividad es familiarizarse con la creación y organización de repositorios, el registro de cambios mediante commits y la colaboración utilizando Git y GitHub.

---

## 📄 Licencia

Este proyecto se distribuye bajo la **licencia MIT**.
