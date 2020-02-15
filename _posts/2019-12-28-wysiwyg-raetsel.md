---
layout: post
title:  Das WYSIWYG–Editor Rätsel
date:   2019-12-28 17:32:35 +0100
description: "Wenn sich WYSIWYG-Editoren nicht an gängige Konventionen halten, nützt einfache Anwendung auch wenig."
categories: werkzeuge
tags: [CSS, Editoren, HTML, Textformatierung, WYSIWYG]
---
Ich habe schon einige sogenannte <abbr title="What You See Is What You Get">WYSIWYG</abbr>–Editoren gesehen, und je öfter ich einen benutze, umso weniger mag ich sie. Ich frage mich, ob das wirklich nur an mir und meiner Vorliebe für sinnvolles, semantisches <abbr title="HyperText Markup Language">HTML</abbr> liegt.
<!--more-->
<figure>
<p><img src="{{site.baseurl}}/assets/images/wysiwyg.png" /></p>
<figcaption>
<p>Abbildung: What You See Is What You Get (But Hardly Evuh What You Want)</p>
</figcaption>
</figure>

Was genau wäre jetzt der Vorteil von „einfach drauf los schreiben“ können, wenn man hinterher von Hand alle „doppelten“ Zeilenumbrüche durch standardkonforme Absätze ersetzen muss, damit der Browser semantisches <abbr>HTML</abbr> zu lesen bekommt? Die wenigen zum Verfassen sinnvoller, gut lesbarer Texte wirklich notwendigen <abbr>HTML</abbr>–Tags hat jeder halbwegs begabte Blogger nach ein, zwei selbst geschriebenen Artikeln ganz nebenbei gelernt.

Ein außergewöhnliches Exemplar an wenig logischer Umsetzung — und ich möchte das wirklich nicht als harsche Kritik, vielleicht aber als zarten Hinweis für kommende Versionen, verstanden wissen — scheint mir der Texteditor bei <em>Blogger</em> zu sein.

Ich dachte wirklich eine Weile, ich sei einfach zu doof, die Anwendung zu verstehen (oder hätte vielleicht irgendeine relevante Einstellung übersehen). Aber nein, es ist tatsächlich so, dass korrekt ausgezeichnete Absätze (<code>&lt;p&gt;…&lt;/p&gt;</code>) in einfache Zeilenumbrüche (<code>&lt;br /&gt;</code>) verwandelt werden, sobald man von der <abbr>HTML</abbr>– in die Verfassen–Ansicht wechselt — und zwar vollkommen unabhängig davon, welche Optionen man (in der Leiste, rechts des Editorfensters) ausgewählt hat. Analog dazu werden dann auch einfache Zeilenumbrüche im Quellcode ausgezeichnet. Benutzt man die Verfassen–Ansicht nicht, bleiben die vorhandenen Absatzformatierungen erhalten, und werden auch im Quellcode korrekt ausgezeichnet.

Außergewöhnlich ist dieses Verhalten insofern, als derselbe Editor, ohne dass der Benutzer Zauberformeln murmeln und Kräuter verbrennen muss, brav eine Vielzahl an Sonderzeichen (mit Ausnahme von Umlauten, Akzenten und der <abbr>sz</abbr>–Ligatur) in die entsprechenden (also korrekten) Unicode–Sonderzeichen umwandelt.

Bei manchen allerdings, verweigert er die widerstandslose Zusammenarbeit vollkommen. Wenn man beispielsweise &szlig; ins Textfeld der HTML–Ansicht eingibt und anschließend aktualisiert, wird ein „scharfes–s“ im Browserfenster ausgegeben (so soll es auch sein). Wechselt man aber einmal in die Verfassen–Ansicht, treten nicht nur alle bereits beschriebenen Phänomene auf, es wird auch noch das &amp;szlig; im Quellcode zu &amp;amp;szlig; und damit zu &amp;szlig; im Ausgabefenster. (Fun fact: Das renommierte <em>Wall Street Journal</em> hat dasselbe Problem.)

<h3>Wie die semantisch korrekte Welt eigentlich aussehen sollte</h3>

Da jetzt alle Klarheiten endgültig beseitigt sind, sprechen wir doch darüber, wie die semantisch korrekte Welt eigentlich aussehen sollte.

Einfache Zeilenumbrüche in digitalen Fließtexten müssen überhaupt nicht ausgezeichnet werden. Die Zeilenlänge wird entweder durch den vorhandenen Platz im Browserfenster oder (idealerweise) durch eine entsprechende Anweisung im <abbr title="Cascading Style Sheet">CSS</abbr> vorgegeben. Gibt man eine Breite von 30em vor (das wären dann etwa 60 Zeichen), so entspricht das, nach ausreichend verbreiteter Ansicht, der optimalen Zeilenlänge für gute, flüssige Lesbarkeit.

Veröffentlicht man aber ein Gedicht oder einen Liedtext (der ja auch ein Gedicht ist), wird es schon sinnvoll sein, dem Browser aufs Zeichen genau zu sagen, wo die Zeile umgebrochen werden soll. Also: <code>&lt;br /&gt;</code> (Weil Zeilenumbrüche „Leerelemente“ sind — und nicht paarweise auftreten — müssen sie sich selbst schließen.)

Im Browserfenster ist zwischen den Zeilen nur ein „einfacher Durchschuss“ (oder „normaler Zeilenabstand“, wie wir modernen Menschen sagen) zu erkennen. Im Gegensatz dazu, erkennen wir Absätze in digitalen Dokumenten üblicherweise am „doppelten Durchschuss“. Also: <code>&lt;p&gt;…&lt;/p&gt;</code>

Wer’s ganz klassisch mag, kann bei Absätzen den normalen Zeilenabstand beibehalten, aber die erste Zeile „einziehen“. Davon wäre aber bei längeren Texten abzuraten, da sich die Lesbarkeit dadurch nicht wirklich verbessert (dafür aber der Formatierungsaufwand steigt).

Da sich das „<abbr>WYSIWYG</abbr>–Editor Rätsel“ heute ohnehin nicht lösen lässt, hier noch ein Wort zum Zeilenabstand: Für gute Lesbarkeit wird üblicherweise ein Abstand in 1,3–facher Zeichenhöhe (Schriftgröße) empfohlen. Also: body <code>{font-size: 1em; line-height: 1.3em;}</code>

Wer lieber auf die gute alte Physik zurückgreift, kann aber auch 1:1,618 verwenden (das wäre dann der „Goldene Schnitt“). Also: <code>body {font-size: 1em; line-height: 1.618em;}</code>
