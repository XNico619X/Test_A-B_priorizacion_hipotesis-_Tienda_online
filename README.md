# Test A/B y Priorización de Hipótesis - Tienda Online 🧪

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat&logo=scipy&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

> Proyecto desarrollado como parte del bootcamp de Data Analytics
> de TripleTen (2026). Análisis estadístico completo sobre datos
> reales de una tienda online - pedidos, visitas y resultados
> de experimento A/B.

---

## 1. Problema de negocio

Una gran tienda online tenía **9 hipótesis** para aumentar
ingresos pero recursos limitados para probarlas todas. Además,
ya había ejecutado un test A/B cuyos resultados necesitaban
interpretación rigurosa para tomar una decisión: ¿implementar
la variante B, mantener A, o necesitar más datos?

**Dos preguntas clave:**
1. ¿Qué hipótesis priorizar primero dado el impacto, alcance
   y esfuerzo requerido?
2. ¿Qué dice la evidencia estadística del test A/B ejecutado?

---

## 2. Metodología

### Parte 1 - Priorización de hipótesis

**Framework ICE** (Impact × Confidence × Ease)
- Evaluación individual de las 9 hipótesis
- Ordenamiento descendente por prioridad ICE

**Framework RICE** (Reach × Impact × Confidence × Ease)
- Incorporación del alcance de usuarios como variable
- Comparación de rankings ICE vs RICE
- Análisis de por qué cambia la prioridad al incluir el Reach

### Parte 2 - Análisis del test A/B

**Paso 1 - Limpieza y detección de anomalías**
- Identificación de usuarios presentes en ambos grupos
  simultáneamente
- Detección de outliers por percentiles **95 y 99**
  en pedidos por usuario y en precios de pedidos

**Paso 2 - Análisis exploratorio**
- Ingresos acumulados por grupo (A vs B) en el tiempo
- Tamaño de pedido promedio acumulado por grupo
- Diferencia relativa del grupo B vs grupo A
- Tasas de conversión diarias por grupo

**Paso 3 - Pruebas de significancia estadística**
- Conversión: datos brutos y datos filtrados (sin outliers)
- Ticket promedio: datos brutos y datos filtrados
- Cálculo de p-valores para cada escenario

---

## 3. Herramientas utilizadas

| Herramienta | Uso |
|---|---|
| Python | Lenguaje principal de análisis |
| Pandas | Manipulación y limpieza de datos |
| SciPy | Pruebas de hipótesis estadísticas |
| Matplotlib / Seaborn | Visualizaciones del experimento |
| Jupyter Notebook | Entorno de desarrollo y documentación |

---

## 4. Hallazgos principales

### ICE vs RICE - diferencia clave

Al incorporar el **Reach** (alcance de usuarios) en el
framework RICE, el ranking de hipótesis cambió
significativamente. La hipótesis top en ICE no era la
top en RICE, las hipótesis que impactan a más usuarios
subieron posiciones aunque requirieran más esfuerzo.

### Test A/B - resultados estadísticos

| Métrica | Grupo A | Grupo B | P-valor | Significativo |
|---|---|---|---|---|
| Tasa de conversión (bruta) | 2.685% | 3.098% | 0.017 |  Sí |
| Tasa de conversión (filtrada) | 2.626% | 3.050% | 0.013 |  Sí |
| Ticket promedio (bruto) | $115.90 | $145.06 | 0.404 |  No |
| Ticket promedio (filtrado) | $102.10 | $101.35 | 0.924 |  No |

**Hallazgo crítico:** La aparente ventaja de **$29 en ticket
promedio del grupo B desapareció completamente al filtrar
outliers**, era ruido estadístico puro. El efecto real
del test estaba únicamente en conversión.

**Mejora real confirmada:**
- **+16.2% en tasa de conversión** del grupo B vs grupo A
- **98.7% de confianza estadística**
- Resultado consistente con y sin filtrado de outliers

---

## 5. Recomendaciones de negocio

**- Detener el test y declarar al Grupo B como ganador.**
La mejora en conversión es estadísticamente sólida,
consistente bajo ambos análisis (bruto y filtrado) y
representa un impacto real medible en el negocio.

**- No optimizar el ticket promedio** basándose en los
resultados de este test. La diferencia observada no es
real, es ruido generado por valores atípicos.

**- Implementar variante B con monitoreo post-lanzamiento**
para confirmar que la mejora de conversión se mantiene
en producción.

**- Priorizar según RICE, no ICE**. El alcance de usuarios
es un factor determinante que ICE ignora y que puede
cambiar completamente el orden de implementación.

**- Usar este proceso como estándar** para futuros tests:
siempre analizar datos con y sin outliers antes de
concluir, y verificar significancia estadística antes
de implementar cualquier cambio.

---

## 6. Cómo ejecutar el proyecto

```bash
# 1. Clona el repositorio
git clone https://github.com/XNico619X/Test_A-B_priorizacion_hipotesis-_Tienda_online

# 2. Instala las dependencias
pip install pandas scipy matplotlib seaborn jupyter

# 3. Abre el notebook
jupyter notebook gran_tienda_online.ipynb
```

> Los archivos de datos deben estar en la misma carpeta
> que el notebook para que el análisis funcione correctamente.

---

## 7. Estructura del repositorio

Test_A-B_priorizacion_hipotesis-_Tienda_online
- gran_tienda_online.ipynb # Análisis completo
- orders_us.csv # Datos de pedidos del test
- visits_us.csv # Datos de visitas del test
- hypotheses_us.csv # Las 9 hipótesis evaluadas
- README.md # Este archivo

##  Autor

**Nicolás Espinosa Bedoya** — Data Analyst
 [Portafolio](https://xnico619x.github.io) ·
 [LinkedIn](https://www.linkedin.com/in/nicolas-espinosa-bedoya-data-analyst) ·
 inge.nicoespi@gmail.com
