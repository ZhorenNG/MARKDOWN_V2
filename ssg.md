# SSG: construir la web antes de recibir visitas

Autor: Rodrigo Neyra

## ¿Qué es un SSG?

Un SSG (*Static Site Generator*) es un generador de sitios estáticos. Combina contenido y plantillas para crear archivos listos para publicar, como HTML, CSS y JavaScript.

La diferencia principal respecto a una web dinámica está en el momento de generar las páginas: el SSG las prepara durante la construcción del proyecto, antes de que alguien las visite.

> «Estático» describe cómo se entrega el contenido prerenderizado, no que la web tenga que ser aburrida o carecer de interacción.

![Esquema del funcionamiento de un SSG](imagenes/funcionamiento-ssg.png)

## ¿Cómo funciona?

1. Escribimos el contenido, por ejemplo en archivos `.md`.
2. Preparamos las plantillas y la configuración.
3. Ejecutamos el generador.
4. La herramienta crea los archivos del sitio.
5. Publicamos esos archivos en un servidor o una CDN.

Una CDN es una red de servidores que distribuye archivos desde diferentes ubicaciones. Puede facilitar la entrega del contenido a los visitantes.

Si modificamos un artículo prerenderizado, debemos reconstruir y volver a publicar las páginas afectadas. Este proceso puede automatizarse para que se ejecute al subir cambios al repositorio.

### Ventajas y límites

- Sirve páginas ya preparadas, reduciendo el trabajo del servidor por visita.
- Permite llevar el contenido y el código en un repositorio.
- No necesita una base de datos en producción para servir las páginas generadas.
- Puede incorporar servicios externos:
  - Formularios.
  - Búsquedas.
  - Comentarios.

Como límites, hay que configurar el proceso de construcción y resolver aparte las funciones que necesitan un backend. Además, un sitio grande puede tardar más en reconstruirse. Tampoco debemos confundir una superficie de ataque menor con una seguridad garantizada: las dependencias y los servicios externos siguen necesitando atención.

## Comparación entre Jekyll, Hugo y Astro

| Aspecto | Jekyll | Hugo | Astro |
|---|---|---|---|
| Base tecnológica | Ruby. | Go. | Ecosistema JavaScript/TypeScript. |
| Plantillas | Liquid. | Go Templates. | Componentes `.astro`, con sintaxis basada en HTML. |
| Contenido | Markdown, HTML y datos del proyecto. | Markdown, datos y otros formatos compatibles. | Markdown, MDX, componentes y fuentes de datos. |
| Enfoque | Blogs y sitios basados en plantillas. | Generación estática con muchas opciones de organización. | Webs de contenido con componentes e interactividad selectiva. |
| Interactividad | Se puede añadir JavaScript o integrar servicios. | Se puede añadir JavaScript o integrar servicios. | Permite activar componentes interactivos mediante su arquitectura de islas. |
| Generación dinámica | Requiere soluciones externas al generador estático. | Requiere soluciones externas al generador estático. | También admite renderizado bajo demanda mediante adaptadores. |
| Punto a tener en cuenta | Hay que familiarizarse con Ruby, sus dependencias y Liquid. | Hay que aprender su configuración y Go Templates. | Las integraciones y componentes pueden aumentar la complejidad. |

### Jekyll

Jekyll transforma contenido escrito en Markdown y otros formatos en una web estática utilizando plantillas. Está desarrollado en Ruby y emplea Liquid para definir elementos reutilizables.

Lo veo como una opción razonable para un blog de prácticas donde las entradas sigan una estructura parecida. Permite centrarse en escribir y mantener un diseño común, aunque personalizarlo exige aprender cómo se organiza el proyecto.

### Hugo

Hugo está desarrollado en Go y destaca por su orientación a la generación rápida de sitios estáticos. Utiliza Go Templates y permite organizar contenidos, menús, taxonomías y recursos.

Lo utilizaría para una documentación técnica con bastantes páginas. Eso no significa que vaya a ser siempre el más rápido en cualquier proyecto: el resultado depende de las plantillas, los recursos y la configuración. Para trabajar con Hugo no hace falta programar habitualmente en Go, pero sí aprender su sistema de plantillas.

### Astro

Astro es un framework web que permite generar sitios estáticos, aunque no se limita a ese modo de funcionamiento. También puede renderizar rutas bajo demanda cuando se configura un adaptador compatible.

Su característica más interesante es la arquitectura de **islas**: gran parte de la página puede entregarse como HTML y solo los componentes que necesitan interacción reciben el JavaScript correspondiente. También permite integrar componentes de herramientas como React, Vue o Svelte.

Lo elegiría para un portfolio con proyectos, artículos y algún componente interactivo, sin convertir toda la página en una aplicación JavaScript.

## Ejemplo de un artículo en Jekyll

El siguiente ejemplo utiliza *front matter*: un bloque inicial de metadatos. En Jekyll podemos crear una entrada como `_posts/2026-10-27-practica-samba.md`:

```markdown
---
layout: post
title: "Mi práctica con Samba"
---

# Compartir una carpeta en red

En esta práctica configuramos un recurso compartido.

- Instalar el servicio.
- Definir los permisos.
- Probar el acceso desde otro equipo.
```

El ejemplo presupone que el proyecto dispone de una plantilla llamada `post`. No es un archivo que podamos copiar sin cambios a cualquier generador y esperar el mismo resultado.

## ¿Cuál escogería?

- Para un blog sencillo basado en plantillas, valoraría Jekyll.
- Para una documentación extensa y centrada en contenido, valoraría Hugo.
- Para combinar contenido con componentes interactivos, valoraría Astro.

No hay un ganador universal. La decisión depende de la experiencia del equipo, la forma de publicar y las funciones de la web.

~~Usar un SSG significa renunciar a un CMS.~~ Se pueden combinar: el CMS aporta el panel de edición y el SSG genera los archivos publicados.

---

## Vídeo explicativo

[Ver «Hugo in 100 Seconds», de Fireship](https://www.youtube.com/watch?v=0RKpf3rK57I).

- Duración real del vídeo completo: 2 minutos y 33 segundos.
- Idioma: inglés.
- Presenta Hugo y explica el uso de Markdown, plantillas y generación estática con un ejemplo concreto.

## Documento relacionado

[Volver a la explicación de los CMS y su comparación con los SSG](cms.md).

## Revisión del documento

- [x] Definir qué es un SSG y explicar su funcionamiento.
- [x] Comparar Jekyll, Hugo y Astro.
- [x] Añadir imagen, tabla, listas, cita y código.
- [x] Incluir un vídeo de menos de cinco minutos.
- [ ] Comprobar la vista previa y hacer la captura en GitHub.

## Fuentes consultadas

- [Documentación oficial de Jekyll](https://jekyllrb.com/docs/).
- [Documentación oficial de Hugo](https://gohugo.io/documentation/).
- [Astro: comparación y migración desde Jekyll](https://docs.astro.build/en/guides/migrate-to-astro/from-jekyll/).
- [Astro: comparación y migración desde Hugo](https://docs.astro.build/en/guides/migrate-to-astro/from-hugo/).
- [Astro: arquitectura de islas](https://docs.astro.build/en/concepts/islands/).
