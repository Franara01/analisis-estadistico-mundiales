# Análisis Estadístico de Goles en Mundiales FIFA (2002-2022)

Autor: Francisco Ara

Contacto: ffranciscoara@gmail.com | https://www.linkedin.com/in/francisco-ara/

Repositorio: [https://github.com/Franara01/analisis-estadistico-mundiales/edit/main/README.md]

Resumen
-------
Análisis comparativo de la cantidad de goles por partido en Mundiales FIFA (masculino vs femenino) desde 2002.
El objetivo fue determinar si existen diferencias significativas en el promedio de goles por partido entre ambos torneos.

Contenido
---------
- notebook.ipynb        -> Notebook reproducible con todo el análisis
- notebook - Final Version.pdf -> Versión PDF lista para presentación. :contentReference[oaicite:0]{index=0}
- data/                 -> CSVs crudos (men_results.csv, women_results.csv)
- README.md             -> Este archivo

Qué hace el notebook
--------------------
1. Carga y limpieza de datos.
2. Filtrado: solo partidos de la Copa Mundial FIFA desde 2002.
3. Creación de la variable `total_goals = home_score + away_score`.
4. Visualizaciones: histogramas y estadísticas descriptivas.
5. Tests estadísticos:
   - Mann–Whitney U (no paramétrico)
   - Welch's t-test (paramétrico, alternativa 'greater')
6. Conclusión y discusión de resultados.

Resultados principales
----------------------
Ambas pruebas (no paramétrica y t-test de Welch) dieron p-value < 0.1, rechazando la hipótesis nula al 10%:
concluimos que, en este dataset y periodo, los partidos femeninos presentan en promedio más goles por partido.

Cómo reproducir
---------------
1. Clonar repo.
2. Colocar los CSV en `data/`.
3. Crear y activar virtualenv: `python -m venv venv && source venv/bin/activate`
4. `pip install -r requirements.txt`
5. Abrir `notebook.ipynb` y ejecutar todas las celdas, o ver `notebook - Final Version.pdf`.

Notas técnicas
--------------
- Tests: `pingouin.mwu` y `scipy.stats.ttest_ind` (Welch).
- Nivel de significancia usado: alpha = 0.1.





# Statistical Analysis of Goals in FIFA World Cups (2002–2022)

Author: Francisco Ara  
Contact: ffranciscoara@gmail.com | https://www.linkedin.com/in/francisco-ara/  
PDF Report: "notebook - Final Version.pdf" (included in this repository)

Overview
--------
This project analyzes whether women’s FIFA World Cup matches feature more goals per game than men’s World Cup matches, using official match results from 2002 onward.  
The analysis includes data cleaning, exploratory statistics, visualizations, and both parametric and non-parametric hypothesis testing.

The full research-style report is available in:  
**`notebook - Final Version.pdf`** (provided in this repository).  
It contains all explanations, charts, and statistical interpretations. :contentReference[oaicite:0]{index=0}

Repository Structure
--------------------
- `notebook.ipynb` — Reproducible Jupyter Notebook with all analysis steps  
- `notebook - Final Version.pdf` — Final polished report (presentation-ready)  
- `data/` — Raw datasets (men_results.csv, women_results.csv)  
- `requirements.txt` — Python dependencies  
- `README.md` — This file  

Objectives
----------
The main question addressed is:

**Do women’s World Cup matches have a higher average number of total goals than men’s World Cup matches?**

To test this, the project:

1. Filters the datasets to include only FIFA World Cup matches from 2002 onward.  
2. Computes `total_goals` for each match (home + away).  
3. Explores descriptive statistics and goal distributions.  
4. Performs:
   - **Mann–Whitney U test** (non-parametric)  
   - **Welch’s t-test** (parametric, unequal variances)

Both tests use a **significance level of α = 0.10**, matching the research hypothesis.

Key Results
-----------
Both statistical tests returned **p-values < 0.10**, which means:

> We reject the null hypothesis.  
> According to this

- Se documentan supuestos y limitaciones en la sección "Discusión" del notebook.

Licencia
--------
MIT

