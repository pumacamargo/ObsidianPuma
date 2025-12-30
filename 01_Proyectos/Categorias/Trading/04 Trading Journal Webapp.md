# 📊 Trading Journal Webapp

**Estado:** 🔵 Planificación (Fase: Design & Architecture) | **Prioridad:** 🟡 MEDIA | **Progreso:** 5%

---

## 📋 Resumen Ejecutivo

Webapp personal para trackear **todos mis trades** de múltiples brokers (Webull, NinjaTrader, TD RRSP) en un solo lugar. La feature clave es **upload screenshots + AI automático** para extraer información de trades sin typing manual.

**Diferenciador:** No necesito conectar APIs complejas de brokers - simplemente subo screenshot y AI lo parsea.

**Propósito:** Herramienta personal (no monetizar, no compartir)
**Acceso:** Desde cualquier dispositivo (webapp responsive)

---

## 🎯 Objetivo Principal

✅ Centralizar trades de Webull + NinjaTrader + TD RRSP en un solo dashboard
✅ Upload screenshots → AI extrae automáticamente: ticker, fecha, strike, P&L, etc.
✅ Dashboard con métricas clave: Win rate, P&L total, mejor/peor trade
✅ Accesible desde cualquier dispositivo (laptop, tablet, phone)
✅ Histórico completo de todos mis trades desde inicio
✅ Análisis: ¿Qué estrategias funcionan mejor? ¿Qué días/horas?

---

## ✨ FEATURE PRINCIPAL: Upload Screenshot + AI Parsing

### Cómo Funciona

**Paso 1:** Tomo screenshot de trade en Webull/NinjaTrader
**Paso 2:** Upload a webapp
**Paso 3:** AI (Claude Vision o GPT-4 Vision) extrae automáticamente:
- Ticker
- Tipo de trade (Put, Call, Long, Short)
- Strike price
- Fecha entrada
- Fecha salida (si cerrado)
- Premium recibido/pagado
- P&L
- DTE (días hasta expiración)
- Broker (Webull, NT, TD)

**Paso 4:** Confirmo/edito si AI se equivocó
**Paso 5:** Save → Aparece en dashboard automáticamente

### Por Qué Esta Feature Es Crítica

- ✅ **Cero typing manual** - Solo upload screenshot
- ✅ **Funciona con cualquier broker** - No dependo de APIs
- ✅ **Rápido** - 5 segundos vs 2 minutos typing manual
- ✅ **Histórico fácil** - Puedo subir screenshots viejos para poblar DB
- ✅ **Flexible** - Si cambio de broker, sigue funcionando

---

## 🛠️ Tech Stack Recomendado

### Frontend: Next.js 14 + React + Tailwind CSS
**Por qué:**
- ✅ Webapp funciona en cualquier dispositivo
- ✅ PWA capable (instalar como app en phone)
- ✅ Server-side rendering (rápido)
- ✅ Deployment gratis en Vercel

### Backend + Database: Firebase
**Por qué:**
- ✅ **Firestore:** Base de datos NoSQL (trades, métricas)
- ✅ **Firebase Storage:** Guardar screenshots
- ✅ **Firebase Auth:** Login seguro (solo tú)
- ✅ **Gratis tier:** Hasta 50K reads/día (suficiente para uso personal)
- ✅ **Real-time:** Sincroniza entre dispositivos automáticamente

### AI Parsing: Claude API (Anthropic)
**Por qué:**
- ✅ **Claude 3.5 Sonnet Vision:** Excelente para extraer texto de screenshots
- ✅ **Structured outputs:** Puede devolver JSON directamente
- ✅ **Costo:** ~$0.01-0.03 per screenshot (barato)
- ✅ **Ya lo conoces:** Usas Claude para todo

**Alternativa:** OpenAI GPT-4 Vision (similar pricing, similar calidad)

### Hosting: Vercel
- ✅ **Gratis tier:** Ilimitado para proyectos personales
- ✅ **CI/CD automático:** Push a GitHub → deploy automático
- ✅ **Edge functions:** Llamadas a Claude API rápidas

---

## 📐 Arquitectura de la App

### Estructura de la DB (Firestore)

**Collections:**

**1. `trades/` (documento por trade)**
```json
{
  "id": "trade_001",
  "broker": "Webull | NinjaTrader | TD",
  "ticker": "QS",
  "type": "Put | Call | Long | Short",
  "strike": 8.50,
  "entryDate": "2025-01-15",
  "exitDate": "2025-02-10",
  "premium": 45.00,
  "pnl": 22.50,
  "dte": 35,
  "screenshot_url": "gs://...",
  "notes": "Cerré en 50% profit como regla",
  "strategy": "Wheel | Trend Following | Mean Reversion",
  "createdAt": timestamp,
  "status": "Open | Closed"
}
```

**2. `metrics/` (métricas agregadas)**
```json
{
  "total_trades": 47,
  "win_rate": 68.5,
  "total_pnl": 1240.00,
  "best_trade": { ticker: "QS", pnl: 120 },
  "worst_trade": { ticker: "F", pnl: -85 },
  "avg_pnl_per_trade": 26.38,
  "by_broker": {
    "Webull": { trades: 25, pnl: 650 },
    "NinjaTrader": { trades: 15, pnl: 400 },
    "TD": { trades: 7, pnl: 190 }
  },
  "by_strategy": {
    "Wheel": { trades: 25, win_rate: 72, pnl: 650 },
    "Trend Following": { trades: 15, win_rate: 60, pnl: 300 }
  }
}
```

**3. `screenshots/` (metadata de screenshots)**
```json
{
  "url": "gs://...",
  "uploaded_at": timestamp,
  "parsed": true,
  "trade_id": "trade_001"
}
```

---

## 🎨 UI/UX - Pantallas Principales

### 1. Dashboard (Home)
**Métricas principales:**
- 📊 Total P&L (+ gráfico histórico)
- 📈 Win Rate %
- 🔢 Total Trades
- 💰 Avg P&L per Trade
- 📅 Mejores/peores meses

**Gráficos:**
- Line chart: P&L acumulado por mes
- Bar chart: Trades por broker
- Pie chart: P&L por estrategia

**Recent trades:** Últimos 5 trades con quick view

---

### 2. Upload Screenshot
**UI simple:**
- Drag & drop area o botón "Select Screenshot"
- Preview del screenshot subido
- Loading spinner mientras AI parsea
- Form pre-populated con datos extraídos
- Editar campos si AI se equivocó
- Botón "Save Trade"

---

### 3. All Trades (Lista)
**Tabla filtrable/sorteable:**
- Columnas: Date, Ticker, Type, Strike, P&L, Status, Broker
- Filtros: Por broker, por estrategia, por fecha range
- Sort: Por P&L, por fecha, por ticker
- Search: Buscar por ticker
- Actions: View details, Edit, Delete

---

### 4. Trade Details (Modal/Page)
**Vista detallada:**
- Thumbnail del screenshot original
- Todos los campos del trade
- Notes (editable)
- Timeline: Entrada → Exit
- Related trades (mismo ticker)
- Performance metrics para ese ticker

---

### 5. Analytics
**Análisis profundo:**
- Win rate por broker
- Win rate por estrategia
- Mejor día de la semana para trading
- Mejor hora del día
- Drawdown máximo
- Rachas (winning/losing streaks)
- Heatmap: P&L por día del mes

---

## 🗓️ Roadmap de Desarrollo

### Sprint 1: Setup & Auth (Semana 1)
- [ ] Crear proyecto Next.js 14
- [ ] Setup Firebase (Firestore + Storage + Auth)
- [ ] Setup Vercel deployment
- [ ] Implementar login (solo tú, email/password)
- [ ] Layout básico (navbar, sidebar)

**Tiempo:** 6-8 horas

---

### Sprint 2: Upload Screenshot + AI Parsing (Semana 2-3)
- [ ] UI para upload screenshot
- [ ] Integrar Claude API (Vision)
- [ ] Prompt engineering para extraer trades correctamente
- [ ] Save screenshot en Firebase Storage
- [ ] Form pre-populated con datos de AI
- [ ] Validación + save en Firestore

**Tiempo:** 10-15 horas
**Costo:** $5-10 para testing (50-100 screenshots)

---

### Sprint 3: Dashboard + Metrics (Semana 4)
- [ ] Fetch trades de Firestore
- [ ] Calcular métricas (win rate, total P&L, etc.)
- [ ] Gráfico de P&L acumulado (recharts o chart.js)
- [ ] Cards con métricas principales
- [ ] Responsive design (mobile + desktop)

**Tiempo:** 8-12 horas

---

### Sprint 4: All Trades List (Semana 5)
- [ ] Tabla con todos los trades
- [ ] Filters por broker, estrategia, fecha
- [ ] Sort por columnas
- [ ] Search por ticker
- [ ] Edit/Delete trades
- [ ] Pagination (si >100 trades)

**Tiempo:** 6-8 horas

---

### Sprint 5: Analytics & Polish (Semana 6-7)
- [ ] Analytics page con gráficos avanzados
- [ ] Win rate por estrategia/broker
- [ ] Heatmap calendario
- [ ] Export data (CSV/JSON)
- [ ] Dark mode (opcional)
- [ ] PWA setup (instalar en phone)

**Tiempo:** 10-12 horas

---

### Sprint 6: Testing & Launch (Semana 8)
- [ ] Subir 20-30 screenshots históricos para poblar
- [ ] Testing en mobile + desktop
- [ ] Fix bugs
- [ ] Deploy final a Vercel
- [ ] Bookmark en todos mis dispositivos

**Tiempo:** 4-6 horas

---

## 💰 Costos Estimados

| Item | Costo Mensual | Costo Anual |
|------|---------------|-------------|
| **Vercel Hosting** | $0 (free tier) | $0 |
| **Firebase** (Firestore + Storage) | $0-5 (free tier 99% suficiente) | $0-60 |
| **Claude API** | $2-10 (20-100 screenshots/mes) | $24-120 |
| **Domain** (opcional) | $1-2/mes | $12-24 |
| **TOTAL** | **$3-17/mes** | **$36-204/año** |

**Nota:** Con free tiers, probablemente $0-5/mes en práctica.

---

## 📊 Métricas de Éxito

| Métrica | Meta | Actual |
|---------|------|--------|
| **MVP funcional** | 6-8 semanas | 0% |
| **Trades históricos cargados** | 50+ | 0 |
| **AI accuracy** | 90%+ campos correctos | - |
| **Uso diario** | Abrir app 1x/día | - |
| **Tiempo agregar trade** | <30 segundos | - |
| **Uptime** | 99%+ | - |

---

## 🎯 Features Futuras (Post-MVP)

### Fase 2 (Opcional, después de 3+ meses uso)
- [ ] **Bulk upload:** Subir múltiples screenshots a la vez
- [ ] **Auto-sync brokers:** Conectar APIs de Webull/TD (si vale la pena)
- [ ] **Alertas:** "Ya tienes 5 trades perdiendo esta semana"
- [ ] **Goals tracking:** "Meta: $500/mes, vas en $320"
- [ ] **Tax reporting:** Export para impuestos
- [ ] **Backup automático:** Export semanal a Google Drive
- [ ] **Voice notes:** "Alexa, agrega nota a trade QS..."
- [ ] **AI insights:** "Claude, ¿por qué perdí en F?"

### Fase 3 (Eventual, si útil)
- [ ] **Multi-user:** Compartir con amigo trader
- [ ] **Compare performance:** Mi Webull vs mi NinjaTrader
- [ ] **Backtesting integration:** Importar backtests de NT
- [ ] **Mobile app nativa:** Flutter/React Native (si webapp no suficiente)

---

## 🔐 Seguridad & Privacidad

**Importante:** Esta app contiene información financiera sensible

### Medidas de Seguridad
- ✅ **Firebase Auth:** Login requerido siempre
- ✅ **Firestore Rules:** Solo tú puedes read/write tus trades
- ✅ **HTTPS:** Vercel usa SSL automáticamente
- ✅ **API Keys:** Nunca en frontend, usar Vercel env variables
- ✅ **Screenshots:** Private en Firebase Storage, URLs firmadas

### Firestore Security Rules
```javascript
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /trades/{tradeId} {
      allow read, write: if request.auth != null
                         && request.auth.uid == 'TU_USER_ID';
    }
    match /metrics/{metricId} {
      allow read, write: if request.auth != null
                         && request.auth.uid == 'TU_USER_ID';
    }
  }
}
```

---

## 🛠️ Prompt Engineering para AI Parsing

### Prompt Template para Claude Vision

```
Analiza este screenshot de un trade de opciones/futuros y extrae la siguiente información en formato JSON:

{
  "broker": "Webull | NinjaTrader | TD | Unknown",
  "ticker": "símbolo del activo (ej: QS, MNQ, AAPL)",
  "type": "Put | Call | Long | Short",
  "strike": número del strike price (si aplica),
  "entryDate": "YYYY-MM-DD",
  "exitDate": "YYYY-MM-DD o null si aún abierto",
  "premium": número del premium recibido/pagado,
  "pnl": número positivo o negativo del profit/loss,
  "dte": días hasta expiración al momento de entrada,
  "quantity": número de contratos/acciones,
  "status": "Open | Closed"
}

Reglas:
- Si un campo no está visible en el screenshot, usa null
- Premium y P&L deben ser números (no incluir $)
- Fechas en formato ISO (YYYY-MM-DD)
- Si no estás seguro del broker, marca "Unknown"

Screenshot:
[imagen]
```

### Validación Post-AI
- Verificar que ticker es válido (no gibberish)
- Verificar que fechas son lógicas (exit > entry)
- Verificar que P&L no es absurdamente alto ($10,000+ warning)
- Mostrar confidence score si Claude lo provee

---

## 📚 Stack de Herramientas Completo

| Categoría | Herramienta | Propósito |
|-----------|-------------|-----------|
| **Framework** | Next.js 14 | Frontend + API routes |
| **UI Library** | React 18 | Components |
| **Styling** | Tailwind CSS | Diseño rápido |
| **Database** | Firebase Firestore | NoSQL database |
| **Storage** | Firebase Storage | Screenshots |
| **Auth** | Firebase Auth | Login seguro |
| **AI** | Claude 3.5 Sonnet Vision | Parse screenshots |
| **Charts** | Recharts | Gráficos |
| **Hosting** | Vercel | Deploy |
| **Version Control** | GitHub | Código |
| **Icons** | Lucide React | Iconos |

---

## 🎨 Design System

### Colors
- **Primary:** Blue (#3B82F6) - Acciones principales
- **Success:** Green (#10B981) - Trades ganadores
- **Danger:** Red (#EF4444) - Trades perdedores
- **Neutral:** Gray (#6B7280) - Background
- **Dark:** (#1F2937) - Texto

### Typography
- **Font:** Inter (Google Fonts)
- **Headers:** Font-bold, text-2xl/3xl
- **Body:** Font-normal, text-base
- **Small:** text-sm (metadata)

---

## 🔗 Relacionado

- [[00 Trading]] - Hub central de trading
- [[01 Options Webull]] - Trades de Webull irán aquí
- [[02 Futures NinjaTrader]] - Trades de NT irán aquí
- [[03 Options TD RRSP]] - Trades de TD irán aquí
- [[../../Development/00 Development]] - Categoría Development (es también un proyecto dev)

---

## 💡 Notas Importantes

### Por Qué Webapp y No Google Sheets
- ✅ **AI parsing:** Google Sheets no puede parsear screenshots automáticamente
- ✅ **UI better:** Dashboard más visual que spreadsheet
- ✅ **Mobile friendly:** Sheets difícil de usar en phone
- ✅ **Gráficos:** Recharts > Google Charts
- ✅ **Control total:** Puedo agregar cualquier feature

### Por Qué Firebase y No Supabase
- ✅ **Firebase Storage:** Guardar screenshots fácil
- ✅ **Real-time:** Sincronización entre dispositivos
- ✅ **Free tier:** Muy generoso para uso personal
- ✅ **Ya lo conoces:** Has usado Firebase antes

### Por Qué No Conectar APIs de Brokers
- ❌ **Webull no tiene API pública** para retail
- ❌ **NinjaTrader API compleja** de configurar
- ❌ **TD API requiere aprobación** (semanas)
- ✅ **Screenshot + AI es más simple** y funciona ya

---

## 📋 Próximos Pasos Inmediatos

### Esta Semana (Si Empiezas Ya)
- [ ] **Crear repo en GitHub:** `trading-journal-webapp`
- [ ] **Setup Next.js project:** `npx create-next-app@latest`
- [ ] **Setup Firebase project:** Crear en console.firebase.google.com
- [ ] **Claude API key:** Obtener de console.anthropic.com

### Semana 1-2 (Sprint 1)
- [ ] Implementar login básico
- [ ] Layout + navegación
- [ ] Deploy inicial a Vercel

### Semana 2-3 (Sprint 2)
- [ ] Upload screenshot funcionando
- [ ] AI parsing funcionando
- [ ] Save trades en Firestore

**Tiempo total estimado:** 6-8 semanas de desarrollo part-time (10-15 hrs/semana)

---

**Creado:** 30 Diciembre 2024
**Última actualización:** 30 Diciembre 2024
**Próximo paso:** Setup inicial (GitHub + Firebase + Next.js)
