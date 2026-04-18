# Libro académico con bookdown, R, GitHub Codespaces y GitHub Pages

Este repositorio contiene una plantilla base para construir, compilar y publicar un libro académico en HTML usando **bookdown**.

## Estructura general

- `index.Rmd`: portada, configuración general y objeto de datos base.
- `01-...Rmd` a `10-...Rmd`: capítulos del libro.
- `_bookdown.yml`: orden y salida del libro.
- `_output.yml`: formato HTML y opciones visuales.
- `style.css`: estilo visual.
- `references.bib`: bibliografía.
- `data/`: bases de datos.
- `images/`: imágenes.
- `docs/`: salida HTML para GitHub Pages.

## Paquetes necesarios

En R:

```r
install.packages(c(
  "bookdown", "rmarkdown", "knitr", "tidyverse", "janitor",
  "skimr", "DT", "kableExtra", "broom", "ggplot2", "readr", "here"
))
```

## Compilar el libro

```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

## Publicar en GitHub Pages

1. Sube el contenido del repositorio a GitHub.
2. Ve a **Settings > Pages**.
3. En **Build and deployment**, selecciona **Deploy from a branch**.
4. Elige la rama `main` y la carpeta `/docs`.
5. Guarda los cambios.

## Nota

La carpeta `docs/` es el destino del libro compilado y es la carpeta que GitHub Pages publicará.
