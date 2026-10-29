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

### Arquitectura Headless CMS

En un CMS tradicional, como una instalación habitual de WordPress, la gestión del contenido y la presentación de la web forman parte del mismo sistema. En un **Headless CMS**, esas tareas se separan: el CMS administra la información y una aplicación independiente decide cómo mostrarla. El contenido se entrega mediante una **API**, normalmente como datos JSON, en lugar de depender de una única plantilla del gestor. [Explicación de Contentful](https://www.contentful.com/headless-cms/).

El nombre *headless* puede resultar confuso. No significa que el editor se quede sin panel de administración: lo que se elimina es la dependencia de una presentación pública integrada. Los redactores siguen creando y organizando contenido desde una interfaz, mientras los desarrolladores preparan la web, la aplicación móvil u otros canales. [Explicación de Strapi](https://strapi.io/blog/headless-cms-explained).

#### Componentes de la arquitectura

| Componente | Función | Ejemplo orientativo |
|---|---|---|
| Panel de administración | Permite crear, revisar y publicar contenido, además de gestionar los permisos disponibles. | Un editor redacta una noticia. |
| Repositorio de contenido | Guarda los datos estructurados y las relaciones entre ellos. | Una noticia tiene título, texto, autor e imagen. |
| API | Permite consultar el contenido desde aplicaciones autorizadas. | La web solicita las noticias publicadas y recibe JSON. |
| Frontend independiente | Convierte esos datos en la interfaz que ve el usuario. | Astro construye la web y una aplicación móvil muestra una versión adaptada. |

La organización por repositorio, API y frontend se describe en la [documentación explicativa de Contentful](https://www.contentful.com/headless-cms/). El panel es la herramienta de trabajo del equipo editorial, no la web pública.

# Ranking de los 5 CMS Más Utilizados del Mundo

Un **Sistema de Gestión de Contenido** (*Content Management System* o **CMS**) permite crear, gestionar y modificar contenido en un sitio web sin necesidad de escribir código desde cero. A continuación se presenta el ranking actualizado de los 5 CMS más populares a nivel global, según la cuota de mercado entre sitios con CMS conocido y su presencia general en la web.

---

## 📊 Tabla Comparativa Global

| Ranking | Plataforma (CMS) | Cuota en Mercado CMS (%) | Presencia en Toda la Web (%) | Enfoque Principal |
| :---: | :--- | :---: | :---: | :--- |
| **1** | **WordPress** | 58.7% – 59.1% | 40.2% – 41.2% | Todo tipo de webs (Blogs, Empresas, E-commerce) |
| **2** | **Shopify** | 7.6% – 7.8% | 5.3% – 5.4% | Comercio Electrónico (*E-commerce*) |
| **3** | **Wix** | 6.1% – 6.2% | 4.2% – 4.3% | Creador visual sin código (*No-code*) |
| **4** | **Squarespace** | 3.5% – 3.6% | 2.5% | Diseño visual, Portafolios y Creativos |
| **5** | **Webflow / Joomla** | 1.2% – 1.7% | 0.9% – 1.2% | Diseñadores Web Profesionales / Portales complejos |

---

## 🔍 Análisis Detallado por Plataforma

### 1. WordPress (WordPress.org)
* **Cuota de mercado CMS:** ~58.7% – 59.1%
* **Tipo:** Código abierto (*Open-source*) / Autohospedado
* **Descripción:** Mantiene un dominio abrumador en el ecosistema web global. Su flexibilidad basada en un ecosistema masivo de más de 59,000 *plugins* y 13,000 *temas* permite construir desde blogs personales hasta grandes medios de comunicación global.
* **Puntos fuertes:** Gran comunidad, escalabilidad, control total sobre el código y SEO.

### 2. Shopify
* **Cuota de mercado CMS:** ~7.6% – 7.8%
* **Tipo:** Plataforma como Servicio (*SaaS*)
* **Descripción:** Es la solución líder mundial orientada exclusivamente al comercio electrónico. Simplifica la gestión de tienda, pagos, inventario e infraestructura técnica, eliminando las complicaciones de servidor y seguridad para los comerciantes.
* **Puntos fuertes:** Excelente rendimiento de conversión, seguridad gestionada e integración fluida con pasarelas de pago globales.

### 3. Wix
* **Cuota de mercado CMS:** ~6.1% – 6.2%
* **Tipo:** Creador web SaaS (*Drag and Drop*)
* **Descripción:** Plataforma que ha experimentado un crecimiento acelerado gracias a su editor visual intuitivo y mejoras constantes en rendimiento (*Core Web Vitals*). Es la opción preferida por pequeños negocios y profesionales independientes.
* **Puntos fuertes:** Facilidad de uso, hosting incluido y plantillas de alta calidad sin necesidad de programación.

### 4. Squarespace
* **Cuota de mercado CMS:** ~3.5% – 3.6%
* **Tipo:** Plataforma integrada SaaS
* **Descripción:** Destaca por sus diseños limpios y minimalistas orientados a creadores de contenido, artistas, fotógrafos y marcas enfocadas en la identidad visual.
* **Puntos fuertes:** Estética visual pulida, herramientas integradas de marketing y boletines, e interfaz simplificada.

### 5. Webflow / Joomla
* **Cuota de mercado CMS:** ~1.2% – 1.7%
* **Tipo:** Diseñador SaaS (*Webflow*) / Código abierto (*Joomla*)
* **Descripción:** 
  * **Webflow:** Se consolida entre diseñadores web y agencias por permitir maquetar con control visual directo sobre la estructura CSS y HTML sin escribir código manualmente.
  * **Joomla:** Mantiene presencia en portales institucionales y sistemas de gestión avanzados de usuarios.
* **Puntos fuertes:** Control fino sobre el diseño visual y la estructura web.

---

## 📈 Tendencias Clave del Mercado

1. **Avance de las plataformas SaaS (*Hosted Builders*):** Soluciones como Shopify, Wix y Squarespace continúan ganando terreno frente a plataformas tradicionales que requieren mantenimiento manual de servidores.
2. **Prioridad en el Rendimiento Web:** Los indicadores *Core Web Vitals* de Google han motivado a plataformas cerradas a optimizar la velocidad de carga de sus sitios.
3. **Comercio Unificado:** El crecimiento del *e-commerce* ha posicionado a Shopify como el CMS con mayor aceleración comercial de la década.

---

## 📚 Fuentes y Referencias

* **[W3Techs - World Wide Web Technology Surveys](https://w3techs.com/technologies/overview/content_management):** Monitorización diaria de tecnologías web en el TOP de sitios de internet.
* **[BuiltWith Trends](https://builtwith.com/):** Base de datos e indexación técnica de la presencia de CMS en sitios en vivo.
* **[Colorlib CMS Market Share Report](https://colorlib.com/wp/cms-market-share/):** Análisis consolidado de cuota de mercado, estadísticas interanuales y métricas de rendimiento.
* **[DiviFlash CMS Industry Report](https://diviflash.com/cms-statistics/):** Recopilación estadística de tendencias en plataformas de gestión de contenido.

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


## Fuentes consultadas

- [Acquia: sistemas de gestión de contenidos](https://www.acquia.com/solutions/content-management).
- [Strapi: CMS headless frente a tradicional](https://strapi.io/headless-cms/headless-cms-vs-traditional-cms-understanding-the-difference).
- [Pantheon: WordPress tradicional y headless](https://pantheon.io/learning-center/headless/cms-vs-wordpress).
- [Documentación de Jekyll](https://jekyllrb.com/docs/).
- 
