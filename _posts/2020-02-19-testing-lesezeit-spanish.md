---
layout: post
title:  Prueba de «Jekyll Lesezeit» en Español
date:   2020-02-19 09:32:35 +0100
lang: es
categories: fehlersuche
description: "Esta página es solo para pruebas de software en español."
tags: [JekyllLesezeit]
---
Abra este artículo para ver la demostración en vivo en Español y cómo implementar el script.
<!--more-->

### Caso de uso n. ° 1

Desea que <em>Lesezeit</em> muestre información <em>en el idioma de su sitio</em>.

Establecer idioma del sitio en <code>config.yml</code>. En este sitio: <code>lang: de</code>

No establecer el idioma en «frontmatter» de páginas individuales.

<pre>
---
layout: post
title: El Título de Tu Página
date: YYYY-MM-DD HH:MM:SS
categories: opcional
description: "Alguna descripción útil."
tags: [Opcional, DePende, de-usted]
---
</pre>

Resultado: <em>Lesezeit</em> muestra el recuento de palabras y el tiempo de lectura en el idioma del sitio.

### Caso de uso n. ° 2

Desea que las páginas individuales muestren <em>Lesezeit</em> en (un) idioma(s) <em>diferente(s) del idioma de su sitio</em>.

Establecer idioma del sitio en <code>config.yml</code>. En este sitio: <code>lang: de</code>

Establecer el idioma de la página en «frontmatter» de las páginas individuales. En esta página:

<pre>
---
layout: post
title: Prueba de «Jekyll Lesezeit» en Español
date: 2020-02-19 09:32:35 +0100
lang: es
categories: fehlersuche
description: "Esta página es solo para pruebas de software en español."
tags: [JekyllLesezeit]
---
</pre>

Resultado: El idioma del sitio sigue siendo «Alemán». El idioma de la página es «Español» (o eso espero). <em>Lesezeit</em> muestra el recuento de palabras y el tiempo de lectura en esta página en Español.
