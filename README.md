# Proyecto de Título: Modelo de Estimación de Retornos Ajustados para Acciones Ilíquidas

Memoria para optar al título de Ingeniera Civil Industrial en la Universidad Técnica Federico Santa María.

Profesor Guía: Werner Kristjanpoller

## Resumen
En la presente memoria se desarrolla un algoritmo capaz de realizar predicciones de los precios de las acciones de baja liquidez de 3 mercados latinoamericanos: Chile, Brasil y México. Los datos utilizados son los precios de cierre disponibles y volúmenes de transacción de las acciones que cotizan en la Bolsa de Comercio de Santiago, Bolsa de Valores de São Paulo y Bolsa Mexicana de Valores. 

**La necesidad de desarrollar un método de predicción diferente para las acciones de baja liquidez se debe a la falta de información que existe en días en los que no ocurre transacción**, por lo que se propone un modelo que ajusta los retornos para suplir esta falta de información, clasifica las acciones en quintiles según ILLIQ para identificar las que se pronosticarán y utiliza coeficientes que relacionan las acciones del quintil de mayor liquidez con las de menor liquidez y generar la predicción.

La predicción del modelo propuesto se compara con la del modelo CAPM mediante Model Confidence Set (MCS), de esto se obtiene que si se hubiera realizado el experimento solo utilizando el modelo propuesto se obtendrían en promedio el 77% los mejores modelos para MSE y 75% para MAPE, mientras que si se hubiera realizado solo con el modelo CAPM se obtendría en promedio el 75% de los mejores modelos para MSE y 68% para MAPE, mostrando cierta superioridad del modelo propuesto.



## Objetivos

* **Objetivo Principal:** Proponer un modelo de predicción de precios de acciones ilíquidas de la Bolsa de Santiago, São Paulo y México, con el fin de compararlo con el modelo CAPM.
* **Objetivos Específicos:**
    * Definir el criterio que se utilizará para clasificar las acciones como líquidas o ilíquidas mediante revisión bibliográfica.
    * Programar el algoritmo del modelo propuesto en el software R para obtener una predicción.
    * Comparar la predicción del modelo propuesto con la del modelo CAPM para evaluar su desempeño.



## Tecnologías y Herramientas Utilizadas

* **Lenguaje & Entorno:** R / Quarto (`.qmd`) / RStudio
* **Habilidades Utilizadas:**
    * Estructuras de datos: Matrices, dataframes, listas, etc.
    * Importación, limpieza y manipulación de datos: Utilizando librerías como `readr`,`tidyverse`, `dplyr` y `data.table`.
    * Condicionales `if`, iteraciones `for` y funciones.
    * Modelamiento mediante regresión lineal múltiple en ciclo `for` y entrenamiento y testeo de modelo.
    * Visualización de datos: Utilizando librerías como `ggplot2`.
    * Exportación de resultados como archivo de Excel.



## Metodología y Resultados

1. **Preprocesamiento de Datos:** Carga de datos, limpieza y ordenar dataframes.
2. **Medición de liquidez:** Identificación de acciones más y menos líquidas, cálculo de Amihud y sepación en quintiles según liquidez.
4. **Modelamiento:** Cálculo de retornos ponderados, cálculo de coeficientes para ajustar la regresión lineal, predicción mediante el modelo de regresión lineal múltiple ajustado con coeficientes y transformación de resultados a retornos no ponderados y finalmente a precios para comparación.
5. **Resultados Destacados:** La comparación de resultados del modelo propuesto y el modelo tradicional CAPM se realizó mediante Model Confidence Set (MCS), de esto se obtiene que si se hubiera realizado el experimento solo utilizando el modelo propuesto se obtendrían en promedio el 77% los mejores modelos para MSE y 75% para MAPE, mientras que si se hubiera realizado solo con el modelo CAPM se obtendría en promedio el 75% de los mejores modelos para MSE y 68% para MAPE, mostrando cierta superioridad del modelo propuesto.

## Estructura del Repositorio

```text
├── Memoria.qmd    # Documento Quarto con el código completo y anotaciones
├── README.md      # Presentación del proyecto
