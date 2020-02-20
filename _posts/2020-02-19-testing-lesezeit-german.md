---
layout: post
title:  „Jekyll Lesezeit“ auf Deutsch testen
date:   2020-02-19 09:32:35 +0100
lang: de
categories: fehlersuche
description: "Diese Seite ist nur zum Testen von Software auf Deutsch gedacht."
tags: [JekyllLesezeit]
---
Öffnen Sie diesen Eintrag wenn Sie die Live–Demo auf Deutsch interessiert und wissen wollen wie das Skript angewendet wird.
<!--more-->

### Anwendungsfall #1

Sie wollen, dass <em>Lesezeit</em> die Information <em>in der Sprache der Website</em> ausgibt.

Setzen Sie eine globale Sprache in <code>config.yml</code> fest. Auf dieser Website: <code>lang: de</code>

Setzen Sie keine Sprachparameter im „Frontmatter“ einzelner Seiten.

<pre>
---
layout: post
title: Ihr Seitentitel
date: YYYY-MM-DD HH:MM:SS
categories: optional
description: "Eine sinnvolle Seitenbeschreibung."
tags: [Optional, WieSie, wol-len]
---
</pre>

Ergebnis: <em>Lesezeit</em> zeigt Wortanzahl und Lesezeit in der Sprache der Website an.

### Anwendungsfall #2

Sie wollen auf einzelnen Seiten <em>Lesezeit</em> in (einer) anderen Sprache(n) anzeigen, die <em>nicht die Website–Sprache ist (sind)</em>.

Setzen Sie eine globale Sprache in <code>config.yml</code> fest. Auf dieser Website: <code>lang: de</code>

Setzen Sie eine Seitensprache im „Frontmatter“ der jeweiligen Seite. Auf dieser Seite:

<pre>
---
layout: post
title: „Jekyll Lesezeit“ auf Deutsch testen
date: 2020-02-19 09:32:35 +0100
lang: de
categories: fehlersuche
description: "Diese Seite ist nur zum Testen von Software auf Deutsch gedacht."
tags: [JekyllLesezeit]
---
</pre>

Ergebnis: Die Sprache der Website bleibt „Deutsch“ (<code>&#60;html lang=&#34;de&#34;&#62;</code>). Die Sprache unterschiedlicher Seiten auf dieser Website ist nicht Deutsch (also etwa <code>&#60;html lang=&#34;en&#34;&#62;</code> oder <code>&#60;html lang=&#34;it&#34;&#62;</code>). <em>Lesezeit</em> zeigt Wortanzahl und Lesezeit in der jeweiligen Seitensprache an.
