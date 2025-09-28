# 🌍 Análisis exploratorio de la calidad del aire en Madrid (2001–2022)
## 📌 Descripción del proyecto

Este proyecto consiste en un análisis exploratorio de datos (EDA) sobre la calidad del aire en la ciudad de Madrid durante el periodo 2001–2022.

Se utiliza un dataset público que recoge valores horarios de diferentes contaminantes atmosféricos medidos en estaciones de la ciudad. El objetivo es explorar tendencias, identificar picos críticos, analizar distribuciones y estudiar la variabilidad estacional/anual de los principales contaminantes.

## 📂 Estructura del proyecto

```
├── data/
│   └── MadridPolution2001-2022.csv   # Dataset principal
├── notebook.ipynb                    # Notebook con el análisis
└── README.md                         # Documentación del proyecto
```

## 🔬 Metodología

1. Carga y limpieza de datos
- Conversión de la columna temporal a datetime.
- Eliminación de filas con valores nulos en columnas clave.
- Creación de variables auxiliares: year, month, day, hour.
2. Selección de contaminantes
- Se analizaron los siguientes contaminantes principales:
  - 🟦 NO₂ (Dióxido de Nitrógeno, µg/m³)
  - 🟩 O₃ (Ozono troposférico, µg/m³)
  - 🟧 PM10 (Partículas ≤10 µm, µg/m³)
  - 🟥 PM2.5 (Partículas ≤2.5 µm, µg/m³)
  - Otros incluidos: BEN, CH4, CO, EBE, NMHC, NO, NOx, SO2, TCH, TOL.
3. Análisis exploratorio
- Estadísticas descriptivas globales y anuales.
- Distribuciones → histogramas globales y por año.
- Evolución temporal → series anuales y mensuales.
- Identificación de picos extremos → días con mayor concentración.

## 📊 Resultados principales
### 1️⃣ Evolución anual de contaminantes
Se observa una tendencia decreciente en NO₂ y PM10, reflejando mejoras en políticas medioambientales, aunque persisten episodios críticos.

### 2️⃣ Mes con peor calidad del aire (NO₂)
- Para cada año se identificó el mes con la media más alta de NO₂.
- El invierno suele concentrar los valores más altos (efecto de calefacciones + meteorología).

### 3️⃣ Distribución de O₃
- Histograma global y por año: muestra que los picos de ozono se concentran en primavera-verano.
- Variabilidad estacional clara: máximos en verano y mínimos en invierno.

### 4️⃣ Picos diarios de PM10
- Se identificó el día con mayor concentración de PM10 en cada año.
- Muchos picos coinciden con episodios de intrusión de polvo sahariano y episodios de tráfico intenso.

## 🛠️ Tecnologías utilizadas

- Python 3.x
- Pandas → manipulación de datos.
- Matplotlib / Seaborn → visualización.
- Jupyter Notebook → entorno de desarrollo.

## 📌 Conclusiones

- La calidad del aire en Madrid ha mejorado en las últimas dos décadas, pero persisten episodios críticos.
- NO₂ muestra un claro descenso, aunque sigue superando límites recomendados en ciertos años.
- O₃ presenta una fuerte variabilidad estacional, con máximos en verano.
- PM10 registra picos extremos vinculados a fenómenos externos (polvo sahariano, tráfico, climatología).
