# Aprendizajes: investigación y pruebas

Qué se estudió para construir este agente, qué hay en el Drive de Seba y qué se aprendió probándolo con casos reales.
Sin datos de consultantes: sólo patrones y reglas.

---

## 1. Cómo se hizo la investigación (septiembre 2026)

- Se leyeron (sólo lectura) **unos 30 casos completos** del Drive, de 2023 a 2026, repartidos por paso entre cinco
  análisis en paralelo: línea de tiempo, 4 primeros pasos, reprogramación de útero, proyecto y sentido, árbol + reorixins.
- Se compararon **pares transcripción → caso redactado** (línea de tiempo, PyS 1ra y 2da parte) para sacar las reglas de
  transformación.
- Se comparó un **borrador generado por ChatGPT → versión final corregida por Seba** (4PP): Seba quita placeholders,
  deja sólo el medio de limpieza que se usó y acorta el "Pensamiento de mamá" a una idea.
- Se verificaron negritas, itálicas y subrayados abriendo el XML de los `.docx`.
- Se leyeron la plantilla oficial (`estrutura ciclo consultas`), el cuestionario de Proyecto y Sentido, informes de PyS
  hechos con IA, hipótesis transgeneracionales, árboles dibujados (PDF) y formularios del Campus.
- Seba confirmó después las decisiones abiertas (ver [preguntas-abiertas.md](preguntas-abiertas.md)).

## 2. Qué hay en el Drive

Carpeta `00 casos individuales`:
- `estrutura ciclo consultas.docx`: la plantilla oficial de todos los pasos.
- `casos individuales/`: una carpeta por consultante (~90). En cada una:
  - `APELLIDO_EXPERIENCIA DE CONSULTA` (.docx o Google Doc): **el caso**, una consulta tras otra.
  - `turno Nombre Apellido.pdf`: solicitud de turno (de acá sale la **fecha de nacimiento**).
  - `Formulario Entrevista - N - Apellido - fecha.pdf`: planilla BEX EyE (económica) o formulario general de Humano
    Puente (salud); también formularios de **control intermedio** y de **cierre** del Campus.
  - Transcripciones `.txt` de Tactiq: `LT …` / `LDT …` (línea de tiempo), `PyS …` (proyecto y sentido).
  - Subcarpetas `arbol` (CorelDraw + PDF del genosociograma) y `pys` (informes de proyecto y sentido).
  - A veces: hipótesis transgeneracional (Google Doc, hecha con IA), respuestas del cuestionario de PyS, análisis de nombres.
- `YOBB/`: tutorías (otro rol de Seba; no es BEC).

Los `.docx` de los casos suelen ir **atrasados** respecto del proceso real: hay consultantes con árbol dibujado o
reorixins hechos que todavía no están escritos en el caso. Por eso el agente redacta a partir de transcripciones.

Seba usa (usaba) GPTs de ChatGPT por paso: perfil del consultante, línea de tiempo, 4 primeros pasos, útero, proyecto y
sentido, transgeneracional y árbol, reorixins, actualización de consultas. Este agente los reemplaza.

## 3. Formato de las transcripciones (Tactiq)

```
# Meeting Transcription
  Meeting started: D/M/AAAA, HH:MM a.m.      ← fecha de la sesión = fecha de la Actualización
  Duration: N minutes
  Participants: …                             ← el nombre del consultante puede venir mal escrito
  ## Highlights                               ← fragmentos automáticos: IGNORAR
  ## Transcript
  MM:SS Nombre: texto…
```
- Una sesión dura ~3 horas: la primera media hora es cuarentena (y a veces tutoría), después inducción, escenas,
  descargas, recurso y cierre.
- Errores típicos de reconocimiento: nombres propios, marcas, lugares ("canchas de pan" = canchas de pádel), apellidos.
  Corregir por contexto y marcar `[VERIFICAR]` si hay duda.
- Tactiq ya censura algunas palabras (p\*\*\*, m\*\*\*\*\*).

## 4. Lecciones de la primera prueba (línea de tiempo por patrones, 2 escenas)

1. **Tutoría al inicio.** A veces Seba dedica la primera parte a ideas de tutoría (negocio, emprendimiento, YOBB). No
   va al caso. En la Actualización sólo entra lo que el consultante toma como propio ("me lo llevo", "lo voy a probar").
2. **Anuncio del paso.** Si Seba dice que va a cerrar el ciclo ("vamos a terminar la línea de tiempo por patrones"):
   `Terminamos ciclo por patrones`.
3. **Edad corregida.** Si el consultante cambia la edad durante la escena (dice una edad y más adelante la corrige),
   vale la última; marcarla en la lista de verificación.
4. **La recapitulación de Seba** antes de "¿qué está pasando?" confirma el orden y los datos de la escena, pero si el
   consultante dijo otra cosa y Seba lo repite distinto, vale lo que dijo el consultante.
5. **Datos que no se preguntaron** (momento del día, algún detalle) se deducen sólo si es obvio ("cielo celeste" = de día)
   y se marcan para verificar.
6. **Muchos destinatarios de una misma familia** (p. ej. varios hermanos): una línea por persona con su texto y, al
   final, una línea de grupo con la acción que se hizo con todos.
7. **Órdenes o consejos al destinatario.** Seba suele frenar al consultante ("no le digas lo que tiene que hacer, decile
   lo que te da bronca"). Se omiten las órdenes, **salvo** que contengan la clave de la escena (p. ej. un pedido a uno de
   los padres que después Seba retoma y se vuelve la toma de consciencia).
8. **Emoción de la descarga distinta de la ESK.** Si el consultante nombra otra emoción explícitamente (p. ej. aclara
   que con esa persona es envidia y no odio), se respetan sus palabras.
9. **Tdc a partir de lo que Seba devuelve.** Cuando Seba une los puntos y el consultante confirma (dice "sí", llora,
   agrega), va como `Tdc:` con "(llora)". Si queda como hipótesis de Seba, va como `Obs:`.
10. **Conexiones con la vida actual** (un hijo que hoy tiene la edad de la escena, la pareja que eligió) suelen
    aparecer después de las descargas: van como Tdc u Obs.
11. **Apellidos escondidos.** El apellido puede aparecer en nombres de negocios o marcas familiares: usar iniciales o
    describirlo ("el negocio de mis papás").
12. **Comentarios después del cierre** (lo que el consultante cuenta al despedirse) no van en la consulta: se le
    avisan a Seba para la próxima Actualización.
13. **Lo que se pide para la próxima** (p. ej. "traé un recipiente con bombilla para los 4PP") no va en el caso: se
    le recuerda a Seba en las notas.
14. **Recurso.** Seba ofrece dos escenas de rescate (a veces de las ya usadas en otras consultas) y el consultante elige;
    en el caso va sólo la elegida con su fórmula.

## 5. Errores encontrados en casos reales (para no repetirlos)

- Actualizaciones con fecha fuera de orden, o pegadas en el caso de otro consultante.
- Saltos en la numeración de consultas.
- Restos de plantilla: "etc.", "Lo guió" para una mujer, placeholders, "Bing Bang".
- Encabezados `###` pegados desde ChatGPT; voz de la meditación guiada (2da persona) colada en el texto.
- Recursos sin colores; acciones de descarga en 1ra persona ("la ahorco") en vez de 3ra ("la ahorca").
- En informes hechos con IA: confundir a la consultante con la madre embarazada, cronologías de concepción mal
  calculadas, efemérides con fecha equivocada, santos dudosos presentados como oficiales, perder los datos concretos
  por sobre-abstraer.

---

*Cada vez que Seba devuelva correcciones sobre un borrador, agregar acá la lección y actualizar la guía del paso.*
