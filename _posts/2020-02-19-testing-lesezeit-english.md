---
layout: post
title:  Testing “Jekyll Lesezeit” in English
date:   2020-02-19 09:32:35 +0100
lang: en
categories: fehlersuche
description: "This page is for software testing in English only."
tags: [JekyllLesezeit]
---
Open this article to see the live demo in English and how to deploy the script.
<!--more-->

### Use Case #1

You want <em>Lesezeit</em> to display information <em>in your site language</em>.

Set global language in <code>config.yml</code>. On this site: <code>lang: de</code>

Don’t set language in “frontmatter” of individual pages.

<pre>
---
layout: post
title: The Title of Your Page
date: YYYY-MM-DD HH:MM:SS
categories: optional
description: "Some useful description."
tags: [Optional, all-up, ToYou]
---
</pre>

Result: <em>Lesezeit</em> displays word count and reading time in site language.

### Use Case #2

You want individual pages to display <em>Lesezeit</em> in (a) language(s) <em>different from your site language</em>.

Set global language in <code>config.yml</code>. On this site: <code>lang: de</code>

Set page language in “frontmatter” of individual pages. On this page:

<pre>
---
layout: post
title: Testing “Jekyll Lesezeit” in English
date: 2020-02-19 09:32:35 +0100
lang: en
categories: fehlersuche
description: "This page is for software testing in English only."
tags: [JekyllLesezeit]
---
</pre>

Result: Site language remains “German” (<code>&#60;html lang=&#34;de&#34;&#62;</code>). Page language is “English” (<code>&#60;html lang=&#34;en&#34;&#62;</code>). <em>Lesezeit</em> displays English word count and reading time on this page.
