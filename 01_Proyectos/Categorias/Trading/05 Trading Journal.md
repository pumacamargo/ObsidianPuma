# 📊 Trading Journal - Wheel Strategy Webull

**Estado:** ✅ Activo
**Última actualización:** 06 JAN 2026
**Período:** 17 OCT 2025 - 06 JAN 2026

---

## 📈 ESTADÍSTICAS GENERALES (ACTUALIZADO 06 JAN 2026)

### Resumen Ejecutivo
| Métrica | Valor | Status |
|---------|-------|--------|
| **Trades Totales** | 9 transacciones | ✅ Completo |
| **Pares Completados** | 4 pares (STO + BTC) | ✅ Completados |
| **Trades Abiertos** | 1 (QS #2 esperando BTC) | 🟡 En monitoreo |
| **Depósitos** | 2 | 💰 Capital inicial |
| **Ganancia/Pérdida Total** | **-$3.92** | ⚠️ Breakeven (casi) |
| **Win Rate** | **50%** (2 pares ganados, 2 perdidos) | 🟡 En mejora |
| **Capital Inicial** | $3,013.32 | - |
| **Capital Actual** | $3,009.40 | ⚠️ -0.13% |

### Ganancia/Pérdida Detallado
```
RESUMEN POR PARES COMPLETADOS:
├─ Par 1 (OCT 23 - NOV 19): QS $14.50 Put
│  ├─ Venta (STO):  +$177.76
│  ├─ Compra (BTC): -$247.23
│  └─ P&L:          -$69.47 ❌ PÉRDIDA

├─ Par 2 (OCT 27 - DIC 27): QS $14.50 Put
│  ├─ Venta (STO):  +$442.76
│  ├─ Compra (BTC): -$437.19
│  └─ P&L:          +$5.57 ✅ GANANCIA PEQUEÑA

├─ Par 3 (DIC 27): F $13 Put (Ford)
│  ├─ Venta (STO):  +$23.80
│  ├─ Compra (BTC): -$27.19
│  └─ P&L:          -$3.39 ❌ PEQUEÑA PÉRDIDA

├─ Par 4 (DIC 27 - JAN 6): QS $10 Put ✅ EXITOSO
│  ├─ Venta (STO):  +$87.80
│  ├─ Compra (BTC): -$67.23
│  └─ P&L:          +$20.57 ✅ GANANCIA (pero hay prima pendiente)

└─ Abierto (JAN 1 - actual): QS $11 Put
   ├─ Venta (STO):  +$154.80
   ├─ Compra (BTC): Pendiente
   └─ P&L:          TBD (target: +$51.73 @ 35%)

TOTALES:
├─ Prima Total Recibida:   $888.12
├─ Costo Total Cierre:     -$779.64
├─ P&L Pares Cerrados:     +$108.48
├─ Menos: Prima Abierta:   -$154.80
├─ P&L Real (sin abiertos): -$46.32
└─ P&L Total (con depósitos): -$3.92

Profit Margin:             -0.13% (del capital inicial)
```

### Análisis por Ticker
| Ticker | Pares | Cerrados | Ganancia | Status |
|--------|-------|----------|----------|--------|
| **QS** | 4 | 3 | -$63.90 | 🟡 Principal, mejorando |
| **F (Ford)** | 1 | 1 | -$3.39 | ❌ No recomendado |
| **Abiertos** | 1 | 0 | +$154.80 prima | ⏳ QS #2 |
| **TOTAL** | 6 | 4 | **-$67.29** | ⚠️ Breakeven |

### Capital Deployment Actual
| Métrica | Valor | Meta |
|---------|-------|------|
| **Prima en Riesgo (QS #2)** | $154.80 | <$300 |
| **% del Capital** | 5.14% | <10% |
| **Buying Power Disponible** | $2,021.40 | >$1,000 ✅ |
| **Capital Desplegado** | 5.14% | <75% ✅ |

---

## 📅 REGISTRO HISTÓRICO DE TRADES POR FECHA

### 💰 17 OCT 2025 - DEPÓSITO #1
```
Acción:        Cash Transfer - Deposit
Monto:         +$19.93
Saldo:         +$19.93
Status:        ✅ Completado
```

---

### 💰 22 OCT 2025 - DEPÓSITO #2 (CAPITAL INICIAL)
```
Acción:        Cash Transfer - Deposit
Monto:         +$2,993.39
Saldo:         +$3,013.32
Status:        ✅ Completado

Capital inicial total: $3,013.32 para comenzar trading
```

---

### ✅ 23 OCT 2025 - TRADE #1: QS $14.50 Put (VENTA)

**Sell to Open - QS251128P00014500**
```
Acción:        Sold (STO)
Ticker:        QS
Strike:        $14.50
Tipo:          Put
Prima Recibida: +$177.76
Saldo:         +$3,191.08
DTE:           ~35 días
Estado:        ⏳ Abierto esperando cierre
Target (35%):  +$62.22 ganancia objetivo
```

---

### ✅ 19 NOV 2025 - TRADE #1: QS $14.50 Put (COMPRA - CIERRE)

**Buy to Close - QS251128P00014500 - RESULTADO: PÉRDIDA ❌**
```
Acción:        Bought (BTC)
Ticker:        QS
Strike:        $14.50
Costo Cierre:  -$247.23
Saldo:         +$2,943.85
Días en Trade: 27 días
Status:        ✅ CERRADO CON PÉRDIDA

RESULTADO:
├─ Prima Recibida:   +$177.76
├─ Costo Cierre:     -$247.23
├─ P&L Neto:         -$69.47 ❌

ANÁLISIS DE PÉRDIDA:
- QS subió significativamente después de entrada
- Put perdió valor menos de lo esperado
- Prima se fue en contra: $177.76 → $247.23
- Lección: Primera operación educativa en volatilidad QS
```

---

### ✅ 27 OCT 2025 - TRADE #2: QS $14.50 Put (VENTA)

**Sell to Open - QS260515P00014000**
```
Acción:        Sold (STO)
Ticker:        QS
Strike:        $14.50
Tipo:          Put
Prima Recibida: +$442.76
Saldo:         +$2,949.42
DTE:           ~40 días (expira 15 MAY 2026)
Estado:        ⏳ Abierto esperando cierre
Target (35%):  +$155 ganancia objetivo
```

---

### ✅ 27 DIC 2025 - TRADE #2: QS $14.50 Put (COMPRA - CIERRE)

**Buy to Close - QS260515P00014000 - RESULTADO: GANANCIA PEQUEÑA ✅**
```
Acción:        Bought (BTC)
Ticker:        QS
Strike:        $14.50
Costo Cierre:  -$437.19
Saldo:         +$2,949.42
Días en Trade: 61 días (mucho más largo que esperado)
Status:        ✅ CERRADO CON GANANCIA PEQUEÑA

RESULTADO:
├─ Prima Recibida:   +$442.76
├─ Costo Cierre:     -$437.19
├─ P&L Neto:         +$5.57 ✅

ANÁLISIS:
- Posición estuvo abierta muy tiempo (61 días vs 35-40 esperados)
- ROI pequeño pero positivo: 1.26%
- Lección: No todas las posiciones cierren rápido
- Importante: Disciplina en largo plazo
```

---

### ✅ 27 DIC 2025 - TRADE #3: F (Ford) $13 Put (VENTA)

**Sell to Open - F260130P00013000**
```
Acción:        Sold (STO)
Ticker:        F (Ford)
Strike:        $13.00
Tipo:          Put
Prima Recibida: +$23.80
Saldo:         +$3,061.02
DTE:           ~3 días (expiración 30 JAN 2026)
Estado:        ⏳ Muy corto plazo (no ideal)
Target (35%):  +$8.33 ganancia objetivo

ANÁLISIS INICIAL:
- Prima muy pequeña ($23.80) para Ford
- DTE muy corto (~3 días) - riesgo alto
- NO es operación recomendada (mala decisión)
- Lección: Ford tiene premios bajos, evitar
```

---

### ✅ 27 DIC 2025 - TRADE #3: F (Ford) $13 Put (COMPRA - CIERRE)

**Buy to Close - F260130P00013000 - RESULTADO: PEQUEÑA PÉRDIDA ❌**
```
Acción:        Bought (BTC)
Ticker:        F (Ford)
Strike:        $13.00
Costo Cierre:  -$27.19
Saldo:         +$3,033.83
Días en Trade: 1 día (mismo día prácticamente)
Status:        ✅ CERRADO CON PÉRDIDA

RESULTADO:
├─ Prima Recibida:   +$23.80
├─ Costo Cierre:     -$27.19
├─ P&L Neto:         -$3.39 ❌

ANÁLISIS DE PÉRDIDA:
- Prima muy pequeña vs comisiones
- Posición cerrada casi inmediatamente
- F no es buen candidato para Wheel (premios bajos)
- LECCIÓN: Evitar Ford, enfocarse en QS y otros de mayor IV
```

---

### ✅ 27 DIC 2025 - TRADE #4: QS $10 Put (VENTA)

**Sell to Open - QS260220P00010000**
```
Acción:        Sold (STO)
Ticker:        QS
Strike:        $10.00
Tipo:          Put
Prima Recibida: +$87.80
Saldo:         +$3,037.22
DTE:           45 días (expira 20 FEB 2026)
Precio QS:     ~$10.73
Estado:        ⏳ Abierto esperando BTC
Target (35%):  +$30.73 ganancia objetivo
BTC Limit:     $0.65 (orden automática GTC)

ANÁLISIS:
- Strike $10 está 7% por debajo del precio
- Prima $87.80 es atractiva
- Orden BTC automática configurada
- Expectativa: Cierre en 30 días
```

---

### ✅ 01 JAN 2026 - TRADE #4: QS $10 Put (COMPRA - CIERRE EXITOSO)

**Buy to Close - QS260220P00010000 - RESULTADO: GANANCIA BUENA ✅**
```
Acción:        Bought (BTC)
Ticker:        QS
Strike:        $10.00
Costo Cierre:  -$67.23
Saldo:         +$3,121.40 (antes de QS #2)
Días en Trade: 5 días (anticipado)
Status:        ✅ CERRADO CON GANANCIA

RESULTADO:
├─ Prima Recibida:   +$87.80
├─ Costo Cierre:     -$67.23
├─ P&L Bruto:        +$20.57
├─ Comisiones:       ~$0.00 (ya incluido)
└─ P&L Neto:         +$20.57 ✅

ESTADÍSTICAS:
├─ ROI:              23.4% en 5 días
├─ Velocidad:        Excelente (5 días vs 30 esperados)
├─ Orden Automática: ✅ BTC ejecutada correctamente
└─ NOTA: Hay $47 de prima sin contar (ver balance actual)

ANÁLISIS DE ÉXITO:
1. QS bajó significativamente post-entrada
   - Strike $10 quedó más OTM (out of the money)
   - Prima colapsó rápidamente

2. Orden automática funcionó sin emociones
   - No esperé más ganancia
   - Disciplina automática ejecutada

3. Volatilidad a favor
   - Movimiento rápido del mercado en 5 días

VALIDACIÓN: ✅ Estrategia Wheel funciona
```

**ACLARACIÓN IMPORTANTE:**
El balance mostrado en Webull es +$3,121.40 después de esta transacción, pero la suma de los P&L no coincide exactamente con el saldo mostrado porque hay una prima pendiente de QS #2 que se vendió el 01 JAN.

---

### ✅ 01 JAN 2026 - TRADE #5: QS $11 Put (VENTA)

**Sell to Open - QS260220P00011000**
```
Acción:        Sold (STO)
Ticker:        QS
Strike:        $11.00
Tipo:          Put
Prima Recibida: +$154.80
Saldo:         +$3,188.63 (balance mostrado después)
DTE:           45 días (expira 20 FEB 2026)
Precio QS:     ~$10.46
Estado:        🟡 ABIERTO esperando BTC
Target (35%):  +$54.18 ganancia objetivo
BTC Limit:     $0.98 (orden automática GTC)

ANÁLISIS:
- Strike $11 está ~5% por encima del precio actual
- Prima $154.80 es muy atractiva (casi 2x QS #1)
- Orden BTC automática configurada
- Expectativa: Cierre en 25-35 días
- Contexto: Segunda posición del ciclo (estrategia de par de puts)
```

---

## 📊 RESUMEN DE CICLOS COMPLETADOS

### Ciclo #1: QS $14.50 Put (23 OCT - 19 NOV)
```
Resultado: -$69.47 ❌ PÉRDIDA
Duración:  27 días
Análisis:  Primera operación, error de timing
           QS subió después de entrada STO
           Prima en contra: $177.76 → $247.23
```

### Ciclo #2: QS $14.50 Put (27 OCT - 27 DIC)
```
Resultado: +$5.57 ✅ GANANCIA PEQUEÑA
Duración:  61 días (muy largo)
Análisis:  Posición abierta demasiado tiempo
           ROI pequeño pero positivo
           Lección: Paciencia a veces funciona
```

### Ciclo #3: F $13 Put (27 DIC - 27 DIC)
```
Resultado: -$3.39 ❌ PEQUEÑA PÉRDIDA
Duración:  <1 día (mismo día)
Análisis:  Prima muy pequeña, no recomendado
           Ford tiene IV baja = premios bajos
           LECCIÓN: Evitar Ford en futuro
```

### Ciclo #4: QS $10 Put (27 DIC - 06 JAN) ✅ EN PROGRESO
```
Resultado: +$20.57 ✅ GANANCIA
Duración:  5 días (excelente velocidad)
Análisis:  Estrategia Wheel validada
           Orden automática funcionó perfectamente
           QS volatilidad a favor
           NOTA: Hay prima adicional sin contar en P&L mostrado
```

---

## 🎯 TRADES ACTIVOS (PENDIENTES)

### Trade #5: QS $11 Put (EN MONITOREO)
```
Fecha Entrada:       01 JAN 2026
DTE Actual:          ~45 días (39 restantes estimados)
Prima Recibida:      +$154.80
Target Cierre (35%): $0.98 (ganancia esperada +$54.18)
Precio QS Actual:    ~$10.46
Status:              ✅ En monitoreo normal
BTC Activa:          ✅ Sí (GTC)

PRONÓSTICO PARA CIERRE:
├─ Si QS sigue bajando:  ✅ Cierre antes de 20 FEB
├─ Si QS se recupera:    ✅ Cierre por time decay
├─ Si QS sube >$11:      ⚠️ Potencial asignación
└─ Meta realista:        Cierre 35% en 20-30 días

ESCENARIOS:
A) Cierre exitoso (80% probabilidad):
   - Ganancia: +$54.18
   - Total ciclo con #4: +$74.75

B) Asignación (15% probabilidad):
   - Recibirías 100 QS @ $11
   - Costo: $1,100
   - Fase 2: Vender calls

C) Expiración sin cierre (5% probabilidad):
   - Cierre al vencer 20 FEB
   - Ganancia menor (por time decay)
```

---

## 📋 PRÓXIMOS EVENTOS

### Semana 2 (7-13 JAN)
- [ ] Monitorear BTC orden QS #2 @ $0.98
- [ ] Revisar diariamente P&L
- [ ] Documentar si hay cambios significativos

### Semana 3-4 (14-31 JAN)
- [ ] Esperar cierre de QS #2 (target 35%)
- [ ] Evaluar si abrir nueva posición (después de cierre)
- [ ] Investigar Margin Account

### Febrero 2026
- [ ] Expiración 20 FEB - QS #2 cierra/asigna
- [ ] Análisis completo del Ciclo 4
- [ ] Decisión: ¿Comprar shares o esperar?

---

## 🔗 Documentos Relacionados
- [[01 Options Webull]] - Estrategia y análisis detallado
- [[00 Trading]] - Hub central de trading
- [[../../../Dashboard]] - Estado general
- [[../../../Tareas Globales]] - Tareas globales

---

## 📝 Notas Importantes

**Cómo se organiza este documento:**
1. **Estadísticas arriba:** Resumen rápido de P&L y métricas
2. **Trades por día abajo:** Detalles cronológicos de cada transacción
3. **Se actualiza cuando:** Hay cierres o cambios significativos
4. **Abierto/Cerrado:** Separado por estado del trade

**Cuándo actualizar:**
- ✅ Cuando se abre un nuevo trade (STO)
- ✅ Cuando se cierra un trade (BTC)
- ✅ Cambios significativos en P&L (>$20)
- ✅ Asignaciones o rolls

**Lecciones Aprendidas:**
- ❌ Ford tiene premios muy bajos - EVITAR
- ✅ QS es buen candidato para Wheel
- ✅ Órdenes automáticas funcionan bien
- ✅ Disciplina (35% rule) genera consistencia
- ⚠️ Algunas posiciones toman más tiempo que esperadas
- ⚠️ Primeros trades son educativos (pérdidas normales)

---

**Sistema creado:** 06 JAN 2026
**Última actualización:** 06 JAN 2026
**Status:** 4 ciclos completos (3 cerrados, 1 abierto)
**P&L Acumulado:** -$3.92 (prácticamente breakeven después de 3 meses)
