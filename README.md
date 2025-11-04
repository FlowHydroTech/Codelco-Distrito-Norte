# Codelco-Distrito-Norte

Repositorio dedicado al desarrollo, procesamiento y análisis de bases de datos hidrogeológicas para el proyecto **Codelco Distrito Norte**, enfocado en la gestión y control de niveles estáticos.

---

## Estructura del Proyecto

```bash
Codelco-Distrito-Norte/
│
├── data/
│   ├── raw/                # Datos crudos (archivos originales)
│   └── procesados/         # Resultados y análisis generados (Excel, figuras, etc.)
│
├── notebooks/
│   ├── 01_Importa_infraestructuras.ipynb
│   ├── 02_Procesamiento_Niveles.ipynb   # Dashboard interactivo de niveles estáticos
│
├── iframe_figures/         # Exportaciones HTML interactivas (Plotly)
│
├── .venv/                  # Entorno virtual gestionado con uv
├── pyproject.toml          # Dependencias y metadatos del entorno
├── README.md               # Documento de descripción del proyecto
└── main.py (opcional)      # Flujo automatizado futuro

```

---

## Objetivo General

Desarrollar un sistema reproducible y automatizado para el **procesamiento, análisis y comparación de niveles estáticos** en pozos de monitoreo, integrando:

- Limpieza y validación de datos
- Etiquetado automático de outliers (método IQR)
- Generación de estadísticos por pozo
- Comparación entre niveles medidos y calculados
- Visualización interactiva mediante Plotly + ipywidgets

---

## Componentes Principales

### 1. `01_Importa_infraestructuras.ipynb`
Importa y consolida la información base de pozos, sectores y acuíferos.  
Prepara el dataset maestro para los análisis siguientes.

### 2. `02_Procesamiento_Niveles.ipynb`
Dashboard interactivo que permite:

- Seleccionar un pozo específico (`HoleID`)
- Visualizar:
  - **Distribución nivel estatico medido**
  - **QQ Plots - Box Plots**
  - **Serie temporal original vs outliers**
- Ver **estadísticos descriptivos** e interpretación automática

### 3. Archivos de salida
Los resultados se exportan automáticamente a:

```bash
data/procesados/
├── analisis_niveles_estaticos_completo.xlsx
└── comparacion_niveles_estaticos.xlsx

```

Cada archivo contiene hojas separadas con:
- Datos etiquetados  
- Estadísticos descriptivos  
- Resumen de outliers  
- Métricas comparativas por pozo


---

### Flujo Analítico

1. **Carga del dataset principal (`df_niveles`)**  
2. **Conversión de tipos y limpieza**  
3. **Etiquetado de valores anómalos (outliers)**  
4. **Generación de métricas y correlaciones**  
5. **Visualización dinámica e interpretación**  
6. **Exportación automática de resultados**

---





