# Análisis de secuencias de ADN

Proyecto académico colaborativo del Máster Universitario en Bioinformática de UNIR, orientado a organizar el desarrollo de herramientas para el análisis de secuencias de ADN mediante Python y R.

## Objetivos

- Crear y organizar un repositorio de un proyecto de bioinformática.
- Utilizar Git y GitHub para registrar cambios y colaborar.
- Documentar la estructura, los objetivos y el uso previsto del proyecto.
- Planificar módulos para la lectura, validación y análisis de secuencias de ADN.
- Separar el código, los datos, la documentación, las pruebas y los resultados.

## Estado del proyecto

El proyecto se encuentra en fase de planificación y organización.

Los archivos de los módulos describen las funcionalidades previstas y están pendientes de implementación. Su presencia en el repositorio no implica que esas funcionalidades puedan ejecutarse.

## Estructura del repositorio

| Archivo o carpeta | Contenido |
|---|---|
| `src/` | Módulos previstos para el análisis de secuencias mediante Python. |
| `R/` | Archivos destinados a análisis estadísticos y visualización mediante R. |
| `data/` | Datos de ejemplo y metadatos. |
| `docs/` | Documentación del proyecto. |
| `results/` | Carpeta destinada a los resultados de los análisis. |
| `test/` | Carpeta destinada a las pruebas del proyecto. |
| `README.md` | Presentación e instrucciones generales. |
| `requirements.txt` | Archivo destinado a recoger las dependencias de Python. |
| `.gitignore` | Reglas para excluir archivos temporales y otros archivos innecesarios del control de versiones. |
| `LICENSE` | Licencia MIT del proyecto. |

### Archivos destacados

- `data/metadata.csv`: archivo destinado a los metadatos asociados a las secuencias.
- `src/sequence_validation.py`: descripción del módulo previsto para validar secuencias de ADN.
- `src/sequence_complement.py`: descripción del módulo previsto para obtener secuencias complementarias y reverso-complementarias.
- `src/report_generator.py`: descripción del módulo previsto para generar informes de resultados.
- `test/gitkeep`: archivo con la documentación inicial de la carpeta de pruebas.

## Funcionalidades previstas

Las siguientes funcionalidades forman parte de la planificación:

- Lectura de secuencias de ADN en formato FASTA.
- Validación de las secuencias introducidas.
- Cálculo de la longitud y la composición de nucleótidos.
- Cálculo del porcentaje de guanina y citosina, o contenido GC.
- Obtención de secuencias complementarias y reverso-complementarias.
- Generación de informes.
- Análisis estadístico y representación gráfica mediante R.

### Secuencias complementarias

El módulo `sequence_complement.py` estará destinado a aplicar las correspondencias `A ↔ T` y `C ↔ G`.

Por ejemplo, para una secuencia original `5′-ATGC-3′`:

- Complementaria alineada: `3′-TACG-5′`.
- Reverso-complementaria escrita en sentido 5′ → 3′: `5′-GCAT-3′`.

## Tecnologías previstas

- **Python:** procesamiento y análisis de secuencias.
- **R:** análisis estadístico y visualización.
- **Git:** control de versiones.
- **GitHub:** alojamiento del repositorio y colaboración mediante ramas y pull requests.

Las bibliotecas y sus versiones se concretarán durante la implementación.

## Cómo obtener el proyecto

### Clonar con Git

```bash
git clone https://github.com/Christian-Salmeron/analisis-secuencias-adn.git
cd analisis-secuencias-adn
```

### Descargar como ZIP

1. Abrir el repositorio en GitHub.
2. Seleccionar **Code → Download ZIP**.
3. Descomprimir el archivo.

La descarga ZIP permite consultar los archivos, pero no incluye el historial de Git.

## Uso actual

Actualmente se puede explorar la estructura del repositorio y consultar la documentación de las funcionalidades previstas.

Todavía no se dispone de un programa completo ejecutable. Las instrucciones de instalación de dependencias y ejecución se incorporarán cuando los módulos estén implementados.

## Datos

La carpeta `data/` contiene los archivos de ejemplo y los metadatos del proyecto.

Los datos de ejemplo se utilizan con fines educativos. Al incorporar nuevos conjuntos de datos, deberán documentarse su origen, formato y condiciones de uso.

## Pruebas

La carpeta `test/` está reservada para las pruebas del proyecto y contiene documentación inicial en `test/gitkeep`.

Las pruebas automatizadas están pendientes de implementación. Se prevé comprobar, entre otros aspectos:

- La lectura correcta de archivos de secuencias.
- La detección de caracteres no válidos.
- El cálculo de la longitud y del contenido GC.
- La obtención de secuencias complementarias y reverso-complementarias.


## Próximos pasos

- Implementar los módulos descritos.
- Definir las dependencias necesarias.
- Añadir instrucciones de ejecución con ejemplos reproducibles.
- Incorporar pruebas automatizadas.
- Documentar los resultados obtenidos.
- Mantener el README actualizado conforme evolucione el proyecto.

## Autoría

Proyecto desarrollado de forma colaborativa por los cuatro integrantes del grupo.

Las contribuciones pueden consultarse en el historial de commits y en las pull requests del repositorio. Los titulares del copyright figuran en el archivo `LICENSE`.

## Licencia

Este proyecto se distribuye bajo la licencia MIT. Consulta el archivo [LICENSE](LICENSE) para conocer sus condiciones.
