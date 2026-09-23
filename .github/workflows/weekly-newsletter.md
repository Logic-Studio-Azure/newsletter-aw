---
description: |
  Genera semanalmente una nueva edición del newsletter siguiendo `proceso.md`,
  crea el HTML en `page/` y actualiza `README.md` con la nueva edición.

on:
  schedule: weekly
  workflow_dispatch:

permissions:
  contents: read
  copilot-requests: write

network:
  allowed:
    - defaults
    - github
    - https://anthropic.com
    - https://claude.com
    - https://openai.com

safe-outputs:
  create-pull-request:
    allowed-files:
      - "page/**"
      - "README.md"
---

# Generación semanal de newsletter

Tu objetivo es ejecutar el proceso definido en `proceso.md` para generar una nueva edición del newsletter.

## Instrucciones

1. Lee y sigue estrictamente `proceso.md`.
2. Usa `fuentes.md` para buscar noticias y `lineamientos-marketing.md` para validar relevancia.
3. Extrae para cada noticia:
   - Título.
   - Resumen en español.
   - Enlace original.
   - Imagen destacada (si es YouTube y no hay portada, usa `https://img.youtube.com/vi/{ID_DEL_VIDEO}/hqdefault.jpg`).
4. Usa `News Template.html` y modifica únicamente la sección `<!-- Sección de noticias -->`.
5. Crea el archivo con el formato `News <MMM> <YYYY> <numero_semana>.html`.
6. Guarda el archivo en `page/<YYYY>/<mmm>/News <MMM> <YYYY> <numero_semana>.html`.
7. Actualiza `README.md` para incluir la nueva edición en la sección correspondiente.
8. Entrega los cambios mediante `create-pull-request`.

## Criterios de no-op

Si no encuentras noticias que cumplan lineamientos o no puedes obtener contenido verificable, usa `noop` con una razón breve.
