---
description: Ejecuta el flujo diario de la agencia (plan → guiones → control de calidad → paquete listo para publicar)
argument-hint: "[fecha AAAA-MM-DD opcional] [indicaciones extra opcionales]"
---

Ejecutá el flujo diario de la agencia de viralización y conversión.

Fecha de trabajo: usá la primera palabra de `$ARGUMENTS` si tiene formato AAAA-MM-DD; si no, la fecha de hoy (`date +%F`). El resto de `$ARGUMENTS` son indicaciones extra del dueño para hoy (pasáselas al manager y al editor).

Seguí estos pasos EN ORDEN, delegando con la herramienta Agent a cada subagente. Los subagentes no pueden llamarse entre sí: vos orquestás.

1. **Preparación**: creá `contenido-diario/<fecha>/`. Si `negocio.md` todavía tiene muchos `[...]`, avisame en una línea pero seguí.
2. **Plan** → subagente `manager-publicaciones`: "Armá el plan de 5 publicaciones para <fecha>. Indicaciones extra: <...>". Verificá que exista `contenido-diario/<fecha>/plan.md` con 5 videos y 5 códigos distintos.
3. **Guiones** → subagente `editor-publicaciones`: "Escribí los 5 guiones de <fecha> según el plan".
4. **Calidad** → subagente `supervisor-calidad`: "Revisá los guiones de <fecha>, ronda 1".
5. **Correcciones**: si hay rechazados, volvé a llamar a `editor-publicaciones` ("corregí los rechazados según informe-calidad.md") y luego a `supervisor-calidad` (ronda siguiente). Máximo 2 rondas de corrección. Si después de eso algún guion sigue rechazado, reemplazalo vos por el mejor guion aprobado del día adaptado con otro código, y anotalo en el informe.
6. **WhatsApp en paralelo**: si `whatsapp/manual-respuestas.md` no existe o los códigos de hoy no tienen bienvenida, llamá a `conversor-whatsapp` para crear/actualizar el manual (podés lanzarlo en paralelo con el paso 3).
7. **Métricas**: si `metricas/registro-diario.csv` tiene resultados cargados de ayer, llamá a `analista-metricas` para el chequeo diario. Si hoy es domingo, pedile además el informe semanal.

Al final mostrame un resumen corto:
- Tabla de los 5 videos: hora, tipo, código, primera frase del gancho.
- Ruta de `LISTO-PARA-PUBLICAR.md`.
- Los atajos de WhatsApp nuevos de hoy (si hubo).
- Recordatorio: "Esta noche cargá vistas, visitas al perfil, chats y ventas por código en `metricas/registro-diario.csv`".
