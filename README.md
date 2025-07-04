## tfm-transformadores
# Trabajo de Fin de Máster - Pronóstico de demanda para transformadores de potencia en Chilquinta Transmisión

## Descripción del Proyecto

Este repositorio contiene el código y análisis desarrollado para el Trabajo de Fin de Máster enfocado en la predicción de demanda de potencia en transformadores eléctricos. El proyecto implementa y compara diferentes modelos de machine learning para predecir la potencia activa y reactiva en transformadores específicos.
## Transformadores Analizados

- **San Felipe T1**: Transformador con inversión de flujo
- **Valparaíso T1**: Transformador sin inversión de flujo

Para cada transformador se predicen:
- **Potencia Activa** (kW)
- **Potencia Reactiva** (kVAr)

## Tecnologías Utilizadas

- **Python**: Lenguaje principal
- **TensorFlow/Keras**: Para modelos LSTM
- **Prophet**: Para modelos de series temporales
- **Pandas**: Manipulación de datos
- **NumPy**: Operaciones numéricas
- **Matplotlib/Seaborn**: Visualización
- **Scikit-learn**: Métricas y preprocesamiento

## Estructura del Repositorio

### 📁 `limpieza-EDA/`
Análisis exploratorio y preprocesamiento de datos:

- `Limpieza_data_transformadores.ipynb` - Limpieza y preparación de datos de transformadores
- `Limpieza_data_meteorologica.ipynb` - Procesamiento de datos meteorológicos
- `Analisis_correlacion.ipynb` - Estudio de correlaciones entre variables

### 📁 `modelos/`
Contiene los modelos de predicción implementados:

- **Modelos LSTM**: Redes neuronales recurrentes para predicción de series temporales
  - `LSTM_San_Felipe_T1_P.ipynb` - Modelo LSTM para potencia activa del transformador San Felipe T1
  - `LSTM_san_Felipe_T1_Q.ipynb` - Modelo LSTM para potencia reactiva del transformador San Felipe T1
  - `LSTM_Valparaiso_T1_P.ipynb` - Modelo LSTM para potencia activa del transformador Valparaíso T1
  - `LSTM_Valparaiso_T1_Q.ipynb` - Modelo LSTM para potencia reactiva del transformador Valparaíso T1

- **Modelos Prophet**: 
  - `Modelos_Prophet_final_SanFelipe_Valparaiso.ipynb` - Modelos Prophet para transformadores San Felipe T1 y Valparaíso T1, potencia activa y reactiva
  - `Modelo_prophet_ValparaisoT1_p_q_mejoras.ipynb` - Optimizaciones y mejoras aplicadas a los modelos Prophet para Valparaíso T1 para potencia activa y ractiva
  - `Modelo_prophet_San_Felipe_p_mejoras.ipynb` - Optimizaciones y mejoras aplicadas a los modelos Prophet para la potencia activa del transformador San Felipe T1
  - `Modelo_prophet_San_Felipe_q_mejoras.ipynb` - Optimizaciones y mejoras aplicadas a los modelos Prophet para la potencia reactiva del transformador San Felipe T1

### 📁 `todos-transformadores/`
Aplicación de los mejores modelos a todos los transformadores:

- Modelos Prophet optimizados aplicados a todos los transformadores según su clasificación:
  - `Ejecución_no_invierte (P).ipynb`- Potencia activa para transformadores sin inversión de flujo
  - `Ejecucion_no_invierte_Q.ipynb`- Potencia reactiva para transformadores sin inversión de flujo
  - `Ejecucion_invierte_P.ipynb`- Potencia activa para transformadores con inversión de flujo
  - `Ejecucion_invierte_Q.ipynb`- Potencia reactiva para transformadores con inversión de flujo
  - `Ejecucion_invierte_Q_festivos.ipynb`- Potencia reactiva para transformadores con inversión de flujo solo festivos
 
### 📁 `tfm-transformadores/`
- `Errores_Chilquinta.ipynb` - Cálculo del error de Chilquinta para comparación y validación de modelos
- `Tratamiento outliers gráficas específicas por transformador.pdf`- Gráficas post tratamiento de outliers por transformador
