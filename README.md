#  Monte Carlo Asset Risk Dashboard

Este repositorio contiene una **Aplicación Web interactiva** desarrollada en Python con **Streamlit**. La herramienta permite a inversores y analistas realizar simulaciones estocásticas de portafolios multivariados para cuantificar el riesgo de mercado de forma dinámica.



##  El Problema y la Solución
Los inversores suelen subestimar el riesgo al mirar solo rendimientos promedio. Esta aplicación resuelve ese problema permitiendo realizar **Stress Testing** mediante 5,000+ escenarios posibles, calculando el **Value at Risk (VaR)** en tiempo real.

##  Metodología Cuantitativa
La aplicación no solo genera números al azar; utiliza rigor matemático:
1. **Geometric Brownian Motion (GBM):** Modela la evolución de precios considerando el 'drift' y la volatilidad anualizada.
2. **Correlación de Cholesky:** A diferencia de simuladores básicos, este motor descompone la matriz de covarianza para asegurar que los activos simulados mantengan su correlación histórica real.
3. **Distribución de Probabilidad:** Genera un histograma final para identificar el "peor escenario" con niveles de confianza del 95% y 99%.



##  Stack de Tecnologías
* **Frontend:** Streamlit (Web UI)
* **Datos:** YFinance API (Precios históricos en tiempo real)
* **Cálculo:** NumPy (Álgebra lineal vectorizada) & Pandas
* **Gráficos:** Matplotlib (Visualización de densidades de probabilidad)

##  Cómo usar la App
1. Selecciona los activos de tu interés (Stocks o Cripto) en la barra lateral.
2. Ajusta el horizonte de tiempo y el número de simulaciones.
3. Analiza el gráfico de trayectorias y el cálculo de VaR para entender tu exposición al riesgo.

> **Accede a la App aquí:** [TU_LINK_DE_STREAMLIT_CLOUD_AQUÍ]

##  Conclusiones Técnicas
* **Escalabilidad:** El motor de cálculo está vectorizado, lo que permite procesar miles de rutas para portafolios complejos en segundos.
* **Interactividad:** El usuario puede "estresar" el modelo cambiando activos y viendo el impacto inmediato en el riesgo de cola (*tail risk*).
