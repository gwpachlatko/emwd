---
layout: post
title:  Test de Jekyll Lesezeit en Français
date:   2020-02-19 09:32:35 +0100
lang: fr
categories: fehlersuche
description: "Cette page est destinée aux tests de logiciels en français uniquement."
tags: [JekyllLesezeit]
---
Ouvrez cet article pour voir la démo en direct en Français et comment déployer le script.
<!--more-->

### Cas d’utilisation n ° 1

Vous souhaitez que Lesezeit affiche des informations <em>dans la langue de votre site</em>.

Définir la langue globale dans <code>config.yml</code>. Sur ce site: <code>lang: de</code>

Ne pas définir la langue de la page dans &#171;frontmatter&#187; des pages individuelles.

<pre>
---
layout: post
title: Le Titre de Votre Page
date: YYYY-MM-DD HH:MM:SS
categories: facultatif
description: "Une description utile."
tags: [Facultatif, a-vous, DeVoir]
---
</pre>

Résultat: <em>Lesezeit</em> affiche le nombre de mots et le temps de lecture dans la langue du site.

### Cas d’utilisation n ° 2

Vous souhaitez que des pages individuelles affichent <em>Lesezeit</em> dans une (des) langue(s) <em>différentes de la langue de votre site</em>.

Définir la langue globale dans <code>config.yml</code>. Sur ce site: <code>lang: de</code>

Définir la langue de la page dans &#171;frontmatter&#187; des pages individuelles. Sur cette page:

<pre>
---
layout: post
title: Test de Jekyll Lesezeit en Français
date: 2020-02-19 09:32:35 +0100
lang: fr
categories: fehlersuche
description: "Cette page est destinée aux tests de logiciels en français uniquement."
tags: [JekyllLesezeit]
---
</pre>

Résultat: La langue du site reste &#171;Allemand&#187; (<code>&#60;html lang=&#34;de&#34;&#62;</code>). La langue de la page est &#171;Français&#187; (ou alors j'espère) (<code>&#60;html lang=&#34;fr&#34;&#62;</code>). <em>Lesezeit</em> affiche le nombre de mots et le temps de lecture sur cette page en français.
