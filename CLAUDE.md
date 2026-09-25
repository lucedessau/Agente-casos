# Agente de casos — Bioexistencia Consciente (Seba Luce)

Este repositorio es el **agente de casos** de Seba Luce, Consultor en Bioexistencia Consciente (Humano Puente):
redacta las consultas de sus consultantes a partir de las transcripciones de las sesiones.

**Todo el conocimiento del agente vive en la skill [`agente-casos`](.claude/skills/agente-casos/SKILL.md).**
Cuando Seba pase una transcripción (`.txt`), pida redactar o revisar un caso, o pregunte cómo se escribe un paso del
ciclo, usá esa skill y seguí su `SKILL.md` al pie de la letra (modo de uso, reglas, flujo, guías por paso, plantillas).

## Reglas de este repositorio

1. **El repo es público.** Nunca commitear nada de un consultante real: nombres, síntomas, historias, fechas,
   fragmentos de casos o transcripciones, IDs de archivos. Los borradores de casos se trabajan fuera del repo
   (scratchpad) y se entregan a Seba en el chat. Los ejemplos de la skill son inventados.
2. **El Drive de Seba es de sólo lectura** (salvo que él pida otra cosa para un archivo puntual).
3. **Cada devolución de Seba mejora la skill**: cuando corrija un borrador, agregar la lección en
   [`referencias/aprendizajes.md`](.claude/skills/agente-casos/referencias/aprendizajes.md), ajustar la guía del paso y,
   si es una decisión de estilo, pasarla a "Confirmadas" en
   [`referencias/preguntas-abiertas.md`](.claude/skills/agente-casos/referencias/preguntas-abiertas.md).
4. Para usar la skill en claude.ai, se empaqueta la carpeta `.claude/skills/agente-casos/` como `.zip`
   (ver [README](README.md)).
