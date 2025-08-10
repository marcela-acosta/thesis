# Enfoque Robusto de Machine Learning para Trading del SPY

Este repositorio contiene el código fuente, los notebooks de análisis y los resultados de la tesis de Maestría en Ciencia de Datos: *"Desarrollo y validación de un enfoque robusto y sistemático basado en machine learning, con el objetivo de optimizar la rentabilidad ajustada por riesgo del SPY, desde la perspectiva del inversor minorista"*.

## Resumen del Proyecto

Este trabajo diseña y valida un flujo de trading cuantitativo completo, fundamentado en las mejores prácticas de las finanzas algorítmicas modernas. A diferencia de los enfoques tradicionales basados en series de tiempo calendáricas, nuestra metodología se centra en el **muestreo basado en eventos** para filtrar el ruido del mercado y mejorar la robustez estadística de los modelos.

El objetivo final es construir una estrategia que supere a un *benchmark* pasivo (Buy and Hold) no necesariamente en rentabilidad absoluta, sino en métricas de desempeño ajustado por riesgo, como el Ratio de Sharpe y, crucialmente, la reducción del Maximum Drawdown (MDD).

## Metodología Clave

El flujo de trabajo implementado incluye:
- **Muestreo Basado en Eventos:** Transformación de la serie de precios del SPY en "barras informativas" basadas en umbrales de volatilidad (ATR), siguiendo los principios de López de Prado.
- **Modelos Ocultos de Markov (HMM):** Identificación de regímenes de mercado (ej. alta/baja volatilidad) como una variable predictora adicional.
- **Clasificación de Señales con XGBoost:** Uso de un modelo de Gradient Boosting para predecir la dirección del siguiente evento informativo.
- **Backtesting y Validación Rigurosa:** Implementación de validación cruzada con ventana rodante (*rolling window*) y un backtest realista que incluye costos transaccionales (comisiones y spread).

## Contenido del Repositorio

- Contiene los Jupyter Notebooks con el análisis exploratorio, el modelado y la validación.

## Autores

- **Marcela Paula Acosta Burguete**
- **Jorge Martín Coronel Caticha**

Tutor: **Franco Donnangelo**
