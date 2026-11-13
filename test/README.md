# Plan de pruebas

Esta carpeta contiene archivos reservados para las futuras pruebas automatizadas de los módulos del proyecto de análisis de secuencias de ADN.

## Estado actual

Las pruebas todavía no están implementadas ni ejecutadas. Los archivos existentes describen las comprobaciones previstas.

## Objetivos

- Comprobar que las funciones producen resultados correctos.
- Detectar errores en la validación y el análisis de secuencias.
- Verificar el funcionamiento de los módulos después de introducir cambios.
- Facilitar el mantenimiento del proyecto.

## Archivos incluidos

| Archivo | Comprobaciones previstas |
|---|---|
| `test_sequence_validation.py` | Validación del formato FASTA, detección de secuencias vacías y caracteres no permitidos. |
| `test_sequence_analysis.py` | Cálculo de longitud, recuentos de nucleótidos y contenido GC. |
| `test_multiple_sequence_alignment.py` | Generación de alineamientos múltiples y conservación de los identificadores y las secuencias de entrada. |
| `test_conservation_analysis.py` | Identificación de posiciones conservadas y variables a partir de un alineamiento. |
| `test_phylogenetic_analysis.py` | Cálculo de distancias genéticas y reconstrucción de árboles filogenéticos. |

## Herramientas previstas

Se prevé utilizar `pytest` para implementar y ejecutar las pruebas de Python.

Las dependencias y las instrucciones de ejecución se documentarán cuando existan casos de prueba funcionales.

## Alcance

Los archivos actuales constituyen un plan inicial y no cubren todos los módulos del proyecto. Su presencia no implica que las funcionalidades correspondientes estén implementadas o verificadas.

## Documentación relacionada

- [Presentación general del proyecto](../README.md)
- [Código fuente en Python](../src/README.md)
- [Datos de entrada](../data/README.md)
- [Metodología prevista](../docs/metodologia.md)
- [Resultados previstos](../results/README.md)
