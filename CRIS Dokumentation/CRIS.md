[alert color="#e5be01"]
[columns number="3"]
[column span="1"]
[divider]
<p style="text-align: center;">[icon icon="solid exclamation-triangle" style="5x"]</p>
[/column]
[column span="2"]

Derzeit bieten wir keinen Support und keine Weiterentwicklung des CRIS-Plugins an.
<strong>Der Support und die Weiterentwicklung wird vom CRIS-Team der FAU durchgeführt: cris-support@fau.de</strong>.
[/column]
[/columns]
[/alert]
<a href="https://www.wordpress.rrze.fau.de/files/2020/04/cris-schaubild.jpg"><img class="size-full wp-image-20477" src="https://www.wordpress.rrze.fau.de/files/2020/04/cris-schaubild.jpg" alt="CRIS Übersicht" width="2000" height="1125" /></a>
<h2>Daten aus dem FAU-Forschungsinformationssystem CRIS in den Webauftritt einbinden</h2>
Das Plugin bindet Daten aus dem FAU Forschungsinformationssystem CRIS (<a href="http://cris.fau.de">cris.fau.de</a>) in die Webseite ein. Die Einbindung funktioniert über einen Shortcode, über den sich verschiedene Ausgabeformen einstellen lassen.
<h3>Shortcodes</h3>
[alert style="info"]
Bei einigen Shortcode-Parametern können Sie IDs von einzelnen Organisationseinheiten, Personen oder Forschungsleistungen eingeben. Diese lesen Sie aus der URL aus, wenn Sie die gewünschte Organisationseinheit, Person oder Forschungsleistung auf cris.fau.de anzeigen lassen:
z.B. https://cris.fau.de/converis/portal/Organisation/<strong><em>141517</em></strong>...
oder https://cris.fau.de/converis/portal/Person/<strong><em>123456</em></strong>...
bzw. https://cris.fau.de/converis/portal/Award/<em><strong>123456</strong></em>...

[/alert]
[collapsibles]
[collapse title="Unterstützte Forschungsleistungen"]
Aktuell werden folgende in CRIS erfasste Forschungsleistungen unterstützt:
<ul>
 	<li>Publikationen</li>
 	<li>Auszeichnungen</li>
 	<li>Projekte</li>
 	<li>Patente</li>
 	<li>Forschungsaktivitäten</li>
 	<li>Forschungsbereiche</li>
 	<li>Equipment</li>
 	<li>Standardisierungen</li>
</ul>
Über den Shortcode lassen sich jeweils verschiedene Ausgabeformate einstellen.
[/collapse]
[collapse title="Shortcodes"]

[notice-tipp title="Neu: Idm-Kennung und FAU.ORG-Nummern"]
Statt der von CRIS vergebenen IDs für Personen (s.o.) können ab sofort auch IdM-Kennungen verwendet werden (<code>persID="ab12cdef"</code>). Statt der CRIS-eigenen Organisations-IDs funktionieren nun auch FAU.ORG-Nummern.
[/notice-tipp]
<ul>
 	<li>Publikationsliste (automatisch nach Jahren gegliedert):
<code>[[cris show="publications"]]</code></li>
 	<li>Auszeichnungen (automatisch nach Jahren sortiert):
<code>[[cris show="awards"]]</code></li>
 	<li>Forschungsprojekte (automatisch nach Jahren sortiert):
<code>[[cris show="projects"]]</code></li>
 	<li>Patente:
<code>[[cris show="patents"]]</code></li>
 	<li>Forschungsaktivitäten:
<code>[[cris show="activities"]]</code></li>
 	<li>Forschungsbereiche:
<code>[[cris show="fields"]]</code></li>
 	<li>Equipment:
<code>[[cris show="equipment"]]</code></li>
 	<li>Standardisierungen:
<code>[[cris show="standardizations"]]</code></li>
</ul>
[/collapse]
[/collapsibles]
<h2>Mögliche Zusatzoptionen</h2>
[collapsibles]
[collapse title="ID Überschreiben"]
<h3>ID überschreiben</h3>
Grundsätzlich werden die Ergebnisse für die in den Einstellungen festgelegte CRIS-ID ausgegeben. Diese kann jedoch überschrieben werden, entweder durch die ID einer anderen Organisationseinheit, oder durch die ID einer einzelnen Person.
<ul>
 	<li><code>orgID="123456"</code> für eine von den Einstellungen abweichende Organisations-ID. Sie können auch mehrere Organisations-IDs angeben, durch Komma getrennt: <b>orgID="123456,987654"</b>.</li>
 	<li><code>persID="123456"</code> für die Einträge zu einer konkreten Person. Auch hier sind mehrere IDs möglich.</li>
</ul>
[notice-tipp]Ergebnisse in Bezug zu anderen Entitäten (z.B. alle Publikationen eines Forschungsbereichs) werden über den Shortcode <code>cris-custom</code> ausgegeben:[/notice-tipp]
<pre>[[cris-custom show="fields" field="123456"]
#publications#
[/cris-custom]]</pre>
Genauere Informationen dazu finden Sie auf der Seite <a href="https://www.wordpress.rrze.fau.de/plugins/fau-cris/erweiterte-optionen/">Erweiterte Optionen</a>.
[/collapse]
[collapse title="Gliederung"]
<h3>Gliederung</h3>
<ul>
 	<li><code>orderby="year"</code>: Liste nach Jahren absteigend gegliedert (Voreinstellung bei Publikationen)</li>
 	<li><code>orderby="type"</code>: Liste nach Publikations- bzw. Auszeichnungs-(etc.)typen gegliedert. Die Reihenfolge der kann in den Einstellungen nach Belieben festgelegt werden.</li>
 	<li><code>orderby="subtype"</code>: Liste nach Publikations-Subtypen gegliedert.</li>
 	<li>Bei Publikationen sind zwei Gliederungsebenen möglich:
<ul>
 	<li><code>orderby="year, type"</code></li>
 	<li><code>orderby="type, year"</code></li>
 	<li><code>orderby="type, subtype"</code></li>
</ul>
</li>
 	<li><code>orderby="role"</code> (nur bei Projekten einer Person): Gliederung nach „Projektleitung“ und „Projektmitarbeit“</li>
</ul>
[/collapse]
[collapse title="Filter"]
<h3>Filter</h3>
<ul>
 	<li><code>year="2015"</code>: Nur Einträge aus einem bestimmten Jahr</li>
 	<li><code>start="2000"</code>: Nur Einträge ab einem bestimmten Jahr</li>
 	<li><code>end="2010"</code>: Nur Einträge bis zu einem bestimmten Jahr</li>
 	<li><code>type="…"</code>: Es werden nur Einträge eines bestimmten Typs angezeigt. Die korrekten Filterparameter finden Sie auf der Seite <a href="https://www.wordpress.rrze.fau.de/plugins/fau-cris/typen-filter/">"Typen-Filter"</a>.</li>
 	<li><code>subtype="…"</code> Subtyp einzelner Publikationstypen. Die korrekten Filterparameter finden Sie auf der Seite <a href="https://www.wordpress.rrze.fau.de/plugins/fau-cris/typen-filter/#subtypen">"Typen-Filter"</a>.</li>
 	<li><code>publication="12345678"</code>: Nur eine einzelne Publikation (hier die CRIS-ID der Publikation angeben)</li>
 	<li><code>fau="1"</code> (nur bei Publikationen): Nur FAU-Publikationen anzeigen (0 = nur Publikationen anzeigen, die nicht an der FAU entstanden; keine Angabe = alle Publikationen anzeigen)</li>
 	<li><code>peerreviewed="1"</code> (nur bei Publikationen): Nur entsprechend begutachtete Publikationen anzeigen (0 = nur nicht begutachtete Publikationen anzeigen; keine Angabe = alle Publikationen anzeigen)</li>
 	<li><code>notable="1"</code> (nur bei Publikationen): Die wichtigsten Publikationen einer Person anzeigen.</li>
 	<li><code>language="…"</code> (nur bei Publikationen): Nur Publikationen in einer oder mehreren bestimmten Sprachen anzeigen. Nach folgenden Sprachen kann gefiltert werden: German, English, Arabic, Chinese, Danish, Finnish, French, Greek, Italian, Japanese, Latin, Dutch, Norwegian, Polish, Portuguese, Russian, Swedish, Slovak, Slovenian, Spanish, Czech, Turkish, Ukrainian.</li>
 	<li>Die Publikationen <em>innerhalb eines Forschungsbereichs oder Projektes</em> filtern Sie analog mit den Attributen <code>publications_year</code>, <code>publications_start</code>, <code>publications_type</code>, <code>publications_subtype</code>, <code>publications_fau</code>, <code>publications_peerreviewed</code>, <code>publications_orderby</code>, <code>publications_notable</code>.</li>
 	<li><code>awardnameid="123"</code>: Nur eine einzelne Auszeichnung (hier die CRIS-ID der Auszeichnung angeben)</li>
 	<li><code>award="12345678"</code>: Nur eine einzelne Auszeichnung (hier die CRIS-ID der Auszeichnung angeben).
Hinweis zum Unterschied zwischen awardnameid und award: <b>awardnameid</b> bedeutet die ID eines Preises, der normalerweise mehrfach vergeben wird, z.B. der "Gottfried-Wilhelm-Leibniz-Preis". <b>award</b> (bzw. dessen ID) bedeutet die konkrete, einmalige Verleihung dieses Preises an eine bestimmte Person.</li>
 	<li><code>project="123456"</code>: Nur ein einzelnes Projekt. Hier ist die Ausgabe ausführlicher, u.a. mit Nennung der Projektbeteiligen (Projektleiter und -mitarbeiter) und einer Liste der dazugehörigen Publikationen.</li>
 	<li><code>status="current"</code> bzw. <code>completed</code> oder <code>future</code> (nur bei Projekten): Nur aktuell laufende bzw. abgeschlossene oder zukünftige Projekte anzeigen.</li>
 	<li><code>role="leader"</code> bzw. <code>role="member"</code>(nur bei Projekten einer Person): Nur Projekte anzeigen, bei denen die Person Projektleiter bzw. Projektmitarbeiter ist/war.</li>
 	<li><code>standardization="12345678"</code>: Nur eine einzelne Standardisierung (hier die CRIS-ID der Standardisierung angeben). Auch mehrere IDs, per Komma getrennt, sind möglich.</li>
 	<li><code>items="5"</code>: Nur die ersten 5 Publikationen anzeigen. In dem Fall werden "orderby"-Parameter ignoriert – es wird eine nicht gegliederte Liste ausgegeben.</li>
 	<li>Filter lassen sich auch kombinieren: z.B. <code>year="2014" type="buecher"</code> (= alle Bücher aus dem Jahr 2014)</li>
</ul>
[/collapse]
[collapse title="Darstellung"]
<h3>Darstellung</h3>
[accordion]
[accordion-item title="Darstellung"]
<ul>
 	<li><code>format="accordion"</code>: gegliederte Listen (z.B. orderby="year") werden als <a href="https://www.wordpress.rrze.fau.de/redaktion/accordion/">Accordions</a> ausgegeben (Standard wären sonst Zwischenüberschriften).</li>
 	<li><code>display_language="en"</code> bzw. <code>display_language="de"</code>: Sprache der Ausgabe abweichend von der eingestellten Hauptsprache der Website oder Seite.</li>
</ul>
[/accordion-item]
[accordion-item title="Publikationen"]
<h4>Publikationen</h4>
<ul>
 	<li><code>quotation="apa"</code> bzw. <code>quotation="mla"</code>: Ausgabe im Zitationsstil APA bzw. MLA</li>
 	<li><code>sortby="created"</code> bzw. <code>sortby="updated"</code>: Standardmäßig werden die Publikationen nach ihrem Veröffentlichungsdatum sortiert. Alternativ dazu kann man mit diesem Attribut eine Sortierung nach Erstellung oder letzter Bearbeitung in CRIS wählen.</li>
 	<li><code>display="no-list"</code>: Darstellung ohne Listenpunkte</li>
 	<li><code>showimage="1"</code>: Wenn vorhanden, Bild der Publikation anzeigen</li>
 	<li><code>image_align="right"</code> bzw. <code>image_align="left"</code>: Bild rechts oder links vom Text ausgeben (Standard: rechts)</li>
 	<li><code>publications_orderby="year"</code>: Sortierung nach Veröffentlichungsjahr</li>
 	<li><code>publications_format="accordion"</code>: Darstellung als Accordion</li>
</ul>
[/accordion-item]
[accordion-item title="Auszeichnungen"]
<h4>Auszeichnungen</h4>
<div class="example">[cris show="awards" awardnameid="136844017" display="gallery"]</div>
<h5>Shortcode</h5>
<div class="example"><code>[[cris show="awards"]]</code></div>
<h5>Modifikationen</h5>
<ul>
 	<li><code>display="gallery"</code>: Bildergalerie mit Bild des Preisträgers und Angaben zum Preis</li>
 	<li><code>showname=0</code>: Der Name des Preisträgers wird nicht angezeigt. Das kann z.B. bei Darstellungen auf einer Personenprofilseite sinnvoll sein.</li>
 	<li><code>showyear=0</code>: Die Jahreszahl wird nicht angezeigt (z.B. für eine nach Jahren gegliederten Ansicht).</li>
 	<li><code>showawardname=0</code>: Der Name der Auszeichnung wird nicht angezeigt (z.B. bei der Ausgabe awardnameid=123).</li>
</ul>
[/accordion-item]
[accordion-item title="Projekte"]
<h4>Projekte</h4>
<ul>
 	<li><code>hide="details, abstract, publications, end"</code>: Ein oder mehrere Elemente können ausgeblendet werden.</li>
 	<li><code>quotation="apa"</code> bzw. <code>quotation="mla"</code>: Ausgabe der Projekt-Publikationen im Zitationsstil APA bzw. MLA</li>
</ul>
<h4>Forschungsbereiche</h4>
<ul>
 	<li><code>quotation="apa"</code> bzw. <code>quotation="mla"</code>: Ausgabe der Publikationen im Zitationsstil APA bzw. MLA</li>
</ul>
[/accordion-item]
[accordion-item title="Equipment"]
<h4>Equipment</h4>
<ul>
 	<li><code>manufacturer</code> Nur Forschungsequipment eines bestimmten Herstellers anzeigen</li>
 	<li><code>constructionyear</code> Forschungsequipment aus einem bestimmten Herstellungsjahr anzeigen</li>
 	<li><code>constructionyearstart</code> Forschungsequipment ab einem bestimmten Herstellungsjahr anzeigen</li>
 	<li><code>constructionyearend</code> Forschungsequipment bis zu einem bestimmten Herstellungsjahr anzeigen</li>
 	<li><code>location</code> Forschungsequipment an einem bestimmten Standort</li>
 	<li><code>hide="name, description, image, details, manufacturer, model, constructionYear, location, url, year, funding, fields, projects"</code> Versteckt den angegebenen Inhalt</li>
</ul>
[/accordion-item]
[accordion-item title="Forschungsbereiche"]
<h4>Forschungsbereiche (Fields)</h4>
<ul>
 	<li><code>hide="title, projects, contactpersons, persons, publications"</code>Versteckt den angegebenen Inhalt</li>
</ul>
[/accordion-item]

[accordion-item title="Forschungsaktivitäten"]
<h3>Forschungsaktivitäten</h3>
<ul>
 	<li><code>hide="type"</code>: Typ der Forschungsaktivität ausblenden</li>
</ul>
<h4>Forschungsinfrastruktur</h4>
<ul>
 	<li><code>hide="name, description, image, details, manufacturer, model, constructionYear, location, url, year, funding, fields, projects"</code>: In der Einzelansicht können ein oder mehrere Elemente ausgeblendet werden.</li>
 	<li><code>quotation="apa"</code> bzw. <code>quotation="mla"</code>: Ausgabe der Projekt-Publikationen im Zitationsstil APA bzw. MLA</li>
</ul>
[/accordion-item]
[accordion-item title="Standardisierungen"]
<h3>Standardisierungen</h3>
<ul>
 	<li><code>hide="title, description, type, documentNumber, url, contributionTo, acceptedIn, authors, organization, group, date, host, venue"</code>: Blendet die angegebenen Inhalte aus.</li>
 	<li><code>hide="details"</code>: Blendet documentNumber, url, contributionTo, acceptedIn und authors aus</li>
 	<li><code>hide="committee"</code>: Blendet organization und group aus</li>
 	<li><code>hide="meeting"</code>: Blendet date, host und venue aus</li>
 	<li><code>display="no-list"</code>: Darstellung ohne Listenpunkte</li>
</ul>
[/accordion-item]
[/accordion]
[/collapse]
[/collapsibles]
<h2>Beispiele</h2>
Die Daten lassen sich gliedern und/oder filtern:
<code>[[cris show="publications" type="buecher"]]</code> =&gt; Alle Bücher
<code>[[cris show="publications" year="2015"]]</code> =&gt; Alle Publikationen aus dem Jahr 2015
<code>[[cris show="publications" persID="123456" year="2000" orderby="pubtype"]]</code> =&gt; Alle Publikationen der Person mit der CRIS-ID 123456 aus dem Jahr 2000, nach Publikationstypen gegliedert
<h2><a id="fau-person"></a>Integration "FAU Person"</h2>
Wenn Sie das <a href="https://github.com/RRZE-Webteam/fau-person">FAU-Person-Plugin</a> verwenden, können Autoren aus der Publikationsliste mit ihrer FAU-Person-Kontaktseite verlinkt werden.

Wenn diese Option in den Einstellungen des CRIS-Plugins aktiviert ist, überprüft das Plugin selbstständig, welche Personen vorhanden sind und setzt die entsprechenden Links.
<h2>Github</h2>
[button link="https://github.com/RRZE-Webteam/fau-cris"]Zur Github-Seite des Plugins[/button]
[button link="https://github.com/RRZE-Webteam/fau-cris/issues"]Zu den Github Issues des Plugins[/button]