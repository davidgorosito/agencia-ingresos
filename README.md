# agencia-ingresos

Agencia de viralización (TikTok) y conversión de ventas (WhatsApp personal) para Argentina, armada con subagentes de Claude Code.

## Estructura
```
.claude/agents/            5 subagentes
  manager-publicaciones.md   plan diario de 5 videos + códigos de seguimiento
  editor-publicaciones.md    guiones en rioplatense con CTA
  supervisor-calidad.md      aprueba/rechaza y arma el paquete final
  conversor-whatsapp.md      manual de respuestas rápidas para WhatsApp
  analista-metricas.md       3 métricas clave + informe semanal
.claude/commands/
  agencia-diaria.md          comando /agencia-diaria (orquesta todo)
negocio.md                 ficha del negocio (COMPLETAR PRIMERO)
contenido-diario/AAAA-MM-DD/  plan.md, guiones.md, informe-calidad.md, LISTO-PARA-PUBLICAR.md
whatsapp/manual-respuestas.md
metricas/registro-diario.csv  (1 fila por video)  ·  metricas/chats.csv (1 fila por chat)
PLAN-3-DIAS.md
```

## Uso
1. Completá `negocio.md`.
2. Abrí Claude Code en esta carpeta y escribí:
   ```
   /agencia-diaria
   ```
   o con fecha e indicaciones: `/agencia-diaria 2026-11-20 hoy hay promo de envío gratis`.
3. Grabá desde `contenido-diario/<fecha>/LISTO-PARA-PUBLICAR.md`.
4. A la noche cargá los resultados en `metricas/registro-diario.csv`.
5. Domingos: `Usá el subagente analista-metricas para el informe semanal`.

Los agentes y el comando viven en `.claude/` del proyecto (se versionan con git). Si los querés disponibles en todos tus proyectos, copialos a `~/.claude/agents/` y `~/.claude/commands/`.

## La pieza que hace medible todo: códigos de palabra
Cada video tiene un código (`MATE`, `REGALO`…). El CTA pide escribirlo por WhatsApp o en comentarios. Cuando llega "Hola, MATE", sabés qué video vendió. Sin esto, no se puede saber qué contenido trae plata.

## Cómo recibir el tráfico de TikTok con WhatsApp personal (sin romper reglas ni generar desconfianza)
1. **Un solo camino oficial: el link de la bio.** Poné un link `wa.me` con mensaje precargado ("Hola! Vengo de TikTok"). El link en bio requiere cuenta de empresa (gratis, pero restringe la música a la biblioteca comercial) o cierta cantidad de seguidores en cuenta personal; revisá qué te habilita TikTok hoy en *Editar perfil*. Si todavía no podés poner link, usá el CTA "comentá la palabra" y respondé cada comentario invitando a escribirte por mensaje directo de TikTok, y ahí pasás el contacto.
2. **Nunca el número en el video, la descripción ni los comentarios.** TikTok trata los datos de contacto y la redirección repetida como spam y puede bajar el alcance o restringir la cuenta. Tampoco dejes comentarios iguales copiados en masa.
3. **CTA suave y variado**: "link en mi perfil", "comentá X", "te paso info por privado". "WhatsApp" como mucho una vez por video, y no en los 5 videos del día.
4. **El link tiene que caer en una persona, no en un número anónimo**: foto, nombre real, info con horario, estados con pedidos reales. El titular del alias/CBU debe coincidir con tu nombre.
5. **Ofrecé una forma de pago protegida**: link de Mercado Pago (permite cuotas con tarjeta) y/o retiro en persona. La sola opción ya baja la desconfianza aunque después te transfieran.
6. **Respondé rápido y con un audio**: en Argentina un audio corto de una persona real vence muchísima desconfianza.
7. **Mandá vos el primer paso de verificación**: "Antes de despachar te mando foto/video de tu pedido con tu nombre".
8. **No hagas difusión a quien no te escribió**: solo listas de difusión con contactos que te tienen agendado (si no, WhatsApp no les entrega y te pueden reportar/bloquear el número).
9. **Respuestas rápidas sin WhatsApp Business**: usá la sustitución de texto del teclado (Gboard: Diccionario personal / iPhone: Sustitución de texto). Nota: WhatsApp Business es gratis y suma respuestas rápidas, etiquetas y catálogo; si en algún momento querés separar lo personal de las ventas, es la opción natural.
