---
layout: post
title:  Die wahren Barrieren sind im Kopf
date:   2020-01-04 17:32:35 +0100
lang: de
categories: barrierefrei
description: "Das Internet kennt keine Einschränkungen die wir landläufig als Barrieren bezeichnen. Diese würden schließlich der Absicht, Informationen allgemein zugänglich zu machen, grundsätzlich widersprechen."
tags: [Accessibility, Zugänglichkeit, Barrierefreiheit]
---

<p>Ich vermute, Leser eines gewissenen Alters werden die Anspielung im Titel sofort erkannt haben. Jene, die sich schon eingehender mit Webdesign befasst haben, werden wahrscheinlich sogar zustimmen, dass auch der Rest von André Hellers berühmter Textzeile durchaus zutreffend ist: &#8222;&#8230; und sind sie nicht im Kopf, dann sind sie nirgendwo.&#8220;</p>
<!--more-->
<p>Das Internet &#8212; und damit eigentlich auch Webdesign als Konzept &#8212; kennt keine Einschränkungen die wir landläufig als Barrieren bezeichnen. Diese würden schließlich der Absicht, Informationen allgemein zugänglich zu machen, grundsätzlich widersprechen. Webseiten müssen daher nicht barrierefrei „gemacht“ werden — es würde schon reichen, diese barrierefrei zu halten.</p>

<p>Am einfachsten lässt sich diese Aussage (oder Annahme) anhand von Links (Verweisen) in alten (<abbr title="das heißt">d.h.</abbr>, in den 1980er <abbr title="beziehungsweise">bzw.</abbr> frühen 1990er Jahren registrierten) Webseiten, die heute noch verfügbar sind, überprüfen.</p>

<p>Die überwiegende Mehrheit dieser Dokumente weist noch blaue Links aus, und die allermeisten davon sind tatächlich unterstrichen. Bereits besuchte Verweise werden violett dargestellt (solange, bis der Browserspeicher gelöscht wird), und aktive Links leuchten kurz rot auf (das lässt sich allerdings bei heutigen Verbindungsgeschwindigkeiten kaum mehr erkennen, aber dass diese Seiten keine Anweisungen für die Darstellung von Links enthalten ist ein starkes Indiz dafür).</p>

<p>Es lässt sich also festhalten, Links werden standardmäßig leicht erkennbar (und damit gut zugänglich) dargestellt &#8212; und das ist schon &#8222;eine ganze Weile&#8220; so. Ich erinnere mich an kein relevantes Browsermodell, das diese Konvention nicht befolgt hätte.</p>

<p>Fügt man nun noch einen Titel (<code>&lt;a title="kurzer, sinnvoller Text, der die Zielseite beschreibt" &#8230;&gt;</code>) in den Anker&#8211;Tag ein, und wählt, wenn irgend möglich, eine sinnvolle Textpassage, die dieser umschließen soll, ist man schon auf der sicheren Seite. Mehr bräuchte es gar nicht.</p>

<p>Zugegeben, dann wären alle Verweise in allen digitalen Dokumenten dieser Welt blau und unterstrichen, und Webdesigner arbeitslos. Ja, genau &#8230; als ob die Webdesigner dieser Welt nicht anderes zu tun hätten, als Links in allen möglichen Farben darzustellen. Wobei, man könnte bisweilen schon auf diesen Gedanken verfallen.</p>

<p>Kürzlich sah ich tatsächlich Links, die in der <a title="dieser Link verweist auf sich selbst, er dient lediglich der Veranschaulichung eines Missstandes" href="#text" class="text" name="text">Farbe des Fließtextes</a> ausgezeichnet waren. Hier hatte man offenkundig wirklich nichts Dringenderes zu tun. Die Aufgabe (für sehende Benutzer) ist, &#8222;finde den Verweis&#8220;; selbst volle Sehschärfe hilft hier nichts, man muss tatsächlich mit dem Zeigegerät über den Verweis &#8222;stolpern&#8220;.</p>

<p>So stören Links das Schriftbild zweifellos am wenigsten. Aber ist ein ungestörtes Schriftbild der tiefere Sinn dieser Übung? Wozu dann überhaupt einen Link setzen? Und wie genau sollen Benutzer erkennen, ob es sich &#8222;bloß&#8220; um eine betonte Stelle oder vielleicht doch um einen klickbaren Link handelt? Kursiver Schnitt wird landläufig für Markennamen, Buch&#8211; oder Filmtitel und Betonungen verwendet. (Diese werden im Quellcode durch <code>&lt;em&gt;&#8230;&lt;&#47;em&gt;</code> ausgezeichnet. Im <abbr>CSS</abbr> verweist man dann für diese Tags auf den kursiven Schnitt der verwendeten Schriftart. Siehe dazu auch <a title="Interner Verweis auf diesen Artikel" href="{{ site.baseurl }}{% post_url 2020-01-01-typografie %}">Nun sag, wie hast Du&#8217;s mit der Typografie?</a>)</p>

<p>Ohne jegliche Anweisung würde der <a title="dieser Link verweist auf sich selbst, er dient lediglich der Veranschaulichung eines Missstandes" href="#navy" class="navy" name="navy">Link in Marineblau und unterstrichen</a> erscheinen.</p>

<p>Wer sich tatsächlich nicht mit den &#8222;bunten&#8220; Links anfreunden kann, könnte die Farbe ruhig dem Fließtext anpassen (auf dieser Seite wäre das <code>a:link {color: &#35;000;}</code>). Auftrag ausgeführt! Das sähe dann so aus: <a title="dieser Link verweist auf sich selbst, er dient lediglich der Veranschaulichung eines Missstandes" href="#black" class="black" name="black">Link in Schriftfarbe aber unterstrichen</a>.</p>

<p>Wem das immer noch nicht zusagt, der könnte einen Schritt weiter gehen, die Unterstreichung aufheben und dafür einen &#8222;unteren Rand&#8220; anweisen: <code>a:link {color: &#35;000; text-decoration: none; border-bottom: 1px &#35;000 solid;}</code>, was dann so aussähe: <a title="dieser Link verweist auf sich selbst, er dient lediglich der Veranschaulichung eines Missstandes" href="#blackbb" class="blackbb" name="blackbb">Link in Schriftfarbe, nicht unterstrichen, aber mit Unterrandung</a>.</p>

<p>In diesem Fall könnte man sich sogar die Randstärke aussuchen, indem man etwa die obige Anweisung auf <code>border-bottom: 2px &#35;000 solid;</code> abändert: <a title="dieser Link verweist auf sich selbst, er dient lediglich der Veranschaulichung eines Missstandes" href="#blackbb2" class="blackbb2" name="blackbb2">Link in Schriftfarbe mit Unterrandung dem Gewicht der Schrift entsprechend.</a></p>

<p>Gar keine optische Auszeichnung ist jedenfalls eine klare &#8222;Themenverfehlung&#8220; &#8230; davon einmal abgesehen, ist der Aufwand praktisch genauso groß wie bei allen anderen genannten Varianten: <code>a:link {color: &#35;000; text-decoration: none; font-style: italic;}</code>. Worin läge der Sinn dieser &#8222;Fleißaufgabe&#8220;, zumal die optische Auszeichnung von Verweisen in Fließtexten ohnehin schon eine weitverbreitete &#8212; und eigentlich auch beliebte &#8212; Praxis ist.</p>

<p>Es muss ja nicht immer Marineblau sein. Das verlangt doch niemand. Es wird auch nicht gleich eine Klagenflut über den Seitenbetreiber hereinbrechen, wenn die Seiten nicht dem allerhöchsten Standard genügen. Aber ein wenig mehr Hausverstand und etwas weniger &#8222;Kreativität&#8220; wäre schon wünschenswert.</p>

<p>Leider ist es aber so, dass die eben erwähnte &#8222;Kreativität&#8220; (gar nicht so selten) lieber dazu verwendet wird, vorhandene Standards zu umgehen &#8212; oder, wie im eben gezeigten Beispiel, damit sogar Unsinn zu treiben.</p>

<p>Dieses Phänomen ist auch nicht mehr ganz neu, <a rel="external" title="Verweis auf die Seite milk.com" href="milk.com">wie die Seite milk.com indirekt beweist</a>. Im Jahr 1994 veröffentlicht, enthielt sie bereits den Hinweis ihres Betreibers, Dan Bornstein, dass seine Seiten keine Blink&#8211;Elemente (wer diese nicht kennt, hat wirklich nichts versäumt) enthalten.</p>

<p>Halten wir abschießend noch fest, worauf es bei Links wirklich ankommt:</p>

<p>Die verwendete Farbe ist weniger entscheidend als der Kontrast zur Umgebung. Farben die sich zu wenig vom Hintergrund oder der <em>Schriftfarbe des Fließtextes</em> (&larr; dies wäre einfach nur eine Betonung des Begriffs) unterscheiden, sind keine so gute Wahl &#8212; besonders dann, wenn auch noch auf jegliche andere optische Auszeichnung verzichtet wird. Ist der <a title="dieser Link verweist auf sich selbst, er dient lediglich der Veranschaulichung eines Missstandes" href="#simbg" class="simbg" name="simbg">Kontrast zum Hintergrund</a> zu gering, nützt auch unterstreichen wenig.</p>

<p>Ist der Linktext schlecht vom Hintergrund unterscheidbar, ließe sich noch mit dem Fokus ein wenig von der Benutzbarkeit retten. Etwa so: <code>a:focus, a:hover {color:&#35;006;}</code> Optimal wäre allerdings, gleich von Beginn an eine brauchbare Farbpalette zu erarbeiten und vernünftige Auszeichnungskonventionen einzuhalten.</p>

<p>Ist der Linktext zu wenig vom Fließtext zu unterscheiden, hilft leider kaum etwas. Wird ein Link gar nicht als solcher erkannt, wird auch kein Benutzer darauf reagieren.</p>

<p>Spannend in diesem Zusammenhang sind natürlich immer Fragen nach der Häufigkeit von Bedarfsfällen und, in der Folge, nach dem vermeintlichen wirtschaftlichen Nutzen solcher Überlegungen.</p>

<p>Nun, Probleme mit der Farberkennung haben definitiv mehr Menschen, als es offiziell &#8222;Farbblinde&#8220; gibt. Klinisch anerkannte Farbfehlsichtigkeit als Rechengrundlage zu nehmen ist Unsinn, und ebenso fragwürdig ist die Überlegung wie viele statistisch erfasste Benutzer von Geräten für &#8222;Nutzer mit speziellen Bedürfnissen&#8220; es überhaupt gibt.</p>

<p>Hier ein einfaches Rechenbeispiel: Selbst wenn all die Hürden die wir in unseren digitalen Dokumenten durch Unachtsamkeit, Unwissenheit oder Desinteresse verursachen nur bestimmte Gruppen von Behinderungen beträfen, und selbst wenn deren Gesamtzahl &#8222;nur&#8220; 20% aller Nutzer ausmachte, würde jedem Fünften der &#8222;im wirklichen Leben&#8220;, aus welchen Gründen immer, einen Raum betreten will die Tür ins Gesicht geschlagen. Noch Fragen zur Wirtschaftlichkeit von Barrierefreiheit?</p>

<p>Ist meine Argumentation <span title="befangen, einseitig, nicht neutral">tendenziös</span>, hochgradig unfair, emotional geführt, unsachlich? Ja, das ist sie. Alles davon, aber dennoch keineswegs falsch. Die Wahrscheinlichkeit, dass ausgerechnet dieser fünfte Besucher für den Seitenbetreiber den großen Unterschied machen wird, liegt bestimmt sogar unter 20%, aber wer will schon dieser fünfte Besucher sein &#8212; und wer der Seitenbetreiber, dem dieser Besucher den Rücken kehrt?</p>
