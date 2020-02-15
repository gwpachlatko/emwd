---
layout: post
title:  "Jekyll: Wortanzahl und Lesezeit in Artikeln anzeigen"
date:   2020-02-15 13:32:35 +0100
description: "Eine einfache Lösung, um Wortanzahl und Lesezeit in einem Jekyll–Post auszugeben."
categories: werkzeuge
tags: [Liquid, GitHub]
---
Ich habe es immer als sehr praktisch empfunden, bereits vor Beginn der Lektüre wenigstens ungefähr zu wissen wie lange ein Artikel ist. Wer will schon den Lesefluss unterbrechen müssen, weil die vorhandene Zeit nicht reicht? Aber auch als Autor finde ich es angenehm, möglichst früh zu wissen, ob ein Artikel zu lang zu werden droht.<!--more-->

Deshalb habe ich schon früh die Angewohnheit übernommen, die Lesezeit bei meinen Artikeln anzugeben. Nur in deutscher Sprache ist mir dieser Service noch nie untergekommen — was vielleicht auch daran liegt, dass ich zu selten deutschsprachige Artikel lese, ich weiß es nicht.

Nun, hier gibt’s ab jetzt auch den Hinweis auf die (geschätzte) Lesezeit. Grundlage ist die Annahme, dass durchschnittlich geübte Leser etwa 180 Worte pro Minute sinnerfassend lesen können. (Wer mich eines Besseren belehren will — nur zu.)

Die Angabe der Wortanzahl ist eigentlich nur eine Spielerei (die aber während des Schreibens schon recht hilfreich sein kann).

<h3>Wie geht das?</h3>

Die Anwendung ist sehr einfach: Man zählt die Worte in einem Artikel (einem Post, Online–Dokument, was auch immer) und dividiert die Summe durch die Anzahl der vermutlich gelesenen Worte pro Minute.

Jekyll liefert die Wortzahl pro Seite ab Werk — das ist praktisch — und mit Liquid wird das Ergebnis (recht handlich) eingebunden und ausgegeben.

Der <a title="zum Repository auf GitHub" href="https://github.com/gwpachlatko/jekyll-lesezeit">Quellcode ist auf GitHub</a> gelagert. Zur Benutzung gibt es nicht viel anzumerken:

Die Datei <code>lesezeit.html</code> wird im Verzeichnis <code>&#47;&#95;includes&#47;</code> abgespeichert und an gewünschter Stelle in einem Dokument eingebunden: <code>&#123;&#37;&#45; include lesezeit.html &#45;&#37;&#125;</code>