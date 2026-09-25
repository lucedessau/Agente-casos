# Agente-casos
Agente de casos de bioexistencia consciente (humano puente)

Agente (Claude) que redacta los casos de los consultantes de **Seba Luce** con su misma estructura y estilo, a partir de
las transcripciones de las sesiones: vos le pasás el `.txt` de la reunión y te devuelve la consulta lista para pegar.

## Dónde está todo

Todo el conocimiento está en la skill **[`.claude/skills/agente-casos/`](.claude/skills/agente-casos/)**:

| Archivo | Qué tiene |
|---|---|
| [`SKILL.md`](.claude/skills/agente-casos/SKILL.md) | Rol, modo de uso, reglas, flujo de trabajo e índice |
| [`referencias/ciclo.md`](.claude/skills/agente-casos/referencias/ciclo.md) | El ciclo de consultas y el orden de los pasos |
| [`referencias/estilo.md`](.claude/skills/agente-casos/referencias/estilo.md) | Voz, formato, fórmulas fijas, censura y glosario |
| [`referencias/transcripcion-a-caso.md`](.claude/skills/agente-casos/referencias/transcripcion-a-caso.md) | Cómo pasar de la transcripción al texto del caso |
| [`referencias/pasos/`](.claude/skills/agente-casos/referencias/pasos/) | Una guía por paso: línea de tiempo, 4 primeros pasos, útero, proyecto y sentido, árbol, REORIxINS |
| [`referencias/aprendizajes.md`](.claude/skills/agente-casos/referencias/aprendizajes.md) | Cómo se investigó, qué hay en el Drive y lecciones de las pruebas |
| [`referencias/preguntas-abiertas.md`](.claude/skills/agente-casos/referencias/preguntas-abiertas.md) | Decisiones confirmadas por Seba y pendientes |
| [`referencias/seba-luce.md`](.claude/skills/agente-casos/referencias/seba-luce.md) | Perfil de Seba |
| [`plantillas/`](.claude/skills/agente-casos/plantillas/) | Esqueletos para copiar |

[`CLAUDE.md`](CLAUDE.md) le indica a Claude Code que use la skill al trabajar en este repo.

## Cómo usarlo

- **Claude Code** (web, app o terminal) abierto en este repo: la skill se carga sola. Pasale el `.txt` y pedile el caso
  (o escribí `/agente-casos`).
- **claude.ai** (chat): generá el `.zip` de la skill y subilo en *Configuración → Capacidades → Skills*:
  ```bash
  cd .claude/skills && zip -r agente-casos.zip agente-casos
  ```

> **Privacidad:** este repositorio es público. No contiene datos de consultantes reales: todos los ejemplos son inventados.
> Los casos se leen desde el Drive de Seba (sólo lectura) y los borradores se entregan fuera del repo.
