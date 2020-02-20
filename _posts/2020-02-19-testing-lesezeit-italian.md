---
layout: post
title:  Test di Jekyll Lesezeit in Italiano
date:   2020-02-19 09:32:35 +0100
lang: it
categories: fehlersuche
description: "Questa pagina è solo per test del software in italiano."
tags: [JekyllLesezeit]
---
Apri questo articolo per vedere la demo live in Italiano e come distribuire lo script.
<!--more-->

### Caso d’uso n. 1

Desideri che <em>Lesezeit</em> visualizzi le informazioni <em>nella lingua del tuo sito</em>.

Imposta la lingua del sito in <code>config.yml</code>. Su questo sito: <code>lang: de</code>

Non impostare la lingua in &#171;frontmatter&#187; delle singole pagine.

<pre>
---
layout: post
title: Il Titolo della Tua Pagina
date: YYYY-MM-DD HH:MM:SS
categories: opzionale
description: "Qualche descrizione utile."
tags: [Opzionale, spetta-a-voi, DeCidere]
---
</pre>

Risultato: <em>Lesezeit</em> visualizza il conteggio delle parole e il tempo di lettura nella lingua del sito.

### Caso d’uso n. 2

Desideri che le singole pagine visualizzino <em>Lesezeit</em> in (una lingua diversa) lingue diverse da quella del tuo sito.

Imposta la lingua del sito in <code>config.yml</code>. Su questo sito: <code>lang: de</code>

Imposta la lingua della pagina in &#171;frontmatter&#187; delle singole pagine. In questa pagina:

<pre>
---
layout: post
title: Test di Jekyll Lesezeit in Italiano
date: 2020-02-19 09:32:35 +0100
lang: it
categories: fehlersuche
description: "Questa pagina è solo per test del software in italiano."
tags: [JekyllLesezeit]
---
</pre>

Risultato: La lingua del sito rimane &#171;Tedesco&#187; (<code>&#60;html lang=&#34;de&#34;&#62;</code>). La lingua della pagina è &#171;Italiano&#187; (o almeno spero) (<code>&#60;html lang=&#34;it&#34;&#62;</code>). <em>Lesezeit</em> visualizza il conteggio delle parole e il tempo di lettura su questa pagina in italiano.
