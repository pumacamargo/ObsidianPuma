# 📱 Checklist Diario - Telegram Bot

## Propósito
Registro diario de lo que el bot de Telegram debe revisar y alertarte, y checklist manual para antes de operar.

---

## 🤖 Lo que el Bot debe monitorear y alertarte

### Alertas en Tiempo Real
- [ ] Cambios >10% en precio de QS
- [ ] Cambios >10% en precio de F
- [ ] Si el delta de posición abierta cambia >0.05
- [ ] Si una posición abierta alcanza 50% de ganancia (VENDER)
- [ ] Si una posición abierta está >15% en contra con >21 DTE (EVALUAR ROLL)
- [ ] Earnings announcement para QS o F (próximas 2 semanas)

### Alertas Diarias (9:30 AM - Apertura del Mercado)
- [ ] Resumen de todas las posiciones abiertas
- [ ] P&L actual de posiciones (ganancia/pérdida acumulada)
- [ ] Días hasta expiración de cada contrato abierto
- [ ] Capital deployment actual vs meta (75%)
- [ ] Buying power disponible en Webull

### Alertas Semanales (Viernes)
- [ ] Resumen semanal de trades completados
- [ ] Win rate de la semana
- [ ] Ganancia/pérdida neta de la semana
- [ ] Próximas acciones para la semana siguiente

---

## ✅ Checklist Manual Diario

**Tiempo recomendado:** 5-10 minutos

### Mañana (Antes de mercado)
- [ ] **9:00 AM:** Revisar notificaciones de Telegram
- [ ] Abrir Webull y verificar que todo esté como se dejó ayer
- [ ] Revisar Earnings Calendar (TradingView, Bloomberg, o similar)
  - ¿Hay earnings esta semana para QS o F?
  - Si sí, NO abrir nuevas posiciones
- [ ] Revisar precio actual de QS y F
  - Nota: ¿Se mueve hacia mis strikes?

### Durante Mercado (Midday Check)
- [ ] **12:00 PM:** Revisar alertas del bot
- [ ] Si hay alertas:
  - [ ] Posición alcanzó 50% ganancia → VENDER AHORA
  - [ ] Posición >15% en contra con >21 DTE → Evaluar ROLL
    - Pasos para roll: [Ver sección abajo]
  - [ ] Precio cambió >10% → Documentar en journal, evaluar si afecta estrategia

### Cierre de Mercado (4:00 PM)
- [ ] **4:15 PM:** Revisar estado final del día
- [ ] Actualizar tabla de posiciones en Trading Journal
- [ ] ¿Se completó algún trade hoy?
  - Si sí, documentar en [[Trading Journal]]
- [ ] ¿Necesito abrir nuevo trade mañana?
  - Si sí, revisar condiciones (precio, DTE, delta)

---

## 🔄 Procedimiento para ROLL de Posición

**Solo hacer roll si:**
- ✅ Posición está >15% en contra
- ✅ Tiene >21 DTE
- ✅ NO es semana de earnings
- ✅ Siguiente expiración (30-45 DTE) tiene mejor setup

**Pasos:**
1. Abrir Webull
2. Identificar la posición a hacer roll
3. Ver opciones de siguiente expiración (30-45 DTE away)
4. Ejecutar:
   - Cerrar la posición actual (BTC si es PUT, STC si es CALL)
   - Abrir nueva posición en expiración más lejana
   - Mismo strike o ligeramente más OTM para mejorar probabilidad
5. Documentar en Trading Journal:
   - Precio de cierre original
   - Precio de apertura del roll
   - Razón del roll
   - Nueva fecha de expiración

---

## 📊 Verificación de Margin Account Webull

**Esta es una verificación CRÍTICA diaria:**

- [ ] Ir a Webull → Account → Margin
- [ ] Verificar:
  - **Cash-Secured Puts:** Capital reservado está disponible
  - **Buying Power:** Suficiente para abrir nuevas posiciones
  - **Margin Utilizado:** No >75% del capital total
  - **Maintenance Requirement:** Si >50%, NO abrir nuevas posiciones

**Fórmula:**
```
Capital Deployment = (Capital Utilizado) / Capital Total
Meta: 75% máx
Mínimo Cash Reserve: $500
```

Ejemplo:
- Capital Total: $3,000
- Capital en puts/calls: $2,250 (75%)
- Cash Reserve: $750 (25%)
- ✅ CORRECTO

---

## 🚨 Alertas de Acción Requerida

### Escenario: Posición alcanza 50% de ganancia
**Acción:** VENDER INMEDIATAMENTE
- No esperar a que expire
- No ser codicioso
- Repetir: **50% PROFIT RULE SIEMPRE**
- Documentar en Trading Journal

### Escenario: Posición >15% en contra, >21 DTE
**Acción:** Evaluar ROLL
- ¿Siguiente expiración tiene mejor delta?
- ¿Vale la pena el trade (comisiones vs ganancia esperada)?
- Si yes → ROLL
- Si no → Dejar que expire o cerrar

### Escenario: Earnings próximas
**Acción:** EVITAR NUEVAS POSICIONES
- Revisar earnings calendar semanalmente
- NO abrir puts/calls en semana de earnings
- Si tienes posición abierta y earnings llegan:
  - Considera cerrar antes de earnings si está ganando
  - Si está perdiendo, mantén y espera roll (si aplica)

### Escenario: Cambio >10% en precio
**Acción:** REVISAR IMPACTO
- ¿Afecta mis deltas?
- ¿Sigue siendo probable que se ejecute mi plan?
- ¿Necesito hacer ajustes?
- Documentar en journal

---

## 📋 Template Diario Rápido

Copiar y pegar cada día después de cerrado el mercado:

```
## [Fecha - DD/MM/YYYY]

**Posiciones Abiertas:**
- QS: [Tipo] [Strike] - P&L: $[X]
- F: [Tipo] [Strike] - P&L: $[X]

**Acciones Hoy:**
- [ ] Revisé Telegram bot
- [ ] Revisé Webull margin
- [ ] Revisé earnings calendar
- [ ] Documenté movimientos

**Notas:**
-

**Próxima Acción:**
-
```

---

## 🤖 Integración N8N Sugerida

Para automatizar algunas alertas, considera:
1. **N8N Telegram Integration:**
   - Conectar Webull API (si disponible)
   - Enviar resumen diario a 9:30 AM
   - Alertas de precio en tiempo real

2. **Alerts que se pueden automatizar:**
   - Precio cambió >10%
   - Posición alcanzó 50% ganancia
   - Earnings announcement
   - Resumen diario de P&L

---

## 📚 Referencias
- [[Categorias/Trading]] - Reglas de la estrategia
- [[Trading Journal]] - Registro de trades
- [[Dashboard]] - Estado general
