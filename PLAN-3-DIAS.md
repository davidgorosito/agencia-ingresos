# Plan de arranque: 3 días

Objetivo de los 3 días: **no** es viralizar más. Es demostrar que tus vistas actuales pueden convertirse en chats y los chats en ventas. Meta mínima: **15 chats y 2 ventas** al final del día 3.

---

## Día 0 (hoy a la noche, 45 min) — Preparar la "recepción"
1. Completá `negocio.md` (al menos producto, precios, cobro, envíos).
2. **Perfil de TikTok**
   - Foto con tu cara (o logo + cara en los videos).
   - Nombre: `Tu Nombre | Lo que vendés` (ej: `Lucas | Termos personalizados`).
   - Bio de 3 líneas: qué vendés + a dónde enviás + cómo comprar.
     Ej: `Termos grabados a mano 🧉 / Envíos a todo el país · Retiro en Caballito / Pedí el tuyo 👇`
   - Link en la bio: ver la sección "Cómo recibir el tráfico" del README.
3. **WhatsApp personal**
   - Foto de perfil clara, nombre real, "Info": `Termos personalizados · Respondo de 9 a 21`.
   - Armá el link `https://wa.me/549XXXXXXXXXX?text=Hola!%20Vengo%20de%20TikTok` (549 + código de área sin 0 + número sin 15).
   - Subí 3 **estados**: un pedido empaquetado, una captura de cliente contento (con permiso, datos tapados), tu cara/taller.
4. En Claude Code: corré `/agencia-diaria` para mañana y pedile al subagente `conversor-whatsapp` el manual. Cargá los 10 atajos más usados en el teclado del celular.

---

## Día 1 — "Romper el hielo de la confianza"
Contenido (el plan exacto lo genera `/agencia-diaria`, esta es la mezcla sugerida):

| Hora | Tipo | Idea |
|------|------|------|
| 07:30 | Alcance | Opinión/humor del nicho: "Cosas que solo entiende alguien que [usa tu producto]" |
| 12:30 | Deseo | "Te muestro un pedido real que sale hoy" (proceso + empaque) |
| 16:00 | Confianza | Cara a cámara: "Soy [nombre], vendo [X] desde [cuándo]. Así comprás sin miedo" (Mercado Pago / retiro / video antes de despachar) |
| 19:30 | Conversión | "Hoy los primeros 10 que me escriban **[CÓDIGO]** tienen [beneficio real: envío gratis / grabado sin cargo]" |
| 22:00 | Deseo | Respuesta a un comentario de tus videos viejos con más vistas ("¿cuánto sale?" / "¿envían a…?") |

Acción extra (clave, y gratis): **respondé con video o por mensaje los comentarios de tus videos virales anteriores** que preguntaban precio o info. Ahí hay gente que ya quiso comprar.

WhatsApp:
- Teléfono a mano en 12:30–14:00 y 19:30–22:30. Respuesta en < 5 min.
- Cada chat: bienvenida → 2 preguntas → precio con 2 opciones → audio corto tuyo → cierre por alternativa.
- Anotá cada chat en `metricas/chats.csv` (código, hasta qué etapa llegó, objeción).

Noche: cargá los números de cada video en `metricas/registro-diario.csv` (vistas, visitas al perfil, chats por código).

---

## Día 2 — "Doblar lo que trajo chats"
1. Corré `/agencia-diaria` (el manager ya va a leer los datos de ayer).
2. Indicale algo como: `/agencia-diaria 2026-11-20 repetir el ángulo del video con más chats con otro gancho`.
3. Si un video tuvo muchas vistas y 0 chats: el problema es el CTA o el "motivo para escribir". Hoy probá "comentá la palabra" en vez de "link en el perfil".
4. Chats que quedaron en "lo pienso": seguimiento a las 24 h con el atajo de seguimiento (algo útil, no "¿y? ¿lo pensaste?").
5. Pedile a cada comprador del día 1 una captura/foto con el producto → material de confianza para el día 3.

---

## Día 3 — "Prueba social + primer diagnóstico"
1. Video de confianza con la reseña/foto de un comprador de ayer ("Le llegó a [nombre] de [ciudad]").
2. Video respondiendo la objeción que más apareció en `metricas/chats.csv`.
3. Noche: pedile a `analista-metricas` un diagnóstico de los 3 días:
   ```
   Usá el subagente analista-metricas: diagnóstico de los primeros 3 días, decime dónde se pierde la venta y qué cambio hacer mañana.
   ```
4. Pedile a `conversor-whatsapp` que mejore las respuestas de la etapa donde más chats se cortaron (pegale 1-2 conversaciones reales, sin datos personales).

### Cómo leer el resultado del día 3
| Situación | Dónde está el problema | Qué hacer |
|-----------|------------------------|-----------|
| < 5 chats en 3 días | TikTok → WhatsApp | CTA más claro, más videos de "conversión", revisar que el link funcione |
| Chats pero 0 ventas | WhatsApp | Velocidad, confianza (audio + Mercado Pago), precio con 2 opciones |
| Ventas con ticket bajo | Oferta | Combos, opción "recomendada" |
