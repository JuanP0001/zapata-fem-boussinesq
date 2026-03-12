# 🏗️ Análisis Comparativo: FEM (SAP2000) vs Boussinesq
### Esfuerzos verticales en subsuelo — Zapata Aislada

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter&logoColor=white)

---

## 📌 ¿De qué trata este proyecto?

Comparativa cuantitativa entre dos metodologías para estimar esfuerzos verticales transmitidos al subsuelo por una zapata aislada:

- **SAP2000** — Modelo de Elementos Finitos (FEM) 3D
- **Boussinesq (1885)** — Solución analítica clásica para semiespacio elástico homogéneo

El análisis cubre 18 profundidades desde **z = 0.25 m** hasta **z = 6.0 m** y cuantifica las diferencias con métricas estadísticas (RMSE, MAE, R²).

---

## 📊 Resultados principales

| Zona | Profundidad | Error relativo | Diagnóstico |
|------|-------------|----------------|-------------|
| Superficial crítica | z = 0.50 m | **39.4 %** | 🔴 FEM capta rigidez de zapata |
| Franja de diseño | z = 0.75 – 3.0 m | **< 5 %** | ✅ Boussinesq completamente válido |
| Profundidad | z > 3.5 m | 10 – 57 % | 🟡 Diferencias altas pero baja magnitud |

**R² global = 0.9896** — alta correlación entre ambos métodos.

---

## 📁 Estructura del repositorio

```
zapata-fem-boussinesq/
├── analisis_zapata.ipynb        # Notebook principal
├── analisis_zapata.png          # Panel de gráficas exportado
├── img/
│   └── Zapata sap2000.png       # Captura del modelo FEM en SAP2000
├── README.md
└── requirements.txt
```

---

## 🚀 Cómo ejecutar

```bash
# 1. Clonar el repositorio
git clone https://github.com/JuanP0001/zapata-fem-boussinesq.git
cd zapata-fem-boussinesq

# 2. Instalar dependencias
pip install -r requirements.txt

# 3. Abrir el notebook
jupyter notebook analisis_zapata.ipynb
```

---

## 🛠️ Tecnologías utilizadas

- `Python 3.10+`
- `NumPy` — cálculo numérico
- `Pandas` — manejo de datos y tablas
- `Matplotlib` — visualización
- `Jupyter Notebook` — entorno interactivo

---

## 🧠 Conclusión

> Boussinesq **no está obsoleto**. Es confiable en la franja geotécnica de diseño (z = 0.75 – 3.0 m).  
> El FEM es indispensable cuando hay estratificación del suelo, cargas excéntricas o interacción suelo–estructura compleja.

---

## 👤 Autor

**Juan Fernando Pineda Cano**  
Ingeniero Civil 

[LinkedIn](https://www.linkedin.com/in/juan-fernando-pineda-236134205/) · [GitHub](https://github.com/JuanP0001)

---

*Datos obtenidos de modelo FEM en SAP2000 y formulación clásica de Boussinesq (1885)*
