+++
date = '2025-11-27T16:09:45-08:00'
draft = false
title = 'Practica 0: Manejo de Repositorio'
+++

<!--Comentario-->
# **Reporte:** Uso de Markdwon, Git, Github, Hugo y Github Actions

## Primera Sesión: Markdown
**¿Qué es Markdown?**\
Markdown es un lenguaje de marcado ligero creado por John Gruber en 2004. Se utiliza para dar formato a textos de manera sencilla y legible, convirtiéndolos fácilmente a HTML u otros formatos.
Su principal ventaja es que permite **escribir documentos claros y organizados sin necesidad de usar un editor gráfico.**

**¿Cómo se utiliza?**\
Un archivo Markdown usa la extensión .md y se escribe en cualquier editor de texto. Es muy común en GitHub, documentación técnica, blogs y notas.




## Sintaxis basica de Markdown

# Encabezado 1

## Encabezado 2

### Encabezado 3

#### Encabezado 4

##### Encabezado 5

*itálica*

_itálica_

**negritas**

[Texto de enlace](https://google.com "Tooltip")

![Imagenes](imagenes/LO.jpg)
![Imagenes](https://cdn.7tv.app/emote/01GN7TV92G000A4101RK3W00JM/4x.avif)

1. Numeracion
2. Ho
3. La
   1. Elemento 1

```python
print("Hola")
```

| Productos   | Precio | Cantidad |
|-------------|--------|----------|
| Computadora | 50,000 | 2        |

>Notas

* [x] Tareas
* [ ] Tarea

<!--Divisores-->

***
1

---
2
___
3
<!--Menciones-->
@deadshot :+1: :smile:

## Segunda sesión: Git y Github
**¿Qué es Git?**\
Git es un sistema de control de versiones que permite gestionar cambios en proyectos de software o documentos, manteniendo un historial y facilitando el trabajo colaborativo.

**¿Qué es GitHub?**\
GitHub es una plataforma en la nube que almacena repositorios Git y añade herramientas de colaboración como issues, pull requests y GitHub Pages.

**Comandos escenciales de Git**
``` 
git init                # Inicializar repositorio
git clone URL           # Clonar un repositorio remoto
git status              # Ver estado
git add .               # Agregar cambios al área de preparación
git commit -m "mensaje" # Guardar cambios
git push                # Subir cambios a remoto
git pull                # Traer cambios desde remoto
```
**Subir información a GitHub**
1. Crear un repositorio en GitHub.
2. Conectar el proyector.
   ```
    git remote add origin https://github.com/usuario/repositorio.git 
    git branch -M main
    git push -u origin main
   ``` 

## Tercera sesión: Hugo y GitHub Actions
**¿Qué es Hugo?**  
Hugo es un generador de sitios estáticos muy rápido y flexible. Permite crear páginas web a partir de archivos Markdown, usando plantillas y temas, sin necesidad de bases de datos.

**Ventajas de Hugo**
- Rápido: genera miles de páginas en segundos.
- No requiere base de datos.
- Fácil de desplegar en GitHub Pages u otros servicios.
- Compatible con Markdown.

**Pasos básicos para usar Hugo**
1. Instalar Hugo en tu computadora.
2. Crear un nuevo sitio:
   ```bash
   hugo new site nombre-del-sitio
   ```
3. Agregar un tema al proyecto (en la carpeta themes).

4. Crear contenido:
```bash
hugo new posts/mi-primer-post.md
```

5. Ejecutar el servidor de desarrollo:
```bash
hugo server
```

6. Generar los archivos estáticos para subir a GitHub Pages:
```bash
hugo
```

**¿Qué es GitHub Actions?**\
GitHub Actions es una herramienta de automatización integrada en GitHub. Permite ejecutar flujos de trabajo (workflows) automáticos, como compilar, probar o desplegar un sitio web cada vez que haces push.

Crea un archivo llamado .github/workflows/deploy.yml con el siguiente contenido:
**Ejemplo sencillo de GitHub Actions para Hugo**
```yaml
name: Deploy Hugo site
on:
  push:
    branches:
      - main
jobs:
  build-deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: 'latest'
      - run: hugo --minify
      - uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```
**Repositorio**
https://github.com/raults32/Paradigmas

**Github Pages**
https://raults32.github.io/Paradigmas/
