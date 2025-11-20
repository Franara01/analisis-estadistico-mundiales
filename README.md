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
- requirements.txt      -> Dependencias (pandas, matplotlib, scipy, pingouin, etc.)
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
- Se documentan supuestos y limitaciones en la sección "Discusión" del notebook.

Licencia
--------
MIT

