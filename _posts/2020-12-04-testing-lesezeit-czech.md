---
layout: post
title:  Testování „Jekyll Lesezeit“ v češtině
date:   2020-12-04 09:32:35 +0100
lang: cz
categories: hledání chyb
description: "Tato stránka je určena pouze pro testování softwaru v češtině."
tags: [Jekyll, Lesezeit, čeština]
---
Pokud máte zájem o live–demo v češtině a chcete vědět, jak lze tento skript použít, otevřete prosím tenhle článek.
<!--more-->

### 1. Možnost použití

Chcete, aby vám <em>Lesezeit</em> poskytl informaci v jazyku webové stránky.

Zadejte jeden z globálních jazyků ve <code>config.yml</code>. Na této webové stránce: <code>lang: de</code>

Nezadávejte ve frontmatteru jednotlivých stránek žádné jazykové parametry.

<pre>
---
layout: post
title: Vámi zvolený titul webové stránky
date: YYYY-MM-DD HH:MM:SS
categories: opce
description: "Smysluplný popis webové stránky."
tags: [opce,jak,chcete]
---
</pre>

Výsledek: <em>Lesezeit</em> vám ukáže počet slov a čas, který je potřeba k přečtení textu.

### 2. Možnost použití

Chcete, aby vám <em>Lesezeit</em> ukázal text v jiném jazyku nebo v jiných jazycích, než je originální jazyk webové stránky.

Zadejte jeden z globálních jazyků ve <code>config.yml</code>. Na této webové stránce: <code>lang: de</code>

Zadejte jazyk ve frontmatteru příslušné webové stránky. Na této webové stránce:

<pre>
---
layout: post
title: Test „Jekyll Lesezeit“ v češtině
date: 2020-12-04 09:32:35 +0100
lang: cz
categories: hledání chyb
description: "Myšleno pouze k testování softwaru v češtině."
tags: [Jekyll, Lesezeit, čeština]
---
</pre>

Výsledek: Jazykem webových stránek zůstává „němčina“ (<code>&#60;html lang=&#34;de&#34;&#62;</code>). Jazyk různých stránek na tomto webu není německý (<abbr>např.</abbr> <code>&#60;html lang=&#34;en&#34;&#62;</code> nebo <code>&#60;html lang=&#34;it&#34;&#62;</code>). <em>Lesezeit</em> zobrazuje počet slov a dobu čtení v příslušném jazyce stránky.
