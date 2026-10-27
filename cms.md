# CMS: gestionar una web sin empezar desde cero

Autor: Rodrigo Neyra

## ¿Qué es un CMS?

Un CMS (*Content Management System*) es un sistema de gestión de contenidos. Permite crear, organizar, editar y publicar información en una web desde un panel de administración, sin tener que programar cada página a mano.

Por ejemplo, para publicar una noticia en WordPress podemos escribir el título, añadir el texto, subir una imagen y pulsar «Publicar». La plantilla se encarga de presentar ese contenido con el diseño de la web. Esto no significa que nunca haga falta programar: las funciones más específicas pueden necesitar desarrollo.

> La idea principal es separar el contenido del trabajo técnico necesario para mostrarlo.

## ¿Cómo funciona un CMS dinámico?

![Esquema del funcionamiento de un CMS dinámico](imagenes/funcionamiento-cms.png)

En una instalación tradicional que utiliza una base de datos, el proceso se puede resumir así:

1. El editor entra en el panel con su usuario y contraseña.
2. Redacta el contenido y añade los recursos necesarios.
3. El CMS guarda los datos y las referencias a los archivos.
4. Cuando llega una visita, el servidor combina el contenido con una plantilla.
5. El navegador recibe la página y muestra el resultado.

La **caché** permite reutilizar páginas o respuestas ya preparadas. Por eso, no sería exacto decir que un CMS dinámico consulta siempre la base de datos y construye todo desde cero en cada visita.

### Elementos habituales

- Panel de administración.
- Gestión de entradas, páginas e imágenes.
- Temas o plantillas para el diseño.
- Extensiones para añadir funciones.
- Usuarios con distintos permisos:
  - Administrador: configura y mantiene la web.
  - Editor: revisa y publica contenidos.
  - Autor: redacta sus publicaciones.

Los nombres y permisos concretos dependen del CMS.

## Tipos de CMS y ejemplos

### Según su arquitectura

| Tipo | Cómo organiza el contenido y su presentación | Ejemplos |
|---|---|---|
| Tradicional o acoplado | El mismo sistema gestiona el contenido y genera la web. | WordPress, Joomla y Drupal en su uso tradicional. |
| Headless | Gestiona el contenido y lo entrega mediante una API; otra aplicación se encarga de mostrarlo. | Strapi, Contentful y Sanity. |

Una API es una interfaz que permite que distintas aplicaciones intercambien información. Por ejemplo, una web y una aplicación móvil pueden obtener las mismas noticias de un CMS headless.

Estas categorías no son cerradas: WordPress también puede utilizarse como backend headless mediante su API.

### Según su finalidad

También podemos distinguir herramientas orientadas a blogs, webs corporativas o comercio electrónico. Es otra forma de clasificarlas, no una arquitectura diferente. Por ejemplo, WordPress se utiliza para publicar contenidos y PrestaShop está orientado a tiendas online.

## Comparación: CMS dinámico y generador de sitios estáticos

| Aspecto | CMS dinámico tradicional | SSG |
|---|---|---|
| Generación de páginas | Habitualmente en el servidor cuando se solicitan, con posibilidad de caché. | Durante la construcción, antes de recibir visitas. |
| Contenido | Suele gestionarse en una base de datos desde un panel. | Puede proceder de Markdown, archivos de datos o un CMS. |
| Publicación de cambios | Normalmente se publica desde el panel. | Los cambios prerenderizados requieren una nueva construcción y despliegue. |
| Alojamiento | Necesita un entorno compatible con la aplicación. | Para servir los archivos generados basta un alojamiento estático. |
| Rendimiento | Depende del servidor, las consultas, las extensiones y la caché. | Servir archivos ya preparados reduce el trabajo por visita. |
| Mantenimiento | Hay que actualizar el CMS, sus extensiones y el entorno. | También hay que mantener dependencias, código y servicios externos. |
| Funciones dinámicas | Pueden integrarse mediante módulos o desarrollo. | Suelen apoyarse en JavaScript, APIs o servicios de backend. |
| Ejemplo de uso | Una web gestionada por varios redactores desde un panel. | Un portfolio o una documentación técnica. |

No son opciones incompatibles: un CMS headless puede proporcionar contenido a un SSG. El CMS sirve para editar y el generador para construir la web.

### Un ejemplo cercano

Para una web de apuntes de sistemas, un SSG encaja bien si escribimos en Markdown y publicamos los cambios desde un repositorio. Si varias personas necesitan editar noticias desde un panel visual, un CMS puede resultar más cómodo. La elección depende de cómo vayamos a trabajar, no solo de cuál parezca más rápido.

~~Un sitio estático no puede tener ninguna interacción.~~ Puede tenerla; lo importante es distinguir los archivos prerenderizados de los servicios que aportan funciones dinámicas.

## Ejemplo de contenido

Este fragmento muestra cómo podríamos preparar una entrada sencilla en Markdown. No todos los CMS lo admiten directamente; algunos necesitan un editor o una extensión compatible.

```markdown
# Instalación de Ubuntu Server

En esta práctica configuramos una máquina virtual.

- Crear la máquina.
- Instalar el sistema.
- Comprobar la conexión de red.
```

El nombre de un archivo, como `practica-redes.md`, se puede destacar usando código en línea.

---

## Vídeo explicativo

[Ver «Headless CMS explained in 2 minutes», de Sanity](https://www.youtube.com/watch?v=-Uor3I0n_vQ).

- Duración: 2 minutos y 3 segundos.
- Idioma: inglés.
- Explica el CMS tradicional y utiliza esa comparación para presentar la arquitectura headless.

## Documento relacionado

[Continuar con los generadores de sitios estáticos y la comparación entre Jekyll, Hugo y Astro](ssg.md).

## Revisión del documento

- [x] Explicar qué es un CMS y cómo funciona.
- [x] Incluir tipos, ejemplos y comparación con un SSG.
- [x] Añadir imagen, tabla, listas, cita y código.
- [x] Enlazar el vídeo y el documento sobre SSG.
- [ ] Comprobar la vista previa y hacer la captura en GitHub.

## Fuentes consultadas

- [Acquia: sistemas de gestión de contenidos](https://www.acquia.com/solutions/content-management).
- [Strapi: CMS headless frente a tradicional](https://strapi.io/headless-cms/headless-cms-vs-traditional-cms-understanding-the-difference).
- [Pantheon: WordPress tradicional y headless](https://pantheon.io/learning-center/headless/cms-vs-wordpress).
- [Documentación de Jekyll](https://jekyllrb.com/docs/).
