# 📊 Netflix Content Analysis Project

Este repositorio contiene un análisis completo de la biblioteca de contenido de Netflix, explorando patrones en películas y series, preferencias regionales y la evolución del catálogo a lo largo del tiempo.

---

## 🧠 Objetivo del Proyecto

Este proyecto busca extraer insights del catálogo global de Netflix, respondiendo preguntas como:

- ¿Netflix tiene más películas o series?
- ¿Qué países producen más contenido para Netflix?
- ¿Cómo ha cambiado la oferta de contenido a lo largo de los años?
- ¿Qué géneros son más populares?
- ¿Qué diferencias existen entre películas y series según región?

---

## ⚙️ Instalación y Configuración

```bash
# Clonar el repositorio
git clone https://github.com/your-username/netflix-analysis.git
cd netflix-analysis

# Instalar dependencias
pip install -r requirements.txt

netflix-analysis/
├── README.md
├── netflix_analysis.py            # Script principal (automatización)
├── requirements.txt               # Dependencias
├── data/
│   └── netflix_titles.csv         # Dataset
├── notebooks/
│   └── exploratory_analysis.ipynb # Análisis exploratorio
├── visualizations/                # Imágenes generadas
└── database/
    └── netflix.db                 # Base de datos SQLite 
```
# 📊 Análisis Exploratorio (EDA)

## 🔹 Tipo de contenido
- **70%** del contenido corresponde a **películas**.
- Las **series** están aumentando en proporción en años recientes.

## 🔹 Evolución temporal
- **Pico de adiciones** de contenido entre **2018 y 2020**.
- Se estabiliza en años posteriores.

## 🔹 Producción por país
- **Estados Unidos** lidera por lejos, seguido de **India**, **Reino Unido** y **Canadá**.
- Producción regional creciente en países como **Corea del Sur** y **Brasil**.

## 🔹 Géneros populares
- **Películas**: Dramas, Documentales, Comedias.
- **Series**: Docuseries, Reality Shows, Crime TV.

## 🔹 Ratings más comunes
- **TV-MA**, **TV-14** y **PG-13** dominan.
- El **contenido adulto** supera al contenido familiar.

---

## 📐 A/B Testing Simulado

Se generaron dos grupos con niveles de engagement diferentes:

- **Grupo A**: contenido promocionado con *trailers*.
- **Grupo B**: contenido con solo *sinopsis*.

**Resultados del T-test**:
- `p-value < 0.05` → diferencia **estadísticamente significativa**.

**Conclusión**: las campañas con *trailers* generan **mayor engagement**.

---

## 🗺️ Ejemplos de Visualizaciones

📌 Distribución de contenido por tipo  
📌 Series temporales del contenido agregado  
📌 Gráfico de barras de países con más producciones  
📌 KDE plot de A/B testing  
📌 Gráficos de géneros por país  

📁 Todas las visualizaciones se encuentran en la carpeta `visualizations/`.

---

## 🗃️ Base de Datos (opcional)

Se construyó una base de datos **SQLite** con la tabla limpia `netflix_titles`.

Consultas SQL permiten responder preguntas como:
- ¿Qué géneros crecieron más rápido?
- ¿Qué año tuvo más contenido nuevo por país?

---

## 🧰 Tecnologías Utilizadas

- Python  
- Pandas & NumPy  
- Matplotlib & Seaborn  
- SQLite3  
- SciPy (T-test)  
- Jupyter Notebook  

---

## 🔍 Posibles Extensiones

🤖 Entrenar un modelo de clasificación de géneros  
📈 Predecir el éxito de un contenido con *machine learning*  
🧩 Integrar datos de IMDb o Rotten Tomatoes  
🌐 Crear un dashboard con Streamlit o Power BI  

---

## 📬 Contacto

**Juan Camilo Cortés Sánchez**  
[LinkedIn](#)  
📧 tu.email@ejemplo.com  
🔗 Proyecto: [https://github.com/your-username/netflix-analysis](https://github.com/your-username/netflix-analysis)

---

## 📝 Licencia

Este proyecto está licenciado bajo la licencia **MIT**.  
Consulta el archivo `LICENSE` para más detalles.




