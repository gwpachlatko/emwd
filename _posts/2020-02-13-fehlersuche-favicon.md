---
layout: post
title:  "Dringend gesucht: Favicon"
date:   2020-02-13 16:32:35 +0100
categories: fehlersuche
description: "Das Favicon erscheint nur auf der Homepage, nicht aber auf den Unterseiten? Dann sagen Sie dem Browser, wo’s lang geht."
tags: [Favicon]
---
„Dringend gesucht: Favicon. Abgängig seit: Jahren. Zuletzt gesehen: auf der Homepage. Besondere Merkmale: klein und schwer zu fassen.“ So (oder so ähnlich) könnte man die Lage, wie sie sich seit Jahren — und durchaus systemübergreifend — in diversen Hilfeforen darstellt, in einem Suchaufruf zusammenfassen.<!--more-->

Eigentlich ist es ein eher kleines Problem — nicht nur wegen der geringen Größe des Icons. Das große Problem scheint in diesem Fall zu sein, dass sich die Suchenden zuweilen selbst (und gegenseitig) im Weg stehen.

Aber der Reihe nach: Als „Favicon“ wird landläufig das kleine Bild bezeichnet das einerseits Browser und andererseits unterschiedliche Ausgabegeräte benutzen, um einzelne Webseiten oder „Apps“ für den Benutzer optisch leichter unterscheid– <abbr title="beziehungsweise">bzw.</abbr> identifizierbar zu machen.

<h3>Sich in Binsenweisheit zu verbeissen bringt nichts</h3>
Im Prinzip ist es wirklich keine große Angelegenheit. Man speichert das Bild im Wurzelverzeichnis der Website ab, und referenziert die Datei im Kopf der einzelnen Seiten — so zumindest die gut verbreitete Theorie. Eine Standardübung, könnte man meinen.

Nur, von <em>einem</em> Standard scheinen wir auch hier noch weit entfernt zu sein. Im Netz werden gleich mehrere „Standards“ (und — noch viel überraschender — mehr als eine „richtige Umsetzung“, wovon jede die einzige und beste zu sein scheint) gehandelt — wohl je nach dem, wer von wem (und wann) die jeweilige Idee übernommen hat, und wie oft diese verbreitet wurde. Das Ergebnis lässt sich am besten mit zwei Worten zusammenfassen: Geplantes Scheitern.

Ja, manche Browser halten sich immer noch nicht an vermeintlich allgemeingültige Konventionen. Zur Kenntnis genommen und verkündet.

Ja, es kann schon darauf ankommen, welche Software im speziellen Fall verwendet wird. Zur Kenntnis genommen und verkündet.

Nein, es bringt gar nichts, sich darüber zu ärgern. Ein Ausgabegerät zu entwickeln, das alle vermeintlich allgemeingültigen Konventionen unterstützt und einhält, dauert länger als die Fehlersuche im speziellen Fall. (Diese Weisheit könnte unendlich oft verkündet werden, sie scheint nie zur Kenntnis genommen zu werden.)

<h3>Was bringt uns weiter?</h3>

Also, was bringt uns weiter, wenn das Favicon nur auf der Homepage dargestellt wird, nicht aber auf den Unterseiten der Website? (Ich darf davon ausgehen, dass wir alle wissen, dass wir hier von dynamisch erstellten Websites sprechen?)

<ol>
  <li>Nachsehen, ob das entsprechende Bild auch wirklich (also physikalisch) an angegebener Stelle liegt.</li>
  <li>Auf etwaige Tippfehler bei der Namensgebung des Bildes achten.</li>
  <li>Überprüfen, ob der angegebene Pfad zum Bild korrekt ist.</li>
  <li>Auf etwaige Tipp– oder Logikfehler bei der Pfadangabe achten.</li>
  <li>Überprüfen, welcher Konvention die verwendete Software bei der Auszeichnung von Verweisen (und Pfaden) folgt.</li>
</ol>

<h3>Wo befindet sich das Wurzelverzeichnis?</h3>

Es scheint sich auch nach Jahrzehnten noch nicht landläufig herumgesprochen zu haben: Als Wurzelverzeichnis (<abbr>Engl.</abbr>, root; üblicherweise durch einen einzelnen Schrägstrich dargestellt) wird jene Ebene bezeichnet, in der die Index–Datei (<code>index.html</code>, <code>index.php</code> <abbr title="oder ähnliches">o.ä.</abbr>) der Website am Server abgespeichert ist.

Beispiel: <a title="Verweis auf die Startseite dieser Website" href="https://gwpachlatko.github.io/emwd">https://gwpachlatko.github.io/emwd</a> verweist auf das Wurzelverzeichnis dieser Website — und führt zur Index–Datei (sofern diese vorhanden ist).

Denselben Effekt erzielt man, wenn man „root“ in der Webadresse mit angibt: <a title="Verweis auf die Startseite dieser Website" href="https://gwpachlatko.github.io/emwd/">https://gwpachlatko.github.io/emwd/</a>. Der letzte Schrägstrich in dieser Adresse symbolisiert das Wurzelverzeichnis.

Wenn Sie beide Links ausprobiert (und dabei auf die Adresszeile des Browsers geachtet) haben, wissen Sie jetzt, dass der Server immer das Wurzelverzeichnis mit angibt — weshalb Sie es bei der Eingabe auch weglassen können. Server folgen im Allgemeinen nicht den Konventionen einzelner Designer — leider ist zuweilen auch die Umkehrung dieser Weisheit wahr.

<h3>Tipp– und Logikfehler</h3>

Tippfehler können immer und überall (also jedem) passieren. Das kann leicht zum „Nadel–im–Heuhaufen–Problem“ führen. Bei dynamisch erstellten Websites kann ein einzelner Tippfehler weitreichende, und auch recht verwirrende, Auswirkungen haben: Er wird nur einmal gemacht, aber, je nach dargestellter Situation, zu unterschiedlichen Ergebnissen führen, weil ein bestimmter Teil (der eben diesen Fehler enthält) immer wieder verwendet wird. Hier hilft nur, sich einen Überblick über den Seitenaufbau zu verschaffen, um die betroffene Datei (und damit den Fehler) zu lokalisieren.

Logikfehler sind da schon wesentlich leichter in den Griff zu bekommen. Finden Sie eine gut nachvollziehbare Konvention und halten Sie sich strikt daran. Legen Sie etwa alle Bilddateien immer im selben Verzeichnis ab; etwa so <code>/img/bild.png</code> oder so <code>/images/bild.png</code> oder auch so <code>/assets/images/bild.png</code>.

Die letztgenannte Variante hat gleich zwei Vorteile: Sie können Ihre Bild– und <abbr>CSS</abbr>–Datei(en) gleich „nebenan“ in einem gemeinsamen Unterverzeichnis lagern (also etwa so <code>/assets/images/bild.png</code> und <code>/assets/css/main.css</code>), und nicht wenige <abbr title="Content Management Systeme">CMS</abbr> folgen ebenfalls dieser Verwaltungslogik.

Alles andere führt nur zu Unordnung und erschwerter Fehlersuche. Wenn Sie einige Dateien hier, einige woanders und wieder einige ganz woanders lagern, und eine wirklich umfangreiche Seite betreiben, dann bleibt Ihnen nur, auf lange, einsame Winternächte zu hoffen.

<h3>Ja, aber manche Browser …</h3>

Nein, nicht wirklich. Wenn manche Browser auch ohne Referenzierung des Favicons „by default“ (also quasi ab Werk) im Wurzelverzeichnis danach suchen, gut. Alle folgen diesem „Standard“ offensichtlich nicht, weshalb wir hier und jetzt überhaupt darüber reden. Was aber alle können (und wohl auch machen) ist, klare Anweisungen im Quellcode befolgen.

Rufen Sie den Quellcode dieser Seite auf. Das könnte je nach verwendetem System unterschiedlich ablaufen, ich hab’s jetzt nicht im Kopf. Bei mir geht’s am schnellsten mit der Tastenkombination <abbr title="Steuerung (ganz unten links) und den Buchstaben u gemeinsam drücken">Strg+U</abbr>.

Es müsste schon mit dem Teufel zugehen, würden die Referenzen für Bild– und <abbr>CSS</abbr>–Dateien nicht als Verweise dargestellt. Klicken Sie diese der Reihe nach an. Sie sollten alle zu der jeweils angegebenen Datei führen. Ist das der Fall, werden die entsprechenden Informationen (die diese Dateien enthalten) auch umgesetzt — und als Konsequenz im Browser dargestellt <abbr>bzw.</abbr> verarbeitet.

Die Überlegung was „manche Browser machen (und andere auch oder vielleicht doch nicht)“ kann nie zu einer stabilen Lösung führen. Der einzige (nach meinem bescheidenen Verständnis) vernünftige Ansatz ergibt sich aus der Frage: „Was machen alle Browser?“ Und die Antwort darauf ist: „Anweisungen im Quellcode ausführen.“ Und je weniger „Hacks“ dafür notwendig sind, desto besser.

<h3>Da wären dann noch die Eigenarten einzelner Systeme …</h3>

Ja, die wären da noch. Es ist mir auch schon aufgefallen, dass einzelne Content Management Systeme teilweise recht unterschiedliche Ansätze bezüglich relativer Verweise (<abbr title="das heißt">d.h.</abbr> relativ zur Gesamtstruktur der Website) verfolgen.

Die einzige generische (allgemeingültige, universelle) Lösung die mir dazu aus dem Stegreif einfiele, wäre alle Links absolut anzugeben — unabhängig davon, welcher Konvention die Entwickler des jeweiligen <abbr>CMS</abbr> eigentlich folgen. Das könnte sich zuweilen mühsam gestalten, sollte aber zu keinen „technischen Verwicklungen“ führen. Das würde dann hier im Falle des Favicons so aussehen:

<code>&lt;link rel=&#34;icon&#34; type=&#34;image/png&#34; sizes=&#34;16x16&#34; href=&#34;https://gwpachlatko.github.io/emwd/assets/images/favicon-16x16.png&#34; &#47;&gt;</code>

Ansonsten bleibt nur, sich dem jeweiligen System und seinen Konventionen anzupassen.

Beispiel: Um das Favicon hier in Jekyll verlässlich einzubinden und auf allen Seiten angezeigt zu bekommen, habe ich alle Bilddateien in <code>/assets/images/</code> gesammelt, und verweise darauf mittels „Liquids“ nach der ansonsten in diesem <abbr>CMS</abbr> üblichen Konvention. Also etwa:

<code>&lt;link rel=&#34;icon&#34; type=&#34;image/png&#34; sizes=&#34;16x16&#34; href=&#34;&#123;&#123; site.baseurl &#125;&#125;/assets/images/favicon-16x16.png&#34; &#47;&gt;</code>

Damit wirft der Server keine Fehler aus, die Seiten validieren nach <abbr title="World Wide Web Consortium; die Organisation, die Empfehlungen für Webstandards ausspricht">W3C</abbr> und das Favicon wird auf allen Seiten und in allen (getesteten) Browsern angezeigt. Fall erledigt.
