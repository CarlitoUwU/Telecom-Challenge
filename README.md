# 📊 Análisis de Evasión de Clientes TelecomX
### *Informe Completo de Customer Churn Analysis*

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green?style=flat&logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-orange?style=flat)
![Seaborn](https://img.shields.io/badge/Seaborn-0.12+-red?style=flat)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)

---

## 🎯 **Resumen Ejecutivo**

Este proyecto presenta un análisis exhaustivo de la evasión de clientes (Customer Churn) para TelecomX, una empresa de telecomunicaciones. Utilizando técnicas de análisis exploratorio de datos (EDA), identificamos patrones críticos que explican por qué los clientes cancelan sus servicios y desarrollamos estrategias basadas en datos para mejorar la retención.

### **📈 Hallazgos Clave:**
- **Tasa de Evasión Actual:** 26.5% de los clientes cancelan sus servicios
- **Factor Crítico:** Los primeros 6 meses son determinantes (50% de cancelaciones)
- **Oportunidad de Negocio:** Potencial de reducir evasión al 18% con ROI de 4:1
- **Impacto Económico:** Clientes fieles generan $1,000+ más en ingresos

---

## 🎯 **Objetivos del Proyecto**

- 🔍 **Identificar patrones** de comportamiento en clientes que cancelan vs. los que permanecen
- 📊 **Analizar distribuciones** de evasión según variables categóricas y numéricas  
- 💡 **Generar insights accionables** para estrategias de retención
- 🎯 **Proponer recomendaciones** basadas en datos para reducir la tasa de evasión
- 📈 **Desarrollar segmentación** de clientes por nivel de riesgo

---

## 📂 **Estructura del Proyecto**

```
challenge-TelecomX/
│
├── 📓 Telecom-X.ipynb          # Notebook principal con análisis completo
├── 📄 README.md                # Documentación del proyecto
└── 📊 TelecomX_Data.json         # JSON desde GitHub 
```

---

## 🔍 **Metodología de Análisis**

### **1. 📥 Extracción y Preparación de Datos**
- **Fuente:** Datos JSON desde GitHub con 7,043 registros de clientes
- **Categorías:** Demographics, Phone Services, Internet Services, Account Info
- **Limpieza:** Normalización de estructuras JSON, conversión de tipos de datos
- **Ingeniería:** Creación de variables derivadas (cuentas diarias)

### **2. 📊 Análisis Exploratorio**
- **Distribución de Churn:** Análisis de balance de clases
- **Variables Categóricas:** 15+ variables analizadas con visualizaciones
- **Variables Numéricas:** Análisis de tenure, gastos totales y mensuales
- **Correlaciones:** Identificación de relaciones entre variables

### **3. 🎯 Segmentación y Perfilado**
- **Perfiles de Riesgo:** Extremo (80%), Moderado (30%), Bajo (8%)
- **Factores Críticos:** Contratos, métodos de pago, demografía
- **Segmentación Estratégica:** 3 niveles de intervención

---

## 🔑 **Hallazgos Principales**

### **📋 Variables Categóricas Críticas**

#### **🔴 Factores de Alto Riesgo:**
| Factor | Tasa de Evasión | Impacto |
|--------|----------------|---------|
| **Contratos mes a mes** | 42% | vs. 3% en contratos de 2 años |
| **Electronic check** | 45% | vs. 15-18% métodos automáticos |
| **Fiber Optic** | 30% | Problema calidad/precio |
| **Senior Citizens** | 41% | vs. 23% no-senior |
| **Sin familia** | 33% | vs. 20% con familia |

#### **🟢 Factores Protectores:**
- **Contratos largos (1-2 años):** Reducen evasión a 11-19%
- **Débito automático:** Mayor conveniencia y compromiso
- **Servicios adicionales:** Cada servicio reduce 5-8% la evasión
- **Clientes con familia:** 20% menos probabilidad de cancelar

### **⏰ Variables Temporales y Económicas**

#### **Tiempo de Contrato (Tenure):**
- **Período crítico:** Primeros 6 meses = 50% de cancelaciones
- **Punto de inflexión:** 24+ meses = solo 10% de evasión
- **Diferencia promedio:** Clientes fieles permanecen 19.7 meses más

#### **Valor Económico:**
- **CLV Diferencial:** Clientes fieles gastan $1,532 más en promedio
- **Correlación fuerte:** 0.82 entre tiempo y gasto total
- **Segmento crítico:** Clientes <$1,000 tienen 45% evasión

---

## 🎯 **Perfiles de Cliente Identificados**

### **🚨 Riesgo Extremo (Score 85-95%)**
```
✓ Nuevo cliente (≤6 meses)
✓ Contrato mes a mes + Electronic check  
✓ Sin servicios adicionales
✓ Senior citizen sin familia
✓ Gasto total <$500
→ Probabilidad evasión: ~80%
```

### **⚠️ Riesgo Moderado (Score 50-70%)**
```
✓ Antigüedad 6-18 meses
✓ Contrato anual + Facturación digital
✓ Servicio Fiber Optic
✓ Gasto medio ($1,000-2,500)
→ Probabilidad evasión: ~30%
```

### **🛡️ Cliente Fiel (Score 10-25%)**
```
✓ Antigüedad >24 meses
✓ Contrato bianual + Débito automático
✓ Bundle completo de servicios
✓ Con familia/dependientes
✓ Alto CLV (>$3,000)
→ Probabilidad evasión: ~8%
```

---

## 🚀 **Recomendaciones Estratégicas**

### **🎯 ESTRATEGIA 1: Programa "Primeros 100 Días"**
**Objetivo:** Reducir evasión en clientes nuevos del 50% al 25%

**Componentes:**
- 📋 **Onboarding estructurado** (Días 1, 7, 30, 60, 90)
- 💰 **Incentivos económicos** (20% descuento primeros 3 meses)
- 🎯 **Migración a contratos anuales** (15% bonificación)

### **🔧 ESTRATEGIA 2: Optimización de Productos**
**Objetivo:** Mejorar satisfacción y competitividad

**Acciones:**
- 🔍 **Auditoría Fiber Optic** (30% evasión → target 18%)
- 📦 **Bundling inteligente** (Familia, Senior, Profesional)
- 💰 **Benchmarking de precios** (-15% vs. competencia)

### **💳 ESTRATEGIA 3: Modernización de Pagos**
**Objetivo:** Reducir fricción y aumentar conveniencia

**Implementación:**
- 📱 **Wallets digitales** (Apple Pay, Google Pay)
- 🔄 **Migración de Electronic check** (incentivos $50)
- 💳 **5% descuento** por débito automático

---

## 📊 **Tecnologías Utilizadas**

### **🐍 Python & Librerías**
```python
import pandas as pd              # Manipulación de datos
import requests                  # Carga de datos externos
import numpy as np              # Cálculos numéricos
import matplotlib.pyplot as plt  # Visualizaciones base
import seaborn as sns           # Visualizaciones estadísticas
```

### **📈 Análisis y Visualización**
- **Pandas:** Procesamiento y transformación de datos
- **Matplotlib/Seaborn:** 20+ visualizaciones profesionales
- **Estadística Descriptiva:** Correlaciones, distribuciones, segmentaciones
- **Jupyter Notebook:** Ambiente interactivo de desarrollo

---

## 🚀 **Cómo Ejecutar el Proyecto**

### **1. Clonar el Repositorio**
```bash
git clone https://github.com/CarlitoUwU/Telecom-Challenge
cd Telecom-Challenge
```

### **2. Instalar Dependencias**
```bash
pip install pandas numpy matplotlib seaborn requests jupyter
```

### **3. Ejecutar el Notebook**
```bash
jupyter notebook Telecom-X.ipynb
```

### **4. Explorar el Análisis**
El notebook está estructurado en secciones:
- 📥 Carga y limpieza de datos
- 🔍 Análisis exploratorio
- 📊 Visualizaciones interactivas  
- 💡 Insights y conclusiones
- 🎯 Recomendaciones estratégicas

---

## 📞 **Contacto**

**Desarrollador del Proyecto**

- 📧 Email: [cvaldivialu@gmail.com](mailto:cvaldivialu@gmail.com)
- 💼 LinkedIn: [Carlo Joaquín Valdivia Luna](https://www.linkedin.com/in/carlo-joaquin-valdivia-luna/)
- 🐙 GitHub: [CarlitoUwU](https://github.com/CarlitoUwU)
