# ![Python](https://img.shields.io/badge/Python-3.x-blue?style=flat-square) ![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat-square) ![pandas](https://img.shields.io/badge/pandas-Data%20Analysis-green?style=flat-square) ![License](https://img.shields.io/badge/License-MIT-gray?style=flat-square)

# Análisis de Ventas Ecovida 2023-2025

**Análisis integral de 192,831 transacciones para identificar oportunidades de crecimiento, optimización de mix de canales y mitigación del riesgo de concentración en retail. Cuantificación de impacto por gestor comercial y recomendaciones de pricing diferenciado basadas en rentabilidad versus volumen.**

---

## 📌 Contexto de Negocio

Ecovida (marca de Alimentos Claudet) es una empresa chilena especializada en alimentos saludables sin gluten y opciones light, operando a través de 12+ canales de distribución que incluyen retail masivo (Walmart, Cencosud), comercio electrónico, mayoristas independientes y comercio tradicional. Con ventas totales de **$21.3 mil millones CLP** en el período 2023-2025 y 29.5 millones de unidades distribuidas, el desafío crítico radica en balancear la dependencia del retail masivo (78% de ingresos en top 5 clientes) con la expansión de canales de menor concentración y mayor margen operacional.

---

## 🎯 Preguntas que Responde este Análisis

1. **¿Cuál es la contribución de ingresos y margen por canal de venta y cómo evolucionó en el período?**
   - Identificar canales rentables versus canales de volumen para rebalance de inversión comercial.

2. **¿Qué productos generan mayor rentabilidad versus volumen y existen oportunidades de mix de productos?**
   - Evaluar estrategia de pricing diferenciado entre líneas sin gluten, light y convencionales.

3. **¿Cuál es el desempeño de cada KAM y cómo impacta en la retención y crecimiento de clientes?**
   - Benchmarking de productividad y correlación entre diversificación de cartera y retención.

4. **¿Cómo optimizar la estrategia comercial considerando la alta concentración en Walmart y Cencosud?**
   - Plan de diversificación de riesgo y aceleración en canales digitales y mayoristas independientes.

---

## 📊 Estructura del Análisis

| # | Sección | Técnica | Insight Clave |
|---|---------|---------|---------------|
| 1 | Contexto de Negocio y Exploración de Datos | EDA, agregación temporal | Tendencia de ventas, estacionalidad, cobertura de canales y clientes |
| 2 | Contribución de Ingresos y Margen por Canal de Venta | Análisis de pareto, decomposición temporal | SPMK CADENA y FS RETAIL dominan volumen; DIGITAL y TRADICIONAL lideran margen |
| 3 | Rentabilidad versus Volumen: Análisis de Mix de Productos | Matriz margen-volumen, curva ABC | Productos sin gluten >40% margen; oportunidad de bundling con línea light |
| 4 | Desempeño de KAMs y Gestión de Cartera | Benchmarking, análisis de correlación | 60-40% dispersión en productividad; KAMs con cartera diversificada muestran +15% retención |
| 5 | Concentración de Clientes y Riesgo de Dependencia | Curva de Lorenz, análisis de concentración | Top 5 = 78% ventas; top 20 = 92%; riesgo alto de dependencia |
| 6 | Recomendaciones Estratégicas y Plan de Acción | Matriz de oportunidades | Quick-wins (DIGITAL, mayoristas) vs transformacionales; impacto financiero estimado |

---

## 🛠️ Stack Técnico

| Herramienta | Uso en este Proyecto |
|-------------|----------------------|
| **Python 3.x** | Lenguaje base para procesamiento y análisis |
| **pandas** | Limpieza, transformación y agregación de 192K+ transacciones |
| **matplotlib** | Visualización de tendencias temporales y evolución de canales |
| **seaborn** | Gráficos avanzados (heatmaps de correlación, distribuciones) |
| **Jupyter Notebook** | Documentación interactiva con análisis paso a paso |
| **NumPy** | Cálculos vectorizados de margen, volatilidad y concentración |

---

## 🚀 Cómo Ejecutar

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/tu-usuario/analisis-ventas-ecovida.git
   cd analisis-ventas-ecovida
   ```

2. **Crear entorno virtual e instalar dependencias:**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Ejecutar el notebook principal:**
   ```bash
   jupyter notebook notebooks/01_analisis_ventas_ecovida.ipynb
   ```

4. **Generar reporte ejecutivo (opcional):**
   ```bash
   python scripts/generar_reporte.py --formato pdf --output reportes/
   ```

---

## 📁 Estructura del Repositorio

```
analisis-ventas-ecovida/
├── README.md
├── requirements.txt
├── data/
│   ├── ventas_ecovida_2023_2025.csv          # Dataset bruto (192.8K registros, 33 variables)
│   └── diccionario_variables.xlsx             # Mapeo de campos y definiciones de negocio
├── notebooks/
│   ├── 01_analisis_ventas_ecovida.ipynb      # Notebook principal: EDA → recomendaciones
│   ├── 02_analisis_canales_kams.ipynb         # Análisis detallado de canales y KAMs
│   └── 03_concentracion_clientes.ipynb        # Estudio de riesgo y diversificación
├── scripts/
│   ├── limpieza_datos.py                      # Funciones de data cleaning
│   ├── metricas_negocio.py                    # Cálculo de KPIs (margen, ROI por canal)
│   └── generar_reporte.py                     # Automatización de reportes
├── reportes/
│   ├── resumen_ejecutivo.md                   # 1-página para stakeholders
│   └── recomendaciones_comerciales.pdf        # Plan de acción con impacto financiero
└── visualizaciones/
    ├── evolucion_ventas_por_canal.png
    ├── matriz_margen_volumen.png
    └── concentracion_clientes_lorenz.png
```

---

## 💡 Hallazgos Clave

- **Concentración Crítica de Riesgo:** Walmart y Cencosud generan **$10.3 mil millones CLP (48% del total)**. Los top 20 clientes concentran **92% de ingresos**, limitando la capacidad de negociación y exponiendo a cambios en políticas de retail.

- **Mix de Canales Subóptimo:** Canales SPMK CADENA y FS RETAIL aportan 65% de volumen pero solo 52% de margen. Canales DIGITAL y TRADICIONAL muestran **5-8 puntos porcentuales superior** en rentabilidad, indicando oportunidad de rebalance.

- **Estacionalidad y Estabilidad:** Las ventas exhiben patrón cíclico trimestral con peaks en **Q4 (diciembre-enero)**. La desviación estándar interanual es baja, lo que permite forecasting confiable para planificación operacional.

- **Dispersión de Productividad en KAM:** Top 20% de gestores concentran 45% de cartera, con retención 15 puntos superior en quienes manejan 8+ clientes versus concentración en 1-2 grandes cuentas. Oportunidad de replicar modelo de portafolio diversificado.

---

*Desarrollado por [Equipo de Analítica Ecovida] — 2025*