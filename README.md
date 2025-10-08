# 🚗 Dashboard de Simulación - ParkingZone S.R.L.

> **Proyecto Académico**: Análisis y optimización del sistema de parqueo mediante simulación de eventos discretos
> 
> **Materia**: Simulación y Dinámica de Sistemas  
> **Institución**: Universidad Adventista de Bolivia  
> **Fecha**: Octubre 2025


---

## 📋 Tabla de Contenidos

- [Descripción del Proyecto](#-descripción-del-proyecto)
- [Contexto del Caso de Estudio](#-contexto-del-caso-de-estudio)
- [Metodología Aplicada](#-metodología-aplicada)
- [Estructura del Dashboard](#-estructura-del-dashboard)
- [Guía de Interpretación](#-guía-de-interpretación)
- [Resultados Clave](#-resultados-clave)
- [Tecnologías Utilizadas](#-tecnologías-utilizadas)
- [Cómo Usar el Dashboard](#-cómo-usar-el-dashboard)
- [Instalación Local](#-instalación-local)
- [Equipo](#-equipo)

---

## 🎯 Descripción del Proyecto

Este proyecto implementa las **10 etapas del proceso de experimentación en simulación** para analizar y optimizar el funcionamiento de **ParkingZone S.R.L.**, un parqueo privado de 8 pisos en Cochabamba, Bolivia.

### Objetivo General
Maximizar la rentabilidad del parqueo mediante la optimización de:
- ✅ Estructura de tarifas
- ✅ Capacidad operativa (casetas de pago)
- ✅ Distribución de espacios (motos vs vehículos)
- ✅ Implementación de tecnología inteligente

### Resultados Alcanzados
- 📈 **+35% en ingresos** mensuales
- ⏱️ **-85% en tiempos de espera**
- 🚗 **+54% en ocupación** general
- ⭐ **+48% en satisfacción** del cliente

---

## 🏢 Contexto del Caso de Estudio

### Características del Parqueo

| Característica | Especificación |
|----------------|----------------|
| **Ubicación** | Centro de Cochabamba |
| **Número de pisos** | 8 pisos |
| **Capacidad por piso** | 45 espacios vehículos + 10 espacios motos |
| **Capacidad total** | 440 espacios |
| **Horario** | 24/7 (operación continua) |
| **Entradas** | 6 entradas |
| **Salidas** | 2 salidas con casetas de pago |

### Tarifas Actuales

| Tipo | Horario | Tarifa |
|------|---------|--------|
| **Vehículos** | 8:00 - 19:00 | 8 Bs/hora |
| | 19:00 - 22:00 | 10 Bs/hora |
| | 22:00 - 8:00 | 15 Bs/hora |
| **Motocicletas** | 8:00 - 22:00 | 3 Bs/hora |
| | Nunca nocturno | N/A |

### Problemas Identificados

1. **Subutilización de Capacidad**: Solo 35.7% de ocupación promedio
2. **Cuello de Botella**: Tiempo de pago de 3 min/vehículo genera colas de >5 minutos
3. **Desbalance de Pisos**: Pisos 1-3 saturados, pisos 4-8 vacíos
4. **Baja Rentabilidad de Motos**: 9.87% de vehículos generan solo 2.8% de ingresos
5. **Incumplimiento Normativo**: 0% de vehículos eléctricos en Piso 4 designado

---

## 🔬 Metodología Aplicada

### 10 Etapas de Simulación Implementadas

```
1. Identificación del Problema
   └─> Análisis de ineficiencias operativas y financieras

2. Definición de Objetivos
   └─> Incrementar ingresos, mejorar ocupación, reducir tiempos

3. Variables de Salida y Factores Experimentales
   └─> 8 factores identificados, 40+ variables medidas

4. Diseño del Modelo Conceptual
   └─> Diagrama de flujo, entidades, procesos

5. Recolección y Análisis de Datos
   └─> 4,852 registros históricos (31 días)
   └─> Análisis estadístico: distribuciones, patrones

6. Formulación del Modelo Computacional
   └─> Simulación de eventos discretos (DES)
   └─> Implementación en Python/SimPy y AnyLogic

7. Verificación
   └─> Pruebas unitarias, balance de entidades
   └─> Validación lógica del código

8. Validación
   └─> Comparación con datos históricos
   └─> Validación con expertos (face validity)

9. Diseño y Ejecución de Experimentos
   └─> 19 escenarios simulados
   └─> 30 réplicas por escenario
   └─> Total: 590 corridas de simulación

10. Análisis e Interpretación de Resultados
    └─> Identificación de escenario óptimo
    └─> Recomendaciones estratégicas
```

### Datos Utilizados

- **Período de análisis**: 7 septiembre - 7 octubre 2025 (31 días)
- **Registros totales**: 4,852 vehículos
- **Promedio diario**: 157 vehículos/día
- **Variables registradas**: Fecha, hora, tipo vehículo, piso, cubículo, tiempo estancia, placa, color

---

## 📊 Estructura del Dashboard

El dashboard está organizado en **5 secciones interactivas** accesibles mediante pestañas:

### 1️⃣ Resumen Ejecutivo

**Propósito**: Vista general de las mejoras propuestas vs situación actual

**Componentes**:
- **4 KPI Cards**: Métricas principales con indicadores de cambio
- **Gráfico de Barras**: Comparación directa Baseline vs Óptimo
- **Gráfico de Líneas**: Ocupación por piso (antes/después)

**Métricas Destacadas**:
- Incremento de Ingresos: +35% (+166,712 Bs/mes)
- Mejora Ocupación: De 35.7% a 55.2%
- Reducción Tiempo Espera: De 5.2 a 0.8 minutos
- Satisfacción Cliente: De 6.2 a 9.2 sobre 10

---

### 2️⃣ Comparación de Escenarios

**Propósito**: Análisis comparativo de los 6 escenarios principales simulados

**Escenarios Incluidos**:

| ID | Nombre | Descripción |
|----|--------|-------------|
| BASE | Situación Actual | Configuración sin cambios (línea base) |
| 1A-2 | 4 Casetas | Aumentar casetas de pago de 2 a 4 |
| 1B-2 | Pago Automático | Automatizar proceso (3 min → 0.75 min) |
| 2A-2 | Tarifas Diferenciadas | Precios premium pisos 1-3, descuento 4-8 |
| 3A-1 | Menos Motos | Reducir espacios motos (10 → 5 por piso) |
| 5 | **ÓPTIMO INTEGRAL** | Combinación de mejores prácticas |

**Gráfico Principal**: Barras agrupadas comparando ingresos y ocupación

**Tabla Detallada**: Todas las métricas por escenario con fila destacada para el óptimo

---

### 3️⃣ Análisis Financiero

**Propósito**: Evaluación de viabilidad económica del proyecto

**KPIs Financieros**:
- **Inversión Requerida**: $110,000 USD (desembolso único)
- **Período de Recuperación (Payback)**: 5.5 meses
- **Valor Actual Neto (VAN)**: 8.2 millones Bs (5 años)
- **Tasa Interna de Retorno (TIR)**: 285%
- **Retorno sobre Inversión (ROI)**: 557%

**Gráfico de Líneas - Rentabilidad**: 
- Muestra ingresos, costos y utilidad para cada escenario
- Permite identificar cuál genera mayor margen

**Gráfico de Flujo de Caja**:
- Proyección a 12 meses
- Compara flujo acumulado Baseline vs Óptimo
- Marca el punto de equilibrio (mes 6)

**Interpretación**: 
- La inversión se recupera antes de 6 meses
- A partir del mes 7, todo es ganancia adicional
- VAN positivo indica que el proyecto es rentable a largo plazo

---

### 4️⃣ Métricas Operacionales

**Propósito**: Análisis del desempeño operativo del sistema

**Gráficos Incluidos**:

#### A) Tiempos de Espera por Escenario
- **Tipo**: Gráfico de barras con código de colores
- **Escala de colores**:
  - 🟢 Verde (<1.5 min): Excelente
  - 🟡 Amarillo (1.5-3 min): Aceptable
  - 🔴 Rojo (>3 min): Inaceptable
- **Insight**: Automatización y más casetas reducen drásticamente la espera

#### B) Vehículos Atendidos vs Rechazados
- **Tipo**: Barras apiladas
- **Verde**: Vehículos que ingresaron y fueron atendidos
- **Rojo**: Vehículos rechazados por falta de espacio
- **Meta**: Minimizar rechazos (<2%)

#### C) Evolución de Ocupación
- **Tipo**: Gráfico de líneas (8 semanas proyectadas)
- **Baseline**: Línea plana (~36%)
- **Con Mejoras**: Crecimiento gradual hasta 55%
- **Interpretación**: Muestra el período de adaptación y adopción

---

### 5️⃣ Recomendaciones

**Propósito**: Conclusiones y plan de acción estratégico

**Contenido**:

#### Recomendación Principal
Un panel destacado con fondo verde que resume:
- **Decisión**: Implementar Escenario Óptimo Integral
- **Fases**: 3 fases en 6 meses
- **Inversión total**: $110K distribuida
- **Métricas de éxito**: ROI 557%, Payback 5.5 meses

#### Plan de Implementación

**FASE 1 (Mes 1-2)**: Quick Wins - $0
- ✅ Ajustar tarifas diferenciadas por piso
- ✅ Aumentar tarifa motos de 3 a 4 Bs/h
- ✅ Implementar política Piso 4 para eléctricos
- **Impacto**: +21% ingresos inmediatos

**FASE 2 (Mes 3-4)**: Mejoras Operativas - $45K
- ✅ Instalar 2 casetas adicionales (4 total)
- ✅ Automatizar sistema de pago (0.75 min)
- **Impacto**: -71% tiempo espera

**FASE 3 (Mes 5-6)**: Transformación Digital - $65K
- ✅ Sistema de asignación automática
- ✅ App móvil con pre-pago
- ✅ Sensores de ocupación en tiempo real
- **Impacto**: +47% ocupación pisos superiores

#### Componentes de la Solución

Lista detallada de los 4 pilares:
1. **Operación**: Casetas y automatización
2. **Precios**: Tarifas diferenciadas por piso y horario
3. **Infraestructura**: Redistribución espacios motos/vehículos
4. **Tecnología**: Sistemas inteligentes

#### Matriz de Riesgos

Tabla que identifica:
- Riesgos potenciales
- Probabilidad de ocurrencia
- Impacto en el proyecto
- Estrategias de mitigación

**Ejemplo**:
- **Riesgo**: Rechazo a precios premium
- **Probabilidad**: Media
- **Impacto**: Medio
- **Mitigación**: Implementación gradual, comunicación de valor

---

## 🔍 Guía de Interpretación

### Cómo Leer los Gráficos

#### 📊 Gráficos de Barras
- **Eje Y**: Valor de la métrica (ingresos, ocupación, etc.)
- **Eje X**: Categorías (escenarios, pisos, etc.)
- **Colores**: Código visual para identificar rápidamente
  - Verde: Positivo/Óptimo
  - Rojo: Negativo/Problema
  - Azul: Neutro/Informativo

**Tip**: Barras más altas = mejor desempeño (para ingresos, ocupación, satisfacción)

#### 📈 Gráficos de Líneas
- **Línea Base (gris)**: Situación actual sin cambios
- **Línea Óptima (verde)**: Proyección con mejoras implementadas
- **Área sombreada**: Intervalo de confianza (variabilidad)

**Tip**: La distancia entre líneas muestra el impacto de las mejoras

#### 🎯 KPI Cards
Estructura de cada tarjeta:
1. **Icono + Color**: Identifica el tipo de métrica
2. **Etiqueta**: Nombre de la métrica
3. **Valor Principal**: Número destacado (resultado)
4. **Cambio Porcentual**: Mejora respecto a baseline
   - Verde con "+" = Mejora positiva
   - Rojo con "-" = Reducción (puede ser bueno, ej: -85% tiempo espera)

**Ejemplo de Lectura**:
```
💰 Incremento de Ingresos
+35%
+166,712 Bs/mes
```
Significa: Los ingresos aumentan 35%, equivalente a 166,712 Bolivianos adicionales cada mes.

---

### Términos Clave

| Término | Definición | Ejemplo |
|---------|------------|---------|
| **Baseline** | Situación actual sin cambios, línea de comparación | 476,538 Bs/mes |
| **Escenario Óptimo** | Mejor combinación de factores identificada | ESC-5: +35% ingresos |
| **Ocupación** | % de cubículos usados del total disponible | 35.7% actual → 55.2% óptimo |
| **Tiempo de Espera** | Minutos promedio en cola de salida | 5.2 min → 0.8 min |
| **Throughput** | Vehículos procesados por hora | 20 veh/h → 80 veh/h |
| **ROI** | Retorno sobre inversión (ganancia/inversión) | 557% = $5.57 por cada $1 |
| **Payback** | Tiempo para recuperar inversión inicial | 5.5 meses |
| **VAN** | Valor actual neto (valor presente ganancias futuras) | 8.2M Bs |
| **TIR** | Tasa interna retorno (rentabilidad del proyecto) | 285% |

---

### Interpretación de Métricas Específicas

#### 📈 Ocupación (%)
- **0-30%**: Subutilización crítica (pérdida de ingresos)
- **30-50%**: Baja utilización (mejorable)
- **50-70%**: Ocupación óptima (rentable sin congestión)
- **70-90%**: Alta ocupación (rentable pero riesgo rechazo)
- **90-100%**: Saturación (rechazos frecuentes)

**Situación Actual**: 35.7% (subutilizada)  
**Meta Óptima**: 55.2% (zona verde)

#### ⏱️ Tiempo de Espera
- **0-1 min**: 😊 Excelente (cliente muy satisfecho)
- **1-2 min**: 🙂 Bueno (aceptable)
- **2-4 min**: 😐 Regular (mejorable)
- **4-6 min**: ☹️ Malo (insatisfacción)
- **>6 min**: 😡 Crítico (pérdida clientes)

**Situación Actual**: 5.2 min (malo)  
**Meta Óptima**: 0.8 min (excelente)

#### 💰 Incremento de Ingresos
Fórmula:
```
Incremento % = ((Ingresos_Nuevo - Ingresos_Actual) / Ingresos_Actual) × 100
```

Ejemplo:
```
Actual: 476,538 Bs
Óptimo: 643,250 Bs
Incremento: ((643,250 - 476,538) / 476,538) × 100 = 35%
```

---

## 🏆 Resultados Clave

### Resumen Cuantitativo

| Métrica | Baseline | Óptimo | Mejora | Significado |
|---------|----------|--------|--------|-------------|
| **Ingresos mensuales** | 476,538 Bs | 643,250 Bs | **+35%** | +2M Bs/año adicionales |
| **Ocupación general** | 35.7% | 55.2% | **+54.6%** | Mejor uso de capacidad |
| **Ocupación pisos 4-8** | 28.1% | 58.4% | **+107.8%** | Equilibrio entre pisos |
| **Tiempo espera salida** | 5.2 min | 0.8 min | **-84.6%** | Experiencia mejorada |
| **Vehículos atendidos** | 4,852 | 6,050 | **+24.7%** | Más clientes servidos |
| **Satisfacción (NPS)** | 6.2/10 | 9.2/10 | **+48.4%** | Mayor lealtad cliente |

### Comparación de Escenarios (Ranking)

```
🥇 1º - Escenario Óptimo Integral (ESC-5)
   └─ Ingresos: 643,250 Bs | Ocupación: 55.2% | Satisfacción: 9.2
   └─ ✅ RECOMENDADO

🥈 2º - Tarifas Diferenciadas (ESC-2A-2)
   └─ Ingresos: 562,345 Bs | Ocupación: 46.5% | Satisfacción: 7.8
   └─ ⚡ Alternativa si presupuesto limitado

🥉 3º - Menos Motos (ESC-3A-1)
   └─ Ingresos: 548,920 Bs | Ocupación: 42.3% | Satisfacción: 7.5
   └─ 💡 Buen impacto, sin inversión tecnológica

4º - Pago Automático (ESC-1B-2)
   └─ Mejora operativa sin impacto financiero directo

5º - 4 Casetas (ESC-1A-2)
   └─ Solución tradicional, menos eficiente que automatización

6º - Baseline (situación actual)
   └─ ❌ Mantener status quo significa pérdida de oportunidad
```

### Beneficios Cualitativos

Además de las mejoras numéricas, se logra:

- ✅ **Cumplimiento normativo**: 68% eléctricos en Piso 4
- ✅ **Imagen corporativa**: Parqueo moderno e inteligente
- ✅ **Ventaja competitiva**: Diferenciación por tecnología
- ✅ **Sostenibilidad**: Incentivos a vehículos eléctricos
- ✅ **Escalabilidad**: Modelo replicable en otros parqueos
- ✅ **Data-driven**: Decisiones basadas en datos reales

---

## 💻 Tecnologías Utilizadas

### Frontend
- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos, gradientes, animaciones
- **JavaScript ES6+**: Lógica de interacción, manipulación DOM

### Visualización de Datos
- **Chart.js v4.4.0**: Biblioteca de gráficos
  - Gráficos de barras
  - Gráficos de líneas
  - Gráficos radar (multidimensional)

### Hosting
- **GitHub Pages**: Hosting estático gratuito

### Herramientas de Desarrollo
- **Git**: Control de versiones
- **VS Code**: Editor de código
- **Chrome DevTools**: Debugging y testing

### Ventajas Técnicas

✅ **Sin dependencias npm**: Carga directa desde CDN  
✅ **Un solo archivo**: index.html autocontenido  
✅ **Responsive**: Funciona en móviles y tablets  
✅ **Rápido**: Carga en <2 segundos  
✅ **SEO-friendly**: HTML semántico  

---

## 🎮 Cómo Usar el Dashboard

### Navegación Básica

1. **Acceder al Dashboard**
   - Abre el enlace: `https://TU-USUARIO.github.io/parkingzone-dashboard`
   - Compatible con Chrome, Firefox, Safari, Edge

2. **Cambiar entre Secciones**
   - Clic en las pestañas superiores:
     - 📊 Resumen Ejecutivo
     - 📈 Comparación Escenarios
     - 💰 Análisis Financiero
     - ⚙️ Métricas Operacionales
     - ✅ Recomendaciones

3. **Interactuar con Gráficos**
   - **Hover**: Pasa el mouse sobre elementos para ver detalles
   - **Tooltip**: Aparece información exacta al posicionarte
   - **Leyenda**: Clic en elementos de leyenda para mostrar/ocultar series

### Tips de Uso

💡 **Para Presentaciones**:
- Inicia en "Resumen Ejecutivo" para contexto general
- Navega a "Comparación" para mostrar alternativas
- Termina en "Recomendaciones" con el plan de acción

💡 **Para Análisis Detallado**:
- Usa "Análisis Financiero" para justificación económica
- Consulta "Métricas Operacionales" para indicadores técnicos

💡 **Para Compartir**:
- El enlace es permanente y estático
- Funciona sin instalación
- Accesible desde cualquier dispositivo

---

### Referencias Bibliográficas

- Law, A. M. (2015). *Simulation Modeling and Analysis* (5th ed.). McGraw-Hill.
- Banks, J., et al. (2010). *Discrete-Event System Simulation*. Pearson.
- Winston, W. L. (2004). *Operations Research: Applications and Algorithms*. Thomson.
- Montgomery, D. C. (2017). *Design and Analysis of Experiments*. Wiley.

---

## 📝 Licencia

Este proyecto está bajo la Licencia MIT.

```
MIT License

Copyright (c) 2025 Rolando Vasquez

Se permite el uso, copia, modificación y distribución de este software
con fines académicos y educativos.
```
---

## 🎯 Conclusión

Este dashboard representa la culminación de un proyecto integral de simulación que:

1. ✅ **Identifica problemas reales** en un sistema operativo
2. ✅ **Aplica metodología científica** (10 etapas de simulación)
3. ✅ **Propone soluciones cuantificadas** con métricas claras
4. ✅ **Presenta resultados profesionalmente** mediante visualización
5. ✅ **Genera valor real** (+35% ingresos, -85% tiempo espera)

Los hallazgos y recomendaciones están listos para ser implementados en un caso real, demostrando la aplicabilidad práctica de la simulación en la optimización de sistemas complejos.
