.# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

---

## 📚 Repository Overview

This is **Puma**: A centralized project management and entrepreneurial venture system in Obsidian. It documents a multi-project strategy to generate $10,000+/month across 5 major categories (Trading, Content Creation, Service, E-commerce, Commerce).

**Type:** Knowledge management system (Obsidian vault) + Documentation repository
**Language:** Spanish (with some English technical terms)
**Current Focus:** Content Creation (5 sub-projects) + Trading (3 strategies)

---

## 📁 Architecture & Structure

### Top-Level Organization
```
Puma/
├── 01_Proyectos/              ← Main projects hub
│   ├── Dashboard.md           ← Central entry point
│   ├── Notas de Progreso.md   ← Weekly/monthly progress tracking
│   ├── Ideas.md               ← Brainstorm & future ideas
│   └── Categorias/            ← 5 main project categories
│
├── 02_Notebook/
│   └── Learning.md            ← Educational progress
│
├── Tareas Globales.md         ← Global task list by priority
└── CLAUDE.md                  ← This file
```

### Project Categories (Categorias/)

#### 1. **Trading** (00 Trading.md + 3 sub-projects)
- 01 Options Webull (Wheel Strategy - selling covered calls)
- 02 Futures NinjaTrader (Quantum Liberty bot - 3 simple strategies)
- 03 Options TD RRSP ($50k+ RRSP account, requires TD verification)

**Status:** 🔵 Planning (35% done for Futures, others need setup)
**Income Target:** $1,500+/month

#### 2. **Content Creation** (00 Content Creation.md + 5 sub-projects) ← MOST DEVELOPED
- 01 TiktokShop Affiliate AI (Sell 20+ products anonymously, $200+/month)
- 02 Story 3D Animator (Narrative stories in 3D, $500+/month)
- 03 Original Character - Kids Series (Shimajiro-style, $1,000+/month)
- 04 Live Streaming Game - Interactive Multiplayer (Battle Royale for streams, $500+/month)
- 05 Haz Dinero con AI (Documentary channel - "Make Money with AI", $500+/month)

**Status:** 🔵 Planning (5-15% on each)
**Income Target:** $3,000+/month
**Key Strategy:** Synergistic - (05) documents all projects and drives traffic to others

#### 3. **Service** (00 Service.md + 2 sub-projects)
- 01 AI Agency (Recurring clients, $2,500+/month)
- 02 WebPage B2B (Web development services, $3,000+/month)

**Status:** 🔵 Planning (15-20%)
**Income Target:** $5,000+/month

#### 4. **Ecommerce** (00 Ecommerce.md + 5 sub-projects)
- 01 Lenticular (3D effect products, $50-300)
- 02 Kitchen Cardboard (Eco-friendly organizers, $30-200)
- 03 Kids Craft (Educational kits, $50-300)
- 04 Dropshipping (Trending products, $100-800)
- 05 TiktokShop Seller (Direct selling on TikTok Shop, $100-600)

Plus digital products: Game Dev, App Dev, WebApp, Roblox, AI Video Course, Japanese Game
**Status:** 🔵 Planning
**Income Target:** $1,000+/month (physical) + $300+/month (digital)

#### 5. **Commerce** (00 Commerce.md + 3 sub-projects)
- 01 Comida Mexicana (Mexican food products, $100-600/month)
- 02 Bolsas Mexicanas (Artisan bags, $75-400/month)
- 03 Impresiones 3D (3D printed toys, $150-800/month)

**Status:** 🔵 Planning
**Income Target:** $500+/month

---

## 🎯 Key Concepts & Strategy

### The "1 Dollar More" Philosophy
Core concept: Can you make $1 USD more profit than yesterday? This drives:
- **Daily tracking** of actual income/expenses
- **Honesty over hype** (documenting real failures too)
- **Multi-project synergy** where documentation of one project promotes others
- **Realistic timelines** (not "make $100k in 30 days" lies)

### Project Synergy Model
```
Original Character (03)
    ↓
    ├─→ Story 3D Animator (02) - Uses characters
    ├─→ Merchandise - Physical sales
    └─→ Live Game (04) - Cosmetics
         ↓
         Haz Dinero con AI (05) - Documents everything
         ↓
         TiktokShop Affiliate (01) ← Gets traffic from documentary
```

### Execution Phases
**Phase 1 (Weeks 1-4): MVP**
- Launch "Haz Dinero con AI" channel (documentation)
- Create 50 TiktokShop videos
- Setup tracking/dashboard

**Phase 2 (Weeks 5-12): Expansion**
- Live Game MVP
- First Story Animator episode

**Phase 3 (Month 3-4+): Full Launch**
- Original Character complete + merch
- Multiple projects generating revenue

---

## 📋 File Types & Naming Conventions

### Markdown Files (.md)
- **00 [Category].md** = Hub/overview for a category
- **01-05 [Project].md** = Individual project details
- Nested structure matches folder hierarchy
- Cross-references use `[[filename]]` Obsidian syntax
- Status indicators: 🔴 ALTA, 🟡 MEDIA, 🟢 BAJA (priority)
- Progress states: 🔵 Planificación, 🟡 En Progreso, ✅ Completado

### Standard Sections in Project Files
Every project file includes:
- **Resumen Ejecutivo** - Executive summary
- **Objetivo Principal** - Main goals (✅ checklist format)
- **Estado Actual** - Current status table
- **Monetización** - Income model with projections
- **Tareas Inmediatas** - Next steps by week/phase
- **Relacionado** - Cross-references to other projects

### Content Creation Projects - Extended Structure
- **Concepto/Estrategia** - Core idea explanation
- **Formatos de Video** - Content types
- **Herramientas** - Required tools/stack
- **Workflow** - Production pipeline
- **Métricas** - Success KPIs
- **Roadmap** - Timeline with milestones
- **Riesgos & Mitigación** - Risk analysis

---

## 🔄 Common Claude Code Tasks

### Task 1: Expand a Project with Full Documentation
When user says "Expand [Project]" or "Document [Project] completely":
1. **Read** the current `.md` file for existing content
2. **Structure** using the standard template above
3. **Add** detailed sections:
   - Strategic overview + examples
   - Multi-option approaches (usually Opción A/B/C)
   - Realistic timelines and monetary projections
   - Step-by-step workflows
   - Comprehensive risk analysis
4. **Cross-link** related projects with `[[filename]]`
5. **Update** the hub file (00 Category.md) with the new details

**Examples in repo:** `02 Story 3D Animator.md`, `03 Original Character.md`, `04 Live Streaming Game.md` are fully expanded

### Task 2: Create Hub/Overview Files
When creating category hubs (00 files):
1. **Summarize** all sub-projects in quick table format
2. **Show** income projections combined (Bajo/Medio/Alto columns)
3. **Include** comparison table (Difficulty, ROI, Timeline, Scalability)
4. **Document** project synergies with diagrams
5. **Provide** execution roadmap and priorities
6. **List** all tools/resources by project

**Example:** `00 Content Creation.md` shows how all 5 projects connect

### Task 3: Update File Names & Cross-References
When renaming files (e.g., "05 Live Streaming Character" → "05 Haz Dinero con AI"):
1. **Rename** the `.md` file with Bash `mv` command
2. **Update** ALL cross-references in `[[filename]]` format
3. **Edit** hub files with new descriptions
4. **Verify** all links still work (Obsidian will show broken links)

### Task 4: Reorganize Projects Into Categories
When user asks to reorganize:
1. **Create** folder structure: `Categorias/[Category]/00 Hub.md + 01-05 Projects.md`
2. **Move** files maintaining numbering
3. **Update** cross-links in all files
4. **Create** comprehensive hub files showing relationships
5. **Update** main Dashboard if applicable

**Pattern used:** Trading → 3 projects, Content Creation → 5 projects, etc.

### Task 5: Financial Projections & Income Models
When documenting monetization:
1. **Research** realistic rates for platform (YouTube RPM, TikTok rates, affiliate %, etc.)
2. **Show** formulas: (Views/Users × Rate × Conversion%) = Income
3. **Project** across months: Mes 1-2 (building) → Mes 3-4 (early) → Mes 5-6 (growth) → Mes 12 (scale)
4. **Break down** by revenue source (ads, sales, sponsorships, etc.)
5. **Be conservative** - show realistic scenarios, not "make $100k" hype

**Pattern:** Always show Bajo/Medio/Alto scenarios with formulas

---

## 📝 Update Patterns & Best Practices

### How Files Get Updated
1. **Project files** rarely fully rewrite - use Edit tool for sections
2. **Hub files** get major rewrites to reflect new understanding
3. **Cross-links** updated whenever filenames change
4. **Status fields** updated as projects progress
5. **Income projections** refined as real data comes in

### Document Structure Patterns
- **Lead with concept**, then execution details
- **Use tables** for comparisons (easy scanning)
- **Use bullet points** for lists (>3 items)
- **Use code blocks** for workflows, formulas, examples
- **Use emoji** for visual hierarchy (🎯, 💰, ⚠️, etc.)
- **Nest sections** max 3 levels deep

### Linking Strategy
- **Hub files** link to sub-projects: `[[01 ProjectName]]`
- **Sub-projects** link up to hub: `[[00 Category]]`
- **Cross-category** links: `[[../../Category/00 Hub]]` (relative paths)
- **Related files** always have "🔗 Relacionado" section at end

---

## 🚨 Important Constraints & Rules

### Obsidian-Specific
- File extensions must be `.md`
- Spaces in filenames supported but numbered (e.g., `05 Haz Dinero con AI.md`)
- Links use `[[filename]]` format (not URLs unless external)
- Folder structure matters for navigation
- `.obsidian/` folder contains config (don't edit directly)

### 🔧 Editing Files While Obsidian is Open
- **YES, I can edit files while Obsidian is open** using Edit tool
- If Edit tool fails with "File unexpectedly modified", use bash `cat >` command instead
- When using bash command: Read file first, then completely rewrite with `cat >` or `cat <<'EOF'`
- Obsidian will auto-refresh when file changes are detected
- **Best practice:** Use Edit tool first; only use bash if Edit tool fails
- No need to close Obsidian before making changes from Claude

### Language
- Repository uses **Spanish** for project docs
- Use Spanish headers, Spanish descriptions
- English OK for technical terms (YouTube, TikTok, Stripe, etc.)
- Mix is fine: "Setup en OBS", "Payload en Telegram bot"

### Content Rules
- **No sensitive data** in files (API keys, passwords, private financial details)
- **Realistic numbers only** - no fake "gane $100k en 30 días"
- **Link everything** - cross-reference heavily between projects
- **Document decisions** - show why one approach chosen over others
- **Include timestamps** - dates matter for tracking (Créado: X, Última actualización: Y)

### Naming Conventions
- Categories: Singular + descriptor (Trading, Content Creation, Service, Ecommerce, Commerce)
- Projects: **00 Category.md** (hub), **01-05 ProjectName.md** (sub-projects)
- Folders: **Categorias/** for categories, folders don't have numbers
- Files: Use capital letters, hyphens for multi-word (not underscores)

---

## 🔧 Common Workflows

### Adding a New Project
1. Create file: `[Category]/[Number] [ProjectName].md`
2. Use template from `01_Proyectos/README.md`
3. Link from hub file: Add to `[[00 Category.md]]`
4. Add to global task list: `Tareas Globales.md`
5. Cross-link related projects in "🔗 Relacionado" section

### Updating Progress
1. Edit `Estado Actual` table with status change
2. Update `Progreso` percentage field
3. Update sections if strategy changed
4. Mark complete tasks with ✅ in objectives
5. Add timestamp: "Última actualización: DD Mes YYYY"

### Tracking Income
- All income goes in `Trading Journal` or relevant project file
- Use `Tareas Globales.md` to aggregate across projects
- Monthly review in `Notas de Progreso.md`
- Projects show "Proyección Total" but real numbers from journal

---

## 📊 Current State Summary

**Last Updated:** 03 JAN 2026 (ACTUALIZADO)

### Active Work Areas (REAL-TIME)
- **Trading (Webull):** 95% documented, **WAIT & SEE strategy**
  - 2 QS Puts activos (strikes $10 + $11)
  - Prima total: $235.60 | Ganancia objetivo: $82.46 (35% rule)
  - Órdenes BTC automáticas: Activas (GTC) hasta 20 FEB 2026
  - **Estrategia POST-FEB 20:** Vender calls (Wheel Fase 2)
  - Capital: $2,975.63 | Buying Power: $1,088.63
  - Comprehensive doc: 01 Options Webull.md (800+ líneas con análisis completo)

- **Content Creation (TikTok):** 40% documented, **producción orgánica activa**
  - ✅ 1,000 followers alcanzados
  - Enfoque: 20-30 videos de calidad + interacción orgánica ENERO
  - Aplicación TikTok Shop: FEB 10-15 (después de 30+ videos + engagement)
  - No aplicar inmediatamente (riesgo shadowban)

- **Service, Ecommerce, Commerce:** 20-30% documented, pausados

### Priority Next Steps (ACTUALIZADO 03 JAN)
1. ✅ Trading Ciclo #1: WAIT & SEE hasta 20 FEB (órdenes BTC automáticas)
2. 🟡 TikTok: Producir 20-30 videos ENERO + interacción orgánica
3. ⏳ Setup Trading Journal (Google Sheets) - después FEB 20
4. ⏳ Aplicar a TikTok Shop (FEB 10-15) con 30+ videos + engagement
5. ⏳ POST-FEB: Decidir si comprar 100 QS shares o esperar

### Income Target
**Combined:** $10,000+/month by month 12
**Distribution:** Trading ($1,500) + Content ($3,000) + Service ($5,000) + E-commerce ($1,000) + Commerce ($500)

---

## 🎓 Key Decisions & Philosophies

### Why This Structure?
- **Categorization by revenue type** (not by effort) → Focus on income
- **Hub + sub-project format** → Overview + deep dives
- **Heavy documentation** → Transparency + learning from failures
- **Cross-linking** → See how projects help each other
- **Spanish language** → User's primary language

### Why These Projects?
- **Trading:** Real-time income, active skill-building
- **Content:** Scalable, network effect, can be passive
- **Service:** High margins, recurring revenue
- **Ecommerce:** Inventory assets, multiple sales channels
- **Commerce:** Local/hands-on, tangible products

### Why "Haz Dinero con AI" is Central
- Documents ALL projects simultaneously
- Drives traffic to other 4 projects
- Generates own revenue (YouTube ads + sponsors)
- Creates accountability through public documentation
- Teaches viewers (and user) what actually works vs. hype

---

## 🔗 External References (Not in Repo)

These tools are referenced but not stored here:
- **Trading platforms:** Webull, NinjaTrader, TD Ameritrade, Questrade
- **Content creation:** TikTok, YouTube, CapCut, Blender, Figma
- **Monetization:** Stripe, PayPal, YouTube Partner Program, Etsy
- **Communication:** Telegram, Discord
- **Analytics:** Google Analytics, Platform analytics (TikTok Studio, YouTube Studio)

---

## ✨ Quick Reminders for Future Work

1. **Always link cross-projects** - This system is strongest when interconnected
2. **Update status regularly** - Mark progress, update percentages
3. **Keep timelines realistic** - Under-promise, over-deliver on documentation
4. **Show both sides** - Document failures as thoroughly as successes
5. **Income is #1 metric** - All projects measured by monetization viability
6. **Phase execution carefully** - Don't start all 5 projects simultaneously
7. **Reuse documentation** - Show how docs from one project help another

---

**System created by user + Claude Code collaboration**
**Last revision:** 03 JAN 2026
**Status:** Active - TRADING LIVE + TIKTOK PRODUCTION IN PROGRESS

**Trading Status Snapshot (03 JAN 2026):**
- 2 contratos QS activos (strikes $10 + $11)
- Prima cobrada: $235.60 | Ganancia objetivo: $82.46 (35% rule)
- Órdenes de cierre automáticas: 2 BTC activas (GTC) hasta 20 FEB
- Estrategia: WAIT & SEE - monitorea órdenes, deja que funcionen
- POST-FEB 20: Transición a Wheel Fase 2 (sell calls en 100 QS shares)
- Capital actual: $2,975.63 | Buying Power: $1,088.63

**TikTok Status Snapshot (03 JAN 2026):**
- ✅ 1,000 followers alcanzados
- Enfoque ENERO: 20-30 videos + interacción orgánica
- Aplicación TikTok Shop: FEB 10-15 (con 30+ videos + engagement >3%)
- Expectativa: Aprobación en 5-10 días | Monetización FEB 20+

**Documentation Notes:**
- Archivos pueden ser editados incluso con Obsidian abierto (Edit tool o bash)
- Todos los documentos sincronizados vía git (commits después de cambios)
- Sistema español + terminología técnica en inglés (mix aceptado)
