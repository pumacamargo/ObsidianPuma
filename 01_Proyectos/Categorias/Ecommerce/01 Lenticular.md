# 🖼️ Lenticular - Productos Interactivos 3D

**Estado:** 🔵 Planificación (Fase: Prototipado)
**Prioridad:** 🟢 BAJA
**Progreso:** 5% → 20% (objetivo: validar prototipos)
**Última actualización:** Dic 30, 2024

---

## 📋 Resumen Ejecutivo

Venta de productos lenticulares interactivos generados con IA. Dos variantes principales:
1. **Lenticular 3D Estéreo** - Foto → Imagen 3D (cada ojo ve perspectiva diferente)
2. **Lenticular de Video** - Video → Animación por ángulo (movimiento vertical reproduce video)

Proceso totalmente automatizado: cliente sube archivo → IA procesa → imprime → ensambla carcasa → envía.

**Diferenciador:** Calidad premium + automatización + experiencia única.

---

## 🎯 Concepto & Estrategia

### Variante 1: Lenticular 3D Estéreo (Foto)
**Qué es:** Cliente envía 1 foto → Sistema genera 2 perspectivas 3D → Se ve en 3D al mirar con ambos ojos

**Cómo funciona:**
- IA analiza la foto
- Genera imagen izquierda + imagen derecha (offset 3D)
- Cada imagen se imprime en columnas alternadas
- Lente lenticular alinea: ojo izquierdo ve columnas 1,3,5... / ojo derecho ve columnas 2,4,6...
- Resultado: Efecto 3D/holográfico

**Formato final:**
- Impreso en papel de alta calidad (o glossy)
- Montado en lente lenticular transparente
- Carcasa interesante (marco, acrílico, etc.)
- Tamaño: Estándar 10x15cm (postales), 15x20cm, 20x30cm (posters)

---

### Variante 2: Lenticular de Video (Video)
**Qué es:** Cliente envía video corto → Sistema convierte a lenticular → Movimiento vertical reproduce el video

**Cómo funciona:**
- Video se divide en frames (ej: 15-30 frames)
- Cada frame se asigna a una sección vertical del lenticular
- Al mover el producto de arriba a abajo (o girar), ves diferentes frames
- Resultado: "Video" que se reproduce mediante movimiento físico

**Formato final:**
- Múltiples frames impresos verticalmente
- Lente lenticular alineado verticalmente
- Carcasa que permite fácil manipulación
- Tamaño: Típicamente cuadrado o rectangular vertical

**Requisitos técnicos:**
- Video debe ser corto (3-5 segundos)
- Resolución: Full HD mínimo
- Vertical o cuadrado preferiblemente
- Movimiento claro para que se vea bien en lenticular

---

## 🔄 Fase 1: Validación de Prototipos (Enfoque Actual)

**Objetivo:** Demostrar que ambas variantes funcionan técnicamente y generan valor percibido.

**Success Criteria:**
- ✅ Prototipo 3D estéreo producido y funcional
- ✅ Prototipo video lenticular producido y funcional
- ✅ Pruebas con usuarios: feedback positivo en efectividad visual
- ✅ Documentación del proceso automatizado
- ✅ Identificar puntos críticos de calidad

---

## 🛠️ Herramientas & Tech Stack para Prototipado

### Software - Procesamiento IA
| Herramienta | Función | Estado |
|-----------|---------|--------|
| **Stereolab / Depth AI** | Generar mapas de profundidad de fotos | A investigar |
| **DALL-E / Midjourney** | Generar perspectivas 3D alternativas | Alternativa manual |
| **Python + OpenCV** | Script para generar columnas alternadas | Desarrollo |
| **FFmpeg** | Extraer frames de video | Disponible |

### Hardware - Fabricación
| Componente | Uso | Proveedor |
|-----------|-----|----------|
| **Impresora de Inyección** | Imprimir imágenes de alta calidad | Por determinar |
| **Lentes Lenticulares** | Cristal con lineas paralelas micro | Alibaba / Proveedores locales |
| **Material para Carcasa** | PVC, acrílico, o cartón grueso | Por determinar |
| **Guillotina/Cortador** | Cortar preciso las impresiones | Por determinar |
| **Pegamento de precisión** | Alinear impresión + lente | Por determinar |

**Nota:** Fase de prototipo = uso artesanal/manual. Escalado posterior requerirá maquinaria especializada.

---

## 🔧 Workflow Prototipo Detallado

### Prototipo 1: Lenticular 3D Estéreo

**Paso 1: Adquisición de Imagen**
- Usuario sube foto (mínimo 2000x3000px)
- Formato: JPG/PNG
- Validación: Debe tener profundidad clara (foreground + background)

**Paso 2: Procesamiento IA**
- Script Python analiza profundidad de imagen
- Genera 2 versiones: perspectiva izquierda (-5°) y derecha (+5°)
- Output: 2 imágenes de la misma resolución

**Paso 3: Generar Lenticular**
- Combinar 2 imágenes en formato "columnas alternadas"
- Algoritmo: Columna 1 (izq), Columna 2 (der), Columna 3 (izq), etc.
- Ancho resultado: Mismo que original
- Alto resultado: Puede optimizarse (típicamente 40-50% del original)

**Paso 4: Impresión**
- Imprimir imagen combinada en papel gloss/photo
- Tamaño: 10x15cm (postales), 15x20cm (pequeño poster)
- Resolución: Mínimo 300 DPI
- Color: Full color

**Paso 5: Montaje Lenticular**
- Cortar lente lenticular a medida exacta
- Alinear verticalmente sobre impresión (líneas paralelas)
- Pegamento de baja viscosidad para no afectar transparencia
- Presión uniforme durante 24h secado

**Paso 6: Carcasa & Presentación**
- Marco de cartón o acrílico
- Empaque protector
- Instrucción simple: "Mira a diferentes ángulos para ver 3D"

**Paso 7: QA & Ajustes**
- Validar efecto 3D visible
- Revisar alineación lente
- Ajustar ángulos IA si necesario

---

### Prototipo 2: Lenticular de Video

**Paso 1: Adquisición de Video**
- Usuario sube video (máximo 5 segundos)
- Formato: MP4/MOV
- Validación: Full HD mínimo, orientación vertical/cuadrada
- FPS: 24-30fps

**Paso 2: Extracción de Frames**
- FFmpeg extrae frames cada X ms (depende duración)
- Ejemplo: 5 segundos = 30 frames (1 frame cada 167ms)
- Redimensionar todos a altura uniforme (ej: 3000px) × ancho variable
- Output: 30 imágenes PNG individuales

**Paso 3: Composición Vertical**
- Apilar todas las imágenes verticalmente
- Imagen final: ancho=1 frame width, alto=altura × número frames
- Resultado: imagen "tall and narrow" con todos los frames

**Paso 4: Impresión**
- Imprimir imagen vertical en papel gloss
- Tamaño: 8x30cm o 10x40cm (tall rectangle)
- Resolución: 300 DPI
- Corte preciso en bordes

**Paso 5: Montaje Lenticular**
- Lente lenticular alineado VERTICALMENTE (no horizontal)
- Líneas paralelas deben estar perpendiculares al stack de frames
- Pegamento uniforme
- Presión 24h secado

**Paso 6: Carcasa & Presentación**
- Carcasa que proteja pero permita movimiento
- Instrucción: "Mueve de arriba a abajo para ver el video"
- Empaque reforzado (riesgo de daño en tránsito)

**Paso 7: QA & Ajustes**
- Validar reproducción del video
- Revisar suavidad de transición entre frames
- Ajustar número de frames si hay saltos

---

## 📊 Métricas de Validación Prototipo

### Prototipo 3D Estéreo
| Métrica | Criterio de Éxito | Método de Validación |
|---------|------------------|----------------------|
| Efecto 3D visible | Sí/No a 30cm de distancia | Prueba visual |
| Alineación lente | ±1mm de desviación máx | Medición física |
| Claridad imagen | Sin distorsión evidente | Inspección visual |
| Durabilidad | Mantiene efecto tras 10 manipulaciones | Test repetición |
| Tiempo producción | <30 min end-to-end | Cronometrado |

### Prototipo Video Lenticular
| Métrica | Criterio de Éxito | Método de Validación |
|---------|------------------|----------------------|
| Video reproducible | Movimiento claro de frames | Prueba manual |
| Suavidad | Mínimo 15 frames para fluidez | Conteo frames |
| Alineación vertical | ±0.5mm entre lineas | Inspección |
| Tamaño óptimo | <20cm alto (manejable) | Medición |
| Durabilidad | Resiste 20 ciclos up-down | Test repetición |

---

## ⚠️ Riesgos Técnicos & Mitigación

### Riesgo 1: Calidad de imagen entrada inconsistente
**Problema:** Si usuario manda foto de mala calidad/ángulo, resultado será malo
**Impacto:** Cliente no satisfecho, devoluciones
**Mitigación:**
- [ ] Crear guía clara: "Requisitos de foto para 3D" (ej: buena iluminación, profundidad clara)
- [ ] Validación automática: rechazar fotos con baja resolución o bajo contraste
- [ ] Opción manual: preview antes de procesar

### Riesgo 2: Alineación lente-impresión imprecisa
**Problema:** Movimiento incluso de 1-2mm arruina el efecto 3D
**Impacto:** Producto no funcional
**Mitigación:**
- [ ] Invertir en herramienta de alineación (jig físico o láser)
- [ ] Usar pegamento de baja viscosidad (menos movimiento)
- [ ] Test: 5 prototipos con diferentes pegamentos

### Riesgo 3: IA genera perspectivas 3D incorrectas
**Problema:** Algoritmo de profundidad no entiende objeto
**Impacto:** Efecto 3D antinatural o nulo
**Mitigación:**
- [ ] Probar con múltiples algoritmos (Stereolab, COLMAP, etc.)
- [ ] Fallback manual: usuario puede proporcionar 2 fotos (izq/der)
- [ ] Beta testing: validar con 10-20 fotos reales

### Riesgo 4: Lentes lenticulares defectuosos
**Problema:** Proveedor entrega lentes con lineas imprecisas
**Impacto:** Efecto visual degradado
**Mitigación:**
- [ ] Pedir samples de 3 proveedores antes de producción
- [ ] QA: inspeccionar cada lote visualmente
- [ ] Especificar tolerancia: lineas deben ser ±0.05mm paralelas

### Riesgo 5: Video tiene mucho movimiento/blur
**Problema:** Frames individuales son borrosos en lenticular
**Impacto:** Video no se ve bien
**Mitigación:**
- [ ] Guía usuario: "Videos claros, sin blur, movimiento suave"
- [ ] Validación: rechazar videos con FPS bajo o blur excesivo
- [ ] Opción: ofrecer "stabilization" de video

---

## 🗓️ Roadmap Prototipado

### Sprint 1: Investigación & Preparación (1-2 semanas)
- [ ] Investigar herramientas de generación 3D (Stereolab, etc.)
- [ ] Identificar proveedores de lentes lenticulares (muestras)
- [ ] Comprar/obtener impresora de prueba
- [ ] Documentar requisitos técnicos exactos

### Sprint 2: Prototipo 3D Estéreo (2-3 semanas)
- [ ] Desarrollar script Python para procesamiento
- [ ] Hacer 5 prototipos iterativos
- [ ] Testing: ajustar ángulos, profundidad
- [ ] Feedback visual: ¿Se ve el 3D? ¿Es natural?

### Sprint 3: Prototipo Video Lenticular (2-3 semanas)
- [ ] Desarrollar pipeline extracción frames
- [ ] Hacer 5 prototipos con diferentes videos
- [ ] Testing: suavidad, reproducción
- [ ] Ajustar número de frames vs tamaño físico

### Sprint 4: Integración & Documentación (1 semana)
- [ ] Integrar ambos workflows en 1 sistema
- [ ] Documentar paso a paso (para futura automatización)
- [ ] Crear guías para usuario
- [ ] Validación final con usuarios externos

---

## 📋 Tareas Inmediatas (Próximas Acciones)

### AHORA - Esta semana
- [ ] Investigar 3 herramientas generación 3D desde fotos
- [ ] Contactar 5 proveedores de lentes lenticulares para obtener samples
- [ ] Buscar impresora de prueba (alquilar o comprar)
- [ ] Crear documento: "Especificaciones técnicas lenticular"

### SIGUIENTE - Semana 2
- [ ] Recibir samples de lentes
- [ ] Tener acceso a impresora
- [ ] Instalar herramientas IA necesarias
- [ ] Empezar desarrollo script Python

### SIGUIENTE - Semana 3-4
- [ ] Prototipo 1 (3D estéreo) - versión 1
- [ ] Test y feedback
- [ ] Iteración prototipo

### SIGUIENTE - Semana 5-6
- [ ] Prototipo 2 (video lenticular) - versión 1
- [ ] Test y feedback
- [ ] Iteración prototipo

---

## 🔗 Relacionado

- [[00 Ecommerce]] - Hub principal
- [[02 Kitchen Cardboard]] - Otro producto físico (empaque interesante)
- [[03 Kids Craft]] - Posible sinergía: productos educativos lenticulares
- [[05 Haz Dinero con AI]] - Documentar proceso de R&D en video
