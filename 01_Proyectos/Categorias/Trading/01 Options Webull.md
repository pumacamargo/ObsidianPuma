# ✅ Options Trading Webull - Wheel Strategy

**Estado:** ✅ Activo (Operando posiciones reales)
**Prioridad:** 🔴 ALTA
**Progreso:** 70% (Prototipo terminado, trading activo)

---

## 📋 Resumen Ejecutivo

Implementación y operación activa de la estrategia Wheel en Webull con asistencia de IA y automatización. El prototipo está terminado y ya estoy ejecutando trades reales con capital de $3,000.

**Roles clave:**
- Claude AI: Asesoramiento para decisiones de entrada/salida
- N8N: Automatización de flujos
- Telegram Bot: Alertas diarias y monitoreo
- Webull: Ejecución de trades

---

## 📋 La Estrategia: Wheel Strategy

### Phase 1 - Sell Cash-Secured Puts
- **Vender puts** 10-15% por debajo del precio actual
- **Delta:** 0.20-0.30 (probabilidad de asignación 20-30%)
- **DTE:** 30-45 Días hasta expiración
- **Resultado:** Si es asignado → avanzar a Phase 2

### Phase 2 - Sell Covered Calls
- **Vender calls** 15-25% por encima del cost basis
- **Delta:** 0.20-0.30
- **Resultado:** Si es asignado → regresamos a Phase 1 con ganancia

---

## 💰 Reglas de Capital

- **Capital Total:** $3,000
- **Máx Desplegado:** 75% = $2,250
- **Mín Cash Reserve:** $500 (25%)

### Asignación por Ticker
- **QS (Quantum Sphere):** ~$1,150 (38% del capital)
- **F (Ford):** ~$1,330 (44% del capital)

---

## ⚙️ Reglas de Strikes

### QS (Quantum Sphere)
- Solo números enteros ($8.00, $8.50, $9.00, etc)
- Nunca por debajo de $8
- Ejemplo: $8, $8.50, $9, $9.50...

### F (Ford)
- Incrementos de $0.50
- Nunca por debajo de $11
- Ejemplo: $11, $11.50, $12, $12.50...

---

## 🎯 Reglas de Salida

### 50% Profit Rule ⭐ (MÁS IMPORTANTE)
- **Cerrar posición en 50% de ganancia**
- No ser codicioso esperando más
- Aplicar SIEMPRE, sin excepciones
- Ejemplo: Si gano $50, cierro. No espero $100.

### Rolling Trades
- **Hacer roll SI:**
  - Posición está >15% en contra AND
  - >21 DTE (días hasta expiración) AND
  - NO es semana de earnings
  - Siguiente expiración (30-45 DTE away) tiene mejor setup
- **Roll significa:** Cerrar posición actual + abrir en expiración más lejana

### Earnings Avoidance
- Nunca abrir nuevas posiciones en semana de earnings
- Si tienes posición abierta en earnings:
  - Considera cerrar antes si está ganando
  - Si está perdiendo, mantén y espera roll

---

## 🤖 Herramientas & Automatización

| Herramienta | Función | Frecuencia |
|------------|---------|-----------|
| **Webull** | Broker principal, ejecución de trades | Diaria |
| **Claude AI** | Asesoramiento sobre entrada/salida | Por necesidad |
| **N8N** | Automatización de flujos y alertas | Continuo |
| **Telegram Bot** | Alertas de cambios, posiciones, ganancias | Diaria |

---

## 📊 Posiciones Activas (Actualizar diariamente)

| Ticker | Tipo | Strike | Entrada | DTE Entrada | DTE Actual | P&L | Status | Acción |
|--------|------|--------|---------|------------|-----------|-----|--------|--------|
| QS | Put | - | - | - | - | - | - | - |
| F | Put | - | - | - | - | - | - | - |

**Leyenda:**
- **Tipo:** Put (venta de put) / Call (venta de call)
- **Status:** Abierta / En Monitoreo / Ganancia >50% (cerrar) / Pérdida >15% (evaluar roll)
- **Acción:** Próxima acción recomendada

---

## ✅ Tareas Diarias & Semanales

### Diariamente (5-10 minutos)
- [ ] **9:00 AM:** Revisar notificaciones de Telegram bot
- [ ] **Verificar Webull:**
  - Todas las posiciones abiertas
  - P&L actual
  - Buying power disponible
  - Margin utilizado (<75%)
- [ ] **12:00 PM:** Revisar alertas midday
- [ ] **4:15 PM:** Actualizar tabla de posiciones
- [ ] **Revisar si algún trade alcanzó 50% ganancia → VENDER**

### Semanalmente (1-2 horas)
- [ ] **Guardar trades en [[Trading Journal]]**
  - Precios de entrada/salida
  - Ganancia/pérdida
  - Análisis: ¿qué funcionó? ¿qué no?
- [ ] **Revisar Earnings Calendar**
  - Próximas 2 semanas para QS y F
  - Marcar semanas para evitar nuevas posiciones
- [ ] **Análisis de la semana:**
  - ¿Seguí la estrategia 100%?
  - ¿Tomé decisiones emocionales?
  - ¿Necesito ajustes?

### Mensualmente (2-3 horas)
- [ ] **Análisis profundo de resultados:**
  - Win rate actual vs 65%+ meta
  - Ganancia/pérdida neta
  - Ciclos Wheel completados
  - ¿La estrategia está funcionando?
- [ ] **Ajustes a la estrategia si es necesario**

---

## 📈 Métricas Principales

| Métrica | Meta | Actual | Estado |
|---------|------|--------|--------|
| Ganancia Neta (mensual) | $200-400 | - | 🔄 Tracking |
| Win Rate | 65%+ | - | 🔄 Tracking |
| Ciclos Wheel Completados | 2-3/mes | - | 🔄 Tracking |
| Capital Deployment | 75% | - | 🔄 Tracking |
| Promedio Ganancia/Trade | - | - | 🔄 Tracking |

---

## 🔄 Procedimiento para ROLL (Detallado)

**Usar SOLO si:**
- ✅ Posición >15% en contra
- ✅ >21 DTE
- ✅ NO es semana de earnings
- ✅ Siguiente expiración tiene mejor setup

**Pasos:**
1. Abrir Webull
2. Ir a posición actual (ejemplo: QS $8 Put)
3. Revisar siguiente expiración (30-45 DTE away)
   - ¿Qué strike tiene mejor delta?
   - ¿Vale la pena por comisiones?
4. Ejecutar:
   ```
   BTC (Buy to Close) la posición actual
   STO (Sell to Open) nueva posición en expiración más lejana
   ```
5. Documentar en Trading Journal:
   - Precio de cierre original
   - Precio de apertura del roll
   - Razón del roll
   - Nueva fecha de expiración

---

## 🔗 Documentos Relacionados
- [[00_Trading]] - Hub central de trading
- [[../../../Trading Journal]] - Registro de todos los trades
- [[../../../Checklist Diario Telegram Bot]] - Verificaciones diarias
- [[../../../Dashboard]] - Estado general

---

## 💡 Notas Críticas

1. **50% RULE ES ABSOLUTA** - No negociar esto
2. **Capital Management** - Nunca >75% deployed
3. **Earnings** - Siempre revisar calendario antes de abrir
4. **Margin Account** - Confirmar diariamente que está bien configurada
5. **Documentación** - Guardar CADA trade en journal para análisis
6. **Disciplina** - Seguir la estrategia 100%, sin emociones

---

## 📚 CURVA DE APRENDIZAJE (Fase Actual)

**Estado actual:** APRENDIENDO (Mes 1-2)
**P&L actual:** -$100 (normal en fase de aprendizaje)
**Trades/mes:** 2-3 (bajo volumen mientras aprendo)

### ¿Qué Esperar en los Primeros Meses?

**Mes 1-3: LEARNING PHASE** 🎓
- **P&L esperado:** -$100 a $0 (breakeven)
- **Objetivo:** NO es ganar dinero, es APRENDER
- **Focus:**
  - Entender mecánica de la estrategia
  - Practicar selección de strikes
  - Aprender a usar Webull interface
  - Cometer errores pequeños (mejor ahora que con $10K)
  - Documentar CADA decisión

**Indicadores de que estás aprendiendo bien:**
- ✅ Sigues las reglas 80%+ del tiempo
- ✅ Documentas trades en journal
- ✅ No entras en panic selling
- ✅ Entiendes POR QUÉ cierras en 50% profit
- ✅ No agregas capital todavía

**Errores comunes en Fase 1 (evitar):**
- ❌ Esperar ganancias inmediatas
- ❌ Cambiar estrategia cada semana
- ❌ Agregar más capital sin probar consistencia
- ❌ No documentar trades
- ❌ Operar basado en emociones

---

## 💰 PROYECCIONES DE INGRESOS REALISTAS

### Fase 1: Learning (Mes 1-3) - ACTUAL
**Capital:** $3,000
**Trades/mes:** 2-3
**Win Rate esperado:** 40-60% (aprendiendo)

| Escenario | P&L/Mes | P&L Acumulado 3 Meses |
|-----------|---------|----------------------|
| **Bajo** (muchos errores) | -$50 | -$150 |
| **Medio** (aprendiendo) | -$30 a $0 | -$90 a $0 |
| **Alto** (aprende rápido) | $0 a $50 | $0 a $150 |

**Nota:** Si pierdes más de $200 en 3 meses, PAUSAR y revisar estrategia con Claude.

---

### Fase 2: Consistencia (Mes 4-6)
**Capital:** $3,000 (no agregar hasta demostrar consistencia)
**Trades/mes:** 4-6 (más confianza)
**Win Rate esperado:** 60-70%

| Escenario | P&L/Mes | P&L Acumulado 3 Meses |
|-----------|---------|----------------------|
| **Bajo** | $30-50 | $90-150 |
| **Medio** | $80-120 | $240-360 |
| **Alto** | $150-200 | $450-600 |

**Trigger para Fase 3:** 3 meses consecutivos con P&L positivo + win rate >65%

---

### Fase 3: Rentable (Mes 7-12)
**Capital:** $3,000-5,000 (considerar agregar $2K si consistente)
**Trades/mes:** 6-10
**Win Rate esperado:** 65-75%

| Escenario | Capital | P&L/Mes | P&L Anual (6 meses) |
|-----------|---------|---------|---------------------|
| **Bajo** | $3,000 | $150-200 | $900-1,200 |
| **Medio** | $4,000 | $250-350 | $1,500-2,100 |
| **Alto** | $5,000 | $350-500 | $2,100-3,000 |

**Criterio para agregar capital:**
- ✅ 3 meses consecutivos rentables
- ✅ Win rate >65%
- ✅ Siguiendo reglas 90%+ del tiempo
- ✅ Journal documentado

---

### Fase 4: Escalado (Año 2+)
**Capital:** $5,000-10,000+
**Trades/mes:** 10-15
**Win Rate esperado:** 70%+

| Escenario | Capital | P&L/Mes | P&L Anual |
|-----------|---------|---------|-----------|
| **Bajo** | $5,000 | $300-400 | $3,600-4,800 |
| **Medio** | $7,500 | $500-650 | $6,000-7,800 |
| **Alto** | $10,000 | $700-1,000 | $8,400-12,000 |

**Meta objetivo:** $400-800/mes (alcanzable con $7,500-10,000 capital + 70% win rate)

---

## 🎯 CRITERIOS DE SELECCIÓN DE TICKERS

### Por Qué F (Ford) Tiene Premium Bajo
- **Precio bajo:** ~$11-12 → Premios pequeños ($20-40 típico)
- **Baja volatilidad:** Menos movimiento = menos prima
- **No ideal para Wheel con capital pequeño**

### Criterios para Buenos Tickers de Wheel

**1. Precio del Ticker:**
- ✅ **Ideal:** $15-50/acción
- ✅ **Razón:** Premios decentes sin requerir mucho capital
- ❌ **Evitar:** <$10 (premios muy bajos) o >$100 (requiere mucho capital)

**2. Volatilidad (IV):**
- ✅ **Ideal:** IV 40-80%
- ✅ **Razón:** Más volatilidad = mejores premios
- ❌ **Evitar:** IV <30% (premios insignificantes)

**3. Liquidez de Opciones:**
- ✅ **Ideal:** Open Interest >500, Bid-Ask Spread <$0.10
- ✅ **Razón:** Fácil entrar/salir, no pierdes en spread

**4. Empresas que Conoces/Entiendes:**
- ✅ **Ideal:** Empresas sólidas que no te importaría tener acciones
- ✅ **Razón:** Si te asignan, estás OK con mantener

### Tickers Recomendados para Reemplazar F

| Ticker | Precio | IV Típica | Por Qué Es Bueno |
|--------|--------|-----------|------------------|
| **PLTR** | $25-35 | 60-80% | Alta volatilidad, buenas premios |
| **AMD** | $140-180 | 50-70% | Tech popular, líquido |
| **NVDA** | $120-140 | 50-70% | Muy líquido, buenas premios |
| **SOFI** | $8-12 | 70-90% | Alta IV = premios altos |
| **NIO** | $5-8 | 80-100% | Muy volátil, premios grandes |

**Recomendación:** Considera cambiar F por **PLTR** o **SOFI** (similar capital requerido pero mejores premios)

### Cómo Investigar Nuevos Tickers
1. **Screener en Webull:**
   - Filtrar por precio $15-50
   - IV >50%
   - Volumen opciones >1,000

2. **Validar con Claude:**
   - "¿Es [TICKER] bueno para Wheel strategy?"
   - Revisar fundamentals básicos

3. **Paper trade primero:**
   - Probar 1-2 ciclos antes de usar capital real

---

## 💸 IMPUESTOS & FISCALIDAD (Pendiente Investigar)

**Situación:** Vives en Japón, operas en Webull (broker USA)

### Tareas Pendientes 🚨
- [ ] **Investigar impuestos de trading en Japón:**
  - ¿Cómo reportar ganancias de broker extranjero?
  - ¿Retención automática o declaración manual?
  - ¿Impuesto sobre ganancias de capital en Japón?

- [ ] **Consultar con accountant/asesor fiscal:**
  - Idealmente uno que entienda USA + Japón
  - Costo típico: $200-500/año

- [ ] **Documentar proceso para próximo año fiscal:**
  - ¿Qué formularios necesito?
  - ¿Cuándo declarar?

### Recursos Iniciales
- **Japan Tax Agency:** https://www.nta.go.jp/english/
- **r/JapanFinance** (Reddit) - Comunidad de expats
- **Webull Tax Documents:** Disponibles en febrero/marzo

**Nota:** NO dejar esto para último momento. Investigar AHORA aunque aún no seas rentable.

---

## 🆚 COMPARACIÓN: Wheel vs Iron Condor

### Por Qué Elegiste Wheel

**Contexto:**
- Amigo trader recomendó estrategia
- AI (Claude) recomendó Iron Condor inicialmente
- Con $3,000 USD, Iron Condor no viable
- AI también recomendó Wheel como mejor opción

### Iron Condor vs Wheel con $3K

| Criterio | Iron Condor | Wheel |
|----------|-------------|-------|
| **Capital mínimo** | $5,000-10,000 | $2,000-3,000 ✅ |
| **Margen requerido** | Alto | Moderado ✅ |
| **Complejidad** | 4 legs, más difícil | 1-2 legs, simple ✅ |
| **Win rate típico** | 70-80% | 65-75% |
| **Profit por trade** | Pequeño ($50-150) | Variable ($50-300) |
| **Riesgo** | Limitado pero complejo | Moderado, más claro ✅ |
| **Mejor para** | $10K+ capital | $3K-5K capital ✅ |

**Conclusión:** Wheel es la estrategia correcta para tu capital actual. Cuando llegues a $10K+, puedes explorar Iron Condor.

---

## 📊 EJEMPLOS DE TRADES (Por Documentar)

### Trade Ejemplo #1 - [PENDIENTE]
**Ticker:** TBD
**Tipo:** Put / Call
**Fecha Entrada:** TBD
**Strike:** TBD
**Prima Recibida:** TBD
**DTE Entrada:** TBD
**Fecha Salida:** TBD
**P&L:** TBD
**Notas:** ¿Qué salió bien? ¿Qué mejorar?

### Trade Ejemplo #2 - [PENDIENTE]
(Agregar cuando tengas más trades documentados)

**Acción:** Documentar próximos 3-5 trades aquí para análisis

---

## 🚀 PLAN DE ESCALADO DE CAPITAL

### Cuándo Agregar Más Capital

**NO agregar capital si:**
- ❌ Win rate <60%
- ❌ Menos de 3 meses trading
- ❌ P&L negativo en últimos 2 meses
- ❌ No sigues reglas consistentemente

**SÍ agregar capital si:** ✅
- ✅ **3 meses consecutivos rentables**
- ✅ Win rate >65%
- ✅ Siguiendo reglas 90%+ del tiempo
- ✅ Journal documentado (prueba de disciplina)
- ✅ Entiendes POR QUÉ ganas/pierdes

### Cuánto Agregar

**Fase 1 → Fase 2:**
- Actual: $3,000
- Agregar: $1,000-2,000
- Nuevo total: $4,000-5,000
- **Requisito:** 3 meses rentables consecutivos

**Fase 2 → Fase 3:**
- Actual: $4,000-5,000
- Agregar: $2,000-3,000
- Nuevo total: $7,000-8,000
- **Requisito:** 6 meses rentables, win rate >70%

**Fase 3 → Fase 4:**
- Actual: $7,000-8,000
- Agregar: $2,000-5,000
- Nuevo total: $10,000-15,000
- **Requisito:** 1 año rentable, estrategia validada

### Fuente del Capital Nuevo
- ✅ Ganancias de otros proyectos (Trading NinjaTrader, Content Creation)
- ✅ Ahorros personales (solo si cómodo perdiendo)
- ❌ Deuda o préstamos (NUNCA)

---

## ⏱️ TIEMPO DE DEDICACIÓN

**Tiempo diario:** 10-20 minutos
**Desglose:**
- 5 min - Revisar posiciones en Webull
- 5 min - Verificar alertas/Telegram
- 5-10 min - Consultar con Claude si necesario
- 0-5 min - Ejecutar trades (si hay señal)

**Tiempo semanal adicional:** 30-60 minutos
- Documentar trades en journal (10 min)
- Revisar earnings calendar (5 min)
- Análisis semanal de resultados (15-30 min)
- Research de nuevos tickers (opcional, 15-30 min)

**Total/semana:** ~2-3 horas (muy manejable)

**Nota:** Esta es una estrategia PART-TIME. No requiere estar pegado a la pantalla.
