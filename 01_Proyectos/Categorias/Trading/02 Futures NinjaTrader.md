# 🤖 Quantum Liberty - MNQ Futures Trading Bot

**Estado:** 🟡 En Pivot (Simplificación)
**Prioridad:** 🔴 ALTA
**Progreso:** 35% (Framework base existente, pivotando a estrategias simples)

---

## 📋 Resumen Ejecutivo

**PIVOT DECISION:** El proyecto original era demasiado complejo (3 modelos IA: XGBoost + LSTM + DQN). Ahora estamos simplificando a un **framework modular en Python** que puede ejecutar diferentes estrategias simples de trading en MNQ (Micro Nasdaq Futures).

**Nuevo Enfoque:**
- Framework base que gestiona ejecución + risk management
- Estrategias intercambiables y seleccionables
- Bridge con NinjaTrader para ejecución
- Objetivo: Trading consistente a largo plazo en prop firms

---

## 🎯 Nuevo Objetivo

✅ Crear un bot flexible que pueda ejecutar X estrategias diferentes
✅ Seleccionar estrategia desde un menú/config
✅ Risk management automatizado (stop loss, position sizing)
✅ Validar cada estrategia en paper trading antes de prop firm
✅ Generar ingresos consistentes pasando challenges en prop firms
✅ Timeframe: Daily trading (swing/posición, 1-2 trades/día máx)

---

## 📊 Estado Actual del Proyecto

| Fase | Descripción | Status | % Completado |
|------|-------------|--------|-------------|
| 1. Framework Base | Servers Python + API listos | ✅ Completado | 80% |
| 2. Arquitectura | Definir estructura modular | 🟡 En Progreso | 40% |
| 3. Estrategia 1 | Implementar primera estrategia simple | 🔵 Planificación | 0% |
| 4. Backtesting | Validar en datos históricos | 🔵 Planificación | 0% |
| 5. Paper Trading | Prueba sin dinero real | 🔵 Planificación | 0% |
| 6. Prop Firm Testing | Pasar challenges y generar ingresos | 🔵 Futuro | 0% |

---

## 📐 Especificaciones del Bot

### Mercado Objetivo
- **Contrato:** MNQ (Micro Nasdaq Futures)
- **Razón:** Liquido, bajo capital requerido para prop firms
- **Contratos máximos:** 1-2 simultáneos

### Timeframe & Operación
- **Timeframe:** Daily (Cierre de vela diaria)
- **Trades esperados:** 1-2 por día máximo
- **Horarios:** Mercado regular (9:30-16:00 ET)
- **Evitar:** Últimos 15 min de cierre, earnings week

### Risk Management (Consistente para todas las estrategias)
- **Stop Loss:** 50-100 pips (configurable por estrategia)
- **Take Profit:** 100-200 pips (configurable)
- **Position Size:** 1 MNQ = $100 por punto
- **Max Loss/Día:** -$500 USD
- **Max Trades/Día:** 2 máximo
- **Ratio R:R:** 1:2 mínimo

### Reglas Generales del Bot
- Solo 1 estrategia activa a la vez
- Validación de horario antes de operar
- Log de todos los trades en archivo
- Alertas a Telegram en cada operación

---

## 🎯 3 Estrategias Recomendadas para Implementar

### 1. ⬆️ Trend Following (Seguidor de Tendencia)
**Lógica Simple:**
- Media móvil rápida (8 días) > Media móvil lenta (21 días) = TREND UP
- Comprar en retroceso hacia MA8 con RSI >40
- Vender en target o cuando MA8 cruza bajo MA21

**Ventajas:** Funciona bien en mercados con tendencia
**Riesgo:** Se queda atrapado en rangos

**Parámetros:**
- MA Rápida: 8
- MA Lenta: 21
- SL: 80 pips
- TP: 160 pips
- Ver detalles: [[Estrategias/01 Trend Following]]

---

### 2. 🔄 Mean Reversion (Reversión a la Media)
**Lógica Simple:**
- RSI >70 (overbought) = Vender
- RSI <30 (oversold) = Comprar
- Tomar ganancias en media móvil de 20 periodos

**Ventajas:** Excelente en mercados sin tendencia
**Riesgo:** Falla si inicia tendencia fuerte

**Parámetros:**
- RSI Período: 14
- Overbought: >70
- Oversold: <30
- SL: 100 pips
- TP: 150 pips
- Ver detalles: [[Estrategias/02 Mean Reversion]]

---

### 3. 📊 Volume Profile (Perfil de Volumen)
**Lógica Simple:**
- Identificar niveles de alto volumen (soporte/resistencia)
- Comprar/vender cerca de estos niveles
- TP en siguiente nivel de volumen

**Ventajas:** Niveles dinámicos basados en precio real
**Riesgo:** Requiere más datos históricos para calcular

**Parámetros:**
- Período para calcular volumen: 20 días
- Threshold de volumen: >75 percentil
- SL: 60 pips
- TP: 120 pips
- Ver detalles: [[Estrategias/03 Volume Profile]]

---

## 📋 Roadmap de Implementación

### Phase 1: Framework Base (Esta Semana) - 2-3 días
- [ ] Limpiar/refactorizar código Python existente
- [ ] Crear estructura modular (estrategias como módulos)
- [ ] Sistema de selección de estrategia (config/menú)
- [ ] Documentar arquitectura en [[Bot Architecture]]

### Phase 2: Estrategia 1 - Trend Following (Semana 2) - 3-4 días
- [ ] Implementar lógica de Trend Following
- [ ] Agregar validaciones (horario, max trades, etc)
- [ ] Backtesting con 1 año de datos MNQ
- [ ] Documentar resultados

### Phase 3: Backtesting & Ajustes (Semana 3) - 3-4 días
- [ ] Analizar métricas de backtesting
- [ ] Optimizar parámetros si es necesario
- [ ] Validar que gana después de comisiones
- [ ] Crear reportes

### Phase 4: Paper Trading (Semana 4) - 1 semana
- [ ] Conectar bot a NinjaTrader con paper money
- [ ] Monitorear 5 días de trades en vivo
- [ ] Validar ejecución correcta
- [ ] Documentar cualquier issue

### Phase 5: Estrategia 2 (Semana 5) - Similar a Phase 2-4
- [ ] Implementar Mean Reversion
- [ ] Backtesting
- [ ] Paper Trading

### Phase 6: Lanzamiento a Prop Firm (Semana 6+)
- [ ] Seleccionar prop firm con desafío menor
- [ ] Ir live con capital cuenta prop
- [ ] Pasar challenge y generar ingresos

---

## 📊 Métricas de Backtesting

Cuando hagas backtest, busca estas métricas:

| Métrica | Meta | Actual |
|---------|------|--------|
| Win Rate | 60%+ | - |
| Profit Factor | 1.5+ | - |
| Max Drawdown | <20% | - |
| Recovery Factor | >2.0 | - |
| Avg Winner/Loser Ratio | 1.5:1 | - |
| Total Trades | 100+ | - |

---

## 🤖 Stack Tecnológico

| Componente | Tecnología | Status |
|-----------|-----------|--------|
| **Servidor de Señales** | Python + TA-Lib | ✅ Existente |
| **API REST** | Python Flask/FastAPI | ✅ Existente |
| **Bridge NT** | Socket/HTTP a NinjaTrader | 🟡 En desarrollo |
| **Base de Datos** | SQLite (logs de trades) | ✅ Existente |
| **Alertas** | Telegram Bot API | ✅ Existente |
| **Backtest** | Pandas + TA-Lib | ✅ Existente |

---

## 📚 Documentación Relacionada

- [[Bot Architecture]] - Arquitectura técnica del framework (POR CREAR)
- [[Estrategias/01 Trend Following]] - Detalles estrategia 1 (POR CREAR)
- [[Estrategias/02 Mean Reversion]] - Detalles estrategia 2 (POR CREAR)
- [[Estrategias/03 Volume Profile]] - Detalles estrategia 3 (POR CREAR)
- [[../../Trading Journal]] - Registrar resultados de backtesting

---

## 📈 Checklist de Backtesting

Cuando hagas backtest, verificar:
- [ ] Mínimo 1 año de datos históricos
- [ ] >100 trades en el período
- [ ] Incluir períodos de tendencia y rango
- [ ] Revisar drawdown máximo
- [ ] Calcular ratio sharpe
- [ ] Análisis de pérdidas consecutivas
- [ ] ¿Es rentable después de comisiones?

---

## ⚠️ Errores Comunes a Evitar

1. **Overfitting** - Estrategia perfecta en backtest pero falla en real
2. **Curva fitting** - Optimizar demasiado para un período específico
3. **No incluir slippage** - Asumir ejecución al precio exacto (no realista)
4. **Ignorar comisiones** - Backtesting perfecto puede ser improfitable con comisiones
5. **No limitar riesgo** - Sin stop loss fijo es desastres garantizado
6. **Cambios constantes** - Tweakear estrategia cada que baja el precio
7. **No validar antes de prop** - Paper trading es OBLIGATORIO antes de dinero real

---

## 🔗 Documentos Relacionados
- [[00_Trading]] - Hub central de trading
- [[../../../Trading Journal]] - Registrar backtest y resultados reales
- [[../../../Dashboard]] - Estado general de proyectos
- [[../../../Checklist Diario Telegram Bot]] - Monitoreo diario

---

## 📌 Próximas Acciones Inmediatas

1. **Esta semana:**
   - [ ] Crear documento [[Bot Architecture]]
   - [ ] Crear carpeta Estrategias con 3 sub-notas
   - [ ] Comenzar refactoring del código existente

2. **Semana que viene:**
   - [ ] Implementar Trend Following
   - [ ] Primeros backtests

**Nota:** El framework base ya existe (80% completado). Solo hay que conectar piezas e implementar estrategias simples.
