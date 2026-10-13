---
description: Pone al día la oficina (index.html) con el estado real de los agentes
---

Actualiza las fichas de la oficina de agentes en `index.html` para que reflejen cómo están de verdad los agentes.

El usuario es principiante: explícale en español y sin tecnicismos lo que vas haciendo.

## 1. Mira cómo están los agentes

Los agentes viven en carpetas hermanas de esta, dentro de `C:\Users\Usuario\Documents\carpetas-claude\` (las que empiezan por `agente-`). Solo **léelas**: no cambies nada en ellas.

De cada carpeta, mira:
- `CLAUDE.md`, `.claude/commands/`, `.claude/agents/` y `.claude/skills/`: qué hace el agente y con qué comando se usa.
- Las fechas de esos archivos: cuándo se creó.
- Si ya ha generado resultados: si está a medias o ya funciona.

Si encuentras una carpeta `agente-...` que no está en la oficina, o un agente de la oficina sin carpeta, pregunta al usuario qué hacer antes de añadirlo o quitarlo.

## 2. Actualiza las fichas

Edita solo el bloque `DATOS` del `<script>` de `index.html` (las listas `SALAS` y `AGENTES`). No toques el diseño ni el resto del código.

Cada ficha lleva solo estos campos:
- `rol`: unas pocas palabras.
- `hace`: una o dos frases sobre qué hace el agente, en general.
- `comando`: cómo se usa.
- `estado`:
  - `activo` si ya funciona y se ha probado.
  - `en-preparacion` si ya está creado pero aún no ha terminado su primer trabajo completo.
  - `por-crear` si todavía no existe.
- `version` y `creado`, por ejemplo `'v1'` y `'13 oct 2026'`; `null` si está por crear.
- `id`, `nombre`, `sala` y `aspecto`: no los cambies en los agentes que ya existen.

**La página es pública (está en GitHub).** Las fichas deben ser genéricas. Nunca pongas:
- nombres de tiendas o empresas de la competencia, reseñas ni precios;
- cestas o listas de productos;
- nombres de archivos internos ni rutas de carpetas;
- nombres de personas ni datos de clientes;
- resultados concretos de los agentes (cifras, conclusiones, número de vídeos…).

## 3. Publica y cuéntalo

1. Antes de publicar, vuelve a comprobar que las fichas no incumplen ninguna de las reglas de arriba.
2. Sin preguntar (el usuario lo ha pedido así): haz `git add` de los cambios, commit con un mensaje en español y `git push` a `origin main`.
3. Resume al usuario qué ha cambiado en cada ficha y confirma que ya está subido.
