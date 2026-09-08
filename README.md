# Factores asociados a la supervivencia de pasajeros del Titanic

Repositorio del proyecto desarrollado para la asignatura **MCDI503 - Exploración Inteligente para la Ciencia de Datos**. El trabajo corresponde al avance sumativo de la Fase 1 y presenta un análisis exploratorio reproducible del conjunto de datos `titanic` disponible en Seaborn.

## Integrantes

- Jennifer Nilo
- Patricio Núñez
- Grupo 08

## Objetivo del proyecto

Caracterizar la estructura y la calidad del conjunto de datos y describir cómo varía la supervivencia según el sexo registrado, la clase del pasaje, la edad, la tarifa, el contexto familiar y el puerto de embarque.

El análisis es descriptivo y exploratorio. Las asociaciones observadas no se interpretan como relaciones causales.

## Estructura del repositorio

```text
.
├── README.md
├── notebooks/
│   └── mcdi503_f1_sumativo_grupo08.ipynb
└── docs/
    └── mcdi503_f1_sumativo_grupo08.pdf
```

- `notebooks/`: contiene los notebooks ejecutados correspondientes a cada avance del proyecto.
- `docs/`: contiene los informes complementarios presentados en formato PDF.

El repositorio mantiene solamente estos dos directorios. Los archivos temporales, entornos virtuales, exportaciones de celdas y datos descargados durante la ejecución no deben incorporarse al control de versiones.

## Contenido del notebook

El notebook sigue una secuencia acumulativa:

1. Identificación y contexto del proyecto.
2. Configuración del entorno y registro de versiones.
3. Carga y validación del conjunto de datos.
4. Inspección estructural y diagnóstico de calidad.
5. Descripción estadística y visualizaciones preliminares.
6. Transformaciones exploratorias documentadas.
7. Respuesta a las cinco preguntas exploratorias.
8. Registro de decisiones y matriz de trazabilidad.
9. Supuestos, limitaciones y controles de reproducibilidad.
10. Cierre del avance y bibliografía.

## Reproducción en Google Colab

Google Colab es el entorno principal previsto para ejecutar el análisis.

### Requisitos

- Navegador web con acceso a Internet.
- Cuenta de Google para utilizar Google Colab.
- Acceso al archivo ubicado en `notebooks/`.

### Procedimiento

1. Descarga el repositorio o abre el notebook directamente desde GitHub.
2. Carga `notebooks/mcdi503_f1_sumativo_grupo08.ipynb` en Google Colab.
3. Reinicia el entorno de ejecución para descartar variables o estados conservados de una sesión anterior.
4. Selecciona **Entorno de ejecución > Ejecutar todas**.
5. Espera a que finalicen todas las celdas y comprueba que no existan mensajes de error.
6. Guarda o descarga el notebook ejecutado conservando sus salidas antes de entregarlo.

No es necesario cargar manualmente un archivo CSV. El conjunto de datos se obtiene durante la ejecución con:

```python
titanic_raw = sns.load_dataset("titanic")
```

La descarga depende de la conexión a Internet y de la disponibilidad del repositorio de datos utilizado por Seaborn.

## Verificaciones esperadas

Una ejecución correcta debe mostrar lo siguiente:

- Mensaje de carga completada desde Seaborn.
- Dimensiones de entrada iguales a **891 filas y 15 columnas**.
- Esquema de variables coincidente con el documentado en el notebook.
- Copia original `titanic_raw` conservada sin modificaciones.
- Vista analítica `titanic_eda` con las 891 filas originales.
- Evidencia ejecutada para las cinco preguntas exploratorias.
- Resultado final de **10 de 10 controles de reproducibilidad superados**.
- Ausencia de celdas con errores o ejecutadas fuera de secuencia.

Si falla una validación de dimensiones o columnas, no se debe eliminar la aserción. El error puede indicar un cambio en la fuente de datos y debe revisarse antes de continuar con el análisis.

## Entorno registrado

La ejecución utilizada para el avance sumativo registró las siguientes versiones:

| Componente | Versión o valor |
|---|---:|
| Python | 3.13.15 |
| pandas | 2.2.3 |
| NumPy | 2.1.3 |
| Seaborn | 0.13.2 |
| Matplotlib | 3.10.0 |
| Semilla | 42 |

Estas versiones sirven como referencia para comparar ejecuciones. El notebook utiliza librerías disponibles por defecto en Google Colab y no depende de rutas locales, archivos ocultos ni pasos manuales intermedios.

## Criterios de reproducibilidad aplicados

- La fuente se conserva en `titanic_raw` y las transformaciones se realizan sobre copias con nombres explícitos.
- Las dimensiones y columnas esperadas se validan antes de iniciar el EDA.
- Las transformaciones quedan registradas junto con su entrada, operación, salida y efecto.
- Los resultados numéricos incluidos en las interpretaciones se calculan desde el código.
- Las tasas se presentan junto con el número de registros utilizado.
- Los valores faltantes, grupos pequeños y valores extremos se mantienen visibles.
- El análisis debe ejecutarse de principio a fin para detectar dependencias ocultas entre celdas.
- Las decisiones, supuestos y limitaciones se documentan dentro del mismo notebook.

## Archivos de entrega

El notebook ejecutado es la evidencia técnica principal del proyecto. El informe almacenado en `docs/` funciona como síntesis y debe mantener correspondencia con las preguntas, decisiones, transformaciones, tablas, figuras y hallazgos presentados en el notebook.

Las fuentes bibliográficas y las citas en formato APA 7 utilizadas en el proyecto se encuentran dentro de ambos entregables.
