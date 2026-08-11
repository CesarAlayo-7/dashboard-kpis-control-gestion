# 📊 Dashboard de KPIs de Control de Gestión

Dashboard ejecutivo en Power BI que simula el reporte mensual de un área de **Control de Gestión**: seguimiento de CAPEX/OPEX (presupuestado vs. real) e indicadores operativos clave (KPIs) por planta, orientado a la toma de decisiones de la alta dirección.

![Dashboard preview](screenshots/dashboard_overview.png)

## 🎯 Objetivo del proyecto

Replicar el flujo de trabajo real de un Analista de Control de Gestión: consolidar información financiera y operativa de distintas plantas, calcular variaciones contra presupuesto, y presentar un resumen claro y accionable para directorio.

## ❓ Problema que resuelve

En muchas organizaciones industriales, la información de gastos, inversiones y KPIs vive dispersa por planta y por área, lo que retrasa la elaboración de reportes gerenciales. Este dashboard centraliza esa información y automatiza el seguimiento de:

- Ejecución de CAPEX y OPEX vs. presupuesto, por planta y por mes.
- Indicadores operativos clave (Cumplimiento de CAPEX, OEE, Rentabilidad por negocio, Cumplimiento de presupuesto OPEX).
- Variaciones y alertas (semáforo) cuando el resultado real se aleja de la meta.

## 🗂️ Datos

Los datos utilizados son **sintéticos** (generados para fines de este portafolio, no corresponden a ninguna empresa real). Estructura:

| Hoja | Contenido |
|---|---|
| `Datos_CAPEX_OPEX` | Presupuestado vs. Real de CAPEX y OPEX, por planta, mes y concepto (2025) |
| `KPIs_Operativos` | Meta vs. Real de 4 indicadores operativos, por planta y mes |
| `Notas` | Descripción del dataset y sugerencias de uso |

Fuente: [`Dataset_Control_Gestion_2025.xlsx`](Dataset_Control_Gestion_2025.xlsx)

## 🛠️ Herramientas utilizadas

- **Power BI Desktop** — modelado de datos y visualización
- **DAX** — medidas de variación, cumplimiento y semáforos
- **Excel** — fuente de datos

## 🔧 Proceso

1. Carga de datos desde Excel (dos tablas: financiera y de KPIs).
2. Modelado de relaciones entre plantas, meses e indicadores.
3. Creación de medidas DAX:
   - `Variación % = DIVIDE([Real] - [Presupuestado], [Presupuestado])`
   - `Cumplimiento KPI = DIVIDE([Real], [Meta])`
   - Semáforo de estado (rojo/ámbar/verde) según desviación vs. meta.
4. Diseño de visuales: evolución mensual, comparativo por planta, tabla resumen ejecutivo.

## 📈 Resultado

Un dashboard de una sola vista que permite identificar en segundos:
- Qué planta está por encima o por debajo de su presupuesto de CAPEX/OPEX.
- Qué indicadores operativos están fuera de meta y requieren atención.
- La tendencia mensual del gasto y su proyección.

## 🚀 Cómo usarlo

1. Descarga [`Dataset_Control_Gestion_2025.xlsx`](Dataset_Control_Gestion_2025.xlsx).
2. Ábrelo en Power BI Desktop (`Obtener datos → Excel`).
3. Importa las hojas `Datos_CAPEX_OPEX` y `KPIs_Operativos`.
4. Replica las medidas DAX descritas arriba y arma tus propios visuales.

## 👤 Autor

**César Alayo Ávalos** — Ingeniero Industrial | Data Analyst | Business Intelligence
[LinkedIn](https://www.linkedin.com/in/cesar-alayo/) · cesar.alayo7@gmail.com
