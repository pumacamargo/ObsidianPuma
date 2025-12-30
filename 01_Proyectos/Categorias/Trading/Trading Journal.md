# 📔 Trading Journal - Registro de Operaciones

## Propósito
Documentar cada trade ejecutado para análisis, aprendizaje y validación de estrategias. Este journal es crítico para medir si las estrategias están funcionando como se espera.

---

## 📊 Resumen General

### Enero 2025
| Métrica | Valor |
|---------|-------|
| Total Trades | 0 |
| Trades Ganadores | 0 |
| Trades Perdedores | 0 |
| Win Rate | 0% |
| Ganancia Neta | $0 |
| Pérdida Máxima | $0 |
| Mejor Trade | $0 |

---

## 🎯 Trades por Estrategia

### Wheel Strategy (Webull - Options)

#### Trade #1
- **Fecha Apertura:** [DD/MM/YYYY]
- **Ticker:** QS o F
- **Tipo:** Put / Call
- **Strike:**
- **DTE al Abrir:**
- **Precio Entrada:**
- **Capital Utilizado:**
- **Fecha Cierre:**
- **Precio Salida:**
- **Ganancia/Pérdida:** $
- **Resultado:** ✅ Ganancia / ❌ Pérdida / 🔄 En Curso
- **Razón de Cierre:** Profit target alcanzado / Stopped out / Roll realizado / Asignado
- **Análisis:**
  - ¿Qué funcionó bien?
  - ¿Qué mejorar?
  - ¿Seguiste la estrategia? Sí/No, ¿por qué?

#### Trade #2
- **Fecha Apertura:** [DD/MM/YYYY]
- **Ticker:**
- **Tipo:**
- **Strike:**
- **DTE al Abrir:**
- **Precio Entrada:**
- **Capital Utilizado:**
- **Fecha Cierre:**
- **Precio Salida:**
- **Ganancia/Pérdida:** $
- **Resultado:** ✅ Ganancia / ❌ Pérdida / 🔄 En Curso
- **Razón de Cierre:**
- **Análisis:**
  - ¿Qué funcionó bien?
  - ¿Qué mejorar?
  - ¿Seguiste la estrategia? Sí/No, ¿por qué?

---

## 📈 Ciclos Wheel Completados

### Ciclo #1 - QS
| Fase | Ticker | Tipo | Strike | DTE | Entrada | Salida | Ganancia |
|------|--------|------|--------|-----|---------|--------|----------|
| Phase 1 | QS | Put | 8.50 | 35 | 0.45 | 0.22 | $57.50 |
| Phase 2 | QS | Call | 10.50 | 30 | 0.55 | 0.27 | $70.00 |
| **Total Ciclo** | - | - | - | - | - | - | **$127.50** |

### Ciclo #2 - F
| Fase | Ticker | Tipo | Strike | DTE | Entrada | Salida | Ganancia |
|------|--------|------|--------|-----|---------|--------|----------|
| Phase 1 | F | Put | 10.50 | 40 | 0.65 | 0.32 | $82.00 |
| Phase 2 | F | Call | 12.50 | 28 | 0.72 | 0.36 | $90.00 |
| **Total Ciclo** | - | - | - | - | - | - | **$172.00** |

---

## 🔄 Trades en Curso

### Posiciones Abiertas
| Ticker | Tipo | Strike | Fecha Apertura | DTE Entrada | DTE Actual | Precio Actual | Ganancia/Pérdida | Status |
|--------|------|--------|-----------------|-------------|-----------|---------------|------------------|--------|
| QS | Put | 8.50 | 2025-01-15 | 42 | 35 | 0.35 | -$25 (esperando) | Monitoreando |
| F | Call | 12.50 | 2025-01-10 | 45 | 28 | 0.40 | +$45 | Monitoreando |

---

## 📋 Checklist Diario de Revisión

**Cada mañana, revisar:**
- [ ] Abrir Telegram bot y revisar alertas overnight
- [ ] Verificar si hay cambios >5% en posiciones
- [ ] Revisar earnings calendar para próximas 2 semanas
- [ ] Revisar Webull - confirmar margin account status
- [ ] Actualizar tabla de posiciones abiertas
- [ ] ¿Hay trades que cierren hoy? Documentar
- [ ] ¿Necesidad de rolls? Evaluar según reglas

---

## 📊 Análisis Semanal

### Semana de [Fecha]
**Resumen:**
- Trades completados:
- Ganancia/Pérdida:
- Win rate:
- Capital deployment: %

**Lo que funcionó:**
-

**Lo que no funcionó:**
-

**Ajustes para próxima semana:**
-

---

## 💡 Notas Importantes

1. **Disciplina de Entrada:** Solo abrir cuando todas las condiciones de la estrategia se cumplan
2. **50% Profit Rule:** Siempre cerrar en 50% de ganancia, no ser codicioso
3. **Rolling Trades:** Solo hacer roll si:
   - >15% en contra de la posición AND
   - >21 DTE AND
   - Siguiente expiración tiene mejor delta/DTE
4. **Earnings Evoidance:** Nunca abrir posiciones en semana de earnings
5. **Capital Management:** Nunca desplegar >75% del capital

---

## 📈 Métricas Acumuladas

**Desde Inicio:**
- Ganancia Total Neta: $0
- Trades Totales: 0
- Win Rate Acumulado: 0%
- Mejor Mes: -
- Peor Mes: -
- Ciclos Wheel Completados: 0

---

## 🔗 Referencias
- [[00 Trading]] - Estrategia Wheel completa
- [[../../Dashboard]] - Estado general de proyectos
