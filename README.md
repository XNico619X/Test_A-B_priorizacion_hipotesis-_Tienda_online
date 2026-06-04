# Test A/B y Priorización de Hipótesis para Tienda Online

## 1. Descripción del proyecto/problema que se resolvió

Este proyecto resolvió un reto de priorización y decisión en una tienda online que contaba con 9 hipótesis distintas para aumentar ingresos. El problema principal era que los recursos eran limitados, por lo que no era viable implementar todas las mejoras de inmediato. Además, existía la necesidad de analizar e interpretar los resultados de un test A/B ya ejecutado para saber si debía aplicarse el cambio probado.

El objetivo fue determinar qué hipótesis tenían mayor impacto y cómo traducir los resultados del experimento en una recomendación práctica para el negocio.

## 2. Metodología: cómo se resolvió

1. Revisión y clasificación de hipótesis:
   - Se describieron las 9 hipótesis y su posible impacto en el comportamiento del usuario.
   - Se evaluó cada hipótesis según criterios de relevancia, factibilidad y costo.

2. Análisis del test A/B existente:
   - Se cargaron y revisaron los datos del experimento.
   - Se analizaron métricas clave como conversión, ingresos promedio y diferencias entre grupo de control y grupo variante.
   - Se verificó si los resultados eran estadísticamente significativos y consistentes.

3. Priorización basada en impacto y riesgo:
   - Se comparó el potencial de beneficio de cada hipótesis con el costo de implementación.
   - Se definió un orden de ejecución en función de la mayor rentabilidad esperada y menor riesgo.

4. Formulación de recomendaciones:
   - Se determinó si el cambio del test A/B debía implementarse de inmediato, si requería más estudios o si debía descartarse.
   - Se propusieron acciones concretas para la tienda online según los hallazgos.

## 3. Herramientas usadas

- Python (para análisis de datos y generación de conclusiones).
- Jupyter Notebook (`gran_tienda_online.ipynb`) para documentar el proceso y los resultados.
- Librerías comunes de análisis (por ejemplo, `pandas`, `numpy`, `matplotlib`/`seaborn` si se usan gráficas).
- Metodología de prueba A/B y criterios de priorización de hipótesis.

## 4. ¿Qué descubriste?

- No todas las hipótesis eran igualmente prometedoras: algunas tenían mayor potencial de impacto que otras.
- El test A/B ya ejecutado permitió identificar si la variante propuesta mejoraba métricas comerciales clave frente al control.
- La decisión de implementación debió basarse no solo en el resultado del test, sino también en la factibilidad operativa y el tamaño del efecto.
- Las hipótesis con mejora directa en conversión y menor costo técnico fueron las mejores candidatas para avanzar primero.

## 5. Implicaciones para la empresa o recomendaciones para el negocio

- Priorizar las hipótesis con mayor retorno esperado y menor esfuerzo de implementación.
- Implementar primero el cambio que mostró un mejor desempeño en el test A/B, siempre que el resultado sea estadísticamente robusto y el impacto en ingresos sea significativo.
- Evitar invertir en cambios que no demuestren un beneficio claro en métricas clave o que requieran altos costos operativos.
- Usar este análisis como base para planificar futuros tests A/B y mejorar continuamente la priorización de hipótesis.
- Mantener una cultura de decisiones basada en datos, donde cada hipótesis se valida con métricas cuantificables antes de ser desplegada.
