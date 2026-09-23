## Proceso para generación de Newsletter

1. Buscar noticias.
2. Extraer contenido.
3. Generar HTML.
4. Actualizar README.md.

### Buscar noticias.

- En el archivo `fuentes.md` se encuentra un listado de páginas en los que se puede buscar noticias relevantes.
- En el archivo `lineamientos-marketing.md` se encuentran las pautas para determinar la relevancia de las noticias.
- Debes seleccionar 4 noticias relevantes.

### Extraer contenido.

- Una vez identificadas las noticias relevantes, se debe extraer:
    - Título de la noticia.
    - Resumen de la noticia en español.
    - Enlace a la noticia original.
    - Imagen destacada de la noticia.

### Generar HTML.

- El archivo `News Template.html` contiene la plantilla que debe utilizarse para generar el HTML del newsletter.
- Solo modifica `<!-- Sección de noticias -->` en la plantilla. El resto debe permanecer intacto.
- Utiliza el siguiente formato para agregar la sección las nuevas noticias.
```HTML
<div class="noticia">
            <h2>
                <a href="{URL DE LA NOTICIA}" target="_blank" style="color:#24292f;text-decoration:none;">
                    {TITULO DE LA NOTICIA}
                </a>
            </h2>
            <img src="{IMAGEN DE PORTADA}" alt="Portada Seguridad Copilot" width="700">
            <p>{PARRAFO DE RESUMEN}</p>
            <p><a href="{URL DE LA NOTICIA}" target="_blank">Leer más</a></p>
        </div>
```
- Si la noticia es un video de YouTube y no tiene imagen de portada, utiliza el thumbnail de YouTube como imagen representativa. La URL del thumbnail tiene el siguiente formato:
```
https://img.youtube.com/vi/{ID DEL VIDEO}/hqdefault.jpg
```
- Crear un archivo con el nombre `News <MMM> <YYYY> <numero_semana>.html`.
- Guardar el archivo en la carpeta correspondiente dentro de la carpeta `page`. Por ejemplo:
    - `page/2026/sep/News <MMM> <YYYY> <numero_semana>.html`

- Valida que el archivo contenga las 4 noticias agregadas.

### Actualizar README.md.

- Una vez generado el archivo HTML del newsletter, se debe subir a la rama `main` correspondiente en el repositorio de GitHub.
- Actualizar el archivo `README.md` para reflejar la nueva edición del newsletter en la sección correspondiente.