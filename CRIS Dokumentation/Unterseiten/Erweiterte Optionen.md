<h2>Individuelle Darstellung von Publikationen, Projekten und Forschungsbereichen</h2>
Mithilfe des Shortcodes <code>[[cris-custom] … [/cris-custom]]</code> lässt sich die Darstellung von Publikationen, Projekten, Forschungsbereichen (und allgemeinen Forschungsinformationen, siehe <a title="&quot;Automatische Synchronisierung&quot;" href="https://www.wordpress.rrze.fau.de/plugins/fau-cris/automatische-synchronisierung/">"Automatische Synchronisierung"</a>) in der Detailansicht individuell anpassen. Alle einzelnen Elemente stehen als Platzhalter zur Verfügung und können beliebig angeordnet und wie ganz normaler Text formatiert werden.
<h3>Beispiel:</h3>
Folgende Eingabe...
<pre>[[cris-custom show=projects project=100888]
<strong>#title#</strong>
Start: #start#
Ende: #end#
URL: &lt;a href="#url#"&gt;#url#&lt;/a&gt;
[/cris-custom]]</pre>
... erzeugt folgende Ansicht:
<div class="example">[cris-custom show=projects project=100888]
<strong>#title#</strong>
Start: #start#
Ende: #end#
URL: <a href="http://#url#">#url#</a>
[/cris-custom]</div>
[alert style="info"]Wichtig ist dabei, dass der Shortcode aus einem öffnenden (<code>[[cris-custom]</code>) und einen schließenden (<code>[/cris-custom]]</code>) Element besteht. Nur darin sind die einzelnen Elemente verfügbar.[/alert]

[notice-tipp title="Tipp"]Alle<strong> Sortier- und Filtermöglichkeiten </strong>des Standard-<code>[[cris]]</code>-Shortcodes sowie das<strong> Format der (Projekt-)Publikationen</strong> (Standard/APA/MLA) funktionieren auch in der Custom-Ausgabe.[/notice-tipp]
[collapsibles]
[collapse title="Platzhalter für Publikationen"]
<h3>Platzhalter für Publikationen:</h3>
<ul>
 	<li>#author#</li>
 	<li>#title#</li>
 	<li>#oaIcon# (Open-Access-Icon, wenn zutreffend)</li>
 	<li>#url#</li>
 	<li>#city#</li>
 	<li>#publisher#</li>
 	<li>#year#</li>
 	<li>#pubType#</li>
 	<li>#pubStatus#</li>
 	<li>#pagesTotal#</li>
 	<li>#pagesRange#</li>
 	<li>#lexiconColumn#</li>
 	<li>#volume#</li>
 	<li>#series#</li>
 	<li>#seriesNumber#</li>
 	<li>#ISBN#</li>
 	<li>#ISSN#</li>
 	<li>#DOI#</li>
 	<li>#URI#</li>
 	<li>#editors#</li>
 	<li>#bookTitle#</li>
 	<li>#journalTitle#</li>
 	<li>#eventTitle#</li>
 	<li>#eventLocation#</li>
 	<li>#eventStart#</li>
 	<li>#eventEnd#</li>
 	<li>#originalTitle#</li>
 	<li>#language#</li>
 	<li>#bibtexLink#</li>
 	<li>#subtype#</li>
 	<li>#articleNumber#</li>
 	<li>#projectTitle# (Projekt, zu dem diese Publikation erschienen ist)</li>
 	<li>#projectLink# (Projekttitel mit Link auf Projektseite)</li>
</ul>
[/collapse]
[collapse title="Platzhalter für Projekte"]
<h3>Platzhalter für Projekte</h3>
<ul>
 	<li>#title#</li>
 	<li>#type#</li>
 	<li>#parentprojecttitle#</li>
 	<li>#start#</li>
 	<li>#end#</li>
 	<li>#extend# (Datum der Laufzeitverlängerung)</li>
 	<li>#funding#</li>
 	<li>#url#</li>
 	<li>#acronym#</li>
 	<li>#description#</li>
 	<li>#leaders#</li>
 	<li>#members#</li>
 	<li>#publications#</li>
 	<li>#image1#, #image2#, #image3# (je nach dem, wie viele Bilder in CRIS hinterlegt sind)</li>
</ul>
[/collapse]
[collapse title="Platzhalter für Forschungsbereiche"]
<h3>Platzhalter für Forschungsbereiche</h3>
<ul>
 	<li>#title#</li>
 	<li>#description#</li>
 	<li>#persons#</li>
 	<li>#contactpersons#</li>
 	<li>#image1#, #image2#, #image3# (je nach dem, wie viele Bilder in CRIS hinterlegt sind)</li>
 	<li>#projects#</li>
 	<li>#publications#</li>
</ul>
[/collapse]
[collapse title="Platzhalter für die Seite 'Forschung'"]
<h3>Platzhalter für die Seite "Forschung"</h3>
<ul>
 	<li>#description#</li>
 	<li>#image1#, #image2#, #image3# (je nach dem, wie viele Bilder in CRIS hinterlegt sind)</li>
</ul>
[/collapse]

[collapse title="Platzhalter für Equipment"]
<h3>Platzhalter für Equipment</h3>
<ul>
 	<li>#name#</li>
 	<li>#description#</li>
 	<li>#image1#, #image2#, #image3# (je nach dem, wie viele Bilder in CRIS hinterlegt sind)</li>
 	<li>#manufacturer#</li>
 	<li>#model#</li>
 	<li>#constructionYear#</li>
 	<li>#location#</li>
 	<li>#url#</li>
 	<li>#year#</li>
 	<li>#funding#</li>
 	<li>#fields#</li>
 	<li>#projects#</li>
 	<li>#publications#</li>
</ul>
[/collapse]

[collapse title="Platzhalter für Standardisierungen"]
<h3>Platzhalter für Standardisierungen</h3>
<ul>
 	<li>#title#</li>
 	<li>#description#</li>
 	<li>#documentNumber#</li>
 	<li>#url#</li>
 	<li>#contributionTo#</li>
 	<li>#acceptedIn#</li>
 	<li>#committeeOrganization#</li>
 	<li>#committeeGroup#</li>
 	<li>#meetingStart#</li>
 	<li>#meetingEnd#</li>
 	<li>#meetingVenue#</li>
 	<li>#meetingHost#</li>
 	<li>#year#</li>
 	<li>#type#</li>
</ul>
[/collapse]
[/collapsibles]