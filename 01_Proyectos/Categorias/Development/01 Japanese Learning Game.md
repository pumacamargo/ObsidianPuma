# 🎮 Japanese Learning Game - Robot Rescue

**Nombre de trabajo:** Robot Rescue
**Estado:** 🔵 Planificación (Fase: Pre-Development)
**Prioridad:** 🟢 BAJA
**Progreso:** 5% → 30% (objetivo: MVP Act 1 en Itch.io)
**Última actualización:** Dic 30, 2024

---

## 📋 Resumen Ejecutivo

### Visión
Crear un juego educativo narrativo que enseñe japonés (A0-A1) a través de la historia de un niño que descubre un robot roto que solo habla japonés. El robot enseña mediante mini-games de typing integrados mientras revela gradualmente su misterioso pasado.

### Promesa Central
Los jugadores aprenden **700-900 palabras, 150-200 kanjis, hiragana/katakana completo** en 15-25 horas de gameplay, permitiéndoles entender anime básico sin subtítulos.

### Por Qué Funciona Este Proyecto
- **Diferenciador único:** Mecánica de typing + narrativa (no existe en el mercado)
- **Justificación narrativa:** Aprender japonés es necesario para el progreso, no arbitrario
- **Motivación intrínseca:** Relación emocional robot-niño crea engagement
- **Mercado validado:** 500M+ fans de anime, 50M+ aprendiendo japonés
- **Monetización clara:** Itch.io + Steam (indie game market probado)

---

## 🎯 Concepto Narrativo

### La Historia

Un niño descubre un robot destruido en un vertedero. La pantalla y teclado del robot funcionan, nada más. Al activarlo, el robot habla solo japonés y está desesperado por obtener ayuda del niño para repararse.

Para ayudar al robot, el niño debe aprender japonés. El robot acepta enseñarle a través de un juego especial en su pantalla. A medida que el niño aprende, comprende gradualmente el pasado trágico del robot y debe decidir si salvarlo.

### Por Qué Funciona Narrativamente
- **Justificación lógica:** Aprender no es arbitrario—es necesario para avanzar
- **Progresión emocional:** El niño y robot desarrollan relación
- **Meta-juego:** Aprendizaje ocurre dentro del juego del robot (game within a game)
- **Comprensión progresiva:** Historia temprana confunde al jugador; historia tardía se aclara con vocabulario creciente
- **Múltiples finales:** El resultado cambia según cuánto aprendió el jugador

### Ganchos Narrativos
1. "¿Cuál es el pasado trágico del robot?"
2. "¿Por qué fue abandonado en un vertedero?"
3. "¿Qué está intentando construir/reparar?"
4. "¿Quién es el personaje misterioso?"
5. "¿Qué pasa si lo ayudo/abandono?"
6. "¿Es el robot sentiente o IA?"

---

## 🎮 Diseño de Juego

### Mecánica Principal: Falling Words Mini-Game

#### Visuals & Mechanics

**Pantalla de juego:**
- Palabras en japonés caen verticalmente desde la parte superior
- Jugador ve palabra en hiragana/kanji con furigana
- Caja de entrada en la parte inferior muestra caracteres en tiempo real
- Contador de puntuación, timer, medidor de precisión

**Entrada del jugador:**
- Escribe la palabra en hiragana/romaji
- Enter para confirmar
- Correcto: Puntos + feedback visual satisfactorio
- Incorrecto: Palabra se reinicia, pierde puntos

**Progresión de dificultad:**
- Niveles 1-3: Palabras cortas (2-3 caracteres), velocidad lenta
- Niveles 4-7: Palabras medias (4-6 caracteres), velocidad moderada
- Niveles 8-12: Palabras largas (7+ caracteres), velocidad rápida
- Niveles 13+: Múltiples palabras simultáneas, velocidad extrema

**Sistema de bonificación:**
- Puntos por velocidad
- Combo system (respuestas consecutivas correctas)
- Multiplicadores de puntuación
- Points → Money in-game (para reparar robot)

#### Variaciones del Mini-Game

| Modo | Descripción | Dificultad |
|------|-----------|-----------|
| **Classic** | Escribe palabra exacta | Media |
| **Multiple Choice** | Selecciona de 3 opciones, luego escribe | Fácil |
| **Sentence** | Palabra faltante en oración | Media-Alta |
| **Kanji** | Ve kanji, escribe lectura | Alta |
| **Translation** | Pista en inglés, escribe japonés | Media |

### Loop Principal de Juego

```
Escena Visual Novel (2-5 min)
    ↓ Aprende 5-10 palabras nuevas
    ↓
Mini-Game Falling Words (3-10 min)
    ↓ Gana dinero, desbloquea progresión
    ↓
Exploración/Misiones (5-15 min)
    ↓ Habla con NPCs, usa vocabulario aprendido
    ↓
Siguiente escena (si dinero suficiente)
```

---

## 📖 Estructura Narrativa (3 Actos)

### Act 1: Introducción - 200 palabras

**Tema:** Robot despierta, comunicación rota
**Duración:** 3-5 horas de gameplay
**Vocabulario Inicial:**
- Saludos e introducciones
- Números (esencial para dinero/tiempo)
- Verbos básicos (ir, hacer, comprar, fabricar, ayudar)
- Pronombres personales (yo, tú, él, ella)
- Palabras interrogativas (qué, dónde, quién, por qué)
- Sí/no y respuestas simples

**Secuencias de Historia:**
1. Descubrimiento y activación
2. Primer intento de comunicación (caos)
3. Robot propone teaching game
4. Tutorial mini-game
5. Primera misión verdadera (ganar dinero)
6. Primera interacción con NPC

**Reward:** Desbloquea Act 2

---

### Act 2: Desarrollo - 300-400 palabras

**Tema:** El niño ayuda al robot, aprende su historia
**Duración:** 7-15 horas de gameplay
**Vocabulario Expandido:**
- Lugares (tienda, casa, templo, calle, parque, escuela)
- Objetos cotidianos (dinero, comida, ropa, herramientas, piezas)
- Adjetivos básicos (grande, pequeño, nuevo, viejo, caliente, frío, bueno, malo)
- Sentimientos/emociones (feliz, triste, asustado, enojado, emocionado)
- Acciones diarias (comer, dormir, trabajar, hablar, aprender, comprar)
- Palabras relacionadas con tiempo (hoy, mañana, ayer, mañana, tarde)
- Familia (madre, padre, hermana, hermano)
- Colores y descripciones simples

**Secuencias de Historia:**
- Escenas 1-3: Múltiples NPCs, diálogos se aclaran
- Escenas 4-6: Mini-quests en el pueblo
- Escenas 7-9: Robot revela memorias fragmentadas
- Escenas 10-12: El niño se vincula con robot, aprendizaje acelera
- Escenas 13-14: Personaje misterioso aparece (insinúa giro)
- Escenas 15-16: Revelación sobre propósito del robot

**Reward:** Acceso a Act 3 (final)

---

### Act 3: Clímax - 200-300 palabras

**Tema:** Revelación y elección final
**Duración:** 5-10 horas de gameplay
**Vocabulario Avanzado:**
- Expresiones emocionales complejas
- Descripciones narrativas
- Tiempo pasado simple (historia del robot)
- Solicitudes y comandos corteses
- Frases de despedida emocionales
- Formas de pregunta avanzadas
- Declaraciones condicionales (si/cuando)

**Secuencias de Historia:**
- Escenas 1-3: La investigación se profundiza
- Escenas 4-5: La verdad final se revela
- Escenas 6-7: Confrontación emocional
- Escenas 8-9: Elección final (salvar, abandonar, alternativa)
- Escena 10: Final (varía según elección del jugador)
- Post-créditos: Teaser para posible secuela

**Múltiples finales según:**
- Cantidad de palabras aprendidas
- Dinero gastado en reparaciones
- Elecciones dialógicas durante juego
- Palabras opcionales descubiertas

---

## 🛠️ Especificaciones Técnicas

### Stack Tecnológico

#### Frontend - Game Engine
| Herramienta | Función | Razón |
|-----------|---------|-------|
| **Phaser 3** | Motor de juego web | Perfecto para 2D, comunidad grande, gratis |
| **JavaScript ES6+** | Lenguaje | Nativo en web, ampliamente soportado |
| **HTML5 Canvas** | Renderizado | Soporte universal |
| **CSS3** | Estilos UI | Responsive, animaciones |

#### Build & Distribution
| Herramienta | Función | Costo |
|-----------|---------|-------|
| **Webpack/Vite** | Bundler | Gratis (open-source) |
| **Electron** | Desktop app | Gratis (open-source) |
| **Itch.io** | Distribución web + desktop | Gratis (10% optional) |
| **Steam** | Distribución desktop | $100 one-time + 30% revenue share |

#### Infrastructure
| Componente | Solución | Costo |
|-----------|----------|-------|
| **Save System** | LocalStorage / IndexedDB | Gratis |
| **Version Control** | Git + GitHub | Gratis |
| **Hosting Web** | Itch.io | Gratis |

### Requisitos Técnicos

**Browser Support:**
- Chrome 90+, Firefox 88+, Safari 14+, Edge 90+

**System Requirements:**
- Minimum: 500MB space (web), 1GB (desktop)
- RAM: 512MB
- Keyboard: Físico (esencial para typing mechanic)

**Japanese Character Support:**
- Full Unicode para hiragana, katakana, kanji
- Web-safe fonts (Noto Sans JP)
- Proper rendering automático

### Assets Requeridos

**Visuales:**
- Robot sprite (múltiples estados: roto, feliz, triste, etc.)
- Niño sprite (múltiples emociones)
- 5-10 sprites NPC (pueblerinos, personaje misterioso)
- UI elements (cajas, botones, barras, iconos)
- Background artwork (vertedero, pueblo, interiores)
- Particle effects y animaciones

**Audio:**
- Background music (3-4 piezas distintas, looping)
- Sound effects (UI, typing, game over)
- Ambient sounds (viento, pueblerino)
- Voice acting (opcional, future enhancement)

**Data:**
- dialogue.json (diálogos en japonés + English translations)
- vocabulary.json (700-900 palabras con lecturas, significados, ejemplos)
- kanjis.json (150-200 kanji con trazos, lecturas)
- progression.json (estructura de niveles, orden de escenas, unlocks)

---

## 📊 Fase 1: Prototipado (Enfoque Actual)

**Objetivo:** Demostrar que la mecánica core y narrativa funcionan juntas. Crear MVP jugable (Act 1) que pueda distribuirse en Itch.io.

**Success Criteria:**
- ✅ Mecánica falling words perfectamente funcional
- ✅ Sistema de progresión narrativa trabajando
- ✅ Act 1 completo (200 palabras, 6 escenas)
- ✅ Save/load system functando
- ✅ Mínimo 1,000+ downloads en Itch.io
- ✅ Feedback positivo de jugadores (4.5+ stars)

---

## 🗓️ Roadmap de Desarrollo

### Sprint 1: Setup & Core Prototype (Semana 1-2)
- [ ] Inicializar proyecto Phaser 3
- [ ] Crear mecánica básica falling words
- [ ] Sistema de escenas visual novel
- [ ] Input handler para typing
- [ ] Save/load system skeleton
- **Deliverable:** Demo jugable de 1 escena

### Sprint 2: Act 1 Completo (Semana 3-6)
- [ ] Implementar todas 6 escenas Act 1
- [ ] Mini-game con todas las variaciones
- [ ] UI pulida (menus, progression screen)
- [ ] Sistema de progresión (dinero, desbloques)
- [ ] Integración de audio
- **Deliverable:** Act 1 completo (3-5 horas gameplay)

### Sprint 3: Polish & Testing (Semana 7-8)
- [ ] Optimización de performance
- [ ] Cross-browser testing
- [ ] Bug fixes
- [ ] User playtesting
- [ ] Ajustes de balance de dificultad
- **Deliverable:** Production-ready Act 1

### Sprint 4: Itch.io Launch (Semana 9)
- [ ] Build web (HTML5)
- [ ] Build desktop (Electron)
- [ ] Test en Itch.io sandbox
- [ ] Crear página Itch.io
- [ ] Escribir descripción + screenshots
- **Deliverable:** Live en Itch.io

### Sprint 5-7: Acts 2-3 (Semana 10-20)
- [ ] Todas las escenas Acts 2-3
- [ ] Feature additions based on feedback
- [ ] Balance ajustes
- [ ] Ending variations
- **Deliverable:** Full game completo

### Sprint 8: Steam Prep (Semana 21-22)
- [ ] Steam-compatible builds
- [ ] Trailer de gameplay
- [ ] Steam store page
- [ ] Marketing assets
- **Deliverable:** Ready for Steam submission

---

## 💰 Monetización

### Fase 1: Itch.io - Free Act 1 (Semana 9-20)

**Estrategia:** Validar concepto, construir comunidad
- **Precio:** $0 (gratis)
- **Objetivo:** 1,000+ downloads, 4.5+ stars rating
- **Métricas:** Downloads, engagement, community feedback
- **Revenue:** $0 (inversión en validación)

### Fase 2: Itch.io - Acts 2-3 Monetizados (Semana 10-20)

**Estrategia:** Freemium model (Act 1 free, Acts 2-3 paid)

**Opción A: One-time Purchase** ✅ Recomendado
- Precio: $9.99 USD
- Incluye: Acts 2-3 + todos los futuros updates
- Expected conversion: 30-40% de Act 1 players

**Opción B: Pay-What-You-Want**
- Mínimo: $1.99
- Sugerido: $9.99
- Mayor accesibilidad, variable pricing

**Opción C: Suscripción** (alternativa)
- Precio: $2.99/mes
- Incluye: Acts 2-3 + new content monthly
- Recurrent revenue

### Fase 3: Steam Launch (Semana 22+)

**Estrategia:** Monetizar larger audience
- **Precio:** $12.99 USD (one-time purchase)
- **Expected:** 500-1,000 sales year 1
- **Revenue Share:** 30% para Steam, 70% para developer
- **First month expectation:** $3K-$5K revenue

### Revenue Projections

**Conservative (Year 1):**
- Itch.io Act 1: 1,000-2,000 downloads
- Itch.io Acts 2-3 conversión (30%): 300-600 → $3K-$6K
- Steam sales: 300-500 copies → $3K-$5K
- **Total:** $6K-$11K

**Optimistic (Year 1):**
- Itch.io: 5,000-10,000 downloads
- Conversión (40%): 2,000-4,000 → $20K-$40K
- Steam: 1,000-2,000 copies → $10K-$20K
- **Total:** $30K-$60K

### No Predatory Monetization
- ❌ No ads
- ❌ No battle pass / FOMO
- ❌ No loot boxes / gambling
- ❌ No premium currency
- ❌ No energy system

**Razón:** Juego educativo para teens/adultos; responsabilidad ética.

---

## 📊 Métricas de Éxito

### Act 1 Launch Success
- ✅ 1,000+ downloads en primer mes
- ✅ 4.5+ star average (20+ reviews)
- ✅ 500+ Discord members activos
- ✅ Cero game-breaking bugs
- ✅ Feedback positivo en aprendizaje

### Acts 2-3 Completion Success
- ✅ 30%+ conversion rate (Act 1 → Paid)
- ✅ 500-1,000 paying customers Itch.io
- ✅ 2,000+ Discord members
- ✅ Testimoniales de mejora en comprensión anime

### Steam Launch Success
- ✅ 500+ Steam wishlists
- ✅ 500+ sales first month
- ✅ 4.0+ rating Steam
- ✅ $5,000+ revenue first month

### Year 1 Success
- ✅ 10,000+ total players across platforms
- ✅ 1,000+ paying customers
- ✅ $10,000+ revenue
- ✅ Featured en indie game media
- ✅ Established community + partnerships

---

## ⚠️ Riesgos & Mitigación

### Riesgo 1: Mecánica typing es demasiado difícil
**Problema:** Jugadores se frustran, abandonan
**Mitigación:**
- [ ] Tutoriales claros con dificultad escalada
- [ ] Difficulty settings (fácil, normal, difícil)
- [ ] Pause anytime sin penalidad
- [ ] Opción de practice mode (sin presión)

### Riesgo 2: Narrativa no es lo suficientemente emocional
**Problema:** Relación robot-niño no enganche
**Mitigación:**
- [ ] Writing profesional o collaborator
- [ ] User testing early con target audience
- [ ] Iteración basada en feedback
- [ ] Voice acting considera si presupuesto permite

### Riesgo 3: Mercado saturado de language learning apps
**Problema:** Competencia con Duolingo, Anki, etc.
**Mitigación:**
- [ ] Diferenciador claro: narrativa + typing (no existe)
- [ ] Community engagement (Discord, Reddit)
- [ ] Word-of-mouth marketing (anime community)
- [ ] Cross-promotion con influencers

### Riesgo 4: Development delays
**Problema:** Timeline slip (6 meses → 1 año)
**Mitigación:**
- [ ] Scope management (fijar Act 1, después expandir)
- [ ] Regular check-ins sobre progreso
- [ ] Escalado de trabajo si es needed
- [ ] Contingency: launch Act 1 temprano (6 semanas vs 9)

### Riesgo 5: Low initial traction
**Problema:** <500 downloads first month
**Mitigación:**
- [ ] Marketing early (Reddit, Discord communities)
- [ ] YouTube channels partnerships
- [ ] Anime community outreach
- [ ] Influencer reviews (no pago, solo copies)
- [ ] Consistent social media presence

---

## 📋 Tareas Inmediatas

### AHORA - Esta semana
- [ ] Crear Git repository para proyecto
- [ ] Setup Phaser 3 boilerplate
- [ ] Crear documento: "Falling Words Mechanics Spec"
- [ ] Draft completo Act 1 dialogue (Japanese + English)
- [ ] Crear asset list detallada
- [ ] Investigar herramientas para crear sprites

### SIGUIENTE - Semana 2
- [ ] Prototipo jugable: 1 falling words game
- [ ] Basic visual novel scene implementada
- [ ] Input handler funcionando
- [ ] Primeras pruebas jugabilidad
- [ ] Crear guía de estilo visual (art direction)

### SIGUIENTE - Semana 3-4
- [ ] Mecanismo de puntuación + dinero
- [ ] Sistema de progresión narrativa
- [ ] Act 1 escena 1-2 completas
- [ ] Asset creation (sprites, backgrounds)
- [ ] Testing de dificultad balance

### SIGUIENTE - Semana 5-6
- [ ] Act 1 escenas 3-6 completas
- [ ] Save/load system funcional
- [ ] UI menus (main menu, settings, pause)
- [ ] Audio integration
- [ ] Playtesting interno

### SIGUIENTE - Semana 7-8
- [ ] Bug fixes y polish
- [ ] Performance optimization
- [ ] Builds para web + desktop
- [ ] Setup Itch.io account
- [ ] Marketing materials

### SIGUIENTE - Semana 9
- [ ] Itch.io page creation
- [ ] Live on Itch.io
- [ ] Announce en Reddit, Discord
- [ ] Community building begins

---

## 🎓 Referencias & Inspiración

### Juegos de Aprendizaje
- Duolingo (gamificación, microtasks)
- Anki (spaced repetition)
- Wanikani (kanji progression)
- Katakana Hero (typing mechanic)

### Juegos Narrativos
- Disco Elysium (dialogue-heavy)
- What Remains of Edith Finch (emotional narrative)
- Gris (visual storytelling)
- A Short Hike (wholesome, exploration)

### Educational Game Design
- "Learning Sciences" (spaced repetition, active production)
- "Intrinsic Motivation" research
- "Flow Theory" (challenge vs skill balance)

---

## 🔗 Relacionado

- [[00 Development]] - Hub Development
- [[../../00 Ecommerce]] - Otros digital products
- [[../../01_Proyectos/Content\ Creation/05\ Haz\ Dinero\ con\ AI]] - Documentar game dev en video
- [[../../01_Proyectos/Content\ Creation/02\ Story\ 3D\ Animator]] - Posible colaboración: personajes 3D
