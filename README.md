# 🚴 Evolución del rendimiento individual y colectivo en el Tour de Francia (2007–2026)

## 1. Descripción del proyecto

Este proyecto analiza la evolución del rendimiento individual y colectivo en el Tour de Francia masculino durante el periodo 2007–2026, mediante técnicas de análisis exploratorio e inferencial de datos.

El estudio busca identificar tendencias en el rendimiento de los ciclistas y equipos, considerando indicadores como la velocidad media, las diferencias de tiempo entre los primeros clasificados, la concentración de equipos en el Top 10 y la persistencia de los corredores en las posiciones destacadas.

## 2. Objetivo general

Analizar la evolución del rendimiento individual y colectivo en el Tour de Francia entre 2007 y 2026, mediante herramientas estadísticas y técnicas de análisis de datos.

## 3. Hipótesis y dimensiones de análisis

- **H1. Evolución de la velocidad media:** analizar si la velocidad media de los ganadores presenta una tendencia creciente a lo largo del periodo.
- **H2. Brechas temporales:** comparar las diferencias de tiempo entre el ganador y el segundo clasificado durante los periodos 2007–2016 y 2017–2026.
- **H3. Concentración de equipos:** estudiar descriptivamente la distribución de las posiciones del Top 10 entre los equipos participantes.
- **H4. Persistencia individual:** evaluar si haber conseguido previamente una posición en el Top 10 se relaciona con la posibilidad de repetir ese resultado.

Como análisis complementario, se estudia la relación entre la edad de los ciclistas y su velocidad media individual.

## 4. Fuentes de información

Se utilizaron principalmente las siguientes fuentes:

- **LeTourDataSet:** archivos históricos en formato CSV con información de corredores y etapas del Tour de Francia.
- **ProCyclingStats:** consulta y contraste de información histórica de corredores y competiciones.

Debido a que ProCyclingStats no permitía descargar directamente los datasets completos requeridos, fue necesario recopilar manualmente información complementaria.

Particularmente, las edades de los ciclistas se consultaron y copiaron año por año a Microsoft Excel. Posteriormente, los registros se organizaron, revisaron y convirtieron en datasets estructurados para su integración y análisis en Python.

## 5. Metodología

El proyecto se desarrolló en las siguientes etapas:

1. Obtención y recopilación de información.
2. Inspección y exploración de los datasets.
3. Limpieza y depuración de registros.
4. Tratamiento de valores ausentes e inconsistencias.
5. Integración de información de corredores y etapas.
6. Construcción de variables e indicadores de rendimiento.
7. Análisis exploratorio mediante estadísticas descriptivas y visualizaciones.
8. Análisis inferencial mediante modelos y pruebas estadísticas.
9. Interpretación de resultados y elaboración de conclusiones.

## 6. Principales resultados

- **H1:** se identificó una tendencia creciente de la velocidad media de los ganadores, con un incremento estimado de 0,1675 km/h por año (p = 0,000020).
- **H2:** no se encontraron diferencias estadísticamente significativas entre las brechas temporales de ambas décadas.
- **H3:** se observó una distribución desigual de las posiciones del Top 10 entre equipos. El análisis fue descriptivo.
- **H4:** la repetición del Top 10 fue mayor entre ciclistas que ya habían conseguido ese resultado, aunque el modelo GEE no confirmó una asociación estadísticamente significativa al 5 %.
- **Análisis complementario de edad:** no se encontró una asociación estadísticamente significativa entre la edad y la velocidad media individual.

## 7. Herramientas utilizadas

- Python.
- Jupyter Notebook.
- Pandas.
- NumPy.
- Statsmodels.
- Matplotlib.
- Microsoft Excel.
- Git y GitHub.

## 8. Estructura del proyecto

```text
Proyecto_EDA_Tour_de_Francia/
│
├── .venv/                         # Entorno virtual local (no se sube)
│
├── src/
│   ├── data/                       # Conjuntos de datos
│   ├── notebooks/                  # Notebooks complementarios
│   ├── utils/                      # Funciones auxiliares
│   ├── main.ipynb                  # Análisis exploratorio
│   ├── analisis_inferencial.ipynb  # Análisis inferencial
│   ├── ciclistas_2007_2026.csv
│   └── etapas_2007_2026.csv
│
├── docs/                           # Documentación y entregables
│   ├── Memoria_Proyecto_Tour_de_Francia.pdf
│   ├── Memoria_Proyecto_Tour_de_Francia.docx
│   ├── Presentacion_Tour_de_Francia.pptx
│   └── Guion_Exposicion_20_diapositivas.docx
│
├── README.md                       # Documentación principal
└── .gitignore                      # Archivos excluidos de Git

```

*Nota: la estructura representa la organización prevista del proyecto. Los nombres y ubicaciones deberán coincidir con los archivos definitivos.*

## 9. Entorno de trabajo y reproducibilidad

El proyecto utiliza un entorno virtual de Python denominado `.venv`, destinado a gestionar de manera aislada las bibliotecas y dependencias necesarias para ejecutar los análisis.

Este entorno se mantiene localmente y no se incluye en el repositorio de GitHub, ya que contiene archivos específicos del equipo donde se desarrolló el proyecto.

Para reproducir el análisis en otro equipo, se recomienda crear un nuevo entorno virtual e instalar las bibliotecas necesarias.

En Windows, el entorno puede crearse mediante:

```bash
python -m venv .venv
```

Para activarlo:

```bash
.venv\Scripts\activate
```

Instalación de las principales bibliotecas utilizadas:

```bash
pip install pandas numpy matplotlib statsmodels jupyter
```

Los notebooks pueden ejecutarse desde Jupyter o mediante la extensión correspondiente de Visual Studio Code.

## 10. Limitaciones

El estudio está condicionado por la disponibilidad y consistencia de los registros históricos. La recopilación manual de edades requirió un proceso adicional de transcripción, organización y validación.

Asimismo, existen factores externos que pueden influir en el rendimiento, como el recorrido, el desnivel, las condiciones meteorológicas y las estrategias de competición, que no fueron incorporados directamente en todos los modelos.

## 11. Conclusiones

Los resultados muestran que la evolución del rendimiento en el Tour de Francia es multidimensional.

Aunque la velocidad media de los ganadores presenta una tendencia creciente, las brechas temporales, la concentración de equipos y la persistencia individual muestran comportamientos diferentes.

El proyecto permite aplicar herramientas de análisis exploratorio e inferencial para transformar datos históricos en información útil para comprender la evolución de la competición.

---

**Proyecto desarrollado como parte del Data Science Bootcamp 2026.**
