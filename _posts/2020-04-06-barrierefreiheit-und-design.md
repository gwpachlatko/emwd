---
layout: post
title: Mehr als nur ein hübsches Gesicht
date:   2020-04-06 09:32:35 +0100
lang: de
categories: barrierefrei
description: "Dieser Artikel macht mit dem Vorteil, Barrierefreiheit und ansprechendes Design würden nicht zusammengehen, Schluss."
tags: [Accessibility, Zugänglichkeit, Barrierefreiheit]
---
Was habe ich nicht schon alles an Argumenten gehört, warum Barrierefreiheit „sicherlich schon auch wichtig, aber leider nichts für uns“ ist. Ganz oben auf der Liste der „Hinderungsgründe“ stehen natürlich meist der vermeintliche Aufwand und die damit verbundenen Kosten. Bald danach kommen schon „Designfragen“.
<!--more-->

Bei Aufwand und Kosten bin ich gedanklich noch im Boot — aber ich muss mich schon an die Bordwand klammern, um nicht das Gleichgewicht zu verlieren. Ja, als „nachträglicher Gedanke“ kann Zugänglichkeit schon zum Kostenfaktor werden. Aber selbst dann sollte sich der Mehraufwand eigentlich in vernünftigen Grenzen bewegen. Merke: Die Barrieren, die man vorher nicht aufgebaut hat, muss man hinterher nicht einreißen.

Der logische Zusammenhang zwischen Barrierefreiheit und der optischen Gefälligkeit eines Internetauftritts erschließt sich mir allerdings nicht. Wo genau steht geschrieben, dass optisch ansprechende Auftritte nicht barrierefrei sein können — oder auch umgekehrt, dass zugängliche Seiten „altbacken“, „irgendwie komisch“ oder einfach nur „hässlich“ sein müssen?   

### Ein neues Gesicht für diesen Auftritt

Dass dieser Internetauftritt bislang mit der nur etwas abgeänderten Basisversion der Benutzeroberfläche auskommen musste, hat mich nicht gestört. Das „Theme“ mit dem Jekyll ausgeliefert wird, heißt übrigens „Minima“, was wohl eine Anspielung auf minimalistisches Design sein soll.

Dieses kann dann vom jeweiligen Benutzer durch eigene Anweisungen erweitert werden. Das bedeutet dreierlei:

<ul>
<li>Jeder kann ohne großen Aufwand die Oberfläche optisch den eigenen Wünschen anpassen. (Das ist gut.)</li>
<li>Einige der vorgegebenen Anweisungen müssen vom jeweiligen Benutzer überschrieben werden. (Das ist nicht so gut.)</li>
<li>Strukturelle Mängel werden dadurch nicht behoben. (Das ist gar nicht gut.)</li>
</ul>

Was mich an „Minima“ von Beginn an störte, war nicht so sehr die schlichte optische Darstellung (ganz im Gegenteil), sondern dass ich die Navigation nicht logisch mit der Tastatur bedienen konnte.

### Ein neues Theme erstellen?

„Minima“ (das sogenannte „default theme“, es wird mit Jekyll gebündelt installiert) anzupassen ist keine große „Hexerei“, aber dadurch wird das „Stylesheet“ (die für den optischen Entwurf zuständige Datei) unnötig aufgebläht, weil Grundeinstellungen nur überschrieben <abbr title="beziehungsweise">bzw.</abbr> erweitert werden.

Bereits bestehende „Themes“ auf der „Whitelist“ für „GitHub–Pages“ erfüllen (nach meiner bescheidenen Ansicht) tatsächlich den „Tatbestand der Altbackenheit“ beziehungsweise schmerzen meine Augen bis zur Unerträglichkeit.

Bliebe also nur noch, ein eigenes Jekyll—Theme zu erstellen und als sogenannten „Ruby gem“ zu veröffentlichen. Das ist zwar auch nicht gerade Astrophysik, aber da müsste es doch auch einen Mittelweg geben. So dachte ich mir das — und ging gleich daran, es auszuprobieren.

Das Ergebnis liegt dem geschätzten Leser nun vor. „Minima“ wurde komplett außer Dienst gestellt, aber die sogenannte Codebase von Jekyll ist weiterhin (und großteils unverändert) intakt.

Was ich wirklich gemacht habe, ist die Importanweisung von „Minima“ (<code>@import "minima";</code>) aus dem „Stylesheet“ zu entfernen. Dadurch werden die Grundeinstellungen nicht mit geladen. Jekyll „glaubt“ nach wie vor (laut <code>config.yml</code>) „Minima“ zu verwenden, greift aber nicht auf die Werkseinstellungen zu.

Der Rest ergab sich durch meine eigenen Anweisungen im „Stylesheet“ und einige kleinere Anpassungen in verschiedenen „includes“ <abbr>bzw.</abbr> „layouts“. Das Ergebnis sind eine nur etwa 4,8 <abbr>KB</abbr> (statt ursprünglich etwa 11 <abbr>KB</abbr>) große <abbr>CSS</abbr>–Datei, eine deutlich verbesserte Zugänglichkeit und eine frischere, moderne Darstellung des Inhalts.

Ob diese Benutzeroberfläche den Geschmack der werten Leser trifft? Ich weiß es nicht. Schönheit liegt (bis zu einem gewissen Grad) immer im Auge des Betrachters. Jedenfalls kann ich sagen, sie hat mehr zu bieten als nur ein hübsches Gesicht.
