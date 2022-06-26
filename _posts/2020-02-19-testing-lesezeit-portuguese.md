---
layout: post
title:  Testando o «Jekyll Lesezeit» em Português
date:   2020-02-19 09:32:35 +0100
lang: pt
categories: fehlersuche
description: "Esta página é apenas para teste de software em português."
tags: [Jekyll, Lesezeit, Português]
---
Abra este artigo para ver a demonstração ao vivo em Português e como implantar o script.
<!--more-->

### Caso de uso nº 1

Você deseja que o <em>Lesezeit</em> exiba informações <em>no idioma do site</em>.

Defina o idioma global em <code>config.yml</code>. Este site: <code>lang: de</code>

Não defina o idioma na «frontmatter» de páginas individuais.

<pre>
---
layout: post
title: O Título da Sua Página
date: YYYY-MM-DD HH:MM:SS
categories: opcional
description: "Alguma descrição útil."
tags: [Opcional, vo-ce, DeCide]
---
</pre>

Resultado: O <em>Lesezeit</em> exibe a contagem de palavras e o tempo de leitura no idioma do site.

### Caso de uso nº 2

Você deseja que páginas individuais exibam o <em>Lesezeit</em> em (um) idioma(s) <em>diferente do idioma do site</em>.

Defina o idioma global em <code>config.yml</code>. Este site: <code>lang: de</code>

Defina o idioma da página em «frontmatter» de páginas individuais. Esta página:

<pre>
---
layout: post
title: Testando o «Jekyll Lesezeit» em Português
date: 2020-02-19 09:32:35 +0100
lang: pt
categories: fehlersuche
description: "Esta página é apenas para teste de software em português."
tags: [Jekyll, Lesezeit, Português]
---
</pre>

Resultado: O idioma do site permanece «Alemão» (<code>&#60;html lang=&#34;de&#34;&#62;</code>). O idioma da página é o «Português» (ou então eu finjo) (<code>&#60;html lang=&#34;pt&#34;&#62;</code>). <em>Lesezeit</em> exibe a contagem de palavras em português e o tempo de leitura nesta página.
