# Pruebas automatizadas

Esta carpeta contiene las pruebas automatizadas destinadas a verificar el correcto funcionamiento de los diferentes módulos del programa de análisis de secuencias de ADN.

## Objetivos

- Comprobar que las funciones de Python producen resultados correctos.
- Detectar posibles errores en el procesamiento y análisis de secuencias.
- Verificar que los módulos funcionan correctamente después de realizar modificaciones.
- Facilitar el mantenimiento y la fiabilidad del programa.
- Comprobar la integración entre los diferentes módulos de análisis.

## Archivos de pruebas

| Archivo | Función prevista |
|---|---|
| `test_sequence_validation.py` | Comprobar la validación de secuencias de ADN, incluyendo su formato, longitud y composición nucleotídica. |
| `test_sequence_analysis.py` | Comprobar el análisis de secuencias, incluyendo el cálculo de la longitud, el recuento de nucleótidos y el contenido GC. |
| `test_sequence_complement.py` | Verificar la obtención de secuencias complementarias y reverso-complementarias. |
| `test_orf_detection.py` | Comprobar la identificación de posibles marcos abiertos de lectura (ORF). |
| `test_sequence_translation.py` | Verificar la traducción de secuencias de ADN a aminoácidos. |
| `test_report_generator.py` | Comprobar la generación y exportación de informes con los resultados de los análisis. |
| `test_multiple_sequence_alignment.py` | Comprobar la generación y calidad de los alineamientos múltiples de secuencias. |
| `test_conservation_analysis.py` | Comprobar la identificación de posiciones conservadas y variables en los alineamientos. |
| `test_phylogenetic_analysis.py` | Comprobar el cálculo de distancias genéticas y la reconstrucción de árboles filogenéticos. |

## Herramientas

Se utilizará **pytest**, un framework de Python que permite crear, organizar y ejecutar pruebas automatizadas.

Las pruebas podrán ejecutarse individualmente o en conjunto para verificar el funcionamiento de los diferentes módulos.

## Estado actual

Los archivos de pruebas están incorporados a la estructura del proyecto. La implementación de los casos de prueba y su ejecución se realizarán progresivamente, conforme se desarrollen y verifiquen las funcionalidades correspondientes.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Código fuente en Python](../src/README.md)
- [Datos de entrada](../data/README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Resultados del análisis](../results/README.md)
