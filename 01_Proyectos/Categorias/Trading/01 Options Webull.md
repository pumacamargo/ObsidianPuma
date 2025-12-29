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
